## 👋 안녕하세요!

🧑‍💻 **Backend Developer**를 꿈꾸는 개발자입니다.

- 🎓 **SSAFY 13기 수료** (서울 3반)
- 🔭 최근 **backend-pass** - 부하 상황에서의 서버 동작을 측정하고 개선하는 개인 프로젝트
- 💡 개선을 주장하기 전에 측정하는 것을 원칙으로 삼습니다
- 🌱 Kafka, OpenSearch, LangChain 학습 중
- 📫 Email: 01040307z@gmail.com

---

### 🛠️ Main Tech Stack

<div>
  <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=Java&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/Spring Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" height="25"/>
</div>

### ☁️ Infra & DevOps

<div>
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white" height="25"/>
</div>

### 📊 Data & AI

<div>
  <img src="https://img.shields.io/badge/Apache Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/OpenSearch-005EB8?style=flat-square&logo=opensearch&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" height="25"/>
</div>

### 📈 Testing & Monitoring

<div>
  <img src="https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white" height="25"/>
</div>

### 🔧 Tools

<div>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/GitLab-FC6D26?style=flat-square&logo=gitlab&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/Notion-000000?style=flat-square&logo=notion&logoColor=white" height="25"/>
  <img src="https://img.shields.io/badge/IntelliJ IDEA-000000?style=flat-square&logo=intellijidea&logoColor=white" height="25"/>
</div>

---

### 🚀 Featured Projects

#### ⚡ backend-pass - 백엔드 성능 최적화 실습
> 개인 프로젝트 | 2026.01 - 2026.03

부하 상황에서만 드러나는 성능 병목을 코드로 재현하고, 개선 전후를 측정 조건과 함께 기록한 프로젝트

- **역할**: 단독 개발
- **다룬 문제**
  - 동시성 제어: 낙관적 · 비관적 · Named Lock · Redis 분산 락 4가지 구현 및 k6 비교
  - Redis 캐시 장애 패턴: Cache Penetration, Avalanche, Hot Key
  - JPA N+1: Fetch Join · @EntityGraph · @BatchSize 3가지 비교
  - 통계 쿼리 역정규화, Bulk Insert 배치 최적화
- **측정 결과** (모두 k6 + Prometheus로 계측)
  - 통계 조회 p95 59,989ms → 99ms (50~100 VU ramp, 8분, 100만 건)
  - Bulk Insert p95 2,475ms → 115ms (1,440건)
  - Hot Key 캐시 미스 시 DB 조회 ~300회 → 2회 (300 VU 동시 요청)
- **기술 스택**: Java 17, Spring Boot 3.1.5, JPA, MySQL, Redis, k6, Prometheus, Grafana, Docker

#### 🔍 LogLens - AI 기반 로그 분석 모니터링 시스템
> SSAFY 13기 자율 프로젝트 (우수상) | 2025.10 - 2025.11 | 6인 팀

분산된 로그를 통합 수집하고 LLM으로 오류 원인을 분석하는 관측 플랫폼

- **역할**: Backend Developer (로그 적재 파이프라인, 챗봇 에이전트, 알림 도메인, 배포)
- **핵심 작업**
  - 임베딩 유사도 기반 조건 검사로 중복 LLM 호출 제거 (OpenSearch KNN, 임계값 0.92)
  - LangChain ReAct Agent 커스텀 도구 **38개** 구현
  - Jenkins Blue-Green 배포 파이프라인 (ALB 타깃 그룹 전환, 헬스 체크 실패 시 롤백)
  - 에러 알림 중복 발송 문제를 5분 윈도우와 프로젝트별 트랜잭션 격리로 해결
- **기술 스택**: Spring Boot, FastAPI, Kafka, Logstash, OpenSearch, LangChain, Jenkins, Prometheus, Grafana

#### 💰 OSM - 청소년 금융 교육 플랫폼
> SSAFY 13기 특화 프로젝트 (최우수상) | 2025.08 - 2025.10 | 6인 팀

퀴즈, 상품 거래, 마니또 활동을 통한 게이미피케이션 기반 금융 교육 서비스

- **역할**: Backend Developer (14개 도메인), CI/CD 파이프라인 구축, 모니터링 시스템 구축
- **핵심 작업**
  - Blue-Green 무중단 배포 구현 (헬스 체크 통과 후 트래픽 전환, 즉시 롤백)
  - SSE 기반 실시간 알림 시스템 구현
  - 14개 도메인 설계
- **기술 스택**: Spring Boot, Spring Security, JPA, MySQL, Redis, FastAPI, Docker, Nginx, Jenkins, Prometheus, Grafana

#### 🍯 꿀띱 (KKULDDIP) - 마감 할인 중개 플랫폼
> SSAFY 13기 공통 프로젝트 | 2025.07 - 2025.08 | 6인 팀

마감 임박 음식을 할인 판매하는 플랫폼

- **역할**: Backend Developer (결제 도메인, 인증, 가게 조회)
- **핵심 작업**
  - Toss Payments 연동에 앞서 주문·결제·외부 API의 처리 순서와 검증 기준을 문서로 정리해 팀 합의
  - 결제 도메인 모델 구현: 주문번호 UNIQUE 제약, 상태 검증으로 이중 확정 차단
  - 거리 기반 무한 스크롤의 중복·누락 문제를 (거리, store_id) 복합 커서로 해결
  - OAuth2 인증과 JWT 발급
- **기술 스택**: Spring Boot, JPA, MySQL, Redis, Toss Payments, Docker

---

### 📊 Statistics

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=goni02)](https://solved.ac/goni02)
![mazandi profile](http://mazandi.herokuapp.com/api?handle=goni02&theme=warm)

---

### 📫 Contact

<div align="center">
  <a href="mailto:01040307z@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
  <a href="https://mirage-bird-372.notion.site/32be1b00e2b5804c9ab2e63697fa63d2">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=notion&logoColor=white"/>
  </a>
  <a href="https://github.com/Olga201207">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
</div>
