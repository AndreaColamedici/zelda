# Contributing to Forest Dweller's Project

Thanks for wanting to help build the most complete TotK companion out there. Here's how.

## Ways to Contribute

### 1. Add Game Data

The most valuable contribution right now is expanding the knowledge base. Each item in the database follows a consistent structure.

**Weapon example:**
```json
{
  "id": "w11",
  "name": "Royal Broadsword",
  "type": "weapon",
  "subtype": "One-Handed Sword",
  "attack": 26,
  "rarity": "uncommon",
  "location": "Hyrule Castle, enemy camps",
  "lat": -0.05,
  "lng": 0.08,
  "description": "A sword favored by the Royal Family's knights...",
  "fuse": "Best combined with Silver Bokoblin Horn (+25)."
}
```

**To add items:**
1. Fork the repository
2. Add your items to the `KNOWLEDGE_BASE` object in `index.html` (or to the relevant JSON file in `data/`)
3. Make sure every item has: `id`, `name`, `type`, `subtype`, `rarity`, `location`, `lat`, `lng`, `description`
4. Submit a Pull Request with a clear description of what you added

### 2. Submit Builds

Ultrahand and Fuse builds are what make TotK special. To submit a build:

- Name and description of what it does
- Complete list of Zonai devices / materials needed
- Difficulty rating (Easy / Medium / Hard)
- Where it's most useful
- Optional: screenshot or video link

### 3. Fix Data

If you spot wrong stats, incorrect locations, or outdated information:
1. Open an Issue describing the error
2. Or submit a PR with the fix

### 4. Improve the App

For code contributions:
- Keep it vanilla (no frameworks, no build tools)
- The app must work as a single HTML file opened locally
- Test in both Chrome and Firefox
- Follow the existing code style

## Coordinate System

Map coordinates use Leaflet's Simple CRS. The approximate mapping to in-game coordinates:

- `lat`: North-South (negative = north, positive = south)
- `lng`: East-West (negative = west, positive = east)
- Center (0, 0) = Hyrule Castle

When adding items, estimate position based on the game map region.

## Rarity Tiers

- `legendary` — Unique or extremely rare items (Master Sword, Ancient Hero's Aspect)
- `rare` — Hard to obtain, limited sources (Gloom weapons, Savage Lynel drops)
- `uncommon` — Available but requires some effort (regional armor, cave materials)
- `common` — Widely available (basic weapons, common materials)

## Pull Request Guidelines

- One PR per category or feature (don't mix weapons and UI fixes)
- Include source for stats (wiki link, in-game verification)
- Keep descriptions concise but informative (2-4 sentences)
- Test that the app still loads and works after your changes
