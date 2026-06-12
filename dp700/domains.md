# The three domains

DP-700 is split into three **equally weighted** domains, each worth roughly **30–35%** of the exam. That even split is a strategy in itself: you can't afford to skip any one of them.

## 1. Implement and manage an analytics solution

The foundational setup and governance layer of Fabric. Expect questions on:

- **Workspace configuration** — Spark settings, domain settings, OneLake settings.
- **Lifecycle management** — Git integration, deployment pipelines, database projects (CI/CD for Fabric items).
- **Security and governance** — workspace- and item-level access, row-/column-/object-level security, dynamic data masking, sensitivity labels, OneLake security.
- **Orchestration** — when to use Dataflow Gen2 vs. pipelines vs. notebooks; event-based triggers and scheduling.

## 2. Ingest and transform data

The core data engineering domain — getting data in and shaping it, for both batch and streaming patterns:

- **Loading patterns** — full loads vs. incremental/upsert; choosing the right strategy.
- **Batch** — pipelines, Dataflows Gen2, and Spark notebooks (PySpark / Spark SQL).
- **Streaming** — Eventstreams and Real-Time Intelligence, querying with **KQL**.
- **Transformation** — cleaning, conforming and modelling data across the medallion tiers.

## 3. Monitor and optimise an analytics solution

Keeping the solution healthy once it's running:

- **Monitoring** — tracking pipeline and item runs, capacity usage, and failures.
- **Troubleshooting** — diagnosing failed or slow workloads.
- **Optimisation** — performance tuning across Spark, SQL and the lake (file sizes, partitioning, query patterns).

## How to read this

Map every bullet in the official *"Skills Measured"* list to something you've actually clicked through in a Fabric trial. The exam rewards hands-on familiarity far more than memorised definitions.

## Where to go next

- **[Study plan & advice](/dp700/study-plan-and-advice)** — turn these domains into a schedule.
