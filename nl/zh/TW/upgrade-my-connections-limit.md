---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 升級連線限制
{: #upgrading-the-connections-limit}

「本端負載平衡器」可以隨時進行升級，增量為 250、500、1000、2500 和 5000。所做的所有變更都將以遞增的方式進行到下一個層次，但可以依次進行多個升級以跳過多個增量。 

若要升級連線限制，請遵循下列這些指示：

1. 從[本端負載平衡器詳細資料](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details)頁面中，針對「負載平衡器」按下拉功能表中的**動作 > 升級連線限制**。
2. 會顯示一個確認對話框，向您顯示負載平衡器的下一個可用增量和升級成本。按一下**是**以確認升級。按一下**否**即可取消動作。

新的連線限制會立即生效。
