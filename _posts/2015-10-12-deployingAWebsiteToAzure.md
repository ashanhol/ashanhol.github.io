---
layout: single
title:  "Deploying A Website To Azure"
date:   2015-10-12 15:51:13 -0400   
#categories:  [ ".NET", ".NET Core", "cross platform", "dotnet core", "github", "Open Source", "OSS" ]
---

# Deploying a Website to Azure

12 Oct, 2015  in Blog Posts  tagged Azure / coding / deploying a website / github / hackathon / programming / visual studio / website by adinas
Deploying a website from source control to Azure

We have our website, now how do we get it on the cloud? Using popular source control systems such as GitHub, BitBucket, or CodePlex, it’s easy to use Azure’s built-in features to automate web app deployment. Azure makes it easy to roll back to earlier deployments if necessary.

![Changing the Deployment to Git](https://web.archive.org/web/20170716064222im_/http://i2.wp.com/adinashanholtz.com/wp-content/uploads/2015/10/azure5-disconnect.png?w=778)

<!-- List -->
How to set up step-by-step
* There are step by step instructions here, starting at “Deploy your Project”.
* Other useful (more in depth) source here.
* A video on deploying from GitHub with Kudu here.

 
# Deploying a standard website with Azure using Visual Studio Community

Visual Studio is a Microsoft IDE that is useful for web development and makes it easy to deploy web apps. Visual Studio offers more features, such as creating and deleting web apps, viewing logs as they are created in real-time, debugging remotely, and most importantly, integrating with source control systems such as Git repositories.

![Publishing the application in Visual Studio](https://web.archive.org/web/20170716064222im_/http://i2.wp.com/adinashanholtz.com/wp-content/uploads/2015/10/choosepublish.png?w=526)

<!-- List -->
How to set up step-by-step

    This [tutorial](https://web.archive.org/web/20170716064222/https://azure.microsoft.com/en-us/documentation/articles/web-sites-dotnet-get-started/) is for a project coded in ASP.NET, however the steps are still the same whether you have a Visual Studio project in HTML/CSS, or JavaScript.

# Deploying a Python website to Azure

Want to use the useful Python framework Flask with the Azure cloud? Then look no further! You’ll create the website from the Azure gallery, set up Git deployment, and clone and run the repository locally. When you need to make changes, you can commit and push them to Azure.

![ptvs-solution-flask](https://web.archive.org/web/20170430011848/http://i2.wp.com/adinashanholtz.com/wp-content/uploads/2015/10/ptvs-solution-flask.png)
<caption>Coding a Flask web app in Visual Studio</caption>

![windows-browser-flask](https://web.archive.org/web/20170430011848/http://i1.wp.com/adinashanholtz.com/wp-content/uploads/2015/10/windows-browser-flask.png)

![Running a Flask web app locally.](https://web.archive.org/web/20170716064222im_/http://i1.wp.com/adinashanholtz.com/wp-content/uploads/2015/10/windows-browser-flask.png?w=524)

<!-- List -->
How to set up step-by-step

[Here](https://web.archive.org/web/20170716064222/https://azure.microsoft.com/en-us/documentation/articles/web-sites-python-create-deploy-flask-app/) are step-by-step instructions on deploying flask to Azure.
For those that would like a video walkthrough, module 6 of [this video](https://web.archive.org/web/20170716064222/http://www.microsoftvirtualacademy.com/training-courses/introduction-to-creating-websites-using-python-and-flask) will help.

 
# Deploying a Ruby website to Azure

Want to use Ruby on Rails with the Azure cloud? Then look no further! You’ll create an Azure VM with a Linux image and deploy it to the cloud.

![Virtual Machines List](https://web.archive.org/web/20170716064222im_/http://i2.wp.com/adinashanholtz.com/wp-content/uploads/2015/10/vmlist.png?w=650)

![Ruby on Rails web app running on Azure](https://web.archive.org/web/20170430011848/http://i1.wp.com/adinashanholtz.com/wp-content/uploads/2015/10/basicrailscloud.png)

<!-- Ruby on Rails web app running on Azure -->

<!-- List -->
How to set up step-by-step

    Step-by-step instructions on deploying a Ruby on Rails VM to Azure [here](https://web.archive.org/web/20170716064222/https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-ruby-rails-web-app-linux/).
    Useful [link](https://web.archive.org/web/20170716064222/http://azure.microsoft.com/en-us/develop/ruby/).
