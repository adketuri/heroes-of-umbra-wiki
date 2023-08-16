---
title: Version History
description: All the changelogs
published: true
date: 2023-08-16T18:11:22.518Z
tags: 
editor: markdown
dateCreated: 2023-03-18T17:09:04.395Z
---

# 1.3.2
* Added jump gems for armor + accessories.
* Rebalanced Summoner a bit
  * Storm damage scaled back a bit
  * Offensive summon fireball damage reduced
* Drops that fall off a map/land in lava automatically respawn above the player (experimental)
* Fixed bugs as a result of the storage revamp
  * Wrong character slot would reload opening storage
  * Adding gems to gear got weird sometimes
  
# 1.3.1
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