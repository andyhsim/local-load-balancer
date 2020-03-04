---
copyright:
  years: 1994, 2017
lastupdated: "2019-11-12"

keywords: limitations, support, troubleshooting, load balancer, logging, problems
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank_"}
{:note: .note}

# Known limitations with local load balancer
{: #known-limitations-with-local-load-balancer}

There are some known limitations to be aware of when working with IBM© Cloud Local Load Balancer.
{: shortdesc}

Due to the nature of a proxy load balancer, the source IP of the client request comes from the IP of the load balancer. This will affect log statistical programs and other applications that look at the source IP for obtaining client information. IBM© Cloud provides a solution to correctly rewrite log entries for Apache (All Platforms) and IIS (Windows).

In order to access the instructions and necessary additional plug-ins you must first be connected to the IBM Cloud VPN. Once connected, visit the [Downloads page ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://downloads.softlayer.local/loadbalancer/){: new_window} to find the plugins and instructions for your {{site.data.keyword.loadbalancer_short}}.

You must be logged into the IBM Cloud VPN in order to access the download link.
{: note}
