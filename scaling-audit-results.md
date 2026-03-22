# Spirit of Vengeance — Scaling Audit Results

**Auditor:** Claude Opus 4.6
**Date:** March 20, 2026
**Source Documents:** spirit-of-vengeance-design-notes.md (sections 1–25), penance-stare-design-reference.md, existential-dread-mechanic.md
**Authoritative Table:** Design notes section 21 (class progression)
**Design Principles Tiebreaker:** Section 23

---

## EXECUTIVE SUMMARY

| # | Check | Verdict |
|---|-------|---------|
| 1 | Action Economy | **WATCH** |
| 2 | Penance DC vs Enemy Will | **WATCH** |
| 3 | Medallion Soul Pressure vs Surge Frequency | **REVISED** |
| 4 | Overburn Risk Curve | **PASS** |
| 5 | Steed Stacking | **PASS** |
| 6 | AC at Each Tier | **REVISED** |
| 7 | Feat Tax | **PASS** |
| 8 | Party Role Overlap | **PASS** |
| 9 | Level 1–3 Survivability | **PASS** |
| 10 | Compound Risk: Overburn + Full Medallion | **REVISED** |

**Bottom line:** No outright failures. Four items warrant monitoring or table guidance. The hockey-stick overburn curve, feat budget, and steed stacking all check out clean. Penance DC falls behind at high levels (by design, margin is tight). The original Medallion AC and capacity-trigger math was broken — **revised and locked during this audit** (see Addendum A). Two guidebook sidebars recommended.

---

## GLOBAL ASSUMPTIONS

All checks use the following baseline Host unless stated otherwise:

| Property | L1 | L5 | L10 | L15 | L20 |
|----------|----|----|-----|-----|-----|
| CHA | 16 (+3) | 17 (+3) | 18 (+4) | 19 (+4) | 20 (+5) |
| STR (base) | 16 (+3) | 16 (+3) | 17 (+3) | 18 (+4) | 18 (+4) |
| CON (base) | 13 (+1) | 13 (+1) | 14 (+2) | 14 (+2) | 14 (+2) |
| WIS | 10 (+0) | 10 (+0) | 10 (+0) | 10 (+0) | 10 (+0) |
| DEX | 14 (+2) | 14 (+2) | 14 (+2) | 14 (+2) | 14 (+2) |

CHA increases at levels 4, 8, 12, 16. STR bumped at 12, 20. CON bumped at 8. Human, standard point buy.

**Will save (base only):** Fort and Will are good saves.

| Level | Base Will | WIS Mod | Total |
|-------|-----------|---------|-------|
| 1 | +2 | +0 | **+2** |
| 5 | +4 | +0 | **+4** |
| 10 | +7 | +0 | **+7** |
| 12 | +8 | +0 | **+8** |
| 15 | +9 | +0 | **+9** |
| 20 | +12 | +0 | **+12** |

**Transformation rounds/day** (design notes section 2: CHA mod + class level):

| Level | CHA Mod | Class Level | Total |
|-------|---------|-------------|-------|
| 1 | +3 | 1 | **4** |
| 5 | +3 | 5 | **8** |
| 10 | +4 | 10 | **14** |
| 15 | +4 | 15 | **19** |
| 20 | — | — | **Unlimited** |

---

## CHECK 1: ACTION ECONOMY

### Verdict: **WATCH**

**Method:** At each breakpoint, list every ability by action type, then simulate a 3-round and 6-round combat to check for priority conflicts.

### Action Catalog

**Level 1** (4 rounds available)

