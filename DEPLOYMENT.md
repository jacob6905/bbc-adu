# BBC ADU Deployment

## Current Cloudflare Pages Site

- Project: `bbcadu`
- Live site: `https://bbcadu.pages.dev`
- Production branch: `main`
- Publish directory: `public`
- GitHub repo: `https://github.com/jacob6905/bbc-adu`

## Custom Domain

Cloudflare Pages has these domains attached:

- `bbcadu.com`
- `www.bbcadu.com`

Both are pending DNS verification. Cloudflare currently reports: `CNAME record not set`.

In SpaceShip DNS, add or update:

| Host | Type | Value |
| --- | --- | --- |
| `@` | `CNAME` or `ALIAS/ANAME` | `bbcadu.pages.dev` |
| `www` | `CNAME` | `bbcadu.pages.dev` |

If SpaceShip does not allow `CNAME` at `@`, use its `ALIAS`, `ANAME`, or flattened CNAME option for the root domain. If that is not available, connect the domain by changing nameservers/DNS hosting to Cloudflare.

## GitHub Setup

GitHub is connected as the source repo:

- Repo: `jacob6905/bbc-adu`
- Branch: `main`
- Cloudflare Pages project: `bbcadu`

Cloudflare Pages build settings:

- Framework preset: None
- Build command: empty
- Build output directory: `public`
- Production branch: `main`
