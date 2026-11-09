# TSH Studios website — tshstudios-site

Static site for TSH Studios (3D printing studio). No build step, no database.
Plain HTML/CSS/JS: `index.html` (home: who we serve, three lanes, daily
living, Fleetframe + stack builder, files, custom, pledge, FAQ) and
`tsh-products.html` (the Time Strong Health shelf: fitness products, clinic
products, personalized merch). Logo SVGs and product photos in `assets/`.

## Live deployment (2026-11-08)

Deployed by Merlin via the Vercel connector — project **tsh-studios**
(prj_YudMMYFhTuHJyOkZm9K5fv0kaVUQ) in Hector's Vercel account, production:
**https://tsh-studios.vercel.app** (no custom domain yet, by Hector's call).
Redeploy = upload changed files and create a new deployment on the same
project. Note: the connector passes file contents as command arguments, so
keep individual files under ~90 KB (the product photos are web-compressed
for this reason; full-res originals live in Hector's photo files).

## Attach tshstudios.com (when Hector buys it at Porkbun)

1. In the Vercel project: Settings → Domains → add `tshstudios.com` and
   `www.tshstudios.com`.
2. At Porkbun (Domain → DNS), point the domain at Vercel using the exact
   values Vercel shows on that Domains screen — typically:
   - A record, host `@` → `76.76.21.21`
   - CNAME, host `www` → `cname.vercel-dns.com`
   If Vercel displays different values, Vercel's win.
3. Wait for the SSL certificate to issue (automatic, a few minutes).

## Notes

- Contact buttons use `hello@tshstudios.com` — live once the Google Workspace
  for tshstudios.com exists.
- Storefront CTAs are launch-list mode until the Etsy shop opens; swap the
  hero/contact buttons to the Etsy URL at launch.
- The rack line is branded **Fleetframe** (Hector's pick, 2026-11-08, after
  RackStack / ClusterCrate / HexStack / Stackforge / Modulair / Hiveframe all
  failed collision checks). Known neighbors, different industries: a
  truck-banner frame product also called FleetFrame, and an acquired Dutch
  telematics firm. No use in 3D printing / computer hardware; fleetframe.com
  is a parked for-sale domain (not needed — the line lives on tshstudios.com).
  Social handles were not verifiable by search; confirm at account creation,
  fallbacks @fleetframeracks / @getfleetframe.
- If a real waitlist/order form is wanted later, Supabase is the planned
  backend; v1 deliberately has none.
