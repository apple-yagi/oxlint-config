# @apple-yagi/oxlint-config

Opinionated Oxlint config for TypeScript and React projects.

## Installation

```bash
pnpm add -D @apple-yagi/oxlint-config oxlint oxlint-tsgolint
```

`oxlint-tsgolint` is required because this preset enables many `typescript/*` rules.

## Usage

Create `.oxlintrc.json`:

```json
{
  "$schema": "./node_modules/oxlint/configuration_schema.json",
  "extends": ["./node_modules/@apple-yagi/oxlint-config/.oxlintrc.json"]
}
```

Then run:

```bash
oxlint .
```

## Philosophy

- Prefer correctness-focused rules.
- Enable type-aware linting by default (`typeAware: true`, `typeCheck: true`).
- Keep React and import rules strict to prevent common production issues.

## Included Plugins

- `oxc`
- `eslint`
- `typescript`
- `jsx-a11y`
- `import`
- `promise`
- `react`
- `react-perf`
- `unicorn`
- `jest`
- `vitest`
