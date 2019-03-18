---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Importando um certificado SSL
{: #importing-an-ssl-certificate}

Após a emissão de um certificado SSL para um website, ele pode ser importado no
Portal do cliente. Importando SSL Certificates no Portal do cliente, os certificados
podem ser aplicados a produtos e serviços que possam exigi-los, como transferência SSL de
um balanceador de carga. Por padrão, os certificados SSL emitidos pelo IBM© Cloud não são importados para a lista,
pois eles devem ser manipulados apenas pelo destinatário. Portanto,
qualquer certificado SSL para uso com um produto ou serviço IBM Cloud deve ser
importado manualmente por um usuário autorizado na conta.

Execute o procedimento a seguir para importar um certificado SSL no Portal do
cliente.

1. Em seu navegador, abra [Portal do Cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} e efetue login em sua conta.
2. Na navegação do Portal do cliente, selecione **Segurança > SSL > Certificados**.
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

Após a importação do SSL Certificate para o Portal do cliente, ele será armazenado
na tela SSL Certificates até que seja excluído manualmente. Para todos os produtos ou
serviços que requerem detalhes do certificado SSL, o novo certificado SSL aparecerá na
lista de certificados disponíveis para uso ao interagir com o recurso SSL do produto
ou serviço desejado. É possível atualizar o certificado ou fazer download de forma segura
de seus detalhes a qualquer momento.
