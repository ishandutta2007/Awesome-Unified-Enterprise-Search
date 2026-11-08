# Awesome-Unified-Enterprise-Search

# Awesome Unified Enterprise Search

> A curated list of top Unified Enterprise Search platforms — both SaaS/Hosted commercial solutions and open-source alternatives for connecting siloed knowledge, delivering permission-aware answers, and powering AI agents with company context.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Glean](#glean)
  - [Coveo](#coveo)
  - [Amazon Kendra](#amazon-kendra)
  - [Perplexity Enterprise](#perplexity-enterprise)
  - [Elastic Enterprise Search (Legacy)](#elastic-enterprise-search-legacy)
- [Open-Source Software](#-open-source-software)
  - [PipesHub](#pipeshub)
  - [Sercha Core](#sercha-core)
  - [Fess](#fess)
  - [Turing ES](#turing-es)
  - [Gerev AI](#gerev-ai)
  - [Apache Solr](#apache-solr)
  - [OpenSearch](#opensearch)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Unified Enterprise Search platforms. These are not open-source but are included as reference points for feature comparison.

### Glean
**Type:** Enterprise AI coworker with search foundation  
Glean has evolved from enterprise search into a broader AI platform that connects to 100+ apps including Google Drive, Slack, Confluence, Jira, Salesforce, and Microsoft 365 [citation:1][citation:8]. Search remains a core capability: users find documents, messages, tickets, and conversations in one place, with results limited to what they already have permission to see [citation:1]. The platform provides grounded answers with citations, people discovery (who owns a topic, who worked on related projects), and code search across GitHub and GitLab [citation:1]. Glean is also available inside Slack and other tools, and can be used as company context inside AI tools via MCP [citation:1]. Gartner reviewers note it functions like an expert who has read every company document, though some wish for more out-of-the-box connectors and better support for custom on-prem connectors [citation:14].  
**Best for:** Organizations wanting a mature enterprise AI platform grounded in a proven search foundation, with broad connector coverage and permission-aware answers.

### Coveo
**Type:** AI-Relevance platform for enterprise search and generative experiences  
Coveo's platform unifies an organization's content and data into a single searchable index through connectors to systems like SAP, Salesforce, ServiceNow, SharePoint, Confluence, Jira, Slack, GitHub, and Google Drive [citation:2][citation:15]. It delivers AI-relevance with generative answering, passage retrieval API, and detailed analytics with Snowflake integration [citation:15]. Security is early-binding with document-level permissions, and the platform is ISO 27001/27018 certified, SOC 2 Type II, HIPAA compatible, and offers a 99.999% SLA [citation:9][citation:15]. Coveo is rated a Leader by Gartner (7x), Forrester (6x), and IDC (2x), with customers including Pfizer, Eaton, Cummins, and Okta [citation:9][citation:15].  
**Best for:** Large enterprises managing massive content volumes across complex systems, needing AI-powered relevance with strong security and compliance certifications.

### Amazon Kendra
**Type:** AWS-managed intelligent enterprise search  
Amazon Kendra is a fully managed ML-powered enterprise search service that provides unified search across structured and unstructured content repositories [citation:4][citation:10]. It uses NLP for highly accurate answers without requiring ML expertise, with tunable relevance based on content attributes, freshness, and user behavior [citation:4]. Kendra can be combined with LLMs for RAG-based generative AI experiences, and integrates with AWS services for chatbots and in-app search [citation:10]. AWS claims 25% employee productivity improvement and 75% lower first-year TCO compared to traditional enterprise search tools [citation:10].  
**Best for:** Organizations already standardized on AWS wanting managed semantic search with RAG capabilities and no infrastructure to maintain.

### Perplexity Enterprise
**Type:** AI answer engine with enterprise connectors  
Perplexity Enterprise provides access to Perplexity's answer engine with enterprise controls, including SSO, user management, and centrally governed File Connectors [citation:11]. Enterprise Pro includes Perplexity Computer, an agent that researches across the web and connected apps, creates documents and presentations, and runs background automations [citation:11]. Data is never used to train or fine-tune Perplexity's models, with SOC 2 Type II certification and data protection agreements with third-party AI providers preventing training on Perplexity data [citation:11].  
**Best for:** Teams wanting an AI-first answer engine with enterprise governance and agentic capabilities, rather than a traditional search index over internal documents.

### Elastic Enterprise Search (Legacy)
**Type:** Search platform (end-of-life announced)  
Elastic Enterprise Search (including App Search and Workplace Search) is being deprecated in version 9.0, with Elastic shifting focus to Elasticsearch for enterprise search use cases [citation:3]. Current 8.x deployments remain available and maintained until January 15, 2027, with support until July 15, 2027 [citation:3]. New customers cannot access App Search and Workplace Search after the 9.0 release. Elastic positions Elasticsearch (available in Elastic Cloud Serverless) as the path forward [citation:3].  
**Best for:** Existing Elastic customers with current 8.x deployments; new implementations should evaluate Elasticsearch directly or open-source alternatives.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Unified Enterprise Search tools. The open-source ecosystem splits between **permission-aware AI context platforms**, **traditional enterprise search servers**, and **connector-heavy search backends**.

### PipesHub
**Stack:** Python / TypeScript / Docker | **License:** Apache-2.0  
PipesHub is a fully open-source, self-hostable platform for connecting AI applications to company knowledge across business systems [citation:13]. It connects Slack, Google Drive, GitHub, Microsoft 365, and Notion (50+ enterprise connectors with real-time and scheduled indexing), then provides **permission-aware search with citations** for teams and trusted context for AI agents through APIs, SDKs, and MCP [citation:13]. Access is resolved at query time against the source system's own permissions, so agents retrieve exactly what a specific person is allowed to see [citation:13]. Answers come from an agent loop combining hybrid search, grep, knowledge-graph navigation, and full-document reading, with precise block citations to original documents. Deploys via Docker Compose with an interactive installer [citation:13].  
**Best for:** Organizations wanting a genuinely open-source, self-hosted platform that serves both human search and AI agent context with permission enforcement, without vendor lock-in.

### Sercha Core
**Stack:** Go / Vespa / PostgreSQL | **License:** Apache-2.0  
Sercha Core is a self-hosted, team-wide search platform that connects organizational data sources and provides unified search across all of them [citation:7]. Features include 11+ connectors (GitHub, GitLab, Slack, Notion, Confluence, Jira, Google Drive, Google Docs, Linear, Dropbox, S3), hybrid search (BM25 lexical + semantic embeddings via Vespa), OAuth2 authentication with JWT sessions, role-based access, and an admin UI for managing sources and search [citation:7]. Deploys as a single container or scales horizontally across multiple nodes. Unlike the Sercha CLI (designed for individual use), Sercha Core is built for teams with shared data [citation:7].  
**Best for:** Teams wanting a lightweight, self-hosted unified search platform with modern connectors and hybrid search, keeping data on their own infrastructure.

### Fess
**Stack:** Java / OpenSearch or Elasticsearch | **License:** Apache-2.0  
Fess is an easily deployable, full-featured enterprise search server built on OpenSearch/Elasticsearch with extensive out-of-the-box crawlers [citation:6]. Features include web, file system, and database crawlers; Active Directory and LDAP role-based search filtering; support for 20+ languages; and a management UI. It is designed for traditional on-premises environments needing automated crawling of local file shares, intranet portals, and relational databases [citation:6].  
**Best for:** Organizations needing a proven, crawler-heavy enterprise search server for on-premises file shares, intranets, and databases with LDAP/AD integration.

### Turing ES
**Stack:** Java / Solr / Elasticsearch / Lucene | **License:** Open Source (per project)  
Turing ES (Viglet) is an open-source enterprise search and generative AI platform featuring faceted semantic search, hybrid BM25 + vector ranking with Reciprocal Rank Fusion, and RAG chat with inline citations [citation:6]. It offers multi-engine abstraction (Apache Solr, Elasticsearch, embedded Lucene), Viglet Dumont connectors for Adobe AEM and WordPress, MCP tool agents, and air-gapped readiness [citation:6].  
**Best for:** Enterprise CMS and portal deployments (Adobe Experience Manager, WordPress) requiring turnkey semantic search and inline generative citations in air-gapped environments.

### Gerev AI
**Stack:** Python / Vector indexing | **License:** Open Source (per project)  
Gerev AI is an open-source AI-powered enterprise search engine designed for workplace knowledge discovery [citation:6]. It indexes internal communication and wikis to surface direct answers, with connectors for Confluence, Slack, Google Drive, and Jira. Features include vector indexing and a conversational UI [citation:6].  
**Best for:** Teams exploring lightweight self-hosted internal search prototypes with AI-powered answer surfacing, particularly for Confluence/Slack/Jira-heavy environments.

### Apache Solr
**Stack:** Java / Lucene | **License:** Apache-2.0  
Apache Solr is a mature, highly reliable enterprise search server built on Apache Lucene, providing distributed indexing, advanced schema definitions, and XML/JSON APIs [citation:6]. Features include SolrCloud distributed architecture with ZooKeeper coordination, complex faceted navigation, spatial search, and rich document parsing via Apache Tika [citation:6].  
**Best for:** Legacy enterprise IT architectures, digital libraries, and e-commerce catalogs requiring deep query customization and proven clustering stability, where you are prepared to build the ingestion and UI layers yourself.

### OpenSearch
**Stack:** Java / Lucene | **License:** Apache-2.0  
OpenSearch is a community-driven, Apache-licensed search and analytics suite derived from Elasticsearch 7.10.2. It provides full-text search, analytics, and observability capabilities with k-NN plugins for vector search (HNSW, Faiss, NMSLIB) [citation:12]. It is the foundational engine for tools like Fess and is the most-used Apache-licensed search engine in enterprise environments.  
**Best for:** Organizations wanting an Apache-licensed, community-governed search engine as a foundation for building custom enterprise search, with no licensing concerns.

---

## 📊 Comparison at a Glance

| Software | License | Type | Permission-Aware | AI/Agent Context | Self-Hosted | Best For |
|----------|---------|------|------------------|------------------|-------------|----------|
| **Glean** | Proprietary | Enterprise AI coworker | ✅ | ✅ MCP | ❌ | Enterprise AI + search |
| **Coveo** | Proprietary | AI-Relevance platform | ✅ | ✅ Generative | ❌ | Large-scale enterprise search |
| **Amazon Kendra** | Proprietary | Managed semantic search | (AWS IAM) | ✅ RAG | ❌ | AWS-native semantic search |
| **Perplexity Enterprise** | Proprietary | AI answer engine | (File connectors) | ✅ Computer agent | ❌ | AI-first answer engine |
| **PipesHub** | Apache-2.0 | AI context + search | ✅ Source-level | ✅ MCP + SDKs | ✅ | Open-source permission-aware AI context |
| **Sercha Core** | Apache-2.0 | Team search platform | (OAuth2/JWT) | Limited | ✅ | Lightweight team unified search |
| **Fess** | Apache-2.0 | Crawler-based search | ✅ LDAP/AD | ❌ | ✅ | On-prem file/intranet search |
| **Turing ES** | Open Source | Semantic + RAG search | (Check) | ✅ RAG citations | ✅ | CMS/portal semantic search |
| **Gerev AI** | Open Source | AI workplace search | (Check) | ✅ Vector + chat | ✅ | Lightweight Confluence/Slack search |
| **Apache Solr** | Apache-2.0 | Search server | (Custom) | ❌ | ✅ | Proven clustered search foundation |
| **OpenSearch** | Apache-2.0 | Search engine | (Custom) | ❌ | ✅ | Apache-licensed search foundation |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Unified Enterprise Search tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem **splits** between permission-aware AI context platforms (PipesHub), team search backends (Sercha Core), crawler-heavy search servers (Fess), and foundational search engines (Solr, OpenSearch). PipesHub is currently the closest open-source equivalent to Glean's permission-aware AI context model, though it is newer and less mature.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
