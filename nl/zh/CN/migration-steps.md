---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud

subcollection: local-load-balancer

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# 将 Local Load Balancer 迁移到 IBM Cloud Load Balancer

您可以通过执行以下过程将 Local Load Balancer 迁移到 IBM© Cloud Load Balancer。

## 步骤 1：订购 Cloud Load Balancer
{: #step-1-order-a-cloud-load-balancer}

要订购 IBM Cloud Load Balancer 服务，请从 [IBM Cloud 目录 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")]( https://cloud.ibm.com/catalog/infrastructure/load-balancer-group){:new_window} 中选择 **IBM Cloud Load Balancer**。单击**创建**，然后执行以下过程：

1. 定义基本服务参数，例如名称和描述。
2. 选择数据中心。
3. 将负载均衡器类型选择为**公共**。
4. 选择要部署负载均衡器的目标子网。

  您的负载均衡器服务实例将在此子网上具有其中一个网络接口。请确保应用程序服务器位于此子网上或可从此子网进行访问。如果必要，请启用 VLAN 生成。
  {: note}

5. 利用与您当前在 Local load Balancer 中使用的服务组相同的配置，创建前端和后端应用程序协议和端口。有关此配置的更多信息，请参阅[配置 IBM Cloud Load Balancer 参数](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configuring-ibm-cloud-load-balancer-parameters)。
6. 要启用 SSL 卸载，请将前端协议设置为 HTTPS，将后端协议设置为 HTTP。然后，从“证书”下拉框中选择与 Local Load Balancer 相同的 SSL 证书。Local Load Balancer 所使用的证书位于下拉列表中，因为所有现有 SSL 证书都通过 [IBM Cloud 证书库 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/classic/security/sslcerts){:new_window} 进行管理。
7. 根据需要调整运行状况检查参数，否则使用缺省设置。有关运行状况检查参数的更多信息，请参阅 [IBM Cloud Load Balancer 参数](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configure-health-checks)。
8. 单击**连接服务器**，以添加之前用于 Local Load Balancer 服务的任何服务器实例。
9. 复查此页面，确认“服务协议”，然后单击**创建**。

此时会显示负载均衡器列表，其中包含您的所有服务实例。

新创建的负载均衡器可能不会立即在此列表中显示。几分钟之后，新的负载均衡器将显示为灰色，表示其状态为 `Offline`。再过几分钟之后，新的负载均衡器将显示为绿色，表示其状态为 `Online`。您可能需要刷新屏幕才能看到这些更改。
{: note}

单击此页面上的服务名称将带您进入服务概述页面。您可以导航至**协议**、**运行状况检查**和**服务器实例**选项卡，以进一步编辑配置。

## 步骤 2：验证 Cloud Load Balancer 是否按预期运行
{: #step-2-verify-your-cloud-load-balancer-is-working-as-expected}

此时请注意，您现在有两个负载均衡器在同时运行：旧的 Local Load Balancer 和新的 IBM Cloud Load Balancer。
{: important}

使用上面状态页面中列出的域测试新的 IBM Cloud Load Balancer，以确保其功能与 Local load Balancer 中的 VIP 相同。

然后，将使用 Local Load Balancer VIP 的任何位置更新为使用新的 Cloud Load Balancer 域。

新 Cloud Load Balancer 的这个配置可能是在迁移过程中出现的唯一停机或流量中断。
{: note}

## 步骤 3：取消旧的 Local Load Balancer
{: #step-3-cancel-your-local-load-balancer}

将所有 Local load Balancer VIP 替换为新 IBM Cloud Load Balancer 的域且已验证功能按预期运行后，您可以安全地取消 Local Load Balancer 服务。要进行此操作，请执行以下步骤：

1. 转至 [Local Load Balancer 列表页面](https://cloud.ibm.com/classic/network/loadbalancing/local)。
2. 找到要删除的负载均衡器并展开其旁边的箭头。
3. 单击行末尾的红色 **X** 来取消负载均衡器。
