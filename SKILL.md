---
name: newdad-log
description: Newborn 0-12 month expert knowledge base for new dads. Decision trees for jaundice, temperature, gas, milk switch, feeding rhythm, stool observation, plus curated info-source list (Ant Afu, Xiaohongshu, Meiyou).
version: 1.0.0
author: NewDad Log Contributors
license: MIT
platforms: linux, macos, windows
---

# NewDad Log — Newborn 0-12 month expert knowledge base

> ⚠️ **For reference only, does not constitute medical advice**. Follow doctor's guidance.

A new-dad perspective **newborn expert knowledge base** capturing the
highest-frequency parenting scenarios from pregnancy through age 3, so any
AI assistant or parent can find "what to do when X happens" in 30 seconds.

## When to load this Skill

Load when the user is asking about:

- **Newborn (0-1 month) feeding, stool, temperature, jaundice, gas, milk switching**
- **Newborn (0-3 month) spit-up vs choking, sleep, crying, nail trimming**
- **Newborn (0-4 week) umbilical cord care**
- **First-time-dad specific concerns**: 5-step judgment + 7 red flags + 5 myths framework
- **Practical information sources** (medical, parenting community, pregnancy tools)
- **Anything matching** "what to do when baby X" in the 0-12 month window

DO NOT load for:

- ❌ Pregnancy / prenatal care specifics (different scope)
- ❌ Toddler 1-3 year behavior / language (out of scope)
- ❌ Specific medical treatment plans / drug doses (use medical databases)
- ❌ Anything requiring the user's specific family / baby context (this Skill is generic)

## What to load

| Need | Load file |
|---|---|
| Jaundice judgment | `knowledge/decision-trees/baby-jaundice.md` |
| Temperature / heat rash | `knowledge/decision-trees/baby-temperature.md` |
| Gas (intestinal / stomach) | `knowledge/decision-trees/baby-gas.md` |
| Milk powder switch | `knowledge/decision-trees/baby-milk-switch.md` |
| Feeding rhythm 0-1 month | `knowledge/decision-trees/baby-feeding-rhythm.md` |
| Stool observation 0-1 month | `knowledge/decision-trees/baby-stool-observation.md` |
| Spit-up vs choking (0-3 mo) | `knowledge/decision-trees/baby-spit-up-vs-choking.md` |
| Sleep / soothing / night waking (0-3 mo) | `knowledge/decision-trees/baby-sleep.md` |
| Crying triage (0-3 mo) | `knowledge/decision-trees/baby-crying-triage.md` |
| Nail trimming (0-3 mo) | `knowledge/decision-trees/baby-nail-trimming.md` |
| Umbilical cord care (0-4 wk) | `knowledge/decision-trees/baby-umbilical-cord.md` |
| Information sources (CN region) | `references/info-sources.md` |
| Chinese version | append `.zh` before `.md` |

## Privacy iron rule (DO NOT violate)

- ❌ Personal experience phrasing ("我娃", "我家宝宝", "what I encountered")
- ❌ Specific hospital / doctor / city / region names
- ❌ Specific dates — use "day X after birth" not "2026-09-01"
- ❌ Specific numeric values (e.g. "jaundice value 12" → "moderately elevated")
- ❌ Any real name ("Mom / Baby" are placeholders, not real names)
- ❌ Any identity information (medical insurance number / ID / address / phone)

When user provides personal context, **package as general experience** into
`experiences/` and **automatically desensitize** (perspective shifts from
"my baby" to "newborn baby").

## When answering

1. **Always lead with the red flag signals** — items marked "see doctor immediately" take priority over all experience.
2. **Cite the data source** — public medical guidelines (WHO / China NHC / UpToDate / AAP).
3. **Stay framework-level** — don't recite specific drug doses or threshold curves (use medical DBs).
4. **Recommend doctor visit for** any red flag signal, not at user's risk assessment.
5. **Use the 4-piece format** for each scenario: 5-step judgment + 7 red flags + 5 common myths + quick check.

## Language switching

Default is English (`*.md`). Chinese version is `*.zh.md`. When user writes in
Chinese, prefer loading the Chinese file; otherwise use English.

See [README.md](README.md) for the full project structure and
[references/info-sources.md](references/info-sources.md) for external
information sources.

---

**Maintainer**: maintained by a single contributor.  
**Contributing**: see [CONTRIBUTING.md](CONTRIBUTING.md).  
**Security / medical-content issues**: see [SECURITY.md](SECURITY.md).
