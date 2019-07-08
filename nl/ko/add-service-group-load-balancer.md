---
copyright:
  years: 1994,2017,2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Load Balancer에 서비스 그룹 추가
{: #adding-a-service-group-to-a-load-balancer}

{{site.data.keyword.loadbalancer_short}}를 추가하고 나면 언제든지 {{site.data.keyword.loadbalancer_short}}에 새 서비스 그룹을 추가할 수 있습니다. 서비스 그룹은 다양한 유형으로 지원되며 광범위한 단일 또는 하이브리드 밸런싱 메소드를 제공합니다. 새 서비스 그룹을 추가할 때 모든 그룹 연결 할당의 합계가 100% 인지 확인하는 것이 중요합니다. 아래 단계를 따라 {{site.data.keyword.loadbalancer_short}}에 새 서비스 그룹을 추가하십시오.

1. [Local Load Balancer 세부사항](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details) 페이지에서 **그룹 추가** 단추를 클릭하십시오. 또는 **조치 > 그룹 추가**를 클릭할 수 있습니다. 페이지 맨 아래에 새 서비스 그룹 섹션이 추가됩니다.
2. **그룹** 드롭 다운 목록에서 원하는 그룹 유형을 선택하고 **메소드** 드롭 다운 목록에서 원하는 밸런싱 메소드를 선택하십시오. 각 로드 밸런싱 메소드에 대한 자세한 정보는 [로드 밸런싱 메소드](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-load-balancing-methods#load-balancing-methods)를 참조하십시오.
3. **가상 포트** 필드에 서비스 그룹에 사용할 포트 번호를 입력하십시오. 자세한 정보는 [공통 서비스 포트 FAQ](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-faqs-for-local-load-balancer#what-services-can-be-load-balanced-)를 참조하십시오.

	**참고:** 각 서비스 그룹에는 고유 포트가 지정되어야 합니다. 고유 포트가 지정되지 않은 경우 페이지의 맨 위에 오류가 표시되며 고유 가상 포트를 지정할 때까지 서비스 그룹이 추가되지 않습니다.
4. **할당** 필드에 할당을 입력하십시오.
5. 원하는 경우 **참고** 텍스트 상자에 참고를 입력하십시오.
6. **구성 저장** 단추를 클릭하여 새 서비스 그룹을 추가하십시오. **취소**를 클릭하여 조치를 취소하십시오.

서비스 그룹을 추가하고 나면 언제든지 삭제하거나 편집할 수 있습니다. 연결을 서비스 그룹으로 재설정하고 새 서비스를 그룹에 추가할 수 있습니다. 서비스 그룹이 지정된 연결 할당을 기반으로 로드 밸런싱을 시작하려면 하나 이상의 서비스를 서비스 그룹에 [추가](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group)해야 합니다.

## 다음으로 수행할 사항
{: #what-happens-next-a}

[서비스 그룹에 서비스 추가](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group).
