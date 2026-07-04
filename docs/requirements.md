# Requirements

## Phase 0: Project Setup & GitHub Workflow

### Goal

Create a professional repository structure and collaboration workflow.

### Requirements

- Create `main` and `develop` branches.
- Add README.
- Add Git workflow documentation.
- Add Pull Request template.
- Add Issue templates.
- Add `.gitignore`.
- Add `.env.example`.
- Add initial GitHub Actions workflow.
- Define labels and milestones.

## Phase 1: Auth, Authorization & User Management

### Goal

Implement authentication, JWT-based authorization, and role-based permissions for `CUSTOMER`, `STAFF`, and `ADMIN`.

### Features

- Customer registration.
- Login with JWT.
- Get current user profile.
- Change password.
- Admin creates staff account.
- Admin locks/unlocks user.
- Role-based API protection.

### Business Rules

- Email must be unique.
- Password must be hashed.
- Locked users cannot log in.
- Customer cannot call staff/admin APIs.
- Staff cannot manage users or roles.
- Admin can manage customers and staff.
