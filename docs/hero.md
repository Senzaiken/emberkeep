# Hero

The hero is the one who leaves the keep: expeditions, road events and fights. Their gear comes from the [Forge](forge.md), and their health limits how often they can set out.

## Health

| | |
|---|---|
| Max health | 100 + 25 × armor tier (+ relic bonuses) |
| Needed to depart | at least 25% of max health |
| Resting at the keep | heals from empty to full in 4 minutes (only while not on an expedition, including while the game is closed) |

Health is shown in the header, and as a small bar over the hero in the Journey view.

### Taking damage

- **Foes**: each foe on the road hits once when the hero reaches it, for the region's damage × `max(0.35, 1 − 0.12 × armor tier − 0.06 × weapon tier)`. Tapping the foe first halves the hit.
- **Road events**: losing the fight at the Goblin Toll Bridge costs 20% of max health, and an ambush at the Abandoned Camp costs 15%.

The Explore tab shows the approximate damage per hit for each region with your current gear.

### Defeat

If health reaches 0 mid-trip, the hero is beaten back. The trip ends immediately, everything already gathered is kept, and there's no relic roll. The hero must rest (or be healed) back to 25% before leaving again.

### Healing

| Source | Amount |
|---|---|
| Resting at the keep | Full in 4 minutes |
| **Mending Light** (spell, 1 Verdant per cast) | 50% of max health, usable on the road too |
| Wayside Shrine event, "Kneel and rest" | 30% of max health (+10s to the trip) |

Health is the brake on endless exploring. It's also the planned hook for a premium item later, such as an instant full heal (see [Roadmap](roadmap.md)).

## Appearance

The hero in the Journey view is drawn from their gear: tunic and armor colour by armor tier, a shield from tier 1, a helmet from tier 2, the forged weapon in hand, and the pickaxe when mining rock, ore or crystal. At night they carry a small lantern glow.
