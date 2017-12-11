
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![label](https://img.shields.io/github/issues-raw/badges/shields/website.svg)]()

# pySC2 mini-games
Curated list of pysc2 mini-games 


## Minigame task description

Minigames come as a controled environments that might be useful to exploit game features in SC2. General purpose learning system for Startcraft 2 can be a daunting task. So there is a logical option in splitting this tasks into minitask in orther to advance in research . Mini-games focus on different elements of Starcraft II Gameplay .

To investigate elements of the game in isolation, and to provide further fine-grained steps towards playing the full game, Deepmind has built several mini-games. These are focused scenarios on small maps that have been constructed with the purpose of testing a subset of actions and/or game mechanics with a clear reward structure. Unlike the full game where the reward is just win/lose/tie, the reward structure for mini-games can reward particular behaviours (as defined in a corresponding .SC2Map file).


## Minigames repositories 

## ArChon 
https://github.com/4rChon/sc2-ai-mini-games


   ## DefeatZealots
   
![alt tag](https://github.com/SoyGema/pySC2-mini-games/blob/master/images/4rChon/DefeatZealots%20.png)

### Description

A map with 2 Stalkers opposite to 3 Zealots. Rewards are earned by using the Stalkers to defeat the Zealots. Whenever all Zealots have been defeated, a new group of 3 Zealots is spawned and the surviving Stalkers are moved to a random point on the opposite spawning location, retaining their existing health. Whenever new units are spawned, all unit positions are reset to opposite sides of the map.

### Initial State
* 2 Stalkers at a random side of the map (preselected)
* 3 Zealots at the opposite side of the map from the Stalkers

### Rewards
* Zealot defeated: +5
* Stalker defeated: -1

### End Conditions
* Time elapsed
* All Stalkers Defeated

### Time Limit
* 160 seconds

### Additional Notes
* Fog of War disabled
* No camera movement required (single-screen)
* Target skill(s): Kiting

### Notes for scripted agent and/or agent Policy Design (separate good agents from bad ones) 
* Optimal policy might learn micro strategy to move Stalkers away from zealots and atack them in distance . Focusing on attacking one zealot until it's dead seems to have an optimal outcome. 
* Great map for micro Stalker unit learning 
  
### Variations of DefeatZealots 

  * Defeat Zealots Blink
   

## SoyGema 
https://github.com/SoyGema/Startcraft_pysc2_minigames
  
   ## HallucinIce ( Debugged ) 

![alt tag](https://github.com/SoyGema/pySC2-minigames/blob/master/images/SoyGema/HallucinIce%20.png)

#### Description

The mini-game is an imbalanced  melee in between Terran and Prottoss.
The goal is to exploit sentry hallucination function 

#### Initial State

*   3 Sentry at left playable size
*   5 Hellions at right playable size


 #### Rewards

Protoss defeated : -10
Terran defeated : +10

 #### End Conditions

Time elapsed
Zerg defeated

### Time Limit 
30 seconds

#### Additional Notes
Terrain condition designed for hallucination defense game development 
Fog of war disabled
No camera movement required (single-screen)

### Notes for scripted agent and/or agent Policy Design (separate good agents from bad ones) 
* Optimal policy might learn micro strategy to hallucinate units that might absorb the maximum damage possible and positioning hallucinated units protecting sentrys 
* Great map for micro sentry unit learning 

## deadzombie2333
https://github.com/deadzombie2333/Minigame_Predict_Battle_Outcome


 ## PredictBattleOutcome ( Debugged - reviewed with author ) 
 
 ![alt tag](https://github.com/SoyGema/pySC2-minigames/blob/master/images/deadzombie2333/Predict_Battle_Outcome.png)
 
### Description
Two considerable amount of random enemy armies confront each other in a open area, having random upgrade and skills of their own. Determine or predict wich one will win the batlle .After 2 seconds of pause, both side will march toward each other and start their bloody battle until only one side of the army stand on the battle ground.


### Initial State
* 1 to 22 Marines, 1 to 4 marauders and 1 to 4 tanks displayed randomly 
* 1 to 23 zerlings, 1 to 9 banelings and 1 to 11 Hydralisks displayed randomly 

### Rewards
* Terran defeated: +1
* Zerg defeated: -1

 #### End Conditions

Time elapsed
Zerg defeated

### Time Limit 
30 seconds

#### Additional Notes
Objective for your agent/AI is to determine which side will win. In order to do that, you have to gather as much information as possible in limited amount of time. 

### Notes for scripted agent and/or agent Policy Design (separate good agents from bad ones) 
* Optimal policy will predict the outcome of the battle having a high degree of accuracy in a early stage of the game visualization ( before 2 seconds ) 

## TitanEX1
https://github.com/TitanEX1


 ## DefeatRavagersRepairCyclones ( Debugged + time limit changed - review with author asked ) 
 
 ![alt tag](https://github.com/SoyGema/pySC2-minigames/blob/master/images/TitanEX1/DefeatRavagersRepairCyclones.png)
 
 ### Description
Defeat Zerg enemy using the repair function by SCVs. Learn to micro focusing fire and reparing units while attack


### Initial State
* 4 Ravagers
* 2 Cyclones and 2 SCVs 

### Rewards
* Terran defeated: 
* Zerg defeated: 

 #### End Conditions

Time elapsed
Zerg defeated

### Time Limit 
60 seconds

### Additional Notes
Fog of war disabled
No camera movement required (single-screen)

### Notes for scripted agent and/or agent Policy Design (separate good agents from bad ones) 
* Optimal policy might learn micro strategy to differenciate in between repair and attack units and exploit each one functions. 
* Great map for micro terran repair/attck unit learning 
