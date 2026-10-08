# Architecture

This directory contains architecture notes and technical decisions for GemeloIA.

The architecture documented here must remain aligned with the project report and with the implementation.

## Current architecture

GemeloIA is designed as a layered Java 21 / Spring Boot backend.

### External systems

- **Telegram Bot API** — user-facing communication channel
- **OpenAI API** — generation of contextualized responses

### Presentation layer

- `GemeloIABot`
- `TelegramUpdateHandler`

This layer receives Telegram updates, extracts channel-specific data and delegates application logic.

### Application layer

Main planned services:

- `ConversationService` — coordinates the conversation flow
- `UsuarioService` — manages user profile data
- `ContextoUsuarioService` — builds the relevant persistent context
- `RecomendacionService` — manages recommendation generation and lifecycle
- `RegistroService` — manages habits, food and emotional records
- `IAService` — interface that defines AI generation
- `OpenAIService` — OpenAI implementation of `IAService`

### Persistence layer

- Spring Data JPA repositories
- Hibernate ORM
- PostgreSQL

The persistence model includes users, sessions, interactions, habits, food records, emotional records, goals, interests, recommendations and recommendation feedback.

### Build and deployment

- Apache Maven for dependency management, testing and packaging
- Docker for reproducible deployment
- Ubuntu VPS as the planned production environment

## Architectural principles

- separation of responsibilities between layers
- dependency injection through Spring
- external APIs isolated behind application services
- persistence accessed through repositories
- contextual memory built from stored data rather than duplicated as a separate copy
- secrets supplied through environment configuration and never committed to Git
