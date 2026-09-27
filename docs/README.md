# Emberkeep Wiki

Design and technical documentation for Emberkeep, a medieval fantasy idle game. These pages describe the game as it is currently built. When a mechanic changes, its page changes in the same commit.

**Play:** https://senzaiken.github.io/emberkeep/

## Pages

| Page | What it covers |
|---|---|
| [Overview](overview.md) | Concept, core loop, stack, hosting, how we work |
| [Economy](economy.md) | Gold, tapping, holdings, upgrades, Renown and ascension |
| [Expeditions](expeditions.md) | Trip timeline, the Journey view, tap to help, road events, regions |
| [Hero](hero.md) | Health, damage, defeat, healing, how the hero looks |
| [Relics](relics.md) | Rare finds, levels, the full collection |
| [Forge](forge.md) | Hero equipment slots, tiers, recipes and effects |
| [Magic](magic.md) | Elemental crystals, the Crystal Mine, learning and casting spells |
| [Day and Night](day-night.md) | The 10-minute cycle and what it affects |
| [Saving](saving.md) | Save data, offline progress, resetting |
| [Roadmap](roadmap.md) | Planned work and open design questions |
| [Changelog](changelog.md) | What changed, and when |

## Conventions

- Numbers in these pages match the constants in `index.html`. If they disagree, the code is the truth and the page needs fixing.
- "Reign" means the time since the last ascension. "Lifetime" means since the save was created.
- Timings are prototype values, kept short for testing. The Roadmap tracks real tuning.
