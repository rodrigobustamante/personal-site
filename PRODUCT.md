# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Two audiences with equal weight:

- **Recruiters and hiring managers** deciding whether Rodrigo fits a role. They skim the home page, open one or two case studies, then either email him or download the CV.
- **Technical peers** (frontend engineers, design-system practitioners) who arrive through a blog post, `/system` or `/uses`. For them the writing and the site itself are the proof of judgment. Some of them are also the people who refer or hire.

## Product Purpose

Rodrigo Bustamante's bilingual personal site (rodrigobustamante.cl): portfolio, case studies, a blog on web performance and design systems, and the site's own design system and build notes. It exists to get him hired into design-system and frontend-architecture roles, and to back that up with evidence a reader can check. It succeeds when the right person reaches out, or leaves convinced by a case study or a post.

## Positioning

Design systems first: a specialist who builds and runs design systems at scale, with Hangar Design System (LATAM Airlines, 50+ teams) as the anchor case. Frontend platform architecture is the supporting skill (current role: Software Architect at Vantaz). Senior Frontend Engineer is the floor, not the headline.

The claim no neighbouring portfolio can copy is the record itself: one design system adopted across an airline (millions of passengers), an architecture rebuilt for a copper-mining supplier platform, and a site that publicly documents its own tokens and build.

The hero role, contact copy, page titles, meta description and JSON-LD `jobTitle` all follow this positioning; keep them in step when it changes.

## Operating Context

- Visitors land on `/` (English) or `/es` (Spanish). A Cloudflare Worker picks the language at the edge from a cookie or `Accept-Language`, and visitors can switch it from the header.
- Typical recruiter path: home → `/work` case study → contact email or CV download.
- Typical peer path: a blog post (`/blog/<lang>/…`) or `/system` / `/uses` → home.
- Links get shared on LinkedIn and in job applications, so each page has a generated Open Graph card.

## Capabilities and Constraints

- Astro static site on Cloudflare Workers with static assets. MDX content collections for posts (`src/content/post`) and case studies (`src/content/work`). RSS feed per language, sitemap.
- Fully bilingual: English at `/`, Spanish under `/es`, blog at `/blog/en` and `/blog/es`. Every piece of content and every change ships in both languages at once.
- Light and dark themes, plus two base styles (Cosmos and Paper).
- Isometric SVG dioramas illustrate the case studies and the home page.
- Performance is part of the product: the site has to practise what the blog preaches (Lighthouse CI in the pipeline, scores of 94 and up, green Core Web Vitals).
- CI gates: ESLint, Prettier, `node --test`, build and Lighthouse.

## Brand Commitments

- Name: Rodrigo Bustamante, based in Madrid. Open to remote work.
- Vantaz is named. Its copper-mining client is never named anywhere: not in copy, images, alt text or metadata.
- English and Spanish carry the same voice; neither one is a translation afterthought.

## Evidence on Hand

- Case studies (`src/content/work/{en,es}`): Hangar Design System (LATAM Airlines, Software Architect), LATAM Airlines Home (Web UI Developer → Senior Software Engineer), Supplier Management Platform (Vantaz, copper mining, Chile; Software Architect), and the side projects PACE, Intervalo and A11yScan.
- Hero figures already published: 9 years of engineering, 50+ teams on the design system, millions of passengers reached, 10+ countries.
- Blog posts on Core Web Vitals and speculative rendering, in EN and ES.
- `/system` (the site's tokens and components) and `/uses` (how it's built, including a GitHub activity graph).
- Downloadable CV.
- No testimonials, client logos or quoted metrics beyond those above. Future work must not invent any.

## Product Principles

1. **Proof over claims.** Every assertion points to a case study, a post or the site itself.
2. **Design systems lead.** Order and emphasis favour design-system work; general frontend work supports it.
3. **The site is the demo.** Performance, accessibility and craft are part of the evidence, so any regression in them weakens the product.
4. **Two languages, one product.** EN and ES stay in parity in content, structure and quality.
5. **Discretion is part of credibility.** Client confidentiality is never traded for a better story.

## Accessibility & Inclusion

WCAG 2.2 AA at minimum: AA contrast in every theme and style, full keyboard access, and motion respects `prefers-reduced-motion`. Lighthouse accessibility 100 is the bar the site already meets.
