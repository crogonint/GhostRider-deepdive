---
title: "Full Research and Session Notes"
aliases: ["Full Research", "Session Notes Complete"]
tags: [pf1e, ghost-rider, marvel-rpg, research, session-notes]
---

# Ghost Rider PF1E — Full Research & Session Notes

*Complete session memory. Every decision, every data point, every calculation.*

---

## PART 1: WILL SAVE RESEARCH — DEMON LORDS, EMPYREAL LORDS, DEITIES

### Confirmed Will Saves (from fetched PF1e stat blocks)
| Creature | CR | Will Save | Source |
|---|---|---|---|
| Baphomet | 27 | +31 | ✓ stat block |
| Dagon | 28 | +33 | ✓ stat block |
| Deskari | 29 | +32 | ✓ stat block |
| Nocticula | 30 | +35 | ✓ stat block |
| Shax | ~27 | +28 | ✓ stat block |
| Sifkesh | ~27 | +30 | ✓ stat block |
| Xoveron | ~28 | +33 | ✓ stat block |
| Ragathiel | 27 | +27 | ✓ stat block |
| Black Butterfly | 28 | +28 | ✓ stat block |

### Calculated Will Saves (HD + Wis mod, formula: 2+floor(HD/2)+Wis)
| Creature | CR | Type | Will Save | Method |
|---|---|---|---|---|
| Kostchtchie | 26 | Demon Lord | ~+27 | 31 HD → base +17, Wis +10 |
| Pazuzu | ~28 | Demon Lord | ~+31 | 35 HD → base +19, Wis +12 |
| Korada | 26 | Empyreal Lord | ~+28 | Wis 34 back-calc'd from AC |
| Cernunnos | 28 | Empyreal Lord | ~+25 | Wis 22, calculated |
| Bokrug | ~28 | Great Old One | ~+27 | 30 HD → base +17, Wis +10 |
| Hastur | ~27 | Great Old One | ~+24 | 25 HD → base +14, Wis +10 |
| Cthulhu | ~28 | Great Old One | ~+28 | 27 HD → base +15, Wis +13 |

### Key Note on Save Formula
- PF1E natural 1 = auto-fail (5% floor always)
- PF1E natural 20 = auto-succeed (5% ceiling always)
- P(fail) = clamp(DC − Will − 1, min=1, max=19) / 20
- At DC 40: Will +35 = 20% fail; Will +39 = nat-1 only (5%)

### Will Save Fail Rate Table (from session research)
| Tier | CR | WIS | Will Save | Fail DC30 | Fail DC40 | Fail DC50 |
|---|---|---|---|---|---|---|
| Mortal low | 11 | 10 | +5 | 95% | 95% | 95% |
| Mortal high | 11 | 18 | +13 | 80% | 95% | 95% |
| Mortal low | 16 | 12 | +8 | 95% | 95% | 95% |
| Mortal high | 16 | 22 | +17 | 60% | 95% | 95% |
| Champion low | 21 | 14 | +12 | 85% | 95% | 95% |
| Champion high | 21 | 26 | +22 | 35% | 85% | 95% |
| Empyreal Lord low | ~27 | 22 | +27 | 10% | 60% | 95% |
| Empyreal Lord high | ~27 | 34 | +28 | 5% | 55% | 95% |
| Great Old One | ~28 | 31-36 | +26 | 15% | 65% | 95% |
| Demon Lord low | ~28 | 29-30 | +27 | 10% | 60% | 95% |
| Demon Lord avg | ~28 | 31-32 | +31 | 5% | 40% | 90% |
| Demon Lord high | ~30 | 32-36 | +35 | 5% | 20% | 70% |
| Demigod low | ~37 | ~31 | ~+32 | 5% | 35% | 85% |
| Demigod high | ~37 | ~38 | ~+36 | 5% | 15% | 65% |
| Lesser Deity low | ~42 | ~32 | ~+40 | 5% | 5% | 45% |
| Lesser Deity high | ~42 | ~38 | ~+45 | 5% | 5% | 20% |
| Intermediate Deity | ~50 | ~44 | ~+53 | 5% | 5% | 5% |
| Greater Deity | ~60 | ~45 | ~+62 | 5% | 5% | 5% |

