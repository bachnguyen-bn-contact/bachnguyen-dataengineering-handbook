# PySpark

## Read and write Delta [Basics]

The workhorse for large-scale transformation in Data Engineering notebooks. Distributed DataFrame operations over the lakehouse.

```python
df = spark.read.format("delta").load("Tables/bronze_orders")
clean = df.dropDuplicates(["order_id"]).filter(df.amount > 0)
clean.write.mode("overwrite").saveAsTable("silver_orders")
```

## Fixing data skew [Advanced]

When one partition is far larger than the rest, a few tasks run long while the cluster idles. Diagnose skew in the Spark UI, then redistribute.

```python
# repartition on a higher-cardinality key to even out work
balanced = clean.repartition(200, "customer_id")
```

> [!TIP]
> Repartitioning on a well-chosen key cuts stage-level shuffle and can meaningfully lift throughput on large datasets.

## Where to go next

- [SQL (T-SQL)](/fabric/sql)
- Official: [Use notebooks in Fabric](https://learn.microsoft.com/en-us/fabric/data-engineering/how-to-use-notebook)
