# Architekturübersicht

## Architekturansatz

Die Bugtracker API folgt einer Schichtenarchitektur (Layered Architecture) mit klarer Trennung von Verantwortlichkeiten.
Ziel ist eine wartbare, testbare und erweiterbare Systemstruktur mit klar definierten Abhängigkeiten.

Die Abhängigkeiten verlaufen strikt in eine Richtung:

API → Services → Repositories → Datenbank

Keine untere Schicht darf von einer darüberliegenden abhängig sein.

---

## Architekturebenen

### 1. Präsentationsschicht (API)

Verantwortlich für:
- HTTP-Endpunkte
- Request- und Response-Modelle
- Eingabevalidierung
- Statuscode-Verarbeitung

Diese Schicht enthält keine Geschäftslogik.

---

### 2. Applikations- / Service-Schicht

Verantwortlich für:
- Geschäftslogik
- Orchestrierung der Repositories
- Berechtigungsprüfungen
- Transaktionssteuerung

Hier befindet sich das zentrale Verhalten der Anwendung.

Services dürfen keine HTTP-spezifischen Abhängigkeiten besitzen.

---

### 3. Domänenschicht

Verantwortlich für:
- Kernentitäten
- Domänenmodelle
- Fachliche Regeln (falls relevant)

Die Domänenschicht ist framework-unabhängig und bildet den fachlichen Kern des Systems.

---

### 4. Infrastruktur-Schicht

Verantwortlich für:
- Datenbankzugriffe
- ORM-Modelle
- Repository-Implementierungen
- Externe Integrationen

Diese Schicht kapselt technische Implementierungsdetails.

---

## Projektstruktur

Die Projektstruktur ist wie folgt aufgebaut:

bugtracker/
│
├── app/
│   ├── main.py
│   │
│   ├── api/
│   │   ├── v1/
│   │   │   ├── routes/
│   │   │   │   ├── users.py
│   │   │   │   ├── projects.py
│   │   │   │   ├── tickets.py
│   │   │   │   └── auth.py
│   │   │   └── router.py
│   │
│   ├── core/
│   │   ├── config.py
│   │   ├── security.py
│   │   └── dependencies.py
│   │
│   ├── domain/
│   │   ├── models/
│   │   └── schemas/
│   │
│   ├── services/
│   │   ├── user_service.py
│   │   ├── project_service.py
│   │   └── ticket_service.py
│   │
│   ├── repositories/
│   │   ├── user_repository.py
│   │   ├── project_repository.py
│   │   └── ticket_repository.py
│   │
│   └── db/
│       ├── base.py
│       ├── session.py
│       └── models.py
│
├── tests/
│
├── docker/
│
├── alembic/
│
├── requirements.txt
└── README.md

---

## Abhängigkeitsregeln

- Die API-Schicht darf Services verwenden.
- Services dürfen Repositories verwenden.
- Repositories dürfen auf Datenbankmodelle zugreifen.
- Zirkuläre Abhängigkeiten sind nicht erlaubt.
- Geschäftslogik darf nicht in Route-Handlern implementiert werden.
- HTTP-spezifische Logik darf nicht in Services enthalten sein.

---

## Gestaltungsprinzipien

- Klare Trennung von Verantwortlichkeiten
- Eindeutige Zuständigkeiten pro Schicht
- Hohe Testbarkeit
- Geringe Kopplung
- Containerisierte Bereitstellung
- Dokumentation von Architekturentscheidungen

---

## Weiterentwicklungsstrategie

Die Architektur ist so konzipiert, dass:

- Neue Funktionen ohne strukturelle Änderungen ergänzt werden können
- Refactorings möglich sind, ohne externe Schnittstellen zu brechen
- Skalierung und zukünftige Erweiterungen (z. B. Caching oder Monitoring) unterstützt werden

Strukturelle Stabilität hat Vorrang vor schneller Feature-Erweiterung.
