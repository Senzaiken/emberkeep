# Changelog

Newest first. Dates are US Eastern.

## 2026-09-27

- **Spellbook.** A book button next to the health bar opens a bottom sheet with Mend, Hasten and every learned spell, ready to cast. It replaces the Mend/Hasten pills under the health bar. Learning stays in the Magic tab's grimoire.
- **Errand hints.** While an errand is active, a violet ✦ marks what advances it: the Explore tab, tags with progress on the right region rows, or a pill on the castle for tap-gold errands.
- **Errand timer.** A countdown to Arthrex's next errand floats over him in the keep view, and appears in the spire section with a progress bar.
- **Tutorial polish.** The tutorial auto-completes when the first expedition returns, before Arthrex speaks. Fixed the tutorial, road-event and update cards running edge to edge on phones: all overlay cards now keep a 20px margin.
- **Guided tutorial.** A spotlight walkthrough for new games: tap the keep, open Explore, send the hero to Whisperwood, learn to tap ahead in the Journey view. The rest of the screen is shadowed and blocked, and there's a **Skip tutorial** button on every step. See [Story and Arthrex](story.md#guided-tutorial).
- **Story and Arthrex.** An opening card for new games. After the first expedition, **Arthrex, the court sorcerer**, explains crystals and gives 10 of each. He then offers errands (walk a region, slay foes, bring supplies, tap gold, find a relic) that pay in crystals and gold. His spire always stands on the east grounds: tap it to visit him. The "Wizard Tower" holding is now **Apprentice Hall**. See [Story and Arthrex](story.md).
- **Expeditions cost health.** Setting out costs health by region (10 / 15 / 22 / 30 / 45), on top of foe damage. The old "25% health to depart" rule is replaced by "more health than the trip costs".
- **Crystal quick actions.** **Mend** (1 Verdant: +50% health) and **Hasten** (1 Storm: halve the remaining trip, once per trip) are now buttons under the health bar. Mending Light is no longer a spell to learn.
- **iPhone top edge fix.** Opaque status bar for the home-screen app, a solid strip behind the top safe area, and more space above the header, so the top of the game no longer fades under the clock.
- **Update banner and cache busting.** The game checks `version.json` (uncached) and shows a "new version is ready, Reload" banner when there's a new build. There's also a **Check for updates** button in the Ascend tab. Reloads save first and use a unique URL to get past the cache. See [Saving](saving.md#updates-and-caching).
- **Expeditions reworked.** Each trip is now a timeline of beats (trees, ore rocks, crystals, foes, treasure chests) with loot arriving as it happens. There's a new **Journey** view (a side-scrolling scene per region, with the hero drawn from their gear) and a Keep/Journey switch on the canvas. Tap what lies ahead to help: extra loot, and half damage from foes. See [Expeditions](expeditions.md).
- **Road events.** Seven choice cards (Goblin Toll Bridge, A Glinting Vein, A Fallen Giant, Abandoned Camp, Wounded Traveller, Crystal Seep, Wayside Shrine). Each has a 20-second timer and a safe default if you don't choose.
- **Hero health.** Foes and some events hurt the hero. At 0 health the trip ends early, and the hero needs 25% health to depart. They heal while resting at the keep. New spell: **Mending Light**. See [Hero](hero.md).
- **Relics.** 15 relics across the five regions with passive bonuses, levelling up to 5 from duplicates, and kept through ascension. The collection book is in the Explore tab. See [Relics](relics.md).
- **Compact top bar.** Scrolling down shows a sticky bar with the icon, gold, gold/sec and gold/tap, and the day/night countdown. Tabs stick below it, and notifications moved to the top of the screen.
- **More detailed scenery.** Snow-capped mountain range behind the hills, lit hill crests, layered pines and round oaks in Whisperwood, a dirt road from the gate, grass tufts and stones. The castle now has brickwork, lit and shaded faces, conical tower roofs with pennants, arched windows with sills and a warm glow at night, and a portcullis gate. Every surface still blends between day and night colours.
- **Day and night cycle.** 10-minute cycle (5 min day, 5 min night) anchored to the real clock. The sun and moon arc across the sky, the sky blends through dawn and dusk, stars fade by day, the landscape changes colour, and the header shows a countdown. Visual only for now. See [Day and Night](day-night.md).
- **Wiki.** Added these docs under `docs/`.
- **App icon.** Castle-against-the-moon icon with an ember crystal. Favicon, Apple touch icon and web manifest.
- **Moved to GitHub Pages.** The game is now hosted at senzaiken.github.io/emberkeep and saves in the browser there. It was a Claude artifact before, where progress didn't survive closing it.
- **Crystals, expeditions and forge.** Replaced mana with elemental crystals (Ember, Frost, Verdant, Storm) from a Crystal Mine and deep expeditions. Spells are now learned individually and cost crystal reagents. Added hero expeditions for wood, stone, copper, tin and iron, and a forge with weapon, armor and pickaxe tiers.
- **First prototype.** Tap-for-gold idle game with 8 holdings, upgrades, spells, and ascension for Renown.
