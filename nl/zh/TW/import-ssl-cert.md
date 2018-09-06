---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 匯入 SSL 憑證

在為網站發出「SSL 憑證」之後，可能會將其匯入「客戶入口網站」。透過將「SSL 憑證」匯入「客戶入口網站」中，「憑證」可套用至可能需要它們的產品和服務，例如「負載平衡器」的「SSL 卸載功能」。依預設，IBM Cloud 所發出的「SSL 憑證」不會匯入到清單中，因為它們預期只會由接受者操作。因此，任何用於 IBM Cloud 產品或服務的「SSL 憑證」都必須由該帳戶上的授權使用者手動匯入。

請執行下列程序來將「SSL 憑證」匯入「客戶入口網站」中。

1. 從您的瀏覽器中，開啟[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window} 並登入您的帳戶。
2. 在「客戶入口網站」導覽中，選取**安全 > SSL > 憑證**。
3. 按一下 **SSL 憑證**頁面右上角的**匯入 SSL 憑證**鏈結。
2. 輸入「SSL 憑證詳細資料」。 

	**附註：**「匯入 SSL 憑證」蹦現框中所輸入的詳細資料必須完全依憑證管理中心所提供的內容來輸入，包括間距和換行。若未完全依所提供的內容來輸入，則會發生錯誤。如下所示將資料移入欄位中：
  - **憑證：**憑證管理中心所提供的憑證明細。一般這是一個英數的文字區塊。
  - **私密金鑰：**憑證管理中心所提供的「憑證」詳細資料。一般這是一個英數的文字區塊。
  - **中繼憑證：**憑證管理中心所提供的「中繼憑證」詳細資料。「中繼憑證」不是必要的。但是，如果有「SSL 憑證」的資訊可用，則應輸入該資訊。
  - **憑證簽署要求：**憑證管理中心所提供的「憑證簽署要求 (CSR)」詳細資料。CSR 詳細資料不是必要的，但如果它們是「憑證」的一部分，則應提供。請勿以任何方式變更 CSR。公開金鑰可以附於 CSR 中，且不應被「私密金鑰」所取代。
  - **附註：**可能對其他使用者有幫助的任何「SSL 憑證」相關附註。
4. 按一下**匯入**以匯入「SSL 憑證」。按一下**取消**即可取消動作。

在將「SSL 憑證」匯入「客戶入口網站」之後，它會儲存在「SSL 憑證」畫面上，直到手動將其刪除為止。對於需要「SSL 憑證」明細的所有產品或服務，新的「SSL 憑證」會出現在可用憑證的清單中，以便在與所要產品或服務的 SSL 特性互動時使用。您可以隨時更新憑證或安全地下載其詳細資料。