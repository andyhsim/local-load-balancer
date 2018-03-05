---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-07"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Limitações conhecidas

Devido à natureza de um balanceador de carga proxy, o IP de origem da solicitação do cliente vem do IP do balanceador de carga. Isso afetará os programas de log de estatística e outros aplicativos que examinam o IP de origem para obter informações do cliente. O IBM Cloud fornece uma solução para reescrever corretamente as entradas de log para Apache (todas as plataformas) e IIS (Windows).

Para acessar as instruções e plug-ins adicionais necessários, deve-se primeiro estar conectado à [VPN do IBM Cloud](https://console.bluemix.net/docs/infrastructure/iaas-vpn/getting-started.html){: new_window}. Uma vez conectado, visite a [página Downloads](http://downloads.softlayer.local/loadbalancer/){: new_window} para localizar os plug-ins e as instruções para o {{site.data.keyword.loadbalancer_short}}.
