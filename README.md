<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=16&pause=1600&color=5EEAD4&center=true&vCenter=true&width=700&lines=Oscar+Ndugbu+%E2%80%94+Staff%2B+Full-Stack+%C2%B7+ML+%C2%B7+Infra;The+system+has+to+work+at+2am.;That%E2%80%99s+not+a+slogan.+It%E2%80%99s+a+design+constraint.;Built+under+Lagos+constraints.+Deployed+globally.;4hrs+%E2%86%92+15min+%C2%B7+99.9%25%2B+uptime+%C2%B7+sub-150ms+p99.)](https://git.io/typing-svg)

<br/>

[![Portfolio](https://img.shields.io/badge/scardubu.dev-000000?style=flat-square&logo=vercel&logoColor=5eead4)](https://scardubu.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-oscardubu-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/oscardubu)
[![Email](https://img.shields.io/badge/Email-oscar@scardubu.dev-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:oscar@scardubu.dev)
[![Location](https://img.shields.io/badge/Lagos%2C%20Nigeria%20🇳🇬-1e293b?style=flat-square)](https://scardubu.dev)

[![Available](https://img.shields.io/badge/AVAILABLE%20FOR-Staff%2B%20%2F%20Principal%20Roles-5eead4?style=for-the-badge&labelColor=0a2020)](https://scardubu.dev/#section-contact)

![Profile views](https://komarev.com/ghpvc/?username=Scardubu&style=flat-square&color=5eead4&label=profile+views)

</div>

---

## `$ whoami`

I build systems that stay alive when everything else is failing — mid-audit, mid-outage, mid-storm, at 2am on a generator. Not as a boast. As a specification.

My four production systems span Nigerian federal infrastructure, ensemble ML, multi-agent AI orchestration, and ZK blockchain privacy. Every one has a hard constraint the architecture had to survive, documented in the codebase with a `chosen / over / because` triple. The metrics below are not estimates.

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
    <td align="center"><b>450ms → 87ms</b><br/><sub>p95 after FastAPI migration<br/>73% Redis cache hit rate</sub></td>
    <td align="center"><b>90–95%</b><br/><sub>Test coverage<br/>TaxBridge · Hashablanca · CI</sub></td>
  </tr>
</table>

</div>

---

## Architecture DNA

Every system I ship carries a decision record — because the engineer debugging at 2am needs to know *why* it's shaped this way.

<table>
<tr>
  <th>System</th>
  <th>Chosen</th>
  <th>Over</th>
  <th>Because</th>
</tr>
<tr>
  <td><b>TaxBridge</b><br/><sub>Fintech · Compliance</sub></td>
  <td>PostgreSQL Row-Level Security</td>
  <td>Application-layer tenant filtering</td>
  <td>NRS audit demands proof data cannot cross-contaminate — RLS enforces this at the engine, not the app layer</td>
</tr>
<tr>
  <td><b>SabiScore</b><br/><sub>ML · Observability</sub></td>
  <td>FastAPI + Redis Pub/Sub</td>
  <td>Synchronous REST + DB polling</td>
  <td>Sub-50ms event fan-out at sustained load with dead-letter recovery is impossible with polling under concurrent sessions</td>
</tr>
<tr>
  <td><b>SwarmXQ</b><br/><sub>AI · Orchestration</sub></td>
  <td>Autonomous evolution layer with LLM-guided mutation</td>
  <td>Static agent configs + manual tuning</td>
  <td>Manual tuning cannot adapt to novel inputs at scale — evolution scores strategies against real outcomes and rewrites low performers</td>
</tr>
<tr>
  <td><b>Hashablanca</b><br/><sub>ZK · Privacy</sub></td>
  <td>Groth16 ZK proofs, off-chain proving</td>
  <td>Database timestamp signatures</td>
  <td>DB timestamps are mutable — ZK proofs give cryptographic verifiability of document existence without exposing content</td>
</tr>
<tr>
  <td><b>UBEC Pipeline</b><br/><sub>Federal · Data Eng.</sub></td>
  <td>Blocking + probabilistic record linkage</td>
  <td>Exact-match dedup on school_name</td>
  <td>State submissions use inconsistent spellings — exact match misses 15–20% of true duplicates in validation runs</td>
</tr>
</table>

---

## Featured Systems

<details open>
<summary><b>🧾 TaxBridge</b> &nbsp;·&nbsp; Compliance Platform · Fintech &nbsp;·&nbsp; <code>case-study</code></summary>

<br/>

> **4 hours of Nigerian SME tax filing compressed to 15 minutes — NRS-integrated, audit-ready, zero data-loss.**

Full tax compliance workflow automation across VAT, withholding tax, and annual returns. PostgreSQL RLS isolates each tenant at the engine level. Real-time calculations under `<150ms` at load. Idempotent BullMQ queues survive mid-request server failure without double-processing. Hash-chained immutable audit trails. 95% test coverage.

**Hard constraint:** NRS API rate limits at 30 req/min per TIN — the queue must absorb burst filing windows without client-visible failure.

```
Fastify 5 · Java 17 · Spring Boot 3 · PostgreSQL 15 RLS · Redis 7
BullMQ · React Native · Turborepo · GraphQL · Prisma · TypeScript
```

</details>

---

<details>
<summary><b>📈 SabiScore</b> &nbsp;·&nbsp; ML Platform · Observability &nbsp;·&nbsp; <code>live</code> &nbsp;·&nbsp; <a href="https://sabiscore.scardubu.dev">↗ demo</a> · <a href="https://github.com/Scardubu/Sabiscore">↗ repo</a></summary>

<br/>

> **99.9%+ uptime. 45% MTTD improvement. Ensemble ML that alerts before users notice.**

Ensemble credit and prediction scoring (XGBoost + LightGBM + CatBoost) with real-time output quality monitoring. Prometheus tracks a 90-day uptime window. 30% inference latency reduction via Redis caching (73% hit rate in production). Incident count: 80+/month → 2/month in a 4-week reliability sprint.

**Hard constraint:** Ensemble inference must complete in `<120ms` p99 at peak load, no model warmup on cold start.

```
FastAPI · XGBoost · LightGBM · CatBoost · Redis Pub/Sub · Prometheus · Grafana · PostgreSQL
```

</details>

---

<details>
<summary><b>🤖 SwarmXQ</b> &nbsp;·&nbsp; Multi-Agent AI Platform &nbsp;·&nbsp; <code>live</code> &nbsp;·&nbsp; <a href="https://github.com/Scardubu/SwarmXQ">↗ repo</a></summary>

<br/>

> **Self-improving agent fleet. Live dashboard. Checkpoint-based fault recovery. Zero manual tuning cycles.**

Agents autonomously improve their own task strategies between runs. Local LLM inference via Ollama — Phi-4-mini for routing, DeepSeek-R1 for reasoning, Qwen2.5-Coder for code generation — zero cloud egress. The evolution layer scores outcomes and rewrites low-performing configs via LLM-guided mutation without engineering intervention.

**Hard constraint:** Agents must hold correctness under Lagos network conditions running under 8GB RAM without model offloading.

```
Python · FastAPI · Ollama · Next.js 15 · React Native · BullMQ · Redis 7 · WebSocket
```

</details>

---

<details>
<summary><b>🔐 Hashablanca</b> &nbsp;·&nbsp; ZK Privacy Infrastructure &nbsp;·&nbsp; <code>case-study</code> &nbsp;·&nbsp; <a href="https://github.com/Scardubu/hashablanca">↗ repo</a></summary>

<br/>

> **ZK proofs for document integrity — confidentiality and verifiability as simultaneous properties, not a tradeoff.**

Circom 2 circuits with Groth16 proofs. Any verifier can confirm a document existed and was unmodified at a given timestamp without seeing it. Multi-chain across Ethereum, Polygon, BSC, and StarkNet. CBOR streaming handles 4GB+ archives. 90%+ test coverage. GDPR-compliant PII detection.

```
Circom 2 · snarkjs (Groth16) · Solidity · FastAPI · Web3.py · PostgreSQL · Docker
```

</details>

---

<details>
<summary><b>🏛️ UBEC Data Pipeline</b> &nbsp;·&nbsp; Federal Infrastructure · Data Engineering &nbsp;·&nbsp; <code>case-study</code></summary>

<br/>

> **Abuja HQ · Education data for 40 million Nigerian students across 36 states — ministry-grade reporting.**

Batch ingestion for the Universal Basic Education Commission. Probabilistic deduplication at `<2%` false-positive rate. Per-state DAG tasks mean one late state doesn't block the other 35. Great Expectations validation gate flags anomalies before they reach ministry reports.

```
Python 3.11 · Apache Airflow · pandas · PostgreSQL · Great Expectations · dedupe.io · Docker
```

</details>

---

## Open Source

<table>
<tr>
  <th>Package</th>
  <th>Install</th>
  <th>What it solves</th>
</tr>
<tr>
  <td><a href="https://github.com/Scardubu/pg-tenant"><b>pg-tenant</b></a><br/><sub>Node.js · PostgreSQL</sub></td>
  <td><code>npm i pg-tenant</code></td>
  <td>RLS-based multi-tenancy at the engine. One tenant's rows are invisible to another even when application bugs exist.</td>
</tr>
<tr>
  <td><a href="https://github.com/Scardubu/audit-chain"><b>audit-chain</b></a><br/><sub>Fintech · Compliance</sub></td>
  <td><code>npm i audit-chain</code></td>
  <td>Hash-chained log entries — retroactive tampering is instantly detectable. Built for NRS and GDPR trails.</td>
</tr>
<tr>
  <td><a href="https://github.com/Scardubu/node-debug-llm"><b>node-debug-llm</b></a><br/><sub>AI · DevOps</sub></td>
  <td><code>npm i node-debug-llm</code></td>
  <td>Streams live logs to an LLM, returns ranked plain-English root causes. Incident triage in minutes, not hours.</td>
</tr>
<tr>
  <td><a href="https://github.com/Scardubu/SwarmXQ"><b>llm-dispatch</b></a><br/><sub>AI · Orchestration</sub></td>
  <td><code>pip install llm-dispatch</code></td>
  <td>Triadic GGUF routing from SwarmXQ — Phi-4-mini, DeepSeek-R1, Qwen2.5-Coder — with fallback chains, zero cloud egress.</td>
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

This portfolio's own CI is a production pipeline — because the portfolio is itself a production system.

```
push → typecheck → lint → build → Playwright smoke
                                   ├── font invariant (zero unauthorised typefaces)
                                   ├── TypeScript strict (zero :any / as any)
                                   ├── conviction string verification (live copy contracts)
                                   ├── V16–V22 architecture contract checks
                                   └── Lighthouse CI:
                                       Perf ≥ 85 · A11y ≥ 95 · SEO ≥ 95 · BP ≥ 95
                                       FCP ≤ 2.5s · LCP ≤ 4s · CLS ≤ 0.1 · TBT ≤ 600ms
```

Husky pre-commit + lint-staged on every staged file. Playwright smoke runs against compiled `.next/` output, not dev mode.

---

## Writing

Staff+ signal articles. All metrics from production.

| Article | Key Metric | System |
|---------|-----------|--------|
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

## GitHub Analytics

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=Scardubu&show_icons=true&hide_border=true&rank_icon=github&include_all_commits=true&count_private=true&theme=transparent&title_color=5eead4&icon_color=5eead4&text_color=94a3b8" />
&nbsp;&nbsp;
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Scardubu&layout=compact&hide_border=true&theme=transparent&title_color=5eead4&text_color=94a3b8&langs_count=8" />

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

```
→ SwarmXQ v2 — autonomous evolution layer hitting production benchmarks
→ TaxBridge mobile — React Native Expo SDK 54 · offline-first architecture
→ Writing: ZK proof generation performance on constrained hardware
→ Open to Staff+ / Principal full-stack or ML infra roles — global, remote
```

---

<div align="center">

*Shipped in Lagos · Running globally · Battle-tested in audit season*

</div>
