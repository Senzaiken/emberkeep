# Saving

## Where saves live

The whole game state is saved as JSON in the browser's `localStorage` under the key `emberkeep-save-v2`, on the `senzaiken.github.io` site.

- Saved every 3 seconds, and whenever the app is hidden or closed.
- A home-screen shortcut and Safari share the same save for the site.
- The save is per device and per browser. There is no cloud sync yet (see [Roadmap](roadmap.md)).
- Deleting and re-adding the home-screen shortcut does not erase the save. Clearing Safari's website data does.

## Offline progress

When the game resumes after more than 10 seconds away, it credits the time missed, **capped at 8 hours**:

- Gold from holdings (temporary spell boosts don't count toward offline time).
- Crystals from the Crystal Mine.
- A finished expedition is collected.

A toast summarises what was earned while away.

## Save shape

Top-level fields of the saved object (see `fresh()` in `index.html`):

| Field | Meaning |
|---|---|
| `gold`, `total`, `life` | Current gold, gold earned this reign, gold earned ever |
| `owned` | Holdings owned, by id |
| `up` | Purchased upgrade ids |
| `renown` | Renown points |
| `mat`, `cry` | Materials and crystals |
| `gear` | Tier per slot: `weapon`, `armor`, `pick` |
| `known`, `spells` | Learned spell ids; active spell expiry timestamps |
| `exp` | Current expedition `{id, start, end}` or `null` |
| `mine`, `mineAcc` | Crystal Mine depth and progress toward the next crystal |
| `taps`, `chron`, `last` | Tap count, chronicle flags, last tick timestamp |

If the save shape changes in a way old saves can't load, bump the key (for example `-v3`) and note it in the [Changelog](changelog.md).

## Resetting

Ascend tab → **Start from nothing** (tap twice to confirm) wipes everything, including Renown.
