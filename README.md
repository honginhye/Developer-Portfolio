# Developer-Portfolio 포트폴리오
홍인혜 포트폴리오

<p align="center">
  <a href="https://github.com/honginhye/Developer-Portfolio/blob/main/%ED%99%8D%EC%9D%B8%ED%98%9C%20%ED%8F%AC%ED%8A%B8%ED%8F%B4%EB%A6%AC%EC%98%A4%20%20(1).pdf" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-View%20PDF-blue?style=for-the-badge&logo=adobeacrobatreader&logoColor=white" alt="Portfolio Badge" />
  </a>
</p>


</a>
</p>
---
## 소개
- **이름:** 홍인혜 (Hong In-hye)
- **포지션:** Backend Developer(Full-stack Developer)
- **연락처:** hih3776@naver.com
---
## Core Tech Stacks
- **Language & Framework:** Java, Spring Boot, Spring MVC
- **Data & ORM:** Oracle DB, MyBatis, JPA
- **DevOps & Infra:** AWS (EC2), Docker, Jenkins, GitHub Actions, Ubuntu
- **Cooperation:** Git, GitHub, Notion
---
## 프로젝트 요약
### 1. 호텔 통합 예약 서비스 및 운영 관리 시스템
- 담당기능       - 개발환경 구축
                - Database 설계 및 구축
                - 다이닝 회원 및 비회원 예약, 예약 조회 기능 구현
                - 다이닝 관리자 예약 현황 조회 및 대시보드 구현
                - 다이닝 관리자 운영 관리 기능 구현
                - 다이닝 관리자 매장 정보 수정 관리 기능 구현
                - 다이닝 수익 관리 기능 및 수익 대시보드 구현
### 2. 안경 쇼핑몰 운영 시스템
- 담당기능      - 개발환경 구축 및 상품 관련 전체 기능 담당
               - 상품 등록, 수정, 삭제(CRUD) 기능 구현
               - 상품 찜하기 및 장바구니 기능 구현
               - 상품 구매 흐름에 따른 구매 파이프라인 구축
               - 상품 구매 및 수량 트랜잭션 관리 
               - 상품 구매 알림 기능 구현
               - 상품 구매 결제 및 내역 확인 기능 구현

## 핵심 트러블슈팅 및 성과 요약
### 1. 운영 서버 배포 자동화 및 환경 최적화
- **문제:** 배포 자동화 중 빌드 진입점 미인식, DB 스크립트 불일치 및 런타임 정적 리소스 경로 참조 오류 발생
- **해결:** `build.gradle`에 `mainClass` 명시, 운영 DB 맞춤형 SQL 수정, `WebMvcConfigurer` 기반
`classpath` 정밀 매핑 적용
- **성과:** 로컬-운영 간 환경 격차 해결 및 배포 파이프라인의 전반적인 구동 안정성 확보
### 2. 매출/재고 정합성 관리를 위한 Soft Delete 도입
- **문제:** 품절·판매 종료 상품 삭제 시 과거 주문 내역 매출 통계 왜곡 및 누적 재고 이력 유실 위험 확인
- **해결:** 물리적 삭제 대신 테이블 내 상태값 컬럼(`pstatus`)을 추가하여 판매 중(1)/중지(0) 구조로 로직 전
환
- **성과:** 유실 리스크 예방 및 비즈니스 데이터의 완벽한 무결성·정합성 보존
