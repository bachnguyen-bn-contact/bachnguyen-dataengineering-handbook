# Data quality

## Validate on the way through [Intermediate]

Trustworthy Gold tables start with checks in Silver: enforce types, reject or quarantine bad rows, and assert row counts and key uniqueness before you publish.

## Built-in error logging [Intermediate]

A reusable ELT framework should capture validation failures, log them with context, and surface metadata mappings — so a bad load is visible and diagnosable rather than silent.

> [!CAUTION]
> Silent data quality failures are the expensive kind. Fail loudly, log clearly, and make the last-good state recoverable.

## Where to go next

- [Power BI & Direct Lake](/fabric/powerbi-direct-lake)
- Official: [Data Activator and monitoring](https://learn.microsoft.com/en-us/fabric/data-activator/data-activator-introduction)
