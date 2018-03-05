---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar verificações de funcionamento para um serviço

Verificações de funcionamento são projetadas para verificar regularmente se um servidor está on-line e aceitar tráfego para que um
{{site.data.keyword.loadbalancer_short}} passe pelo tráfego. As verificações de funcionamento são projetadas para responder com uma resposta ATIVO ou INATIVO, dependendo do tempo limite customizado. O intervalo padrão é 120 segundos.

Há vários métodos de configurar verificações de funcionamento.

- **Padrão:** a configuração padrão é Ping.
- **HTTP:** verifica se a porta 80 para o endereço IP listado responde com código HTTP 200 (Ok).
- **HTTP-CUSTOM:** muito semelhante ao HTTP regular, exceto que você designa o tipo de conexão, o local de sua verificação de funcionamento e a resposta que está sendo prevista. Esta é uma opção avançada.
- **Ping:** um teste simples de ping sobre ICMP.
- **TCP:** muito semelhante a um teste de ping, mas explicitamente sobre TCP. Esta opção deverá ser usada se você tiver conexões ICMP bloqueadas.

Será possível configurar verificações de funcionamento para um serviço específico
quando você [incluir o serviço em um grupo de
serviços](add-service-service-group.html) ou [editando o serviço](edit-service-load-balancer.html)
após ele ter sido criado.

Quando sua configuração tiver sido salva, as mudanças entrarão em vigor imediatamente. Você será capaz de monitorar o status de suas verificações de funcionamento pelo ícone de status no grupo de serviços.
