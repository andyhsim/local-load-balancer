---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Incluir um serviço em um grupo de serviços

Após a inclusão de um grupo de serviços em um
{{site.data.keyword.loadbalancer_short}}, serviços podem ser incluídos para
iniciar o processo de balanceamento. Diversos serviços podem ser incluídos em um grupo de
serviços e podem ser ponderados para permitir a priorização sobre como cada dispositivo
deve receber a carga de trabalho em um determinado momento. Siga as etapas abaixo para
incluir um novo serviço em um grupo de serviços para um
{{site.data.keyword.loadbalancer_short}}.

1. Na página [Detalhes do Local Load
Balancer](view-all-load-balancers.html), clique em Ações > Incluir serviço no menu
suspenso, na linha correspondente ao grupo de serviços no qual você gostaria de incluir
um serviço. Como alternativa, expanda os Detalhes do grupo clicando no ícone de expansão
no lado esquerdo da linha e clique no botão **Incluir serviço**. Uma
nova seção Serviço será incluída na parte inferior da seção Detalhes do grupo de serviços.
2. Digite os parâmetros de serviço:
  - **IP de destino:** o endereço IP do servidor de destino.
  - **Porta de destino:** o número da porta a ser utilizada para rotear o tráfego para o servidor de destino.
  - **Verificação de funcionamento:** o método de verificação de funcionamento preferencial dessas opções.

     - **Padrão:** a configuração padrão é Ping.
     - **HTTP:** verifica se a porta 80 para o endereço IP listado responde com código HTTP 200 (Ok).
     - **HTTP-CUSTOM:** muito semelhante ao HTTP regular, exceto que você designa o tipo de conexão, o local de sua verificação de funcionamento e a resposta que está sendo prevista. Esta é uma opção avançada.
     - **Ping:** um teste simples de ping sobre ICMP.
     - **TCP:** muito semelhante a um teste de ping, mas explicitamente sobre TCP. Esta opção deverá ser usada se você tiver conexões ICMP bloqueadas.
  - **Peso:** a prioridade numérica para o Serviço. Pesos são um sistema de designação de valores numéricos a quais servidores você deseja receber mais tráfego. Um número maior representa uma prioridade mais alta, contato que o servidor esteja on-line de acordo com as verificações de funcionamento. Por exemplo, se _server1_ tiver um peso de 80 e _server2_ tiver um peso de 20, então, para cada 10 conexões que passarem, _server1_ será alocado a 8 e _server2_ obterá 2. Se _server1_ ficar off-line ou for removido do conjunto, todas as conexões irão para _server2_.
  - **Notas:** campo para notas.
3. Marque a caixa de seleção **Ativado** para ativar o serviço.
4. Clique no botão **Salvar configuração** para incluir o serviço. Clique em **Cancelar** para cancelar a ação.

Depois de incluir um serviço em um grupo de serviços, ele aparecerá na grade de
serviços do grupo. Se tiver sido ativado, ele iniciará a assistência nos esforços de
balanceamento de carga com base no peso fornecido quando o serviço foi incluído. Se
estiver desativado, ele ainda aparecerá no Grupo de serviços, mas não ajudará no
balanceamento até que tenha sido ativado. Verificações de funcionamento serão executadas
no serviço em intervalos e seu status será refletido como ativo ou inativo, com
base no resultado da verificação de funcionamento. Os serviços podem ser editados ou
excluídos a qualquer momento e verificações de funcionamento customizadas de HTTP podem
ser incluídas em qualquer serviço existente pelo menu suspenso Ações.
