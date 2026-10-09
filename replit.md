# Fantasy Realm

A browser-based fantasy RPG where players create a hero, explore quests, fight monsters, earn rewards, and save progress in the browser.

## Run & Operate

- `pnpm --filter @workspace/fantasy-realm run typecheck` — check the game app
- The `artifacts/fantasy-realm: web` workflow starts the browser game.

## Stack

- pnpm workspace, React, Vite, and TypeScript
- Browser local storage for saved single-player progress

## Where things live

- `artifacts/fantasy-realm/src/game/` — game types, rules, browser save adapter, and state hook
- `artifacts/fantasy-realm/src/App.tsx` — RPG screens and navigation
- `artifacts/fantasy-realm/src/index.css` — visual system and responsive styles

## Architecture decisions

- Game rules are separated from the React UI; keep future combat and quest logic out of page components.
- Browser saving is behind a `GameSaveStore` interface. A future online version will need server-authoritative actions and shared persistence rather than trusting browser state.

## Product

Fantasy Realm is a single-player first version with character customization, health/mana/XP/levels, coins and inventory, turn-based monster battles, quest rewards, a local leaderboard, and browser-saved progress.

## User preferences

The user wants the code organized so multiplayer features can be added later.

## Gotchas

_Populate as you build — sharp edges, "always run X before Y" rules._

## Pointers

- See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details
