---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 在負載平衡器上配置 SSL 卸載功能

「負載平衡器」有能力提供 SSL 卸載功能，其可顯著降低目前執行該功能的系統上的負載。為了使用 SSL 卸載功能，必須購買一個提供該功能的 {{site.data.keyword.loadbalancer_short}}。提供 SSL 功能的負載平衡器會在**訂購本端負載平衡器**對話框中標記「具有 SSL 卸載功能」。在佈建啟用 SSL 卸載功能的 {{site.data.keyword.loadbalancer_short}} 之後，它必須進行配置。請遵循以下的步驟，以在 {{site.data.keyword.loadbalancer_short}} 上配置 SSL 卸載功能。

1. 從[本端負載平衡器詳細資料](view-all-load-balancers.html)頁面中，針對「負載平衡器」按下拉功能表中的**動作 > 配置 SSL**。
2. 從**憑證**下拉方框中選取想要的 SSL 憑證。請記住下列事項：
  - 非專用的 {{site.data.keyword.loadbalancer_short}} 虛擬 IP (VIP) 限制為 2048 的最大 SSL 憑證位元大小。
  - 至少有一個 SSL 憑證必須儲存在「客戶入口網站」上，才能順利完成此步驟。請參閱[匯入 SSL 憑證](import-ssl-cert.html)。
3. 選取**已啟用**勾選框。
4. 選取您想要支援的密碼。
5. 按一下**更新**按鈕。

在 {{site.data.keyword.loadbalancer_short}} 上啟動 SSL 卸載功能之後，SSL 的狀態會從**已停用**變更為**作用中**。之前處理 SSL 連線的系統所承載的負載一般會在已啟動 SSL 卸載功能後減少。在任何時候，SSL 卸載功能狀態可能會變更。回到「卸載 SSL」標籤，然後取消選取勾選框，以停用 {{site.data.keyword.loadbalancer_short}} 的 SSL 卸載功能。
