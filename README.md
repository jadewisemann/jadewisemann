<!--
  이 파일의 소스는 프라이빗 레포 jadewisemann/_jadewisemann 이다.
  공개 레포(jadewisemann/jadewisemann)의 README.md 를 직접 고치지 마라 — 다음 동기화 때 덮어써진다.
  작성 기준은 DESIGN.md (§8 포지셔닝, §9 표기 제외 항목, §5 표준 구조, §3 주장-증거 결합).
  사실의 출처는 ../resume/wiki/ — document/ 의 기여 요약은 낡았다. 링크는 절대 URL (§7).
-->

# 팀이 쓸 기반을 만드는 프론트엔드

환경을 세팅해본 사람이라, 세팅되지 않은 곳에 던져놔도 굴러갑니다.
1년 간격으로 두 팀에서 품질 인프라를 세웠고, 두 번째는 리뷰해줄 프론트엔드 동료 없이 혼자 했습니다.

<br>

## Featured Projects

### YORR — 모바일 실시간 멀티플레이 게임 플랫폼
2026.07 – 08 · 6인 팀 (BE 3 · AI 1 · Infra 1 · **FE 1, 본인 단독**) · 프론트엔드 약 52,000 LOC

- **문제** — 3.5주짜리 프로젝트에 프론트엔드 리뷰어가 없었습니다. 코드를 봐줄 사람이 없으면 회귀는 배포되고 나서야 발견됩니다.
- **결정** — 사람 대신 기계가 막도록 검증 장치를 직접 세웠습니다. 커버리지 래칫(테스트가 import한 파일이 아니라 **전체 `src`를 분모로** 둬야 수치가 안전망 크기를 말합니다), 프로덕션 빌드용 WebSocket 페이크와 실서버를 각각 겨냥한 Playwright 2단 E2E, Biome 정적 분석, dpdm 순환 의존성 검사.
- **결과** — 커버리지가 실행마다 흔들리던 파일 하나를 **동일 테스트 2회 실행 비교로 특정**(전역 branches 90.48% vs 91.43%)하고, 대안(파일별 glob 하한)이 전역 분모를 줄이지 못함까지 확인한 뒤 제외했습니다. 근본 해결책(렌더 루프에 시간 주입)은 코드에 근거와 함께 남겨뒀습니다. E2E 18스펙 · 디바이스 4종.

레이어 우선이던 구조를 **도메인 우선으로 236파일 재편**해, 게임 하나 추가가 폴더 하나 추가로 끝나게 정리했습니다. 자신이 만든 404파일 리팩터링이 배포 회귀를 내자 롤백을 판단·실행한 커밋도 그대로 남아 있습니다.

