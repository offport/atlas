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
| ◍ | **Earth** | A living 3D Earth: city lights on the night side, drifting clouds and the seasons set by its real 23.44° tilt. Slice it open to a to‑scale cutaway of the crust, mantle and core, or peel back the layered atmosphere — and flip on the tectonic plates. |
| 🩻 | **Human Anatomy** | Explore the body in 3D: the full skeleton and the muscular system, every structure named and searchable. Hover to identify any bone or muscle, then lift a single one out on its own and spin it 360°. |
| ⚛ | **Periodic Table** | All 118 elements, grouped by family. Click any one to open its atom in 3D — a nucleus of protons and neutrons wrapped in its real electron shells — and spin it 360°. |
| 🎖️ | **The Two World Wars** | Both world wars side by side: why each began, who fought (tap a flag), the machines that changed warfare, a year‑by‑year timeline you can filter, the twenty years between them and what each one left behind. |
| 🪙 | **The Story of Money** | Scroll through 5,000 years of money, from barter and cowrie shells to coins, paper, the gold standard, plastic and code, with each kind compared for carrying, lasting and trust. |

### Running it

Everything is static. Serve the folder over HTTP (the Solar System’s ES‑module import and the iframes need a real origin — `file://` won’t do):

```bash
python -m http.server 8799
# then open http://127.0.0.1:8799/
```

### Built with, and thanks to

- **three.js** (MIT) for the 3D **Solar System** and **Earth** — planet, ring and moon textures from **threex.planets** by Jérôme Etienne (MIT, derived from NASA imagery), with planet positions from **JPL** Keplerian orbital elements.
- The **Periodic Table** element data (names, masses, categories, electron shells, grid positions, summaries) is from **[Bowserinator/Periodic‑Table‑JSON](https://github.com/Bowserinator/Periodic-Table-JSON)** (sourced from Wikipedia). The 3D atom is a schematic **Bohr model** (electrons shown as particles in fixed shells; real electrons occupy quantum orbitals), rendered with three.js.
- The **Human Anatomy** page's 3D meshes are from **[Z‑Anatomy](https://www.z-anatomy.com/)** (CC BY‑SA 4.0), the libre 3D atlas of anatomy, derived from **BodyParts3D** / The Database Center for Life Science (CC BY‑SA 2.1 Japan); structure names follow Terminologia Anatomica. See `anatomy-assets/ATTRIBUTION.md`. Rendered with three.js (GLTFLoader + Draco).
- The **Earth** page's day and night (city‑lights) and cloud maps are NASA Blue Marble / Black Marble imagery via **[Solar System Scope](https://www.solarsystemscope.com/textures/)** (CC BY 4.0). Interior depths and temperatures follow **USGS** and the Preliminary Reference Earth Model (PREM); atmosphere altitudes follow **NOAA / UCAR**; tectonic‑plate boundaries are the PB2002 model (Peter Bird) via **[fraxen/tectonicplates](https://github.com/fraxen/tectonicplates)**. Day/night, the seasons and the terminator are computed from Earth's real axial tilt.
- **Countries** data from [mledoze/countries](https://github.com/mledoze/countries), the **World Bank** (populations), **GeoNames** (cities & elevation) and **Natural Earth / world‑atlas** (map geometry). Weather figures are a clearly‑labelled climate *model*, not forecasts.

Each topic page also opens on its own, straight from its file.
