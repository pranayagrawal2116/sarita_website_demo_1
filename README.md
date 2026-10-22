# Sarita Infotech Website & Operations Demonstration

A modern React + TypeScript + Vite web platform and workflow demonstration for **Sarita Infotech Pvt. Ltd.**, showcasing public product and service showcases, an interactive customer support ticketing system, an admin operations workspace, partner lead management, and demo scheduling.

🌐 **Live Website URL**: [https://pranayagrawal2116.github.io/sarita_website_demo_1/](https://pranayagrawal2116.github.io/sarita_website_demo_1/)

---

## 🌟 Overview

This prototype models a complete corporate web presence and operational workflow suite for enterprise and institutional clients:

- **Public Marketing & Solutions**: Comprehensive product landing pages, solutions by industry, services, resources, company overview, contact form, and SEO essentials (`robots.txt`, `sitemap.xml`).
- **Core Product Suite**:
  - 🏥 **Sarita HealthCare**: Connected hospital information system covering patient administration, clinical operations, billing, diagnostics, pharmacy, and ABDM / NHCX digital health interoperability readiness.
  - 🚢 **Sarita Nimble**: Trade documentation, export/import management, shipment tracking, compliance, and invoice workflows.
  - 🏦 **Sarita BankWare**: Core cooperative banking and credit society operations platform for deposits, loans, collections, and branch reporting.
  - 🛍️ **Sarita Retail**: Unified inventory management, point-of-sale, purchase workflows, and multi-location visibility.
- **Customer Support Portal (`/customer`)**: Role-protected dashboard for tracking support requests, submitting new tickets with category/priority/attachments, and conversing with support agents.
- **Admin Operations Console (`/admin`)**: Operations management queue for cross-account tickets, assignment, internal notes separation, status updates, and interactive demo agenda management.
- **Partner Portal (`/partners`)**: Dedicated workspace for registered channel partners to register leads, track opportunities, and access enablement resources.
- **Demo Request System (`/request-demo`)**: Interactive scheduling flow with product selection, date validation, and reference ID generation.

---

## 🚀 Quick Start

### Prerequisites
- Node.js (v18.0.0 or higher recommended)
- npm or yarn

### Installation & Local Run

```bash
# Clone the repository
git clone https://github.com/pranayagrawal2116/sarita_website_demo_1.git
cd sarita_website_demo_1

# Install dependencies
npm install

# Start Vite development server
npm run dev
```

Open the local development URL (typically `http://localhost:5173`) in your browser.

### Production Build

```bash
# Type check and build bundle
npm run build

# Preview production build locally
npm run preview
```

---

## 🔑 Demo Mode & Access Credentials

This application runs in an isolated client-side demonstration mode with in-memory state:
- Any valid email address (e.g., `user@example.com`) and a password of **8 or more characters** will authenticate.
- **Portals**:
  - `/customer/login`: Customer Support Portal (pre-seeded with demo account *Asterwell Hospital*)
  - `/admin/login`: Operations Admin Console
  - `/partners/login`: Channel Partner Portal
  - `/request-demo`: Request product demonstrations with reference code assignment

> [!NOTE]
> All session data lives purely in the active browser memory for safe demonstration purposes. No persistent customer data or real emails are dispatched in demo mode.

---

## 🛠️ Tech Stack

- **Framework**: React 18
- **Language**: TypeScript (strict mode)
- **Bundler & Dev Server**: Vite 5
- **Routing**: React Router v6 (`react-router-dom`)
- **Icons**: Lucide React (`lucide-react`)
- **Styling**: Modern responsive CSS with custom design tokens and semantic layout

---

## 📁 Project Structure

```text
sarita-infotech-web/
├── public/
│   ├── robots.txt          # Search crawler directives
│   └── sitemap.xml         # SEO site map
├── src/
│   ├── main.tsx            # Routes, portals, state, and UI components
│   ├── styles.css          # Responsive styling, layout grid, typography, tokens
│   └── vite-env.d.ts       # Vite client TypeScript declarations
├── index.html              # HTML5 entrypoint with metadata and fonts
├── package.json            # Project dependencies and build scripts
├── tsconfig.json           # TypeScript configuration
└── vite.config.ts          # Vite build and plugin configuration
```

---

## 📋 Production Integration Roadmap

To transition this demonstration into full multi-tenant production:
1. **Authentication & Identity**: Integrate an enterprise auth provider (e.g., Supabase Auth, Firebase Auth, or Auth0) with MFA and RBAC.
2. **Database & Persistence**: Implement PostgreSQL / Cloud SQL schema with Row-Level Security (RLS) for tenant isolation:
   - `profiles`, `organizations`, `customer_accounts`
   - `tickets`, `ticket_messages`, `ticket_internal_notes`, `ticket_attachments`
   - `demo_requests`, `demo_appointments`
   - `partners`, `partner_leads`, `partner_opportunities`
3. **Storage & Attachments**: Secure private object storage (S3 / GCS) with presigned upload URLs and virus scanning for ticket attachments.
4. **Notifications & Calendar**: Integrate transactional email/SMS (SendGrid, Postmark) and calendar availability sync (Google Calendar / Outlook / Cal.com).
5. **Auditing & Compliance**: Add immutable audit logging for administrative actions, ticket status modifications, and partner lead attribution.

---

## 📄 License

Private & Confidential · Developed for **Sarita Infotech Pvt. Ltd.**
