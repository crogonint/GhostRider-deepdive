---
title: "Penance Stare Design Reference"
aliases: ["Penance Stare", "Penance Stare Mechanics"]
tags:
  - pf1e
  - ghost-rider
  - mechanics
system: Pathfinder 1E
---

# Ghost Rider — Penance Stare Design Reference

![](images/Penance_Stare.jpg)

### Mechanical Design Space & Scaling Analysis

---

## Core Math

All fail rates use PF1E d20 resolution:

```
P(fail) = clamp( DC − Will − 1,  min=1,  max=19 ) / 20
```

Natural 1 always fails (5% floor). Natural 20 always succeeds (5% ceiling).

```
E[dmg/round] = P(fail) × avg_fail_dmg  +  P(success) × avg_success_dmg
Rounds to catatonic ≈ Wis Score / E[dmg/round]
```

---

## Design Targets

| Tier | CR | Sample Wis | Sample Will | Target Rounds |
|---|---|---|---|---|
| Street Level | 1–5 | 10 | +3 | 1 |
| Veteran | 6–10 | 11 | +5 | 1 |
| Elite Warrior | 11–15 | 14 | +8 | 1–2 |
| Master Caster | 11–15 | 20 | +15 | 1–2 |
| Champion Warrior | 16–21 | 14 | +12 | 2–3 |
| Elite Caster | 16–21 | 26 | +22 | 2–4 |
| Demon Lord (low) | 26–28 | 30 | +28 | 10–15 |
| Demon Lord (high) | 29–30 | 34 | +35 | 12–20 |
| Demigod | 35–39 | 36 | +36 | 15–25 |
| Lesser Deity | 40–45 | 38 | +45 | 20–35 |
| Intermediate Deity | 46–54 | 44 | +53 | 25–45 |
| Greater Deity | 55–65 | 45 | +62 | 30–60 |

---

## Target Reference Stats

Nine representative targets used throughout all tables below.

| Code | Tier | CR | Wis | Will Save |
|---|---|---|---|---|
| T1 | Street | 5 | 10 | +3 |
| T2 | Veteran | 10 | 11 | +5 |
| T3 | Master Caster | 15 | 20 | +15 |
| T4 | Elite Caster | 21 | 26 | +22 |
| T5 | Demon Lord (high) | 30 | 34 | +35 |
| T6 | Demigod | 37 | 36 | +36 |
| T7 | Lesser Deity | 42 | 38 | +45 |
| T8 | Intermediate Deity | 50 | 44 | +53 |
| T9 | Greater Deity | 60 | 45 | +62 |

---

---

# PART 1: DC MECHANISM OPTIONS

Six ways to set the Will save DC. Each table shows P(fail) per target.

---

## DC-A — Fixed DC 35 (Baseline / Current Direction)

> Simple. Ghost Rider is trivially resistible by anyone with divine Will saves.

| Target | Will | P(fail) |
|---|---|---|
| T1 (CR5) | +3 | **95%** |
| T2 (CR10) | +5 | **95%** |
| T3 (CR15) | +15 | **95%** |
| T4 (CR21) | +22 | **60%** |
| T5 (CR30) | +35 | **5%** ← nat-1 only |
| T6 (CR37) | +36 | 5% |
| T7 (CR42) | +45 | 5% |
| T8 (CR50) | +53 | 5% |
| T9 (CR60) | +62 | 5% |

**Verdict:** Perfect for mortals. T5-T9 are all at the 5% floor — no differentiation across the entire divine tier. Demon Lords and Greater Gods are mechanically identical under this DC.

---

## DC-B — Fixed DC 50

> The "middle" fixed option. Creates a useful spread in the demon lord tier.

| Target | Will | P(fail) |
|---|---|---|
| T1 (CR5) | +3 | **95%** |
| T2 (CR10) | +5 | **95%** |
| T3 (CR15) | +15 | **95%** |
| T4 (CR21) | +22 | **95%** |
| T5 (CR30) | +35 | **70%** |
| T6 (CR37) | +36 | **65%** |
| T7 (CR42) | +45 | **20%** |
| T8 (CR50) | +53 | **5%** |
| T9 (CR60) | +62 | 5% |

