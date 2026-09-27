# Overview

## Concept

Emberkeep is an incremental (idle) game set in a medieval world where magic is real but scarce. You rule a keep on a hill. Gold flows from your holdings, but real power comes from what your hero brings back from the wilds and from the elemental crystals mined beneath the realm.

Tone: medieval fantasy, low-tech. No modern or futuristic technology.

## Core loop

1. **Tap the keep** for gold. Build **holdings** that produce gold on their own.
2. Send your **hero on expeditions** for wood, stone, copper, tin and iron. Watch the journey, tap to help, make choices at road events, and find relics. Foes wear down the hero's health, which has to recover between trips.
3. **Forge** better equipment from those materials. Better gear means stronger taps, safer and faster expeditions, and better mining.
4. Dig the **Crystal Mine** for Ember, Frost, Verdant and Storm crystals.
5. **Learn spells** one at a time, then cast them using crystals as reagents.
6. **Ascend** to found a new dynasty, trading your reign's progress for permanent Renown.

The systems feed each other. Expeditions need armor, armor needs ore, ore needs expeditions and a good pickaxe, and spells need crystals from the mine, which is dug with gold, stone and ore.

## Stack

| Layer | Choice | Notes |
|---|---|---|
| Engine | Phaser 3.80.1 | Loaded from cdnjs. Draws the realm scene (the canvas). |
| UI | Plain HTML/CSS/JS | Panels, tabs and buttons are DOM, not canvas. |
| Code layout | Single `index.html` | Data tables, economy, UI and the Phaser scene, in that order. |
| Hosting | GitHub Pages | `main` branch, root folder. Pushing to `main` deploys in about a minute. |
| Native (planned) | Capacitor | Wrap the same web build for iOS/TestFlight. See [Roadmap](roadmap.md). |

Fonts: *IM Fell English SC* (display) and *Alegreya Sans* (body), from Google Fonts.

## How we work

Development happens from a phone. Uri describes a change, Claude edits the code, updates these docs and the [Changelog](changelog.md), then commits and pushes. GitHub Pages redeploys, and the change shows up on the home-screen app.

## Code map (`index.html`)

| Section marker | Contents |
|---|---|
| `DATA` | Buildings, upgrades, gear, expedition regions, mine depths, spells |
| `STATE` | Save shape (`fresh()`), load and save |
| `ECONOMY` | Formulas and every player action (buy, forge, depart, dig, learn, cast, ascend), hero health, relics, the expedition timeline and road events |
| `FORMAT` | Number and time formatting |
| `UI` | DOM rows, `refresh()`, tabs, toasts |
| `PHASER REALM` | Day/night cycle, the `Realm` scene (the keep), scenery drawing |
| `JOURNEY` | The `Journey` scene: side-scrolling expedition view, hero sprite, beats, tap to help |
| `BOOT` | Start-up, game loop timers |
