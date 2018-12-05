---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 로드 밸런서의 가중치 구성

가중치는 더 많은 트래픽을 받게 할 서버에 숫자 값을 지정하는 시스템입니다. 상태 검사 결과에 따라 서버가 온라인 상태에 있는 한 숫자가 높을수록 우선순위가 높은 것입니다.  

예를 들어 _server1_의 가중치가 80이고 _server2_의 가중치가 20이면 입력되는 10개의 연결마다 _server1_에 8개가 할당되고 _server2_에 2개가 할당됩니다. _server1_이 오프라인이 되거나 풀에서 제거되면 모든 연결이 _server2_로 이동합니다.

[서비스 그룹에 서비스를 추가](add-service-service-group.html)할 때 또는 서비스를 작성한 다음 [서비스를 편집](edit-service-load-balancer.html)하여 특정 서비스의 가중치를 구성할 수 있습니다.

구성이 저장되고 나면 변경이 즉시 적용됩니다. 서비스의 세부사항에서 서비스 연결을 모니터할 수 있습니다.
