# Development Journal

## Purpose

This journal captures the thought process behind the development of AI Career Assistant.

Rather than documenting only completed tasks, it records observations, design decisions, challenges, lessons learned, and how my understanding evolves throughout the project.

The intention is to reflect on engineering decisions instead of simply tracking implementation progress.

---

# Day 1 — Project Foundation

## Date

02 July 2026

---

## Goal

Establish the initial backend foundation and organize the project for long-term development.

---

## Initial Thoughts

At the beginning of the project, my primary objective was simply to start building the application.

However, after discussing the project approach and reviewing feedback, I realized that the engineering process itself is just as important as the final application.

Instead of focusing only on writing code, I decided to organize the repository, document architectural decisions, and build the project incrementally.

---

## Key Decisions Made

- Created separate backend and frontend directories.
- Introduced a dedicated documentation folder.
- Chose MongoDB as the database.
- Created a dedicated configuration module for the database connection.
- Began documenting technical decisions alongside implementation.

---

## Challenges Faced

The initial Git setup became more complex than expected because the GitHub repository already contained a README and other files.

While restructuring the project, I also encountered merge conflicts caused by file renaming.

Although these issues slowed down development, resolving them improved my understanding of Git workflows.

---

## What I Learned

A project starts long before writing business logic.

Repository organization, documentation, and planning have a significant impact on maintainability.

I also realized that making structural decisions early reduces future refactoring effort.

---

## AI Reflection

AI was extremely helpful in brainstorming project organization and explaining different architectural options.

However, I found that understanding *why* a suggestion was made is more valuable than simply copying it.

The process of questioning AI-generated suggestions helped strengthen my own understanding of the project.

---

## Questions for Future Me

- Will the current project structure continue to scale as more modules are added?
- At what point should a service layer be introduced?
- Should the backend eventually move to a feature-based architecture instead of a layered architecture?

These questions will be revisited later in the project.

---

## Next Goal

Implement secure authentication using JWT while continuing to document architectural decisions and lessons learned.
