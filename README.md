# Bugtracker API

## Projektvision

Die Bugtracker API ist ein produktionsnah entwickeltes Backend-System zur strukturierten Verwaltung von Projekten und Tickets.
Ziel ist es, eine klar aufgebaute, erweiterbare und wartbare API bereitzustellen, die typische Anforderungen moderner Softwareteams abbildet.

Im Fokus steht nicht nur die Funktionalität, sondern insbesondere eine saubere Architektur, klare Verantwortlichkeiten im Code sowie ein professioneller Entwicklungsprozess.


## Problemstellung

Viele kleine und mittelgroße Teams verwalten Aufgaben und Fehlerberichte über Tabellen, E-Mails oder überladene Tools.
Dies führt häufig zu:

- Fehlender Transparenz
- Unklaren Zuständigkeiten
- Ineffizienter Priorisierung
- Eingeschränkter Nachvollziehbarkeit von Änderungen

Dieses Projekt adressiert diese Probleme durch eine klar strukturierte, rollenbasierte Backend-API.


## Zielsetzung

Die Anwendung soll:

- Projekte und Tickets strukturiert verwalten
- Benutzer- und Rollenmodelle abbilden
- Rechte sauber kontrollieren
- Erweiterbarkeit ermöglichen
- Testbar und wartbar sein
- Produktionsnahe Standards erfüllen

Der Schwerpunkt liegt auf Backend-Architektur, Sicherheit, Qualitätssicherung und sauberer Strukturierung.


## Technologischer Fokus

- FastAPI
- PostgreSQL
- JWT-Authentifizierung
- Rollen- & Rechteverwaltung
- Layered Architecture
- Unit- und Integrationstests
- CI/CD
- Docker


## MVP (Minimum Viable Product)

Der initiale Funktionsumfang umfasst:

- Benutzerregistrierung und Login
- JWT-basierte Authentifizierung
- Rollen- und Rechteverwaltung
- Projekte erstellen und verwalten
- Tickets erstellen, bearbeiten und priorisieren
- Statusverwaltung (Open, In Progress, Done)
- Basis-Filter und Pagination


## Geplante Erweiterungen (Post-MVP)

- Kommentarsystem
- Soft Delete
- Performance-Optimierung
- Caching
- Monitoring & Logging
- Erweiterte Filter- und Suchfunktionen


## Qualitätsanspruch

Das Projekt wird nach klar definierten Standards entwickelt:

- Trennung von Business-Logik und Infrastruktur
- Dokumentierte Architekturentscheidungen
- Testabdeckung als Qualitätsindikator
- Reproduzierbarer Entwicklungsprozess
- Containerisierte Bereitstellung

## Projektstatus

Derzeit befindet sich das Projekt in der Planungsphase.
Architektur, Scope und Qualitätsziele werden definiert, bevor die Implementierung beginnt.
