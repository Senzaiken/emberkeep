# Expeditions

The hero can be on **one expedition at a time**. Trips are **open-ended**: the hero keeps going deeper into the region until you call them home, their health falls to your turn-back point, or they're beaten. Each trip is a journey you can watch: loot, foes, treasure and road events come up one after another.

## Depth

A trip is made of **depths**. Each depth lasts the region's base time (Whisperwood 20s up to the Caldera 6m, shortened by armor and relics), and each one deeper is richer and more dangerous:

| Per depth deeper | |
|---|---|
| Loot (resources, crystals, chest gold) | +25% |
| Foe damage | +15% |
| Relic chance at the end of each depth | +10% (base: 60% of the region's relic chance) |
| Treasure chest chance | 15% at depth 1, +3% per depth, up to 50% |

Loot grows faster than damage, so going deeper is more efficient per point of health, but a single hit hurts more and the walk home gets harder.

## Carried loot

Everything found on the road (resources, crystals, event gold, chest gold) is **carried**, not banked. It reaches your stores only when the hero gets home safely. If the hero is **beaten** (health 0), **half the haul is lost**, along with any unused draughts. **Relics** are the exception: they're kept the moment they're found.

## Preparations

The Explore tab has a **preparations** card above the regions:

| Setting | Options | Effect |
|---|---|---|
| **Turn back at** | 50% · 30% (default) · 15% · Never | When health drops to this share of max after a hit, the hero turns for home by themselves. |
| **Verdant draughts** | 0 up to **2 + armor tier** (max 6), plus 2 per **Moonsilk satchel** (up to 3 satchels, sewn from Sylvanreach's moonsilk in the same card), limited by the Verdant crystals you hold | Taken from your crystals when the hero departs. Below **40% health** the hero drinks one and heals 50% of max. Unused draughts come home on a safe return, and are lost on defeat. |

Both settings are remembered. Draughts are checked before the turn-back point, so a packed hero drinks first and turns back only once the draughts run out.

## The road home

Turning back (by the **Return home** button, the turn-back point, or after 8 hours on the road) starts a **walk home** lasting 15% of the time spent out, between 6 and 30 seconds. Nothing new is found on the way back, but **foes wait on the road home**:

| Depth reached | Foes on the way back |
|---|---:|
| 1 | 0 |
| 2–3 | 1 |
| 4–6 | 2 |
| 7–9 | 3 |
| 10–12 | 4 |
| 13+ | 5 |

They hit at the depth-reached strength, and you can tap them (they come from the left now) for half damage. Each drops a little of the region's main resource. The journey bar shows how rough the road home looks from where the hero is now, so you can judge when to call them back.

This is the risk/reward in the turn-back setting: **50%** banks steadily, **15%** is greedy and can end in a rout at depth, and **Never** is for a well-packed hero you're watching.

## How the road is built

Each depth is planned as a **timeline** as the hero reaches it:

- **Beats**: things the hero meets on the road, each at a set moment:
  - **Resource nodes**: trees (wood), boulders (stone), ore rocks with coloured veins (copper, tin, iron), and crystal clusters.
  - **Foes**: they guard a resource and drop it when beaten, but they hurt the hero ([Hero](hero.md)). About 20% of resource beats are foes.
  - **Treasure chest**: a 15% chance per trip, and it holds gold.
- **Road events**: choice cards partway through longer trips (see below).

Because everything is timestamped, a trip plays out the same whether you watch it, switch tabs or close the game (the hero keeps exploring while you're away, drinking and turning back by your settings). Loot is added to the carried haul when each beat's moment passes. Beats long behind the hero are dropped from the save to keep it small.

Each depth has about one beat per 5 seconds, between 3 and 12. The depth's loot is rolled from the region's ranges (below), multiplied by the depth bonus, and split across its beats.

## Watching the journey

Departing switches the canvas to the **Journey** view: a side-scrolling scene of the region with parallax layers. The **Keep / Journey** switch in the canvas corner flips between the two, and the Explore tab's **Watch** button does the same.

- The hero's look reflects the forge: armor colour, a shield from Oaken Buckler up, a helmet from Copper Scale up, and the current weapon (or pickaxe when mining).
- A health bar floats above the hero, and a **!** appears when a road event is waiting.
- On the walk home the hero turns round, moves to the right of the view, and the road scrolls back the other way.

### Journey bar

Under the scene while you watch: the depth, **everything carried** item by item (gold, each material and crystal, with icons), roughly what foes hit for, how many foes wait on the road home, draughts left, and your turn-back point, with a **Return home** button. On the walk home it shows the time left, the foes still ahead, and **Hasten**.
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

| Region | Health cost | Time per depth | Danger | Foes | Hit damage (depth 1) | Relic chance | Loot per depth (before bonuses) |
|---|---:|---:|---:|---|---:|---:|---|
| Whisperwood | 10 | 20s | 0 | Wild Boar, Grey Wolf | 6 | 6% | 4–7 wood, 0–2 stone |
| Greystone Quarry | 15 | 45s | 0 | Grey Wolf, Bandit | 8 | 8% | 5–8 stone, 1–3 copper |
| Copperfen Hills | 22 | 90s | 1 | Bog Lurker, Goblin | 12 | 10% | 5–9 copper, 2–5 tin, 2–4 stone |
| Ironroot Deep | 30 | 3m | 2 | Goblin, Cave Bat | 16 | 12% | 5–9 iron, 1–3 tin, 1–2 crystals |
| Shattered Caldera | 45 | 6m | 3 | Fire Imp, Salamander | 22 | 15% | 8–14 iron, 4–8 copper, 3–5 crystals |

**Health cost** is paid when the hero sets out ([Hero](hero.md)). **Danger** is the armor tier needed to enter. Expedition crystals are a random element.

## Road events

Regions with depths of 40 seconds or more (every region but Whisperwood) have a 50% chance of a road event halfway through each depth. Each is picked from the region's pool, avoiding repeats until the pool runs out. Events still ahead are skipped once the hero turns for home.

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
| Armor tier | Each depth takes 8% less time per tier. Also reduces foe damage (see [Hero](hero.md)) and lets the hero carry one more draught. |
| Weapon tier | Wood yield × (1 + 0.25 × tier). Better odds in fights. |
| Pickaxe tier | Stone and ore yield ×1, 1.25, 1.5, 2, 2.5 |
| Relics | Resource yields, trip speed, crystal drops, relic chance (see [Relics](relics.md)) |
| Hasten (1 Storm crystal, once per trip, on the journey bar during the walk home) | Halves the rest of the walk home, and brings its foes closer to match |
| Quickened Road (spell) | The hero is home at once with the whole haul, skipping the walk and its foes. Waiting road events take their default. |

## End of a trip

When the hero reaches the keep, the carried haul is banked, unused draughts go back to your crystals, and a toast lists everything with the depth reached. The view switches back to the keep a moment later. Only safe returns count as completed trips (for errands and achievements).

If health reaches 0 anywhere (out or on the way home), the hero is **beaten back**: half the haul and all draughts are lost, and the hero comes home **wounded** (see [Hero](hero.md#defeat)).

Saves from before open-ended trips bring an old fixed trip straight home on load, with its remaining loot.
