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
- The expedition timeline plays forward: new depths are generated, beats are collected into the carried haul, foes deal damage, draughts are drunk, the hero turns back by the turn-back setting, overdue road events take their default, and a hero who reaches home banks the haul. A trip that has run 8 hours turns for home by itself.
- The hero heals while resting at the keep.

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
| `exp` | Current expedition or `null`: `{v:2, id, start, len, pause, gen, rolled, deepest, beats[], events[], used[], carry{}, pack, blessed, seq, returning, retAt, end, hasted}`. `len` is ms per depth, `pause` is time added by road events, `gen` the last depth generated, `carry` the haul not yet banked, `pack` draughts left. Each beat is `{id, t, st, k, r, n, done, tap, bonus?, foe?, cut?, ret?}` (`st` depth, `cut` skipped by turning back, `ret` a foe on the road home), and each event is `{id, t, deadline, done, choice, cut?}`. Saves with an older fixed-length trip bank its remaining loot and clear it on load. |
| `retreat`, `pack` | Turn-back setting (index into 50% / 30% / 15% / Never, default 1) and the number of Verdant draughts to pack. Kept through ascension. |
| `wounded` | `true` after a defeat, until the hero is back to full health (halves resting). |
| `hp` | Hero health |
| `relics` | Relic levels, by id |
| `story` | `{intro, met, brom}`: seen the opening, met Arthrex, met Brom |
| `seen` | Resources the player has discovered (shown in the satchel) |
| `favs` | Starred spell ids, in order (the quick-cast bar) |
| `tut`, `tutV`, `tutBase` | Tutorial step index (`null` = not started, past the last step = finished or skipped), tutorial version (3; saves on version 2 at step 7 or later move up one for the new Return home step), and an old tap-count field |
| `quest`, `questNext`, `questSpan` | Arthrex's current errand (or `null`), when the next one is offered, and the length of that wait (for the progress bar) |
| `stats` | Lifetime counters: `trips{region}`, `foes`, `foeKinds{}`, `tapGold`, `relics`, `quests`, `casts` |
| `dynasty` | Current life number (1 + ascensions) |
| `log`, `logNew`, `logInit` | Adventurer's Log entries `{id: {t, life}}`, unseen count, and whether the one-time backfill ran |
| `mine`, `mineAcc` | Crystal Mine depth and progress toward the next crystal |
| `forging` | Brom's current job `{slot, start, end}` or `null` |
| `digging` | The gallery being dug `{level, start, end}` or `null` |
| `taps`, `chron`, `last` | Tap count, chronicle flags, last tick timestamp |

If the save shape changes in a way old saves can't load, bump the key (for example `-v3`) and note it in the [Changelog](changelog.md).

## Updates and caching

GitHub Pages lets browsers cache the page for about 10 minutes, and home-screen apps hold on to it longer. To get around that:

- Every commit that touches the game stamps a new build id into `index.html` (`const BUILD`) and `version.json`, using the `tools/pre-commit` hook.
- The game fetches `version.json` with caching disabled 3 seconds after opening, whenever it comes back to the foreground, and every 2 minutes. If the build differs, a **"A new version of Emberkeep is ready"** banner appears.
- **Reload** saves the game, then reopens the page as `?v=<build>`. The unique URL forces fresh files.
- Legacy tab → **Check for updates** does the same check on demand and reloads right away if there's a new build. The current build id is shown next to it.

## Resetting

Legacy tab → **Start from nothing** (tap twice to confirm) wipes everything, including Renown.
