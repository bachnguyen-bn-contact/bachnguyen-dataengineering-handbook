# Power BI & Direct Lake

## Semantic models [Basics]

Power BI is the serving layer. Semantic models define the measures (in DAX) and relationships that reports and stakeholders consume.

```dax
Total Revenue = SUMX( Sales, Sales[Quantity] * Sales[UnitPrice] )
```

## Direct Lake [Intermediate]

Direct Lake is a storage mode that reads Delta/Parquet **straight from OneLake** — close to import speed without a separate refresh, and fresher than DirectQuery. A strong default for models built on lakehouse or warehouse tables.

> [!TIP]
> Build Gold tables with reporting in mind (right grain, clean keys) and Direct Lake models stay fast with little tuning.

## Where to go next

- [Real-Time Intelligence](/fabric/realtime)
- Official: [Direct Lake overview](https://learn.microsoft.com/en-us/fabric/fundamentals/direct-lake-overview)
