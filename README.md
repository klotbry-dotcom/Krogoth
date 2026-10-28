# Krogoth

A mech-themed, grid-based mazing tower defence game in pixel art, in the spirit of Gem TD.

The whole game is one file: `index.html` (HTML, CSS and JavaScript, no libraries).

## Core loop

- Each round you place **5 random metal pieces** on the refinery floor and **keep 1**. The other 4 become **scrap**, which stays on the floor as maze walls.
- Enemies enter at the **spawn portal** (left edge, top lanes), visit **checkpoints 1–6 in order**, and head for the **Refinery** (bottom-right). Your scrap and towers decide the route; you can never fully block it.
- Layout copied from Gem TD (top-left cell of each 2×2 checkpoint): spawn (0,2) → 1 (24,2) → 2 (24,26) → 3 (56,26) → 4 (56,2) → 5 (40,2) → 6 (40,42) → Refinery (66,42). Each checkpoint has T-shaped no-build arms toward its lanes.
- The 5→6 leg crosses the 2→3 leg, so **air waves** (which fly straight from checkpoint to checkpoint) pass that crossing twice.
- **Combining:** two identical pieces (same metal, same tier) merge into the next tier. At least one of the pair has to be from the current round. The other piece becomes scrap.
- **Odds:** spend gold to raise the chance that new pieces start at a higher tier.
- **Scrap:** tap scrap to **Dispose** of it (free, any time; enemies already walking re-route). While placing your 5, tap scrap and choose **Use as piece n of 5** to turn it into one of them.
- **Kills:** every tower records its kills and gains +1% damage per 5 kills. Combining keeps both towers' kills.
- **Speed:** 1×, 2×, 3×, 5×.
- **Difficulty:** from wave 6 enemies get 4% faster each wave (up to about double speed).

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

## Combat feel

- Towers turn to aim at their target (and idly scan when nothing is in range), with recoil and muzzle flashes.
- Projectiles: Iron shells arc and explode, Cobalt fires ice shards, Uranium lobs radiation globs, Gold flings coins, Titanium fires tracers (Skyhawk fires homing missiles). Copper chains lightning and Tungsten fires beams instantly.
- Enemies are machines: Scuttler (ground), Runner (fast), Hornet drone (air) and Warlord (boss). They flash white when hit and break into debris and smoke when destroyed.

## Grid

- 70 × 46 cells (Gem TD's grid). Towers and scrap take 2 × 2 cells and can be placed on any cell.
- Enemies fit through a 1-cell gap (no squeezing diagonally between two corners).
- The field scrolls (drag) and zooms (pinch or mouse wheel).
- Drawn in a 3/4 view: towers stand on plinths, scrap is 3D blocks, everything is depth-sorted.

## Not built yet

Recipes and special mechs, saving a run, sound, more enemy types.
