---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# サービス・グループの削除
{: #deleting-a-service-group}

サービス・グループを削除するときは、そのグループに関連付けられているすべてのサービスも削除されます。 {{site.data.keyword.loadbalancer_short}}のサービス・グループを削除するには、以下の手順を実行します。

1. [「ローカル・ロード・バランサーの詳細」](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details)ページで、削除するサービス・グループの行を識別し、**「アクション」>「グループの削除」**をクリックします。
2. **「構成の保存」**をクリックします。

サービス・グループを削除すると、そのサービス・グループは{{site.data.keyword.loadbalancer_short}}から削除されます。 関連付けられたすべてのサービスも削除され、そのサービス・グループに関連付けられた仮想ポートが、将来、別のサービス・グループで必要になった場合に備えて使用可能になります。 削除の際には、残りのすべてのグループについて、残りのサービス・グループの「接続割り振り」のパーセンテージを手動で変更する必要があります。
