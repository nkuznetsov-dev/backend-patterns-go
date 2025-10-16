# Backend Patterns — Go

Mini services to practice common backend patterns in Go:
- **REST `/users`** (clean structure, proper errors)
- **Middleware: rate limiting**
- **HTTP client** (timeouts, retries, backoff)
- **Background jobs** (cron/worker, graceful shutdown)

> Goal: компактные, изолированные примеры с понятным запуском и инженерным процессом.

---

## Tech stack
Go 1.22 · net/http / (router TBD) · context · logging · testing · Docker/Compose (later) · GitHub Actions (later)

---

## Structure (planned)

- backend-patterns-go/
  - patterns/
    - 01-rest-users/ — REST CRUD sample
      - cmd/
        - api/
      - internal/
        - handlers/
        - repo/
        - domain/
      - README.md
    - 02-middleware-rate-limit/ — request limiting
      - cmd/
        - api/
      - internal/
        - middleware/
      - README.md
    - 03-client-external-api/ — HTTP client with timeout/retry
      - cmd/
        - app/
      - internal/
        - client/
      - README.md
    - 04-background-jobs/ — cron/worker, graceful shutdown
      - cmd/
        - worker/
      - internal/
        - jobs/
      - README.md
  - .github/
    - workflows/ — CI (later)

**Convention**
- Каждая тема — отдельная папка в `patterns/NN-<slug>/` с собственным `README.md`.
- Общие утилиты по возможности держим рядом с примером (минимум общего кода).

---

## Run locally
_Запуск добавим после реализации первого паттерна._
```bash
# example (later)
go run ./patterns/01-rest-users/cmd/api


