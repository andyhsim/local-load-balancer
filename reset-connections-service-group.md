---
copyright:
  years: 1994, 2017 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Resetting Connections for a Service Group
{: #resetting-connections-for-a-service-group}

When a Service Group is active on a Load Balancer, a connection may exist for each Service associated with that Group based on how clients use the Service. At times, clients may be connected to one or more Services for an inappropriate amount of time. Because connections are considered a limited resource, it may be necessary to manually reset the connections for a Service Group to ensure that other clients have the opportunity to utilize the Load Balancer. Follow the steps below to reset connections for a Load Balancer.

1. From the [Local Load Balancer Details](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details) page, identify the row of the Service Group you would like to reset the connections and click **Actions > Reset Connections**.
2. Confirm the action by pressing **Yes**. Choose **No** to cancel the action.

After requesting that all active connections be reset, the Service Group will drop the active connections to each Service. A green text box will appear at the top of the screen after the connections have been reset to confirm the success of the action. When connections are dropped, clients will be able to reconnect as necessary. 

You can repeat the steps above to reset the connections for the Service Group at any time.