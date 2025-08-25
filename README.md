# Spring Boot API

A production‑ready REST API built with **Spring Boot**, featuring **JWT authentication**, **PostgreSQL**, **external API integrations**, and a **Dockerized environment**.  
Includes observability via Micrometer + Prometheus/Grafana and full test coverage with **Testcontainers**.

---

## 🚀 Tech Stack

- **Backend Framework**: Spring Boot 3.x
- **Language**: Java 21
- **Build Tool**: Maven (or Gradle)
- **Database**: PostgreSQL
- **Caching / Tokens**: Redis
- **Auth**: JWT (roles, claims, refresh tokens)
- **Testing**: JUnit 5 + Testcontainers (PostgreSQL, Redis)
- **Docs**: Springdoc OpenAPI / Swagger UI
- **Observability**: Micrometer, Prometheus, Grafana (Dockerized)
- **Containerization**: Docker / Docker Compose

---

## 📂 Project Structure

```
spring-boot-api/
├─ src/
│  ├─ main/
│  │  ├─ java/com/tonisilvan/api/   # Source code
│  │  ├─ resources/                 # application.yml, configs
│  └─ test/                         # Unit & integration tests
├─ docker-compose.yml               # DB + Redis + Monitoring
├─ pom.xml / build.gradle           # Dependencies & build
└─ README.md
```

---

## 🔐 Features

- JWT‑based authentication (access + refresh tokens)
- Role‑based authorization
- CRUD endpoints with validation
- PostgreSQL persistence with JPA/Hibernate
- Redis caching & token blacklisting
- External API integration (example: GitHub REST API / OpenAI / Stripe)
- Health checks (`/actuator/health`)
- Metrics (`/actuator/prometheus`)
- Swagger UI docs at `/swagger-ui.html`
- Docker Compose for full local environment

---

## 🧪 Testing

- **Unit tests** with JUnit 5 & Mockito
- **Integration tests** with Testcontainers (Postgres, Redis)
- Coverage report via JaCoCo

Run tests:
```bash
mvn test
```

---

## ⚙️ Getting Started

### Prerequisites
- Java 21+
- Maven 3.9+ (or Gradle)
- Docker & Docker Compose

### Clone and build
```bash
git clone https://github.com/tonisilvan/spring-boot-api.git
cd spring-boot-api
mvn clean install
```

### Run locally
```bash
mvn spring-boot:run
# API available at http://localhost:8080
```

### Run with Docker Compose
```bash
docker-compose up --build
# API → http://localhost:8080
# Swagger → http://localhost:8080/swagger-ui.html
# Prometheus → http://localhost:9090
# Grafana → http://localhost:3000
```

---

## 🔗 Example Endpoints

- `POST /auth/login` → authenticate user, returns JWT
- `GET /users/me` → get current user profile
- `GET /external/github/{user}` → fetch GitHub data (demo external API)
- `GET /metrics` → Prometheus metrics

---

## 📜 Roadmap

- [ ] Add GraphQL endpoint
- [ ] Add CI/CD pipeline (GitHub Actions → Docker Hub)
- [ ] Add Kubernetes manifests (Helm chart)
- [ ] Improve observability (distributed tracing with OpenTelemetry)

---

## 📄 License

MIT © Toni Silván
