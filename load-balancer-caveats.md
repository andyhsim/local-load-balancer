---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-07"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Known Limitations

Due to the nature of a proxy load balancer, the source IP of the client request comes from the IP of the load balancer. This will affect log statistical programs and other applications that look at the source IP for obtaining client information. IBM Cloud provides a solution to correctly rewrite log entries for Apache (All Platforms) and IIS (Windows).

In order to access the instructions and necessary additional plug-ins you must first be connected to the [IBM Cloud VPN](https://console.bluemix.net/docs/infrastructure/iaas-vpn/getting-started.html){: new_window}. Once connected, visit the [Downloads page](http://downloads.softlayer.local/loadbalancer/){: new_window} to find the plugins and instructions for your {{site.data.keyword.loadbalancer_short}}.