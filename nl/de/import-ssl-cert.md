---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# SSL-Zertifikat importieren

Nachdem ein SSL-Zertifikat für eine Website ausgestellt wurde, kann es in das Kundenportal importiert werden. Durch den Import von SSL-Zertifikaten in das Portal können die Zertifikate auf Produkte und Services angewendet werden, für die sie erforderlich sind, beispielsweise für die SSL-Auslagerung einer Lastausgleichsfunktion. Standardmäßig werden SSL-Zertifikate, die von IBM Cloud ausgegeben werden, nicht in die Liste importiert, da sie nur vom Empfänger bearbeitet werden sollen. Daher müssen alle SSL-Zertifikate, die mit einem IBM Cloud-Produkt oder -Service verwendet werden sollen, manuell von einem berechtigten Benutzer für das Konto importiert werden.

Führen Sie die folgenden Schritte aus, um ein SSL-Zertifikat in das Kundenportal zu importieren.

1. Öffnen Sie das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} über einen Browser und melden Sie sich bei Ihrem Konto an.
2. Wählen Sie im Navigationsbereich des Kundenportals **Sicherheit > SSL > Zertifikate** aus.
3. Klicken Sie oben rechts auf der Seite **SSL-Zertifikate** auf den Link **SSL-Zertifikate importieren**.
2. Geben Sie die Details für das SSL-Zertifikat ein. 

	**Hinweis:** Die Details, die im Popup-Fenster zum Importieren von SSL-Zertifikatdetails eingegeben werden, müssen genauso wie von der Zertifizierungsstelle vorgegeben angegeben werden, einschließlich Abstand und Zeilenumbrüche. Wenn sie nicht exakt so eingegeben werden, tritt ein Fehler auf. Geben Sie in den Feldern die folgenden Werte ein:
  - **Zertifikat:** Zertifikatsdetails, die von der Zertifizierungsstelle bereitgestellt wurden. Hierbei handelt es sich für gewöhnlich um einen alphanumerischen Textblock.
  - **Privater Schlüssel:** Details für den privaten Schlüssel, die von der Zertifizierungsstelle bereitgestellt wurden. Hierbei handelt es sich für gewöhnlich um einen alphanumerischen Textblock.
  - **Zwischenzertifikat:** Details für das Zwischenzertifikat, die von der Zertifizierungsstelle bereitgestellt wurden. Zwischenzertifikate sind nicht obligatorisch. Wenn die Informationen jedoch für das SSL-Zertifikat verfügbar sind, sollten sie eingegeben werden.
  - **Zertifikatssignieranforderung:** Details für die Zertifikatssignieranforderung, die von der Zertifizierungsstelle bereitgestellt wurden. Diese Details sind zwar nicht erforderlich, sollten jedoch angegeben werden, wenn sie Teil des Zertifikats sind. Die Zertifikatssignieranforderung darf nicht geändert werden. Die Anforderung kann einen öffentlichen Schlüssel enthalten, der nicht durch den privaten Schlüssel ersetzt werden sollte.
  - **Anmerkungen:** Anmerkungen zum SSL-Zertifikat, die für andere Benutzer nützlich sein können.
4. Klicken Sie auf **Importieren**, um das SSL-Zertifikat zu importieren. Wenn Sie die Aktion abbrechen möchten, klicken Sie auf **Abbrechen**.

Nachdem das SSL-Zertifikat in das Kundenportal importiert wurde, wird es so lange in der Anzeige mit den SSL-Zertifikaten gespeichert, bis es manuell gelöscht wird. Für alle Produkte und Services, für die SSL-Zertifikatsdetails erforderlich sind, wird das neue SSL-Zertifikat bei der Interaktion mit der SSL-Funktion für das gewünschte Produkt oder den gewünschten Service in der Liste der verfügbaren Zertifikate angezeigt. Sie können das Zertifikat jederzeit aktualisieren oder die entsprechenden Details herunterladen.
