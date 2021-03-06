---
layout: lab
title: 2. Login and Tour of Red Hat Mobile Application Platform
subtitle: A guided tour of Red Hat Mobile Application Platform
html_title: Login and Tour of Red Hat Mobile Application Platform
categories: [lab, intro, welcome, developers, ops]
---

## Welcome to Red Hat Mobile Application Platform !

This lab provides a quick tour of the console to help you get familiar with the user interface along with some key terminology we will use in subsequent lab content.  If you are already familiar with the basics of Red Hat Mobile Application Platform you can skip this lab - after making sure you can login.

## Key Terms
We will be using the following terms throughout the workshop labs so here are some basic definitions you should be familiar with.  And you'll learn more terms along the way, but these are the basics to get you started.

* Project - Projects help you group all code bases related to a single mobile application in one place.
* Client App - Applications deployed on mobile devices used by the end users.
* Cloud App - Applications deployed in the mBaaS that handle requests from client apps and communicate with other internal or external systems.
* mBaaS Service - Reusable services used by cloud apps and shared across multiple projects.
* FHC - FeedHenry Command Line tool used to access the platform.  
* Studio - The Red Hat Mobile Application Platform's web interface used to help developers and operations work together to build mobile apps.

## Accessing Red Hat Mobile Application Platform
Red Hat Mobile Application Platform or RHMAP provides a web console that allow you to perform various tasks via a web browser.  Additionally, you can utilize a command line tool to perform tasks.  Let's get started by logging into both of these and checking the status of the platform.

### Let's Login
<blockquote>
<i class="fa fa-desktop"></i> Navigate to the URI provided by your instructor and login with the user/password provided (if there's an icon on the Desktop, just double click that)
</blockquote>

<img src="{{ site.baseurl }}/www/4.2/default/screenshots/rhmap-login.png" width="600"/><br/>
   *Login Webpage*

Once logged in you should see your available actions.  Administrator's have access to Role and user based control to alter what appears on this home screen.
<img src="{{ site.baseurl }}/www/4.2/default/screenshots/rhmap-homepage.png" width="600"/><br/>
   *homepage with admin access*

## Let's take a look at what a project looks like
First let's open a project.  Select the project named "Welcome Project."

<img src="{{ site.baseurl }}/www/4.2/default/screenshots/rhmap-threecolumn.png" width="600"/><br/>
*project home*

In this screen you will note the three columns: Client apps, Cloud apps and mBaaS Services.  A project Must contain a Cloud App and a Client apps.  mBaaS Services are an optional albeit extremely powerful tool to work with pre-existing systems and API's.

### Command Line Login
Let's now login to the platform through the command line tool, "FHC".  to get started we need to set the platform target:
<blockquote>
<i class="fa fa-terminal"></i> Type this in terminal(replace [lab-studio-domain] with the studio domain provided to you):
</blockquote>
{% highlight csh %}
$ fhc target https://[lab-studio-domain].us.demos.redhatmobile.com
{% endhighlight %}

We can then login using the credentials your instructor provided you:
<blockquote>
<i class="fa fa-terminal"></i> Type this in terminal(replace 'username' and 'password' with the credentials provided to you.):
</blockquote>
{% highlight csh %}
$ fhc login username password
{% endhighlight %}


You can view a list of projects you have access to:
<blockquote>
<i class="fa fa-terminal"></i> Type this in terminal:
</blockquote>

```
Note: This command may take some time.
```
{% highlight csh %}
$ fhc projects
{% endhighlight %}


<img src="{{ site.baseurl }}/www/4.2/default/screenshots/rhmap-fhc-projects.png" width="600"/><br/>
*fhc projects list*

## What's coming up
To get started with Red Hat Mobile Application Platform (RHMAP) quickly, the first step is to understand the project life cycle. This involves creating a project, creating a client and a cloud app from templates, deploying the cloud app to the mBaaS, building the client app, and deploying it to a mobile device.  We will learn about Node.js and do a little development with it.  