**Verdict:** Creates strong pressure on Demon Lords (~70% fail) and a cliff at Lesser Deity. T8-T9 both nat-1 only — still no differentiation at deity tier.

---

## DC-C — Fixed DC 65

> High enough that the interesting band moves up into deity territory.

| Target | Will | P(fail) |
|---|---|---|
| T1–T7 | +3 to +45 | **95%** |
| T8 (CR50) | +53 | **55%** |
| T9 (CR60) | +62 | **10%** |

**Verdict:** Trivializes everything through Lesser Deity (all 95%). The "interesting zone" becomes only the Intermediate/Greater Deity tier. Demon Lords and Empyreal Lords are destroyed like mortals.

---

## DC-D — Tiered Bracket DC

> DC jumps based on which CR tier the target belongs to.

Brackets: CR 1–20 → DC 35 | CR 21–30 → DC 50 | CR 31–45 → DC 65 | CR 46+ → DC 80

| Target | CR Bracket | DC | Will | P(fail) |
|---|---|---|---|---|
| T1 (CR5) | 1–20 | 35 | +3 | **95%** |
| T2 (CR10) | 1–20 | 35 | +5 | **95%** |
| T3 (CR15) | 1–20 | 35 | +15 | **95%** |
| T4 (CR21) | 21–30 | 50 | +22 | **95%** |
| T5 (CR30) | 21–30 | 50 | +35 | **70%** |
| T6 (CR37) | 31–45 | 65 | +36 | **95%** ← bracket reset |
| T7 (CR42) | 31–45 | 65 | +45 | **95%** ← bracket reset |
| T8 (CR50) | 46+ | 80 | +53 | **95%** ← bracket reset |
| T9 (CR60) | 46+ | 80 | +62 | **85%** |

**Verdict:** The bracket resets are a serious problem. Each time a target enters a new tier, P(fail) jumps back to 95%. T6 (Demigod) is actually harder to resist than T5 (top Demon Lord), which is backwards. Creates "difficulty spikes" at bracket transitions rather than a smooth curve.

---

## DC-E — Dynamic: DC = 30 + (Target CR / 2)

> DC scales linearly with target CR. Creates a smooth curve with no bracket resets.

Formula: `DC = 30 + round(CR / 2)`

| Target | CR | DC | Will | P(fail) |
|---|---|---|---|---|
| T1 (CR5) | 5 | 33 | +3 | **95%** |
| T2 (CR10) | 10 | 35 | +5 | **95%** |
| T3 (CR15) | 15 | 38 | +15 | **95%** |
| T4 (CR21) | 21 | 41 | +22 | **90%** |
| T5 (CR30) | 30 | 45 | +35 | **45%** |
| T6 (CR37) | 37 | 49 | +36 | **60%** |
| T7 (CR42) | 42 | 51 | +45 | **25%** |
| T8 (CR50) | 50 | 55 | +53 | **5%** |
| T9 (CR60) | 60 | 60 | +62 | **5%** |

**Note on T5 vs T6:** T6 (Demigod, Will +36) actually fails MORE than T5 (Demon Lord high, Will +35) because the DC jumped by 4 points while Will only went up by 1. This is correct narrative behavior — Demigods are harder to kill than Demon Lords under this formula. However T8 and T9 both converge at 5% (nat-1 floor). Better than fixed DCs but the top of the deity scale still compresses.

---

## DC-F — Opposed Check: Ghost Rider Intimidate vs Target Will

> GR rolls d20 + Intimidate; target rolls d20 + Will. GR wins on tie.
> Approximation formula: `P(fail) ≈ clamp( 50% + (GR_bonus − Will) × 5%,  5%,  95% )`

Using GR Intimidate **+45** (reasonable for a CR 28–30 entity):

