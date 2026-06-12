# Full QA Cycle — Urban Scooter

[![Web](https://img.shields.io/badge/Web-Manual%20Testing-2E5FA3?style=flat-square)](.)
[![Mobile](https://img.shields.io/badge/Mobile-Android-43B02A?style=flat-square&logo=android)](.)
[![API](https://img.shields.io/badge/API-Postman-FF6C37?style=flat-square&logo=postman)](.)
[![SQL](https://img.shields.io/badge/SQL-PostgreSQL-336791?style=flat-square&logo=postgresql)](.)
[![Status](https://img.shields.io/badge/Status-Complete-green?style=flat-square)](.)

🇺🇸 [English](#-english) · 🇪🇸 [Español](#-español)

---

## 🇺🇸 English

### The Problem

**Urban Scooter** was an electric scooter rental service — web app, mobile app, API backend, and a SQL database. Each layer could have bugs independently.

The web form might accept an invalid date. The mobile app might crash on a different screen size. The API might return 200 when it should return 400. The database might have orphan records after a cancellation. Testing only one layer gives false confidence.

The problem: **how do you validate that a multi-platform system actually works end-to-end?**

### Why This Matters

This is the **final project** of the bootcamp — a full QA cycle that brings together everything from the previous sprints:

| Previous Projects | This Project Combines |
|---|---|
| regression-testing (web) | Web testing |
| mobile-testing (Android) | Mobile testing |
| api-testing (Postman) | API testing |
| console-sql (SQL) | Database validation |
| test-design (EC + BVA) | Requirements → design → execution |
| cross-browser-testing (multi-env) | Multi-platform coordination |

It's one thing to test a single layer. It's another to **coordinate QA across 4 layers** — understanding how a web order affects the database, how an API call affects the mobile app, and how a bug in one layer might indicate a deeper issue in another.

### The Approach — Scope & Cuts

I tested **4 layers** of Urban Scooter:

| Layer | Application | Tools Used |
|---|---|---|
| **Web** | Urban Scooter web app — order status, rental form, recipient form | Chrome, Excel |
| **Mobile** | Urban Scooter native Android app | Android Studio, AVD |
| **API** | Urban Scooter backend endpoints | Postman |
| **Database** | Data integrity after business transactions | SQL (PostgreSQL) |

**What was cut:**
- No automation — the full QA cycle is manual by design for the final project
- No cross-browser — scope was functional validation across layers, not environments
- No performance testing — functional + data integrity were the priorities

> 4 layers, 3 application types, 1 database. The scope is broad by design — the point is showing you can work across the entire stack, not just one area.

### Tools — Chosen by Need

| Tool | Why, Not Just What |
|---|---|
| **Chrome** | Standard browser for web UI testing. No special setup. |
| **Android Studio + AVD** | The standard Android emulator. Mobile testing in a controlled environment. |
| **Postman** | REST API testing. Same tool used in the api-testing project. |
| **SQL (PostgreSQL)** | Database verification — ensuring data matches what the UI and API show. |

Each tool was chosen because it's the **standard for its layer**. The project isn't about learning new tools — it's about **coordinating testing across them**.

### How It Was Broken Down

4 independent sessions, one per layer:

1. **Requirements analysis** → Mind map → Test strategy (cross-layer)
2. **Web testing** — Functional UI, form fields, checklists
3. **Mobile testing** — Android emulator, native app flows
4. **API testing + SQL validation** — Backend endpoints + database integrity

Sessions 1 was the planning phase. Sessions 2–4 could be done in any order — no dependencies between layers once the strategy was set.

### The Results

| Layer | Approach | Key Technique |
|---|---|---|
| **Web** | Functional checklist, field validation | Equivalence partitioning, BVA |
| **Mobile** | Android emulator, native UI | Screen transitions, touch targets |
| **API** | REST endpoints via Postman | HTTP methods, status code validation |
| **Database** | SQL queries after transactions | Data integrity, CRUD verification |

All defects documented in `bug-reports/` organized by layer (web, mobile, API) with environment details, steps to reproduce, and expected vs. actual results.

---

### Repository Structure

```
📦 full-qa-cycle/
├── docs/               # Requirements & analysis docs
├── test-artifacts/     # All test materials
│   ├── api-testing/        # API test cases
│   ├── mobile-tests/       # Mobile test cases
│   └── test-cases/         # Web test cases & checklists
└── bug-reports/        # Defect documentation by layer
```

---

## 🇪🇸 Español

### El Problema

**Urban Scooter** era un servicio de alquiler de scooters eléctricos — app web, app móvil, backend API y base de datos SQL. Cada capa podía tener bugs de forma independiente.

El formulario web podía aceptar una fecha inválida. La app móvil podía fallar en un tamaño de pantalla diferente. La API podía devolver 200 cuando debería devolver 400. La base de datos podía tener registros huérfanos después de una cancelación. Probar una sola capa da falsa confianza.

El problema: **cómo validás que un sistema multiplataforma realmente funciona end-to-end.**

### Por Qué Importa

Este es el **proyecto final** del bootcamp — un ciclo completo de QA que integra todo lo aprendido en los sprints anteriores:

| Proyectos anteriores | Este proyecto combina |
|---|---|
| regression-testing (web) | Pruebas web |
| mobile-testing (Android) | Pruebas móviles |
| api-testing (Postman) | Pruebas de API |
| console-sql (SQL) | Validación de base de datos |
| test-design (EC + BVA) | Requisitos → diseño → ejecución |
| cross-browser-testing (multi-entorno) | Coordinación multiplataforma |

Una cosa es probar una sola capa. Otra es **coordinar QA a través de 4 capas** — entender cómo un pedido web afecta la base de datos, cómo una llamada API afecta la app móvil, y cómo un bug en una capa puede indicar un problema más profundo en otra.

### El Enfoque — Alcance y Recortes

Probé **4 capas** de Urban Scooter:

| Capa | Aplicación | Herramientas |
|---|---|---|
| **Web** | App web Urban Scooter | Chrome, Excel |
| **Móvil** | App Android nativa | Android Studio, AVD |
| **API** | Endpoints del backend | Postman |
| **Base de datos** | Integridad de datos | SQL (PostgreSQL) |

**Lo que se recortó:**
- Sin automatización — el ciclo completo de QA es manual por diseño para el proyecto final
- Sin cross-browser — el alcance fue validación funcional entre capas, no entornos
- Sin pruebas de rendimiento — funcional + integridad de datos fueron las prioridades

> 4 capas, 3 tipos de aplicación, 1 base de datos. El alcance es amplio por diseño — el punto es demostrar que podés trabajar en todo el stack, no solo en un área.

### Stack — Elegido por Necesidad

| Herramienta | Por Qué, No Solo Qué |
|---|---|
| **Chrome** | Navegador estándar para pruebas web UI. Sin configuración especial. |
| **Android Studio + AVD** | El emulador Android estándar. Pruebas móviles en entorno controlado. |
| **Postman** | Pruebas de API REST. Misma herramienta usada en el proyecto api-testing. |
| **SQL (PostgreSQL)** | Verificación de base de datos — asegurar que los datos coinciden con UI y API. |

Cada herramienta fue elegida porque es el **estándar para su capa**. El proyecto no es sobre aprender herramientas nuevas — es sobre **coordinar pruebas entre ellas**.

### Cómo se Fragmentó

4 sesiones independientes, una por capa:

1. **Análisis de requisitos** → Mapa mental → Estrategia de pruebas (entre capas)
2. **Pruebas web** — UI funcional, campos de formulario, checklists
3. **Pruebas móviles** — Emulador Android, flujos de app nativa
4. **Pruebas de API + validación SQL** — Endpoints backend + integridad de base de datos

La sesión 1 fue la planificación. Las sesiones 2–4 podían hacerse en cualquier orden — sin dependencias entre capas una vez definida la estrategia.

### Los Resultados

| Capa | Enfoque | Técnica clave |
|---|---|---|
| **Web** | Checklist funcional, validación de campos | Partición de equivalencia, BVA |
| **Móvil** | Emulador Android, UI nativa | Transiciones de pantalla, targets táctiles |
| **API** | Endpoints REST via Postman | Métodos HTTP, validación de códigos de estado |
| **Base de datos** | Consultas SQL post-transacciones | Integridad de datos, verificación CRUD |

Todos los defectos documentados en `bug-reports/` organizados por capa (web, mobile, API) con entorno, pasos de reproducción, y resultado esperado vs. actual.

---

### Estructura del Repositorio

```
📦 full-qa-cycle/
├── docs/               # Docs de requisitos y análisis
├── test-artifacts/     # Materiales de prueba
│   ├── api-testing/        # Casos de API
│   ├── mobile-tests/       # Casos móviles
│   └── test-cases/         # Casos web y checklists
└── bug-reports/        # Defectos por capa
```
