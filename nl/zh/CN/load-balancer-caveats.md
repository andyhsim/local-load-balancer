---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 本地负载均衡器已知限制
{: #known-limitations-with-local-load-balancer}

由于代理负载均衡器的性质，客户机请求的源 IP 将来自负载均衡器的 IP。 这将影响日志统计程序以及查看源 IP 以获取客户机信息的其他应用程序。IBM© Cloud 为 Apache（所有平台）和 IIS (Windows) 提供了可正确重写日志条目的解决方案。

要访问指示信息和必要的附加插件，必须先连接到 IBM Cloud VPN。连接后，请访问[下载页面 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://downloads.softlayer.local/loadbalancer/){: new_window} 来查找 {{site.data.keyword.loadbalancer_short}} 的插件和指示信息。

**注：**您必须登录到 IBM Cloud VPN 以访问下载链接。
