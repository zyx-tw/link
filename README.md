# link

A URL shortener at link.zyx.tw: paste a URL, get a short code, and the code redirects to the URL.

## Development

```sh
bun install
cp .env.example .env.local   # set DATABASE_URL
bun run dev
```

The table is in `db/schema.sql`.

## Checks

```sh
bun run typecheck && bun run lint && bun run format:check
```

## Deploy

ci builds the image in the pull request; a merge to main ships it to VM 117 through land (`.github/workflows/release.yml`). The stack lives in `/opt/link` with `compose.yaml` and `.env` (see `.env.example`).

## License

MIT
