# TSH Studios website — tshstudios-site

Static site for TSH Studios (3D printing studio). No build step, no database.
Plain HTML/CSS/JS: `index.html` (home: who we serve, three lanes, daily
living, Fleetframe + stack builder, files, custom, pledge, FAQ) and
`tsh-products.html` (the Time Strong Health shelf: fitness products, clinic
products, personalized merch). Logo SVGs and product photos in `assets/`.

## Live deployment (2026-11-08)

Project **tsh-studios** (prj_YudMMYFhTuHJyOkZm9K5fv0kaVUQ) in Hector's
Vercel account, production: **https://tsh-studios.vercel.app**. Custom
domain **tshstudios.com** was bought on Porkbun and attached to the project
on 2026-11-08 (www 308-redirects to the apex); it serves the site once
Vercel's domain verification finishes propagating.

The project is **git-connected to this repository** (hectorTSH/tsh-studios,
production branch `main`): every push to main auto-deploys to production.
History: first deployed by Merlin via connector file uploads, then Hector
had the code moved to GitHub and the project linked the same evening.
Note: Merlin's GitHub connection pushes text files only and passes file
contents as command arguments, so keep individual text files under ~90 KB
(the product photos are web-compressed; full-res originals live in Hector's
photo files; photos reached the repo via a one-time web upload).

## tshstudios.com (attached 2026-11-08)

1. Vercel project: Settings → Domains → `tshstudios.com` added as Production,
   `www.tshstudios.com` added with a 308 redirect to the apex. Done.
2. Porkbun DNS points the domain at Vercel with the values Vercel's Domains
   page recommends for this project:
   - A record, host `@` → `216.150.1.1`
   - CNAME, host `www` → `6e6b488ab68bad1d.vercel-dns-016.com`
   - Plus the two `_vercel` TXT verification records Vercel issued.
   (The legacy pair `76.76.21.21` / `cname.vercel-dns.com` also works.)
3. SSL certificate issues automatically once verification completes.
   The same Porkbun zone also carries the Google Workspace records for
   @tshstudios.com mail (Google MX/SPF/DKIM, google-site-verification) —
   don't disturb them when editing the Vercel records.

## Notes

- Contact buttons use `hello@tshstudios.com` — live since 2026-11-08
  (Google Workspace for tshstudios.com is set up and Gmail is activated).
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
