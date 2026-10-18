# Awesome-Data-Quality-Observability

# Top Data Quality & Observability Ecosystem

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

- **Monte Carlo**  
  **The data + AI observability platform** for detecting, resolving, and preventing data quality incidents across warehouses, lakes, BI tools, and AI agents . **Pricing**: **Quote-only enterprise pricing** with tiered plans (Start, Scale, Enterprise) based on tables and users—**no public per-table rate** . **Start** covers warehouse, BI, and ETL monitoring for up to 10 users and 1,000 tables . **Scale** adds lakes (Databricks, Hive, Glue), databases, GenAI pipelines, SSO, PII filtering, and customer-hosted agents . **Enterprise** adds EDW (Oracle, SAP Hana, Teradata), audit logging, and unlimited users . **GraphQL API** exposes every web app feature; **Push Ingest API** for custom metadata; **MCP server** with 56 tools for AI agent integration . **The market leader** by G2 and Gartner Peer Insights with 500+ deployments .

- **Bigeye**  
  **Enterprise data observability with legacy system support** . **Pricing**: **Quote-only**—enterprise sales-led . **Key differentiators**: **customizable data quality dimensions** (align metrics with your governance framework), **join rules** for cross-database integrity checks (LEFT, RIGHT, INNER, FULL OUTER with column filtering), and **asset linking** to map virtual table metrics back to physical critical data elements (CDEs) . **bigAI incident co-pilot** summarizes incidents in plain language, suggests remediation steps, and produces stakeholder impact statements—**cuts mean time to resolution in half** in beta . **Extensive legacy connectors**: Oracle, SQL Server, Informatica, IBM DB2, DataStage, SSIS, SnapLogic, Qlik Replicate . **Best for**: enterprises migrating thousands of rules from legacy tools while needing modern automation .

- **IBM Databand**  
  **Observability software for data pipelines and warehouses** that automatically collects metadata . Features **pipeline monitoring** (DAGs, runs, tasks), **data warehouse monitoring** (hourly table snapshots, query history), **alerts** for null and duplicate checks, **live view** for active runs, and **role-based access control** . **Databand Self-Hosted** keeps all metadata within your network . **Table transactions collected every 10 seconds**; **table summaries and quality checks every hour** . **Best for**: organizations already in the IBM ecosystem needing self-hosted observability .

- **Acceldata (ADOC)**  
  **Data Observability Cloud** with **Agentic Data Management (ADM)** . Features **Discovery** (60+ data sources, automatic schema scanning), **Policies** (data quality, reconciliation, freshness, schema drift, data drift, profile anomaly), and **Insights & Actions** (Slack/Email/Teams alerts, reliability reports, root cause drilldowns) . **ADM** provides natural-language investigation—explains why a policy failed, summarizes contributing rules, and guides remediation . **Best for**: teams wanting **guided incident investigation** on top of observability .

- **Soda**  
  **AI-native, fully automated data quality platform** . **Pricing**: **Free plan** for up to 3 production datasets . **Team at $8 per dataset per month** (billed annually)—pay only for datasets you test and monitor, unlimited users . **Enterprise** adds no-code interface, AI-powered features, audit logs, RBAC, private deployment, and SSO . **Best for**: teams wanting **per-dataset pricing transparency** with a generous free tier .

- **Anomalo**  
  **AI-native enterprise data quality platform** backed by **both Databricks and Snowflake** . **Pricing**: **Quote-only** . **Key differentiator**: **unsupervised ML** automatically profiles data and detects anomalies **without manual rules**—works across **structured, semi-structured, and unstructured** data . **Agentic Platform** (2026) adds **Table Observability Agent**, **Data Quality Agent**, **Data Issue First Responder Agent** (investigates and acts on runbooks, initiates ServiceNow/JIRA workflows), and **Data Insights Agent** (proactively investigates and delivers analyst-grade reports) . **Best for**: enterprises wanting **no-code ML anomaly detection** with agentic remediation .

- **Metaplane**  
  **Data observability with ML-based anomaly detection and end-to-end column-level lineage** . Features **Chrome extension** to check dashboard data integrity in-place—confirm source data, freshness, and lineage without leaving the BI tool . **Monitor entire data stack within 30 minutes** . **Best for**: teams wanting **fast setup** and in-context visibility from BI dashboards .

- **Telmai**  
  **AI-powered data observability for the agentic AI era** . Features **continuous validation** (structured, semi-structured, unstructured), **MCP-compliant server** for LLM agents (Claude, Bedrock, Vertex) to query validated data and quality metadata, and **Data Reliability Agents** for natural-language anomaly investigation and remediation suggestions . **Best for**: teams building **agentic AI workflows** needing real-time quality signals at the source .

- **Lightup**  
  **Next-generation data quality and observability** with **MCP integration** (Claude Code) . Features **data profiles** (automatic static analysis), **auto metrics** for common checks, **custom metrics** (no-code to SQL), **slices** for per-segment monitoring, and **threshold or anomaly detection monitors** . **Best for**: teams wanting **flexible metric definition** with MCP-native agent access .

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
