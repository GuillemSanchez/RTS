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
