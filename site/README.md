# Intrepid Media — Client Invoice Pages

## Structure

```
your-repo/
├── robots.txt                          ← ADD to repo root (blocks /clients/ from search)
├── clients/
│   ├── index.html                      ← Redirects to main site
│   ├── familia-grove/
│   │   ├── index.html                  ← Redirects to main site
│   │   └── IM-2026-003.html            ← Invoice page
│   ├── next-client/
│   │   ├── index.html                  ← Copy redirect template
│   │   └── IM-2026-004.html            ← Next invoice
│   └── ...
```

## Deploying

1. Copy the `clients/` folder into your GitHub Pages repo root
2. Merge `robots.txt` with your existing one (add the `Disallow: /clients/` line)
3. Push to your deploy branch
4. Share the direct URL with your client:
   **`https://intrepidmedia.co/clients/familia-grove/IM-2026-003.html`**

## Adding Future Invoices

1. Create a new folder: `clients/{client-slug}/`
2. Drop a redirect `index.html` in it (copy from any existing client folder)
3. Name the invoice file with its number: `IM-2026-004.html`
4. Push and share the URL

## Security Model

- **Unlisted**: No links from main site, nav, or sitemap
- **noindex**: Every invoice has `<meta name="robots" content="noindex, nofollow">`
- **robots.txt**: Blocks entire `/clients/` path from crawlers
- **Redirects**: Browsing `/clients/` or `/clients/familia-grove/` redirects home

Someone would need the exact URL to access an invoice. For most client work this is sufficient.
If you ever need tighter access control, Cloudflare Access (free) can gate the path behind email verification.

## Naming Convention

- **Folders**: lowercase, hyphenated client name → `familia-grove`, `acme-corp`
- **Files**: Invoice number → `IM-2026-003.html`
- **URLs**: `intrepidmedia.co/clients/{client}/{invoice}.html`
