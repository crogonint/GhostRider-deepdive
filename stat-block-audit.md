---
title: "Stat Block Audit"
aliases: ["Stat Audit", "PF1E Verification"]
tags:
  - pf1e
  - ghost-rider
  - stat-blocks
  - audit
system: Pathfinder 1E
---

# Ghost Rider & Zarathos — Stat Block Audit
### First-Principles Verification Against PF1E Formulas

---

## Audit Key

| Symbol | Meaning |
|---|---|
| ✓ | Correct |
| ⚠️ | Minor error / off by 1–2, explainable by feat |
| ✗ | Significant error requiring correction |
| 🔵 | Design choice, not a calculation error — flag for review |
| ❓ | Cannot derive cleanly from stated stats — source unknown |

---

---

# GHOST RIDER — CR 19, 18 HD Outsider

---

## Ability Scores — No Issues

![](images/pf1e_str_reference.svg)

![](images/str_chart_0_60.svg)


STR 30 / DEX 18 / CON 32 / INT 13 / WIS 22 / CHA 24. No contradictions found.

---

## HP

| | Value |
|---|---|
| Stated | 294 |
| Calculated (18d10 + CON×18) | 297 |
| Delta | −3 |
| Verdict | ⚠️ Off by 3. Rounding artifact from conversion. Negligible. |

**Correction:** HP 297 (18d10+198).

---

## Armor Class

| Component | Stated | Calculated | Verdict |
|---|---|---|---|
| AC | 32 | 32 | ✓ |
| Flat-footed | 28 | 28 | ✓ |
| **Touch** | **14** | **20** | **✗** |

**Touch AC error is significant.** In PF1E, deflection bonuses *do* apply to touch AC. Ghost Rider's +6 deflection is being excluded from touch.

Correct touch AC = 10 + 4 (Dex) + 6 (deflection) = **20**.

The stated 14 only counts Dex. This makes him dramatically easier to hit with touch attacks (rays, incorporeal, etc.) than he should be.

---

## Saving Throws

Base good save at 18 HD = +11.

| Save | Stated | Base + Ability | Delta | Explanation |
|---|---|---|---|---|
| Fort | +24 | +11 +11 (CON) = +22 | +2 | ⚠️ Great Fortitude feat (+2) ✓ |
| Ref | +16 | +11 +4 (DEX) = +15 | +1 | ❓ Lightning Reflexes gives +2, not +1. Source unclear. |
| Will | +19 | +11 +6 (WIS) = +17 | +2 | ⚠️ Iron Will feat (+2) ✓ |

**Fort and Will:** Explained cleanly by Great Fortitude + Iron Will. These should be listed in his feat block.

**Ref:** Cannot be explained by a standard feat. Lightning Reflexes gives +2 which would put him at +17, not +16. The +1 discrepancy is either a conversion rounding error or an untracked minor bonus. **Recommend:** Either add Lightning Reflexes and set Ref to +17, or treat as a conversion error and leave at +16 (it barely matters).

---

## BAB / CMB / CMD

| Stat | Stated | Calculated | Verdict |
|---|---|---|---|
| BAB | +18 | +18 | ✓ |
| CMB | +28 | BAB+18 + STR+10 = +28 | ✓ |
| CMB grapple/disarm | +32 | +28 + 4 | ⚠️ Improved Grapple + Improved Disarm each add +2 ✓ |
| CMD | 43 | 10+18+10+4 = 42 | ⚠️ Off by +1. Dodge feat? |

**Correction:** CMD should be **42** unless Dodge feat is listed. If Dodge is intentional, add it to feat block.

---

## SR

SR 30 = 11 + CR 19. ✓

---

## Attack Rolls

| Attack | Stated | Calculated | Verdict |
|---|---|---|---|
| Hellfire chain | +28 | BAB+18 + STR+10 = +28 | ✓ |
| Ranged touch | +22 | BAB+18 + DEX+4 = +22 | ✓ |

Both correct. The hellfire chain should probably carry an enhancement bonus (+1 minimum for a named magic weapon), which would push it to +29/+24/+19/+14. Currently listed with no enhancement bonus factored in.

---

## Special Ability DCs

Standard PF1E formula: 10 + ½ HD + ability modifier = 10 + 9 = 19 base.

