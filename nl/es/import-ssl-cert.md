---
copyright:
  years: 1994, 2019
lastupdated: "2019-06-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Importar certificado SSL
{: #importing-an-ssl-certificate}

Una vez que se emite un certificado SSL para un sitio web, se puede importar en el portal de clientes de la infraestructura de {{site.data.keyword.cloud}}. Al importar certificados SSL en el portal de clientes, estos se aplicarán a productos y servicios que los puedan necesitar, como por ejemplo una descarga SSL del equilibrador de carga. De forma predeterminada, los certificados SSL emitidos por {{site.data.keyword.cloud_notm}} no se importan en la lista, ya que están pensados para ser manipulados solo por el destinatario. Por lo tanto, cualquier certificado SSL para utilizar con un producto o servicio de {{site.data.keyword.cloud_notm}} debe importarlo manualmente un usuario autorizado en la cuenta.

Realice el procedimiento siguiente para importar un certificado SSL en el portal de clientes.

1. En el navegador, abra el [portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} e inicie sesión en su cuenta.
2. En la navegación del portal de clientes, seleccione **Seguridad > SSL > Certificados**.
3. Pulse el enlace **Importar certificado SSL** en la parte superior derecha de la página **Certificados SSL**.
2. Especifique los detalles del certificado SSL. 

	**Nota:** Los detalles introducidos en el recuadro emergente Importar certificado SSL deben especificarse exactamente como lo proporciona la entidad emisora de certificados, incluidos el espaciado y los saltos de línea. Si no se especifican exactamente como se proporciona, se producirá un error. Rellene los campos de la siguiente manera:
  - **Certificado:** Detalles del certificado, proporcionados por la entidad emisora de certificados. Generalmente, se trata de un bloque de texto alfanumérico.
  - **Clave privada:** Detalles de la clave privada, proporcionados por la entidad emisora de certificados. Generalmente, se trata de un bloque de texto alfanumérico.
  - **Certificado intermedio:** Detalles del certificado intermedio, proporcionados por la entidad emisora de certificados. Los certificados intermedios no son necesarios. Sin embargo, si la información está disponible para el certificado SSL, debe introducirse.
  - **Solicitud de firma de certificado:** Detalles de la Solicitud de firma de certificado (CSR), proporcionados por la entidad emisora de certificados. Los detalles de CSR no son necesarios, pero deben proporcionarse si forman parte del certificado. No cambie la CSR de ningún modo. Debe incluirse una clave pública con la CSR y no debería reemplazarse por la Clave privada.
  - **Notas:** Cualquier nota sobre el certificado SSL que pueda ser útil para otros usuarios.
4. Pulse **Importar** para importar el certificado SSL. Pulse **Cancelar** si desea cancelar la acción.

Una vez que se haya importado el certificado SSL en el portal de clientes, se almacenará en la pantalla Certificados SSL hasta que se suprima manualmente. Para todos los productos o servicios que requieran detalles del certificado SSL, el nuevo certificado SSL aparecerá en la lista de certificados disponibles para su uso al interactuar con la característica SSL para el producto o servicio deseado. Puede actualizar el certificado o descargar de forma segura sus detalles en cualquier momento.
