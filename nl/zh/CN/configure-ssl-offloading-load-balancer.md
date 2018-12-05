---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 在负载均衡器上配置 SSL 卸载

负载均衡器能够提供 SSL 卸载，这可以显著减少当前执行该功能的系统上的负载。为了利用 SSL 卸载，必须购买提供该功能的{{site.data.keyword.loadbalancer_short}}。提供 SSL 功能的负载均衡器在**订购本地负载均衡器**对话框中标有注释“带 SSL 卸载”。在供应了支持 SSL 卸载的{{site.data.keyword.loadbalancer_short}}后，必须对其进行配置。执行以下步骤以在{{site.data.keyword.loadbalancer_short}}上配置 SSL 卸载。

1. 从[本地负载均衡器详细信息](view-all-load-balancers.html)页面，单击负载均衡器下拉菜单中的**操作 > 配置 SSL**。
2. 从**证书**下拉框中选择所需的 SSL 证书。请注意以下事项：
  - 非专用{{site.data.keyword.loadbalancer_short}}虚拟 IP (VIP) 的最大 SSL 证书位大小限制为 2048。
  - 必须在客户门户网站上存储至少一个 SSL 证书才能成功完成此步骤。请参阅[导入 SSL 证书](import-ssl-cert.html)。
3. 选中**已启用**复选框。
4. 选择要支持的密码。
5. 单击**更新**按钮。

在{{site.data.keyword.loadbalancer_short}}上激活 SSL 卸载后，SSL 的状态会从**已禁用**更改为**活动**。先前处理 SSL 连接的系统所承担的负载通常会在激活 SSL 卸载后降低。SSL 卸载状态可随时更改。返回“卸载 SSL”选项卡并取消选中相应复选框可禁用{{site.data.keyword.loadbalancer_short}}的 SSL 卸载。
