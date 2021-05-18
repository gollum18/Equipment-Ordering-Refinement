# Equipment Ordering and Refinement
A mod for Skyrim SE with the goal of allowing players to custom order and refine equipment at a unique blacksmith vendor. The goal of this mod is to provide an alternative to the Blacksmithing skill.


## Goals
- [X] Compute costs for every piece of equipment craftable by the vendor.
- [ ] Implement equipment cost in-game.
- [ ] Write quests for the vendor to unlock special equipment crafting and refinement.
- [ ] Write dialogue for the vendor/player interaction.
- [ ] Record the dialogue for the vendor.
- [ ] Design and implement the vendors' skills and appearance.
- [ ] Implement the quests in-game and tie them to the vendors skill/perk progression.
- [ ] Implement dialogue system for equipment crafting.
- [ ] Implement dialogue system for equipment refining.
- [ ] Implement an appropriate schedule and idle animations.
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
The below table contains notes on all of the blacksmith vendors in the base game and its' DLCs including their smithing level and speech level. Additionally, it also contains generated smithing mastery and speech mastery categories that are based on a forced normal distribution with the following ranges [0.0, 0.15), [0.15, 0.50), [0.50, 0.85), [0.85, 1]. See the table itself for where the individual smiths stand in terms of smithing and speech mastery. 


| ID                     | Name                   | Location             | Smithing | Speech | Smithing Percentile | Speech Percentile | Smithing Mastery | Speech Mastery |
|------------------------|------------------------|----------------------|----------|--------|---------------------|-------------------|------------------|----------------|
| AdrianneAvenicci       | Adrianne Avenicci      | Whiterun             | 26       | 26     | 0.403846154         | 0.488372093       | Apprentice       | Apprentice     |
| Alvor                  | Alvor                  | Riverwood            | 39       | 40     | 0.653846154         | 0.813953488       | Expert           | Expert         |
| Arnskar                | Arnskar Ember-Master   | Ragged Flaggon       | 39       | 40     | 0.653846154         | 0.813953488       | Expert           | Expert         |
| Asbjorn                | Asbjorn Fire-Tamer     | The Scorched Hammer  | 31       | 31     | 0.5                 | 0.604651163       | Adept            | Adept          |
| Balimund               | Balimund               | The Scorched Hammer  | 35       | 36     | 0.576923077         | 0.720930233       | Adept            | Adept          |
| Beirand                | Beirand                | Solitude Blacksmith  | 37       | 37     | 0.615384615         | 0.744186047       | Adept            | Adept          |
| DLC1Gunmar             | Gunmar [1]             | Fort Dawnguard       | 57       | 48     | 1                   | 1                 | Master           | Master         |
| DLC1Hestla             | Hestla                 | Castle Volkihar      | 20       | 15     | 0.288461538         | 0.23255814        | Apprentice       | Novice         |
| DLC2RRGloverMallory    | Glover Mallory         | Raven Rock           | 15       | 20     | 0.192307692         | 0.348837209       | Apprentice       | Apprentice     |
| DLC2SVBaldorIronShaper | Baldor Iron-Shaper [2] | Skaal Village        | 5        | 5      | 0                   | 0                 | Novice           | Novice         |
| Dushnamub              | Dushnamub              | Narzulbur            | 20       | 15     | 0.288461538         | 0.23255814        | Apprentice       | Novice         |
| Elrindir               | Elrindir               | The Drunken Huntsman | 21       | 24     | 0.307692308         | 0.441860465       | Apprentice       | Apprentice     |
| EorlundGrayMane        | Eorlund Gray-Mane      | Skyforge             | 44       | 38     | 0.75                | 0.76744186        | Expert           | Expert         |
| Fihada                 | Fihada                 | Fletcher             | 27       | 26     | 0.423076923         | 0.488372093       | Apprentice       | Apprentice     |
| Filnjar                | Filnjar                | Shor's Stone         | 35       | 36     | 0.576923077         | 0.720930233       | Adept            | Adept          |
| Gharol                 | Gharol                 | Dushnikh Yal         | 20       | 15     | 0.288461538         | 0.23255814        | Apprentice       | Novice         |
| GhorzaGraBagol         | Ghorza gra-Bagol       | Markarth             | 5        | 5      | 0                   | 0                 | Novice           | Novice         |
| Lod                    | Lod                    | Falkreath            | 27       | 27     | 0.423076923         | 0.511627907       | Apprentice       | Apprentice     |
| MothgroBagol           | Moth gro-Bagol         | Markarth Keep        | 5        | 5      | 0                   | 0                 | Novice           | Novice         |
| Oengul                 | Oengul War-Anvil       | Windhelm             | 27       | 27     | 0.423076923         | 0.511627907       | Apprentice       | Apprentice     |
| Rustleif               | Rustleif               | Dawnstar             | 31       | 31     | 0.5                 | 0.604651163       | Adept            | Adept          |
| Shuftharz              | Shuftharz              | Mor Khazgur          | 31       | 26     | 0.5                 | 0.488372093       | Adept            | Apprentice     |
| Ulfberth               | Ulfberth War-Bear      | Whiterun             | 27       | 27     | 0.423076923         | 0.511627907       | Apprentice       | Apprentice     |
|                        | Knight-Paladin Gelebor | Min                  | 5        | 5      |                     |                   |                  |                |
|                        |                        | Max                  | 57       | 48     |                     |                   |                  |                |
|                        |                        | 15th Percentile      | 16.5     | 15     |                     |                   |                  |                |
|                        |                        | 50th Percentile      | 27       | 27     |                     |                   |                  |                |
|                        |                        | 85th Percentile      | 38.4     | 37.7   |                     |                   |                  |                |
|                        |                        | 100th Percentile     | 57       | 48     |                     |                   |                  |                |


Note that this table is unused by the newest iteration of the mod as described in the **Overview** section. This table was to be utilized by the first iteration of the mod back when every blacksmithing vendor was planned to be able to craft and refine equipment.
