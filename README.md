# Sarita Infotech Website & Workflow Demonstration

React + TypeScript + Vite demonstration application for the Sarita Infotech public website, customer support, admin operations, demo scheduling and partner portal.

## Run locally

```bash
cd /Users/pranay/Documents/Development/CodexWork/sarita-infotech-web
npm install
npm run dev
```

Then open the URL printed by Vite (normally `http://localhost:5173`). Production verification:

```bash
npm run build
npm run preview
```

## Demo mode

This is an explicitly isolated client-side demonstration. Any valid-format email and a password of eight or more characters opens the matching portal. Data lives only in the active browser session and is never presented as real, persistent, multi-user data.

- `/customer/login` leads to customer support. New registrations remain **Pending Approval**.
- `/admin/login` opens the clearly-labelled mock admin workspace.
- `/partners/login` opens the isolated mock partner workspace.
- `/request-demo` creates a request with **Awaiting Confirmation** status; it never claims a calendar booking or email notification.

## Implemented workflows

- Public marketing routes, product pages, service/industry informational routes, legal pages, responsive navigation, branded 404, robots directives and sitemap.
- Four product detail pages, including clearly qualified ABDM and NHCX sections on Sarita HealthCare.
- Customer route protection, registration approval messaging, dashboard, ticket list/search, ticket creation, ticket details and customer replies.
- Admin route protection, metrics derived from mock records, ticket workspace, ticket assignment/status controls, customer-only/internal note separation, and demo status controls.
- Partner route protection, partner dashboard and isolated lead-registration experience.

## Production integration checklist

Before using this beyond demonstration mode, connect a server-side auth provider (for example Supabase Auth) and database; implement row-level organization isolation and roles; move ticket/demo/lead ID generation to the database; validate inputs server-side; store attachments privately; add audit history; configure CSRF/rate limiting/session security; integrate transactional email and an availability-aware calendar; add accessibility and security testing; then replace all mock-mode labels only after those systems are verified.

Suggested core tables: `profiles`, `organizations`, `organization_members`, `customer_accounts`, `tickets`, `ticket_messages`, `ticket_internal_notes`, `ticket_history`, `ticket_attachments`, `demo_requests`, `demo_appointments`, `partners`, `partner_leads`, `partner_opportunities`, and `notifications`.
