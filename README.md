# GemeloIA

GemeloIA is an AI-powered digital twin assistant integrated with Telegram. The project is being developed as part of a Higher Vocational Training programme (Grado Superior) in Multiplatform Application Development (DAM) in Spain.

The assistant progressively builds a structured user context from profile data, conversation history, habits, food records, emotional state, goals and interests. This context is used to generate increasingly personalized responses and recommendations through the OpenAI API.

## Technology stack

- Java 21
- Spring Boot
- Spring Data JPA
- Hibernate
- PostgreSQL
- Telegram Bot API
- TelegramBots for Java
- OpenAI API
- Apache Maven
- Docker
- Git and GitHub

## Architecture

GemeloIA follows a layered backend architecture:

1. **Presentation** — receives and sends Telegram updates through the bot integration.
2. **Application** — coordinates conversations, users, context, records and recommendations.
3. **AI integration** — isolates access to the OpenAI API behind an application service interface.
4. **Persistence** — uses Spring Data JPA and Hibernate to manage domain entities.
5. **Data** — stores persistent information in PostgreSQL.

The project documentation and implementation are intended to evolve together so that the diagrams describe the real codebase.

## Current status

**Design completed → implementation pending.**

The current project report already defines:

- conceptual Entity-Relationship model
- domain class diagram
- layered architecture
- use-case diagram
- sequence diagram
- Telegram wireframes and mockups
- reference Java code for Telegram processing, JPA persistence, contextual memory and OpenAI integration

## Repository structure

- `docs/architecture/` — architecture notes and technical decisions
- `docs/diagrams/` — source files and exports of the project diagrams
- `.env.example` — example environment configuration
- `.gitignore` — ignored local, IDE and build files

The Java/Spring Boot source structure will be added when implementation begins.

## Configuration

Copy `.env.example` to a local `.env` file or configure the equivalent environment variables in your development environment.

Never commit real API keys, Telegram bot tokens or database passwords.

## Academic context

This repository supports the development of the GemeloIA final project for the DAM programme. The repository is kept aligned with the project report so that the academic documentation, architecture and implemented system remain consistent.
