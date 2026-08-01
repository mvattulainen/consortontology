# CONSORT 2025 Guideline Ontology

This repository publishes the CONSORT 2025 guideline ontology as a Quartz site.

- Website: https://mvattulainen.github.io/consortontology/
- Start page: `content/index.md`
- Quartz configuration: `quartz.config.yaml`

## Local preview

Requires Node.js 22 or later.

```text
npm ci
npx quartz plugin install --from-config
npm run install-plugins
npx quartz build --serve
```

Pushing to `main` triggers the GitHub Pages deployment workflow.
