---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud

subcollection: local-load-balancer

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# 將 Local Load Balancer 移轉至 IBM Cloud Load Balancer

您可以執行下列程序，將 Local Load Balancer 移轉至 IBM© Cloud Load Balancer。

## 步驟 1：訂購 Cloud Load Balancer
{: #step-1-order-a-cloud-load-balancer}

若要訂購 IBM Cloud Load Balancer 服務，請從 [IBM Cloud 型錄 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")]( https://cloud.ibm.com/catalog/infrastructure/load-balancer-group){:new_window} 選取 **IBM Cloud Load Balancer**。按一下**建立**，然後執行下列程序：

1. 定義基本服務參數，例如名稱及說明。
2. 選取資料中心。
3. 選取**公用**負載平衡器類型。
4. 選取您要部署負載平衡器的子網路。

  在此子網路上，負載平衡器服務實例會有它的一個網路介面。請確定應用程式伺服器位在此子網路上或可透過此子網路連接。必要的話，請啟用 VLAN Spanning。
  {: note}

5. 使用與 Local load Balancer 中目前所使用之服務群組相同的配置，建立前端和後端應用程式的通訊協定及埠。如需此配置的相關資訊，請參閱[配置 IBM Cloud Load Balancer 參數](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configuring-ibm-cloud-load-balancer-parameters)。
6. 若要啟用 SSL 卸載功能，請將前端通訊協定設為 HTTPS，並將後端通訊協定設為 HTTP。接著，從「憑證」下拉方塊中選取與 Local Load Balancer 相同的「SSL 憑證」。您可與 Local Load Balancer 搭配使用的「憑證」位於下拉清單中，因為所有現有的 SSL 憑證都是透過 [IBM Cloud 憑證庫  ![外部鏈結圖示 ](../../icons/launch-glyph.svg "外部鏈結圖示 ")](https://cloud.ibm.com/classic/security/sslcerts){:new_window} 進行管理。
7. 視需要調整性能檢查參數，否則，請使用預設值。如需性能檢查參數的相關資訊，請參閱 [IBM Cloud Load Balancer 參數](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configure-health-checks)。
8. 按一下**附加伺服器**，以新增您用於 Local Load Balancer 服務的所有伺服器實例。
9. 檢閱該頁面，確認「服務合約」，然後按一下**建立**。

即會顯示 Load Balancer 清單，其中顯示所有的服務實例。

新建立的負載平衡器可能不會立即顯示在此清單中。幾分鐘之後，新的負載平衡器將以灰色顯示，表示其狀態為 `Offline`。再過幾分鐘後，新的負載平衡器會顯示綠色，表示其為 `Online`。您可能需要重新整理畫面，才能看到這些變更。
{: note}

在此頁面上按一下服務名稱，會帶領您前往服務概觀頁面。您可以導覽至**通訊協定**、**性能檢查**及**性伺服器實例**標籤，以進一步編輯配置。

## 步驟 2：驗證 Cloud Load Balancer 如預期般運行
{: #step-2-verify-your-cloud-load-balancer-is-working-as-expected}

請注意，在此時，您有兩個負載平衡器同時運行：舊的 Local Load Balancer 及新的 IBM Cloud Load Balancer。
{: important}

請使用上述狀態頁面中所列的網域測試新的 IBM Cloud Load Balancer，以確定其功能與 Local load Balancer 中的 VIP 相同。

接著，請更新所有使用 Local Load Balancer VIP 的位置，以改用新的 Cloud Load Balancer 網域。

這個新 Cloud Load Balancer 配置將是移轉處理程序中可能遭遇運作中斷或傳輸中斷的唯一時間。
{: note}

## 步驟 3：取消舊的 Local Load Balancer
{: #step-3-cancel-your-local-load-balancer}

如果您已使用新 IBM Cloud Load Balancere 的網域取代所有 Local load Balancer VIP，並驗證功能如預期般運行，您就可以安全地取消 Local Load Balancer 服務。若要這樣做，請執行下列步驟：

1. 移至 [Local Load Balancer 清單頁面](https://cloud.ibm.com/classic/network/loadbalancing/local)。
2. 找到您要刪除的 Load Balancer，並展開它旁邊的箭頭。
3. 按一下列尾的紅色 **X**，以取消該 Load Balancer。
