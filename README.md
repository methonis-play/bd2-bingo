# Bingo Card Generator for GitHub Pages

This is a static bingo-card web app designed to be hosted on **GitHub Pages**.

## What it does

- Generates a new bingo card when you click **New Card**
- Uses a **shareable card ID** in the URL, like `?card=abc12345`
- Recreates the same card when someone opens the same link
- Supports **Copy Share Link** and **Print**
- Requires **no backend** and **no database**

## Files in this package

- `index.html` — the full app
- `.nojekyll` — tells GitHub Pages to serve the site as-is
- `README.md` — these instructions

## Publish on GitHub Pages

### Option A: Upload through the GitHub website

1. Create a new GitHub repository.
2. Upload `index.html`, `.nojekyll`, and `README.md` to the root of the repository.
3. In the repository, go to **Settings** → **Pages**.
4. Under **Build and deployment**, set:
   - **Source** = `Deploy from a branch`
   - **Branch** = `main`
   - **Folder** = `/ (root)`
5. Save.
6. Wait for GitHub Pages to publish your site.

Your site URL will usually look like:

- `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`

### Option B: Push with git locally

```bash
git init
git add .
git commit -m "Initial bingo card site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Then enable Pages in **Settings** → **Pages** using the `main` branch and `/ (root)` folder.

## How sharing works

The app stores the card ID in the URL query string:

- `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/?card=abc12345`

That `card` value is used as a deterministic seed, so the same ID always produces the same card.

## Customizing entries

Open `index.html` and edit the `ENTRIES` array.

You can also adjust the `SHORTEN_OVERRIDES` object to control how long phrases are shortened in squares.

## Notes

- This project is intentionally static and simple.
- If you later want multiple boards, user-submitted entries, saved sessions, or analytics, you can still keep GitHub Pages and add a small backend later.