| Target | Will | P(fail) |
|---|---|---|
| T1 (CR5) | +3 | **95%** |
| T2 (CR10) | +5 | **95%** |
| T3 (CR15) | +15 | **95%** |
| T4 (CR21) | +22 | **95%** |
| T5 (CR30) | +35 | **95%** |
| T6 (CR37) | +36 | **95%** |
| T7 (CR42) | +45 | **50%** ← inflection point |
| T8 (CR50) | +53 | **10%** |
| T9 (CR60) | +62 | **5%** |

**Variant — GR Intimidate +55:**

| Target | Will | P(fail) |
|---|---|---|
| T5 | +35 | **95%** |
| T6 | +36 | **95%** |
| T7 | +45 | **95%** |
| T8 | +53 | **60%** |
| T9 | +62 | **10%** |

**Verdict:** The opposed roll's inflection point shifts with GR's bonus. Elegant but requires tracking GR's Intimidate as a living stat rather than a fixed DC. Also — a Greater Deity can potentially beat GR's roll even when they'd normally auto-fail a fixed DC, which is narratively satisfying. Primary drawback: adds a die roll to the contact attempt, which may feel redundant with the existing Intimidate/Bluff check for eye contact.

---

---

# PART 2: DAMAGE FORMULA OPTIONS

Five ways to calculate Wisdom damage per round. Each table shows avg fail damage.
Success damage is shown separately — this turns out to be the single most important variable at the divine tier (see notes).

---

## Dmg-I — Flat Moderate: 4d4 fail / 1d4 success

> Simple. Avg fail: **10**. Avg success: **2.5**.

Damage is the same against everyone. The DC determines how often they fail.

> **Critical note on success damage:** At the divine tier where P(fail) = 5% (nat-1 only), the success damage completely dominates expected rounds. With success = 1d4 (avg 2.5): E[dmg] = 0.05×10 + 0.95×2.5 = **2.875/round** → Greater Deity (Wis 45) dies in **~16 rounds**. With success = 1 (flat): E[dmg] = 0.05×10 + 0.95×1 = **1.45/round** → dies in **~31 rounds**. The difference between 1d4 and 1 on the success result is the difference between 16 rounds and 31 rounds at the deity tier. Choose carefully.

---

## Dmg-II — Flat Higher: 3d6 fail / 1 fixed success

> Avg fail: **10.5**. Success: flat **1**. Nearly identical to Dmg-I in expected value, more bell-curved variance. Interchangeable with Dmg-I for design purposes.

---

## Dmg-III — Scales With Ghost Rider's CR: 1d4 per 5 GR-CR

> At GR CR 30: **6d4** (avg 15). Avg success: flat **1**.

| GR CR | Fail Damage | Avg |
|---|---|---|
| CR 20 | 4d4 | 10 |
| CR 25 | 5d4 | 12.5 |
| CR 30 | 6d4 | 15 |
| CR 35 | 7d4 | 17.5 |

The same damage hits a CR 5 soldier and a Greater Deity. At GR CR 30 with 6d4 (avg 15), success damage 1:
- T1 (P=95%): E=14.3. Rounds=10/14.3=**0.7** (instant) ✓
- T9 (P=5%): E=0.05×15+0.95×1=1.7. Rounds=45/1.7=**26.5** (slightly fast, target 30-60)

**Verdict:** Slightly too powerful at the deity tier. Better than the current 1d4/2CR formula but the fixed GR-CR basis means target tier doesn't matter — a CR5 soldier and a Greater Deity take the same dice on a failed save.

---

## Dmg-IV — Tiered Flat by Target CR

> Damage steps down as targets get more divine. Success: flat **1** throughout.

| Target CR Range | Tier Label | Fail Damage | Avg |
|---|---|---|---|
| CR 1–20 | Mortal | 4d4 | 10 |
| CR 21–35 | Champion / Demon Lord | 2d4+2 | 7 |
| CR 36–50 | Demigod / Lesser Deity | 2d4 | 5 |
| CR 51+ | Intermediate / Greater Deity | 1d6 | 3.5 |

**Design rationale:** Ghost Rider's fire burns less hot against more divine beings — not because he's weaker, but because divinity itself is a form of resistance. Mechanically this lets P(fail) stay high while rounds-to-catatonic scale appropriately.

---

## Dmg-V — Escalating Per Round in Lock