| Ability | Stated DC | Basis | Calculated | Delta | Verdict |
|---|---|---|---|---|---|
| Penance Stare | 30 | WIS? | 10+9+6 = **25** | +5 | 🔵 Deliberately elevated — see design notes |
| Hellfire nova | 27 | CHA | 10+9+7 = **26** | +1 | ⚠️ Off by 1 — conversion rounding |
| Brimstone impact | 30 | CON | 10+9+11 = **30** | 0 | ✓ |
| Soul binding | 27 | CHA | **26** | +1 | ⚠️ Off by 1 |
| Cold hellfire | 27 | CON? | CON=30, CHA=26 | ❓ | Neither matches 27 cleanly |
| Hellfire breath | 27 | CHA | **26** | +1 | ⚠️ Off by 1 |
| Righteous Terror (evil) | 30 | CHA | **26** | +4 | 🔵 Deliberately elevated |
| Righteous Terror (non-evil) | 25 | WIS | **25** | 0 | ✓ |

**Pattern:** CHA-based abilities are consistently off by +1. This is a systemic conversion rounding error — whoever did the Marvel conversion likely used 10 + ½HD (rounded up) instead of floor division. 

**Corrections:**
- Hellfire nova, soul binding, hellfire breath → **DC 26** (CHA-based)
- Cold hellfire → **DC 30** (CON-based) for consistency with brimstone impact
- Penance Stare and Righteous Terror DCs are deliberate design choices, not formula errors — discussed separately

---

## Channel Resistance +4

🔵 **Design flag.** Channel Resistance is mechanically an undead trait in PF1E. Applying it to a living outsider is non-standard. It's narratively defensible (Ghost Rider resists divine channeling) but requires a custom ability explanation — it can't just be inherited from creature type. **Recommend:** Keep it but define it as a named special quality rather than the standard undead trait.

---

## Ghost Rider Summary

| Category | Count | Notes |
|---|---|---|
| ✓ Correct | 8 | BAB, CMB, SR, FF AC, melee, ranged touch, brimstone DC, non-evil terror DC |
| ⚠️ Minor | 6 | HP, Fort, Ref, Will, CMD, CHA-based DCs +1 |
| ✗ Significant | 1 | **Touch AC 14 → should be 20** |
| 🔵 Design flags | 3 | Penance Stare DC, Righteous Terror DC, Channel Resistance trait |

---

---

# ZARATHOS — CR 26, 25 HD Large Outsider

---

## Ability Scores — CON ERROR

| Ability | Stated | Evidence | Correct Value |
|---|---|---|---|
| STR | 38 | CMB checks out | ✓ |
| DEX | 21 | Touch/FF AC check out | ✓ |
| **CON** | **36** | **HP 487 requires CON mod +14 → CON 38** | **✗ Should be 38** |
| INT | 22 | No contradiction | ✓ |
| **WIS** | **24** | Low for CR 26 demigod tier | 🔵 See notes |
| CHA | 34 | DCs derive correctly | ✓ |

**CON correction:** HP 487 = 25 × 5.5 + 25 × CON_mod. Solving: CON_mod = (487 − 137.5) / 25 = **14**. CON mod +14 = **CON 38**. The stated CON 36 (+13) produces HP ~462. CON must be **38**.

**WIS note:** Wis 24 (+7) is low for a CR 26 entity — typical Demon Lords at this CR sit at Wis 29–34. Zarathos is canonically a creature of raw destructive power rather than insight or judgment, so this may be intentional. However it produces a Will save of only +24 (see below) which makes him notably vulnerable to Will-based effects relative to his CR. **Flagged for your decision.**

---

## HP

| | Value |
|---|---|
| Stated | 487 |
| Calculated (CON 36, +13) | ~462 |
| Calculated (CON 38, +14) | ~487 |
| Verdict | ✗ CON is wrong in ability score block — HP confirms CON 38 |

---

## Armor Class

| Component | Stated | Calculated | Verdict |
|---|---|---|---|
| AC | 40 | 10+5+8+12+6−1 = 40 | ✓ |
| Flat-footed | 35 | AC − DEX = 35 | ✓ |
| **Touch** | **18** | **32** | **✗ Major error** |

**Touch AC error is severe.** In PF1E both deflection *and* profane bonuses apply to touch AC.

Correct touch AC = 10 + 5 (Dex) + 12 (deflection) + 6 (profane) − 1 (size) = **32**.

The stated 18 appears to be 10 + 5 (Dex) − 1 (size) + 4 (unknown) = 18, which excludes both deflection and profane entirely. This makes Zarathos almost trivially easy to hit with touch attacks — a significant combat error. A CR 26 entity should not have touch AC 18.

The same error exists in Ghost Rider's block and is probably a systemic issue in the original Marvel conversion — they may have been treating deflection and profane as armor-type bonuses only.

---

## Saving Throws

Base good save at 25 HD = +14. Using corrected CON 38 (+14):

