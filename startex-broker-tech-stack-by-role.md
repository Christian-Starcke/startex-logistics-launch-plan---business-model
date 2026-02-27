## StarTex Logistics – Tech Stack by Role & Responsibility

This document translates the role structure in `startex-broker-org-structure.md` into a **concrete tech stack** and shows **which responsibilities each tool supports**. It’s written so it can be shared externally (e.g. with vendors, advisors, or hires).

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
- **CRM (Sales Hub)** – *HubSpot (starter) or similar*
  - Track shipper accounts, contacts, and opportunities
  - Log calls, emails, meetings
  - Manage pipeline and forecast volume
- **Email & Calendar** – *Google Workspace (Gmail + Calendar)*
  - Shipper-facing communication and meeting scheduling
  - Calendar for follow-ups and bid deadlines
- **Sales Engagement / Sequencing (Optional Phase 2)** – *HubSpot Sequences or similar*
  - Automated outbound sequences to targeted chemical manufacturers
  - Template library for outreach
- **Data & Prospecting (Optional)** – *NAICS / industry databases, LinkedIn Sales Navigator*
  - Build lists of target chemical manufacturers (NAICS 325110, $50M–$250M)
  - Enrich accounts with decision-maker info
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
- **CRM**
  - Single source of truth for existing accounts (volumes, lanes, contacts)
  - Track expansions into new lanes/modes
- **TMS (Transportation Management System)**
  - View historical load data by shipper (volume, lanes, service performance)
  - Support lane forecasting and service review prep
- **Analytics & Reporting**
  - Simple **BI layer** (Google Sheets + Looker Studio or built-in TMS reports)
  - Shipper scorecards: on‑time %, claims, spend, lane volume
- **Communication Tools**
  - Google Workspace (Gmail, Meet) for QBRs / service reviews

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
- **TMS**
  - Core workspace for posting loads, assigning carriers, tracking status
  - Carrier profiles (lanes, equipment, performance history)
- **Load Board**
  - **DAT Loadboard** for posting freight and sourcing spot capacity
  - Integrated with TMS where possible
- **Carrier Directory / Sourcing**
  - **Carrier Source** or similar for carrier discovery and rating
- **Communication**
  - Google Voice / phone system for carrier calls
  - SMS-capable tools or in‑app messaging (where supported by TMS)
- **Rate Intelligence**
  - **DAT RateView** for live market rate benchmarks

---

### Carrier Development / Carrier Sales

**Key Responsibilities**  
- Onboard new carriers at scale  
- Build long-term capacity pools  

**Core Tech Stack**
- **TMS + Carrier Database**
  - Structured carrier onboarding workflow (documents, insurance, authority)
  - Tags for preferred lanes, equipment, and performance
- **e-Signature Tool**
  - For Broker–Carrier Agreements (e.g. DocuSign, PandaDoc)
- **Compliance & Verification**
  - Integration or process with **SAFER**, insurance verification portals

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
- **TMS**
  - Load lifecycle management (pickup → in transit → delivered → invoiced)
  - Document storage (rate cons, BOLs, PODs)
- **Track & Trace Tools**
  - TMS built‑in tracking or integrations (ELD/telematics, carrier apps)
  - Email/SMS automations for status updates (where supported)
- **Shared Communication**
  - Google Workspace (Gmail, Calendar, Drive) for appts & doc sharing
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
- **TMS + Tracking Module**
  - Central place to log location updates and ETA changes
  - Standard workflow/checklist per load
- **Dialer / Call System**
  - VoIP system (e.g. Google Voice or lightweight call center tool)
- **Automation (Phase 2)**
  - Automated location pings via app/ELD integrations
  - Simple RPA/n8n flows to notify reps when loads go off‑schedule

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
  - DAT RateView (and similar tools) for market benchmarks
- **Data Workspace**
  - Google Sheets + Looker Studio or BI tool on top of TMS export
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
  - Google Sheets for bid grids, lane modeling
  - BI on top of historical TMS data for win‑rate and profitability
- **Document Management**
  - Google Drive folders for RFPs, proposals, and contracts
- **e-Signature**
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
- **TMS + BI**
  - On‑time %, claims, dwell, and service metrics by shipper
- **Reporting Layer**
  - Looker Studio / Power BI on top of TMS + QuickBooks
  - Standard QBR decks (Google Slides) fed from these reports
- **Ticketing / Support (Optional)**
  - Simple shared inbox in Gmail
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
  - QuickBooks Online as the financial system of record
- **TMS ↔ Accounting Integration**
  - Push loads from TMS to QuickBooks for invoicing & payables
- **Factoring Platform**
  - Freight factoring portal for invoice submission and funding
- **Document Storage**
  - Google Drive for invoices, rate cons, and supporting docs

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
  - SAFER, insurance certificate tracking, and TMS carrier compliance fields
- **Policy & Playbooks**
  - Internal Google Docs for risk thresholds, approval workflows

---

## 7️⃣ Compliance & Safety

### Carrier Compliance

**Key Responsibilities**  
- Insurance validation  
- Authority checks  
- Safety ratings  
- Fraud detection  

**Core Tech Stack**
- **Compliance Workflow in TMS**
  - Required fields for insurance, authority, safety rating
  - Expiry reminders for insurance renewals
- **External Data Sources**
  - SAFER, FMCSA portals, carrier insurance portals
- **Document Management**
  - Google Drive folders per carrier for certificates and agreements

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
  - Centralize TMS + QuickBooks + CRM data (could start with BigQuery or Postgres)
- **Automation Platform**
  - n8n or similar tool to automate repetitive workflows (status updates, notifications, basic matching)
- **Optimization & AI (Longer-Term)**
  - Python/SQL analytics stack or vendor tools for routing + pricing
  - Experimentation layer for AI-assisted pricing and load matching

---

## 9️⃣ Summary View – Core Systems by Function

- **TMS** – Operational backbone: loads, carriers, track & trace, documents  
- **CRM** – Shipper relationship + revenue pipeline (AE/AM)  
- **Load Board & Rate Tools** – DAT Loadboard + RateView for capacity and pricing  
- **Accounting (QuickBooks) + Factoring** – Cash flow, invoicing, payables  
- **Compliance Stack** – SAFER + insurance verification + TMS fields  
- **Collaboration Stack** – Google Workspace (Gmail, Drive, Docs, Sheets, Slides, Meet)  
- **Automation / Data (Phase 2+)** – n8n, BI, basic data warehouse for reporting and optimization  

This stack keeps **startup complexity low** while directly supporting the **specialized roles and responsibilities** defined in `startex-broker-org-structure.md`.

