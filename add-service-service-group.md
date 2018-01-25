---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-23"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Add a Service to a Service Group

After a Service Group has been added to a {{site.data.keyword.loadbalancer_short}}, Services may be added to begin the balancing process. Multiple Services may be added to a Service Group and may be weighted to allow for prioritization on how each device should receive the workload at any given time. Follow the steps below to add a new Service to a Service Group for a {{site.data.keyword.loadbalancer_short}}.

1. From the [Local Load Balancer Details](view-all-load-balancers.html) page, click **Actions > Add Service** in the dropdown menu on the row corresponding to the Service Group where you would like to add a service. Alternatively, expand the Group details by clicking on the expand icon on the left hand side of the row and click on the **Add Service** button. A new Service section will be added to the bottom of the Service Group details section.
2. Enter the Service parameters:
  - **Destination IP:** The IP address of the destination server.
  - **Dest. Port:** The port number to use to route traffic to the destination server.
  - **Health Check:** The preferred health check method from these options.

     - **Default:** The default configuration is Ping.
     - **HTTP:** Checks over port 80 to the IP address listed responds with HTTP code 200 (okay).
     - **HTTP-CUSTOM:** Much like regular HTTP, except you assign the type of connection, the location of your health check, and the response that you are anticipating. This is an advanced option.
     - **Ping:** A simple ping test over ICMP.
     - **TCP:** Much like a ping test but explicitly over TCP. This option should be used if you have ICMP connections blocked.
  - **Weight:** The numeric priority for the Service. Weights are a system of assigning numerical values to which servers you wish to receive more traffic. A higher number represents a higher priority as long as the server is online according to health checks. For example, if _server1_ has a weight of 80 and _server2_ has a weight of 20, then for each 10 connections that come through, _server1_ will be allocated 8 and _server2_ will get 2. If _server1_ goes offline or is removed from the pool, all connections will go to _server2_.
  - **Notes:** Field for notes.
3. Select the **Enabled** check box to enable the Service.
4. Click the **Save Configuration** button to add the Service. Click **Cancel** to cancel the action.

After adding a Service to a Service Group, it will appear in the Services grid for the Group. If it has been enabled, it will begin assisting in Load Balancing efforts based on the weight provided when the Service was added. If it is disabled, it will still appear in the Service Group, but it will not assist in balancing until it has been activated. Health checks will be performed on the Service in intervals and its Status will be reflected as up or down, based on the result of the health check. Services may be edited or deleted at any time and HTTP Custom Health Checks may be added to any existing service through the Actions drop down menu.
