# Equipment Ordering and Refinement
A mod for Skyrim SE with the goal of allowing players to custom order and refine equipment at blacksmith vendors. The goal of this mod is to provide an alternative to the Blacksmithing skill.


## Goals
- [] Ordering of a single piece of equipment
- [] Ordering of armor sets
- [] Ordering/refinement based on vendor skill
- [] Ordering takes a certain amount of in-game time based on vendor skill and equipment ordered
- [] Increasing cost based on vendor skill and equipment ordered/refined
- [] Player must provide crafting materials for equipment orders


## Motivation
You may ask: "Why would I need this mod if the blacksmithing skill exists?" or "What is the point of the blacksmithing skill with this mod installed?" 


Back in the ye-olden days of Oldrim when the game first launched, blacksmithing was a viable skill to level up out of the gate (without glitching the game). This was primarily because of two features of Oldrim:
1. Blacksmithing in Oldrim did not possess a diminishing return curve on smithed items and equipment meaning it was entirely possible to level the skill to 100 by just crafting Iron Daggers through slight time investment.
2. The most abundant ore type in Skyrim is iron ore. The only other ore type in Skyrim that is even remotely close to it's abundance is ebony ore, which the player cannot utilize in smithing until they are nearly finished leveling the skill.


Sometime around patch 1.5 for Oldrim, Bethesda decided to do away with static levelling of the Blacksmithing skill and added a diminishing return curve for blacksmithing xp from items and equipment. The intent was obviously to make it feel more rewarding and prevent players from spamming their way to the best equipment as soon as they start the game (usually well before said equipment was available as levelled loot or from vendors). This single change made the blacksmithing skill far more expensive and time-consuming, akin to the same skill in a game like World of Warcraft. Outside of iron ore and ebony ore, the other types of ore are far more precious and rare in the Skyrim game world. Levelling the blacksmithing skill in an updated version of Oldrim or Skyrim SE thus requires purchasing raw materials from vendors at a much higher cost than what was realizable before the patch.


This mod seeks to balance this change by introducing a feature I've always wanted in the game and a feature that it seems Bethesda wanted as well considering the voice acting of the blacksmith vendors: equipment ordering and refinement. The basic premise is to allow players to order equipment and refine it at blacksmiths provided they have the materials and the vendor has the requisite skill. Vendors with higher skill should take less time to produce equipment at a higher cost with the opposite holding true for less skilled vendors. For instance, because crafting dragon equipment takes Master-level skill, only Eorlund Gray-Mane in Whiterun can produce said equipment at a hefty cost as well as a not-insignificant time investment. Of course, equipment that requires the use of a specific forge such as Skyforged equipment should only be orderable at the vendor who would naturally be able to make such equipment.


Note that this mod is meant to be immersive with the Skyrim game world. The prices for the new blacksmith services will eventually be balanced the Skyrim economy.


## Overview
This mod introduces two additional fields to all blacksmiths: Smithing Mastery and Speech Mastery. Smithing Mastery is used to determine what types of equipment blacksmithing vendors can craft and refine. Speech Mastery is used to help determine the cost of ordering and refining equipment. 


Each mastery aligns with one of the traditional skill mastery levels from oldschool Elder Scrolls: Novice, Apprentice, Adept, Expert, and Master. The mastery levels were calculated by extracting the Smithing and Speech skill levels of each blacksmith using the Creation Kit. Skill levels were fitted to a pseudo-normalized distribution where each smith falls into a range of the 15th, 50th, 85th, and 100th percentile. The Smithing and Speech skills of each smith were normalized to a [0, 1] range and were then fitted to the prior percentiles. The following table details the range for each mastery level.


| Lower Range | Upper Range |   Mastery  |
|:-----------:|:-----------:|:----------:|
|      0      |      15     |   Novice   |
|      15     |      50     | Apprentice |
|      50     |      85     |    Adept   |
|      85     |     100     |   Expert   |
|     100     |             |   Master   |


This distribution results in a single Master level smithing vendor in all of Skyrim as can be seen in the following table.


