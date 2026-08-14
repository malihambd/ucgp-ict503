# UCGP — Unified Cybersecurity and Cloud Governance Platform

A multi-tenant platform that gives NSW IT Support technicians and their SME clients a single dashboard for security alerts, compliance scoring (Essential Eight / ISO 27001), and cloud resource oversight — instead of switching between multiple disconnected tools.

Built as the ICT503 Applied IT Project B submission, continuing from the ICT502 Applied IT Project A proposal.

## 🚦 Project Status

**Design phase complete — development starting Sprint 1.**

- ✅ Systems Design Documentation (Assessment 1) complete
- ✅ Functional & non-functional requirements defined
- ✅ Architecture designed (block diagram, ER diagram, sequence diagram)
- ✅ Benchmarked against 4 competitor products
- 🔄 Environment setup in progress
- ⬜ Development not yet started

## 📋 What It Does

- Ingests security events from Azure Sentinel, Defender for Cloud, and Microsoft Graph
- Scores events for risk using Azure Machine Learning
- Tracks Essential Eight and ISO/IEC 27001 compliance maturity per client
- Manages the full incident lifecycle (create → assign → triage → close)
- Provides two dashboards: one for technicians (multi-client view), one for each SME client (their own data only)
- Exports compliance/incident reports as PDF/CSV

## 🏗️ Architecture

Five-layer design: Presentation → API Gateway → Microservices → Data Layer → Integration Layer.
Full diagrams and explanation: [`/diagrams`](./diagrams) and [`/docs`](./docs)

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 18 + TypeScript |
| Backend | .NET 8 (C#) |
| Database | Azure SQL (transactional) + Cosmos DB (event telemetry) |
| Auth | Azure AD / Entra ID |
| Hosting | Azure (free-tier services) |

## 📁 Repository Structure

frontend/              → React dashboard (MSP console + tenant view)
backend/
├── AlertingService/     → Event scoring & alert generation
├── ComplianceService/   → Essential Eight / ISO 27001 scoring
├── IncidentService/     → Incident lifecycle management
└── ReportingService/    → PDF/CSV report generation
docs/                   → Design documentation
diagrams/               → Architecture diagrams

## 📄 Documentation

Full systems design documentation: [`/docs`](./docs)

## 👤 Author

Maliha Mohammadi
ICT503 Applied IT Project B — Individual Submission

## 📚 Context

This project continues from **ICT502 Applied IT Project A**, where research into NSW IT Support identified the need for a unified security/compliance/cloud governance platform for SME clients.
