<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://capsule-render.vercel.app/api?type=waving&color=0:050d10,40:0a2525,100:050d10&height=160&section=header&text=Oscar%20Ndugbu&fontSize=48&fontColor=5eead4&animation=fadeIn&fontAlignY=60&desc=Staff%2B%20Full-Stack%20%C2%B7%20ML%20%C2%B7%20Infra%20%E2%80%94%20Lagos%20%E2%86%92%20Global&descAlignY=78&descSize=15&descColor=64748b" />
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:050d10,40:0a2525,100:050d10&height=160&section=header&text=Oscar%20Ndugbu&fontSize=48&fontColor=5eead4&animation=fadeIn&fontAlignY=60&desc=Staff%2B%20Full-Stack%20%C2%B7%20ML%20%C2%B7%20Infra%20%E2%80%94%20Lagos%20%E2%86%92%20Global&descAlignY=78&descSize=15&descColor=64748b" />
</picture>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=17&pause=1600&color=5EEAD4&center=true&vCenter=true&width=860&lines=The+system+has+to+work+at+2am.;That%E2%80%99s+not+a+slogan.+It%E2%80%99s+a+design+constraint.;Built+under+Lagos+constraints.+Deployed+to+global+standards.;4hrs+%E2%86%92+15min+%C2%B7+99.9%25%2B+uptime+%C2%B7+sub-150ms+p99.)](https://git.io/typing-svg)

<br/>

[![Portfolio](https://img.shields.io/badge/scardubu.dev-000?style=for-the-badge&logo=vercel&logoColor=5eead4)](https://scardubu.dev)
[![LinkedIn](https://img.shields.io/badge/oscardubu-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/oscardubu)
[![Email](https://img.shields.io/badge/oscar@scardubu.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:oscar@scardubu.dev)
[![Available](https://img.shields.io/badge/AVAILABLE-Staff%2B%20%2F%20Principal%20Roles-5eead4?style=for-the-badge&labelColor=0a2020)](https://scardubu.dev/#section-contact)
[![Location](https://img.shields.io/badge/Lagos%2C%20Nigeria%20🇳🇬-20232a?style=for-the-badge)](https://scardubu.dev)

![](https://komarev.com/ghpvc/?username=Scardubu&style=flat-square&color=5eead4&label=profile+views)

</div>

---

## `$ whoami`

I build systems that stay alive when everything else is failing — mid-audit, mid-outage, mid-storm, at 2am on a generator. Not as a boast. As a specification.

My four production systems span Nigerian federal infrastructure, ensemble ML, multi-agent AI orchestration, and ZK blockchain privacy. Every one of them has a hard constraint the architecture had to survive, documented in the codebase with a `chosen / over / because` triple. The metrics below are not estimates.

<div align="center">

<table>
  <tr>
    <td align="center"><b>4h → 15min</b><br/><sub>Tax filing time<br/>TaxBridge · accountant-reported</sub></td>
    <td align="center"><b>99.9%+</b><br/><sub>90-day uptime<br/>SabiScore · Prometheus window</sub></td>
    <td align="center"><b>sub-150ms</b><br/><sub>API p99 under load<br/>TaxBridge + SabiScore</sub></td>
    <td align="center"><b>45% MTTD</b><br/><sub>Faster incident detection<br/>SabiScore · vs reactive baseline</sub></td>
  </tr>
  <tr>
    <td align="center"><b>80+ → 2/mo</b><br/><sub>ML API incidents<br/>4-week reliability sprint</sub></td>
    <td align="center"><b>&lt;2%</b><br/><sub>Dedup false-positive rate<br/>UBEC · 36-state pipeline</sub></td>
    <td align="center"><b>450ms → 87ms</b><br/><sub>p95 latency after FastAPI migration<br/>73% Redis cache hit rate</sub></td>
    <td align="center"><b>90–95%</b><br/><sub>Test coverage<br/>TaxBridge · Hashablanca · CI-enforced</sub></td>
  </tr>
</table>

</div>

---

## Architecture DNA

Every system I ship carries a decision record. Not documentation for its own sake — because the next engineer debugging at 2am needs to understand *why* the system is shaped the way it is.

<table>
<tr>
  <th>System</th>
  <th>Chosen</th>
  <th>Over</th>
  <th>Because</th>
</tr>
<tr>
  <td><b>TaxBridge</b><br/><sub>Fintech · Compliance</sub></td>
  <td>PostgreSQL Row-Level Security for multi-tenancy</td>
  <td>Application-layer tenant filtering</td>
  <td>NRS audit scrutiny demands proof that tenant data cannot cross-contaminate — RLS enforces this at the database engine, not the app layer</td>
</tr>
<tr>
  <td><b>SabiScore</b><br/><sub>ML · Observability</sub></td>
  <td>FastAPI + Redis Pub/Sub for inference serving</td>
  <td>Synchronous REST with database polling</td>
  <td>Sub-50ms event fan-out at sustained load with dead-letter recovery is impossible with polling under concurrent sessions</td>
</tr>
<tr>
  <td><b>SwarmXQ</b><br/><sub>AI · Agent Platform</sub></td>
  <td>Autonomous evolution layer with LLM-guided strategy mutation</td>
  <td>Static agent configs with manual tuning cycles</td>
  <td>Manual tuning cannot adapt to novel inputs at scale — autonomous evolution scores strategies against real outcomes and rewrites low performers between runs</td>
</tr>
<tr>
  <td><b>Hashablanca</b><br/><sub>ZK · Privacy</sub></td>
  <td>Groth16 ZK proofs with off-chain proving</td>
  <td>Database timestamp signatures</td>
  <td>Database timestamps are mutable — ZK proofs give cryptographic verifiability of document existence without exposing content</td>
</tr>
<tr>
  <td><b>UBEC Pipeline</b><br/><sub>Federal · Data Eng.</sub></td>
  <td>Blocking + probabilistic record linkage (dedupe.io)</td>
  <td>Exact-match deduplication on school_name</td>
  <td>State submissions use inconsistent spellings across ministries — exact match misses 15–20% of true duplicates in validation runs</td>
</tr>
</table>

---

## Featured Systems

<details open>
<summary>
  <b>🧾 TaxBridge</b> &nbsp;·&nbsp;
  <img src="https://img.shields.io/badge/Compliance%20Platform-fintech-5eead4?style=flat-square" />
  <img src="https://img.shields.io/badge/status-case--study-64748b?style=flat-square" />
</summary>

<br/>

> **4 hours of Nigerian SME tax filing compressed to 15 minutes — NRS-integrated, audit-ready, zero data-loss.**

Full tax compliance workflow automation for Nigerian small businesses across VAT, withholding tax, and annual returns. PostgreSQL RLS isolates each tenant at the database engine level. Real-time calculations under `<150ms` at load. Idempotent BullMQ job queues survive mid-request server failure without double-processing. Hash-chained immutable audit trails.

**Hard constraint:** NRS API rate limits at 30 req/min per TIN — the queue must absorb burst filing windows without client-visible failure.

```
Fastify 5 · Java 17 · Spring Boot 3 · PostgreSQL 15 RLS · Redis 7
BullMQ · React Native · Turborepo · GraphQL · Prisma · TypeScript
```

</details>

---

<details>
<summary>
  <b>📈 SabiScore</b> &nbsp;·&nbsp;
  <img src="https://img.shields.io/badge/ML%20Platform-observability-a78bfa?style=flat-square" />
  <img src="https://img.shields.io/badge/status-live-22c55e?style=flat-square" />
  &nbsp;<a href="https://sabiscore.scardubu.dev">↗ demo</a>&nbsp;·&nbsp;<a href="https://github.com/Scardubu/Sabiscore">↗ repo</a>
</summary>

<br/>

> **99.9%+ uptime. 45% MTTD improvement. Ensemble ML that alerts before users notice.**

Ensemble credit and prediction scoring (XGBoost + LightGBM + CatBoost) with real-time output quality monitoring. Alerts engineers the moment a model begins degrading, before any user is affected. Prometheus tracks a 90-day uptime window. 30% inference latency reduction via Redis caching (73% hit rate in production). Incident count fell from 80+/month to 2/month in a 4-week reliability sprint.

**Hard constraint:** Ensemble inference must complete in `<120ms` p99 at peak load, no model warmup on cold start.

```
FastAPI · XGBoost · LightGBM · CatBoost · Redis Pub/Sub
Prometheus · Grafana · PostgreSQL
```

</details>

---

<details>
<summary>
  <b>🤖 SwarmXQ</b> &nbsp;·&nbsp;
  <img src="https://img.shields.io/badge/Multi--Agent-AI%20orchestration-f59e0b?style=flat-square" />
  <img src="https://img.shields.io/badge/status-live-22c55e?style=flat-square" />
  &nbsp;<a href="https://github.com/Scardubu/SwarmXQ">↗ repo</a>
</summary>

<br/>

> **Self-improving agent fleet. Live dashboard. Checkpoint-based fault recovery. Zero manual tuning cycles.**

Agents autonomously improve their own task strategies between runs. Local LLM inference via Ollama — Phi-4-mini for task routing, DeepSeek-R1 for multi-step reasoning, Qwen2.5-Coder for code generation — triadic model selection per task type, zero cloud egress. The evolution layer scores outcomes against quality benchmarks and replaces low-performing configs via LLM-guided mutation without engineering intervention.

**Hard constraint:** Agents must hold correctness under Lagos network conditions — unreliable connectivity, intermittent API availability — running under 8GB RAM without model offloading.

```
Python · FastAPI · Ollama · Next.js 15 · React Native
BullMQ · Redis 7 · WebSocket
```

</details>

---

<details>
<summary>
  <b>🔐 Hashablanca</b> &nbsp;·&nbsp;
  <img src="https://img.shields.io/badge/ZK%20Proofs-privacy-ec4899?style=flat-square" />
  <img src="https://img.shields.io/badge/status-case--study-64748b?style=flat-square" />
  &nbsp;<a href="https://github.com/Scardubu/hashablanca">↗ repo</a>
</summary>

<br/>

> **ZK proofs for document integrity — confidentiality and verifiability as simultaneous properties, not a tradeoff.**

Privacy-preserving blockchain infrastructure using Circom 2 circuits and Groth16 proofs. Any verifier can confirm a document existed and was unmodified at a given timestamp without seeing the document. Multi-chain distribution across Ethereum, Polygon, BSC, and StarkNet. CBOR streaming handles 4GB+ file archives. 90%+ test coverage. GDPR-compliant PII detection and anonymisation.

```
Circom 2 · snarkjs (Groth16) · Solidity · FastAPI · Web3.py · PostgreSQL · Docker
```

</details>

---

<details>
<summary>
  <b>🏛️ UBEC Data Pipeline</b> &nbsp;·&nbsp;
  <img src="https://img.shields.io/badge/Federal%20Infrastructure-data%20engineering-0ea5e9?style=flat-square" />
  <img src="https://img.shields.io/badge/status-case--study-64748b?style=flat-square" />
</summary>

<br/>

> **Abuja HQ · Education data for 40 million Nigerian students across 36 states — ministry-grade reporting.**

Batch ingestion pipeline for the Universal Basic Education Commission. Probabilistic deduplication (dedupe.io + PostgreSQL) at `<2%` false-positive rate — exact-match alone misses 15–20% of true duplicates. Per-state DAG tasks mean one late state submission does not block reporting for the other 35. Great Expectations validation gate flags anomalies before they enter ministry reports.

```
Python 3.11 · Apache Airflow · pandas · PostgreSQL · Great Expectations · dedupe.io · Docker
```

</details>

---

## Open Source

Four packages extracted from production systems and published for the ecosystem.

<table>
<tr>
  <th>Package</th>
  <th>Install</th>
  <th>What it solves</th>
</tr>
<tr>
  <td><a href="https://github.com/Scardubu/pg-tenant"><b>pg-tenant</b></a><br/><sub>Node.js · PostgreSQL</sub></td>
  <td><code>npm i pg-tenant</code></td>
  <td>RLS-based multi-tenancy at the engine level — mathematically enforced, not filtered in app code. One tenant's rows are invisible to another even when application bugs exist.</td>
</tr>
<tr>
  <td><a href="https://github.com/Scardubu/audit-chain"><b>audit-chain</b></a><br/><sub>Fintech · Compliance</sub></td>
  <td><code>npm i audit-chain</code></td>
  <td>Hash-chained log entries where retroactive tampering is instantly detectable. Built for NRS and GDPR trails where proof of integrity is non-negotiable.</td>
</tr>
<tr>
  <td><a href="https://github.com/Scardubu/node-debug-llm"><b>node-debug-llm</b></a><br/><sub>AI · DevOps</sub></td>
  <td><code>npm i node-debug-llm</code></td>
  <td>Streams live system logs and traces to an LLM, returns a ranked plain-English list of likely root causes — incident triage in minutes, not hours.</td>
</tr>
<tr>
  <td><a href="https://github.com/Scardubu/SwarmXQ"><b>llm-dispatch</b></a><br/><sub>AI · Orchestration</sub></td>
  <td><code>pip install llm-dispatch</code></td>
  <td>Triadic GGUF model routing extracted from SwarmXQ. Right model per task type — Phi-4-mini, DeepSeek-R1, Qwen2.5-Coder — with fallback chains and zero cloud egress.</td>
</tr>
</table>

**15+ upstream contributions merged** to XGBoost · scikit-learn and other OSS projects.

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
|-------|-------------|
| **Frontend** | Next.js 15 · React 19 · TypeScript strict · React Native / Expo SDK 54 · Tailwind CSS v4 · Framer Motion · Turborepo 2 · GraphQL |
| **Backend** | Fastify 5 · FastAPI · Java 17 · Spring Boot 3 · Node.js 22 · Python 3.11 · Pydantic v2 · Effect-TS · Go 1.22 |
| **Data** | PostgreSQL 15 RLS · Prisma ORM · Redis 7 · BullMQ · pgvector / FAISS · Apache Airflow · Prometheus + Grafana |
| **ML / AI** | XGBoost · LightGBM · CatBoost · scikit-learn · Evidently AI · Ollama (GGUF) · Triadic LLM routing · RAG pipelines · LangChain |
| **Blockchain** | Circom 2 · snarkjs (Groth16) · Solidity · ethers.js · Hardhat · Noir |
| **Infra** | Docker · GitHub Actions · Vercel Edge · AWS S3 + CloudFront · Sentry · Nginx |
| **Compliance** | NRS / DigiTax API · Row-Level Security · Immutable Audit Trails · NDPC · GDPR PII detection |

</details>

---

## Quality Gates

This portfolio's own CI is a production-grade pipeline — because the portfolio is itself a production system.

```
push → typecheck → lint → build → Playwright smoke
                                   ├── font invariant (zero unauthorised typefaces)
                                   ├── TypeScript strict (zero :any / as any)
                                   ├── conviction string verification (live copy contracts)
                                   ├── V16–V22 architecture contract checks
                                   └── Lighthouse CI gating:
                                       Performance ≥ 85 · Accessibility ≥ 95
                                       SEO ≥ 95 · Best Practices ≥ 95
                                       FCP ≤ 2.5s · LCP ≤ 4s · CLS ≤ 0.1 · TBT ≤ 600ms
```

Husky pre-commit + lint-staged enforce lint on every staged file. The Conviction Engine CI runs on every push to `main` and every PR. Build artifacts are cached between jobs. Playwright smoke runs against the compiled `.next/` output, not dev mode.

---

## Writing

Staff+ signal articles. All metrics from production.

| Article | Key Metric | System |
|---------|-----------|--------|
| [Ensemble Models in Production: How We Achieved 71% Accuracy](https://scardubu.dev/blog/ensemble-models-production) | 64% → 71% accuracy · Brier 0.19 → 0.15 | SabiScore |
| [FastAPI for ML Engineers: Serving Models with <100ms Latency](https://scardubu.dev/blog/fastapi-ml-engineers) | 450ms → 87ms p95 · 73% cache hit rate | SabiScore |
| [0 to 99.9% Uptime: Turning a Flaky ML API Into a Reliable Product in 4 Weeks](https://scardubu.dev/blog/mlops-999-uptime-transformation-case-study) | 80+ incidents → 2/month | SabiScore |
| [Redis Caching Patterns for ML APIs](https://scardubu.dev/blog/redis-caching-patterns-ml-apis) | 73% cache hit rate · production-confirmed | SabiScore |

---

## Certifications

[![AWS](https://img.shields.io/badge/AWS%20Certified%20Developer-Dec%202023-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/certification/)
[![GCP](https://img.shields.io/badge/GCP%20Associate%20Cloud%20Engineer-Aug%202023-4285F4?style=flat-square&logo=google-cloud&logoColor=white)](https://cloud.google.com/certification)
[![OpenJS](https://img.shields.io/badge/OpenJS%20JSNSD-May%202024-339933?style=flat-square&logo=nodedotjs&logoColor=white)](https://openjsf.org/certification/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL%2014%20Associate-Mar%202024-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.enterprisedb.com/training/postgres-certification)

---

## GitHub Analytics

<div align="center">

[![Trophies](https://github-profile-trophy.vercel.app/?username=Scardubu&theme=nord&no-frame=true&column=7&margin-w=8)](https://github.com/ryo-ma/github-profile-trophy)

<br/>

<img height="175" src="https://github-readme-stats.vercel.app/api?username=Scardubu&show_icons=true&hide_border=true&rank_icon=github&include_all_commits=true&count_private=true&theme=transparent&title_color=5eead4&icon_color=5eead4&text_color=94a3b8&ring_color=5eead4" />
&nbsp;
<img height="175" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Scardubu&layout=compact&hide_border=true&theme=transparent&title_color=5eead4&text_color=94a3b8&langs_count=8" />

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com/?user=Scardubu&hide_border=true&background=00000000&ring=5eead4&fire=5eead4&currStreakLabel=5eead4&sideLabels=94a3b8&dates=64748b&currStreakNum=e2e8f0&sideNums=e2e8f0)](https://git.io/streak-stats)

</div>

<div align="center">

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Scardubu&hide_border=true&bg_color=00000000&color=5eead4&line=5eead4&point=ffffff&area=true&area_color=5eead420)](https://github.com/Ashutosh00710/github-readme-activity-graph)

</div>

<!-- CONTRIBUTION SNAKE — Generated daily via GitHub Actions -->
<!-- Setup: .github/workflows/snake.yml using platane/snk@v3 -->
<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Scardubu/Scardubu/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Scardubu/Scardubu/output/github-snake.svg" />
    <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/Scardubu/Scardubu/output/github-snake.svg" />
  </picture>
</div>

---

## Now

```
→ SwarmXQ v2 — autonomous evolution layer hitting production benchmarks
→ TaxBridge mobile — React Native Expo SDK 54 · offline-first architecture
→ Writing: ZK proof generation performance on constrained hardware
→ Open to Staff+ / Principal full-stack or ML infra roles — global, remote
```

---

<div align="center">

*Shipped in Lagos · Running globally · Battle-tested in audit season*

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://capsule-render.vercel.app/api?type=waving&color=0:050d10,40:0a2525,100:050d10&height=100&section=footer" />
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:050d10,40:0a2525,100:050d10&height=100&section=footer" />
</picture>

</div>
