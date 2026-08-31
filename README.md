<!--
  이 파일의 소스는 프라이빗 레포 jadewisemann/_jadewisemann 이다.
  공개 레포(jadewisemann/jadewisemann)의 README.md 를 직접 고치지 마라 — 다음 동기화 때 덮어써진다.
  작성 기준은 루트 DESIGN.md (§1 포지셔닝 v10, §6 README 설계)이고, 사실의 출처는 ref/다.
  링크와 이미지는 공개 레포에서도 동작하도록 절대 URL만 사용한다.
-->

<div align="center">

# 정유진

**프론트엔드 엔지니어**

6인 팀의 프론트엔드를 단독 담당했고, 화면보다 상태와 데이터 흐름을 먼저 설계하는 프론트엔드 엔지니어입니다.

[포트폴리오](https://jadewisemann.space) · [GitHub](https://github.com/jadewisemann) · [Velog](https://velog.io/@jadewisemann) · [이메일](mailto:jadewisemann@gmail.com)

</div>

---

## 프로젝트

### 01 · [YORR](https://github.com/jadewisemann/yorr)

`2026.07–08` · `6인` · `프론트엔드 단독` · `실시간 멀티플레이 게임 플랫폼`

`React` · `TypeScript` · `Vite` · `TanStack Router` · `Zustand` · `Three.js` · `Rapier3D`

<a href="https://yorr.site">
  <picture>
    <source media="(max-width: 600px)" srcset="https://raw.githubusercontent.com/jadewisemann/yorr/main/frontend/public/hero/yacht-narrow.webp">
    <img src="https://raw.githubusercontent.com/jadewisemann/yorr/main/frontend/public/hero/yacht-wide.webp" alt="YORR 요트 다이스 게임 히어로 이미지" width="100%">
  </picture>
</a>

| 영역 | 구현 스펙 |
|---|---|
| 입력·연출 | 모션 센서 원시값 → 클라이언트 판정 이벤트 · 3D 물리·진동·소리 클라이언트 처리 |
| 구조 | 프론트엔드 236파일 도메인 우선 재편 · `dpdm` 순환 의존성 검사 |
| 검증 | Playwright E2E 18스펙 (`mock` 14 · `real` 4) · 320px 가로 넘침 기하 판정 · 전체 `src` 기준 커버리지 측정 |
| 복원·회귀 | `sessionToken` 기반 게임 재접속 상태 복원 · 배포 회귀 리팩터링 롤백 |

[데모](https://yorr.site) · [코드](https://github.com/jadewisemann/yorr) · [아키텍처](https://github.com/jadewisemann/yorr/blob/main/frontend/docs/architecture.md) · [커밋](https://github.com/jadewisemann/yorr/commits?author=jadewisemann)

<br>

### 02 · [FestiFriends](https://github.com/FestiFriends/ff_frontend)

`2025.05–07` · `8인` · `PM` · `프론트엔드`

`Next.js` · `React` · `TypeScript` · `TanStack Query` · `Tailwind CSS` · `Zod` · `Jest` · `MSW`

| 영역 | 구현 스펙 |
|---|---|
| URL 상태 | 공연 필터·정렬·페이지네이션 ↔ URL query parameter · TanStack Query 연동 |
| 컴포넌트 | 접근 가능한 headless compound `PerformanceCard` · 목록·상세·찜 화면 공통화 |
| 품질 | ESLint·Prettier · commitlint · Husky `pre-push` (`lint → test → build`) · Jest/MSW · PR·이슈 템플릿 |
| 디버깅 | `PerformanceDatePicker` 무한 렌더 · 불안정한 `useEffect` 의존성 제거 · `useCallback` 안정화 |

[데모](https://ff-frontend-rust.vercel.app/) · [코드](https://github.com/FestiFriends/ff_frontend) · [버그 수정 커밋](https://github.com/FestiFriends/ff_frontend/commit/786efc5285bf72f1ac980659a3c269cb7e75f71d)

<br>

### 03 · [Pookjayo](https://github.com/jadewisemann/Pookjayo)

`2025.03–04` · `5인` · `팀장·PM` · `프론트엔드`

`React` · `JavaScript` · `Vite` · `Zustand` · `Tailwind CSS` · `Firebase` · `Firestore` · `IndexedDB`

| 영역 | 구현 스펙 |
|---|---|
| 정합성 | Firestore transaction으로 예약·잔여 객실·검색 인덱스·포인트·거래 기록 원자적 갱신 · 중복 예약 방지 |
| 결제 상태 | `IDLE → DATA_LOADED → PROCESSING → COMPLETED / ERROR` · `PROCESSING` 중복 요청 거부 |
| 검색·캐시 | 1–3-gram 토큰 인덱스 · 메모리/IndexedDB 2단 캐시 |

[데모](https://pookjayo.vercel.app/) · [코드](https://github.com/jadewisemann/Pookjayo)

---

## 기술 스택

### 01 · 핵심 프론트엔드

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=20232A) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=000000) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

### 02 · 상태·라우팅·데이터

![Zustand](https://img.shields.io/badge/Zustand-433E38?style=flat-square) ![TanStack Query](https://img.shields.io/badge/TanStack%20Query-FF4154?style=flat-square) ![TanStack Router](https://img.shields.io/badge/TanStack%20Router-FF4154?style=flat-square) ![React Router](https://img.shields.io/badge/React%20Router-CA4245?style=flat-square&logo=reactrouter&logoColor=white) ![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=000000) ![Firestore](https://img.shields.io/badge/Firestore-FFCA28?style=flat-square) ![Firebase Auth](https://img.shields.io/badge/Firebase%20Auth-FFCA28?style=flat-square) ![Axios](https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white) ![Context API](https://img.shields.io/badge/Context%20API-61DAFB?style=flat-square&logo=react&logoColor=20232A) ![IndexedDB](https://img.shields.io/badge/IndexedDB-3C873A?style=flat-square)

### 03 · UI·인터랙션

![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white) ![Rapier3D](https://img.shields.io/badge/Rapier3D-000000?style=flat-square) ![Radix UI](https://img.shields.io/badge/Radix%20UI-161618?style=flat-square&logo=radixui&logoColor=white) ![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square) ![Responsive / Mobile-first](https://img.shields.io/badge/Responsive%20%2F%20Mobile--first-0F172A?style=flat-square)

### 04 · 폼·테스트·품질

![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square) ![React Hook Form](https://img.shields.io/badge/React%20Hook%20Form-EC5990?style=flat-square&logo=reacthookform&logoColor=white) ![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white) ![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white) ![Jest](https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white) ![React Testing Library](https://img.shields.io/badge/React%20Testing%20Library-E33332?style=flat-square) ![MSW](https://img.shields.io/badge/MSW-FF6A33?style=flat-square) ![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=flat-square&logo=eslint&logoColor=white) ![Prettier](https://img.shields.io/badge/Prettier-F7B93E?style=flat-square&logo=prettier&logoColor=000000) ![Husky](https://img.shields.io/badge/Husky-4E4E4E?style=flat-square) ![commitlint](https://img.shields.io/badge/commitlint-000000?style=flat-square)

### 05 · 서버리스·데이터 수집

![Firebase Functions](https://img.shields.io/badge/Firebase%20Functions-FFCA28?style=flat-square&logo=firebase&logoColor=000000) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Beautiful Soup](https://img.shields.io/badge/Beautiful%20Soup-2D2D2D?style=flat-square) ![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white)

### 06 · 협업·개발 도구

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white) ![GitHub Flow](https://img.shields.io/badge/GitHub%20Flow-181717?style=flat-square&logo=github&logoColor=white) ![PR / Issue Templates](https://img.shields.io/badge/PR%20%2F%20Issue%20Templates-0969DA?style=flat-square) ![Documentation](https://img.shields.io/badge/Documentation-0969DA?style=flat-square)

## 교육

- 2026–현재 · 삼성청년SW아카데미(SSAFY) 15기 · SW 역량테스트 A+
- 2025 · 코드잇 스프린트 프론트엔드 심화
- 2024–2025 · 이스트소프트 오르미 프론트엔드 4기

<div align="center">

<a href="https://solved.ac/profile/jadejadejade"><img src="https://mazassumnida.wtf/api/v2/generate_badge?boj=jadejadejade" alt="solved.ac 프로필"></a>

<a href="mailto:jadewisemann@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="이메일 보내기"></a>
<a href="https://velog.io/@jadewisemann"><img src="https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white" alt="Velog 블로그"></a>

</div>

<!-- 이력서 링크 확보되면 푸터에 추가 (DESIGN.md §8) -->
