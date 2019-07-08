---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud, faq, support

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
{:faq: data-hd-content-type='faq'}

# Perguntas frequentes sobre a migração do IBM Cloud Load Balancer
{: #migration-faq}

As perguntas mais frequentes a seguir se aplicam ao processo de migração do IBM Local Load Balancer.

## Qual é o anúncio e a data de vigência para o término de marketing (EOM) do Local Load Balancer?
{: faq}

A data do anúncio do EOM é 1º de março de 2019 e a data de vigência é 1º de junho de 2019. Nenhuma nova venda pode ocorrer após essa data.

## O suporte estará disponível após o EOM?
{: faq}

Sim, o suporte estará disponível para os clientes existentes do Local Load Balancer.

## Como posso começar a usar o IBM Cloud Load Balancer?
{: faq}

Recomendamos que você comece lendo a [documentação do IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-getting-started).

## Existirá um caminho de migração do serviço Local Load Balancer para o IBM Cloud Load Balancer?
{: faq}

Não existirá nenhum caminho de migração automatizado. No entanto, será possível solicitar que seu serviço Local Load Balancer seja desativado e, em seguida, solicitar o serviço Cloud Load Balancer no IBM Cloud Console.

## Qual é a diferença entre o Local Load Balancer e o Cloud Load Balancer?
{: faq}

O Local Load Balancer é um serviço de balanceamento de carga local baseado em hardware e o IBM Cloud Load Balancer é um serviço nativo da nuvem que oferece uma solução de balanceamento de carga de dimensionamento automático com custo reduzido e suporte para redes públicas e privadas.

## O Cloud Load Balancer usa a mesma terminologia que o Local Load Balancer?
{: faq}

Em alguns casos, isso não acontece. A tabela a seguir compara termos-chave no Local Load Balancer com seus termos correspondentes e diferentes no Cloud Load Balancer.

| Termo do Local Load Balancer  | Termo do Cloud Load Balancer |
| ------------- | ------------- |
| Grupos de Serviços | Protocols |
| Serviço | Instâncias do Servidor |
| VIP | FQDN |

## Ainda terei um endereço IP fixo e único para meu balanceador de carga quando migrar para o Cloud Load Balancer?
{: faq}

Os IPs para o IBM Cloud Load Balancer não são fixos. O Cloud Load Balancer designa instâncias de balanceador de carga de um conjunto, que exige sempre um nome de domínio completo (FQDN). Como resultado, o endereço IP individual de um Cloud Load Balancer pode mudar.

## O IBM Cloud Load Balancer está disponível para as soluções de VSI público/privado e bare metal?
{: faq}

Sim, o Cloud Load Balancer está disponível para VSIs públicos e privados, bem como para bare metal.

## O IBM Cloud Load Balancer é compatível com o GDPR?
{: faq}

Sim, a oferta do Cloud Load Balancer é compatível com o GDPR.

## Depois de iniciar a migração, quanto tempo de inatividade ou interrupção de tráfego posso esperar de meu sistema?

Nenhum tempo de inatividade ou interrupção de tráfego ocorrerá como resultado da migração do balanceador de carga. O único tempo de inatividade ou interrupção de tráfego que pode ser encontrado ocorre ao atualizar sua configuração do Local Load Balancer para o novo FQDN do IBM Cloud Load Balancer.

## Suas instruções dizem que devo solicitar o IBM Cloud Load Balancer antes de cancelar o Local Load Balancer. Haverá algum impacto no meu sistema ou carga de trabalho enquanto configuro os dois dispositivos?

Não, o Cloud Load Balancer e o Local Load Balancer são duas ofertas separadas que funcionam de forma independente.

## Eu costumava escolher uma opção de "conexões por segundo" com meu Local Load Balancer. Também preciso configurar isso no Cloud Load Balancer?

Não. O IBM Cloud Load Balancer ajusta automaticamente sua capacidade de carga. É possível ler mais sobre isso no tópico [Escala horizontal do Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-performing-ibm-cloud-load-balancer-basics#horizontal-scaling).

## Quais protocolos posso escolher ao usar o Cloud Load Balancer?

É possível escolher os protocolos HTTP, HTTPS e TCP. Também oferecemos o suporte de Camada 7. Consulte [Visão geral de recursos](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-about-ibm-cloud-load-balancer#overview-of-features) para obter mais informações.

## Preciso de um tipo específico de cifra. O Cloud Load Balancer suporta isso?

O IBM Cloud Load Balancer suporta o TLS versão 1.2 com a transferência SSL. É possível localizar mais informações sobre as cifras SSL suportadas em [Conjuntos de cifras SSL do Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-ssl-offload-with-ibm-cloud-load-balancer#ssl-cipher-suites)
