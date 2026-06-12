# Real-Time Intelligence

## Data in motion [Intermediate]

Real-Time Intelligence ingests, stores, queries and acts on streaming data. **Eventstreams** route events, the **Eventhouse** stores them, and **Activator** triggers actions on conditions.

## KQL [Intermediate]

Kusto Query Language queries high-volume event and telemetry data. If you come from a SQL-only background, this is usually the biggest new thing to learn.

```kql
Orders
| where Timestamp > ago(1h)
| summarize revenue = sum(Amount) by Region
| order by revenue desc
```

## Where to go next

- [Security & governance](/fabric/security)
- Official: [Real-Time Intelligence overview](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/overview)
