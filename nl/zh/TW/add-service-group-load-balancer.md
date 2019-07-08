---
copyright:
  years: 1994,2017,2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 將服務群組新增至負載平衡器
{: #adding-a-service-group-to-a-load-balancer}

在已新增 {{site.data.keyword.loadbalancer_short}} 之後，新的「服務群組」可能隨時會新增至 {{site.data.keyword.loadbalancer_short}}。「服務群組」可在各式各樣的「群組類型」中取得，而且它提供一系列廣泛的單一或混合平衡方法。新增「服務群組」時，確保所有群組「連接配置」的總和等於 100% 是非常重要的。請遵循以下的步驟來將「服務群組」新增至 {{site.data.keyword.loadbalancer_short}}。

1. 從[本端負載平衡器詳細資料](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details)頁面中，按一下**新增群組**按鈕。或者，您可以按一下**動作 > 新增群組**。新的「服務群組」區段會新增至頁面的底端。
2. 從**群組**下拉清單中選取想要的「群組類型」，並從**方法**下拉清單中選取想要的「平衡方法」。如需每個負載平衡方法的相關資訊，請參閱[負載平衡方法](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-load-balancing-methods#load-balancing-methods)。
3. 在**虛擬埠**欄位中，輸入將用於服務群組的埠號。如需相關資訊，請參閱[一般服務埠常見問題 (FAQ)](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-faqs-for-local-load-balancer#what-services-can-be-load-balanced-)。

	**附註：**每個「服務群組」都必須指派給唯一的埠。若未指派唯一的埠，則會在頁面頂端出現錯誤，而「服務群組」可能必須等到指派唯一的虛擬入口網站之後才會加以新增。
4. 在**配置**欄位中輸入一個配置。
5. 在**附註**文字框中輸入任何附註（若想要的話）。
6. 按一下**儲存配置**按鈕，以新增「服務群組」。按一下**取消**即可取消動作。

新增「服務群組」之後，可以隨時加以刪除或編輯。可能會對「服務群組」重設連線，而且可能會將新的服務新增至群組中。為了讓「服務群組」根據其指派的「連線配置」來開始平衡負載，必須將一個以上的服務[新增](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group)至「服務群組」中。

## 後續情形
{: #what-happens-next-a}

[將服務新增至服務群組](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group)。
