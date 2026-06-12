# What Microsoft Fabric is

## The one-platform idea [Basics]

Microsoft Fabric is a unified, software-as-a-service (SaaS) analytics platform. Instead of stitching together separate products for ingestion, storage, transformation and reporting, Fabric brings those stages into one environment that runs on shared compute and a shared store.

The practical payoff: data and artifacts move between workloads **without being copied**. A table written by a Spark notebook can be queried by the SQL endpoint, modelled in Power BI, and acted on in Real-Time Intelligence — all over the same physical data.

## The workloads [Basics]

| Workload | What it's for |
|---|---|
| **Data Factory** | Pipelines and Dataflows Gen2 for ingesting and orchestrating data. |
| **Data Engineering** | Spark notebooks and lakehouses for large-scale transformation. |
| **Data Warehouse** | A transactional T-SQL warehouse for set-based analytics. |
| **Real-Time Intelligence** | Eventstreams, Eventhouse and KQL for data in motion. |
| **Data Science** | Notebooks, experiments and models, with semantic link to Power BI. |
| **Power BI** | Semantic models and reports — the serving layer. |

> [!NOTE]
> Fabric ships updates monthly, so it pays to track what is in **preview** versus **generally available** before you depend on a feature.

## Where to go next

- [OneLake](/fabric/onelake) — the single store everything sits on.
- Official: [What is Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/fundamentals/microsoft-fabric-overview)
