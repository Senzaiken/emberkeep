# Hero

The hero is the one who leaves the keep: expeditions, road events and fights. Their gear comes from the [Forge](forge.md), and their health limits how often they can set out.

## Health

| | |
|---|---|
| Max health | 100 + 25 × armor tier (+ relic bonuses) |
| Setting out | every expedition **costs health** up front: Whisperwood 10, Greystone Quarry 15, Copperfen Hills 22, Ironroot Deep 30, Shattered Caldera 45. The hero needs more health than the cost to depart. |
| Resting at the keep | heals from empty to full in 4 minutes (only while not on an expedition, including while the game is closed) |

Health is shown in the header, and as a small bar over the hero in the Journey view.

### Taking damage

- **Setting out**: the region's travel cost, paid when the hero departs.

- **Foes**: each foe on the road hits once when the hero reaches it, for the region's damage × `max(0.35, 1 − 0.12 × armor tier − 0.06 × weapon tier)`. Tapping the foe first halves the hit.
- **Road events**: losing the fight at the Goblin Toll Bridge costs 20% of max health, and an ambush at the Abandoned Camp costs 15%.

The Explore tab shows the approximate damage per hit for each region with your current gear.

### Defeat

If health reaches 0 mid-trip, the hero is beaten back. The trip ends immediately, everything already gathered is kept, and there's no relic roll. The hero must rest, or be mended, above the next trip's cost before leaving again.

### Healing

| Source | Amount |
|---|---|
| Resting at the keep | Full in 4 minutes |
| **Mend** (button under the health bar, 1 Verdant crystal) | 50% of max health, usable anytime, including on the road |
| Wayside Shrine event, "Kneel and rest" | 30% of max health (+10s to the trip) |

Health is the brake on endless exploring: trips cost health, resting takes time, and crystals let you skip the wait. It's also the planned hook for a premium item later, such as an instant full heal (see [Roadmap](roadmap.md)).

## Crystal quick actions

These live in the **spellbook**: the book button to the right of the health bar opens a bottom sheet (see [Magic](magic.md#spellbook)).

| Button | Cost | Effect |
|---|---|---|
| **Mend** | 1 Verdant crystal | Heal 50% of max health. Available whenever the hero is hurt. |
| **Hasten** | 1 Storm crystal | Halve the remaining time of the current expedition. Everything still ahead on the road (beats, road events, the return) moves proportionally closer. **Once per trip.** Only shown while the hero is away. |

These replace the old Mending Light spell. Healing no longer needs to be learned.

## Appearance

The hero in the Journey view is drawn from their gear: tunic and armor colour by armor tier, a shield from tier 1, a helmet from tier 2, the forged weapon in hand, and the pickaxe when mining rock, ore or crystal. At night they carry a small lantern glow.
