## StarTex Logistics – Tech Stack by Role & Responsibility

This document translates the role structure in `startex-broker-org-structure.md` into a **concrete tech stack** and shows **which responsibilities each tool supports**. It's written so it can be shared externally (e.g. with vendors, advisors, or hires).

---

## 🔗 Shared Infrastructure (Cross-Role Tools)

These tools are used by **multiple roles** across the organization:

- **CRM (Twenty – Open source)** – Shared by: AE, AM, Carrier Rep
- **TMS (Transportation Management System)** – Shared by: AM, Carrier Rep, Carrier Development, Operations Coordinator, Track & Trace, Customer Operations, Billing, Credit & Risk, Carrier Compliance, Network Optimization
- **Sales Engagement – Calls (Custom Power-Dialer)** – Shared by: AE, Carrier Rep
- **Sales Engagement – Email (Instantly.ai)** – Shared by: AE, Carrier Rep
- **Sales Engagement – LinkedIn (Sprouts/HeyReach)** – Shared by: AE, Carrier Rep
- **Google Workspace** (Gmail, Calendar, Drive, Docs, Sheets, Slides, Meet) – Shared by: AE, AM, Carrier Rep, Operations Coordinator, Pricing Analyst, Bid/RFP Team, Customer Operations, Billing, Credit & Risk, Carrier Compliance
- **Google Meet** – Shared by: AE, AM, Customer Operations
- **Granola (AI Meeting Notetaker)** – Shared by: AE, AM
- **Google Drive** – Shared by: Operations Coordinator, Bid/RFP Team, Billing, Carrier Compliance
- **Google Sheets** – Shared by: AM, Pricing Analyst, Bid/RFP Team
- **DAT RateView** – Shared by: AE, AM, Carrier Rep, Pricing Analyst
- **SAFER** – Shared by: Carrier Rep, Carrier Development, Credit & Risk, Carrier Compliance
- **e-Signature (DocuSign/PandaDoc)** – Shared by: AE, Carrier Development, Bid/RFP Team
- **Fraud Detection System** – Shared by: Credit & Risk, Carrier Compliance
- **QuickBooks Online** – Shared by: Billing, Customer Operations (reporting)
- **n8n (Automation Platform)** – Shared by: Track & Trace, Network Optimization

---

## 1️⃣ Shipper Acquisition (Revenue Side)

### Shipper Sales Rep / Account Executive (AE)

**Key Responsibilities (from org structure)**  
- Prospect & close shippers  
- Negotiate pricing frameworks  
- Lane discovery  
- Contract setup  
- Relationship ownership  
- Forecast volume  

**Core Tech Stack**
- **CRM (Sales Hub)** – *Twenty (Open source)* *(Shared with AM)*
  - Track shipper accounts, contacts, and opportunities
  - Log calls, emails, meetings
  - Manage pipeline and forecast volume
- **Lead Data Source** – *Apollo.io*
  - Build lists of target chemical manufacturers (NAICS 325110, $50M–$250M)
  - Access company and contact databases for prospecting
- **Lead Enrichment** – *Clay or Custom*
  - Enrich accounts with decision-maker info
  - Data enrichment and contact verification
- **Sales Engagement – Email** – *Instantly.ai* *(Shared with Carrier Rep)*
  - Automated outbound email sequences to targeted chemical manufacturers
  - Template library for outreach
  - Email deliverability and tracking
- **Sales Engagement – Calls** – *Custom Power-Dialer* *(Shared with Carrier Rep)*
  - Power-dialing system for high-volume outbound calls
  - Call logging and tracking integration with CRM
- **Sales Engagement – LinkedIn** – *Sprouts / HeyReach* *(Shared with Carrier Rep)*
  - LinkedIn outreach automation and sequencing
  - Connection requests and messaging automation
- **Email & Calendar** – *Google Workspace (Gmail + Calendar)* *(Shared across multiple roles)*
  - Shipper-facing communication and meeting scheduling
  - Calendar for follow-ups and bid deadlines
- **Virtual Meeting Infrastructure** – *Google Meet* *(Shared with AM, Customer Operations)*
  - Video meetings with shippers and prospects
  - Integrated with Google Calendar for scheduling
- **AI Meeting Notetaker** – *Granola* *(Shared with AM)*
  - Automated meeting notes and summaries
  - Action items and follow-up tracking
- **Rate Intelligence** – *DAT RateView* *(Shared with AM, Carrier Rep, Pricing Analyst)*
  - Market rate benchmarks for pricing negotiations
  - Lane rate intelligence for lane discovery
