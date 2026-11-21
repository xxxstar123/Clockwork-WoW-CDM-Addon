# Changelog

Recent versions of Clockwork (1.8.x).

## 1.8.31
- New: item buffs. An aura icon can now show the buff an item gives you: a trinket's on-use buff, a trinket proc (Equip effect) or a potion. Retail and WoW Forever.
- In the buff picker, "Item buffs" comes first: Trinket 1 / Trinket 2 (follows the slot, also after a gear swap) or an exact item (your trinkets, potions in your bags).
- It works like every aura icon: hidden while the buff is not on you (takes no place unless "Keep its place while hidden"), shown in combat, works in collapsing rows, with Show / Hide rules, glows and sounds.
- Clockwork finds the buff from the game's own data, the item's use spell and its tooltip. For the few procs the data can't link, it learns the buff out of combat the first time it sees it. The new "Item" tab shows the buff IDs and where each came from; "Forget learned ids" (or `/cwk itemauras forget <itemID>`) clears one item, `/cwk itemauras reset` clears all.
- Lighter in combat: proc glow, glow lines, timer text, the key press look and the rotation highlight are now made before the fight, not on their first show in combat.
- Lighter glow animation: the traveling glow / marching ants redraw at most about 60 times a second and only move pieces that moved. Same look and speed.
- Faster proc glow checks.
- Errors now show in BugSack (or the game's error window): if an icon or bar fails to update, Clockwork reports it once instead of failing silently.
- Fixed: an error when a bar leaves a collapsing row that stays a collapsing row (e.g. a bar dragged out of a side-bar group).
- Existing designs and settings are unchanged. Restart WoW fully after updating (new files) – a /reload is not enough.

## 1.8.30.2
- Collapse in combat (Live): a row of aura icons no longer slides to the side when it holds an aura you haven't learned or an ability Clockwork hides itself (seen on Guardian with Ravage not learned).
- The same fix for a row holding a group that a Show / Hide rule or a form hides in combat, and for a whole row hidden by its own rule (the next row no longer sits a row too high).
- Rows with bars on the left and right of a middle of icons: the side bars no longer get pushed outwards when an aura is up behind one that is down. At most a one-frame flicker remains when an aura changes.
- Works for every class and spec, Retail and WoW Forever. Nothing changes out of combat, no settings changed. A /reload is enough after updating.

## 1.8.30.1
- Design mode: the move handle now sits in the center of the selected group, icon or bar. Every other control stays where it was.
- Design mode: hovering any group, icon or bar shows a soft gold outline; the selected one keeps the full gold outline, with a thin dark line around it so it reads on bright backgrounds.
- New `/cwk livetint` (debug): see-through colors on the boxes the in-combat collapse uses, for a screenshot when you report a layout problem.
- `/cwk debug` now also saves the in-combat collapse state. A /reload is enough after updating.

## 1.8.30
- Starter layouts: new players get a "Choose a starter layout" window with a ready-made layout for their class and spec (Compact, Wide, Healer).
- Every Retail spec and every WoW Forever class covered; spell IDs checked against the game data.
- `/cwk starter` adds a starter layout any time, without deleting anything.
- Existing designs and imported profiles are never touched; never shown in combat.

## 1.8.29
- Cleaner addon folder: Core, UI, Display, Tracking, Designer and Media.
- The three largest files are split into smaller ones by job.
- No change in behavior. Restart WoW fully after updating (files moved).

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
- Spells you haven't learned are hidden in play and drawn gray in design mode.

## 1.8.0 – 1.8.3
- Major lightweight pass: about 76 % fewer objects, 70 % less garbage, zero idle per-frame updates.
- `/cwk debug` collapse report names the failing row, icon and check.
