---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Excluir um serviço 

Depois que um serviço tiver sido incluído em um Grupo de serviços para um
{{site.data.keyword.loadbalancer_short}}, ele poderá ser excluído a qualquer
momento. A exclusão um serviço de um grupo de serviços evita que o serviço seja utilizado
pelo {{site.data.keyword.loadbalancer_short}} a menos que seja manualmente
incluído de volta em um grupo de serviços. 

Como alternativa, um serviço pode ser desativado, o que o manterá associado
ao grupo e ao mesmo tempo o tornará indisponível para os esforços de balanceamento. Para
manter o serviço associado ao grupo de serviços do
{{site.data.keyword.loadbalancer_short}},
[edite o serviço](edit-service-load-balancer.html) e
desmarque a caixa de seleção **Ativado**. 

Siga as etapas abaixo para excluir o serviço do
{{site.data.keyword.loadbalancer_short}}.

1. Na página [Detalhes do Local Load
Balancer](view-all-load-balancers.html), localize o serviço que você gostaria de excluir e expanda a seta no lado
esquerdo.
2. Clique no 'x' vermelho no final da linha do serviço.
3. Clique em **Salvar configuração** na parte inferior da
página que as configurações sejam atualizadas.

Depois de excluir o serviço, a configuração será salva e as mudanças entrarão em
vigor imediatamente. Se o serviço excluído for o único associado a um grupo de serviços,
o grupo não será capaz de executar qualquer atividade de balanceamento de carga até que
um novo serviço seja incluído.
