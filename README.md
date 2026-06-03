<div align="center">

# ZIPS AI

### 스마트홈 월패드 모바일 연동 시스템 구축

실시간 모니터링 및 원격 제어를 위한 모바일 애플리케이션 · 서버 개발

<br>


<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/SpringBoot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" />

<br>

<img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" />
<img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" />
<img src="https://img.shields.io/badge/Swift-F05138?style=for-the-badge&logo=swift&logoColor=white" />

<br>

<img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white" />
<img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=for-the-badge&logo=influxdb&logoColor=white" />

</div>

---

## 📌 Overview

자사 스마트홈 월패드와 연동하여 사용자가 모바일 환경에서 실시간 상태를 확인하고 원격 제어할 수 있도록 Android, iOS 애플리케이션과 백엔드 서버를 구축하는 프로젝트



## ✨ Features

* 월패드 상태 실시간 모니터링
* 모바일 기반 원격 제어
* 실시간 사용자 위치 데이터 수집 및 저장
* 관리자용 백오피스 시스템 구축
* Android / iOS 통합 서비스 제공


## 🏗 Architecture

<div align="center">
  <img src="./img/architecture.png" width="1000"/>
</div>

## ⚙ Tech Stack

| Category | Stack                                 |
| -------- | ------------------------------------- |
| Backend  | Node.js, JavaScript, SpringBoot, Java |
| Mobile   | Flutter, Kotlin, Swift                |
| Database | MariaDB, InfluxDB, MongoDB            |
| Infra    | Docker Container                      |



## 🛠 My Role

* 서비스 요구사항 분석 및 시스템 설계
* 클라이언트 · 서버 통합 아키텍처 설계
* Node.js, SpringBoot 기반 RESTful API 개발
* MariaDB, InfluxDB, MongoDB 데이터 모델 설계
* Mobile Application 개발
* 관리자 시스템 개발


## 🚀 Technical Highlights

#### 사용자 위치 데이터 수집 시스템 설계·구현

위치 기반 서비스 및 AI 학습 데이터 확보를 위해 사용자 위치 데이터 수집 시스템을 설계

Android(Kotlin), iOS(Swift) 환경에서 백그라운드 위치 수집 기능을 구현하여 애플리케이션이 실행되지 않은 상태에서도 지속적으로 위치 정보를 수집할 수 있도록 구성

초기에는 수집된 위치 데이터를 측정 즉시 서버에 전송하는 방식으로 운영하였으나, 빈번한 네트워크 요청으로 인해 모바일 배터리 소모가 증가하고 사용자 수 증가에 따라 서버 트래픽 부담이 커지는 문제가 발생

이를 개선하기 위해 일정 시간 동안 수집한 위치 데이터를 묶어서 전송하는 Bulk 전송 방식을 적용하여 네트워크 요청 횟수를 최소화

위치 데이터의 연속성과 정확도를 유지하면서도 서버 트래픽을 약 70% 절감하고 모바일 애플리케이션의 배터리 소모량을 약 20% 감소

<br>

#### 레거시 시스템 구조 개선

기존 레거시 코드의 높은 결합도와 유지보수 문제를 해결하기 위해
MVC 패턴 기반 구조로 리팩토링 수행

관심사 분리를 통해 코드 가독성 및 유지보수성을 향상하고
기능 확장 시 개발 효율성을 개선

<br>

#### IoT 기기 연동 시스템 재설계

기존 시스템은 IoT 기기의 시리얼 번호만으로 사용자 계정과 기기를 연동하는 구조로 설계되어 있어, 시리얼 번호가 노출될 경우 제3자가 임의로 기기를 등록하거나 기존 사용자와의 연결을 탈취할 수 있는 보안 위험이 존재

이를 개선하기 위해 기기에서 일회성 인증 코드(난수)를 생성하는 연동 방식을 설계 및 구현

사용자는 기기에 표시된 인증 코드를 입력해야만 연동이 가능하도록 변경하였으며, 새로운 인증 코드가 발급될 경우 기존 연동 정보를 모두 무효화하여 불필요한 접근을 차단

이를 통해 단순 식별자 기반 인증 구조를 일회성 인증 기반 구조로 개선하여 무단 기기 등록 및 계정 탈취 가능성을 방지하고 시스템 보안성을 강화

<br>

## 📈 Results

* 모바일 애플리케이션 (Android / iOS) 서비스 구축 및 앱 마켓 배포
* 개발 편의성 및 유지보수성 확보를 위해 크로스 플랫폼(Flutter)으로 포팅
* 백그라운드 사용자 위치 데이터 수집 시스템 구축
* 시스템 보안성 및 유지보수성 향상

