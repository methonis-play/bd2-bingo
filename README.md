# Brown Dust 2 Bingo for GitHub Pages

This is a static GitHub Pages site that generates a Brown Dust 2 themed bingo card.

## Features

- Generates a shareable bingo card from a URL card ID
- Click squares to mark / unmark them during a stream or live event
- Share either:
  - the card only, or
  - the card **plus current marks**
- Works as a plain static site on GitHub Pages
- Includes links to official Brown Dust 2 media pages

## Files

- `index.html` - the whole app
- `.nojekyll` - tells GitHub Pages to serve the site as-is

## Publish on GitHub Pages

1. Create a new GitHub repository.
2. Upload all files from this folder into the root of the repository.
3. Commit the files.
4. In GitHub, open **Settings** for the repository.
5. Open **Pages**.
6. Under **Build and deployment**, set:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
7. Save.
8. Wait for GitHub Pages to publish the site.

Your site URL will usually look like:

`https://YOUR-USERNAME.github.io/REPO-NAME/`

## How links work

### Share a card

A card is identified by the `card` query parameter:

`https://YOUR-USERNAME.github.io/REPO-NAME/?card=abc12345`

Anyone opening that link sees the same bingo card.

### Share a card with current marked squares

Marked squares are stored in the `marks` query parameter:

`https://YOUR-USERNAME.github.io/REPO-NAME/?card=abc12345&marks=0-3-7-12`

That reproduces the same card and the same marked squares.

## Theme / assets

This version uses publicly accessible Brown Dust 2 branding references:

- official site favicon for the app icon
- official media page link
- official digital goodies / wallpaper pages for inspiration and references

If you want to add more direct background artwork later, make sure the asset is allowed to be hotlinked or download it and place it inside the repository yourself.

## Customizing entries

Open `index.html` and edit the `ENTRIES` array in the script section.

## Notes

This app does not require a server, database, or build step.
