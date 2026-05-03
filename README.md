# 🏥 ChainCare - Web3 Electronic Medical Record (EMR)

ChainCare is an Electronic Medical Record (EMR) platform built on a modern microservices architecture, integrating Web3 technology to ensure patient data security. The project prioritizes data privacy through database-level encryption and wallet-based identity.

## ✨ Key Features

- **🔐 Web3 Identity:** Patient authentication and identification via Wallet Address.
- **🛡️ Data Encryption:** Sensitive information is stored in an encrypted format.
- **🧩 Microservices Architecture:** Decoupled services (Core Service & API Gateway) for high scalability.
- **⚡ gRPC Communication:** Efficient inter-service data exchange using Protocol Buffers.

## 🏗️ System Architecture

The project utilizes external REST APIs for client requests and internal gRPC for service-to-service communication.

- **💻 Client:** Next.js
- **🚪 API Gateway:** REST to gRPC translation layer.
- **⚙️ Core Service:** Golang-based service handling business logic and database transactions.
- **🗄️ Database:** PostgreSQL with GORM.

## 🛠️ Tech Stack

| Component | Technology |
| --- | --- |
| **Language** | Golang |
| **Transport Layer** | gRPC, Protocol Buffers v3 |
| **Database ORM** | GORM (PostgreSQL Driver) |
| **Containerization** | Docker, Docker Compose |
| **Live Reload** | Air |
| **Frontend** | Next.js, TypeScript |

## 📂 Repository Structure
```text
.
├── backend/
│   ├── pkg/             
│   ├── proto/           
│   └── services/
│       └── core-service/
├── client/              
├── docker-compose.yml   
└── .env