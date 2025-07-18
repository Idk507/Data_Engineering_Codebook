Here’s a **comprehensive breakdown** of **all components and features** in Databricks—organized as you see them on the platform and official documentation:

---

## 1. 🏢 Account, Workspace & Governance

* **Account**: The top-level entity that manages billing, Unity Catalog, support and multi-workspace administration ([Databricks Documentation][1])
* **Workspace**: A cloud environment containing folders, notebooks, libraries, jobs, etc. ([Databricks Documentation][1])

### Identity & Access

* **Users, Groups, Service Principals**: Identities and service accounts ([Databricks Documentation][1])
* **ACLs & RBAC**: Fine-grained permissions on all assets ([Databricks Documentation][1])
* **Personal Access Token (PAT)**: For REST/CLI authentication ([Databricks Documentation][1])

---

## 2. 💰 Billing & Usage

* **Databricks Units (DBUs)**: Compute usage billing units ([Databricks Documentation][1])

---

## 3. 🧭 Interfaces & APIs

* **UI**: Web-based interface
* **REST API / SQL REST API**: Programmatic control ([Databricks Documentation][1])
* **CLI**: Command-line control
* **Git Folders (Repos)**: Git-integrated source control ([Databricks Documentation][1])

---

## 4. 🗄️ Data Management & Catalog

* **Unity Catalog**: Central metastore with governance, lineage, permissions ([Databricks Documentation][1])
* **Catalogs, Schemas (Databases)**: Namespace hierarchy ([Microsoft Learn][2])
* **Tables (Delta Tables)**: ACID tables with time-travel ([Microsoft Learn][2])
* **Views**: SQL-defined queries
* **Volumes**: For unstructured data ([Microsoft Learn][2])
* **Metastore (Unity or Hive legacy)**&#x20;
* **Catalog Explorer**: Data/AI asset discovery ([Databricks Documentation][1])

---

## 5. ⚙️ Compute & Execution

* **Clusters**:

  * All-purpose
  * Job clusters&#x20;
* **Pools**: Pre-warmed VMs to reduce latency&#x20;
* **Databricks Runtime**:

  * Standard
  * ML (pre-installed libraries & GPU support) ([Databricks Documentation][1])
* **Execution Context**: REPL for Python, Scala, SQL, R ([Databricks Documentation][1])

---

## 6. 🛠️ Data Engineering & Pipelines

* **Notebooks**: Multi-language interactive development&#x20;
* **Libraries**: Cluster-scoped dependencies&#x20;
* **Delta Lake**: Storage layer for ACID, versioning ([Baytech Consulting][3])
* **Auto Loader**, **Structured Streaming**: Efficient file ingestion
* **Delta Live Tables (Pipelines / Lakeflow Declarative Pipelines)**: Declarative ETL with lineage & quality ([Microsoft Learn][2])
* **Jobs & Pipelines UI**: Orchestrate notebooks, SQL, DLT, etc. ([Microsoft Learn][2])

---

## 7. 📊 SQL Analytics & BI

* **SQL Warehouse**: Scalable compute for SQL workloads
* **Query Editor & History**, **Dashboards**
* **BI Integrations**: JDBC/ODBC support (Power BI, Tableau, Looker…) ([Baytech Consulting][3])

---

## 8. 🤖 AI, ML & Generative AI

* **MLflow**: Experiment tracking, model registry ([Databricks Documentation][1])
* **Machine Learning Runtime**: Pre-configured ML/DL libraries ([Databricks Documentation][1])
* **Feature Store**: Shareable and consistent feature pipelines ([Databricks Documentation][1])
* **Experiments & Runs**: In MLflow&#x20;
* **Model Registry**: Central model lifecycle management&#x20;
* **Model Serving (Mosaic AI Model Serving)**: REST API deployment ([Databricks Documentation][1])
* **Mosaic AI / DBRX**: Generative and foundation model support ([Wikipedia][4])
* **AI Playground / Chat with LLMs**: Interactive LLM testing ([Databricks Documentation][1])

---

## 9. 🧠 Genie & AI‑Powered Experiences

* **AI/BI Genie**: Natural-language querying and visualizations ([Databricks][5])
* **Genie Spaces**: Domain-specific semantic configs ([Microsoft Learn][6])
* **Genie Agent / MCP Server**: API for integrating Genie with tools ([FlowHunt][7])

---

## 10. 🔗 Integrations & Ecosystem

* **Partner Connect**: Integration with Fivetran, Datadog, etc.
* **Marketplace**: Pre-built datasets, models, apps&#x20;
* **Cloud Storage Connectors**: S3, ADLS Gen2, GCS&#x20;

---

## 11. 🔒 Security, Auditing & Compliance

* **Encryption**: In-transit and at-rest via cloud.
* **Audit Logging**: Workspace, job, data access logs ([Databricks Documentation][1])
* **Lineage & Governance**: Unity Catalog + Audit logs ﹘ centralized data/AI governance ([Baytech Consulting][3])

---

## 12. ⚙️ Orchestration & Operational Management

* **Jobs API & Scheduler**: Define triggers, dependencies&#x20;
* **Monitoring & Alerts**: Job health & failure notifications
* **Cost & Performance**: DBU tracking, serverless compute, pools optimization €citeturn0search0turn0search4

---

## 🧩 All-Together View

* **Control Plane**: UI, metadata, scheduling, APIs
* **Compute Plane**: Clusters, pools, runtimes, jobs
* **Storage & Governance**: Delta Lake, Unity Catalog, volumes
* **Engineering & Orchestration**: Notebooks, DLT, Jobs, Pipelines
* **Analytics & BI**: SQL Warehouses, Dashboards, BI tools
* **AI/ML & Generative AI**: MLflow, Feature Store, Model Serving, DBRX, Genie & Mosaic AI

---

This version **includes everything** visible in the platform—from **Workflows and Pipelines to Genie spaces, AI Playground, Mosaic AI, MCP Server**, and core Platform architecture. Let me know if you want to explore any component in more depth!

[1]: https://docs.databricks.com/aws/en/getting-started/concepts?utm_source=chatgpt.com "Databricks components"
[2]: https://learn.microsoft.com/en-us/azure/databricks/getting-started/concepts?utm_source=chatgpt.com "Azure Databricks components - Learn Microsoft"
[3]: https://www.baytechconsulting.com/blog/databricks-data-intelligence-platform-2025?utm_source=chatgpt.com "Databricks Data Intelligence Platform 2025 - Baytech Consulting"
[4]: https://en.wikipedia.org/wiki/Databricks?utm_source=chatgpt.com "Databricks"
[5]: https://www.databricks.com/product/business-intelligence/ai-bi-genie?utm_source=chatgpt.com "GenAI-Powered Business Intelligence - Databricks"
[6]: https://learn.microsoft.com/en-us/azure/databricks/genie/?utm_source=chatgpt.com "What is an AI/BI Genie space - Azure Databricks - Learn Microsoft"
[7]: https://www.flowhunt.io/mcp-servers/databricks-genie/?utm_source=chatgpt.com "Databricks Genie MCP Server - FlowHunt"
