# Spirit of Vengeance — Design Notes Revision (March 2026)

**Source:** scaling-audit-results.md, Addendum A
**Scope:** Medallion of Power (Section 13) only. All other sections unchanged.
**Status:** Locked.

---

## WHAT CHANGED

Two values in Section 13. Everything else in the Medallion (capacity, harvest, active spends, Zarathos pressure on overburn, durability) is untouched.

---

## CHANGE 1: Passive AC Bonus

### Before

> +1 sacred AC per 2 souls stored (max +5 at 10 souls).

### After

> Sacred AC bonus by Medallion capacity tier:
>
> | Level | Capacity | AC Bonus (Sacred) |
> |-------|----------|-------------------|
> | 8 | 3 | +2 |
> | 12 | 5 | +3 |
> | 16 | 7 | +4 |
> | 20 | 10 | +5 |
>
> Bonus granted when Medallion is at capacity. Souls beyond the AC threshold are ammunition for active spends.

### Why

The old formula (+1 per 2 souls) capped at +5 but was functionally unusable — carrying enough souls to earn the AC also triggered the capacity surge at unsurvivable DCs. The new version ties AC to tier breakpoints, making the bonus predictable and the progression clean. Host AC reaches Fighter/Paladin parity at 16 and edges past slightly at 20 as a capstone reward.

---

## CHANGE 2: Capacity Trigger DC

### Before

> Will DC 20 + souls stored, each round of combat at max capacity.

At level 12 with 5 souls: DC 25. Host Will +8. 80% failure per round. Guaranteed surge within 2 rounds. Effectively made full Medallion incompatible with combat.

### After

> Will DC 15 + current Medallion AC bonus, each round of combat at max capacity.

| Level | AC Bonus | DC | Will | Need | Success Rate |
|-------|----------|----|------|------|-------------|
| 8 | +2 | 17 | +6 | 11+ | **50%** |
| 12 | +3 | 18 | +8 | 10+ | **55%** |
| 16 | +4 | 19 | +10 | 9+ | **60%** |
| 20 | +5 | 20 | +12 | 8+ | **65%** |

### Why

The old trigger scaled with soul count, which scaled with the thing it punished. More souls = harder save = guaranteed surge = souls unusable. The new trigger scales with AC bonus, which caps at +5 and produces a teaching curve: coinflip at 8 (scary, lesson learned), comfortable by 16 (reward for experience), background noise at 20.

Escape hatch unchanged: spend one soul → drop below capacity → trigger stops.

---

## WHAT DID NOT CHANGE

- **Capacity:** 3 (L8), 5 (L12), 7 (L16), 10 (L20). Unchanged.
- **Harvest:** Swift action on evil kill while transformed. Unchanged.
- **Active spends:** All six spends (Deny the Reaper, Soulshield, Soul Deflection, Hellfire Retort, Shatter Binding, Cheat Death) unchanged.
- **Overburn pressure:** +1 to overburn DC per soul stored. Unchanged. This is the gambling mechanic — it should bite.
- **Surge on 0 HP:** Automatic unless Cheat Death spent. Unchanged.
- **Surge aftermath:** Medallion emptied, exhausted 10 min, can't transform 1 hour. Unchanged.
- **Durability:** Suppressible by Dispel/Antimagic, breakable by artifact force. Unchanged.

---

## REVISED SECTION 13 TEXT (drop-in replacement)

> **Passive:** Sacred AC bonus by Medallion tier: +2 (L8), +3 (L12), +4 (L16), +5 (L20). Granted when Medallion is at capacity. Even at maximum (+5 at L20), Host AC reaches Fighter/Paladin parity — never far above it. Defense must be earned by killing evil and banking souls.
>
> **Capacity Trigger:** At maximum soul capacity, the Host must succeed on a Will save (DC 15 + current Medallion AC bonus) each round of combat or Zarathos surges. Spending souls below capacity removes the trigger entirely.

---

## PEER AC COMPARISON (revised)

| Level | Host (w/souls) | Host (no souls) | Fighter | Paladin | Cavalier |
|-------|----------------|-----------------|---------|---------|----------|
| 8 | ~22 | ~20 | ~24 | ~25 | ~24 |
| 12 | ~28 | ~25 | ~29 | ~30 | ~28 |
| 16 | ~33 | ~29 | ~33 | ~34 | ~32 |
| 20 | ~38 | ~33 | ~37 | ~36 | ~36 |
