---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud

subcollection: local-load-balancer

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Migrando um Local Load Balancer para o IBM Cloud Load Balancer

É possível migrar seu Local Load Balancer para um IBM© Cloud Load Balancer executando o seguinte procedimento.

## Etapa 1: solicitar um Cloud Load Balancer
{: #step-1-order-a-cloud-load-balancer}

Para solicitar um serviço IBM Cloud Load Balancer, selecione **IBM Cloud Load Balancer** no [Catálogo do IBM Cloud  ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")]( https://cloud.ibm.com/catalog/infrastructure/load-balancer-group){:new_window}. Clique em **Criar** e, em seguida, execute o seguinte procedimento:

1. Defina seus parâmetros básicos de serviço, como o nome e a descrição.
2. Selecione seu data center.
3. Selecione um tipo de balanceador de carga **Público**.
4. Selecione a sub-rede na qual você gostaria implementar seu balanceador de carga.

  A instância do serviço de balanceador de carga terá uma de suas interfaces de rede nesta sub-rede. Assegure-se de que seus servidores de aplicativos estejam nessa sub-rede ou sejam acessíveis nessa sub-rede. Se necessário, ative o VLAN Spanning.
  {: note}

5. Crie protocolos e portas de aplicativos de front-end e back-end com a mesma configuração que os grupos de serviços que você está usando atualmente em seu Local Load Balancer. Para obter mais informações sobre essa configuração, consulte [Configurando os parâmetros do IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configuring-ibm-cloud-load-balancer-parameters).
6. Para ativar a transferência SSL, defina os protocolos de front-end, como HTTPS, e os protocolos de back-end, como HTTP. Em seguida, selecione o mesmo Certificado SSL como seu Local Load Balancer na caixa suspensa Certificado. O Certificado usado com seu Local Load Balancer está na lista suspensa porque todos os certificados SSL existentes são gerenciados por meio do [IBM Cloud Certificate Store  ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/classic/security/sslcerts){:new_window}.
7. Ajuste os parâmetros de verificação de funcionamento, se desejado, caso contrário, use as configurações padrão. Para obter mais informações sobre os parâmetros de verificação de funcionamento, consulte [Parâmetros do IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configure-health-checks).
8. Clique em **Conectar servidor** para incluir quaisquer instâncias do servidor usadas para o seu serviço Local Load Balancer.
9. Revise a página, confirme o Contrato de Serviço e clique em **Criar**.

A lista Balanceador de carga é exibida, mostrando todas as suas instâncias de serviço.

Seu balanceador de carga recém-criado pode não ser exibido imediatamente nessa lista. Após alguns minutos, o novo balanceador de carga será exibido em cinza, indicando que seu status é `Offline`. Após alguns minutos, o novo balanceador de carga será exibido em verde, indicando que está `Online`. Pode ser necessário atualizar sua tela para ver essas mudanças.
{: note}

Clicar no nome do serviço nessa página o levará para a página de visão geral do serviço. É possível navegar para as guias **Protocolos**, **Verificações de funcionamento** e **Instâncias do servidor** para editar sua configuração posteriormente.

## Etapa 2: verificar se seu Cloud Load Balancer está funcionando conforme esperado
{: #step-2-verify-your-cloud-load-balancer-is-working-as-expected}

Observe que, neste momento, há dois balanceadores de carga trabalhando ao mesmo tempo: o seu Local Load Balancer anterior e o novo IBM Cloud Load Balancer.
{: important}

Teste o novo IBM Cloud Load Balancer usando o domínio listado na página de status acima, certificando-se de que ele funcione da mesma maneira que o VIP de seu Local Load Balancer.

Em seguida, atualize todos os locais que usam o VIP do Local Load Balancer para que usem o novo domínio do Cloud Load Balancer.

Essa configuração do novo Cloud Load Balancer será a única ocasião na qual um tempo de inatividade ou uma interrupção no tráfego do processo de migração possa ocorrer.
{: note}

## Etapa 3: cancelar seu Local Load Balancer anterior
{: #step-3-cancel-your-local-load-balancer}

Após substituir todos os VIPs do Local Load Balancer pelo domínio do seu novo IBM Cloud Load Balancer e verificar se a funcionalidade está funcionando conforme o esperado, será possível cancelar com segurança seu serviço Local Load Balancer. Para isso, execute as seguintes etapas:

1. Acesse a [página de lista do Local Load Balancer](https://cloud.ibm.com/classic/network/loadbalancing/local).
2. Localize o Balanceador de Carga que deseja excluir e expanda a seta próxima a ele.
3. Clique no **X** vermelho no final da linha para cancelar o Balanceador de Carga.
