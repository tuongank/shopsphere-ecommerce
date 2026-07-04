# ShopSphere - E-commerce Backend System

ShopSphere is a learning-focused e-commerce backend system designed to simulate real-world software development workflows, including Git branching, pull requests, code review, role-based access control, order lifecycle management, inventory tracking, voucher validation, and payment simulation.

## Goals

- Practice GitHub workflow like a real engineering team.
- Build a realistic e-commerce backend system for junior developer interviews.
- Learn how to split requirements into GitHub Issues.
- Practice feature branches, commits, pull requests, and code review.
- Apply clean code, layered architecture, validation, and business rules.

## Roles

- `CUSTOMER`: buys products, manages cart, places orders, reviews products.
- `STAFF`: handles orders, shipping, reviews, and operational workflows.
- `ADMIN`: manages users, products, inventory, vouchers, dashboard, and audit logs.

## Roadmap

| Phase | Name | Goal |
|---:|---|---|
| 0 | Project Setup & GitHub Workflow | Repository, docs, branching, templates, CI |
| 1 | Auth, Authorization & User Management | Login, JWT, roles, permissions, user management |
| 2 | Product Catalog Management | Category, product, variant, search/filter/sort |
| 3 | Inventory, Cart & Wishlist | Stock tracking, cart, wishlist |
| 4 | Voucher, Checkout & Order Lifecycle | Voucher, checkout, order status flow |
| 5 | Payment, Shipping & Notification | Mock payment, webhook, shipping, notification |
| 6 | Review, Return/Refund & Dashboard | Review, return/refund, admin reporting |
| 7 | Audit Log, Testing & Production Readiness | Audit log, tests, docs, CI/CD polish |

## Git Workflow

Main branches:

- `main`: stable production-ready branch.
- `develop`: integration branch for active development.
- `feature/*`: feature branches created from `develop`.
- `bugfix/*`: bug fix branches created from `develop`.
- `hotfix/*`: urgent fixes created from `main`.

Feature flow:

```bash
git checkout develop
git pull origin develop
git checkout -b feature/auth-register

# code...

git add .
git commit -m "feat(auth): add register API"
git push origin feature/auth-register
```

Then create a Pull Request into `develop`.

## Commit Convention

Use Conventional Commits:

```text
feat(auth): add register API
fix(auth): handle invalid credentials
refactor(order): extract order status validation
docs(readme): add setup guide
test(order): add checkout transaction tests
chore(ci): add GitHub Actions workflow
```

## Local Setup

This section should be updated after the backend stack is selected.

Expected files:

- `.env.example`
- `docker-compose.yml`
- database migration scripts
- seed data scripts

## Demo Accounts

```text
Admin: admin@example.com / Admin@123
Staff: staff@example.com / Staff@123
Customer: customer@example.com / Customer@123
```

## Project Board Columns

- Backlog
- Ready
- In Progress
- In Review
- Changes Requested
- Done

## Backend:
- Java 17+
- Spring Boot 3.x
- Spring Web
- Spring Data JPA
- Spring Security
- MySQL
- Maven
- Docker Compose
- Lombok
- Validation
- JWT
- Swagger/OpenAPI
- JUnit 5