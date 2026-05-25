# 21.gifts — website

Static landing page for [21.gifts](https://21.gifts) — peer-to-peer Bitcoin
Lightning gifts with NOSTR as the invisible communication substrate.

The application itself lives at [`21gifts/app`](https://github.com/21gifts/app),
the backend at [`21gifts/api`](https://github.com/21gifts/api), and the project
concept (vision, architecture, decisions) is documented in
[`21gifts/api/CONCEPT.md`](https://github.com/21gifts/api/blob/develop/CONCEPT.md).

## Tech stack

Pure HTML + CSS. No frameworks, no build step. The only dev dependency is
Prettier for formatting.

## Languages

English only. Internationalization is out of scope for v1.

## Local development

```bash
npm install            # installs prettier
npx serve .            # any static server works
```

## Format

```bash
npm run format         # write
npm run format:check   # the same gate CI runs
```

## Deploy targets

| Branch    | Cloudflare Pages target | URL                    |
| --------- | ----------------------- | ---------------------- |
| `develop` | `21gifts-website` / dev | `https://dev.21.gifts` |
| `main`    | `21gifts-website` / prd | `https://21.gifts`     |

CI checks Prettier on every push and pull request. Deploys are automatic:
`develop` → DEV, `main` → PRD.

## License

[MIT](LICENSE)
