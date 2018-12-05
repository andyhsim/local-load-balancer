---
copyright:
  years: 1994,2017,2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Incluir um grupo de serviços em um balanceador de carga

Depois que um {{site.data.keyword.loadbalancer_short}} foi incluído, um
novo Grupo de serviços pode ser incluído no
{{site.data.keyword.loadbalancer_short}} a qualquer momento. Grupos de serviço
estão disponíveis em uma variedade de Tipos de grupo e oferecem uma ampla matriz de
Métodos de balanceamento únicos ou híbridos. Ao incluir um novo Grupo de serviços, é
importante assegurar que a soma de todos os grupos de Alocações de conexão seja igual a
100%. Siga as etapas abaixo para incluir um novo Grupo de serviços em um
{{site.data.keyword.loadbalancer_short}}.

1. Na página [Detalhes do Local Load
Balancer](view-all-load-balancers.html), clique no botão Incluir grupo. Como alternativa,
você pode clicar em **Ações > Incluir grupo**. Uma nova seção Grupo de
serviços será incluída na parte inferior da página.
2. Selecione o Tipo de grupo desejado na lista suspensa
**Grupo** e selecione o Método de balanceamento desejado na lista
suspensa **Método**. Consulte
[Métodos de balanceamento de carga](load_balancing_methods.html) para
obter mais informações sobre cada método de balanceamento de carga.
3. Insira o número da porta que será usado para o grupo de serviços no campo
**Porta virtual**. Consulte as [Perguntas mais frequentes de portas de serviço comum](load-balancing-faqs-2.html#what-services-can-be-load-balanced-) para obter mais informações. 

	**Nota:** cada Grupo de serviços deve ser designado a uma porta exclusiva. Se uma porta exclusiva não for designada, um erro aparecerá na parte superior da página e o Grupo de serviços poderá não ser incluído até que um portal virtual exclusivo seja designado.
4. Insira uma alocação no campo **Alocação**.
5. Insira quaisquer notas na caixa de texto **Notas**, se desejado.
6. Clique no botão **Salvar configuração** para incluir o novo Grupo de serviços. Clique em **Cancelar** para cancelar a ação.

Depois de incluir um Grupo de serviços, ele poderá ser excluído ou editado a qualquer
momento. As conexões podem ser reconfiguradas para o grupo de serviços e novos
serviços podem ser incluídos no grupo. Para que um Grupo de serviços comece a balancear a
carga com base em suas Alocações de conexão designadas, um ou mais serviços devem
ser [incluídos](add-service-service-group.html) no Grupo de serviços.

## O que acontece em seguida

[Incluir um serviço no grupo de serviços](add-service-service-group.html).
