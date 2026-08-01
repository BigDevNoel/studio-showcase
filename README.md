# studio-showcase

A monorepo holding 6 independent demo websites for a portfolio: 5 fictional
business sites plus a hub/landing page that links to all of them.

```
studio-showcase/
├── carpentry/      — fictional carpentry business
├── hairsalon/       — fictional hair salon
├── gym/              — fictional gym
├── architecture/     — fictional architecture firm
├── clinic/           — fictional clinic
└── hub/               — landing page linking to the 5 sites above
```

## How this repo is organized

Each of the 6 folders is a **fully self-contained, independent Astro +
Tailwind CSS project** — its own `package.json`, `astro.config.mjs`,
`tsconfig.json`, `src/`, etc. There is nothing shared between them and no
root-level `package.json` for the sites themselves.

## Deploying

Each site deploys **independently on Vercel**. For each folder, create a
separate Vercel project pointed at this repo, and set its **Root Directory**
to the corresponding folder (e.g. `carpentry`, `hub`). Vercel will detect
Astro automatically and run `npm install` / `npm run build` scoped to that
subdirectory.

## Local development

From inside any project folder:

```bash
cd carpentry        # or hairsalon, gym, architecture, clinic, hub
npm install
npm run dev
```

## Stack

- [Astro](https://astro.build) 7
- [Tailwind CSS](https://tailwindcss.com) 4 (via `@tailwindcss/vite`)

## Status

Scaffolding only — each site currently shows a placeholder homepage
("[Business] — coming soon"). Designs and content are built out per-folder
next.
