---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# サービスの削除
{: #deleting-a-service}

サービスは、{{site.data.keyword.loadbalancer_short}}のサービス・グループに追加された後、いつでも削除できます。 サービス・グループからサービスを削除すると、そのサービスは、手動でサービス・グループに追加し直さない限り、{{site.data.keyword.loadbalancer_short}}で使用できなくなります。 

代替方法として、サービスを無効にすることもできます。こうすると、そのサービスはバランシング操作には使用できなくなりますが、サービス・グループには関連付けられたままになります。 サービスを{{site.data.keyword.loadbalancer_short}}のサービス・グループに関連付けられたままにするには、[サービスを編集](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service)し、**「有効」**チェック・ボックスのチェック・マークを外します。 

{{site.data.keyword.loadbalancer_short}}からサービスを削除するには、以下の手順を実行します。

1. [「ローカル・ロード・バランサーの詳細」](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details)ページで、削除するサービスを見つけ、左側の矢印を展開します。
2. サービスの行の終わりにある赤い「x」をクリックします。
3. 設定を更新するために、ページ下部の**「構成の保存」**をクリックします。

サービスを削除した後、構成が保存され、変更はすぐに有効になります。 削除したサービスが、サービス・グループに関連付けられている唯一のサービスの場合、そのグループは、新しいサービスが追加されるまでロード・バランシング・アクティビティーを実行できなくなります。
