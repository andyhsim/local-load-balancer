---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Editar um serviço 

Depois que um serviço foi incluído no grupo de serviços de um balanceador de carga,
ele pode ser editado a qualquer momento. Todas as configurações básicas de um serviço são
elegíveis para edições e notas adicionais também podem ser incluídas usando o recurso de
edição. 

Siga as etapas abaixo para editar um serviço.

1. Na página [Detalhes do Local Load
Balancer](view-all-load-balancers.html), localize o serviço que você gostaria de editar expandindo a seta à
esquerda.
2. Edite os campos a seguir, conforme desejado:
  - **IP de destino:** o endereço IP do servidor de destino.
  - **Porta de destino:** o número da porta a ser usada para rotear o tráfego para o servidor de destino.
  - **Verificação de funcionamento:** o método de verificação de funcionamento preferencial dessas opções.
      - **Padrão:** a configuração padrão é Ping.
      - **HTTP:** verifica se a porta 80 para o endereço IP listado responde com código HTTP 200 (Ok).
      - **HTTP-CUSTOM:** muito semelhante ao HTTP regular, exceto que você designa o tipo de conexão, o local de sua verificação de funcionamento e a resposta que está sendo prevista. Esta é uma opção avançada.
      - **Ping:** um teste simples de ping sobre ICMP.
      - **TCP:** muito semelhante a um teste de ping, mas explicitamente sobre TCP.  Esta opção deverá ser usada se você tiver conexões ICMP bloqueadas.
  - **Peso:** a prioridade numérica para o Serviço. Pesos são um sistema de designação de valores numéricos a quais servidores você deseja receber mais tráfego. Um número maior representa uma prioridade mais alta, contato que o servidor esteja on-line de acordo com as verificações de funcionamento. Por exemplo, se _server1_ tiver um peso de 80 e _server2_ tiver um peso de 20, então, para cada 10 conexões que passarem, _server1_ será alocado a 8 e _server2_ obterá 2. Se _server1_ ficar off-line ou for removido do conjunto, todas as conexões irão para _server2_.
  - **Notas:** campo de texto em formato livre.
  - **Ativado:** marque ou desmarque essa caixa de seleção para ativar ou desativar o serviço.
3. Clique no botão **Salvar configuração** botão para atualizar o serviço. Clique em **Cancelar** para cancelar a ação.

Depois de editar um serviço, as edições aparecerão na linha que contém o serviço na
seção Serviço. Edições adicionais podem ser feitas a qualquer momento repetindo as etapas
acima.
