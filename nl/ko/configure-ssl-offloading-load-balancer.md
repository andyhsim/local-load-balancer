---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 로드 밸런서에서 SSL 오프로딩 구성

로드 밸런서에는 SSL 오프로딩을 제공하는 기능이 있으므로, 현재 기능을 수행하는 시스템의 로드를 현저히 줄일 수 있습니다. SSL 오프로딩을 활용하려면 이 기능을 제공하는 {{site.data.keyword.loadbalancer_short}}를 구매해야 합니다. SSL 기능을 제공하는 로드 밸런서는 **로컬 로드 밸런서 주문** 대화 상자에 "SSL 오프로드 포함"이라고 명시되어 있습니다. SSL 오프로딩 사용 {{site.data.keyword.loadbalancer_short}}를 프로비저닝한 후 구성해야 합니다. 다음 단계를 따라 {{site.data.keyword.loadbalancer_short}}에서 SSL 오프로딩을 구성하십시오.

1. [로컬 로드 밸런서 세부사항](view-all-load-balancers.html) 페이지의 로드 밸런서 드롭 다운 메뉴에서 **조치 > SSL 구성**을 클릭하십시오.
2. **인증서** 드롭 다운 상자에서 원하는 SSL 인증서를 선택하십시오. 다음을 참고하십시오.
  - 전용이 아닌 {{site.data.keyword.loadbalancer_short}} 가상 IP(VIP)는 최대 SSL 인증서 비트 크기인 2048로 제한됩니다.
  - 이 단계를 성공적으로 완료하려면 하나 이상의 SSL 인증서를 고객 포털에 저장해야 합니다. [SSL 인증서에서 가져오기](import-ssl-cert.html)를 참조하십시오.
3. **사용** 선택란을 선택하십시오.
4. 지원할 암호를 선택하십시오.
5. **업데이트** 단추를 클릭하십시오.

{{site.data.keyword.loadbalancer_short}}에서 SSL 오프로딩을 활성화하고 나면 SSL 상태가 **사용 안함**에서 **활성**으로 변경됩니다. SSL 오프로딩을 활성화하고 나면 이전에 SSL 연결을 처리한 시스템에서 수행한 로드가 일반적으로 줄어듭니다. 언제든지 SSL 오프로딩 상태를 변경할 수 있습니다. 오프로드 SSL 탭으로 돌아가서 선택란을 선택 취소하여 {{site.data.keyword.loadbalancer_short}}의 SSL 오프로딩을 사용하지 않도록 설정하십시오.
