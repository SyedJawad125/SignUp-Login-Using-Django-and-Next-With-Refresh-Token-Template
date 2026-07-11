<!-- You are a Senior Software Architect, Senior Django Developer, Senior Next.js Developer, Senior PostgreSQL Database Designer, DevOps Engineer, and UI/UX Expert with 15+ years of experience.

Your task is to generate a COMPLETE PRODUCTION READY project using the following technology stack.

=================================================
TECH STACK
=================================================

Backend
--------
• Python 3.13+
• Django 5+
• Django Rest Framework
• PostgreSQL
• Redis
• Celery
• JWT Authentication
• Docker
• Docker Compose
• Nginx
• Gunicorn
• Swagger/OpenAPI
• DRF Spectacular
• Pillow
• django-filter
• CORS
• Environment Variables
• Logging
• Email Services

Frontend
---------
• Next.js 15+
• React 19+
• TypeScript
• Tailwind CSS
• Shadcn UI
• React Hook Form
• Zod Validation
• Axios
• TanStack Query
• Redux Toolkit
• Next Auth (if needed)
• Responsive UI

Database
----------
PostgreSQL

=================================================
PROJECT STRUCTURE
=================================================

The architecture must always follow

Backend

apps/

users/
notifications/
images/
common/
core/
utils/

Frontend

app/

(auth)
dashboard
components
hooks
services
store
types
utils
lib

=================================================
CODING RULES
=================================================

Always follow

✔ Clean Architecture

✔ SOLID Principles

✔ DRY

✔ KISS

✔ Repository Pattern where needed

✔ Service Layer

✔ Reusable Components

✔ Generic APIs

✔ Generic Pagination

✔ Generic Search

✔ Generic Filtering

✔ Generic Sorting

✔ Generic Error Handling

✔ Proper HTTP Status Codes

✔ Production Ready Code

✔ Scalable Architecture

Never generate beginner code.

=================================================
DATABASE
=================================================

Use PostgreSQL.

Every model must include

created_at

updated_at

created_by

updated_by

soft delete if required

audit logs if needed

=================================================
USER MODEL
=================================================

The authentication system MUST use the following existing custom User model.

Fields

• username
• first_name
• last_name
• full_name
• email
• mobile
• profile_image
• login_attempts
• is_blocked
• is_staff
• is_superuser
• is_active
• is_verified
• password_link_token
• password_link_token_created_at
• password_reset_code
• password_reset_code_created_at
• password_reset_verified
• address
• last_password_changed
• role
• type
• activation_link_token
• activation_link_token_created_at
• deactivated
• password

User Manager

create_user()

create_superuser()

Authentication

JWT Authentication

Refresh Tokens

Access Tokens

Password Reset OTP

Email Verification

Role Based Authentication

Permission Based Authorization

=================================================
ROLE MODEL
=================================================

Use existing Role model

Fields

name

code_name

permissions

description

=================================================
PERMISSION MODEL
=================================================

Fields

name

code_name

module_name

module_label

description

=================================================
EMPLOYEE MODEL
=================================================

OneToOne with User

Status

INVITED

ACTIVE

DEACTIVATED

=================================================
USER FEATURES
=================================================

Generate complete APIs for

Register

Login

Logout

Refresh Token

Forgot Password

Verify OTP

Reset Password

Change Password

Update Profile

Upload Profile Image

Deactivate User

Activate User

Block User

Unblock User

User Listing

Search User

Filter User

Pagination

Delete User

Assign Role

Assign Permissions

Employee Invite

Employee Activation

=================================================
EMAIL TEMPLATE MODEL
=================================================

Use EmailTemplate model

Fields

name

subject

alternative_text

html_template

code_name

Generate APIs

Create Email Template

Update Email Template

Delete Email Template

List Templates

Preview Template

Render Variables

=================================================
IMAGE MODULE
=================================================

Categories

Images

Generate APIs

Upload Image

Delete Image

Update Image

Search Image

Pagination

Category CRUD

Multiple Image Upload

Image Validation

=================================================
NOTIFICATION SYSTEM
=================================================

Implement

Email Notifications

Password Reset Email

Verification Email

Welcome Email

Invitation Email

OTP Email

Reusable Email Service

HTML Templates

Background Email Sending using Celery

=================================================
BACKEND REQUIREMENTS
=================================================

Always generate

Models

Serializers

Views

ViewSets

Routers

URLs

Services

Selectors

Permissions

Validators

Signals

Managers

Admin

Tests

Swagger Documentation

=================================================
API FEATURES
=================================================

Every endpoint must support

Pagination

Filtering

Searching

Ordering

Validation

Permission Checking

