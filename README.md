# Faraway Barn — website

A small, fast, hand-coded static website for the Airbnb listing **Faraway Barn**
(South Gloucestershire). It's a "showcase" site: every booking button points to the Airbnb
listing, so all stays stay inside Airbnb's payments + AirCover protection.

## Files

```
faraway-barn/
├─ index.html        Home
├─ the-barn.html     The accommodation (gallery, amenities, floor plan)
├─ the-area.html     Things to do nearby (the main SEO page)
├─ robots.txt        Search-engine crawl rules
├─ sitemap.xml       List of pages for Google
└─ assets/
   ├─ styles.css     All styling (edit colours at the top in :root)
   └─ images/        Photos (.avif modern + .jpg fallback for each)
```

No build step, no dependencies. It's plain HTML/CSS — open `index.html` in a browser to view it.

## Run it locally

Just double-click `index.html`, or for a more accurate preview run a tiny local server:

```bash
# from inside the faraway-barn folder
python -m http.server 8080
# then open http://localhost:8080
```

## Things to change before going live  ⚠️

These are placeholders — search/replace them across all 4 HTML files + sitemap/robots:

1. ~~**Domain**~~ — done: live at `https://farawaybarn.co.uk`.
2. **Communications** — all enquiries route through Airbnb (no email on the site by design).
3. **Airbnb link** — currently `https://www.airbnb.co.uk/rooms/1699802364503795984`. Confirm it's right.
4. **Drive times on `the-area.html`** — these are *approximate*; sanity-check them against Google Maps.
5. **`petsAllowed`** in the structured data (index.html) is set to `false`. Change to `true` if dogs are welcome.

## Deploying (cheapest reliable options)

All of these are free or near-free for a site this size:

- **Cloudflare Pages** or **Netlify** — drag-and-drop the folder, or connect a Git repo. Free HTTPS, fast.
- **GitHub Pages** — free if you're comfortable with Git.

Then point your domain's DNS at the host (each provides instructions).

## Don't forget (the other half of "getting found on Google")

The website alone isn't enough. Two free, high-impact steps:

1. **Set up a Google Business Profile** for "Faraway Barn" (category: holiday/vacation
   home rental). This is what puts you on Google Maps and in the local results.
2. **Submit the sitemap** in Google Search Console (`https://search.google.com/search-console`)
   once the site is live, so Google indexes it quickly.

## Later: adding direct bookings ("Option C")

The site is structured so you can graduate from "book on Airbnb" to taking **direct, commission-free
bookings** later — by adding a channel manager (Lodgify / Hospitable / Beds24) that syncs your Airbnb
calendar, plus a standalone short-term-let insurance policy to replace AirCover on direct bookings.
When you're ready, the booking buttons just need to point at the booking engine instead of Airbnb.
