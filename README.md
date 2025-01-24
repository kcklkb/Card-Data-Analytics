# Card-Data-Analytics

카드사 데이터 기반 데이터 시각화 및 인사이트 도출

  
## 목차
1. [프로젝트 소개](#프로젝트-소개)
2. [개발환경](#개발환경)
3. [아키텍처 구조](#아키텍처-구조)
4. [개발환경 구성](#개발환경-구성)
5. [데이터 시각화](#데이터-시각화)
6. [인사이트 도출](#인사이트-도출)
7. [트러블 슈팅](#트러블-슈팅)
8. [프로젝트 고찰 및 회고](#프로젝트-고찰-및-회고)


## 1. 프로젝트 소개

이 프로젝트는 카드사 데이터를 시각화하고 인사이트를 도출하고자 했습니다. Ubuntu 리눅스에 Elasticsearch와 Kibana를 설치하여 카드사 데이터를 Elasticsearch에 insert하고, Kibana를 통해 데이터를 시각화했습니다. 시각화된 데이터를 기반으로 연령대별 카드 이용 분야 및 금액을 분석하고, 각 연령층의 선호 분야에 맞춘 할인 제휴 혜택을 제공하는 프로모션을 기획했습니다. 이를 통해 신규 카드 발급자를 유치하고, 고객 맞춤형 혜택을 제공하여 카드 사용 촉진을 목표로 했습니다.


## 2. 개발환경

![VirtualBox](https://img.shields.io/badge/virtualbox-2F61B4?style=for-the-badge&logo=virtualbox&logoColor=blue) ![Ubuntu](https://img.shields.io/badge/ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=blue) ![ElasticSearch](https://img.shields.io/badge/ElasticSearch-005571?style=for-the-badge&logo=ElasticSearch&logoColor=black) ![Kibana](https://img.shields.io/badge/Kibana-005571?style=for-the-badge&logo=kibana&logoColor=white)


## 3. 아키텍처 구조

## 4. 개발 환경 구성

- **ElasticSearch/Kibana 7.11.1 설치**: GPG키 및 저장소 추가 -> 패키지 목록 업데이트 및 설치

![image](https://github.com/user-attachments/assets/b5973e1b-5705-43bf-9e2b-b0c215ea9bab)
![image](https://github.com/user-attachments/assets/6b5478de-c84a-400f-a1a8-234d641e9e6b)


- **ElasticSearch/Kibana 네트워크 설정**: 포트 9200/5601사용 -> network.host: 0.0.0.0

![image](https://github.com/user-attachments/assets/76f35525-9028-4b03-91c0-9e1a3707225f)
![image](https://github.com/user-attachments/assets/9cbe1c7e-5c06-4d2e-a747-18d9a25fc618)


- **ElasticSearch vm.max_map_count 값 수정/파일 권한 확인 및 설정**

![image](https://github.com/user-attachments/assets/a0292464-00fc-4c03-ac06-e24ba4019c35)
![image](https://github.com/user-attachments/assets/f317ee73-172f-4c62-af84-98cb4dfe4437)

- **서비스 활성화 및 시작**

![image](https://github.com/user-attachments/assets/4bd5ead3-c295-4423-827d-504ab37a6267)
![image](https://github.com/user-attachments/assets/85224540-2dd2-4828-9628-5a486a2c8175)

- **포트 포워딩**

![image](https://github.com/user-attachments/assets/5a4311e4-6eb9-4300-ab95-bc8ee86b4ba3)

## 5. 데이터 시각화
- **연령대별 총 사용 금액 및 신용/체크카드 사용 금액**: 각 연령별 사용 금액분석

![image](https://github.com/user-attachments/assets/fe56b0ee-6f2f-40ca-87c7-761b2a45a6ef)


- **연령대별 선호 분야**: 각 연령대에 맞춘 카드 사용 패턴 분석

![image](https://github.com/user-attachments/assets/f68e147a-d441-4e4b-a963-abb9ac00d6dc)


- **라이프 스테이지별 사용 금액**: 특정 라이프 스테이지에 인기 있는 카테고리 제안

![image](https://github.com/user-attachments/assets/a4806371-3675-4022-a077-adde942cd24f)


## 인사이트 도출

- **카드 발급 유도 전략**: 분석 결과를 기반으로 신규 고객을 유도할 수 있는 혜택 기획

## 트러블 슈팅

1. **ubuntu내 ElasticSearch 설치 시 싱글 노드 사용 문제**  
   - 문제: 데이터를 Elasticsearch에 삽입할 때 발생한 오류 해결 과정
   - 해결 방법: 로그 분석 및 설정 변경을 통한 해결

2. **ubuntu내 Kibana 설치 시 yml파일 내 네트워크 설정 문제**  
   - 문제: Kibana에서 데이터가 제대로 시각화되지 않은 문제
   - 해결 방법: 필터와 쿼리 수정, 시각화 설정 조정

## 프로젝트 고찰 및 회고

이번 프로젝트는 카드사 데이터를 Elasticsearch에 입력하고, Kibana를 통해 시각화를 할 수 있는 기회였습니다. 특히, Ubuntu 리눅스 환경에서 Elasticsearch와 Kibana를 설치하고 구성하는 과정에서 각종 네트워크 설정을 변경하고 최적화하는 경험을 얻을 수 있었습니다. 이러한 과정은 시스템 설정에 대한 깊은 이해를 돕고, 향후 서버 관리에 필요한 기술적인 역량을 키울 수 있는 기회가 되었습니다.

또한, 데이터를 시각화하는 과정에서 실제 마케팅에 활용할 수 있는 인사이트를 도출하는 재미를 느꼈습니다. 연령대별 카드 이용 패턴을 분석하고, 고객 맞춤형 혜택을 제공하는 방법을 고민하면서, 현업에서 활용 가능한 대용량 데이터를 기반으로 한 데이터 분석의 중요성과 가능성을 실감했습니다. 앞으로도 이러한 분석 작업을 통해 더 많은 인사이트를 도출하고, 실제 마케팅 전략에 반영할 수 있는 데이터 분석을 이어가고 싶다는 생각이 들었습니다.







