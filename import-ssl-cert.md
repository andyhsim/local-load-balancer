---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Importing an SSL Certificate

After an SSL Certificate is issued for a website, it may be imported into the Customer Portal. By importing SSL Certificates into the Customer Portal, the Certificates may be applied to products and services that may require them, such as a Load Balancer's SSL Offloading. By default, SSL Certificates issued by IBM© Cloud are not imported into the list, as they are intended to be manipulated by the recipient only. Therefore, any SSL Certificate for use with an IBM Cloud product or service must be manually imported by an authorized user on the account.

Perform the following procedure to import an SSL Certificate into the Customer Portal.

1. From your browser, open  [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} and log into your account.
2. In the Customer Portal navigation, select **Security > SSL > Certificates**.
3. Click the **Import SSL Certificate** link on the top right hand side of the **SSL Certificates** page.
2. Enter the SSL Certificate Details. 

	**Note:** Details entered in the Import SSL Certificate pop-up box must be entered exactly as provided by the certificate authority, including spacing and line breaks. If they are not entered exactly as provided, an error will occur. Populate the fields as follows:
  - **Certificate:**  Certificate details, provided by the certificate authority. This is generally an alpha-numeric block of text.
  - **Private Key:**  Details for the private key, provided by the certificate authority. This is generally an alpha-numeric block of text.
  - **Intermediate Certificate:** Intermediate Certificate details, provided by the certificate authority. Intermediate Certificates are not required. However, if the information is available for the SSL Certificate, it should be entered.
  - **Certificate Signing Request:** Certificate Signing Request (CSR) details, provided by the certificate authority. CSR details are not required, but should be provided if they are part of the Certificate. Do not change the CSR in any way. A public key may be included with the CSR and should not be replaced by the Private Key.
  - **Notes:** Any notes regarding the SSL Certificate that may be helpful to other users.
4. Click **Import** to import the SSL Certificate. Click **Cancel** to cancel the action.

After the SSL Certificate has been imported to the Customer Portal, it will be stored on the SSL Certificates screen until it is manually deleted. For all products or services requiring SSL Certificate details, the new SSL Certificate will appear in the list of available certificates for use when interacting with the SSL feature for the desired product or service. You can update the certificate or securely download its details at any time.