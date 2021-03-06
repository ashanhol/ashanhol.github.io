---
layout: single
title:  "Deploying A Website To Azure"
date:   2015-10-12 15:51:13 -0400   
#categories:  [ ".NET", ".NET Core", "cross platform", "dotnet core", "github", "Open Source", "OSS" ]
---

# Deploying a Website from source control to Azure

We have our website, now how do we get it on the cloud? Using popular source control systems such as GitHub, BitBucket, or CodePlex, it’s easy to use Azure’s built-in features to automate web app deployment. Azure makes it easy to roll back to earlier deployments if necessary.

![Changing the Deployment to Git]({{site.url}}/assets/images/deploying_a_website_to_azure/azure5-disconnect.png)
<em style="display: block">Changing the Deployment to Git</em>

<!-- List -->
**How to set up step-by-step**
* There are step by step instructions [here](https://azure.microsoft.com/en-us/documentation/articles/web-sites-publish-source-control/), starting at “Deploy your Project”.
* Other useful (more in depth) source [here](https://www.asp.net/aspnet/overview/developing-apps-with-windows-azure/building-real-world-cloud-apps-with-windows-azure/source-control).
* A video on deploying from GitHub with Kudu [here](https://channel9.msdn.com/Shows/Azure-Friday/Deploying-to-Web-Sites-with-GitHub-using-Kudu-with-David-Ebbo).

 
# Deploying a standard website with Azure using Visual Studio Community

Visual Studio is a Microsoft IDE that is useful for web development and makes it easy to deploy web apps. Visual Studio offers more features, such as creating and deleting web apps, viewing logs as they are created in real-time, debugging remotely, and most importantly, integrating with source control systems such as Git repositories.

![Publishing the application in Visual Studio]({{site.url}}/assets/images/deploying_a_website_to_azure/choosepublish.png)
<em style="display: block">Publishing the application in Visual Studio</em>

**How to set up step-by-step**
* This [tutorial](https://azure.microsoft.com/en-us/documentation/articles/web-sites-dotnet-get-started/) is for a project coded in ASP.NET, however the steps are still the same whether you have a Visual Studio project in HTML/CSS, or JavaScript.

# Deploying a Python website to Azure

Want to use the useful Python framework Flask with the Azure cloud? Then look no further! You’ll create the website from the Azure gallery, set up Git deployment, and clone and run the repository locally. When you need to make changes, you can commit and push them to Azure.

![ptvs-solution-flask]({{site.url}}/assets/images/deploying_a_website_to_azure/ptvs-solution-flask.png)
<em style="display: block">Coding a Flask web app in Visual Studio</em>

![Running a Flask web app locally.]({{site.url}}/assets/images/deploying_a_website_to_azure/windows-browser-flask.png)
<em style="display: block">Running a Flask web app locally.</em>

<!-- List -->
**How to set up step-by-step**

* [Here](https://azure.microsoft.com/en-us/documentation/articles/web-sites-python-create-deploy-flask-app/) are step-by-step instructions on deploying flask to Azure.
* For those that would like a video walkthrough, module 6 of [this video](https://www.microsoftvirtualacademy.com/training-courses/introduction-to-creating-websites-using-python-and-flask) will help.

 
# Deploying a Ruby website to Azure

Want to use Ruby on Rails with the Azure cloud? Then look no further! You’ll create an Azure VM with a Linux image and deploy it to the cloud.

![Virtual Machines List]({{site.url}}/assets/images/deploying_a_website_to_azure/vmlist.png)
<em style="display: block">Virtual Machines List</em>

![Ruby on Rails web app running on Azure]({{site.url}}/assets/images/deploying_a_website_to_azure/basicrailscloud.png)
<em style="display: block">Ruby on Rails web app running on Azure</em>

<!-- List -->
**How to set up step-by-step**

* Step-by-step instructions on deploying a Ruby on Rails VM to Azure [here](https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-ruby-rails-web-app-linux/).
* Useful [link](https://azure.microsoft.com/en-us/develop/ruby/).
