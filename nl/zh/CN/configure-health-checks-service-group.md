---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 为服务配置运行状况检查

运行状况检查旨在定期检查服务器是否处于联机状态并在接受{{site.data.keyword.loadbalancer_short}}传递的流量。运行状况检查旨在根据定制超时以“已启动”或“已关闭”应答进行响应。缺省时间间隔为 120 秒。

有多种配置运行状况检查的方法。

- **缺省值：**缺省配置为 Ping。
- **HTTP：**检查所列 IP 地址的端口 80 是否使用 HTTP 代码 200（正常）进行响应。
- **HTTP 定制：**与常规 HTTP 非常类似，但您要指定连接类型、运行状况检查的位置以及所期望的响应。这是高级选项。
- **Ping：**通过 ICMP 执行的简单 ping 测试。
- **TCP：**与 ping 测试非常类似，但要通过 TCP 显式执行。如果阻塞了 ICMP 连接，那么应该使用此选项。

您可以在[向服务组添加服务](add-service-service-group.html)时，为特定服务配置运行状况检查，也可以在创建服务后通过[编辑服务](edit-service-load-balancer.html)来配置。

保存配置后，更改将立即生效。您将能够通过服务组中的“状态”图标来监视运行状况检查的状态。
