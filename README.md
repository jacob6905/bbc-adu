# BBC ADU

Static landing page for BBC ADU, a local ADU-focused construction company established in March 1996.

## Project Structure

- `index.html` and `styles.css` are the editable source for the main landing page.
- `assets/` stores source image assets.
- `themes.html` and `themes.css` are the internal color-theme review board.
- `public/` is the production publish folder for Cloudflare Pages.

## Deployment

Cloudflare Pages project: `bbcadu`

Current production publish directory: `public`

Manual deploy command:

```powershell
npx.cmd wrangler pages deploy public --project-name bbcadu --branch main
```

When updating the main site, copy the changed production files into `public/` before deploying.
