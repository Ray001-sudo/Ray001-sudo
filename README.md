<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=58A6FF&center=true&width=750&lines=Benson+Ray+%7C+Software+Engineer;MLOps+%7C+Backend+Systems+%7C+Cybersecurity;Building+production-grade+infrastructure+from+Nairobi+🇰🇪)](https://git.io/typing-svg)

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/benson-ray)
[![Website](https://img.shields.io/badge/Website-000000?style=flat-square&logo=vercel&logoColor=white)](https://bensonray.pages.dev/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:bensonray25@gmail.com)
[![Live Demo](https://img.shields.io/badge/Live_Demo-58A6FF?style=flat-square&logo=render&logoColor=white)](https://drift-dashboard-vth9.onrender.com/)
![Profile Views](https://komarev.com/ghpvc/?username=Ray001-sudo&style=flat-square&color=58A6FF&label=profile+views)

</div>

---

## About Me

I'm a software engineer and cybersecurity researcher based in Nairobi, Kenya. My work sits at the intersection of backend engineering, ML infrastructure, and applied security — I build systems that are observable, resilient, and maintainable in production, not just in development.

I care about the operational reality of software: what happens after deployment, how systems behave under failure, and how to make complex distributed infrastructure understandable to the people who run it.

---

## Featured Project — Real-Time ML Model Drift Detection System

> *Production-grade ML monitoring infrastructure. Not a notebook. Not a demo.*

[![View Repository](https://img.shields.io/badge/Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Ray001-sudo/drift-detector)
[![Live Demo](https://img.shields.io/badge/Live_Dashboard-58A6FF?style=for-the-badge&logo=render&logoColor=white)](https://drift-dashboard-vth9.onrender.com/)

### The Problem

ML models silently degrade when real-world data distributions shift away from training data. A model can have 99.9% uptime and zero HTTP errors while producing systematically wrong predictions for weeks. Standard application monitoring is completely blind to this. By the time business metrics reflect the degradation, the damage is done.

### What This System Does

A fully containerised, self-healing ML monitoring system that detects distribution shift in live inference traffic within minutes and responds autonomously — no human intervention required.

**Statistical detection layer** — three complementary methods, each catching what the others miss:

| Method | What it catches | Threshold |
|--------|----------------|-----------|
| **KL-Divergence** | Continuous feature distribution shape changes | > 0.15 |
| **PSI** | Both continuous and categorical individual feature shifts | > 0.20 |
| **MMD** | Joint multivariate drift — correlation shifts KL and PSI miss entirely | p < 0.05 |

**Infrastructure highlights:**
- Kafka-backed inference interceptor adds < 2ms latency to every prediction request
- Faust-Streaming processor computes drift scores on tumbling windows (1,000 records or 60 seconds)
- Redis-backed distributed circuit breaker — state shared across replicas, never in-process memory
- Alert deduplication via atomic `SET NX EX` — prevents alert storms across multiple alerter replicas
- Airflow DAG fetches fresh data, retrains, validates F1 against production model, and promotes via MLflow registry — fully automated
- Auto baseline registration: new model versions self-register reference distributions from live traffic
- FastAPI dashboard with JWT auth, WebSocket live updates, asyncio-safe broadcast with heartbeat/ping
- 13-panel Grafana observability suite with Prometheus scraping all services
- Kubernetes-ready: HPA, NetworkPolicy, PodDisruptionBudget, zero-downtime rolling deployments

**Security:** OWASP headers · JWT + bcrypt (factor 12) · SlowAPI + Redis rate limiting · Parameterised SQL · SASL/SCRAM-512 Kafka · TLS PostgreSQL · Non-root containers · RBAC · Full audit log

**Stack:** `Python 3.11` `FastAPI` `Kafka` `Faust-Streaming` `PostgreSQL 16` `Redis 7` `Airflow` `MLflow` `Prometheus` `Grafana` `Docker` `Kubernetes` `NumPy` `SciPy` `OpenTelemetry`

---

## Other Projects

| Project | Description | Stack | Status |
|---------|-------------|-------|--------|
| [Sovereign Root Protocol](https://github.com/Ray001-sudo/domain-generator) | Cryptographically secure, censorship-resistant domain ownership protocol on a P2P ledger | Rust, TypeScript, Libp2p | 🔨 Active |
| [POS Platform](https://github.com/Ray001-sudo/pos) | Multi-tenant point-of-sale system with offline-first C++ client and cloud sync | C++, Python, JavaScript, Tailwind | ✅ Complete |
| [Shule360](https://github.com/Ray001-sudo/S.M.SY) | Dual-curriculum school management platform for Kenyan boarding schools (8-4-4 + CBC/CBE) | Next.js, Node.js, Python, PostgreSQL | 🔨 Active |

---

## Tech Stack

#### Languages
![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)

#### Backend & Infrastructure
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)

#### MLOps & Observability
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white)
![Apache Airflow](https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

#### Security & Frontend
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white)

---

## GitHub Stats

<div align="center">

<a href="https://github.com/Ray001-sudo">
  <img height="180em" src="https://github-readme-stats-eight-theta.vercel.app/api?username=Ray001-sudo&show_icons=true&theme=github_dark&hide_border=true&count_private=true&include_all_commits=true&rank_icon=github" />
  <img height="180em" src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=Ray001-sudo&layout=compact&theme=github_dark&hide_border=true&langs_count=8&exclude_repo=github-readme-stats" />
</a>

<br/><br/>

[![GitHub Streak](https://streak-stats.demolab.com/?user=collabray&theme=github-dark-blue&hide_border=true&date_format=j%20M%5B%20Y%5D)](https://git.io/streak-stats)

<br/>

![collabray's Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=collabray&theme=github-compact&hide_border=true&area=true&color=58A6FF&line=58A6FF&point=FFFFFF)

</div>

---

## Currently

- Deepening expertise in distributed systems and production ML infrastructure
- Learning Rust for systems-level programming
- Researching applied cryptography and network security
- Building in public and representing the African engineering community globally

---

<div align="center">
<sub>Open to senior engineering roles, MLOps contracts, and cybersecurity consulting engagements.</sub>
<br/>
<sub>Based in Nairobi, Kenya — available remotely worldwide.</sub>
</div>
