# Magic

Magic in Emberkeep is powered by **elemental crystals**. There is no mana: every spell consumes crystals as reagents.

## Elemental crystals

| Crystal | Element | Colour |
|---|---|---|
| Ember | Fire | Orange-red |
| Frost | Water / ice | Pale blue |
| Verdant | Earth / life | Green |
| Storm | Air / lightning | Violet |

Sources: the Crystal Mine (steady, over time) and the deeper [Expeditions](expeditions.md) (random element).

## Crystal Mine

Opened and deepened with gold and materials. Each gallery adds an element and digs faster. Mining continues while the game is closed. Glowing shards appear on the eastern slope once the mine is open.

| Depth | Name | Cost | Yields | Base time per crystal |
|---:|---|---|---|---:|
| 1 | Crystal Mine | 250 gold, 20 wood, 15 stone | Ember, Frost | 30s |
| 2 | Verdant Gallery | 5,000 gold, 40 stone, 15 copper | + Verdant | 22s |
| 3 | Storm Vault | 100K gold, 60 stone, 30 iron | + Storm | 15s |
| 4 | The Heartvein | 2M gold, 80 iron, 40 tin | all four | 9s |

```
secondsPerCrystal = baseTime / (pickaxeCrystalMult × (1 + 0.1 × wizardTowers))
```

Each crystal is a random element from those the current depth yields. The mine resets on ascension.

## Spells

Spells must be **learned individually** (a one-time cost in gold and crystals). After that, each cast costs crystal reagents. Learned spells are **kept through ascension**.

| Spell | Learn cost | Reagents per cast | Effect |
|---|---|---|---|
| Midas Touch | 300 gold, 3 Ember | 1 Ember | Taps earn ×10 gold for 20s |
| Summon Familiar | 2,500 gold, 3 Storm | 1 Storm | A wisp taps the keep 8×/sec for 20s |
| Quickened Road | 4,000 gold, 3 Frost, 2 Storm | 1 Frost, 1 Storm | Hero returns from the current expedition at once |
| Bountiful Harvest | 8,000 gold, 3 Verdant | 1 Verdant, 1 Frost | All holdings produce ×3 for 30s |
| Dragon's Tithe | 1M gold, 5 of each crystal | 1 of each crystal | Collect 5 minutes of production at once |

A timed spell can't be recast while it's active. Quickened Road can only be cast while the hero is away.