> Each round of unbroken Penance Stare lock, damage increases.
> Formula: **Round N: (N+1)d4** on fail. Success: flat **1**.

| Round | Fail Dice | Avg Fail Dmg |
|---|---|---|
| 1 | 2d4 | 5 |
| 2 | 3d4 | 7.5 |
| 3 | 4d4 | 10 |
| 5 | 6d4 | 15 |
| 10 | 11d4 | 27.5 |
| 15 | 16d4 | 40 |

**Design note:** Escalating damage means rounds-to-catatonic cannot be computed as a simple ratio. Requires cumulative sum. See Package 8 for full calculation. Thematically strong — the stare compounds as more sins are recalled. Practically: mortals die fast because they fail saves constantly during the early rounds when damage is still low, and it snowballs. Gods survive the early rounds but the accelerating damage eventually overwhelms even their resilience.

---

---

# PART 3: PACKAGE MATRICES

Eight complete packages showing rounds-to-catatonic for all nine target tiers.
**Bold** = hits design target. ⚠️ = slightly outside target. ✗ = significantly off.

> All calculations use: `Rounds = Wis / ( P(fail)×fail_avg + P(success)×success_avg )`
> Success damage = **1 flat** for all packages unless noted.
> Design targets: T1-T2: 1 | T3: 1-2 | T4: 2-4 | T5: 10-20 | T6: 15-25 | T7: 20-35 | T8: 25-45 | T9: 30-60

---

## Package 1 — DC-A (35) + Dmg-I (4d4/1)

Fixed DC 35. Flat 4d4 fail / 1 success. Baseline for comparison.

| Target | Wis | Will | P(fail) | E[dmg/rnd] | Rounds | Target | ✓? |
|---|---|---|---|---|---|---|---|
| T1 (CR5) | 10 | +3 | 95% | 9.55 | **1.0** | 1 | ✓ |
| T2 (CR10) | 11 | +5 | 95% | 9.55 | **1.2** | 1 | ✓ |
| T3 (CR15) | 20 | +15 | 95% | 9.55 | **2.1** | 1–2 | ✓ |
| T4 (CR21) | 26 | +22 | 60% | 6.40 | **4.1** | 2–4 | ✓ |
| T5 (CR30) | 34 | +35 | 5% | 1.45 | **23.4** | 10–20 | ⚠️ high |
| T6 (CR37) | 36 | +36 | 5% | 1.45 | **24.8** | 15–25 | ✓ |
| T7 (CR42) | 38 | +45 | 5% | 1.45 | **26.2** | 20–35 | ✓ |
| T8 (CR50) | 44 | +53 | 5% | 1.45 | **30.3** | 25–45 | ✓ |
| T9 (CR60) | 45 | +62 | 5% | 1.45 | **31.0** | 30–60 | ✓ |

**Summary:** Surprisingly effective! T5 is the main problem — Demon Lords last 23 rounds (target 10–20). T5 through T9 all converge at 5% fail, so they're all bunched between 23–31 rounds with no meaningful spread. There is no mechanical difference between fighting Nocticula and fighting a Greater God at this DC.

---

## Package 2 — DC-B (50) + Dmg-I (4d4/1)

Fixed DC 50. Kills Demon Lords aggressively. Dangerous to the middle tier.

| Target | Wis | Will | P(fail) | E[dmg/rnd] | Rounds | Target | ✓? |
|---|---|---|---|---|---|---|---|
| T1 | 10 | +3 | 95% | 9.55 | **1.0** | 1 | ✓ |
| T2 | 11 | +5 | 95% | 9.55 | **1.2** | 1 | ✓ |
| T3 | 20 | +15 | 95% | 9.55 | **2.1** | 1–2 | ✓ |
| T4 | 26 | +22 | 95% | 9.55 | **2.7** | 2–4 | ✓ |
| T5 | 34 | +35 | 70% | 7.30 | **4.7** | 10–20 | ✗ too fast |
| T6 | 36 | +36 | 65% | 6.85 | **5.3** | 15–25 | ✗ too fast |
| T7 | 38 | +45 | 20% | 2.80 | **13.6** | 20–35 | ✗ too fast |
| T8 | 44 | +53 | 5% | 1.45 | **30.3** | 25–45 | ✓ |
| T9 | 45 | +62 | 5% | 1.45 | **31.0** | 30–60 | ✓ |

