# Project Specification: Alt Lending - Signal-Based Lead Generation

## Project Overview
Real-time Signal-Based Lead Generation and Engagement System that continuously monitors public web sources and social media for positive financial signals associated with lead segments. The system identifies key moments of improved financial capacity (new jobs, promotions, professional license renewals) to enable repayment conversations at the most opportune times, dramatically increasing engagement and conversion rates.

**Target Market:** "Second Chance" Borrowers
- Demographics: 21-30 years old, United States
- Loan Status: 90+ days delinquent on federal or private student loans
- Pain Points: Overwhelmed by debt, aggressive collection calls, credit score concerns
- Goals: Lower monthly payments, simple path out of delinquency, financial control

## Project Goals and Objectives

### Real-time Monitoring
Establish a continuous monitoring system that tracks predefined financial signals across public web sources and social media for target lead segments

### Context-Aware Engagement
Provide actionable insights and context-aware engagement opportunities based on monitored signals

### Timely Outreach
Enable timely outreach to leads at the precise moment their financial capacity shows signs of improvement

### Increased Conversion Rates
Achieve a measurable increase in the conversion rate of leads into active repayment plans

## Requirements

### Phase 1: Discovery and Strategy

**Collaborative Workshop:**
- Define target lead segments
- Identify key financial signals to monitor
- Establish signal prioritization criteria

**Data Source Identification:**
- LinkedIn profile updates and activity (primary data source)
- Apify scraper for LinkedIn

**System Architecture:**
- Technical specifications documentation
- Data flow diagrams
- Security and compliance requirements
- Integration architecture with existing CRM

### Phase 2: System Development and Implementation

**Data Scraping and Aggregation:**
- Apify scraper integration for LinkedIn
- Rate limiting and respectful crawling
- Data deduplication and normalization
- Error handling and retry logic
- Compliance with robots.txt and LinkedIn Terms of Service

**NLP Models for Signal Detection:**
- Natural Language Processing for job announcements
- Entity recognition for names and companies
- Sentiment analysis for career updates
- Classification models for signal types:
  - New employment
  - Promotions/raises
  - Professional certifications
  - License renewals
  - Awards and recognition
  - Business launches
  - Educational achievements

**Centralized Database:**
- Lead profile storage
- Signal history tracking
- Timestamp and metadata for each signal
- Relationship mapping (lead → signals)
- Data retention policies
- Archive and purge mechanisms

**CRM API Integration:**
- Secure REST API for CRM communication
- Real-time signal push to CRM
- Lead enrichment with signal data
- Bidirectional sync capabilities
- Webhook support for event notifications
- Authentication and authorization (OAuth 2.0)

### Phase 3: Dashboard and Alerting

**Web-Based Dashboard:**
- Real-time signal feed
- Lead profile views with signal history
- Filtering and search capabilities
- Signal prioritization and scoring
- Analytics and reporting:
  - Signals detected per day/week
  - Conversion rates by signal type
  - Team response times
  - Engagement outcomes
- Role-based access control
- Responsive design (desktop, tablet, mobile)

**Daily Digest Alerting:**
- Email alerts with all detected signals
- Alert organization by priority level
- Digest customization by signal type and priority
- Alert routing to specific team members
- Escalation rules for unactioned signals

### Phase 4: Training and Handover (Day 10)

**Team Training:**
- System usage and navigation training
- Best practices for signal-based outreach
- Dashboard functionality walkthrough
- Alert management training
- CRM integration usage
- Troubleshooting common issues

**Project Documentation:**
- User Manual (dashboard and alert usage)
- Technical Specifications (system architecture, APIs)
- Data Source Documentation (scrapers, update frequency)
- CRM Integration Guide
- Handover Report (system status, credentials, access)
- Runbooks for common operations

### Phase 5: Compliance and Monitoring (Day 11)

**Comprehensive Logging:**
- Log all scraping activity (timestamp, borrower, source URL, success/failure)
- Alert and email audit trail
- System error logging
- Rate limiting incident tracking

**Compliance Enforcement:**
- Rate limiting enforcement and monitoring
- Robots.txt compliance verification
- User-agent configuration validation
- Automated compliance checklist

**Opt-Out Mechanism:**
- "Do not scrape" flag in database
- Admin UI for opt-out management
- Borrower-facing opt-out request form
- Automatic exclusion from scraping jobs

**Admin Monitoring:**
- Real-time admin dashboard with metrics
- Daily admin summary email:
  - Total profiles scraped
  - Total signals detected
  - Total alerts sent
  - System errors/failures
  - Rate limiting incidents
  - Compliance status

**Deliverables:**
- Comprehensive logging system
- Rate limiting enforcement
- Opt-out functionality
- Compliance verification dashboard
- Admin monitoring dashboard
- Daily admin summary email system
- Activity audit trail
- Compliance documentation

## Technical Requirements

### Data Collection Infrastructure
- Apify scraper for LinkedIn data collection
- Google Custom Search JSON API for company domain discovery
- Firecrawl MCP for company About page scraping
- Proxy rotation for IP management
- CAPTCHA handling (when necessary and legal)
- Scheduled job execution (cron, Airflow)

### Machine Learning & NLP
- NLP library (spaCy, NLTK, or Hugging Face Transformers)
- Named Entity Recognition (NER) models
- Text classification models
- Model training pipeline
- Model versioning and deployment

### Backend Services
- RESTful API (Node.js, Python Flask/FastAPI, or similar)
- Authentication service (JWT, OAuth 2.0)
- Background job processing (Celery, Bull)
- Caching layer (Redis)
- Message queue (RabbitMQ, Kafka)

