# Bugtracker API – Quality Standards
The project is developed according to clearly defined standards:

- Separation of business logic and infrastructure
- Documented architectural decisions
- Test coverage as quality indicator
- Reproducible development process
- Containerized deployment

## 1. Code Quality
- Enforce linting & formatter
- Activate pre-commit hooks
- Follow conventional commit guidelines

## 2. Testing
- Unit tests for business logic
- Integration tests for endpoints
- Test coverage >70%

## 3. Security
- JWT & token rotation
- Roles & permissions checks
- Rate limiting & brute-force protection
- Input validation & CORS handling

## 4. Deployment & Operations
- Containerization (Docker)
- CI/CD pipeline for build and test
- Logging & health checks

## 5. Documentation
- API documentation via OpenAPI
- Versioned architectural decisions
- Keep roadmap & feature list up to date
