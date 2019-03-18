---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# ロード・バランサーでの SSL オフロードの構成
{: #configuring-ssl-offloading-on-a-load-balancer}

ロード・バランサーは SSL オフロードを提供することができます。それにより、現在 SSL 機能を実行しているシステムの負荷を大幅に削減できます。 SSL オフロードを使用するには、この機能を提供する{{site.data.keyword.loadbalancer_short}}を購入する必要があります。 SSL オフロード機能を提供するロード・バランサーには、**「ローカル・ロード・バランサーの注文」**ダイアログで「SSL オフロード付き」の注釈が付いています。 SSL オフロード対応の{{site.data.keyword.loadbalancer_short}}は、プロビジョンした後に構成する必要があります。 以下のステップに従って、{{site.data.keyword.loadbalancer_short}}に SSL オフロードを構成します。

1. [「ローカル・ロード・バランサーの詳細」](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details)ページから、ロード・バランサーのドロップダウン・メニューで**「アクション」>「SSL の構成」**をクリックします。
2. **「証明書」**ドロップダウン・ボックスから、目的の SSL 証明書を選択します。 以下の点に注意してください。
  - 非専用{{site.data.keyword.loadbalancer_short}}仮想 IP (VIP) は、SSL 証明書の最大ビット・サイズが 2048 に制限されています。
  - このステップを正常に完了するには、少なくとも 1 つの SSL 証明書がカスタマー・ポータルに保管されている必要があります。 [SSL 証明書のインポート](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-importing-an-ssl-certificate)を参照してください。
3. **「有効」**チェック・ボックスを選択します。
4. サポートする暗号を選択します。
5. **「更新」**ボタンをクリックします。

{{site.data.keyword.loadbalancer_short}}で SSL オフロードをアクティブにすると、SSL の状態が**「無効」**から**「アクティブ」**に変わります。 以前 SSL 接続を処理したシステムにかかっていた負荷は、SSL オフロードがアクティブになると、通常減少します。 オフロードの状況はいつでも変更できます。 {{site.data.keyword.loadbalancer_short}}の SSL オフロードを無効にするには、「SSL オフロード」タブに戻り、チェック・ボックスを選択解除します。
