---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar a transferência SSL em um balanceador de carga

Os Load Balancers têm a capacidade de fornecer transferência SSL, que pode
reduzir grandemente a carga nos sistemas que atualmente executam a função. Para utilizar
a transferência SSL, deve ser comprado um
{{site.data.keyword.loadbalancer_short}} que ofereça a capacidade. Os
balanceadores de carga que oferecem capacidade de SSL trazem a observação "com
transferência SSL" na caixa de diálogo **Pedir Local Load Balancer**. Depois
que o {{site.data.keyword.loadbalancer_short}} ativado para transferência SSL
tiver sido provisionado, ele deverá ser configurado. Siga as etapas abaixo para
configurar a transferência SSL em um {{site.data.keyword.loadbalancer_short}}.

1. Na página [Detalhes do Local Load
Balancer](view-all-load-balancers.html), clique em Ações > Configurar SSL no menu
suspenso para o balanceador de carga.
2. Selecione o Certificado SSL desejado na caixa suspensa
**Certificado**. Observe o seguinte:
  - IPs virtuais (VIPs) do {{site.data.keyword.loadbalancer_short}} não
dedicados são limitados a um tamanho máximo de bit de certificado SSL de 2048.
  - Pelo menos um certificado SSL deve ser armazenado no Portal do cliente para
concluir com êxito esta etapa. Consulte [Importar um certificado SSL](import-ssl-cert.html).
3. Marque a caixa de seleção **Ativado**.
4. Selecione as cifras que você deseja suportar.
5. Clique no botão **Atualizar**.

Depois de ativar a transferência SSL em um
{{site.data.keyword.loadbalancer_short}}, o estado do SSL muda de
**desativado** para **ativo**. A carga transportada
por sistemas que já manipulavam conexões SSL geralmente diminuirá após a ativação da
transferência SSL. A qualquer momento, o status de transferência SSL pode ser mudado. Retorne
à guia Transferir SSL e desmarque a caixa de seleção para desativar a
transferência SSL para o {{site.data.keyword.loadbalancer_short}}.
