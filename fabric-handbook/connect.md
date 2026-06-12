# Connecting to sources

## Connectors [Basics]

Fabric ships hundreds of connectors for databases, SaaS apps, files and cloud storage. The copy activity in a pipeline and the source step in a Dataflow Gen2 both draw from the same connector library.

## On-premises data [Intermediate]

To reach data behind your firewall, install the **on-premises data gateway** and reference it from your connection. It brokers traffic securely between Fabric and the source.

## Authentication [Intermediate]

> [!CAUTION]
> Prefer managed identities, service principals or OAuth over embedding credentials. Store secrets in a vault, not in notebook cells or pipeline parameters.

## Where to go next

- [PySpark](/fabric/pyspark) — transform what you have ingested.
- Official: [Connectors in Fabric](https://learn.microsoft.com/en-us/fabric/data-factory/connector-overview)
