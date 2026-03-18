# Portfolio Site — Final Site Map & Component Plan
**Date:** 2026-02-23
**Status:** Ready for build — pending wireframe approval

---

## FINAL ARCHITECTURE DECISION

**Hybrid: Rich scrollable index + one depth sub-page**

- `index.html` → rich single-page scroll (Brittany Chiang style), all sections present, anchor-linked nav
- `projects.html` → full filterable project list (index shows 3 featured cards + "See all →" link)
- `404.html` → custom error page

The nav links scroll to sections on the same page (anchor links). The "multiple pages" feel comes from:
- The projects sub-page
- A distinct nav bar that feels like it navigates between destinations
- Clear section transitions

**Why not flat multi-page (Option B)?**
After looking at the Brittany Chiang example she liked, the single-page scroll with anchor-linked sections IS the pattern — it gives the feeling of multiple distinct zones without splitting content across files. Recruiters can skim all at once; deep readers can follow section links. The projects page gives a genuine second page for filtering/exploring.

---

## PAGE MAP

```
fwsara95h.github.io/
├── index.html           ← Main portfolio (scrollable, 8 sections)
├── projects.html        ← Full filterable project showcase
├── 404.html             ← Custom error page
├── assets/
│   ├── css/
│   │   └── style.css    ← All styles (CSS variables for light/dark)
│   ├── js/
│   │   └── main.js      ← Nav toggle, dark mode, project filter, back-to-top
│   ├── img/
│   │   ├── headshot.*   ← Professional photo (to be uploaded)
│   │   ├── favicon.*    ← To be created
│   │   └── og-image.*   ← Open Graph preview image
│   └── files/
│       └── FWSH_CV2025.pdf   ← Resume download
```

---

## INDEX.HTML — SECTION ORDER

```
[NAV] Saarah Hossain | About  Experience  Community  Projects  Skills  Contact  [🌙]
│
├── #hero
├── #about
├── #experience
├── #community          ← volunteering + ecosystem engagement combined
├── #projects           ← 3 featured + "See all projects →"
├── #skills
├── #certifications     ← grouped within skills or adjacent section
└── #contact
│
[FOOTER] links · French phrase · © · 🌀 (TARDIS easter egg bottom-right)
[↑] Back-to-top button (fixed, appears after scroll)
```

---

## SECTION DETAIL

### 1. HERO `#hero`
```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│   Saarah Hossain                                        │
│   Software Engineer & Systems Builder        [photo or  │
│                                               cartoon]  │
│   Brief bio — 2-3 sentences. Tagline here.             │
│                                                         │
│   Bonjour! Ingénieure logicielle basée à London, ON.   │  ← French line
│                                                         │
│   [GH icon] [LI icon] [SO icon] [Email icon]           │
│   [Download CV]                                         │
└─────────────────────────────────────────────────────────┘
```
**Content:** Name, headline, 2–3 sentence bio, lowkey French intro line, social icon row (GitHub, LinkedIn, Stack Overflow, email), resume download CTA.
**Notes:** Photo/headshot placement TBD (right-aligned card on desktop, stacked on mobile). Cartoon pop-out style if illustration is available, otherwise styled headshot.

---

### 2. ABOUT `#about`
```
┌─────────────────────────────────────────────────────────┐
│  About Me                                               │
│                                                         │
│  Extended bio paragraph...                              │
│  Career narrative: hardware → software → ML...          │
│                                                         │
│  Languages:                                             │
│  🇬🇧 English (native)  🇧🇩 Bengali (native)             │
│  🇫🇷 French (professional, TCF B2)                     │
│  + others                                               │
│                                                         │
│  ✨ Outside the IDE: [fun/personality snippet]          │
└─────────────────────────────────────────────────────────┘
```
**Content:** Extended bio, career pivot story (short form), language list with flags, a small humanizing note (interests, bookbinding, math YouTube, etc.).

---

