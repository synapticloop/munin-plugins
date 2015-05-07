Piwik
=========

Handy munin graph creators for various [piwik](http://piwik.org) 
statistics at a glance


Requirements
============

 - Munin (of course)
 - Python

Installation
============

## Python

>     sudo apt-get install python

Munin Configuration
===================

copy the file conf/piwik to /etc/munin/plugin-conf.d/piwik i.e.:

>     cp conf/piwik /etc/munin/plugin-conf.d/

Edit the piwik file to change the following values

>     env.piwik.url https://your.piwik.server.com
>     env.piwik.token_auth YourAuthKeyGoesHere


## piwik-num-visits_

This script is used to generate data for several graphs of number of visits
per site for the piwik installation.

You must know the site number of your piwik installation and create a
symbolic link to the site number that you wish to track

For example to track site 1

>     cd /etc/munin/plugins
>     ln -s /usr/share/munin/plugins/piwik-num-visits_ piwik-num-visits_1
>     /etc/init.d/munin-node restart
