# Day and Night

The realm runs on a **10-minute cycle: 5 minutes of day, then 5 minutes of night**.

## How it works

- The cycle is anchored to the real clock (`Date.now() % 10 minutes`), not to when the game was opened. Everyone sees the same time of day, and closing the game doesn't pause or reset it.
- The sun crosses the sky in an arc during the day, and the moon follows the same arc at night.
- The first and last 10% of the day are twilight. The sky and land blend between night and day colours, and the horizon glows orange at dawn and dusk.
- Stars fade out during the day, and lit castle windows glow softly at night.
- The mountains, hills, trees, road, castle and buildings are drawn with a night colour and a day colour for each surface, blended by the current light level.
- The pinned top bar always shows it on the right: a sun or moon icon, "Day" or "Night", and a countdown to dusk or dawn.
- The Journey view follows the same cycle (sky, sun, moon, stars and land colours). Ironroot Deep is a cave and stays torch-lit.

Code: `dayInfo()` returns `{day, u, light, warm, left}`, where `u` is progress through the current half (0–1), `light` is daylight 0–1, and `warm` is twilight glow 0–1.

## Gameplay effects

**None yet.** The cycle is visual only for now. See the ideas in [Roadmap](roadmap.md#day-and-night-ideas).
