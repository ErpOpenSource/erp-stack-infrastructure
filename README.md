# 🚀 ERP Infrastructure Stack

Infrastructure as Code (IaC) repository for the Open Source ERP ecosystem.
This project manages the core persistence and caching layers with a focus on high availability and observability.

---

## 🛠 Components

### PostgreSQL 16 (Alpine)
Relational database with native support for `uuid-ossp` and `unaccent` extensions.

### Redis 7 (Alpine)
High-performance cache and message queue management with AOF persistence.

### Exporters
Native Prometheus exporters for real-time infrastructure monitoring.

---

## 🚀 Deployment

### 1️⃣ Create the shared network
The stack communicates through a global Docker network.
```bash
docker network create erp-platform
```

### 2️⃣ Configure environment variables
Create your local `.env` file from the template:
```bash
cp .env.example .env
```

### 3️⃣ Spin up the stack
Run the containers in detached mode:
```bash
docker compose up -d
```

---

## 📊 Observability

This stack is fully integrated with the `erp-observability-platform`.

| Source | Details |
|---|---|
| **Logs** | Automatically forwarded to Loki via the Docker `json-file` driver |
| **Database Metrics** | Scraped from `erp_postgres_exporter:9187` |
| **Cache Metrics** | Scraped from `erp_redis_exporter:9121` |

---

## ⚙️ Maintenance Commands

### Access Database
```bash
docker exec -it erp_postgres psql -U erp_admin -d erp_main_db
```

### Check Redis Health
```bash
docker exec -it erp_redis redis-cli -a ${REDIS_PASSWORD} ping
```

### Follow Logs
```bash
docker compose logs -f
```
