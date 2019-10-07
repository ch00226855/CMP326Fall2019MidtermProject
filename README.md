# CMP 326 Midterm Project: Text-Based Adventure Game

In this project you will create a simple text-based adventure game. The game will create a player object using information from a file, build a dungeon of three rooms each containing a monster, and allow the player to challenge the monster one-by-one and explore for treasure. The game will display messages on the screen to tell user what happens. It also creates a log file that keeps a record of the game.
The program contains the following classes: (See Javadocs for detailed descriptions)

1.	A MyCreature class that implements interface Creature with attributes name, description, hitPoints, damage, and room. A creature object can attack and take damage. It also has an isAlive() method and a toString() method.
2.	A MyPlayer class that inherits MyCreature and implements interface Player. A player has an attribute healAmount, and a heal() method that increase player’s hitPoints by healAmount.
3.	A MyMonster class that inherits MyCreature and implements Monster. A monster as an attribute enrageThreshold, and will be enraged (double its attack damage) if its hitPoints falls below the threshold. It has methods canEnrage() and enrage().
4.	A MyRoom class that implements interface Room with attributes roomIndex, description, and monster. It has an enter() methods that displays description of the room and the monster in the room, and then initiates a battle between player and monster. The class also has a isComplete() method and a toString() method.
5.	A MyTreasureRoom class that inherits MyRoom and implements TreasureRoom. A MyTreasureRoom has a String treasure, and an overrided enter() method that in addition to what MyRoom’s enter() method does, if the player defeats the monster, displays a message that player finds the treasure.
6.	A MyBattle class that implements interface Battle and has attributes player and monster. There is a run() method that let player and monster battle against each other until one of them dies. In each player turn, the method displays player hitPoints and monster hitPoints, then attack or heal following player’s command, and checks if monster is killed. In each monster turn, the method checks if the monster is going to enrage, then let the monster attack the player and checks if player is killed.
7.	A MyGame class that implements interface Game with attributes player and dungeon. Dungeon is an array of 3 MyRoom objects. There is a constructor that constructs the player object using information from a file, and constructs three monsters and three rooms with attributed given in the tables below. There is a play() method that let the player enter the dungeon rooms one by one until the player dies or clears all rooms. The method also updates the GameLog file as player progresses. 
8.	Finally, the MyGame class has a static main method that instantiates a MyGame object and runs the game.

|Monster Name	|Room Index	|Description	|Hit Points	|Attack Damage	|Enrage Threshold|
|---------------|---------------|---------------|---------------|---------------|----------------|
|Orc	|0	|Covered with green blood	|20	|5	|0|

|Skeleton	|1	|Funny how it moves	|40	|10	|10|

|Fire Dragon	|2	|Spout fire with each breath	|100	|20	|40|


|Room Index	|Description	|Monster in the Room|
|---------------|---------------|-------------------|
|0	|A room with an unbearable smell	|Orc|

|1	|Dark and cold	|Skeleton|

|2	|A giant hall with something shiny on the other end	|Fire Dragon|

Each student is required to present the program in class. Grading rubric is as follows:
	Pts
	
Student presents the program on presentation day	10

The program can create a player object	10

The program generates a dungeon properly	10

The program displays the description of the first dungeon room	10

The program initiates a player-monster battle.	10

The program correctly performs one player action according to user's choice	10

The program finished a player-monster battle.	10

The game was completed properly.	10

The program handles negative player hitpoints correctly	5

The program handles negative damages correctly	5

The game play messages were correctly written to the GameLog.txt file	10

Total	100

