---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Métodos de balanceamento de carga

| Método|Descrição|
|:---|:---|
|IP de hash consistente|<ul><li>Mapeia as solicitações do cliente para servidores reais efetuando hashing de IPs de origem da solicitação.</li><li>Os relacionamentos cliente/servidor são mantidos entre as portas.</li></ul>|
|Inserir cookie|<ul><li>Insere um cookie de rastreamento na solicitação.<span style="mso-spacerun:yes">&nbsp; </span>Os dados da sessão contidos no cookie são usados com a solicitação subsequente para enviar o tráfego de volta para o mesmo servidor real.</li><li>A persistência é codificada permanentemente por sessão.</li><li>O cookie expira após o navegador do cliente ser encerrado.</li><li>Requer que o cliente aceite cookies para ser eficaz.</li></ul>|
|Menos conexões|<ul><li>O servidor real com o menor número de conexões ativas recebe primeira prioridade.</li><li>O algoritmo requer uma diferença de 10 conexões, o que pode defasar os resultados para os clientes</li></ul>|
|IP persistente|<ul><li>Liga o IP de origem do solicitante ao servidor real que processa a solicitação por um hash dos 4 octetos do endereço IP solicitante.</li><li>Persiste por 60 minutos</li></ul>|
|Round-robin|<ul><li>Cada nova solicitação é designada ao próximo servidor real na rotação.</li><li>A distribuição balanceada ocorre durante amostras grandes, embora amostras pequenas possam exibir um balanceamento desproporcional.</li></ul>|
|Resposta mais curta|<ul><li>O servidor com o tempo de resposta mais curto que recebe a solicitação.</li><li>Conforme o tempo de carregamento e resposta aumenta,os servidores mais lentos começam a processar menos solicitações.</li></ul>|
|Round Robin com IP persistente|<ul><li>Cada nova solicitação é designada ao próximo servidor real na rotação.</li><li>O endereço IP do solicitante é ligado ao servidor real, resultando em solicitações subsequentes do IP sendo designadas ao mesmo servidor real.</li></ul>|
|Round Robin com inserção de cookie|<ul><li>Cada nova solicitação é designada ao próximo servidor real na rotação.</li><li>O balanceador de carga insere um cookie na solicitação e usa as informações de sessão do cookie para direcionar o tráfego para o mesmo servidor real para solicitações subsequentes.</li></ul>|
|Menos conexões com IP persistente|<ul><li>Cada nova solicitação é designada ao servidor real com o menor número de conexões ativas no momento.</li><li>O endereço IP do solicitante é ligado ao servidor real, resultando em solicitações subsequentes do IP sendo designadas ao mesmo servidor real.</li></ul>|
|Menos conexões com inserção de cookie|<ul><li>Cada nova solicitação é designada ao servidor real com o menor número de conexões ativas no momento.</li><li>O balanceador de carga insere um cookie na solicitação e usa as informações de sessão do cookie para direcionar o tráfego para o mesmo servidor real para solicitações subsequentes.</li></ul>|
|Resposta mais curta com IP persistente|<ul><li>Cada nova solicitação é designada ao servidor real com o tempo de resposta mais curto.</li><li>O endereço IP do solicitante é ligado ao servidor real, resultando em solicitações subsequentes do IP sendo designadas ao mesmo servidor real.</li></ul>|
|Resposta mais curta com inserir de cookie|<ul><li>Cada nova solicitação é designada ao servidor real com o tempo de resposta mais curto.</li><li>O balanceador de carga insere um cookie na solicitação e usa as informações de sessão do cookie para direcionar o tráfego para o mesmo servidor real para solicitações subsequentes.</li></ul>|
