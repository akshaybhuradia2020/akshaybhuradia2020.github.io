# Portfolio & LinkedIn guide (Akshay Bhuradia)

Quick reference for this site, what changed, and how to keep **GitHub Pages** and **LinkedIn** in sync.

---

## Live links

| What | URL |
|------|-----|
| **Portfolio (GitHub Pages)** | https://akshaybhuradia2020.github.io/ |
| **GitHub repo** | https://github.com/akshaybhuradia2020/akshaybhuradia2020.github.io |
| **LinkedIn profile** | https://www.linkedin.com/in/akshaybhuradia/ |
| **GitHub** | https://github.com/akshaybhuradia2020 |

---

## Deploy / update website

GitHub Pages deploys automatically when you push to `main`. No separate redeploy step.

```bash
cd /Users/akshaybhuradia/portfolio_akshaybhuradia

git status
git add index.html styles.css script.js   # add files you changed
git commit -m "Describe your change"
git push origin main
```

Wait 1–3 minutes, then hard refresh the site (Cmd+Shift+R).

**If push fails (403):** log in as `akshaybhuradia2020`:

```bash
gh auth switch -u akshaybhuradia2020
gh auth setup-git
```

---

## Site structure

| File | Purpose |
|------|---------|
| `index.html` | Content: hero, about, experience, skills, contact |
| `styles.css` | Theme (violet/cyan), layout, company link styles |
| `script.js` | Theme toggle, menu, scroll reveal, copy email/phone |

---

## Changelog (recent updates)

### Experience narrative (EthicalHat → MadeCard)

- **MadeCard (Aug 2026 – Present):** Direct full-time employee.
- **EthicalHat (Mar 2024 – Jul 2026):** Employed by EthicalHat; backend work for **client MadeCard** under EthicalHat’s services agreement. Resigned Jul 2026; joined MadeCard directly from Aug 2026.

### Company website links (Experience section)

| Company | Link |
|---------|------|
| MadeCard | https://www.madecard.com/ |
| EthicalHat | https://www.ethicalhat.com/ |
| Vylt Technologies | https://vylt.in/ |
| Nebularc Technologies | https://nebularc.com/home |
| Dynapt Solutions | https://www.dynapt.com/ |

### Contact

- **Email:** akshaybhuradia25@gmail.com  
- **Phone:** +91-9716414797 (`tel:+919716414797`)  
- Copy buttons for email and phone in Contact section  
- Phone also listed under About → Quick facts  

### LinkedIn URL on site

Contact → LinkedIn points to: `https://www.linkedin.com/in/akshaybhuradia/`

### Theme

- Violet/cyan dark/light theme (see `styles.css` tokens).

---

## LinkedIn checklist (manual — not on the website)

### Headline (example — broaden beyond payments only)

```
Senior Backend Engineer | Python · Node.js · AWS | Card · Onboarding · Integrations | Production systems
```

### Experience dates (important)

| Role | Dates |
|------|--------|
| MadeCard — Backend Engineer, **direct** | **Aug 2026 – Present** |
| EthicalHat — Software Engineer, **client MadeCard** | **Mar 2024 – Jul 2026** |

Do **not** start MadeCard at Apr 2024 unless that was direct employment (your story: consulting via EthicalHat first).

### Profile additions

1. **Contact info** → Website → portfolio URL  
2. **Featured** → link to portfolio (and optionally GitHub)  
3. **Skills** → pin Python, PostgreSQL, AWS, Node.js, etc.  
4. **Banner** → use a **1584×396** (or `*-504.png`) file — see below  

### Company URLs on LinkedIn

When editing each role, attach or link the same company URLs as on the portfolio (LinkedIn company pages where available).

---

## LinkedIn banner files (local only — not deployed unless you add them)

| File | When to use |
|------|-------------|
| `linkedin-banner-blue-504.png` | Simple text, fills LinkedIn crop editor |
| `linkedin-banner-illustrated-504.png` | Illustrated style, taller export |
| `linkedin-banner-blue.png` | Text-only, exact 1584×396 |
| `linkedin-banner.svg` / `linkedin-banner-blue.svg` | Edit text, then export PNG (see below) |

**Avoid uploading:** `linkedin-banner-fintech.jpg` (wrong aspect ratio — grey bars in crop UI).

**Preview:** open `linkedin-banner.html` in a browser.

**Export SVG to PNG (after editing `.svg`):**

```bash
rsvg-convert -w 1584 -h 396 linkedin-banner-blue.svg -o linkedin-banner-blue.png
```

*(Requires `librsvg`: `brew install librsvg`.)*

### Banner text themes (for reference)

- Payments (**Column Bank**), card issuing, onboarding (Taktile, Socure, TransUnion)  
- Reporting, live streaming (career), production & bug fixing  
- Stack: Python, Node.js, PostgreSQL, Redis, AWS (no Docker on banner)  

---

## How to edit common content

### New bullet under MadeCard

Edit `index.html` → search for `MadeCard` → add `<li>...</li>` in that job’s `<ul>`.

### Change phone or email

- `index.html`: Contact section + Quick facts  
- `script.js`: `copyText(...)` values for copy buttons  

### Change LinkedIn link

- `index.html`: Contact → `linkedin.com/in/akshaybhuradia/`  

---

## Suggested git commit messages

- `Update MadeCard experience bullets`  
- `Add company website links in experience`  
- `Add phone number to contact`  
- `Clarify EthicalHat consulting and direct MadeCard employment`  
- `Fix LinkedIn profile URL`  

---

## Optional next steps

- [ ] Push latest `index.html` / `styles.css` / `script.js` if not already on GitHub  
- [ ] Align LinkedIn dates with this guide  
- [ ] Add Featured + website on LinkedIn  
- [ ] Pin skills on LinkedIn  
- [ ] Upload `linkedin-banner-blue-504.png` (or preferred banner)  

---

*Last updated: November 2026*