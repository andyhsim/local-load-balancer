---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:note: .note}

# Local Load Balancer 的已知限制
{: #known-limitations-with-local-load-balancer}

由於 Proxy 負載平衡器的本質，用戶端要求的來源 IP 是來自負載平衡器的 IP。這會影響查看來源 IP 以取得用戶端資訊的日誌統計程式和其他應用程式。IBM© Cloud 為 Apache（所有平台）和 IIS (Windows) 提供一個正確重寫日誌項目的解決方案。

為了存取指示及必要的其他外掛程式，您必須先連接到 IBM Cloud VPN。連接之後，請造訪[下載頁面 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://downloads.softlayer.local/loadbalancer/){: new_window}，以為您的 {{site.data.keyword.loadbalancer_short}} 尋找外掛程式及指示。

您必須登入 IBM Cloud VPN 以便存取下載鏈結。
{: note}