- **Lane Intelligence / Analytics**
  - TMS historical lane data exports
  - DAT lane analytics for lane discovery and opportunity identification
- **e-Signature Tool** – *DocuSign / PandaDoc* *(Shared with Carrier Development, Bid/RFP Team)*
  - Contract execution and setup with shippers
- **Digital Presence**
  - Company **website** (StarTex Logistics site) for credibility
  - **Branded email domain** (e.g. `@startexlogistics.com`)

---

### Account Manager (AM)

**Key Responsibilities**  
- Daily customer contact  
- Forecasting lanes  
- Rate discussions  
- Service reviews  
- Expansion into new modes/lanes  

**Core Tech Stack**
- **CRM** *(Shared with AE)*
  - Single source of truth for existing accounts (volumes, lanes, contacts)
  - Track expansions into new lanes/modes
- **TMS (Transportation Management System)** *(Shared across operations, carrier, and financial roles)*
  - View historical load data by shipper (volume, lanes, service performance)
  - Support lane forecasting and service review prep
- **Analytics & Reporting**
  - Simple **BI layer** (Google Sheets + Looker Studio or built-in TMS reports)
  - Shipper scorecards: on‑time %, claims, spend, lane volume
- **Rate Intelligence** – *DAT RateView* *(Shared with AE, Carrier Rep, Pricing Analyst)*
  - Market rate benchmarks for rate discussions with shippers
- **Communication Tools**
  - Google Workspace (Gmail, Meet) for QBRs / service reviews *(Shared across multiple roles)*
  - **AI Meeting Notetaker (Granola)** *(Shared with AE)* for automated QBR notes and action items

---

## 2️⃣ Capacity Procurement (Supply Side)

### Carrier Rep / Capacity Rep

**Key Responsibilities**  
- Source carriers  
- Negotiate buy rates  
- Build carrier relationships  
- Vet compliance  
- Cover loads  

**Core Tech Stack**
- **TMS** *(Shared across operations, carrier, and financial roles)*
  - Core workspace for posting loads, assigning carriers, tracking status
  - Carrier profiles (lanes, equipment, performance history)
- **CRM** *(Shared with AE, AM)*
  - Track carrier relationships, contacts, and opportunities
  - Log calls, emails, meetings with carriers
  - Manage carrier pipeline and capacity commitments
- **Load Board**
  - **DAT Loadboard** for posting freight and sourcing spot capacity
  - Integrated with TMS where possible
- **Carrier Directory / Sourcing**
  - **Carrier Source** or similar for carrier discovery and rating
- **Sales Engagement – Calls** – *Custom Power-Dialer* *(Shared with AE)*
  - Power-dialing system for high-volume outbound calls to carriers
  - Call logging and tracking integration with CRM
- **Sales Engagement – Email** – *Instantly.ai* *(Shared with AE)*
  - Automated email sequences to new and existing carriers
  - Template library for carrier outreach
  - Email deliverability and tracking
- **Sales Engagement – LinkedIn** – *Sprouts / HeyReach* *(Shared with AE)*
  - LinkedIn outreach automation to carrier decision-makers
  - Connection requests and messaging automation
- **Communication**
  - Google Voice / phone system for carrier calls
  - SMS-capable tools or in‑app messaging (where supported by TMS)
  - Google Workspace (Gmail, Calendar) *(Shared across multiple roles)*
- **Rate Intelligence**
  - **DAT RateView** *(Shared with AE, AM, Pricing Analyst)* for live market rate benchmarks
- **Compliance & Verification**
  - **SAFER** *(Shared with Carrier Development, Credit & Risk, Carrier Compliance)* for carrier authority, safety ratings, and compliance vetting
  - TMS compliance fields for tracking carrier credentials

---

### Carrier Development / Carrier Sales

**Key Responsibilities**  
- Onboard new carriers at scale  
- Build long-term capacity pools  

**Core Tech Stack**
- **TMS + Carrier Database** *(Shared across operations, carrier, and financial roles)*
  - Structured carrier onboarding workflow (documents, insurance, authority)
  - Tags for preferred lanes, equipment, and performance
- **e-Signature Tool** *(Shared with Bid/RFP Team)*
  - For Broker–Carrier Agreements (e.g. DocuSign, PandaDoc)
- **Compliance & Verification**
  - Integration or process with **SAFER** *(Shared with Credit & Risk, Carrier Compliance)*, insurance verification portals

