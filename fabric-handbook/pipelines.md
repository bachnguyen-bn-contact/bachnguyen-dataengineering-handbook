# Pipelines & ingestion

## Data pipelines [Basics]

Pipelines (the Fabric Data Factory experience) orchestrate work: copy activities, notebook runs, dataflows, stored procedures, and control flow with conditions and loops. They are how you schedule and chain the steps of an end-to-end load.

## Dataflows Gen2 [Basics]

Dataflows Gen2 give a low-code, Power Query interface for transforming data on the way in — handy for analysts and for lighter shaping that does not need Spark.

## Orchestration choices [Intermediate]

| Need | Reach for |
|---|---|
| Schedule and chain steps | **Pipeline** |
| Low-code transforms | **Dataflow Gen2** |
| Heavy/custom transforms | **Spark notebook** |

> [!TIP]
> A common pattern: a pipeline triggers a notebook for transformation, then a second activity refreshes a semantic model — all on a schedule or an event trigger.

## Where to go next

- [Connecting to sources](/fabric/connect)
- Official: [Data Factory in Fabric](https://learn.microsoft.com/en-us/fabric/data-factory/data-factory-overview)
