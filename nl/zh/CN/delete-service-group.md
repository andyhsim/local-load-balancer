---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 删除服务组
{: #deleting-a-service-group}

删除服务组时，还将删除与该组关联的所有服务。执行以下步骤来删除{{site.data.keyword.loadbalancer_short}}的服务组。

1. 从[本地负载均衡器详细信息](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details)页面，确定要删除的服务组所在的行，然后单击**操作 > 除去组**。
2. 单击**保存配置**。

删除服务组后，即会将其从{{site.data.keyword.loadbalancer_short}}中除去。还将删除所有关联的服务，但与该服务组关联的虚拟端口仍可用，以备未来其他服务组之需。删除后，其余服务组的连接分配百分比必须针对所有其余组进行手动更改。
