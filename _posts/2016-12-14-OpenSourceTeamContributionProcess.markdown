---
layout: single
title:  "Open Source Team Contribution Process"
date:   2016-12-14 15:53:10 -0400
#categories:  [ ".NET", ".NET Core", "C#", "coding", "Dev Diary", "development", "dotnet core", "Git", "github", "JabbR", "Open Source", "OSS", "programming", "projects" ]
---

A little bit ago I made a [blog post](http://ashanhol.github.io/contributing-to-open-source/) detailing an open source project I worked on called JabbR. It was waaaaay to hard to cram everything we learned into one blog post, so I’m dedicating this to discussing the “JabbR-Core Process”.
Breaking it down:

* [Where did we start? Porting vs. Refactoring & Re-architecting.](#step-one-starting)
* [Git](#git)
* [Workflow Tooling](#tools-for-workflow)
* [Working with teammates](#working-with-teammates)

# [Step One Starting](#step-one-starting)


Despite my years of experience and the fancy piece of paper that says I officially studied computer science in college, I had never “ported” something from one technology to another. I didn’t even know where to start. We had two options, either totally re-write the code from scratch and redesign the architecture using the original JabbR as a guideline (the refactor and re-architect option), or copy large sections of the code base and rewrite only what we need to. Luckily for us, we had help from [David Fowler](https://twitter.com/davidfowl), the original creator of JabbR, who helped us make the decision. At his suggestion, we started with a brand new ASP.NET Core project and brought over files ones by one, setting up what we needed in order to make it run. Just run, not necessarily do anything.

For ASP.NET Core, this meant making sure files like our Startup.cs and Project.JSON were configured properly and pointing to the right places, dragging over the the front end scripts, configuring the project to use MVC (model-view-controller), and making a new HomeController that would return the front page. Once you see something working, you move on to trying to get the next feature to work by dragging over as much as you can and re-writing what you need. Rinse and repeat!

…I promise it’s not as easy as it sounds. The part that’s conveniently left out is the hours spent falling down rabbit holes trying to figure out which files rely other files to function. We were truly deceived by how quick it was to set up and see the loading screen, as it took another couple of weeks to get past that loading screen.

# [Git](#git)

If you don’t know what git is, I’ll point you to this [handy guide](http://www.tobiahz.com/2014/08/intro-git-github-0/) my awesome coworker Tobiah Zarlez wrote.
Basically using git for the first half of this project was like this.

![XKCD_Git.png](http://i2.wp.com/imgs.xkcd.com/comics/git.png?resize=330%2C478)

I never thought I would get to the point where it didn’t feel like that comic, but even though I still have to look up the merge command to make sure I don’t go the wrong way, I actually feel comfortable with this tool. Our team’s version of “friend you call who knows git” was [James Earle](https://twitter.com/ItsJamesIRL). It’s always really great to work with someone who’s not afraid to jump in and try to fix a messy issue when you’re first learning.

Here are some **common mistakes** our team ran into while working on this project:

* Not actually adding your changes when trying to commit.
   -Turns out `git add .` doesn’t add from the directory above you.

![Commits.png](http://i1.wp.com/adinashanholtz.com/wp-content/uploads/2016/12/overvio.jpg?resize=1024%2C593)

After creating a pull request, not merging in the latest copy of the destination branch into your source branch.
-Not gonna lie, git seems like a bunch of magic when you’re first using it. I didn’t quite understand what was going on when you accepted a pull request, so I would make my features, have someone test them, then have my pull request merged in. For reference, _**DON’T DO THAT**_. We’d run into situations where suddenly our main branch would no longer work. What I should have done was after testing my features, merge in the latest copy of the main branch, have someone else test it and :shipit:, then accept my pull request.

![Commits.png](http://i1.wp.com/adinashanholtz.com/wp-content/uploads/2016/12/pr.png?resize=1024%2C571)

* Windows vs. Unix capitalization differences.
    -Did you know that Unix and Windows systems are different in how they see lowercase vs. upercase versions of files? It would have [saved me a lot of time](https://github.com/MachUpskillingFY17/JabbR-Core/pull/305) to know index.cs is not the same as Index.cs, and will make my build crash on a Unix machine. One more reason to always test your application on multiple kinds of systems.
    -We also ran into trouble with pushing to Github from our systems running Windows, and seeing two versions of the same file with different capitalization on Github but not on our local machines.

# Tools for Workflow
We wanted everything about the JabbR-Core project to be as close to the OSS development teams at Microsoft as possible, all the way down to the workflow process. Software development isn’t exactly new, so you’d think by now there’d be an official way to do “team workflow”.
Not really.
We started by using the same tool used by the .NET Core team, which aggregated data from Github and displayed what everyone was working on. However, that’s really all it did- display your open issues. There wasn’t really anything other than Github itself to use for other things like managing milestones, finding issues, etc. We were several weeks into the project before we realized we were creating much more work for ourselves combing through lists of everything that’s open, trying to organize it the way we needed.
So we switched to this tool called Overv.io (pronounced overview?), that’s built on top of Github.

![Commits.png](https://web.archive.org/web/20170704165953im_/http://i1.wp.com/adinashanholtz.com/wp-content/uploads/2016/12/overvio.jpg?resize=1024%2C593)

Overv.io doesn’t create things that Github doesn’t have, it just lets you customize your workflow by displaying the data in a way that’s easiest for your team. The “In Progress” and “Blocked” tabs are just tags on an issue, but displayed in a way that let’s us view our workflow. It also has some nifty sorting features such as seeing which issues have gotten to old (or “toxic”), blocking/greying out certain users to better see what people are working on, and even lets you create issues in bulk.

Finding the right tool for our team made all the difference. We had all the data before, but refining the process saved us time and helped with our daily standups.

# [Working with Teammates](#working-with-teammates)
Ok, I know what I’m about to say is not the most popular opinion, but I actually like working on a team and coding with other people. It’s always been my experience both in and out of college that compsci people prefer to work alone. I’m actually the opposite- not only do I prefer to work with other people, but I actually do much better working with others. I realized my senior year of college that I actually excel while pair-programming.

I realized this all over again while on this project for a number of reasons.

The very first day of our project, I experienced something called “mob programming”. It’s exactly what it sounds like: one person sitting at the computer while a group of people (in this case really brilliant people on the .NET Core team) puzzle out code and tell them what to type. You might think “that sounds like the worst thing ever”, and it was, it was terrifying. It was also the best thing ever. I personally puzzle out problems by talking things out and bouncing ideas around, and there’s no better way to experience ideas bouncing around than mob programming. The team was patient while I learned new hotkeys, and no one did this.

Another instance that stood out happened while I was pair programming with a teammate. While preparing for this project, I decided to focus a lot on learning C# and [LINQ](https://msdn.microsoft.com/en-us/library/bb397906.aspx) queries. We were working on a section of code, when I realized that the LINQ queries that she wrote weren’t getting iterated over. In LINQ, without an iterator like a foreach loop or .first() or .ToArray(), statements won’t evaluate properly. Catching this and working to rewrite it saved us a future debugging headache.

I’m at the point in my career where everyone has experience in different areas. Being able to collaborate with people who have different experiences definitely helps with problem solving.

