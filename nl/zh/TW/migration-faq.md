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

# IBM Cloud Load Balancer 移轉常見問題
{: #migration-faq}

下列常見問題適用於 IBM Local Load Balancer 移轉處理程序。

## Local Load Balancer 行銷結束 (EOM) 的公告及生效日期為何？
{: faq}

EOM 公告日期為 2019 年 3 月 1 日，而生效日期為 2019 年 6 月 1 日。於此日期之後不再進行新的銷售。

## EOM 之後會提供支援嗎？
{: faq}

會，現有的 Local Load Balancer 客戶可以取得支援。

## 如何開始使用 IBM Cloud Load Balancer？
{: faq}

我們建議您從閱讀 [IBM Cloud Load Balancer 文件](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-getting-started)開始。

## 是否有從 Local Load Balancer 服務到 IBM Cloud Load Balancer 的移轉路徑？
{: faq}

沒有自動移轉路徑。不過，您可以要求關閉您的 Local Load Balancer 服務，並從「IBM Cloud 主控台」訂購 Cloud Load Balancer 服務。

## Local Load Balancer 與 Cloud Load Balancer 之間的差異為何？
{: faq}

Local Load Balancer 是一種硬體式本端負載平衡服務，而 IBM Cloud Load Balancer 是一種雲端原生服務，可提供具成本效益、自動調整的負載平衡解決方案，且同時支援公用及專用網路。

## Cloud Load Balancer 使用的術語是否與 Local Load Balancer 相同？
{: faq}

在某些情況下，術語並不相同。下表會比較 Local Load Balancer 中的重要術語與其在 Cloud Load Balancer 中相對應的不同術語。

| Local Load Balancer 術語 | Cloud Load Balancer 術語 |
| ------------- | ------------- |
| 服務群組 | 通訊協定 |
| 服務 | 伺服器實例 |
| VIP | FQDN |

## 當我移轉至 Cloud Load Balancer 時，負載平衡器是否仍使用單一、固定的 IP 位址？
{: faq}

IBM Cloud Load Balancer 的 IP 並不固定。Cloud Load Balancer 會從儲存區指派負載平衡器實例，這始終需要完整的網域名稱 (FQDN)。因此，Cloud Load Balancer 的個別 IP 位址可能會變更。

## IBM Cloud Load Balancer 可用於公用/專用 VSI 及裸機解決方案嗎？
{: faq}

可以，Cloud Load Balancer 可用於公用和專用 VSI 以及裸機。

## IBM Cloud Load Balancer 是否遵循 GDPR？
{: faq}

是，Cloud Load Balancer 供應項目遵循 GDPR。

## 開始移轉之後，預期系統遭遇的運行中斷或傳輸中斷有多長？

由於是負載平衡器移轉，因此您不會遭遇運行中斷或傳輸中斷。唯一可能會遭遇運行中斷或傳輸中斷的情況，是將 Local Load Balancer 配置更新為新的 IBM Cloud Load Balancer FQDN 時。

## 您的指示說明要在取消 Local Load Balancer 之前訂購 IBM Cloud Load Balancer。當我配置兩個裝置時，是否會對系統或工作負載造成任何影響？

不會，Cloud Load Balancer 及 Local Load Balancer 是兩個獨立運作的個別供應項目。

## 我之前在 Local Load Balancer 中選擇「每秒連線數」選項。是否也需要在 Cload Load Balancer 中進行此配置？

不需要。IBM Cloud Load Balancer 會自動調整其負載容量。您可以在 [Cloud Load Balancer 水平調整](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-performing-ibm-cloud-load-balancer-basics#horizontal-scaling)主題中閱讀此項的相關資訊。

## 使用 Cloud Load Balancer 時可以選擇哪些通訊協定？

您可以選擇 HTTP、HTTPS 及 TCP 通訊協定。我們也提供「第 7 層支援」。如需相關資訊，請參閱[特性概觀](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-about-ibm-cloud-load-balancer#overview-of-features)。

## 我需要一種特定類型的密碼。Cloud Load Balancer 是否支援該密碼？

IBM Cloud Load Balancer 支援具有 SSL 卸載功能的 TLS 1.2 版。您可以在 [Cloud Load Balancer SSL 密碼組合](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-ssl-offload-with-ibm-cloud-load-balancer#ssl-cipher-suites)中找到所支援 SSL 密碼的更多相關資訊。
