<!--
  이 파일의 소스는 프라이빗 레포 jadewisemann/_jadewisemann 이다.
  공개 레포(jadewisemann/jadewisemann)의 README.md 를 직접 고치지 마라 — 다음 동기화 때 덮어써진다.
  작성 기준은 루트 DESIGN.md (§1 포지셔닝 v3, §6 README 설계)이고, 사실의 출처는 ref/다.
  링크와 이미지는 공개 레포에서도 동작하도록 절대 URL만 사용한다.
-->

<div align="center">

# 정유진

**프론트엔드 엔지니어**

`6인 팀 FE 단독` · `실시간 멀티플레이` · `상태 관리` · `3D 인터랙션` · `E2E 테스트`

`React` · `TypeScript` · `Next.js` · `Vite` · `Three.js`

[GitHub](https://github.com/jadewisemann) · [Velog](https://velog.io/@jadewisemann) · [이메일](mailto:jadewisemann@gmail.com)

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

<div align="center">

<a href="https://skillicons.dev">
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="https://skillicons.dev/icons?i=ts,js,react,nextjs,vite,tailwind,threejs,firebase,vitest,jest,git&perline=6&theme=light">
    <img src="https://skillicons.dev/icons?i=ts,js,react,nextjs,vite,tailwind,threejs,firebase,vitest,jest,git&perline=6&theme=dark" alt="주요 기술: TypeScript, JavaScript, React, Next.js, Vite, Tailwind CSS, Three.js, Firebase, Vitest, Jest, Git">
  </picture>
</a>

<br>

<sub>학습 중</sub><br>
<a href="https://skillicons.dev">
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="https://skillicons.dev/icons?i=java,spring,vue&perline=3&theme=light">
    <img src="https://skillicons.dev/icons?i=java,spring,vue&perline=3&theme=dark" alt="학습 중인 기술: Java, Spring Boot, Vue 3">
  </picture>
</a>

</div>

**핵심** · TypeScript · JavaScript · React · Next.js · Vite<br>
**상태·데이터** · Zustand · TanStack Query · React Hook Form · Zod · Firebase · Firestore · Firebase Functions · IndexedDB<br>
**UI·그래픽** · Tailwind CSS · Radix UI · Three.js · Rapier3D<br>
**테스트·품질** · Vitest · Playwright · Jest · React Testing Library · MSW · ESLint · Prettier · Husky · commitlint<br>
**학습 중** · Java · Spring Boot · Vue 3 · SQL

## 교육

- `2026–현재` · 삼성청년SW아카데미(SSAFY) 15기 · SW 역량테스트 A+
- `2025` · 코드잇 스프린트 프론트엔드 심화
- `2024–2025` · 이스트소프트 오르미 프론트엔드 4기
- `2024` · 인하대학교 화학과

<div align="center">

[GitHub](https://github.com/jadewisemann) · [Velog](https://velog.io/@jadewisemann) · [이메일](mailto:jadewisemann@gmail.com)

<a href="https://solved.ac/profile/jadejadejade"><img src="https://mazassumnida.wtf/api/v2/generate_badge?boj=jadejadejade" alt="solved.ac 프로필"></a>

<a href="mailto:jadewisemann@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="이메일 보내기"></a>
<a href="https://velog.io/@jadewisemann"><img src="https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white" alt="Velog 블로그"></a>

</div>

<!-- 이력서 링크 확보되면 푸터에 추가 (DESIGN.md §8) -->
