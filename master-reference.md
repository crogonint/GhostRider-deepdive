---
title: "Master Reference"
aliases: ["Master Reference", "Session Notes", "Build Reference"]
tags: [pf1e, ghost-rider, marvel-rpg, session-notes, research]
system: Pathfinder 1E
---

# Ghost Rider PF1E Build — Master Research & Session State

*Complete session memory document. All decisions, canon facts, design choices, and outstanding items from the build session.*

---

## OUTPUT FILES (all at /mnt/user-data/outputs/)

### Primary Character Documents
| File | Contents | Status |
|------|----------|--------|
| `ghost-rider-johnny-blaze.md` | Combined Johnny/GR stat block, final v3 | ✓ Final |
| `zarathos-spirit-of-vengeance.md` | Zarathos stat block, final v3 | ✓ Final |
| `the-hellcycle.md` | Vehicle stat block | ✓ Final |
| `the-sword-of-uri-el.md` | Major artifact with Zarathos resonance | ✓ Final |
| `canon-reference.md` | Clean canon lore (replaced Deep Dive) | ✓ Final |
| `dm-and-player-guide.md` | Play/mechanics guide | ✓ Final |

### Design Reference Documents
| File | Contents |
|------|----------|
| `image-gallery.md` | All campaign images with file reference table |
| `the-hellfire-chain.md` | Chain artifact stat block |
| `the-hellfire-shotgun.md` | Dual stat blocks (Johnny/GR forms) |
| `existential-dread-mechanic.md` | Soul Awareness tier system |
| `penance-stare-design-reference.md` | Full damage scaling analysis (8 packages) |
| `stat-block-audit.md` | 26-item audit log |
| `final-stat-blocks.md` | Consolidated stat blocks (all three forms) |
| `corrected-stat-blocks.md` | Post-audit corrected stat blocks |
| `canon-deep-dive.md` | Extended canon analysis and design notes |
| `johnny-blaze-complete-character-document.md` | Full Johnny Blaze character document |
| `master-reference.md` | This file — session state and quick reference |
| `full-research-and-session-notes.md` | Complete research notes and session log |

### Foundry VTT
| File | Contents |
|------|----------|
| `johnny_blaze_foundry_v3.json` | CURRENT working PC sheet (v3, use this one) |
| `ghost_rider_foundry_v1.json` | CURRENT Ghost Rider NPC sheet (v1) |
| `zarathos_foundry_v1.json` | CURRENT Zarathos NPC sheet (v1, Large Outsider) |
| `johnny_blaze_foundry_v2.json` | Deprecated |
| `johnny_blaze_foundry.json` | Deprecated |

---

## INHERITANCE CHAIN

```
Johnny Blaze (CR 6, Expert 7, Human)
    ↓ transforms into
Ghost Rider (CR 19, 18 HD, Medium Outsider)  — inherits ALL Blaze feats + qualities
    ↓ surges into
Zarathos (CR 26, 26 HD, Large Outsider)  — inherits ALL GR + Blaze feats + qualities
                                             EXCEPT chain weapon feats (natural attacks instead)
```

---

## FINAL CORRECTED STATS

### Johnny Blaze (CR 6)
| Stat | Value |
|------|-------|
| HD | 7d8 |
| HP | 42 (7d8+7; includes Toughness +7) |
| AC | 12 (touch 12, FF 10) |
| Fort/Ref/Will | +3 / +4 / +8 (+10 vs supernatural fear) |
| BAB/CMB/CMD | +5 / +6 / 18 |
| STR/DEX/CON | 13 / 14 / 13 |
| INT/WIS/CHA | 13 / 11 / 16 |
| Init | +2 |
| Height/Weight | 5'10" / 180 lbs |
| Age | ~28 (Marvel sliding timescale; late 20s canonical) |
| Alignment | CN |

**Saves breakdown:**
- Fort: base +2 + CON +1 = +3
- Ref: base +2 + DEX +2 = +4
- Will: base +5 + Iron Will +2 + Indomitable Faith +1 = +8; +10 vs supernatural fear (Nerves of Steel)
- NOTE: Foundry will calculate Will +8 correctly. Earlier v1/v2 JSON had WIS 16 (wrong) — FIXED in v3.

**Johnny's Feats (7):**
1. Diehard
2. Endurance
3. Exotic Weapon Proficiency (firearms)
4. Indomitable Faith (+1 Will, trait)
5. Iron Will (+2 Will)
6. Nerves of Steel (+2 Will vs supernatural fear)
7. Toughness (+7 HP)