[Demo](https://yorr.site) · [Code](https://github.com/jadewisemann/yorr) · [내 커밋](https://github.com/jadewisemann/yorr/commits?author=jadewisemann)

### FestiFriends — 공연 예매 · 모임 커뮤니티
2025.05 – 07 · 8인 팀 · 형상관리 · 컨벤션 담당

- **문제** — 8인이 붙는 프로젝트에서 컨벤션을 문서로만 두면 지켜지지 않습니다. 리뷰가 스타일 지적으로 소모됩니다.
- **결정** — 파일 · 폴더명 규칙을 **린트 규칙으로 강제**하고, commitlint 와 husky pre-push(lint → test → build)로 게이트를 걸었습니다. Jest + MSW 초기 세팅과 PR · 이슈 템플릿도 함께 만들었습니다.
- **결과** — 규칙 위반이 리뷰가 아니라 훅에서 걸립니다. 공용 컴포넌트는 사용법 `.md` 와 테스트를 함께 붙여 넘겼습니다.

[Demo](https://ff-frontend-rust.vercel.app/) · [Code](https://github.com/FestiFriends/ff_frontend) · [내 커밋](https://github.com/FestiFriends/ff_frontend/commits?author=jadewisemann)

### Pookjayo — 숙박 예약 플랫폼
2025.03 – 04 · 5인 팀 · **팀장 / PM**

- **문제** — 결제와 예약 확정이 클라이언트에서 끝나면, 금액을 위조하거나 같은 방을 중복으로 잡을 수 있습니다.
- **결정** — 결제 검증과 예약 체결을 Cloud Functions 로 옮기고, 여러 문서에 걸친 확정 과정을 단일 Firestore 트랜잭션으로 묶었습니다.
- **결과** — 예약이 확정되는 경로에서 클라이언트가 보낸 값을 신뢰하는 지점을 없앴습니다. 검색은 N-gram 인덱스 쿼리 빌더로 모듈화하고, 같은 조건의 재검색은 IndexedDB 캐시로 걷어냈습니다.

[Demo](https://pookjayo.vercel.app/) · [Code](https://github.com/jadewisemann/Pookjayo)

<br>

## Skills

숙련도는 세 단계로 나눠 적습니다. 전부 "능숙"으로 쓰면 전부 의심받기 때문입니다.

**주력** — 직접 설계 · 구현했고 코드로 설명할 수 있습니다

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-087EA4?style=flat-square&logo=react&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-433E38?style=flat-square)
![TanStack Query](https://img.shields.io/badge/TanStack%20Query-FF4154?style=flat-square&logo=reactquery&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=flat-square&logo=eslint&logoColor=white)

→ [YORR](https://github.com/jadewisemann/yorr/commits?author=jadewisemann) · [FestiFriends](https://github.com/FestiFriends/ff_frontend/commits?author=jadewisemann) · [Pookjayo](https://github.com/jadewisemann/Pookjayo)

**사용 경험** — 프로젝트에 적용했으나 범위가 부분적입니다

![Firebase](https://img.shields.io/badge/Firebase-DD2C00?style=flat-square&logo=firebase&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)
![MSW](https://img.shields.io/badge/MSW-FF6A33?style=flat-square&logo=mockserviceworker&logoColor=white)
![React Hook Form](https://img.shields.io/badge/React%20Hook%20Form-EC5990?style=flat-square&logo=reacthookform&logoColor=white)
![Radix UI](https://img.shields.io/badge/Radix%20UI-161618?style=flat-square&logo=radixui&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

**학습 중** — 교육 과정에서 다루는 중이고, 실무 프로젝트 적용은 아직 없습니다

![Java](https://img.shields.io/badge/Java-E76F00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue%203-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![MySQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

<br>

## 학력 · 교육

![SSAFY](https://img.shields.io/badge/SSAFY%2015기-0F4C81?style=flat-square)
![코드잇](https://img.shields.io/badge/코드잇%20스프린트%20FE-3E4A5B?style=flat-square)
![오르미](https://img.shields.io/badge/이스트소프트%20오르미%20FE%204기-5A3E8E?style=flat-square)
![인하대학교](https://img.shields.io/badge/인하대학교%20화학과-1B4F8A?style=flat-square)

- **삼성청년SW아카데미(SSAFY) 15기** — 2026.01 ~ 재학 · SW 역량테스트 **A+** · 알고리즘 스터디 조직 · 운영
- **코드잇 스프린트 프론트엔드 심화** — 2025.04 ~ 07 수료
- **이스트소프트 오르미 프론트엔드 4기** — 2024.11 ~ 2025.04 수료
- **인하대학교 화학과** — 2015.03 ~ 2024.08 졸업

<br>

## 지표

[![solved.ac](https://mazassumnida.wtf/api/v2/generate_badge?boj=jadejadejade)](https://solved.ac/profile/jadejadejade)

<br>

## Contact

- **Email** — jadewisemann@gmail.com
- **Blog** — [velog.io/@jadewisemann](https://velog.io/@jadewisemann) · 알고리즘 · 컴퓨터구조 · 네트워크 학습 기록 125편
<!-- - **이력서** — <링크 확보되면 추가> -->