|         Vendor         |       Location       | Smithing Mastery | Speech Mastery |
|:----------------------:|:--------------------:|:----------------:|----------------|
|    Adrianne Avenicci   |       Whiterun       |    Apprentice    |   Apprentice   |
|          Alvor         |       Riverwood      |      Expert      |     Expert     |
| Arnskar   Ember-Master |    Ragged Flaggon    |      Expert      |     Expert     |
|   Asbjorn Fire-Tamer   |  The Scorched Hammer |       Adept      |      Adept     |
|        Balimund        |  The Scorched Hammer |       Adept      |      Adept     |
|         Beirand        |  Solitude Blacksmith |       Adept      |      Adept     |
|         Gunmar         |    Fort Dawnguard    |      Master      |     Master     |
|         Hestla         |    Castle Volkihar   |    Apprentice    |     Novice     |
|     Glover Mallory     |      Raven Rock      |      Novice      |   Apprentice   |
|   Baldor Iron-Shaper   |     Skaal Village    |      Novice      |     Novice     |
|        Dushnamub       |       Narzulbur      |    Apprentice    |     Novice     |
|        Elrindir        | The Drunken Huntsman |    Apprentice    |   Apprentice   |
|    Eorlund Gray-Mane   |       Skyforge       |      Expert      |     Expert     |
|         Fihada         |       Fletcher       |    Apprentice    |   Apprentice   |
|         Filnjar        |     Shor's Stone     |       Adept      |      Adept     |
|         Gharol         |     Dushnikh Yal     |    Apprentice    |     Novice     |
|    Ghorza gra-Bagol    |       Markarth       |      Novice      |     Novice     |
|           Lod          |       Falkreath      |    Apprentice    |   Apprentice   |
|     Moth gro-Bagol     |     Markarth Keep    |      Novice      |     Novice     |
|    Oengul War-Anvil    |       Windhelm       |    Apprentice    |   Apprentice   |
|        Rustleif        |       Dawnstar       |       Adept      |      Adept     |
|        Shuftharz       |      Mor Khazgur     |       Adept      |   Apprentice   |
|    Ulfberth War-Bear   |       Whiterun       |    Apprentice    |   Apprentice   |


Prior to the Dawnguard DLC, Eorlund Gray-Mane, true to his name, was the most skilled smith in Skyrim. However, that title now belongs to Gunmar from the Dawnguard DLC. Surprisingly, none of the smiths in Skyrim actually have a smithing level anywhere near 100. The lowest smithing level in Skyrim SE is 5 while the highest smithing level in Skyrim SE is 57. This is why the mod introduces Smithing Mastery to control who can produce and refine the various types of equipment. 


Each type of equipment maps to a required Smithing Mastery level as defined in the following table.


| Equipment Type | Smithing Mastery |
|----------------|------------------|
| Advanced       | Adept            |
| Arcane         | Adept            |
| Bonemold       | Novice           |
| Chitin         | Apprentice       |
| Daedric        | Master           |
| Dragon         | Master           |
| Dwarven        | Apprentice       |
| Ebony          | Master           |
| Elven          | Apprentice       |
| Glass          | Expert           |
| Nordic         | Adept            |
| Orcish         | Adept            |
| Steel          | Novice           |


As can be seen in the prior table, Daedric, Dragon, and Ebony equipment are locked behind Master level smithing. Skyforged arms can only be forged by Eorlund Gray-Mane. Wolf armor can only be forged by Eorlund Gray-Mane after you complete the quest "The Silver Hand" from the Harbingers questline. Stalhrim arms and armor can only be forged by Baldor Iron-Shaper after you complete the optional quest "A New Source of Stalhrim". The decision to align the best equipment with Gunmar works lore-wise because the Dawnguard focus on martial prowess while the Ancient Vampires focus on magical prowess. I've always considered it a bad move from a player perspective to join the Ancient Vampires in the Dawnguard DLC if my character does not focus on magic given that the vanilla vampire perks focus entirely on enhancing magic abilities.
