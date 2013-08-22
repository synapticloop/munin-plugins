stripe
======

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
