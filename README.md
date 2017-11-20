# pySC2 mini-games
Curated list of pysc2 mini-games 


## Minigame task description

Minigames come as a controled environments that might be useful to exploit game features in SC2. General purpose learning system for Startcraft 2 can be a daunting task. So there is a logical option in splitting this tasks into minitask in orther to advance in research . Mini-games focus on different elements of Starcraft II Gameplay .

To investigate elements of the game in isolation, and to provide further fine-grained steps towards playing the full game, Deepmind has built several mini-games. These are focused scenarios on small maps that have been constructed with the purpose of testing a subset of actions and/or game mechanics with a clear reward structure. Unlike the full game where the reward is just win/lose/tie, the reward structure for mini-games can reward particular behaviours (as defined in a corresponding .SC2Map file).


## Minigames repositories 

ArChon https://github.com/4rChon/sc2-ai-mini-games


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

### Notes for scripted agent and/or agent Policy Design 
* Optimal policy might learn micro strategy to move Stalkers away from zealots and atack them in distance 
  
  
  
  * Defeat Zealots Blink
  
  * Defeat Single Zealot
  
Deadzombie2333 https://github.com/deadzombie2333/Minigame_Predict_Battle_Outcome

  * Defeat lings and Hydralisk
  
  * Predict battle outcome 

SoyGema https://github.com/SoyGema/Startcraft_pysc2_minigames

  * Sentry Defense 
  
  * HallucinIce

keaneu Tan https://github.com/TitanEX1/SC2-Scenario-Designs
