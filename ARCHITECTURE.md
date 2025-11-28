# Architecture & Technical Standards

> **Status:** Living Document
> **Owner:** Engineering Lead Agent
> **Last Updated:** [Date]

## 1. Technology Stack (The "Hard Constraints")
*Defines the exact tools available. Engineering Lead must strictly adhere to this.*
- **Language/Runtime:** [e.g., C# .NET 8, Node.js 20, Python 3.11]
- **Frameworks:** [e.g., ASP.NET Core, Express, FastAPI]
- **Database:** [e.g., PostgreSQL, MongoDB, SQL Server]
- **Messaging/Async:** [e.g., MassTransit, RabbitMQ, Kafka]
- **Containerization:** [e.g., Docker, Kubernetes]

## 2. System Map (High-Level)
*Maps logical layers to physical source folders. Engineering Lead must maintain this map.*
- `src/API`: [e.g., Public REST Controllers, Middleware]
- `src/Core`: [e.g., Domain Entities, Value Objects, Interfaces]
- `src/Infrastructure`: [e.g., EF Core DbContext, External Service Clients]
- `src/Features`: [e.g., Vertical Slices containing Handlers and Validators]
- `src/Shared`: [e.g., Common utilities, logging, auth]

## 3. Engineering Standards
*Rules for implementation.*
- **Testing Strategy:** [e.g., Unit tests in `tests/Unit`, Integration in `tests/Integration`]
- **Error Handling:** [e.g., Use Result pattern, Global Exception Handler]
- **Logging:** [e.g., Serilog, structured logging required]
- **Code Style:** [e.g., Follow .editorconfig, ESLint rules]
- **Documentation:** [e.g., OpenAPI/Swagger required for all endpoints]
