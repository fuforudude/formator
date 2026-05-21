# AGENTS.md

# Project Overview

This project is a web application for managing pedagogical and administrative activity for a freelance trainer/intervenor working with multiple schools.

The application centralizes:
- schools
- courses
- prestations
- invoices
- documents
- planning

The goal is to build a realistic MVP:
- maintainable
- modular
- simple
- fast to develop
- professional enough for a school project presentation

The application is designed for ONE administrator user only.

No advanced multi-user management is required.

---

# Tech Stack

## Frontend
- React
- TypeScript
- React Router
- Axios
- TailwindCSS

## Backend
- NestJS
- TypeScript
- REST API
- JWT Authentication

## Database
- PostgreSQL

## Infrastructure
- Docker
- docker-compose

---

# Architecture

The application uses a modular monolithic architecture.

Structure:
- /frontend
- /backend

Communication:
- REST API only

Rules:
- NO microservices
- NO CQRS
- NO event sourcing
- NO websocket
- NO distributed architecture
- NO unnecessary abstraction
- NO overengineering

Focus on:
- readability
- maintainability
- simplicity
- delivery speed

---

# Backend Architecture Rules

Use NestJS modules.

Each feature module must contain:
- controller
- service
- dto
- entity

Example:
backend/src/modules/schools/
- schools.controller.ts
- schools.service.ts
- dto/
- entities/

Controllers must remain thin.

Business logic must stay inside services.

Use DTO validation with:
- class-validator
- class-transformer

Use REST naming conventions.

---

# Database Rules

Use PostgreSQL.

Prefer simple relations.

Avoid premature optimization.

Use clear entity naming.

Use timestamps on major entities:
- createdAt
- updatedAt

Prefer enums for statuses.

---

# Frontend Rules

Frontend structure:
- pages
- components
- services
- hooks
- layouts
- types

Rules:
- small reusable components
- avoid huge pages
- use TypeScript everywhere
- use Axios service layer for API calls
- no Redux unless truly necessary

Use TailwindCSS for styling.

Responsive design required.

---

# Authentication

Single administrator user.

Requirements:
- JWT authentication
- login page
- protected routes
- no registration system
- no role system

---

# Core Features

## Schools
- create school
- edit school
- delete school
- school details page
- administrative information
- contacts
- notes

## Courses
- create course
- edit course
- delete course
- school association
- planning/calendar view
- start/end date
- duration

## Prestations
- follow completed hours
- prestation status:
  - planned
  - completed
  - invoiced
  - paid

## Invoices
- generate invoices
- invoice PDF export
- payment follow-up
- unpaid invoices
- non-invoiced prestations detection

## Documents
- upload files
- associate documents with:
  - schools
  - courses
  - invoices
- local file storage

## Dashboard
- upcoming courses
- unpaid invoices
- quick statistics

---

# Features NOT Included

Do NOT implement:
- advanced student management
- grading system
- attendance system
- school platform synchronization
- real-time features
- messaging system
- notifications system
- complex integrations
- multi-tenant architecture

---

# Docker Rules

Use Docker for:
- frontend
- backend
- postgres

Use docker-compose for local development.

Environment variables must be stored in:
- .env

Never hardcode secrets.

---

# Code Quality

Rules:
- TypeScript everywhere
- async/await only
- clear naming
- avoid duplicated logic
- short functions
- simple architecture
- maintainable code

Avoid:
- unnecessary patterns
- generic abstractions
- premature optimization

---

# API Conventions

REST API conventions:

GET /schools
GET /schools/:id
POST /schools
PATCH /schools/:id
DELETE /schools/:id

Use:
- DTO validation
- proper HTTP status codes
- consistent JSON responses

---

# Entity Suggestions

## School
- id
- name
- address
- email
- phone
- adminContact
- pedagogicalContact
- notes

## Course
- id
- title
- startDate
- endDate
- duration
- room
- schoolId
- status

## Prestation
- id
- courseId
- hours
- rate
- status

## Invoice
- id
- number
- amount
- status
- issuedAt
- paidAt

## Document
- id
- filename
- path
- type
- relatedEntity
- uploadedAt

---

# Development Philosophy

The goal is NOT to create:
- a full ERP
- a full school management system
- a complex SaaS

The goal IS:
- a coherent MVP
- a clean architecture
- a realistic application
- a maintainable codebase
- a successful school project

Always prefer:
- simplicity
- readability
- modularity
- realistic scope