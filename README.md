<h1 align="center">Henry Fernández</h1>
<p align="center">
  <b>Senior Fullstack Engineer &amp; Software Architect</b><br/>
  <sub>Colombia · Available for contract work</sub>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/henryjosefernandez-villarreal/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://henryjfv.github.io/CV/"><img src="https://img.shields.io/badge/Curriculum-1F2328?style=for-the-badge&logo=readdotcv&logoColor=white" alt="CV"/></a>
  <a href="mailto:henryfernandezv@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="https://medium.com/@henryfernandezv"><img src="https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white" alt="Medium"/></a>
</p>

---

I design and build systems for companies that have outgrown their tooling — legacy ERPs with no API, reporting stacks that stopped scaling, manual processes that should have been pipelines.

My work sits at the boundary between **product engineering and data infrastructure**: the application layer people see, and the ingestion, modeling and automation underneath that makes it trustworthy.

<br/>

## 🏛️ How I architect systems

The recurring idea: a **canonical contract** in the middle, adapters at the edges. Sources change, clients change, the model in the middle stays stable.

```mermaid
flowchart LR
    subgraph SRC["🗄️ Sources"]
        A1[Legacy ERP]
        A2[Client databases]
        A3[Documents · XML · PDF]
    end

    subgraph ING["⚙️ Ingestion"]
        B1[Airflow DAGs]
        B2[Adapters per source]
    end

    subgraph CORE["🧩 Canonical model"]
        C1[(PostgreSQL)]
        C2[Redis cache]
    end

    subgraph API["🔌 Contract layer"]
        D1[FastAPI · Django]
        D2[Typed schemas]
    end

    subgraph CLI["📱 Clients"]
        E1[Angular · React]
        E2[Messaging channels]
    end

    A1 --> B2
    A2 --> B2
    A3 --> B1
    B1 --> C1
    B2 --> C1
    C1 <--> C2
    C1 --> D1
    D1 --> D2
    D2 --> E1
    D2 --> E2

    classDef src fill:#2D1B56,stroke:#C8B197,stroke-width:2px,color:#FFFFFF
    classDef ing fill:#1F4E5F,stroke:#7FD1C1,stroke-width:2px,color:#FFFFFF
    classDef core fill:#7A3E1D,stroke:#E5A663,stroke-width:2px,color:#FFFFFF
    classDef api fill:#1E3A5F,stroke:#7FB2E5,stroke-width:2px,color:#FFFFFF
    classDef cli fill:#3D2A5C,stroke:#B49AE0,stroke-width:2px,color:#FFFFFF

    class A1,A2,A3 src
    class B1,B2 ing
    class C1,C2 core
    class D1,D2 api
    class E1,E2 cli
```

<br/>

## 🔄 How an engagement runs

```mermaid
flowchart LR
    S1["🔍 Discovery<br/><sub>constraints, systems, people</sub>"]
    S2["📐 Architecture<br/><sub>options, trade-offs, ADRs</sub>"]
    S3["🔨 Build<br/><sub>iterative, reviewable</sub>"]
    S4["✅ Validation<br/><sub>human checkpoints</sub>"]
    S5["📦 Handover<br/><sub>docs the team can run</sub>"]

    S1 --> S2 --> S3 --> S4 --> S5
    S4 -.->|feedback| S3

    classDef step fill:#2D1B56,stroke:#C8B197,stroke-width:2px,color:#FFFFFF
    class S1,S2,S3,S4,S5 step
```

Decisions get written down. Every non-obvious choice ends up as an ADR — the constraint, the options considered, what was picked and why. Clients keep the reasoning after I leave.

<br/>

## 🛠️ Technologies I work with

<table>
<tr><td><b>Languages</b></td><td>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
<img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white"/>
<img src="https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white"/>
<img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white"/>
</td></tr>

<tr><td><b>Backend</b></td><td>
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white"/>
<img src="https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white"/>
<img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white"/>
<img src="https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white"/>
<img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white"/>
</td></tr>

<tr><td><b>Frontend</b></td><td>
<img src="https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white"/>
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black"/>
<img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white"/>
<img src="https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white"/>
<img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white"/>
</td></tr>

<tr><td><b>Data</b></td><td>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/SQL_Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white"/>
<img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white"/>
<img src="https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white"/>
<img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black"/>
</td></tr>

<tr><td><b>Infra</b></td><td>
<img src="https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white"/>
<img src="https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>
</td></tr>

<tr><td><b>Automation</b></td><td>
<img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white"/>
<img src="https://img.shields.io/badge/Robot_Framework-000000?style=flat-square&logo=robotframework&logoColor=white"/>
<img src="https://img.shields.io/badge/Qdrant-24386C?style=flat-square&logo=qdrant&logoColor=white"/>
<img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white"/>
</td></tr>
</table>

<br/>

## 📂 Selected work

| Project | What it is | Stack |
|---|---|---|
| [`fastapi-grafana-demo`](https://github.com/henryjfv/fastapi-grafana-demo) | Instrumented API service with metrics and dashboards | `Python` `FastAPI` `Grafana` |
| [`mi-alacena`](https://github.com/henryjfv/mi-alacena) | Household inventory tracking app | `TypeScript` |
| [`CV`](https://henryjfv.github.io/CV/) | Full background and engagement history | `Web` |

<br/>

---

<p align="center">
  <sub>Open to freelance and contract engagements</sub><br/>
  <a href="https://www.linkedin.com/in/henryjosefernandez-villarreal/"><img src="https://img.shields.io/badge/Get_in_touch-2D1B56?style=for-the-badge&logo=minutemailer&logoColor=white" alt="Contact"/></a>
</p>
