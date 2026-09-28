# Forge

The forge is run by **Brom, Master Smith**, who introduces it during the tutorial (see [Story](story.md#brom-master-smith)).

The hero has three equipment slots. Each slot upgrades one tier at a time using gold plus materials from [Expeditions](expeditions.md). Equipment **resets on ascension**.

Material progression: **wood and stone → copper → bronze (copper + tin) → iron**.

## Forging takes time

Brom works on **one piece at a time**. You pay when you start, and the piece is equipped automatically when it's done, including while the game is closed.

| Tier | Forging time |
|---:|---:|
| 1 | 15s |
| 2 | 1m |
| 3 | 3m |
| 4 | 8m |

**Stoke the forge** (1 Ember crystal) halves the time left, and you can use it repeatedly. It's on the anvil card at the top of the Forge tab. A ⚒ countdown shows near the keep while he works. Anything in progress is lost on ascension, along with the gear.

## Weapon

Multiplies tap gold and boosts wood from expeditions.

| Tier | Item | Cost | Tap gold | Wood yield |
|---:|---|---|---:|---:|
| 0 | Bare Fists | — | ×1 | ×1 |
| 1 | Oak Cudgel | 50 gold, 12 wood | ×2 | ×1.25 |
| 2 | Copper Blade | 1,000 gold, 10 wood, 20 copper | ×4 | ×1.5 |
| 3 | Bronze Sword | 20K gold, 10 wood, 25 copper, 15 tin | ×8 | ×1.75 |
| 4 | Iron Longsword | 400K gold, 20 wood, 40 iron | ×16 | ×2 |

## Armor

Sets how dangerous a region the hero can enter, and shortens trips.

| Tier | Item | Cost | Reaches danger | Trip time |
|---:|---|---|---:|---:|
| 0 | Travelling Cloak | — | 0 | 100% |
| 1 | Oaken Buckler | 40 gold, 15 wood | 1 | 92% |
| 2 | Copper Scale | 800 gold, 30 copper, 5 wood | 2 | 84% |
| 3 | Bronze Mail | 15K gold, 30 copper, 20 tin | 3 | 76% |
| 4 | Iron Plate | 300K gold, 60 iron, 20 stone | 4 | 68% |

## Pickaxe

Boosts ore and stone from expeditions, and speeds up the [Crystal Mine](magic.md).

| Tier | Item | Cost | Ore yield | Crystal speed |
|---:|---|---|---:|---:|
| 0 | Bare Hands | — | ×1 | ×1 |
| 1 | Stone Pick | 30 gold, 10 wood, 10 stone | ×1.25 | ×1.5 |
| 2 | Copper Pick | 600 gold, 10 wood, 20 copper | ×1.5 | ×2.25 |
| 3 | Bronze Pick | 12K gold, 10 wood, 20 copper, 10 tin | ×2 | ×3.5 |
| 4 | Iron Pick | 250K gold, 10 wood, 30 iron | ×2.5 | ×5 |

## Enchantments

Below the anvil, the Forge tab has **Enchantments**: Brom forges, Arthrex binds. Each item can be enchanted without limit, paid in one element's crystals. Level *n* → *n+1* costs `ceil(3 × 1.35^n)` crystals: 3, 5, 6, 8, 10, 14, … about 60 at level 10 and 270 at level 15.

| Item | Crystal | Per level |
|---|---|---|
| Weapon | Ember | +10% tap gold |
| Armor | Frost | Foe damage ×0.97 (so −26% at level 10) |
| Pickaxe | Verdant | +8% stone and ore from expeditions |
| Ship's hull | Verdant | +6% max hull (shown once the shipyard is built) |
| Ship's ballistae | Storm | +6% bolt damage (shown once the shipyard is built) |

Enchantments belong to the item, not the tier, so they carry over when Brom or Maren upgrades it. They reset on ascension, like the gear itself.
