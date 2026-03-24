# Hey, I'm Vlad

**Backend Developer** building scalable distributed systems and APIs.

Working with cryptocurrency platforms, fintech, and high-load applications. Author of [Vorq](https://github.com/baccaraaa/vorq) -- type-safe distributed task queue for TypeScript.

## Tech Stack

```
Backend       TypeScript, NestJS, Node.js, Python, FastAPI
Databases     PostgreSQL, Redis, MongoDB
Messaging     RabbitMQ, Redis Streams
ORM           Prisma, TypeORM, SQLAlchemy
Frontend      React, Next.js
Infra         Docker, Kubernetes, GitHub Actions
```

## Featured Projects

### [Vorq](https://github.com/baccaraaa/vorq) -- Distributed Task Queue

Type-safe task queue for TypeScript with compile-time workflow validation.

```ts
const pipeline = vorq
  .workflow<{ url: string }>("etl")
  .step("fetch", async (ctx) => {
    return { data: await fetchData(ctx.input.url) };
  })
  .step("transform", async (ctx) => {
    // ctx.results.fetch is fully typed at compile time
    return { rows: normalize(ctx.results.fetch.data) };
  })
  .build();
```

**4 packages** on npm | **175 tests** | Redis & RabbitMQ | NestJS integration

[![npm](https://img.shields.io/npm/v/@vorq/core?label=%40vorq%2Fcore)](https://www.npmjs.com/package/@vorq/core)

### [Task Manager](https://github.com/baccaraaa/TaskManager) -- REST API

Production-ready task management API on FastAPI with async architecture.

```bash
curl -X POST /api/v1/tasks/ -H "Authorization: Bearer <token>" \
  -d '{"title": "Deploy v2", "priority": "high", "project_id": 1}'
```

**FastAPI + PostgreSQL + Redis + Celery** | JWT auth | WebSocket | **131 tests**

## Experience

- Payment processing systems handling 100k+ daily requests
- Cryptocurrency trading bots and wallet infrastructure
- Telegram Mini Apps and bot automation
- Financial analytics platforms

## Contact

[![Telegram](https://img.shields.io/badge/Telegram-@notdaemon-26A5E4?logo=telegram&logoColor=white)](https://t.me/notdaemon)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-vladeveloper-0A66C2?logo=linkedin&logoColor=white)](https://linkedin.com/in/vladeveloper)
