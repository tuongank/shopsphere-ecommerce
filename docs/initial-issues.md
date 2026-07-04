# Initial GitHub Issues

## Phase 0

### SETUP-001: Initialize repository documentation

Labels: `phase: setup`, `type: docs`, `difficulty: easy`

Acceptance Criteria:

- [ ] README exists.
- [ ] Roadmap is documented.
- [ ] Roles are documented.
- [ ] Local setup section exists.

### SETUP-002: Add Git workflow guide

Labels: `phase: setup`, `type: docs`, `difficulty: easy`

Acceptance Criteria:

- [ ] Branch strategy is documented.
- [ ] Commit convention is documented.
- [ ] Pull Request flow is documented.
- [ ] Intern can follow the guide to create a feature branch.

### SETUP-003: Add GitHub Pull Request template

Labels: `phase: setup`, `type: chore`, `difficulty: easy`

Acceptance Criteria:

- [ ] `.github/pull_request_template.md` exists.
- [ ] Template includes related issue, test evidence, checklist.
- [ ] Template reminds developer not to commit secrets.

### SETUP-004: Add Issue templates

Labels: `phase: setup`, `type: chore`, `difficulty: easy`

Acceptance Criteria:

- [ ] Feature request template exists.
- [ ] Bug report template exists.
- [ ] Feature template includes requirements, API design, validation, business rules, acceptance criteria.

### SETUP-005: Add environment and Docker base setup

Labels: `phase: setup`, `type: chore`, `difficulty: medium`

Acceptance Criteria:

- [ ] `.env.example` exists.
- [ ] `docker-compose.yml` includes PostgreSQL.
- [ ] `.env` is ignored by Git.

### SETUP-006: Add placeholder CI workflow

Labels: `phase: setup`, `type: chore`, `difficulty: medium`

Acceptance Criteria:

- [ ] GitHub Actions workflow exists.
- [ ] CI runs on PR to `develop` and `main`.
- [ ] CI validates basic repository structure.

## Phase 1

### AUTH-001: Implement customer register API

Labels: `phase: auth`, `module: auth`, `type: feature`, `difficulty: medium`

Acceptance Criteria:

- [ ] Customer can register with full name, email, and password.
- [ ] Email must be unique.
- [ ] Password must be hashed.
- [ ] New customer has role `CUSTOMER`.
- [ ] Response does not include password or password hash.
- [ ] Invalid input returns 400.
- [ ] Duplicate email returns 409.

### AUTH-002: Implement login API with JWT

Labels: `phase: auth`, `module: auth`, `type: feature`, `difficulty: hard`

Acceptance Criteria:

- [ ] User can login with email and password.
- [ ] Valid login returns JWT access token.
- [ ] Invalid credentials return 401.
- [ ] Locked user cannot login.
- [ ] Token contains user id, email, and role.
- [ ] JWT secret is not hard-coded.

### AUTH-003: Implement get current user API

Labels: `phase: auth`, `module: auth`, `type: feature`, `difficulty: easy`

Acceptance Criteria:

- [ ] Authenticated user can get own profile.
- [ ] Unauthenticated request returns 401.
- [ ] Response does not include sensitive data.

### AUTH-004: Implement role-based authorization

Labels: `phase: auth`, `module: auth`, `type: feature`, `difficulty: hard`

Acceptance Criteria:

- [ ] Public APIs are accessible without token.
- [ ] Protected APIs require token.
- [ ] Customer cannot call staff/admin APIs.
- [ ] Staff cannot call admin-only APIs.
- [ ] Admin can call admin APIs.

### USER-001: Admin creates staff account

Labels: `phase: auth`, `module: user`, `type: feature`, `difficulty: medium`

Acceptance Criteria:

- [ ] Admin can create staff account.
- [ ] Staff email must be unique.
- [ ] Password must be hashed.
- [ ] Non-admin users cannot create staff.

### USER-002: Admin locks and unlocks user

Labels: `phase: auth`, `module: user`, `type: feature`, `difficulty: medium`

Acceptance Criteria:

- [ ] Admin can lock customer/staff account.
- [ ] Admin can unlock customer/staff account.
- [ ] Locked user cannot login.
- [ ] Staff cannot lock/unlock users.
