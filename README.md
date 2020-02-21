# Async FastAPI-based application

- NoSQL support (motor asyncio)
- Pydantic-based models
- Fast

## Installation

Run using docker to checkout mongo support

```
cp -rv env.example .env  # populate with your own values
docker-compose up -d
```

## Routes

### Static files

The `nginx` service serves both static files from the front and backend.

Add staticfiles for
- frontend: to the `rollup` build process OR to
`frontend/dist/`
- backend: to `backend/static`

### API

The `backend` service is to be accessed from the frontend using `/api` prefix.

Thus any backend routes are now `/api/route-to-be-accessed`. Because of this,
the API docs are hosted at `/api/docs`.

### DB Interface

For easy debugging purposes, there is an express mongodb interface provided at
`/db_interface/`.
