---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Known Limitations with Local Load Balancer

Due to the nature of a proxy load balancer, the source IP of the client request comes from the IP of the load balancer. This will affect log statistical programs and other applications that look at the source IP for obtaining client information. IBM© Cloud provides a solution to correctly rewrite log entries for Apache (All Platforms) and IIS (Windows).

In order to access the instructions and necessary additional plug-ins you must first be connected to the IBM Cloud VPN. Once connected, visit the [Downloads page ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://downloads.softlayer.local/loadbalancer/){: new_window} to find the plugins and instructions for your {{site.data.keyword.loadbalancer_short}}.

**NOTE:** You must be logged into the IBM Cloud VPN in order to access the download link.
