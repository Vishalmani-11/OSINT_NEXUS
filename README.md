# 🔎 OSINT Nexus

A modern, open-source **OSINT (Open Source Intelligence) Investigation Platform** designed to help analysts organize investigations, manage entities, visualize relationships, and streamline intelligence workflows.

Built with a modern microservice architecture, OSINT Nexus combines a React frontend, FastAPI backend, PostgreSQL, Redis, Neo4j, Celery, and Docker to provide a complete self-hosted investigation platform.

---

## ✨ Features

* 🔍 Investigation & Case Management
* 👥 Entity Management
* 🌐 Relationship Graph Visualization (Neo4j)
* ⚡ FastAPI REST API
* 📊 Interactive API Documentation
* 📨 Background Task Processing (Celery + Redis)
* 🗄 PostgreSQL Database
* 🐳 Fully Dockerized Deployment
* 🔐 Authentication & Role-Based Access
* 🚀 Modern React User Interface

---

# 🏗 Tech Stack

| Component        | Technology              |
| ---------------- | ----------------------- |
| Frontend         | React                   |
| Backend          | FastAPI                 |
| Database         | PostgreSQL              |
| Graph Database   | Neo4j                   |
| Cache / Queue    | Redis                   |
| Background Jobs  | Celery                  |
| Reverse Proxy    | Nginx                   |
| Containerization | Docker & Docker Compose |

---

# 📦 Prerequisites

Before running the project, install:

* Docker
* Docker Compose
* Git
* Make (Optional)

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/<your-username>/osint-nexus.git
cd osint-nexus
```

Start the platform

```bash
make up
```

or

```bash
docker compose up -d
```

---

# 🌐 Access the Application

| Service      | URL                                 |
| ------------ | ----------------------------------- |
| Frontend     | http://localhost:3000               |
| Register     | http://localhost:3000/register      |
| API Docs     | http://localhost:8000/api/v1/docs   |
| Health Check | http://localhost:8000/api/v1/health |
| Neo4j        | http://localhost:7474               |

> **Note:** The **first registered user automatically becomes the Administrator**.

---

# 📂 Useful Commands

### Start

```bash
make up
```

### View Logs

```bash
make logs
```

### Load Demo Data

```bash
make seed
```

### Stop

```bash
make down
```

### Restart

```bash
make down
make up
```

---

# 📸 Screenshots

Add screenshots here.

Example:

```
docs/dashboard.png

docs/investigation.png

docs/api-docs.png

docs/neo4j.png
```

---

# 📖 API Documentation

FastAPI automatically generates interactive documentation.

Swagger UI:

```
http://localhost:8000/api/v1/docs
```

---

# 🗂 Project Architecture

```
                React Frontend
                      │
                      ▼
                 Nginx Gateway
                      │
                      ▼
                 FastAPI Backend
             ┌────────┴─────────┐
             │                  │
             ▼                  ▼
      PostgreSQL           Redis Queue
                                │
                                ▼
                           Celery Workers
                                │
                                ▼
                           Neo4j Database
```

---

# 📁 Project Structure

```
.
├── backend/
├── frontend/
├── docker/
├── nginx/
├── alembic/
├── docs/
├── docker-compose.yml
├── Makefile
└── README.md
```

---

# 🛠 Development

To rebuild the containers after making changes:

```bash
docker compose up --build
```

To monitor running services:

```bash
docker ps
```

To inspect logs:

```bash
docker compose logs -f
```

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new feature branch
3. Commit your changes
4. Open a Pull Request

---

# 📜 License

This project is open source and is distributed under its respective license. Refer to the repository's `LICENSE` file for details.

---

# ⭐ Support

If you found this project useful:

* ⭐ Star the repository
* 🍴 Fork it
* 🛠 Contribute improvements
* 🐞 Report issues
* 💡 Suggest new features

Happy Investigating! 🚀
