# NewDad Log

> A new-dad perspective **newborn expert knowledge base** —
> Captures the highest-frequency parenting scenarios from pregnancy through age 3,
> so any AI assistant or parent can find "what to do when X happens" in 30 seconds.

🌐 English | [中文](README.zh.md)

---

## What this is

Not a diary. Not a parenting blog. Not a doctor's prescription.
It is a **growing collection of decision trees** — for the scenarios new parents panic about most (baby crying, jaundice, gas, formula switch, rashes), broken down into a **4-piece framework: 5-step judgment + 7 red flags + 5 common myths + quick check**.

**Core value**: **Expert consensus** + **pitfalls new parents fall into** + **routines you won't find by searching online** — combined.

---

## 🎯 Target audience

**Written for**: new dads in the **chaotic first month postpartum** — the must-have knowledge base.

- ✅ Just leveled up to "dad" 0-30 days ago
- ✅ Face baby jaundice / crying / refusing to feed / gas / rashes and don't know what to do
- ✅ Searching at 3 AM and can't tell which source is authoritative
- ✅ Don't want to take detours / want to avoid common pitfalls / want to become a dad who "knows how to parent"

**Not limited to**:

- Moms / nannies / grandmas / postpartum care nurses all benefit equally
- Dads-to-be in pre-pregnancy / pregnancy stage can also read ahead
- 0-12 month scenarios are all covered (currently prioritizing 0-1 month)

**Not for**:

- ❌ "Kindergarten stage" issues above age 1 (out of project scope)
- ❌ Premature / allergic / special medical conditions (follow doctor's advice, outside general knowledge)

---

## Use cases

✅ **Suitable for**:

- New parents (0-12 month babies) making quick judgments on common problems
- AI Agents loading as a newborn-domain Skill
- Family internal use, prenatal training, pediatric clinic knowledge sharing
- Programmers preparing to / upgrading to "dad" building a "parenting tech stack"

❌ **Not suitable for**:

- Premature / allergic / special medical conditions (follow doctor's advice, outside general knowledge)
- Acute critical symptoms (call 120 / seek emergency care immediately)
- Replacing professional pediatric consultations

---

## ⚠️ Disclaimer (Important)

> **All content in this project is for reference only and does not constitute medical advice.**

1. **Does not replace a doctor** — for any health issue, medication decision, or treatment plan, **consult a professional pediatrician in person**.
2. **Data may be outdated** — medical guidelines are continuously updated; this project **does not guarantee** complete reflection of the latest research.
3. **Individual differences** — every baby is different; the methods here **do not guarantee** universal applicability.
4. **Red flag signals** — items marked "seek medical care immediately" in the text take **priority over all experience**.
5. **Usage risk** — any consequences from using this project are borne by the user.
6. **Open source contribution** — any secondary work that cites this content **must retain this disclaimer**.

**Recommendation**: Use this project as a "knowledge map" and "decision aid", **not as a diagnostic basis**.

---

## 🔒 Privacy iron rule (Highest priority) ⭐⭐⭐

> The project's target output is an **open-source Skill** — any personal experience or content with exposure risk **will not be recorded**.

### Absolutely not recorded

- ❌ Any personal experience phrasing like "my baby", "my friend's kid", "what I encountered"
- ❌ Any specific hospital / doctor / city / region name
- ❌ Any specific date (use "day X after birth" instead of "2026-09-01")
- ❌ Any specific numeric value (e.g. "jaundice value 12" → "moderately elevated")
- ❌ Any real name ("Mom / Baby / First baby" are placeholders, not real names)
- ❌ Any identity information (medical insurance number / ID card / address / phone)

### Sedimentation workflow

1. User input **may involve specific scenarios**
2. Reader / maintainer **digests + packages into general experience**
3. ✅ Reflection-type content **only writes how to design the Skill** (no user context)
4. ✅ Personal experience **not recorded in project** — stays in local `~/.hermes/notes/`, no git, no Skill

### Data sources

- Public medical guidelines (WHO / China NHC / UpToDate / AAP)
- General medical consensus
- Industry controversy summaries
- ✅ **Never mixed with personal / family-specific data**

---

## 📁 File structure

```
newdad-log/
├── README.md                          # This file (English, default)
├── README.zh.md                       # 中文版
├── knowledge/                         # General expert knowledge (open-source-ready)
│   ├── _index.md                      # Knowledge index (English, default)
│   ├── _index.zh.md                   # 知识索引（中文版）
│   └── decision-trees/                # "What to do when X happens" decision trees
│       ├── baby-jaundice.md           # Jaundice judgment
│       ├── baby-jaundice.zh.md        # 黄疸判断（中文版）
│       ├── baby-temperature.md        # Temperature, room temp, heat rash vs allergy
│       ├── baby-temperature.zh.md     # 体温监测（中文版）
│       ├── baby-gas.md                # Intestinal gas vs stomach gas
│       ├── baby-gas.zh.md             # 肠胀气/肠绞痛（中文版）
│       ├── baby-milk-switch.md        # Milk powder switch (healthy full-term)
│       ├── baby-milk-switch.zh.md     # 奶粉切换（中文版）
│       ├── baby-feeding-rhythm.md     # Newborn feeding rhythm (0-1 month)
│       ├── baby-feeding-rhythm.zh.md  # 喂养节奏（中文版）
│       ├── baby-stool-observation.md  # Newborn stool observation (0-1 month)
│       └── baby-stool-observation.zh.md # 大便观察（中文版）
├── references/                        # Reference materials & tool list
│   ├── info-sources.md                # Parenting info-gathering tools (CN region)
│   └── info-sources.zh.md             # 资料来源工具清单（中文版）
```

---

## 🛠️ Workflow

### Recording (user-triggered)

- User says "note: xxx" → **stays in local `~/.hermes/notes/`**, not in project
- User says "sediment as skill" → write to `knowledge/decision-trees/xxx.md` (already desensitized)

### Querying (user-triggered)

- User asks "what to do when Z" → check `decision-trees/`
- User says "what was said before" → search chat history (project has no independent `queries/` yet, relies on chat history)

### Open-sourcing the Skill (final)

When the project is finalized (child turns 3 / voluntarily stopped) → write `SKILL.md`. The open-source version **only includes general knowledge + decision trees**, no personal data whatsoever.

---

## 📊 Current accumulation

- **6 decision trees**: jaundice / temperature / gas / milk switch / feeding rhythm / stool observation
- **0 personal cases** (strictly desensitized)
- **0 private data** (privacy iron rule)
- **1 information-source tool list** (Ant Afu / Xiaohongshu / Meiyou etc.) — see [references/info-sources.zh.md](references/info-sources.zh.md)

> Data update: synchronized with this document after each new sediment.

---

## 📜 License

MIT — open-source, free to cite, modify, redistribute.
**Conditions**: retain disclaimer + privacy iron rule + data source attribution.

---

## 🤝 Contributing

Currently **single maintainer** (maintainer + contributor dual perspective).
Welcome:

- Open Issue pointing out medical errors (AI assistants do not replace doctors, please provide authoritative sources)
- Open PR adding decision trees (please follow privacy iron rule + disclaimer template)
- Citing this document (please retain source attribution)

---

**Last updated**: continuously updating  
**Contact**: open an Issue on this repository
