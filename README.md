Deployogi
=========
The yoga of autodeployment, in other words: putting a new version of a website in production by simply hitting enter.

Why?
====
To move away from handhacking webapplications into production.
So teams can deploy and upgrade many webapplications in one and the same way.
The maintaining-upgrade-test-and-deploy-cycle for many webapplication can be done in many ways, and therefore can a 
counterproductive effect on deadlines. 

Demonstration
=============
Check the following link to see a very basic tutorial/showcase(http://playterm.org/r/deployogi-automatic-webdeployment-1375465953)

> `NOTE`: the showcase is very basic, and does not really show how to extend deployogi. Many webframework support triggering of testing, 
> configuration thru console. Please keep in mind that deployogi has been designed to specifically trigger these things, in order to 
> find out if the deployment is going good or bad (and alternatively refuse to deploy). 

For who?
========
Well not for one-man-banddevelopers, in those cases handhacking is part of the fun!
But in case of a devteam it is the only way to be flexible in scalability of your team.
Actually `deployogi` applies to Rule 14 of the UN*X philosophy: *Rule of Generation: Avoid hand-hacking; write programs to write programs when you can.*, 
so if you like unix, you'll like this as well. 

How?
====
Simply by pushing to a remote git-repository.
Only thing to do once is writing a config-file. 
Thats it!
Further extension can be done using deployogi hook-scripts (n a similar fashion as git hooks)

Are git hooks not enough?
=========================
No, if you dive into this matter you'll soon find out there will be many obstacles because [GIT is not a deploymenttool](http://gitolite.com/the-list-and-irc/deploy.html) 

Requirements
============

* LAMP server
* a webapplication which supports cli-invokation (to configure frameworkrelated variables from the commandline)
* you have to know about of commandline (bash) stuff 

Installation
============
For now lets assume you wanna get started asap, then copy/paste this oneliner into your terminal :

    wget "https://raw.github.com/coderofsalvation/deployogi/master/deployogi" -O deployogi; chmod 755 deployogi; 

Then run:

    ./deployogi

Workflow / the philosophy behind this deploymenttool/model
==========================================================
Deployogi assumes a push-backup-clone-merge-test and compare-deploymentmodel.
Read [this article](http://leon.vankammen.eu/blog/automatic-deployment-with-git-and-deployogi-scripts) to learn more about it.
Here you can see the simplest way of deploying (for more details read article) : 

<img src="https://dl.dropboxusercontent.com/s/88zzcgb4hp9k641/seqdiagram-deployogi-easy.png?dl=1"> 

