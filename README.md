# DMC-268 UI (Team 3)

Vite + React + TypeScript frontend for DMC-268 Team 3.

## Setup & Run

Requires Node 24 (`.nvmrc`) and pnpm 12 (`npm install -g pnpm@12.9.1`, or `corepack enable`).

```bash
pnpm install      # also installs the Husky git hooks
pnpm dev
```

## Quality checks

| Command                             | What it does                                                                     |
| ----------------------------------- | -------------------------------------------------------------------------------- |
| `pnpm lint`                         | ESLint (typescript-eslint strict, type-aware) + Stylelint, zero warnings allowed |
| `pnpm lint:fix`                     | same, auto-fixing what it can                                                    |
| `pnpm check-types`                  | `tsc --noEmit` (strict)                                                          |
| `pnpm format` / `pnpm format:check` | Prettier                                                                         |
| `pnpm build`                        | type-check + production build into `dist/`                                       |

Git hooks (Husky): **pre-commit** runs lint-staged (ESLint/Stylelint `--fix` + Prettier on staged files) and blocks the commit on errors; **pre-push** runs `check-types` and `lint`.
