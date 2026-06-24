# The Noise Report
**Live NYC noise complaint history for any address — built on 4.9M+ official 311 records.**

## What it does
Type any NYC address and get an instant noise profile: a label (Quiet → Very Loud), a borough percentile ranking, a year-by-year complaint trend, and a list of the most recent 311 reports filed at or near that address.

## How it works
Queries the NYC 311 dataset live via the Socrata SODA API — no backend, all queries run client-side. Searches first for an exact address match, then widens to the surrounding block (±50 house numbers), then the full street if needed. Your score label is based on the last 12 months of complaints ranked against up to 1,000 sampled addresses in the same borough. The borough map compares all five boroughs per 100,000 residents using 2025 Census estimates.

## Features
- Live data — pulled fresh on every search
- 3-pass address matching with block range shown (e.g. 197–297 Center Street)
- Borough percentile ranking against up to 1,000 comparable addresses
- Year-by-year noise trend chart with peak year insight
- Complaint type breakdown (residential, street, vehicle, etc.)
- Most recent reports list with load-more pagination
- Five-borough comparison map with per-capita ranking
- Fully responsive — works on desktop and mobile web
- Single HTML file, no build step, no dependencies, no backend

## Stack
- Vanilla JS + HTML + CSS
- [NYC Open Data / Socrata SODA API](https://dev.socrata.com/)
- [NYC GeoSearch API](https://geosearch.planninglabs.nyc)
- Fonts: Source Serif 4, Libre Franklin (Google Fonts)
