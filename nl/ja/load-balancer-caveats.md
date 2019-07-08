---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:note: .note}

# ローカル・ロード・バランサーの既知の制限事項
{: #known-limitations-with-local-load-balancer}

プロキシー・ロード・バランサーの性質により、クライアント要求のソース IP は、ロード・バランサーの IP になります。 このことは、クライアント情報を取得するためにソース IP を確認するログ統計プログラムやその他のアプリケーションに影響を与えます。 IBM© Cloud には、Apache (すべてのプラットフォーム) および IIS (Windows) 用にログ項目を正しく再書き込みするためのソリューションが用意されています。

説明や必要な追加プラグインにアクセスするためには、まず IBM Cloud VPN に接続する必要があります。 接続したら、[「ダウンロード」ページ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://downloads.softlayer.local/loadbalancer/){: new_window}にアクセスして、ご使用の{{site.data.keyword.loadbalancer_short}}用のプラグインと説明を見つけてください。

ダウンロード・リンクにアクセスするには IBM Cloud VPN にログインする必要があります。
{: note}