| Save | Stated | Base + Ability | Delta | Explanation |
|---|---|---|---|---|
| Fort | +29 | +14 +14 (CON 38) = +28 | +1 | ❓ Great Fortitude gives +2 → would be +30. Off by −1 from feat explanation. Likely conversion error. |
| Ref | +21 | +14 +5 (DEX) = +19 | +2 | ⚠️ Lightning Reflexes (+2) ✓ |
| Will | +24 | +14 +7 (WIS) = +21 | +3 | ❓ Iron Will gives +2 → would be +23. Still off by +1. |

**Pattern:** Ref is clean (Lightning Reflexes). Fort and Will each have a residual +1 that can't be explained by standard feats. This is consistent with a systemic +1 offset in the Marvel conversion's save calculations — they may have been using a slightly different base progression table.

**Recommended corrections:**
- Fort: +28 base + Great Fortitude = **+30**, OR accept +29 as written with conversion offset noted
- Will: +21 base + Iron Will = **+23**, OR accept +24 as written with conversion offset noted
- Ref: **+21** ✓ with Lightning Reflexes

---

## BAB / CMB / CMD

Large creature: +1 CMB, −1 CMD, −1 attack.

| Stat | Stated | Calculated | Verdict |
|---|---|---|---|
| BAB | +25 | +25 | ✓ |
| CMB | +40 | BAB+25 + STR+14 + size+1 = +40 | ✓ |
| CMD | 56 | 10+25+14+5−1 = 53 | ⚠️ Off by +3 |

**CMD:** Off by +3. Dodge (+1) explains one point. The remaining +2 is unexplained. Most likely a conversion error. **Recommend:** CMD **54** (53 base + Dodge) or **53** if no Dodge feat.

---

## SR

SR 37 = 11 + CR 26. ✓

---

## Attack Rolls

Large outsider: −1 size penalty to attack rolls.

| Attack | Stated | Calculated | Delta | Verdict |
|---|---|---|---|---|
| Claw | +37 | BAB+25 + STR+14 − size 1 = +38 | −1 | ⚠️ Off by −1. Power Attack built in? Or conversion error. |
| Ranged touch | +31 | BAB+25 + DEX+5 − size 1 = +29 | +2 | ⚠️ Weapon Focus + Point Blank Shot? Or +2 conversion offset. |

**Claws:** Should be **+38/+33** (or +37/+32 if Power Attack is built into the listed value — clarify intent).

**Hellfire blast:** +31 is +2 above base. If Weapon Focus (ray) and Point Blank Shot are intended feats, this works. If not, correct to **+29**.

---

## Special Ability DCs

Base = 10 + 12 (half of 25 HD) = 22.

| Ability | Stated DC | Basis | Calculated | Delta | Verdict |
|---|---|---|---|---|---|
| Hellfire nova | 34 | CHA | 22+12 = **34** | 0 | ✓ |
| **Penance Stare** | **38** | CHA+AF? | 34+2 (Ability Focus) = **36** | +2 | ❓ |
| Soul rend | 36 | CON | 22+14 (CON 38) = **36** | 0 | ✓ (confirms CON 38) |
| Chain of damnation | 34 | CHA | **34** | 0 | ✓ |
| **Possession** | **38** | CHA+AF? | **36** | +2 | ❓ |
| Cold hellfire | 34 | CHA | **34** | 0 | ✓ |
| Ancient Dread aura | 34 | CHA | **34** | 0 | ✓ |

**Penance Stare and Possession DC 38:** Cannot be derived from stated stats even with Ability Focus (+2 gives 36). The DC 38 appears to be a deliberate narrative override — these are Zarathos's signature abilities and were probably set higher intentionally. However the formula doesn't support it cleanly.

**Two options:**
1. Accept DC 38 as a design choice and note it as such (no feat justification needed for homebrew)
2. Correct to DC 36 (CHA + Ability Focus) for RAW consistency

**Soul rend DC 36** independently confirms CON should be 38 — this is the most useful data point in the entire audit.

---

## Intimidate

+40 = ranks 25 + class 3 + CHA +12. No Intimidating Prowess needed. ✓

---

## Zarathos Summary

| Category | Count | Notes |
|---|---|---|
| ✓ Correct | 7 | BAB, CMB, SR, FF AC, most DCs, Intimidate |
| ⚠️ Minor | 5 | Fort/Will saves, CMD, claw attack, ranged touch |
| ✗ Significant | 3 | **CON 36→38**, **Touch AC 18→32**, **HP wrong due to CON error** |
| 🔵 Design flags | 2 | Wis 24 (low for tier), Penance Stare/Possession DC 38 (above formula) |

