# The Sea

Once the keep is well established, a **Harbor** opens: build a shipyard, take the helm of your own ship, and sail the Ember Sea to chart islands and dig up treasure. Four foreign castles stand on the far islands, each of a different people. Claiming them comes in later updates (see [Roadmap](roadmap.md#the-sea)).

## Unlocking

The **Harbor** tab appears once you have **Copper Scale** armor (tier 2) and have dug the **Verdant Gallery** (mine depth 2). With the Harbor tab, the tab bar becomes four columns.

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

## Foreign castles

| Castle | People | Island |
|---|---|---|
| Karak Brine | Dwarven sea-fort | A rocky stack to the north |
| Skarholm | Frost jarl's hall | An island of ice and pine, far north-east |
| Sylvanreach | Elven isle | White spires in a forest, far south-east |
| Redtide Hold | Corsair stronghold | A timber palisade on a sandy isle to the south |

For now their harbor chains are raised: they need a warship. Ship battles and claiming castles come next.

## Ascension

The shipyard, ship, cargo and charted islands reset on ascension. Log entries for islands stay.
