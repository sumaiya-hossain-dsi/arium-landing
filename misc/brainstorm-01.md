# Portfolio Site — Brainstorm Session 1
**Date:** 2026-02-23
**Status:** In progress — awaiting decisions

---

## WHO WE'RE BUILDING FOR

**Saarah Hossain** — systems-oriented software engineer and community builder.

**Core narrative tension to resolve:**
She has genuine technical depth AND genuine community involvement AND is multilingual AND has a hardware background AND is pivoting toward ML/AI. That's a lot. The site has to make her feel _cohesive_ not scattered.

**GPT report's best one-liner:** "Systems-minded builder with a community heart."

---

## SECTION 1: POSITIONING

### What is the primary audience?

| Audience | What they care about | Implication |
|----------|---------------------|-------------|
| Tech recruiters (SWE/mobile/backend) | GitHub, shipped products, stack breadth | Lead with projects and skills |
| Data/ML recruiters | Research, Python, ML tools, certs | ML section prominent |
| Research positions / academia | Papers, research experience, academic rigor | Academic framing, MEng front-and-center |
| Non-profit / community orgs | Volunteer work, community leadership | Highlight CRC, LMM, Data for Good |
| General networking | Overall personality and credibility | Cohesive human narrative |

**Decision needed:** What's the primary target? One page can serve multiple audiences with smart layout but it shapes the _hero_ framing most of all.

> **[My Decision :] -->** General networking -- prioritizing tech profession , but also want to highlight community contributions and let personality peek through. (I feel like highlighting the Stack Overflow contributions somewhere might tie it together a bit somehow...just not sure how.)

### Positioning headline options:

1. **Technical breadth:** "Software Engineer | ML Practitioner | Systems Builder"
2. **Pivot narrative:** "From Hardware to ML: Versatile Engineer Building Meaningful Systems"
3. **Community angle:** "Engineer & Builder — In Code and Community"
4. **GPT report phrase:** "Systems-Minded Builder with a Community Heart"
5. **Simple + strong:** "Saarah Hossain — Software Engineer"

The GPT reports suggest she leans toward honesty + authenticity over flashiness. I'd lean toward something clean and confident rather than trying to cram in everything.

> **[My Decision :] -->** Agreed...can we create an extensive checklist of elements to include in terms of content and I can categorize them as 'must have', 'must omit', 'prefer to have', 'prefer to omit', 'neutral', etc?

---

## SECTION 2: PAGE STRUCTURE OPTIONS

She wants **multiple pages** (explicitly stated). GitHub Pages handles this cleanly with static HTML files.

### Option A: Main hub + depth pages
One rich scrollable landing page that covers everything briefly, with sub-pages for depth.

```
index.html          ← hero, about blurb, featured projects, skills summary, contact
about.html          ← fuller narrative, values, languages, interests
projects.html       ← all projects with descriptions
experience.html     ← work + volunteer timeline
```

**Pros:** Visitors get the full picture fast from index. Deep divers can explore.
**Cons:** Index page may feel long/complex to build.

### Option B: Flat multi-page nav
Each major section is its own page, linked from a consistent nav.

```
index.html          ← hero + brief intro + CTAs
about.html          ← longer bio
projects.html       ← projects showcase
experience.html     ← work + volunteering
skills.html         ← tech stack, certs, languages
contact.html        ← contact
```

**Pros:** Clean, navigable, each page focused.
**Cons:** More files to maintain; visitors may not explore all pages.

### Option C: Single-page scroll (all sections)
Everything on one long scrollable page with anchor links.

**Pros:** Simple to build and maintain, common for portfolios.
**Cons:** She explicitly wants multiple pages.

### Recommendation: **Option A** — rich index + depth sub-pages
This is the most common professional portfolio pattern today. The index serves as a "trailer" and recruiters who want to skim can; those who want depth can go deeper.

