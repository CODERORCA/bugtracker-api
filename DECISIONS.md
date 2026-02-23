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

### In-Scope (MVP):
- Benutzerregistrierung
- Login mit JWT
- Rollen (z. B. Admin, Member)
- Projekte anlegen / bearbeiten
- Tickets erstellen / bearbeiten
- Statusverwaltung
- Basis-Filter + Pagination

### Out-of-Scope
- Kein Frontend
- Keine Echtzeit-Funktionen (WebSockets)
- Keine Multi-Tenant-Architektur
- Kein Microservice-Setup
- Keine OAuth-Provider (Google etc.)
- Keine Mobile-App
- Kein komplexes Notification-System

## 4. Qualitätsstandards
- Clean Code & SOLID
- Typisierung in Python
- Testabdeckung >70%
- CI/CD von Anfang an

## 5. Weitere Entscheidungen
- OpenAPI für API-Dokumentation
- ADR-Dokumentation für Architekturänderungen
- Fokus auf produktionsnahe Features