**Johnny's Skills:**
| Skill | Ranks | Total | Notes |
|-------|-------|-------|-------|
| Acrobatics | 7 | +12 | |
| Bluff | 5 | +11 | +15 urban/road (Street Smarts) |
| Craft (mechanical/motorcycle) | 7 | +11 | |
| Intimidate | 7 | +13 | Intimidating Prowess (STR +1 + CHA +3) |
| Knowledge (arcana) | 7 | +11 | +15 vs demons |
| Knowledge (local) | 7 | +11 | |
| Knowledge (planes) | 7 | +11 | +15 vs demons |
| Knowledge (religion) | 7 | +11 | +15 vs demons |
| Perception | 7 | +10 | +14 urban/road |
| Profession (stunt rider) | 7 | +10 | |
| Ride | 7 | +12 | +16 with Nine World Records buff |
| Sense Motive | 7 | +10 | +14 urban/road; +18 with Contract Immunity |

**Johnny's Special Qualities:**
- Burning Judgment Eyes (Su) — constant true seeing, detect evil, sin sight, aura sight; cannot be suppressed
- Nine World Records (Ex) — +4 Ride; reroll once/scene; +2 engine vehicles without proficiency
- Street Smarts (Ex) — +4 Bluff/Perception/Sense Motive urban/road; never lost on land
- Occult Scholar (Ex) — +4 Knowledge (arcana/religion/planes) vs demons/contracts/hellfire
- Hellfire Spark (Su) — free action lighter-sized empyreal flame; orange-black; no damage; no transformation needed
- Hellfire Stigma (Su) — 10 ft. radius; evil creatures DC 16 Will or shaken 1 round; soul-based not mind-affecting
- Infernal Contract Immunity (Ex/Su) — +8 insight to Will saves and Sense Motive; −10 penalty on social checks against him when goal conflicts with his values; HARD RULE: impossible to manipulate him into altering his contract, harming innocents, or changing his nature — no roll made, period
- Bound Soul — transformation mechanics (see file)
- Unbreakable Bond — cannot harm genuinely innocent; loved-one's name DC 22 Will

---

### Ghost Rider (CR 19)
| Stat | Value |
|------|-------|
| HD | 18d10 |
| HP | 319 (18d10+198+18; Toughness inherited) |
| AC | 32 (touch 20, FF 28) — +4 Dex, +12 natural, +6 deflection |
| Fort/Ref/Will | +24 / +17 / +20 |
| SR | 30; Channel Resistance +4 |
| DR | 10/cold iron and good |
| BAB/CMB/CMD | +18 / +32 (+36 grapple, +36 disarm) / 47 |
| STR/DEX/CON | 39 / 18 / 32 |
| INT/WIS/CHA | 13 / 22 / 24 |
| Speed | 40 ft. foot; 120 ft. tactical Hellcycle |
| Intimidate | +42 |
| Penance Stare DC | 40 |
| Existential Dread DC | 30 |

**Key corrections from original:**
- WIS: 17→22
- Touch AC: 14→20 (deflection applies to touch in PF1E)
- HP: 294→319 (Toughness inherited, avg recalc)
- Will: +16→+20 (Iron Will + Indomitable Faith documented)
- Ref: +16→+17 (Lightning Reflexes documented)

**Ghost Rider Feats (25):**
Cleave, Combat Reflexes, Cornugon Smash, Diehard*, Dodge, Dreadful Carnage, Endurance*, Furious Focus, Great Cleave, Great Fortitude, Imperious Command, Improved Bull Rush, Improved Critical (spiked chain), Improved Disarm, Improved Grapple, Indomitable Faith*, Intimidating Prowess, Iron Will, Lightning Reflexes, Lunge, Power Attack, Shatter Defenses, Toughness*, Weapon Focus (spiked chain), Weapon Specialization (spiked chain)
(*inherited from Blaze)

**Hellfire chain proficiency is INHERENT to GR's divine office — no feat required.**

---

