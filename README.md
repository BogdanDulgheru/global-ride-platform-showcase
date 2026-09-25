# Global Ride Platform — Engineering Showcase

> A full-stack ride-hailing platform prototype built as a hands-on engineering project with Flutter and Python/FastAPI.

[![Flutter](https://img.shields.io/badge/Flutter-Dart-02569B?logo=flutter)](https://flutter.dev/)
[![FastAPI](https://img.shields.io/badge/FastAPI-Python-009688?logo=fastapi)](https://fastapi.tiangolo.com/)
[![Google Maps](https://img.shields.io/badge/Google%20Maps-Platform-4285F4?logo=googlemaps)](https://mapsplatform.google.com/)
![Repository](https://img.shields.io/badge/source-private-important)

## Overview

Global Ride explores the architecture and end-to-end workflow of a modern ride-hailing product. The project combines a Flutter client with a Python/FastAPI backend and models the interaction between passengers, drivers, operators, vehicles, rides, routing and payments.

This public repository is intentionally a **showcase**, not a source-code mirror. The complete implementation is maintained in a private repository.

## What the project demonstrates

- Passenger and driver application modes
- Destination search and place autocomplete
- Google Maps integration, GPS/location handling and route computation
- Ride categories: Economy, Comfort and XL
- Ride request and driver acceptance workflow
- Persistent ride storage through SQLAlchemy/PostgreSQL-oriented data access
- Driver, operator, user and vehicle domain models
- Ride feedback with rating, tip and comments
- Payment/receipt domain flow implemented as demo infrastructure
- HTTP API communication between Flutter and FastAPI
- Modular backend structure with API, schemas, services, models and database layers

## Architecture

```text
┌─────────────────────────────────────┐
│            Flutter Client           │
│                                     │
│ Passenger UI        Driver UI       │
│ Maps • GPS • Search • Ride Flow     │
└──────────────────┬──────────────────┘
                   │ HTTP / JSON
                   ▼
┌─────────────────────────────────────┐
│          Python / FastAPI API       │
│                                     │
│ Places • Routes • Rides • Payments  │
└─────────┬───────────────┬───────────┘
          │               │
          ▼               ▼
┌─────────────────┐  ┌────────────────┐
│ Google Maps     │  │ Service / Data │
│ Places & Routes │  │ Access Layers  │
└─────────────────┘  └───────┬────────┘
                              ▼
                     ┌────────────────┐
                     │ SQLAlchemy /   │
                     │ PostgreSQL     │
                     └────────────────┘
```

## Technology stack

| Layer | Technologies |
| --- | --- |
| Mobile / UI | Flutter, Dart, Material |
| Maps & location | Google Maps Flutter, Geolocator, Google Places & Routes APIs |
| API | Python, FastAPI, Pydantic |
| HTTP | Dart HTTP, HTTPX |
| Persistence | SQLAlchemy, PostgreSQL-oriented persistence |
| Local state | SharedPreferences |
| Domain | Passenger, Driver, Operator, Vehicle, Ride, Payment |
| Engineering workflow | Git, GitHub, AI-assisted development |

## Backend organization

The private implementation is organized around clear responsibilities:

```text
backend/
├── app/
│   ├── api/          # HTTP route modules
│   ├── core/         # shared utilities
│   ├── database/     # persistence and data-access layer
│   ├── models/       # domain models
│   ├── schemas/      # request/response contracts
│   └── services/     # maps, rides and payment logic
└── main.py           # FastAPI application
```

The Flutter application contains the passenger/driver experience, map interaction, destination workflow and API communication.

## Engineering decisions

**Server-side Maps access.** Sensitive server credentials are read from environment configuration rather than committed to source control. Places and route operations are exposed through backend endpoints.

**Persistent ride state.** Ride data is handled through a service/data-access layer rather than relying on in-memory application state.

**Separated domain concepts.** Users, drivers, operators and vehicles are represented independently so the model can evolve beyond a single-user prototype.

**Explicit API contracts.** Pydantic schemas define ride creation, acceptance, routing, feedback and payment-related requests.

## Current project status

Global Ride is an evolving portfolio project, not a production transportation service. The current implementation demonstrates the application architecture and core ride lifecycle. Payment processing is intentionally demo infrastructure; no real card processor is connected.

Areas intended for further development include authentication/authorization hardening, production payment integration, real-time event delivery, automated testing, deployment infrastructure and production observability.

## Screenshots & demo

### Passenger destination search

<p align="center">
  <img src="assets/destination-search.jpg" width="320" alt="Global Ride destination search showing Vienna Airport autocomplete" />
</p>

The working demo includes the complete ride lifecycle: destination autocomplete, route calculation, Economy/Comfort/XL fare selection, driver matching, driver acceptance, pickup/arrival, ride start and completion, passenger rating and tip, payment selection, and receipt generation.

The screenshot above is captured from the running Android demo and shows the live destination-search flow for Vienna Airport.

> **Full source code is maintained in a private repository and can be made available for technical review upon request.**

## About the developer

Built by **Bogdan Dulgheru** as a portfolio engineering project focused on Python, AI-assisted software development, backend architecture and cross-platform application development.

AI coding tools are used as part of the engineering workflow while architecture, validation, testing and final implementation decisions remain developer responsibilities.

---

### Why this repository is public

The goal of this repository is to let recruiters and engineering teams evaluate the project's scope, architecture and engineering decisions without publishing the complete implementation or sensitive configuration.