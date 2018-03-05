---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Excluir um grupo de serviços

Ao excluir um grupo de serviços, todos os serviços associados ao grupo também serão
excluídos. Siga as etapas abaixo para excluir um grupo de serviços para um
{{site.data.keyword.loadbalancer_short}}.

1. Na página [Detalhes do Local Load
Balancer](view-all-load-balancers.html), identifique a linha do grupo de serviços que você gostaria de
excluir e clique em **Ações > Remover grupo**.
2. Clique em **Salvar configuração**.

Depois de excluir um grupo de serviços, ele será removido do
{{site.data.keyword.loadbalancer_short}}. Todos os serviços associados também
serão excluídos e a porta virtual associada ao grupo de serviços estará disponível, caso
seja necessária para outro grupo de serviços no futuro. Na exclusão, a porcentagem
de alocação de conexão para os grupos de serviço restantes deve ser mudada manualmente
para quaisquer grupos restantes.
