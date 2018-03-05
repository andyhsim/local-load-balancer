---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-02"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Perguntas Frequentes
Este tópico contém respostas às perguntas mais frequentes sobre o Local Load Balancer.

## Quais produtos de balanceamento de carga a IBM oferece?
Para obter uma comparação detalhada das ofertas de balanceamento de carga no IBM Cloud, consulte este
[tópico
![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://dev-console.bluemix.net/docs/infrastructure/loadbalancer-service/explore-load-balancers.html#explore-load-balancers){: new_window}.

## Qual é a diferença entre um balanceador de carga compartilhado e dedicado?

Há dois tipos de balanceadores de carga, compartilhado e dedicado. Com um
balanceador de carga compartilhado, clientes diferentes compartilham o mesmo dispositivo
físico e estão limitados a um número específico de conexões dependendo do que foi pedido. Os
balanceadores de carga dedicados são usados por um cliente apenas e suas conexões são
limitadas apenas pelas especificações do dispositivo.

## O que é um serviço?
Serviços são configurados dentro de um grupo de serviços e representam os
servidores reais para os quais o balanceador de carga estará balanceando o tráfego. Eles
consistem em um IP de destino, porta de destino, verificação de funcionamento e peso.

## O que é um grupo de serviços?
Um grupo de serviços é o meio pelo qual você configura a maneira como os clientes se conectam ao seu ambiente por meio do balanceador de carga. Um grupo de serviços consiste em um protocolo, método de balanceamento de carga, porta virtual (que é a porta de conexão dos clientes), alocação de conexão (porcentagem) e os serviços associados ao grupo.

## Por que estou recebendo erros 502 Gateway ao usar a transferência SSL?

Isso normalmente é causado pela porta de saída do balanceador de carga sendo
configurada como porta 443. Se o balanceamento de carga estiver ativado, o tráfego de
saída, para seu servidor, precisará ser configurado para a porta não SSL do servidor. Esta
geralmente é a porta 80 para HTTP.

## Posso ter diversos certificados SSL em um único balanceador de carga?

Isso é possível em determinadas configurações. A regra geral é um certificado SSL
por IP virtual (VIP). Um balanceador de carga local suporta apenas um único VIP, mas isso
pode ser aumentado em nossos balanceadores de carga dedicados e corporativos.

## O que é uma porta virtual?

Uma porta virtual em um balanceador de carga do IBM Cloud é simplesmente a porta na
qual você deseja executar o serviço. Um exemplo seria a porta 80 para HTTP.

## Qual método de balanceamento de carga é usado para balanceadores de carga local e dedicado?

Nossos balanceadores de carga são baseados em proxy.

## Quais serviços podem ter carga balanceada?

Os mais comuns são as portas, como HTTP (80), HTTPS (443), FTP (21), DNS (53), POP3
(110) e SMTP (25). No entanto, qualquer serviço pode ter carga balanceada.

## Posso incluir transferência SSL em um balanceador de carga existente?

Isso não é suportado atualmente. Uma nova ordem para um balanceador de carga com
transferência SSL precisará ser feita.

## Quanto tempo leva para instalar um balanceador de carga?

Os balanceadores de carga devem ser instalados e estar disponíveis para sua
configuração aproximadamente cinco minutos após a compra.

## Como posso fazer downgrade do meu balanceador de carga local?

Essa opção está disponível somente abrindo um chamado.

## Quais métodos de balanceamento estão disponíveis com um balanceador de carga?

O IBM Cloud oferece vários métodos de balanceamento, incluindo únicos e híbridos. Consulte
[Métodos de balanceamento de carga](load_balancing_methods.html) para
obter mais informações sobre cada método de balanceamento de carga que atualmente
oferecemos.

## É possível balancear a carga do tráfego SSL criptografado com permanência de sessão?

Isso é possível, mas apenas com um método de balanceamento persistente. Outros
métodos não são suportados porque o tráfego é criptografado.

