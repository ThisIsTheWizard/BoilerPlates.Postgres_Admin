# BoilerPlates.Postgres_Admin

A boilerplate setup for running **PostgreSQL** with **pgAdmin** using Docker Compose.
This repository provides an easy way to spin up a PostgreSQL database along with a web-based admin interface for managing your databases.

---

## 🚀 Features

- PostgreSQL database in a Docker container
- pgAdmin 4 for database administration
- Persistent storage with Docker volumes
- Simple configuration via environment variables

---

## 📂 Project Structure

```
BoilerPlates.Postgres_Admin/
│── docker-compose.yml
│── .env
│── README.md
```

---

## ⚙️ Setup

### 1. Clone the repository

```bash
git clone https://github.com/ThisIsTheWizard/BoilerPlates.Postgres_Admin.git
cd BoilerPlates.Postgres_Admin
```

### 2. Configure environment variables

Edit the `.env` file (sample provided) to set database credentials:

```env
# -------------------------
# PostgresDB Settings
# -------------------------
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
POSTGRES_DB=postgres

# -------------------------
# Postgres Admin Settings
# -------------------------
PGADMIN_DEFAULT_EMAIL=postgres@postgres.com
PGADMIN_DEFAULT_PASSWORD=postgres
```

### 3. Start services

```bash
docker-compose up -d
```

---

## 🌐 Access

- **PostgreSQL** → `localhost:5432`
- **pgAdmin** → [http://localhost:8080(http://localhost:8080)

  - Login with the credentials from `.env`

---

## 📖 Usage

1. Open pgAdmin in your browser.
2. Add a new server with the following details:

   - **Host:** `postgres` (service name in Docker Compose)
   - **Port:** `5432`
   - **User & Password:** values from `.env`

---

## 🛠️ Commands

- Start containers:

  ```bash
  docker-compose up -d
  ```

- Stop containers:

  ```bash
  docker-compose down
  ```

- View logs:

  ```bash
  docker-compose logs -f
  ```

---

## 📦 Volumes

Data is persisted via Docker volumes:

- `postgres_data` → Stores PostgreSQL database files
- `pgadmin_data` → Stores pgAdmin configuration

---

## 📝 License

This boilerplate is provided under the MIT License.
Feel free to use and modify it for your projects.
