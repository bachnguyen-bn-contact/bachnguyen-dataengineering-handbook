# Lakehouse & Warehouse

## Lakehouse [Basics]

A lakehouse combines the flexibility of a data lake with warehouse-style analytics. You can work with the same Delta tables two ways: **Spark** (notebooks in PySpark, Scala or Spark SQL) for heavy transformation, and the read-only **SQL analytics endpoint** for T-SQL queries.

## Warehouse [Basics]

The warehouse is a full T-SQL experience with transactional (ACID) guarantees and write support — aimed at engineers and analysts who prefer set-based SQL development.

## Which one? [Intermediate]

> [!NOTE]
> Reach for the **lakehouse** when the work is Spark- and file-centric; reach for the **warehouse** when it is T-SQL- and table-centric. Both store data in OneLake, so you are never locked into one.

## Where to go next

- [Delta tables & the medallion pattern](/fabric/delta-medallion)
- Official: [Lakehouse vs warehouse decision guide](https://learn.microsoft.com/en-us/fabric/fundamentals/decision-guide-lakehouse-warehouse)
