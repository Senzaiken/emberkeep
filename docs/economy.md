# Economy

## Gold

Gold comes from **tapping the keep** and from **holdings** that produce it every second. The game ticks every 100 ms.

### Tap value

```
tap = (1 + flatBonus) × tapMult × weaponMult × renownMult  +  goldPerSec × tapPct
```

The result is ×10 while **Midas Touch** is active. `weaponMult` comes from the [Forge](forge.md): ×1, 2, 4, 8, 16 by weapon tier.

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
| Wizard Tower | 20M | 7,800 | Also speeds the Crystal Mine by 10% each |
| Dragon's Lair | 330M | 44,000 | A dragon circles the sky |

A holding is revealed once the previous one is owned, or once the reign has earned half its base cost. The next hidden one shows as "Unknown holding".

Castle windows light up as you own more holdings: one more window per 4 holdings.

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

- Renown earned on ascending: `floor(sqrt(reignGold / 1,000,000))`, so the first point needs 1M gold in one reign.
- Each point of Renown adds **+5%** to all gold (taps and holdings).
- **Ascending resets:** gold, holdings, upgrades, materials, crystals, the Crystal Mine, any running expedition and active spells.
- **Ascending keeps:** Renown, hero equipment, learned spells, lifetime stats.
