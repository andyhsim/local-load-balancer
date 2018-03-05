---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 刪除服務 

在為 {{site.data.keyword.loadbalancer_short}} 將「服務」新增至「服務群組」之後，它可能隨時會被刪除。從「服務群組」中刪除「服務」會阻止該「服務」被 {{site.data.keyword.loadbalancer_short}} 使用，除非將其手動新增回到「服務群組」。 

或者，「服務」可能會已停用，這將使該「服務」與「服務群組」相關聯，同時使其無法用來平衡工作負載。若要使該「服務」與「{{site.data.keyword.loadbalancer_short}} 服務群組」相關聯，請[編輯服務](edit-service-load-balancer.html)並取消勾選**已啟用**勾選框。 

請遵循以下的步驟來從 {{site.data.keyword.loadbalancer_short}} 中刪除該「服務」。

1. 從[本端負載平衡器詳細資料](view-all-load-balancers.html)頁面中，找到您想要刪除的服務並展開左手邊的箭頭。
2. 按一下「服務」列尾的紅色 'x'。
3. 針對要更新的設定，按一下頁面底端的**儲存配置**。

刪除該「服務」之後，配置會加以儲存，而變更會立即生效。如果已刪除的「服務」是唯一與「服務群組」相關聯的服務，則在新增「服務」之前，該「群組」將無法執行任何「負載平衡」活動。