> **[My Decision :] -->** am leaning a bit towards B , but am curious what you mean by "subpages" in A. (would it be possible to explore some other portfolios before deciding? can you see/explore other portfolios by link? like https://saad-hossain.github.io/ seems nice, can you take a look at its setup? can you suggest some others for me to look at and discuss?)

---

## SECTION 3: CONTENT — WHAT TO INCLUDE

### Confirmed content (plenty of source material):

- **Hero / About** — headline, 2-3 sentence bio, photo (need to confirm availability)
- **Featured Projects** (3–5 on index, full list on projects page):
  - TCF Practice Tracker (Go + SQLite, Boot.dev Hackathon 2025, 5 stars, public)
  - Chaos Pebble (Android + Kotlin + Jetpack Compose, internal Play Store release)
  - Hardware Logic Encryption (VLSI/CMOS, senior design, research quality, public)
  - Arium Landing Page (client work, live deployed, shows real-world delivery)
  - MVT in Silico cerebral blood flow tool (research context, commercial context)
  - AI Chatbot Engine at Loosely Coupled (commercial, saved 20hrs/week)
- **Experience timeline** — 4 work roles + current RA, education, volunteering
- **Skills & Certifications** — 60+ skills by category, 17+ certs with links, 8 languages
- **Community** — CRC PDAT, LMM librarian/operations, Data for Good, Smithsonian
- **Stack Overflow** — 4,790 rep, 444 posts (shows technical community engagement)
- **Resume downloads** — one or multiple tailored versions
- **Contact** — email, GitHub, LinkedIn, Stack Overflow

### Content decisions needed:

1. **Photo?** Does she have a professional headshot available? [**MyAnswer**: yes]
2. **Resume strategy:**
   - Option 1: Single "master" resume download
   - Option 2: Multiple role-targeted versions (data, Android, RA, etc.)
   - Option 3: Interactive online resume view
   > [**MyAnswer**: single  "master" resume download for now, but must put together something fitting...]
3. **Blog/Writing section?** Stack Overflow presence is strong but no blog posts found. Include a SO profile link or skip writing section for now? 
   > [**MyAnswer**: unfortunately I have blog yet...will have to see if I can start something, but not for a few months yet. Would just like to have SO link and icon in list of profile links at some prominent section.]
4. **Community section prominence:** Subtle (2-3 bullets in about) vs. full standalone section? 
   > [**MyAnswer**: undecided...would prefer a list somewhere. A popup modal?]
5. **French content?** Even a brief French intro sentence could signal bilingual capability without adding full translation maintenance overhead. 
   > [**MyAnswer**: yes I like that idea, let's keep it realistic and a bit lowkey though.]

---

## SECTION 4: DESIGN AESTHETIC OPTIONS

### Option 1: Clean Technical Minimal
- Light background (white / near-white), lots of whitespace
- Monospace or geometric sans-serif typography
- Single strong accent color (e.g., deep teal `#0D7377` or electric blue)
- Think: Linear, Stripe, well-designed dev tools
- **Tone:** Professional, technical, no-frills
- **Good for:** SWE/backend/mobile roles
- **Risk:** Can feel cold or generic if not executed with care

### Option 2: Warm Modern Professional
- Off-white / cream background or soft light grey
- Serif headings + clean sans body (contrast adds personality)
- Warmer accent (muted terracotta, warm purple, or deep warm navy)
- Think: Notion docs, academic personal sites done well
- **Tone:** Approachable, credible, human
- **Good for:** Research roles, community-facing roles, non-profits
- **Risk:** May feel less "SWE/tech" to some recruiters

### Option 3: Dark Mode Bold ⭐ (my lean)
- Dark background (`#0F1117` or deep slate) + light text
- Clean grid/card-based layout (reflects systems-thinking aesthetic)
- Strong accent color — deep teal `#1A535C` or vibrant violet-blue `#6C63FF`
- Cards for projects, timeline for experience, tags for skills
- Toggle between dark and light mode
- **Tone:** Distinctive, modern, technical with personality
- **Good for:** Any tech role, makes a strong visual impression
- **Risk:** Slightly more complex to implement well

### Option 4: Systems/Blueprint Aesthetic
- Dark navy or deep charcoal background
- Grid lines or subtle blueprint-style texture
- Monospace accents, technical typography
- Very distinctive, references hardware/systems engineering background
- **Tone:** Unique, memorable, nerdy in a good way
- **Risk:** Could be too niche or feel dated; harder to pull off cleanly

### Color palette thoughts (for any option):
Her background includes Jordan, Malaysia, Bangladesh, Canada — no specific palette suggestion from the data, but the GPT reports describe her aesthetic style as "pragmatist" who values function + clarity. Clean, confident colors over decorative ones.

Possible accent colors:
- Deep teal `#1A535C` — professional, distinctive, not overused
- Violet-blue `#6C63FF` — modern, ML/AI adjacent
- Warm amber `#F5A623` — energetic, human
- Forest green `#2D6A4F` — community-oriented, grounded

> **[My Decision :] -->** I really don't know how to swing with this...maybe some combo of or compromise between options 1 and 2? Legibility and accessibililty are v important to me too. Must prioritize RWD and UX.

---

## SECTION 5: TECH STACK FOR THE SITE

Constraints:
- Static only (GitHub Pages)
- No build pipeline unless deliberately chosen
- Phone-friendly maintenance (root README mentions this)
- Accessibility + SEO important (root README notes)

### Options:

| Stack | Pros | Cons |
|-------|------|------|
| Pure HTML/CSS/JS | No dependencies, simplest maintenance | More verbose CSS, manual organization |
| HTML + Tailwind CDN | Utility-first, fast to style, no build step needed with CDN | CDN dependency, slightly large |
| HTML + Pico CSS | Beautiful minimal defaults, semantic HTML | Less control over heavy customization |
| HTML + custom CSS (variables) | Full control, lightweight, modern CSS is very capable | More upfront work |
| Jekyll (GitHub Pages native) | Layouts, includes, front matter — DRY | Template syntax overhead, build step |
| 11ty / Astro | Modern SSG, great for multi-page | Requires local build + push, more complex |

**Recommendation:** `HTML + custom CSS with CSS custom properties (variables)` + minimal vanilla JS for interactivity (mobile nav toggle, maybe dark mode toggle). This is:
- Zero dependencies
- Easy to maintain via web UI or local
- Full control
- Modern CSS (grid, flexbox, variables) is more than capable

Optional enhancement: add **Tailwind CDN** if utility classes would speed things up significantly. Can decide during implementation.

> **[My Decision :] -->** Let's go with the recommended [HTML + custom CSS + vanilla JS] plus maybe the optional Tailwind CDN. I'd probably like to play with Jekyll later but not now.

---

## SECTION 6: KEY QUESTIONS FOR SAARAH

Before proceeding to design mockups or implementation:

1. **Primary audience:** Who is the main person you're trying to impress? (Tech recruiters, research labs, community orgs, or all equally?) [AnsweredAbove]
2. **Aesthetic direction:** Which of the 4 design options above appeals most, or describe your own? [AnsweredAbove]
3. **Photo:** Do you have a professional headshot you're happy with? [AnsweredAbove]
4. **Resume strategy:** Single download or multiple role-targeted ones? [AnsweredAbove]
5. **Community section:** How prominently do you want your volunteer work featured? (Subtle / Equal to work experience / Full separate section?) [AnsweredAbove]
6. **Blog/writing:** Want to include this now (even if empty as a placeholder) or skip for v1? [AnsweredAbove]
7. **French toggle:** Worth adding even a subtle bilingual touch, or keep English-only for simplicity? [AnsweredAbove]
8. **Domain:** Keeping fwsara95h.github.io or planning a custom domain (e.g., saarahhossain.com)? [**MyAnswer**: no custom domain just yet]
9. **Contact method:** Email visible on site or only via form/GitHub/LinkedIn? [**MyAnswer**: sure I'll put my uwo email]

---

## SECTION 7: OVERALL RECOMMENDATION (DRAFT)

If I were building this today with what I know:

**Structure:** Option A (rich index + 3-4 depth sub-pages)
**Nav pages:** Home, About, Projects, Experience, Contact
**Design:** Clean dark-mode-primary with teal accent, card-based project grid, timeline for experience, tags for skills
**Tech stack:** HTML + custom CSS (variables) + minimal vanilla JS
**Hero framing:** "Software Engineer & Systems Builder" with a 2-3 sentence human bio
**Community:** Dedicated section on the About page + a brief callout on the index, rather than a standalone page
**Resume:** One primary download on the index (master CV) with a note that role-targeted versions available on request or on the Experience page
**French:** One bilingual line in the hero or footer as a subtle signal, no full translation

---

## DECISIONS LOG

| Decision | Status | Notes |
|----------|--------|-------|
| Primary audience | ❓ Pending | |
| Aesthetic direction | ❓ Pending | |
| Page structure | ❓ Pending | Lean: Option A |
| Hero headline | ❓ Pending | |
| Community section prominence | ❓ Pending | |
| Resume strategy | ❓ Pending | |
| Blog/writing section | ❓ Pending | |
| French content | ❓ Pending | |
| Domain | ❓ Pending | |
| Tech stack | ❓ Pending | Lean: HTML + custom CSS |
| Photo availability | ❓ Pending | |
