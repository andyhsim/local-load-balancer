---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 编辑服务 

向负载均衡器的服务组添加服务后，可随时对其进行编辑。服务的所有“基本设置”都可以进行编辑，还可以使用编辑功能来添加其他注释。 

执行以下步骤来编辑服务。

1. 从[本地负载均衡器详细信息](view-all-load-balancers.html)页面，通过展开左侧的箭头来找到要编辑的服务。
2. 根据需要编辑以下字段：
  - **目标 IP：**目标服务器的 IP 地址。
  - **目标端口：**用于将流量路由到目标服务器的端口号。
  - **运行状况检查：**以下选项中的首选运行状况检查方法。
      - **缺省值：**缺省配置为 Ping。
      - **HTTP：**检查所列 IP 地址的端口 80 是否使用 HTTP 代码 200（正常）进行响应。
      - **HTTP 定制：**与常规 HTTP 非常类似，但您要指定连接类型、运行状况检查的位置以及所期望的响应。这是高级选项。
      - **Ping：**通过 ICMP 执行的简单 ping 测试。
      - **TCP：**与 ping 测试非常类似，但要通过 TCP 显式执行。如果阻塞了 ICMP 连接，那么应该使用此选项。
  - **权重：**以数字表示的服务优先级。权重是为期望接收更多流量的服务器分配数字值的一种机制。只要运行状况检查的结果是服务器处于联机状态，那么数字越大，表示优先级越高。例如，如果 _server1_ 的权重为 80，_server2_ 的权重为 20，那么每传递 10 个连接，将为 _server1_ 分配 8 个连接，_server2_ 将获得 2 个连接。如果 _server1_ 脱机或从池中将其除去，那么所有连接都将转至 _server2_。
  - **注释：**自由格式文本字段。
  - **已启用：**选中或取消选中此复选框可启用或禁用服务。
3. 单击**保存配置**按钮以更新服务。单击**取消**以取消该操作。

编辑服务后，编辑内容将显示在“服务”部分中包含该服务的行中。可以通过重复上述步骤随时进行其他编辑。