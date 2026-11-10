# 최창민(WOODY) · QA Engineer

> 라이브 커머스 · 글로벌 다국어(L10n) · AI 에듀테크 도메인의 QA
> 테스트를 설계하고, 반복되는 확인은 Playwright · Appium · pytest로 자동화합니다.
> LLM은 QA 도구를 만드는 데 쓰고, 결과를 믿어도 되는지는 근거로 따로 확인합니다.

**이 페이지에서 볼 수 있는 것**
- 웹 E2E 자동화 2개 — 외부 사이트 대상([playwright-e2e](https://github.com/changmindev/playwright-e2e))과 내 저장소의 앱 대상([loyalhub-e2e](https://github.com/changmindev/loyalhub-e2e))을 나눈 이유
- 이슈 트래커와 연결한 QA 도구 — 릴리스 준비도 판정 · 테스트케이스 생성 · 자동화 결과 비교([redmine-qa-platform](https://github.com/changmindev/redmine-qa-platform))
- 결함 기록 — AI 빌더로 세운 데모 앱에서 찾은 결함 24건과 처리 근거([loyalhub](https://github.com/changmindev/loyalhub))
- 모바일 자동화 — Android 앱 Appium Excel-Driven 프레임워크, 데이터를 익명화한 공개용 데모([auto-test.demo](https://github.com/changmindev/auto-test.demo))

---

## Experience

### 위버스브레인 · QA Engineer (2026.02 ~ 현재)
> 회사 코드는 비공개입니다. 아이디어 일부는 [redmine-qa-platform](https://github.com/changmindev/redmine-qa-platform)에 새로 구현했습니다.

**사내 QA 허브** · 단독 기획·설계, Claude Code로 개발
- **사내망 서버 직접 운영(관리자)** — 허용 대역에서만 팀원이 접속하도록 열고, 역할별 권한·팀원 계정·매일 자동 백업 관리. 팀원 개선 요청도 기능으로 반영
- **AI가 만든 TC 자동 검사** — 근거 누락·중복, '전과 같다'처럼 판정 기준을 미룬 표현을 걸러냄. 자동화 범위는 테스트 코드를 실행하지 않고 전체·부분·미구현으로 분류
- **중복 결함 등록 방지** — 사람이 2단계로 확인한 결함만 올림. 전송 결과가 불확실하면 재전송 대신 이슈 트래커 재조회
- **자동화 실행 통제** — 기본 꺼짐, 실행 내용에 묶인 1회용 확인 키, 자동화 코드에 비밀값 미전달, 실계정 데이터를 바꾸는 테스트는 확인 문구 필수
- **데이터 안전 우선 변경** — AI 설계안 2개를 실측 비교해 서버 기록만 SQLite로 이관, 전후 응답 대조. 모든 변경은 확인용 허브에서 코드 리뷰·전체 테스트 후 반영
- **집계 규칙 통일** — 현황·판정·보고서를 같은 규칙으로 계산하고, 지난 실행 대비 새 실패·불안정 TC를 따로 표시

**회귀 자동화** · Claude Code로 개발
- **허위 PASS 적발** — 이어받은 자동화가 목록 화면 값만 읽고 통과시키던 판정을 찾아 로직 재작성
- **TC 1건 = 스크립트 1개** — 뇌새김 앱·웹 TC를 새 코드로 옮겨 회귀 실행(Android Appium·WebdriverIO, 웹 Playwright)
- **iOS 실기기 실행 추가** — MAX AI 실행 대상을 Android·iOS로 나눔(Xcode 개발자 서명·WebDriverAgent)
- **전화영어 웹 회귀 평일 CI 운영** — 화면 값과 API 응답 대조, 오류 응답 주입 후 복구 확인. 실패 분석 AI는 읽기 도구만 쓰고 판정은 못 바꿈

**제품 QA**
- **SSO 전환 QA 단독, 운영 배포까지 완료** — 전환 경로를 4개 축으로 나눠 TC 설계·수행, 개발 완료 / 테스트 완료 / 릴리즈 가능 판정 기준 명세
- **STT·TTS 검증 기준 수립** — 사용자 발화 인식과 튜터 음성 출력, 영어·일본어·프랑스어·베트남어 등 다국어 학습 콘텐츠

### 와이즈스톤 (Shoplive Korea 파견) · QA Engineer (2023.08 ~ 2025.12)
- **QA 프로세스 0→1** — 검증 기준이 없던 B2B 라이브 커머스 SaaS에 테스트 계획·결함 등급·Jira 결함 처리 흐름 도입, 크리티컬 결함은 릴리즈 차단
- **SDK 연동 QA** — 특정 OS에서 Studio가 동작하지 않는 결함을 찾아 고객사 장애 사전 차단. 무신사·29CM 등 고객사 SDK 버전 회귀, iOS·Android 대조
- **버즈빌 SDK 연동 QA** — 라이브 시청 체류 시간 구간별 보상 차이, 보상 중복·누락, 네트워크 유실 시 동작 검증
- **실시간 스트리밍** — 복구 실패·방송 끊김·싱크 지연을 배포 전 차단. 단절·복구, 시청 중 Wi-Fi·LTE 전환을 Charles Proxy·Link Conditioner로 재현
- **AI Clip 성공률 85% → 99%** — 생성 실패 원인을 유형별로 규명해 하나씩 차단
- **지표·글로벌** — 클릭 1회가 2회로 잡히던 대시보드 중복 집계, eBay Auction 다국어 시트 대조로 원화 표시 불일치 발견

---

## Tech Stack

**QA / 자동화**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![Appium](https://img.shields.io/badge/Appium-662D91?style=flat-square&logo=appium&logoColor=white)
![ADB](https://img.shields.io/badge/ADB-3DDC84?style=flat-square&logo=android&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Keycloak](https://img.shields.io/badge/Keycloak-4D4D4D?style=flat-square&logo=keycloak&logoColor=white)
![Anthropic](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**사이드 프로젝트 활용 기술**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)

---

## Projects

### [playwright-e2e](https://github.com/changmindev/playwright-e2e) · [loyalhub-e2e](https://github.com/changmindev/loyalhub-e2e)
> 웹 E2E 자동화 — **대상을 고칠 권한이 있느냐 없느냐**로 저장소를 나눴습니다

```
playwright-e2e   97 tests — 90 passed, 7 xfailed    (외부 사이트 대상)
loyalhub-e2e     27 tests — 27 passed               (내 저장소의 앱 대상)
```

- **`playwright-e2e`** — 통제할 수 없는 외부 사이트(Swag Labs · 네이버 날씨)가 대상입니다. `xfailed` 7건은 실패를 덮은 게 아니라 **결함이 심어진 계정으로 같은 검증을 한 번 더 돌려, 자동화가 제품 결함을 잡아내는지 확인한 결과**입니다
- **`loyalhub-e2e`** — 대상 앱도 제 저장소(AI 빌더로 세운 화면을 직접 정비)라서, 테스트가 요구하는 것을 제품에 반영할 수 있습니다. 셀렉터를 추측하지 않고 계약(`data-testid` · `aria-pressed`)으로 고정했습니다
- **CI 판단이 정반대입니다** — 외부 사이트는 해외 IP 러너에서 돌리면 코드가 멀쩡해도 빨간불이 뜨므로 **구조 검사만** 하고, 내 제품은 시드가 결정적이라 **전부 실행 + 매일 스케줄**로 돌립니다
- 대상 사이트 개편으로 깨진 3건을 복구 — `wait_for_url` 만으로는 부족했습니다. 주소가 화면보다 먼저 바뀌어서, 그 화면에만 있는 요소가 붙었는지까지 확인하도록 고쳤습니다
- **Stack** : Playwright (Python · TypeScript) · pytest · Page Object Model · GitHub Actions

---

### [Redmine QA 플랫폼](https://github.com/changmindev/redmine-qa-platform)
> 이슈 트래커 연동 QA 자동화 — 릴리스 준비도 판정 · AI 기반 테스트케이스 생성

- 근거(evidence) 기반 신뢰도 판정 — 생성된 테스트케이스마다 원문 근거를 남겨, 사람 검수 없이 실행해도 되는지 시스템이 스스로 판단
- 이슈 → 테스트케이스 → 실행결과 → 결함을 잇는 요구사항 추적 매트릭스(RTM), 우선순위 가중 워크로드 진단
- **자동화 결과 화면** — JUnit XML(Playwright·pytest)을 올리면 지난 실행과 비교해 **새 실패 / 계속 실패 / 고쳐짐 / 사라진 TC**로 나누고, 통과↔실패가 자꾸 뒤바뀌는 **불안정 TC**를 따로 모읍니다. 실패율이 아니라 뒤바뀐 횟수로 세는 이유는 [DECISIONS.md 10장](https://github.com/changmindev/redmine-qa-platform/blob/main/DECISIONS.md#10-자동화-결과와-결함-등록-2단계)에 있습니다
- **결함 등록 2단계** — 미리보기에서 사람이 확인해야만 Redmine에 등록됩니다. 확인은 화면이 아니라 서버가 강제해서, API를 바로 부르는 스크립트·AI 도구도 같은 단계를 밟습니다
- pytest 197케이스(외부 호출은 전부 mock). URL 읽기는 Figma만 허용(SSRF 차단), 엑셀 내보내기의 수식 주입(Formula Injection) 차단
- **Stack** : Python · Flask · Anthropic Claude SDK/CLI · pytest

---

### [모바일 앱 자동화 프레임워크](https://github.com/changmindev/auto-test.demo)
> Android 앱 대상 Appium(UiAutomator2) 기반 Excel-Driven 자동화 프레임워크
> — 앱 정보·테스트케이스 데이터를 전부 익명화한 공개용 데모입니다.

- Excel로 테스트케이스 관리, HTML 리포트 + JSON + 스크린샷 자동 생성
- `actions / core / utils` 단방향 의존 구조로 정리 — 새 액션 추가 시 수정 지점을 한 곳으로 고정
- **Stack** : Python · Appium · openpyxl · ADB

---

### [LoyalHub — 소상공인 고객 관리 데모](https://github.com/changmindev/loyalhub)
> 🔗 **[loyalhub-demo.vercel.app](https://loyalhub-demo.vercel.app)** — 환경변수 없이 바로 뜹니다
> 초기 화면은 AI 빌더로 세우고, **결함을 찾아 고치고 자동화 가능한 상태로 정비하는 작업은 직접** 했습니다.

- **결함 24건 발견 · 22건 수정** — 재현 절차·기대/실제·원인·처리를 [DEFECTS.md](https://github.com/changmindev/loyalhub/blob/main/docs/DEFECTS.md)에 기록. 나머지 2건(부분 대응 1 · 미수정 1)은 **왜 거기서 멈췄는지**를 남겼습니다
- 그중 7건은 **1차 수정을 배포본에서 직접 조작해 확인하다 나왔습니다** — 로컬 `lint · test · build`가 전부 초록인 상태였습니다. import가 빠진 화면이 배포까지 간 것(D-22)은 셋 다 타입을 검사하지 않아서였고, CI에 `typecheck`를 넣어 같은 종류를 막았습니다
- **보안 점검** — 개발 서버가 모든 네트워크 인터페이스에 열려 있던 설정, 배포본의 보안 헤더 부재를 잡았습니다. `npm audit` 잔여분은 **지금 고치지 않는 근거**까지 [SECURITY.md](https://github.com/changmindev/loyalhub/blob/main/docs/SECURITY.md)에 적었습니다
- **문자·알림톡 발송은 범위 밖입니다** — 건당 비용과 발신번호 사전등록이 필요합니다. 데모는 네트워크 요청 자체를 만들지 않아 실수로 나갈 경로가 없습니다
- **Stack** : React · TypeScript · Tailwind CSS · Supabase · Vite · Vitest · GitHub Actions

---