---

## 3️⃣ Execution Layer (Operations)

### Operations Coordinator / Load Coordinator

**Key Responsibilities**  
- Dispatch confirmation  
- Track & trace  
- Appointment scheduling  
- Status updates  
- Exception handling  
- Documentation flow  

**Core Tech Stack**
- **TMS** *(Shared across operations, carrier, and financial roles)*
  - Load lifecycle management (pickup → in transit → delivered → invoiced)
  - Document storage (rate cons, BOLs, PODs)
- **Track & Trace Tools**
  - TMS built‑in tracking or integrations (ELD/telematics, carrier apps)
  - Email/SMS automations for status updates (where supported)
- **Shared Communication**
  - Google Workspace (Gmail, Calendar, Drive) *(Shared across multiple roles)* for appts & doc sharing
- **Issue Management**
  - Internal notes in TMS for exceptions
  - Shared Slack/Teams (optional) for internal war‑room comms

---

### Track & Trace Team

**Key Responsibilities**  
- Call drivers  
- Update tracking systems  
- Check milestones  
- Flag delays  

**Core Tech Stack**
- **TMS + Tracking Module** *(Shared across operations, carrier, and financial roles)*
  - Central place to log location updates and ETA changes
  - Standard workflow/checklist per load
- **Dialer / Call System**
  - VoIP system (e.g. Google Voice or lightweight call center tool)
- **Automation (Phase 2)**
  - Automated location pings via app/ELD integrations
  - Simple RPA/n8n flows *(Shared with Network Optimization)* to notify reps when loads go off‑schedule

---

## 4️⃣ Pricing & Margin Control

### Pricing Analyst / Market Pricing Team

**Key Responsibilities**  
- Market rate analysis  
- Bid pricing (RFPs)  
- Lane benchmarking  
- Spot vs contract strategy  

**Core Tech Stack**
- **Rate Intelligence**
  - DAT RateView *(Shared with Carrier Rep)* (and similar tools) for market benchmarks
- **Data Workspace**
  - Google Sheets *(Shared with AM, Bid/RFP Team)* + Looker Studio or BI tool on top of TMS export
  - Lane P&L dashboards, margin analysis
- **RFP Tooling (Lightweight)**
  - Structured templates in Google Sheets/Docs for bids
  - Optional RFP software later (for very large bids)

---

### Bid / RFP Team

**Key Responsibilities**  
- Annual shipper bids  
- Network modeling  
- Contract rate strategy  

**Core Tech Stack**
- **Spreadsheet + BI**
  - Google Sheets *(Shared with AM, Pricing Analyst)* for bid grids, lane modeling
  - BI on top of historical TMS data for win‑rate and profitability
- **Document Management**
  - Google Drive *(Shared with Operations Coordinator, Billing, Carrier Compliance)* folders for RFPs, proposals, and contracts
- **e-Signature** *(Shared with Carrier Development)*
  - DocuSign / PandaDoc for final contract execution

---

## 5️⃣ Customer Success & Service

### Customer Operations / Client Services

**Key Responsibilities**  
- Issue resolution  
- Reporting  
- KPI tracking  
- SLA compliance  
- Weekly/monthly reviews  

**Core Tech Stack**
- **TMS + BI** *(TMS shared across operations, carrier, and financial roles)*
  - On‑time %, claims, dwell, and service metrics by shipper
- **Reporting Layer**
  - Looker Studio / Power BI on top of TMS + QuickBooks *(QuickBooks shared with Billing)*
  - Standard QBR decks (Google Slides) fed from these reports
- **SLA Tracking & Compliance**
  - SLA-specific tracking dashboard in BI layer
  - Automated alerts for SLA violations
  - SLA compliance reporting by shipper
- **Ticketing / Support (Optional)**
  - Simple shared inbox in Gmail *(Google Workspace shared across multiple roles)*
  - Optional: lightweight helpdesk (e.g. Zendesk/Freshdesk) once volume is higher

---

## 6️⃣ Financial Operations

### Billing / Settlement Team

**Key Responsibilities**  
- Carrier payables  
- Shipper invoicing  
- Accessorial approvals  
- Margin validation  

**Core Tech Stack**
- **Accounting System**
  - QuickBooks Online *(Shared with Customer Operations for reporting)* as the financial system of record
- **TMS ↔ Accounting Integration** *(TMS shared across operations, carrier, and financial roles)*
  - Push loads from TMS to QuickBooks for invoicing & payables
