---
layout: single
title:  "Contributing to Open Source"
date:   2016-11-21 14:46:14 -0400        
#categories:  [ ".NET", ".NET Core", "cross platform", "dotnet core", "github", "Open Source", "OSS ]
---

It’s been a while since I made a blog post. Looking back, seems like I jumped from project to project, since the last thing I did was release [Silent Dream]({{site.url}}/2016/11/21/silentDream.html). I’m excited to talk about what I’ve been up to!

The last four months I have been contributing to an open source project called [JabbR](https://github.com/MachUpskillingFY17/JabbR-Core). I’ve learned so much from this experience, I’m breaking it up into other blog posts about our [team process]({{site.url}}/2016/12/14/open-source-team-contribution-process.html), .NET Core technology, and bundling.

In this particular post, I’ll discuss what it means to [have a project be open source]({{site.url}}/2016/11/21/contributing-to-open-source.html#what-is-open-source), how to [contribute to open source]({{site.url}}/2016/11/21/contributing-to-open-source.html#how-to-contribute) projects, and give an [overview of the project]({{site.url}}/2016/11/21/contributing-to-open-source.html#what-is-jabbr) I worked on.

What is Open Source?
The answer to this might seem intuitive. Open source = access to source code.
While this is true, there are more criteria that define open source projects. Open source software must allow free redistribution, allow derived works, and not discriminate on usage or people, as well as have a licence that doesn’t restrict other software and be technology neutral. A full list can be found here on [opensource.org](https://opensource.org/osd-annotated).
There are multiple licenses that open source projects use, such as the [MIT License](https://opensource.org/licenses/MIT) or the [GNU Public License](https://www.gnu.org/licenses/gpl-3.0.en.html).

TLDR; Basically, show your code for free, allow people to see/learn from/redistribute your code, don’t discriminate or hinder anyone/anything in the process.

What’s this JabbR project thing?
Unless you’re in the .NET community , you’re probably not familiar with JabbR. [JabbR](https://github.com/JabbR/JabbR) is an IRC style chat application built with ASP.NET and SignalR (for those not familiar with what .NET is, it was written in C#). If you clicked the link you saw the original JabbR GitHub repo. When our team picked up the project, the last commit happened 3 years prior. In fact, the original hosting website had to be taken offline as its SSL certificate had just expired. So we decided to revamp this site by porting it over to [.NET Core](https://github.com/dotnet/core).

So why did I, a Technical Evangelist who just released a game, pivot so suddenly? As it turns out, when I first took this job, I had no official training to get started. Coming out of college, I was confused and overwhelmed on every aspect of the job. While I’ve learned so much in my first year, I still didn’t have any formal developer experience on a large team project (despite being a computer science major).

There is no better way to learn these skills than hands on experience.

If I hadn’t joined this project, I would have never looked at .NET, even though it’s a core Microsoft technology. We specifically focused on the new .NET Core stack, which is cross platform and open source. By tackling this technology, I definitely leveled up my C# skills, which not only helps me in Unity, but also helps me expand to cross platform technologies like [Xamarin](https://www.xamarin.com/).

How do I contribute to Open Source Projects?
I thought the idea of contributing to a big open source project sounded really cool, I just never imagined that it would be really easy or I could do it any time I wanted.
You can contribute in a number of ways. Take the time to explore GitHub to see projects out there. Before I started this project, I would go to a project on GitHub, maybe click around the code to try and figure it out, and give up because that’s a terrible way to try and figure out what’s going on in a project.
Here’s the tricks:

Open source projects that want community contributions will sometimes have a document that say CONTRIBUTING, listing ways you can help out.
The Issues tab is your best friend. Projects will keep tags you can peruse that say “help wanted” or “bug” or “enhancement”.
If you’re not comfortable with contributing code at first, sometimes spell check fixes are a good way to do your first commit.
Actually, [Scott Hanselman](https://www.hanselman.com/), who supported our project, has this really cool site called [First Timers Only](https://www.firsttimersonly.com/), which is dedicated to encouraging people to contribute for the first time to open source projects.

Story time.
Not gonna lie, when I was trying to wrap my head around contributing to an open source project in college, a friend told me to “just write a test”. I was too insecure as a computer science major to reply that I didn’t know how to do that. A year+ out of college and now I know how, because of this project.