**Summary:** Demon Lords die in 5 rounds, Demigods in 5 rounds. Both are drastically too fast. Ghost Rider becomes an extinction event for the CR 26–45 tier.

---

## Package 3 — DC-C (65) + Dmg-I (4d4/1)

Fixed DC 65. Everything through Lesser Deity is at 95% fail. Divine beings are slaughtered.

| Target | Wis | Will | P(fail) | E[dmg/rnd] | Rounds | Target | ✓? |
|---|---|---|---|---|---|---|---|
| T1–T7 | 10–38 | +3 to +45 | 95% | 9.55 | 1.0–3.98 | varies | ✗ T5–T7 too fast |
| T5 | 34 | +35 | 95% | 9.55 | **3.6** | 10–20 | ✗ |
| T6 | 36 | +36 | 95% | 9.55 | **3.8** | 15–25 | ✗ |
| T7 | 38 | +45 | 95% | 9.55 | **4.0** | 20–35 | ✗ |
| T8 | 44 | +53 | 55% | 6.00 | **7.3** | 25–45 | ✗ |
| T9 | 45 | +62 | 10% | 1.90 | **23.7** | 30–60 | ⚠️ low |

**Summary:** Ghost Rider is a god-killer with a time limit. Demon Lords die in 4 rounds, Greater Gods in 24 rounds. Thematically interesting but canonically overpowered for the lower divine tiers.

---

## Package 4 — DC-E (30+CR/2) + Dmg-I (4d4/1)

Dynamic DC, flat damage. The smoothest DC curve of any fixed-formula approach.

| Target | CR | DC | Will | P(fail) | E[dmg/rnd] | Rounds | Target | ✓? |
|---|---|---|---|---|---|---|---|---|
| T1 | 5 | 33 | +3 | 95% | 9.55 | **1.0** | 1 | ✓ |
| T2 | 10 | 35 | +5 | 95% | 9.55 | **1.2** | 1 | ✓ |
| T3 | 15 | 38 | +15 | 95% | 9.55 | **2.1** | 1–2 | ✓ |
| T4 | 21 | 41 | +22 | 90% | 9.10 | **2.9** | 2–4 | ✓ |
| T5 | 30 | 45 | +35 | 45% | 5.05 | **6.7** | 10–20 | ⚠️ fast |
| T6 | 37 | 49 | +36 | 60% | 6.40 | **5.6** | 15–25 | ✗ |
| T7 | 42 | 51 | +45 | 25% | 3.25 | **11.7** | 20–35 | ⚠️ fast |
| T8 | 50 | 55 | +53 | 5% | 1.45 | **30.3** | 25–45 | ✓ |
| T9 | 60 | 60 | +62 | 5% | 1.45 | **31.0** | 30–60 | ✓ |

**Summary:** Mortals and Elite Casters are perfect. T5 (Demon Lord, 6.7 rounds) and T6 (Demigod, 5.6 rounds) are faster than desired. T7 (Lesser Deity, 11.7 rounds) is slightly fast. T8-T9 hit target range. The Will save advancement curve isn't perfectly linear with CR, causing T6 to ironically die faster than T5 despite being "more divine" — a quirk of the Demigod's Will save (+36) being only 1 point above the top Demon Lord (+35) while the DC jumped by 4.

---

## Package 5 — DC-40 Fixed + Dmg-I (4d4/1)
### ⭐ STANDOUT OPTION

> **DC 40 is the mathematical sweet spot where Will save advancement naturally produces the desired spread across all tiers.** No dynamic formula needed. No tiers. One number.

