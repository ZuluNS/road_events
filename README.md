# road_events
## Overview

This Sports Events Management System provides a full-featured backend API for:

- **Authentication & User Management** — Secure JWT-based authentication with refresh tokens, password reset, and role assignment.
- **Event Management** — Create, update, and manage sports events with categories, schedules, and participant limits.
- **Event Enrolment** — Allow athletes to register for events with status tracking (pending, approved, rejected, waitlisted, checked-in).
- **Categories** — Organize events into hierarchical sport categories.
- **Organizers** — Dedicated profiles for event organizers with dashboard analytics.
- **Results & Leaderboards** — Record and publish event results with global leaderboard support.
- ## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Database Setup](#database-setup)
- [Running the Application](#running-the-application)
- [Project Structure](#project-structure)
- [API Documentation](#api-documentation)
- [Authentication & Authorization](#authentication--authorization)
- [Role-Based Access Control](#role-based-access-control)
- [Environment Variables](#environment-variables)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

- ## Tech Stack

| Layer | Technology |
| --- | --- |
| **Framework** | ASP.NET Core 8.0+ |
| **Language** | C# 12 |
| **ORM** | Entity Framework Core |
| **Database** | SQL Server / PostgreSQL |
| **Authentication** | ASP.NET Core Identity + JWT Bearer |
| **Documentation** | Swagger / OpenAPI |
| **Testing** | xUnit, Moq, FluentAssertions |
| **Logging** | Serilog |
| **Mapping** | AutoMapper |

## Project Plan Fles
ERD AND SQL
[Prog_poe1.pdf](https://github.com/user-attachments/files/31848653/Prog_poe1.pdf)

## Role-Based Access Control

| Role | Permissions |
| --- | --- |
| **Public** | View events, categories, organizers, published results |
| **Athlete** | Enrol in events, manage own profile, view own enrolments |
| **Organizer** | Create/manage own events, manage enrolments for own events, submit results, view organizer dashboard |
| **Admin** | Full system access — manage users, all events, all enrolments, categories, organizers, and results |

Role checks are enforced via `[Authorize(Roles = "...")]` attributes on controllers and actions.

## Environment Variables

Create a `.env` file or set the following environment variables:

| Variable | Description | Example |
| --- | --- | --- |
| `ASPNETCORE_ENVIRONMENT` | Runtime environment | `Development` |
| `ConnectionStrings__DefaultConnection` | Database connection string | `Server=...` |
| `JwtSettings__Secret` | JWT signing secret | `your-secret-key` |
| `JwtSettings__Issuer` | Token issuer | `SportsEventsApi` |
| `JwtSettings__Audience` | Token audience | `SportsEventsClient` |
| `EmailSettings__SmtpServer` | SMTP server for notifications | `smtp.gmail.com` |
| `EmailSettings__FromAddress` | Sender email address | `noreply@sportsevents.com` |

- 
## Features

| Feature | Description |
| --- | --- |
| 🔐 JWT Authentication | Secure token-based auth with refresh token rotation |
| 👥 Role-Based Access | Public, Athlete, Organizer, and Admin roles |
| 📅 Event Scheduling | Full CRUD for events with date ranges and registration deadlines |
| 🏷️ Category System | Hierarchical sport categories |
| 📝 Enrolment Workflow | Multi-status enrolment with approval and check-in |
| 📊 Results & Rankings | Result recording with leaderboard aggregation |
| 📄 Pagination & Filtering | Consistent pagination and query filtering across endpoints |
| 🛡️ Input Validation | FluentValidation / Data Annotations on all DTOs |
| 🧪 Unit & Integration Tests | xUnit test coverage for core services |

## Getting Started
## API Documentation

The API is organized into the following functional modules:

| Module | Base Route | Description |
| --- | --- | --- |
| Authentication | `/api/auth` | Login, register, refresh tokens, password reset |
| User Profiles | `/api/users` | Profile management and role assignment |
| Events | `/api/events` | Event CRUD, filtering, and upcoming events |
| Categories | `/api/categories` | Sport category management |
| Enrolments | `/api/enrolments` | Event registration and status management |
| Organizers | `/api/organizers` | Organizer profiles and dashboards |
| Results | `/api/results` | Result submission and leaderboards |

### Prerequisites

- [.NET 8.0 SDK](https://dotnet.microsoft.com/download) or later
- [SQL Server](https://www.microsoft.com/en-us/sql-server) or [PostgreSQL](https://www.postgresql.org/)
- [Git](https://git-scm.com/)
- (Optional) [Docker](https://www.docker.com/) for containerized deployment

## License

This project is licensed under the **MIT License**.

See [LICENSE](LICENSE) for details.

---

## Support

For questions, issues, or feature requests, please open an issue on GitHub or contact the development team.
