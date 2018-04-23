---
layout: single
title:  "Dev Diary- Unity3D game Defense Brigade part 3"
date:   2015-11-24 21:02:26 -0400 
#categories:  [ "Dev Diary", "Game Design", "programming", "Unity" ]
---

Hey guys, this is going to be the last dev diary for Defense Brigade for now. With our enemies spawning properly now, the main aspects of the game are done. Now all that’s left are the touch ups such as letting the player know how to play the game and ending the game.

# Health and Score
So the space shooter tutorial had a [great section](https://unity3d.com/learn/tutorials/projects/space-shooter/counting-points?playlist=17147) about keeping and displaying score. Using the game controller to update the global variables such as score and health is the best way to make sure  nothing interferes with them, since the game controller interacts with the game but game objects don’t interact with it.
These variables are displayed to the screen with a GUIText object. In the game controller script we have a special function that is called specifically to update the GUIText object. Other functions that subtract health or add to the score are done separately from this.

![The update functions.](https://i1.wp.com/adinashanholtz.com/wp-content/uploads/2015/11/update.png)
<em style="display: block;">The update functions.</em>

Health is a little different from score. Since health is contingent on the weak character’s status, I attached a “gameover” script that keeps track of when the weak character gets hit by an enemy, and updates the game controller’s subtract health function and triggers temporary invincibility accordingly. Additionally, it plays a “hit” sound. I found the code from [this tutorial](https://unity3d.com/learn/tutorials/modules/beginner/live-training-archive/sound-effects-scripting) was very helpful for sound.

# Game Over
Additionally, if the health variable gets below zero, the gameover script will trigger to a game over screen. This is done with  Application.LoadLevel(“Scene name”). One thing to note (which confused me for a bit) is in order to make sure the next scene actually loads when you play the game, you have to add it to your “build”. Just referencing it in the script isn’t enough.

![build](https://i2.wp.com/adinashanholtz.com/wp-content/uploads/2015/11/build.png)

# Instructions
Due to time restrictions, the way I did instructions was pretty quick and simple. I made a sprite with the instructions written on it, and in the game controller script, used the “i” key to toggle the sprite renderer on and off. In addition, in order to “pause” the game while the instructions screen was up, I set the timescale to 0 using  Time.timeScale = 0;. There’s probably a fancier way to do instructions involving GUI layers and text and such, but this method works for this game.

# Deploying
One thing I desperately wish I knew before spending a couple of hours on it was **don’t use Unity web player**. Chrome no longer supports that extension, and most other browsers will have to download it. In addition, I was getting a weird error saying “you do not have permission to view this directly or page” that forced me to write a redirect script in order to get it to work.  Turns out the ~new and improved~ way to do it is with HTML5 WebGL, which is one of the build options in Unity. My lovely coworker Livi has a [perfect blog post](https://livierickson.com/blog/2015/06/03/hosting-a-unity-webgl-game-with-azure-webapps/) about hosting a Unity WebGL game in azure, which is exactly what I did. You can play the final game [here](https://defensebrigade.azurewebsites.net/, and see the final write up of the game I did [here](https://adinashanholtz.com/defense-brigade-game-design-with-unity3d.

Thank you for reading my dev diary. I hope you enjoyed the process of going through creating this Unity game with me. Stay tuned for my next project!

 


