---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-03"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQs
This topic contains frequently asked questions relating to the Local Load Balancer.

## What is the difference between a shared and dedicated load balancer?

There are two types of load balancers, shared and dedicated. With a shared load balancer, different customers share the same physical device, and are limited to a specific number of connections depending on what has been ordered. Dedicated load balancers are used by one customer only and their connections are limited only by the specifications of the device.

## What is a service group?
A service group is the means by which you configure the way clients connect to your environment through the load balancer. A service group consists of a protocol, load balancing method, virtual port (which is the port clients will connect to), connection allocation (percentage), and the services associated with the group.

# What is a service?
Services are configured within a service group and represent the real servers that the load balancer will be balancing traffic to. They consist of a destination IP, destination port, health check, and weight.