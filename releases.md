---
title: Version History
description: All the changelogs
published: true
date: 2024-06-20T00:27:53.954Z
tags: 
editor: markdown
dateCreated: 2023-03-18T17:09:04.395Z
---

# 1.4.0 (Beta)
* Overhaul all the game libraries
	* Upgrade desktop to LWJGL3
  * Update controller library
  * Remove OUYA support (RIP)
* Launch on Android and iOS
* Players can synchronize save data with dreamstone.
* Players can create their own servers
	* Steam networking has been killed
* Add multicast 
	* CSPD over 100 has a chance to cast multiple copies of certain magic-based skills.
* Add support for refresh rates other than 60fps
* Add camera smoothing
* Minor tweaks
	* Bump quest item drop rate from 20% to 25%
  * Throttle game saves when repeatedly opening/closing the menu
  * Correctly render skill hotkeys on mobile
  * Adjust network player interpolation: other players' jumps should feel less jittery
  * Redo moving platform network sync
* Skill Changes
* Orb Changes
	* Orb of Strike now has a chance to auto-cast strike when attacking
* Bugfixes
	* Invalid items no longer load from player data
	* Fix missing hair for male hair 10 during cast
  * Fix stretching sprites when a character blinks during a cutscene's pose change 
  
## 1.3.11
* Add back missing platforms on Onyx Keep boss map
* Change Summons so their time depletes faster in water
* Fix issues updating characters from ancient save versions (pre-1.2.0)
* Fix a visual issue with the max level of deluxe gems.
* Change internal representation of currencies, display them all in the menu.
   * Note this imposes some currency caps for the health of the game: 999m flips, 9k shards, 999 scraps, 999 essence.
* Include a new secret costume in the Orb Garden bonus boss gem vendor. 
* Add [aspd modifiers](/mechanics/weapon-modifiers) to weapon types
   * In practice this means more aspd is needed to cap swing speed for non-daggers
* Add [mastery multipliers](/mechanics/weapon-modifiers) to weapon types
   * This means certain weapon types get percentage damage boosts. 
* Fix a bug where position updates weren't sent to the server when the main menu was open
* Fix the yeti skips for real
* Refactor skills and hotkeys to be player-specific, instead of static.
   * This fixes an issue where creating a character wipes your previous characters' skills
* Include a new beach area
   * New enemy: [Jellyfish](/monsters/jellyfish)
   * New items, simple quest.
* Orb changes
   * Orb of Blitz now consumes all EP, dealing boosted damage per extra EP spent
* Correct an off-by-one error when calculating the primary skill tree
* Add blinking animation to characters 
* Hide exp needed at level 99.
* Warrior skill changes
  * Cyclone slightly nerfed (-15% damage)
  * Earthquake damage slightly boosted (roughly +30%)
  * Blitz rank scaling slightly reduced (rank 9 damage is equivalent)

## 1.3.10
* Allow skills to be cast while Leap is active
* Auto-scroll long descriptions in inventory/upgrade menus
* Correct aspd health scaling oversight for Leech
   * This nerfs the healing received at extremely high attack speeds, to accommodate the aspd refactor done as part of 1.3.0
* Add versioning to created items/players
   * This has no player impact, but allows the game to support things like seasonal content in the future
* Correct an oversight that prevented Master from using one of his skills.
* Decay success rate of Deluxe Gems by 2% per rank, down to a minimum of 1% success rate
   * This makes leveling your blacksmith relevant again!

## 1.3.9
* Add a new item, [Garden Tranquility](/items/garden-tranquility), which adds 4 minutes to the current garden run. Find it from the Orb Garden
* Implement a new `/what` command which tells you any missing steps needed to complete rebirth
* Swap the "Dungeons Completed" data on save profiles to use local player data, instead of the server slot data.
* Add a missing key when using [Essence Node](/items/essence-node).
* Change Master minion spawn rate from 60s to 30s
* Disable autoscrolling on Android

## 1.3.8
* Fix a crash rejoining games

## 1.3.7
* Fix a crash when entering certain Orb Gardens
* Allow Orb Garden entrances to spawn on more tile types
* Sync bonuses immediately after beating the boss
   * This should prevent a race condition in which you beat the boss and get sent out before the next server update
* Store bosses defeated in player data
* Rewrite Android touch conversion to work a little nicer on wider devices
   * If things still feel off there's a new command `/debugtouch` to debug this if you're on Android.

## 1.3.6
* Fix a crash when loading the game on android or opening storage
* Reduce the shard cost of all orb garden npcs by ~15-20%
* Cut the cost of [Tome of Gardens](/items/tome-of-gardens)  roughly in half.
* Extend collisions past the top of the map
* Fix a crash changing to non-English locales
* Lower the sell value of Tier2/3 gear
* Clean up upgrading, hopefully no more slots vanishing
* Fix [Slash Commands](/mechanics/slash-commands) to send chat messages

## 1.3.5
* Prevent an occasional crash with overspawning enemies in gardens.
* Handle transforming gear better, so item attributes aren't sometimes lost.
* Swap some confusing text on upgrading orbs
* Scale back stats on the randomized gear a bit.

## 1.3.4
* Persist map seeds to enable saving bonus data
* Adjust [Tome of Gardens](/items/tome-of-gardens) to gradually decay in success rate. Past rank 100 it can't be used to raise orb ranks.
  * This is to encourage running gardens instead of farming items to reach higher orb/prestige levels.