---

---

# CROSS-BLOCK ISSUES

## Touch AC Systemic Error

Both stat blocks share the same touch AC calculation error — deflection and profane bonuses excluded. This is almost certainly a systemic issue in the original Marvel conversion. The fix is the same in both cases: include deflection (and profane where applicable) in touch AC.

| Block | Stated Touch | Corrected Touch |
|---|---|---|
| Ghost Rider | 14 | **20** |
| Zarathos | 18 | **32** |

## CHA-based DC +1 offset (Ghost Rider)

All CHA-based DCs in Ghost Rider's block are +1 above formula. This is a systemic rounding error in the conversion — probably used ceiling instead of floor for ½HD. Correct all CHA-based DCs from 27 → **26**.

---

# CORRECTED VALUES — QUICK REFERENCE

## Ghost Rider Corrections

| Stat | Old | New |
|---|---|---|
| HP | 294 | **297** |
| Touch AC | 14 | **20** |
| Ref save | +16 | **+17** (if Lightning Reflexes) or flag as unexplained |
| CMD | 43 | **42** (or 43 if Dodge is a listed feat) |
| Hellfire nova DC | 27 | **26** |
| Soul binding DC | 27 | **26** |
| Hellfire breath DC | 27 | **26** |
| Cold hellfire DC | 27 | **30** (CON-based) |
| Penance Stare DC | 30 | **40** (design decision — see design doc) |

## Zarathos Corrections

| Stat | Old | New |
|---|---|---|
| CON | 36 | **38** |
| HP | 487 | **487** ✓ (now consistent with CON 38) |
| Touch AC | 18 | **32** |
| Fort | +29 | **+30** (CON 38 + Great Fortitude) or **+29** with conversion offset |
| Will | +24 | **+23** (Iron Will) or **+24** with conversion offset |
| CMD | 56 | **54** (with Dodge) or **53** |
| Claw attack | +37 | **+38** (or clarify Power Attack intent) |
| Hellfire blast | +31 | **+29** (or add Weapon Focus + PBS to feat block) |
| Penance Stare DC | 38 | **36** (RAW) or **38** (design override — confirm intent) |
| Possession DC | 38 | **36** (RAW) or **38** (design override — confirm intent) |

---

# DECISIONS NEEDED FROM YOU

1. **Touch AC:** Confirm correction to 20 (GR) and 32 (Zarathos) — this changes how they play against casters significantly.
2. **Zarathos WIS 24:** Intentionally low (raw power, poor judgment flavor) or increase to ~28–30 to match tier?
3. **Penance Stare DC:** Accept 38 as design override, or standardize to 36 (RAW)?
4. **Zarathos Fort/Will saves:** Accept the +1 offset from conversion, or recalculate cleanly to +30/+23?
5. **Claw attacks +37 vs +38:** Is Power Attack built into the listed number, or is it a conversion error?
6. **Hellfire blast +31:** Add Weapon Focus + Point Blank Shot to feat block, or correct to +29?

---

## AUDIT ADDENDUM — Final Locked Values

All decisions above have since been resolved. Final locked stats:

| Character | STR | CMB | CMD | Intimidate | Primary Attack |
|-----------|-----|-----|-----|------------|----------------|
| Johnny Blaze | 13 (+1) | +6 | 18 | +13 | +6 unarmed |
| Ghost Rider | 39 (+14) | +32 | 47 | +42 | Chain +32 |
| Zarathos | 48 (+19) | +44 | 60 | +60 | Claw +45 |

**STR scaling rationale:**
- Johnny STR 13 — peak athletic human, top of non-enhanced published range
- Ghost Rider STR 39 — overhead 5,440 lbs / max 10,880 lbs; old school 5-ton canon confirmed
- Zarathos STR 48 — overhead 19,200 lbs / max 38,400 lbs (9.6 tons); 2× contemporaries; beats Pazuzu STR 40, Baphomet STR 36, Storm Giant STR 39

**Touch AC:** Confirmed 20 (GR) and 32 (Zarathos). Deflection and profane both apply to touch in PF1E. ✓
**Zarathos WIS 24:** Intentionally low — raw destructive force, poor judgment, deliberate flavor. ✓
**Penance Stare DC:** 40 (design override). ✓
**Foundry VTT JSONs:** All three built — `johnny_blaze_foundry_v3.json`, `ghost_rider_foundry_v1.json`, `zarathos_foundry_v1.json`. Zarathos size bug `"lrg"` → `"lg"` fixed post-upload.
