# In Good Company — Website

The landing page for **In Good Company**, photo booths + event experiences in Houston, TX.
Plain HTML/CSS/JS — no build step, no dependencies.

> Good photos. Good people. Good company.

## Files

| File | What it is |
|------|------------|
| `index.html` | The entire website (HTML, CSS, and JS in one file) |
| `assets/` | Logo and doodle artwork extracted from the brand guide |
| `In_Good_Company_Brand_Guide.pdf` | Source brand guide |
| `netlify.toml` | Netlify deploy config (static, no build) |
| `.gitignore` | Keeps OS/editor junk out of the repo |

## Brand reference

Pulled directly from the brand guide — keep these exact:

| Color | Hex | Role |
|-------|-----|------|
| Good Company Green | `#1F3025` | Hero background / primary |
| Warm Ivory | `#F4EBD8` | Logo, doodles, borders, paper |
| Soft Cream | `#FBF7ED` | Light backgrounds |
| Muted Sage | `#A4AA8D` | Secondary accent only |
| Ink | `#171914` | Text / near-black |

Balance is roughly **60% green / 30% ivory / 5% cream / 5% accent**.

- **Display type:** Bodoni Moda — headlines, package names, large statements
- **Supporting type:** Montserrat — body copy, pricing, FAQs, small uppercase labels (add letter spacing to short uppercase lines)
- **Voice:** warm, social, short, lightly cheeky, never corporate

### Logo files in `assets/`

| File | Use on |
|------|--------|
| `logo-horizontal.png` | Green backgrounds (site header, footer) |
| `logo-horizontal-green.png` | Ivory / cream backgrounds |
| `logo-stacked.png` | Green backgrounds — profile graphics, signage |
| `logo-stacked-green.png` | Ivory / cream backgrounds |
| `doodle.png` / `doodle-green.png` | Dancing-couple mark on its own |

These were extracted from the brand guide PDF with the green keyed out to
transparency. Per the guide, treat the logo as **artwork** — don't retype or
rebuild the lettering. Before ordering signage or large-format prints,
vectorize the approved master art rather than regenerating it.

## Before you go live — edit these

Open `index.html` and search for `EDIT:` to find every spot that needs your info:

1. **Email** — replace `hello@ingoodcompanyhtx.com` in two places: the contact block
   *and* the `TO=` line in the `<script>` at the bottom. This is where inquiry
   form submissions are sent.
2. **Phone & Instagram** — swap the placeholders in the contact block.
3. **Prices / wording** — edit freely in the Packages section.
4. **Gallery photos** — search for `GALLERY:` for how to swap the placeholder tiles.

## Deploy with GitHub + Netlify

1. **Push to GitHub** (already set up — repo: `108-photobooth`):
   ```bash
   git add .
   git commit -m "Describe your change"
   git push
   ```
2. **Connect Netlify**: in Netlify, choose *Add new site → Import an existing project*,
   authorize GitHub, and pick this repo.
3. **Build settings**: leave the build command **empty** and set the publish
   directory to `.` (the repo root). Click deploy.
4. **Done.** Netlify gives you a live URL. Every future `git push` to `main`
   automatically redeploys the site.

## Custom domain (optional)

In Netlify: *Domain settings → Add a custom domain*. You can buy a domain through
Netlify or point one you already own. HTTPS is provisioned automatically.
