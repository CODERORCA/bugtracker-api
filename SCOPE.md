# Scope Definition

This project has a clearly defined scope. The goal is to develop a stable, maintainable, and extensible backend API with a production-oriented structure.
The scope is deliberately limited to prioritize quality, architecture, and maintainability.

---

## In Scope (MVP – Minimum Viable Product)

The initial feature set includes:

### 1. User & Authentication System
- User registration
- JWT-based login authentication
- Password hashing
- Role model (e.g., Admin, Member)
- Role-based access control

### 2. Project Management
- Create, edit, and delete projects
- Assign users to projects
- Project-related ticket management

### 3. Ticket Management
- Create, edit, and delete tickets
- Status management (Open, In Progress, Done)
- Prioritization
- Assign tickets to users
- Basic filtering and pagination

### 4. Technical Requirements
- Layered Architecture
- Separation of business logic and infrastructure
- PostgreSQL database
- Docker containerization
- Unit tests for core logic
- Basic CI/CD pipeline

---

## Out of Scope (Explicitly Excluded)

The following features are **not part of the MVP**:

- Frontend application
- Real-time functionality (e.g., WebSockets)
- Microservice architecture
- Multi-tenant architecture
- OAuth integration (Google, GitHub, etc.)
- Complex notification system
- Mobile app
- Tenant capability
- Enterprise features (e.g., enterprise-level audit logging)

This ensures focus on architecture quality and core functionality.

---

## Non-Functional Requirements

The project targets the following quality goals:

- Testable business logic
- Documented architectural decisions
- Clean code structure and clear responsibilities
- Extensibility without structural overhaul
- Reproducible development environment
- Deployment-ready container setup

---

## Scope Principle

New features will be evaluated and prioritized **only after full stabilization of the MVP**.
Architecture and maintainability take precedence over feature expansion.

## Planned Extensions (Post-MVP)
- Comment system
- Soft delete
- Performance optimization
- Caching
- Monitoring & logging
- Advanced filter and search capabilities
