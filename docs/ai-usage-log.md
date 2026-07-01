# AI Usage Log

## Purpose

This document records how AI is used throughout the development of AI Career Assistant.

The objective is not to document every prompt, but to evaluate where AI accelerated development, where it introduced incorrect or suboptimal suggestions, and how those suggestions were reviewed before implementation.

Each entry records the engineering judgment applied when collaborating with AI.

---

# Session 1 — Project Planning

## Objective

Define the overall project scope and development approach.

## How AI was Used

AI was used to brainstorm project ideas, identify possible features, and organize the project into manageable milestones.

## Outcome

The final roadmap was refined manually to focus on building features incrementally instead of implementing everything at once.

## Reflection

AI was useful for exploring ideas quickly, but prioritization required human judgment.

---

# Session 2 — Repository Organization

## Objective

Design the repository structure.

## AI Suggestion

Organize the repository into separate backend, frontend, and documentation directories.

## Decision

Accepted.

## Reason

The separation provides better maintainability and keeps implementation, documentation, and future frontend development independent.

## Learning

Project organization is much easier when done early rather than after features have already been implemented.

---

# Session 3 — Backend Setup

## Objective

Initialize the backend application.

## AI Assistance

AI suggested the initial Express project structure and configuration.

## Decision

Accepted with modifications.

## Changes Made

The database connection was placed inside a dedicated configuration module instead of keeping all initialization logic in a single file.

## Reflection

AI accelerated the setup process, but understanding the purpose of each file was necessary before adopting the generated structure.

---

# Session 4 — Database Selection

## Objective

Choose a database for the project.

## AI Assistance

AI compared MongoDB and PostgreSQL based on the project requirements.

## Decision

MongoDB was selected.

## Reason

Resume analysis and AI-generated reports are naturally document-oriented and likely to evolve throughout development.

## Reflection

AI provided a useful comparison, but the final decision was based on the expected evolution of the application's data model.

---

# Lessons Learned So Far

- AI significantly reduces repetitive setup work.
- Architectural decisions should not be accepted without understanding the trade-offs.
- Reviewing AI-generated suggestions improves learning and confidence in the implementation.
- AI works best as a collaborative assistant rather than a replacement for engineering judgment.

---

# Future Sessions

Future entries will include:

- JWT Authentication
- Password Hashing
- Token Blacklisting
- File Upload Architecture
- AI Prompt Engineering
- Resume Parsing
- Gemini Integration
- PDF Generation
- Deployment
