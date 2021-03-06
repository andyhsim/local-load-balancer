---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2019-11-12"

keywords: edit, editing, service, group, service group, load balancer
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank_"}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Editing a service group
{: #editing-a-service-group}
{: help}
{: support}

After adding a Service Group to a {{site.data.keyword.loadbalancer_short}}, its Basic Settings (including Balancing Method and Virtual Port), Connection Allocation and Notes may be edited. Edits to each Service Group are immediately visible and additional edits may be made at any time.
{: shortdesc}

If the Group Type for a Service Group needs to be changed, the Service Group must be deleted and a new Service Group must be added that reflects the desired Group Type.

Follow the steps below to edit an existing Service Group for a {{site.data.keyword.loadbalancer_short}}.

1. From the [Local Load Balancer Details](/docs/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details#viewing-local-load-balancer-details) page, expand the Service Group details by clicking on the expand icon on the left hand side of the row corresponding to the Service Group you would like to edit.
2. Update the Service Group settings:
  - **Method:** Select a Balancing Method from the dropdown list.
  - **Virtual Port:** Port number that will be used for the Service Group. Refer to the [Common Service Ports FAQ](/docs/local-load-balancer?topic=local-load-balancer-faqs-for-local-load-balancer#what-services-can-be-load-balanced-) for more information.

  	**Note:** Each Service Group must be assigned to a unique port. If a unique port is not assigned, an error will appear at the top of the page and the Service Group may not be added until a unique Virtual Portal is assigned.
  - **Allocation:**  Allocation for the Service Group.
  - **Notes:** Freeform text to identify Service Group.
3. Click the **Save Configuration** button to update the Service Group. Click the **Cancel** button to cancel the action.

Edits to the Service Group will be reflected on the Details screen under the associated Group. If a change was made to the Connection Allocation, additional edits for other Service Groups may be necessary. If a change was made to the Balancing Method, services associated with the Group may require additional edits to align with the new Balancing Method. Additional edits to the Service Group may be made at any time by repeating the steps above.
