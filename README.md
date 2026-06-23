# NestFinder

Find your PG. Fill your beds.

NestFinder is a multi-tenant SaaS platform connecting PG seekers with PG
operators across Bangalore, Hyderabad, and Pune.

## Roles

- **Tenant** — searches and books PG accommodation
- **PG Operator** — lists and manages PG properties and beds
- **Building Owner** — lists buildings available for PG operators to lease

## Run locally

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app/main.py
```

## Health check

```bash
curl localhost:5000/health
```
