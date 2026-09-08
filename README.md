# Library SOP Manual

A small static website for the Department of Library and Information Science, Central University of Himachal Pradesh, presenting three Standard Operating Procedures (Acquisition, Serials Control, Circulation) with a mapping to Koha's modules for classroom use.

No build step — plain HTML/CSS/JS. This can be hosted for free on **GitHub Pages**.

## Files

```
index.html               Home page listing the SOPs
acquisition.html          Acquisition SOP
serials.html              Serials Control SOP
circulation.html          Circulation SOP
technical-processing.html Technical Processing (Cataloguing) SOP
assets/style.css          Shared stylesheet
assets/nav.js             Mobile menu toggle
docs/*.docx                Downloadable Word versions of each SOP
```

## Option A — Deploy from GitHub's website (no command line)

1. Go to [github.com](https://github.com) and sign in (create a free account if needed).
2. Click the **+** icon (top right) → **New repository**.
3. Name it, e.g. `library-sops`. Keep it **Public** (required for free GitHub Pages). Click **Create repository**.
4. On the new repo's page, click **uploading an existing file**.
5. Drag in all the files and folders from this package (`index.html`, `acquisition.html`, `serials.html`, `circulation.html`, `technical-processing.html`, the `assets` folder, and the `docs` folder), then click **Commit changes**.
6. Go to **Settings** (top tab of the repo) → **Pages** (left sidebar).
7. Under "Build and deployment" → **Source**, choose **Deploy from a branch**.
8. Under **Branch**, choose `main` and folder `/ (root)`, then **Save**.
9. Wait a minute, then refresh — GitHub will show your live URL, typically:
   `https://<your-username>.github.io/library-sops/`

Any time you want to update the site, just upload the changed file again from the repo's **Add file → Upload files** screen and commit.

## Option B — Deploy with git from the command line

```bash
cd library-sops          # the folder containing these files
git init
git add .
git commit -m "Initial SOP site"
git branch -M main
git remote add origin https://github.com/<your-username>/library-sops.git
git push -u origin main
```

Then repeat steps 6–9 above in the repo's Settings → Pages.

## Updating content later

- Edit the relevant `.html` file directly — each page is plain HTML with the text visible and easy to find.
- Shared look-and-feel lives in `assets/style.css`.
- To add a fourth SOP (e.g. Technical Processing), copy `circulation.html` as a starting template, edit its content, add a link to it in the sidebar `<nav>` block of **every** page (including `index.html`), and add a card for it on the home page.
