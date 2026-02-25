## Scope Definition

Dieses Projekt verfolgt einen klar abgegrenzten Funktionsumfang. Ziel ist es, eine stabile, wartbare und erweiterbare Backend-API mit produktionsnaher Struktur zu entwickeln. Der Scope ist bewusst begrenzt, um Qualität, Architektur und Wartbarkeit in den Mittelpunkt zu stellen.

---

### In Scope (MVP – Minimum Viable Product)

Der initiale Funktionsumfang umfasst:

#### 1. Benutzer- & Authentifizierungssystem
- Benutzerregistrierung
- Login mit JWT-basierter Authentifizierung
- Passwort-Hashing
- Rollenmodell (z. B. Admin, Member)
- Rollenbasierte Zugriffskontrolle

#### 2. Projektverwaltung
- Projekte erstellen, bearbeiten und löschen
- Benutzer Projekten zuweisen
- Projektbezogene Ticketverwaltung

#### 3. Ticketverwaltung
- Tickets erstellen, bearbeiten und löschen
- Statusverwaltung (Open, In Progress, Done)
- Priorisierung
- Zuordnung zu Benutzern
- Basis-Filter und Pagination

#### 4. Technische Anforderungen
- Layered Architecture
- Trennung von Business-Logik und Infrastruktur
- PostgreSQL als Datenbank
- Containerisierung mit Docker
- Unit-Tests für Kernlogik
- CI/CD-Grundstruktur

---

### Out of Scope (bewusst ausgeschlossen)

Folgende Features sind explizit nicht Bestandteil des MVP:

- Frontend-Anwendung
- Echtzeit-Funktionalität (z. B. WebSockets)
- Microservice-Architektur
- Multi-Tenant-Architektur
- OAuth-Integration (Google, GitHub etc.)
- Komplexes Benachrichtigungssystem
- Mobile-App
- Mandantenfähigkeit
- Enterprise-Features wie Audit-Logging auf Enterprise-Niveau

Diese Abgrenzung dient der Fokussierung auf Architekturqualität und Kernfunktionalität.

---

### Nicht-funktionale Anforderungen

Das Projekt verfolgt folgende Qualitätsziele:

- Testbare Business-Logik
- Dokumentierte Architekturentscheidungen
- Saubere Code-Struktur und klare Verantwortlichkeiten
- Erweiterbarkeit ohne strukturelle Umbrüche
- Reproduzierbare Entwicklungsumgebung
- Deployment-fähige Containerstruktur

---

### Scope-Prinzip

Neue Features werden erst nach vollständiger Stabilisierung des MVP bewertet und priorisiert. Architektur und Wartbarkeit haben Vorrang vor Feature-Expansion.
