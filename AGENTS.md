# AGENTS

Next.js template with the App Router in `app/` and the Pages Router in `pages/`. [README.md](README.md) covers setup and commands.

## Source

- `app/`: home page, layout, metadata routes (`manifest`, `robots`, `sitemap`).
- `pages/`: `api/index.ts`, `oauth.tsx`, and the `_app` and `_document` shells.
- `common/`: constants, hooks, API queries (`queries.ts`), server helpers (`server.ts`), utilities.
- `components/`: layouts, providers, modal context.
- `modules/`: vendored AES, cookie, and CORS code.
- `global.css`, `animations.css`: global styles, imported by both routers.

## Conventions

- Import through the `tsconfig.json` aliases, such as `@common/*`, `@components/*`, and `@modules/*`.
- Follow `.prettierrc`. Prettier is not a dependency, so nothing enforces it.
- `package-lock.json` and `next-env.d.ts` are generated and gitignored.
- `/api` and `/oauth` need `API_AES_KEY` and `API_IV_KEY` in `.env`. See `common/server.ts`.
- ESLint is not installed: `eslint-config-next` depends on `typescript-eslint`, which does not support TypeScript 7 yet.

## Verification

There is no test suite. `npm run build` compiles the app and type-checks it with the local `tsc`. `npm audit` and `npm outdated` report dependency state.

## Skills

This repository has no skills yet. Add one only for a repeated workflow, and record its location here.

<!-- BEGIN:nextjs-agent-rules -->

## This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` (resolved from this file's directory; in monorepos the `next` package may not be visible from the repo root) before writing any code. Heed deprecation notices.

This block is written and re-added by `next dev` — verify at `node_modules/next/dist/server/lib/generate-agent-files.js`. Removing it from a diff only re-creates the uncommitted change; committing it with your work keeps the tree clean.

<!-- END:nextjs-agent-rules -->
