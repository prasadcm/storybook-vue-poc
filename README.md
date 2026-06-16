# Storybook Vue 3 — GitHub Pages Sample

A sample project demonstrating how to build and host a [Storybook](https://storybook.js.org/) for a Vue 3 + TypeScript + Vite app on [GitHub Pages](https://pages.github.com/) using GitHub Actions.

Live: [prasadcm.github.io/storybook-vue-poc](https://prasadcm.github.io/storybook-vue-poc/)

## Stack

- [Vue 3](https://vuejs.org/) with `<script setup>` SFCs
- [TypeScript](https://www.typescriptlang.org/)
- [Vite](https://vitejs.dev/)
- [Storybook 10](https://storybook.js.org/)

## Local development

```bash
npm install

# Run the Vite dev server
npm run dev

# Run Storybook locally (http://localhost:6006)
npm run storybook
```

## Building Storybook

```bash
npm run build-storybook
```

Output is written to `storybook-static/`.

## Deployment

Storybook is automatically deployed to GitHub Pages on every push to `main` via the workflow at [.github/workflows/deploy.yml](.github/workflows/deploy.yml).

The workflow:

1. Checks out the repo
2. Installs dependencies with `npm ci`
3. Builds Storybook with `npm run build-storybook`
4. Uploads `storybook-static/` as a Pages artifact
5. Deploys it to GitHub Pages
