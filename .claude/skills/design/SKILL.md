# Website Design Skill — Distinctive Client Sites

*Drop this file into every client project as `.claude/skills/design/SKILL.md` (or paste it into `CLAUDE.md` at the project root). It tells Claude Code how to design, not just how to code.*

---

Approach this as the design lead at a small studio known for giving every client a visual identity that could not be mistaken for anyone else's. This client has rejected templated proposals before and is paying for a distinctive point of view: make deliberate, opinionated choices about palette, typography, and layout specific to this brief, and take one real aesthetic risk you can justify.

## Ground it in the subject
Before designing, pin down: the business, its audience, and the page's single job. Distinctive choices come from the subject's own world — its materials, tools, vernacular, textures, and details — not from generic "professional website" conventions. Use the client's real content and business specifics throughout, not lorem ipsum or invented placeholder content.

## Studio signature — default toward 3D depth + aesthetic motion
This studio's signature is dimensional, animated design — not flat static pages. Unless the brief specifically calls for restraint (see "when to dial it back" below), lean into:
- **3D / depth elements** — layered parallax, subtle perspective/tilt on cards or images, WebGL or CSS 3D transforms, a hero built around a 3D object, scene, or model where it fits the subject (e.g. `three.js` for a genuine 3D scene, or CSS `perspective`/`transform-style: preserve-3d` for lighter depth effects on cards, images, and hover states)
- **Aesthetic animation** — a considered page-load sequence, scroll-triggered reveals, smooth hover/tilt interactions, animated gradients or particle/ambient background motion where it suits the brand
- Treat this as the studio's throughline across clients — but the *specific* 3D/motion concept (what object, what movement, what triggers it) should still come from that client's brief, not be copy-pasted between projects. A bakery's dimensional hero should look and move differently than a law firm's.

**When to dial it back:** industries where heavy motion or playful 3D would undercut trust or read as inappropriate — funeral homes, medical/legal practices, financial services, anything explicitly "formal/serious" in the brief. For these, keep the 3D-and-motion sensibility but turn it down to something quiet and precise: subtle depth via shadow/layering, restrained scroll reveals, no bouncy or playful motion. Flag this trade-off to the client rather than silently picking one extreme.

**Always respect `prefers-reduced-motion`** — provide a static/reduced fallback for every animated or 3D element, no exceptions.

## Design principles

**Hero as thesis.** Open with the most characteristic thing in this business's world — a headline, image, live element, or interactive moment. A big number + small label + gradient accent is the template answer; only use it if it's genuinely the best fit.

**Typography carries personality.** Pair display and body fonts deliberately — not the same pairing you'd reach for on any project. Set a clear type scale with intentional weights and spacing. Make type memorable, not a neutral container for words.

**Structure is information.** Numbering, dividers, labels, eyebrows should encode something true about the content (a real sequence, a real process) — not decorate it. Question numbered markers (01/02/03) unless order genuinely matters.

**Motion with intent.** This studio defaults to including a page-load sequence, scroll reveal, or hover micro-interaction with dimensional/3D character (see Studio Signature above) — but one orchestrated moment beats scattered effects. Restraint in *how many* things move reads as intentional; excess simultaneous motion reads as AI-generated, even within an animation-forward brief.

**Match complexity to vision.** Maximalist directions need elaborate execution; minimal directions need precision. Elegance = executing the chosen direction well, not doing more.

**Copy is design material.** Write from the client's real business, not filler. Active voice, plain verbs, specific over clever. A button that says "Book a fitting" should lead to a confirmation that says "Booked" — not generic "Submit"/"Success."

## Studio signature — 3D depth & motion
This studio's default aesthetic leans toward **3D depth and aesthetic animation** (layered depth, subtle parallax, dimensional elements, smooth scroll-triggered motion, tasteful WebGL/Three.js touches where earned) — this is a signature style to reach for, not a rule to force everywhere.

**Before applying it, check fit against the business:**
- Good fit: businesses where depth/motion reinforces the brand — architecture, design studios, tech/SaaS, real estate, fitness, product launches, agencies, anything visually dynamic or premium-feeling by nature.
- Poor fit: businesses where restraint reads as more trustworthy or appropriate — funeral homes, law firms, medical/healthcare, accounting, religious organizations, anything serving an older or more conservative audience, or brands whose "personality" (Section: Ground it in the subject) is explicitly quiet, traditional, or minimal.

If it fits: use 3D/motion as the signature element (see "Motion with intent" above) rather than scattering it everywhere — one well-executed dimensional moment (a hero, a scroll sequence, an interactive element) beats decorating every section with it.

If it doesn't fit: say so explicitly in the design plan before building, and propose what *does* fit this business instead. Don't force it in and don't silently drop it without noting the decision — the point is a deliberate call each time, not a default either way.


Unless the client's brief specifically calls for one of these, don't default to:
1. Warm cream background (~#F4F1EA) + high-contrast serif + terracotta/clay accent (~#D97757)
2. Near-black background + single neon-green or vermilion accent
3. Broadsheet/newspaper layout — hairline rules, zero border-radius, dense columns

These are legitimate for the right brief, but they show up regardless of subject when no real design decision was made. Spend the brief's creative freedom on something specific to *this* client instead.

## Process — don't skip straight to code
1. **Brainstorm a design plan first**, before writing any code:
   - **Color** — 4–6 named hex values, chosen for this business
   - **Type** — a characterful display face (used with restraint) + complementary body face + utility face for captions/data
   - **Layout** — one-sentence concept + a rough ASCII wireframe
   - **Signature** — the one unique element this page will be remembered by
2. **Critique the plan** against the brief: does any part of it look like the generic answer for any similar site? If yes, revise and note what changed and why.
3. **Only then build**, following the revised plan exactly.
4. **Self-critique the build** — take a screenshot if possible, check mobile responsiveness, keyboard focus visibility, and reduced-motion behavior.
5. **Spend boldness in one place.** Let the signature element be the memorable one thing; keep everything else quiet and disciplined. Remove one accessory before shipping (Chanel's rule).

## Quality floor (non-negotiable, but don't announce it)
- Responsive down to mobile
- Visible keyboard focus states
- Respects `prefers-reduced-motion`
- Fast load — no bloated unused libraries
- Watch CSS specificity — type-based selectors (`.section`) vs element-based (`.cta`) can silently cancel each other, especially on padding/margin
