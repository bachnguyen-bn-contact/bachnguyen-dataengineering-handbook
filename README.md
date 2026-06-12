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

## Repository structure

Each topic now lives in its own folder of Markdown files, so content is easy to edit and
expand without touching `index.html`. The page loads each note at runtime via `fetch()`.

```
index.html                 # the whole app (HTML + CSS + JS); content is NOT inlined
README.md
_redirects                 # Netlify SPA routing
assets/                    # resume PDF, images, and other static files
  Bach_Nguyen_Resume.pdf
fabric-handbook/           # Fabric Handbook — one .md per section
  what-is-fabric.md
  onelake.md
  lakehouse-warehouse.md
  ... (etc.)
dp700/                     # DP-700 Handbook — one .md per section
  exam-overview.md
  domains.md
  ... (etc.)
blog/                      # Blog — one .md per post
  welcome.md
  onelake-shortcuts-vs-mirroring.md
```

The list of topics and the order of sections is controlled by the `window.SITE` object near
the top of `index.html`. Each category has a `dir` (its folder) and a list of `articles`,
and each article's file is `<dir>/<slug>.md`.

### Add a new section to an existing handbook

1. Drop a new Markdown file in the topic folder, e.g. `fabric-handbook/medallion-tips.md`.
2. Add an entry to that category's `articles` array in `window.SITE`:
   ```json
   { "slug": "medallion-tips", "title": "Medallion tips", "summary": "Short blurb." }
   ```
   (The file is resolved automatically as `fabric-handbook/medallion-tips.md`.)

### Add a brand-new topic (handbook)

1. Create a folder, e.g. `spark-handbook/`, and add your `.md` files.
2. Add a category to `window.SITE.categories`:
   ```json
   {
     "id": "spark", "title": "Spark Handbook", "kind": "handbook",
     "dir": "spark-handbook", "blurb": "Notes on Apache Spark.",
     "articles": [ { "slug": "intro", "title": "Intro", "summary": "..." } ]
   }
   ```
   Any category with `"kind": "handbook"` is added to the **Topics** dropdown in the nav
   automatically. Categories with `"kind": "blog"` stay as a top-level link.

### Markdown notes

Supported: headings, **bold**/*italic*, `inline code`, fenced code blocks, tables,
ordered/unordered lists, task lists, blockquotes, and GitHub-style callouts
(`> [!NOTE]`, `> [!TIP]`, `> [!WARNING]`, `> [!CAUTION]`). A trailing
`[Basics]` / `[Intermediate]` / `[Advanced]` on a heading renders as a colored badge.

> Because notes are fetched at runtime, the site must be served over HTTP. It works on
> Netlify (or any static host) and on a local server (`python -m http.server`). Opening
> `index.html` directly from disk with `file://` will not load the topic content.

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

## About my site
This site is independent and not affiliated with or endorsed by Microsoft.
