# Wes Shelton | Portfolio Site

Source for my portfolio site, published with GitHub Pages.

**Live site:** https://automater89.github.io/Agent-Showcase/

The site connects my experience to three kinds of roles: AI enablement, HR and benefits technology, and benefits operations. Visitors pick a view, and the site reorders the same set of case studies for that audience. The facts don't change between views.

## How the content is labeled

Each example is labeled so it's clear what kind of work it was:

- **Workplace project or program:** work I did in a job, described at the scope I can support.
- **Workplace contribution:** part of a team effort, not something I owned.
- **Experience summary:** recurring work, not a single product.
- **Portfolio example:** independent projects in my other repos. These are not production deployments.

Workplace figures appear only where they're program measures I can stand behind, and each case study includes a short "Scope of this example" note. No employer screenshots, diagrams, or internal materials are included.

## Technical notes

- One static `index.html` with inline CSS and plain JavaScript. No build step and no tracking.
- Responsive from phone to desktop width.
- Accessibility: semantic landmarks, visible keyboard focus, labeled controls, and reduced-motion support.

## Run locally

```bash
git clone https://github.com/Automater89/Agent-Showcase.git
cd Agent-Showcase
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Contact

- LinkedIn: https://www.linkedin.com/in/wallace-shelton-559b0364
- Email: wshelton89@gmail.com
- Plymouth, MI
