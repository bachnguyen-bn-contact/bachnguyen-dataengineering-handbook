# Delta tables & the medallion pattern

## Delta as the table format [Basics]

Fabric tables are Delta (Parquet plus a transaction log), giving ACID writes, time travel and schema enforcement over files in OneLake. Both Spark and SQL read the same Delta tables.

## Bronze, Silver, Gold [Basics]

Most lakehouse designs organise data into quality tiers:

- **Bronze** — raw, landed as-is, full history. Your replayable record.
- **Silver** — cleansed, de-duplicated, conformed into consistent entities.
- **Gold** — aggregated, business-ready tables and semantic models for consumption.

> [!NOTE]
> Keep Bronze append-only. If a downstream layer has a bug, you can always reprocess from Bronze rather than re-ingesting from the source.

## Keeping tables healthy [Advanced]

Compact small files and tidy history so reads stay fast.

```sql
OPTIMIZE silver_orders;
VACUUM silver_orders RETAIN 168 HOURS;
```

## Where to go next

- [Data quality](/fabric/data-quality)
- Official: [Delta Lake table optimization](https://learn.microsoft.com/en-us/fabric/data-engineering/delta-optimization-and-v-order)
