# Dongwoong Seo — Academic Website

Plain HTML/CSS, no build step. Replicates the previous Google Sites layout: **Home / Research / CV**.

## Files
- `index.html` — Home (photo, bio, news)
- `research.html` — Working papers
- `cv.html` — Link to CV
- `assets/` — put your headshot and CV PDF here once you're ready to self-host them
- `.nojekyll` — tells GitHub Pages to serve the files as-is

## Before you publish — three things to check

1. **Photo.** `index.html` currently hotlinks the photo from your old Google Sites page (its `lh3.googleusercontent.com` URL). It works for now, but it's not under your control and could break later. Download the image, save it as `assets/photo.jpg`, and change the `<img src="...">` in `index.html` to `assets/photo.jpg`.

2. **Research links.** A few "Draft" / "Slides" labels aren't linked yet — they're marked `<!-- TODO -->` in `research.html`. Also: the "Slides" link on the bracket-creep paper points to a file named `dwseo_thesis.pdf`. Double-check that's really the slides and not your thesis draft before this goes live.

3. **CV hosting.** `cv.html` links to Google Drive. That's fine, but a PDF sitting in `assets/Seo_CV.pdf` and linked with a relative path is one less thing that can go wrong (no Drive sharing settings to worry about). Swap it in whenever convenient.

## Publish with GitHub Pages

1. Create a new repo on GitHub.
   - For a site at `https://<username>.github.io` (clean root URL — recommended for a personal site), the repo must be named exactly `<username>.github.io`.
   - For a site at `https://<username>.github.io/<reponame>`, any repo name works.
2. Add these files to the repo's default branch (drag-and-drop on github.com works fine, or `git push`).
3. On GitHub: **Settings → Pages → Source → Deploy from a branch → `main` / `(root)`** → Save.
4. Wait about a minute, then visit the URL from step 1.
5. *(Optional)* Custom domain: add a `CNAME` file containing your domain, then point your domain's DNS at GitHub Pages.

## Preview locally

Just double-click `index.html` (or open it in a browser) — everything is self-contained, no server needed.
