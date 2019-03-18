---
copyright:
  years: 1994,2017,2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 向负载均衡器添加服务组
{: #adding-a-service-group-to-a-load-balancer}

添加了{{site.data.keyword.loadbalancer_short}}后，可以随时向{{site.data.keyword.loadbalancer_short}}添加新的服务组。服务组有多种组类型可用，并提供各种各样的单个或混合均衡方法。添加新的服务组时，重要的是确保所有组连接分配的总和等于 100%。请执行以下步骤来向{{site.data.keyword.loadbalancer_short}}添加新的服务组。

1. 从[本地负载均衡器详细信息](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details)页面，单击**添加组**按钮。或者，可以单击**操作 > 添加组**。这将向该页面底部添加新的“服务组”部分。
2. 从**组**下拉列表中选择所需的组类型，然后从**方法**下拉列表中选择所需的均衡方法。有关每种负载均衡方法的更多信息，请参阅[负载均衡方法](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-load-balancing-methods#load-balancing-methods)。
3. 在**虚拟端口**字段中，输入将用于服务组的端口号。有关更多信息，请参阅[常用服务端口常见问题](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-faqs-for-local-load-balancer#what-services-can-be-load-balanced-)。 

	**注：**必须为每个服务组分配一个唯一端口。如果未分配唯一端口，那么会在页面顶部显示错误，并且只有在分配唯一的虚拟端口之后，才能添加服务组。
4. 在**分配**字段中输入分配比例。
5. 根据需要，在**注释**文本框中输入任何注释。
6. 单击**保存配置**按钮以添加新的服务组。单击**取消**以取消该操作。

添加服务组后，可随时将其删除或对其进行编辑。连接可能会重置为连接到该服务组，并且可向该组添加新服务。要使服务组开始根据其分配的连接分配对负载进行均衡，必须向该服务组[添加](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group)一个或多个服务。

## 后续操作

[向服务组添加服务](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group)。
