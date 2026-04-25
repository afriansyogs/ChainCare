# ChainCare - Web3 Electronic Medical Record (EMR)

ChainCare adalah platform pengelolaan rekam medis elektronik (EMR) yang dirancang dengan arsitektur microservices modern dan mengintegrasikan teknologi Web3 untuk keamanan data pasien. Proyek ini memprioritaskan privasi data melalui enkripsi dan identitas berbasis dompet digital (Wallet Address).

## Gambaran Proyek

Tujuan utama ChainCare adalah memecahkan masalah fragmentasi data medis. Dengan menggunakan ChainCare, data pasien tidak hanya tersimpan di satu rumah sakit, tetapi terhubung secara aman menggunakan identitas blockchain, sementara data sensitif tetap terenkripsi di sisi server.

### Fitur Utama
- **Identitas Web3:** Login dan identifikasi pasien menggunakan Wallet Address.
- **Data Terenkripsi:** Informasi sensitif seperti NIK dan Nama disimpan dalam bentuk terenkripsi.
- **Arsitektur Microservices:** Pemisahan layanan (Core Service & API Gateway) untuk skalabilitas tinggi.
- **Komunikasi gRPC:** Pertukaran data antar-layanan menggunakan Protocol Buffers (Protobuf) yang jauh lebih cepat dibanding REST JSON konvensional.

## Arsitektur Sistem

Proyek ini menggunakan pola komunikasi internal gRPC dan eksternal REST API.

- **Client:** Next.js (React Framework) untuk antarmuka pengguna.
- **API Gateway:** Entry point yang mengubah request REST dari frontend menjadi panggilan gRPC internal.
- **Core Service:** Layanan utama berbasis Golang yang menangani logika bisnis dan interaksi database PostgreSQL.
- **Database:** PostgreSQL dengan integrasi GORM untuk manajemen skema otomatis.

## Teknologi yang Digunakan

| Komponen | Teknologi |
| --- | --- |
| **Language** | Golang |
| **Transport Layer** | gRPC, Protocol Buffers v3 |
| **Database ORM** | GORM (PostgreSQL Driver) |
| **Containerization** | Docker, Docker Compose |
| **Live Reload (Dev)** | Air (Golang Hot Reload) |
| **Frontend** | Next.js, TypeScript |

## Struktur Folder

```
.
├── backend/
│   ├── pkg/             # Kode yang bisa digunakan berulang (shared library)
│   ├── proto/           # Definisi kontrak gRPC (.proto files)
│   └── services/
│       └── core-service/# Layanan pusat data pasien
├── client/              # Frontend Next.js
├── docker-compose.yml   # Orchestrasi container
└── .env                 # Konfigurasi environment (tidak masuk git)