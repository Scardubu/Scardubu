# Oscar Ndugbu — scardubu.dev

**Staff+ Full-Stack • Infrastructure • ML Systems Engineer**

I design and ship **high-stakes production systems** that survive audits, outages, burst traffic, weak connectivity, and 2 a.m. incidents — while maintaining compliance and zero data loss.

**Live Portfolio:** [scardubu.dev](https://scardubu.dev)  
**Location:** Lagos, Nigeria 🇳🇬  
**Open to:** Staff+ / Principal roles in Full-Stack Platforms, ML Infrastructure, or High-Reliability Systems (Remote / Global)

<div align="center">

[![Portfolio](https://img.shields.io/badge/scardubu.dev-000000?style=flat-square&logo=vercel&logoColor=5eead4)](https://scardubu.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-oscardubu-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/oscardubu)
[![Email](https://img.shields.io/badge/oscar%40scardubu.dev-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:oscar@scardubu.dev)
[![Open to Staff+ / Principal](https://img.shields.io/badge/OPEN_TO-Staff%2B_%2F_Principal-5eead4?style=for-the-badge&labelColor=0a2020)](https://scardubu.dev/#section-contact)

</div>

---

## Impact at a Glance

<div align="center">

| **4h → 15min** | **99.9%+ Uptime** | **sub-150ms p99** | **45% MTTD Reduction** |
|----------------|-------------------|-------------------|------------------------|
| Nigerian SME tax filing | 90-day Prometheus window | TaxBridge + SabiScore | SabiScore observability |

</div>

---

## Who I Am

I build systems where **failure is expensive**. From compressing Nigerian SME tax compliance workflows to deploying production-grade ensemble ML scoring and self-improving multi-agent platforms, my work consistently delivers measurable business impact under real-world constraints.

Every project answers the same four questions:
- What measurable outcome did it drive?
- What hard constraints were overcome?
- Why this architecture over alternatives?
- Will it survive production pressure?

**Battle-tested in Lagos. Running globally.**

---

## Featured Production Systems

### 🧾 TaxBridge — Fintech Compliance Platform

**4 hours → 15 minutes** end-to-end tax filing for Nigerian SMEs. NRS-integrated, audit-ready, zero data loss.

**Key Achievements**
- PostgreSQL Row-Level Security for true engine-level tenant isolation
- Idempotent BullMQ queues that survive mid-request failures
- Hash-chained immutable audit trails for compliance
- Sub-150ms API p99 latency under load
- 95% test coverage

**Stack:** Fastify 5 · Java 17 + Spring Boot 3 · PostgreSQL 15 RLS · Redis 7 · BullMQ · React Native · GraphQL

[Full Case Study →](/work/taxbridge)

### 📈 SabiScore — Production ML Observability Platform

**Live Demo:** [sabiscore.scardubu.dev](https://sabiscore.scardubu.dev) • [Repo](https://github.com/Scardubu/Sabiscore)

Ensemble credit & prediction scoring (XGBoost + LightGBM + CatBoost) with real-time quality monitoring and observability.

**Key Results**
- 99.9%+ uptime (90-day Prometheus window)
- 45% reduction in Mean Time To Detect
- 73% Redis cache hit rate → 30% lower inference latency
- Incidents: 80+/month → 2/month

**Hard constraint met:** <120ms p99 ensemble inference on cold start.

**Stack:** FastAPI · XGBoost/LightGBM/CatBoost · Redis Pub/Sub · Prometheus + Grafana

[Full Case Study →](/work/sabiscore)

### 🤖 SwarmXQ — Self-Improving Multi-Agent AI Platform

**Live:** [Repo](https://github.com/Scardubu/SwarmXQ)

Autonomous multi-agent orchestration with local inference and strategy evolution.

- Triadic LLM routing (Phi-4-mini → DeepSeek-R1 → Qwen2.5-Coder)
- Zero cloud egress with graceful degradation under memory pressure
- Live fleet dashboard (Next.js 15)
- Deterministic fallback behavior on constrained hardware

**Stack:** Next.js 15 · Ollama (GGUF) · Redis · WebSocket · React Native

[Full Case Study →](/work/swarmxq)

### 🔐 Hashablanca — Zero-Knowledge Privacy System

Privacy-preserving transactions using ZK proofs and verifiable state transitions.

**Stack:** Circom 2 · snarkjs · Solidity · ethers.js · Hardhat

[Full Case Study →](/work/hashablanca)

---

## Open Source Contributions

| Package | Install | Impact |
|---------|--------|--------|
| **[pg-tenant](https://github.com/Scardubu/pg-tenant)** | `npm i pg-tenant` | True PostgreSQL RLS-based multi-tenancy at the engine level |
| **[audit-chain](https://github.com/Scardubu/audit-chain)** | `npm i audit-chain` | Tamper-evident hash-chained logs for fintech compliance |
| **[node-debug-llm](https://github.com/Scardubu/node-debug-llm)** | `npm i node-debug-llm` | Streams logs to LLMs for plain-English root cause analysis |
| **[llm-dispatch](https://github.com/Scardubu/SwarmXQ)** | `pip install llm-dispatch` | Local triadic GGUF routing with fallback chains |

**Upstream:** 15+ merged contributions to XGBoost, scikit-learn, and related projects.

---

## Technical Arsenal

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)

</div>

**Core Strengths**
- **Systems & Backend** — Fastify, FastAPI, Java 17 + Spring Boot, Node.js 22, Effect-TS
- **Data & ML** — PostgreSQL (RLS + pgvector), Redis, XGBoost/LightGBM/CatBoost, Ollama GGUF, RAG pipelines
- **Frontend & Mobile** — Next.js 15, React 19 (strict TS), React Native + Expo 54, Tailwind v4
- **Infra & Observability** — Docker, Kubernetes, Prometheus + Grafana, Sentry, GitHub Actions
- **Specialized** — Zero-Knowledge Proofs (Circom/snarkjs), Multi-agent orchestration, Immutable audit systems

[Full Stack Matrix →](https://scardubu.dev)

---

## Thought Leadership

Translating deep production experience into reusable insights:

- [Ensemble Models in Production: 71% Accuracy](https://scardubu.dev/blog/ensemble-models-production)
- [FastAPI for ML Engineers: <100ms Latency](https://scardubu.dev/blog/fastapi-ml-engineers)
- [0 to 99.9% Uptime in 4 Weeks](https://scardubu.dev/blog/mlops-999-uptime-transformation-case-study)
- [Redis Caching Patterns for ML APIs](https://scardubu.dev/blog/redis-caching-patterns-ml-apis)

---

## Now & Next

- Shipping **SwarmXQ v2** — autonomous evolution layer hitting production benchmarks
- Building **offline-first** React Native architecture for TaxBridge mobile
- Researching ZK proof generation performance on constrained hardware

---

<div align="center">

**Battle-tested in Lagos · Running globally · Ready for your most demanding challenges.**

**[View Full Portfolio →](https://scardubu.dev)** • **[Get in touch](mailto:oscar@scardubu.dev)**

*Personal portfolio. All content © Oscar Ndugbu.*

</div>
