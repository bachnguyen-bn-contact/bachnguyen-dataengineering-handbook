# OneLake shortcuts vs mirroring

When you need data that lives *outside* your Fabric workspace, the instinct is to write a copy job. Often you don't have to. Fabric gives you two ways to bring outside data in without standing up your own pipeline: **shortcuts** and **mirroring**. They solve overlapping problems but in different ways.

## Shortcuts: reference in place

A shortcut is a pointer. It makes data that already exists somewhere — another OneLake location, ADLS, Amazon S3, Google Cloud Storage — appear inside your lakehouse as if it were local. Nothing is copied; you're reading the source bytes through a link.

Reach for a shortcut when:

- the data already sits in a lake you can reach, and
- you want to query it *as it is right now*, with no duplication.

The catch: you're at the mercy of the source's availability and format. If the source is slow or goes away, so does your shortcut.

## Mirroring: a synced copy in open format

Mirroring targets **operational databases** — Azure SQL, Cosmos DB, Snowflake and friends. It replicates the database into OneLake and keeps it in near-real-time sync, landing the data in open Delta format ready for analytics.

Reach for mirroring when:

- the source is a transactional database, not a lake, and
- you want analytics-ready data without building and operating change-data-capture yourself.

The catch: it *is* a copy (a managed one), so it has its own freshness characteristics and lands as a replicated dataset rather than a live pointer.

## A quick decision

| Question | Lean towards |
|---|---|
| Is the source already a data lake? | **Shortcut** |
| Is the source a transactional database? | **Mirroring** |
| Do you want zero duplication? | **Shortcut** |
| Do you want a resilient, synced analytics copy? | **Mirroring** |

Both beat hand-rolling an ingestion job for these cases. Start by asking *what the source actually is* — that usually answers the question for you.
