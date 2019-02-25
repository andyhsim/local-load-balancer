---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuring Weights for the Load Balancer
{; #configuring-weights-for-the-load-balancer}

Weights are a system of assigning numerical values to the servers you wish to receive more traffic. A higher number represents a higher priority as long as the server is online according to health checks.  

For example, if _server1_ has a weight of 80 and _server2_ has a weight of 20, then for each 10 connections that come through, _server1_ will be allocated 8 and _server2_ will get 2. If _server1_ goes offline or is removed from the pool, all connections will go to _server2_.

You can configure weights for a particular service when you [add the Service to a Service Group](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) or by [editing the Service](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service) after it has been created.

Once your configuration has been saved, the changes will take effect immediately. You can monitor the connections of the Service in the details for the Service.