# Paris Arrondissement Heat Map

An interactive map of Paris’s 20 arrondissements.  
Choose what you care about (quality, culture, transport, safety, etc.) and the map recolors instantly to show which districts score higher.

👉 **Live Map:** https://coreyprator.github.io/Paris-Arrondissement-Heat-Map/

---

## How to Use

**On phone or tablet**
- Tap **Go to Map**, **Go to Settings**, or **Go to Scores** at the top to jump to that section.
- Use **two fingers** to pan the map (so you don’t accidentally scroll the page).
- Pinch to zoom the map.

**On any device**
1. **Choose datasets** (right side / “Settings”)  
   - *Jay (YouTube ranking)*  
   - *Paris Énigmes* categories: **Qualité**, **Culture**, **Transports**, **Commerces**, **Environnement**, **Sécurité**  
2. The map recolors using a **simple average** of the checked datasets  
   - **Red = higher** score, **Green = lower** score.
3. **Scores table** (bottom)  
   - Shows **Average** (based on your selection) and each checked dataset’s **individual** score per arrondissement.  
   - Tap a **column header** to sort by that column (tap again to reverse the order).

---

## Sources

- 🎥 Jay’s arrondissement ranking (YouTube): https://youtu.be/mMikt4FlXRM?si=grOt9HbVgLVbWN9u  
- 📊 Paris Énigmes — Guide des 20 arrondissements: https://www.parisenigmes.com/blog/guide-arrondissement-paris/  
- 🗺️ Official geometry (GeoJSON) — Paris Open Data: https://opendata.paris.fr/explore/dataset/arrondissements/

---

## Troubleshooting

- **Blank map or red error panel?**  
  Make sure `arrondissements.json` exists at the site root:  
  `https://<your-username>.github.io/Paris-Arrondissement-Heat-Map/arrondissements.json`

- **Map moves when I try to scroll on mobile**  
  Use the **jump buttons** at the top (Map / Settings / Scores), or scroll outside the map area.

---

## Developer Notes (optional)

- App file: **`Paris Arrondissement Dashboard.html`**  
- Geometry: **`arrondissements.json`** (from Paris Open Data), kept in the repo **root**.  
- Landing page: **`index.html`** (redirects to the app).  
- Tech: Leaflet + vanilla JS, no build step.

### Adding another dataset
Open a PR with:
```json
{ "1": number, "2": number, ..., "20": number }
