---
copyright:
  years: 1994, 2019
lastupdated: "2019-06-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Importando um certificado SSL
{: #importing-an-ssl-certificate}

Depois que um Certificado SSL é emitido para um website, ele pode ser importado para o portal do cliente da infraestrutura do {{site.data.keyword.cloud}}. Ao importar Certificados SSL para o portal do cliente, eles podem ser aplicados a produtos e serviços que possam requerê-los, como a Transferência SSL do Balanceador de Carga. Por padrão, Certificados SSL emitidos pelo {{site.data.keyword.cloud_notm}} não são importados para a lista, uma vez que devem ser manipulados apenas pelo destinatário. Portanto, qualquer Certificado SSL a ser usado com um produto ou serviço {{site.data.keyword.cloud_notm}} deve ser importado manualmente por um usuário autorizado na conta.

Execute o procedimento a seguir para importar um Certificado SSL para o portal do cliente.

1. Em seu navegador, abra o [portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} e faça login na sua conta.
2. Na navegação do portal do cliente, selecione **Segurança > SSL > Certificados**.
3. Clique no link **Importar certificado SSL** no lado superior direito da página **SSL Certificates**.
2. Insira os Detalhes do certificado SSL. 

	**Nota:** os detalhes inseridos na caixa pop-up Importar certificado
SSL devem ser inseridos exatamente como fornecidos pela autoridade de certificação,
incluindo espaçamento e quebras de linha. Se eles não forem inseridos exatamente como fornecidos, um erro ocorrerá. Preencha os campos conforme a seguir:
  - **Certificado:** detalhes do certificado, fornecidos pela autoridade de certificação. Geralmente é um bloco alfanumérico de texto.
  - **Chave privada:** detalhes da chave privada, fornecidos pela autoridade de certificação. Geralmente é um bloco alfanumérico de texto.
  - **Certificado intermediário:** detalhes do certificado intermediário, fornecidos pela autoridade de certificação. Os certificados intermediários não são obrigatórios. No entanto, se as informações estiverem disponíveis para o certificado SSL, elas deverão ser inseridas.
  - **Solicitação de assinatura de certificado:**
detalhes da solicitação de assinatura de certificado (CSR), fornecidos pela autoridade
de certificação. Os detalhes da CSR não são obrigatórios, mas deverão ser fornecidos se
fizerem parte do certificado. Não mude a CSR de maneira alguma. Uma chave pública pode ser incluída no CSR e não deve ser substituída pela Chave Privada.
  - **Notas:** quaisquer notas sobre o certificado SSL que possam ser úteis para outros usuários.
4. Clique em **Importar** para importar o certificado SSL. Clique em **Cancelar** para cancelar a ação.

Depois que o Certificado SSL for importado para o portal do cliente, será armazenado na tela Certificados SSL até ser excluído manualmente. Para todos os produtos ou
serviços que requerem detalhes do certificado SSL, o novo certificado SSL aparecerá na
lista de certificados disponíveis para uso ao interagir com o recurso SSL do produto
ou serviço desejado. É possível atualizar o certificado ou fazer download de forma segura
de seus detalhes a qualquer momento.
