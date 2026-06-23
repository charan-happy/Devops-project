# NestFinder Architecture

## Stage 0 — Single server, monolith

NestFinder starts as a single Flask application backed by SQLite.
There is no deployment pipeline, no containerization, and no external
services. Everything runs on one machine.

### Components

- Flask app (Python 3.11)
- SQLite (local development) → Postgres (production, Stage 1)
- Systemd service (Stage 1)
- Nginx reverse proxy (Stage 1)

### Roles

1. Tenant — searches PGs by city, gender type, share type, budget
2. PG Operator — lists properties, manages bed availability
3. Building Owner — lists buildings available to lease for PG operation

### Business model

Free to list. Tenants pay a small fee to unlock operator contact details.
No rent transactions on platform (avoids GST complexity at this stage).
