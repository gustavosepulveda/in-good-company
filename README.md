# 108 Photobooth — Website

The landing page for **108 Photobooth**, an open-air photo booth rental serving Houston, TX.
Plain HTML/CSS/JS — no build step, no dependencies.

## Files

| File | What it is |
|------|------------|
| `index.html` | The entire website (HTML, CSS, and JS in one file) |
| `netlify.toml` | Netlify deploy config (static, no build) |
| `.gitignore` | Keeps OS/editor junk out of the repo |

## Before you go live — edit these

Open `index.html` and search for `EDIT:` to find every spot that needs your info:

1. **Email** — replace `hello@108photobooth.com` in two places: the contact block
   *and* the `TO=` line in the `<script>` at the bottom. This is where inquiry
   form submissions are sent.
2. **Phone & Instagram** — swap the placeholders in the contact block.
3. **Prices / wording** — edit freely in the Packages section.

## Deploy with GitHub + Netlify

1. **Create a GitHub repo** and push this folder to it:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/108-photobooth.git
   git push -u origin main
   ```
2. **Connect Netlify**: in Netlify, choose *Add new site → Import an existing project*,
   authorize GitHub, and pick this repo.
3. **Build settings**: leave the build command **empty** and set the publish
   directory to `.` (the repo root). Click deploy.
4. **Done.** Netlify gives you a live URL. Every future `git push` to `main`
   automatically redeploys the site.

## Making changes later

Edit `index.html` (yourself, or with Claude Code), then:
```bash
git add .
git commit -m "Describe your change"
git push
```
The push triggers Netlify to rebuild and your live site updates automatically.

## Custom domain (optional)

In Netlify: *Domain settings → Add a custom domain*. You can buy a domain through
Netlify or point one you already own. HTTPS is provisioned automatically.
