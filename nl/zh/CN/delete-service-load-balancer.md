---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 删除服务
{: #deleting-a-service}

向{{site.data.keyword.loadbalancer_short}}的服务组添加服务后，可随时将其删除。从服务组中删除服务会阻止{{site.data.keyword.loadbalancer_short}}利用该服务，除非手动将该服务添加回服务组。 

或者，服务可能处于禁用状态，这将使服务与服务组保持关联，但不可用于均衡工作。要使服务与{{site.data.keyword.loadbalancer_short}}服务组保持关联，请[编辑服务](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service)，并取消选中**已启用**复选框。 

执行以下步骤来从{{site.data.keyword.loadbalancer_short}}中删除服务。

1. 从[本地负载均衡器详细信息](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details)页面，找到要删除的服务，然后展开左侧的箭头。
2. 单击服务所在行末尾的红色“x”。
3. 单击页面底部的**保存配置**以更新设置。

删除服务后，将保存配置并且更改将立即生效。如果删除的服务是与某个服务组关联的唯一服务，那么在添加新服务之前，该组将无法执行任何负载均衡活动。
