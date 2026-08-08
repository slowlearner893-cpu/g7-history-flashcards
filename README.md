# Grade 7 East Asian History — Flashcards

A single-file web app. Everything (all study modes, all cards, styling, and logic)
lives inside `index.html`. There is no build step and there are no dependencies.

## What's in it
- **Flip Cards** — term ⇄ definition, tap to flip (toggle for which side shows first)
- **Type the Term** — see a definition, type the term (lenient on spelling)
- **2-Player Game** — turn-based, self-scored, first to a target score wins.
  Quiz style can be: definition → term, term → definition (flip style), or a mix.
- **Unit picker** and **shuffle** throughout.

## Deploying (Vercel + GitHub)
1. Create a GitHub repo (e.g. `g7-history-flashcards`).
2. Put `index.html` at the **root** of the repo. (Drag-and-drop upload on github.com works.)
3. In Vercel: **Add New → Project → Import** the repo → **Deploy**.
   Framework preset: **Other**. Nothing else to configure.
4. You get a live URL. Vercel auto-redeploys on every push to the repo.

## Adding a new unit (the repeatable loop)
The code never changes to add a unit — a unit is just data.
1. Tell Claude "add Unit N" and paste that unit's **objective vocabulary** (the
   underlined terms from the unit objectives).
2. Claude pulls the unit's worksheet vocabulary + definitions from Drive,
   drafts definitions for any proper nouns, and adds the unit to the deck.
3. Claude returns an updated `index.html`.
4. Replace `index.html` in the repo and commit. Vercel redeploys in ~30 seconds.
   The new unit appears in the dropdown automatically.

## Notes
- Definitions for worksheet terms come verbatim from your answer keys.
- Definitions for objective-only proper nouns (e.g. Pan Gu, Erlitou) are drafts
  written at grade-7 level — review and tweak any you want to change.
