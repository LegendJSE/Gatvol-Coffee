# Beanstock — Coffee Shop Inventory (starter)

## Included
- Product catalogue for finished, ready-to-sell products
- Categories: Coffee & beverages, Sweet food, Savoury food, Other
- Current quantities, minimum stock thresholds and low/out-of-stock status
- Manual sale recording and stock receiving
- Movement history and CSV export
- JSON backup and restore
- Basic browser notification permission flow
- Responsive web app / PWA shell

## Important limitations
This is a working starter app, **not yet connected to Yoco**. It does not read Yoco POS transactions or sync between devices. The Yoco status is intentionally shown as not connected. A secure shared database, backend integration and approved Yoco POS sales-data access are required before automatic sales deductions can work reliably. Manual-amount sales need item/quantity identification.

Data in this starter is saved in the browser on the current device. Export JSON backups regularly. Do not use this starter as the sole source of truth for business stock until cloud sync, access controls and backups are implemented.

## Run locally
Open `index.html` in a browser. For PWA installation and service-worker caching, serve it over HTTPS (for example through GitHub Pages).

## GitHub Pages deployment
1. Create a GitHub repository.
2. Upload `index.html`, `manifest.webmanifest`, `sw.js`, and `README.md` to the repository root.
3. In repository Settings → Pages, deploy from the `main` branch and `/ (root)`.
4. Open the published HTTPS address on your iPhone and use Share → Add to Home Screen.

## Next production phase
1. Confirm Yoco POS App merchant integration access and available product-level sales events/endpoints with Yoco.
2. Add a secure backend and shared database (e.g. Supabase or equivalent).
3. Implement authenticated Yoco connection, webhook/polling sync as officially supported, idempotency, refund/void handling and reconciliation.
4. Add server-side push notifications, role-based staff access and audit logs.
