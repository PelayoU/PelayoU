![Pelayo Urzaiz banner](assets/github-banner-pelayo_1.png)

# Pelayo Urzaiz

**MSc in Quantitative Finance** (UNED) · **MSc in Financial Sector Technologies — FinTech** (UC3M, in progress, TFM active) · **BSc in Applied Statistics** (UCM).

Quantitative Finance + FinTech engineering background, **expanding into DeFi and on-chain settlement**. **Solidity** and **TypeScript** are part of the active stack. The projects speak for themselves.

---

## Stack

| Area | Tech |
| :--- | :--- |
| **Languages** | C++ · Java · Python · R · SQL · Bash · **Solidity** · **TypeScript** |
| **Quantitative Finance** | Derivatives pricing engines · Valuation adjustments — xVAs (CVA / DVA / FVA) · Curve calibration · Monte Carlo simulation · Quantitative ML · Backtesting |
| **Capital Markets Technology** | Aeron · Hazelcast IMDG · FIX Protocol (QuickFIX/J) · Protobuf · Kryo · Low-latency systems |
| **Cloud & Distributed Systems** | AWS · Docker · Spring Boot · MongoDB · Hadoop · Linux |
| **Sovereign AI / RAG** | Ollama · Qdrant · n8n · Semantic Router · RAG · Jupyter |
| **Blockchain / DeFi** | Solidity · Foundry · Hardhat · Ethereum · ERC-20 · Arbitrum · Web3 |
| **Cybersecurity & Cryptography** | AES · RSA · TLS · PKCS#12 · Spring Security |
| **Data Engineering** | SPARQL · OpenRefine · pandas · NumPy · Oracle · Data warehousing |
| **Tools** | CMake · Maven · Git |

---

## Repositories

### [front-office-algorithms](https://github.com/PelayoU/front-office-algorithms)

Front-office quant engineering — pricing engines and counterparty-risk adjustments.

