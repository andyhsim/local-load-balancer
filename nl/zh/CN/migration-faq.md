---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud, faq, support

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
{:faq: data-hd-content-type='faq'}

# IBM Cloud Load Balancer 迁移常见问题
{: #migration-faq}

以下常见问题适用于 IBM Local Load Balancer 迁移过程。

## Local Load Balancer 终止销售 (EOM) 的声明和生效日期是哪天？
{: faq}

EOM 声明日期是 2019 年 3 月 1 日，而生效日期是 2019 年 6 月 1 日。在此日期之后不会再销售。

## EOM 之后还可获得支持吗？
{: faq}

是的，现有 Local Load Balancer 客户还可获得支持。

## 如何开始使用 IBM Cloud Load Balancer？
{: faq}

我们建议您通过阅读 [IBM Cloud Load Balancer 文档](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-getting-started)开始使用。

## 是否有什么途径可以从 Local Load Balancer 服务迁移到 IBM Cloud Load Balancer？
{: faq}

不存在自动迁移途径。但是，您可以请求关闭 Local Load Balancer 服务，然后从 IBM Cloud 控制台订购 Cloud Load Balancer 服务。

## Local Load Balancer 和 Cloud Load Balancer 之间有哪些差异？
{: faq}

Local Load Balancer 是基于硬件的本地负载均衡服务，而 IBM Cloud Load Balancer 是云本机服务，可提供经济有效的自动缩放负载均衡解决方案，支持公共和专用网络。

## Cloud Load Balancer 与 Local Load Balancer 使用的术语是否相同？
{: faq}

在某些情况下不相同。下表将 Local Load Balancer 中的关键术语与 Cloud Load Balancer 中的相应术语和不同术语进行了比较。

| Local Load Balancer 术语 | Cloud Load Balancer 术语 |
| ------------- | ------------- |
| 服务组 | 协议 |
| 服务 | 服务器实例 |
| VIP | FQDN |

## 迁移到 Cloud Load Balancer 后我的负载均衡器是否仍具有单一固定 IP 地址？
{: faq}

IBM Cloud Load Balancer 的 IP 不是固定的。Cloud Load Balancer 从池中分配负载均衡器实例，始终需要标准域名 (FQDN)。因此，Cloud Load Balancer 的单个 IP 地址可能会更改。

## IBM Cloud Load Balancer 是否可用于公共/专用 VSI 及裸机解决方案？
{: faq}

是的，Cloud Load Balancer 可用于公共和专用 VSI 以及裸机。

## IBM Cloud Load Balancer 是否符合 GDPR 标准？
{: faq}

是的，Cloud Load Balancer 产品符合 GDPR 标准。

## 开始迁移后，可以预期我的系统有多少停机时间或流量中断？

负载均衡器迁移时不会出现停机或流量中断。唯一可能出现的停机或流量中断是在将 Local Load Balancer 配置更新到新的 IBM Cloud Load Balancer FQDN 时。

## 指示信息要求我在取消 Local Load Balancer 之前订购 IBM Cloud Load Balancer。配置两台设备时，我的系统或工作负载是否会受到影响？

不会，Cloud Load Balancer 和 Local Load Balancer 是两款可独立工作的不同产品。

## 在使用 Local Load Balancer 时我经常选择“每秒连线数”选项。我是否需要对 Cloud Load Balancer 配置此选项？

不需要。IBM Cloud Load Balancer 会自动调整其负载容量。您可以在 [Cloud Load Balancer 水平缩放](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-performing-ibm-cloud-load-balancer-basics#horizontal-scaling)主题中了解更多相关信息。

## 使用 Cloud Load Balancer 时我可以选择哪些协议？

您可以选择 HTTP、HTTPS 和 TCP 协议。我们还提供第 7 层支持。有关更多信息，请参阅[功能概述](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-about-ibm-cloud-load-balancer#overview-of-features)。

## 我需要特殊类型的密码。Cloud Load Balancer 是否支持特殊类型的密码？

IBM Cloud Load Balancer 支持具有 SSL 卸载功能的 TLS V1.2。您可以在 [Cloud Load Balancer SSL 密码套件](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-ssl-offload-with-ibm-cloud-load-balancer#ssl-cipher-suites)中找到有关受支持 SSL 密码的更多信息
