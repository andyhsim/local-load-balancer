---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configure SSL Offloading on a Load Balancer

Load Balancers have the ability to provide SSL offloading, which can dramatically reduce the load on systems currently performing the function. In order to utilize SSL offloading, a {{site.data.keyword.loadbalancer_short}} must be purchased that offers the capability. Load balancers offering SSL capability are noted “with SSL offload” in the **Order Local Load Balancer** dialog. After the SSL offloading-enabled {{site.data.keyword.loadbalancer_short}} has been provisioned, it must be configured. Follow the steps below to configure SSL offloading on a {{site.data.keyword.loadbalancer_short}}.

1. From the [Local Load Balancer Details](view-all-load-balancers.html) page, click on **Actions > Configure SSL** in the dropdown menu for the Load Balancer.
2. Select the desired SSL Certificate from the **Certificate** drop down box. Note the following:
  - Non-dedicated {{site.data.keyword.loadbalancer_short}} virtual IPs (VIPs) are limited to a maximum SSL certificate bit size of 2048.
  - At least one SSL Certificate must be stored on the Customer Portal in order to successfully complete this step. Refer to [Import an SSL Certificate](import-ssl-cert.html).
3. Select the **Enabled** check box.
4. Select the ciphers you wish to support.
5. Click the **Update** button.

After activating SSL offloading on a {{site.data.keyword.loadbalancer_short}}, the state of the SSL changes from **disabled** to **active**. The load carried by systems that previously handled SSL connections will generally decrease after SSL offloading has been activated. At any time, the SSL offloading status may be changed. Return to the Offload SSL tab and deselect the check box to disable SSL offloading for the {{site.data.keyword.loadbalancer_short}}.