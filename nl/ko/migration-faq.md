---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud, faq, support

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
{:faq: data-hd-content-type='faq'}

# IBM Cloud Load Balancer 마이그레이션 FAQ
{: #migration-faq}

다음과 같은 자주 질문되는 내용(FAQ)이 IBM Local Load Balancer 마이그레이션 프로세스에 적용됩니다. 

## Local Load Balancer 마케팅 종료(EOM) 발표 및 발효 날짜는 언제입니까? 
{: faq}

EOM 발표 날짜는 2019년 3월 1일이고 발효 날짜는 2019년 6월 1일입니다. 이 날짜 이후에는 새로운 판매가 발생할 수 없습니다. 

## EOM 이후에도 지원이 제공됩니까? 
{: faq}

예. 기존 Local Load Balancer 고객에 대한 지원은 제공됩니다. 

## IBM Cloud Load Balancer를 시작하려면 어떻게 해야 합니까? 
{: faq}

[IBM Cloud Load Balancer 문서](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-getting-started)부터 읽는 것이 좋습니다. 

## Local Load Balancer 서비스에서 IBM Cloud Load Balancer로 마이그레이션 경로가 존재합니까? 
{: faq}

자동화된 마이그레이션 경로는 존재하지 않습니다. 하지만 Local Load Balancer 서비스를 끄도록 요청하고 IBM Cloud 콘솔에서 Cloud Load Balancer 서비스를 주문할 수 있습니다. 

## Local Load Balancer와 Cloud Load Balancer의 차이점은 무엇입니까? 
{: faq}

Local Load Balancer는 하드웨어 기반 로컬 로드 밸런싱 서비스이고 IBM Cloud Load Balancer는 공용 네트워크와 사설 네트워크 모두를 지원하는 비용 효율적이고 자동으로 스케일링되는 로드 밸런싱 솔루션을 제공하는 클라우드 기반 서비스입니다. 

## Cloud Load Balancer가 Local Load Balancer와 동일한 용어를 사용합니까? 
{: faq}

동일한 용어를 사용하지 않는 경우도 있습니다. 다음 표에서는 Local Load Balancer의 주요 용어와 Cloud Load Balancer의 차이가 있는 해당 용어를 비교합니다. 

| Local Load Balancer 용어 | Cloud Load Balancer 용어 |
| ------------- | ------------- |
| 서비스 그룹 | 프로토콜 |
| 서비스 | 서버 인스턴스 |
| VIP | FQDN |

## Cloud Load Balancer로 마이그레이션해도 내 로드 밸런서에 대해 단일 고정 IP 주소를 계속 가집니까? 
{: faq}

IBM Cloud Load Balancer에 대한 IP는 고정 IP가 아닙니다. Cloud Load Balancer는 풀에서 로드 밸런서 인스턴스를 지정하며 이를 위해서는 언제나 완전한 도메인 이름(FQDN)이 필요합니다. 따라서 Cloud Load Balancer의 개별 IP 주소는 변경될 수 있습니다. 

## 공용/사설 VSI 및 베어메탈 솔루션에 IBM Cloud Load Balancer를 사용할 수 있습니까? 
{: faq}

예. 공용 및 사설 VSI와 베어메탈에 Cloud Load Balancer를 사용할 수 있습니다. 

## IBM Cloud Load Balancer가 GDPR과 호환됩니까? 
{: faq}

예. Cloud Load Balancer 오퍼링은 GDPR과 호환됩니다. 

## 마이그레이션을 시작한 후 내 시스템에서 예상되는 작동 중단 시간 또는 트래픽 중단 시간은 얼마나 됩니까? 

로드 밸런서 마이그레이션 덕분에 작동 중단 또는 트래픽 중단이 발생하지 않습니다. Local Load Balancer 구성을 새 IBM Cloud Load Balancer FQDN으로 업데이트할 때만 작동 중단 또는 트래픽 중단이 발생할 수 있습니다. 

## 지시사항에는 Local Load Balancer를 취소하기 전에 IBM Cloud Load Balancer를 주문하라고 되어 있습니다. 두 디바이스를 구성하는 동안 내 시스템 또는 워크로드에 영향이 있습니까? 

아니오. Cloud Load Balancer와 Local Load Balancer는 독립적으로 작동하는 두 개의 개별 오퍼링입니다. 

## 내 Local Load Balancer에 대해 "초당 연결" 옵션을 선택했었습니다. Cloud Load Balancer에 대해서도 이렇게 구성해야 합니까? 

아니오. IBM Cloud Load Balancer는 로드 용량을 자동으로 조정합니다. [Cloud Load Balancer 수평적 확장](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-performing-ibm-cloud-load-balancer-basics#horizontal-scaling) 주제에서 이에 대한 자세한 내용을 읽을 수 있습니다. 

## Cloud Load Balancer 사용 시 어떤 프로토콜을 선택할 수 있습니까? 

HTTP, HTTPS 및 TCP 프로토콜을 선택할 수 있습니다. 계층 7 지원도 제공합니다. 자세한 정보는 [기능 개요](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-about-ibm-cloud-load-balancer#overview-of-features)를 참조하십시오. 

## 특정 유형의 암호가 필요합니다. Cloud Load Balancer가 해당 암호를 지원합니까? 

IBM Cloud Load Balancer는 SSL 오프로드의 TLS 버전 1.2를 지원합니다. [Cloud Load Balancer SSL 암호 스위트](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-ssl-offload-with-ibm-cloud-load-balancer#ssl-cipher-suites)에서 지원되는 SSL 암호에 대한 자세한 정보를 찾을 수 있습니다. 
