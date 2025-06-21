# 🧪 microservices-lab

A Kotlin + Spring Boot monorepo designed to explore microservice architecture patterns, technologies, and tools in the JVM ecosystem.

This project starts with a `product-service` and includes PostgreSQL via Docker Compose and embedded PostgreSQL for fast integration testing.

---

## 🧱 Project Structure

```

microservices-lab/
├── services/
│   └── product-service/        # Product microservice (Spring Boot + Kotlin)
├── docker/                     # Docker Compose setup for local dev
├── gradle/                     # Gradle wrapper and version catalog
├── build.gradle.kts            # Root Gradle config (version catalog enabled)
├── settings.gradle.kts         # Module and catalog setup

````

---

## 🚀 Getting Started

### 1. Clone the Repo

```bash
git clone https://github.com/JakubHorakCZ/microservices-lab.git
cd microservices-lab
````

### 2. Start PostgreSQL (via Docker)

```bash
docker-compose -f docker/docker-compose.yml up -d
```

This will start PostgreSQL on `localhost:5432` using:

* **DB name**: `productdb`
* **User**: `user`
* **Password**: `password`

### 3. Run the Product Service

```bash
./gradlew :services:product-service:bootRun
```

The service will start on [http://localhost:8080](http://localhost:8080)

---

## 🧪 Running Tests

This project uses **Zonky Embedded PostgreSQL** for realistic database tests.

```bash
./gradlew test
```

---

## 🧰 Tech Stack

* ✅ Kotlin + Spring Boot
* ✅ Gradle (with Version Catalogs)
* ✅ Docker Compose (PostgreSQL)
* ✅ Embedded PostgreSQL for tests
* ✅ JUnit 5

---

## 📦 Services (Work in Progress)

* `product-service`: Product catalog management (CRUD)

More services (orders, inventory, payments, etc.) coming soon...

---

## 📌 Goals

* Practice microservices architecture patterns
* Apply CQRS, DDD, async messaging, observability, and testing strategies
* Build a reusable Kotlin/Spring Boot template for production-grade services

---

## 📄 License

MIT © Jakub
