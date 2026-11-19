# Groupie Tracker

Groupie Tracker is a Go web application that fetches a public artists/concerts API and displays artist, member, album, location, date and relation data in a user-friendly website.

**Status:** the first milestone is complete. The current implementation includes the data and server foundation: API fetching, normalized in-memory catalog data, basic route rendering, search JSON, static assets, health checks, and shared error handling.

## Run

```bash
go run .
```

The server listens on `http://localhost:8080` by default. Set `PORT` to use another port:

```bash
PORT=3000 go run .
```

## Test

```bash
go test ./...
gofmt -w .
```

The project uses only Go standard library packages.

## Routes

- `/` - catalog home page
- `/artist/{id}` - artist detail page
- `/api/search?q=...` - JSON search endpoint
- `/healthz` - health check
- `/static/*` - embedded static assets

## Documentation

- `docs/PRD.md`: product requirements and acceptance cases
- `docs/architecture.md`: packages, routing and the full planned design. The
  async search worker and richer UI described there were planned for the next
  milestone and are not implemented yet.
