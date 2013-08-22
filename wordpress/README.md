Wordpress
=========

Handy munin graph creators for various [wordpress](http://www.wordpress.org) 
related downloads and installations


Requirements
============

 - Munin (of course)
 - Python

Installation
============

## Python

>     sudo apt-get install python

## wordpress

Count the number of wordpress blogs running in the wild

### Installation

>     sudo cp wordpress /usr/share/munin/plugins/wordpress
>     sudo cd /etc/munin/plugins
>     sudo ln -s /usr/share/munin/plugins/wordpress wordpress
>     sudo /etc/init.d/munin-node restart

## wordpress_plugin_download_counter_

Count the number of wordpress plugin downloads

### Installation

This script is used to generate data for several graphs. To generate data for
one specific wordpress plugin instance, you need to create a symbolic link
with a name like wordpress_plugin_download_counter_<NAME> to this script.
For example: to track the WP Super Cache number of downloads

The URL for it is 

>     http://wordpress.org/plugins/wp-super-cache/

So you would use the following

>     wp-super-cache

as the name, so to start munin monitoring the downloads for WP Super Cache

>     sudo cp wordpress_plugin_download_counter_ /usr/share/munin/plugins/wordpress_plugin_download_counter_
>     sudo cd /etc/munin/plugins
>     sudo ln -s /usr/share/munin/plugins/wordpress_plugin_download_counter_ wordpress_plugin_download_counter_wp-super-cache
>     sudo /etc/init.d/munin-node restart
