# Muhammad Umair

**Full-stack software engineer, UK.** I build production systems end to end: React + TypeScript front ends, Python services, retrieval and ML pipelines, and the AWS and CI/CD that ship them. Six years in industry and research, MSc Data Science.

[Portfolio](https://umairleo1.github.io/portfolio/) · [LinkedIn](https://www.linkedin.com/in/muhammad-umair-amin/) · [umair.leo17@gmail.com](mailto:umair.leo17@gmail.com)

---

### Now

**Software Engineer, NIHR Innovation Observatory, Newcastle University** (May 2026 – present)
Replacing a legacy ASP.NET MVC research database with a React 19 + TypeScript SPA on AWS: Cognito sign-in (authorisation code + PKCE, MFA), Lambda services behind API Gateway, and GitHub Actions deploys to S3 + CloudFront. I designed a shared search / edit / merge screen kit that every section of the app is built on.

### Building: [Docnus](https://docnus.com)

A multi-tenant SaaS that answers questions over a company's own documents, with citations. I designed and built it solo, front end to infrastructure (~850 commits, live in production; source is private).

- **Ingestion:** Docling OCR for native and scanned PDFs, DOCX and DOC, running in a separate Celery worker that scales on its own; header-aware chunking; OpenAI embeddings into Pinecone.
- **Retrieval:** hybrid search with reranking, plus a knowledge graph built from extracted entities, with entity resolution and Leiden community summaries. Claude writes the cited answers.
- **Measured, not guessed:** a retrieval-evaluation harness on a labelled golden set (currently 94% recall, 0.69 nDCG@10), scored in CI against a committed baseline so tuning changes can't silently regress.
- **Production concerns:** RBAC and per-plan quotas, Stripe billing with idempotent webhook handling, TOTP MFA for admins, PII detection and GDPR tooling, Prometheus and Sentry, Alembic migrations.
- **Quality:** 1,200+ backend tests and Playwright end-to-end tests on the React 19 front end.

### Selected open source

| Project | What it shows |
| --- | --- |
| **Nutrient Predictor** · [app](https://github.com/umairleo1/nutrient-predictor-frontend) · [API](https://github.com/umairleo1/nutrient-predictor-backend) · [model](https://github.com/umairleo1/nutrient-predictor-model-development) · [live](https://umairleo1.github.io/nutrient-predictor-frontend/) | ML from data to product: NHANES preprocessing, calibrated XGBoost risk models, a FastAPI service, and a React + TypeScript UI that explains each prediction. |
| [**subscription-tracker-backend**](https://github.com/umairleo1/subscription-tracker-backend) | FastAPI service with linked multi-account auth, Celery background jobs, Alembic migrations and Docker Compose. |
| [**currency-analysis**](https://github.com/umairleo1/currency-analysis) · [live](https://umairleo1-currency-analysis-app-l0fbth.streamlit.app/) | Exchange-rate pipeline with volatility and correlation metrics, served as an interactive Streamlit dashboard. |
| [**portfolio**](https://github.com/umairleo1/portfolio) · [live](https://umairleo1.github.io/portfolio/) | React + TypeScript site with semantic-release, Lighthouse CI, Dependabot and PR checks. |

### Before this

| | |
| --- | --- |
| **UNICEF UK** · Data Integrations Developer · 2025 | Salesforce → Snowflake ETL in Python, SQL and AWS Lambda behind GitLab CI gates; nightly load time down 45%, 5M rows reconciled at 99.8% accuracy. |
| **University of Greenwich** · Software Developer (AI) · 2023–25 | LangGraph ML pipeline over 100 GB of data (+30% throughput); SQL analytics adopted by the AML research team. |
| **SprintX** · AI Software Engineer · 2022 | React apps and CircleCI / Jenkins pipelines; release lead time down 60%, test coverage 55% → 85%, production regressions down 40%. |
| **Frizhub** · AI Software Engineer · 2020–21 | React Native apps and Dockerised AWS / GCP stacks with Terraform and Jenkins; deployment time halved, crash rate down 25%. |

### Stack

**Languages** TypeScript, Python, SQL · **Front end** React, TanStack Query, Redux Toolkit, Vite, Tailwind, shadcn/ui · **Back end** FastAPI, SQLAlchemy, PostgreSQL, Redis, Celery · **AI / data** RAG, Pinecone, OpenAI and Anthropic APIs, XGBoost, pandas · **Cloud** AWS (Lambda, Cognito, API Gateway, S3, CloudFront, CDK), Docker, Terraform · **Delivery** GitHub Actions, Vitest, Jest, Playwright, pytest
