---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-02"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Preguntas más frecuentes
Este tema contiene respuestas a las preguntas más frecuentes sobre el equilibrador de carga local.

## ¿Qué productos de equilibrio de carga ofrece IBM?
Para obtener una comparación detallada de las ofertas de equilibrio de carga en IBM Cloud, consulte este [tema ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://dev-console.bluemix.net/docs/infrastructure/loadbalancer-service/explore-load-balancers.html#explore-load-balancers){: new_window}.

## ¿Cuál es la diferencia entre un equilibrador de carga compartido y dedicado?

Hay dos tipos de equilibradores de carga: compartidos y dedicados. Con un equilibrador de carga compartido, diferentes clientes comparten el mismo dispositivo físico, y se limitan a un número específico de conexiones en función de lo que se ha pedido. Los equilibradores de carga dedicados los utiliza un solo cliente y sus conexiones se limitan solo mediante las especificaciones del dispositivo.

## ¿Qué es un servicio?
Los servicios están configurados dentro de un grupo de servicios y representan los servidores reales a los que el equilibrador de carga equilibrará tráfico. Constan de una IP de destino, de un puerto de destino, de comprobación de estado y de ponderación.

## ¿Qué es un grupo de servicios?
Un grupo de servicios es el medio mediante el cual puede configurar la forma en que los clientes se conectan a su entorno a través del equilibrador de carga. Un grupo de servicios consta de un protocolo, un método de equilibrio de carga, un puerto virtual (que es el puerto al que se conectarán los clientes), una asignación de conexión (porcentaje), y los servicios asociados con el grupo.

## ¿Por qué obtengo errores 502 Gateway al utilizar la descarga SSL?

Suele estar causado por el puerto saliente del equilibrador de carga, que está establecido en el puerto 443.  Si el equilibrio de carga tiene habilitado tráfico saliente a su servidor, necesitará estar establecido en el puerto no SSL del servidor.  Este es normalmente el puerto 80 para HTTP.

## ¿Puedo tener varios certificados SSL en un equilibrador de carga único?

Esto es posible en determinadas configuraciones.  La regla general es un certificado SSL por IP Virtual (VIP). Un equilibrador de carga local solo admite un único VIP, pero esto puede incrementarse en nuestros equilibradores de carga dedicados y empresariales.

## ¿Qué es un puerto virtual?

Un puerto virtual en un equilibrador de carga de IBM Cloud es simplemente el puerto en el que desea ejecutar el servicio. Un ejemplo sería el puerto 80 para HTTP.

## ¿Qué método de equilibrio de carga se utiliza para los equilibradores de carga local y dedicado?

Nuestros equilibradores de carga se basan en proxy.

## ¿Qué servicios pueden ser de carga equilibrada?

Los más comunes son puertos como HTTP (80), HTTPS (443), FTP (21), DNS (53), POP3 (110) y SMTP (25). Sin embargo, cualquier servicio puede ser de carga equilibrada.

## ¿Puedo añadir descarga SSL a un equilibrador de carga existente?

Esto no se admite actualmente. Tendrá que realizarse un nuevo pedido para un equilibrador de carga con descarga SSL.

## ¿Cuánto se tarda en instalar un equilibrador de carga?

Los equilibradores de carga deberían estar instalados y disponibles para configurarse cinco minutos después de su compra.

## ¿Cómo puedo degradar mi equilibrador de carga local?

Esta opción solo está disponible al abrir una incidencia.

## ¿Qué métodos de equilibrio están disponibles con un equilibrador de carga?

IBM Cloud ofrece varios métodos de equilibrio, incluidos los únicos y los híbridos.  Consulte [Métodos de equilibrio de carga](load_balancing_methods.html) para obtener más información sobre cada método de equilibrio de carga que se ofrece actualmente.

## ¿Es posible equilibrar la carga de tráfico cifrado SSL con la retención de sesión?

Es posible, pero solo con un método de equilibrio persistente. Otros métodos no están soportados, puesto que el tráfico está cifrado.

