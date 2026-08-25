# Rahul Vinod — Portfolio

Personal portfolio site for **Rahul Vinod**, Human Capital Consultant — Total Rewards,
Organizational Design, Performance Management and HR Analytics.

🔗 **Live site:** `https://adarshbabuk.github.io/rahulPortfolio/`

---

## What's inside

A single-page, dependency-free static site:

| Section | Contents |
| --- | --- |
| Hero | Name, positioning statement, résumé download, contact links |
| About | Professional summary and an "at a glance" fact panel |
| Experience | Timeline — TIAA \| Nuveen Bank, Deloitte, Altimetrik |
| Expertise | Four practice areas plus tools and platforms |
| Education | Degrees, certifications, projects and papers |
| Beyond Work | Leadership, activities, languages, interests |
| Contact | Email, phone, LinkedIn, résumé download |

**Features:** light/dark theme with OS detection and `localStorage` persistence, sticky
nav with scroll-spy, scroll progress bar, reveal-on-scroll animations, a mobile menu,
print styles, and `prefers-reduced-motion` support.

## Tech

Plain HTML, CSS and JavaScript. No build step, no framework, no npm install.
The only external request is Google Fonts (Fraunces + Inter).

## Project structure

```
.
├── index.html                     # the entire page
├── assets/
│   ├── css/style.css              # design tokens + all styling
│   ├── js/main.js                 # theme, nav, scrollspy, reveal
│   ├── img/favicon.svg
│   └── Rahul-Vinod-Resume.pdf     # downloadable résumé
├── .github/workflows/deploy.yml   # GitHub Pages deployment
├── .nojekyll
└── README.md
```

## Run locally

Open `index.html` directly in a browser, or serve it:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deploy to GitHub Pages

1. Create a repository on GitHub and push this folder to it.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **GitHub Actions**.

The included workflow publishes the site on every push to `main`.

> Prefer no workflow? Set **Source** to *Deploy from a branch* → `main` / `/ (root)` instead.
> The `.nojekyll` file makes sure GitHub serves the folder as-is.

## Customising

- **Content** lives entirely in `index.html` — edit the text in place.
- **Colours, spacing and type** are CSS custom properties at the top of
  `assets/css/style.css` (`:root` for light, `[data-theme="dark"]` for dark).
  Changing `--accent` re-themes the whole site.
- **Résumé:** replace `assets/Rahul-Vinod-Resume.pdf`, keeping the filename.

---

© Rahul Vinod · [LinkedIn](https://linkedin.com/in/rahulvinod71) · [rahulvinod71@gmail.com](mailto:rahulvinod71@gmail.com)
