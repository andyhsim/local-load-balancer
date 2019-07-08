---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:note: .note}

# Limitações conhecidas com o Local Load Balancer
{: #known-limitations-with-local-load-balancer}

Devido à natureza de um balanceador de carga proxy, o IP de origem da solicitação do cliente vem do IP do balanceador de carga. Isso afetará os programas de log de estatística e outros aplicativos que examinam o IP de origem para obter informações do cliente. O IBM© Cloud fornece uma solução para reescrever corretamente as entradas de log para Apache (todas as plataformas) e
IIS (Windows).

Para acessar as instruções e os plug-ins adicionais necessários, deve-se primeiro estar conectado à VPN do IBM Cloud. Depois de se conectar, visite a [página Downloads![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://downloads.softlayer.local/loadbalancer/){: new_window} para localizar os plug-ins e as instruções para o {{site.data.keyword.loadbalancer_short}}.

Deve-se estar conectado à VPN do IBM Cloud para acessar o link de download.
{: note}
