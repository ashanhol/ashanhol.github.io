---
layout: single
title:  "Dev Diary- Unity3D game Defense Brigade part 1"
date:   2015-11-24 19:57:46 -0400
#categories:  [ "Dev Diary", "Game Design", "programming", "Unity" ]
---

Hey all! I’m starting a segment called Dev Diary to track progress when I start projects. Right now I’m working on a game in Unity3D which has the working title Defense Brigade.  This will be a place for me to post bits and pieces of unfinished projects, hurdles that I’ve run into, etc.

# Idea
Basically it’s a 2-D game with top down perspective, and functions so that you use both WASD and arrow keys to control. You are controlling two characters, a weak character that’s vulnerable to enemy attacks and if hit will trigger a game over, and a strong character that’s invincible and will destroy enemies when running into them. The objective is to get the highest score.

# Character Movement
The first thing I did was create character movement. The characters themselves are default sprites I found already loaded into Unity. It’s easier to get the basic game working with minimal art and add in fancier sprites and animation later.

![characters]({{site.url}}/assets/images/dev_diary_defense_brigade_part_1/characters.png)
<em style="display: block;">The two characters and camera. Picture taken after game completion.</em>

As for movement, a good chunk of the tutorials expect only one character and therefore use Input.GetAxis to get the horizontal and vertical movements. This makes sense as that method automatically adjusts to varying frame-rates. However, that method reads for both arrow keys and WASD, which meant I couldn’t use it for both characters since they would end up moving together. So instead I calculated velocity based on a vector that was updated by individual key presses. That way I could move only the strong character with WASD, and only the weak character with the arrow keys.  As for flipping horizontally and vertically, I multiplied the local scale by -1 as suggested by [this tutorial](https://unity3d.com/learn/tutorials/modules/beginner/2d/2d-overview?playlist=17093).

![Movement code]({{site.url}}/assets/images/dev_diary_defense_brigade_part_1/movementcode.png)
<em style="display: block">Movement code for the strong character.</em>

After character controllers I then made boundaries so the player wouldn’t go off the screen accidentally. This was just giving colliders to the characters and off screen boxes.

After seeing how sprites interact with this world I feel as if I can take the next steps into a 2.5-D game (where the world and characters are 3-D but the player only interacts with the world in a 2-D way).

![The New Super Marios - screenshot]({{site.url}}/assets/images/dev_diary_defense_brigade_part_1/nsmbwhd06.jpg)
<em style="display: block">The New Super Mario Bros is an example of a 2.5-D game, where Mario and the enemies are 3-D but the game is played 2-D, the same way as the original.</em>

That’s it for now. For more in my development adventure, see the next dev diary post 😊

