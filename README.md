# NestFinder 🏠

> Find your PG. Fill your beds.

NestFinder is a multi-tenant SaaS platform that connects PG seekers with PG
operators across Bangalore, Hyderabad, and Pune — making the process of finding
and managing paying guest accommodation transparent, fast, and trustworthy.

---

## The Problem

Every year, thousands of college students, fresh graduates, working
professionals, and newly relocated couples land in an unfamiliar city and face
the same struggle: finding a decent PG without physically walking every street,
calling disconnected numbers, or getting misled by outdated listings.

On the supply side, PG operators struggle to keep beds filled and building
owners have no reliable channel to reach operators looking for new properties.

NestFinder solves both sides of this market.

---

## Who Is This For

| Role | Who They Are | What They Need |
|---|---|---|
| **Tenant** | Student / employee / couple new to the city | Search, filter, and contact verified PGs fast |
| **PG Operator** | Runs day-to-day PG operations (food, beds, maintenance) | List properties, manage availability, receive leads |
| **Building Owner** | Owns the property, wants to rent it to a PG operator | List building, receive enquiries from operators |

---

## Core Features (MVP)

### For Tenants
- Search PGs by city, area, gender type, sharing option, and budget
- View photos, amenities, rules, and pricing per sharing type
- Unlock operator contact details to connect directly
- Save and compare shortlisted PGs

### For PG Operators
- List one or multiple properties with full details
- Manage bed availability per sharing type (1-share, 2-share, 3-share, 4-share)
- Receive and track tenant enquiries
- Get notified when a tenant unlocks contact

### For Building Owners
- List buildings available for lease to PG operators
- Specify floor count, room count, locality, expected rent
- Receive expressions of interest from operators

---

## Sharing Types Supported

- 1-Share (single occupancy)
- 2-Share
- 3-Share
- 4-Share
- 5-Share
- Dormitory (open beds)

---

## Cities at Launch

- Bangalore
- Hyderabad
- Pune

---

## Business Model

**Free to list. Pay to connect.**

- PG operators list properties for free
- Tenants pay a small platform fee (₹99–199) to unlock operator contact details
- Building owners list for free; operators pay to express interest
- No rent transactions on platform (avoids GST complexity at this stage)

This model is proven — NoBroker and 99acres use similar lead-unlock mechanics.

---

## Tech Stack (evolves with scale)

| Stage | Stack |
|---|---|
| Stage 0 — 0 customers | Python, Flask, SQLite, systemd, Git |
| Stage 1 — 10 customers | Postgres, Nginx, GitHub Actions, TLS, Backups |
| Stage 2 — 100 customers | Redis, Celery, Prometheus, Grafana |
| Stage 3 — 1000 customers | Docker, CI pipelines, structured logging |
| Stage 4 — 10,000 customers | Kubernetes, HPA, managed DB |
| Stage 5 — 100,000 customers | Platform engineering, multi-region, CDN |

The project intentionally starts with zero infrastructure complexity and grows
only when the problem demands it — mirroring how real startups evolve.

---

## Repository Structure

```
nestfinder/
├── app/
│   ├── api/          # Route handlers
│   ├── models/       # Database models
│   ├── services/     # Business logic
│   └── templates/    # Jinja2 HTML templates
├── db/               # Migrations and seed data
├── docs/             # Architecture decisions, runbooks
├── scripts/          # Ops and utility scripts
├── tests/            # Unit and integration tests
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Running Locally (Stage 0)

```bash
git clone https://github.com/charan-happy/Devops-project.git nestfinder
cd nestfinder
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app/main.py
```

Health check:

```bash
curl localhost:5000/health
# {"status": "ok", "service": "nestfinder", "version": "0.1.0"}
```

---

## Engineering Goals

This project is designed to simulate the full lifecycle of a real SaaS startup:

- Production incidents and postmortems
- Zero-downtime deployments
- Database migrations under load
- Security audits and secret rotation
- Cost optimization under growth
- SLO/SLI definition and error budgets
- DR drills and backup validation

The goal is not feature completion. The goal is engineering depth.

---

## Roadmap

- [ ] Stage 0: Working monolith with auth, listings, search
- [ ] Stage 1: Production VM, Nginx, HTTPS, GitHub Actions CI
- [ ] Stage 2: Redis caching, async notifications, observability
- [ ] Stage 3: Containerization, structured logging, staging environment
- [ ] Stage 4: Kubernetes, autoscaling, managed Postgres
- [ ] Stage 5: Multi-region, CDN, platform engineering layer

---

## License

Private. All rights reserved.