| Project | Description |
| :--- | :--- |
| **[Bonds, Swaps & Curve Calibration Engine](https://github.com/PelayoU/front-office-algorithms/tree/main/bonds-swaps-and-curve-calibration-engine)** | C++14 fixed-income valuation engine. Continuously-compounded zero-coupon curves, IRS pricing on Euribor 6M, par-swap rate, off-market MtM, bond cash-flow discounting, iterative bootstrapping (deposits + par swaps), Factory pattern with builder registration. **62 Boost.Test cases passing**, every numeric tied to a worked example. |
| **[xVA — Credit and Funding Valuation Adjustments](https://github.com/PelayoU/front-office-algorithms/tree/main/xva-credit-and-funding-adjustments)** | CVA / DVA / FVA Monte Carlo on a four-deal book under five mitigant regimes (no agreement → netting → asymmetric CSA → symmetric CSA → strict CSA). Sign-weighted exposure formula for opposite-sign tramos, full collateral-account roll under Threshold / MTA, MPR-style effective-NPV, FVA bonus track. Bilingual analysis of the comparative results. |

### [financial-sector-technologies](https://github.com/PelayoU/financial-sector-technologies)

Capital-markets infrastructure and applied research notes from the FinTech master's at UC3M.

| Project | Description |
| :--- | :--- |
| **[Low-Latency Messaging Benchmarks with Aeron](https://github.com/PelayoU/financial-sector-technologies/tree/main/low-latency-messaging-benchmarks-with-aeron)** | Java pub/sub benchmarks on the Aeron transport — IPC, UDP unicast and UDP multicast — measuring throughput and end-to-end latency across the three media. Latency / Simple publisher-subscriber pairs, dedicated low-latency vs back-off media drivers. |
| **[Hazelcast IMDG — Market Volume Control](https://github.com/PelayoU/financial-sector-technologies/tree/main/hazelcast-imdg-market-volume-control)** | Java + Hazelcast 5.5 in-memory data grid showcasing the patterns most often deployed in capital-markets infrastructure. Cluster fundamentals (TCP discovery, distributed `IMap`, **CP subsystem** Raft primitives) plus a market-data flow with a real-time volume listener and an end-of-day batch `EntryProcessor` modelling risk caches and post-trade jobs. |
| **[FIX Protocol Market Data Client](https://github.com/PelayoU/financial-sector-technologies/tree/main/fix-protocol-market-data-client)** | Java FIX 4.4 client (QuickFIX/J) implementing market-data subscription / snapshot flows, with acceptor + initiator session logs. |
| **[Latency and Jitter Analysis](https://github.com/PelayoU/financial-sector-technologies/tree/main/latency-jitter-analysis)** | Java + HdrHistogram. Service Time vs Response Time benchmarking, P99 / P99.9 / P99.99 tail measurement, **coordinated omission** correction. |
| **[Low-Latency Market Data Messenger](https://github.com/PelayoU/financial-sector-technologies/tree/main/low-latency-market-data-messenger)** | Java TCP + UDP-multicast server / client for market-data dissemination, ring-buffer wire format. |
| **[Spring Boot Basic Auth Lab](https://github.com/PelayoU/financial-sector-technologies/tree/main/spring-boot-basic-auth-lab)** | Secured REST microservice for market-data-style endpoints — Basic Auth, Spring Security, Actuator, role-based authorisation. |
| **[Applied Cryptography — AES, RSA & TLS](https://github.com/PelayoU/financial-sector-technologies/tree/main/applied-cryptography-aes-rsa-tls)** | Spring Boot 3.4 + Java 21. Self-signed PKCS#12 keystore + Spring Boot HTTPS endpoint, symmetric AES helper, asymmetric RSA helper, plus a performance benchmark quantifying why production stacks combine the two algorithms (HTTPS, FIX-over-TLS, SWIFT). |
| **[Serialization Benchmarks — Protocol Buffers vs Kryo](https://github.com/PelayoU/financial-sector-technologies/tree/main/serialization-benchmarks-protobuf-kryo)** | Java 21. **5,000,000-iteration** comparison of schema-driven (Protobuf 4.28) vs reflection-driven (Kryo 5.6) serialization over a market reference-data payload. |
| **[Blockchain in Capital Markets — Applied Research Note](https://github.com/PelayoU/financial-sector-technologies/tree/main/blockchain-capital-markets-research-note)** | End-to-end Ethereum smart-contract toolchain — Solidity reading on `Ballot.sol`, ERC-20 deployment in Remix, then live Sepolia testnet deployment with publicly verifiable on-chain artefacts. |
| **[Generative AI in Finance — Applied Research Note](https://github.com/PelayoU/financial-sector-technologies/tree/main/generative-ai-in-finance-research-note)** | Three case studies on LLMs in finance — IRR (numerical drift), investment-committee report (audience mismatch), pedagogical swap explanation (level of abstraction as prompt parameter). |

### [technological-infrastructures](https://github.com/PelayoU/technological-infrastructures)

Architecture design for capital-markets and crypto-derivatives infrastructure.

| Project | Description |
| :--- | :--- |
| **[Hybrid OTC Derivatives Platform](https://github.com/PelayoU/technological-infrastructures)** | Architecture design for an OTC platform that prices and settles **Forwards and Swaps on digital assets** under a hybrid on-chain / off-chain model. Co-located with Binance liquidity and **Arbitrum L2 settlement** inside AWS Tokyo (`ap-northeast-1`) for sub-2 ms internal latency. ECS Fargate for OMS / pricing / settlement, GPU-backed EKS for stochastic risk (MC VaR / ES), AWS Nitro Enclaves for transactional signing and key custody. Three modules: functional decomposition + zoning, communications, deployment + 3-year TCO. |

### [SEM-AI](https://github.com/PelayoU/SEM-AI)

Master's thesis (TFM) in progress — *AI as Infrastructure, Human as Author.*

| Project | Description |
| :--- | :--- |
| **[SEM-AI — AI Software Engineering Management for working with AI](https://github.com/PelayoU/SEM-AI)** | Final master's thesis. A reformulation of classical **SEM** (Software Engineering Management) materialised as a layer of homologous AI agents around the engineer's work. Each SEM role (Coach, PO, Architect, Developer, QA, Security Officer, DevOps) gets a homologous agent in `.claude/agents/` that reads and writes its own slice of a shared `vault/` segmented by role (vision → goals → capabilities → features → stories → specs → ADRs). Three structural mechanisms — segmentation by perspective, reactive discipline at write / commit / PR, atomic traceability — absorb the multiplied review cost of working with AI. Authorship and technical judgment stay with the human. |

### [fintech-homelab](https://github.com/PelayoU/fintech-homelab)

Personal homelab — distributed cluster + sovereign AI for sensitive financial data + scheduled fintech pipelines.

| Project | Description |
| :--- | :--- |
| **[3-Node Hybrid Cluster](https://github.com/PelayoU/fintech-homelab)** | Custom 3-node hybrid cluster running **15 containers** continuously: Sovereign AI / RAG (n8n + Qdrant + Jupyter), private cloud (Nextcloud + MariaDB + Redis), network edge (Nginx Proxy Manager + Pi-hole + WireGuard), ops (code-server + Portainer). |
| **[Secure Quant RAG — Distributed Vector Logic](https://github.com/PelayoU/fintech-homelab/tree/main/Secure-Quant-RAG-Distributed%20Vector%20Logic)** | A **Semantic Router** that dispatches each prompt between local private AI (Ollama) for sensitive material — smart-contract audits, M&A NDAs, proprietary code — and cloud models (Gemini) for general reasoning. Proprietary algorithms and client data never leave the on-premise infrastructure. |
| **[Crypto Daily Monitor — n8n Workflow](https://github.com/PelayoU/fintech-homelab/tree/main/crypto-daily-monitor-n8n)** | Scheduled n8n pipeline pulling daily BTC / ETH / SOL / ARB price snapshots from CoinGecko, structuring them into a clean JSON snapshot for downstream consumers (Postgres archive, Qdrant time-series RAG, threshold alerts). |

### [big-data](https://github.com/PelayoU/big-data)

Data engineering, big-data infrastructure, Linked Open Data.

| Project | Description |
| :--- | :--- |
| **[Linked Open Data Pipeline — Nobel Laureates in Physics](https://github.com/PelayoU/big-data/tree/main/linked-open-data-nobel-physics-pipeline)** | Full LOD lifecycle on a real-world target. **DBpedia SPARQL** acquisition, **Nobel Prize REST API** acquisition, **OpenRefine + GREL** cleaning and `cross()` integration, **Wikidata reconciliation** to `Q5` entities, Wikidata-only enrichment. Six SPARQL queries and seven GREL transformations checked into the repo, fully reproducible. |
| **[MongoDB Sharded Cluster (Docker)](https://github.com/PelayoU/big-data/tree/main/mongodb-sharded-cluster-docker)** | Sharded MongoDB cluster with replica sets — config servers, shards, `mongos` routers — deployable both via raw `docker run` and via Docker Compose. |
| **[Oracle SQL — Music Data Warehouse](https://github.com/PelayoU/big-data/tree/main/oracle-music-data-warehouse)** | Star-schema data warehouse on Oracle: staging area, dimensional model, materialised views and analytical queries. |
| **[Oracle SQL — Melomaniacs Concert DB](https://github.com/PelayoU/big-data/tree/main/oracle-sql-melomaniacs-concert-db)** | Operational OLTP schema for a concert database — DDL, queries, integrity constraints. |
| **[Hadoop Publishing Analytics — Pig + Hive](https://github.com/PelayoU/big-data/tree/main/hadoop-publishing-analytics-pig-hive)** | Pig and Hive analytics over a publishing-domain dataset on a Hadoop cluster — ETL in Pig, dimensional querying in Hive. |

### [data-analysis-machine-learning](https://github.com/PelayoU/data-analysis-machine-learning)

Quantitative / ML research on European indices.

| Project | Description |
| :--- | :--- |
| **[Euro Stoxx 50 — Sliding Windows Classification](https://github.com/PelayoU/data-analysis-machine-learning/tree/main/eurostoxx50-classification-sliding-windows)** | R. Forecasts the 50-session forward sign of the index with three classifiers (logistic, CART, random forest) under a strict expanding sliding-window backtest with a 50-run random baseline. Honest negative finding — none beats the random baseline on this target — backed by reproducible CSV/PDF outputs. No look-ahead in features, no global hyperparameter tuning. |
| **[DAX 30 — Supervised ML Experiments](https://github.com/PelayoU/data-analysis-machine-learning/tree/main/dax30-supervised-ml-experiments)** | R. Two paired experiments on `^GDAXI`: KNN regression on the 30-session forward return, and a `caret` head-to-head (KNN, CART, Naïve Bayes) classifying the 65-session forward sign. Train-test scaling without look-ahead leakage. |
| **[IBEX 35 — Ingestion and Visual Exploration](https://github.com/PelayoU/data-analysis-machine-learning/tree/main/ibex35-data-ingestion-and-visual-exploration)** | R. ETL pipeline over Yahoo Finance: caching, listwise deletion at ingest, LOCF for calendar alignment (no look-ahead), Base 100 normalisation, OLS Beta regression Santander / Mapfre vs IBEX. |

### [high-performance-cpp](https://github.com/PelayoU/high-performance-cpp)

Modern C++ for performance-sensitive numerical work.

| Project | Description |
| :--- | :--- |
| **[C++ Matrix — Templated, Parallel](https://github.com/PelayoU/high-performance-cpp/tree/main/cpp-matrix-templated-parallel)** | Header-only templated matrix library with full Rule-of-Five RAII over `std::unique_ptr<T[]>`, capacity controls (`reservar` / `redimensionar`), and a parallel functional pipeline (`map`, `par_map`, `par_reduce`) using `std::async` / `std::future`. Ships a side-by-side legacy raw-pointer implementation for direct RAII contrast. **17/17 CTest tests passing** across both versions. |

---

## Background

- **MSc in Quantitative Finance** — Universidad Nacional de Educación a Distancia (UNED). Risk models, derivatives, time series, ML for finance, valuation, portfolio and risk management.
- **MSc in Financial Sector Technologies — FinTech** — Universidad Carlos III de Madrid (UC3M, in progress). Financial Sector Technologies, Big Data, Blockchain and Cybersecurity, High-Performance Programming (C++), Financial Sector Technological Infrastructure (Java). TFM in progress: SEM-AI framework — see Repositories above.
- **BSc in Applied Statistics** — Universidad Complutense de Madrid (UCM). Probability, inference, econometrics, time series, optimisation, data analysis.

---

## Contact

- **Email:** pelayo.urzaiz@gmail.com
- **LinkedIn:** [pelayourzaiz](https://www.linkedin.com/in/pelayourzaiz/)
