---
layout: single
title:  "Dev Diary- Unity3D game Defense Brigade part 2 "
date:   2015-11-23 18:07:10 -0400
#categories:  [ "Dev Diary", "Game Design", "programming", "Unity" ]
---

Dev Diary part 2 – Electric Boogaloo. See here for the previous dev diary. So at this stage in the game we’ve got our characters controlled and not going off screen, but not much else. The next big players are the enemies.

# Enemy movement
So the next big aspect of the game is, you know, the challenge. I didn’t just want plain obstacles, I wanted them to target the weak character, so that the strong character not only had to beat back the enemies, the player will have to dodge incoming enemies with the weak character.

![Enemies converging on the weak character.](https://i2.wp.com/adinashanholtz.com/wp-content/uploads/2015/11/enemyconverging.png) 
<em style="display: block;">Enemies converging on the weak character.</em>

The logic is basically “move towards the weak character player”. Lucky for us, Unity has a built in function, Vector2.MoveTowards. So the code for moving an enemy toward a player is

```cs 
float step = speed * Time.deltaTime;
transform.position = Vector2.MoveTowards(transform.position, weakcharacter.transform.position, step);```

# Spawning waves
I have to admit, I couldn’t have asked for a better enemy spawning tutorial than the one Unity has here. It goes through the motions of creating a game controller that spawns enemies at various intervals that the developer can set. However, I made some changes that made it more relevant to this game.  One thing was that I didn’t want  a win condition that would have a set high score, so I set them to spawn automatically until the player lost. This would allow for unique high scores.
I also had to make sure that the enemies would spawn randomly all around the screen, not just at the top. After generating a random location the game controller instantiates a new enemy at spawnPosition. See below.
randomgeneratedenemies

![Enemies spawning in random areas around the screen.](https://i0.wp.com/adinashanholtz.com/wp-content/uploads/2015/11/randomgeneratedenemies.png)
<em style="display: block;">Enemies spawning in random areas around the screen.</em>

# Prefabs
In order for the strong character to defeat the enemies, the enemies would detect if the strong character entered a trigger, then destroy itself. Before I remembered that prefabs existed, I kept running into this problem where the strong character would run into a couple of enemies, then they’d stop spawning and I’d get a Missing Reference Exception.

```cs 
MissingReferenceException: The object of type 'GameObject' has been destroyed but you are still trying to access it.
Your script should either check if it is null or you should not destroy the object.```

The problem was that I was deleting the original reference to the enemy object, which was solvable by creating a prefab of the enemy and referencing that. A prefab is essentially an object template. Any modifications made to a prefab is made to all instances of that object. This made it so I wasn’t editing the original object, just spawning copies of it.

