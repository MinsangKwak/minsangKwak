# Minsang Kwak · 곽민상

**UI 개발 · 웹 퍼블리싱 · 프론트엔드 개발**

### 사용하기 쉬운 화면, 이어가기 좋은 코드.

금융 서비스의 복잡한 사용자 흐름을 공통 UI와 접근성 있는 화면으로 정리해 왔습니다.
지금은 React·Next.js·TypeScript로 직접 서비스를 만들고, 사용자 피드백을 받아 고칩니다.

**[📂 포트폴리오](https://kwakminsang.notion.site/overview)** · [Blog](https://minsangkwak.github.io/) · [Email](mailto:minsangwork0821@gmail.com)

| 01 / UI Architecture | 02 / Accessibility | 03 / Build & Operate |
| --- | --- | --- |
| 화면과 상태의 공통 규칙을 설계하고, 바꾸기 쉬운 컴포넌트로 만듭니다. | 키보드·포커스·ARIA를 처음부터 사용자 흐름에 넣습니다. | 구현에서 테스트·배포까지 잇고, 운영하며 다음 개선을 정합니다. |

### 🗺 프로젝트로 보는 경험의 범위

금융 화면을 구현하던 경험에서 시작해 서비스 운영, 자동화, 계산 로직, 서버 이해까지 넓혀 왔습니다.
아래 순서는 시작한 시점이 아니라 **읽으면 좋은 순서**입니다. 서비스 전체를 연결한 moncamp를 먼저 보고, 나머지는 각자 깊게 판 주제로 보시면 됩니다.

| 프로젝트 | 집중한 경험 | 확인할 내용 |
| --- | --- | --- |
| [moncamp](#01-moncamp--서비스-하나를-기획부터-운영까지) | 서비스 전체 설계·구현·운영 | 기획과 디자인 시스템이 화면·API·QA·배포로 이어진 과정 |
| [대한민국 조간](#02-대한민국-조간--매일-반복되는-발행을-자동화하기) | 반복 업무의 자동화 | 자료·초안 → 검사 → 발행·배포, 실패하면 멈추는 기준과 정정 |
| [subway-midpoint](#03-subway-midpoint--공평한-만남을-계산-기준으로-바꾸기) | 문제를 계산 로직으로 구현 | 추천 기준, 노선 모델, 최단경로와 React 상태 관리 |
| [Spring MVC](#04-spring-mvc--화면-밖의-서버-동작-이해하기) | 백엔드 요청·응답 이해 | 전송 방식별 바인딩, 서버 검증과 오류 응답 비교 |

### 💼 Experience

🏦 **금융결제원 · UX/UI팀** (2025.06 ~ 현재)
국세 납부 POS 21개 화면, 은행 공동망 본인확인서비스, 어카운트인포 PC 웹 141개 화면을 새로 구축했습니다. 홈페이지와 대외 서비스 22개의 화면 수정·리팩터링·리소스 최적화도 맡고 있습니다.

🔐 **NICE평가정보 · 플랫폼사업실** (2023.05 ~ 2025.05)
통신 3사·MVNO로 흩어진 인증 흐름을 공통 구조로 묶고, jQuery 의존 코드를 ES6로 옮겼습니다. 웹폰트를 정리해 LCP를 약 3초에서 1초대로 줄였습니다(Lighthouse 기록 기준). 올리미와 카드사 제휴 서비스를 개발·운영했습니다.

📚 **이지 회계사·세무 아카데미 · 프리랜서** (2025.03 ~ 2025.06)
Next.js·React·TypeScript·Sass로 반응형 교육 웹서비스 UI를 구축했습니다.

<sub>어카운트인포는 UI 프로토타입·퍼블리싱 산출물 검토를 마쳤고, 개발·배포는 2027.07 예정입니다.</sub>

### 📌 Projects — 서비스 전체 경험에서 기술별 깊이로

실무에서는 공통 UI와 접근성, 금융 업무의 예외 흐름을 다뤘습니다. 개인 프로젝트에서는 문제와 우선순위를 직접 정하고 구현·검증·운영까지 이었습니다.
프로젝트마다 **붙잡은 질문 → 왜 만들었나 → 어떻게 풀었나 → 무엇으로 확인했나** 순서로 적었습니다.

---

#### 01. moncamp — 서비스 하나를 기획부터 운영까지

> **사용자가 정보를 찾고, 비교하고, 다음 행동을 정하게 하려면 무엇을 이어야 할까?**

**왜 만들었나** — Pokémon GO를 하다 보면 일정, 도감, 배틀 순위를 각각 다른 곳에서 찾아야 했습니다. 정보는 많은데 "그래서 뭘 잡고, 뭘 키우지?"에 답해 주는 곳이 없었습니다. 흩어진 정보를 **보스 탐색 → 후보 비교 → 덱 구성**의 한 흐름으로 묶는 데서 시작했습니다.

**어떻게 풀었나** — 혼자 진행했지만 역할은 나눴습니다. 요구가 바뀌면 디자인·코드·검증 중 어디를 같이 고쳐야 하는지 추적하기 위해서입니다.

- **기획·PM** — 사용자 문제, 우선순위, 사용 흐름, WBS, 실험 공개 범위
- **UX/UI** — 픽셀 필드 디자인 방향을 토큰·공통 컴포넌트·반응형·두 테마 규칙으로 구체화
- **프론트엔드·API** — React·TypeScript → Next.js, 자체 OAuth·권한 API, 공개 정보와 회원 데이터 분리, Neon 이관
- **QA·운영** — 제보 재현 → 수정 → 회귀 검사 → 배포된 화면·API 응답 확인

**무엇으로 확인했나**

| 작업 | 결과 | 근거 |
| --- | --- | --- |
| 공통 스타일 정리 | 대상 CSS 100KB → 67KB, `!important` 48개 → 0개 | [PR #180](https://github.com/MinsangKwak/pogo-rank/pull/180) |
| 이미지 경량화 | 대상 자산 PNG 21MB → WebP 1.4MB | [PR #181](https://github.com/MinsangKwak/pogo-rank/pull/181) |
| React 전환 | 비교한 20개 화면의 글자·구조 차이 0건 | [PR #104](https://github.com/MinsangKwak/pogo-rank/pull/104) |

<sub>수치는 각 작업 당시의 대상에 한정합니다. 서비스 전체 속도나 이용자 증가로 넓혀 말하지 않습니다. 2026.09.01부터 운영 중이며, 2026.10.22 기준 v6.4.4입니다.</sub>

[Live](https://moncamp.kr/) · [Source](https://github.com/MinsangKwak/pogo-rank)

---

#### 02. 대한민국 조간 — 매일 반복되는 발행을 자동화하기

> **매일 자료를 모으고 공개하는 일을 어떤 규칙으로 반복 실행할 수 있을까?**

**왜 만들었나** — 같은 경제 지표라도 집계 기간이나 비교 시점이 다르면 기사마다 숫자가 달라집니다. 같은 날 코스피 기사 두 개가 지난주 하락률을 14.46%와 11.21%로 쓴 적도 있습니다. 둘 다 맞는 계산이었는데, 어느 기사에도 출발점은 없었습니다. 숫자만 요약하면 독자는 결국 원문을 다시 찾아야 합니다. 그래서 **값 옆에 출처·기준일·집계 조건을 붙이는 것**을 서비스의 중심으로 정했습니다.

**어떻게 풀었나** — 매일 하는 일이라 사람 손에만 맡기면 언젠가 빠집니다. 그렇다고 자동으로 다 내보내면 틀린 숫자도 같이 나갑니다. 그래서 먼저 정한 건 **무엇이 갖춰져야 공개하고, 언제 멈출지**였습니다.

- **00시** — 외부 예약 작업이 자료를 조사하고 초안을 씁니다
- **06시** — GitHub Actions가 오늘 호와 공개 조건을 확인하고, 검사를 통과한 호만 배포합니다
- **사람이 원문을 대조한 호**는 '편집자 확인'으로 표시하고, 확인하지 못한 호는 자동 발행으로 구분합니다. 사람 이름을 확인자로 적지 않습니다
- **오늘 호 누락·검사 실패·브랜치 충돌**이면 공개하지 않습니다. 고친 값은 변경 전후와 이유를 정정 기록에 남깁니다

화면은 프레임워크 없이 HTML·CSS·Vanilla JavaScript로 만들었습니다. 디자인 토큰은 JSON 하나에서 CSS로 생성하고, CI가 둘이 어긋나지 않는지 확인합니다. 상승·하락은 색만이 아니라 기호와 글자로도 구분합니다.

**무엇으로 확인했나** — 8개 섹션·17개 시도, Python 테스트 36개 통과. 호별 검색용 HTML·RSS·사이트맵을 같은 발행 목록에서 생성합니다.

<sub>자동 검사는 형식과 일부 운영 조건까지만 봅니다. 원문 사실 확인은 사람의 몫으로 분리했습니다. 2026.10.19 시안 공개, 10.20 첫 승인 호, 10.22 도메인 연결.</sub>

[Live](https://korea-jogan.com/) · [Source](https://github.com/MinsangKwak/korea-jogan)

---

#### 03. subway-midpoint — ‘공평한 만남’을 계산 기준으로 바꾸기

> **다른 역에서 출발할 때, 누구에게도 이동 부담이 쏠리지 않게 하려면?**

**왜 만들었나** — 만날 장소를 정할 때 지도 한가운데만 보면, 분기와 환승이 많은 사람이 늘 손해를 봅니다. 그래서 '공평한 중간'을 **가장 오래 걸리는 사람의 예상 시간이 가장 짧은 역**으로 정의했습니다. 후보 A가 20분·40분, 후보 B가 32분·32분이면 합계는 같아도 B를 먼저 추천합니다.

**어떻게 풀었나**

- **노선 모델** — 역 배열을 그대로 이으면 1호선 분기에서 실제로 붙어 있지 않은 역이 연결됩니다. 역 노드와 운행 구간을 나눠 같은 구간의 이웃만 잇고, 환승은 별도 간선으로 만들었습니다
- **계산** — 이진 최소 힙 다익스트라. 환승역에서 출발하면 모든 노선을 비용 0으로 시작해 첫 환승 비용이 붙지 않게 했습니다. 후보는 최대 예상 시간 → 전체 합계 → 역 이름순으로 정렬합니다
- **화면** — 입력이 바뀌면 이전 결과를 지우고, 한글 조합 중 Enter는 역 선택으로 처리하지 않습니다. 지도 SDK가 실패해도 추천 결과는 볼 수 있습니다

**무엇으로 확인했나** — Vitest 7개 파일·38개 테스트, lint·타입 검사·3가지 경로 빌드. OpenStreetMap에서 1~9호선 404개 역을 다시 생성할 수 있는 데이터 파이프라인.

<sub>이동시간은 평균 속도·환승 5분을 적용한 추정값으로 실제 시각표와 다릅니다. 실제 Kakao 지도 렌더링과 실기기 스크린리더는 검증 범위에 넣지 않았습니다.</sub>

[Live](https://minsangkwak.github.io/subway-midpoint/) · [Source](https://github.com/MinsangKwak/subway-midpoint)

---

#### 04. Spring MVC — 화면 밖의 서버 동작 이해하기

> **프론트엔드가 보낸 값은 서버에서 어떻게 읽히고, 왜 오류로 돌아올까?**

**왜 만들었나** — 화면에서 API를 부르는 쪽에만 있다 보니, 같은 값도 경로·쿼리·폼·JSON 중 무엇으로 보내느냐에 따라 서버가 읽는 방법이 다르다는 걸 감으로만 알고 있었습니다. 2023년에 쓴 Spring MVC 기초 예제를 꺼내, 요청부터 응답까지를 **한 화면에서 비교하는 실습**으로 다시 만들었습니다.

**어떻게 풀었나**

- **백엔드** — 요청 바인딩 6종, HTTP 메서드 4종, `@Valid` 입력 검증. 오류 응답은 `code`·`message`·`errors`로 통일했습니다
- **프론트엔드** — 상태 코드와 응답 본문을 그대로 보여 주고, 필드 오류를 입력칸에 연결했습니다. 전송 중 중복 요청은 막고, 시간 초과 뒤에는 다시 요청할 수 있습니다
- **기존 예제에서 바꾼 점** — 콘솔 출력 테스트를 값·상태 코드 검증으로, `innerHTML` 삽입을 `textContent`로, 공유 변수 증가를 `AtomicLong`으로

**무엇으로 확인했나** — JUnit·MockMvc 서버 테스트 40개, Playwright 브라우저 시나리오, GitHub Actions의 빌드·서버·브라우저·Docker 검증.

<sub>HTTP와 서버 연동 기본기를 확인하는 학습 프로젝트입니다. DB·회원·인증·영속 저장은 범위에 넣지 않았습니다. 무료 서버라 첫 접속에 50초 이상 걸릴 수 있습니다.</sub>

[웹 실습](https://spring-mvc-k14y.onrender.com/) · [Swagger UI](https://spring-mvc-k14y.onrender.com/swagger-ui.html) · [Source](https://github.com/MinsangKwak/spring-mvc)

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
  <img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=openjdk&logoColor=white">
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white">
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white">
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white">
  <img src="https://img.shields.io/badge/Cloud_Run-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white">
  <img src="https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white">
  <img src="https://img.shields.io/badge/GA4-E37400?style=for-the-badge&logo=googleanalytics&logoColor=white">
</div>

### 🧭 How I Work

- **사용자 흐름부터** — 화면을 그리기 전에 이동 순서와 오류·예외가 생기는 곳을 먼저 나눕니다.
- **반복은 공통 구조로** — 같은 버튼과 모달을 복사하지 않고 컴포넌트와 상태 규칙으로 정리합니다.
- **접근성은 처음부터** — 키보드, 포커스, ARIA, 표 구조와 고대비를 초기 마크업에 넣습니다.
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

채용 제안과 인터뷰 문의는 [minsangwork0821@gmail.com](mailto:minsangwork0821@gmail.com)으로 부탁드립니다. 프로젝트별 상세 기록은 **[Portfolio](https://kwakminsang.notion.site/overview)** 에 있습니다.
