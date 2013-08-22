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

Munin Configuration
===================

copy the file conf/stripe to /etc/munin/plugin-conf.d/stripe i.e.:

>     cp conf/stripe /etc/munin/plugin-conf.d/


## stripe_customer_count

Provide a running total of the number of customers that are in your stripe account

### Installation

>     sudo cp stripe_customer_count /usr/share/munin/plugins/stripe_customer_count
>     sudo ln -s /usr/share/munin/plugins/stripe_customer_count /etc/munin/plugins/stripe_customer_count
>     sudo /etc/init.d/munin-node restart

## stripe_account_balance

Provide a running of the balance of your stripe account

### Installation

>     sudo cp stripe_account_balance /usr/share/munin/plugins/stripe_account_balance
>     sudo ln -s /usr/share/munin/plugins/stripe_account_balance /etc/munin/plugins/stripe_account_balance
>     sudo /etc/init.d/munin-node restart

## stripe_event_counter_

Provides a daily tally of the number of events that stripe has sent out, at the time
of writing, the following events are supported see [Stripe documentation for a complete list](https://stripe.com/docs/api/python#list_events)

 
 - account.updated
 - account.application.deauthorized
 - balance.available
 - charge.succeeded
 - charge.failed
 - charge.refunded
 - charge.captured
 - charge.dispute.created
 - charge.dispute.updated
 - charge.dispute.closed
 - customer.created
 - customer.updated
 - customer.deleted
 - customer.card.created
 - customer.card.updated
 - customer.card.deleted
 - customer.subscription.created
 - customer.subscription.updated
 - customer.subscription.deleted
 - customer.subscription.trial_will_end
 - customer.discount.created
 - customer.discount.updated
 - customer.discount.deleted
 - invoice.created
 - invoice.updated
 - invoice.payment_succeeded
 - invoice.payment_failed
 - invoiceitem.created
 - invoiceitem.updated
 - invoiceitem.deleted
 - plan.created
 - plan.updated
 - plan.deleted
 - coupon.created
 - coupon.deleted
 - transfer.created
 - transfer.updated
 - transfer.paid
 - transfer.failed
 - ping


### Installation

To install a munin statistic to count the number of customer.created (see second command below)

>     sudo cp stripe_event_counter_ /usr/share/munin/plugins/stripe_event_counter_
>     sudo ln -s /usr/share/munin/plugins/stripe_event_counter_ /etc/munin/plugins/stripe_event_counter_account.created
>     sudo /etc/init.d/munin-node restart
