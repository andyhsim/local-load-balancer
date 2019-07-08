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

# Migración de Local Load Balancer a IBM Cloud Load Balancer

Puede migrar su Local Load Balancer a IBM© Cloud Load Balancer siguiendo el procedimiento siguiente.

## Paso 1: Pedir un Cloud Load Balancer
{: #step-1-order-a-cloud-load-balancer}

Para solicitar un servicio IBM Cloud Load Balancer, seleccione **IBM Cloud Load Balancer** en el [catálogo de IBM Cloud ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")]( https://cloud.ibm.com/catalog/infrastructure/load-balancer-group){:new_window}. Pulse **Crear**, y siga el procedimiento siguiente:

1. Defina los parámetros de servicio básicos, como el nombre y la descripción.
2. Seleccione el centro de datos.
3. Seleccione el tipo de equilibrador de carga **Público**.
4. Seleccione la subred en la que desee desplegar el equilibrador de carga.

  La instancia del servicio de equilibrador de carga tendrá una de las interfaces de red en esta subred. Asegúrese de que los servidores de aplicaciones estén en esta subred o sean accesibles desde la misma. Si es necesario, habilite la expansión de VLAN.
  {: note}

5. Cree protocolos y puertos de aplicaciones frontales y de fondo con la misma configuración que los grupos de servicios que utiliza actualmente en su Local Load Balancer. Para obtener más información sobre esta configuración, consulte [Configuración de los parámetros de IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configuring-ibm-cloud-load-balancer-parameters).
6. Para habilitar la descarga SSL, establezca los protocolos frontales en HTTPS y los protocolos de fondo en HTTP. A continuación, seleccione el mismo certificado SSL que tiene para Local Load Balancer en el recuadro desplegable Certificado. El certificado que utiliza con Local Load Balancer está en la lista desplegable porque todos los certificados SSL existentes están gestionados a través del [Almacén de certificados de IBM Cloud ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/classic/security/sslcerts){:new_window}.
7. Ajuste los parámetros de la comprobación de estado si lo desea; de lo contrario, utilice los valores predeterminados. Para obtener más información sobre los parámetros de comprobación de estado, consulte [Parámetros de IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configure-health-checks).
8. Pulse **Adjuntar servidor** para añadir las instancias de servidor que utilizaba para el servicio Local Load Balancer.
9. Revise la página, confirme el acuerdo de servicio y pulse **Crear**.

Se muestra la lista del equilibrador de carga con todas las instancias de servicio.

Puede que el equilibrador de carga que acaba de crear no se muestre inmediatamente en esta lista. Al cabo de unos pocos minutos, se visualizará el nuevo equilibrador de carga de color gris, que indica que está en estado `Offline`. Después de otros pocos minutos, el nuevo equilibrador de carga estará de color verde, que indica que está `Online`. Puede que tenga que renovar la pantalla para ver estos cambios.
{: note}

Al pulsar el nombre de servicio en la página, irá a la página de visión general del servicio. Puede desplazarse por los separadores **Protocolos**, **Comprobaciones de estado** e **Instancias de servidor** para editar la configuración.

## Paso 2: Verifique que Cloud Load Balancer funciona como se espera
{: #step-2-verify-your-cloud-load-balancer-is-working-as-expected}

En ese punto, asegúrese de tener los equilibradores de carga funcionando a la vez: el antiguo Local Load Balancer y el nuevo IBM Cloud Load Balancer.
{: important}

Pruebe el nuevo IBM Cloud Load Balancer utilizando el dominio que se lista en la página de estado arriba, asegurándose de que funciona igual que la VIP de Local Load Balancer.

A continuación, actualice las ubicaciones que utilizan la VIP de Local Load Balancer para que utilicen en su lugar el nuevo dominio de Cloud Load Balancer.

Durante esta configuración del nuevo Cloud Load Balancer será la única vez que experimentará tiempo de inactividad o interrupción de tráfico en todo el proceso de migración.
{: note}

## Paso 3: Cancele el antiguo Local Load Balancer
{: #step-3-cancel-your-local-load-balancer}

Cuando haya sustituido todas las VIP de Local Load Balancer por el dominio del nuevo IBM Cloud Load Balancer y haya verificado que la funcionalidad es correcta, puede cancelar de forma segura el servicio Local Load Balancer. Para ello, realice los pasos siguientes:

1. Vaya a la [página de lista de Equilibradores de carga locales](https://cloud.ibm.com/classic/network/loadbalancing/local).
2. Localice el equilibrador de carga que desee suprimir y expanda la flecha que hay al lado.
3. Pulse en la **X** roja del final de la fila para cancelar el equilibrador de carga.