### 3. EXPERIENCE `#experience`
```
┌─────────────────────────────────────────────────────────┐
│  Experience                              [Download CV ↓]│
│                                                         │
│  ── WORK ──────────────────────────────────────────     │
│                                                         │
│  ● Aug 2025 – present                                   │
│    Research Assistant · Beauséjour FRC · NB, Canada     │
│    • bullet...                                          │
│    • bullet...                                          │
│                                                         │
│  ● Mar – Aug 2024                                       │
│    Software Developer & BA · MVT in Silico · London ON  │
│    ...                                                  │
│                                                         │
│  ● Sep 2019 – Aug 2020                                  │
│    Technology Specialist, AI & DS · LCT · Kuala Lumpur  │
│    ...                                                  │
│                                                         │
│  ● Jul – Aug 2018                                       │
│    ASIC Design Intern · PrimeSilicon · Dhaka, BD        │
│    ...                                                  │
│                                                         │
│  ── EDUCATION ──────────────────────────────────────    │
│                                                         │
│  ● 2024  MEng Software Engineering · Western University │
│         Graduate Diploma also conferred                 │
│         Notable projects: [indoor localization, ML...] │
│                                                         │
│  ● 2019  BSc Electrical Engineering · PSUT · Jordan     │
│         Capstone: Hardware Logic Encryption → [link]    │
└─────────────────────────────────────────────────────────┘
```
**Content:** Vertical timeline. Work (4 roles) + Education (2 degrees). Date ranges + org + location + 3–5 bullets per role. CV download button top-right. Capstone links to projects page.

---

### 4. COMMUNITY & VOLUNTEERING `#community`
```
┌─────────────────────────────────────────────────────────┐
│  Community & Volunteering                               │
│                                                         │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐  │
│  │ 🏥 Canadian  │  │ 📚 London    │  │ 📊 Data for  │  │
│  │  Red Cross   │  │ Muslim Mosque│  │  Good Toronto│  │
│  │  PDAT        │  │  Assoc.      │  │              │  │
│  │  Responder   │  │  Librarian   │  │              │  │
│  │  Apr 2025–   │  │  Apr 2025–   │  │  Aug 2025–   │  │
│  └──────────────┘  └──────────────┘  └──────────────┘  │
│                                                         │
│  + Smithsonian Digital Volunteers · Muslim Wellness     │
│    Network · Elevate Festival · Ilma Girls' School      │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │  Stack Overflow  ·  4,790 rep  ·  444 posts  →  │   │  ← SO callout card
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  Also: TEDxPSUT curation · Immigrants in Tech Summit    │
└─────────────────────────────────────────────────────────┘
```
**Content:** 3 main volunteer orgs as cards (CRC, LMM, Data for Good) + a secondary compact list for others (Smithsonian, Muslim Wellness Network, Elevate, Ilma, Ramadan Giving). SO callout card inline. TEDxPSUT + Immigrants in Tech Summit as brief mentions.
**Notes:** Accordion expand available on each card for more detail — avoids modal complexity while keeping the index clean.

---

### 5. PROJECTS `#projects`
```
┌─────────────────────────────────────────────────────────┐
│  Projects                                               │
│                                                         │
│  [All] [Mobile] [Hardware] [Web] [ML/AI]               │  ← filter tabs
│                                                         │
│  ┌───────────────┐  ┌───────────────┐  ┌─────────────┐ │
│  │ TCF Practice  │  │ Hardware Logic │  │  Chaos      │ │
│  │ Tracker       │  │ Encryption     │  │  Pebble     │ │
│  │               │  │               │  │  [WIP 🚧]   │ │
│  │ Go · SQLite   │  │ VLSI · CMOS   │  │ Android     │ │
│  │ [GH] [⭐5]    │  │ [GH] [paper?] │  │ Kotlin      │ │
│  └───────────────┘  └───────────────┘  └─────────────┘ │
│                                                         │
│                         [See all projects →]            │
└─────────────────────────────────────────────────────────┘
```
**Content:** 3 featured project cards. Filter tabs (All / Mobile / Hardware / Web / ML·AI). "See all →" links to `projects.html`. Chaos Pebble shown with 🚧 WIP badge (visible but flagged as in-progress).
**Notes:** AI Chatbot (Loosely Coupled commercial) included on `projects.html` as a non-public project (described as role project, no code link). Project screenshots as WebP with `loading="lazy"` — no performance hit.

