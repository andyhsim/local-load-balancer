---
copyright:
  years: 1994,2017,2018
lastupdated: "2018-01-23"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Add a Service Group to a Load Balancer

After a {{site.data.keyword.loadbalancer_short}} has been added, a new Service Group may be added to the {{site.data.keyword.loadbalancer_short}} at any time. Service groups are available in a variety of Group Types and offer a wide array of single or hybrid Balancing Methods. When adding a new Service Group, it is important to ensure that the sum of all the groups Connection Allocations equals 100%. Follow the steps below to add a new Service Group to a {{site.data.keyword.loadbalancer_short}}.

1. From the [Local Load Balancer Details](view-all-load-balancers.html) page, click on the **Add Group** button. Alternatively, you can click on **Actions > Add Group**. A new Service Group section will be added to the bottom of the page.
2. Select the desired Group Type from the **Group** dropdown list and select the desired Balancing Method from the **Method** dropdown list. Refer to the [Load Balancing Methods](load_balancing_methods.html) for more information on each load balancing method.
3. Enter the port number that will be used for the service group in the **Virtual Port** field. Refer to the [Common Service Ports FAQ](load-balancing-faqs-2.html#what-services-can-be-load-balanced-) for more information. 

	**Note:** Each Service Group must be assigned to a unique port. If a unique port is not assigned, an error will appear at the top of the page and the Service Group may not be added until a unique Virtual Portal is assigned.
4. Enter an allocation in the **Allocation** field.
5. Enter any notes in the **Notes** text box, if desired.
6. Click the **Save Configuration** button to add the new Service Group. Click **Cancel** to cancel the action.

After adding a Service Group, it may be deleted or edited at any time. Connections may be reset to the Service Group and new services may be added to the group. For a Service Group to begin balancing the load based on its assigned Connection Allocations, one or more services must be [added](add-service-service-group.html) to the Service Group.

## What Happens Next

[Add a Service to the Service Group](add-service-service-group.html).
