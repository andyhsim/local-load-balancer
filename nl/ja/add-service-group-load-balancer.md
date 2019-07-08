---
copyright:
  years: 1994,2017,2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# ロード・バランサーへのサービス・グループの追加
{: #adding-a-service-group-to-a-load-balancer}

{{site.data.keyword.loadbalancer_short}}が追加されたら、その{{site.data.keyword.loadbalancer_short}}に新しいサービス・グループをいつでも追加できます。 サービス・グループはさまざまなグループ・タイプで使用可能であり、幅広い単一またはハイブリッドのバランシング方法を提供します。 新しいサービス・グループを追加するときは、すべてのグループの「接続割り振り」の合計が確実に 100% になるようにすることが重要です。新しいサービス・グループを{{site.data.keyword.loadbalancer_short}}に追加するには、以下の手順に従ってください。

1. [「ローカル・ロード・バランサーの詳細」](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details)ページで、**「グループの追加」**ボタンをクリックします。 あるいは、**「アクション」>「グループの追加」**をクリックできます。 新しい「サービス・グループ」セクションがページの下部に追加されます。
2. **「グループ」**ドロップダウン・リストから、希望するグループ・タイプを選択し、**「方法」**ドロップダウン・リストから、希望するバランシング方法を選択します。 各ロード・バランシング方法について詳しくは、[ロード・バランシング方法](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-load-balancing-methods#load-balancing-methods)を参照してください。
3. **「仮想ポート」**フィールドに、サービス・グループに使用するポート番号を入力します。 詳細情報については、[共通のサービス・ポートに関する FAQ ](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-faqs-for-local-load-balancer#what-services-can-be-load-balanced-)を参照してください。

	**注:** 各サービス・グループは、固有のポートに割り当てる必要があります。 固有のポートが割り当てられていない場合、ページの上部にエラーが表示され、固有の仮想ポートが割り当てられるまでサービス・グループを追加できません。
4. **「割り振り」**フィールドに割り振りを入力します。
5. 必要な場合、**「メモ」**テキスト・ボックスにメモを入力します。
6. **「構成の保存」**ボタンをクリックして、新しいサービス・グループを追加します。 アクションをキャンセルするには、**「キャンセル」**をクリックします。

サービス・グループを追加した後は、そのサービス・グループをいつでも削除または編集できます。 サービス・グループへの接続をリセットしたり、新しいサービスをグループに追加したりすることもできます。 サービス・グループが、割り当てられた「接続割り振り」に基づいて負荷のバランシングを開始するためには、1 つ以上のサービスがそのサービス・グループに[追加](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group)されている必要があります。

## 次のステップ
{: #what-happens-next-a}

[サービスをサービス・グループに追加します](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group)。