---

### 6. SKILLS `#skills`
```
┌─────────────────────────────────────────────────────────┐
│  Skills                                                 │
│                                                         │
│  Languages                                              │
│  [Python] [JavaScript] [Go] [Kotlin] [Java] [C/C++]    │
│  [R] [SQL] [Tcl] [VHDL] [Assembly]                     │
│                                                         │
│  Frameworks & Tools                                     │
│  [Android SDK] [Jetpack Compose] [Next.js] [HTML/CSS]  │
│  [UiPath] [Git] [Docker] [Kubernetes]                   │
│                                                         │
│  Cloud & DevOps                                         │
│  [Google Cloud] [Azure] [CI/CD]                         │
│                                                         │
│  AI / ML                                               │
│  [Machine Learning] [NLP] [Data Science] [Predictive]  │
│                                                         │
│  Databases                                              │
│  [SQL Server] [SQLite] [Oracle]                         │
│                                                         │
│  Hardware & Embedded                                    │
│  [VLSI/ASIC] [Synopsys] [Arduino] [Simulink] [LTSpice] │
└─────────────────────────────────────────────────────────┘
```
**Content:** Tag chips grouped by category. No progress bars. Approx 6 categories.

---

### 7. CERTIFICATIONS `#certifications`
*(within or immediately after Skills section)*
```
┌─────────────────────────────────────────────────────────┐
│  Certifications                                         │
│                                                         │
│  Cloud & DevOps                                         │
│  [Google Cloud Essentials ↗] [AZ-900 Azure ↗]          │
│  [Deploy Kubernetes ↗] [Serverless Cloud Run ↗] ...    │
│                                                         │
│  AI & Data Science                                      │
│  [DeepLearning.AI Supervised ML ↗] [IBM Cloud ↗]       │
│  [HarvardX Data Science ↗] [AI in Healthcare ↗]        │
│                                                         │
│  Mobile Development                                     │
│  [Meta Android Developer ↗]                             │
└─────────────────────────────────────────────────────────┘
```
**Content:** Grouped by domain. Each cert is a clickable tag/badge linking to Coursera/Credly credential. Logo images where available (lazy-loaded).

---

### 8. CONTACT `#contact`
```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│  Let's connect.                                         │
│                                                         │
│  [firstname.lastname@uwo.ca]                            │
│                                                         │
│  [GitHub] [LinkedIn] [Stack Overflow] [Email]           │
│                                                         │
│  [Book a call ↗]   ← optional Calendly/GCal link       │
└─────────────────────────────────────────────────────────┘
```

---

## PROJECTS.HTML — FULL PROJECT LIST

```
[Back to portfolio ←]

All Projects

[All] [Mobile] [Hardware] [Web/Frontend] [ML·AI] [Automation]

┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐
│ TCF Practice    │  │ Hardware Logic  │  │ Chaos Pebble    │
│ Tracker         │  │ Encryption      │  │ [WIP 🚧]        │
│ Go · SQLite     │  │ VLSI · Synopsys │  │ Android · Kotlin│
│ [GH] [⭐5]      │  │ [GH]            │  │ Compose         │
└─────────────────┘  └─────────────────┘  └─────────────────┘

┌─────────────────┐  ┌─────────────────┐
│ AI Chatbot      │  │ TEDxPSUT        │
│ Engine          │  │ Curation        │
│ (Loosely Coupled│  │ (Project Lead)  │
│ R · MSSQL · NLP │  │ Event Prod.     │
│ [role project]  │  │                 │
└─────────────────┘  └─────────────────┘
```

---

## GLOBAL COMPONENTS

### Navigation
```
[Saarah Hossain]  About  Experience  Community  Projects  Skills  Contact  [🌙/☀]
```
- Sticky top, transparent → solid on scroll
- Mobile: hamburger → full-height slide-in menu
- Active section highlighted as user scrolls (scroll-spy)
- Dark/light toggle icon at right end

