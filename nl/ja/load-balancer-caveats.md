---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-07"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 既知の制限事項

プロキシー・ロード・バランサーの性質により、クライアント要求のソース IP は、ロード・バランサーの IP になります。 このことは、クライアント情報を取得するためにソース IP を確認するログ統計プログラムやその他のアプリケーションに影響を与えます。 IBM Cloud には、Apache (すべてのプラットフォーム) および IIS (Windows) 用にログ項目を正しく再書き込みするためのソリューションが用意されています。

説明や必要な追加プラグインにアクセスするためには、まず [IBM Cloud VPN](https://console.bluemix.net/docs/infrastructure/iaas-vpn/getting-started.html){: new_window} に接続する必要があります。 接続したら、[「ダウンロード」ページ](http://downloads.softlayer.local/loadbalancer/){: new_window} にアクセスして、ご使用の{{site.data.keyword.loadbalancer_short}}用のプラグインと説明を見つけてください。