Error Handling

Standard Response

Response format

{
    "success": true,
    "message": "",
    "data": {},
    "errors": []
}

=================================================
SECURITY
=================================================

Implement

JWT

Refresh Tokens

Role Based Access

Permission Based Access

CORS

CSRF

Rate Limiting

Password Validation

OTP Expiry

Email Token Expiry

Account Lock

Login Attempts

=================================================
NEXT JS FRONTEND
=================================================

Generate

Modern UI

Responsive Design

Dark Mode

Authentication

Dashboard

Sidebar

Navbar

Reusable Components

Loading Skeleton

Error Pages

Toast Notifications

Protected Routes

Role Based Pages

Permission Based UI

Forms using

React Hook Form

Zod

=================================================
PAGES
=================================================

Login

Register

Forgot Password

Verify OTP

Reset Password

Dashboard

Profile

Users

Roles

Permissions

Employees

Email Templates

Image Categories

Images

Settings

=================================================
FRONTEND FEATURES
=================================================

Generate

Reusable Table

Reusable Modal

Reusable Form

Reusable Button

Reusable Input

Reusable Select

Reusable Search

Pagination

Filters

Sorting

File Upload

Image Preview

Profile Upload

=================================================
STATE MANAGEMENT
=================================================

Use

Redux Toolkit

RTK Query or TanStack Query

Axios

Refresh Token Handling

=================================================
API INTEGRATION
=================================================

Generate

API Service Layer

Axios Interceptors

Automatic Token Refresh

Global Error Handling

Reusable Hooks

=================================================
POSTGRESQL
=================================================

Optimize

Indexes

Foreign Keys

Unique Constraints

Database Performance

=================================================
DOCKER
=================================================

Generate

Dockerfile

docker-compose.yml

Nginx

Production Configuration

Development Configuration

=================================================
TESTING
=================================================

Generate

Unit Tests

API Tests

Serializer Tests

Model Tests

Permission Tests

=================================================
CODE QUALITY
=================================================

Use

Black

isort

flake8

pre-commit

=================================================
PROJECT DOCUMENTATION
=================================================

Generate

README.md

Installation Guide

Environment Variables

Deployment Guide

API Documentation

Folder Structure

=================================================
OUTPUT FORMAT
=================================================

Whenever I ask for any module,

Always generate in this order

1. Database Design

2. Models

3. Serializers

4. Services

5. Permissions

6. Validators

7. Signals

8. Views

9. URLs

10. Tests

11. Swagger Documentation

12. Next.js Pages

13. Components

14. API Integration

15. Redux Store

16. UI Screens

17. Deployment Steps

18. Best Practices

19. Optimization

20. Security Improvements

Never skip any step.

Always generate enterprise-level production code that can be directly used in real client projects. -->











# Enterprise Full-Stack Boilerplate

A **production-ready, enterprise-grade full-stack template** built with **Django REST Framework** on the backend and **Next.js 15+ (React 19)** on the frontend. This boilerplate is designed to be cloned and extended for real client projects — authentication, RBAC, notifications, media management, and DevOps tooling are already wired up out of the box.

---

## Table of Contents

