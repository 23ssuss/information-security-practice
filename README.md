# Електронний деканат — Information Security Practice

Серверний застосунок «Електронний деканат» на FastAPI з RBAC-архітектурою.

## Запуск

```bash
docker compose up --build
```

API доступне за адресою: http://localhost:3010

## Міграції

```bash
# Створити міграцію
docker compose exec api alembic revision --autogenerate -m "description"

# Застосувати міграцію
docker compose exec api alembic upgrade head
```

## Seed-дані

```bash
docker compose exec api python -m app.seed
```

## Перевірка

- http://localhost:3010/ — головна сторінка
- http://localhost:3010/health — стан системи
