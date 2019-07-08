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

# Local Load Balancer를 IBM Cloud Load Balancer로 마이그레이션

다음 프로시저를 수행하여 Local Load Balancer를 IBM© Cloud Load Balancer로 마이그레이션할 수 있습니다. 

## 1단계: Cloud Load Balancer 주문
{: #step-1-order-a-cloud-load-balancer}

IBM Cloud Load Balancer 서비스를 주문하려면 [IBM Cloud 카탈로그![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")]( https://cloud.ibm.com/catalog/infrastructure/load-balancer-group){:new_window}에서 **IBM Cloud Load Balancer**를 선택하십시오. **작성**을 클릭한 후 다음 프로시저를 수행하십시오. 

1. 기본 서비스 매개변수를 정의하십시오(예: 이름 및 설명). 
2. 데이터 센터를 선택하십시오. 
3. 로드 밸런서 유형으로 **공용**을 선택하십시오. 
4. 로드 밸런서를 배치할 서브넷을 선택하십시오. 

  로드 밸런서 서비스 인스턴스는 이 서브넷의 네트워크 인터페이스 중 하나를 보유하게 됩니다. 애플리케이션 서버가 이 서브넷에 있는지 아니면 이 서브넷에서 접근할 수 있는지 확인하십시오. 필요한 경우 VLAN Spanning을 사용으로 설정하십시오.
  {: note}

5. 로컬 로드 밸런서에서 현재 사용 중인 서비스 그룹과 동일한 구성으로 프론트 엔드 및 백엔드 애플리케이션 프로토콜 및 포트를 작성하십시오. 이 구성에 대한 자세한 정보는 [IBM Cloud Load Balancer 매개변수 구성](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configuring-ibm-cloud-load-balancer-parameters)을 참조하십시오. 
6. SSL 오프로드를 사용으로 설정하려면 프론트 엔드 프로토콜을 HTTPS로 설정하고 백엔드 프로토콜을 HTTP로 설정하십시오. 그런 다음 인증서 드롭 다운 상자에서 Local Load Balancer와 동일한 SSL 인증서를 선택하십시오. 모든 기존 SSL 인증서는 [IBM Cloud 인증서 저장소![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com/classic/security/sslcerts){:new_window}를 통해 관리되기 때문에 Local Load Balancer에 사용하는 인증서는 드롭 다운 목록에 있습니다. 
7. 원하는 경우 상태 검사 매개변수를 조정하고 그렇지 않으면 기본 설정을 사용하십시오. 상태 검사 매개변수에 대한 자세한 정보는 [IBM Cloud Load Balancer 매개변수](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configure-health-checks)를 참조하십시오. 
8. **서버 연결**을 클릭하여 Local Load Balancer 서비스에 사용한 서버 인스턴스를 추가하십시오. 
9. 페이지를 검토하고 서비스 계약을 확인한 후 **작성**을 클릭하십시오. 

모든 서비스 인스턴스를 보여주는 로드 밸런서 목록이 표시됩니다. 

새로 작성된 로드 밸런서가 이 목록에 즉시 표시되지 않을 수 있습니다. 몇 분이 지나면 새 로드 밸런서가 회색(상태가 `Offline`임을 나타냄)으로 표시됩니다. 다시 몇 분이 지나면 새 로드 밸런서가 초록색(`Online` 상태임을 나타냄)으로 표시됩니다. 이러한 변경을 보기 위해 화면을 새로 고쳐야 할 수 있습니다.
{: note}

이 페이지에서 서비스 이름을 클릭하면 서비스 개요 페이지로 이동합니다. **프로토콜**, **상태 검사** 및 **서버 인스턴스** 탭으로 이동하여 구성을 추가로 편집할 수 있습니다. 

## 2단계: Cloud Load Balancer가 예상대로 작동 중인지 확인
{: #step-2-verify-your-cloud-load-balancer-is-working-as-expected}

이 지점에서는 이제 이전의 Local Load Balancer와 새 IBM Cloud Load Balancer라는 두 개의 로드 밸런서가 동시에 작동하고 있습니다.
{: important}

위의 상태 페이지에 나열된 도메인을 사용하여 새 IBM Cloud Load Balancer를 테스트하여 로컬 로드 밸런서의 VIP와 동일하게 작동하는지 확인하십시오. 

그런 다음 새 Cloud Load Balancer 도메인을 대신 사용하도록 Local Load Balancer VIP를 사용하는 위치를 업데이트하십시오. 

새 Cloud Load Balancer의 이 구성을 수행할 때 유일하게 마이그레이션 프로세스에서 작동 중단 또는 트래픽 중단이 발생할 수 있습니다.
{: note}

## 3단계: 이전 Local Load Balancer 취소
{: #step-3-cancel-your-local-load-balancer}

새 IBM Cloud Load Balancer에 대한 도메인으로 모든 Local Load Balancer VIP를 대체하고 기능이 예상대로 작동함을 확인한 경우 Local Load Balancer 서비스를 안전하게 취소할 수 있습니다. 이를 위해서는 다음과 같은 단계를 수행하십시오. 

1. [Local Load Balancer 목록 페이지](https://cloud.ibm.com/classic/network/loadbalancing/local)로 이동하십시오. 
2. 삭제할 로드 밸런서를 찾아서 옆에 있는 화살표를 펼치십시오. 
3. 행의 끝에 있는 빨간색 **X**를 클릭하여 로드 밸런서를 취소하십시오. 
