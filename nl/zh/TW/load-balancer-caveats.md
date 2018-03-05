---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-07"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 已知限制

由於 Proxy 負載平衡器的本質，用戶端要求的來源 IP 是來自負載平衡器的 IP。這會影響查看來源 IP 以取得用戶端資訊的日誌統計程式和其他應用程式。IBM Cloud 為 Apache（所有平台）和 IIS (Windows) 提供一個正確重寫日誌項目的解決方案。

為了存取指示及必要的其他外掛程式，您必須先連接到 [IBM Cloud VPN](https://console.bluemix.net/docs/infrastructure/iaas-vpn/getting-started.html){: new_window}。連接之後，請造訪[下載頁面](http://downloads.softlayer.local/loadbalancer/){: new_window}，以為您的 {{site.data.keyword.loadbalancer_short}} 尋找外掛程式及指示。
