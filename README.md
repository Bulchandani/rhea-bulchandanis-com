# rhea.bulchandanis.com

Static landing page for Rhea Bulchandani — creator, filmmaker, writer, performer. Single `index.html`, no build step.

## Deploy

```bash
git init
git add .
git commit -m "Initial site"
gh repo create Bulchandani/rhea-bulchandanis-com --public --source=. --remote=origin --push
```

Then in Cloudflare:
1. **Workers & Pages → Create application → Pages → Connect to Git** → pick the repo
2. Build settings: framework preset `None`, build command empty, output dir empty → **Save and Deploy**
3. **Custom domains → Add `rhea.bulchandanis.com`** → Cloudflare auto-creates the CNAME (since DNS is on Cloudflare) → SSL provisions

## Update

Edit `index.html`, push to `main`, Cloudflare auto-deploys in ~30 seconds.
