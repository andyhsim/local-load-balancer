---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 配置服務的性能檢查
{: #configuring-health-checks-for-a-service}

「性能檢查」旨在定期檢查伺服器是否在線上並接受 {{site.data.keyword.loadbalancer_short}} 的資料流量，以將資料流量傳遞過去。「性能檢查」旨在根據您的自訂逾時以 UP 或 DOWN 回覆來作出回應。預設間隔為 120 秒。

有幾種配置性能檢查的方法。

- **預設：**預設配置為 Ping。
- **HTTP：**透過埠 80 對 IP 位址進行檢查，並列示 HTTP 代碼 200 (OK) 的回應。
- **HTTP-CUSTOM：**很像一般 HTTP，除了您會指派連線的類型、性能檢查的位置，以及您正在預期的回應之外。這是進階選項。
- **Ping：**透過 ICMP 的簡式 ping 測試。
- **TCP：**很像 ping 測試，但它是明確地透過 TCP 來進行測試。如果您封鎖 ICMP 連線，則應使用此選項。

當您[將服務新增至服務群組](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group)，或在服務建立之後透過[編輯服務](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service)時，您可以為特定的服務配置「性能檢查」。

儲存您的配置之後，變更會立即生效。您將能夠從服務群組中的狀態圖示監視性能檢查的狀態。
