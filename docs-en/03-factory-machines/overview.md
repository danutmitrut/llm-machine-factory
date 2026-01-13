# Factory Machines - Overview

## The Machine Ecosystem

LLM Machine Factory includes **3 main machines** + **1 factory** (AIM):

```
┌─────────────────────────────────────────────────────────────┐
│                    LLM MACHINE FACTORY                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│   ┌─────────────────────────────────────────────────────┐   │
│   │          AIM - Machine Factory                      │   │
│   │     (Intelligent Metaprompt Architect)              │   │
│   └──────────────────────┬──────────────────────────────┘   │
│                          │                                  │
│            ┌─────────────┼─────────────┐                    │
│            ▼             ▼             ▼                    │
│   ┌────────────┐ ┌──────────────┐ ┌────────────┐            │
│   │ Solutions  │ │   Veracity   │ │   Meta-    │            │
│   │ Architect  │ │   Auditor    │ │ Cognitive  │            │
│   │   V2.3     │ │    V1.0      │ │ Architect  │            │
│   └────────────┘ └──────────────┘ └────────────┘            │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## When to use each machine

| You need to... | Use |
|----------------|-----|
| Solve a complex problem | [Solutions Architect V2.3](solutions-architect.md) |
| Verify text for hallucinations | [Veracity Auditor V1.0](veracity-auditor.md) |
| Build a new machine (fast) | [Meta-Cognitive Architect V1.0](meta-cognitive-architect.md) |
| Build a new machine (with control) | [AIM](../02-aim-core/aim-complete.md) |

---

## Brief description of each machine

### Solutions Architect V2.3
**Main reasoning engine**

- Receives a complex problem
- Executes 5-15 internal reasoning iterations
- Includes user synchronization point
- Generates original, actionable, reality-anchored solution

**Key features:**
- Cognitive Continuity Principle
- Integrated web search
- Visible reasoning (see each iteration)

---

### Veracity Auditor V1.0
**Anti-hallucination verifier**

- Receives text to audit
- Segments it into verifiable units
- Verifies each: factual claims, concepts, conclusions
- Generates audit report with scores

**Key features:**
- Web search for factual verification
- Hallucination risk score (0-5)
- Correction suggestions

---

### Meta-Cognitive Architect V1.0
**Automatic machine generator**

- Receives description of desired machine
- Asks 7 key questions
- Generates complete metaprompt

**Difference from AIM:**
- No intermediate synchronization points
- Faster, less control
- For experienced users

---

## Recommended combinations

### For rigorous analysis:
```
Solutions Architect → Veracity Auditor
```
Generate solution, then verify for hallucinations.

### For machine building:
```
AIM (first time) → Meta-Cognitive Architect (for fast iterations)
```
Learn the process with AIM, then accelerate with Meta-Cognitive Architect.

### For important decisions:
```
Solutions Architect → Auditor → Solutions Architect (with feedback)
```
Refinement cycle: generation → verification → regeneration.

---

## Next step

Choose the machine you need:
- → [Solutions Architect V2.3](solutions-architect.md) - solve problems
- → [Veracity Auditor V1.0](veracity-auditor.md) - verify texts
- → [Meta-Cognitive Architect V1.0](meta-cognitive-architect.md) - build machines fast
- → [How to combine them](combining-machines.md) - advanced workflows
