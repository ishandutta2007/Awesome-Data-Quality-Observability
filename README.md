# Awesome-Data-Quality-Observability

## Top Data Quality & Observability Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Automated Anomaly Detection, Data Contracts & Pipeline Testing*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Quality & Observability**. These tools enable data teams to detect, triage, and resolve data issues before they impact downstream dashboards, models, or business decisions—from ML-powered anomaly detection that learns what "normal" looks like to declarative testing frameworks that enforce data contracts in CI/CD.



**Examples** include Monte Carlo, Bigeye, IBM Databand, Acceldata, Soda, Great Expectations, Anomalo, Metaplane, Telmai, and Lightup (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, declarative data testing, and open observability infrastructure—ideal for data engineers, analytics teams, and organizations seeking transparent, vendor-independent data reliability.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms

| Platform | Company Scale (Valuation / Revenue) | Starting Pricing Tier | Free Tier / Trial Limits | Key Capabilities & Best For |
| :--- | :--- | :--- | :--- | :--- |
| **IBM Databand** | **~$215B Market Cap** (Parent IBM; ~$150M Databand acquisition) | **~$450/month** (Essentials tier baseline via IBM Cloud/watsonx, scaling to $1,750+/mo) | **30-day free trial** (Full feature access via IBM Cloud / watsonx.data; no permanent free plan) | Observability software for data pipelines (DAGs, runs, tasks) and warehouses with hourly snapshots, run live views, and self-hosted deployment options. Best for IBM ecosystem users. |
| **Monte Carlo** | **$1.6B Valuation** (Series D unicorn; $236M+ raised) | **~$25,000 – $50,000/year** (Baseline entry/AWS Marketplace package; Start tier covers up to 10 users & 1,000 monitors) | **14 to 30-day POC / Pilot** (Tailored evaluation on 1–3 warehouses/lakes and subset of critical tables; no permanent free plan) | Leading data + AI observability platform across warehouses, lakes, BI, and AI agents with GraphQL/Push Ingest APIs and 56-tool MCP server. Best for end-to-end enterprise coverage. |
| **Acceldata (ADOC)** | **~$360M Valuation** (Series C; $106M+ raised) | **~$100,000/year** (Enterprise platform tier based on compute/volume starting ~$0.20/GB or TB/month units) | **30-day free trial** (Full access to data observability cloud, automated scanning, and policies; no permanent free plan) | Data Observability Cloud with Agentic Data Management (ADM) providing natural-language incident drilldowns, 60+ data connectors, and drift/reconciliation policies. Best for guided incident RCA. |
| **Bigeye** | **~$180M Valuation** (Series B; $68.5M+ raised) | **~$45,000/year** (Entry AWS Marketplace tier covering up to 100 actively monitored tables; $75,000/yr for 300 tables) | **14 to 30-day Proof of Concept (PoC)** (Hands-on evaluation scoped to target warehouse connectors and sample CDEs; no permanent free plan) | Enterprise data observability with deep legacy connector support (Informatica, DB2, SSIS, DataStage), bigAI incident copilot, and cross-database join rules. Best for enterprise legacy migrations. |
| **Anomalo** | **~$165M Valuation** ($100M–$250M range; $72M+ raised) | **~$58,000/year** (Entry tier via AWS Marketplace / Vendr median ~$115k/yr based on monitored table count) | **14 to 30-day enterprise pilot / POC** (Scoped evaluation on up to 50–100 production tables with full ML anomaly detection; no permanent free plan) | AI-native enterprise data quality with unsupervised ML across structured, semi-structured, and unstructured data, backed by Databricks and Snowflake. Best for zero-rule automated ML profiling. |
| **Soda (Soda Cloud)** | **~$70M Valuation** ($27.9M raised; $14M 2024 round) | **$750/month** (Team tier, includes core platform features and base SPUs; previously $8/dataset/mo) | **Free-forever plan: Up to 3 production datasets** (Includes pipeline testing, metrics observability, and alerting; unlimited time) | AI-native automated data quality platform with SodaCL checks-as-code, no-code rule builder, and self-serve dataset monitoring. Best for transparent modular adoption. |
| **Metaplane** | **~$50M Valuation** ($23M raised; Series A led by Felicis) | **$10/monitored table/month** (Pro tier; minimum spend commonly starts at ~$500/month with 12 users) | **Free-forever plan: Up to 10 monitored tables & 4 users** (Includes automated anomaly detection, schema tracking; also offers a 14-day Pro trial) | ML-based anomaly detection with end-to-end column-level lineage and Chrome extension to verify dashboard data directly in BI tools. Best for fast 30-minute setup and BI integration. |
| **Telmai** | **~$25M Valuation** ($11.3M raised; YC alum & Seed led by Glasswing) | **~$25,000 – $50,000/year** (Entry annual contract based on in-place query units and data source volume) | **14-day guided trial / sandbox** (Hands-on evaluation environment connecting to sample cloud warehouse or private VPC; no permanent free plan) | AI-powered data observability for agentic workflows with continuous validation (structured/unstructured), zero-copy decoupled metrics, and MCP-compliant server. Best for agentic AI pipelines. |
| **Lightup** | **~$20M Valuation** ($9.0M raised; Series A led by a16z) | **~$24,000 – $36,000/year** (Cloud annual subscription baseline; custom Enterprise tier for hybrid/on-prem) | **30-day cloud trial** (Demo workspace sandbox capped at 5 users and sample warehouse connections; no permanent free plan) | Next-generation data quality with automatic data profiling, SQL/no-code custom metrics, slicing, and native Claude Code MCP integration. Best for flexible metric slicing and MCP agent access. |



## Open-Source GitHub Projects



- **Great Expectations (GX)**  

  **Shared, open standard for data quality** (Apache-2.0) — **the most widely adopted open-source data testing framework** . **Expectations** are the workhorse abstraction—each declares an expected state of the data (`expect_column_values_to_not_be_null`, `expect_column_values_to_match_regex`, `expect_table_row_count_to_be_between`, etc.) . **Expectation Suites** bundle Expectations for a dataset; **Checkpoints** automate testing and trigger Actions (alerts, pipeline blocking) based on results . **Data Docs** generate human-readable documentation—technical and non-technical stakeholders can inspect results . **Processes data in place**—no data leaves your systems . **Integrates with CI/CD** and works with Redshift, S3, Databricks, Flyte, and more . **Note**: **GX Cloud shut down June 1, 2026**—the open-source core remains Apache-2.0 and fully functional . **The reference implementation for declarative data testing** .



- **Soda Core**  

  **Open-source library and CLI for data quality testing** (Apache-2.0) . **SodaCL (Soda Checks Language)** turns user-defined input into SQL queries for validation . **Free and open source** with **18+ data source connections** . **Soda Library** (commercial extension) adds Soda Cloud connectivity, complex SodaCL checks, and additional features . **Best for**: teams wanting **SQL-native checks** without the full GX framework—**simpler and lighter than Great Expectations** for basic validation .



- **Elementary**  

  **dbt-native data observability** (Apache-2.0) . **The dbt-native choice**—**monitor pipelines in minutes** with a dbt package that adds data quality tests and anomaly detection **directly into dbt** . **Available as self-hosted or cloud service** with premium features . **Best for**: teams already running dbt who want observability **without adding a separate platform** .



### Additional Strong Open-Source Options



- **dbt tests** — Built-in testing for dbt models (Apache-2.0) . **The simplest data quality layer**—declarative tests (`not_null`, `unique`, `accepted_values`, `relationships`) run as part of `dbt test` . **No separate infrastructure**—if you're using dbt, you already have this .

- **dbt-meta-testing** — dbt package for documentation and test coverage (open-source) . **Granular control** over which models and columns are tested .

- Community **n8n** workflows for data quality alerting and incident routing.



**Frameworks for building custom systems**: Combine **Great Expectations** for declarative testing and Data Docs with **Soda Core** for SQL-native checks, **Elementary** for dbt-native observability, and **dbt tests** for the simplest validation layer—creating a comprehensive open-source data quality stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Data quality platforms handling enterprise data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls.

- **Open-source data quality is mature for declarative testing but limited for automated anomaly detection.** **Great Expectations** is the **most widely adopted open-source data testing framework** with human-readable Data Docs . **Soda Core** provides **SQL-native checks** with 18+ sources . **Elementary** brings observability to dbt . **But no open-source tool provides the ML-powered anomaly detection, automated profiling, and incident triage of Monte Carlo or Anomalo**—**integration work is required** .

- **The pricing models vary dramatically.** **Soda** charges **$8 per dataset per month** with a free tier for 3 datasets—**the most transparent pricing** in the category . **Monte Carlo** is **quote-only enterprise pricing** with tiers based on tables and users . **GX Cloud shut down June 1, 2026**—the open-source core remains free, but the managed offering is gone . **Model expected dataset count and table volume before committing** .

- **The "rules vs. ML" distinction is the core trade-off.** **Great Expectations and Soda** require **you to define what "good" looks like** via Expectations or SodaCL checks—**precise but manual** . **Monte Carlo and Anomalo** use **unsupervised ML to learn what "normal" looks like**—**zero configuration but probabilistic** . **Most mature teams use both**: declarative checks for known-critical constraints, ML for discovering unknown unknowns .

- **Agentic integration is the 2026 frontier.** **Monte Carlo** has an **MCP server with 56 tools** and **19 Apache-2.0 Agent Skills** for coding agents . **Telmai** has an **MCP-compliant server** so LLM agents can query validated data and quality metadata . **Lightup** integrates with **Claude Code** . **Data quality is becoming a tool that AI agents call, not just a dashboard humans read** .

- **Self-hosted open-source solutions require proper infrastructure management, check maintenance, and ongoing tuning.** **Data quality checks drift as schemas and business logic evolve**—budget for maintenance regardless of platform choice.



---



**Made for data engineers, analytics teams, and organizations building transparent data quality solutions.**  

Let's make Data Quality & Observability more open, data-driven, and reliable.
