Deployogi
=========
The yoga of autodeployment, in other words: putting a new version of a website in production by simply hitting enter.

Why?
====
To move away from handhacking webapplications into production.
So teams can deploy and upgrade many webapplications in one and the same way.
The maintaining-upgrade-test-and-deploy-cycle for many webapplication can be done in many ways, and therefore can a 
counterproductive effect on deadlines. 

For who?
========
Well not for one-man-banddevelopers, in those cases handhacking is part of the fun!
But in case of a devteam it is the only way to be flexible in scalability of your team.
Actually `deployogi` applies to Rule 14 of the UN*X philosophy: *Rule of Generation: Avoid hand-hacking; write programs to write programs when you can.*, 
so if you like unix, you'll like this as well. 

How?
====
Simply by pushing to a remote git-repository.
Only thing to do once is writing a config-file and optionally some triggerfiles ('on.backup' / 'on.update' e.g.).
Thats it!

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

Example workflow
================
Lets assume you have at least one application maintainer (who merges gitbranches into staging- and master-branch) and developers
who create feature-branches. 
