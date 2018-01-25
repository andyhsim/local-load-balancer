# Exploring Product Options
IBM offers several options for firewalls and load balancers for customers to choose from. The tables in this topic conveniently compare the options for both product sets, providing information and specifications to choose the product that's right for you.

## Firewall Options
The following table provides details on all of IBM's firewall offerings. 

To view more detailed information about these offerings, click its name in the table.

|        | [Security Groups](https://console.bluemix.net/docs/infrastructure/security-groups/sg_index.html) | [Hardware Firewall (Shared)]() | [Hardware Firewall (Dedicated)]() | [Fortigate Security Appliance 1g]() | [Virtual Router Appliance](https://console.bluemix.net/docs/infrastructure/virtual-router-appliance/getting-started.html#getting-started) | [Fortigate Security Appliance 10g](https://console.bluemix.net/docs/infrastructure/fortigate-10g/getting-started.html#getting-started)
| ------- | :------: | :------: | :------: | :------: | :------: | :------:
**Stateful Packet Inspection**|Yes|Yes|Yes|Yes|Yes|Yes
**Public Network Protection**|Yes|Yes|Yes|Yes|Yes|Yes
**Private Network Protection**|Yes|No|No|No|Yes|Yes
**Ingress Rules**|Yes|Yes|Yes|Yes|Yes|Yes
**Egress Rules**|Yes|No|No|Yes|Yes|Yes
**Single Tenant Appliance**|No|No|Yes|Yes|Yes|Yes
**VLAN Protection**|No|No|Yes|Yes|Yes|Yes
**Multi-VLAN Support**|No|No|No|No|Yes|Yes
**NAT Support**|No|No|No|Yes|Yes|Yes
**SSL/IPsec VPN Termination**|No|No|No|Yes|Yes|Yes
**Open VPN Termination**|No|No|No|No|Yes|No
**HA Option**|N/A|No|Yes|Yes|Yes|Yes
**Manage from API & Portal**|Yes|Yes|Yes|Appliance GUI|Appliance GUI|Appliance GUI
**10Gbps Support**|N/A|No|No|No|Yes|Yes
**NGFW  Add-ons (IPS, AV, WF)**|No|No|No|Yes|No|Yes
**Cost**|$0/Month |Starting $99.00/month|Starting $1999.00/month|Starting $1999.00/month|Starting $219.00/month|Starting $4,999.00 /month

## Load Balancer Options
The following table provides details on all of IBM's load balancer offerings. 

To view more detailed information about these offerings, click its name in the table.

|        | [IBM Cloud Load Balancer](https://console.bluemix.net/docs/infrastructure/loadbalancer-service/getting-started.html#getting-started)| [Local Load Balancer]() (Monthly) (Shared)| [Local Load Balancer]() (Monthly) (Dedicated)| [Citrix NetScaler]() VPX/MPX (Standard)| [Citrix NetScaler VPX/MPX]() (Platinum) 
| ------- | :------: | :------: | :------: | :------: | :------: 
**Public VIP**|Yes|Yes|Yes|Yes|Yes 
**Private VIP**|No|No|Yes|Yes|Yes
**Layer 4 LB**|Yes|Yes|Yes|Yes|Yes 
**Layer 7 LB**|No|Cookie Persistence|Cookie Persistence|Yes|Yes 
**Health Checks**|Yes|Yes|Yes|Yes|Yes 
**SSL Offload**|Yes|Yes|Yes|Yes|Yes 
**Management**|via IBM Portal|via IBM Portal|via IBM Portal|Self-manage (Vendor GUI)|Self-manage (Vendor GUI)
**High Availability**|Built-in|Built-in|Optional|Optional|Optional
**Advance LB (TCP Optimization, Compress, Caching, WAF)**|No|No|No|Limited|Yes 
**Global LB (GLB)**|No|No|No|No|Yes
**Pricing**|Usage-based|Monthly Flat|Monthly Flat|Monthly Flat|Monthly Flat 