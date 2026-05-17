# Billy Nugraha's Personal Portfolio Website

## Overview

Single-page personal portfolio website for **Billy Nugraha Sutandi** — a Senior Robotics Software Engineer. The site showcases his robotics expertise, projects, work experience, skills, and client testimonials. It serves as both a professional portfolio and a client acquisition tool, with prominent CTAs pointing to Fiverr and direct contact.

Live at: **billynugrahas.github.io**

## Tech Stack

- **Single `index.html` file** — no build tools, no framework, no bundler
- **Tailwind CSS** via CDN (`cdn.tailwindcss.com`) with custom config inline
- **Lucide Icons** via CDN (`unpkg.com/lucide@latest`)
- **Google Fonts**: Manrope (body), Space Mono (monospace/terminal)
- **Vanilla JavaScript** — typing effect, mobile menu, tag filtering, project modals, scroll animations

## Architecture

Everything lives in `index.html`:
- `<head>`: Tailwind config, custom CSS (animations, scrollbar, grid overlay, modal styles)
- `<body>`: Semantic HTML sections + inline `<script>` at the bottom
- `assets/images/`: Profile photo, project screenshots/logos

### Page Sections (in order)

1. **Nav** — Fixed top navbar with mobile hamburger menu
2. **Hero** — Typing effect headline, terminal card (styled as ROS 2 CLI output), CTAs, social links
3. **About** — Photo, bio text, deployment stats, education, key achievements
4. **Projects** — Filterable card grid (tags: Navigation, LiDAR, Hardware, Competition) with detail modals
5. **Experience** — Timeline of 6 roles (Movel AI, Widya Robotics, Niagraha Tech, UGM, Re-link Plastics, BMKG)
6. **Skills** — 6 category cards (Languages, Robotics, Perception, Platforms, Tools, Integration)
7. **Testimonials** — 6 Fiverr client reviews with country flags and star ratings
8. **Contact** — Grid of contact links (Email, LinkedIn, GitHub, Instagram, Fiverr)
9. **Footer** — Branding, copyright, status indicator

### Key Features

- **Typing effect**: Cycles through phrases about robotics expertise
- **Tag-based project filtering**: Client-side filter with fade animations
- **Project detail modal**: Click project card to see full writeup
- **Intersection Observer**: Scroll-triggered fade-up animations
- **Responsive**: Mobile menu, responsive grid layouts
- **Terminal aesthetic**: Dark theme with neon green (#00ff00) and cyan (#00d7ff) accents, scanline overlay, grid background, noise texture

## Design System

- **Background**: `#0a0a0a` (dark-900)
- **Accent 1**: `#00ff00` (neon green) — primary CTA, highlights
- **Accent 2**: `#00d7ff` (cyan) — secondary highlights, links
- **Text**: `#e6e6e6` (primary), `#999999` (muted)
- **Surfaces**: `#111111`, `#1a1a1a`, `#1e1e1e`, `#2a2a2a`, `#333333`
- **Selection**: Green highlight on dark

## Editing Notes

- **No build step required** — edit `index.html` directly, push to `master` branch on GitHub, and GitHub Pages serves it
- **Git branching**: `master` (live), `2020-design` (old design)
- **Project data** is hardcoded in HTML (no CMS or data files)
- **Images** are in `assets/images/` — project images in `assets/images/projects/`
- When adding new projects: add an `<article>` card to `#projectsGrid` with `data-tags`, and include a `hidden .project-source` div for the modal content
- When adding testimonials: add a card to the `#testimonials` grid
- Tailwind classes are used extensively — modify the inline `tailwind.config` for theme changes
