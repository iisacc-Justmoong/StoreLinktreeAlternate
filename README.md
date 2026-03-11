# SvelteKit Project

This project has been migrated from plain Svelte + Vite to **SvelteKit**.

## Run

```bash
npm install
npm run dev
```

## Validate

```bash
npm run check
npm run build
```

## Structure

- `src/routes/+page.svelte`: main page
- `src/routes/+layout.svelte`: global layout (imports `src/app.css`)
- `src/app.html`: SvelteKit app template
- `static/`: static assets served from `/`
