---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Editar um grupo de serviços

Depois de incluir um grupo de serviços em um
{{site.data.keyword.loadbalancer_short}}, suas configurações básicas (incluindo
método de balanceamento e porta virtual), alocação de conexão e notas podem ser editadas. As
edições em cada grupo de serviços são imediatamente visíveis e edições adicionais podem
ser feitas a qualquer momento. 

Se for necessário mudar o tipo de um grupo de serviços, o grupo deverá ser excluído
e um novo deverá ser incluído para refletir o tipo de grupo desejado. 

Siga as etapas abaixo para editar um grupo de serviços existente para um
{{site.data.keyword.loadbalancer_short}}.

1. Na página [Detalhes do Local Load
Balancer](view-all-load-balancers.html), expanda os detalhes do Grupo de serviços clicando no ícone de expansão
no lado esquerdo da linha correspondente ao Grupo de serviços que você gostaria de
editar.
2. Atualize as configurações do grupo de serviços:
  - **Método:** selecione um [Método de balanceamento](load_balancing_methods.html) na lista suspensa.
  - **Porta virtual:** o número da porta que será usada para o grupo de serviços. Consulte as [Perguntas mais frequentes de portas de serviço comum](load-balancing-faqs-2.html#what-services-can-be-load-balanced-) para obter mais informações. 

  	**Nota:** cada Grupo de serviços deve ser designado a uma porta exclusiva. Se uma porta exclusiva não for designada, um erro aparecerá na parte superior da página e o Grupo de serviços poderá não ser incluído até que um Portal Virtual exclusivo seja designado.
  - **Alocação:** a alocação para o grupo de serviços.
  - **Notas:** texto em formato livre para identificar o grupo de serviços.
3. Clique no botão **Salvar configuração** para atualizar o grupo de serviços. Clique no botão **Cancelar** para cancelar a ação.

As edições no grupo de serviços serão refletidas na tela Detalhes do grupo
associado. Se uma mudança foi feita na alocação de conexão, edições adicionais para
outros grupos de serviço poderão ser necessárias. Se uma mudança foi feita no método de
balanceamento, serviços associados ao grupo poderão requerer edições adicionais para
alinhar com o novo método de balanceamento. Edições adicionais no grupo de serviços podem
ser feitas a qualquer momento repetindo as etapas acima.
