---
name: js-state-engine
description: Rules for updating vanilla JS state, dynamic pricing calculators, and modal workflows in index.html.
---

# JavaScript State & DOM Management Rules

## Global State Architecture
- `configState`: Holds `{ basePackage, excursions, spaType, spaDuration }`.
- `scoreSheet`: Tracks archetype calculation (`EARTH`, `WATER`, `FIRE`, `AIR`).

## Reactive Calculation Rules
- Any change to package selection, excursion toggles, or spa dropdowns MUST invoke `recalculateBooking()`.
- Dynamic totals calculation formula: `Total = Base Package + Excursion Sum + Spa Base (+ $30 if 90min duration)`.
- Modal Triggers: Modals use standard `.classList.remove('hidden')` and `.classList.add('hidden')` animations with backdrop blur.
