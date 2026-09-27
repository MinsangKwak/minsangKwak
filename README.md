# 곽민상 · Minsang Kwak

**Frontend · Web UI Developer**

사용자 흐름과 접근성을 바탕으로, 복잡한 화면을 유지보수 가능한 구조로 만듭니다.
금융 서비스의 공통 UI·인증 흐름을 설계해왔으며, 개인 프로젝트에서는 React·Next.js·TypeScript를 중심으로 데이터·인증·배포·운영까지 직접 연결하고 있습니다.

[포트폴리오](https://kwakminsang.notion.site/overview) · [기술 블로그](https://minsangkwak.github.io/) · [이메일](mailto:kmsdevwork@gmail.com)

---

## 만드는 것

### moncamp

**Pokémon GO에서 무엇을 잡고, 키우고, 배틀에 사용할지 판단하도록 돕는 서비스**

작은 정보 페이지에서 시작해 도감·랭킹·일정·덱 도구와 계정 기능을 갖춘 운영 서비스로 확장했습니다. 기획부터 UX/UI, 프론트엔드, 인증 서버, 데이터와 운영까지 직접 다룹니다.

- **구조 전환** — HTML·Vanilla JavaScript → React·TypeScript → Next.js로 단계적으로 개선
- **인증·데이터** — Fastify 기반 Google OAuth·권한 관리, Neon Postgres, Python 데이터 파이프라인
- **품질·운영** — 디자인 시스템·Storybook, 사용자 제보와 QA, 개발·운영 배포 분리, GA4·운영 통계

`Next.js` `React` `TypeScript` `Fastify` `PostgreSQL` `Python` `Vercel` `Cloud Run`

[서비스](https://moncamp.kr/) · [코드](https://github.com/MinsangKwak/pogo-rank) · [개발 문서](https://github.com/MinsangKwak/pogo-rank/tree/main/docs)

### subway-midpoint

**여러 출발역에서 가장 오래 이동하는 사람의 부담을 줄이는 지하철 중간역 추천 서비스**

역 검색부터 후보 비교와 지도 경로 표시까지 구현했습니다. 노선의 분기·순환·환승을 데이터로 표현하고, 계산 로직을 화면과 분리했습니다.

- **알고리즘** — 이진 최소 힙 다익스트라, 환승역 다중 출발점, 최대 예상 이동시간을 최소화하는 후보 선정
- **데이터** — OpenStreetMap·Overpass API 기반 1~9호선 데이터 생성, 역 이름 정규화와 환승역 통합
- **사용성·검증** — 키보드 검색·ARIA·한글 IME 처리, 지도 오류와 계산 분리, Vitest 회귀 테스트와 CI

`React` `TypeScript` `Vite` `Kakao Maps` `OpenStreetMap` `Vitest` `GitHub Actions`

[서비스](https://minsangkwak.github.io/subway-midpoint/) · [코드](https://github.com/MinsangKwak/subway-midpoint) · [설계 문서](https://github.com/MinsangKwak/subway-midpoint/blob/main/docs/ARCHITECTURE.md)

<sub>소요시간은 거리·환승 비용에 따른 추정값이며 실제 시각표를 반영하지 않습니다.</sub>

---

## 해온 일

| 경험 | 맡은 일 |
| --- | --- |
| **금융결제원 · UX/UI팀** | 국세 납부 POS, 은행 공동망 본인확인서비스, 어카운트인포 PC 웹 UI 신규 구축과 금융 서비스 운영 |
| **NICE평가정보 · 플랫폼사업실**<br>2023.05–2025.05 | 통신사 본인인증 흐름 공통화, ES6 기반 구조 개선, 신용·제휴 서비스 프론트엔드 개발·운영 |
| **이지 회계사·세무 아카데미 · 프리랜서**<br>2025.03.15–2025.06.09 | Next.js·React·TypeScript·Sass 기반 반응형 교육 웹서비스 UI 구축 |

<details>
<summary>주요 구현 경험 더 보기</summary>

### 규모가 커져도 수정 범위를 알 수 있는 UI

- **국세 납부 POS:** 1024×768 무인수납기 환경의 서비스 화면 21개와 UI 가이드 구축. 조회부터 카드 납부 결과까지 전체 UI와 QA 담당
- **어카운트인포 PC 웹:** 141개 화면을 버튼·입력·표·모달과 공통 레이아웃으로 구성. 계좌·카드·금융정보 업무의 단계와 상태 규칙 정리
- **현재 상태 구분:** 어카운트인포는 UI 프로토타입·퍼블리싱 산출물 검토 완료 단계이며, 개발·배포는 2027.07 예정

### 인증 흐름과 예외 상태

- 통신 3사·MVNO 인증 흐름을 공통화하고 상태·이벤트·DOM·스타일의 책임 분리
- 입력 오류, 캡차, 인증 시간 초과, 서비스 점검 등 사용자가 다음 행동을 판단해야 하는 상태 구현
- 입력 조건이나 화면이 바뀔 때 이전 오류·선택 상태가 남지 않도록 초기화 구조 개선

### 접근성과 운영 품질

- KWCAG 기반 키보드 탐색, ARIA 모달, 포커스 이동·복귀, 표 구조와 고대비 UI 적용
- 운영 서비스의 중복 코드 정리, 웹폰트·이미지 리소스 최적화, 반응형·접근성 QA 수행

[경력과 프로젝트 상세 보기 →](https://kwakminsang.notion.site/overview)

</details>

## 사용하는 기술

| 영역 | 실무·프로젝트에서 사용한 기술 |
| --- | --- |
| **Frontend** | JavaScript ES6+ · TypeScript · React · Next.js · HTML · CSS · Sass · jQuery |
| **UI · Accessibility** | Atomic Design · Design Tokens · CSS Modules · Storybook · KWCAG · ARIA |
| **Server · Data** | Node.js · Fastify · Google OAuth · PostgreSQL · Python |
| **Quality · Operations** | Vitest · ESLint · GitHub Actions · Vercel · Cloud Run · Cloudflare · GA4 |

## 일하는 방식

- **사용자 흐름부터 정리합니다.** 화면을 만들기 전에 이동 순서와 오류·예외 상태를 나눕니다.
- **반복되는 UI는 공통 구조로 만듭니다.** 컴포넌트뿐 아니라 상태와 입력 규칙도 함께 정리합니다.
- **접근성을 초기 설계에 포함합니다.** 키보드, 포커스, ARIA와 명암비를 구현 과정에서 확인합니다.
- **출시 이후까지 봅니다.** 테스트·배포·사용자 피드백을 다음 개선으로 연결합니다.

---

자세한 작업 범위와 구현 기록은 [포트폴리오](https://kwakminsang.notion.site/overview)에서 확인할 수 있습니다.
업무·협업 문의는 [kmsdevwork@gmail.com](mailto:kmsdevwork@gmail.com)으로 보내주세요.
