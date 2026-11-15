# Fast-API-POSTGRES-SQLALCHEMY-DOCKER

A containerized web application built with **FastAPI**, **PostgreSQL**, and **SQLAlchemy** for managing student records, orchestrated with **Docker Compose**, and bundled with a simple frontend interface[cite: 1, 4, 7].

---

## 🛠️ Project Structure

```text
docker fastapi and postgres/
├── .dockerignore
├── .env
├── .gitignore
├── app.js             # Frontend JavaScript integration
├── docker.yml         # Docker Compose configuration file
├── Dockerfile         # Docker build setup for FastAPI
├── index.html         # Frontend interface
├── main.py            # FastAPI application entry point
├── PLAYGROUND.PY      # Testing & experimentation script
├── requirements.txt   # Python dependencies
├── students.json      # Sample dataset / initial data
└── styles.css         # Styling for the web interface
```[cite: 4, 7]

---

## 🚀 Tech Stack

* **Backend:** [FastAPI](https://fastapi.tiangolo.com/)
* **Database:** [PostgreSQL](https://www.postgresql.org/)[cite: 4]
* **ORM:** [SQLAlchemy](https://www.sqlalchemy.org/)
* **Containerization:** [Docker & Docker Compose](https://www.docker.com/)[cite: 4]
* **Frontend:** HTML, CSS, JavaScript[cite: 7]

---

## ⚡ Quick Start

### Prerequisites
Make sure you have [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed and running.

### Setup & Running

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/persie901/Fast-API-POSTGRES-SQLALCHEMY-DOCKER.git](https://github.com/persie901/Fast-API-POSTGRES-SQLALCHEMY-DOCKER.git)
   cd Fast-API-POSTGRES-SQLALCHEMY-DOCKER
   ```[cite: 5, 6]

2. **Start the application with Docker Compose:**
   ```powershell
   docker compose -f docker.yml up --build
   ```[cite: 3, 4, 7]

3. **Access the application:**
   * **API Base URL:** `http://localhost:8000`[cite: 4]
   * **Interactive API Docs (Swagger):** `http://localhost:8000/docs`

---

## 📊 Database Schema (`student_records`)

The database stores student information with the following attributes[cite: 1, 4]:

| Field | Type | Description |
| :--- | :--- | :--- |
| `id` | String | Unique identifier (e.g., `S001`) |[cite: 1]
| `name` | String | Student's full name |[cite: 1]
| `age` | Integer | Student's age |[cite: 1]
| `course` | String | Enrolled course |[cite: 1]
| `marks` | Integer | Student's marks |[cite: 1]
| `email` | String | Student's email address |[cite: 1]

---

## ⚙️ Environment Configuration

Database configuration set in `docker.yml`[cite: 4, 7]:

* **POSTGRES_USER:** `postgres`[cite: 4]
* **POSTGRES_PASSWORD:** `postgres`[cite: 4]
* **POSTGRES_DB:** `studentdb`[cite: 4]
* **DATABASE_URL:** `postgresql://postgres:postgres@db:5432/studentdb`[cite: 4]
