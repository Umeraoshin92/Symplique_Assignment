# Azure Cosmos DB Billing Record Optimization (Serverless Archival)

This project implements a cost-effective, serverless architecture to optimize storage costs in a read-heavy Azure Cosmos DB billing system by archiving records older than 90 days to Azure Blob Storage.

## ✅ Features
- Seamless migration of old billing records to cold storage
- Zero downtime & no changes to existing API contracts
- Transparent read fallback from Blob if data is archived
- Cost-optimized with tiered storage (Cosmos DB + Blob)
- Easy to maintain and deploy via Azure Functions

## 📦 Components
- `archive_function.py` – Moves old billing records to Azure Blob
- `read_proxy_function.py` – Retrieves data from Cosmos DB or Blob
- `architecture.png` – High-level diagram
- `requirements.txt` – Required Python packages

## 📁 Folder Structure
azure-cost-optimization/
├── README.md
├── diagrams/
│ └── architecture.png
├── functions/
│ ├── archive_function.py
│ └── read_proxy_function.py
├── requirements.txt
└── .gitignore