| Target | Wis | Will | P(fail) | E[dmg/rnd] | Rounds | Target | ✓? |
|---|---|---|---|---|---|---|---|
| T1 (CR5) | 10 | +3 | **95%** | 9.55 | **1.0** | 1 | ✓ |
| T2 (CR10) | 11 | +5 | **95%** | 9.55 | **1.2** | 1 | ✓ |
| T3 (CR15) | 20 | +15 | **95%** | 9.55 | **2.1** | 1–2 | ✓ |
| T4 (CR21) | 26 | +22 | **85%** | 8.65 | **3.0** | 2–4 | ✓ |
| T5 (CR30) | 34 | +35 | **20%** | 2.80 | **12.1** | 10–20 | ✓ |
| T6 (CR37) | 36 | +36 | **15%** | 2.35 | **15.3** | 15–25 | ✓ |
| T7 (CR42) | 38 | +45 | **5%** | 1.45 | **26.2** | 20–35 | ✓ |
| T8 (CR50) | 44 | +53 | **5%** | 1.45 | **30.3** | 25–45 | ✓ |
| T9 (CR60) | 45 | +62 | **5%** | 1.45 | **31.0** | 30–60 | ✓ |

**Why DC 40 works:** The Will save band at the Demon Lord tier (+28 to +35) sits almost exactly at the DC 40 inflection point. A Demon Lord needs to roll a 5–12 on the d20 to succeed — plausible but far from reliable. Mortals are almost always well below (need 1–3 to succeed). Deities are well above (need 1 to succeed — nat-1 only). No tiering required. The natural Will save progression does the work.

**The success damage insight:** With 1d4 success (avg 2.5), Greater Deity dies in **~16 rounds** (too fast). With success = **1 flat**, they die in **~31 rounds** (perfect). The choice of success damage is the most powerful tuning lever at the divine tier. One die type is the difference between 16 and 31 rounds.

**One weakness:** T7 through T9 all converge at 5% fail, giving them rounds in the 26–31 range with relatively little spread (Lesser Deity dies only marginally faster than Greater Deity). This can be addressed with Dmg-IV (see Package 6).

---

## Package 6 — DC-40 + Dmg-IV (Tiered Damage)

DC 40 with damage that decreases at higher divine tiers to widen the spread.

Damage tiers: CR 1–20: 4d4 (avg 10) | CR 21–35: 2d4+2 (avg 7) | CR 36–50: 2d4 (avg 5) | CR 51+: 1d6 (avg 3.5). Success: 1 flat.

| Target | CR | Wis | Will | P(fail) | Fail dmg | E[dmg/rnd] | Rounds | Target | ✓? |
|---|---|---|---|---|---|---|---|---|---|
| T1 | 5 | 10 | +3 | 95% | 10 | 9.55 | **1.0** | 1 | ✓ |
| T2 | 10 | 11 | +5 | 95% | 10 | 9.55 | **1.2** | 1 | ✓ |
| T3 | 15 | 20 | +15 | 95% | 10 | 9.55 | **2.1** | 1–2 | ✓ |
| T4 | 21 | 26 | +22 | 85% | 7 | 6.10 | **4.3** | 2–4 | ✓ |
| T5 | 30 | 34 | +35 | 20% | 7 | 2.20 | **15.5** | 10–20 | ✓ |
| T6 | 37 | 36 | +36 | 15% | 5 | 1.60 | **22.5** | 15–25 | ✓ |
| T7 | 42 | 38 | +45 | 5% | 5 | 1.20 | **31.7** | 20–35 | ✓ |
| T8 | 50 | 44 | +53 | 5% | 5 | 1.20 | **36.7** | 25–45 | ✓ |
| T9 | 60 | 45 | +62 | 5% | 3.5 | 1.125 | **40.0** | 30–60 | ✓ |

**Summary:** Nearly perfect across all tiers. Every design target is hit. The tiered damage resolves the convergence problem from Package 5 — T7-T9 now span 32 to 40 rounds instead of bunching at 26–31. The trade-off: adds one lookup table for damage tier. This is the most mechanically complete single option.

---

## Package 7 — DC-E (30+CR/2) + Dmg-IV (Tiered Damage)

Dynamic DC + tiered damage. Double scaling for maximum precision.