### Empyreal Lords — Special Note
- All have **Seed of Life** trait (like Demon Lords' Abyssal Resurrection) — they return if slain
- Most have Regen suppressed by deific/mythic damage (accessible to high-level PCs)
- Notable exception: Black Butterfly Regen 30 is harder to suppress
- **Korada** (CR 26, Wis 34) is the outlier — highest Wis of the group, adds Wis to AC (monk)
- Ragathiel and Cernunnos both Wis 22 — dramatically lower than Demon Lord equivalents at same CR
- Empyreal Lords sit at CR 26-28, directly overlapping lower-tier Demon Lords

### Cosmological Note (user-confirmed)
The PF1E cosmology includes a **God Over All / One True God** who physically wrestled the known universe away from Cthulhu and the Great Old Ones. The Great Old Ones create universes just to destroy them and collect the energy released. The One True God keeps this from happening to the current universe while greater gods administer the celestial plane polytheistically. Empyreal Lords and Archangels serve this hierarchy. Named archangels (Michael, Raphael, Uriel) are categorically different from Empyreal Lords — Will saves in the +45-55+ range, potentially immune to Wis damage as a trait.

---

## PART 2: PENANCE STARE — FULL DESIGN ANALYSIS

### Original Problem Statement
- Original DC 30 meant Demon Lords (~Will +35) fail only on nat-1 (5%)
- At 5% fail with 1d4/2CR fail damage: Demon Lord (CR 30) = 15d4 on a fail = catastrophic but near-useless since 95% success
- No design space between "immediately destroyed" and "mosquito bite"

### Design Targets Set
| Tier | CR | Wis | Will | Target Rounds |
|---|---|---|---|---|
| Street mortal | 1-5 | 10 | +3 | 1 |
| Veteran | 6-10 | 11 | +5 | 1 |
| Master Caster | 11-15 | 20 | +15 | 1-2 |
| Elite Caster | 16-21 | 26 | +22 | 2-4 |
| Demon Lord low | 26-28 | 30 | +28 | 10-15 |
| Demon Lord high | 29-30 | 34 | +35 | 12-20 |
| Demigod | 35-39 | 36 | +36 | 15-25 |
| Lesser Deity | 40-45 | 38 | +45 | 20-35 |
| Intermediate Deity | 46-54 | 44 | +53 | 25-45 |
| Greater Deity | 55-65 | 45 | +62 | 30-60 |

### DC Options Evaluated

**Option A: d20 + Wis mod vs DC 26 (raw soul)**
- Demon Lord dies in 5 rounds. Greater Deity in 10. Tier scaling collapses at top.

**Option B: Opposed d20+Will vs d20+GR(+30)**
- Mathematically breaks when target's Will exceeds GR's Penance Rating. Deities literally cannot fail.

**Option D: d20 + Wis mod + ½HD vs DC 40 (soul + power)**
- Greater Deity correct (31 rounds). Demon Lord tier 5-6 rounds — too fast.

**Option E: Soul Resistance (d20 + Wis mod + base Will progression, no feats/items)**
- Strips Iron Will, resistance cloaks, magic. Demon Lord drops from 12→6 rounds.
- Mortals unaffected (never had investment to lose). Deities unaffected (at 5% floor regardless).

**FINAL DECISION: Flat DC 40 Will Save**
- Rationale: Will save naturally spans +3 to +62 (59-point range), producing the correct curve
- No alternative ability score formula can reproduce this spread
- DC 40 is the mathematical inflection point where the natural Will progression produces the target spread
- At DC 40: Will +35 (Demon Lord) → 20% fail. Will +39 → 5% fail. Perfect natural separation.

### The Critical Success Damage Discovery
**This is the most important finding in the entire analysis:**
- At deity tier, 95% of rounds are SUCCESS rounds (only nat-1 fails)
- Success damage completely dominates expected rounds at this tier
- Success = 1d4 (avg 2.5): Greater Deity (Wis 45) dies in **~16 rounds**
- Success = 1 flat: Greater Deity dies in **~31 rounds**
- One die type is the difference between 16 and 31 rounds at deity tier

### Final Penance Stare — LOCKED
```
DC 40 Will save (soul-based, not mind-affecting)
Contact: Opposed Intimidate (GR +38 / Zarathos +55)
         Voluntary eye contact = immediate lock, no roll
Judgment Lock: paralyzed, no save to break, external intervention only
On fail:    GR: 4d4 Wis/round | Zarathos: 5d4 Wis/round
On success: 1 Wis damage flat (NOT 1d4)
At Wis 0: catatonic, soul consumed, DC 45 Heal / miracle / wish only
```

### Rounds to Catatonic — Both Forms
| Target | GR | Zarathos | Design |
|---|---|---|---|
| Street mortal (CR5) | 1.0 | 0.7 | 1 |
| Veteran (CR10) | 1.2 | 0.9 | 1 |
| Master Caster (CR15) | 2.1 | 1.4 | 1-2 |
| Elite Caster (CR21) | 3.0 | 2.0 | 2-4 |
| Demon Lord high (CR30) | 12.1 | 8.9 | 10-20 |
| Demigod (CR37) | 15.3 | 11.6 | 15-25 |
| Lesser Deity (CR42) | 26.2 | 22.4 | 20-35 |
| Intermediate Deity (CR50) | 30.3 | 27.9 | 25-45 |
| Greater Deity (CR60) | 31.0 | 28.6 | 30-60 |

---

## PART 3: EXISTENTIAL DREAD — DESIGN PROCESS

### Problem: Standard Fear Is Mind-Affecting
All standard fear mechanics are [mind-affecting]. Immunity list includes: undead, constructs, mindless, oozes, plants, vermin, aeons, inevitables, qlippoth. Ghost Rider canonically frightens all of these.

**RAW bypass options reviewed:**
| Method | What it strips | Limitation |
|---|---|---|
| Aura of Cowardice (Antipaladin 3) | ALL fear immunity, −4 to saves | Living creatures only — undead/constructs still immune |
| Draconic Malice (3rd level spell) | Fear + mind-affecting immunity | Living creatures only |
| Horror Adventures optional rule | Converts immunity to resistance | GM fiat only |

**Conclusion:** No RAW mechanism allows frightening a lich, vampire, or construct. Ghost Rider canonically can. Solution: type reclassification.

### Solution: Soul-Based Fear
Ghost Rider's fear is not psychological — it's existential recognition of divine judgment by a creature's soul. Mechanical reclassification:
- NOT [mind-affecting]
- NOT [emotion]  
- NOT [fear]
- Soul-based supernatural effect — bypasses all three immunity types for souled creatures
- Mindless creatures (constructs, oozes, mindless undead) remain immune — no soul to recognize

### User's Insight
"Ghost Rider doesn't induce fear. He induces Existential Dread."
Those more aware of what they're looking at are MORE terrified, not less — awareness and dread are proportional, not inverse. This inverts every other immunity system in the game.

### Soul Awareness Tiers (Final)
DC 30 (GR) / DC 35 (Zarathos)

| Tier | Who | Fail | Success |
|---|---|---|---|
| 0 | No soul (constructs, mindless) | Immune | — |
| 1 | Animal soul (INT 1-2) | Flee max speed | −1 all checks |
| 2 | Mortal soul (INT 3+) | Shaken 1d6 rds (evil: Frightened) | None |
| 3 | Aware soul (divine casters, 10+ ranks religion/planes) | Frightened 1d4 rds | Shaken 1 round |
| 4 | Cosmic soul (outsiders, intelligent undead, demigods) | Panicked 1d4 rds | Frightened 1 round |
| 5 | Soul-thieves (liches, soul-consuming demons) | Panicked + DC or Cower | Frightened 1d4 rds |
| 6 | Divine (gods) | Frightened 1d6 rds | Shaken 1d6 rds |

**The Reaper distinction:** Psychopomps doing LEGITIMATE soul collection are Tier 2 at worst — they're in the same business, different department. SOUL THIEVES (liches, beings who imprison souls against natural law) are Tier 5 — they get the worst treatment.

**Spellcasting in aura:** DC 26 (GR) / DC 35 (Zarathos) concentration check for [emotion]/[fear] spells or concentration spells.

**Zarathos only — Primordial Wrongness:** Tier 0 creatures (mindless/constructs) suffer −2 to attacks and skills within 120 ft. No save. Not fear-coded.

---

## PART 4: STAT BLOCK AUDIT — FULL FINDINGS

### Ghost Rider Audit
| Stat | Original | Corrected | Reason |
|---|---|---|---|
| Touch AC | 14 | **20** | Deflection applies to touch in PF1E |
| HP | 294 | **319** | Toughness +18 (1/HD, not flat +3) + avg recalc |
| WIS | 17 | **22** | Conversion error |
| Ref | +16 | **+17** | Lightning Reflexes documented |
| Will | +16→+19 | **+20** | Indomitable Faith inherited from Blaze |
| Cold hellfire DC | 27 | **30** | CON-based (10+9+11), not CHA |
| Soul binding DC | 27 | **30** | CON-based |
| Hellfire breath DC | 27 | **26** | CHA-based (10+9+7) |
| Penance Stare DC | 30 | **40** | Design decision |
| Feat count | 18 listed | **25** | +Diehard, Endurance, Indomitable Faith, Toughness (inherited) + fear chain |
| Melee chain damage | STR+8 | **STR+12** | WS+2 documented, STR mod corrected |

**DC formula note:** Original used ceiling division for ½HD instead of floor — caused all CHA-based DCs to be +1 high.

### Zarathos Audit
| Stat | Original | Corrected | Reason |
|---|---|---|---|
| CON | 36 | **38** | HP 487 independently confirms +14 mod; soul rend DC 36 also confirms CON 38 |
| HD | 25 | **26** | Bumped for inheritance consistency |
| HP | 487 | **537** | CON 38 + Toughness 26 HP (1/HD) + HD bump |
| Touch AC | 18 | **32** | Deflection +12 AND profane +6 both apply to touch |
| Fort | +29 | **+31** | CON 38 + Great Fortitude (+2) |
| Ref | +21 | **+22** | Lightning Reflexes (+2) |
| Will | +24 | **+25** | Full inheritance chain documented |
| CMB | +40 | **+41** | HD bump +1 |
| CMD | 56 | **55** | Recalculated |
| Claw attack | +37 | **+40 base / +35 PA** | Size −1 corrected; base vs PA variant listed separately |
| Intimidate | +40 | **+55** | Intimidating Prowess inherited from GR (STR +14) |
| Penance DC | 38 | **40** | Design decision |
| Possession DC | 38 | **37** | CHA + Ability Focus = 36 RAW, not 38 |
| Soul rend DC | 36 | **37** | CON 38 + ½HD 13 = 37 |
| Most ability DCs | 34 | **35** | HD bump: ½ of 26 = 13 |
| Feat count | 14 listed | **39** | Full inheritance chain + sword feats + Vital Strike chain |
| Unholy aura | present in SLAs | **removed** | Predates angelic/demonic divide |

### The Inheritance Chain Resolution
The previously mysterious +3 on Zarathos's Will save was:
- Iron Will (+2) + Indomitable Faith (+1) — inherited from Blaze through GR
- Exactly +3. Not a conversion error at all — correct but undocumented.

---

## PART 5: INHERITANCE CHAIN ANALYSIS

### Johnny Blaze (Expert 7, CR 6)
**How CR was determined:** Original block labeled as CR 19 (mislabeled — GR's CR). Back-calculated from HP 38/42, saves, and feat count:
- Expert 7: Fort +3 ✓, Ref +4 ✓, Will +5 + Iron Will +2 + Indomitable Faith +1 = +8 ✓
- HP 42: 8 + 6×4.5 + 7×CON(+1) = 42 ✓
- 7 feats with Human level 7 = correct

**Feats Johnny contributes:**
- Diehard, Endurance, Indomitable Faith (+1 Will), Iron Will (+2 Will), Nerves of Steel, Toughness

**Johnny's Intimidate (Intimidating Prowess):**
- Ranks 7 + class 3 + CHA +3 + STR +1 = +14 base (IP active). Displayed as +13 base without IP buff active.
- STR 13 finalized — peak athletic human, top of non-enhanced published range

### Ghost Rider Inherits From Johnny
- Diehard, Endurance, Indomitable Faith, Toughness (carried explicitly)
- Nerves of Steel — inherited but redundant (GR immune to fear)
- Nine World Records, Street Smarts, Occult Scholar (special qualities)
- Indomitable Faith bumps GR Will: +19 → +20

### Zarathos Inherits From GR + Johnny
- ALL GR feats EXCEPT chain weapon feats (EWP spiked chain, WF/WS/IC spiked chain)
- Chain feats replaced with: INA (claw), Multiattack, WF (claw), WS (claw), Improved Critical (claw)
- Sword of Uri-El feats added: MWP (longsword), WF (longsword), WS (longsword), IC (longsword)
- Additional Zarathos-native: Ability Focus (possession), Critical Focus, Devastating Strike, Flyby Attack, Greater Vital Strike, Improved Vital Strike, Vital Strike, Quicken SLA (hellfire blast), Staggering Critical
- Intimidating Prowess inherited: STR 48 = +19 mod → Intimidate +60 (STR updated 38→48 final)
- Note: Zarathos's Intimidate is +55 on final sheet (IP + full calculation)

---

## PART 6: FEAR FEAT CHAIN

Added during session to represent GR's active use of his terror aura:

**Cornugon Smash** → free Intimidate check on any Power Attack hit
**↓** → triggers **Imperious Command** → demoralized target Cowers 1 round before becoming Shaken
**↓** → **Shatter Defenses** → shaken targets are flat-footed when hit
**↓** → **Dreadful Carnage** → kills spread Existential Dread to nearby enemies (automatic on kill)

This chain means: hit with Power Attack → free demoralize → target Cowers → next hit flat-footed → if killed, everyone nearby must save.

---

## PART 7: HELLFIRE SHOTGUN — CANON RESEARCH

### Origin Discrepancy (Comics vs Film)
**Comics origin** (Ghost Rider vol. 3 #14, 1991): Johnny was carrying an ordinary shotgun when Danny Ketch's Ghost Rider physically grabbed it — the weapon absorbed Danny's hellfire and was permanently transformed. It's a small double-barreled shotgun in the comics. Power later revealed to come from within Johnny himself, not the weapon.

**Film origin** (2007 film): Winchester Model 1887 lever-action, given to Johnny by Carter Slade (the Caretaker), transformed when Johnny thrust it into a shadow.

**Build decision:** Winchester Model 1887 as physical form (iconic visually), comic origin as mechanics (power from within Johnny). The gun is inert without Blaze — a damaged non-magical shotgun in anyone else's hands.

**Also confirmed canon:** Unlimited ammunition, motorcycle conjuration ability (rarely discussed), dramatic supercharge in Ghost Rider's hands.

---

## PART 8: ABILITY DC CALCULATIONS — BASE FORMULAS

Standard PF1E formula: 10 + ½ HD + ability modifier

**Ghost Rider (18 HD):**
- Base: 10 + 9 = 19
- CON-based (CON 32, +11): **30** — nova, brimstone, soul binding, cold hellfire
- CHA-based (CHA 24, +7): **26** — breath, suggestion, curse, etc.
- WIS-based (WIS 22, +6): **25** — terror DCs for non-evil
- Penance Stare: **40** (design decision)

**Zarathos (26 HD):**
- Base: 10 + 13 = 23
- CHA-based (CHA 34, +12): **35** — nova, aura, hellfire blast
- CON-based (CON 38, +14): **37** — soul rend
- CHA + Ability Focus (possession): **37** (not 38 as originally stated)
- Penance Stare: **40** (design decision)

---

## PART 9: SWORD OF URI-EL — LAHAT DISCOVERY

### Hebrew Etymology
The sword placed at the gate of Eden (Genesis 3:24) is named in Hebrew: **Lahat HaCherev HaMithappekhet** — "the flame of the ever-turning/whirling sword." The word *lahat* specifically relates to supernatural fire/enchantment.

Associated with Uriel in multiple traditions — "stands at the Gate of Eden with a fiery sword."

The Sword of Uri-El is also correctly called **Lahat HaCherev** — the actual Biblical name of the weapon, predating Uriel's personal identification with it.

### Zarathos Resonance — Why It's Complete vs Partial
- Ghost Rider's resonance is PARTIAL: two flames that recognize each other as the same fundamental fire in different vessels
- Zarathos's resonance is COMPLETE: he IS the ancient fire. The sword is the ancient fire wearing a different shape. When it recognizes him, it becomes what it was always trying to be.

---

## PART 10: FOUNDRY VTT — SCHEMA LESSONS LEARNED

### Files Used as Schema Reference
- Blank PC: `fvtt-Actor-asdf-cvW74hYok9UvAZFw.json` (character type)
- NPC sample: `fvtt-Actor-human-bandit-zbCKcVGG5xIl5ESK.json` (npc type, Warrior class)

### Critical Schema Facts (PF1e v10.8 / Foundry v11)
| Field | Wrong | Correct |
|---|---|---|
| abilities.str.penalty | `penalty` | `userPenalty` |
| attributes.hp | `{value, max, min}` | `{base, temp, nonlethal, offset}` |
| attributes.savingThrows.fort | `{value: 0}` | `{base: 0, ability: "con"}` |
| traits.senses | string | structured object `{dv, ts, bs, bse, ll, sid, tr, si, sc, custom}` |
| traits.languages.custom | `""` | `[]` |
| traits.di/dv/ci.custom | `""` | `[]` |
| traits.weaponProf.custom | `""` | `[]` |
| traits.weaponProf/armorProf | absent | present on actor AND feat/race/class items |
| traits.weaponProf/armorProf | present | NOT on weapon items |
| skills structure | `{rank, cs, acp}` | `{ability, rt, acp, rank}` |
| skill abbrevs | `slh, knl, knp, kna` | `slt, klo, kpl, kar` |
| details.xp | bare number | `{value: n}` |
| feat.featType | `featType` | `subType` |
| feat.subType values | various | `"feat"`, `"trait"`, `"misc"`, `"racial"` |
| change format | `{_id, formula, operator, target, subTarget, modifier}` | `{_id (8 char), formula, target, type}` |
| change _id length | 16 chars | **8 chars** |
| actor/item _id length | varies | **16 chars** |
| weapon weight | `8` (bare) | `{"value": 8}` |
| class subType | `classType: "npc"` | `subType: "npc"` |
| class fc | `{hp, skill}` | `{hp, skill, alt: {value, notes}}` |
| class item | no tag | needs `tag: "expert"` etc. |

### What Broke Each Version
**v1:** `_comment` root keys; wrong-length IDs; missing `changeFlags`; bare `weight: 8`; `languages.value: ["common"]` wrong
**v2:** `languages.custom: ""` should be `[]`; `weaponProf`/`armorProf` missing from actor traits; missing from ALL items (reduce iterates every item); wrong ability score field names throughout; wrong skill structure
**v3:** Built from real schema — works

### Icon Path Facts
- `icons/weapons/guns/gun-brown.webp` — **confirmed exists** (user confirmed)
- `icons/weapons/guns/gun-blunderbuss-ornate-brown.webp` — **404, does not exist**
- `systems/pf1/icons/items/weapons/pistol.jpg` — **404, does not exist**
- **Rule going forward: ASK USER for icon paths rather than guessing**
- Core Foundry icons at `icons/...` — ask for directory listing
- PF1e system icons at `systems/pf1/icons/...` — ask for directory listing

---

## PART 11: JOHNNY BLAZE FOUNDRY SHEET — FULL CORRECTIONS LOG

### Errors Found During Review (corrected in v3)
| Field | Wrong (v1/v2) | Correct (v3) | How Found |
|---|---|---|---|
| STR | 10 | 13 | Finalized — peak athletic human |
| CON | 12 | 13 | Audit vs MD |
| WIS | 16 | 11 | Audit vs MD (WIS/CHA were SWAPPED) |
| CHA | 14 | 16 | Audit vs MD |
| Bluff ranks | 7 | 5 | Total +11 requires only 5 ranks with CHA +3 +3 |
| Knowledge (Religion) | 0 | 7 | Listed in MD, missing from JSON |
| Profession (stunt rider) | 0 | 7 | Listed in MD, missing from JSON |
| Height | 6'0" | 5'10" | User correction |
| Age | 35 | ~28 | Invented; canon says late 20s |
| EWP (Firearms) proficiency | missing | added | User correction |
| Infernal Contract Immunity | missing | added | User correction |
| weapons/guns icon | 404 | gun-brown.webp | User correction |

### Skills NOT Yet in v3 JSON (require manual Buff items)
- Nine World Records: +4 Ride (always on)
- Street Smarts: +4 Bluff/Perception/Sense Motive in urban/road environments (situational)
- Occult Scholar: +4 Knowledge vs demons/contracts/hellfire (situational)
- Nerves of Steel: +2 Will vs supernatural fear (situational, not automated)
- Contract Immunity Sense Motive +8: Only Will save change is automated; Sense Motive bonus needs manual buff

### Will Save Note
Foundry will show Will **+11** (correct). Source stat block showed +8 because WIS mod (+0 at WIS 11) was NOT zero in the original — it was just written without the WIS mod notation. The calculation is: 5 (base) + 0 (WIS 11) + 2 (Iron Will) + 1 (Indomitable Faith) = +8. The Foundry calculation of +8 is also correct — it auto-adds WIS +0. Earlier error was having WIS 16 in the JSON (which would make it +11).

---

## PART 12: DALL-E 3 PROMPTS GENERATED

### Prompt 1: Hellfire Shotgun — Weapon
*(Description of the weapon on a surface)*

### Prompt 2: Ghost Rider Firing Shotgun
"Ghost Rider, a towering figure with a flaming human skull for a head, stands in a wide aggressive stance firing a sawed-off Winchester Model 1887 lever-action shotgun directly toward the camera. The skull face is contorted in fury — jaw open in a silent roar, eye sockets blazing with intense orange-black hellfire, the flames streaming backward from the skull like a wreath of angry fire. He wears a black leather biker jacket with spiked shoulders, dark jeans, and heavy boots. The shotgun is extended forward in both hands, mid-blast — the muzzle erupting in a massive cone of orange-black hellfire that fills the lower foreground and partially obscures the implied target just off-camera below the frame. The muzzle flash is wrong in color — not yellow-white but deep orange fading to black at the edges, supernatural and consuming. Burning embers and wisps of hellfire trail back from the barrel toward the shooter. The veins of hellfire running along the shotgun's metalwork are fully lit. Background: a dark rain-slicked urban alley at night, distant streetlights haloed in smoke. Dramatic low-angle shot looking slightly up at Ghost Rider, the camera at roughly chest height of the implied victim in the foreground. Cinematic lighting — the hellfire is the primary light source, casting hard orange-black shadows upward across the skull face. Photorealistic, high contrast, dark fantasy, comic book realism. No text. No borders."

### Prompt 3: Existential Dread — Moment of Contact
"A powerful demon lord — hulking, armored, radiating dark energy, clearly a being of immense and terrible power — frozen mid-stride, one clawed hand half-raised. Every muscle locked. His face is the centerpiece: eyes wide, pupils blown, jaw slightly open. Not in pain. In recognition. He knows exactly what this is and exactly what it means for him. Behind his eyes, faint translucent impressions of his own past acts of cruelty are visible as ghostly overlapping images — faces of victims, moments of violence, rendered as pale amber afterimages layered across his face like a double exposure. He is not being attacked. He is being shown. Ghost Rider stands at the edge of the frame, partially out of shot, only the burning orange-black skull visible in profile, watching without expression. The demon lord's shadow behind him shows not his own silhouette but a cowering, smaller shape — the shadow of what he has always been afraid he truly is. Dark fantasy, photorealistic render, dramatic high-contrast lighting, the amber ghost-images providing warm secondary illumination against cold darkness. Shallow depth of field with the demon lord's face as the sharpest point. No text. No borders. Cinematic."

### Prompt 4: Ghost Rider Standing — Atmospheric Scene (DM Guide intro)
"Ghost Rider stands motionless at the center of a rain-slicked dystopian intersection at night, hands at his sides, the hellfire chain coiled loosely at his hip. He is doing nothing. He does not need to. His skull burns with deep orange-black flame that streams upward in the windless air, casting hard shadows in impossible directions. He is looking at nothing in particular. This is what makes it worse. A circle of dead grey grass and wilted weeds radiates outward from where he stands, the plants having given up in concentric rings. Puddles in the cracked asphalt nearest him are steaming, the water evaporating without heat, as if the moisture simply wants to leave. A flock of pigeons is caught mid-flight in the background, every bird banking sharply away from him in a single panicked arc. A stray dog in the far distance is already running and is not looking back. In the middle distance, a handful of ordinary people on a sidewalk have stopped walking. They do not know why. One has pressed himself against a wall. One woman has both hands over her mouth. A man in a suit has dropped his briefcase and is staring at his own hands. None of them can see anything wrong. None of them can stop feeling it. The air above Ghost Rider shimmers faintly amber, like heat haze, except the temperature is not the problem. A thin column of brimstone-yellow smoke rises lazily from a crack in the asphalt at his feet. The streetlights within half a block have dimmed to almost nothing. The ones beyond that radius blaze normally. Photorealistic dark fantasy render, wide shot, Ghost Rider small-to-medium in frame so the emptiness around him reads clearly. No text. No borders. The scene should smell like sulfur and scorched stone and the moment before a storm that never arrives."

---

## PART 13: CANON NOTES — MISCELLANEOUS

### Hellfire — Color and Nature
- Color: **orange-black**, not orange-yellow. This is what makes it look cosmologically wrong, not merely hot.
- Cold hellfire is a SEPARATE thing — "cold hellfire affects the human spirit" — no physical/heat damage
- Basis for Cold Hellfire Touch (Wis damage only, no fire damage)
- The chain responds to mental commands; upper length "unknown" per Marvel Database
- Chain binds the SOUL, not the body — basis for paralysis (not entangled condition), no teleportation, standard magic cannot break it

### The Deal
- Made at age 17
- Mephisto cured Crash Simpson's cancer; Crash died in a stunt accident anyway (technicality)
- Bond later sealed beyond Mephisto's ability to alter by archangel Zadkiel and the One Above All
- Mephisto CANNOT change terms — limited to loopholes, lying about facts, proxies
- Johnny been to Hell three times; walked out twice on his own; third time an angel opened the door

### Motorcycle Conjuration
Genuine canon ability — rarely discussed. Johnny can conjure a mundane motorcycle by pointing at any open surface (1/day). Ghost Rider can conjure a full Hellcycle by firing a barrel at the ground (3/day). This is why it's in both shotgun stat blocks.

### Zarathos Age
21,000+ years old minimum. Predates angelic/demonic divide. Canonically described as having possessed 21 millennia of hosts — basis for Tongues ability (all mortal languages from 21,000 years of hosts).

### Johnny's Age (Canon)
No fixed canonical age. Research summary: he makes the deal at 17; is consistently depicted as "young adult in late 20s to early 30s" at origin. Marvel sliding timescale prevents definitive aging. Build uses **~28**.

### Ghost Rider Height
- Johnny Blaze: **5'10"** (user confirmed; original JSON had 6'0" — incorrect)
- Ghost Rider form: **6'2"** (supernatural growth on transformation)

### The Sword of Uri-El — Marvel Canon
- Sources: Blaze Vol 1 #11-12; Uncanny Avengers Annual Vol 1 #1
- Uriel in tradition: "stands at the Gate of Eden with a fiery sword"; "who is over the world and over Tartarus"
- The sword is associated with both Jophiel and Uriel in different traditions
- Eastern Orthodox: after Christ's resurrection, the flaming sword was removed from Eden (making re-entry to Paradise possible)
- Ego: 28; communicates via sensation (warmth/cold, ease/resistance in the hand)

---

## PART 14: DESIGN DECISIONS — COMPLETE LIST

1. **DC 40 flat** for Penance Stare Will save (both GR and Zarathos)
2. **Success damage = 1 flat** (not 1d4) — deity tier survival depends on this
3. **Fail damage = 4d4 GR / 5d4 Zarathos** Wis per round
4. **Empyreal descriptor** bypasses all fire AND holy AND unholy resistance/immunity
5. **Hellfire chain proficiency** = inherent to divine office, no feat required
6. **EWP (Firearms)** = included for RAW compliance on Hellfire Shotgun
7. **Zarathos WIS 24** = intentional — raw destructive force, not wisdom
8. **Zarathos unholy aura removed** = predates angelic/demonic divide, carries empyreal
9. **MWP (longsword) on Zarathos** = RAW-clean feat for Sword of Uri-El (Willing Blade acceptance also valid as inherent)
10. **Penance Stare same DC (40) for both forms** — same power, same divine authority
11. **Soul-based fear type** (not mind-affecting) — core mechanic enabling fear vs all souled creatures
12. **Awareness tiers are proportional to dread** — more powerful/aware beings suffer MORE, not less
13. **Reaper distinction** — legitimate soul workers = Tier 2; soul thieves = Tier 5
14. **Zarathos HD bumped 25→26** — inheritance chain consistency
15. **Chain of Damnation renamed to Soul Binding on Zarathos** — he doesn't use the physical chain, manifests pure hellfire bonds
16. **Contract Immunity as hard rule** — no roll permitted when goal is to alter Johnny's nature/values/contract

---

## PART 15: OUTSTANDING / PENDING

- [ ] Age field in JSON: using ~28
- [ ] Continue reviewing Johnny Blaze v3 sheet in Foundry for additional errors  
- [ ] Ghost Rider Foundry sheet (CR 19) — not yet created
- [ ] Zarathos Foundry sheet (CR 26) — not yet created
- [ ] Manual Buff items needed in Foundry: Nine World Records, Street Smarts, Occult Scholar, Nerves of Steel, Sense Motive +8 from Contract Immunity

