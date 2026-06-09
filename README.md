# 🛴 Urban Scooter — Full QA Cycle

**TripleTen QA Engineering Bootcamp · Cohort 23 · Proyecto Final**
👤 Luis Manco · Medellín, Colombia

[![Web](https://img.shields.io/badge/Web-Manual%20Testing-2E5FA3?style=flat-square)](.)
[![Mobile](https://img.shields.io/badge/Mobile-Android-43B02A?style=flat-square&logo=android)](.)
[![API](https://img.shields.io/badge/API-Postman-FF6C37?style=flat-square&logo=postman)](.)
[![SQL](https://img.shields.io/badge/SQL-PostgreSQL-336791?style=flat-square&logo=postgresql)](.)
[![Status](https://img.shields.io/badge/Status-Complete-green?style=flat-square)](.)

🇺🇸 [English](#-english) · 🇪🇸 [Español](#-español)

---

## 🇺🇸 English

### Project Overview

This repository contains the complete QA cycle for **Urban Scooter**, a modern electric scooter rental service. The project covers web, mobile, and API testing — from requirements analysis and test design through execution and defect reporting.

This is the **final project** of the TripleTen QA Engineering Bootcamp, demonstrating a full-lifecycle QA process across multiple platforms.

### Skills Demonstrated

| Skill | Applied In |
|-------|-----------|
| ✅ Requirements Analysis | Docs review → mind map → test strategy |
| ✅ Test Design | Equivalence Partitioning, Boundary Value Analysis |
| ✅ Web Testing | Functional UI validation, form field testing |
| ✅ Mobile Testing | Native Android app, emulator-based testing |
| ✅ API Testing | Postman, REST endpoints, status code validation |
| ✅ SQL | Data integrity queries, transaction verification |
| ✅ Defect Reporting | Professional bug reports with steps to reproduce |

### Repository Structure

```
📦 urban-scooter-qa-project/
├── docs/               # Requirements & analysis docs
│   ├── requirements-backend.pdf
│   ├── requirements-mobile.pdf
│   └── requirements-web.pdf
├── test-artifacts/     # All test materials
│   ├── api-testing/        # API test cases (.csv, .xlsx)
│   ├── mobile-tests/       # Mobile test cases (.csv, .xlsx)
│   └── test-cases/         # Web test cases & checklists
│       ├── data_validation/
│       └── testing_checklist/
├── bug-reports/        # Defect documentation
│   ├── api-testing-bugs/
│   ├── mobile-tests-bugs/
│   └── test-cases-bugs/
└── README.md
```

### What Was Tested

| Layer | Application | Tools |
|-------|------------|-------|
| **Web** | Urban Scooter web app — order status, rental form, recipient form | Chrome, Excel |
| **Mobile** | Urban Scooter native Android app | Android Studio, AVD |
| **API** | Urban Scooter backend endpoints | Postman |
| **Database** | Data integrity after business transactions | SQL (PostgreSQL) |

### Key Findings

- Designed and executed tests across **3 application layers** (web, mobile, API)
- Applied **equivalence partitioning** and **boundary value analysis** to form fields and API inputs
- Created **SQL queries** to verify database state after CRUD operations
- Documented all defects in structured bug reports with environment details, steps to reproduce, and expected vs. actual results

---

## 🇪🇸 Español

### Descripción del Proyecto

Este repositorio contiene el ciclo completo de QA para **Urban Scooter**, un servicio moderno de alquiler de scooters eléctricos. El proyecto cubre pruebas web, móviles y de API — desde el análisis de requisitos y diseño de pruebas hasta la ejecución y reporte de defectos.

Este es el **proyecto final** del TripleTen QA Engineering Bootcamp, demostrando un proceso de QA de ciclo completo a través de múltiples plataformas.

### Habilidades Demostradas

| Habilidad | Aplicada en |
|-----------|-------------|
| ✅ Análisis de requisitos | Revisión de docs → mapa mental → estrategia de pruebas |
| ✅ Diseño de pruebas | Partición de equivalencia, Análisis de valores límite |
| ✅ Pruebas web | Validación funcional de UI, campos de formulario |
| ✅ Pruebas móviles | App Android nativa, pruebas en emulador |
| ✅ Pruebas de API | Postman, endpoints REST, validación de códigos de estado |
| ✅ SQL | Consultas de integridad de datos, verificación de transacciones |
| ✅ Reporte de defectos | Informes profesionales con pasos de reproducción |

### Estructura del Repositorio

```
📦 urban-scooter-qa-project/
├── docs/               # Documentos de requisitos y análisis
├── test-artifacts/     # Todos los materiales de prueba
│   ├── api-testing/        # Casos de prueba de API
│   ├── mobile-tests/       # Casos de prueba móviles
│   └── test-cases/         # Casos de prueba web y checklists
└── bug-reports/        # Documentación de defectos
```

### Qué se Probó

| Capa | Aplicación | Herramientas |
|------|-----------|-------------|
| **Web** | App web Urban Scooter | Chrome, Excel |
| **Móvil** | App Android nativa | Android Studio, AVD |
| **API** | Endpoints del backend | Postman |
| **Base de datos** | Integridad de datos | SQL (PostgreSQL) |

### Hallazgos Clave

- Pruebas diseñadas y ejecutadas en **3 capas de aplicación** (web, móvil, API)
- Aplicación de **partición de equivalencia** y **análisis de valores límite**
- **Consultas SQL** para verificar el estado de la base de datos
- Defectos documentados con entorno, pasos de reproducción, y resultado esperado vs. actual

---

> 📚 Final project developed as part of the **TripleTen QA Engineering Bootcamp** · Cohort 23 · Proyecto Final