| Target | CR | DC | Will | P(fail) | Fail dmg | E[dmg/rnd] | Rounds | Target | ✓? |
|---|---|---|---|---|---|---|---|---|---|
| T1 | 5 | 33 | +3 | 95% | 10 | 9.55 | **1.0** | 1 | ✓ |
| T3 | 15 | 38 | +15 | 95% | 10 | 9.55 | **2.1** | 1–2 | ✓ |
| T4 | 21 | 41 | +22 | 90% | 7 | 6.40 | **4.1** | 2–4 | ✓ |
| T5 | 30 | 45 | +35 | 45% | 7 | 3.70 | **9.2** | 10–20 | ✓ |
| T6 | 37 | 49 | +36 | 60% | 5 | 3.40 | **10.6** | 15–25 | ⚠️ fast |
| T7 | 42 | 51 | +45 | 25% | 5 | 2.00 | **19.0** | 20–35 | ✓ |
| T8 | 50 | 55 | +53 | 5% | 5 | 1.20 | **36.7** | 25–45 | ✓ |
| T9 | 60 | 60 | +62 | 5% | 3.5 | 1.125 | **40.0** | 30–60 | ✓ |

**Summary:** T5 (Demon Lord) is now 9 rounds — just barely under the 10-round floor. T6 (Demigod) at 10.6 rounds is too fast (target 15–25). The T5/T6 inversion from Package 4 partially persists. Most other tiers are solid. More complex than Package 6 with marginally less accurate results.

---

## Package 8 — DC-40 + Dmg-V (Escalating)

DC 40 fixed. Round N: (N+1)d4 on fail. Success: 1.

Requires cumulative sum, not ratio. Computed iteratively:
`CumulativeWis[K] = Σ(N=1 to K) [ P(fail)×(N+1)×2.5  +  P(success)×1 ]`
Target dies when CumulativeWis ≥ Wis score.

| Target | Wis | P(fail) | Rounds to Catatonic | Target | ✓? |
|---|---|---|---|---|---|
| T1 (CR5) | 10 | 95% | **~2** | 1 | ⚠️ |
| T2 (CR10) | 11 | 95% | **~2** | 1 | ⚠️ |
| T3 (CR15) | 20 | 95% | **~2** | 1–2 | ✓ |
| T4 (CR21) | 26 | 85% | **~3** | 2–4 | ✓ |
| T5 (CR30) | 34 | 20% | **~9** | 10–20 | ⚠️ fast |
| T6 (CR37) | 36 | 15% | **~11** | 15–25 | ⚠️ fast |
| T7 (CR42) | 38 | 5% | **~20** | 20–35 | ✓ |
| T8 (CR50) | 44 | 5% | **~22** | 25–45 | ⚠️ fast |
| T9 (CR60) | 45 | 5% | **~22** | 30–60 | ⚠️ fast |

**Derivation for T9 (P=5%):**
`CumulativeWis[K] = 0.05 × 2.5 × K(K+1)/2  +  0.95 × K = 0.0625K(K+1) + 0.95K`
Set = 45: `0.0625K² + 1.0125K = 45` → K ≈ **20 rounds**

**Summary:** Escalating damage is thematically compelling — each round the fire intensifies as more sins are surfaced. But the escalation accelerates too quickly; Greater Deities die around round 20 rather than 30–60. Would require a weaker starting die or a lower DC to slow down the divine tier. T1-T2 die in round 2 instead of round 1, which feels slightly wrong for street-level mortals. Escalating works best if the narrative goal is "the longer the stare, the worse it gets" rather than hitting specific round targets.

---

---

# PART 4: SUMMARY MATRIX

Rounds to catatonic across all 8 packages. Design targets in parentheses.

