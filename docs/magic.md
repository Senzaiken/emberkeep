# Magic

Magic in Emberkeep is powered by **elemental crystals**. There is no mana: every spell consumes crystals as reagents.

## Elemental crystals

| Crystal | Element | Colour |
|---|---|---|
| Ember | Fire | Orange-red |
| Frost | Water / ice | Pale blue |
| Verdant | Earth / life | Green |
| Storm | Air / lightning | Violet |

Sources: the Crystal Mine (steady, over time) and the deeper [Expeditions](expeditions.md) (random element). Verdant crystals can also be packed as **draughts** that the hero drinks on the road.

## Crystal Mine

Opened and deepened with gold and materials. Each gallery adds an element and digs faster. Mining continues while the game is closed. Glowing shards appear on the eastern slope once the mine is open.

| Depth | Name | Cost | Yields | Base time per crystal |
|---:|---|---|---|---:|
| 1 | Crystal Mine | 250 gold, 20 wood, 15 stone | Ember, Frost | 30s |
| 2 | Verdant Gallery | 5,000 gold, 40 stone, 15 copper | + Verdant | 22s |
| 3 | Storm Vault | 100K gold, 60 stone, 30 iron | + Storm | 15s |
| 4 | The Heartvein | 2M gold, 80 iron, 40 tin | all four | 9s |

```
secondsPerCrystal = baseTime / (pickaxeCrystalMult × (1 + 0.1 × apprenticeHalls) × (1 + relicMineBonus))
```

Each crystal is a random element from those the current depth yields. The mine resets on ascension.

### Digging takes time

Each gallery is a construction job. Pay the cost, and the miners dig for a while. The current level keeps producing in the meantime.

| Gallery | Dig time |
|---|---:|
| Crystal Mine (opening) | 30s |
| Verdant Gallery | 2m |
| Storm Vault | 5m |
| The Heartvein | 12m |

**Split the rock** (1 Frost crystal) halves the time left, and you can use it repeatedly. It's on the mine row. A ⛏ countdown floats over the mine site in the keep view.

## Transmutation

Once you've met Arthrex, the Magic tab has a **Transmutation** section: he turns crystals into materials, one, ten, or all at a time.

| Crystal | Base yield per crystal |
|---|---|
| Ember | 3 iron, 2 copper |
| Frost | 6 stone, 2 tin |
| Verdant | 10 wood |
| Storm | 2 each of wood, stone, copper, tin and iron |

The yield is multiplied by `(1 + 0.5 × (mine depth − 1)) × (1 + 0.03 × Renown)`, rounded down. At the Storm Vault (depth 3) with 10 Renown that's ×2.6. Keep a few crystals back for Mend, draughts, Hasten, stoking and splitting.

## Arthrex

The court sorcerer explains crystals after your first expedition and gives you 10 of each. He then sets errands that pay in crystals. See [Story and Arthrex](story.md).

## Spells

Spells must be **learned individually** (a one-time cost in gold and crystals). After that, each cast costs crystal reagents. Learned spells **reset on ascension** and must be learned again.

| Spell | Learn cost | Reagents per cast | Effect |
|---|---|---|---|
| Midas Touch | 300 gold, 3 Ember | 1 Ember | Taps earn ×10 gold for 20s |
| Summon Familiar | 2,500 gold, 3 Storm | 1 Storm | A wisp taps the keep 8×/sec for 20s |
| Quickened Road | 4,000 gold, 3 Frost, 2 Storm | 1 Frost, 1 Storm | Hero is home at once with the whole carried haul, skipping the walk home and its foes. Waiting road events take their default. |
| Bountiful Harvest | 8,000 gold, 3 Verdant | 1 Verdant, 1 Frost | All holdings produce ×3 for 30s |
| Dragon's Tithe | 1M gold, 5 of each crystal | 1 of each crystal | Collect 5 minutes of production at once |

A timed spell can't be recast while it's active. Quickened Road can only be cast while the hero is away.

## Spellbook

The **book button** to the right of the hero's health bar opens the spellbook, a bottom sheet with everything you can cast right now:

- **Mend** (1 Verdant: heal 50%). It's always there and doesn't need learning.

The other crystal actions live where they're used, not in the spellbook: **Hasten** (1 Storm, halves the walk home) is on the journey bar under the Journey view, **Stoke the Forge** (1 Ember) is on Brom's anvil card, and **Split the Rock** (1 Frost) is on the mine row. Each crystal element has an everyday use. See [Hero](hero.md#crystal-quick-actions).
- Every spell you've **learned**, with its reagent cost and a Cast button.

Each entry shows why it can't be cast right now, if it can't (for example "Only while your hero is away", or the time left on an active spell). Your crystal counts are shown at the top. A violet dot on the book means Mend is worth casting: the hero is below half health and you have a Verdant crystal. **Open grimoire** jumps to the Magic tab, where new spells are learned.

### Starred spells (quick-cast bar)

Tap the **☆** beside any spellbook entry to star it (★). Starred spells appear as round icons with short labels in a row **just below** the castle scene (outside the tap area, so they can't be hit by accident when tapping the keep), in the order you starred them. The row scrolls sideways if it gets long. You can star as many as you like.

| Icon state | Meaning |
|---|---|
| Colored orb | Ready: tap to cast |
| Greyed out | Can't cast right now: not enough crystals, or not applicable (for example Quickened Road while the hero is home). Tapping explains why. |
| Colored, with a dark ring draining and seconds shown | Already active; the ring shows the time left |

Each spell has its own glyph in its element colour: Mend (cross, Verdant), Midas Touch (crown, gold), Summon Familiar (swirl, Storm), Quickened Road (fast-forward, Frost), Bountiful Harvest (wheat, Verdant), Dragon's Tithe (gem, Ember).
