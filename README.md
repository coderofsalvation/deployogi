Deployogi
=========
Deployogi is a bashscript which enables easy, automatic deployment of webapplications/databases on staging/production webservers using GIT hooks and bash triggers.

Say What?
=========
in other words: putting a new version of a website in production by simply hitting enter.

Why?
====
So teams can deploy many webapplications in one and the same way.
The maintaining-upgrade-test-and-deploy-cycle for many webapplication can be done in many ways. 
Handhacking this process *will* become more and more labourous/specialized as the webapplications mature.

For who?
========
Well not for one-man-banddevelopers, in those cases handhacking is part of the fun!
But in case of a devteam it is the only way to be flexible in scalability of your team.

How?
====
Simply by pushing to a remote git-repository.
Only thing to do once is writing a config-file and optionally some triggerfiles ('on.backup' / 'on.update' e.g.).
Thats it!

Example workflow
================
Lets assume you have at least one application maintainer (who merges gitbranches into staging- and master-branch) and developers
who create feature-branches. 

Requirements
============

* LAMP server
* a webapplication which supports cli-invokation (to configure frameworkrelated variables from the commandline)
