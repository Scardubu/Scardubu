# Oscar Ndugbu — scardubu.dev

Staff+ Full-Stack · Infra · ML portfolio focused on systems that keep working when the pressure is highest: audits, outages, burst traffic, weak connectivity, and 2am incident response.

**Live site:** [scardubu.dev](https://scardubu.dev)  
**Canonical system spec:** [CONVICTION_ENGINE_V1_0.md](CONVICTION_ENGINE_V1_0.md)

<div align="center">

[![Portfolio](https://img.shields.io/badge/scardubu.dev-000000?style=flat-square&logo=vercel&logoColor=5eead4)](https://scardubu.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-oscardubu-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/oscardubu)
[![Email](https://img.shields.io/badge/Email-oscar@scardubu.dev-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:oscar@scardubu.dev)
[![Location](https://img.shields.io/badge/Lagos%2C%20Nigeria%20🇳🇬-1e293b?style=flat-square)](https://scardubu.dev)
[![Open to](https://img.shields.io/badge/OPEN%20TO-Staff%2B%20%2F%20Principal%20Roles-5eead4?style=for-the-badge&labelColor=0a2020)](https://scardubu.dev/#section-contact)

![Profile views](https://komarev.com/ghpvc/?username=Scardubu&style=flat-square&color=5eead4&label=profile+views)

</div>

---

## Why this repo exists

This is a proof-driven portfolio, not a brochure. It shows the systems, constraints, trade-offs, and outcomes behind the work: four production case studies, four open-source packages, 62 verified skills, and a writing trail that explains the engineering decisions.

Everything in the repo is arranged to answer four questions quickly:

1. What do you build?
2. What did it improve?
3. What did you choose over the alternatives?
4. Can the codebase survive real production conditions?

---

## At a glance

<div align="center">

<table>
  <tr>
    <td align="center"><b>4h → 15min</b><br/><sub>Tax filing time<br/>TaxBridge · accountant-reported</sub></td>
    <td align="center"><b>99.9%+</b><br/><sub>90-day uptime<br/>SabiScore · Prometheus window</sub></td>
    <td align="center"><b>sub-150ms</b><br/><sub>API p99 under load<br/>TaxBridge + SabiScore</sub></td>
    <td align="center"><b>45% MTTD</b><br/><sub>Faster incident detection<br/>SabiScore · vs reactive baseline</sub></td>
  </tr>
</table>

</div>

---

## Featured systems

<details open>
<summary><b>🧾 TaxBridge</b> · Compliance Platform · Fintech · <code>case-study</code></summary>

<br/>

> **4 hours of Nigerian SME tax filing compressed to 15 minutes — NRS-integrated, audit-ready, zero data-loss.**

Full tax compliance workflow automation across VAT, withholding tax, and annual returns. PostgreSQL Row-Level Security isolates each tenant at the engine level. Real-time calculations stay under `<150ms` at load. Idempotent BullMQ queues survive mid-request server failure without double-processing. Hash-chained immutable audit trails back the compliance story. Test coverage sits at 95%.

**Hard constraint:** NRS API rate limits at 30 req/min per TIN, so burst filing windows must be absorbed without any client-visible failure.

```text
Fastify 5 · Java 17 · Spring Boot 3 · PostgreSQL 15 RLS · Redis 7
BullMQ · React Native · Turborepo · GraphQL · Prisma · TypeScript
```

[Case study](/work/taxbridge)

</details>

---

<details>
<summary><b>📈 SabiScore</b> · ML Platform · Observability · <code>live</code> · <a href="https://sabiscore.scardubu.dev">demo</a> · <a href="https://github.com/Scardubu/Sabiscore">repo</a></summary>

<br/>

> **99.9%+ uptime. 45% MTTD improvement. Ensemble ML that alerts before users notice.**

Ensemble credit and prediction scoring with XGBoost, LightGBM, and CatBoost, plus real-time output-quality monitoring. Prometheus tracks a 90-day uptime window. Redis caching delivered a 73% hit rate in production and helped cut inference latency by 30%. Incident volume moved from 80+ monthly events to 2/month during a 4-week reliability sprint.

**Hard constraint:** ensemble inference must complete in `<120ms` p99 at peak load with no model warmup on cold start.

```text
FastAPI · XGBoost · LightGBM · CatBoost · Redis Pub/Sub · Prometheus · Grafana · PostgreSQL
```

[Case study](/work/sabiscore)

</details>

---

<details>
<summary><b>🤖 SwarmXQ</b> · Multi-Agent AI Platform · <code>live</code> · <a href="https://github.com/Scardubu/SwarmXQ">repo</a></summary>

<br/>

> **Self-improving multi-agent operator platform — autonomous evolution layer, live fleet dashboard, production-grade reliability under resource constraints.**

Agents improve their own task strategies between runs. Local inference runs through Ollama: Phi-4-mini handles routing, DeepSeek-R1 handles multi-step reasoning, and Qwen2.5-Coder handles code generation. The system keeps zero cloud egress, uses fallback chains that degrade gracefully under memory pressure, and surfaces live fleet telemetry through a Next.js 15 dashboard.

**Hard constraint:** the orchestration layer must remain usable on constrained hardware without giving up deterministic fallback behavior.

```text
Next.js 15 · Ollama · GGUF · Redis 7 · WebSocket · React Native · TypeScript
```

[Case study](/work/swarmxq)

</details>

---

<details>
<summary><b>🔐 Hashablanca</b> · ZK Privacy System · <code>case-study</code></summary>

<br/>

> **Privacy-preserving transaction flow with zero-knowledge proofs and verifiable state transitions.**

Built around cryptographic privacy guarantees rather than trust-by-assertion. The system emphasizes proof generation, state integrity, and auditability under constrained environments.

```text
Circom 2 · snarkjs · Solidity · ethers.js · Hardhat · TypeScript
```

[Case study](/work/hashablanca)

</details>

---

## Open source

| Package | Install | What it solves |
| --- | --- | --- |
| [**pg-tenant**](https://github.com/Scardubu/pg-tenant)<br/><sub>Node.js · PostgreSQL</sub> | `npm i pg-tenant` | RLS-based multi-tenancy at the engine. One tenant’s rows stay invisible even when application logic breaks. |
| [**audit-chain**](https://github.com/Scardubu/audit-chain)<br/><sub>Fintech · Compliance</sub> | `npm i audit-chain` | Hash-chained log entries so retroactive tampering becomes immediately detectable. |
| [**node-debug-llm**](https://github.com/Scardubu/node-debug-llm)<br/><sub>AI · DevOps</sub> | `npm i node-debug-llm` | Streams live logs to an LLM and returns ranked plain-English root causes. |
| [**llm-dispatch**](https://github.com/Scardubu/SwarmXQ)<br/><sub>AI · Orchestration</sub> | `pip install llm-dispatch` | Triadic GGUF routing from SwarmXQ with fallback chains and zero cloud egress. |

**Upstream work:** 15+ merged contributions across XGBoost, scikit-learn, and related OSS.

---

## Stack

#### Frontend
[![skill-icons](https://skillicons.dev/icons?i=nextjs,react,ts,tailwind,html,css,figma)](https://skillicons.dev)

#### Backend & APIs
[![skill-icons](https://skillicons.dev/icons?i=nodejs,python,java,fastapi,graphql,postgres,redis)](https://skillicons.dev)

#### ML / AI
[![skill-icons](https://skillicons.dev/icons?i=pytorch,sklearn,docker,kubernetes,elasticsearch)](https://skillicons.dev)

> `XGBoost · LightGBM · CatBoost · Ollama · RAG · Multi-Agent Orchestration · ZK Proofs`

#### Infrastructure & Tooling
[![skill-icons](https://skillicons.dev/icons?i=github,githubactions,vercel,aws,linux,bash,vscode)](https://skillicons.dev)

<details>
<summary>Full stack matrix</summary>

<br/>

| Layer | Technologies |
| --- | --- |
| **Frontend** | Next.js 15 · React 19 · TypeScript strict · React Native / Expo SDK 54 · Tailwind CSS v4 · Framer Motion · Turborepo 2 · GraphQL |
| **Backend** | Fastify 5 · FastAPI · Java 17 · Spring Boot 3 · Node.js 22 · Python 3.11 · Pydantic v2 · Effect-TS · Go 1.22 |
| **Data** | PostgreSQL 15 RLS · Prisma ORM · Redis 7 · BullMQ · pgvector / FAISS · Apache Airflow · Prometheus + Grafana |
| **ML / AI** | XGBoost · LightGBM · CatBoost · scikit-learn · Evidently AI · Ollama (GGUF) · triadic LLM routing · RAG pipelines · LangChain |
| **Blockchain** | Circom 2 · snarkjs (Groth16) · Solidity · ethers.js · Hardhat · Noir |
| **Infra** | Docker · GitHub Actions · Vercel Edge · AWS S3 + CloudFront · Sentry · Nginx |
| **Compliance** | NRS / DigiTax API · Row-Level Security · immutable audit trails · NDPC · GDPR PII detection |

</details>

---

## Documentation and governance

- **Primary operating standard:** [`CONVICTION_ENGINE_V1_0.md`](CONVICTION_ENGINE_V1_0.md)
- **Release correction history:** [`docs/deployment-history/CORRECTIONS.md`](docs/deployment-history/CORRECTIONS.md)
- **Legacy guidance:** archived inside the `## ARCHIVE — v32.0` section of `CONVICTION_ENGINE_V1_0.md` for historical context only

Each domain has one canonical source. The README mirrors the live system, but it does not replace the source files.

| Domain | Canonical source |
| --- | --- |
| Projects | `lib/projects.ts` |
| Skills | `lib/data/skills.ts` |
| Hero / profile | `lib/portfolio-data.ts` |
| Production proof cards | `components/TestimonialsSection.tsx` |
| Writing posts | `content/writing/*.mdx` via `lib/content.ts` |
| Config / URLs | `lib/config.ts` |
| Live activity feed | `app/api/activity/route.ts` |

---

## Quality gates

This portfolio’s CI is treated like a production pipeline.

```text
push → typecheck → lint → build → Playwright smoke
                           ├── TypeScript strict checks
                           ├── conviction string verification
                           ├── architecture contract checks
                           └── Lighthouse CI targets
```

- `pnpm build` is the main integration check.
- `pnpm type-check` catches strict TypeScript drift.
- `pnpm lint` covers application code and test paths.
- `pnpm test:smoke` and `pnpm test:e2e` protect the core user journey.
- `pnpm lhci` keeps the performance envelope visible.
- Husky + lint-staged run on every staged file.

### Responsive validation targets

When adjusting the hero or layout, verify 320px, 360px, 390px, 768px, 1024px, 1280px, and 1536px. The key checks are overflow, headline wrapping, carousel behavior, and dashboard density.

---

## Local setup

**Requirements:** Node.js ≥ 20, pnpm ≥ 9

```bash
pnpm install
pnpm dev
```

The app starts at `http://localhost:3000`.

### Scripts

```bash
pnpm dev          # local dev server
pnpm build        # production build
pnpm start        # run built app
pnpm lint         # ESLint checks
pnpm lint:fix     # auto-fix lint issues
pnpm type-check   # strict TypeScript checks
pnpm test:smoke   # production build + Chromium smoke subset
pnpm test:e2e     # Playwright smoke suite
pnpm test:all     # full Playwright matrix
pnpm audit:copy   # content compliance checks
pnpm lhci         # Lighthouse CI
```

---

## Writing

The writing section is where the portfolio turns the implementation into reusable signal.

| Article | Key metric | System |
| --- | --- | --- |
| [Ensemble Models in Production: 71% Accuracy](https://scardubu.dev/blog/ensemble-models-production) | 64% → 71% accuracy · Brier 0.19 → 0.15 | SabiScore |
| [FastAPI for ML Engineers: <100ms Latency](https://scardubu.dev/blog/fastapi-ml-engineers) | 450ms → 87ms p95 · 73% cache hit rate | SabiScore |
| [0 to 99.9% Uptime in 4 Weeks](https://scardubu.dev/blog/mlops-999-uptime-transformation-case-study) | 80+ incidents → 2/month | SabiScore |
| [Redis Caching Patterns for ML APIs](https://scardubu.dev/blog/redis-caching-patterns-ml-apis) | 73% cache hit rate · production-confirmed | SabiScore |

---

## Certifications

![AWS](https://img.shields.io/badge/AWS%20Certified%20Developer-Dec%202023-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![GCP](https://img.shields.io/badge/GCP%20Associate%20Cloud%20Engineer-Aug%202023-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![OpenJS](https://img.shields.io/badge/OpenJS%20Node.js%20JSNSD-May%202024-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL%2014%20Associate-Mar%202024-4169E1?style=flat-square&logo=postgresql&logoColor=white)

---

## GitHub analytics

<div align="center">

<table>
  <tr>
    <td width="50%" align="center">
      <picture>
        <source
          srcset="https://github-readme-stats.vercel.app/api?username=Scardubu&show_icons=true&include_all_commits=true&count_private=true&cache_seconds=86400&hide_border=true&theme=dark&rank_icon=github&title_color=5eead4&icon_color=5eead4&text_color=94a3b8&bg_color=00000000"
          media="(prefers-color-scheme: dark)"
        />
        <source
          srcset="https://github-readme-stats.vercel.app/api?username=Scardubu&show_icons=true&include_all_commits=true&count_private=true&cache_seconds=86400&hide_border=true&theme=default&rank_icon=github&title_color=0f172a&icon_color=0f766e&text_color=334155"
          media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)"
        />
        <img
          src="https://github-readme-stats.vercel.app/api?username=Scardubu&show_icons=true&include_all_commits=true&count_private=true&cache_seconds=86400&hide_border=true&theme=default&rank_icon=github"
          alt="Oscar's GitHub stats"
          width="100%"
        />
      </picture>
    </td>
    <td width="50%" align="center">
      <picture>
        <source
          srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Scardubu&layout=compact&langs_count=8&cache_seconds=86400&hide_border=true&theme=dark&title_color=5eead4&text_color=94a3b8&bg_color=00000000"
          media="(prefers-color-scheme: dark)"
        />
        <source
          srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Scardubu&layout=compact&langs_count=8&cache_seconds=86400&hide_border=true&theme=default&title_color=0f172a&text_color=334155"
          media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)"
        />
        <img
          src="https://github-readme-stats.vercel.app/api/top-langs/?username=Scardubu&layout=compact&langs_count=8&cache_seconds=86400&hide_border=true&theme=default"
          alt="Oscar's top languages"
          width="100%"
        />
      </picture>
    </td>
  </tr>
</table>

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com/?user=Scardubu&hide_border=true&background=00000000&ring=5eead4&fire=5eead4&currStreakLabel=5eead4&sideLabels=94a3b8&dates=64748b&currStreakNum=e2e8f0&sideNums=e2e8f0)](https://git.io/streak-stats)

</div>

<div align="center">

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Scardubu&hide_border=true&bg_color=00000000&color=5eead4&line=5eead4&point=ffffff&area=true&area_color=5eead420)](https://github.com/Ashutosh00710/github-readme-activity-graph)

</div>

<!--
  CONTRIBUTION SNAKE — uncomment after running the snake workflow once.
  Setup: copy snake.yml into .github/workflows/, run it manually from the
  Actions tab, then uncomment the block below.

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Scardubu/Scardubu/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Scardubu/Scardubu/output/github-snake.svg" />
    <img alt="contribution snake" src="https://raw.githubusercontent.com/Scardubu/Scardubu/output/github-snake.svg" />
  </picture>
</div>
-->

---

## Now

```text
→ SwarmXQ v2 — autonomous evolution layer hitting production benchmarks
→ TaxBridge mobile — React Native Expo SDK 54 · offline-first architecture
→ Writing — ZK proof generation performance on constrained hardware
→ Open to Staff+ / Principal full-stack or ML infra roles — global, remote
```

---

<div align="center">

*Shipped in Lagos · Running globally · Battle-tested in audit season*

</div>

---

*Personal portfolio. All content copyright Oscar Ndugbu.*
