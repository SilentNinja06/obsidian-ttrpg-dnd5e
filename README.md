# TTRPG Campaign Manager — D&D 5e System Pack

System pack for the [TTRPG Campaign Manager](https://github.com/SilentNinja06/obsidian-ttrpg-core) Obsidian plugin, adding full D&D 5th Edition support.

## What this pack adds

- Six ability scores: STR, DEX, CON, INT, WIS, CHA with automatic modifier calculation
- HP tracking via `hp-current` and `hp-max` frontmatter fields
- Character fields: class, level, race, alignment, AC, speed, proficiency bonus
- d20-based initiative ordered highest-first
- Five currency types: PP, GP, EP, SP, CP
- Arc fields: motivation, secret, current goal, arc stage
- NPC fields: role, faction, agenda, wants from party

## Installation

1. Install the [TTRPG Campaign Manager core plugin](https://github.com/SilentNinja06/obsidian-ttrpg-core)
2. Download `dnd5e.yaml` from the [Releases](../../releases) page
3. Copy it into your vault's `ttrpg/systems/` folder
4. In Obsidian, open Settings → TTRPG Campaign Manager → click "Reload systems"

## Dataview queries

Once installed, you can query your D&D characters across campaigns:

```dataview
TABLE hp-current, hp-max, class, level
FROM "ttrpg/campaigns"
WHERE ttrpg-type = "character" AND system = "dnd5e"
SORT level DESC
```

Find all active loose threads:

```dataview
LIST
FROM "ttrpg/campaigns"
WHERE ttrpg-type = "session" AND system = "dnd5e"
```

## License

MIT
