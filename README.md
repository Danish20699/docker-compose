# 🐳 Docker Compose: Multi-Container Orchestration Labs

[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Docker Compose](https://img.shields.io/badge/Docker_Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://docs.docker.com/compose/)
[![YAML](https://img.shields.io/badge/YAML-CB171E?style=for-the-badge&logo=yaml&logoColor=white)](https://yaml.org/)
[![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)](https://www.linux.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![GitHub Actions](https://img.shields.io/badge/CI/CD-GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)](https://github.com/features/actions)

A structured, hands-on DevOps repository mastering **Docker Compose** multi-container orchestration. This repository transitions from individual, manual container operations into declarative Infrastructure-as-Code (IaC) microservice stacks managed through a single YAML blueprint.

---

## 🏗️ Docker Compose Architecture

```text
                    [ docker-compose.yml ]
                              │
               docker compose up -d (Engine)
                              │
         ┌────────────────────┴────────────────────┐
         ▼                                         ▼
┌──────────────────┐                     ┌──────────────────┐
│  Service: web    │                     │  Service: db     │
│  (Frontend/API)  │                     │  (PostgreSQL)    │
│  Port: 8080:80   │                     │  Port: 5432      │
└────────┬─────────┘                     └────────┬─────────┘
         │                                        │
         └──────────┐              ┌──────────────┘
                    ▼              ▼
┌───────────────────────────────────────────────────────────┐
│        Automated Project Bridge Network (DNS)             │
│        Service discovery via container hostname           │
└───────────────────────────────────────────────────────────┘
                    │              │
         ┌──────────┘              └──────────────┐
         ▼                                        ▼
┌──────────────────┐                     ┌──────────────────┐
│ Host Bind Mounts │                     │ Named Volumes    │
│ (Source Code)    │                     │ (DB Persistence) │
└──────────────────┘                     └──────────────────┘
```

---

## 🧠 Why Docker Compose?

| Without Docker Compose | With Docker Compose |
| :--- | :--- |
| Run 5+ complex `docker run` commands with dozens of flags | Write one `docker-compose.yml` and run `docker compose up -d` |
| Manually create networks and volumes | Networks and volumes are auto-created from the YAML spec |
| No dependency ordering — web app crashes if DB isn't ready | `depends_on` ensures correct startup sequence |
| Cannot share setup with teammates easily | Commit one file to Git — anyone can replicate the entire stack |
| Cleanup requires stopping and removing each container individually | `docker compose down` tears down everything in one command |

---

## 📚 Curriculum & Lab Progress

| Lab | Title & Topic | Key Concepts Practiced | Status |
| :---: | :--- | :--- | :---: |
| **Lab 64** | [Docker Compose Introduction](64-docker-compose-intro.md) | YAML structure, service definitions, `up -d`, `down`, multi-container networking | ✅ Completed |

---

## 🗂️ Repository Structure

```text
docker-compose/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md           # Structured bug report template
│   │   └── feature_request.md      # Feature request template
│   └── workflows/
│       └── ci.yml                  # GitHub Actions CI pipeline
├── assets/                         # Terminal & browser verification screenshots
├── 64-docker-compose-intro.md      # Lab 64 documentation
├── .gitignore                      # Ignore secrets, logs, OS files
├── CODE_OF_CONDUCT.md              # Contributor Covenant v2.1
├── CONTRIBUTING.md                 # Contribution guidelines & PR workflow
├── LICENSE                         # MIT License
└── README.md                       # This file
```

---

## ⚡ Essential Docker Compose CLI Reference

| Command | Purpose |
| :--- | :--- |
| `docker compose up -d` | Build, create, and start all services in detached background mode |
| `docker compose down` | Stop and remove all containers, networks, and resources |
| `docker compose down -v` | Stop containers, remove networks, and delete all associated volumes |
| `docker compose ps` | List current running status and port bindings of all services |
| `docker compose logs -f` | Follow live, color-coded aggregated logs across all services |
| `docker compose restart` | Restart all services defined in the compose file |
| `docker compose build` | Rebuild images for services configured with `build:` |
| `docker compose exec <svc> <cmd>` | Execute a command inside a specific running service container |

---

## 🔧 Quick Start

```bash
# Clone the repository
git clone https://github.com/Danish20699/docker-compose.git
cd docker-compose

# Launch a multi-service stack
docker compose up -d

# Verify running services
docker compose ps

# View aggregated logs
docker compose logs -f

# Tear down everything
docker compose down
```

---

## 👤 Author

- **Engineer**: **Danish Nazir**
- **Track**: MLOps & DevOps Engineering
- **GitHub**: [@Danish20699](https://github.com/Danish20699)
- **LinkedIn**: [Danish Nazir](https://www.linkedin.com/in/danish-nazir-6359a624a/)

