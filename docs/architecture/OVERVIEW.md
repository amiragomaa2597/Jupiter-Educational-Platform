# Architecture Overview

## Style

**Modular monolith** with Clean Architecture dependency rules.

- One deployable API
- Multiple feature modules
- Clear dependency direction
- Incremental migration from legacy BL/DAL

## Dependency rules

```text
API → Application
API → Infrastructure (composition / DI)
Infrastructure → Application → Domain
Infrastructure → DAL / BL (transitional only)
Domain → (no outward framework dependencies)
```

## Frontend architecture

- Feature-first folders (`features/{domain}`)
- Domain HTTP services (`Services/{domain}`)
- Shared list toolkit (`app-data-view`)
- Central routing + role/permission guards
- Environment-based API base URL

## Cross-cutting backend concerns

- JWT authentication extension method
- Exception handling middleware
- Activity logging middleware
- Hangfire background jobs
- Integration ports: email, WhatsApp, FCM, SMS (SMS currently no-op adapter)

## Why this matters to employers

Shows ability to:

- Work inside a real layered codebase
- Keep controllers thin
- Separate business contracts from infrastructure providers
- Evolve architecture without a risky big-bang rewrite