- **Accessorial Approval Workflow**
  - Approval workflow in TMS or QuickBooks for accessorial charges
  - Document storage for accessorial approvals
- **Margin Validation Dashboard**
  - BI layer (Looker Studio / Power BI) for margin validation reports
  - Margin analysis by shipper, lane, and carrier
- **Factoring Platform**
  - Freight factoring portal for invoice submission and funding
- **Document Storage**
  - Google Drive *(Shared with Operations Coordinator, Bid/RFP Team, Carrier Compliance)* for invoices, rate cons, and supporting docs

---

### Credit & Risk

**Key Responsibilities**  
- Shipper credit checks  
- Carrier fraud prevention  
- Payment risk management  

**Core Tech Stack**
- **Credit Tools**
  - Shipper credit reports (e.g. Ansonia, Dun & Bradstreet, factoring provider tools)
- **Carrier Compliance**
  - SAFER *(Shared with Carrier Development, Carrier Compliance)*, insurance certificate tracking, and TMS carrier compliance fields *(TMS shared across operations, carrier, and financial roles)*
- **Fraud Detection System**
  - Red flag system in TMS for carrier fraud detection
  - Pattern recognition for suspicious carrier behavior
  - Integration with SAFER and credit tools for fraud prevention
- **Payment Risk Management**
  - Payment risk scoring/management system or workflow
  - Credit limit tracking and approval workflows
  - Risk threshold monitoring and alerts
- **Policy & Playbooks**
  - Internal Google Docs *(Google Workspace shared across multiple roles)* for risk thresholds, approval workflows

---

## 7️⃣ Compliance & Safety

### Carrier Compliance

**Key Responsibilities**  
- Insurance validation  
- Authority checks  
- Safety ratings  
- Fraud detection  

**Core Tech Stack**
- **Compliance Workflow in TMS** *(TMS shared across operations, carrier, and financial roles)*
  - Required fields for insurance, authority, safety rating
  - Expiry reminders for insurance renewals
- **External Data Sources**
  - SAFER *(Shared with Carrier Development, Credit & Risk)*, FMCSA portals, carrier insurance portals
- **Fraud Detection System**
  - Enhanced fraud detection/red flag system in TMS *(Shared with Credit & Risk)*
  - Pattern recognition for suspicious carrier behavior
  - Automated alerts for compliance violations
- **Document Management**
  - Google Drive *(Shared with Operations Coordinator, Bid/RFP Team, Billing)* folders per carrier for certificates and agreements

---

## 8️⃣ Technology & Optimization

### Network Optimization / Data Ops

**Key Responsibilities**  
- Routing optimization  
- Automation workflows  
- Load matching algorithms  
- AI pricing models  

**Core Tech Stack**
- **Data Warehouse / Central Store (Phase 2+)**
  - Centralize TMS *(Shared across operations, carrier, and financial roles)* + QuickBooks + CRM data (could start with BigQuery or Postgres)
- **Automation Platform**
  - n8n *(Shared with Track & Trace)* or similar tool to automate repetitive workflows (status updates, notifications, basic matching)
- **Optimization & AI (Longer-Term)**
  - Python/SQL analytics stack or vendor tools for routing + pricing
  - Experimentation layer for AI-assisted pricing and load matching

---

## 9️⃣ Summary View – Core Systems by Function

- **TMS** – Operational backbone: loads, carriers, track & trace, documents  
- **CRM (Twenty – Open source)** – Shipper relationship + revenue pipeline (AE/AM), carrier relationship management (Carrier Rep)  
- **Sales Stack** – Apollo.io (lead data), Clay/Custom (enrichment), Instantly.ai (email), Custom Power-Dialer (calls), Sprouts/HeyReach (LinkedIn) – *Shared by AE (shipper outreach) and Carrier Rep (carrier outreach)*  
- **Meeting Infrastructure** – Google Meet + Granola (AI meeting notes)  
- **Load Board & Rate Tools** – DAT Loadboard + RateView for capacity and pricing  
- **Accounting (QuickBooks) + Factoring** – Cash flow, invoicing, payables  
- **Compliance Stack** – SAFER + insurance verification + TMS fields  
- **Collaboration Stack** – Google Workspace (Gmail, Drive, Docs, Sheets, Slides, Meet)  
- **Automation / Data (Phase 2+)** – n8n, BI, basic data warehouse for reporting and optimization  

This stack keeps **startup complexity low** while directly supporting the **specialized roles and responsibilities** defined in `startex-broker-org-structure.md`.