1. [Overview](#overview)
2. [Tech Stack](#tech-stack)
3. [Folder Structure](#folder-structure)
4. [Core Modules](#core-modules)
5. [Getting Started](#getting-started)
6. [Environment Variables](#environment-variables)
7. [Running with Docker](#running-with-docker)
8. [Running Locally (Without Docker)](#running-locally-without-docker)
9. [API Documentation](#api-documentation)
10. [Authentication & Authorization](#authentication--authorization)
11. [Standard API Response Format](#standard-api-response-format)
12. [Testing](#testing)
13. [Code Quality & Pre-commit](#code-quality--pre-commit)
14. [Deployment Guide](#deployment-guide)
15. [Contributing](#contributing)
16. [License](#license)

---

## Overview

This repository provides a fully scaffolded starting point for building multi-tenant, role-based, production applications. It follows **Clean Architecture**, **SOLID principles**, and a strict **service/selector/repository layering** so that business logic stays decoupled from views and models.

Out of the box you get:

- JWT-based authentication with refresh token rotation
- Role-based and permission-based access control (RBAC)
- User, Employee, Role, and Permission management
- Email notification system (OTP, password reset, welcome, invitation) powered by Celery
- Image/media management module with categories
- Fully documented REST API (Swagger / OpenAPI via DRF Spectacular)
- A modern, responsive Next.js dashboard with dark mode, protected routes, and role-aware UI
- Dockerized backend, frontend, database, cache, worker, and reverse proxy

---

## Tech Stack

### Backend

| Category | Technology |
|---|---|
| Language | Python 3.13+ |
| Framework | Django 5+ / Django REST Framework |
| Database | PostgreSQL |
| Cache / Broker | Redis |
| Async Tasks | Celery + Celery Beat |
| Auth | JWT (access + refresh tokens) |
| Docs | drf-spectacular (Swagger / OpenAPI) |
| Media | Pillow |
| Filtering | django-filter |
| Server | Gunicorn + Nginx |
| Containerization | Docker / Docker Compose |

### Frontend

| Category | Technology |
|---|---|
| Framework | Next.js 15+ (App Router) |
| UI Library | React 19+ |
| Language | TypeScript |
| Styling | Tailwind CSS + Shadcn UI |
| Forms | React Hook Form + Zod |
| HTTP Client | Axios (with interceptors) |
| Server State | TanStack Query |
| Client State | Redux Toolkit |
| Auth | NextAuth (optional, JWT-compatible) |

### Database

- PostgreSQL with optimized indexes, foreign keys, and unique constraints.

---

## Folder Structure

### Backend

```
backend/
├── apps/
│   ├── users/            # Custom user, roles, permissions, employees
│   ├── notifications/     # Email templates, Celery email tasks
│   ├── images/            # Image + category management
│   ├── common/            # Shared mixins, pagination, response wrappers
│   └── core/              # Project settings, urls, celery app
├── utils/                 # Helper functions, validators, constants
├── manage.py
├── requirements/
│   ├── base.txt
│   ├── local.txt
│   └── production.txt
├── Dockerfile
└── entrypoint.sh
```

Each app under `apps/` follows the same internal layout:

```
users/
├── models.py
├── managers.py
├── serializers.py
├── services.py        # business logic
├── selectors.py        # read/query logic
├── permissions.py
├── validators.py
├── signals.py
├── views.py
├── urls.py
├── admin.py
└── tests/
```

### Frontend

```
frontend/
├── app/
│   ├── (auth)/            # login, register, forgot/reset password, verify OTP
│   ├── dashboard/         # protected dashboard routes
│   ├── components/        # reusable UI components (table, modal, form, etc.)
│   ├── hooks/             # custom React hooks
│   ├── services/          # API service layer (axios instances per module)
│   ├── store/             # Redux Toolkit slices
│   ├── types/             # shared TypeScript types
│   ├── utils/             # helpers, formatters
│   └── lib/               # config, query client, axios instance
├── public/
├── next.config.js
├── tailwind.config.ts
└── Dockerfile
```

---

## Core Modules

### 1. Users & Authentication
Custom `User` model (username, email, mobile, profile image, login attempts, block/verify/activation flags, role, type, etc.) with:
- Register / Login / Logout
- Access + Refresh token issuance and rotation
- Forgot Password → OTP → Reset Password flow
- Change Password / Update Profile / Upload Profile Image
- Activate / Deactivate / Block / Unblock user
- Listing with pagination, search, filter, and ordering

### 2. Roles & Permissions
- `Role` model: `name`, `code_name`, `permissions`, `description`
- `Permission` model: `name`, `code_name`, `module_name`, `module_label`, `description`
- Assign roles/permissions to users; enforce via DRF permission classes

### 3. Employees
- `Employee` model (OneToOne with `User`)
- Status lifecycle: `INVITED → ACTIVE → DEACTIVATED`
- Invite and activation API flows

### 4. Email Templates & Notifications
- `EmailTemplate` model: `name`, `subject`, `alternative_text`, `html_template`, `code_name`
- CRUD + preview + variable rendering endpoints
- Celery-powered background sending for OTP, password reset, verification, welcome, and invitation emails

### 5. Images
- `Category` and `Image` models
- Single/multiple upload, update, delete, search, and pagination
- Server-side image validation (type, size)

### 6. Common / Core
- Generic pagination, filtering, searching, ordering mixins
- Standardized success/error response wrapper
- Centralized exception handling
- Audit fields (`created_at`, `updated_at`, `created_by`, `updated_by`) and soft-delete mixin on all models

---

## Getting Started

### Prerequisites

- Docker & Docker Compose (recommended), **or**
- Python 3.13+, Node.js 20+, PostgreSQL 15+, Redis 7+ (for local setup)

### Clone the repository

```bash
git clone <your-repo-url>
cd <project-folder>
```

---

## Environment Variables

Create `.env` files for both backend and frontend from the provided examples.

### Backend (`backend/.env`)

```env
# Django
DEBUG=True
SECRET_KEY=change-me
ALLOWED_HOSTS=localhost,127.0.0.1
DJANGO_SETTINGS_MODULE=core.settings.local

# Database
POSTGRES_DB=app_db
POSTGRES_USER=app_user
POSTGRES_PASSWORD=change-me
POSTGRES_HOST=db
POSTGRES_PORT=5432

# Redis / Celery
REDIS_URL=redis://redis:6379/0
CELERY_BROKER_URL=redis://redis:6379/1

# JWT
ACCESS_TOKEN_LIFETIME_MINUTES=15
REFRESH_TOKEN_LIFETIME_DAYS=7

# Email
EMAIL_HOST=smtp.example.com
EMAIL_PORT=587
EMAIL_HOST_USER=your-email@example.com
EMAIL_HOST_PASSWORD=change-me
EMAIL_USE_TLS=True
DEFAULT_FROM_EMAIL=no-reply@example.com

# CORS
CORS_ALLOWED_ORIGINS=http://localhost:3000
```

### Frontend (`frontend/.env.local`)

```env
NEXT_PUBLIC_API_BASE_URL=http://localhost:8000/api/v1
NEXTAUTH_SECRET=change-me
NEXTAUTH_URL=http://localhost:3000
```

---

## Running with Docker

```bash
docker compose up --build
```

This will spin up:

| Service | Description | Default Port |
|---|---|---|
| `backend` | Django + Gunicorn | 8000 |
| `frontend` | Next.js | 3000 |
| `db` | PostgreSQL | 5432 |
| `redis` | Redis | 6379 |
| `celery_worker` | Background task worker | — |
| `celery_beat` | Scheduled task runner | — |
| `nginx` | Reverse proxy | 80 |

Run migrations and create a superuser inside the running backend container:

```bash
docker compose exec backend python manage.py migrate
docker compose exec backend python manage.py createsuperuser
```

---

## Running Locally (Without Docker)

### Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements/local.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

In a separate terminal, run the Celery worker:

```bash
celery -A core worker -l info
celery -A core beat -l info
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

Visit `http://localhost:3000` for the app and `http://localhost:8000/api/docs` for the Swagger UI.

---

## API Documentation

Interactive API documentation is auto-generated via **drf-spectacular**:

- Swagger UI: `/api/docs/`
- ReDoc: `/api/redoc/`
- OpenAPI schema (JSON): `/api/schema/`

All endpoints support pagination, filtering, searching, and ordering via standard query parameters (`?page=`, `?search=`, `?ordering=`, and model-specific filters).

---

## Authentication & Authorization

- **JWT** access + refresh tokens issued on login
- Axios interceptor on the frontend automatically refreshes the access token on `401` responses
- **Role-based** and **permission-based** guards protect both API endpoints (DRF permission classes) and frontend routes/UI elements
- Account protection: login attempt tracking, account lock/block, OTP expiry, and activation/reset token expiry

---

## Standard API Response Format

Every API response follows a consistent envelope:

```json
{
  "success": true,
  "message": "User created successfully",
  "data": {},
  "errors": []
}
```

Error example:

```json
{
  "success": false,
  "message": "Validation failed",
  "data": null,
  "errors": [
    { "field": "email", "message": "This field is required." }
  ]
}
```

---

## Testing

### Backend

```bash
cd backend
pytest
# or
python manage.py test
```

Covers model tests, serializer tests, API/view tests, and permission tests per app.

### Frontend

```bash
cd frontend
npm run test
```

---

## Code Quality & Pre-commit

Backend code style is enforced via **Black**, **isort**, and **flake8**, wired into `pre-commit`:

```bash
pip install pre-commit
pre-commit install
pre-commit run --all-files
```

---

## Deployment Guide

1. Set `DEBUG=False` and configure `ALLOWED_HOSTS` in the production `.env`.
2. Use `requirements/production.txt` and the production `docker-compose.prod.yml`.
3. Collect static files: `python manage.py collectstatic --noinput`.
4. Run database migrations: `python manage.py migrate`.
5. Serve the backend behind **Gunicorn** with **Nginx** as a reverse proxy/TLS terminator.
6. Build the frontend for production: `npm run build && npm run start`, or serve via Nginx/Vercel.
7. Ensure Redis and Celery worker/beat services are running for background email tasks.
8. Configure environment secrets (JWT secret, DB credentials, SMTP credentials) via your hosting provider's secret manager — never commit `.env` files.

---

## Contributing

1. Fork the repository and create a feature branch: `git checkout -b feature/your-feature`
2. Follow the existing service/selector/repository pattern for new modules
3. Add tests for new functionality
4. Run `pre-commit run --all-files` before committing
5. Open a pull request with a clear description of the change

---

## License

This project template is provided as-is for use as a starting point in client and internal projects. Add your organization's license terms here.