# studio-showcase

This is a monorepo of independent demo websites for my freelance web design portfolio.
Each subfolder is a self-contained Astro + Tailwind project, deployed separately on
Vercel (Root Directory set per subfolder). Nothing is shared between subfolders except
the skills in `.claude/skills/`.

## Structure
- `carpentry/`, `hairsalon/`, `gym/`, `architecture/`, `clinic/` — invented-but-realistic
  demo business sites, each showcasing a different aesthetic direction
- `hub/` — my portfolio landing page linking to all 5 demos

## Design differentiation — read this before designing any site
Before proposing a design plan for any subfolder, check the other subfolders in this repo
(read their `src/` files — colors, fonts, layout structure) to see what's already been
built. Each site (`carpentry`, `hairsalon`, `gym`, `architecture`, `clinic`) must have a
genuinely distinct design from every other one already built:
- A different hue family for the palette — not a shade, tint, or filtered variation of a
  palette already used elsewhere in this repo
- A different type category pairing — if a sibling site used a serif, don't reach for
  another serif; if a sibling used a soft/rounded sans, this one should feel structurally
  different, not just recolored
- A distinct layout approach and signature animation moment, not a reskin of a sibling's

This still must follow `.claude/skills/design/SKILL.md`'s anti-generic rule — the goal is
never "different from siblings but generic," it's "specific to this business AND distinct
from what's already built here." If checking siblings reveals every "obvious" direction
for this business is already taken, dig for a second-order idea that's still true to the
business rather than settling for something arbitrary just to be different.

State in the design plan which sibling sites you checked and how this one diverges from
each, before building.

## Rules for every demo site
- Always follow `.claude/skills/design/SKILL.md` and `.claude/skills/stack-marketing/SKILL.md`
- Every site needs a business that's invented but reads as completely real — no lorem
  ipsum, no generic "Acme Co." naming, real-feeling copy
- Every site needs real 3D depth / aesthetic animation, but it must be specific to that
  business's world, not a generic decorative effect
- Photos and video (where used) must be sharp, high-quality, and specific to the business
  — sourced from free-license libraries (Pexels, Unsplash, Pixabay, Mixkit, Coverr),
  optimized for load speed
- Never touch a sibling subfolder while working inside one — each project is independent
- Small footer disclosure required on every demo: "Concept site by [Your Name] · not a
  real business"

## Not covered here
- `hub/` is the exception to most of the above — it's my real portfolio page, should be
  fast and clean rather than animation-heavy, see separate instructions when building it
