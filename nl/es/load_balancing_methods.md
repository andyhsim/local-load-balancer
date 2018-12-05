---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Métodos de equilibrio de carga

| Método|Descripción|
|:---|:---|
|IP de hash coherente|<ul><li>Correlaciona solicitudes de clientes a servidores reales troceando la IP de origen de la solicitud.</li><li>Las relaciones de cliente / servidor se mantienen entre puertos.</li></ul>|
|Insertar cookie|<ul><li>Inserta una cookie de seguimiento en la solicitud.<span style="mso-spacerun:yes">&nbsp; </span>Los datos de sesión contenidos dentro de la cookie se utilizan con solicitudes subsiguientes para enviar tráfico de nuevo al mismo servidor real.</li><li>La persistencia está codificada en una base por sesión.</li><li>La cookie caduca una vez que se cierre el navegador del cliente.</li><li>Requiere que el cliente acepte cookies para que sea efectivo.</li></ul>|
|Conexiones mínimas|<ul><li>El servidor real con el menor número de conexiones activas tendrá prioridad.</li><li>El algoritmo requiere una diferencia de 10 conexiones, lo que puede sesgar los resultados para los clientes</li></ul>|
|IP persistente|<ul><li>Enlaza la IP de origen del solicitante al servidor real que procesa la solicitud mediante un troceado de los 4 octetos de la dirección IP de la solicitud.</li><li>Persiste durante 60 minutos</li></ul>|
|Round Robin|<ul><li>Cada nueva solicitud se asigna al siguiente servidor real de la rotación.</li><li>La distribución equilibrada se produce en ejemplos grandes, aunque los ejemplos pequeños pueden mostrar un equilibrio desproporcionado.</li></ul>|
|Respuesta más corta|<ul><li>El servidor con el tiempo de respuesta más corto recibirá la solicitud.</li><li>A medida que aumenta la carga y el tiempo de respuesta, los servidores más lentos comenzarán a alinear menos solicitudes.</li></ul>|
|Round Robin con IP persistente|<ul><li>Cada nueva solicitud se asigna al siguiente servidor real de la rotación.</li><li>La dirección IP del solicitante está vinculada al servidor real, lo que da lugar a solicitudes subsiguientes de la IP que se asignarán al mismo servidor real.</li></ul>|
|Round Robin con Insertar cookie|<ul><li>Cada nueva solicitud se asigna al siguiente servidor real de la rotación.</li><li>El equilibrador de carga inserta una cookie en la solicitud y utilizará la información de la sesión de la cookie para dirigir el tráfico al mismo servidor real para solicitudes posteriores.</li></ul>|
|Conexiones mínimas con IP persistente|<ul><li>Cada nueva solicitud se asigna al servidor real con el menor número de conexiones activas en este momento.</li><li>La dirección IP del solicitante está vinculada al servidor real, lo que da lugar a solicitudes subsiguientes de la IP que se asignarán al mismo servidor real.</li></ul>|
|Conexiones mínimas con Insertar cookie|<ul><li>Cada nueva solicitud se asigna al servidor real con el menor número de conexiones activas en este momento.</li><li>El equilibrador de carga inserta una cookie en la solicitud y utilizará la información de la sesión de la cookie para dirigir el tráfico al mismo servidor real para solicitudes posteriores.</li></ul>|
|Respuesta más corta con IP persistente|<ul><li>Cada nueva solicitud se asigna al servidor real con el menor tiempo de respuesta.</li><li>La dirección IP del solicitante está vinculada al servidor real, lo que da lugar a solicitudes subsiguientes de la IP que se asignarán al mismo servidor real.</li></ul>|
|Respuesta más corta con Insertar cookie|<ul><li>Cada nueva solicitud se asigna al servidor real con el menor tiempo de respuesta.</li><li>El equilibrador de carga inserta una cookie en la solicitud y utilizará la información de la sesión de la cookie para dirigir el tráfico al mismo servidor real para solicitudes posteriores.</li></ul>|
