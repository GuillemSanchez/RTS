# RTS Balancing
I am Guillem Sánchez, student of the [Bachelor’s Degree in Video Games by UPC at CITM](https://www.citm.upc.edu/ing/estudis/graus-videojocs/). This content is generated for the second year’s subject Project 2, under supervision of lecturer [Ricard Pillosu](https://es.linkedin.com/in/ricardpillosu).
In this Website i'm gonna explain how works the balance of units and some other stuff in RTS videogames like Age of Empires II: The Age of Kings, Ensemble Studios or Praetorians, Pyro Studios.

But, What is balancing in a game?

For me, balancing a game means that any of the game elements are inefective or undesirable to play with or againts.

"An important trait of any game is the illusion of winnability. If a game is to provide a continuing challenge to players, it must also provide a continuing motivation to play. The game must appear to be winnable to all players, beginners and experts, but it must never truly be winnable or it will lose its appeal."

### — Chris Crawford

## Index

## Unit Balancing basics

Now we barely know what is balencing a game, but was is the meaning of this?
Whould you rather play a game that allows this?

Its a bit extremly, but this is NOT fun, we want to avoid this in our games, that is why Units are one of the core components of any RTS video game. It is important to have a balanced roster of units. Without a good unit balance, the game would be like a farming simulation with some types of units that can destroy the rival farm.

### Visible vs Hidden Balancing

There are 2 main kinds of unit balancing, the first one is the visible, this kind is balances that can be directly seen by the player, range of a shot, speed of a unit or type of movement (ground unit, sea unit, flying unit).

The second type of unit balancing is hidden balancing, This kind of balancing is used in the games rules, changing probabilities for events or efficiencies of abilities. Examples of abstract balancing are stats like health, damages, crit. Hidden balancing is usually presented to the player through text labels in the UI (user interface).


### Rock/Paper/Scisors

One way of unit balancing is using the "Ol' reliable" Rock/Paper/Scisors, we have three types of entities, consisting of rock, paper and scissors; and these entities counteract each other: rock wins scissors, scissors wins paper and paper wins rock. Then we only need to change the names of the entities, and PUFFF we have a good balanced game...

#### NOOOOO! Our game doesnt work WHYYYYYYY?????

Our little problem here is that our game is more complicated that the ancient game of Rock/Paper/Scisors, our game have a lot of variables like resources and stats, but we will use the same strategy of R/P/S to solve this problem.

But first lets settle the bases and some maths about why is a fair and balanced game the Rock/Paper/Scisors. Lets make a table with the possible results of a game of R/P/S, the R will mean rock, the P will main paper and the S will mean scissors. If we interpret the results of this table as points, for winning a game, we would obtain + 1 point, for losing -1 points, and for a tie we would obtain 0 points. The first column will be our hand (RM/PM/SM) and the first row will be the oponents hand.

| |R|P|S|
|----|-----|-----|-----|
|RM|0|-1|1|
|PM|1|0|-1|
|SM|-1|1|0|

With this table we can extract the next equations:

#### RM = 0 * R + (- 1) * P + (+ 1) * S

#### PM = (+ 1) * R + 0 * P + (- 1) * S

#### SM = (- 1) * R + (+ 1) * P + 0 * S

simplifying,

#### RM = S - P
#### PM = R - S
#### SM = P - R

R/P/S is a special type of game known as zero-sum games, that means that we gain and lose the same amount of utility, for example, in the first equation RM = 0 * R + (- 1) * P + (+ 1) * S the taking the variables of the right side of the equation goes like this RM = 0 - 1 + 1, the same as RM = 0, that situation means that we don't gain but we don't lose anything. With that we can take that:

#### RM = SM = PM = 0 
(only on the left side of the equation)

If we supose that we will take the same amount of times all the possibilities we can get this equation:

#### R + S + P = 1 
(only on the right side of the equation)


With this two equations we can get this:

#### RM = S - P
#### PM = R - S
#### SM = P - R

#### RM = SM = PM = 0 


#### 0 = S - P
#### 0 = R - S
#### 0 = P - R

S = P

R = S

P = R

We can subsitute this in the next equation:

#### R + S + P = 1 

#### R + R + R = 1
#### R = 1/3

And we get the same if we use the other variables.

#### R = 1/3
#### P = 1/3
#### S = 1/3

This will so important in the last point of this wiki, if you wanna go direct press here. But first let's talk about some points that are also important if you wanna balance well your game.
Before going to a new point i want to talk about weakness support.


### Weakness Support

The method that we were exploring is when you design your units to be strong against a specific type of enemy unit (or type of units), and weak against another. Weakness Support, is when you make sure that all units have a certain weakness. The difference to rock-paper-scissors is that the weakness is based on an stat of the unit, and not on the stat of an enemy unit. For example, the weakness with infantry in the R/P/S is that it's vulnerable to archers. In Weakness support scenario the infantry's weakness would be slow movement.

The “support” in weakness support refers to how the players should reinforce the unit's weakness. For example, if the infantry is slow-moving, then maybe its “weakness support” is wagons which can transport infantry quickly into battle.


### What gamers expect of RTS?

The easy way to answer this question is saying that it depends of the type of strategic gamer that we are asking. RTS fans have largely split off and gravitated towards games that tickled their particular itches more. For real-time battles, you've got Total War. For supply chain management, you've got Factorio. For base-building, you've got Rimworld. For bigger-picture campaigns you've got Paradox's offerings; just as examples.
Gamers will expect of sure that you can craft, refine and execute a strategy, they want to be creative and piece the tools that we give to them together to make powerful strategys, like unit compositions, timing attacks or build orders. Its not the amount of tools that we give to them is the amount of possibles conbinations that can be done.


But lets do a list of some of the most "fun generators" of RTS games:


#### Asymmetric Desing

This is a important point that most of the gamers will search nowadays in RTS games, this "fun generator" affects a lot of areas of the game, for example this will make factions more unique, so players could choose according to their preferences about their playstyle or the aesthetics. Maps can have asymmetric desing to, that will make the 1 player campaing more fun and diverse.


#### RNG

RNG stands for random number generation, some people think that RNG shouldn't be present in RTS games, because they don't want any type of luck in the game, but most of the player basis thinks that RNG can be implemented in that type of games IF the player can influence with some type of strategy or skill to incress the "luck" of some actions, for example, covering some soldiers behind a rock to get a better change of wining a skirimish. RNG makes the game less predictible and adds tension to the gameplay.


#### Unit diferentation

Unit diferentation is really important to a RTS and is something that you should look at any moment to make your game fun to play, units need to feel diferent to the player, its not the same have a army of motorcycles, fast and with great movility, or have a army of tanks, slow but powerfull. Theres is nothing satisfaying about just attack/moving your units, units should be designed in a way that rewards players for being creative.



### What gamers expect of RTS Balance?

Theres at misconception that balances only matters to high-level players, but that is not true, balance is crucial in making a RTS fun.

What we would be the point of having 30 units if only 10 of then are usefull?

Lets say a player strategy is to overwhelm the opponent with some type of bombers (air-ships), they must overcome the fact that bombers are vulnerable to other air units, to complement the bombers the player relies on a antiair infantery. If the antiair infantery is underpowered the strategy will fail, that will cause frustation to the player becauses the strategy failed for reasons which are not faults of their own, the problem was poor balance.

Gamers dont want to have units that doesnt perform its intended role, or an overpower unit that prevents another from doing so. Imbalance is bad and things that are underperfoming or overpowered should be fixed, but good "balance" doesnt make and RTS game more balanced, it emphasizes the unique qualities of each unit, creating more decisions about which tools are used and how they are used.

Gamers like the "meta" but we need to have a flexivle and varied meta, givin the oportuniti to break the current meta with some strategis, to archive that we need to do a good balance of the game, if not players will start to massing the same unit all the time and that is NOT funny.

### Tactics vs Strategy


First we need to know the difference between Strategy and Tactics/skill.

Strategy is a complete algorithm for playing the game, telling a player what to do for every possible situation throughout the game. Its more about resource managment and global vision. We will call it Macromanagment (or macro)

Tactics/skills are short-term actions to attain specific goals. More about units managment. We will call it Micromanagment (Micro)

Which is better for our game? It depends, games like starcraft are more focused in the micro, and are good, but game like Civ are more about macro, and also are good. Nowadays, every RTS (excepting some 4X games) have micro in their gameplay, because is really difficult to avoid it.

#### 4X games
4x or (grand strategy games)are by definition board games in which players control an empire and "explore, expand, exploit, and exterminate". That type of games are more based in macrogestion that anyother. In grand strategy and 4X games you typically don't have much to do with tactics. You decide the target and the ressources you wish to use on that target. Everything that comes after that, namely the tactics, depends on the people who are so tiny that you can't even see them on your interface. Examples of this are Freeciv, Civilization series, or Supremacy 1914.

In theory, strategy/macromanagement is by default more important. The player who comes victorious out of a session is usually the one that could read the game more accurately. In a scenario of two players equally capable in micromanagement, the one who would apply the better macromanagementwould win most of the times.

On the other hand, intensive micromanagement can distract players from macromanagement. The players should make long term decisions, but if they do not have the required speed to execute their moves faster than their opponents, then the strategic part becomes insignificant.

In conclusion, a rough outline of what are the defining characteristics of RTS are can be found in what the senior producer of Command & Conquer: Generals, has said. 

“The fundamentals of these games are pretty similar: they generally have maps or levels to explore and fight over, resources that can be harvested to build structures and units, armies that move and fight, and a technology or “research” tree that unlocks more powerful units and capabilities over time” (Bates 2004)



### Numbers and more Numbers

Lets take again the R/P/S equations and lets aply it to our games. First we need to define our three types of units that we wanna aply the R/P/S system. Lets say that we have a spearmen, a knight (in a horse) and a archer. Now we need to define each roll, archers have long-range attacks that will be lethal to our spearmen, but the spearmen with their spears can kill the knights easy, and our knights are to fast to get killed before they charge to our archers, so spearmen win against knights, knights win against archers and archers win against the spearmen.


As R/P/S we need some type of measure to track our balances. Every unit will have a cost, hp, and attack, the attack will the damage ratio that the unit does to the other type's of unit, so we will have three type of damage:

ID: bonus or damage against infantery units (spearmen)
RD: bonus or damage against ranged units (archers)
CD: bonus or damage against cavalry units (knights)


here is the table of stats:

|Type|Cost|HP|ID|CD|RD|
|---|---|---|---|---|---|
|Spearmen|120|90|8|16|0|
|Archer|60|80|10|4|6|
|Knight|220|200|16|16|10|


You can see that the knight is overpowered, but is that really true? Lets see

First lets make a table like we did it in R/P/S. Lets call "A" our unit and "B" rival's unit, we will use the next formula to calculate the result, the formula is difficult, i will link a table to a excel that it will do it automaticly. This formula is taken out of this link.

Formula:

Min((A cost/ B dmg (against A)), ((B Hp/ A dmg (against B)) * (A dmg (Against B) * (B cost/ B hp) - (B dmg (against A) * (A cost/A hp)))

That formula will give us the result of a 1 vs 1 unit combat effeciency, if the result is positive means that the our unit would be more efficient (less resource wasting) than the enemy unit. 

Lets make our table: (S means spearmen, A means archer and K means Knight, if the acronim have a M means that is our unit)


| |S|A|K|
|----|-----|-----|-----|
|SM|0|-20|38|
|AM|20|0|-38|
|KM|-38|38|0|

Every one of the sections are calculated with the formula from before.

Now lets use the formulas from R/P/S to take the percents and see if our game is balanced or not.

(Zero-sum)
#### SM = AM = KM = 0 

(all posibilities)
#### S + A + K = 1 

(Table resuls)

#### SM = 0 * S + (- 20) * A + (+ 38) * K

#### AM = (+ 20) * S + 0 * A + (- 38) * K

#### KM = (- 38) * S + (+ 38) * A + 0 * K

simplyfied,

#### SM = - 20A + 38K

#### AM = 20S - 38K

#### KM = - 38S + 38A

With the 2 equations (zero-sum, all posibilities)

#### 20A = 38K

#### 20S = 38K

#### 38S = 38A


#### S + A + K = 1 

lets calculate the results:

#### A = 38/96 = 0,39

#### K = 760/2604 = 0,29

#### S = ... = 0,32

From the results of the probability calculation, it can be take that our theoretical RTS video game would actually be fairly balanced, being the three probabilities of the opponent utilizing the units rounding the 0,33. The unit or unit type that would be most underutilized in this hypothetical RTS game would be the knight. If the designer of this game prefered to make gunmen a more relevant unit, they would likely have to decrease the unit’s cost or change some of the stats.




