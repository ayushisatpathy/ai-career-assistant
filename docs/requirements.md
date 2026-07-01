# Software Requirements Specification (SRS)

## 1. Project Overview

AI Career Assistant is a full-stack web application designed to help users improve their resumes and prepare for technical interviews using Generative AI.

The project aims to demonstrate not only AI-powered application development but also the engineering process involved in building software with AI assistance.

---

## 2. Problem Statement

Job seekers often face challenges such as:

- Knowing whether their resume matches industry expectations.
- Understanding missing skills required for a target role.
- Preparing for technical interviews in a structured manner.
- Receiving personalized feedback without relying on expensive coaching platforms.

This project addresses these challenges by providing AI-generated resume feedback and personalized interview preparation.

---

## 3. Objectives

The application should allow users to:

- Create an account securely.
- Upload resumes.
- Receive AI-powered resume analysis.
- Identify missing skills.
- Generate interview questions based on resume content.
- Receive AI-generated interview feedback.
- Download an ATS-optimized resume.

---

## 4. Functional Requirements

### Authentication

- Register
- Login
- Logout
- JWT Authentication
- Protected Routes

### Resume Module

- Upload Resume
- Store Resume
- Retrieve Resume
- Generate ATS Resume PDF

### AI Module

- Resume Analysis
- Skill Extraction
- Skill Gap Detection
- Interview Question Generation
- Interview Feedback

### Dashboard

- View Previous Reports
- Resume History
- Interview History

---

## 5. Non Functional Requirements

- Secure Authentication
- Scalable Architecture
- Modular Code Structure
- Responsive User Interface
- Maintainable Codebase
- AI Response Validation

---

## 6. Assumptions

- Users have resumes in PDF format.
- Gemini API remains available.
- Internet connection is required for AI features.

---

## 7. Future Scope

- Multiple Resume Versions
- Cover Letter Generator
- Company-specific Interview Preparation
- Mock Voice Interviews
- Recruiter Dashboard

---

## 8. Definition of Done

The first version will be considered complete when users can:

- Register and Login
- Upload Resume
- Receive Resume Analysis
- Generate Interview Questions
- Download AI-generated ATS Resume
