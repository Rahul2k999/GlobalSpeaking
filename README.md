# Astro + Bun Master Starter

A lightweight, modern, and production-ready master starter for website projects powered by **Astro 5**, **TypeScript**, and **Bun**.

Designed as a **GitHub Template Repository** to bootstrap client and internal web projects with minimal dependencies, responsive layout, CSS design tokens, dark/light mode, and built-in SEO.

---

## Features

- **Runtime & Tooling:** Ultrafast package management and builds via [Bun](https://bun.sh) with locked dependencies (`bun.lock`).
- **Zero-Bloat Core:** Minimal dependencies (`astro`, `@astrojs/sitemap`, `@astrojs/check`, `typescript`). No unnecessary frameworks until your project needs them.
- **Design Tokens & CSS Variables:** Centralized theme system in `src/styles/global.css` (colors, typography scale, spacing, border radiuses, box shadows).
- **Dark / Light Mode:** Built-in theme switcher component with `localStorage` persistence and system preference fallback (`prefers-color-scheme`). No flash of unstyled theme (FOUC).
- **Reusable UI Components:**
  - `BaseHead.astro`: Automatic canonical URLs, Open Graph, Twitter Cards, favicon, and robots integration.
  - `BaseLayout.astro`: Responsive root layout wrapping header, main content, and footer.
  - `Header.astro`: Navigation with active link detection, logo, and action buttons.
  - `Footer.astro`: Semantic responsive footer with metadata.
  - `Button.astro`: Polymorphic button component (supports variants `primary`, `secondary`, `outline`, `ghost` and renders as `<a>` or `<button>`).
  - `Card.astro`: Reusable content card with tags, hover animations, and slot support.
  - `ThemeToggle.astro`: Accessible toggle for switching between light and dark themes.
- **Built-in SEO & Sitemap:** Automated `@astrojs/sitemap` generation with dynamic `site` configuration and robots.txt.
- **Full TypeScript Support:** Astro strict TypeScript configuration with path alias support (`@/*` -> `./src/*`).

---

## Quick Start

### 1. Prerequisites
Ensure you have [Bun](https://bun.sh) installed (v1.1+ recommended).

```bash
bun --version
```

### 2. Install Dependencies
Install dependencies with locked versions:

```bash
bun install --frozen-lockfile
```

### 3. Start Development Server
```bash
bun run dev
```
Visit `http://localhost:4321` in your browser.

---

## Standard Scripts

| Command | Action |
| :--- | :--- |
| `bun run dev` | Starts local dev server at `localhost:4321` with Hot Module Replacement |
| `bun run build` | Runs type check (`astro check`) followed by production static build |
| `bun run check` | Runs Astro and TypeScript type diagnostics |
| `bun run preview` | Previews the local production build (`dist/`) |

---

## Project Structure

```text
├── .env.example            # Environment variables example (PUBLIC_SITE_URL)
├── .gitignore              # Ignores node_modules, dist, .astro, .env files, secrets
├── astro.config.mjs        # Astro configuration with sitemap integration
├── bun.lock                # Bun lockfile
├── package.json            # Scripts and minimal dependencies
├── tsconfig.json           # Astro strict TypeScript configuration with paths
├── public/
│   ├── favicon.svg         # SVG favicon
│   └── robots.txt          # Search engine crawler instructions
└── src/
    ├── components/
    │   ├── BaseHead.astro  # SEO, Open Graph, Twitter meta tags, theme inline script
    │   ├── Button.astro    # Polymorphic button/link with variants and sizes
    │   ├── Card.astro      # Feature and content cards
    │   ├── Footer.astro    # Global responsive footer
    │   ├── Header.astro    # Global sticky navigation header
    │   └── ThemeToggle.astro # Dark/light mode switcher
    ├── layouts/
    │   └── BaseLayout.astro # Root document layout
    ├── pages/
    │   ├── 404.astro       # Error page
    │   ├── about.astro     # About page example
    │   └── index.astro     # Homepage with hero, features, and component showcase
    └── styles/
        └── global.css      # CSS variables, reset, typography, and utility classes
```

---

## Using as a GitHub Template Repository

### Step 1: Mark as Template on GitHub
1. Push this repository to GitHub (e.g. `your-user/astro-bun-starter`).
2. Go to **Settings** > **General** on the GitHub repository.
3. Check the box **"Template repository"**.

### Step 2: Create a New Website Project
For each new website:
1. Click the green **"Use this template"** button on GitHub and choose **"Create a new repository"**.
2. Give your new project its own repository name (e.g. `client-acme-website`).
3. This creates a separate project repository with a **clean, independent Git history**.
4. Clone the new repository to your machine:
   ```bash
   git clone git@github.com:your-user/client-acme-website.git
   cd client-acme-website
   ```
5. Verify dependencies using the frozen lockfile:
   ```bash
   bun install --frozen-lockfile
   ```
6. Copy `.env.example` to `.env` and set the production site domain:
   ```bash
   cp .env.example .env
   ```
7. Only add project-specific dependencies when required (e.g., UI libraries or backend SDKs):
   ```bash
   bun add <package-name>
   ```
8. Commit only project source files and configuration. Never commit `node_modules`, `.env`, or credential files (pre-configured in `.gitignore`).

---

## Customization Guide

### Design Tokens
Edit `src/styles/global.css` to update:
- `--color-primary`, `--color-accent`
- Background and surface colors for light and dark themes
- Typography fonts, line-heights, and scale
- Spacing, border radiuses, and shadow elevations

### SEO & Site URL
- Update `site` in `astro.config.mjs` or set `PUBLIC_SITE_URL` in your production environment variables.
- Pass custom `title`, `description`, `image`, and `canonicalURL` props into `<BaseLayout>` on each page.
