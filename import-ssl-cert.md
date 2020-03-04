---
copyright:
  years: 1994, 2019
lastupdated: "2019-11-14"

keywords: import, ssh, certificate, load balancing
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank_"}

# Importing an SSL certificate
{: #importing-an-ssl-certificate}

After an SSL Certificate is issued for a website, it may be imported into the {{site.data.keyword.cloud}} console. By importing SSL Certificates into the console, the Certificates may be applied to products and services that may require them, such as the IBM Cloud Load Balancer's SSL Offloading. By default, SSL Certificates issued by {{site.data.keyword.cloud_notm}} are not imported into the list, as they are intended to be manipulated by the recipient only. Therefore, any SSL Certificate for use with an {{site.data.keyword.cloud_notm}} product or service must be manually imported by an authorized user on the account.
{: shortdesc}

Perform the following procedure to import an SSL Certificate into the Cloud console.

1. From your browser, open the [IBM Cloud catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com){:new_window} and log into your account.
2. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) from the top left, then click **Classic Infrastructure**.
3. From the left, select **Security > SSL > Certificates**.
4. Click the **Import SSL Certificate** link on the top right hand side of the **SSL Certificates** page.
5. Enter the SSL Certificate Details.

	**Note:** Details entered in the Import SSL Certificate pop-up box must be entered exactly as provided by the certificate authority, including spacing and line breaks. If they are not entered exactly as provided, an error will occur. Populate the fields as follows:
  - **Certificate:**  Certificate details, provided by the certificate authority. This is generally an alpha-numeric block of text.
  - **Private Key:**  Details for the private key, provided by the certificate authority. This is generally an alpha-numeric block of text.
  - **Intermediate Certificate:** Intermediate Certificate details, provided by the certificate authority. Intermediate Certificates are not required. However, if the information is available for the SSL Certificate, it should be entered.
  - **Certificate Signing Request:** Certificate Signing Request (CSR) details, provided by the certificate authority. CSR details are not required, but should be provided if they are part of the Certificate. Do not change the CSR in any way. A public key may be included with the CSR and should not be replaced by the Private Key.
  - **Notes:** Any notes regarding the SSL Certificate that may be helpful to other users.
6. Click **Import** to import the SSL Certificate. Click **Cancel** to cancel the action.

After the SSL Certificate has been imported to the IBM Cloud console, it will be stored on the SSL Certificates screen until it is manually deleted. For all products or services requiring SSL Certificate details, the new SSL Certificate will appear in the list of available certificates for use when interacting with the SSL feature for the desired product or service. You can update the certificate or securely download its details at any time.
