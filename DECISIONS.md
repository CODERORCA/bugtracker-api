# Bugtracker API – Architektur- & Designentscheidungen

## 1. Projektstruktur
- Layered Architecture: API / Application / Domain / Infrastructure
- Keine Businesslogik in Routern
- Service Layer für zentrale Logik

## 2. Technologieentscheidungen
- FastAPI als Framework
- PostgreSQL als Datenbank
- Docker & docker-compose für Containerisierung
- JWT für Authentifizierung

## 3. Scope-Definition
- Kernziel: Bugtracker-API für Portfolio / Referenz
- Nicht-Ziel: Frontend, Plugins, Jira-Klon

## 4. Qualitätsstandards
- Clean Code & SOLID
- Typisierung in Python
- Testabdeckung >70%
- CI/CD von Anfang an

## 5. Weitere Entscheidungen
- OpenAPI für API-Dokumentation
- ADR-Dokumentation für Architekturänderungen
- Fokus auf produktionsnahe Features