### Zarathos (CR 26)
| Stat | Value |
|------|-------|
| HD | 26d10 |
| HP | 537 (26d10+364+26; CON 38 confirmed) |
| AC | 40 (touch 32, FF 35) — +5 Dex, +8 natural, +12 deflection, +6 profane, −1 size |
| Fort/Ref/Will | +31 / +22 / +25 |
| SR | 37; Channel Resistance +6 |
| DR | 15/cold iron and good |
| BAB/CMB/CMD | +26 / +44 / 60 |
| STR/DEX/CON | 48 / 21 / 38 |
| INT/WIS/CHA | 22 / 24 / 34 |
| Intimidate | +60 |
| Penance Stare DC | 40 |
| Existential Dread DC | 35 |

**Key corrections:**
- CON: 36→38 (HP and soul rend DC both independently confirmed)
- Touch AC: 18→32 (deflection + profane both apply)
- HD: 25→26 (bumped for consistency)
- HP: 487→537 (CON 38 + Toughness + HD bump)

**Zarathos Feats (39):**
Ability Focus (possession), Cleave, Combat Reflexes, Cornugon Smash, Critical Focus, Devastating Strike, Diehard, Dodge, Dreadful Carnage, Endurance, Flyby Attack, Furious Focus, Great Cleave, Great Fortitude, Greater Vital Strike, Imperious Command, Improved Bull Rush, Improved Critical (claw), Improved Critical (longsword), Improved Disarm, Improved Grapple, Improved Natural Attack (claw), Improved Vital Strike, Indomitable Faith, Intimidating Prowess, Iron Will, Lightning Reflexes, Martial Weapon Proficiency (longsword), Multiattack, Power Attack, Quicken SLA (hellfire blast), Shatter Defenses, Staggering Critical, Toughness, Vital Strike, Weapon Focus (claw), Weapon Focus (longsword), Weapon Specialization (claw), Weapon Specialization (longsword)

**Chain weapon feats NOT inherited — Zarathos uses natural attacks and the Sword of Uri-El.**

---

## CUSTOM MECHANICS

