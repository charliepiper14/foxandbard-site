# Fox &amp; Bard — Website (Staging)

Premium static marketing site for **Fox &amp; Bard**, a strategy-and-story agency.
Built as a staging mockup to host on GitHub before migrating to **foxandbard.com**.

*Strategy · Story · Impact — the fox thinks, the bard tells.*

---

## Pages (9)

| File | Purpose |
|------|---------|
| `index.html` | Home — hero, duality signature, results, services, featured work, CTA |
| `services.html` | Four disciplines (Strategy, Brand, Growth, Web) + engagement models |
| `work.html` | Case studies — real, anonymized results |
| `approach.html` | The "Field Guide" — four-stage process, principles, lexicon |
| `about.html` | Story, brand origin, values (features the real logo) |
| `contact.html` | Contact form (front-end demo) + details |
| `privacy.html` | Privacy Policy (placeholder) |
| `terms.html` | Terms &amp; Conditions (placeholder) |
| `404.html` | Not-found page |

Every page is **fully self-contained** — the CSS, JavaScript and logo wordmark are inlined into each `.html` file, so any page renders correctly on its own with no `assets/` folder. Photography loads from the Unsplash CDN; the primary logo and favicon load from your Cloudinary URL.

---

## Deploy on GitHub Pages

1. Create a repo and push these files (keep the folder structure intact).
2. **Settings → Pages → Build and deployment → Source: Deploy from a branch.**
3. Choose your branch (e.g. `main`) and the `/root` folder. Save.
4. Your site goes live at `https://<user>.github.io/<repo>/` in a minute or two.

All internal links and asset paths are **relative**, so it works from a project subpath or a root domain without changes. When you point **foxandbard.com** at it (Pages → Custom domain), everything continues to resolve.

---

## Notes before going live

- **Contact form** is a front-end demo only (no backend) — it validates and shows a success state. Wire it to your provider (Formspree, a serverless function, your CRM, etc.) before launch.
- **Legal pages** (`privacy.html`, `terms.html`) are **placeholder copy, not legal advice** — replace with professionally reviewed text.
- **Logo** is loaded from your Cloudinary URL; favicon and OG image are generated from it via Cloudinary transforms.
- **Photography** is from Unsplash (hotlinked via their CDN with `?auto=format`). Swap for owned/licensed art before launch if you prefer.
- **Fonts**: Cormorant Garamond, Manrope, Space Mono via Google Fonts.
- **Case-study figures** are real results from live accounts, shown **anonymized — client names withheld under NDA** (industries and platforms only).
- Update contact details (`hello@foxandbard.com`, phone) and social links in the footer.

---

## Tech

Hand-built HTML + CSS + vanilla JS. No build step, no dependencies.
Responsive (360px → ultrawide), accessible (skip link, focus states, reduced-motion, ARIA),
SEO/OpenGraph meta on every page. Verified zero horizontal overflow across all breakpoints.
