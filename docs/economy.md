# Economy

## Gold

Gold comes from **tapping the keep** and from **holdings** that produce it every second. The game ticks every 100 ms.

### Tap value

```
tap = (1 + flatBonus) × tapMult × weaponMult × renownMult  +  goldPerSec × tapPct
```

`renownMult` here means all-gold multipliers: Renown × (1 + relic "all gold" bonuses). The Fossil Idol relic adds a further tap-only multiplier. The result is ×10 while **Midas Touch** is active. `weaponMult` comes from the [Forge](forge.md): ×1, 2, 4, 8, 16 by weapon tier.

### Holdings

Each purchase multiplies the next one's price by **1.15**. The Build tab can buy ×1, ×10, or the maximum you can afford.

| Holding | Base cost | Gold/sec each | Notes |
|---|---:|---:|---|
| Peasant Farm | 15 | 0.1 | Fields appear in the foreground |
| Watermill | 100 | 1 | Turning wheel |
| Tavern | 1,100 | 8 | Chimney smoke |
| Silver Mine | 12,000 | 47 | Mine entrance in the eastern hill |
| Market Square | 130,000 | 260 | Tents by the gate |
| Merchant Guild | 1.4M | 1,400 | Banners on the towers |
| Apprentice Hall | 20M | 7,800 | Arthrex's apprentices. Each also speeds the Crystal Mine by 10%, and adds a floating light around the spire (up to 6). The save id is still `tower`. |
| Dragon's Lair | 330M | 44,000 | A dragon circles the sky |

A holding is revealed once the previous one is owned, or once the reign has earned half its base cost. The next hidden one shows as "Unknown holding".

Castle windows light up as you own more holdings: one more window per 4 holdings.

Claimed castles add five holdings each, in their own realm. See [The Sea](sea.md#claimed-castles-realms). Holding achievements count only these eight home holdings.

## Upgrades

### Holding techniques

Each holding has five techniques. Each one doubles that holding's output.

| Tier | Unlocks at | Cost |
|---|---:|---|
| 1 | 1 owned | 10 × base cost |
| 2 | 10 owned | 50 × base |
| 3 | 25 owned | 500 × base |
| 4 | 50 owned | 50,000 × base |
| 5 | 100 owned | 5,000,000 × base |

### Tap upgrades

These unlock in order, each one once the previous is bought and the reign has earned 30% of its cost.

| Upgrade | Cost | Effect |
|---|---:|---|
| Leather Coin Purse | 50 | +1 gold per tap |
| Tax Collector's Ledger | 600 | Tap gold ×2 |
| Alchemist's Palm | 8,000 | Taps also earn 1% of gold/sec |
| Gilded Gauntlet | 150K | Tap gold ×2 |
| Philosopher's Stone | 5M | Taps earn another 2% of gold/sec |
| Crown of Avarice | 200M | Tap gold ×3 |

## Renown and ascension

- Renown earned on ascending: `floor(cbrt(reignGold / 10,000,000))`. The first point needs 10M gold in one reign; 10 points need 10B, 46 need 1T, 100 need 10T.
- Each point of Renown ever earned adds **+2%** to all gold (taps and holdings), forever.
- Renown is also **spent** in the Legacy tree (below). Spending never lowers the +2% bonus: the bonus counts all Renown earned, spent or not.
- **Ascending is a full reset:** gold, holdings, upgrades, hero equipment (and anything Brom is forging), learned spells, relics, materials, crystals, the Crystal Mine, any running expedition, active spells and Arthrex's current errand.
- **Ascending keeps:** Renown (and its gold bonus), the [Adventurer's Log](log.md) (and the life number goes up by one), lifetime stats, story progress (the tutorial isn't replayed, and Arthrex and Brom remember you), discovered resources, and starred spells (they show again once relearned). The hero starts at full health.

### Legacy tree

The tree opens as a sheet **right after you ascend** (it isn't shown in the Legacy tab, which only notes any unspent Renown). Each node has levels, bought in order with Renown, and purchases are permanent. Head starts apply right away, to the life just begun, and at the start of every life after. **Begin your reign** closes the sheet; anything unspent waits for the next ascension.

| Node | Levels | Cost per level | Each level |
|---|---:|---|---|
| Miners' Oath | 4 | 3 / 8 / 20 / 50 | Start with the mine dug to that depth (Crystal Mine → Heartvein) |
| Heirloom Blade | 4 | 2 / 6 / 16 / 40 | Start with that weapon tier (Oak Cudgel → Iron Longsword) |
| Heirloom Armor | 4 | 2 / 6 / 16 / 40 | Start with that armor tier (Oaken Buckler → Iron Plate) |
| Heirloom Pick | 4 | 2 / 6 / 16 / 40 | Start with that pickaxe tier (Stone Pick → Iron Pick) |
| Founder's Cache | 5 | 1 / 3 / 6 / 10 / 15 | Start with 150 wood, 100 stone, 50 copper, 30 tin, 20 iron per level (and get one bundle when bought) |
| Royal Treasury | 10 | 2, 4, … 20 | +10% gold |
| Quartermaster | 10 | 2, 4, … 20 | +10% materials from expeditions, island treasure, ship salvage, flotsam and transmutation |
| Hero's Vigor | 5 | 3 / 6 / 9 / 12 / 15 | +20 hero max health |
| Family Grimoire | 5 | 2 / 4 / 8 / 12 / 30 | Start knowing the grimoire's spells in order (Midas Touch → Dragon's Tithe) |
| Hereditary Shipyard | 2 | 25 / 50 | 1: start with the shipyard built. 2: also an Oak-ribbed Hull and Deck Ballistae |

The whole tree costs about 700 Renown, so it fills over many lives.

**Rescale (September 2026):** Renown used to be `floor(sqrt(reignGold / 1M))` with +5% gold per point, which snowballed. Saves from before were converted with `floor(cbrt(old² / 10))` (for example 400 → 25), and the old milestone boons were replaced by the tree.
