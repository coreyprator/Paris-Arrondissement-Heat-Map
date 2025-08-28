# Paris Arrondissement Heat Map

Single-file, portable, interactive **Leaflet** dashboard that visualizes Paris’s 20 arrondissements with a heat map and a sortable score table. You can toggle datasets (Jay’s YouTube tiers and multiple **Paris Énigmes** categories) and the map recolors using a simple **unweighted average** of the checked sets.

- **Live site (GitHub Pages):** https://coreyprator.github.io/Paris-Arrondissement-Heat-Map/
- **App file:** `Paris Arrondissement Dashboard.html` (all HTML/CSS/JS + GeoJSON embedded)

> The project was built iteratively in ChatGPT based on the user’s requirements in this conversation:  
> - start from Jay’s ranking,  
> - correct map aspect & data geometry,  
> - embed official GeoJSON inline so the file is 100% portable,  
> - add a second dataset (Paris Énigmes) with multiple categories,  
> - provide **composite averaging** and **per-arrondissement score table**,  
> - simplify to a **single-map** view with checkboxes and **inline source links**,  
> - make the score table show **Average + each individual dataset’s score** and allow **column sorting**.

---

## Features

- 🗺️ **Leaflet heat map** of all 20 arrondissements (OpenStreetMap tiles)
- 🔢 **Permanent labels** (arrondissement numbers)
- ✅ **Dataset checkboxes**: Jay + PE (Qualité, Culture, Transports, Commerces, Environnement, Sécurité)
- ➕ **Composite average** (simple mean) updates instantly as you check/uncheck
- 📊 **Sortable score table** showing **Average** and **each dataset’s score** per arrondissement
- 🔗 **Inline source links** next to each dataset and in the footer
- 📦 **Single HTML file** with embedded GeoJSON (no servers, no build step)

---

## Data Sources

- **Jay’s arrondissement ranking (YouTube):** https://youtu.be/mMikt4FlXRM?si=grOt9HbVgLVbWN9u  
- **Paris Énigmes — Guide des 20 arrondissements:** https://www.parisenigmes.com/blog/guide-arrondissement-paris/  
- **Official geometry (GeoJSON) — Paris Open Data:** https://opendata.paris.fr/explore/dataset/arrondissements/

---

## Run locally

Just open `Paris Arrondissement Dashboard.html` in any modern browser (Chrome, Edge, Firefox, Safari). No internet required after first load (tiles use OSM online; the app itself is offline-ready).

---

## GitHub Pages

1. Commit both `index.html` and `Paris Arrondissement Dashboard.html` to the repo root.  
2. In the repo, go to **Settings → Pages**.  
3. **Build and deployment → Source:** select **Deploy from a branch**.  
4. **Branch:** `main` and **/ (root)** → **Save**.  
5. Wait ~1 minute, then open:  
   `https://coreyprator.github.io/Paris-Arrondissement-Heat-Map/`

If you ever rename the app, update the `index.html` redirect target accordingly.

---

## Updating datasets

To avoid human error, please open an issue or PR with:
- The **new dataset** in JSON form: `{ "1": number, "2": number, ..., "20": number }`
- A short **label** (e.g., `PE — Logement`)
- A **source URL**

We’ll bake it into the HTML and add a new checkbox + column in the table.

---

## License

- Map tiles © OpenStreetMap contributors (via OSM tile servers).  
- This repository’s code is MIT unless specified otherwise.
