---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}

# FAQs
This topic contains answers to frequently asked questions about the Local Load Balancer.

## What Load Balancing products does IBM offer?
{:faq}

For a detailed comparison of the Load Balancing offerings in the IBM Cloud, refer to this [topic ![External link icon](../../icons/launch-glyph.svg "External link icon")](/docs/infrastructure/loadbalancer-service/explore-load-balancers.html#explore-load-balancers){: new_window}.

## What is the difference between a shared and dedicated load balancer?
{:faq}

There are two types of load balancers, shared and dedicated. With a shared load balancer, different customers share the same physical device, and are limited to a specific number of connections depending on what has been ordered. Dedicated load balancers are used by one customer only and their connections are limited only by the specifications of the device.

## What is a service?
{:faq}

Services are configured within a service group and represent the real servers that the load balancer will be balancing traffic to. They consist of a destination IP, destination port, health check, and weight.

## What is a service group?
{:faq}

A service group is the means by which you configure the way clients connect to your environment through the load balancer. A service group consists of a protocol, load balancing method, virtual port (which is the port clients will connect to), connection allocation (percentage), and the services associated with the group.

## Why am I getting 502 Gateway errors when using SSL offloading?
{:faq}

This is normally caused by the outgoing port of the load balancer being set to port 443.  If load balancing is enabled outbound traffic, to your server, will need to be set to the non-SSL port of your server.  This is typically port 80 for HTTP.

## Can I have multiple SSL certificates on a single load balancer?
{:faq}

This is possible in certain configurations.  The general rule is one SSL certificate per Virtual IP (VIP). A local load balancer only supports a single VIP but this can be increased on our dedicated and enterprise load balancers.

## What is a virtual port?
{:faq}

A virtual port in an IBM Cloud load balancer is simply the port you wish to run the service on. An example would be port 80 for HTTP.

## What method of load balancing is used for Local and Dedicated load balancers?
{:faq}

Our load balancers are proxy based.

## What services can be load balanced?
{:faq}

The most common ones are ports like HTTP (80), HTTPS (443), FTP (21), DNS (53), POP3 (110), and SMTP (25). Any service can be load balanced, however.

## Can I add SSL offloading to an existing load balancer?
{:faq}

This is currently not supported. A new order for a load balancer with SSL offloading will need to be placed.

## How long does it take to install a load balancer?
{:faq}

Load balancers should be installed and available for your configure about five minutes after purchase.

## How do I downgrade my local load balancer?
{:faq}

This option is only available by opening a ticket.

## What balancing methods are available with a Load Balancer?
{:faq}

IBM Cloud offers multiple balancing methods, including both single and hybrid methods.  Refer to the [Load Balancing Methods](load_balancing_methods.html) for more information about each load balance method we currently offer.

## Is it possible to load balance SSL encrypted traffic with session stickiness?
{:faq}

This is possible but only with a persistent balancing method. Other methods are not supported since the traffic is encrypted.

