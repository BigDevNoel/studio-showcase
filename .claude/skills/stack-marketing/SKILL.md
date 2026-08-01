# Stack Skill — Marketing / Business Websites

*Drop into `.claude/skills/stack-marketing/SKILL.md` for projects that are informational sites — no login, no user data, no persistent app state. Home, About, Services, Contact, Portfolio, Blog, etc.*

---

## Default stack
- **Framework:** Astro. Ships near-zero JS by default, fast by default, add interactive "islands" only where actually needed (a form, a filter, a carousel).
  - Exception: for a genuinely simple 3–5 page site with no interactivity beyond a contact form, plain HTML/CSS/JS is fine and easier to hand off to a non-technical future maintainer.
- **Styling:** Tailwind CSS.
- **Forms:** Formspree, or a lightweight serverless function if the client wants submissions routed somewhere specific (e.g. a CRM webhook).
- **Images:** Astro's built-in image optimization (`astro:assets`) — don't ship unoptimized full-res images.
- **Hosting:** Vercel, Netlify, or Cloudflare Pages — pick based on client preference; all are free-tier friendly with auto SSL and simple custom domain setup.
- **Analytics:** Google Analytics or Plausible, added only if the client asked for it — don't add tracking by default.
- **CMS (only if requested):** If the client wants to self-edit content post-launch, use a lightweight approach — Astro content collections with markdown files (client edits via GitHub, or a simple admin like Decap CMS) rather than standing up a full headless CMS unless the site is large enough to justify it.

## Project structure
```
src/
  components/     # reusable UI pieces (Nav, Footer, Card, etc.)
  layouts/        # page shells
  pages/          # one file per route
  styles/         # global.css, Tailwind config
public/
  images/
```

## Non-negotiables
- Mobile responsive down to ~375px width
- Lighthouse performance score should be high by default — this is Astro's whole point, don't undermine it with heavy unnecessary JS libraries
- Real `<meta>` tags (title, description, OG image) per page, not boilerplate placeholders
- Semantic HTML (`<nav>`, `<main>`, `<footer>`, proper heading hierarchy) — helps both SEO and accessibility
- No backend/database unless the brief explicitly needs one — if a request starts needing persistent data or user accounts, flag that this has become an app-scope project, not a marketing-site one (see `stack-app` skill)
