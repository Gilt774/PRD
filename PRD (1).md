
# Product Requirements Document (PRD)
**Project:** Vercel Website Enhancement  
**Client:** Gilt Farms and Tech  

## 1. Overview
Enhance the Vercel-hosted website with:
- Stripe integration (test mode)
- Zapier email alerts
- Dark mode (auto + toggle)
- Built-in chat system
- Contact form + admin CMS

## 2. Goals & Metrics
| Goal | Metric |
|------|--------|
| Accept test payments | 100% functionality in test mode |
| Email alerts via Zapier | Instant notification |
| Dark mode usability | Auto + manual toggle |
| Chat system | Real-time response |
| Content editing | Secure and smooth |

## 3. Features

### 3.1 Stripe Integration
- Test mode setup with publishable and secret keys.
- Create checkout session, webhook handling, order confirmation.
- Store transaction in DB.

### 3.2 Zapier Integration
- Trigger email alerts on new contact or payment.
- Webhook for Zapier automation.

### 3.3 Dark Mode
- Supports system auto-detect and manual toggle.
- Theme persistence using cookies/localStorage.

### 3.4 Chat System (Built-in)
- Real-time (WebSocket) chat with visitor session ID.
- Admin responds from dashboard.
- Message history saved in DB.

### 3.5 Contact System
- Form fields: name, email, subject, message.
- Stores message in DB + sends alert via Zapier.

### 3.6 Admin CMS
- CRUD for pages, media uploads, and content editing.
- Authentication & role-based access.
- Admin dashboard for chat + contact replies.

## 4. Data Models
Includes Users, Pages, Orders, ContactMessages, ChatSessions, ChatMessages.

## 5. APIs & Routes
- `/api/payments/*`
- `/api/contact/*`
- `/api/chat/*`
- `/api/admin/*`
- `/api/webhooks/zapier`

## 6. Milestones
| Phase | Task | Duration |
|--------|------|----------|
| 1 | CMS setup | 2 weeks |
| 2 | Stripe test integration | 1 week |
| 3 | Contact + Zapier alerts | 1 week |
| 4 | Chat system | 2 weeks |
| 5 | Dark mode + testing | 1 week |

## 7. Hosting Instructions
Place `PRD.md` and `PRD.pdf` in `/public/docs/` on your Vercel project.  
They will be accessible via `/docs/PRD.pdf` and `/docs/PRD.md`.

## 8. Security & Compliance
- PCI compliance for Stripe.
- Input validation and XSS protection.
- Secure API tokens.

## 9. Future Enhancements
- Live Stripe mode.
- Chatbot integration.
- Multi-language support.
