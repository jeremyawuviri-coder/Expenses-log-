# Expense API — Build Plan

Target: 6 weeks, ~8-10 hrs/week. Adjust dates to your calendar.

## Milestone 1 — Foundations (Week 1)
- [ ] Repo created, git initialized, `.gitignore` in place
- [ ] uv/venv set up, dependencies installed, `requirements.txt` frozen
- [ ] Project folder structure created (app/, tests/, alembic/)
- [ ] `config.py`, `database.py`, `main.py` written
- [ ] `/health` endpoint returns `{"status":"ok"}`
- [ ] Swagger UI loads at `/docs`
- [ ] First commit pushed to GitHub

## Milestone 2 — Data Models (Week 2)
- [ ] `User`, `Group`, `GroupMember`, `Expense`, `ExpenseSplit` models written
- [ ] Alembic configured, first migration generated
- [ ] Migration applied (`alembic upgrade head`), tables exist in SQLite
- [ ] Pydantic schemas written for User, Group, Expense, Balance
- [ ] Commit + push

## Milestone 3 — Balance Engine (Week 3) ⭐
- [ ] `balance_engine.py` written (pure functions)
- [ ] Test file `test_balance_engine.py` written
- [ ] All engine tests pass (`pytest -v`)
- [ ] Committed — this is the "I have a working core" milestone
- [ ] (Stretch) Property-based test with `hypothesis`

## Milestone 4 — Auth (Week 4)
- [ ] `security.py`: password hashing + JWT create/verify
- [ ] `POST /auth/signup` — creates user, returns token
- [ ] `POST /auth/login` — validates creds, returns token
- [ ] `GET /users/me` — protected route using token dependency
- [ ] Auth tests pass
- [ ] Commit + push

## Milestone 5 — Groups & Expenses API (Week 5)
- [ ] Group CRUD endpoints (`POST/GET/PATCH/DELETE /groups`)
- [ ] Membership endpoints (`POST/DELETE /groups/{id}/members`)
- [ ] Expense create endpoint (validates splits via Pydantic)
- [ ] Expense list endpoint with pagination
- [ ] `/groups/{id}/balances` and `/groups/{id}/settlements` wired to engine
- [ ] Endpoint tests pass
- [ ] Commit + push

## Milestone 6 — Polish & Ship (Week 6)
- [ ] Error handling: consistent JSON error shape
- [ ] `Dockerfile` + `docker-compose.yml` (API + Postgres)
- [ ] GitHub Actions: `.github/workflows/test.yml` runs pytest on push
- [ ] Deployed to Fly.io / Railway / Render
- [ ] Seed script (`scripts/seed.py`) populates demo data
- [ ] `README.md` complete: what/why, architecture diagram, endpoints, run instructions, live link
- [ ] Tag `v1.0` and share the link
