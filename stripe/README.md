stripe
======

This is a list of plugins for the truly excellent [Stripe](http://www.stripe.com) 
payment gateway.

Requirements
============

 - Munin (of course)
 - Python (version 2.6 or greater for JSON parser)
 - pip Installer
 - Stripe Python API

Installation
============

## Python

>     sudo apt-get install python

## pip Installer

>     sudo apt-get install python-pip

## Stripe Python API
>     pip install --index-url https://code.stripe.com --upgrade stripe

Munin Setup
===========

copy the file conf/stripe to /etc/munin/plugin-conf.d/stripe i.e.:

>     cp conf/stripe /etc/munin/plugin-conf.d/


## stripe_customer_count

Provide a running total of the number of customers that are in your stripe account

### Installation

>     sudo cp stripe_customer_count /usr/share/munin/plugins/stripe_customer_count
>
>     sudo cd /etc/munin/plugins
>
>     sudo ln -s /usr/share/munin/plugins/stripe_customer_count stripe_customer_count
>
>     sudo /etc/init.d/munin-node restart

## stripe_account_balance

Provide a running of the balance of your stripe account

### Installation

>     sudo cp stripe_account_balance /usr/share/munin/plugins/stripe_account_balance
>
>     sudo cd /etc/munin/plugins
>
>     sudo ln -s /usr/share/munin/plugins/stripe_account_balance stripe_account_balance
>
>     sudo /etc/init.d/munin-node restart

