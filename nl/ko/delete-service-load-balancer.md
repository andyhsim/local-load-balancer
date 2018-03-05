---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 서비스 삭제 

{{site.data.keyword.loadbalancer_short}}의 서비스 그룹에 서비스를 추가하고 나면 언제든지 삭제할 수 있습니다. 서비스 그룹에서 서비스를 삭제하면, 수동으로 서비스 그룹에 다시 추가하지 않는 한 {{site.data.keyword.loadbalancer_short}}에서 서비스를 활용할 수 없습니다. 

또는 서비스를 사용하지 않도록 설정할 수 있습니다. 그러면 밸런싱 작업에 사용하지 않으면서 서비스 그룹과 서비스를 계속 연관시킬 수 있습니다. 서비스를 {{site.data.keyword.loadbalancer_short}} 서비스 그룹과 연관된 상태로 유지하려면 [서비스를 편집](edit-service-load-balancer.html)하고 **사용** 선택란을 선택 취소하십시오. 

다음 단계를 따라 {{site.data.keyword.loadbalancer_short}}에서 서비스를 삭제하십시오.

1. [로컬 로드 밸런서 세부사항](view-all-load-balancers.html) 페이지에서 삭제할 서비스를 찾은 후 왼쪽에 있는 화살표를 펼치십시오.
2. 서비스의 행 끝에 있는 빨간색 'x'를 클릭하십시오.
3. 업데이트할 설정의 페이지 맨 아래에서 **구성 저장**을 클릭하십시오.

서비스를 삭제하고 나면 구성이 저장되고 변경이 즉시 적용됩니다. 삭제된 서비스가 서비스 그룹과 연관된 유일한 서비스이면 새 서비스를 추가해야 그룹에서 로드 밸런싱 활동을 수행할 수 있습니다.
