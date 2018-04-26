---
layout: single
title:  "PhaserBrigade: Defense Brigade using Phaser.js"
date:   2016-01-14 02:09:39 -0400 
#categories:  [ "Game Design", "Game Development", "gaming", "phaser", "phaser.js", "programming" ]
---

![Phaser Brigade]({{site.url}}/assets/images/phaser_brigade/Screenshot-2.png)
<em style="display: block;">Phaser Brigade</em>

So in my tour around different game creation tools, I’ve so far done [Construct2](https://channel9.msdn.com/Blogs/raw-tech/Intro-To-Construct2-Course), GameMaker, Unity, and have finally worked my way to [Phaser.js](https://phaser.io/tutorials/getting-started). I recently designed a game called [Defense Brigade](https://adinashanholtz.com/2015/11/24/defense-brigade-game-design-with-unity3d/), which was designed with Unity, so what better way to learn a new game design tool than to recreate a simple game! Phaser is an open source framework that allows you to create games powered by WebGL and Canvas. I found their [tutorial](https://phaser.io/tutorials/making-your-first-phaser-game) on making your first game to be immensely helpful and it allowed me to jump right in. Phaser is very straightforward for those who have a stronger programming background, and reminded me a lot of using [Processing](https://processing.org/). That said, here are some thoughts I had while making this project.
 
# Server
The first thing Phaser asks you to do in order to get started is set up a local server in order to test your game. This is so the game can run unhindered in your browser, which it can’t if you’re running it in the local file system. Phaser games need to reference assets in other folders (like your sprite images, audio, etc). Now I’ve used Node.js as a backend for projects before, but I thought I’d try something new, and Phaser recommended  [Wamp server](https://www.wampserver.com/en/) if you were running Windows. The benefit of a development environment like that is it installs Apache, PHP and MySQL and can be turned on and off from the comfort of your toolbar. Not as l33t as running a node http-server from the command prompt but oh well.

**Problem:** When I downloaded Wamp for Windows 10, it kept giving me a a message saying that it couldn’t bind to port 80. After great use of my search engine, using the command “netsh winsock reset” in command prompt fixed it.

After I got it up and running, Wamp worked great for this. All I had to do was go to localserver/phaserbrigade and it would run the game no problem.

# Conceptualizing
Using Phaser to design games was a very different experience from other programs like GameMaker or Unity. Those programs have a user interface that allowed the designer to drag and drop within a scene view to see a version of the level or scene before you play it. Since Phaser is a framework, you gotta create games the ol’ fashion way- by ~coding~. This is nothing new to me as I was a Computer Science major before I became a game developer, so I’m used to sketching out the architecture of a program (or in this case, the level in a game) on paper and pencil. It might be a little unusual at first if you’re not used to that, but as long as you’re running your server you can immediately test your code.

I used [Visual Studio Code](https://code.visualstudio.com/) to write the code for my level. It worked very well and syntax highlighted exactly the way I like it. VS Code works especially well for JavaScript projects as it allows for easy switching between multiple open files in a project, which you’re very likely to have in a Phaser game.

![Coding Phaser in VS Code]({{site.url}}/assets/images/phaser_brigade/Screenshot-3.png)
<em style="display: block;">Here’s an example of PhaserBrigade in VS Code</em>

# Getting Started
If you’re looking to get started with Phaser, their website has an [incredible amount of tutorials](https://phaser.io/learn/official-tutorials) that are constantly added to by the community. The [API Documentation](https://phaser.io/docs/2.4.4/index) is quite good, and they have a whole page dedicated to [examples](https://phaser.io/examples) such as audio, different physics systems, and text.

If you make something cool, let me know! (Or leave a comment.)


