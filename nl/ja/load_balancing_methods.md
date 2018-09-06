---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# ロード・バランシング方法

|方法|説明|
|:---|:---|
|整合したハッシュ IP|<ul><li>要求のソース IP をハッシュして、クライアント要求を実サーバーにマップします。</li><li>クライアント/サーバーの関係は、複数のポートにわたって維持されます。</li></ul>|
|Cookie の挿入|<ul><li>トラッキング Cookie を要求に挿入します。<span style="mso-spacerun:yes">&nbsp; </span>Cookie 内に含まれているセッション・データは、後続の要求で、同じ実サーバーにトラフィックを送信するために使用されます。</li><li>永続性は、セッションごとを基本としてハードコーディングされています。</li><li>クライアントのブラウザーが閉じられると、Cookie の有効期限が切れます。</li><li>クライアントが Cookie の有効化を受け入れる必要があります。</li></ul>|
|最小接続数|<ul><li>アクティブ接続の数が最も少ない実サーバーが 1 番の優先順位を取得します。</li><li>アルゴリズムで、10 個の接続の差異が要求されます。それにより、お客様のために結果のスキューを行うことができます。</li></ul>|
|永続 IP|<ul><li>要求を行っている IP アドレスの 4 オクテットすべてのハッシュによって、要求側のソース IP を、要求を処理する実サーバーに結合します。</li><li>60 分間持続します。</li></ul>|
|ラウンドロビン|<ul><li>新しい各要求は、交替で次の実サーバーに割り当てられます。</li><li>小規模サンプルでは不均衡なバランスが示される場合がありますが、大規模サンプルではバランスの取れた分散が行われます。</li></ul>|
|最短応答|<ul><li>応答時間の最も短いサーバーが要求を受信します。</li><li>ロードと応答時間が増えると、遅いサーバーの処理要求数が減少し始めます。</li></ul>|
|永続 IP のあるラウンドロビン|<ul><li>新しい各要求は、交替で次の実サーバーに割り当てられます。</li><li>要求側の IP アドレスは実サーバーに結合されており、その結果、その IP からの後続要求は同じ実サーバーに割り当てられます。</li></ul>|
|Cookie の挿入のあるラウンドロビン|<ul><li>新しい各要求は、交替で次の実サーバーに割り当てられます。</li><li>ロード・バランサーは、要求に Cookie を挿入し、後続の要求については、Cookie のセッション情報を使用して同じ実サーバーにトラフィックを送信します。</li></ul>|
|永続 IP のある最小接続|<ul><li>新しい各要求は、現時点でアクティブ接続の数が最も少ない実サーバーに割り当てられます。</li><li>要求側の IP アドレスは実サーバーに結合されており、その結果、その IP からの後続要求は同じ実サーバーに割り当てられます。</li></ul>|
|Cookie の挿入のある最小接続|<ul><li>新しい各要求は、現時点でアクティブ接続の数が最も少ない実サーバーに割り当てられます。</li><li>ロード・バランサーは、要求に Cookie を挿入し、後続の要求については、Cookie のセッション情報を使用して同じ実サーバーにトラフィックを送信します。</li></ul>|
|永続 IP のある最短応答|<ul><li>新しい各要求は、応答時間が最も短い実サーバーに割り当てられます。</li><li>要求側の IP アドレスは実サーバーに結合されており、その結果、その IP からの後続要求は同じ実サーバーに割り当てられます。</li></ul>|
|Cookie の挿入のある最短応答|<ul><li>新しい各要求は、応答時間が最も短い実サーバーに割り当てられます。</li><li>ロード・バランサーは、要求に Cookie を挿入し、後続の要求については、Cookie のセッション情報を使用して同じ実サーバーにトラフィックを送信します。</li></ul>|