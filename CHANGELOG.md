# Changelog

Recent versions of Clockwork (1.8.x).

## 1.8.29
- Cleaner addon folder: Core, UI, Display, Tracking, Designer and Media.
- The three largest files are split into smaller ones by job.
- No change in behaviour. Restart WoW fully after updating (files moved).

## 1.8.28.1
- New icon presets hide the GCD swipe by default; existing presets keep their setting.

## 1.8.28
- `/cwk tour`: shows every window and tab by itself, 4 s each.
- Auto-width bars: per bar *In combat: keep its width* (default) or *follow the row*.
- GCD swipe is now a per-preset look setting (Show / Hide).
- Aura icons remember which unit an aura was seen on across sessions.
- Blizzard proc glow never flashes the whole animation sheet on the first proc.
- Design mode: a selected group's controls sit outside its children, never over them; the design menu works with secret geometry.

## 1.8.27
- Collapse warnings: clearer causes, a one-click Fix where a size fix helps, "move it out" for a non-aura icon in the middle, one warning per row.
- Design mode stays clickable after leaving and re-entering in all cases.

## 1.8.26 / 1.8.25
- Safer handling of secret values and secret geometry in combat.
- Readable bars (cast bar, stack timers counted from casts) take and give back their place in combat.
- Two-unit rows (your buffs + the target's debuffs) collapse in Frozen mode too.
- In combat collapse defaults to Frozen; Live stays available as an option.
- `/cwk debug` dumps the live layout engine for bug reports.

## 1.8.24 / 1.8.23
- **Live collapse in combat**: setting *In combat: Live / Frozen*.
- Cast bar Show / Hide rules; *Keep its place while hidden* also covers rule-hidden.
- Window polish: hints never cover labels, tabs as wide as their text.

## 1.8.19 – 1.8.20
- **Tidy wrappers** (`/cwk tidy` and a design-mode button): removes one-item wrapper groups only where nothing on screen moves. One undo step.

## 1.8.11 – 1.8.12
- Cast bar latency is a regular bar text.
- Aura bars read through the shared aura cache (fewer calls per refresh).
- Code clean-up and dead-code removal.

## 1.8.10
- **Single-Button Assistant icon** (Retail): shows Blizzard's current suggestion with its keybind.

## 1.8.6 – 1.8.9
- Hidden = no place: anything hidden takes no space in its row or column.
- Design mode: faster, Alt+drag = free move, Snap box and Grid W / H in the toolbar.
- Aura lookup caching.

## 1.8.4 – 1.8.5
- Spells you haven't learned are hidden in play and drawn grey in design mode.

## 1.8.0 – 1.8.3
- Major lightweight pass: about 76 % fewer objects, 70 % less garbage, zero idle per-frame updates.
- `/cwk debug` collapse report names the failing row, icon and check.
