---
copyright:
  years: 1994, 2017 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 서비스 그룹의 연결 재설정
{: #resetting-connections-for-a-service-group}

Load Balancer에서 서비스 그룹이 활성이면 클라이언트에서 서비스를 사용하는 방법에 따라 해당 그룹과 연관된 각 서비스를 위한 연결이 있을 수 있습니다. 경우에 따라 클라이언트는 적당하지 않은 기간 동안 하나 이상의 서비스에 연결될 수 있습니다. 연결은 제한된 리소스로 간주되므로 다른 클라이언트에서 Load Balancer를 활용할 기회가 있도록 서비스 그룹의 연결을 수동으로 재설정해야 할 수도 있습니다. 다음 단계에 따라 Load Balancer의 연결을 재설정하십시오.

1. [Local Load Balancer 세부사항](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details) 페이지에서 연결을 재설정할 서비스 그룹의 행을 식별하고 **조치 > 연결 재설정**을 클릭하십시오.
2. **예**를 눌러 조치를 확인하십시오. **아니오**를 선택하여 조치를 취소하십시오.

모든 활성 연결을 재설정하도록 요청하고 나면 서비스 그룹에서 각 서비스에 대한 활성 연결을 삭제합니다. 연결을 재설정하고 나면 조치의 성공을 확인하기 위해 화면의 맨 위에 초록색 텍스트 상자가 표시됩니다. 연결이 삭제되면 클라이언트에서 필요한 대로 다시 연결할 수 있습니다. 

위의 단계를 반복하여 언제든지 서비스 그룹의 연결을 재설정할 수 있습니다.
