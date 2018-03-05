---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-07"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 已知限制

由于代理负载均衡器的性质，客户机请求的源 IP 将来自负载均衡器的 IP。 这将影响日志统计程序以及查看源 IP 以获取客户机信息的其他应用程序。IBM Cloud 提供了解决方案来为 Apache（所有平台）和 IIS (Windows) 重写日志条目。

为了访问指示信息和必要的其他插件，您必须首先连接到 [IBM Cloud VPN](https://console.bluemix.net/docs/infrastructure/iaas-vpn/getting-started.html){: new_window}。连接后，请访问[下载页面](http://downloads.softlayer.local/loadbalancer/){: new_window}以查找{{site.data.keyword.loadbalancer_short}}的插件和指示信息。
