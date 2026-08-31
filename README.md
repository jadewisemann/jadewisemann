<!--
  이 파일의 소스는 프라이빗 레포 jadewisemann/_jadewisemann 이다.
  공개 레포(jadewisemann/jadewisemann)의 README.md 를 직접 고치지 마라 — 다음 동기화 때 덮어써진다.
  작성 기준은 루트 DESIGN.md (§1 포지셔닝 v2, §6 README 설계)이고, 사실의 출처는 ref/다.
  링크와 이미지는 공개 레포에서도 동작하도록 절대 URL만 사용한다.
-->

<div align="center">

# 정유진

**Frontend Engineer**

Sole frontend engineer on a [six-person team](https://github.com/jadewisemann/yorr) building a real-time multiplayer web game platform.<br>
I turn interaction-heavy behavior into explicit state, clear domain boundaries, and executable quality checks.

[GitHub](https://github.com/jadewisemann) · [Velog](https://velog.io/@jadewisemann) · [Email](mailto:jadewisemann@gmail.com)

</div>

---

## Selected work

### 01 · [YORR](https://github.com/jadewisemann/yorr)

`Real-time multiplayer web game platform controlled by phones`

**Role** · Sole frontend engineer in a six-person team

The client connects a large-screen game with mobile controllers. The interesting work was keeping input, game state, and UI behavior testable as the product grew.

<a href="https://yorr.site">
  <picture>
    <source media="(max-width: 600px)" srcset="https://raw.githubusercontent.com/jadewisemann/yorr/main/frontend/public/hero/yacht-narrow.webp">
    <img src="https://raw.githubusercontent.com/jadewisemann/yorr/main/frontend/public/hero/yacht-wide.webp" alt="YORR yacht dice game hero artwork" width="100%">
  </picture>
</a>

- **Interaction** · Converted raw motion input into client-side game events and handled 3D physics and feedback on the client.
- **Architecture** · Reorganized 236 frontend files around product domains and added dependency-cycle checks.
- **Quality** · Built 18 Playwright specs across mocked and real-server paths, checked 320px overflow geometrically, and measured coverage against the full `src` tree.
- **Reliability** · Implemented session-based game-state restoration and rolled back a large refactor after it caused a deployment regression.

[Demo](https://yorr.site) · [Code](https://github.com/jadewisemann/yorr) · [Architecture](https://github.com/jadewisemann/yorr/blob/main/frontend/docs/architecture.md) · [Commits](https://github.com/jadewisemann/yorr/commits?author=jadewisemann)

<br>

### 02 · [FestiFriends](https://github.com/FestiFriends/ff_frontend)

`Festival discovery and group-matching platform`

**Role** · PM and frontend developer in an eight-person team

- **Navigation** · Synchronized performance filters, sorting, pagination, and TanStack Query state through URL query parameters.
- **Components** · Rebuilt `PerformanceCard` as an accessible, headless compound component for list, detail, and favorites views.
- **Team quality** · Set up ESLint/Prettier conventions, commitlint, Husky `pre-push` (`lint → test → build`), Jest/MSW, and PR/issue templates.
- **Debugging** · Traced an infinite render loop to an unstable function in a `useEffect` dependency, then removed the unstable dependency and stabilized the change handler with `useCallback`.

[Demo](https://ff-frontend-rust.vercel.app/) · [Code](https://github.com/FestiFriends/ff_frontend) · [Bug-fix commit](https://github.com/FestiFriends/ff_frontend/commit/786efc5285bf72f1ac980659a3c269cb7e75f71d)

<br>

### 03 · [Pookjayo](https://github.com/jadewisemann/Pookjayo)

`Mobile-first accommodation search, booking, and payment platform`

**Role** · Team lead / PM; frontend and serverless payment logic

- **Consistency** · Used a Firestore transaction to update reservations, availability, search index, points, and transaction records together; confirmed bookings are checked inside the transaction to prevent double booking.
- **Payment state** · Modeled the client flow as `IDLE → DATA_LOADED → PROCESSING → COMPLETED / ERROR`; invalid transitions from `PROCESSING` reject repeat submissions.
- **Search and cache** · Built a 1–3-gram token index to avoid collection scans and a memory/IndexedDB two-level cache for stable hotel data.

[Demo](https://pookjayo.vercel.app/) · [Code](https://github.com/jadewisemann/Pookjayo)

## Engineering focus

- **Interaction systems** · Mobile motion input, 3D physics, and narrow-width boundaries. ([YORR](https://github.com/jadewisemann/yorr))
- **State and data integrity** · Explicit payment state transitions and transactional updates to derived data. ([Pookjayo](https://github.com/jadewisemann/Pookjayo))
- **Frontend architecture** · Domain-first organization, URL-driven query state, and headless compound components. ([YORR](https://github.com/jadewisemann/yorr) · [FestiFriends](https://github.com/FestiFriends/ff_frontend))
- **Quality engineering** · E2E harnesses, coverage baselines, lint rules, hooks, and tests. ([YORR](https://github.com/jadewisemann/yorr) · [FestiFriends](https://github.com/FestiFriends/ff_frontend))

## Technical stack

**Core**

`TypeScript` · `JavaScript` · `React` · `Next.js` · `Vite`

**State and data**

`Zustand` · `TanStack Query` · `React Hook Form` · `Zod` · `Firebase` · `Firestore` · `Firebase Functions` · `IndexedDB`

**UI and graphics**

`Tailwind CSS` · `Radix UI` · `Three.js` · `Rapier3D`

**Testing and quality**

`Vitest` · `Playwright` · `Jest` · `React Testing Library` · `MSW` · `ESLint` · `Prettier` · `Husky` · `commitlint`

**Currently learning**

`Java` · `Spring Boot` · `Vue 3` · `SQL`

## Education

- `2026–present` · SSAFY 15 · SW competency test A+
- `2025` · Codeit Sprint · Advanced Frontend
- `2024–2025` · ESTsoft Ormi Frontend 4
- `2024` · Inha University · Chemistry

## Contact

[GitHub](https://github.com/jadewisemann) · [Velog](https://velog.io/@jadewisemann) · [Email](mailto:jadewisemann@gmail.com)

<div align="center">

<a href="https://solved.ac/profile/jadejadejade"><img src="https://mazassumnida.wtf/api/v2/generate_badge?boj=jadejadejade" alt="solved.ac profile"></a>

<a href="mailto:jadewisemann@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email jadewisemann"></a>
<a href="https://velog.io/@jadewisemann"><img src="https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white" alt="Velog blog"></a>

</div>

<!-- 이력서 링크 확보되면 푸터에 추가 (DESIGN.md §8) -->
