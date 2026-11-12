<p align="center">
  <img src="logo.svg" width="380" alt="Atlas — a small library of things worth understanding">
</p>

# Atlas

**A small library of things worth understanding.** Atlas is a tabbed hub of self‑contained, interactive pages — each one explores a single topic, and keeps its own look. Open one in a tab, play with it, and switch between them freely.

### Topics

| | Topic | What it does |
|---|---|---|
| 🌌 | **Big Bang to Today** | Scroll from the first instant of the universe to this morning — 13.8 billion years of cosmos, Earth, life and human history on one stretched timeline. |
| 🦴 | **Human Family Tree** | Meet our ancestors and extinct cousins, from *Sahelanthropus* to *Homo sapiens*, as life‑lines on a tree of deep time. |
| 🗺️ | **Countries Atlas** | Every country on an interactive world map (Robinson projection): search and filter them, read their size, people and cities, and drag a yearly timeline to see the weather change. |
| 🪐 | **Solar System** | A real‑time 3D Solar System. Planets sit at their true positions for any date — from NASA/JPL orbital elements — with real sizes, tilts and orbits. Click one to learn about it. |

### Running it

Everything is static. Serve the folder over HTTP (the Solar System’s ES‑module import and the iframes need a real origin — `file://` won’t do):

```bash
python -m http.server 8799
# then open http://127.0.0.1:8799/
```

### Built with, and thanks to

- **three.js** (MIT) for the 3D Solar System — planet, ring and moon textures from **threex.planets** by Jérôme Etienne (MIT, derived from NASA imagery), with positions from **JPL** Keplerian orbital elements.
- **Countries** data from [mledoze/countries](https://github.com/mledoze/countries), the **World Bank** (populations), **GeoNames** (cities & elevation) and **Natural Earth / world‑atlas** (map geometry). Weather figures are a clearly‑labelled climate *model*, not forecasts.

Each topic page also opens on its own, straight from its file.
