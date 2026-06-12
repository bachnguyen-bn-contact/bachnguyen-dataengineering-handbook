# OneLake

## One copy of the data [Basics]

OneLake is the single, tenant-wide data lake, built on open Delta/Parquet formats over ADLS Gen2. There is **one logical copy** of the data, and every workload reads and writes that same store. Think of it as "OneDrive for data" — provisioned automatically, with no infrastructure to stand up.

## Shortcuts [Intermediate]

A shortcut is a pointer that surfaces data living elsewhere — another OneLake location, ADLS, Amazon S3, Google Cloud Storage — as if it were local. The data is **referenced in place**, not copied, so there is no duplication and no sync job to maintain.

> [!TIP]
> Use a shortcut when the data already lives in a lake you can reach and you want it queryable now, with zero duplication.

## Mirroring [Intermediate]

Mirroring brings an external operational database (Azure SQL, Cosmos DB, Snowflake) into OneLake and keeps it in **near-real-time sync**, landing it in open format — without you building change-data-capture by hand.

## Where to go next

- [Lakehouse & Warehouse](/fabric/lakehouse-warehouse) — the two ways to work with OneLake data.
- Official: [OneLake documentation](https://learn.microsoft.com/en-us/fabric/onelake/onelake-overview)
