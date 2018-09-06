---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 서비스 그룹 편집

{{site.data.keyword.loadbalancer_short}}에 서비스 그룹을 추가하고 나면 기본 설정(밸런싱 메소드 및 가상 포트 포함), 연결 할당 및 참고를 편집할 수 있습니다. 각 서비스 그룹의 편집 내용은 즉시 표시되며 언제든지 추가로 편집할 수 있습니다. 

서비스 그룹의 그룹 유형을 변경해야 하는 경우 서비스 그룹을 삭제하고 원하는 그룹 유형을 나타내는 새 서비스 그룹을 추가해야 합니다. 

아래 단계를 따라 {{site.data.keyword.loadbalancer_short}}의 기존 서비스 그룹을 편집하십시오.

1. [로컬 로드 밸런서 세부사항](view-all-load-balancers.html) 페이지에서 편집할 서비스 그룹에 해당하는 행의 왼쪽에 있는 펼치기 아이콘을 클릭하여 서비스 그룹 세부사항을 펼치십시오.
2. 다음과 같은 서비스 그룹 설정을 업데이트하십시오.
  - **메소드:** 드롭 다운 목록에서 [밸런싱 메소드](load_balancing_methods.html)를 선택하십시오.
  - **가상 포트:** 서비스 그룹에 사용할 포트 번호입니다. 자세한 정보는 [공통 서비스 포트 FAQ](load-balancing-faqs-2.html#what-services-can-be-load-balanced-)를 참조하십시오. 

  	**참고:** 각 서비스 그룹에는 고유 포트가 지정되어야 합니다. 고유 포트가 지정되지 않은 경우 페이지의 맨 위에 오류가 표시되며 고유 가상 포트를 지정할 때까지 서비스 그룹이 추가되지 않습니다.
  - **할당:**  서비스 그룹의 할당입니다.
  - **참고:** 서비스 그룹을 식별하는 형식이 없는 텍스트입니다.
3. **구성 저장** 단추를 클릭하여 서비스 그룹을 업데이트하십시오. **취소** 단추를 클릭하여 조치를 취소하십시오.

서비스 그룹을 편집하면 연관된 그룹의 세부사항 화면에 표시됩니다. 연결 할당을 변경한 경우 추가적으로 다른 서비스 그룹을 편집해야 할 수도 있습니다. 밸런싱 메소드를 변경한 경우, 새 밸런싱 메소드에 맞게 그룹과 연관된 서비스를 추가적으로 편집해야 할 수도 있습니다. 위의 단계를 반복하여 언제든지 서비스 그룹을 추가적으로 편집할 수 있습니다.