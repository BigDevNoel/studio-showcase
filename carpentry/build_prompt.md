I'm building a portfolio piece — a website for an invented funiture makers(classy beds, cupboards, chairs etc), as if it were
a real, currently-operating local business. This is for my own portfolio, but it needs to
look and feel completely real and professional, not like a demo, template, or AI-generated
site.

BUSINESS DETAILS
Invent a specific, plausible business name (not generic — avoid anything that sounds like
"Acme" or "Business Co."), a real-sounding address/neighborhood, a believable backstory
(how long they've been open, what they specialize in), and realistic pricing for this type
of business in a mid-size city. Write all copy like a professional copywriter working for
a real client — specific, concrete, no filler ("passionate about quality" with nothing
backing it up is banned). No lorem ipsum anywhere.

DESIGN DIRECTION
Follow the design skill in `.claude/skills/design/SKILL.md` — brainstorm a design plan
first, critique it against this brief, then build. Two hard rules for this project:

1. NOT GENERIC / NOT AI-SLOP: Explicitly avoid the default AI-website looks (cream +
   terracotta serif, black + neon accent, newspaper hairline-rule layout) unless you can
   justify why it's the actual right fit for THIS business. Color, type, and layout
   choices must trace back to something specific about this business, not generic
   "professional website" convention.

2. ANIMATION MUST BE SPECIFIC, NOT DECORATIVE: Real 3D depth and aesthetic animation is
   a hard requirement, but it must be built FROM this business's actual world (materials,
   tools, process, textures, movement specific to the trade) — not a generic dimensional
   effect reused across unrelated businesses. If the same animation would work equally
   well on a totally different business, it's too generic.

Animation intensity for THIS business: [choose per site]
  - Bold & dimensional: layered 3D elements, strong scroll-triggered depth, standout
    hero animation — gym / architecture / hairsalon
  - Refined & subtle: smooth dimensional transitions, restrained parallax, calm but
    still genuinely animated — clinic / conservative-industry sites

Vibe: [pull from your table]

PHOTOS & VIDEO — must be sharp, high-quality, and specific
- Source real photography from free-license stock sites — Pexels, Unsplash, or Pixabay —
  using their high-resolution/original size, not thumbnail or preview quality. Search with
  specific terms tied to this exact business (e.g. "artisan woodworking workshop hand
  tools," not just "carpentry") — no generic corporate stock, no obviously staged photos.
- Where a background or hero video would genuinely elevate the design (not everywhere),
  source a short high-quality looping clip from Pexels Videos, Mixkit, or Coverr — compress
  it appropriately (short loop, muted, lazy-loaded) so it doesn't hurt load speed.
- Confirm the images/videos used are under a free-for-commercial-use license (Pexels,
  Unsplash, Pixabay, Mixkit, and Coverr's standard libraries all qualify) — flag it if
  you're unsure of a specific asset's license rather than using it anyway.
- Optimize everything: serve images as WebP where possible, use Astro's built-in image
  optimization, and keep video files small — sharp quality shouldn't come at the cost of
  a slow page.

STRUCTURE
Pages: Home, About, Services, Contact (add a gallery/portfolio page if relevant).

Footer: one small, unobtrusive line — "Concept site by [Your Name] · not a real business."

PROCESS
1. Show me the design plan first: color/type/layout, the animation signature moment and
   why it's tied to THIS business, and where photo vs. video will be used and why.
2. Flag anything in this brief pushing you toward a default/generic answer instead of a
   considered one.
3. Build it.
4. Note anywhere a real photo/video/asset would meaningfully upgrade a placeholder.