| Action Type | Abilities |
|-------------|-----------|
| Free | Transform (Rider's Mantle), end transformation |
| Standard | Full attack, Hellfire Chain attack |
| Move | Move |
| Swift | — |
| Immediate | — |
| Passive/Always-on | Burning Judgment Eyes (detect evil), Heaven's Brand (+1d4 on all attacks) |

No conflicts. One standard action per round = attack. Clean.

**Level 5** (8 rounds)

| Action Type | Abilities |
|-------------|-----------|
| Free | Transform/end |
| Standard | Full attack, Penance Glare (gained L3) |
| Move | Move |
| Swift | — |
| Immediate | — |
| Passive | Burning Eyes, Sin Sight, Heaven's Brand (+1d4), Existential Dread (30 ft., party buff) |

**Conflict:** Penance Glare competes with attack for standard action. At only 3 + CHA mod uses/day (= 6 uses), the Host won't spam it. In a 3-round fight: transform (free), attack round 1, Glare round 2 (trades damage for shaken condition enabling Cornugon Smash chain), attack round 3. Workable but tight — the Glare-into-melee flow requires the player to plan one round ahead.

**Level 10** (14 rounds)

| Action Type | Abilities |
|-------------|-----------|
| Free | Transform/end, dismiss chain |
| Standard | Full attack, Penance Stare, Hellfire Breath (3/day), Soul Interrogation (1/day) |
| Move | Move, mount/dismount |
| Swift | Medallion harvest (evil kill while transformed), chain reach toggle (L15, not yet) |
| Immediate | Medallion spends: Deny the Reaper, Soulshield, Soul Deflection, Hellfire Retort, Shatter Binding |

**Conflict:** Four abilities compete for standard action. Full attack vs Penance Stare vs Hellfire Breath vs Soul Interrogation. In practice, Soul Interrogation is out-of-combat. Hellfire Breath is 3/day AoE for opening rounds or clusters. Penance Stare is the finisher for high-value targets. Full attack is the default. The flow works: Breath → full attacks → Stare on the boss when you've softened the field. The Medallion spends are all immediate actions and never conflict with anything.

**Level 15** (19 rounds)

Same as L10 plus: Greater Stare (standard), chain reach toggle (swift), Hellfire Leap (move action on mount), Backlash (passive).

**Conflict:** Swift action competition emerges: chain reach toggle vs Medallion harvest. Both are swift. In a given round, you either extend reach OR bank a soul. Not both. This is the first real swift-action crunch.

**Level 20** (unlimited)

Same as L15 plus: Backlash covers mount, Medallion cap 10, dimension door on mount 1/day.

Swift crunch persists but is manageable — reach toggle is once per combat (set it and leave it), so it only conflicts on the round you toggle.

### Level 1 Spotlight: Can the Host Use Their Kit in 3–6 Rounds?

4 rounds available. Kit at L1: Hellfire Chain (+1, 2d4+STR+1d4 empyreal), transform as free action. That's it — no Penance, no Breath, no Medallion. Every round is "move and attack" or "full attack." No priority conflicts because there's nothing to conflict with. The design is clean here by being minimal.

**3-round fight:** Transform (free), move+attack, full attack, full attack. 3 full rounds of output. Fine.

**6-round fight at L1:** Only 4 rounds of transformation. Rounds 5–6 are either overburn (with doubled empyreal = 2d4) or fighting as the untransformed Host with a MW weapon and no empyreal. This is a real problem — see Check 9.

### Assessment

Levels 1–9: Action economy is clean. Only one standard-action ability competes at a time, and the competition is a meaningful tactical choice (attack vs Glare/Stare/Breath), not a frustrating bottleneck.

Level 10+: The Medallion immediate actions are brilliantly designed — they never conflict with the action economy because they're reactive spends. The only crunch is the swift action at 15+ (reach toggle vs harvest), which is minor and only conflicts on the toggle round.

No standard-action logjam at any level. The class stays playable round-to-round.

**WATCH** because the level 1–3 round budget is so tight that a 6-round fight forces difficult choices (see Check 9), not because the action types themselves conflict.

---

## CHECK 2: PENANCE DC VS ENEMY WILL

### Verdict: **WATCH**

**Penance DC = 10 + 1/2 class level + CHA mod:**

| Level | Ability | DC | Derivation |
|-------|---------|-----|------------|
| 3 | Glare | 14 | 10 + 1 + 3 |
| 5 | Glare | 15 | 10 + 2 + 3 |
| 7 | Gaze | 16 | 10 + 3 + 3 |
| 10 | Stare | 19 | 10 + 5 + 4 |
| 15 | Greater | 21 | 10 + 7 + 4 |
| 17 | Lock | 22 | 10 + 8 + 4 |
| 20 | Lock | 25 | 10 + 10 + 5 |

**Expected enemy Will saves at CR = level (PF1E Bestiary averages):**

| CR | Low Will (martial) | Med Will (balanced) | High Will (caster) |
|----|--------------------|---------------------|---------------------|
| 3 | +1 | +3 | +5 |
| 5 | +2 | +4 | +7 |
| 10 | +4 | +8 | +13 |
| 15 | +7 | +12 | +18 |
| 20 | +10 | +16 | +24 |

**Fail rates (P(fail) = clamp(DC − Will − 1, 1, 19) / 20):**

| Level | DC | vs Low Will | vs Med Will | vs High Will |
|-------|-----|------------|------------|-------------|
| 3 | 14 | 60% (+1→12/20) | 50% (+3→10/20) | 40% (+5→8/20) |
| 5 | 15 | 60% (+2→12/20) | 50% (+4→10/20) | 35% (+7→7/20) |
| 10 | 19 | 70% (+4→14/20) | 50% (+8→10/20) | 25% (+13→5/20) |
| 15 | 21 | 65% (+7→13/20) | 40% (+12→8/20) | 10% (+18→2/20) |
| 20 | 25 | 70% (+10→14/20) | 40% (+16→8/20) | 5% (+24→nat-1) |

### Analysis

**Level 3 Glare vs CR 3:** At DC 14, a CR 3 martial enemy (+1 Will) fails 60% of the time. A balanced enemy fails 50%. The Glare IS scary to a CR 3 enemy. **Fine.**

**Level 10 Stare vs CR 10:** DC 19 vs a balanced CR 10 enemy (+8 Will) = 50% fail. Against a high-Will caster (+13) = 25%. The Stare is meaningful against martial targets, unreliable against casters. At this tier, the Stare's fail effect is Panicked 1d4 rounds + 1d2 Wis damage — when it lands, it's devastating. The 25% rate against casters means roughly 1 in 4 attempts sticks, which is appropriate for a save-or-suck ability. **Fine.**

**Level 15 Greater Stare vs CR 15:** DC 21 vs a high-Will outsider (+18) = 10% fail. The Greater Stare (Paralyzed 1 rd + 1d4 Wis/rd) almost never lands against a CR 15 caster/outsider. Against balanced enemies (+12) = 40% fail. Against martials (+7) = 65%.

This is the pressure point. A CR 15 outsider with good Will saves the Greater Stare 90% of the time. The success effect (Shaken 1d4 rounds + 1 Wis flat) is still meaningful — shaken feeds Cornugon Smash → Shatter Defenses, and 1 Wis per round of maintained stare adds up. But the paralysis/heavy-Wis-damage path is unlikely against the targets the player most wants to use it on.

**Level 20 Lock vs CR 20:** DC 25 vs +24 Will = nat-1 only (5%). The Penance Lock's true power at this level is the success effect — Shaken + 1 Wis flat per round, compounding over many rounds because the Lock can't be broken. Against a CR 20 outsider with Wis 26, 1 Wis/round takes 26 rounds to catatonic. That's a LONG fight, but the shaken condition and the Cornugon Smash chain are doing work every round.

### Assessment

The DC curve is intentionally behind (design notes section 8: "DC 40 doesn't work for a leveling class"). The progression tells the right story — scary at low levels, a tactical choice at mid-levels, and at high levels the success effects carry the ability while the fail effects become rare jackpots.

**WATCH** because at level 15–20, the primary Penance effects (Paralyzed, heavy Wis damage) rarely land against level-appropriate high-Will enemies. The class depends on the success effects + fear chain synergy (Shatter Defenses making targets flat-footed) to stay relevant. If a DM is running lots of outsiders with Wis 20+ and good Will saves, the Host's signature ability looks weak on paper. The player needs to understand that maintaining the Stare for the success-damage grind is the intended high-level gameplay, not fishing for the fail.

No fix proposed — this is by design (section 23, principle 7: "Start low, scale slow") and the success effects are the intended high-level workhorse. But consider a sidebar in the guidebook explaining this to players: *"At high levels, the Penance Stare is a siege weapon, not a kill shot. Hold the stare. Grind the Wisdom."*

---

## CHECK 3: MEDALLION SOUL PRESSURE VS SURGE FREQUENCY

### Verdict: **PASS**

**Setup at level 10, 3 stored souls:**

Overburn round 1 base DC = 14. Medallion adds +3 (1 per soul). Effective DC = **17**.
Host Will = +7. Needs 10+ on d20 = **55% success rate.**

Overburn round 2 DC = 17 + 3 = **20**. Needs 13+ = **40% success.**
Overburn round 3 DC = 21 + 3 = **24**. Needs 17+ = **20% success.**

That's a reasonable pressure curve. Round 1 is a coinflip leaning safe. Round 2 is a gamble. Round 3 is dangerous. With 3 souls, the Medallion shifts the curve about 1 round earlier into danger territory compared to an empty Medallion.

**Setup at level 12, 5 stored souls (Medallion at capacity):**

Overburn round 1 DC = 14 + 5 = **19**. Host Will = +8. Needs 11+ = **50% success.**

But here the Medallion-at-capacity surge trigger (section 16) also fires: Will DC 20 + 5 = **25** each round of combat. Host needs 17+ = **20% success per round.**

This is two separate saves per round when in overburn with a full Medallion. The chance of passing BOTH on a given round = 0.50 × 0.20 = **10%.** Surge is almost guaranteed within 1–2 rounds.

However: the Medallion-at-capacity trigger fires during ALL combat rounds while full, not just overburn. During normal transformation with a full Medallion at level 12: DC 25 Will, +8 save, 20% success per round. Over 3 rounds: P(no surge) = 0.20³ = **0.8%.** The Host will almost certainly surge within 3 rounds of combat if the Medallion is full.

### Is this too much pressure?

No. This is the intended tension (section 13): "Every spend drops passive AC. Cheat Death is insurance against auto-surge on 0 HP — players want to hoard it but also need Deny the Reaper and Soulshield in crises. Constant resource agonizing."

A smart player at level 12 with 5 souls either:
1. Spends a soul before combat starts to drop below capacity (loses +1 AC, gains breathing room), or
2. Accepts the surge risk and plans to spend souls reactively during combat (each spend reduces the DC by 1 AND brings them below capacity, killing the trigger), or
3. Uses the souls aggressively in the first round (Hellfire Retort + Soulshield) to drop to 3 and remove the capacity trigger entirely.

The system forces the player to USE the souls rather than hoard them passively — which is exactly what design principle 2 says: "Zarathos bribes, not threatens. Temptation mechanics offer power; punishment comes from accepting too much."

**PASS.** The math is aggressive but the escape hatches (spend souls to reduce pressure) are built into the system. The player who hoards all souls and then enters combat SHOULD feel the squeeze.

---

## CHECK 4: OVERBURN RISK CURVE

### Verdict: **PASS**

**Overburn DC table (section 3):**
Round 1: 14 | Round 2: 17 | Round 3: 21 | Round 4: 26 | Round 5: 32 | Round 6+: +7/round

Add +1 per Medallion soul stored. Also 1d6 untyped damage per overburn round regardless of save.

**Safe zone / Gambling zone / Suicide zone by level:**

"Safe" = >60% success rate. "Gambling" = 30–60%. "Suicide" = <30% (or DC exceeds save+19 = auto-fail on anything but nat-20... actually no, PF1E natural 20 always succeeds on saves).

Wait — PF1E: a natural 20 on a saving throw is always a success. So "auto-fail territory" doesn't exist for saves. The worst case is always 5% success (nat-20). I'll define zones as:
- **Safe:** >50% success
- **Gambling:** 20–50% success
- **Suicide:** <20% success (relying on nat-20 territory)

**With 0 Medallion souls:**

| Level (Will) | Round 1 (DC 14) | Round 2 (DC 17) | Round 3 (DC 21) | Round 4 (DC 26) | Round 5 (DC 32) |
|---|---|---|---|---|---|
| L1 (+2) | Need 12 → 45% (**Gamble**) | Need 15 → 30% (**Gamble**) | Need 19 → 10% (**Suicide**) | Auto nat-20 → 5% (**Suicide**) | 5% |
| L5 (+4) | Need 10 → 55% (**Safe**) | Need 13 → 40% (**Gamble**) | Need 17 → 20% (**Gamble**) | Need 22 → 5% (**Suicide**) | 5% |
| L10 (+7) | Need 7 → 70% (**Safe**) | Need 10 → 55% (**Safe**) | Need 14 → 35% (**Gamble**) | Need 19 → 10% (**Suicide**) | 5% |
| L15 (+9) | Need 5 → 80% (**Safe**) | Need 8 → 65% (**Safe**) | Need 12 → 45% (**Gamble**) | Need 17 → 20% (**Gamble**) | 5% |
| L20 (+12) | Need 2 → 95% (**Safe**) | Need 5 → 80% (**Safe**) | Need 9 → 60% (**Safe**) | Need 14 → 35% (**Gamble**) | Need 20 → 5% (**Suicide**) |

**Summary by level:**

| Level | Safe Rounds | Gambling Rounds | Suicide Starts At |
|-------|-------------|-----------------|-------------------|
| 1 | 0 | 1–2 | 3 |
| 5 | 1 | 2–3 | 4 |
| 10 | 1–2 | 3 | 4 |
| 15 | 1–2 | 3–4 | 5 |
| 20 | 1–3 | 4 | 5 |

The hockey-stick works perfectly. At every level, the player gets 1–3 "it'll probably be fine" rounds, 1–2 "this is a gamble" rounds, and then a cliff. The level 1 player pushing into overburn hits gambling on round 1 and suicide on round 3 — exactly the "try and screw up, lesson learned" experience the user wanted (section 3).

At level 19 (Unbound): overburn no longer triggers surge. The entire table becomes irrelevant. At level 20: unlimited transformation, no overburn needed. Clean capstone reward.

**PASS.** The curve is aggressive at low levels and generous at high levels, exactly matching design intent. Adding Medallion souls shifts the curve 1–3 rounds earlier, which is additional pressure but not a death spiral (souls can be spent to relieve it — see Check 3).

---

## CHECK 5: STEED STACKING

### Verdict: **PASS**

**Case (a): Griffon + Quickening at Level 8**

Griffon base fly speed: 80 ft. (average maneuverability).
Quickening: +20 ft. speed.
Total: **100 ft. fly (average).**

Benchmark: Hippogriff fly speed = 100 ft. (average). Roc at CR 9 = 80 ft. (average). An Advanced Hippogriff mount = 100 ft.

100 ft. fly at level 8 is on par with a Hippogriff, which is available to a druid's Animal Companion or through Leadership. Not unprecedented. The "can cross water/walls for 1 round" adds utility but doesn't break positioning because it's only 1 round duration — you can sprint across a wall, not camp on it.

**Does it break positioning?** In a typical dungeon or urban encounter, 100 ft. fly allows the Host to reach almost any point on the map in a single move action, leaving a standard action for a single attack (no full attack after moving). This is strong mobility but not broken — a Fly spell (available to arcane casters at level 5) gives 60 ft. fly with good maneuverability at-will for minutes/level. The Griffon rider gives up full attacks for mobility. Trade-off works.

**PASS.**

**Case (b): 3PP Motorcycle + Hellfire Leap at Level 14**

Design notes section 15: "Motorcycle + Leap at 14 = 1,200 ft. jump (charge damage ~51, under Cavalier Spirited Charge benchmark ~60)."

Let me verify: Motorcycle base speed (typical 3PP): ~60 ft. Quickening at 8: +20 ft = 80 ft. Hellfire Leap at 14: jump up to 10× move speed as a move action = 800 ft. (The design notes say 1,200 ft., which assumes a faster motorcycle base of ~120 ft. — I'll use their number since it's verified in the notes.)

**Charge damage at level 14:**
- Hellfire Chain +3: 2d4 + STR (base 18 +6 Mantle = 24, +7 mod) + 3 enhancement = 2d4+10 = 15 avg weapon
- Heaven's Brand: 3d4 = 7.5 avg empyreal
- Power Attack at BAB +14: −4/+8 (two-handed effectively +12): +12 damage
- Total per hit: ~34.5 avg
- Charge: ×2 (lance rules don't apply to chain, so this is only if the 3PP motorcycle has Thundering Crash)

If Thundering Crash doubles damage like Spirited Charge: ~69. Design notes say ~51, which is more conservative (likely not assuming double from Thundering Crash, or using lower STR).

**Cavalier Spirited Charge benchmark at 14:** Cavalier with lance, Spirited Charge (×3), Challenge active, Power Attack. Roughly: 1d8+24 (STR+PA+enhancement) × 3 = ~85 avg + Challenge damage. The ~51–69 range is clearly under this.

**Mid-air attacks:** Design notes confirm: "Mid-air attacks require Spring Attack feat (one attack only)." No full attacks off a Leap. No pounce (explicitly blocked for Griffon stacking, same logic applies).

**PASS.** Verified under Cavalier benchmark. One attack only. The Leap is mobility, not a damage multiplier.

---

## CHECK 6: AC AT EACH TIER

### Verdict: **WATCH**

**AC Calculation (transformed, reasonable WBL gear):**

| Component | L1 | L5 | L10 | L15 | L20 |
|-----------|----|----|-----|-----|-----|
| Base | 10 | 10 | 10 | 10 | 10 |
| Armor (MW chain shirt → +1 chain → +2 mithral BP → +3 mithral BP → +5 mithral BP) | 4 | 5 | 8 | 9 | 11 |
| DEX | +2 | +2 | +3¹ | +3 | +3 |
| Natural Armor (Mantle) | +1 | +2 | +2 | +3 | +4 |
| Amulet of Natural Armor | — | — | +1 | +2 | +3 |
| Ring of Protection | — | — | +1 | +2 | +3 |
| Medallion (sacred, per 2 souls) | — | — | +1 (3 souls) | +2 (5 souls) | +5 (10 souls) |
| **Total** | **17** | **19** | **26** | **31** | **39** |

¹ Mithral breastplate allows +5 max DEX; DEX 14 = +2, so this only reaches +3 if DEX increases. Using +2 at L10 if no DEX increase. Adjusting: L10 = 25, not 26.

Let me redo this more carefully:

| Component | L1 | L5 | L10 | L15 | L20 |
|-----------|----|----|-----|-----|-----|
| Base | 10 | 10 | 10 | 10 | 10 |
| Armor | 4 (MW chain shirt) | 5 (+1 chain shirt) | 7 (+2 mithral BP) | 9 (+3 mithral BP) | 11 (+5 mithral BP) |
| DEX | +2 | +2 | +2 | +2 | +2 |
| Natural (Mantle) | +1 | +2 | +2 | +3 | +4 |
| Amulet NA | — | — | +1 | +2 | +3 |
| Ring of Prot | — | +1 | +1 | +2 | +3 |
| Sacred (Medallion) | — | — | +1 | +2 | +5 |
| **Total** | **17** | **20** | **24** | **30** | **38** |

**Without Medallion souls:**

| Level | AC (no souls) | AC (max souls) | Difference |
|-------|---------------|----------------|------------|
| 1 | 17 | 17 (no Medallion) | 0 |
| 5 | 20 | 20 (no Medallion) | 0 |
| 10 | 23 | 24 (+1) | 1 |
| 15 | 28 | 30 (+2) | 2 |
| 20 | 33 | 38 (+5) | 5 |

**Expected enemy primary attack bonus at CR = level (Bestiary averages):**

| CR | Low Atk | Med Atk | High Atk |
|----|---------|---------|----------|
| 1 | +4 | +6 | +8 |
| 5 | +9 | +12 | +15 |
| 10 | +16 | +20 | +24 |
| 15 | +22 | +27 | +32 |
| 20 | +28 | +33 | +38 |

**Hit rate (enemy needs to roll AC − attack bonus or higher, minimum 2, maximum 20):**

| Level | Host AC | vs Med Atk | Hit Rate | vs High Atk | Hit Rate |
|-------|---------|-----------|----------|-------------|----------|
| 1 | 17 | +6 | Need 11 → 50% | +8 | Need 9 → 60% |
| 5 | 20 | +12 | Need 8 → 65% | +15 | Need 5 → 80% |
| 10 | 24 | +20 | Need 4 → 85% | +24 | Need 2 → 95%² |
| 15 (w/souls) | 30 | +27 | Need 3 → 90% | +32 | Need 2 → 95% |
| 20 (w/souls) | 38 | +33 | Need 5 → 80% | +38 | Need 2 → 95% |

²Actually: if AC=24 and atk=+24, the enemy needs to roll 0 or higher, which means they always hit (even nat-1 only auto-misses on attack rolls). Need AC − atk = 24 − 24 = 0, so they need 0+. Since minimum roll is 1 and nat-1 misses, it's 95%.

### Analysis

The Host gets hit a LOT. At level 5, a median-attack enemy hits 65% of the time. At level 10, 85%. The Medallion helps but doesn't save the Host from being a damage sponge.

**Comparison to peers:**
- Fighter at L15 with full plate +3, Dex 12, Amulet NA +2, Ring +2, Shield +3: 10 + 12 + 1 + 2 + 2 + 5 = **32.** With Dodge, Shield Focus: **34.**
- Paladin at L15 similar but add +4 from CHA to saves (not AC) and Smite Evil for CHA to AC vs target: up to **36** vs evil.
- Spirit of Vengeance at L15 with full Medallion: **30.**

The Host is 2–6 points behind Fighter/Paladin AC. This is by design (section 13: "Even at max, Host AC ~27 stays below Paladin 31 and Fighter 33"). My numbers run slightly higher because I assumed good WBL purchases, but the relative gap is consistent.

**Is it survivable?** The Host has d10 HD + decent CON (augmented by Mantle). At level 10 with CON 14 (+2 base, +4 Mantle = 18, +4 mod): HP ≈ 10×(5.5 + 4) = 95. Getting hit 85% of the time with ~95 HP against CR 10 enemies dealing ~20 damage/hit means roughly 5 rounds of combat before going down. That's tight but functional, especially with Medallion spends (Soulshield = 20 temp HP, Cheat Death prevents surge on 0 HP).

**WATCH** because the Host's AC curve runs below the front-liner average at every tier. The Medallion closes the gap but requires souls to be banked (creating surge tension — see Check 3). Without souls, the Host is the easiest target in the front line. The class compensates with fire immunity, fear immunity, Hellfire Backlash (discouraging melee attacks), and Medallion reactive spends — but a new player who doesn't actively spend Medallion charges defensively will feel squishy.

No fix proposed — this is design principle 5 ("Defense must be earned") and the tension is intentional.

---

## CHECK 7: FEAT TAX

### Verdict: **PASS**

**Required fear chain:**
1. Power Attack (prereq: STR 13, BAB +1) — available L1
2. Intimidating Prowess (prereq: none beyond trained Intimidate) — available L1
3. Cornugon Smash (prereq: Power Attack, Intimidate 6 ranks) — available L6

That's 3 feats, with Cornugon Smash available at L6 (6 ranks Intimidate requires level 6). The prompt says Cornugon requires both PA and Intimidating Prowess — actually, Cornugon Smash in PF1E requires only Power Attack and Intimidate 6 ranks. Intimidating Prowess is highly recommended but not a prerequisite. So the hard tax is 2 feats (PA + Cornugon), with Intimidating Prowess as a near-must-have.

**Feat budget:**

Human bonus feat: 1 at L1.
Standard progression: L1, 3, 5, 7, 9, 11, 13, 15, 17, 19 = 10 feats.
Class bonus feats: L2, 5, 9, 12, 15, 18 = 6 bonus feats from combat list.
**Total by L20: 1 + 10 + 6 = 17 feats.**

**Minimum feat spending for core functionality:**

| Feat | Source | Level Available |
|------|--------|----------------|
| Power Attack | Standard L1 | 1 |
| Intimidating Prowess | Standard L1 | 1 |
| Cornugon Smash | Standard L7 (need 6 ranks) | 7 |

That's 3 of 17 feats. 14 remaining.

**Recommended but optional (fear chain extensions):**

| Feat | Source | Level |
|------|--------|-------|
| Shatter Defenses | Bonus L5 or Standard | 5+ (needs Weapon Focus, Dazzling Display, BAB +6) |
| Dreadful Carnage | Bonus L9 or Standard | 9+ (needs Dazzling Display, Great Fortitude) |

Wait — Shatter Defenses requires Weapon Focus, Dazzling Display, and BAB +6. That's a 4-feat chain: Weapon Focus → Dazzling Display → Shatter Defenses. With Power Attack already taken, the full optimal fear chain is:

1. Power Attack (L1)
2. Intimidating Prowess (L1 human bonus)
3. Weapon Focus (L2 class bonus)
4. Dazzling Display (L3)
5. Cornugon Smash (L7)
6. Shatter Defenses (L9 class bonus, needs BAB +6 ✓)

That's 6 feats for the full fear-into-flat-footed chain. 11 remaining for combat functionality.

**Combat functionality feats (typical build):**

| Feat | Level |
|------|-------|
| Combat Reflexes | L5 class bonus |
| Improved Critical (spiked chain) | L11 |
| Weapon Specialization | L12 class bonus |
| Lunge | L13 |
| Furious Focus | L15 class bonus |
| Blind-Fight | L15 |
| Step Up | L17 |
| Greater Vital Strike or Whirlwind Attack | L18 class bonus |

That's 8 more feats, totaling 14. Still 3 feats in reserve for player preference (Iron Will, Dodge, Mobility, Spring Attack, etc.).

**PASS.** The fear chain costs 6 feats (3 minimum, 6 for the full Shatter Defenses combo). With 17 total feats and 6 of those from the class bonus list, there's room for both the fear chain AND a full combat feat suite with 2–3 flex picks. No feat starvation.

---

## CHECK 8: PARTY ROLE OVERLAP

### Verdict: **PASS**

**Comparison matrix:**

| Role | Fighter | Paladin | Barbarian | Cavalier | Spirit of Vengeance |
|------|---------|---------|-----------|----------|---------------------|
| Raw damage/hit | Highest | High (Smite) | High (Rage) | High (Challenge+Charge) | Below average (compensated by empyreal bypass) |
| Sustained DPR | Highest (always-on) | High (Smite limited/day) | High (Rage rounds) | Moderate (charge-dependent) | Moderate (transformation rounds) |
| AC | Highest (heavy armor + shield) | Very high (heavy + CHA) | Low-moderate (no heavy armor) | High (heavy armor) | Low-moderate (medium armor, Medallion-dependent) |
| Anti-evil specialization | None | Best (Smite, Divine Grace, Aura) | None | None | Strong but different (Penance targets guilt not alignment, empyreal bypasses resistances) |
| Fear/debuff | None | Aura of Courage (anti-fear) | Intimidating Glare (Rage) | Banner (anti-fear) | Best (Existential Dread party buff, Penance fear chain, Cornugon→Shatter Defenses) |
| Mounted combat | None (unless built for it) | Divine Bond mount | None | Best (Charge, Banner, Tactician) | Moderate (utility mount, defensive, Hellfire Leap) |
| Transformation resource | None | None | Rage rounds | None | Mantle rounds (tighter than Rage) |
| Out-of-combat utility | Low | Detect evil, Lay on Hands, Mercy | Low | Tactician, Banner | Sin Sight, Soul Interrogation, detect evil always-on, Existential Dread for interrogation scenes |

**Where the Host steps on toes:**

- **vs Fighter (raw damage):** Never. The Host is behind at every tier (section 22: 42 vs 49 at L20). The empyreal bypass makes the Host better against fire/holy/unholy-resistant targets specifically, but a Fighter with a Holy weapon already has that covered against evil creatures. The Host's advantage is against enemies resistant to conventional energy types — demons immune to fire, devils immune to fire, angels immune to holy. Niche advantage, not overlap.

- **vs Paladin (anti-evil):** Moderate overlap in concept but different mechanics. Paladin detects evil as alignment; Host detects guilt as acts. Paladin Smites evil for big single-target damage; Host Penance Stares for crowd control and Wis damage. Paladin has Lay on Hands and Mercies; Host has nothing comparable. The Host is better at debuffing crowds of guilty enemies; the Paladin is better at killing one evil target fast and healing the party. **Different enough.**

- **vs Barbarian (transformation/rage):** Most direct overlap. Both transform, both have limited rounds, both get STR/CON bonuses. Key differences: Barbarian's rage bonuses are larger (+4/+4 base, scaling to +8/+8 with Greater Rage), Barbarian gets DR, Barbarian has no fear chain or crowd control. Host gets the entire empyreal/Penance/Medallion/mount package instead. A Barbarian is a better damage dealer; a Host is a better scene controller. **Different enough.**

- **vs Cavalier (mounted combat):** Minimal overlap. Cavalier's mount is the primary damage platform (Spirited Charge). Host's mount is defensive/mobility only (no empyreal on mount attacks — section 11 rejected this explicitly). Host's Hellfire Leap is a movement tool; Cavalier's charge is a damage multiplier. **Not in competition.**

**Is there a level range where the Host is strictly better than any of these at their own specialty?**

No. The Host never exceeds Fighter damage, never exceeds Paladin anti-evil burst, never exceeds Barbarian raw transformation power, and never exceeds Cavalier charge damage. The Host's unique value is the combination: empyreal bypass + fear/debuff aura + Penance crowd control + Medallion tactical resource + narrative pressure. No single class replicates that combination, and no single element of that combination exceeds its specialist counterpart.

**PASS.** Clear differentiation at every tier. The Host fills a unique role as a fear-based debuff striker with energy bypass, not as a better version of any existing class.

---

## CHECK 9: LEVEL 1–3 SURVIVABILITY

### Verdict: **WATCH**

**Host stats at level 1 (untransformed):**
- HP: 1d10 + CON 1 = ~6.5 avg, call it **11** with max at L1 + Toughness.
  - Actually, with CON 13 (+1) and d10 HD: 10+1 = 11 at L1. Toughness adds +1 at L1 = **12**.
  - But does the build have room for Toughness? With Power Attack at L1 and Intimidating Prowess at L1 (human bonus), Toughness would be a L3 feat. At L1 without Toughness: **11 HP.**
- AC untransformed: 10 + 4 (chain shirt) + 2 (DEX) = **16.**
- AC transformed: 16 + 1 (natural armor) = **17.**

**Transformation budget at L1:** 4 rounds.

**Standard adventuring day: 2–3 encounters.**

Scenario: 3 encounters, each lasting 3–4 rounds. Total combat rounds: 9–12.

The Host has 4 rounds of transformation. That's enough for ONE full encounter. The other 1–2 encounters must be fought as the untransformed Host: a full-BAB martial with a MW weapon, 16 AC, 11 HP, and no class features beyond detect evil.

**Can the untransformed Host survive CR 1 combat?**

A CR 1 enemy (e.g., goblin warrior, skeleton) has approximately: +3 attack, dealing ~5 damage. Against AC 16: needs 13+ = 40% hit rate. At 5 damage per hit and 40% hit rate, expected damage per round from one enemy = 2/round. At 11 HP, the Host can absorb 5–6 rounds of attacks from a single CR 1 enemy. A group of 3 goblins deals ~6 expected/round, dropping the Host in 2 rounds.

That's survivable against single enemies, dangerous against groups. The plan when transformation runs out mid-fight:

1. **Fight with MW weapon.** Full BAB (+1 at L1) + STR 3 = +4 attack, 2d6+4 (greatsword) = 11 avg. Competent but unenhanced.
2. **Retreat.** If transformation ended because rounds ran out and the enemy isn't dead, disengage. Without fire immunity, fear immunity, or empyreal damage, the Host is a generic level 1 martial.
3. **Accept overburn.** Push 1–2 more rounds. At L1 with +2 Will: overburn round 1 DC 14, needs 12+ = 45% success. Round 2 DC 17, needs 15+ = 30%. The doubled Heaven's Brand (2d4 instead of 1d4) is tempting. But failure = Zarathos surge, and the DM takes over.

This is the intended experience (section 3): "The user explicitly wanted players to try at low levels and screw up. Learn their lesson." The level 1 Host is SUPPOSED to feel the squeeze. 4 rounds isn't enough for a full adventuring day. The player must learn to ration.

**Level 2:** CHA 3 + 2 = 5 rounds. Still not enough for 2 encounters.
**Level 3:** CHA 3 + 3 = 6 rounds. Plus mount (The Turning — no food/rest). Getting close to 2 encounters.

**HP at level 3:** 3d10 + 3 (CON) = ~19.5 avg. With Toughness at L3: ~22.5. AC transformed: 17. AC untransformed: 16.

A standard adventuring day at level 3 with 6 transformation rounds is still tight: two 3-round fights exhausts the entire budget. A third encounter means overburn or fighting untransformed.

### Assessment

Levels 1–3 are genuinely hard. The Host is a fragile martial outside transformation, and transformation is a scarce resource. This is by design — section 23 principle 7: "Start low, scale slow." The Host at level 1 isn't meant to be a Barbarian with unlimited rage. They're meant to be someone who gets a few rounds of terrifying power and then has to be a person again.

**WATCH** because a GM who runs more than 2 encounters per day at levels 1–3 will push the Host into either overburn (learning experience as intended) or fighting untransformed with 16 AC and 11 HP (survivable but painful). The guidebook should note that the DM may want to run shorter adventuring days at levels 1–3, or the player should expect to overburn and learn from the consequences.

No mechanical fix proposed — this is the intended difficulty curve. Recommendation: add a DM sidebar to the guidebook noting that 2-encounter days are the sweet spot at levels 1–3.

---

## CHECK 10: COMPOUND RISK — OVERBURN + FULL MEDALLION

### Verdict: **WATCH**

**Setup:** Level 12, 5 souls stored (Medallion at capacity).

**Three overlapping surge pressures:**

1. **Overburn DC (round 1):** 14 + 5 (souls) = **19.** Will +8. Need 11+ = **50% success.**
2. **Medallion-at-capacity trigger:** DC 20 + 5 = **25** each round of combat. Will +8. Need 17+ = **20% success.**
3. **Overburn tax:** 1d6 untyped damage per round. At ~80 HP (L12), this is manageable but cumulative.

**If the Host is in overburn with a full Medallion, they roll TWO Will saves per round:**

| Round | Overburn DC | P(pass) | Capacity DC | P(pass) | P(pass both) | P(surge) |
|-------|------------|---------|-------------|---------|---------------|----------|
| 1 | 19 | 50% | 25 | 20% | 10% | **90%** |
| 2 | 22 | 35% | 25 | 20% | 7% | **93%** |
| 3 | 26 | 10% | 25 | 20% | 2% | **98%** |

The Host surges within 1 round ~90% of the time if they attempt overburn with a full Medallion at level 12.

**Is this a death spiral?**

Technically yes — banking souls makes overburn unusable. But this is the intended interaction:

1. The player is NOT supposed to max out the Medallion AND overburn simultaneously. These are two different power systems that both carry Zarathos-temptation costs. Stacking them is like raging while fatigued — the rules let you, but it's not the optimal play.

2. The Medallion-at-capacity trigger fires during ALL combat, not just overburn. With a full Medallion at L12, the Host faces DC 25 Will every round even during normal transformation. That's the real pressure — the Medallion is screaming "spend me or lose control." Overburn on top of that is just greedy.

3. The escape hatch is spending souls: each soul spent reduces the capacity DC by 1 and may drop the Host below capacity entirely (eliminating the trigger). Spending 2 souls (Cheat Death) drops to 3 souls, well below the 5-soul capacity, killing the capacity trigger and reducing overburn DC from 19 to 17. The system rewards reactive spending.

**Is the compound pressure creating a death spiral where banking souls makes overburn unusable?**

Yes, and that's correct. At level 12, the player faces a clear choice: bank souls for passive AC OR keep the Medallion below capacity for overburn flexibility. They can't have both at maximum. This IS the Medallion's design tension (section 13): "Constant resource agonizing."

**Key question: is the Medallion-at-capacity trigger too aggressive at L12?**

DC 25 with +8 Will = 20% success per round. Over 3 rounds of normal combat (not even overburn): P(no surge) = 0.008. The Host will almost certainly surge during any combat that lasts more than 1 round with a full Medallion.

This means the player effectively cannot carry a full Medallion into combat at level 12. They must spend at least 1 soul pre-combat or in the first round to drop below capacity. This is a strong design constraint — it forces active soul management. But it also means the passive AC bonus from a full Medallion (+2 at 5 souls) is essentially theoretical — the player can never maintain it during combat.

**Comparison at level 16 (Medallion cap 7):** DC 20 + 7 = 27. Will +10. Need 17+ = 20%. Same problem. At level 20 (cap 10): DC 30. Will +12. Need 18+ = 15%. WORSE, but at level 20 overburn is irrelevant (unlimited transformation) so the compound risk disappears — the only pressure is the capacity trigger alone.

### Assessment

The math works as intended but the interaction is unintuitive. A player who doesn't understand that "full Medallion = guaranteed surge in combat" will be surprised and frustrated. A player who DOES understand it will manage their souls actively, which is the correct gameplay.

**WATCH.** No mechanical fix proposed. Recommendation: the guidebook or DM guide should include an explicit callout:

> **Medallion Management Warning:** A Medallion at maximum capacity forces a Will save against Zarathos surge EVERY ROUND of combat. At level 12, this is DC 25 — you will almost certainly lose this save within 2–3 rounds. To avoid involuntary surges, spend at least one soul before or during combat to drop below capacity. The Medallion is designed to be spent, not hoarded. Banking every soul to maximum is the trap Zarathos sets for you — the passive AC is the bait, the surge is the hook.

---

## PROPOSED FIXES & RECOMMENDATIONS

### Recommendation 1: Guidebook Sidebar — Penance at High Levels (Check 2)

Add to the Penance Stare section:

> *At level 15+, the Penance Stare's primary value shifts. Against high-Will enemies (outsiders, casters), the fail effect (Paralysis, heavy Wis damage) becomes rare. The success effect — Shaken + 1 Wis/round — becomes the workhorse. Hold the stare. Grind the Wisdom. The fear chain (Cornugon Smash → Shatter Defenses) does the rest. The Stare is a siege weapon at high levels, not a kill shot.*

### Recommendation 2: Level 1–3 Survivability (Check 9)

No fix. Working as intended — the squeeze IS the gameplay. DM should expect overburn at low levels and let the consequences teach.

---

## ADDENDUM A: MEDALLION REVISION — LOCKED

**Problem:** The original Medallion (+1 AC per 2 souls, capacity trigger DC 20 + souls stored) created a death spiral at level 12. Full Medallion = DC 25 every round, Host +8 Will = 80% failure. The passive AC was theoretically nice but practically unusable because holding it guaranteed a surge within 2 rounds.

**Revision — two changes:**

### 1. Medallion AC Bonus: Tied to Tier, Not Soul Count

| Level | Capacity | AC Bonus (Sacred) |
|-------|----------|-------------------|
| 8 | 3 | +2 |
| 12 | 5 | +3 |
| 16 | 7 | +4 |
| 20 | 10 | +5 |

AC bonus is granted at the tier breakpoint when the Medallion is at capacity. Souls past the AC breakpoint are ammunition for spends.

### 2. Capacity Trigger: DC 15 + Medallion AC Bonus

| Level | AC Bonus | DC | Will | Need | Success Rate |
|-------|----------|----|------|------|-------------|
| 8 | +2 | 17 | +6 | 11+ | **50%** |
| 12 | +3 | 18 | +8 | 10+ | **55%** |
| 16 | +4 | 19 | +10 | 9+ | **60%** |
| 20 | +5 | 20 | +12 | 8+ | **65%** |

### Comparison to Peers (Revised)

| Level | Host AC (w/souls) | Host (no souls) | Fighter | Paladin | Cavalier |
|-------|-------------------|-----------------|---------|---------|----------|
| 8 | ~22 | ~20 | ~24 | ~25 | ~24 |
| 12 | ~28 | ~25 | ~29 | ~30 | ~28 |
| 16 | ~33 | ~29 | ~33 | ~34 | ~32 |
| 20 | ~38 | ~33 | ~37 | ~36 | ~36 |

Behind Fighter/Paladin through 12. Parity at 16. Slight edge at 20 as a capstone reward. Defense earned, not given.

### Design Notes Update (Section 13)

Replace the Medallion passive text with:

> **Passive:** Sacred AC bonus by Medallion tier: +2 (L8), +3 (L12), +4 (L16), +5 (L20). Granted when Medallion is at capacity. Even at maximum (+5 at L20), Host AC stays at or near Paladin/Fighter range — never far above it.
>
> **Capacity Trigger:** At maximum soul capacity, Will save each round of combat: **DC 15 + current Medallion AC bonus.** Coinflip at level 8 (the lesson), comfortable by level 16 (the reward). Spending souls below capacity removes the trigger entirely.

### Why This Works

- **Teaching curve:** 50% at L8 is scary enough to teach soul management. 65% at L20 is background noise.
- **Escape hatch intact:** Spend one soul → below capacity → trigger stops. Same gameplay loop.
- **No death spiral:** Overburn still adds +1/soul to its own DC. The capacity trigger is separate and manageable. Stacking both is still greedy, but no longer suicidal.
- **Capstone feels earned:** +5 sacred AC at L20 with 10 souls banked is a reward for 20 levels of soul management, not a freebie.

---

## AUDIT COMPLETE

All 10 checks performed. Math shown. Three items revised during audit (Medallion AC, capacity trigger, compound risk). One WATCH item remains (Penance DC at high levels — by design). One guidebook sidebar recommended. Zero mechanical failures.

*"Look into my eyes."*