### Footer
```
────────────────────────────────────────────────────────
Designed & built by Saarah Hossain · 2026
[GH] [LI] [SO]
Construite avec soin — London, Ontario 🍁           [🌀]
────────────────────────────────────────────────────────
```
- Left: copyright + social icons
- Centre or right: French phrase
- Bottom-right corner: TARDIS (small, subtle, delightful — animated on hover)

### Fixed UI Elements
- Back-to-top button: appears after 300px scroll, bottom-right (above TARDIS in footer)
- (TARDIS lives in footer, not as a fixed overlay — keeps it subtle)

---

## DESIGN TOKENS (CSS VARIABLES)

```css
/* Light mode (default) */
--bg:          #FAFAF8;    /* warm off-white */
--bg-card:     #FFFFFF;    /* card surface */
--text:        #1E1E2E;    /* near-black */
--text-muted:  #6B7280;    /* secondary text */
--accent:      #1A7070;    /* deep teal */
--accent-light:#E6F4F4;    /* tint for tags/chips */
--border:      #E5E7EB;    /* subtle borders */

/* Dark mode (.dark class on <body>) */
--bg:          #0F1117;
--bg-card:     #1A1B26;
--text:        #E8E8F0;
--text-muted:  #9CA3AF;
--accent:      #2AADAD;    /* slightly brighter teal for dark bg */
--accent-light:#0D3A3A;
--border:      #2D2D3E;
```
Font: **Inter** (via Google Fonts) — clean, humanist, excellent for tech portfolios, great accessibility/readability, free.

---

## TECH STACK (CONFIRMED)

- HTML5 (semantic: `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`)
- CSS (custom properties, grid, flexbox, mobile-first media queries)
- Vanilla JS (`~150–200 lines` expected: nav toggle, dark mode, scroll-spy, project filter, back-to-top)
- Tailwind CDN: optional — decide during build whether utility classes help enough to justify the CDN request
- No frameworks, no build step, no dependencies

---

## PERFORMANCE NOTES

- Images: WebP format, `loading="lazy"` attribute — no lag
- JS: small, deferred — no blocking
- Fonts: preconnect to Google Fonts, only load weights needed
- CSS: one file, no preprocessor needed
- Target: Lighthouse 90+ on all metrics

---

## DEFERRED / LATER

- Jekyll migration (she mentioned wanting to try later)
- French language toggle (planned for future version)
- Blog section (when blog exists)
- Custom domain (future)
- Cartoon pop-out illustration (needs asset — can replace headshot later)
- Multiple resume downloads by role (v2 feature)
- Arium Landing Page as project (needs polish first)

---

## OPEN MICRO-DECISIONS (can decide during build)

| Item | Options | Lean |
|------|---------|------|
| Photo placement on hero | right-aligned card / circular / full-bleed | right-aligned card |
| Volunteering display | 3 cards + secondary list vs. accordion | 3 cards + compact list |
| Skills + Certs | Same section or adjacent sections | Adjacent |
| Calendly/GCal link in contact | Include if she has a booking link | Include if available |
| "Book a call" wording | "Schedule a chat" / "Book time with me" / skip | Skip if no Calendly |

---

## BUILD ORDER (RECOMMENDED)

1. `style.css` — design tokens, reset, base styles, grid/layout system
2. `index.html` shell — nav + all section placeholders + footer
3. Hero section (content + layout)
4. Skills + Certifications (simple content, good for momentum)
5. Experience timeline (timeline component)
6. Projects section (card component + filter)
7. Community & Volunteering section
8. About section
9. Contact section
10. `main.js` — nav toggle, dark mode, scroll-spy, back-to-top
11. Project filter JS
12. `projects.html`
13. `404.html`
14. SEO: meta tags, OG image, favicon, robots.txt
15. Polish: animations, hover states, accessibility pass
16. Final: lighthouse audit, cross-browser check
