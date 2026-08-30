<!--
  이 파일의 소스는 프라이빗 레포 jadewisemann/_jadewisemann 이다.
  공개 레포(jadewisemann/jadewisemann)의 README.md 를 직접 고치지 마라 — 다음 동기화 때 덮어써진다.
  작성 기준은 DESIGN.md (§8 포지셔닝, §9 표기 제외 항목, §5 표준 구조, §3 주장-증거 결합).
  사실의 출처는 wiki/ — resume/document/ 의 기여 요약은 낡았다. 링크는 절대 URL (§7).
-->

<div align="center">

# 팀이 쓸 기반을 만드는 프론트엔드

컨벤션과 품질 기준은 문서가 아니라 도구로 지킵니다.

</div>

<br>

## Projects

### YORR — 모바일 실시간 멀티플레이 게임 플랫폼

<sub>2026.07 – 08 · 6인 팀 (BE 3 · AI 1 · Infra 1 · <b>FE 1, 본인 단독</b>) · FE 약 52,000 LOC</sub>

| | |
|---|---|
| **문제** | 3.5주 일정에 프론트엔드 리뷰어가 없어, 회귀를 사람이 걸러낼 수 없었습니다. |
| **결정** | 기계가 막도록 세웠습니다 — 전체 `src`를 분모로 두는 커버리지 래칫, WebSocket 페이크와 실서버를 각각 겨냥한 Playwright 2단 E2E, Biome 정적 분석, dpdm 순환 의존성 검사. |
| **결과** | 커버리지가 흔들리던 파일을 동일 테스트 2회 실행 비교로 특정해 제외하고, 근본 해결책은 코드에 근거와 함께 남겼습니다. E2E 18스펙 · 디바이스 4종. |

<sub>236파일을 도메인 우선 구조로 재편했고, 회귀를 낸 리팩터링을 스스로 롤백한 커밋도 남아 있습니다.</sub>

[Demo](https://yorr.site) · [Code](https://github.com/jadewisemann/yorr) · [내 커밋](https://github.com/jadewisemann/yorr/commits?author=jadewisemann)

### FestiFriends — 공연 예매 · 모임 커뮤니티

<sub>2025.05 – 07 · 8인 팀 · 형상관리 · 컨벤션 담당</sub>

| | |
|---|---|
| **문제** | 8인 팀에서 문서로만 둔 컨벤션은 지켜지지 않고, 리뷰가 스타일 지적으로 소모됩니다. |
| **결정** | 파일 · 폴더명 규칙을 린트 규칙으로 강제하고, commitlint와 husky pre-push(lint → test → build)로 게이트를 걸었습니다. Jest + MSW 초기 세팅과 PR · 이슈 템플릿도 함께 만들었습니다. |
| **결과** | 규칙 위반이 리뷰가 아니라 훅에서 걸립니다. 공용 컴포넌트는 사용법 문서와 테스트를 붙여 넘겼습니다. |

[Demo](https://ff-frontend-rust.vercel.app/) · [Code](https://github.com/FestiFriends/ff_frontend) · [내 커밋](https://github.com/FestiFriends/ff_frontend/commits?author=jadewisemann)

### Pookjayo — 숙박 예약 플랫폼

<sub>2025.03 – 04 · 5인 팀 · <b>팀장 / PM</b></sub>

| | |
|---|---|
| **문제** | 결제와 예약 확정이 클라이언트에서 끝나면, 금액을 위조하거나 같은 방을 중복으로 잡을 수 있습니다. |
| **결정** | 결제 검증과 예약 체결을 Cloud Functions로 옮기고, 여러 문서에 걸친 확정 과정을 단일 Firestore 트랜잭션으로 묶었습니다. |
| **결과** | 예약이 확정되는 경로에서 클라이언트가 보낸 값을 신뢰하는 지점을 없앴습니다. |

[Demo](https://pookjayo.vercel.app/) · [Code](https://github.com/jadewisemann/Pookjayo)

<br>

## Skills

| | |
|---|---|
| **주력** | ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/React-087EA4?style=flat-square&logo=react&logoColor=white) ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![Zustand](https://img.shields.io/badge/Zustand-433E38?style=flat-square) ![TanStack Query](https://img.shields.io/badge/TanStack%20Query-FF4154?style=flat-square&logo=reactquery&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white) ![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white) ![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white) ![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=flat-square&logo=eslint&logoColor=white) |
| **사용 경험** | ![Firebase](https://img.shields.io/badge/Firebase-DD2C00?style=flat-square&logo=firebase&logoColor=white) ![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white) ![MSW](https://img.shields.io/badge/MSW-FF6A33?style=flat-square&logo=mockserviceworker&logoColor=white) ![React Hook Form](https://img.shields.io/badge/React%20Hook%20Form-EC5990?style=flat-square&logo=reacthookform&logoColor=white) ![Radix UI](https://img.shields.io/badge/Radix%20UI-161618?style=flat-square&logo=radixui&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| **학습 중** | ![Java](https://img.shields.io/badge/Java-E76F00?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Vue.js](https://img.shields.io/badge/Vue%203-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white) ![MySQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |

<br>

## Education

- **삼성청년SW아카데미(SSAFY) 15기** · 2026 ~ · SW 역량테스트 A+
- **코드잇 스프린트 프론트엔드 심화** · 2025
- **이스트소프트 오르미 프론트엔드 4기** · 2024 – 2025
- **인하대학교 화학과** · 2024 졸업

<br>

---

<div align="center">

<a href="https://solved.ac/profile/jadejadejade"><img src="https://mazassumnida.wtf/api/v2/generate_badge?boj=jadejadejade" alt="solved.ac 프로필"></a>

<a href="mailto:jadewisemann@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Gmail"></a>
<a href="https://velog.io/@jadewisemann"><img src="https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white" alt="Velog"></a>

</div>
<!-- 이력서 링크 확보되면 푸터에 추가 (DESIGN.md §9) -->
