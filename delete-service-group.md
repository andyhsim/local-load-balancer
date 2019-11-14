---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2019-11-12"

keywords: service, group, service group, delete, deleting, load balancer
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank_"}

# Deleting a Service Group
{: #deleting-a-service-group}

When deleting a Service Group, all Services associated with the Group will also be deleted. Follow the steps here to delete a Service Group for a {{site.data.keyword.loadbalancer_short}}.
{: shortdesc}

1. From the [Local Load Balancer Details](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details) page, identify the row of the Service Group you would like to delete and click on **Actions > Remove Group**.
2. Click **Save Configuration**.

After deleting a Service Group, it will be removed from the {{site.data.keyword.loadbalancer_short}}. All associated Services will also be deleted and the Virtual Port associated with the Service Group will be available, in case it is needed for another Service Group in the future. Upon deletion, the Connection Allocation percentage for the remaining Service Groups must be changed manually for any remaining groups.
