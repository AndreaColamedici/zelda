# Contributing to Forest Dweller's Project

Thanks for wanting to help build the most complete TotK companion out there. Here's how.

## Adding Images

The companion supports real images for every item. Images go in the `img/` folder and are named by item ID.

**File naming convention:**
- `img/w1.png` — Master Sword (weapon 1)
- `img/a1.png` — Barbarian Set (armor 1)
- `img/m1.png` — Silver Lynel Saber Horn (material 1)
- `img/b1.png` — Air Bike (build 1)

**How to add an image:**
1. Take a screenshot or find a clean image of the item
2. Crop it to show just the item (transparent or dark background works best)
3. Save as `.png` format (256×256 with transparent background preferred)
4. Name it with the item ID (check the `DB` object in `index.html` for IDs)
5. Place it in the `img/` folder and push to the repo

**Image guidelines:**
- Recommended size: 256×256 pixels (or similar square-ish ratio)
- PNG format with transparency
- Transparent background preferred (looks best with the glow effects)
- If no image exists for an item, the emoji automatically shows as fallback

**Full ID reference:**

Weapons (w1–w27): Master Sword, Royal Guard's Claymore, Scimitar of the Seven, Lightscale Trident, Savage Lynel Bow, Hylian Shield, Gloom Sword, Gloom Club, Royal Guard's Bow, Soldier's Broadsword, Traveler's Sword, Royal Broadsword, Zora Sword, Gerudo Scimitar, Royal Claymore, Boulder Breaker, Fierce Deity Sword, Gloom Spear, Zora Spear, Royal Halberd, Forest Dweller's Bow, Royal Bow, Great Eagle Bow, Demon King's Bow, Royal Shield, Savage Lynel Shield, Gloom Shield

Armor (a1–a24): Barbarian, Snowquill, Flamebreaker, Rubber, Zora, Desert Voe, Glide, Climbing, Stealth, Depths, Ancient Hero's Aspect, Fierce Deity, Dark, Froggy, Zonaite, Radiant, Mystic, Ember, Frostbite, Charged, Yiga, Hylian, Soldier's, Miner's

Materials (m1–m19): Silver Lynel Saber Horn, Silver Lynel Mace Horn, Diamond, Ruby, Sapphire, Topaz, Zonaite, Large Zonaite, Muddle Bud, Bomb Flower, Puffshroom, Light Dragon Horn, Dinraal Horn, Naydra Horn, Farosh Horn, Hearty Durian, Endura Carrot, Star Fragment, Ancient Blade

Builds (b1–b6): Air Bike, Flying Platform, Battle Wagon, Rocket Sled, Spring Launcher, Bomb Cart

## Ways to Contribute

### 1. Add Game Data

Each item in the database follows this structure. Add items to the `DB` object in `index.html`:

```json
{
  "id": "w28",
  "name": "New Weapon Name",
  "sub": "One-Handed Sword",
  "atk": 20,
  "rarity": "uncommon",
  "emoji": "🗡️",
  "r": "central",
  "loc": "Where to find it in the game",
  "desc": "Description of the weapon.",
  "fuse": "Best fusion suggestion (optional)"
}
```

Region keys for the `r` field: `hyrule-castle`, `lookout`, `central`, `zora`, `goron`, `rito`, `gerudo`, `gerudo-high`, `kakariko`, `hateno`, `akkala`, `eldin`, `faron`, `lanayru`, `hebra`, `korok`, `depths`, `sky`, `lake-hylia`, `tabantha`, `everywhere`, `light-dragon`, `dinraal-path`, `naydra-path`, `farosh-path`

### 2. Submit Builds

Ultrahand and Fuse builds are what make TotK special. To submit a build:
- Name and description of what it does
- Complete list of Zonai devices / materials needed
- Difficulty rating (Easy / Medium / Hard)
- Where it's most useful

### 3. Fix Data

If you spot wrong stats, incorrect locations, or outdated information:
1. Open an Issue describing the error
2. Or submit a PR with the fix

### 4. Improve the App

For code contributions:
- Keep it vanilla (no frameworks, no build tools)
- The app must work as a single HTML file opened locally
- Test in both Chrome and Firefox

## Rarity Tiers

- `legendary` — Unique or extremely rare items (Master Sword, Ancient Hero's Aspect)
- `rare` — Hard to obtain, limited sources (Gloom weapons, Savage Lynel drops)
- `uncommon` — Available but requires some effort (regional armor, cave materials)
- `common` — Widely available (basic weapons, common materials)

## Pull Request Guidelines

- One PR per category or feature
- Include source for stats (wiki link, in-game verification)
- Keep descriptions concise but informative
- Test that the app still loads and works after your changes
