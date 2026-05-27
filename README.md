# PropVal AU — Free Australian Property Valuation

> Instant market valuation estimates for any Australian property address. **Zero API costs. Zero sign-up. Completely free forever.**

---

## How it works

This is a fully client-side app — no server, no API, no costs:

1. **Parses** the address you enter to extract suburb, state and property type
2. **Looks up** a built-in database of real 2025/26 suburb median prices (sourced from Domain, Cotality/CoreLogic, REIWA, REISA etc.)
3. **Estimates** a market value range based on the suburb median ± a realistic variance band
4. **Generates** direct deep-links to Domain, realestate.com.au, SQM Research, CoreLogic and more

## Coverage

- **250+ suburbs** across all states and territories
- Sydney, Melbourne, Brisbane, Perth, Adelaide, Canberra, Hobart, Darwin
- Data sourced from: Domain, Cotality (formerly CoreLogic), REIWA, REISA, REINT, REITAS (2025–26)
- Fallback to city or national median for unlisted suburbs

## Deploy to GitHub Pages (free, 5 min)

### 1. Create a GitHub repo

Go to github.com → New repository → name it `propval-au` → set to **Public** → Create.

### 2. Push the files

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/propval-au.git
git push -u origin main
```

Or just drag-and-drop `index.html` into your repo on GitHub.

### 3. Enable Pages

Repo → **Settings** → **Pages** → Source: `main` / `/(root)` → **Save**

Live at: `https://YOUR_USERNAME.github.io/propval-au/`

## No API key needed

This app is 100% static HTML + JavaScript. There are no external API calls, no backend, no server, and no ongoing costs whatsoever. It works entirely in the browser using the embedded suburb database.

## Limitations

- Estimates are based on **suburb medians**, not the specific property's attributes (size, condition, views, renovations)
- The suburb database covers ~250 key suburbs — less common suburbs fall back to the city median
- Data reflects 2025/26 conditions and should be refreshed periodically
- Not a substitute for a formal valuation by a Certified Practising Valuer (CPV)

## Updating the data

To update suburb medians, edit the `SUBURBS` object in `index.html`. Each entry follows:
```js
'suburb-state': { h: houseMedian, u: unitMedian, g: '+X.X%', src: 'Source name' }
```

## License

MIT — free to use, modify and deploy.
