---
title: "Spirit of Vengeance — Complete Design Notes (Expanded)"
aliases: ["SoV Design Notes", "Class Design Master", "Design Index"]
tags:
  - pf1e
  - ghost-rider
  - class
  - design-notes
system: Pathfinder 1E
status: All items resolved. Scaling audit pending.
last_updated: March 2026
---

# Spirit of Vengeance — Complete Design Notes (Expanded)

*All locked decisions from the design sessions, WITH full rationale for every choice. This document is intended to give a new reader full context — not just what we decided, but why, what alternatives were rejected, and what pitfalls to avoid.*

*This class is a custom PF1E class for playing Ghost Rider (or a Ghost Rider-like character) as a PC in a Pathfinder 1st Edition campaign. It was designed across multiple sessions with extensive playtesting math, canon research across 40+ Marvel sources, and iterative balancing. The companion documents (stat blocks, Foundry VTT JSONs, canon reference, Penance Stare design reference, etc.) are all in the same project folder.*

---

## TABLE OF CONTENTS

1. [Class Chassis](#1-class-chassis)
2. [Rider's Mantle (Transformation)](#2-riders-mantle)
3. [Overburn — The Devil's Carrot](#3-overburn)
4. [Heaven's Brand (Empyreal Damage)](#4-heavens-brand)
5. [The Empyreal Descriptor](#5-empyreal-descriptor)
6. [Burning Judgment Eyes / Sin Sight](#6-burning-judgment-eyes--sin-sight)
7. [Existential Dread (Aura)](#7-existential-dread)
8. [Penance Progression](#8-penance-progression)
9. [The Hellfire Chain](#9-the-hellfire-chain)
10. [Hellfire Breath](#10-hellfire-breath)
11. [Hellfire Backlash (Defensive)](#11-hellfire-backlash)
12. [Contract Immunity](#12-contract-immunity)
13. [The Medallion of Power](#13-the-medallion-of-power)
14. [Soul Interrogation](#14-soul-interrogation)
15. [The Infernal Steed](#15-the-infernal-steed)
16. [Zarathos Surge](#16-zarathos-surge)
17. [Hellfire Instability (d100 Table)](#17-hellfire-instability)
18. [Bonus Feats](#18-bonus-feats)
19. [Multiclassing](#19-multiclassing)
20. [Unbound / Spirit Unchained (Capstones)](#20-capstones)
21. [Class Progression Table](#21-class-progression-table)
22. [Damage Parity Benchmarks](#22-damage-parity)
23. [Key Design Principles](#23-key-design-principles)
24. [Rejected Alternatives](#24-rejected-alternatives)
25. [Open Items — Scaling Audit](#25-scaling-audit)

---

## 1. Class Chassis

| Property | Value |
|----------|-------|
| Hit Die | d10 |
| BAB | Full (+1/level) |
| Good Saves | Fort, Will |
| Poor Save | Ref |
| Skill Points | 4 + INT mod/level |
| Alignment | Any non-lawful |
| Proficiencies | All simple, all martial, spiked chain, firearms. Light armor, medium armor, shields (not tower). Hellfire Chain proficiency inherent. |

**Architecture decision:** ONE class, ONE character sheet. The player levels the Host (human recommended, any race allowed). Ghost Rider is a transformation — a class feature, not a separate creature. Like Barbarian Rage, not like a summoned monster. The Host's feats, skills, and weapon choices all carry into transformed state. The transformation enhances what you built — it doesn't replace it.

**Three-entity model:**
- **The Host** = your character. You level them normally.
- **Ghost Rider** = what happens when you transform. A class feature.
- **Zarathos** = what happens when you lose control. The DM takes over. (See section 16.)

**Starting Equipment — "Circus Refugee":** One MW weapon of choice (the one from your old life), one mount or vehicle (beat-up chopper, road-worn horse, wagon held together by spite), one set of armor/clothing (up to medium, MW), basic adventurer's kit if GM allows. Not much else. Johnny Blaze was a carnival stunt rider — the starting equipment reflects someone who left a previous life with nothing but what they were wearing.

---

## 2. Rider's Mantle

**Type:** Supernatural (Su). Free action to transform, free action to end.

**Rounds/day:** CHA mod + class level (minimum 1). At level 1 with CHA 14: **3 rounds.** At level 5: 7. At level 10: 12. At level 20: unlimited (Spirit Unchained).

**WHY this formula:** The user specifically wanted only "a couple of rounds to be the badass" at low levels — enough to want more, not enough to coast. The old formula (4 + CHA mod + 2/level) gave too many rounds, removing the temptation to overburn. The entire overburn mechanic (section 3) depends on the Host wanting more rounds than they have. CHA dependency rewards investing in the stat that also drives Penance DCs.

**While transformed:**

| Level | STR | CON | Natural Armor |
|-------|-----|-----|---------------|
| 1-3 | +2 | +2 | +1 |
| 4-10 | +4 | +4 | +2 |
| 11-19 | +6 | +6 | +3 |
| 20 | +8 | +8 | +4 |

Modeled on Barbarian Rage but slightly more conservative. Also grants fire immunity, fear immunity, -4 Diplomacy/Handle Animal, and activates Hellfire Chain, Heaven's Brand, and Existential Dread aura.

---

## 3. Overburn — The Devil's Carrot

**Core philosophy:** Zarathos doesn't threaten. He OFFERS. "Just one more round. Look what we can do together." The player should WANT to push past their limit because the reward is real — and the consequences are dramatic. The user explicitly wanted players to "try at low levels and screw up. Learn their lesson."

**The Carrot:** While in overburn, Heaven's Brand empyreal dice are **doubled** (1d4→2d4, 2d4→4d4, etc.). ONLY empyreal dice — weapon damage, STR, enhancement unchanged. The user vetoed doubling ALL damage: "It is WAY too easy to stack damage on this build."

**The Price — Will Save Each Round:**

| Overburn Round | DC |
|----------------|-----|
| 1 | 14 |
| 2 | 17 |
| 3 | 21 |
| 4 | 26 |
| 5 | 32 |
| 6+ | +7/round |

**WHY this curve:** DC starts EASY on purpose. Round 1 should feel safe — the player is supposed to try. Hockey-stick escalation means rounds 1-2 are approachable, round 3 is gambling, round 4+ is "you learn." At level 1 (~+2 Will), the player pushes, gets doubled empyreal, feels great — fails on round 2-3, Zarathos surges, lesson remembered forever. The original proposal (DC 15+N) was rejected because it was too easy at high levels and insufficiently scary at low levels.

**The Tax:** 1d6 unpreventable damage per round regardless of save. Cannot be reduced or healed while transformed.

**Medallion Pressure:** +1 to DC per soul stored in the Medallion. Full Medallion = more dangerous overburn.

**At level 19 (Unbound):** Overburn no longer triggers surge. At level 20: unlimited rounds.

---

## 4. Heaven's Brand

**Type:** Supernatural (Su). Active on ALL attacks while transformed.

| Level | Bonus | Avg |
|-------|-------|-----|
| 1-4 | +1d4 | 2.5 |
| 5-9 | +1d4 | 2.5 |
| 10-14 | +2d4 | 5.0 |
| 15-19 | +3d4 | 7.5 |
| 20 | +4d4 | 10.0 |

**WHY all d4s:** KISS. One die type. "How many d4s?" Overburn doubling is trivial math. The user explicitly vetoed the original faster curve (which used d6s) because it gave MORE damage at mid-levels when the class was already considered overpowered. This version is LOWER than the old at every tier past level 4. Max at 20 is 16 (avg 10) vs old max 24 (avg 14). Deliberately conservative because multiple damage sources stack.

In overburn: dice doubled (1d4→2d4, etc.).

---

## 5. Empyreal Descriptor

Hellfire is empyreal — divine judgment fire from the Empyrean. Not holy. Not unholy. Third category. Confirmed by canon: Ghost Rider wielded the Sword of Uri-El (archangel's blade) unharmed because hellfire and sacred fire are the same energy.

Bypasses: fire resistance/immunity, holy resistance/immunity, unholy resistance/immunity, general energy resistance.
Immune targets: true constructs (no soul), genuinely innocent (nothing to judge), soulless beings (Centurious-type — Ghost Rider's hard counter).

**WHY this matters:** The empyreal bypass is what makes the class's lower raw damage viable. A Fighter does 49 avg at 20. The Host does 42 — but against fire-resistant demons, those 42 all get through. Against soulless targets, empyreal does NOTHING — meaningful weakness.

---

## 6. Burning Judgment Eyes / Sin Sight

**Level 1 — Burning Judgment Eyes:** Always active, even in Host form. Detect evil at will, 60 ft. Cannot be dispelled or suppressed. Eyes glow orange-black.

**Level 3 — Sin Sight:** Upgrade. Perceives specific acts of harm, not alignment. A LG knight who burned a village glows with that village. A CE demon who never harmed an innocent glows dimly. Reads GUILT, not alignment.

**WHY Sin Sight is foundational:** It's the sensor that feeds every other system. Existential Dread affects "the guilty." Penance only works on creatures that have committed evil acts. Medallion harvests evil souls. Sin Sight determines who qualifies. The distinction between "evil-aligned" and "the guilty" was deliberate — Ghost Rider cares about what you've DONE, not what you ARE.

---

## 7. Existential Dread

**Type:** Supernatural (Su). Passive aura while transformed. Soul-based, NOT mind-affecting, NOT fear.

**WHAT IT DOES NOW:** Allies within aura gain **+1 to saves and DCs** against abilities used by **the guilty.** Scales to +2 at level 13. Against "no save" abilities from the guilty, nat-20 still saves.

**Plus atmospheric flavor (no mechanics):** Plants wilt, water steams, candles die, animals flee.

**Radius:** 15 ft. at 2, 30 at 5, 40 at 9, 50 at 13, 60 at 17.

**DESIGN HISTORY:** The original CR 19 stat block had a full 7-tier system with specific fail/success effects per Soul Awareness Tier. The user's conceptual breakthrough: "Ghost Rider doesn't induce fear, he induces existential dread — higher awareness = WORSE effect." For the leveling class, we removed ALL fear conditions (Penance handles fear) and made it a party buff. The user wanted to avoid making the Host a solo wrecking ball — a party buff makes the Host a force multiplier that other players WANT on the field.

The full 7-tier system is preserved in the CR 19/26 stat blocks for NPC use.

---

## 8. Penance Progression

**DC:** 10 + 1/2 class level + CHA mod. **Uses/day:** 3 + CHA mod. Only works on souled creatures that have committed evil acts.

| Level | Name | Fail | Success |
|-------|------|------|---------|
| 3 | Penance Glare | Shaken 1d4 rds | Uneasy (no effect) |
| 7 | Penance Gaze | Frightened 1d4 rds | Shaken 1 rd |
| 10 | Penance Stare | Panicked 1d4 rds + 1d2 Wis | Shaken 1d4 rds |
| 15 | Greater Stare | Paralyzed 1 rd + 1d4 Wis/rd | Shaken 1d4 rds + 1 Wis flat |
| 17 | Penance Lock | As Greater, cannot break eye contact | — |

**DESIGN HISTORY:** The CR 19 version uses flat DC 40, 4d4 Wis/round, derived from exhaustive math across 8 packages and 9 target tiers (see penance-stare-design-reference.md). DC 40 doesn't work for a leveling class — a level 10 Host gets maybe DC 18. The progression tells a story: at 3, "I can scare you." At 15, "I can break your mind." At 17, "And you can't look away."

Penance Lock: only physical intervention or Host's choice ends it. The nat-20 escape hatch from Existential Dread does NOT apply to the Host's own Lock.

**Penance → Medallion:** At Wis 0, soul auto-absorbed by Medallion if space available.

---

## 9. The Hellfire Chain

Manifests on transformation. Dismissed as free action. **Bonus weapon** — Host's normal weapons still work. Proficiency inherent (divine office).

| Level | Enhancement | Properties |
|-------|------------|------------|
| 1-6 | +1 | Empyreal (via Heaven's Brand) |
| 7-10 | +2 | Flaming (+1d6 empyreal) |
| 11-14 | +3 | Flaming burst |
| 15-18 | +4 | 20 ft. reach (swift action) |
| 19-20 | +5 | Anarchic flaming burst |

**Soul Binding (level 8, requires Medallion):** On confirmed crit, Fort save (DC 10 + 1/2 level + STR) or no magical movement for 1d4 rounds. Binds the soul, not the body. Canon: the chain prevents extradimensional escape.

---

## 10. Hellfire Breath

Level 6. Standard action, 15 ft. cone, 1d6 empyreal per 2 levels, Ref half (DC 10 + 1/2 level + CON), 3/day. CON-based DC (not CHA) because it's physical fire, not judgment.

---

## 11. Hellfire Backlash

**Passive defensive ability.** No action. No uses/day. Any creature that strikes the Host (or mount at 18+) with melee/natural/grapple/touch/bull rush takes empyreal damage. No save.

| Level | Damage | Covers |
|-------|--------|--------|
| 12-14 | 1d4 | Host only |
| 15-17 | 2d4 | Host only |
| 18-19 | 3d4 | Host and mount |
| 20 | 2d6 | Host and mount |

**DESIGN HISTORY:** Originally "Brimstone Rebuke" (immediate action, CON/day). Made passive per user request. Originally the mount had an offensive wreath (2d6 empyreal on mount attacks) but this broke Griffon pounce stacking (3 attacks × 2d6 = 6d6 free empyreal/round from mount). User directed: "Make the entire ability defensive, not just at level 20." Mount's own attacks deal normal damage only — no empyreal on attacks. The mount is on fire; things that HIT it get burned. It doesn't channel judgment through its claws.

**Canon:** Wolverine clawed Ghost Rider's face. Hellfire backfired. He didn't try that again.

---

## 12. Contract Immunity

Level 7. Hard narrative rule — no numbers, no saves.

The bond is sealed by the highest divine authority in the setting. The contract cannot be altered or broken by anyone short of that authority. The Host cannot be forced to harm innocents — reality intervenes if necessary, entropy retaliates against the schemer. The Host CAN be tricked about facts (who is innocent, what's really happening). Protects nature, not knowledge.

**WHY no numbers:** The user cut the original three-layer mechanical system (+8 Will, -10 manipulation penalty, hard rule) down to just the hard rule. "Nothing else is canon. Once the contract is sealed, that's it."

---

## 13. The Medallion of Power

**Physical form:** Adapts to Host — gas cap, pendant, brand, coin. GM can introduce at any level. **Soul storage activates at level 8.**

**Capacity:** 3 (level 8), 5 (12), 7 (16), 10 (20).

**Harvest:** Swift action on evil kill while transformed. Penance auto-feeds at 0 Wis.

**Passive:** Sacred AC bonus by Medallion tier: +2 (L8), +3 (L12), +4 (L16), +5 (L20). Granted when Medallion is at capacity. Even at maximum (+5 at L20), Host AC reaches Fighter/Paladin parity — never far above it. Defense must be earned by killing evil.

**Active Spends (immediate action, soul released to afterlife):**

| Cost | Name | Effect |
|------|------|--------|
| 1 | Deny the Reaper | Reroll failed save |
| 1 | Soulshield | Temp HP = 2× level |
| 1 | Soul Deflection | Negate confirmed crit |
| 1 | Hellfire Retort | Next attack +2d6 empyreal |
| 1 | Shatter Binding | End compulsion/charm/possession on self or adjacent ally |
| 2 | Cheat Death | At 0 HP, drop to 1 HP. Does NOT trigger Zarathos surge. |

**THE TENSION:** Every spend drops passive AC. Cheat Death (2 souls) is insurance against auto-surge on 0 HP — players want to hoard it but also need Deny the Reaper and Soulshield in crises. Constant resource agonizing.

**Zarathos Pressure:** +1 to overburn/surge DCs per soul stored. **Capacity Trigger:** At maximum soul capacity, Will save each round of combat: DC 15 + current Medallion AC bonus. Spending below capacity removes the trigger. **On surge: Zarathos empties the Medallion.** All souls consumed. All bonuses gone.

**Durability:** Suppressible by Dispel/Antimagic (dormant until suppression ends). Breakable by artifact-level force (Zarathos repairs in 1d4 days). Not permanently destroyable short of divine intervention.

**Full canon research** in medallion-of-power-research.md. The Medallion in canon is a transformation catalyst (bridge between mortal and Spirit), not a stat stick. All mechanical effects here are homebrew extrapolation.

---

## 14. Soul Interrogation

Level 10. Standard action, burn 1 Medallion soul. Flash of creature's sins/knowledge/memories. Learn: alignment, greatest sin/virtue, one specific piece of knowledge (player asks, DM answers), whether creature served a greater evil (directional sense toward master). Soul energy spent, soul passes to final destination. 1/day at 10, 2/day at 14, 3/day at 18.

**Replaced "Soul Reading" (touch corpse)** which had no basis — soul is gone, nothing to read.

---

## 15. The Infernal Steed

Our upgrades **stack with** the base mount/vehicle's existing abilities. If the player chose a Griffon, it keeps fly/pounce. If they chose the 3PP motorcycle, it keeps Thundering Crash.

| Level | Name | Change |
|-------|------|--------|
| 3 | The Turning | No food/fuel/rest. Never tires. Mechanically impossible. |
| 8 | The Quickening | +20 ft. speed. Water/walls 1 round. |
| 14 | The Burning | **Hellfire Leap:** Jump up to 10× move speed, move action, no check. Vertical = half horizontal. No fall damage. |
| 20 | The Unchaining | Leap unlimited (DM discretion). Water/walls indefinitely. Dimension door 1/day. |

**NO FLIGHT.** User explicitly removed it: "Not canon anyway. Give them an eyebrow raising jump ability." Also fixed Griffon pounce stacking — can't pounce off a jump.

**Stacking verified:** Griffon + Quickening = 100 ft. fly (matches Hippogriff baseline, not unprecedented). Motorcycle + Leap at 14 = 1,200 ft. jump (charge damage ~51, under Cavalier Spirited Charge benchmark ~60). Mid-air attacks require Spring Attack feat (one attack only). All checked.

---

## 16. Zarathos Surge

**DM takes full control.** No stat block. No numbers. The user directed: "He's the big brother of all demon lords, empyreal lords, and Great Old Ones. He can open any size can of whoop-ass. He IS Justice incarnate." Zarathos is as strong as the scene requires.

**Triggers:**

| Trigger | Save |
|---------|------|
| 0 HP while transformed | Automatic (Cheat Death prevents) |
| Overburn | Will (escalating, section 3) |
| d100 entry #1 | Automatic, 1 round |
| Overwhelming evil / trauma | Will DC 22 + souls stored |
| Medallion at max capacity | Will DC 15 + Medallion AC bonus, each round |

**Nat-1 accumulation counter was KILLED.** Math doesn't work with only 6-8 rounds of transformation. The d100 table handles nat-1 consequences.

**Aftermath:** Exhausted 10 min, can't transform 1 hour, Medallion emptied (all souls consumed by Zarathos), all overburn damage hits at once.

---

## 17. Hellfire Instability

d100 wild magic table. Triggers on nat-1 or nat-20 while transformed (nat-20 stops at 20). Table shrinks with level: 100 entries at 1-4, 80 at 5-8, 60 at 9-12, 40 at 13-16, 20 at 17-19, d20 only at 20. Ranges: 1-20 (Zarathos/disruptive), 21-40 (chaotic), 41-60 (helpful), 61-80 (weird), 81-100 (cosmetic). Full table in guidebook.

---

## 18. Bonus Feats

At levels 2, 5, 9, 12, 15, 18 from combat feat list. Standard prerequisites. The Host picks.

---

## 19. Multiclassing

Open. No restrictions. Class is naturally dip-resistant — all power lives in scaling. A 1-3 dip gets detect evil, 3-5 rounds of minor buffs, +1d4 empyreal. No Medallion (requires level 8). No meaningful Penance. No chain scaling.

---

## 20. Capstones

**Level 19 — Unbound:** Overburn doesn't trigger surge. Free action transform, no save to revert. Immunity to ability damage/drain while transformed.

**Level 20 — Spirit Unchained:** Unlimited transformation. Voluntary surge = shared DM/player control. Instability on nat-1 only. Type → Outsider (native). Backlash 2d6 covers Host and mount. Leap unlimited. Medallion cap 10.

---

## 21. Class Progression Table

| Lvl | BAB | Fort | Ref | Will | Special |
|-----|-----|------|-----|------|---------|
| 1 | +1 | +2 | +0 | +2 | Rider's Mantle, Burning Judgment Eyes, Hellfire Chain (+1), Heaven's Brand (1d4), Circus Refugee, Hellfire Instability |
| 2 | +2 | +3 | +0 | +3 | Existential Dread (15 ft.), Bonus Feat |
| 3 | +3 | +3 | +1 | +3 | Sin Sight, Penance Glare, The Turning (mount) |
| 4 | +4 | +4 | +1 | +4 | Rider's Mantle (+4/+4/+2) |
| 5 | +5 | +4 | +1 | +4 | Existential Dread (30 ft.), Bonus Feat |
| 6 | +6/+1 | +5 | +2 | +5 | Hellfire Breath |
| 7 | +7/+2 | +5 | +2 | +5 | Hellfire Chain (+2, flaming), Contract Immunity, Penance Gaze |
| 8 | +8/+3 | +6 | +2 | +6 | Medallion of Power (3 souls), The Quickening (mount), Soul Binding (chain crit) |
| 9 | +9/+4 | +6 | +3 | +6 | Existential Dread (40 ft.), Bonus Feat |
| 10 | +10/+5 | +7 | +3 | +7 | Penance Stare, Soul Interrogation (1/day), Heaven's Brand (2d4) |
| 11 | +11/+6/+1 | +7 | +3 | +7 | Rider's Mantle (+6/+6/+3), Hellfire Chain (+3, flaming burst) |
| 12 | +12/+7/+2 | +8 | +4 | +8 | Hellfire Backlash (1d4), Medallion (5 souls), Bonus Feat |
| 13 | +13/+8/+3 | +8 | +4 | +8 | Existential Dread (50 ft., +2 allies) |
| 14 | +14/+9/+4 | +9 | +4 | +9 | Soul Interrogation (2/day), The Burning (Hellfire Leap) |
| 15 | +15/+10/+5 | +9 | +5 | +9 | Chain (+4, 20 ft. reach), Greater Stare, Heaven's Brand (3d4), Backlash (2d4), Bonus Feat |
| 16 | +16/+11/+6/+1 | +10 | +5 | +10 | Rider's Mantle (+8/+8/+4), Medallion (7 souls) |
| 17 | +17/+12/+7/+2 | +10 | +5 | +10 | Existential Dread (60 ft.), Penance Lock |
| 18 | +18/+13/+8/+3 | +11 | +6 | +11 | Backlash (3d4, covers mount), Soul Interrogation (3/day), Bonus Feat |
| 19 | +19/+14/+9/+4 | +11 | +6 | +11 | Chain (+5, anarchic flaming burst), Unbound |
| 20 | +20/+15/+10/+5 | +12 | +6 | +12 | Spirit Unchained, Mantle (at-will), Brand (4d4), Backlash (2d6), Medallion (10), Unchaining (mount) |

---

## 22. Damage Parity

**Design intent:** Host should be slightly BELOW fighter baseline. Empyreal bypass closes gap vs resistant targets. Overburn exceeds briefly at risk. Power budget is spread across transformation, aura, Penance, Medallion, mount — NOT concentrated in damage. This is a narrative pressure system that also hits things.

| Level | Fighter | SoV | Notes |
|-------|---------|-----|-------|
| 5 | ~20 | ~18 | Behind. Bypass compensates. |
| 10 | ~32 | ~28 | Behind. Chain utility compensates. |
| 15 | ~41 | ~36 | Behind. Overburn available for burst. |
| 20 | ~49 | ~42 | Behind. Capstone + bypass compensates. |

In overburn at 15: ~43 (briefly exceeds Fighter, at surge risk + 1d6/round).

---

## 23. Key Design Principles

1. **Ghost Rider is a narrative pressure system, not a combat optimizer.** Aura transforms every scene before dice roll.
2. **Zarathos bribes, not threatens.** Temptation mechanics offer power; punishment comes from accepting too much.
3. **Higher awareness = worse effect.** Core inversion of standard fear mechanics.
4. **The guilty, not the evil.** Sin Sight reads acts, not alignment.
5. **Defense must be earned.** Medallion AC requires killing evil and banking souls.
6. **Other players matter.** Existential Dread is a party buff, not a personal debuff aura.
7. **Start low, scale slow.** d4s not d6s. Conservative progression. Multiple modest sources.
8. **DM is Zarathos.** Hand the sheet over on surge. No stat block.
9. **Mount is defensive, not offensive.** Backlash covers mount; no empyreal on mount attacks. Jump not fly.
10. **Canon names, always.** Hellfire Chain, Hellcycle, Penance Stare, Zarathos, empyreal.

---

## 24. Rejected Alternatives — DO NOT REINTRODUCE

1. **Nat-1 accumulation counter** — Math doesn't work with 6-8 transformation rounds.
2. **Soul Reading (touch corpse)** — Soul is gone, nothing to read. Replaced by Soul Interrogation.
3. **Flight on mount** — Not canon. Broke Griffon stacking. Replaced by Hellfire Leap.
4. **Offensive mount wreath** — Griffon pounce + 2d6/attack = 6d6 free/round. Replaced by defensive Backlash.
5. **Medallion granting DR/SR/Channel Resistance** — No canon basis. All fabricated. Replaced by soul-battery AC.
6. **Mechanical Contract Immunity (+8 Will, -10 penalty)** — Cut to hard narrative rule.
7. **Brimstone Rebuke (immediate action, CON/day)** — Merged into passive Hellfire Backlash.
8. **"Class level only" multiclass restriction** — Unnecessary; class is naturally dip-resistant.
9. **Fear effects on the aura** — Penance handles fear. Aura is party buff + flavor.
10. **Double ALL damage in overburn** — Only empyreal doubled. Too easy to stack otherwise.

---

## 25. Scaling Audit — PENDING

- [ ] Action economy at 5/10/15/20 — what competes for standard action?
- [ ] Penance DC vs expected enemy Will saves at each tier
- [ ] Medallion soul pressure vs surge frequency at mid-levels
- [ ] Overburn risk curve per level
- [ ] Steed stacking final verification
- [ ] Total AC with/without Medallion vs expected attack bonuses
- [ ] Feat tax — enough feats for melee + class features?
- [ ] Party role overlap vs Fighter/Paladin/Barbarian/Cavalier
- [ ] Level 1-3 survivability with 3 rounds and paper AC
- [ ] Overburn + Medallion compound risk at mid-levels
