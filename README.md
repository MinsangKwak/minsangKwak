# Minsang Kwak · 곽민상

**웹 퍼블리셔 / 웹 프론트엔드 개발자 · Accessible UI & Web Products**

사용하기 쉬운 화면, 이어가기 좋은 코드를 만듭니다.

금융결제원과 NICE평가정보에서 인증·결제·금융 조회처럼 예외가 많은 화면을 공통 UI와 접근성 있는 구조로 정리해 왔습니다. 지금은 그 경험으로 직접 서비스를 만들고 운영합니다. 기획부터 배포, 사용자 제보 반영까지 혼자 맡고 있습니다.

**[📂 포트폴리오 보기](https://kwakminsang.notion.site/overview)** · [Blog](https://minsangkwak.github.io/) · [Email](mailto:kmsdevwork@gmail.com)

### 🔎 한눈에 보기

| | |
| --- | --- |
| **실무** | 금융결제원 UX/UI팀 · NICE평가정보 플랫폼사업실 · 프리랜서(Next.js) |
| **규모** | 어카운트인포 PC 웹 141개 화면, 국세 납부 POS 21개 화면 신규 구축 · 금융결제원 대외 서비스 22개 운영 |
| **강점** | 공통 컴포넌트 설계 · 웹 접근성(KWCAG·ARIA·포커스 관리) · 레거시 jQuery → ES6 구조 개선 |
| **운영 중인 서비스** | moncamp · subway-midpoint · 대한민국 조간 |

### 📌 Projects

#### [moncamp](https://moncamp.kr/) — Pokémon GO 플레이 판단 도우미 · 운영 중

"무엇을 잡고, 어떤 포켓몬을 먼저 키울지" 정하도록 돕는 서비스입니다. 작은 정보 페이지로 시작했습니다. 지금은 사용자 제보와 이용 데이터를 반영하는 운영 서비스입니다.

- **구조 전환** — 단일 HTML → React·TypeScript → Next.js 15. 첫 판(2026-09-01)부터 37일 동안 281판을 배포하며 다섯 차례 바꿨습니다
- **서버·데이터** — Fastify 기반 Google OAuth·권한 서버, Neon Postgres, Python 데이터 파이프라인
- **품질·운영** — 화면·명암비·API 자동 검사, 매일 운영 스모크, `dev → main → deploy` 배포 분리. 개인정보는 IP 미저장, 통계 거부 시 미전송

[Live](https://moncamp.kr/) · [Source](https://github.com/MinsangKwak/pogo-rank) · [Docs](https://github.com/MinsangKwak/pogo-rank/tree/main/docs)

#### [대한민국 조간](https://minsangkwak.github.io/korea-jogan/) — 출처가 붙은 숫자로 만드는 아침 신문 · 운영 중

같은 날 코스피 기사 두 개가 지난주 하락률을 14.46%와 11.21%로 썼습니다. 둘 다 맞았습니다. 출발점만 달랐는데, 어느 기사에도 그 출발점은 없었습니다. 그래서 숫자마다 출처 기관·원문 링크·기준일·신뢰도를 붙여 매일 00시에 한 호씩 냅니다.

- **AI는 초안까지만** — AI 에이전트가 조사해 `draft`를 쓰고, 제가 원문과 대조해 승인한 호만 배포 검사를 통과합니다
- **출처 없는 숫자는 배포 차단** — 출처·`https` 링크가 빠지면 Python 검사 스크립트가 CI에서 멈춥니다. 확인 못 한 값은 '미확인'으로 적습니다
- **프레임워크 없는 화면** — Vanilla JavaScript(`'use strict'`)와 디자인 토큰, 두 테마 4.5:1 명암비, 44px 터치 영역, 서랍 포커스 가두기·복귀

[Live](https://minsangkwak.github.io/korea-jogan/) · [Source](https://github.com/MinsangKwak/korea-jogan) · [Docs](https://github.com/MinsangKwak/korea-jogan/tree/main/docs/portfolio)

#### [subway-midpoint](https://minsangkwak.github.io/subway-midpoint/) — 지하철 중간역 추천

여러 출발역에서 **가장 오래 걸리는 사람의 시간**을 줄이는 중간역을 찾습니다. 지도 한가운데 역이 공평한 자리는 아니라서요.

- **알고리즘** — 이진 최소 힙 다익스트라, 환승역 다중 출발점, 최대 예상 이동시간 최소화와 동점 처리
- **데이터** — OpenStreetMap·Overpass API로 1~9호선 생성, 분기·순환을 구간 단위로 모델링
- **UX·테스트** — 키보드 검색·ARIA·한글 IME 처리, 지도 SDK 오류와 계산 분리, Vitest 회귀 테스트와 CI

[Live](https://minsangkwak.github.io/subway-midpoint/) · [Source](https://github.com/MinsangKwak/subway-midpoint) · [Architecture](https://github.com/MinsangKwak/subway-midpoint/blob/main/docs/ARCHITECTURE.md)

<sub>소요시간은 거리·환승 비용에 따른 추정값이며 실제 시각표를 반영하지 않습니다. 세 프로젝트 모두 AI 코딩 도구(Claude Code)와 함께 구현했고, 범위·원칙·출시 여부는 직접 정했습니다.</sub>

### 💼 Experience

🏦 **금융결제원 · UX/UI팀**
국세 납부 POS(21개 화면) · 은행 공동망 본인확인서비스 · 어카운트인포 PC 웹(141개 화면) 신규 구축. 홈페이지와 대외 서비스 22개의 화면 수정, 중복 코드 정리, 웹폰트·이미지 최적화

🔐 **NICE평가정보 · 플랫폼사업실** (2023.05 ~ 2025.05)
통신 3사·MVNO 인증 흐름 공통화, jQuery → ES6 구조 전환, 웹폰트 정리로 LCP 약 3초 → 1초대(Lighthouse 기록 기준). 올리미·카드사 제휴 서비스 개발·운영

📚 **이지 회계사·세무 아카데미 · 프리랜서** (2025.03 ~ 2025.06)
Next.js·React·TypeScript·Sass로 반응형 교육 웹서비스 UI 구축

<sub>어카운트인포는 UI 프로토타입·퍼블리싱 산출물 검토 완료 단계이며, 개발·배포는 2027.07 예정입니다.</sub>

### 🛠 Tech Stacks

#### Frontend
<div>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black">
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white">
  <img src="https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white">
</div>

#### UI · Accessibility
<div>
  <img src="https://img.shields.io/badge/Storybook-FF4785?style=for-the-badge&logo=storybook&logoColor=white">
  <img src="https://img.shields.io/badge/CSS_Modules-000000?style=for-the-badge&logo=cssmodules&logoColor=white">
  <img src="https://img.shields.io/badge/Design_Tokens-555555?style=for-the-badge">
  <img src="https://img.shields.io/badge/KWCAG_·_ARIA-005A9C?style=for-the-badge&logo=w3c&logoColor=white">
</div>

#### Server · Data · Operations
<div>
  <img src="https://img.shields.io/badge/Node.js-5FA04E?style=for-the-badge&logo=nodedotjs&logoColor=white">
  <img src="https://img.shields.io/badge/Fastify-000000?style=for-the-badge&logo=fastify&logoColor=white">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub_Pages-222222?style=for-the-badge&logo=githubpages&logoColor=white">
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white">
  <img src="https://img.shields.io/badge/Cloud_Run-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white">
  <img src="https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white">
  <img src="https://img.shields.io/badge/GA4-E37400?style=for-the-badge&logo=googleanalytics&logoColor=white">
</div>

### 🧭 How I Work

- **사용자 흐름부터** — 화면을 그리기 전에 이동 순서와 오류·예외 상태를 먼저 나눕니다.
- **반복은 공통 구조로** — 같은 버튼과 모달을 복사하지 않고 컴포넌트와 상태 규칙으로 만듭니다.
- **접근성은 처음부터** — 키보드, 포커스, ARIA, 명암비를 나중 작업으로 미루지 않습니다.
- **출시 이후까지** — 수정 범위, 리소스 용량, QA와 배포 흐름까지 보고 구조를 정합니다.

### 📊 GitHub Stats

[![MinsangKwak's GitHub stats](https://github-stats-extended.vercel.app/api?username=MinsangKwak&show_icons=true&theme=transparent)](https://github.com/MinsangKwak)
[![Top Langs](https://github-stats-extended.vercel.app/api/top-langs?username=MinsangKwak&layout=compact&theme=transparent&hide=html,css,scss)](https://github.com/MinsangKwak)

[![GitHub Streak](https://streak-stats.demolab.com/?user=MinsangKwak&theme=transparent)](https://github.com/MinsangKwak)

### 🐾 GitAnimals

<a href="https://www.gitanimals.org/">
  <img src="https://render.gitanimals.org/farms/MinsangKwak" width="600" alt="GitAnimals farm of MinsangKwak"/>
</a>

---

화면 수, 구현 방식, 프로젝트별 상세 기록은 **[Portfolio](https://kwakminsang.notion.site/overview)** 에 있습니다.
