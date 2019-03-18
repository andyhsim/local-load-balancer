---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurando pesos para o Load Balancer
{; #configuring-weights-for-the-load-balancer}

Pesos são um sistema de designação de valores numéricos para os servidores que você deseja que recebam mais tráfego. Um número maior representa uma prioridade mais alta, contato que o servidor esteja on-line de acordo com as verificações de funcionamento.  

Por exemplo, se _server1_ tiver um peso de 80 e _server2_ tiver um peso de 20, então, para cada 10 conexões que passarem, _server1_ será alocado a 8 e _server2_ obterá 2. Se _server1_ ficar off-line ou for removido do conjunto, todas as conexões irão para _server2_.

É possível configurar pesos para um serviço específico quando você
[inclui o serviço em um grupo de
serviços](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) ou [editando o serviço](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service)
após ele ter sido criado.

Quando sua configuração tiver sido salva, as mudanças entrarão em vigor imediatamente. É
possível monitorar as conexões do serviço nos detalhes do serviço.
