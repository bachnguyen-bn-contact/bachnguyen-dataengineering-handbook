# SQL (T-SQL)

## Set-based analytics [Basics]

T-SQL is the language of the warehouse and the lakehouse SQL analytics endpoint. Joins, aggregations and window functions — the bread and butter of analytics.

```sql
SELECT region, SUM(amount) AS revenue
FROM gold.sales
WHERE order_date >= '2026-01-01'
GROUP BY region
ORDER BY revenue DESC;
```

## Endpoint vs warehouse [Intermediate]

The lakehouse **SQL analytics endpoint** is read-only over your Delta tables; the **warehouse** supports full read/write T-SQL with transactions. Same language, different write capabilities.

## Where to go next

- [Delta tables & the medallion pattern](/fabric/delta-medallion)
- Official: [Query the SQL analytics endpoint](https://learn.microsoft.com/en-us/fabric/data-engineering/lakehouse-sql-analytics-endpoint)
