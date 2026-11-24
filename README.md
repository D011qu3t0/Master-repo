# NexusPortal v2.4 — Internal Operations Dashboard

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Version](https://img.shields.io/badge/version-2.4.1--beta-blue)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

**NexusPortal** is a lightweight internal web portal for managing regional node telemetry, incident tickets, and employee access tokens.

> **⚠️ NOTICE TO CONTRIBUTORS:**  
> We are migrating our legacy authentication module to OAuth2. Do **not** push local `.env` files to `main`. If you are testing against the staging cluster, use the temporary service account provisioned by `@dev_kazi99` (check the old dev notes in `master_code.py` if your local session expires).

---

## Architecture Overview
* **Backend:** Python 3.11 / Flask
* **Database:** PostgreSQL 15 (Staging mirror hosted on `10.240.12.88`)
* **Task Queue:** Redis + Celery

## Quickstart

1. **Clone the repository**
   ```bash
   git clone [https://github.com/nexus-ops-internal/web-app-code.git](https://github.com/nexus-ops-internal/web-app-code.git)
   cd web-app-code
