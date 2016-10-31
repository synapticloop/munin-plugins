# Newznab

Handy munin graph creator for newznab based installations.

# Requirements


 - Munin (of course)
 - Python

# Installation

## Python

>     sudo apt-get install python

# Munin Configuration

copy the file `plugin-conf.d/newznab_parts_left` to `/etc/munin/plugin-conf.d/newznab_parts_left`

i.e.:

>     cp plugin-conf.d/newznab_parts_left /etc/munin/plugin-conf.d/

Edit the `newznab_parts_left` file to change the following values:

>     env.NEWZNAB_LOG_FILE /var/log/newznab/newznab.log


## `newznab_parts_left`

This script is used to generate the number of parts left to be indexed.

You must know the path to your newznab log file - the default setting `/var/log/newznab/newznab.log`

>     cd /etc/munin/plugins
>     ln -s /usr/share/munin/plugins/newznab_parts_left newznab_parts_left

Then restart the munin node

>     /etc/init.d/munin-node restart

~or~ 

>     service munin-node restart