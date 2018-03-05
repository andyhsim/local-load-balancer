---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 为负载均衡器配置权重

权重是为期望接收更多流量的服务器分配数字值的一种机制。只要运行状况检查的结果是服务器处于联机状态，那么数字越大，表示优先级越高。  

例如，如果 _server1_ 的权重为 80，_server2_ 的权重为 20，那么每传递 10 个连接，将为 _server1_ 分配 8 个连接，_server2_ 将获得 2 个连接。如果 _server1_ 脱机或从池中将其除去，那么所有连接都将转至 _server2_。

您可以在[向服务组添加服务](add-service-service-group.html)时，为特定服务配置权重，也可以在创建服务后通过[编辑服务](edit-service-load-balancer.html)来配置。

保存配置后，更改将立即生效。您可以在服务的详细信息中监视服务的连接。
