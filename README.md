# Alt Lending - Signal-Based Lead Generation System
## 📚 Project Documentation Hub

---

## 🎯 Project Overview

The **Signal-Based Lead Generation System** is a real-time AI-powered platform that monitors public data sources for positive financial signals about delinquent student loan borrowers. By detecting job changes, promotions, professional certifications, and other career milestones, the system enables timely, context-aware outreach that dramatically improves conversion rates.

**Expected Impact:** 20-40% improvement in lead-to-recovery conversion rates

---

## 📖 Documentation Structure

This project includes comprehensive documentation organized for different audiences and purposes:

### 🚀 Quick Start

| Document | Purpose | Best For |
|----------|---------|----------|
| **[QUICK_REFERENCE.md](./QUICK_REFERENCE.md)** | At-a-glance project info, current status, key metrics | Everyone - Start here! |
| **[project_spec.md](./project_spec.md)** | Complete project specification and requirements | Stakeholders, product owners |
| **README.md** | This file - documentation overview and navigation | First-time readers |

### 📋 Planning & Management

| Document | Purpose | Best For |
|----------|---------|----------|
| **[PROJECT_PLAN.md](./PROJECT_PLAN.md)** | Detailed master plan with all phases and tasks | Project managers, team leads |
| **[TIMELINE_ROADMAP.md](./TIMELINE_ROADMAP.md)** | Day-by-day timeline with parallel work streams | Everyone - See the schedule |
| **[ARCHITECTURE_DIAGRAM.md](./ARCHITECTURE_DIAGRAM.md)** | Visual system architecture and data flow | Engineers, architects |

### 📝 JIRA Cards (Implementation Tasks)

#### Epics
- `jira-card-signal-based-lead-generation.md` - Main project epic
- `jira-card-core-pipeline.md` - Core 5-stage AI pipeline
- `jira-card-solution-1-qualified-leads.md` - AI scoring system

#### Phase Stories
1. ✅ `jira-card-phase1-discovery.md` - Discovery & Strategy (COMPLETE)
2. 🔄 `jira-card-phase2-data-scraping.md` - Data Scraping Infrastructure (IN PROGRESS)
3. ⏳ `jira-card-phase2-nlp-models.md` - NLP Models & Signal Detection
4. ⏳ `jira-card-phase2-database-crm.md` - Database & CRM Integration
5. ⏳ `jira-card-phase3-dashboard.md` - Web Dashboard Development
6. ⏳ `jira-card-phase3-alerting.md` - Real-time Alerting System
7. ⏳ `jira-card-phase4-training-handover.md` - Training & Handover

---

## 📊 Project Status

**Current Phase:** Phase 2a - Data Scraping Infrastructure  
**Timeline:** Day 3-5 of 10  
**Status:** 🔄 In Progress  
**Last Updated:** December 1, 2025

### Progress Overview
```
Phase 1: Discovery ████████████████████ 100% ✅ Complete
Phase 2a: Scraping ██████░░░░░░░░░░░░░  30% 🔄 In Progress
Phase 2b: NLP      ░░░░░░░░░░░░░░░░░░░   0% ⏳ Pending
Phase 2c: Database ░░░░░░░░░░░░░░░░░░░   0% ⏳ Pending
Phase 3a: Dashboard░░░░░░░░░░░░░░░░░░░   0% ⏳ Pending
Phase 3b: Alerting ░░░░░░░░░░░░░░░░░░░   0% ⏳ Pending
Phase 4: Training  ░░░░░░░░░░░░░░░░░░░   0% ⏳ Pending
Phase 5: Compliance░░░░░░░░░░░░░░░░░░░   0% ⏳ Pending
```

### Current Focus
- Configuring Apify scraper for LinkedIn
- Configuring proxy rotation and rate limiting
- Building comprehensive LinkedIn scraper (profiles, job changes, promotions, certifications)
- Developing ETL pipeline for data aggregation
- Implementing compliance controls

---

## 🎯 Target Market

**"Second Chance" Borrowers**
- **Age:** 21-30 years old
- **Location:** United States
- **Status:** 90+ days delinquent on federal or private student loans
- **Pain Points:** Debt overwhelm, aggressive collections, credit concerns
- **Goals:** Lower payments, path out of delinquency, financial control

---

## 🔔 Financial Signals Monitored

### High-Priority Signals
1. **New Employment** - New job started
2. **Promotions** - Career advancement, title changes, raises
3. **Professional Certifications** - New licenses, credentials obtained
4. **License Renewals** - Active professional status maintained
5. **Awards & Recognition** - Industry accolades, achievements

