# Automated Marketing Funnel Analyzer (Production-ready)

This repository contains a production-ready version of the Automated Marketing Funnel Analyzer.
It includes:

- FastAPI backend with Postgres (SQLAlchemy + Alembic-ready structure)
- CSV/event ingestion endpoints
- Funnel computation and drop-off detection
- ML suggestions using scikit-learn (DecisionTree) for interpretable feature importances
- React frontend (Vite) with Recharts for visualization
- Dockerfiles and docker-compose for local production-like setup
- .env.example and deployment notes

## Quick start (development with Docker Compose)

1. Copy `.env.example` to `.env` and edit secrets if desired.
2. Build and run:
   ```bash
   docker-compose up --build
   ```
3. Backend: http://localhost:8000
   Frontend: http://localhost:3000

## Notes
- For production, use managed Postgres (RDS/CloudSQL) and configure secrets securely.
- Run Alembic migrations (an Alembic environment is scaffolded; run migration commands in the backend container).
