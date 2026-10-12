---
name: newdad-log
description: |
  Newborn / 0-12 month expert knowledge base for any AI agent or new parent.
  Triggered when user asks: "宝宝 X 怎么办" / "newborn X what to do" / "what to
  check when baby has jaundice / gas / fever / rash / feeding issue" / "jaundice
  decision tree" / "stool observation" / "milk formula switch" / "喂奶节奏" /
  "胀气判断" / "黄疸要不要去医院" / "宝宝哭闹" / "needs newborn domain knowledge",
  or any time the conversation touches a 0-12 month scenario and an agent
  needs a quick, structured judgment frame (5-step + 7 red flags + 5 myths +
  quick check). Privacy-strict: zero personal data, all general medical
  consensus, public guidelines (WHO / AAP / 中国卫健委 / UpToDate).
metadata:
  hermes:
    tags: [parenting, newborn, decision-tree, knowledge-base, medical]
    related_skills: [knowledge-skill-authoring]
---

# NewDad Log — Newborn 0-12 month expert knowledge base

A **decision-tree-only** knowledge base. When user asks "what to do when baby
has X" → load the matching tree, walk through 5-step judgment, escalate on
any of 7 red flags, avoid the 5 common myths, end with quick check.

## Quick navigation (decision trees)

| Scenario | Tree | When to load |
|---|---|---|
| 黄疸 / jaundice | [knowledge/decision-trees/baby-jaundice.md](knowledge/decision-trees/baby-jaundice.md) / [.en.md](knowledge/decision-trees/baby-jaundice.en.md) | Skin / sclera yellow, especially day 2-7 |
| 体温 / temperature | [knowledge/decision-trees/baby-temperature.md](knowledge/decision-trees/baby-temperature.md) / [.en.md](knowledge/decision-trees/baby-temperature.en.md) | Fever / room temp / heat rash vs allergy |
| 胀气 / gas | [knowledge/decision-trees/baby-gas.md](knowledge/decision-trees/baby-gas.md) / [.en.md](knowledge/decision-trees/baby-gas.en.md) | Crying with leg-pull, hard belly, 肠胀气 vs 胃胀气 |
| 换奶 / milk switch | [knowledge/decision-trees/baby-milk-switch.md](knowledge/decision-trees/baby-milk-switch.md) / [.en.md](knowledge/decision-trees/baby-milk-switch.en.md) | Changing formula brand / stage |
| 喂奶节奏 / feeding rhythm | [knowledge/decision-trees/baby-feeding-rhythm.md](knowledge/decision-trees/baby-feeding-rhythm.md) / [.en.md](knowledge/decision-trees/baby-feeding-rhythm.en.md) | 0-1 month feeding frequency / amount |
| 便便 / stool | [knowledge/decision-trees/baby-stool-observation.md](knowledge/decision-trees/baby-stool-observation.md) / [.en.md](knowledge/decision-trees/baby-stool-observation.en.md) | Stool color / frequency / texture abnormal |

Full index: [knowledge/_index.md](knowledge/_index.md) / [English](knowledge/_index.en.md)

## How to use this skill (4-piece framework)

Every decision tree in this base follows the **same shape**:

1. **5-step judgment** — walk through 5 ordered checks; if any fails, jump to next branch
2. **7 red flags** — ANY ONE = **seek medical care immediately**, stop reasoning
3. **5 common myths** — what 家长 typically get wrong, correct them
4. **quick check** — copy-paste checklist before responding to user

When the user asks "what to do when X":
- 1 → load the matching tree
- 2 → answer in the 4-piece shape, **never** improvise a structure
- 3 → any red flag mentioned by user → **stop, say "立即就医" first**, then walk the rest
- 4 → end with quick check confirmation

## Privacy iron rule (highest priority)

This is a **public-ready, open-source** knowledge base. **No personal data
ever.** Personal experience stays in user's local `~/.hermes/notes/`, never
in this project, never in git.

Hard no-go (write-time check, before any commit):
- ❌ Real names (baby / mom / doctor / hospital) — only `妈妈` / `宝宝` placeholders
- ❌ Specific dates — use "day X after birth" not "2026-09-01"
- ❌ Specific numeric values from real cases — use qualitative ("moderately
  elevated") not absolute ("jaundice value 12")
- ❌ Personal experience phrasing ("我娃", "我家宝宝", "what I encountered")
- ❌ Identity info (medical insurance / ID / address / phone)

## Disclaimer (mandatory, surface at top of every response)

> ⚠️ **For reference only, does not constitute medical advice.** Follow
> doctor's guidance. For any of the red flags listed in the tree, seek
> medical care immediately. This Skill does NOT replace in-person pediatric
> consultation.

## Scope

- ✅ 0-12 month healthy full-term babies — most common scenarios
- ✅ 备孕 / 孕中 / 产后 0-30 天 family support
- ❌ Premature / allergic / special medical conditions — must follow doctor's advice
- ❌ Acute critical symptoms — call 120 / emergency immediately
- ❌ 1+ year kindergarten stage — out of scope

## Repo layout

```
newdad-log/
├── SKILL.md                            # This file (entry point)
├── README.md / README.en.md            # Project intro
├── knowledge/
│   ├── _index.md / _index.en.md        # Knowledge index
│   └── decision-trees/                 # 6 trees, each EN + ZH pair
└── references/
    └── info-sources.md / .en.md        # CN-region parenting info tools
```

## When NOT to use this skill

- User is asking for **product recommendations** (formula brand, bottle brand) → this base is not a buyer's guide, redirect to references/info-sources.md tools
- User is asking for **their own baby's specific reading** (lab value, growth curve position) → this base has no individual tracking, redirect to local `~/.hermes/notes/`
- User is in a non-Chinese non-English language → translate on the fly, do not assume
- User mentions a red flag → **stop the skill load, prioritize "立即就医"**
