---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 刪除服務群組

刪除「服務群組」時，也會刪除與「群組」相關聯的所有「服務」。請遵循以下的步驟來刪除 {{site.data.keyword.loadbalancer_short}} 的「服務群組」。

1. 從[本端負載平衡器詳細資料](view-all-load-balancers.html)頁面中，識別您要刪除的「服務群組」列，然後按一下**動作 > 移除群組**。
2. 按一下**儲存配置**。

刪除「服務群組」之後，會從 {{site.data.keyword.loadbalancer_short}} 中將其移除。所有相關聯的「服務」也會予以刪除，且會提供與「服務群組」相關聯的「虛擬埠」，以備將來另一個「服務群組」所需。刪除之後，必須為任何剩餘的群組手動變更其餘「服務群組」的「連線配置」百分比。
