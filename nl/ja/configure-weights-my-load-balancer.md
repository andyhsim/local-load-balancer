---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# ロード・バランサーの重みづけの構成
{; #configuring-weights-for-the-load-balancer}

重みづけとは、より多くのトラフィックを受信させたいサーバーに数値を割り当てるシステムです。 サーバーがヘルス・チェックに準じてオンラインであれば、数値が大きいほど優先順位が高いことを示しています。  

例えば、_server1_ の重みが 80 で、_server2_ の重みが 20 の場合、着信する 10 個の接続ごとに、_server1_ には 8 個が割り振られ、_server2_ には 2 個が割り振られます。_server1_ がオフラインになったり、プールから削除されたりすると、すべての接続が _server2_ に割り振られます。

[サービス・グループにサービスを追加](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group)するとき、または作成後に[サービスを編集](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service)することによって、特定のサービスの重みづけを構成することができます。

構成が保存されると、変更は即時有効になります。 サービスの接続は、サービスの詳細でモニターできます。
