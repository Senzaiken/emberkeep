# Hero

The hero is the one who leaves the keep: expeditions, road events and fights. Their gear comes from the [Forge](forge.md), and their health limits how often they can set out.

## Health

| | |
|---|---|
| Max health | 100 + 25 × armor tier (+ relic bonuses, +25 with Skarholm claimed) |
| Setting out | every expedition **costs health** up front: Whisperwood 10, Greystone Quarry 15, Copperfen Hills 22, Ironroot Deep 30, Shattered Caldera 45. The hero needs more health than the cost to depart. |
| Resting at the keep | heals from empty to full in 4 minutes (8 while **wounded**), only while not on an expedition, including while the game is closed |

Health is shown in the header, and as a small bar over the hero in the Journey view.

### Taking damage

- **Setting out**: the region's travel cost, paid when the hero departs.

- **Foes**: each foe on the road hits once when the hero reaches it, for the region's damage × (1 + 0.15 × (depth − 1)) × `max(0.35, 1 − 0.12 × armor tier − 0.06 × weapon tier)`. Tapping the foe first halves the hit. Foes also wait on the road home (see [Expeditions](expeditions.md#the-road-home)).
- **At sea**: leading a boarding party costs 8 + 6 × the ship's tier, and storming a castle costs a share of max health (see [The Sea](sea.md#sieges)).
- **Road events**: losing the fight at the Goblin Toll Bridge costs 20% of max health, and an ambush at the Abandoned Camp costs 15%.

The Explore tab shows the approximate damage per hit at depth 1 for each region with your current gear. The journey bar shows it for the current depth.

### Defeat

If health reaches 0 on the road, the hero is beaten back. The trip ends at once: **half the carried haul** and every unused draught are lost (relics already found are kept). The hero comes home **wounded** and rests at half speed until back to full health. Mending with Verdant still works as usual. The hero must be above the next trip's cost before leaving again.

Two things stop this happening: the **turn-back point** and packed **Verdant draughts**, both set in the Explore tab (see [Expeditions](expeditions.md#preparations)).

### Healing

| Source | Amount |
|---|---|
| Resting at the keep | Full in 4 minutes |
| **Mend** (spellbook, 1 Verdant crystal) | 50% of max health, usable anytime, including on the road |
| **Verdant draught** (packed before departing, up to 2 + armor tier) | 50% of max health, drunk automatically below 40% health on the road |
| Wayside Shrine event, "Kneel and rest" | 30% of max health (+10s to the trip) |

Health is the brake on endless exploring: trips cost health, foes grow harder the deeper the hero goes, resting takes time, and crystals let you skip the wait or go deeper. It's also the planned hook for a premium item later, such as an instant full heal (see [Roadmap](roadmap.md)).

## Crystal quick actions

**Mend** lives in the **spellbook** (the book button to the right of the health bar). **Hasten** is on the **journey bar** under the Journey view, once the hero is walking home.

| Button | Cost | Effect |
|---|---|---|
| **Mend** | 1 Verdant crystal | Heal 50% of max health. Available whenever the hero is hurt. |
| **Hasten** | 1 Storm crystal | Halve the rest of the walk home (the foes on it move closer to match). **Once per trip.** Shown in place of Return home while the hero is heading back. |

These replace the old Mending Light spell. Healing no longer needs to be learned.

## Appearance

The hero in the Journey view is drawn from their gear (and turns round for the walk home): tunic and armor colour by armor tier, a shield from tier 1, a helmet from tier 2, the forged weapon in hand, and the pickaxe when mining rock, ore or crystal. At night they carry a small lantern glow.