### Medium-Priority Signals
6. **Business Launches** - Entrepreneurship, new business ventures
7. **Educational Achievements** - Degrees completed, continuing education
8. **Industry Speaking** - Conference presentations, thought leadership
9. **Publications** - Articles, books, professional contributions

---

## 📅 11-Day Project Timeline

```
┌─────────────────────────────────────────────────────────────────────┐
│  PHASE 1: Discovery & Strategy                      Days 1-2   ✅   │
│  • Workshops, data source vetting, architecture                     │
└─────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────┐
│  PHASE 2: System Development                        Days 3-7   🔄   │
│  ├─ 2a: Data Scraping (Days 3-5)              [IN PROGRESS]         │
│  ├─ 2b: NLP Models (Days 4-6)                 [UPCOMING]            │
│  └─ 2c: Database & CRM (Days 5-7)             [UPCOMING]            │
└─────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────┐
│  PHASE 3: Dashboard & Alerting                      Days 8-9   ⏳   │
│  ├─ 3a: Web Dashboard                                               │
│  └─ 3b: Daily Digest Alerts (Email)                                 │
└─────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────┐
│  PHASE 4: Training & Handover                       Day 10     ⏳   │
│  • Team training, documentation, system handover                    │
└─────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────┐
│  PHASE 5: Compliance & Monitoring                   Day 11     ⏳   │
│  • Logging, rate limiting, opt-out, admin dashboard                 │
└─────────────────────────────────────────────────────────────────────┘
```

**See [TIMELINE_ROADMAP.md](./TIMELINE_ROADMAP.md) for detailed day-by-day breakdown**

---

## 🛠️ Technology Stack

### Backend & Data
- **API Framework:** [Python Flask](https://flask.palletsprojects.com/) / [FastAPI](https://fastapi.tiangolo.com/) or Node.js Express
- **Scraping:** [Apify](https://docs.apify.com/) scraper for LinkedIn data collection
- **Company Enrichment:** [Google Custom Search JSON API](https://developers.google.com/custom-search/v1/introduction), [Firecrawl](https://docs.firecrawl.dev/) MCP
- **NLP/ML:** [spaCy](https://spacy.io/usage), [Hugging Face Transformers](https://huggingface.co/docs/transformers/index), [scikit-learn](https://scikit-learn.org/stable/user_guide.html)
- **Database:** [Supabase](https://supabase.com/docs) (PostgreSQL-based with real-time features)
- **Search:** [Elasticsearch](https://www.elastic.co/guide/index.html)
- **Queue:** [RabbitMQ](https://www.rabbitmq.com/getstarted.html) or [Kafka](https://kafka.apache.org/documentation/)
- **Cache:** [Redis](https://redis.io/docs/)

### Frontend & UI
- **Framework:** [React](https://react.dev/)
- **State Management:** Redux or Context API
- **UI Library:** [Tailwind CSS](https://tailwindcss.com/docs)
- **Real-time:** [WebSockets](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API) or Server-Sent Events

### Infrastructure & Monitoring
- **Cloud:** [Google Cloud Platform](https://cloud.google.com/docs)
- **Hosting:** [Vercel](https://vercel.com/docs)
- **Proxy Services:** [Bright Data](https://docs.brightdata.com/) or [ScraperAPI](https://www.scraperapi.com/documentation/)
- **Monitoring:** Datadog, New Relic, or Prometheus
- **Error Tracking:** [Sentry](https://docs.sentry.io/)
- **Email:** [Brevo](https://developers.brevo.com/) (formerly Sendinblue)
- **Security:** TLS 1.3, [OAuth 2.0](https://oauth.net/2/), [Google Cloud Secret Manager](https://cloud.google.com/secret-manager/docs)
- **Job Scheduling:** [Apache Airflow](https://airflow.apache.org/docs/) or [cron](https://crontab.guru/)

**See [ARCHITECTURE_DIAGRAM.md](./ARCHITECTURE_DIAGRAM.md) for complete architecture**

---

## 📞 Key Contacts

**Product Owner:** Josh  
**Project Lead:** Samy  
**Engineering Manager:** Brad  
**JIRA Instance:** https://automationarchitecture.atlassian.net/  
**Project Key:** AL  
**Documentation Location:** `/Users/brad/Engineering/Engineers/Samy/Alt-Lending/`

---

*Last Updated: December 1, 2025*  
*Version: 1.0*  
*Status: Phase 2a Active - Data Scraping Infrastructure*  
*Next Milestone: End of Day 5 - Scraping Complete*

---

**Ready to dive in? Start with [QUICK_REFERENCE.md](./QUICK_REFERENCE.md) for an at-a-glance overview, then explore the detailed documents based on your role!** 🚀
