# Contributing to NewDad Log

Thank you for your interest in contributing! NewDad Log is a community
knowledge base for new dads; every contribution helps.

## What we accept

- ✅ **New decision trees** in `knowledge/decision-trees/` (follow the 4-piece format)
- ✅ **Bug fixes / typos** in existing decision trees
- ✅ **Translations** (Chinese → English or vice versa, or other languages)
- ✅ **Updates to references/info-sources.md** when tools change

## What we DON'T accept

- ❌ **Personal experience content** that violates the privacy iron rule
  (see [README.md](README.md) § Privacy)
- ❌ **Specific medical advice** for any user — this is a general knowledge base, not a clinic
- ❌ **Brand / product endorsements** in the main content
- ❌ **Content not backed by public medical sources** (WHO / China NHC / UpToDate / AAP / etc.)

## How to contribute

1. **Fork** the repository
2. **Create a branch** for your contribution: `git checkout -b feat/baby-sleep-tree`
3. **Follow the format** — see existing decision trees for the 4-piece structure
4. **Run privacy check** — `grep -rE "我娃|我朋友|my baby|my friend"` should return 0 (false-positives in negation clauses are OK)
5. **Open a Pull Request** with a clear description of:
   - What scenario you added / fixed
   - Source of medical information (cite guideline name + year)
   - Whether the change applies to English only, Chinese only, or both

## Decision tree format

Every new decision tree should follow:

```markdown
# {Topic} ({age range or context})

> ⚠️ **For reference only, does not constitute medical advice**. Follow doctor's guidance.

## 5-step judgment

1. ...
2. ...
...

## 7 red flags (see doctor immediately)

- ...
- ...
...

## 5 common myths

- ❌ ...
- ❌ ...
...

## quick check

- [ ] ...
- [ ] ...
- [ ] Any 1 of 7 red flags = see doctor immediately
```

## Code of conduct

All contributors are expected to follow our [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
