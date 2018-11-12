---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Edit a Service 

After a Service has been added to a Load Balancer's Service Group, it may be edited at any time. All Basic Settings of a Service are eligible for edits and additional notes may also be added using the edit feature. 

Follow the steps below to edit a Service.

1. From the [Local Load Balancer Details](view-all-load-balancers.html) page, locate the service you would like to edit by expanding the arrow to the left.
2. Edit the follow fields, as desired:
  - **Destination IP:** The IP address of the destination server.
  - **Dest Port:** The port number to use to route traffic to the destination server.
  - **Heath Check:** The preferred health check method from these options.
      - **Default:** The default configuration is Ping.
      - **HTTP:** Checks from port 80 to the IP address listed rand esponds with HTTP code 200 (okay).
      - **HTTP-CUSTOM:** Much like regular HTTP except you assign the type of connection, the location of your health check, and the response that you are anticipating. This is an advanced option.
      - **Ping:** A simple ping test over ICMP.
      - **TCP:** Much like a ping test but explicitly over TCP.  This option should be used if you have ICMP connections blocked.
  - **Weight:** The numeric priority for the Service. Weights are a system of assigning numerical values to the servers you wish to receive more traffic. A higher number represents a higher priority as long as the server is online according to health checks. For example, if _server1_ has a weight of 80 and _server2_ has a weight of 20, then for each 10 connections that come through, _server1_ will be allocated 8 and _server2_ will get 2. If _server1_ goes offline or is removed from the pool, all connections will go to _server2_.
  - **Notes:**  Freeform text field.
  - **Enabled:** Check or uncheck this checkbox to enable or disable the service.
3. Click the **Save Configuration** button to update the Service. Click **Cancel** to cancel the action.

After editing a Service, the edits will appear in the row containing the Service in the Service section. Additional edits may be made at any time by repeating the steps above.
