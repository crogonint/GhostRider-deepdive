---
title: "Master Reference"
tags: [pf1e, ghost-rider, reference]
system: Pathfinder 1E
status: Updated March 2026 — vault restructured, Medallion revised, scaling audit complete.
---

# Ghost Rider — Master Reference

*Session state, file inventory, and locked design decisions.*

---

## FILE INVENTORY

### Core Documents (Start Here)

| File | Contents |
|------|----------|
| `ghost-rider-player-dm-guidebook.md` | Complete class — rules, d100 table, damage parity, Zarathos surge, DM guide |
| `the-host.md` | What a Host is, notable hosts, the human behind the skull |
| `ghost-rider.md` | The mantle, the transformation, notable Riders |
| `spirits-of-vengeance.md` | The entities — Zarathos, Noble Kale, Eli Morrow, surge mechanic |

### Arsenal & Artifacts

| File | Contents |
|------|----------|
| `hellfire-weapons.md` | The Chain, the Shotguns, Heaven's Brand — canon + class progression |
| `hellmounts.md` | Vehicles and creatures — Hellcycle, Hell Charger, horses, Infernal Steed |
| `the-sword-of-uri-el.md` | Major artifact — sacred fire blade with Zarathos resonance |
| `the-medallion-of-power.md` | Soul battery — revised AC (2/3/4/5), capacity trigger, active spends |

### Mechanics & Design

| File | Contents |
|------|----------|
| `penance-stare-design-reference.md` | Canon lore + five-tier class progression |
| `existential-dread-mechanic.md` | Canon lore + class party buff version |
| `the-contract.md` | Mephisto's bargain + Contract Immunity |
| `npc-reference.md` | CR 6 / CR 19 / CR 26 stat blocks — DM use only |

### Lore & Reference

| File | Contents |
|------|----------|
| `canon-lore.md` | Merged canon reference — empyreal descriptor, ability inventory, power calibration |
| `image-gallery.md` | All campaign art with file reference table |

### Session Notes & Research

| File | Contents |
|------|----------|
| `spirit-of-vengeance-design-notes.md` | The bible — all 25 sections, every locked decision |
| `scaling-audit-results.md` | 10-check stress test, levels 1–20 |
| `design-notes-revision-march-2026.md` | Medallion section 13 replacement |

### Foundry VTT

| File | Contents |
|------|----------|
| `spirit_of_vengeance_level1.json` | Level 1 class template |

### Site Infrastructure

| File | Contents |
|------|----------|
| `index.html` | Campaign vault landing page |
| `default.html` | Jekyll layout |
| `_config.yml` | Jekyll config |

---

## KILLED FILES (superseded — do not restore)

| File | Replaced By |
|------|-------------|
| `final-stat-blocks.md` | `npc-reference.md` |
| `corrected-stat-blocks.md` | `npc-reference.md` |
| `ghost-rider-johnny-blaze.md` | `ghost-rider.md` + `npc-reference.md` |
| `johnny-blaze-complete-character-document.md` | `the-host.md` |
| `dm-and-player-guide.md` | Merged into `ghost-rider-player-dm-guidebook.md` Part 7 |
| `canon-reference.md` | Merged into `canon-lore.md` |
| `canon-deep-dive.md` | Merged into `canon-lore.md` |
| `zarathos-spirit-of-vengeance.md` (old) | `spirits-of-vengeance.md` |
| `the-hellfire-chain.md` | Merged into `hellfire-weapons.md` |
| `the-hellfire-shotgun.md` | Merged into `hellfire-weapons.md` |
| `the-hellcycle.md` | Replaced by `hellmounts.md` |
| `the-host-johnny-blaze.md` | Replaced by `the-host.md` |

---

## DESIGN DECISIONS LOCKED

1. **DC 40 flat** for NPC Penance Stare Will save (both GR and Zarathos)
2. **Success damage = 1 flat** (not 1d4) — deity tier survival depends on this
3. **Fail damage = 4d4 GR / 5d4 Zarathos** Wis per round (NPC version)
4. **Empyreal descriptor** bypasses all fire AND holy AND unholy resistance/immunity
5. **Hellfire chain proficiency** = inherent to divine office, no feat required
6. **Zarathos WIS 24** = intentional design choice (NPC), not error
7. **Contract Immunity** = hard narrative rule, no saving throw
8. **Medallion AC bonus** = sacred AC by tier: +2 (L8), +3 (L12), +4 (L16), +5 (L20)
9. **Medallion capacity trigger** = DC 15 + current Medallion AC bonus, each round at max capacity
10. **Overburn curve** = 14/17/21/26/32/+7 per round. Medallion adds +1/soul
11. **Heaven's Brand** = all d4s (1d4/1d4/2d4/3d4/4d4). Not d6s
12. **Rider's Mantle rounds** = CHA mod + class level
13. **Infernal Steed** = Hellfire Leap (not flight). No pounce off Leap. Mount defensive only
14. **Scaling audit complete** — 10 checks passed. See `scaling-audit-results.md`

---

## INHERITANCE CHAIN (NPC versions)

```
Johnny Blaze (CR 6, Expert 7, Human)
    ↓ transforms into
Ghost Rider (CR 19, 18 HD, Medium Outsider)
    ↓ surges into
Zarathos (CR 26, 26 HD, Large Outsider)
```

Each form retains all abilities of forms below it. Chain weapon feats NOT inherited by Zarathos.

---

## OPEN ITEMS

- [ ] Foundry VTT JSONs need rebuild for leveling class (currently NPC stat blocks)
- [ ] Design notes section 13 needs manual update per `design-notes-revision-march-2026.md`
- [x] Scaling audit complete ✓
- [x] Medallion revision locked ✓
- [x] All topical files rewritten with canon lore ✓
- [x] Vault restructured — no old build data in topical files ✓
