---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 配置負載平衡器的權重

權重是一種為希望接收更多資料流量的伺服器指派數值的系統。只要伺服器根據性能檢查在線上，數字越大代表優先順序越高。  

例如，若 _server1_ 有 80 的權重，而 _server2_ 有 20 的權重，則對於通過的每 10 條連線，_server1_ 將配置 8 而 _server2_ 將得到 2。如果  _server1_ 離線或從儲存區中移除，則所有連線都會移至 _server2_。

當您[將服務新增至服務群組](add-service-service-group.html)，或在服務建立之後透過[編輯服務](edit-service-load-balancer.html)時，您可以為特定的服務配置權重。

儲存您的配置之後，變更會立即生效。您可以在「服務」的詳細資料中監視「服務」的連線。
