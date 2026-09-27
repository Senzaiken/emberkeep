# Expeditions

The hero can be on **one expedition at a time**. Each trip is a journey you can watch: loot, foes, treasure and road events come up one after another along the way, and the haul trickles in as it happens.

## How a trip works

When the hero departs, the whole trip is planned up front as a **timeline**:

- **Beats**: things the hero meets on the road, each at a set moment:
  - **Resource nodes**: trees (wood), boulders (stone), ore rocks with coloured veins (copper, tin, iron), and crystal clusters.
  - **Foes**: they guard a resource and drop it when beaten, but they hurt the hero ([Hero](hero.md)). About 20% of resource beats are foes.
  - **Treasure chest**: a 15% chance per trip, and it holds gold.
- **Road events**: choice cards partway through longer trips (see below).

Because everything is timestamped, a trip plays out the same whether you watch it, switch tabs or close the game. Loot is granted when each beat's moment passes.

The number of beats is about one per 5 seconds of travel, between 3 and 48. The trip's total loot is rolled from the region's ranges (below) and split across its beats.

## Watching the journey

Departing switches the canvas to the **Journey** view: a side-scrolling scene of the region with parallax layers. The **Keep / Journey** switch in the canvas corner flips between the two, and the Explore tab's **Watch** button does the same.

- The hero's look reflects the forge: armor colour, a shield from Oaken Buckler up, a helmet from Copper Scale up, and the current weapon (or pickaxe when mining).
- A health bar floats above the hero, and a **!** appears when a road event is waiting.
- The scene follows the day/night cycle, except Ironroot Deep, which is a torch-lit cave.

### Tap to help

Tap something ahead of the hero before they reach it:

| Target | Effect |
|---|---|
| Resource node | +50% of that node's loot (minimum +1) |
| Foe | +50% loot, and the foe deals **half damage** |
| Crystal cluster | 35% chance of +1 crystal |
| Treasure chest | ×1.5 gold |

Each beat can be helped once, and it gets a ✦ marker when you do.

## Regions

| Region | Health cost | Base time | Danger | Foes | Hit damage | Relic chance | Loot (before bonuses) |
|---|---:|---:|---:|---|---:|---:|---|
| Whisperwood | 10 | 20s | 0 | Wild Boar, Grey Wolf | 6 | 6% | 4–7 wood, 0–2 stone |
| Greystone Quarry | 15 | 45s | 0 | Grey Wolf, Bandit | 8 | 8% | 5–8 stone, 1–3 copper |
| Copperfen Hills | 22 | 90s | 1 | Bog Lurker, Goblin | 12 | 10% | 5–9 copper, 2–5 tin, 2–4 stone |
| Ironroot Deep | 30 | 3m | 2 | Goblin, Cave Bat | 16 | 12% | 5–9 iron, 1–3 tin, 1–2 crystals |
| Shattered Caldera | 45 | 6m | 3 | Fire Imp, Salamander | 22 | 15% | 8–14 iron, 4–8 copper, 3–5 crystals |

**Health cost** is paid when the hero sets out ([Hero](hero.md)). **Danger** is the armor tier needed to enter. Expedition crystals are a random element.

## Road events

Trips of 40 seconds or more get road events: 1 event under 2 minutes, 2 events under 5 minutes, and 3 beyond that. Each is picked from the region's pool, with no repeats in a trip.

A card slides up with 2–3 choices and a **20-second timer**. If you don't choose, the hero takes the **default**, which is always free and safe. That way idle play is never punished, and active play is rewarded. Choices that extend the trip push everything still ahead back by that time and add the new beats in the gap.

| Event | Regions | Choices (default in bold) |
|---|---|---|
| Goblin Toll Bridge | all | Pay a gold toll · Fight (win chance from weapon vs. danger: stash of gold + 30% extra primary loot; lose: −20% HP and +10s) · **Wait them out (+15s)** |
| A Glinting Vein | quarry, fen, deep, caldera | Mine it (+20s, +40% of the trip's primary ore) · **Press on** |
| A Fallen Giant | wood | Chop it up (+15s, +50% wood) · **Climb over** |
| Abandoned Camp | all | Search the packs (30% relic, 35% gold purse, 35% ambush for −15% HP) · **Leave it** |
| Wounded Traveller | all | Tend the wound (1 Verdant: gold + 40% relic chance) · Share rations (+10s, a little gold) · **Walk on** |
| Crystal Seep | fen, deep, caldera | Harvest it (+25s, 2–4 random crystals) · **Leave it** |
| Wayside Shrine | all | Leave a gold offering (+50% loot for the rest of the trip) · Kneel and rest (+10s, heal 30% HP) · **Pass by** |

Gold costs and rewards scale with your gold/sec and tap value, so they stay meaningful as you grow.

## Bonuses

| Source | Effect |
|---|---|
| Armor tier | Trips take 8% less time per tier. Also reduces foe damage (see [Hero](hero.md)). |
| Weapon tier | Wood yield × (1 + 0.25 × tier). Better odds in fights. |
| Pickaxe tier | Stone and ore yield ×1, 1.25, 1.5, 2, 2.5 |
| Relics | Resource yields, trip speed, crystal drops, relic chance (see [Relics](relics.md)) |
| Hasten (1 Storm crystal, once per trip) | Halves the remaining trip time |
| Quickened Road (spell) | Ends the trip at once: road events take their default, remaining beats are collected, and foes on the rest of the road do no harm |

## End of a trip

When the timer runs out and every road event is settled, the hero comes home. A toast lists the full haul, and there's a chance to find a relic. The view switches back to the keep a moment later.

If the hero's health reaches 0 on the road, the trip ends early. They keep what they had already gathered, but there's no relic roll.
