# The Techbro Dictionary

A Comprehensive & Definitive Guide to Modern Corporate Jargon, LinkedIn Vernacular &
Startup-Industrial Complex Terminology. Peer-reviewed by absolutely no one.

**Live site:** https://top-shelf-steve.github.io/tss-techbro/

The whole thing is a single, dependency-free `index.html` (HTML + CSS + JS, with the
term entries as an inline JavaScript array). No build step, no frameworks — open the
file in a browser and it just works.

## How to add or edit a term

1. Open `index.html` and find the `const entries = [` array near the bottom.
2. Add an object in the same shape as its neighbors:

   ```js
   { term: "Synergy", pos: "n.", def: "The definition…", ex: "“An example sentence.”" },
   ```

   - `term` — the word or phrase
   - `pos` — part of speech (`n.`, `v.`, `adj.`, etc.)
   - `def` — the definition
   - `ex` — an example usage (entries sort and group alphabetically by `term`)

3. Commit and push to `main`.

That's it — the **Deploy to GitHub Pages** GitHub Action redeploys the site
automatically on every push to `main` (usually live within a minute).

## One-time setup

GitHub Pages must be pointed at the Actions workflow once: in the repo's
**Settings → Pages**, set **Source = GitHub Actions**.

## Files

- `index.html` — the site (everything lives here)
- `techbro-dictionary.pdf` — archived PDF edition (kept in the repo, not linked from the site)
- `.github/workflows/deploy.yml` — the auto-deploy workflow