* Require all bosses/cutscenes to be watched before a character can rebirth.

## 1.3.3
* Prevent a softlock when attempting to upgrade gems with no upgradable attributes
* Persist companion egg lock state when summoning/dismissing companions.
* Fix another issue with seconds played copying to other save slots
* Allow moving by page in the storage menu with left/right keys.
* Reduce the variance in orb garden sizes and bump down the size scaling based on orb rank slightly.
* Force equipment drops to 9 slots and scale random stat rolls based on orb rank. (Rebirth-mode only.)
* Fix a longstanding bug with collisions where sometimes enemies would get hit multiple times when they shouldn't.
	* Related, the Weapon Toss collision is a lot better. It hits a max of two times more consistently.
  * This technically nerfs builds that rely on certain skills like fireball, against bosses. I may revisit certain damage formulas in the future -- let me know what you think.

## 1.3.2
* Added jump gems for armor + accessories.
* Rebalanced Summoner a bit
  * Storm damage scaled back a bit
  * Offensive summon fireball damage reduced
* Drops that fall off a map/land in lava automatically respawn above the player (experimental)
* Fixed bugs as a result of the storage revamp
  * Wrong character slot would reload opening storage
  * Adding gems to gear got weird sometimes
  
## 1.3.1
* Merge with the obsolete android branch
  * This adds back the CashmereCat cap and jump frames from 1.2.9.
* More robust save data/storage tweaks
* Orb of Weapon Toss makes weapon toss spammable
* Fix Medusa poison damage formula from going negative at lower levels
* Boost the max number of chests in Gardens.

# 1.3.0
## New Dungeon: Onyx Keep
* The [Onyx Keep](/dungeons/onyx-keep) is a new dungeon intended for rebirth players.
* It requires a consumable item found somewhere in the [Orb Gardens](/dungeons/orb-gardens)

## New Skill Tree: Summoner
* Summon creatures to aid in combat and provide helpful auras to allies in battle.
* View the [Summoner](/skills/summoner) to learn more.

## Prestige Levels
* Upon completing a rebirth playthrough, you may rebirth again, exchanging any [Orb Ranks](/stats/orb-rank) for permanent skills.
* Learning these skills increases your [Prestige Level](/stats/prestige-level).

## Orb Garden Improvements
* Significantly revamped the [Orb Gardens](/dungeons/orb-gardens) progression
	* Maze size increases and monster changes are more gradual
  * Tweaked medusa/snake exp.
* Added several new chunk variants (more map variety).
* Orb rank is deducted when you first enter the garden, not when you run out of time. 
* New vendor with a unique bartering system to obtain rare items.
* Mystery gems acquired in gardens now have tiers.
  * Higher tiered gems have higher max levels and slightly better stats.
  * Higher ranking gardens will drop higher tiered gems.
* Additional tiers of equipment can be unlocked by reaching higher leveled ranks
* Added a gem shard trader in the boss room.
* Included map variants: Purgatory, Fields, and more.
* Fixed a bug where only up to 30 chests would spawn in the gardens.
* Fixed a bug where some mazes would be unsolveable. (oops teehee)


## Orb Leveling Changes
* Cards cannot be sold for essence
* Orbs destroyed will give essence equal to their level
* The full amount must be paid upfront to level an orb, instead of 1 essence at a time. (This makes it easier to see at a glance if you have enough essence to level up an orb.)

## Balancing Changes
* The exp curve got an overhaul. 
	* Every level takes a flat 20% more exp (rebirth and normal). 
  * Rebirth compounded exp needed per rank reduced from +30% to +25%.
* Attack speed is nerfed slightly
  * Dagger mastery now gives attack speed instead of damage
  * This is primarily to balance swords vs daggers, and keep the playstyles distinct. Attack speed in general is very powerful and easy to max. These changes should require a bit more specialization.
* Crit past 100 gives a chance to deal Perfect Critical hits.
  * These have a new animation/sound effect and deal boosted damage.

## Other Features and Additions
* Items can be locked to prevent accidental selling/dropping.
* Added many more [Orbs](item-types/orb)
* Rare items now have an aura/ping sound that plays when they're dropped
* Summoned companions no longer need to be resummoned upon exiting/reloading a character.
* Chests sparkle ✨
* Many effect animations got a bit larger: impact/jump/cast
* Many drop icons have been updated
* Players can send emoticons to other players via [Slash Commands](slash-commands).

## Bugfixes
* Weapon mastery wasn't working correctly with endure.
* Stat points no longer go crazy with multiple rebirths.
* Unopened gates no longer automatically open when relaunching the client.
* Storage items no longer duplicate in specific circumstances.
* Generating new mystery gear/gems now checks if you have enough inventory space, to prevent possibly losing gear.

# 1.2.0
[Steam Update](https://store.steampowered.com/news/app/645380/view/2082293429517118669)
* New skill tree: Ranged
* New environment: Sunglade Highlands
* Stackable items
* Dramatically reduced load times
* New HP% and Crit Damage% attributes on some gear/gems
* More performant minimaps, colorized world map
* Polish platforms, add bird effect to the beach

# 1.1.26
* Initial steam release