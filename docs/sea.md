# The Sea

Once the keep is well established, a **Harbor** opens: build a shipyard, take the helm of your own ship, and sail the Ember Sea to chart islands, dig up treasure, fight raiders and castle fleets, and claim four foreign castles as realms of your own.

## Unlocking

The **Harbor** tab appears once you have **Copper Scale** armor (tier 2) and have dug the **Verdant Gallery** (mine depth 2). With the Harbor tab, the tab bar becomes four columns: Build · Upgrades · Magic · Explore / Forge · Harbor · Legacy.

## Maren and the shipyard

**Maren**, the shipwright, builds the shipyard for **20,000 gold, 120 wood, 60 stone and 10 iron** (3 minutes). It comes with your first ship, a cog called the **Ember Gull**. Once it's built, a **Sea** button joins Keep and Journey on the canvas, and opening the Harbor tab shows the sea.

Maren also refits the ship, one job at a time:

| Part | Tier | Name | Cost | Time | Effect |
|---|---:|---|---|---:|---|
| Sails | 0 | Patched Sail | – | – | Speed ×1 |
| | 1 | Linen Sails | 30,000 gold, 80 wood, 40 copper | 1m 30s | Speed ×1.15 |
| | 2 | Twin Masts | 300K gold, 150 wood, 40 tin | 4m | Speed ×1.3 (and a second sail) |
| | 3 | Storm-woven Sails | 3M gold, 300 wood, 100 copper, 5 Storm | 10m | Speed ×1.5 |
| Hold | 0 | Small Hold | – | – | 150 goods |
| | 1 | Deep Hold | 25,000 gold, 200 wood, 50 stone | 1m 30s | 300 goods |
| | 2 | Merchant Hold | 250K gold, 300 wood, 40 iron | 4m | 600 goods |
| | 3 | Dragon's Hold | 2.5M gold, 500 wood, 120 iron | 10m | 1,200 goods |
| Hull | 0 | Cog Hull | – | – | 100 hull |
| | 1 | Oak-ribbed Hull | 40,000 gold, 150 wood, 20 iron | 1m 30s | 160 hull |
| | 2 | Iron-banded Hull | 400K gold, 250 wood, 60 iron | 4m | 240 hull |
| | 3 | Dwarf-riveted Hull | 4M gold, 150 iron, 60 tin | 10m | 340 hull |
| Arms | 0 | Crossbow Rail | – | – | 3 bolts a side, 5 damage, reload 3.5s |
| | 1 | Deck Ballistae | 35,000 gold, 100 wood, 25 iron | 1m 30s | 4 bolts, 7 damage, reload 3s |
| | 2 | Twin Ballista Batteries | 350K gold, 150 wood, 60 iron, 40 copper | 4m | 5 bolts, 9 damage, reload 2.6s |
| | 3 | Ember Ballistae | 3.5M gold, 150 iron, 50 tin, 10 Ember | 10m | 6 burning bolts, 12 damage, reload 2.2s |

Better sails also turn the ship faster.

## Sailing

The **Sea** view is a top-down chart of the Ember Sea, with the camera following your ship. You steer live:

