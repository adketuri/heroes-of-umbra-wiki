---
title: Cast Time
description: How cast time is calculated
published: true
date: 2023-09-04T19:38:59.092Z
tags: mechanics
editor: markdown
dateCreated: 2023-09-04T19:38:59.092Z
---

# Cast Speed
Skills have a base cast time of 0.5 seconds. 
* If Haste is applied, that gets halved
* If Tech Bracers is learned (any rank), the cast time is reduced by 20% (multiplicative).
* The final cast time after applying Haste + Tech Bracers modifiers is reduced by 0.5% per point of cspd.

## Example
* Haste + Tech Bracers
* `0.5 * 0.5 * 0.8 = 0.2 seconds` 
* Haste + Tech Bracers + 50 cspd
* `0.2 - (0.2 * 50 / 200) = 0.15 seconds` 

## Notes
There is a hard cap of 0.05 seconds to cast a skill. Cast time cannot go under this value.