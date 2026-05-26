# TypeScript-Skeleton

A starting point for a TypeScript library. Fork or use this repository's "Use this template" button to start a new project.

## What you get

- **bun** for install / test / dev (`bun install`, `bun test`, `bun run dev`).
- **tsc** for the actual build to `dist/` (ESM, full `.d.ts` + sourcemaps).
- **prettier** for formatting.
- Sample `src/index.ts` + `src/index.test.ts` using `bun:test`.
- GitHub Actions CI matrix and a publish workflow that uses npm Trusted Publishing on tag push.
- Dependabot config with `@types/node` major bumps suppressed (stay on the LTS line).

## First steps after forking

1. Rename the package:
   ```sh
   # Edit package.json: set "name", "description", and the repository URL.
   ```
2. Replace `src/index.ts` with your real exports. Update `src/index.test.ts` to match.
3. Update this README.
4. To enable publishing:
   - Pick a name on npm. If it doesn't exist yet you'll need to scope it (e.g. `@your-user/your-name`).
   - Push a first release locally (`bun run build && npm publish --access public`) to create the package on npm. (See "Bootstrap publish" below.)
   - Configure npm Trusted Publishing on the package's access page: GitHub Actions / your-user / your-repo / `publish.yml` / (blank environment).
   - Tag `v*` and push — CI publishes with `--provenance`.

## Scripts

| Command | What it does |
| --- | --- |
| `bun install` | Install dependencies. |
| `bun run dev` | Watch + execute `src/index.ts` (handy for iteration). |
| `bun test` | Run all `*.test.ts` files via the bun test runner. |
| `bun run build` | Compile TypeScript to `dist/`. |
| `bun run lint` | Type-check without emitting. |
| `bun run format` | Format with prettier. |

## Bootstrap publish

npm Trusted Publishing's per-package configuration page only exists once the package itself exists. For a brand-new package:

```sh
bun run build
npm publish --access public
```

(One-time. After this, configure trusted publishing on npmjs.com and let CI handle every subsequent version via tag pushes.)

## Requirements

- Bun >= 1.2 (https://bun.sh).
- The compiled output runs on Node.js 22+ / Bun / Deno (depending on what APIs you use).

## License

MIT.
