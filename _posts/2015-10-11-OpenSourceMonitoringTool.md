---
layout: post
title:  "오픈 소스 서버 모니터링 툴 소개"
date:   2015-10-11 10:10:00
author: 조창현
profile: chcho.png
---

서버 관리자들이 모니터링 없이 서버를 운용한다는 것은 있을 수 없는 일입니다. 서버의 중요 지표를 실시간으로 수집해 관리자가 즉각적으로 인지하도록 표시해 주는 것은 물론, 축적된 지표 데이터를 토대로 향후 발생 할 수 있는 문제를 미연에 방지할 수 있도록 도와주는 것이 모니터링이며, 이는 와탭이 추구하는 궁극적인 목표입니다.

![alt text](/assets/images/chcho/01/1_whatap.png "1_whatap")
<center>[WhaTap]</center> 

##### [와탭이 수집하는 서버의 중요 지표]
	
- 서버의 동작 상태
- CPU, Memory, Disk, Traffic 사용량
- 동작 중인 Process의 서버 자원 사용량
- 파일 및 이벤트 로그의 이상 징후
	
이러한 와탭의 핵심 기능들은 수집된 데이터 보존 기간 제한을 제외하고 사용에 제약 없이 무료로 제공되고 있습니다.

여기 와탭 이외에 무료로 서버를 모니터링 할 수 있는 다양한 오픈 소스 모니터링 툴 중에 세계적으로 인정받는 몇 가지를 간단히 소개합니다.


  
## Nagios 
[https://www.nagios.com](https://www.nagios.com)

![alt text](/assets/images/chcho/01/2_nagios.png "2_nagios")
<center>[Nagios]</center>

Nagios는 오픈 소스 컴퓨터 소프트웨어 어플리케이션으로 시스템, 네트워크 및 인프라스트럭처를 모니터링 합니다. Nagios는 서버, 스위치, 어플리케이션과 서비스에 대한 모니터링과 알림 서비스를 제공하여 각 항목의 상태에 문제가 있음을 알림으로써 그 후 발생할 수 있는 문제를 해결합니다. Nagios는 원래 리눅스에서 실행되도록 설계 되었지만 유닉스 기반의 변종 운영체제에서도 잘 동작합니다. Nagios는 Free Software Foundation이 발표한 GNU 일반 공중 사용 라이선스(GPL) 버전2의 조건에 따라 배포되는 무료 소프트웨어입니다.

Nagios 개발자들은 IT 인프라스트럭처 모니터링의 업계 표준이라고 주장하지만, 지난 몇 년간 많은 발전을 이루지는 못 했습니다. 그들의 주장은 어느 정도 타당하지만 일부에 여전히 해결되지 않는 문제가 존재합니다.

##### [장점]

- 다양한 사용자 커뮤니티를 구성
- 설치하기 쉬운 강력한 플러그인들을 다수 보유
- 웹 프론트 엔드에서 사용하기 편리
- 디버깅 플러그인이 단순
- 호스트 그룹 설정이나 알림 옵션 등의 세심한 설정이 가능
- 인터랙티브 편집 플러그인을 이용해 관리하기 쉬운 그래프를 만들 수 있음  

##### [단점]

- 수집된 모니터링 데이터를 그래프로 만들 수 없는 경우가 있어 다른 툴을 이용해야 하는 경우가 있음
- 복잡한 텍스트로 구성된 설정 방식 때문에 설정에 무리가 있고 매개 변수를 자주 확인해야 함
- 서드파티 플러그인의 경우 잘못된 문서를 제공해주는 경우가 있음
- 직관적이지 않은 웹 인터페이스
- 대부분의 플러그인에 구성 항목이 없어 직접 작성하는 데 시간이 소요
- 플러그인의 모든 파라미터에 별개의 구성 항목이 필요
- 대부분의 체크가 Nagios 서버에서 이뤄지므로 서버에 부하가 걸리는 경우가 있음
- 모든 경고 알림이 기본적으로 설정되어 있어 적절히 설정하지 않으면 알림 스팸을 받을 수 있음


  
## Cacti
[http://www.cacti.net] (http://www.cacti.net)

![alt text](/assets/images/chcho/01/3_Cacti.png "3_Cacti")
<center>[Cacti]</center>

Cacti는 업계 표준 오픈 소스 데이터 로깅 도구인 RRDtool에 대한 프론트 엔드용 응용 프로그램으로 설계된, 오픈 소스 웹 기반 네트워크 모니터링 및 그래프 도구입니다. Cacti는 사용자가 소정의 간격으로 서비스를 폴링하고 그 결과 데이터를 그래프로 표시 할 수 있습니다. 일반적으로 CPU 부하 및 네트워크의 대역폭 같은 수치 데이터를 그래프로 변환합니다. 일반적인 사용은 단순 네트워크 관리 프로토콜 (SNMP)를 통해 네트워크 스위치 또는 라우터 인터페이스를 폴링하여 네트워크 트래픽을 감시하는 것입니다.  
프론트 엔드는 각자의 그래프 세트를 가진 복수의 사용자를 처리 할 수 있어서 전용 서버, 가상 개인 서버 및 코로케이션을 공급하는 웹 호스팅 제공 업체가 고객들의 대역폭 통계를 확인하기 위해 사용하기도 합니다. RRDtool의 수동 구성 없이 모니터링 할 수 있는 특정 설정을 허용하여 데이터 수집 자체를 구성하는 데 사용될 수 있습니다. Cacti는 쉘 스크립트 실행을 통해 다양한 소스를 모니터링 할 수 있도록 확장 할 수 있습니다. 

Cacti는 RRD에 특화된 정교한 프론트 엔드 툴입니다. 대부분의 구성은 자사의 웹 인터페이스를 통해 이뤄집니다. 사용자 인터페이스는 훌륭하지만 신뢰성이 떨어지는 부분과 유연하지 않다는 것이 단점입니다.

###### [장점]
- 대부분의 기능에 아름답고 심플한 웹 인터페이스를 제공
- 자바 스크립트를 사용한 강력한 그래프 기능
- 시스템 권한에 대한 미세한 설정이 가능하여 사용자 별 권한 부여가 가능
- 원하는 정보만 정확하게 볼 수 있게 자유로운 그래프가 배치가 가능

##### [단점]
- 서버의 과부하 없이도 그래프가 아무 이유 없이 작동을 중지하거나 값이 누락되는 경우가 있음
- 다수의 시스템을 설치하거나 다양한 템플릿을 설정할 때 웹 인터페이스에서 그 만큼의 많은 설정을 해야 함
- 일부 서드파티 템플릿의 품질이 좋지 않음
- SNMP를 제대로 처리하지 못 함
- 지표를 수집하는 최소 주기가 5분이라서 데이터 누락 및 잘못된 결과를 얻을 수 있음
- 지표 수집의 오류를 디버깅하는 것이 불가능에 가까움
- 때때로 혼란스러운 웹 인터페이스
- 임계치에 도달해도 알림이 발생하지 않는 경우가 있음
- 디테일한 그래프 데이터를 장기간 보관할 수 없음


  
## Zenoss
[http://www.zenoss.com/] (http://www.zenoss.com/)

![alt text](/assets/images/chcho/01/4_zenoss.gif "4_zenoss")
<center>[Zenoss]</center>

Zenoss(Zenoss 코어)는 Zope 서버에 기초한 애플리케이션, 서버 및 네트워크 관리용 오픈 소스 플랫폼입니다. Zenoss 코어는 시스템 관리자가 가용성, 목록 / 구성, 성능 및 이벤트를 모니터링 할 수 있는 웹 인터페이스를 제공합니다. GNU 일반 공중 사용 라이선스(GPL) 버전 2의 조건에 따라 무료로 배포되고 있습니다.

###### [장점]
- 아름다운 웹 인터페이스
- 구글 맵 등을 통해 설치된 서버의 위치를 세계 지도에서 표현하는 기능
- 일부 매개변수를 시스템에서 자동으로 검색할 수 있음
- 통상의 SNMP 모니터링 에서 잘 동작
- 네이티브 WMI를 통해 윈도우를 모니터링 할 수 있음
- 큰 팬층

###### [단점]
- 웹 인터페이스가 느림
- 실제로 무슨 일이 일어나고 있는지 알 수 없는 불투명한 작업
- 신뢰성에 대한 의심
- 한 개만 지원되는 대시보드
- 설정 및 데이터가 MySQL, 내부 Zope 데이터베이스 스토리지 및 RRD 파일이 저장된 디스크의 전역에 퍼져 있음
- 플래시 기반의 그래프들이 시스템이 연결된 상황을 표시하지만 시스템에 대한 세부 사항을 표시하지 않음
- 제한적인 오픈 소스 버전이며, 풀 버전을 이용하려면 제품 구매가 필요


  
## Zabbix
[http://www.zabbix.com](http://www.zabbix.com)

![alt text](/assets/images/chcho/01/5_zabbix.png "5_zabbix")
<center>[Zabbix]</center>

Zabbix는 Alexei Vladishev에 의해 만들어진 네트워크 및 애플리케이션에 대한 엔터프라이즈 형 오픈 소스 모니터링 솔루션으로 다양한 네트워크 서비스, 서버, 네트워크 하드웨어의 상태를 감시하고 추적 할 수 있도록 설계되었습니다. Zabbix는 데이터를 저장하기 위해 MySQL, PostgreSQL, SQLite, Oracle, IBM DB2를 사용하며, 백 엔드는 C로 작성되었고, 웹 프론트 엔드는 PHP로 작성되었습니다.

Zabbix는 다양한 모니터링 옵션을 제공합니다. 간단한 검사는 모니터링 할 호스트에 소프트웨어를 설치하지 않고도 SMTP나 HTTP와 같은 표준 서비스의 가용성과 응답성을 검증하여 실행할 수 있습니다. Zabbix는 GNU 일반 공중 사용 라이선스(GPL) 버전2의 조건에 따라 배포되는 무료 소프트웨어입니다.

##### [장점]
- 강력한 모니터링 기능과 그래프를 하나의 도구로 결합시킨 점
- 알림에 대해 구성을 고도화 할 수 있음
- 알림에 완벽하게 사용자 정의 메시지를 이용할 수 있음
- 기본적으로 30초 마다 지표를 수집하며, 인터벌을 조정할 수 있음
- 빠른 웹 인터페이스
- 시스템에 대한 사용자 권한 설정으로 특정 사용자를 특정 뷰에 한정
- 수집 된 데이터를 유연하지 못한 RRD 파일 대신 MySQL 등의 데이터베이스에 저장
- 데이터 저장 기간을 자유롭게 구성 할 수 있으며, 데이터베이스를 백업 기능이 지원
- 템플릿을 사용하여 검사 시간을 절약
- 사용자 정의에 따른 다양한 그래프 지원
- 다양한 스크린과 슬라이드 쇼를 이용하여 대시보드를 구현
- 매우 유연한 트리거 설정
- 쉘 스크립트를 사용하여 알림을 쉽게 스크립팅
- Zabbix 프록시를 사용하여 원격 모니터링을 쉽게 할 수 있음

##### [단점]
- 알림 설정 부분에서 다량의 임계치 설정이 필요
- 웹 인터페이스 기능이 너무 많고 복잡
- 맵 편집기를 이용해 설정하는 시간이 많이 소요
- 아이템 당 하나의 값만을 리턴 받을 수 있음
- 같은 종류의 개별 자산을 모니터링 할 때 템플릿이 적용되지 않아 일일이 트리거 설정이 필요해 번거로움
- 모니터링 서버에서 사용할 수 있는 자산을 자동으로 검색하지 않음
- 디버깅하기 어려움


  
## 결론

모니터링 없이 서버를 운용하는 것은 마치 '계기판 없는 자동차를 운행하는 것'과 같습니다. 사용자의 서버 운용 환경에 맞춰 와탭을 비롯한 다양한 모니터링 툴을 이용하여 보다 편리한 서버 관리 환경을 구축할 수 있었으면 하는 바람입니다.