# Real-Time Chat (Java + Spring Boot + React)

> Multi-room chat with **<300ms latency**, WebSocket pub/sub, JWT auth, and durable history.

## Why
I wanted a production-style chat that demonstrates **ownership across the SDLC**: design, build, test, release.

## Architecture
- **Backend:** Spring Boot (MVC), WebSocket/STOMP, Spring Security (JWT), Hibernate/JPA (audit)
- **Store:** MongoDB (messages, rooms, indexes), Redis (rate-limit, presence)
- **Frontend:** React (hooks), WebSocket client
- **Ops:** Docker Compose, GitHub Actions, semantic releases

[React UI] ⇄ [Gateway/API] ⇄ [WebSocket Broker]
│
[MongoDB + Redis]

## Key Features
- JWT login, RBAC (admin/mod/user)
- Reliable delivery (ack + retry), typing indicators
- **Rate limiting** via Redis to protect infra
- Message search with MongoDB text indexes

## Performance
- p95 message round-trip: **<300ms** on local 1k CCU test
- Load tests via k6 (scripts in `/load`)

## Getting Started
```bash
git clone https://github.com/<you>/realtime-chat.git
cd realtime-chat
docker compose up -d  # brings up api, mongo, redis, web
```


---

# GitHub README — CRM Automation (paste as README.md)

```markdown
# Internal CRM Automation (Spring Boot MVC + MySQL + Redis)
```
> Modular **Zoho-replacement** CRM built with Spring MVC, Hibernate/JPA, and MySQL—focused on latency, correctness, and release discipline.

## Modules
- Lead intake (CSV/API), pipeline stages, SLA & rules engine
- User & roles, audit, notifications

## Architecture
- Spring MVC controllers → service layer → JPA repos
- **MySQL** (normalized schema + indexes)
- **Redis** caching (lookups), cache-key invalidation strategy
- Observability: Micrometer + logs (JSON) + dashboards

## Highlights
- **@Transactional** boundaries and batch inserts for bulk intake
- p95 endpoint latency **<150ms** on standard list/detail flows
- Pagination + filtering with safe sorting (whitelist)

## Run Locally
```bash
git clone https://github.com/<you>/crm-automation.git
cd crm-automation
docker compose up -d  # mysql + redis
./mvnw spring-boot:run
```


---

# GitHub README — E-commerce (MERN) (paste as README.md)

```markdown
# E-commerce (MERN)
```

> Full-featured store: auth, product catalog, cart, checkout, payments, and admin.

## Stack
- **Backend:** Node/Express, MongoDB (Mongoose)
- **Frontend:** React (Vite), Redux Toolkit
- **Payments:** Stripe/Razorpay
- **Ops:** Docker Compose, GitHub Actions

## Features
- JWT auth, roles (admin/customer)
- Product CRUD, images, search & filters
- Cart, orders, webhooks for payment success
- Admin dashboard (orders, refunds)

## Local Setup
```bash
git clone https://github.com/<you>/mern-store.git
cd mern-store
docker compose up -d
```

