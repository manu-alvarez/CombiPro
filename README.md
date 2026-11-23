# CombiPro — standalone application

CombiPro is a React/Vite frontend for exploring sports odds and generating combinations. Its numerical outputs are estimates, not guarantees of winning.

## Source and current acceptance

This repository was initialized from the application source in [MSBrossAI/apps/combipro](https://github.com/manu-alvarez/MSBrossAI/tree/1e37070fa51f660b0966d4d14a1d1e78e453d082/apps/combipro), pinned to commit `1e37070fa51f660b0966d4d14a1d1e78e453d082`. A different, non-typechecking version also exists in `SERVER-DEV/apps/combipro`; do not synchronize it blindly.

The imported application builds without a backend, but live market data requires a valid external odds API key and network access. The app sends that key to the upstream odds API directly from the user's browser; it is not a server-side secret store. Do not enter a privileged/shared production key.

## Local development

Requires Node.js 22 and npm.

```bash
npm ci
npm run typecheck
npm run dev
```

Production build: `npm run build`. No automatic deployment is configured in this repository.

## Acceptance gates

- [x] Reproducible source import and Vite build on GitHub Actions.
- [ ] TypeScript checks on the independent repository.
- [ ] Browser functional acceptance with representative API data, empty API responses and error conditions.
- [ ] Review key handling, API availability and deployment paths.
- [ ] Identify canonical ownership and retire duplicated maintenance without breaking existing deployments.

Do not describe the project as production-ready until these gates are verified. Full account-wide tracker: [GitHub 35](https://github.com/manu-alvarez/manu-alvarez.github.io/blob/main/docs/GITHUB-35-CHECKLIST.md).
