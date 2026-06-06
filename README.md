<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=58A6FF&center=true&width=700&lines=Software+Engineer+%7C+MLOps+%7C+Cybersecurity;Building+production-grade+systems+from+Nairobi+🇰🇪;Open+to+collaboration+and+new+opportunities)](https://git.io/typing-svg)

</div>

---

## Ray — Software Engineer & MLOps Practitioner

I'm a full-stack engineer and cybersecurity researcher based in Nairobi, Kenya, with a focus on building production-grade backend systems, ML infrastructure, and secure applications. I care about the operational side of software — systems that are observable, resilient, and maintainable in production, not just demos.

Currently building at the intersection of MLOps and security engineering.

---

## Featured Project

### 🔬 Real-Time ML Model Drift Detection System

> *Production-grade ML monitoring infrastructure — not a notebook, not a demo.*

A fully containerised system that monitors live ML model inference traffic for statistical distribution shift using KL-divergence, PSI, and MMD, then automatically triggers retraining pipelines when drift is detected — with zero human intervention required.

**What it solves:** ML models silently degrade when real-world data distributions shift away from training data. Standard uptime monitoring is completely blind to this. This system detects it within minutes and self-heals.

**Architecture highlights:**
- Kafka-backed inference interceptor captures every feature vector with < 2ms added latency
- Faust-Streaming processor computes drift scores across tumbling windows (1,000 records / 60s)
- Three-layer statistical detection: KL-divergence (continuous features), PSI (categorical + continuous), MMD (multivariate joint distribution — catches correlation shifts the other two miss)
- Redis-backed distributed circuit breaker and alert deduplication (SET NX EX) — safe across multiple replicas
- Airflow DAG auto-retrains, validates F1 score against production model, and promotes via MLflow registry
- FastAPI dashboard with JWT auth, WebSocket live updates, and 13-panel Grafana observability suite
- Automatic baseline registration: new model versions self-register their reference distributions from live traffic — no manual intervention required
- Kubernetes-ready: HPA, NetworkPolicy, PodDisruptionBudget, rolling deployments with zero downtime

**Security controls:** OWASP security headers, rate limiting, bcrypt auth, parameterised SQL, Redis distributed locking, SASL/SSL Kafka, TLS PostgreSQL, non-root containers, read-only root filesystem.

**Stack:** Python 3.11 · FastAPI · Apache Kafka · Faust-Streaming · PostgreSQL · Redis · Airflow · MLflow · Prometheus · Grafana · Docker · Kubernetes · NumPy · SciPy · OpenTelemetry

[![View Repository](https://img.shields.io/badge/View_Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ray123/drift-detector)
[![Live Demo](https://img.shields.io/badge/Live_Demo-58A6FF?style=for-the-badge&logo=vercel&logoColor=white)](https://yourdomain.com)

---

## Tech Stack

#### Languages
![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)

#### Backend & Infrastructure
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)

#### MLOps & Data
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

## Projects

| Project | What it does | Stack | Status |
|---------|-------------|-------|--------|
| [Drift Detector](https://github.com/ray123/drift-detector) | Real-time ML model drift detection, alerting, and auto-retraining | Python, Kafka, FastAPI, K8s | ✅ Production-ready |
| [AI Tools Hub](https://github.com/ray123/ai-tools) | Unified interface for ML/AI tooling | Python, FastAPI | 🔨 Active |
| [React CRM](https://github.com/ray123/crm-react) | Full-featured CRM dashboard | React, Tailwind CSS | ✅ Complete |
| [Hacking Toolkit](https://github.com/ray123/hack-kit) | Ethical hacking and recon scripts | Bash, Python | 🔨 Active |

---

## GitHub Stats

<div align="center">

![Ray's GitHub stats](https://github-readme-stats.vercel.app/api?username=ray123&show_icons=true&theme=github_dark&hide_border=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=ray123&layout=compact&theme=github_dark&hide_border=true)

[![GitHub Streak](https://streak-stats.demolab.com/?user=ray123&theme=github-dark-blue&hide_border=true)](https://git.io/streak-stats)

</div>

---

## Currently

- 🔬 Deepening expertise in distributed systems and ML infrastructure
- 🦀 Learning Rust for systems programming
- 🔐 Researching applied cryptography and network security
- 🌍 Representing the African tech community on the global stage

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_HANDLE)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/YOUR_HANDLE)
[![Website](https://img.shields.io/badge/Website-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://ray.dev)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your@email.com)

![Visitor Count](https://komarev.com/ghpvc/?username=ray123&style=flat-square&color=58A6FF)

---

<div align="center">
<sub>Open to senior engineering roles, MLOps contracts, and cybersecurity consulting. Based in Nairobi — available remotely worldwide.</sub>
</div>
