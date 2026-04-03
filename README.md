# Valery Lobachev · CTO & Enterprise Architect

**Information & AI Systems Architect · SAP FI/CO Lead Consultant · S/4HANA · Open Source**

Moscow, Russia · Remote · [valery@lobachev.biz](mailto:valery@lobachev.biz) · [lobachev.biz](https://www.lobachev.biz) · [LinkedIn](https://www.linkedin.com/in/valery-lobachev-6024a122/)

---

## About

I am an enterprise architect and CTO with **25+ years** at the intersection of business consulting and software engineering. My work spans two domains that rarely meet: **SAP FI/CO / S/4HANA transformation** and **modern distributed systems architecture** — Microservices, Event-Driven, AI/ML.

Today I design multi-agent AI systems, LLM-based document processing pipelines, and ML demand forecasting platforms — while consulting on the most complex SAP CO configurations. I have delivered enterprise systems across manufacturing, FMCG, energy, railways, and finance sectors, with international project experience in **4+ countries** (BAT Africa rollout across 20+ nations, CIS region, Eastern Europe).

---

## 🔑 Core Competencies

| Domain | Technologies & Skills |
|---|---|
| **IS Architecture** | Microservices, EDA, Event Sourcing, CQRS, API-First, RBAC/ABAC/ReBAC, ADR |
| **AI Systems** | Multi-Agent AI, LangChain, LangGraph, vLLM, MLFlow, Prophet, XGBoost, ARIMA |
| **SAP CO / FI** | CO-PC-ACT, CO-PA, CO-PCA, CO-OM, FI-GL/AR/AP/AA/FM, Parallel Valuations (IFRS) |
| **S/4HANA** | Conversion (Discovery → Realization), Fit-Gap, SAP Activate, S/4HANA Finance |
| **Languages** | Scala · Kotlin · Java · Python · Golang · Rust · TypeScript |
| **Infra & DevOps** | Docker · Kubernetes · Kafka · Keycloak · Gitlab CI/CD · Helm |

---

## 🏗️ Open Source Projects

### [`data-dictionary-builder`](https://github.com/valerylobachev/data-dictionary-builder) &nbsp;·&nbsp; Scala &nbsp;·&nbsp; ⭐ 15

**The Single Source of Truth for Your Data Model: Description, Code Generation, and Documentation.**

Define your entire data model once in a typed **Scala DSL** and generate everything from it automatically:

- `SQL DDL` scripts for PostgreSQL and ClickHouse
- Entity code for **Kotlin** and **Go** (GORM, SQLx)
- Technical documentation in **Excel**
- Database schema diagrams in **DBML** format for [dbdiagram.io](https://dbdiagram.io)
- Excel import/export templates

Eliminates the drift between code, database schema, and documentation. Used in production enterprise projects with 600+ tables.

```scala
object OrderDomain {
  val data = domain("Order", "Order model", "Model for simple order management system.")
    .withTables(
      table("Order", "Order")
        .withPK("id" :# "OrderId")
        .withFields(
          "orderDate" :# date :@ "Date of order" :== "CURRENT_DATE",
          dataElementTableField("CustomerId"),
        )
        .withRelations(
          manyToOne("customerId", "Reference to customer", "Customer", "customerId" -> "id")
        )
    )
}
```

---

### [`bench-pg`](https://github.com/valerylobachev/bench-pg) &nbsp;·&nbsp; Rust &nbsp;·&nbsp; Go ·&nbsp; ⭐ 1

**Cross-language PostgreSQL benchmarking suite** designed to measure and compare the performance of different database driver libraries under a realistic, business-like workload.

- Benchmarks PostgreSQL drivers across **multiple languages** side by side
- Realistic workload patterns (not just synthetic TPC-B)
- Written in **Rust** and **Go** for precise, low-overhead measurement
- Useful for choosing the right ORM/driver stack for your production system

---

### [`hdfs-replicator`](https://github.com/valerylobachev/hdfs-replicator) &nbsp;·&nbsp; Go &nbsp;·&nbsp; ⭐ 3

**Tool to replicate files from an HDFS source path to a local destination**, excluding previously copied files. Built during production Big Data work (Hadoop/Spark ML pipelines for predictive maintenance systems).

---

## 🏢 Annette Platform Ecosystem

The **[Annette Platform](https://github.com/annetteplatform/annette)** (`annetteplatform` org) is my main open source initiative — a production-grade distributed microservice platform for building enterprise applications.

**Battle-tested in production:**
- **TELE2 Logistics System** — ~700 users, SAP ERP on HANA integration
- **MIMC Application Processing System** — Moscow International Medical Cluster
- **MVideo-Eldorado Intranet Portal** — 50,000+ employees · 🏆 **[Intranet 2020 Award](https://www.intranetaward.com/)**

**Architecture highlights:**
- Reactive / non-blocking throughout (Akka, Lagom, Pekko)
- Multi-instance Akka Cluster per microservice for HA and horizontal scaling
- Cloud-native: Docker, Kubernetes, OKD, Helm, Istio
- Auth: Keycloak with RBAC, ABAC, and ReBAC
- Data: Cassandra, PostgreSQL, OpenSearch, Kafka, Minio
- Frontend: Vue, React, SAP UI5 for React, Zustand

```
Scala / Akka / Lagom · Golang / go-zero / GORM · Rust / Axum
PostgreSQL · Cassandra · OpenSearch · Kafka · Minio
Docker · Kubernetes · Keycloak · Gitlab CI/CD
```

---

## 💼 Selected Enterprise Projects

| Year | Project | Role | Stack |
|---|---|---|---|
| 2026 | Multi-Agent AI Sales Forecasting System | Architect / Dev | Python, LangGraph, vLLM, MLFlow |
| 2026 | AI Application Processing System (LLM) | Architect / Dev | Go, Kafka, Python, React/SAP UI5 |
| 2023–25 | RZhD Wagon Management System (SAP PM replacement) | Chief Architect | Kotlin, Spring Boot, Kafka, K8s |
| 2021–23 | Pre-Failure Monitoring & Predictive Maintenance | Architect | Hadoop, Spark, Scala, Akka, Kafka |
| 2021 | SAP ECC → S/4HANA Conversion (Discovery Phase) | FI/CO Architect | SAP ECC, S/4HANA |
| 2019–21 | MVideo-Eldorado Intranet Portal 🏆 | Chief Architect | Scala, Akka, K8s, Kafka, Keycloak |
| 2018–19 | Rosneft Digital Transformation Architecture | Solution Architect | SAP, Hadoop, AI/ML concepts |
| 2014–16 | BAT Global SAP Rollout — 20+ countries | Lead FI/CO Consultant | SAP CO, IFRS parallel valuations |

---

## 🎓 Education & Certifications

- **SAP Certified Application Professional** — Financials in SAP S/4HANA (2021)
- **SAP Certified Application Associate** — FI/CO (2006)
- **CMA** (Certified Management Accountant) — 3/4 exams · IMA
- **Sun Certified Java Programmer** (SCJP)
- **M.Sc. Applied Mathematics** — MEPHI, Faculty of Cybernetics (1994–2000)
- **MBA** — Financial Management · Synergy Institute / Plekhanov REA (2004–2006)
- **MIT Sloan** — Finance & Management Accounting (OpenCourseWare, 2004–2006)

---

## 📬 Contact

| | |
|---|---|
| Email | [valery@lobachev.biz](mailto:valery@lobachev.biz) |
| LinkedIn | [linkedin.com/in/valery-lobachev-6024a122](https://www.linkedin.com/in/valery-lobachev-6024a122/) |
| Website | [lobachev.biz](https://www.lobachev.biz) |
| Location | Moscow, Russia · Available Remote |

---

<sub>Open to architecture consulting, SAP FI/CO & S/4HANA transformation projects, and AI system design engagements.</sub>
