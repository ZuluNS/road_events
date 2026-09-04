# road_events
## Overview

This Sports Events Management System provides a full-featured backend API for:

- **Authentication & User Management** — Secure JWT-based authentication with refresh tokens, password reset, and role assignment.
- **Event Management** — Create, update, and manage sports events with categories, schedules, and participant limits.
- **Event Enrolment** — Allow athletes to register for events with status tracking (pending, approved, rejected, waitlisted, checked-in).
- **Categories** — Organize events into hierarchical sport categories.
- **Organizers** — Dedicated profiles for event organizers with dashboard analytics.
- **Results & Leaderboards** — Record and publish event results with global leaderboard support.
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

## License

This project is licensed under the **MIT License**.

See [LICENSE](LICENSE) for details.

---

## Support

For questions, issues, or feature requests, please open an issue on GitHub or contact the development team.
