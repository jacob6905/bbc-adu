# BBC ADU Deployment

## Current Cloudflare Pages Site

- Project: `bbc-adu`
- Live preview: `https://27ace8e9.bbc-adu.pages.dev`
- Production branch: `main`
- Publish directory: `public`

## Custom Domain

Cloudflare Pages has these domains attached:

- `bbcadu.com`
- `www.bbcadu.com`

Both are pending DNS verification. Cloudflare currently reports: `CNAME record not set`.

In SpaceShip DNS, add or update:

| Host | Type | Value |
| --- | --- | --- |
| `@` | `CNAME` or `ALIAS/ANAME` | `bbc-adu.pages.dev` |
| `www` | `CNAME` | `bbc-adu.pages.dev` |

If SpaceShip does not allow `CNAME` at `@`, use its `ALIAS`, `ANAME`, or flattened CNAME option for the root domain. If that is not available, connect the domain by changing nameservers/DNS hosting to Cloudflare.

## GitHub Setup

Create an empty GitHub repo named `bbc-adu` under `jacob6905`, then run:

```powershell
git remote add origin https://github.com/jacob6905/bbc-adu.git
git push -u origin main
```

After that, connect the GitHub repo in Cloudflare Pages:

- Framework preset: None
- Build command: empty
- Build output directory: `public`
- Production branch: `main`
