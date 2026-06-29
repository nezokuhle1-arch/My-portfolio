# Nezokuhle Tshukulwana — Personal Portfolio

This is my personal portfolio website, built as part of a web development assignment called **"Clone Your Future"**. The idea behind the assignment was simple: build something you'd actually be proud to send to a company. Not a throwaway school project, but a real portfolio that evolves as your skills do.

So that's exactly what I set out to do.

---

## 🧠 How We Approached the Build

Rather than jumping straight into code, I planned every section before writing a single line. Each section was broken down into its components, Bootstrap classes, custom CSS needed, and design decisions — then built one step at a time. After each section was working correctly, I committed it to GitHub before moving on. This kept the build clean, organised, and easy to debug.

The build order was:

1. Scaffolding — HTML skeleton, CDN links, CSS variables
2. Navbar
3. Hero Section
4. About Me
5. Projects Grid
6. Contact Section
7. Footer
8. Dark Mode (bonus)

---

## 🎨 Design Philosophy

The design direction I chose was **neomorphism** — a style that sits between flat design and skeuomorphism. Instead of harsh shadows or completely flat cards, neomorphism uses soft, dual-tone shadows that make elements look like they're gently pressed into or raised out of the background surface. It gives the page a tactile, premium feel without being heavy or cluttered.

### Colour Palette

The main colours were chosen deliberately:

| Role | Colour | Hex |
|---|---|---|
| Page background | Soft blue-grey | `#eaf0f7` |
| Card surface | Lighter blue-grey | `#f0f4fa` |
| Primary accent | Electric blue | `#2f7de1` |
| Accent dark | Deep blue | `#1a5fbf` |
| Accent light | Pale blue tint | `#dbeafe` |
| Body text | Dark navy | `#1e2a3a` |
| Muted text | Cool grey | `#6b7a8d` |
| Footer background | Deep navy | `#1e2a3a` |

The blue was chosen because it communicates trust, technology, and professionalism — which felt right for a web developer and entrepreneur's portfolio. The soft grey backgrounds give the neomorphic shadows room to breathe. If the background were pure white, the shadows wouldn't work at all.

### Typography

The entire site uses **Inter** — a modern, geometric sans-serif designed specifically for screens. It's clean, highly legible at all sizes, and has excellent weight variety from 400 right up to 900. The hero headline uses `font-weight: 900` with `clamp()` sizing so it scales smoothly from a 360px phone screen all the way to a 4K monitor without any media query hacks.

### The Navbar

One of the first design decisions was making the navbar a **floating pill** rather than a traditional full-width bar. It sits centred at the top of the page with a frosted glass backdrop filter, giving it a modern, elevated look. The active link uses a small blue pill highlight — a bubble around the active item — which felt more consistent with the pill navbar theme than a simple underline would have.

The logo is a custom 3D metallic coin with my initials **NT**, generated to match the silver/grey tones of the overall palette.

### Hero Section

The hero background is a custom AI-generated image featuring glass morphism shapes in blue and purple. This was a deliberate choice — the glass shapes mirror the neomorphism style of the rest of the page, and the blue and purple tones tie directly into the colour palette. Rather than a heavy dark overlay that would kill the image's beauty, I used a radial gradient overlay that's darker in the centre (where the text sits) and lighter toward the edges, letting the glass shapes glow through.

### Projects

The projects grid was one of the most important sections to get right since it carries the most marks. Cards use `col-sm-6 col-lg-4` to give 3 columns on large screens, 2 on medium, and 1 on mobile. Every card has a consistent image height with `object-fit: cover` so no image ever stretches or squashes regardless of its original dimensions. Cards lift slightly on hover with a smooth transform and shadow transition.

The projects shown are a mix of real-world work and course assignments:

- **Elev8U** — An AI-powered freelancer marketplace I built connecting skilled South Africans with clients. Live at elev8u.co.za.
- **Be At Your Service** — A business services website for a company helping SADC entrepreneurs open FNB accounts and register companies in South Africa.
- **Me, Myself & I** — A fashion brand e-commerce store currently in development.
- **DENGINE** — A website for a petroleum company, currently in development.
- **Tesla Clone** — A recreation of the Tesla landing page, built as a Zaio course assignment.
- **Netflix Clone** — A recreation of the Netflix homepage, built as a Zaio course assignment.
- **YouTube Clone** — A recreation of the YouTube homepage, built as a Zaio course assignment.

### Contact Section

The contact form uses HTML5 native validation only — `required` attributes and `type="email"` — no JavaScript, no backend. Every input has a proper `<label>` tied to it via matching `for` and `id` attributes for full accessibility. The inputs use an inset neomorphic shadow so they look pressed into the surface, contrasting with the raised card around them.

---

## 🌙 Bonus — Auto Dark Mode

The entire site switches to dark mode automatically based on the user's operating system preference using `@media (prefers-color-scheme: dark)`. This was implemented using CSS custom properties — every colour on the site is defined as a variable in `:root`, and the dark mode block simply overrides those variables. No JavaScript required. The dark mode palette swaps the light blue-greys for deep navy tones while keeping the blue accent bright and readable.

---

## ♿ Accessibility

Accessibility wasn't an afterthought — it was built in from the start:

- A **skip-to-content** link is the first element in the page for keyboard users
- All images have descriptive `alt` text
- All form inputs have associated `<label>` elements
- `aria-required`, `aria-label`, and `aria-current` are used throughout
- `:focus-visible` styles ensure keyboard navigation is always visible
- `@media (prefers-reduced-motion: reduce)` disables all transitions for users who prefer it

---

## 🛠 Tech Stack

- **Bootstrap 5.3** — CSS only via CDN, no JavaScript
- **Bootstrap Icons 1.11** — via CDN
- **Google Fonts** — Inter (400, 500, 600, 700, 800, 900)
- **Vanilla HTML5 + CSS3**
- **CSS Custom Properties** for theming and dark mode
- No frameworks, no build tools, no JavaScript

---

## 📂 File Structure

```
portfolio/
├── index.html                      ← Single HTML file, all sections
├── styles.css                      ← All custom styles, variables, dark mode
├── README.md                       ← This file
└── assets/
    └── images/
        ├── logo.png                    ← Custom 3D metallic NT coin logo
        ├── hero-bg.png                 ← AI-generated glass morphism background
        ├── profile.jpg                 ← Profile photo
        ├── elev8u.png                  ← Elev8U project screenshot
        └── be-at-your-service.png      ← Be At Your Service screenshot
```

---

## 🖼 Image Credits

| Image | Source |
|---|---|
| Hero background | AI-generated (personal use) |
| NT Logo | AI-generated (personal use) |
| Elev8U screenshot | Own project — elev8u.co.za |
| Be At Your Service screenshot | Own project |
| MMAI placeholder | Unsplash — free licence |
| DENGINE placeholder | Unsplash — free licence |
| Tesla Clone placeholder | Unsplash — free licence |
| Netflix Clone placeholder | Unsplash — free licence |
| YouTube Clone placeholder | Unsplash — free licence |

---

## 🚀 Deployment

Deployed via **Netlify** — drag and drop deployment, no configuration needed.

Live link: *https://nezzy-ai.netlify.app/*

GitHub repo: [github.com/nezokuhle1-arch](https://github.com/nezokuhle1-arch)

---

*Built by Nezokuhle Tshukulwana · Zaio Web Development Course · 2026*