- **Tap or drag on the water** to set a heading. The ship turns toward it (a small gold ring shows where it's turning to). Tapping while at anchor also raises the sails.
- **Drop anchor / Raise sails** on the sea bar under the canvas stops and starts the ship.
- The ship only moves while you're watching the Sea view. Leave it, and it waits where it is.

### Wind

The wind shifts slowly with the real clock. The **wind rose** in the corner points where it's blowing, and the sea bar says where it's coming from. Speed depends on the angle between your heading and the wind:

| Heading relative to the wind | Speed |
|---|---:|
| Running (wind behind) | 80% |
| Beam reach (wind from the side) | **100%** |
| Close-hauled (45° off the wind) | 55% |
| Nearly into the wind | 25% |
| Straight into the wind | 15% |

Base speed is 46 knots × the sails' multiplier. To go upwind, tack across it.

### The view

- **Taller / Shorter** (under the Keep/Journey/Sea switch) makes the sea view 2.5 times taller, so it fills most of a phone screen and more of the sea is visible around the ship. It's remembered, and only applies to the Sea view: the keep and the journey keep their usual size.

- A **chart** in the bottom-left shows the islands you've charted, your harbor, and the ship.
- Islands are revealed on the chart when you sail within sight of them, and each adds an entry to the [Adventurer's Log](log.md).
- The name of the island you're beside shows at the bottom of the view.
- Day and night follow the [cycle](day-night.md): the sea darkens, castle windows glow, and the ship carries a lantern.

## Treasure and cargo

Six islands hold **buried treasure**, marked with a red ✕ while it's waiting. Sail close, and the sea bar's button becomes **Dig for treasure**. Each dig gives gold (scaled to your income) plus the island's goods, and the treasure refills after a while.

| Island | Tier | Goods | Refills |
|---|---:|---|---:|
| Gull Rock | 1 | 20–40 stone, 5–15 wood | 15m |
| Saltmarsh Cay | 1 | 30–60 wood, 10–20 stone | 15m |
| Wreckers' Reef | 2 | 15–30 copper, 10–20 tin, 20–40 wood | 25m |
| Mistveil Isle | 2 | 10–20 tin, 10–20 copper, 1–3 crystals | 30m |
| Serpent's Tooth | 3 | 20–40 iron, 20–40 stone, 1–2 crystals | 40m |
| The Drowned Tower | 3 | 15–30 iron, 10–20 tin, 3–5 crystals | 45m |

Gold per dig: `max(150 × tier, (gold/sec × 45 + gold/tap × 15) × tier)`.

**Flotsam** (floating barrels) drifts around the ship; sail through it for a little wood, stone or gold.

Everything found at sea goes into the **hold**. Goods (not gold) count against its capacity, and anything that doesn't fit is left behind. The cargo is **banked when you sail back into the harbor** at Emberkeep (the end of the pier).

## Sea battles

Ships at sea fight with **broadsides**: ballista bolts fire sideways from the rail, so you have to turn your side toward the enemy. There's no gunpowder in Emberkeep; everything is bolts, rails and ballistae.

- When an enemy ship comes within about 330 yards, the sea bar shows its name, both hulls and the distance, and its button becomes **Fire!**. It fires from whichever side (port or starboard) faces the nearest enemy, and each side reloads separately.
- Bolts fly about 190 yards in a slightly spread line. Anything they pass through takes the damage; they splash into the sea or hit land otherwise. So aim with the whole ship: turn broadside, then fire.
- Enemy ships do the same: they close in at an angle, then turn broadside to fire, and circle you to keep their side on you. Wind affects them too.
- Their hull shows as a bar over the ship, which turns green when they're **crippled** (35% or less). Crippled ships limp along at under half speed, so you can catch them.

### Taking a ship

| How | What you get |
|---|---|
| **Sink her** | She breaks up and leaves three salvage barrels (gold dot on top) with 60% of her loot. Sail through them to pick it up. |
| **Board her!** | When she's crippled and within about 75 yards, the button becomes **Board her!**. If your hero is home with more than 8 + 6 × tier health, they lead the boarders for that much health and you take **150%** of her loot. If the hero is away on an expedition (or too hurt), the crew boards alone: no health cost, **100%** of her loot. The button's small line says which it will be. Loot goes straight into the hold. |

Loot per ship tier: gold (`max(100 × tier, (gold/sec × 30 + gold/tap × 10) × tier)`), plus tier 1: wood and stone; tier 2: copper, iron, wood; tier 3: iron, tin, 1 crystal; tier 4: iron, tin, 2–4 crystals.

### Ships of the sea

| Ship | Hull | Speed | Bolts | Damage | Range | Tier | Where |
|---|---:|---:|---:|---:|---:|---:|---|
| Corsair Raider | 70 | ×0.95 | 2 | 5 | 150 | 1 | Open sea. Flees when badly hurt. |
| Redtide Galley | 130 | ×0.9 | 3 | 6 | 150 | 2 | Guards Redtide Hold (2). Also roams once your ship has two refits. |
| Dwarven Ironclad | 230 | ×0.72 | 3 | 9 | 150 | 3 | Guards Karak Brine (3) |
| Jarl's Dragonship | 170 | ×1.15 | 3 | 8 | 140 | 3 | Guards Skarholm (3) |
| Elven Swanship | 200 | ×1.05 | 3 | 10 | 195 | 4 | Guards Sylvanreach (3) |

**Raiders** roam the open sea: one at a time, or two once you've charted a castle. They appear every 30–55 seconds, out of sight, never near your own harbor, and they won't fight within about 260 yards of it (the harbor is safe water). **Castle fleets** patrol their island and attack when you come close, or when one of them is hit. A castle's fleet stays broken once sunk or taken.

### Hull, sinking and repairs

The hull only repairs **in your harbor** (full in 3 minutes, even while you're away). If the hull reaches 0, the Ember Gull **sinks**: the cargo is lost, and the crew is towed home with the ship at 25% hull.

## Foreign castles

| Castle | People | Island |
|---|---|---|
| Karak Brine | Dwarven sea-fort | A rocky stack to the north |
| Skarholm | Frost jarl's hall | An island of ice and pine, far north-east |
| Sylvanreach | Elven isle | White spires in a forest, far south-east |
| Redtide Hold | Corsair stronghold | A timber palisade on a sandy isle to the south |

Each castle's harbor chain stays raised while any of its guard ships is afloat. Break the fleet, and the sea bar's button becomes **Besiege** when you're beside it.

### Sieges

| Option | Cost | Notes |
|---|---|---|
| **Storm the gate** | Hero health: max health × (0.3 + 0.15 × defense − 0.04 × power), between 15% and 90% | Instant. The hero must be home and have more health than the cost. |
| **Scale the walls by night** | Half the storm cost | Only at night (see [Day and Night](day-night.md)). |
| **Blockade the harbor** | 8 + 6 × defense minutes, no health | The ship anchors at the castle and can't sail until it falls (it falls while you're away too). **Lift blockade** cancels it. |

Defense: Redtide Hold 1, Karak Brine 2, Skarholm 3, Sylvanreach 4. Power is weapon tier + armor tier + ship arms tier.

## Claimed castles (realms)

A claimed castle is a **realm of your own**. The Build tab gets a realm switcher (Emberkeep plus every castle you hold). Choosing a realm shows its five holdings in the Build tab and its castle in the Keep view, where tapping earns gold as usual. All realms pay into one treasury, so gold/sec counts every holding everywhere. Each realm's holdings have three techniques each in the Upgrades tab (at 1, 10 and 25 owned).

Its port also becomes yours: sailing up to it unloads the hold there, and no fleet guards it.

| Realm | Perk | Holdings (base cost → gold/sec each) |
|---|---|---|
| **Redtide Hold** (corsair) | Treasure, flotsam and prize ships yield **double gold**; the hold carries **50% more** | Rum Distillery 20K → 60 · Dice House 220K → 380 · Fence's Den 2.4M → 2,200 · Chart-maker's Loft 26M → 12K · Prize Court 300M → 65K |
| **Karak Brine** (dwarven) | Forging and shipwright jobs take **half the time**; expeditions bring back **25% more** stone and ore | Ale Cellars 100K → 250 · Stonecutters' Guild 1.1M → 1,500 · Deep Forges 12M → 8,500 · Rune Hall 130M → 48K · Mithril Vault 1.5B → 270K |
| **Skarholm** (frost jarl) | Ship **20% faster** with **25% more hull**; hero **+25 max health** | Whaling Camp 500K → 1,100 · Fur Traders 5.5M → 6,500 · Mead Hall 60M → 37K · Longship Sheds 650M → 210K · Skalds' Circle 7B → 1.2M |
| **Sylvanreach** (elven) | Crystal mine **50% faster**; Verdant draughts heal **75%** | Silk Groves 2M → 4,200 · Moonwell 22M → 24K · Archers' Glade 240M → 140K · Starwatch 2.6B → 800K · Elder Tree 28B → 4.5M |

Each realm's Keep view is its own island: the castle drawn large (corsair palisade and watchtower, dwarven sea-fort with a golden door, snow-roofed longhall, white elven spires), the sea behind, its own trees (palms, bare rock, snowy pines, forest), and a house for each holding you own, which grows as you build more.

## Ascension

The shipyard, ship, cargo, charted islands, broken fleets and claimed castles (with their holdings) all reset on ascension. Log entries for islands, ships and realms stay.
