<h1 align="center">Henry Fernández</h1>
<p align="center"><b>Senior Fullstack Engineer &amp; Software Architect</b><br/>
<sub>Colombia · Available for contract work</sub></p>

<p align="center">
  <a href="https://www.linkedin.com/in/henryjosefernandez-villarreal/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://henryjfv.github.io/CV/"><img src="https://img.shields.io/badge/CV-1f2328?style=flat-square&logo=readdotcv&logoColor=white" alt="CV"/></a>
  <a href="mailto:TU_EMAIL_AQUI"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"/></a>
</p>

---

I design and build systems for companies that have outgrown their tooling — legacy ERPs with no API, reporting stacks that stopped scaling, manual processes that should have been pipelines.

Most of my work sits at the boundary between **product engineering and data infrastructure**: the application layer people see, and the ingestion, modeling and automation underneath that makes it trustworthy.

**What I typically own on an engagement**

- Architecture decisions, documented — trade-offs, constraints and the reasoning behind them, not just the outcome
- Backend and API design: Python/FastAPI, Django, Node.js/TypeScript
- Frontend delivery: Angular, React
- Data platform work: PostgreSQL, SQL Server, Airflow, Redis, BI replacement and migration
- Process automation where no integration point exists: RPA, document extraction, scheduled workers

### How I usually structure things

```mermaid
flowchart LR
    A[Source systems<br/>ERP · client DBs · files] --> B[Ingestion<br/>Airflow · workers]
    B --> C[(Canonical model<br/>PostgreSQL)]
    C --> D[API layer<br/>FastAPI · Django · typed contracts]
    D --> E[Clients<br/>Angular · React · messaging]
    C -.-> F[Cache<br/>Redis]
    F -.-> D
```

The recurring idea: a **canonical contract** in the middle, with adapters at the edges. Sources change, clients change, the model in the middle stays stable.

### Selected work

| Project | What it is |
|---|---|
| [`fastapi-grafana-demo`](https://github.com/henryjfv/fastapi-grafana-demo) | Instrumented FastAPI service with metrics and Grafana dashboards |
| [`mi-alacena`](https://github.com/henryjfv/mi-alacena) | TypeScript app for household inventory tracking |
| [`CV`](https://henryjfv.github.io/CV/) | Full background and engagement history |

### Stack

**Languages** — TypeScript · Python · JavaScript · Java · Dart · SQL
**Backend** — FastAPI · Django · Node.js/Express · REST · Pydantic
**Frontend** — Angular · React · Vue · Flutter
**Data** — PostgreSQL · SQL Server · Airflow · Redis · Power BI
**Infra** — AWS · Azure · Docker · GitHub Actions

---

<p align="center"><sub>Open to freelance and contract engagements · <a href="https://www.linkedin.com/in/henryjosefernandez-villarreal/">Get in touch</a></sub></p>
