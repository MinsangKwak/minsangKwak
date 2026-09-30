# Minsang Kwak · 곽민상

**Frontend Developer · Accessible UI & Web Products**

### 👋 Introduction

- 사용자가 이해하기 쉬운 화면과, 개발자가 이어가기 쉬운 코드를 만듭니다.
- 금융 서비스에서 쌓은 UI·접근성 경험을 바탕으로 React·TypeScript 프로젝트를 만들고 운영합니다.
- 지금은 **moncamp**를 운영하고, **subway-midpoint**에서 데이터 모델과 경로 탐색을 다듬고 있습니다.

```
사용자 흐름을 먼저, 접근성은 처음부터.
```

### 📮 Contact & Channel

- **Portfolio: [kwakminsang.notion.site/overview](https://kwakminsang.notion.site/overview)**
- **Blog: [minsangkwak.github.io](https://minsangkwak.github.io/)**
- **Email: [kmsdevwork@gmail.com](mailto:kmsdevwork@gmail.com)**

### 🛠 Tech Stacks

#### Main Stack
<div>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black">
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white">
</div>

#### UI · Accessibility
<div>
  <img src="https://img.shields.io/badge/Storybook-FF4785?style=for-the-badge&logo=storybook&logoColor=white">
  <img src="https://img.shields.io/badge/CSS_Modules-000000?style=for-the-badge&logo=cssmodules&logoColor=white">
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
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white">
  <img src="https://img.shields.io/badge/Cloud_Run-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white">
</div>

### 📌 Projects

#### [moncamp](https://moncamp.kr/) — Pokémon GO 판단 도우미 (운영 중)

작은 정보 페이지에서 시작해 도감·랭킹·일정·덱 도구와 계정 기능을 갖춘 운영 서비스로 확장했습니다. 기획부터 UX/UI, 프론트엔드, 인증 서버, 데이터와 운영까지 직접 다룹니다.

- **Architecture** — HTML·Vanilla JavaScript → React·TypeScript → Next.js로 단계적으로 개선
- **Auth & Data** — Fastify 기반 Google OAuth·권한 관리, Neon Postgres, Python 데이터 파이프라인
- **Quality & Operations** — 디자인 시스템·Storybook, 사용자 제보와 QA, 개발·운영 배포 분리, GA4·운영 통계

[Live](https://moncamp.kr/) · [Source](https://github.com/MinsangKwak/pogo-rank) · [Docs](https://github.com/MinsangKwak/pogo-rank/tree/main/docs)

#### [subway-midpoint](https://minsangkwak.github.io/subway-midpoint/) — 지하철 중간역 추천

여러 출발역에서 가장 오래 이동하는 사람의 부담을 줄이는 중간역을 추천합니다. 노선의 분기·순환·환승을 데이터로 표현하고, 계산 로직을 화면과 분리했습니다.

- **Algorithm** — 이진 최소 힙 다익스트라, 환승역 다중 출발점, 최대 예상 이동시간을 최소화하는 후보 선정
- **Data Pipeline** — OpenStreetMap·Overpass API 기반 1~9호선 데이터 생성, 역 이름 정규화와 환승역 통합
- **UX & Testing** — 키보드 검색·ARIA·한글 IME 처리, 지도 오류와 계산 분리, Vitest 회귀 테스트와 CI

[Live](https://minsangkwak.github.io/subway-midpoint/) · [Source](https://github.com/MinsangKwak/subway-midpoint) · [Architecture](https://github.com/MinsangKwak/subway-midpoint/blob/main/docs/ARCHITECTURE.md)

<sub>소요시간은 거리·환승 비용에 따른 추정값이며 실제 시각표를 반영하지 않습니다.</sub>

### 💼 Experience

🏦 **금융결제원 · UX/UI팀** — 국세 납부 POS 21개 화면, 은행 공동망 본인확인서비스, 어카운트인포 PC 웹 141개 화면 UI 구축과 금융 서비스 운영<br/>
🔐 **NICE평가정보 · 플랫폼사업실** (2023.05 ~ 2025.05) — 통신사 인증 흐름 공통화, ES6 구조 개선, 신용·제휴 서비스 프론트엔드 개발·운영<br/>
📚 **이지 회계사·세무 아카데미 · 프리랜서** (2025.03 ~ 2025.06) — Next.js·React·TypeScript·Sass 기반 반응형 교육 웹서비스 UI 구축<br/>

<sub>어카운트인포는 UI 프로토타입·퍼블리싱 산출물 검토 완료 단계이며, 개발·배포는 2027.07 예정입니다.</sub>

### 🧭 How I Work

- **User flow first** — 이동 순서와 오류·예외 상태를 먼저 정리합니다.
- **Reusable by design** — 반복되는 UI와 상태·입력 규칙을 공통 구조로 만듭니다.
- **Accessibility from the start** — 키보드, 포커스, ARIA와 명암비를 구현 과정에서 확인합니다.
- **Build, ship, improve** — 테스트·배포·사용자 피드백을 다음 개선으로 연결합니다.

### 📊 GitHub Stats

[![trophy](https://github-profile-trophy.vercel.app/?username=MinsangKwak&column=4&no-frame=true)](https://github.com/ryo-ma/github-profile-trophy)

[![MinsangKwak's GitHub stats](https://github-readme-stats.vercel.app/api?username=MinsangKwak&count_private=true&show_icons=true&theme=transparent)](https://github.com/anuraghazra/github-readme-stats)
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=MinsangKwak&layout=compact&theme=transparent&hide=html,css,scss)](https://github.com/anuraghazra/github-readme-stats)

### 🐾 GitAnimals

<a href="https://www.gitanimals.org/">
  <img src="https://render.gitanimals.org/farms/MinsangKwak" width="600" alt="GitAnimals farm of MinsangKwak"/>
</a>

---

자세한 작업 범위와 구현 기록은 [Portfolio](https://kwakminsang.notion.site/overview)에서 확인할 수 있습니다.
