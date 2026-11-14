# GLOBAL Institute — Spoken English & Personality Development Website

A complete, high-performance static website for **GLOBAL Institute** built with **Astro 5**, **Bun**, and vanilla CSS design tokens. 

Designed for North India's premier English communication institute led by Coach Faizan Khan (15,000+ alumni, 1,700+ MNC placements, 1,000+ teachers placed).

---

## 🌟 Key Features

- **10 Core Homepage Sections in Exact Architectural Flow:**
  1. **Hero Banner:** Headline, call-to-action triggers, trust badges, WhatsApp quick enrollment, and SVG illustration.
  2. **Achievement Statistics:** Key metrics ribbon (15K+ alumni, 1,700+ corporate hires, 1,000+ teachers, 12 levels).
  3. **Our Courses:** Showcase for Spoken English, Personality Development, and Interview Preparation with key features and links to dedicated dynamic pages.
  4. **Meet Our Trainer & Why Choose Us:** Profile of Coach Faizan Khan, Kamal, and the 12-Level neuro-linguistic conversational methodology.
  5. **Our Achievements:** Landmark milestones, corporate hiring partners (Amazon, Infosys, TCS, Deloitte, Genpact, etc.).
  6. **Life at GLOBAL Institute (Gallery):** Interactive gallery with category filtering (All, Campus, Speaking, Podiums, Awards) and modal previews.
  7. **Video Testimonials:** Student story cards with integrated video modal player for masterclasses and alumni reviews.
  8. **Student Reviews & Social Proof:** 4.9/5 star rating banner, Google review cards with verified badges.
  9. **Contact & Enquiry:** Campus address, contact info, interactive Google Map embed, and dual-submission admissions form (direct validation + instant WhatsApp dispatch).
  10. **Comprehensive Footer:** Quick links, course directory, campus hours, accreditation, and sticky mobile quick-action bar.

- **Complete Subpage Suite:**
  - `/about`: Pedagogical philosophy, trainer profiles, and mission.
  - `/courses`: Course comparison matrix and 12-Level ladder overview.
  - `/courses/[slug]`: Dynamic static pages for `spoken-english`, `personality-development`, and `interview-preparation` with detailed phase-by-phase syllabi.
  - `/achievements`: Corporate placement records, hiring partners, and alumni highlights.
  - `/gallery`: Categorized photo gallery with interactive filtering.
  - `/testimonials`: Video stories and student transformation archives.
  - `/reviews`: Full Google review directory with verified student ratings.
  - `/contact`: Campus location, admissions desk, schedule, and FAQs.
  - `/privacy-policy`: Data privacy and student confidentiality commitments.
  - `/404`: Custom responsive error page matching theme.

- **Zero Missing Assets:**
  - Built entirely with standalone SVG vector assets for logos, course illustrations, video thumbnails, gallery scenes, and avatars.

- **Interactive UI Components:**
  - Mobile slide-drawer navigation.
  - Global accessible video modal dialog (`VideoModal.astro`).
  - Client-side validated demo registration form with instant WhatsApp message prefill.
  - Sticky bottom contact bar for mobile screens (Call Now + WhatsApp + Book Demo).

---

## 🚀 Technology Stack

- **Framework:** [Astro 5](https://astro.build/) (Static Site Generation / SSG)
- **Runtime & Package Manager:** [Bun](https://bun.sh/)
- **SEO & Sitemap:** `@astrojs/sitemap`
- **Type Checking:** `@astrojs/check` + TypeScript 5
- **Styling:** CSS variables, responsive fluid typography, and semantic HTML5

---

## 🛠️ Local Development & Build Commands

### Prerequisites
Ensure [Bun](https://bun.sh) is installed.

```bash
# Verify Bun installation
bun --version
```

### Install Dependencies
```bash
bun install --frozen-lockfile
```

### Run Local Development Server
```bash
bun run dev
```
Open [http://localhost:4321](http://localhost:4321) in your browser.

### Type Check & Production Build
```bash
bun run build
```
Generates 13 static HTML pages, SVG assets, CSS bundles, and sitemaps in the `dist/` directory.

### Preview Static Production Build
```bash
bun run preview
```

---

## 📁 Project Architecture

```text
├── public/
│   ├── favicon.svg             # Institute SVG favicon
│   ├── robots.txt              # Crawler instructions
│   └── images/                 # Standalone SVG illustrations, badges & avatars
├── src/
│   ├── components/
│   │   ├── Achievements.astro   # Corporate placement grid & statistics
│   │   ├── BaseHead.astro       # SEO metadata, Open Graph & fonts
│   │   ├── Contact.astro        # Campus info, map embed & enquiry grid
│   │   ├── Courses.astro        # Course cards with syllabus links
│   │   ├── EnquiryForm.astro    # Validated registration & WhatsApp form
│   │   ├── Footer.astro         # Site footer & mobile sticky action bar
│   │   ├── Gallery.astro        # Filterable photo gallery
│   │   ├── Header.astro         # Announcement bar, logo & slide drawer
│   │   ├── Hero.astro           # Homepage hero banner & CTAs
│   │   ├── Reviews.astro        # Google ratings & student feedback
│   │   ├── Stats.astro          # Achievement statistics counter
│   │   ├── Trainer.astro        # Trainer profile & 12-level methodology
│   │   ├── VideoModal.astro     # Accessible global video player modal
│   │   └── VideoTestimonials.astro # Video testimonial grid
│   ├── data/
│   │   ├── achievements.json    # Milestones & corporate partners
│   │   ├── courses.json         # 3 core programs with phase-by-phase syllabus
│   │   ├── gallery.json         # Categorized campus photo items
│   │   ├── reviews.json         # Ratings and testimonials
│   │   ├── site.json            # Institute info, phones, trainer details
│   │   └── videos.json          # Masterclasses and video stories
│   ├── layouts/
│   │   └── BaseLayout.astro     # Core HTML layout shell
│   ├── pages/
│   │   ├── 404.astro            # Custom 404 page
│   │   ├── about.astro          # About institute & Coach Faizan Khan
│   │   ├── achievements.astro   # Corporate placements & milestones
│   │   ├── contact.astro        # Contact & admissions FAQ
│   │   ├── courses/
│   │   │   ├── [slug].astro     # Dynamic static syllabus & detail pages
│   │   │   └── index.astro      # Course catalog & 12-level matrix
│   │   ├── gallery.astro        # Campus gallery page
│   │   ├── index.astro          # 10-section homepage
│   │   ├── privacy-policy.astro # Data confidentiality policy
│   │   ├── reviews.astro        # Verified student reviews page
│   │   └── testimonials.astro   # Video testimonials & stories
│   └── styles/
│       └── global.css           # Design tokens, reset, typography & buttons
├── astro.config.mjs             # Astro configuration + sitemap
├── package.json                 # Scripts and dependencies
└── tsconfig.json                # TypeScript configuration
```
