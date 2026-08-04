# Gyan Prakash Kumar — Portfolio Website

A premium, dark-themed, glassmorphic portfolio site built with pure HTML5, CSS3 and vanilla JavaScript (Bootstrap 5 for grid/utility classes, AOS for scroll animations, Typed.js for the hero role-typing effect, Font Awesome for icons).

## File structure

```
portfolio/
├── index.html                 # Single-page site: Home, About, Skills, Projects,
│                               # Experience, Education, Certifications,
│                               # Achievements, Resume, Contact
├── 404.html                   # Custom error page
├── README.md
└── assets/
    ├── css/
    │   └── style.css          # All design tokens, layout, components, animations
    ├── js/
    │   └── script.js          # Loader, particles, cursor, theme toggle, tabs,
    │                           # filters, counters, form, toasts, scroll logic
    ├── images/                # Put your profile photo / OG image here
    ├── fonts/                 # (Google Fonts are loaded via CDN — folder kept
    │                           # for any local font files you add later)
    └── icons/                 # (Font Awesome is loaded via CDN — folder kept
                                # for any custom icons/favicons)
```

## What's real vs. what needs your input

Everything in the **Skills / Projects / Experience / Education / Certifications /
Achievements** sections is built from what you provided. A few things a template
can't invent for you — placeholders are clearly marked and need to be swapped:

1. **Profile photo** — the hero currently shows a "GPK" monogram avatar instead of
   a photo (I didn't fabricate one). Drop a photo into `assets/images/` and replace
   the `.avatar-inner` div in `index.html` with an `<img>` tag.
2. **Resume PDF** — the Resume section links to
   `assets/resume-gyan-prakash-kumar.pdf`, which doesn't exist yet. Add your actual
   resume PDF at that path (or update the path in `index.html`).
3. **Real links** — GitHub, LinkedIn, project repo links, and live demo links are
   all placeholder `#` anchors and a placeholder email (`hello@example.com`).
   Search `index.html` for `href="#"` and `hello@example.com` and swap in your
   real URLs.
4. **Contact form backend** — the form validates and shows a success/error toast
   client-side, but nothing is actually sent anywhere yet (that needs a backend
   endpoint, e.g. Flask/PHP mailer or a service like Formspree). Wire the `fetch()`
   call into the `submit` handler in `script.js` once you have an endpoint.
5. **Testimonials slider** — intentionally left out. The brief asked for real,
   non-placeholder content, and there were no actual testimonials to include.
   Add a `#testimonials` section + a small slider script once you have real quotes.
6. **Domain in meta tags** — `og:url` / `canonical` currently point to
   `https://gyanprakashkumar.dev/`; update once you know your real domain.

## Features implemented

- Dark/light mode toggle (persisted via `localStorage`)
- Scroll progress bar, custom cursor, animated hamburger menu
- Canvas particle background in the hero
- Typed.js role rotation, AOS scroll-reveal animations
- Animated stat counters, animated skill progress bars with tabbed categories
- Filterable project grid (All / AI / Web / IoT)
- Client-side validated contact form with toast notifications
- Back-to-top button, responsive nav, custom 404 page
- SEO meta tags, Open Graph/Twitter cards, and Person schema markup
- Respects `prefers-reduced-motion`; visible keyboard focus states throughout

## Running it locally

No build step — just open `index.html` in a browser, or serve the folder:

```bash
cd portfolio
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploying

Works as-is on any static host: GitHub Pages, Netlify, Vercel, or Cloudflare
Pages. For GitHub Pages, the included `404.html` will automatically be served
for broken links.