### The Empyreal Descriptor [empyreal]
- Bypasses ALL fire resistance/immunity
- Bypasses ALL holy resistance/immunity
- Bypasses ALL unholy resistance/immunity
- Immune: true constructs (no soul), genuinely innocent (nothing to judge), soulless beings (Centurious-type — Zarathos's hard counter)
- This is NOT holy fire and NOT unholy fire. It is divine judgment fire from the Empyrean.

### Existential Dread — Soul Awareness Tiers
DC 30 (GR) / DC 35 (Zarathos). Soul-based, NOT mind-affecting. Bypasses fear/mind-affecting immunity for souled creatures.

| Tier | Who | Fail | Success |
|------|-----|------|---------|
| 0 | No soul (constructs, mindless) | Immune | — |
| 1 | Animal soul (INT 1-2) | Flee max speed | −1 all checks |
| 2 | Mortal soul (INT 3+) | Shaken 1d6 rds (evil: Frightened) | None |
| 3 | Aware soul (divine casters, 10+ ranks religion/planes) | Frightened 1d4 rds | Shaken 1 round |
| 4 | Cosmic soul (outsiders, intelligent undead, demigods) | Panicked 1d4 rds | Frightened 1 round |
| 5 | Soul-thieves (liches, soul-consuming demons) | Panicked + DC or Cower | Frightened 1d4 rds |
| 6 | Divine (gods) | Frightened 1d6 rds | Shaken 1d6 rds |

Death-workers with divine sanction = Tier 2 at worst (professional courtesy).
Zarathos adds **Primordial Wrongness**: Tier 0 creatures suffer −2 to attacks/skills within 120 ft. No save.

### Penance Stare — FINAL LOCKED
- **DC:** 40 (both forms, soul-based Will save)
- **Contact:** Opposed Intimidate to force eye contact; voluntary = immediate lock
- **Judgment Lock:** Paralyzed once contact established; external physical intervention only to break
- **On fail:** GR: 4d4 Wis/round | Zarathos: 5d4 Wis/round
- **On success:** 1 Wis damage flat (NOT 1d4 — this single die type is the difference between 16 and 31 rounds at deity tier)
- **At Wis 0:** Catatonic. Soul consumed. DC 45 Heal (9th-level divine) or miracle/wish only.

**Rounds to catatonic benchmarks:**
| Target | GR | Zarathos |
|--------|----|---------|
| Street mortal (CR5) | 1.0 | 0.7 |
| Elite caster (CR21) | 3.0 | 2.0 |
| Demon Lord high (CR30) | 12.1 | 8.9 |
| Demigod (CR37) | 15.3 | 11.6 |
| Lesser Deity (CR42) | 26.2 | 22.4 |
| Greater Deity (CR60) | 31.0 | 26.5 |

### Fear Feat Chain
Cornugon Smash (free demoralize on PA hit) → Imperious Command (Cowers before Shaken) → Shatter Defenses (shaken = flat-footed) → Dreadful Carnage (kills spread dread)

---

## THE ZARATHOS DIAL

| Mode | Trigger | Effective CR | Changes |
|------|---------|-------------|---------|
| Blaze Leading | Near innocents, moral anchor | 17 | −2 all DCs; spares non-combatants; Penance Stare vs guilty only; Hellfire Aura suppressed |
| Composite (Default) | Standard combat | 19 | As statted |
| Zarathos Surging | Overwhelming evil, Blaze fails DC 22 Will | 21 | Holy Aura auto-activates; Nova = 15d6 no save; Cold Hellfire freely; Hellfire Aura cannot be suppressed |

**Bonus vs. guilty:** +2 profane to attacks and +2 to empyreal DCs vs evil-aligned.

---

## THE SWORD OF URI-EL

**Also known as:** Lahat HaCherev (Hebrew: "the flame of the whirling sword," Genesis 3:24 — the actual name of the weapon placed at the gate of Eden, associated with Uriel in tradition)

**Scaling by wielder:**
| Property | Standard | Ghost Rider | Zarathos |
|----------|----------|-------------|---------|
| Sacred Fire | +4d6 empyreal | +6d6 empyreal | +8d6 empyreal |
| Soul-Searing DC | 30 | 32 | 35 |
| Soul-Searing dmg | 2d6 Wis | 3d6 Wis | 4d6 Wis |
| Anathema DC | 35 | 38 | 40 |
| Anathema (CR20+ fail) | 20d6 empyreal | 20d6 empyreal | 30d6 empyreal |
| Insight bonus | +4 | +4 | +6 |

**Weight:** 4 lbs (or 0 lbs when Willing Blade accepts wielder)
**Ego:** 28; communicates via sensation not words
**Crit:** 17-20/×3 (built into sword; Improved Critical feat on Zarathos confirms RAW)

---

## HELLFIRE SHOTGUNS

**Two weapons. Both appear from nowhere — reached for behind the back, no sheath. Power comes from WITHIN JOHNNY, not the weapons. Inert in anyone else's hands.**

**Winchester Model 1887** — lever-action, sawed-off, 12-gauge. 2 shots/round.
**Remington 11-87** — semi-auto, sawed-off, pistol grip, pistol foregrip. 4 shots/round. Six-round brass-cased bandoliers on each side.

Both: 18 physical rounds for non-users (12 bandoliers + 6 in tube), brass-cased, flame-proof. Empyreal rounds infinite for Blaze/Ghost Rider — no uses/day.

| Stat | Johnny — Winchester | Johnny — Remington | Ghost Rider (either) |
|------|--------------------|--------------------|---------------------|
| Attack | +7 touch | +7 touch | +22 touch |
| Damage | 2d6+3 empyreal (30 ft.) | 2d6+3 empyreal (30 ft.) | 6d6 empyreal (40 ft.) |
| Rate | 2 shots/round | 4 shots/round | 2 or 4/round (by weapon) |
| Full attack | — | — | +22/+17/+12/+7, 6d6 each |
| Soul fear DC | 16 Will | 16 Will | 30 Will |
| Point-blank soul blast | — | — | DC 40 Judgment Lock within 10 ft. |

---

## HELLCYCLE

- HP: 120; Hardness: 20
- Speed: 120 ft. tactical (combat); supernatural chase speed
- Trail of Hellfire: 10 ft. wide × 15 ft. tall, 6d6 empyreal (DC 25 Ref half), 1 min
- Rampage: straight-line charge hitting all in path
- Cannot be permanently destroyed while Zarathos is bound
- Reforms within 1d10 rounds if destroyed

---

## FOUNDRY VTT JSON — KNOWN ISSUES HISTORY

### v1 (failed to open)
- `_comment` keys at root level (schema violation)
- Item `_id` lengths wrong (not 16 chars)
- Missing `changeFlags: {}` on items
- `weight: 8` should be `weight: { value: 8 }` on physical items
- `languages.value: ["common"]` should be `value: [], custom: "Common"` (wrong — see v2 fix)

### v2 (still failing)
- `languages.custom` must be `[]` not `""`
- `weaponProf` and `armorProf` missing from actor traits
- Same missing from class and race items
- Same missing from ALL feat items (reduce iterates every item)
- Wrong field names throughout (penalty→userPenalty, cs→rt+ability, etc.)

### v3 (current — working)
Built entirely from real schema exports:
- Blank PC export: `fvtt-Actor-asdf-cvW74hYok9UvAZFw.json`
- NPC export (Warrior class): `fvtt-Actor-human-bandit-zbCKcVGG5xIl5ESK.json`

**Key schema facts (PF1e v10.8 / Foundry v11):**
- `abilities.str.userPenalty` not `penalty`
- `attributes.hp`: `{base, temp, nonlethal, offset}` not `{value, max, min}`
- `attributes.savingThrows.fort`: `{base, ability}` not `{value}`
- `traits.senses`: structured object not string
- `traits.languages.custom`: `[]` not `""`
- `traits.di/dv/ci.custom`: `[]` not `""`
- `traits.weaponProf` and `armorProf` ARE on the actor traits block
- `traits.weaponProf` and `armorProf` are NOT on weapon items, but ARE on feat/race/class items
- `skills`: `{ability, rt, acp, rank}` — no `cs` field; ability is the 3-letter key
- PF1e skill abbreviations: Knowledge (arcana)=`kar`, Knowledge (local)=`klo`, Knowledge (planes)=`kpl`, Knowledge (religion)=`kre`, Sleight of Hand=`slt`, not `slh`
- `details.xp`: `{value: n}` not bare number
- `details` has no `level.value` for characters (class item handles level)
- Feat `subType` not `featType`; values: `"feat"`, `"trait"`, `"misc"`, `"racial"`
- Feat `abilityType`: `"na"`, `"ex"`, `"su"`, `"sp"`
- Change format: `{_id (8 char), formula, target, type}` — no `operator` or `subTarget`
- Change `_id`: 8 characters (not 16)
- Actor `_id` and item `_id`: 16 characters
- `weaponProf.custom` and `armorProf.custom` on items: `[]` not `""`
- Physical item `weight`: `{ value: 8 }` not bare `8`
- Weapon needs `actions[]` array with attack definitions to show in combat tab
- Weapon `subType`: `"exotic"`, `"martial"`, `"simple"` (not `"weaponType"`)
- Class item `subType`: `"npc"` or `"base"` (not `"classType"`)
- Class item needs `fc.alt: {value, notes}`

**Icon paths:**
- Core Foundry icons: `icons/weapons/guns/gun-brown.webp` (confirmed exists)
- PF1e system icons: `systems/pf1/icons/...` (chain.jpg, etc.)
- Do NOT use `icons/weapons/guns/gun-blunderbuss-ornate-brown.webp` (404)
- Do NOT use `systems/pf1/icons/items/weapons/pistol.jpg` (404)
- When unsure of icon path: ASK USER

---

## JOHNNY BLAZE FOUNDRY v3 — CORRECTIONS LOG

All errors found during review and corrected in v3:

| Field | Wrong | Correct | Source |
|-------|-------|---------|--------|
| STR | 10 | 13 | MD stat block (finalized — peak athletic human) |
| CON | 12 | 13 | MD stat block |
| WIS | 16 | 11 | MD stat block (WIS/CHA were swapped) |
| CHA | 14 | 16 | MD stat block |
| Bluff ranks | 7 | 5 | Total +11 requires 5 ranks with CHA +3 +3 |
| Knowledge (Religion) | 0 ranks | 7 ranks | Skill listed in MD, missing from JSON |
| Profession (stunt rider) | 0 ranks | 7 ranks | Skill listed in MD, missing from JSON |
| Height | 6'0" | 5'10" | Caught by user |
| Age | 35 | ~28 | Invented; canon says late 20s |
| EWP (Firearms) proficiency | missing | added | Caught by user |
| Infernal Contract Immunity | missing | added | Caught by user |

---

## ITEMS STILL NEEDED FOR JOHNNY BLAZE FOUNDRY SHEET

Manual additions required after import (cannot be automated):
- **Nine World Records** — Buff item, +4 Ride, activate always
- **Street Smarts** — Buff item, +4 Bluff/Perception/Sense Motive, activate in urban/road environments
- **Occult Scholar** — Buff item, +4 Knowledge (arcana/religion/planes) vs demons, activate situationally
- **Nerves of Steel** — Buff item, +2 Will vs supernatural fear, activate situationally
- **Ride +4 base buff** — already captured by Nine World Records above
- **Sense Motive +8 insight** — the Infernal Contract Immunity change only automates the Will save bonus; Sense Motive must be added as a context note or manual buff

---

## CANON FACTS CONFIRMED

### Physical
- Johnny Blaze height: **5'10"** | Ghost Rider height: **6'2"**
- Johnny weight: ~180 lbs
- Age: late 20s (canonical); ~28 for this build
- Hair: blonde | Eyes: blue (glow orange-black in GR proximity)
- Jacket: Hell-Tempered Leathers — +2 leather armor (human) / +3 ghost touch leather (GR); fire immune; Hardness 15

### Deal Structure
- Johnny made the deal at **age 17**
- Mephisto cured Crash Simpson's cancer; Crash died in a stunt accident anyway (technicality)
- The bond was later sealed beyond Mephisto's power to alter by **the archangel Zadkiel** and ultimately by authority of **the One Above All**
- Mephisto CANNOT alter the terms; he can only exploit loopholes, lie about facts, and use proxies
- Johnny has been to Hell three times; walked out twice on his own; the third time an angel opened the door

### Zarathos Canon
- 21,000 years old minimum; predates the angelic/demonic divide
- Carries **empyreal** fire, not holy or unholy — belongs to neither camp cleanly
- This is why he has no Unholy Aura
- His WIS 24 is intentionally low for his CR — raw destructive force, not wisdom
- Hard counter: Centurious-type soulless beings (all soul abilities fail + −4 attacks/saves within 30 ft.)
- Zarathos bound within Crystal of Souls by Centurious at one point; later reconstituted in Blaze

### The Sword
- Marvel source: Blaze Vol 1 #11-12; Uncanny Avengers Annual Vol 1 #1
- Hebrew name: **Lahat HaCherev HaMithappekhet** ("the flame of the ever-turning sword") — Genesis 3:24
- Associated with Uriel/Uri-El in tradition; Uriel stands at the Gate of Eden with a fiery sword
- The sword does not speak; communicates via sensation (warmth/cold, ease/resistance)
- Zarathos's resonance is COMPLETE (he is the ancient fire); Ghost Rider's resonance is PARTIAL (recognizes the same flame in different vessels)

### Hellfire
- Marvel canon describes hellfire as **"empyreal"** — from the Empyrean, the highest Heaven
- VS Battles Wiki: "burns the soul and can be used to burn the physical body"
- NOT hot hellfire vs cold hellfire confusion: cold hellfire affects the spirit only (no physical damage) — basis for Cold Hellfire Touch (Wis damage)
- The chain responds to mental commands; upper length "unknown" per Marvel Database
- Chain binds the SOUL not the body — basis for paralysis (not entangled), no teleportation, standard magic cannot break it

---

## OPEN ITEMS / PENDING DECISIONS

- [x] Age for Johnny Blaze in JSON — set to 28 ✓
- [x] Continue review of Johnny Blaze Foundry sheet for additional errors ✓
- [x] Ghost Rider Foundry sheet (CR 19 form) — `ghost_rider_foundry_v1.json` ✓
- [x] Zarathos Foundry sheet (CR 26 form) — `zarathos_foundry_v1.json` ✓ (70 items; Large size bug `lrg`→`lg` fixed)

---

## DESIGN DECISIONS LOCKED

1. **DC 40 flat** for Penance Stare Will save (both GR and Zarathos)
2. **Success damage = 1 flat** (not 1d4) — difference between 16 and 31 rounds at deity tier
3. **Fail damage = 4d4 GR / 5d4 Zarathos** Wis per round
4. **Empyreal descriptor** bypasses all fire AND holy AND unholy resistance/immunity
5. **Hellfire chain proficiency** = inherent to divine office, no feat required
6. **EWP (Firearms)** = included for RAW compliance on Hellfire Shotgun
7. **Zarathos WIS 24** = intentional design choice, not error
8. **Zarathos unholy aura removed** = predates angelic/demonic divide, carries empyreal
9. **Willing Blade proficiency for Zarathos** = MWP (longsword) added as RAW option (Willing Blade acceptance could also rule it inherent; both valid)
10. **Contract Immunity** = hard narrative rule, not a saving throw — no roll permitted when goal is to alter Johnny's nature/contract/values
