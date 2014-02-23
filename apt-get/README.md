apt-get-status
==============

This is a plugin to chart the apt status of a system

Requirements
============

 - Munin (of course)

Munin Configuration
===================

copy the file plugin-conf.d/apt-get-status to /etc/munin/plugin-conf.d/apt-get-status i.e.:

>     cp plugin-conf.d/apt-get-status /etc/munin/plugin-conf.d/

### Installation

To install the munin plugin - do the following

>     sudo cp apt-get-status /usr/share/munin/plugins/apt-get-status
>     sudo ln -s /usr/share/munin/plugins/apt-get-status /etc/munin/plugins/apt-get-status
>     sudo /etc/init.d/munin-node restart
