# Architecture Decision Records (ADR)

## Purpose

This document records the significant architectural and technical decisions made throughout the development of **AI Career Assistant**.

Rather than documenting only the final implementation, it captures the reasoning behind each decision, the alternatives considered, the trade-offs involved, and reflections after implementation.

The objective is to make the engineering process transparent and easier to evaluate as the project evolves.

---

# ADR-001 — Repository Structure

## Status

Accepted

## Date

02 July 2026

## Context

The application is planned as a full-stack project consisting of:

- A backend API
- A React frontend
- AI integrations
- Project documentation
- Deployment configuration

Initially, it would have been simpler to keep everything inside a single Node.js project. However, as additional features such as authentication, AI modules, resume management, and deployment are introduced, that structure would become increasingly difficult to maintain.

## Decision

The repository is organized into separate top-level directories.

```
backend/
frontend/
docs/
```

## Alternatives Considered

### Option 1 — Single Project Structure

```
src/
client/
package.json
```

#### Advantages

- Simpler initial setup
- Fewer directories
- Faster to start development

#### Disadvantages

- Backend and frontend become tightly coupled.
- Documentation is mixed with implementation.
- Harder to scale as new features are added.

---

### Option 2 — Separate Backend, Frontend and Documentation (Chosen)

#### Advantages

- Clear separation of concerns.
- Independent frontend and backend development.
- Easier future deployment.
- Cleaner project organization.
- Documentation evolves alongside implementation.

#### Disadvantages

- Slightly more setup work during the initial stages.

## Why this decision?

The project is intended to grow into a production-style application rather than remain a tutorial project.

Separating responsibilities early reduces future restructuring and encourages a cleaner development workflow.

---

# ADR-002 — Backend Organization

## Status

Accepted

## Date

02 July 2026

## Context

Even during the initial setup, the backend already required separate responsibilities for application configuration, database connectivity, and data models.

Keeping everything inside a single file would make future development increasingly difficult.

## Decision

The backend currently follows the following structure.

```
backend/

src/
    config/
    models/
    app.js

server.js
```

## Why this structure?

### server.js

Responsible only for starting the HTTP server.

### app.js

Responsible for configuring the Express application.

### config/

Contains infrastructure-related configuration such as database initialization.

### models/

Contains Mongoose schemas representing application data.

## Benefits

- Better separation of responsibilities.
- Easier debugging.
- Easier testing.
- Simpler future expansion.

## Future Evolution

As additional functionality is implemented, the backend will gradually evolve to include:

```
controllers/
routes/
middleware/
services/
validators/
utils/
```

These directories will only be introduced when they become necessary rather than creating empty folders prematurely.

---

# ADR-003 — Database Selection

## Status

Accepted

## Date

02 July 2026

## Context

The application stores user accounts today and will later manage:

- Resume metadata
- AI-generated resume analysis
- Interview reports
- User activity

The structure of AI-generated data is expected to evolve throughout development.

## Decision

MongoDB was selected as the primary database with Mongoose as the ODM.

## Alternatives Considered

### PostgreSQL

#### Advantages

- Strong relational consistency.
- Strict schema enforcement.
- Excellent transactional support.

#### Disadvantages

- Less flexible during rapid feature iteration.
- Schema migrations become more frequent while experimenting.

---

### MongoDB (Chosen)

#### Advantages

- Flexible document structure.
- Naturally stores JSON-like data.
- Excellent integration with Node.js.
- Easier schema evolution during experimentation.

#### Disadvantages

- Validation responsibility shifts more towards the application.

## Why this decision?

Since resumes and AI-generated outputs naturally fit a document-oriented structure, MongoDB offers greater flexibility while the application requirements continue to evolve.

---

# ADR-004 — Documentation Strategy

## Status

Accepted

## Date

02 July 2026

## Context

The goal of this project extends beyond building a working application.

It is also intended to document the engineering process and demonstrate how AI contributes throughout software development.

## Decision

Every major feature will include documentation covering:

- The requirement.
- The implementation approach.
- Architectural decisions.
- AI assistance.
- Development progress.
- Personal reflections.

## Why?

A finished application shows **what** was built.

The accompanying documentation explains **why** it was built that way.

Recording these decisions makes it easier to evaluate the engineering thought process and revisit earlier assumptions as the project evolves.

---

# Planned Future Decisions

This document will continue to evolve throughout development.

Future Architecture Decision Records will include:

- ADR-005 — Authentication Strategy (JWT)
- ADR-006 — Password Security (bcrypt)
- ADR-007 — Token Blacklisting
- ADR-008 — File Upload Architecture
- ADR-009 — Resume Storage Strategy
- ADR-010 — AI Integration Strategy
- ADR-011 — Prompt Engineering
- ADR-012 — Resume Parsing Pipeline
- ADR-013 — PDF Generation Strategy
- ADR-014 — Error Handling
- ADR-015 — Deployment Architecture
