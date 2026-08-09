# 안녕하세요, 최창민(WOODY)입니다.

> QA + LLM을 활용해 아이디어를 서비스로 구현하는 QA Engineer
> Live Commerce · Global 다국어 QA · AI EduTech 도메인 경험

---

## Experience

### 위버스브레인 · QA Engineer (2026.02 ~ 현재)
- **SSO 통합인증(Keycloak) 전환 프로젝트 QA 단독 수행** — 기능·비기능(보안·성능) 테스트 설계·수행, 소셜 로그인(네이버·카카오·애플) 조합별 회귀 테스트, 결함 발견·재현 시나리오 작성
- MAX AI·스피킹맥스 STT 음성 인식·AI 응답 품질 검증 체계 수립, 뇌새김 실기기(갤럭시탭·LG탭) 기준 학습 플로우 E2E 검증
- Claude SDK/MCP 기반 QA 지원 도구 자체 개발, 기존 Appium 자동화 스크립트 고도화

### 와이즈스톤(Shoplive Korea 파견) · QA Engineer (2023.08 ~ 2025.12)
- 라이브 스트리밍 특화 QA 기준 수립(지연·화질 저하·채팅 동기화), Charles Proxy 네트워크 시뮬레이션으로 엣지 결함 발견
- AI Clip 기능 실패 유형 분류·재현 시나리오 문서화, eBay Auction 글로벌 서비스 다국어(L10n) 검증
- Postman API 테스트 컬렉션 구축, Jira·Confluence 기반 QA 프로세스 설계·운영, Shift-Left Testing 참여

---

## Tech Stack

**QA / 자동화**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Appium](https://img.shields.io/badge/Appium-662D91?style=flat-square&logo=appium&logoColor=white)
![ADB](https://img.shields.io/badge/ADB-3DDC84?style=flat-square&logo=android&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Keycloak](https://img.shields.io/badge/Keycloak-4D4D4D?style=flat-square&logo=keycloak&logoColor=white)
![Anthropic](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white)

**사이드 프로젝트 활용 기술**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)

---

## Projects

### [Redmine QA 플랫폼](https://github.com/changmindev/redmine-qa-platform)
> 이슈 트래커 연동 QA 자동화 — 릴리스 준비도 판정 · AI 기반 테스트케이스 생성

- 근거(evidence) 기반 신뢰도 판정 — 생성된 테스트케이스마다 원문 근거를 남겨, 사람 검수 없이 실행해도 되는지 시스템이 스스로 판단
- 이슈 → 테스트케이스 → 실행결과 → 결함을 잇는 요구사항 추적 매트릭스(RTM), 우선순위 가중 워크로드 진단
- pytest 172케이스, SSRF·수식 주입(Formula Injection) 방어 등 보안까지 고려한 설계
- **Stack** : Python · Flask · Anthropic Claude SDK/CLI · pytest

---

### [모바일 앱 자동화 프레임워크](https://github.com/changmindev/auto-test.demo)
> Android 앱 대상 Appium(UiAutomator2) 기반 Excel-Driven 자동화 프레임워크
> — 재직 중 운영·고도화한 자동화 구조를 공개용 데모로 재구성했습니다 (앱 정보·TC 데이터는 전부 익명화).

- Excel로 테스트케이스 관리, HTML 리포트 + JSON + 스크린샷 자동 생성
- `actions / core / utils` 단방향 의존 구조로 정리 — 새 액션 추가 시 수정 지점을 한 곳으로 고정
- **Stack** : Python · Appium · openpyxl · ADB

---

### [LoyalHub — 소상공인 고객관리 앱](https://github.com/changmindev/sideproject)
> 단골 고객 관리 + 쿠폰 SMS 발송 웹 서비스

- LLM을 활용해 기획부터 배포까지 직접 구축 — 초기 화면은 AI 빌더로 빠르게 세우고, 데이터 모델·분석 로직·품질 검증은 직접 설계
- 이탈 위험도 판정 등 분석 함수에 **경계값·예외 입력·설정값 폴백 경로**를 나눠 Vitest 단위 테스트 설계
- **GitHub Actions로 lint · test · build를 push/PR마다 자동 실행**하도록 CI 구성
- **Stack** : React · TypeScript · Tailwind CSS · Supabase · Vite · Vitest · GitHub Actions

---
