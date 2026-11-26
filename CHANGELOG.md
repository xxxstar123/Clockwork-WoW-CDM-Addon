# Changelog

Recent versions of Clockwork (1.8.x).

## 1.8.33.1

Every fix below is for Retail and WoW Forever. A `/reload` is enough after updating (if you are updating from before 1.8.33, quit WoW and start it again once for 1.8.33's new glow files).

### Fixes - Frozen & collapsing rows
- **Side aura bars no longer leave an extra gap next to multi-row icons:** When a collapsing row stacked two or more icon rows that tracked both your buffs and target debuffs on different rows (for example Tidal Waves on one row and Flame Shock on the other), vertical side aura bars were pushed one extra icon-width outward in Frozen, Live and out of combat. Side bars (and Shaman totem bars beside them) now sit flush at your normal spacing.
- **Single shown icon row no longer hovers in the middle beside taller vertical bars:** When a collapsing row or its middle icon column grows from the bottom (or top) next to a two-row-tall vertical aura bar, a single active icon row now stays pinned to the bottom (or top) edge instead of floating in the middle until a second row appears.

Existing designs and settings are unchanged.

### Still in progress (next update)
- Missing-aura icons: a "missing aura" reminder icon does not hide when the buff / debuff is applied while in combat.
- Frozen: totem bars keep their space while the totem is down (the row does not close up yet; nothing overlaps).
- Live: the combo point bar width can be off in combat.

## 1.8.33

Every change below is for Retail and WoW Forever. **Full WoW restart needed after updating** (new files) - quit WoW and start it again; a /reload does not load new files, and the new glows can be missing or look wrong until you restart.

### ✨ Highlights - what's new

**🔆 Brand-new glows + a new "Flash" effect**
- **Pixel glow:** 16 short, crisp dashes marching round the icon, in a brighter shade of your glow colour.
- **Marching ants:** a thin ring with a soft halo and 4 bright streaks travelling round it together.
- **Static glow:** a bright ring with a wide soft glow fading outward and a short glow fading in over the icon edge.
- **NEW - Flash** (icon window > Active tab): the ring lights up, two light sweeps race along the edges, then it fades while sparks drift away - every 2 seconds while the state lasts. Uses your glow colour; Direction flips the sweeps.
- **Lighter than ever:** no glow runs any code per frame any more - the game animates them on its own, even in combat inside buff / debuff icons.

**📋 Layouts per spec**
- Your layout lists show only the layouts of the spec you are playing - a Guardian druid sees Guard, a Feral druid sees CAT. No more scrolling past every spec's layouts.
- Presets stay shared by all layouts. Nothing is deleted or renamed; a layout you named yourself that belongs to no spec shows everywhere, so nothing disappears. On WoW Forever (one spec per class) the list shows your class's layouts.

**📤 Profiles - share your layouts as text**
- `/cwk` > Profiles: tick one layout or all of them and **Export**; paste a text and **Import**. The text holds each layout and every preset it uses, so it looks the same on another PC - WoW Forever and Retail read each other's texts.
- Same name? You choose: Overwrite or Import as copy ("Name (2)"). Your own presets never change. "Use for my current spec" makes the imported layout this spec's design. Design mode: the group menu has "Export this layout".

**🎨 Masque support**
- With Masque loaded: Behavior tab > Icons > **"Skin icons with Masque"** (off by default). One Masque group per preset, so each preset can wear its own skin. Clockwork keeps your size, glows, texts, states and swipe colour in place. Turning it off brings Clockwork's look back at once.

**🔗 Smarter buff / debuff icons (linked auras)**
- Spells whose aura has another id now show the aura worth tracking, from the game's own data - WoW Forever **Pounce shows Pounce Bleed (18 s)**, not the 2 s stun; Retail e.g. Corruption, Outbreak, Rake. The element window tells you what the icon shows. Want the other aura? Type its id in the Spell ID box.

**👓 Easier to read**
- Grey hint text in Clockwork's windows is much brighter: descriptions, notes, search boxes, greyed-out menu entries and the Spell ID / Item ID tooltip line.

### More improvements
- Coolinator import: "Flash" and "Marching ants" now come in as Clockwork's own Flash and Marching ants (before, both came in as Blizzard glow).
- Your glow numbers are kept; presets that still had the old default glow numbers switch to the new look by themselves (once), also in texts imported from an older Clockwork. Gap (Marching ants) now goes up to 48, Softness (Static glow) up to 16.
- Bar window: "Keep its place while hidden" is grayed out while In combat is Frozen (Frozen already keeps the place); your setting comes back when you pick Live.
- Aura pips / stack timers: at most 10 show in combat (Blizzard's aura buttons); the setting and a chat line tell you.
- New layouts and copies are numbered the same way: Name (2), Name (3).
- Masque: renaming or deleting a preset removes its old Masque group at once.
- Selecting several items: time color steps, color thresholds and the power bar Quick setup now apply to all of them.
- Design mode: the collapse warning badge sits outside the group box, so it no longer covers icons.
- Lighter: key presses no longer create tables on every press.
- Chat lines start with a gold "Clockwork:"; "Behaviour" tab is now "Behavior" (American spelling everywhere); "Bevelled" border is "Beveled".
- If the game refuses to create Blizzard's aura slots, Clockwork says so once in chat; a failing bar is reported once to BugSack.

### Fixes
- Totems (from 1.8.32.2, never released on its own): Frozen totem bars like Spirit Link Totem no longer overlap the icons next to them; a totem bar like Healing Tide Totem shows right after the cast, even when the game fills the slot a moment later.
- WoW Forever: a Pounce icon set to On: Auto showed nothing - Auto now knows Target for such spells.
- A proc glow turned on through a spell override (talent or proc) could stay off; Clockwork now also follows the Cooldown Manager's override changes (proc glow, key press look, keybind text, aura links).
- Switching the proc glow color between gold and pure white kept Blizzard's gold art.
- The ranged swing bar shows on Retail.
- Deleting a design with "%" in its name works.
- Coolinator: a failed reset changes nothing, and an icon the import can't read is skipped on its own instead of its whole layout.

Existing designs and settings are unchanged (apart from the glow look above).

### Still in progress (next update)
- Frozen: totem bars keep their space while the totem is down (the row does not close up yet; nothing overlaps).
- Live: the combo point bar width can be off in combat.

## 1.8.32.1

This update also includes 1.8.32 (never released on its own). Every fix below is for Retail and WoW Forever unless it says otherwise. A /reload is enough after updating.

### New
- Totems: aura bars and icons for spells that summon a totem now show while the totem is up, with its own timer. Shaman totems (Healing Tide, Spirit Link, Healing Stream and every other totem), and the other spells that use totem slots (Paladin Consecration, Warlock demons, Priest Shadowfiend, Monk invokes). Before, these never showed, because a totem puts no buff on you.

### Fixed - Auto width bars
- Auto width bars follow their row again, like in 1.8.31: they change size with your forms, in and out of combat, with Collapse in combat set to Live or Frozen. (Before, a bar kept the width of the form you pulled in for the whole fight.)
- Bars that hide when idle (swing timer) or show only in one form (combo points, cat energy) no longer take a wrong or old width.
- Fixed bars becoming about 3 times too wide after opening design mode while their group was hidden.
- Frozen: an Auto width power bar no longer shrinks to a tiny size at the pull.
- Cast bars keep their width in combat by default, so they never shrink to a side bar's width.
- The bar's "In combat" choice (General tab) is still there: "Follow the row" (new default) or "Keep its width" (default for cast bars). If you picked "Keep its width" on a bar in 1.8.28 to 1.8.32, please pick it again - those versions did not save that choice.

### Fixed - Totems
- Totems in slot 5 and 6 now show (when 4 totems were already up).
- The Healing Rain bar shows the Healing Rain buff, not the Surging Totem timer, and no longer shows twice (Frozen).
- Live: totem bars get their own place and no longer sit on top of the next bar.
- A totem you cast for the first time in a fight is recognised more often.

### Fixed - Charge bars
- The recharge now fills and counts down in combat too, also in Mythic+ keys and boss fights (it stayed empty there).
- In combat the recharge no longer flashes on the left (ready) segment before jumping to the right one: the game places it on the recharging segment.

### Fixed - /reload in combat, keys and raids
- After a /reload in a Mythic+ key, a boss fight or a raid: the second row of icons no longer sits on top of the first one.
- After a /reload in combat in a key: vertical aura bars, pip bars and stack-timer bars show again (they stayed hidden until the key ended).
- WoW Forever: after a /reload in combat, the layout catches up again.

### Fixed - Layout
- Frozen: a bar hidden at the pull (e.g. Enrage) no longer overlaps the icons when it shows up - its place opens at the pull.
- Frozen: Restoration Shaman's aura rows no longer float above the cast bar in combat.
- A vertical bar placed directly in a scaled row is now as tall as the other side bars.
- Glows: Blizzard's proc glow no longer covers an icon's cooldown swipe or its stack number.

### Still in progress (next update)
- Shaman, Live: Healing Tide Totem can be missed when the game reports the totem a moment after the cast (about 0.1 s).
- Shaman, Frozen: side totem bars (Healing Tide, Spirit Link) can still move or overlap when a totem drops mid-fight.
- Live: a combo point bar inside a collapsing row can't follow the row's width in combat (Frozen is fine) - the game hides that width from addons in combat.

Existing designs and settings are unchanged.

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
