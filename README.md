# Agent Showcase — Wes Shelton

A single-page, recruiter-facing portfolio site for **Wes Shelton**, IT Project Manager and AI Agent Architect, hosted directly from this repository via GitHub Pages.

> **Live site:** https://automater89.github.io/Agent-Showcase/

The showcase is the storefront for an enterprise AI-agent portfolio built inside the Microsoft 365 / Copilot ecosystem. It is designed to give recruiters and hiring managers a five-minute read of what Wes builds, why it matters, and the outcomes it produces.

---

## What this repo is

- A static, dependency-free `index.html` published with GitHub Pages (`.nojekyll`).
- One file, hand-authored HTML/CSS/JS — no build step, no framework, no tracker.
- Content covers a portfolio of AI agents (SmartDeck, Project Intelligence, PMO governance assistant, HR/Legal/Learning helpers, etc.), grouped by business domain with a journey timeline and a contact CTA.

If you are reading this on GitHub: open the live site for the intended experience. If you are reading this as a recruiter doing a code review: keep scrolling — the "How recruiters should evaluate this" section below is for you.

## What it demonstrates

This repository is itself a small piece of proof-of-work. It demonstrates:

- **AI-workflow design.** Translating real, repetitive knowledge work (slide-building, policy lookups, PM risk reviews, HR/Legal triage) into Copilot Studio agents with measurable outcomes.
- **Portfolio storytelling.** Organising 40+ agents into domains, surfacing the highest-impact ones, and tying each to an outcome a non-technical executive can read in one line.
- **Enterprise enablement & governance.** A timeline that ends in formal agent governance (compliance, security, policy review) — not a tech demo.
- **M365 / Copilot fluency.** Visible stack: Microsoft Copilot, Copilot Studio, Power Automate, SharePoint, Teams, M365, OneDrive, Outlook, Power BI, Azure, Salesforce, SCORM.
- **Documentation & adoption mindset.** Clear language, accessible markup (semantic landmarks, ARIA labels, `prefers-color-scheme`, reduced-motion respect), and a CTA that invites a conversation rather than a download.

## Stack

| Layer        | Choice                                                    |
| ------------ | --------------------------------------------------------- |
| Hosting      | GitHub Pages (static, `.nojekyll`)                        |
| Markup       | Hand-authored semantic HTML5                              |
| Styling      | Modern CSS (custom properties, `clamp()`, `oklch()`, light/dark themes via `data-theme` + `prefers-color-scheme`) |
| Interactivity| Vanilla JS — domain filter tabs, animated counters, modals, intersection-observer reveals |
| Type / Icons | Google Fonts (Instrument Serif, DM Sans), Lucide, simpleicons CDN |
| Build        | None. The file is the artifact.                           |

The "no build step" choice is deliberate: a recruiter, an interviewer, or a future Wes can clone and edit a single file. That matches how the underlying agent work is built — close to the user, low ceremony, easy to hand off.

## Featured work (on the site)

- **SmartDeck 2.0** — converts notes/bullets into branded PowerPoint decks. Flagship of the portfolio; ~1,457 conversions/yr in pilot, ~7,285 hours/yr saved, ~158% projected Year-1 ROI.
- **Project Intelligence Agent** — multi-perspective risk and recommendation engine for IT PMs.
- **PMO Governance Assistant** — portfolio-health, resource-conflict, and milestone tracking for a North America IT PMO.
- **Domain agents** — IT helpdesk, HR, Legal, and Learning enablement.
- **Agent Governance Phase 1** — formal compliance / security / policy rollout across the agent estate.

> All numbers shown on the site are described as **projected** or **in active deployment / pilot**, not retrospective audited results. Read them as portfolio scope, not financial claims.

## How recruiters should evaluate this

Suggested five-minute pass:

1. **Open the [live site](https://automater89.github.io/Agent-Showcase/).** Skim the hero, the Top-Rated Agents grid, and the Journey timeline.
2. **Click into one agent card.** Look at how the problem is framed, the capabilities listed, and the outcome stated. That framing is the same shape Wes uses with business stakeholders.
3. **Check the timeline.** It moves from a single proof-of-concept → portfolio expansion → multi-agent architecture → enterprise governance. The arc matters more than any single agent.
4. **Review this `index.html`.** It is one file. Look for: semantic landmarks, accessible color tokens, reduced-motion handling, light/dark theming, no third-party trackers.
5. **Reach out.** Contact links are at the bottom of the live site.

What this repo is **not** trying to demonstrate: production frontend engineering at scale, framework expertise, or a code sample for a senior IC SWE role. It is a portfolio surface — the engineering work lives inside Copilot Studio, Power Automate, and the M365 tenant where the agents run.

## Where the deeper artifacts live

The agents themselves are tenant-internal and cannot be open-sourced. Cross-repo showcase content (sanitised case studies, redacted flow exports, governance templates, adoption playbooks) belongs in sibling repos under the same GitHub account, linked from the live site as they come online. Suggested layout:

- `Automater89/Agent-Showcase` *(this repo)* — the storefront.
- `Automater89/agent-case-studies` — long-form, redacted write-ups (problem → design → outcome).
- `Automater89/copilot-studio-patterns` — reusable prompt patterns, topic structures, governance checklists.
- `Automater89/power-automate-recipes` — sanitised flow exports and adoption snippets.

Until those exist, this repo is the single source of truth and links should land here.

## Local development

```bash
# Clone
gh repo clone Automater89/Agent-Showcase
cd Agent-Showcase

# Serve locally — pick whichever you have
python3 -m http.server 8000
# or
npx --yes serve .
```

Then open http://localhost:8000.

Editing is direct: change `index.html`, refresh the browser. Agent cards are populated from a JS array near the bottom of the file — adding an agent is one object literal.

## Suggested repo settings

For the recruiter surface to work, the GitHub repo itself needs to be findable and well-labelled:

- **Description:** "Recruiter-facing portfolio for Wes Shelton — AI Agent Architect & IT Project Manager. M365 / Copilot Studio."
- **Website:** `https://automater89.github.io/Agent-Showcase/`
- **Topics:** `portfolio`, `ai-agents`, `copilot-studio`, `microsoft-365`, `power-automate`, `it-project-management`, `ai-workflow`, `enterprise-enablement`, `process-automation`, `github-pages`
- **Pinned on profile:** yes.
- **Pages:** Deploy from `main` / root.
- **Social preview image:** add one (the hero image from the site works).

## Contact

- **Site:** https://automater89.github.io/Agent-Showcase/
- **LinkedIn:** https://www.linkedin.com/in/wallace-shelton-559b0364
- Email and other contact paths are on the live site.
