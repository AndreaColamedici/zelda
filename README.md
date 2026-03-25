# Hyrule Companion

**An intelligent knowledge base and interactive companion for The Legend of Zelda: Tears of the Kingdom.**

Hyrule Companion is an open-source web application that combines an interactive map of Hyrule with a structured database of every weapon, armor set, material, shrine, and Zonai build in the game — plus a conversational companion that answers your questions in natural language.

## What This Is

Most TotK resources are passive catalogs: you search, you find a pin on a map, you go back to the game. Hyrule Companion is different. It's built around three ideas:

1. **Interactive Map** — A Leaflet.js-powered map of Hyrule (Surface, Sky Islands, Depths) with filterable markers for every item category.
2. **Structured Knowledge Base** — A comprehensive JSON database of weapons, armor, materials, shrines, Zonai devices, fusion combinations, and build strategies.
3. **Conversational Companion** — A chat interface where you ask questions in plain language ("What's the strongest weapon?", "How do I build an Air Bike?") and get contextual, detailed answers with links to relevant items on the map.

## Quick Start

This is a static web application. No server, no build step, no dependencies to install.

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/hyrule-companion.git

# Open in browser
open index.html
```

Or deploy it on GitHub Pages: go to Settings → Pages → Deploy from main branch. Done.

## Project Structure

```
hyrule-companion/
├── index.html          # Main application (single-file prototype)
├── README.md           # This file
├── CONTRIBUTING.md     # How to contribute
├── ROADMAP.md          # Development roadmap
└── data/               # (future) Separate JSON data files
    ├── weapons.json
    ├── armor.json
    ├── materials.json
    ├── shrines.json
    └── builds.json
```

## Current Status

This is **v0.1 — Prototype**. The application is fully functional but contains a starter dataset. The roadmap below describes what comes next.

### What works now
- Interactive map with region labels and item markers
- Search across all item categories
- Category filtering (Weapons, Armor, Materials, Shrines, Builds)
- Companion chat with knowledge-base-powered responses
- Click-to-navigate: selecting items in chat or list pans the map
- Layer switching UI (Surface / Sky / Depths)
- Responsive, dark-themed UI inspired by the Sheikah Slate

### What's coming
- Real map tiles (extracted from game data or community-sourced)
- Complete item database (all 150+ weapons, all 36 armor sets, all 152 shrines, all materials)
- AI-powered companion (RAG pipeline with full knowledge base)
- Community contributions via pull requests
- Route planner for efficient farming
- Build calculator for fusion damage

## Roadmap

### Phase 1: Complete Knowledge Base
- [ ] Import all weapons with stats, locations, and fusion data
- [ ] Import all 36 armor sets with upgrade paths
- [ ] Import all 152 shrines with locations and challenge types
- [ ] Import key materials with farming locations
- [ ] Document all notable Ultrahand builds

### Phase 2: Real Map Integration
- [ ] Integrate community-sourced map tiles (Surface, Sky, Depths)
- [ ] Add accurate coordinates for all items
- [ ] Implement proper layer switching between map levels
- [ ] Add Korok seed locations (all 1000)

### Phase 3: AI Companion
- [ ] Build RAG pipeline using the JSON knowledge base
- [ ] Connect to an LLM API for natural language responses
- [ ] Context-aware answers (knows what you've already found)
- [ ] Personalized route suggestions

### Phase 4: Community
- [ ] Contribution guidelines and templates
- [ ] PR-based submission for new builds and strategies
- [ ] User progress tracking (mark items as found)
- [ ] Shareable build links

## Contributing

Contributions are welcome! The easiest way to help right now:

1. **Add data** — Pick a category (weapons, armor, shrines) and add missing items to the knowledge base following the existing JSON structure.
2. **Report issues** — Found wrong stats or missing locations? Open an issue.
3. **Submit builds** — Document your favorite Ultrahand/Fuse combinations with components and use cases.

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## Tech Stack

- **Frontend**: Vanilla HTML/CSS/JavaScript (no framework, no build step)
- **Map**: [Leaflet.js](https://leafletjs.com/) 1.9.4
- **Fonts**: Cinzel (headings), Inter (body)
- **Hosting**: GitHub Pages (static)
- **Data**: JSON (embedded in prototype, separate files in future)

## License

MIT License. This is a fan project — all game content belongs to Nintendo.

## Credits

Built with enthusiasm by players, for players.

Data sourced from community wikis including [Zelda Dungeon](https://www.zeldadungeon.net/), [Game8](https://game8.co/), [Fextralife Wiki](https://zeldatearsofthekingdom.wiki.fextralife.com/), and the [TotK Object Map](https://objmap-totk.zeldamods.org/) project.
