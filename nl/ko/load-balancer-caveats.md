---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 알려진 제한사항

프록시 로드 밸런서의 특성상, 클라이언트 요청의 소스 IP는 로드 밸런서의 IP에서 옵니다. 따라서 클라이언트 정보를 확보하기 위해 소스 IP를 확인하는 로그 통계 프로그램과 기타 애플리케이션에 영향을 미칩니다. IBM Cloud에서는 Apache(모든 플랫폼)와 IIS(Windows)의 로그 항목을 올바르게 다시 작성하는 솔루션을 제공합니다.

지시사항과 필요한 추가 플러그인에 액세스하려면 먼저 [IBM Cloud VPN](/docs/infrastructure/iaas-vpn/getting-started.html){: new_window}에 연결해야 합니다. 연결하고 나면 [다운로드 페이지](http://downloads.softlayer.local/loadbalancer/){: new_window}를 방문하여 {{site.data.keyword.loadbalancer_short}}의 플러그인과 지시사항을 찾으십시오.

**참고:** 다운로드 링크에 액세스하려면 IBM Cloud VPN에 로그인해야 합니다. 
