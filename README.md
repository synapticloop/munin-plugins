munin-plugins
=============

Munin plugins for various things which may or may not be handy to you

## apt-get

**Graph the number of available apt packages that can be upgraded/installed/removed and not upgraded**

  1. copy the file to ```/usr/share/munin/plugins/```
  1. ```cd /etc/munin/plugins/```
  1. ```ln -s /usr/share/munin/plugins/apt-get-status apt-get-status```
  1. copy the configuration file ```plugin-conf.d/apt-get-status``` to ```/usr/share/munin/plugin-conf.d/```
  1. ```etc /init.d/munin-node restart``` **__or__**
  1. ```service munin-node restart```

## piwik

**Graph the number of visitors to a any registered piwik sites**

  1. copy the file to ```/usr/share/munin/plugins/```
  1. ```cd /etc/munin/plugins/```
  1. ```ln -s /usr/share/munin/plugins/piwik-num-visits_ piwik-num-visits_piwiksitenumber```
  1. ```etc /init.d/munin-node restart``` **__or__**
  1. ```service munin-node restart```

To determine the piwik site number

  1. Sign in to your piwik installation
  1. Go to ```Settings``` (top right hand corner of the site)
  1. Click ```Websites``` from the left hand side navigation

And the site number will be listed in the table.

for example, for site number 7, you should:

  1. ```ln -s /usr/share/munin/plugins/piwik-num-visits_ piwik-num-visits_7```

You will also need to place a configuration file in the ```/etc/munin/plugin-conf.d``` directory which contains your site url and piwik authorisation key in it.

There is an example file in the ```conf``` directory.


## seo

  1. Graph the google page rank for any particular site

## ssl-expiry

**Graph the number of days until an SSL cerificate for a domain expires**

To activate this munin plugin

  1. copy the file to ```/usr/share/munin/plugins/```
  1. ```cd /etc/munin/plugins/```
  1. ```ln -s /usr/share/munin/plugins/ssl-expiry_ ssl-expiry_www.yourdomain.name.com```
  1. ```etc /init.d/munin-node restart``` **__or__**
  1. ```service munin-node restart```



## stripe

  1. Graph the stripe account balance
  1. Graph the number of stripe customers
  1. Graph the number of events

## wordpress

  1. Graph the number of WordPress blogs on wordpress.com
  1. Graph the number of plugin downloads for a particular plugin

