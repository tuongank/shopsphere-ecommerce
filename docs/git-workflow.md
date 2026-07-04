# Git Workflow Guide

## Branches

| Branch | Purpose |
|---|---|
| `main` | Stable branch. Only reviewed, tested code should be merged here. |
| `develop` | Integration branch. All feature branches should merge here first. |
| `feature/*` | New features. Example: `feature/auth-register`. |
| `bugfix/*` | Bug fixes during development. |
| `hotfix/*` | Urgent fixes from `main`. |

## Developer Flow

1. Pick an issue from GitHub Project.
2. Move it to `In Progress`.
3. Create a branch from `develop`.
4. Code only the scope of that issue.
5. Commit using Conventional Commits.
6. Push branch.
7. Create Pull Request into `develop`.
8. Wait for review.
9. Fix requested changes if any.
10. Merge only after approval.

## Branch Naming

```text
feature/auth-register
feature/auth-login-jwt
feature/category-crud
feature/product-search-filter
bugfix/cart-quantity-validation
hotfix/fix-login-token-expiry
```

## Commit Examples

```text
feat(auth): add customer register API
feat(auth): add JWT login API
fix(cart): prevent adding inactive product
refactor(order): extract status transition validator
docs(git): add branch workflow guide
test(voucher): add expired voucher test
```

## Pull Request Rules

- Never push directly to `main` or `develop`.
- One Pull Request should solve one issue.
- Pull Request title should be clear.
- Pull Request must link to its issue.
- Pull Request must include test evidence.
- Do not commit `.env`, secrets, build artifacts, or IDE files.
