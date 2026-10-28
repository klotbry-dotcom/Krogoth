# Krogoth

A mech-themed, grid-based mazing tower defence game in pixel art, in the spirit of Gem TD.

The whole game is one file: `index.html` (HTML, CSS and JavaScript, no libraries).

## Core loop

- Each round you place **5 random metal pieces** on the refinery floor and **keep 1**. The other 4 become **scrap**, which stays on the floor as maze walls.
- Enemies enter at the **spawn portal**, visit **checkpoints 1–5 in order**, and head for the **Refinery**. Your scrap and towers decide the route; you can never fully block it.
- **Air waves** ignore the maze and fly straight from checkpoint to checkpoint.
- **Combining:** two identical pieces (same metal, same tier) merge into the next tier. At least one of the pair has to be from the current round. The other piece becomes scrap.
- **Odds:** spend gold to raise the chance that new pieces start at a higher tier.

## Metals

| Metal | Role |
|---|---|
| Iron | Splash damage |
| Copper | Chain lightning |
| Cobalt | Slows enemies |
| Uranium | Spreading radiation |
| Tungsten | Armour-piercing hits |
| Gold | Bonus gold, boosts nearby towers |
| Titanium | Rapid fire, strong against air |

## Tiers

Ore → Ingot → Rod (or Wire) → Bolt → Core → Mech (2 Cores of the same metal).

Flavour names: Gold Nugget, Copper Wire and Coil, Gold Wire, Uranium Fuel Rod and Reactor Core, Tungsten Filament, Cobalt Cryo Core.

Mechs: Iron Juggernaut, Copper Stormcaller, Cobalt Frostwalker, Uranium Meltdown, Tungsten Railbreaker, Gold Midas, Titanium Skyhawk.

## Grid

- 40 × 40 fine cells. Towers and scrap take 2 × 2 cells and can be placed on any cell.
- Enemies need a 2-cell-wide gap to pass.
- The field scrolls (drag) and zooms (pinch or mouse wheel).

## Not built yet

Recipes and special mechs, removing scrap for gold, saving a run, sound, more enemy types.