| Target | P1 DC35 | P2 DC50 | P3 DC65 | P4 DC-E | ⭐P5 DC40 | P6 DC40+Tier | P7 DCE+Tier | P8 Escalate |
|---|---|---|---|---|---|---|---|---|
| T1 (1) | 1.0✓ | 1.0✓ | 1.0✓ | 1.0✓ | 1.0✓ | 1.0✓ | 1.0✓ | 2⚠️ |
| T2 (1) | 1.2✓ | 1.2✓ | 1.2✓ | 1.2✓ | 1.2✓ | 1.2✓ | 1.2✓ | 2⚠️ |
| T3 (1-2) | 2.1✓ | 2.1✓ | 2.1✓ | 2.1✓ | 2.1✓ | 2.1✓ | 2.1✓ | 2✓ |
| T4 (2-4) | 4.1✓ | 2.7✓ | 2.7✓ | 2.9✓ | 3.0✓ | 4.3✓ | 4.1✓ | 3✓ |
| T5 (10-20) | 23⚠️ | 4.7✗ | 3.6✗ | 6.7⚠️ | **12.1✓** | **15.5✓** | 9.2✓ | 9⚠️ |
| T6 (15-25) | 24.8✓ | 5.3✗ | 3.8✗ | 5.6✗ | **15.3✓** | **22.5✓** | 10.6⚠️ | 11⚠️ |
| T7 (20-35) | 26.2✓ | 13.6✗ | 4.0✗ | 11.7⚠️ | **26.2✓** | **31.7✓** | 19.0✓ | 20✓ |
| T8 (25-45) | 30.3✓ | 30.3✓ | 7.3✗ | 30.3✓ | **30.3✓** | **36.7✓** | 36.7✓ | 22⚠️ |
| T9 (30-60) | 31.0✓ | 31.0✓ | 23.7⚠️ | 31.0✓ | **31.0✓** | **40.0✓** | 40.0✓ | 22⚠️ |

**✓ count:** P1=8/9 | P2=5/9 | P3=3/9 | P4=6/9 | **P5=9/9** | **P6=9/9** | P7=7/9 | P8=5/9

---

---

# PART 5: TUNING LEVERS — QUICK REFERENCE

The following changes have these approximate effects on rounds-to-catatonic:

| Change | Effect on Low Tiers | Effect on Mid Tiers | Effect on High Tiers |
|---|---|---|---|
| Raise DC by +5 | Negligible (already 95%) | ↓ ~30% (less rounds) | Depends; may unlock tier |
| Lower DC by -5 | Negligible (already 95%) | ↑ ~30% (more rounds) | May push to 5% floor |
| Raise fail dmg by +2 avg | ↓ proportionally | ↓ proportionally | Negligible (5% fail) |
| Lower fail dmg by -2 avg | ↑ proportionally | ↑ proportionally | Negligible |
| Raise success dmg by +1 | Negligible (rarely succeed) | Minor ↑ | **Major ↓ at deity tier** |
| Lower success dmg by -1 | Negligible | Minor ↓ | **Major ↑ at deity tier** |
| Add escalating multiplier | Faster at all tiers | Faster | Faster |

**The single most impactful, least obvious lever:** Success damage at the deity tier. Success damage 1d4 (avg 2.5) vs flat 1 is the difference between a Greater Deity dying in 16 rounds vs 31 rounds — entirely from the nat-20 majority.

---

## Recommended Starting Point

**Package 5 (DC 40, 4d4/1, success=1 flat)** for simplicity — one DC, one damage die, hits all nine targets within acceptable ranges.

**Package 6 (DC 40, tiered damage, success=1 flat)** for precision — adds a three-tier damage lookup (mortal/demigod-DL/deity) and pushes every tier squarely into target range. Best choice if the campaign will regularly encounter multiple divine tiers.

---

## Penance Stare Revised Wording (Package 5 / Package 6)

**DC 30** in the current draft should be **DC 40**.

**Damage on fail** should be **4d4 Wisdom damage** (not 1d4 per 2 CR of the target — that formula scales catastrophically fast, producing 15d4 on a failed save against a CR 30 entity).

**Damage on success** should be **1 Wisdom damage** (flat, not 1d4 — the die type here has an outsized effect at the deity tier, as shown above).

For Package 6, add a damage tier note:
> *Against CR 21–35 targets (Champion/Demon Lord tier): 2d4+2. Against CR 36+ targets (Demigod/Deity tier): 2d4. Against CR 51+ (Intermediate/Greater Deity): 1d6.*
