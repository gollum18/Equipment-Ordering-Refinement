# Equipment Ordering and Refinement
A mod for Skyrim SE with the goal of allowing players to custom order and refine equipment at a unique blacksmith vendor. The goal of this mod is to provide an alternative to the Blacksmithing skill.


## Goals
- [X] Compute costs for every piece of equipment craftable by the vendor.
- [X] Renovate Falion's house for blacksmithing.
- [X] Implement equipment cost in-game.
- [X] Write quests for the vendor to unlock special equipment crafting and refinement.
- [X] Write dialogue for the vendor/player interaction.
- [ ] Record the dialogue for the vendor.
- [X] Design and implement the vendors' skills and appearance.
- [X] Implement the quests in-game and tie them to the vendors skill/perk progression.
- [X] Implement dialogue system for equipment crafting.
- [ ] Implement dialogue system for equipment refining.
- [X] Implement an appropriate schedule.
- [ ] Implement passive dialogue for the vendor to converse with the player while idling. 
- [ ] Implement relocation to player owned houses. House must have a smithy and forge on premises.


## Motivation
You may ask: "Why would I need this mod if the blacksmithing skill exists?" or "What is the point of the blacksmithing skill with this mod installed?" 


Back in the ye-olden days of Oldrim when the game first launched, blacksmithing was a viable skill to level up out of the gate (without glitching the game). This was primarily because of two features of Oldrim:
1. Blacksmithing in Oldrim did not possess a diminishing return curve on smithed items and equipment meaning it was entirely possible to level the skill to 100 by just crafting Iron Daggers through slight time investment.
2. The most abundant ore type in Skyrim is iron ore. The only other ore type in Skyrim that is even remotely close to it's abundance is ebony ore, which the player cannot utilize in smithing until they are nearly finished leveling the skill.


Sometime around patch 1.5 for Oldrim, Bethesda decided to do away with static levelling of the Blacksmithing skill and added a diminishing return curve for blacksmithing xp from items and equipment. The intent was obviously to make it feel more rewarding and prevent players from spamming their way to the best equipment as soon as they start the game (usually well before said equipment was available as levelled loot or from vendors). This single change made the blacksmithing skill far more expensive and time-consuming, akin to the same skill in a game like World of Warcraft. Outside of iron ore and ebony ore, the other types of ore are far more precious and rare in the Skyrim game world. Levelling the blacksmithing skill in an updated version of Oldrim or Skyrim SE thus requires purchasing raw materials from vendors at a much higher cost than what was realizable before the patch.


This mod seeks to balance this change by introducing a feature I've always wanted in the game and a feature that it seems Bethesda wanted as well considering the voice acting of the blacksmith vendors: equipment ordering and refinement. Initially, I wanted to create a mod that allows all blacksmith vendors in the base game and its' DLC to craft and refine equipment for the Dragonborn based on their smithing level, but I realized that such a mod was too much work for what I wanted to accomplish and was not really unique enough to differentiate this mod from mods that attempt to introduce similar concepts to Skyrim SE. Instead, this mod introduces a unique blacksmith vendor in Morthal as well as several quests that unlock the ability for the blacksmith vendor to craft higher tier equipment.


The prices for crafting equipment are a combination of the equipments' base cost, cost of materials, and labor. Higher tier equipment will naturally cost more as a result. Note that the end price cost is not affected by the Dragonborns speech skill as the worldy travels of this vendor have ensured they have the gift of gab and are a Master in the speech skill.


## Overview
This mod introduces a unique blacksmith vendor in Morthal (located at the Morthal barracks). In addition to having the roles and responsibilities of a traditional blacksmith vendor, this vendor can also craft and refine equipment for the dragonborn for a nominal fee. This vendor starts as an Expert in smithing with a smithing level of 75. Initially, this blacksmith can craft any armor up to Glass equipment for the light equipment side of the smithing tree, and Orcish equipment for the heavy equipment side of the tree. By completing a series of unique quests for the blacksmith, you raise their smithing level to 80, 90, and 100 and unlock the ability for the blacksmith to craft Ebony, Daedric, and Dragon equipment respectively.


This vendor has extensive experience working with the Dunmer people of Morrowind at Mournhold and is fully-versed in the arts of crafting Chitin and Bonemold equipment. However, this vendor has no experience working with the equipment unique to the people of Solstheim. You will need to complete a series of quests to fully unlock the ability for this vendor to craft Nordic Carved equipment and Stalhrim equipment. Historically, the Skaal are reluctant to trust outsiders. It may take some effort on your part to have them part with this knowledge. Likewise, because Improved Bonemold Armor originated on Solstheim, the vendor does not know how to craft it. You must complete the quest "Paid in Full" to learn the formula yourself. You must then offer to teach the vendor how to craft the armor using a dialogue option before they are able to craft it for you.


Equipment cost is based on three factors: base cost, materials cost, labor cost. The base cost and materials cost either come directly from the Creation Kit or are computed from values taken from the Creation Kit so they are based on Skyrims' economy. The labor cost was generated by hand and is what I feel is appropriate per the amount of labor required for each type of equipment. This was added onto the final cost to simulate what a real-life craftsmen would charge for the time and service provided to you. The labor costs break down as follows:


| Category          | Labor Cost of Category |
|-------------------|------------------------|
| Armor             | 250                    |
| Boots             | 50                     |
| Gauntlets/Bracers | 50                     |
| Helmet            | 100                    |
| Shield            | 150                    |
| 1H Weapons        | 150                    |
| 2H Weapons        | 200                    |
| Ammo              | 25                     |


Please see the Blacksmiths SE excel data sheet for the actual cost of each piece of equipment relative to its' base cost, materials cost and labor cost.


## Quests
There are five quests unique to the vendor introduced by this mod **WIP**:
1. ***Mastery of the Ancients*** - Raises the vendors' smithing level to 80 and allows them to craft Ebony equipment and refine it to Legendary quality.
2. ***Mastery of the Daedra*** - Raises the vendors' smithing level to 90 and allows them to craft Daedric equipment and refine it to Legendary quality.
3. ***Mastery of the Dragons*** - Raises the vendors' smithing level to 100 and allows them to craft Dragonplate, Dragonscale, and Dragonbone equipment and refine them to legendary quality.
4. ***Mastery of the Arcane*** - Allows the vendor to refine Daedric artifacts and unique equipment to Legendary level. By comparison, the Dragonborn can only refined Daedric artifacts and most unique equipment to Flawless quality as the smithing requirements needed to refine higher are usually higher than the max smithing level attainable in-game.
5. ***Mastery of the Flames*** - Allows the vendor to refine to Mastercrafted level. Mastercrafted equipment is stronger than Legendary equipment and is intended for very late game (i.e. level 50+). As such, this quest is planned to be extremely difficult to complete. Note: *This may not be possible, I am currently determining its' feasibility.*


## Blacksmith Vendor Notes
For notes on the blacksmiths of Skyrim including their smithing and speech levels, please see "*Blacksmiths SE.xlsx*". The first sheet in the workbook contains information that may be useful to other mod authors as extracted from the Creation Kit. Every other sheet in the workbook shows the calculations and costs of the equipment craftable by the vendor introduced by this mod.


## Version History
Old and current versions of the mod are stored in the plugins folder for posterity and bug-tracking reasons. The following list details each version in the folder.


- Alpha 1.0.0: Initial alpha release. Does not contain the refinement system and quests, player relocation, or voiced dialogue.
