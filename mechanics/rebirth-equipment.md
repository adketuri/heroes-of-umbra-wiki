---
title: Rebirth Equipment
description: Stat generation for equipment dropped from enemies/chests in Rebirth Mode
published: true
date: 2023-08-21T06:17:49.733Z
tags: mechanics, equipment, rebirth
editor: markdown
dateCreated: 2023-08-21T06:13:38.777Z
---

Equipment looted from enemies in Rebirth Mode have boosted attributes based on the player's current Orb Rank. The purpose of looted gear is to act as a bridge between unlocking Tier 2/3 Rebirth Shop gear, provide alternate paths of power, and keep looted gear somewhat relevant for early-rank orb gardens.

Depending on rank, a character will get 2-4 attribute rolls, each of which are applied to one of the equipment's existing attributes. The boost amount is also dependent on that character's rank.

# Boost Amount
A boost amount is based on the attribute's existing base value, calculated as 25% of the base value plus ten. That boost amount is scaled by the player's rank, plus 0.5% per rank up to rank 100. In essence, for each existing stat we calculate that stat's boost amount.

```
base = stat / 4 + 10
boost = base + base * min(rank, 100) / 200
```

For example, [Deathfalchion](/items/deathfalchion) has 60 base attack. It's attack boost value would be 25 at rank 0 and 37 at rank 100 and beyond. Each attribute gets its own boost value.

# Attribute Rolls
Once the boost amounts are calculated, an existing attribute on the equipment is chosen at random and increased based on its base value. This is repeated for a certain number of rolls. The number of rolls is calculated as 2 plus the player's rank divided by 35.

```
rolls = 2 + min(rank, 100) / 35
```

Continuing the Deathfalchion example, assuming rank 100 we get 4 total rolls. The boost amount is 37 attack with a base attribute of 60 attack, so a theoretical max attack on this weapon is 208. (`60 + 37 * 4`). Since Deathfalchion has two attributes (attack and crit) the probability of a Deathfalchion drop having max attack is 1/16. 

# Changes
* Prior to 1.3.5, Boost amount was +1% per rank and the max number of rolls was 6.