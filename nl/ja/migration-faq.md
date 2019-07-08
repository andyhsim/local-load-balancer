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

# IBM Cloud Load Balancer のマイグレーションに関する FAQ
{: #migration-faq}

IBM Local Load Balancer のマイグレーション・プロセスにも、次のよくあるご質問があてはまります。

## Local Load Balancer のマーケティング終了 (EOM) の発表日と発効日はいつですか?
{: faq}

EOM 発表日は 2019 年 3 月 1 日、発効日は 2019 年 6 月 1 日です。
この日付より後に新たな販売はなされません。

## EOM の後にサポートは利用可能ですか?
{: faq}

はい、Local Load Balancer の既存のお客様は、サポートを利用いただけます。

## どうすれば IBM Cloud Load Balancer を始めることができますか?
{: faq}

手始めに、[IBM Cloud Load Balancer のドキュメンテーション](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-getting-started)をお読みになるようお勧めします。

## Local Load Balancer サービスから IBM Cloud Load Balancer へのマイグレーション・パスは存在しますか?
{: faq}

自動化されたマイグレーション・パスは存在しません。
しかし、IBM Cloud Console から、Local Load Balancer のサービスをオフにするように請求し、Cloud Load Balancer のサービスを注文することができます。

## Local Load Balancer と Cloud Load Balancer の間にはどんな違いがありますか?
{: faq}

Local Load Balancer はハードウェア・ベースのローカル・ロード・バランシング・サービスですが、IBM Cloud Load Balancer はクラウド・ネイティブのサービスであり、コスト効率が高く、自動スケーリングのロード・バランシング・ソリューションを提供し、公衆ネットワークでもプライベート・ネットワークでもサポートされます。

## Cloud Load Balancer では Local Load Balancer と同じ用語が使用されていますか?
{: faq}

一部違っています。
Local Load Balancer の主要な用語のうち、それに対応する Cloud Load Balancer の用語が異なっているものを次の表に示します。

| Local Load Balancer の用語 | Cloud Load Balancer の用語 |
| ------------- | ------------- |
| サービス・グループ | プロトコル |
| サービス | サーバー・インスタンス |
| VIP | FQDN |

## Cloud Load Balancer にマイグレーションした場合も、ロード・バランサーの IP アドレスは単一の固定 IP アドレスですか?
{: faq}

IBM Cloud Load Balancer の IP は固定ではありません。
Cloud Load Balancer は、1 つのプールからロード・バランサー・インスタンスを割り当てます。
それには、常に完全修飾ドメイン・ネーム (FQDN) が必要です。
その結果、Cloud Load Balancer の個々の IP アドレスは違う場合があります。

## 公開/プライベート VSI およびベアメタル・ソリューションで IBM Cloud Load Balancer は使用可能ですか?
{: faq}

はい、Cloud Load Balancer は、公開 VSI およびプライベート VSI、さらにベアメタルで使用可能です。

## IBM Cloud Load Balancer は GDPR に準拠していますか?
{: faq}

はい、Cloud Load Balancer のオファリングは GDPR に準拠しています。

## マイグレーション開始後、システムのダウン時間またはトラフィックの中断時間はどれほどになりますか?

ロード・バランサー・マイグレーションの結果として、ダウン時間やトラフィックの中断は発生しません。
ダウン時間またはトラフィック中断が発生する可能性があるのは、Local Load Balancer の構成を新しい IBM Cloud Load Balancer FQDN に更新する場合だけです。

## 指示では、Local Load Balancer をキャンセルする前に IBM Cloud Load Balancer を注文することになっています。
2 つのデバイスを構成している間に、システムまたはワークロードに影響はないのでしょうか?

ありません。Cloud Load Balancer と Local Load Balancer は、互いに独立して動作する 2 つの別個のオファリングです。

## 私の Local Load Balancer では「1 秒あたりの接続数」オプションを選択していました。
Cload Load Balancer でもそれを構成する必要がありますか?

いいえ。IBM Cloud Load Balancer では、その負荷キャパシティーが自動調整されます。
それについては、[Cloud Load Balancer 水平スケーリング](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-performing-ibm-cloud-load-balancer-basics#horizontal-scaling)のトピックを参照してください。

## Cloud Load Balancer を使用する場合には、どんなプロトコルを選択できますか?

HTTP、HTTPS、および TCP プロトコルを選択できます。
レイヤー 7 サポートも提供されています。
詳しくは、[機能の概要](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-about-ibm-cloud-load-balancer#overview-of-features)を参照してください。

## 私は特定のタイプの暗号を必要としています。
Cloud Load Balancer では、それがサポートされますか?

IBM Cloud Load Balancer では、SSL オフロードのある TLS バージョン 1.2 がサポートされています。
サポートされる SSL 暗号については、[Cloud Load Balancer SSL 暗号スイート](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-ssl-offload-with-ibm-cloud-load-balancer#ssl-cipher-suites)を参照してください。
