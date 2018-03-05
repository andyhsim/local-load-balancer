---
copyright:
  years: 1994, 2017 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Reconfigurar conexões para um grupo de serviços

Quando um grupo de serviços está ativo em um balanceador de carga, uma conexão pode
existir para cada serviço associado a esse grupo com base em como os clientes usam o serviço. Às
vezes, os clientes podem estar conectados a um ou mais serviços por um período de
tempo inadequado. Como as conexões são consideradas um recurso limitado, pode ser
necessário reconfigurar manualmente as conexões para um grupo de serviços para assegurar
que outros clientes tenham a oportunidade de utilizar o balanceador de carga. Siga as
etapas abaixo para reconfigurar as conexões de um balanceador de carga.

1. Na página [Detalhes do Local Load
Balancer](view-all-load-balancers.html), identifique a linha do grupo de serviços cujas conexões você gostaria de
reconfigurar e clique em **Ações > Reconfigurar conexões**.
2. Confirme a ação pressionando **Sim**. Escolha **Não** para cancelar a ação.

Após a solicitação para que todas as conexões ativas sejam reconfiguradas, o grupo
de serviços descartará as conexões ativas com cada serviço. Uma caixa de texto verde
aparecerá na parte superior da tela após as conexões terem sido reconfiguradas para
confirmar o sucesso da ação. Quando as conexões forem descartadas, os clientes poderão se
reconectar, conforme necessário. 

Você pode repetir as etapas acima para reconfigurar as conexões para o grupo de serviços a qualquer momento.
