---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud

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

# Local Load Balancer から IBM Cloud Load Balancer へのマイグレーション

Local Load Balancer から IBM© Cloud Load Balancer にマイグレーションするには、次の手順を実行します。

## ステップ 1: Cloud Load Balancer を注文する
{: #step-1-order-a-cloud-load-balancer}

IBM Cloud Load Balancer サービスを注文するには、[IBM Cloud カタログ ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")]( https://cloud.ibm.com/catalog/infrastructure/load-balancer-group){:new_window} から**「IBM Cloud Load Balancer」**を選択します。**「作成」**をクリックした後、次の手順を実行します。

1. 名前や説明など、サービスの基本的なパラメーターを定義します。
2. データ・センターを選択します。
3. ロード・バランサーのタイプとして**「パブリック」**を選択します。
4. ロード・バランサーをデプロイするサブネットを選択します。

  ロード・バランサー・サービス・インスタンスは、このサブネット上にいずれかのネットワーク・インターフェースを持ちます。
アプリケーション・サーバーがこのサブネット上にあるか、またはこのサブネットから到達できることを確認してください。
必要な場合は、VLAN スパンニングを有効にします。
　{: note}

5. 自分の Local Load Balancer で現在使用しているサービス・グループと同じ構成で、フロントエンドとバックエンドのアプリケーション・プロトコルおよびポートを作成します。
この構成については、[IBM Cloud Load Balancer のパラメーターの構成](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configuring-ibm-cloud-load-balancer-parameters)を参照してください。
6. SSL オフロードを有効にするには、フロントエンド・プロトコルを HTTPS に、またバックエンド・プロトコルを HTTP に設定します。
それから、「証明書」ドロップダウン・ボックスから Local Load Balancer と同じ SSL 証明書を選択します。
既存の SSL 証明書はすべて [IBM Cloud 証明書ストア ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://cloud.ibm.com/classic/security/sslcerts){:new_window} によって管理されているため、Local Load Balancer で使用する証明書はドロップダウン・リストに含まれています。
7. 必要な場合は、ヘルス・チェック・パラメーターを調整してください。そうでない場合、デフォルト設定を使用します。
ヘルス・チェック・パラメーターについては、[IBM Cloud Load Balancer のパラメーター](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configure-health-checks)を参照してください。
8. Local Load Balancer サービスで使用していたサーバー・インスタンスを追加するには、**「サーバーに接続」**をクリックします。
9. ページを確認し、サービスのご使用条件に同意した上で、**「作成」**をクリックします。

ロード・バランサーのリストが表示され、そこにサービス・インスタンスのすべてが表示されます。

新たに作成したロード・バランサーは、このリストにすぐには表示されない場合があります。
数分後には、新しいロード・バランサーがグレー表示されます。
これは、そのステータスが`オフライン`であることを示しています。
さらに数分後、新しいロード・バランサーは緑色の表示になります。
これは、それが`オンライン`であることを示しています。
画面を最新表示しないと、それらの変化が表示されないことがあります。
{: note}

このページにあるサービス名をクリックすると、そのサービスの概要ページが表示されます。
**「プロトコル」**タブ、**「ヘルス・チェック」**タブ、および**「サーバー・インスタンス」**タブにナビゲートして、構成をさらに編集することができます。

## ステップ 2: Cloud Load Balancer が期待どおりに動作していることを確認する
{: #step-2-verify-your-cloud-load-balancer-is-working-as-expected}

この時点では、以前の Local Load Balancer と新しい IBM Cloud Load Balancer の 2 つのロード・バランサーが同時に稼働しています。
{: important}

上記のステータス・ページに示されているドメインを使用して新しい IBM Cloud Load Balancer をテストし、それが Local Load Balancer の VIP と同じように機能していることを確認します。

その後、Local Load Balancer VIP を使用するロケーションがあれば、それを更新して、その代わりに新しい Cloud Load Balancer ドメインを使用するようにします。

新しい Cloud Load Balancer のこの構成作業が、マイグレーション・プロセスの中でダウン時間またはトラフィックの中断が発生する唯一のタイミングです。
{: note}

## ステップ 3: 古い Local Load Balancer をキャンセルする
{: #step-3-cancel-your-local-load-balancer}

Local Load Balancer VIP のすべてを新しい IBM Cloud Load Balancer のドメインで置き換えて、機能が予期されるとおりに動作することを確認したら、Local Load Balancer のサービスをキャンセルしても大丈夫です。
そのためには、次の手順を実行します。

1. [「Local Load Balancer リスト (Local Load Balancer list)」ページ](https://cloud.ibm.com/classic/network/loadbalancing/local)に移動します。
2. 削除するロード・バランサーを見つけ、その横にある矢印を展開します。
3. 行の末尾にある赤い**「X」**をクリックして、ロード・バランサーをキャンセルします。
