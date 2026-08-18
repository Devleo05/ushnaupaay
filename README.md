<div align="center">

# UshnaUpaay

**Smart Heatwave Mitigation & Climate Adaptation Platform**

[![GitHub stars](https://img.shields.io/github/stars/Devleo05/ushnaupaay?style=flat-square&logo=github)](https://github.com/Devleo05/ushnaupaay/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Devleo05/ushnaupaay?style=flat-square&logo=github)](https://github.com/Devleo05/ushnaupaay/network/members)
[![GitHub issues](https://img.shields.io/github/issues/Devleo05/ushnaupaay?style=flat-square&logo=github)](https://github.com/Devleo05/ushnaupaay/issues)
[![GitHub license](https://img.shields.io/github/license/Devleo05/ushnaupaay?style=flat-square)](https://github.com/Devleo05/ushnaupaay/blob/main/LICENSE)
[![CI Status](https://img.shields.io/github/actions/workflow/status/Devleo05/ushnaupaay/ci.yml?style=flat-square&label=CI)](https://github.com/Devleo05/ushnaupaay/actions)
[![Coverage](https://img.shields.io/codecov/c/github/Devleo05/ushnaupaay?style=flat-square&logo=codecov)](https://codecov.io/gh/Devleo05/ushnaupaay)
[![Lighthouse](https://img.shields.io/badge/Lighthouse-95%2B-brightgreen?style=flat-square&logo=lighthouse)](https://pagespeed.web.dev/)

<br />

<img src="https://github-readme-stats.vercel.app/api?username=Devleo05&show_icons=true&theme=transparent&hide_border=true&count_private=true" alt="GitHub Stats" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Devleo05&layout=compact&theme=transparent&hide_border=true" alt="Top Languages" />

<br />

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-20-339933?style=flat-square&logo=nodedotjs)](https://nodejs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-4169E1?style=flat-square&logo=postgresql)](https://www.postgresql.org/)
[![Redis](https://img.shields.io/badge/Redis-7-DC382D?style=flat-square&logo=redis)](https://redis.io/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker)](https://www.docker.com/)
[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-2088FF?style=flat-square&logo=githubactions)](https://github.com/features/actions)

</div>

---

## Executive Overview

UshnaUpaay is a production-grade platform designed to help communities, municipalities, and enterprises detect, forecast, and mitigate heatwave risks in real time. It combines environmental data ingestion, predictive modeling, early-warning dissemination, and adaptive response orchestration into a single coherent system.

The platform prioritizes low-latency alerts, verifiable data provenance, and measurable impact on heat-related morbidity and energy demand.

```
┌─────────────────┐     ┌──────────────────┐     ┌────────────────────┐
│  Data Ingestion │────▶│  Processing &    │────▶│  Decision & Alert  │
│  (IoT / APIs /  │     │  Forecasting     │     │  Layer             │
│   Weather)      │     │  Engine          │     │  (SMS / App / API) │
└─────────────────┘     └──────────────────┘     └────────────────────┘
         │                        │                         │
         ▼                        ▼                         ▼
┌─────────────────┐     ┌──────────────────┐     ┌────────────────────┐
│  Time-series DB │     │  Feature Store + │     │  Analytics &       │
│  + Redis Cache  │     │  Model Registry  │     │  Impact Dashboard  │
└─────────────────┘     └──────────────────┘     └────────────────────┘
```

Core value proposition: turn fragmented heat and climate signals into actionable, auditable interventions with measurable outcomes.

---

## Software Testing & Quality Assurance

Quality is treated as a continuous, measurable property of the system rather than a gate at the end of development.

### Testing Matrix

| Layer            | Scope                                      | Tools                          | Frequency          |
|------------------|--------------------------------------------|--------------------------------|--------------------|
| Unit             | Business logic, utilities, pure functions  | Vitest / Jest                  | Every commit       |
| Integration      | API contracts, database interactions       | Supertest + Testcontainers     | Every PR           |
| End-to-End       | Critical user journeys & alert flows       | Playwright                     | Nightly + release  |
| API Load         | Throughput, latency, error rates under load| k6 / Artillery                 | Pre-release        |
| Security         | Dependency scanning, SAST, secret detection| CodeQL, Trivy, gitleaks        | Every PR + weekly  |
| Accessibility    | WCAG 2.2 AA compliance                     | axe-core + Playwright          | Nightly            |

### CI/CD Integration

All quality gates run inside GitHub Actions:

1. **On push / PR**  
   - Lint + type-check  
   - Unit + integration tests  
   - Security scans (SAST + dependency + secrets)  
   - Coverage threshold enforcement (≥ 80% line coverage)

2. **On merge to main**  
   - Full E2E suite  
   - Build and push Docker images  
   - Deploy to staging  
   - Smoke tests against staging

3. **On release tag**  
   - Load testing against staging  
   - Production deployment with canary strategy  
   - Post-deployment synthetic monitoring

Failed quality gates block merges. Coverage and security findings are published as PR comments and tracked over time.

---

## Digital Marketing & Growth Strategy

### Technical SEO Foundations

- Structured data (JSON-LD) for Organization, SoftwareApplication, and FAQPage
- Core Web Vitals targets: LCP < 2.5 s, INP < 200 ms, CLS < 0.1
- Server-side rendering + edge caching for critical landing pages
- Canonical URLs, sitemap, and robots.txt managed via Next.js App Router
- Open Graph and Twitter Card metadata for every public route

### Content & Social Proof

- Technical blog series on heat-risk modeling, early-warning design, and climate-data pipelines
- Case studies with anonymized impact metrics (alert lead time, false-positive rate, energy savings)
- Open-source contributions and reproducible research notebooks to build developer trust
- Community channels (Discussions, Discord) for practitioners and researchers

### Analytics & Conversion Funnels

- Google Tag Manager for event taxonomy and privacy-compliant tracking
- Key events: page_view, alert_subscription, dashboard_engagement, report_download
- Funnel stages: Awareness → Evaluation → Trial → Adoption → Advocacy
- Cohort analysis and retention dashboards powered by first-party analytics
- A/B testing of onboarding flows and call-to-action placement

Growth is measured by activated organizations, alert delivery reliability, and demonstrated reduction in heat-related incidents rather than vanity traffic metrics.

---

## Prerequisites

- Node.js 20 LTS or later
- Docker 24+ and Docker Compose
- PostgreSQL 16 (or use the provided Docker service)
- Redis 7 (or use the provided Docker service)
- Git

Optional for local ML experimentation:
- Python 3.11+
- CUDA-capable GPU (for model training)

---

## Installation

```bash
# Clone the repository
git clone https://github.com/Devleo05/ushnaupaay.git
cd ushnaupaay

# Copy environment template
cp .env.example .env
# Edit .env with your configuration values

# Start infrastructure services
docker compose up -d postgres redis

# Install dependencies
npm ci

# Run database migrations
npm run db:migrate

# Seed reference data (optional)
npm run db:seed

# Start development servers
npm run dev
```

The web application will be available at `http://localhost:3000`.  
API documentation is served at `http://localhost:3000/api/docs`.

### Production Build

```bash
npm run build
npm run start
```

Or via Docker:

```bash
docker compose -f docker-compose.prod.yml up -d --build
```

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

<div align="center">

**UshnaUpaay** — turning heat risk into measurable resilience.

[Repository](https://github.com/Devleo05/ushnaupaay) · [Issues](https://github.com/Devleo05/ushnaupaay/issues) · [Discussions](https://github.com/Devleo05/ushnaupaay/discussions)

</div>