### Database
- Supabase (PostgreSQL-based with real-time features)
  - **Leads table** - Complete debtor/lead information including:
    - Core identity: debtor_name, agency_id_number, loan_number, tax_id, dob
    - Contact info: address, city, state, zip, phone_1, phone_2, email
    - Financial data: org_creditor, referral_amount, received_total, total_due, last_payment_amount
    - Dates & status: referral_date, item_date_c_off, agency_last_payment_date, pcg_last_payment_date, status_description
    - AI enhancement fields: companyDomain (VARCHAR(255) NULL), companyAbout (TEXT NULL)
    - System fields: id, created_at, updated_at
  - Built-in authentication and Row Level Security
  - Real-time subscriptions for data changes
- Time-series data optimization
- Full-text search capabilities (Elasticsearch)
- Automatic backup and recovery

### Frontend Dashboard
- Modern web framework (React)
- Responsive design
- Real-time updates (WebSockets or Server-Sent Events)
- Tailwind CSS for styling

### Monitoring & Alerts
- Email service integration (Brevo)
- System monitoring (Datadog, New Relic, or Prometheus)
- Error tracking (Sentry)
- Uptime monitoring

### Security & Compliance
- FCRA (Fair Credit Reporting Act) compliance
- FDCPA (Fair Debt Collection Practices Act) compliance
- TCPA (Telephone Consumer Protection Act) compliance
- Data privacy regulations (CCPA, GDPR where applicable)
- Encryption at rest and in transit (TLS 1.3)
- Audit logging for all data access
- Opt-out mechanisms for borrowers
- Secure credential management (AWS Secrets Manager, HashiCorp Vault)

## Deliverables

### 1. Signal-Based Lead Generation System
Fully functional, deployed system capable of:
- Monitoring multiple data sources
- Detecting and classifying financial signals
- Storing signal history and metadata
- Providing real-time alerts

### 2. CRM Integration
- Seamless API-based integration with existing CRM
- Real-time signal push to CRM records
- Lead enrichment with signal context
- Webhook endpoints for CRM events

### 3. Web-Based Dashboard
- User-friendly interface for signal monitoring
- Lead profile views with signal timelines
- Analytics and reporting
- Role-based access control
- Mobile-responsive design

### 4. Project Documentation
- **User Manual:** Dashboard navigation, alert management, best practices
- **Technical Specifications:** Architecture, APIs, database schema
- **Data Source Documentation:** Scraper configurations, update schedules
- **CRM Integration Guide:** API endpoints, authentication, data formats
- **Handover Report:** System status, credentials, access instructions

## Acceptance Criteria

### System Functionality
- Successfully monitors and identifies positive financial signals
- Alerts trigger within 24 hours of signal detection
- System tracks job changes, promotions, and professional certifications
- NLP models achieve >80% accuracy in signal classification
- Web scraping operates within legal and ethical boundaries

### Performance
- Signal detection latency < 24 hours from public posting
- Dashboard loads in < 3 seconds
- Real-time alerts delivered within 5 minutes of detection
- System handles 10,000+ leads without performance degradation
- 99.5% uptime SLA

### Integration
- CRM API integration is functional and tested
- Signal data populates in CRM records automatically
- Bidirectional sync maintains data consistency
- API authentication is secure and compliant

### User Experience
- Dashboard is intuitive and requires minimal training
- Alert customization meets team workflow needs
- Role-based access prevents unauthorized data access
- Mobile access allows monitoring on-the-go

### Documentation & Training
- All team members trained on system usage
- Documentation is comprehensive and clear
- Handover includes all credentials and access
- Runbooks cover common operational scenarios

## Expected Outcomes

### Conversion Rate Improvement
- Dramatic increase in conversion rates by initiating conversations at optimal moments
- Target: 20-40% improvement in lead-to-recovery conversion for signal-triggered outreach
- Higher engagement rates due to contextual, timely messaging

### Operational Efficiency
- Real-time alerts for high-priority financial signals
- Reduced time spent on unproductive outreach
- Focused efforts on leads with improved financial capacity
- Context-aware engagement enabling personalized conversations

### Measurable Business Impact
- Measurable uplift in lead-to-recovery conversion rates
- Reduction in average days to payment
- Increased revenue from recovered accounts
- Better borrower experience through empathetic, timely outreach

## Timeline
**Total Duration: 12 Days**

- **Day 1-2:** Phase 1 - Discovery and Strategy
- **Day 3-7:** Phase 2 - System Development and Implementation
- **Day 8-9:** Phase 3 - Dashboard and Alerting
- **Day 10:** Phase 4 - Training and Handover
- **Day 11:** Phase 5 - Compliance and Monitoring

## Dependencies
- Access to existing lead database and CRM system
- CRM API access and documentation
- Legal approval for web scraping and data collection activities
- Email service provider account (Brevo)
- Cloud infrastructure (Google Cloud Platform)
- Third-party API access where required
- Compliance review and approval

## Out of Scope
- Content creation for outreach campaigns (email templates, call scripts)
- Management and execution of outreach campaigns
- Integration with systems other than the specified CRM
- Ongoing system maintenance beyond initial post-launch period
- Costs associated with third-party data providers or API subscriptions

## Notes
- System focuses on public data sources only - no unauthorized access
- All scraping activities must comply with website Terms of Service and robots.txt
- Ethical considerations: signals should inform timing, not manipulate vulnerable borrowers
- Privacy-first approach: only collect necessary data, implement opt-out mechanisms
- Consider FCRA implications of using automated signals for decision-making
- Plan for regular model retraining as signal patterns evolve
- Build in feedback loops to improve signal quality over time
