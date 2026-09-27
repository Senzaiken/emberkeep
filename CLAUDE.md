# Emberkeep: notes for Claude

Medieval fantasy idle game. Uri develops it entirely from his phone, so Claude does the editing, committing and pushing.

- The whole game is `index.html` (Phaser 3 from cdnjs plus plain DOM UI). No build step.
- Pushing to `main` deploys to GitHub Pages: https://senzaiken.github.io/emberkeep/
- **Build stamping:** install the hook once per clone: `cp tools/pre-commit .git/hooks/pre-commit && chmod +x .git/hooks/pre-commit`. It writes a new `BUILD` id into `index.html` and `version.json` on every commit touching the game, which makes open copies show the "new version" banner. Don't edit `BUILD` by hand.
- **Keep the wiki current.** Every change to a mechanic, number or system updates the matching page in `docs/` and adds an entry to `docs/changelog.md` **in the same commit**. New systems get a new page, linked from `docs/README.md`.
- Don't break existing saves (`localStorage` key `emberkeep-save-v2`). New state fields need defaults in `fresh()` and a merge in `load()`. If a breaking change is unavoidable, bump the key and note it in the changelog.
- Before pushing: syntax-check the inline script, and do one quick headless render (Chromium + Phaser from `npm i phaser@3.80.1`, since the CDN is blocked in the sandbox).
- Theme: medieval fantasy only, no modern or future tech.
