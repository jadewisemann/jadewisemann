<!--
  이 파일의 소스는 프라이빗 레포 jadewisemann/_jadewisemann 이다.
  공개 레포(jadewisemann/jadewisemann)의 README.md 를 직접 고치지 마라 — 다음 동기화 때 덮어써진다.
  작성 기준은 루트 DESIGN.md (§1 포지셔닝 v2, §6 README 설계). 사실의 출처는 ref/ 다.
  링크는 절대 URL만 쓴다 (DESIGN.md §7).
-->

<div align="center">

# 정유진 · Frontend Engineer

**6인 팀 · 프론트엔드 단독 · 실시간 멀티플레이 게임 플랫폼**<br>
React · TypeScript · Test Automation · Realtime Web

</div>

<br>

## 프로젝트

### 01. YORR

> 휴대폰을 컨트롤러로 사용하는 실시간 멀티플레이 게임 플랫폼

`React` `TypeScript` `Vite` `TanStack Router` `Zustand` `Three.js` `Rapier3D` `WebSocket` `Vitest` `Playwright` `Biome`

| 구분 | 내용 |
|---|---|
| **기간 · 팀** | 2026.07–08 · 6인 (BE 3 · AI 1 · Infra 1 · **FE 1**) |
| **역할** | 프론트엔드 단독 · 화면, 상태 관리, 실시간 통신, 3D 게임, 테스트 환경 |
| **구조** | 236파일 도메인 우선 구조 재편 · dpdm 순환 의존성 검사 |
| **테스트** | Vitest 커버리지 래칫 · Playwright E2E 18스펙 · 디바이스 4종 |
| **E2E** | WebSocket 페이크 14스펙 · 실서버 4스펙 |
| **품질** | Biome 정적 분석 · 전체 `src` 기준 커버리지 분모 · 불안정 측정 파일 원인 기록 |

- 모바일 모션 센서 입력을 클라이언트에서 판정한 이벤트로 변환
- 320px 가로 넘침을 요소 좌표로 판정하는 E2E
- 배포 회귀를 일으킨 대규모 리팩터링 롤백

[**Demo**](https://yorr.site) · [**Code**](https://github.com/jadewisemann/yorr) · [**Commits**](https://github.com/jadewisemann/yorr/commits?author=jadewisemann)

<br>

### 02. FestiFriends

> 공연 탐색 · 찜 · 동행 모임 플랫폼

`Next.js` `React` `TypeScript` `TanStack Query` `Tailwind CSS` `Zod` `Jest` `RTL` `MSW` `ESLint` `Husky`

| 구분 | 내용 |
|---|---|
| **기간 · 팀** | 2025.05–07 · 8인 · PM · 형상 관리 · 프론트엔드 개발 |
| **구현** | 공연 목록 · 찜 · 모임 개설 · 공통 컴포넌트 · URL 기반 필터 상태 |
| **품질** | ESLint 커스텀 규칙 · commitlint · pre-push `lint → test → build` |
| **테스트** | Jest · RTL · MSW 초기 구성 · 컴포넌트 문서와 테스트 병행 |

[**Demo**](https://ff-frontend-rust.vercel.app/) · [**Code**](https://github.com/FestiFriends/ff_frontend) · [**Commits**](https://github.com/FestiFriends/ff_frontend/commits?author=jadewisemann)

<br>

### 03. Pookjayo

> 모바일 우선 숙박 검색 · 예약 · 결제 플랫폼

`React` `JavaScript` `Vite` `Zustand` `Tailwind CSS` `Firebase Functions` `Firestore` `IndexedDB` `Python`

| 구분 | 내용 |
|---|---|
| **기간 · 팀** | 2025.03–04 · 5인 · 팀장/PM · 프론트엔드 개발 |
| **구현** | 결제 상태 FSM · 예약 트랜잭션 · N-gram 검색 · 메모리/IndexedDB 2단 캐시 |
| **데이터** | 예약 · 잔여 객실 · 검색 인덱스를 단일 Firestore 트랜잭션으로 갱신 |
| **보안** | 클라이언트 쓰기 차단 · 모든 변경을 Firebase Functions로 제한 |

[**Demo**](https://pookjayo.vercel.app/) · [**Code**](https://github.com/jadewisemann/Pookjayo)

<br>

## 기술

| 영역 | 기술 |
|---|---|
| **Frontend** | `TypeScript` `JavaScript` `React` `Next.js` `Vite` `Tailwind CSS` |
| **State · Data** | `Zustand` `TanStack Query` `React Hook Form` `Zod` `Firebase` `IndexedDB` |
| **Test · Quality** | `Vitest` `Playwright` `Jest` `RTL` `MSW` `ESLint` `Biome` `Husky` |
| **Graphics** | `Three.js` `Rapier3D` |
| **Learning** | `Java` `Spring Boot` `Vue 3` `SQL` |

<br>

## 교육

| 기간 | 과정 |
|---|---|
| **2026–현재** | 삼성청년SW아카데미(SSAFY) 15기 · SW 역량테스트 A+ |
| **2025** | 코드잇 스프린트 프론트엔드 심화 |
| **2024–2025** | 이스트소프트 오르미 프론트엔드 4기 |
| **2024 졸업** | 인하대학교 화학과 |

<br>

---

<div align="center">

<a href="https://solved.ac/profile/jadejadejade"><img src="https://mazassumnida.wtf/api/v2/generate_badge?boj=jadejadejade" alt="solved.ac 프로필"></a>

<a href="mailto:jadewisemann@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Gmail"></a>
<a href="https://velog.io/@jadewisemann"><img src="https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white" alt="Velog"></a>

</div>
<!-- 이력서 링크 확보되면 푸터에 추가 (DESIGN.md §8) -->
