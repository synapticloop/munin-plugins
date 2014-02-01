munin-plugins
=============

Munin plugins for various things which may or may not be handy to you

## piwik

  1. Graph the number of visitors to a any registered piwik sites

## seo

  1. Graph the google page rank for any particular site

## ssl-expiry

Graph the number of days until an SSL cerificate for a domain expires

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

