# Geocoder Comparison Tool

A single-page tool to compare geocoding results side-by-side from **Google Places**, **Mapbox Geocoding**, and **HERE Geocoding** — with live latency, result cards, and markers on a shared Mapbox map.

**Live demo:** https://justaghost.github.io/mapsdemo/

## What it does

- Enter your API keys for any combination of Google, Mapbox, and/or HERE
- Type an address and hit **Compare** (or press Enter)
- All three providers are queried in parallel — results appear in side-by-side panels with latency in milliseconds
- Click any result to fly the map to that location; markers for all providers are shown simultaneously

Defaults to South Africa (`country=za` / `countryCode:ZAF`) but the providers accept global queries.

## Getting API keys

| Provider | Where to get it | Notes |
|----------|----------------|-------|
| **Google** | [Google Cloud Console](https://console.cloud.google.com/) → Maps JS API + Places API | Enable both APIs on the key |
| **Mapbox** | [mapbox.com/account/access-tokens](https://account.mapbox.com/access-tokens/) | Public token (`pk.…`) |
| **HERE** | [developer.here.com](https://developer.here.com/) → REST API key | Free tier available |

Only Mapbox is required (it hosts the base map). Google and HERE are optional — their panels are skipped if no key is provided.

## Running locally

Just open `index.html` in a browser — no build step, no server required.

```bash
open index.html   # macOS
start index.html  # Windows
```

## Tech

- [Mapbox GL JS v3.3](https://docs.mapbox.com/mapbox-gl-js/) — base map and markers
- [Google Places Autocomplete Service](https://developers.google.com/maps/documentation/javascript/places-autocomplete)
- [HERE Geocoding & Search API v1](https://developer.here.com/documentation/geocoding-search-api/)
- Vanilla JS, no framework, no bundler
