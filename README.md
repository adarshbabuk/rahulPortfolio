# Rahul Vinod — Portfolio

Personal portfolio site for **Rahul Vinod**, Human Capital Consultant — Total Rewards,
Organizational Design, Performance Management and HR Analytics.

## Two versions

The site ships in two variants, each on its own branch, both published from a single
GitHub Pages site:

| Branch | Live URL | Difference |
| --- | --- | --- |
| `main` | <https://adarshbabuk.github.io/rahulPortfolio/> | Typography-led hero, no photograph |
| `photo` | <https://adarshbabuk.github.io/rahulPortfolio/photo/> | Adds a portrait to the hero and the nav |

Both are cross-linked in the footer, so visitors can switch between them.

`photo` branches from `main` and changes as little as possible — it adds
`assets/img/rahul-vinod.jpg` and `assets/css/photo.css`, and edits `index.html`.
`assets/css/style.css` is **identical on both branches**, so shared styling changes
merge cleanly:

```bash
git checkout photo && git merge main
```

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

Set **Settings → Pages → Source** to **GitHub Actions**.

[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) then runs on every push to
either branch. It checks out `main` into the site root and `photo` into `photo/`,
and publishes them together — so one deploy keeps both versions current.

> Using *Deploy from a branch* instead publishes only the branch you select, and the
> workflow's deploy step will fail. Pick one mode or the other, not both.

## Customising

- **Content** lives entirely in `index.html` — edit the text in place.
- **Colours, spacing and type** are CSS custom properties at the top of
  `assets/css/style.css` (`:root` for light, `[data-theme="dark"]` for dark).
  Changing `--accent` re-themes the whole site.
- **Résumé:** replace `assets/Rahul-Vinod-Resume.pdf`, keeping the filename.

---

© Rahul Vinod · [LinkedIn](https://linkedin.com/in/rahulvinod71) · [rahulvinod71@gmail.com](mailto:rahulvinod71@gmail.com)
