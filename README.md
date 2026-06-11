# Bach Nguyen — Data Engineer

Personal site: **[bachnguyen.netlify.app](https://bachnguyen.netlify.app)**

## About me

I'm a Data Engineer with 2+ years designing ELT pipelines, dimensional data models, and
analytics solutions at enterprise scale. Most of my work lives in **PySpark and SQL** across
**AWS and Azure** — these days largely on **Microsoft Fabric** — and I've processed 50TB+ of
data across 700+ tables. I care about building data platforms teams can actually trust:
clear validations, sensible governance, and pipelines that fail loudly instead of silently.

Currently an **Analytics Engineer II at CoxHealth** in Springfield, MO, where I've architected
a Workday-to-Microsoft Fabric ELT platform processing 50M+ records/day, migrated 1.5B+ records
off legacy systems, and helped retire tools like Snowflake while cutting costs and delivery time.

I hold the **DP-700 (Microsoft Certified: Fabric Data Engineer Associate)** certification, and
this site is where I keep my working notes on all of it.

## What's on the site

- **Fabric Handbook** — what Microsoft Fabric is and the patterns that show up in every project (OneLake, lakehouse vs warehouse, pipelines, PySpark, SQL, Delta/medallion, Direct Lake, Real-Time Intelligence, security, CI/CD).
- **DP-700 Handbook** — a curated route to the Fabric Data Engineer Associate cert: exam shape, the three domains, official resources, and a study plan.
- **Blog** — notes and write-ups as I learn.
- **Resume** — my full background, also downloadable as a PDF.

## Skills

**Languages:** Python, SQL
**Processing & BI:** Apache Spark, dbt, Apache Airflow, SSMS, Data Factory, AWS QuickSight, Power BI, Tableau
**Cloud:** AWS (S3, Glue, Redshift, Lambda), Microsoft Azure (Fabric, Databricks)
**Certification:** DP-700 — Microsoft Certified: Fabric Data Engineer Associate

## Contact

- **Book a 1-on-1:** https://calendly.com/bachnguyen-bn-contact/1-on-1-meeting-with-bach
- **LinkedIn:** https://linkedin.com/in/ben1203/
- **GitHub:** https://github.com/bachnguyen-bn-contact
- **Email:** bachthebusiness@gmail.com

---

## About this site (for me)

A single self-contained `index.html` — all styles, scripts, and content are inline, so there are
no separate asset files that can fail to load. It uses clean URLs via the History API
(`/home`, `/fabric/onelake`, `/dp700/exam-overview`, `/resume`); the `_redirects` file tells
Netlify to serve `index.html` for any path so deep links and refreshes work.

**Deploy:** push this folder to the GitHub repo connected to Netlify (auto-deploys), or drag the
whole `bach-site` folder onto Netlify. Keep `index.html`, `_redirects`, and
`Bach_Nguyen_Resume.pdf` together so the Resume download works.

**Light-mode palette** is adapted from a friend's Fabric guide (CoxHealth blue on white), with
my own navy dark mode. Fabric/DP-700 content is summarised from Microsoft Learn and linked there;
this site is independent and not affiliated with or endorsed by Microsoft.
