# AIM - Intelligent Metaprompt Architect

## What is AIM?

AIM is **the factory that builds factories**.

It's a metaprompt that, through guided dialogue with you, generates other personalized metaprompts (LLM machines) for your specific needs.

---

## Why is AIM the core piece?

The other machines in this package (Solutions Architect, Veracity Auditor) are **examples** of what AIM can generate.

With AIM you can create:
- Machines for your specific industry
- Machines for unique workflows
- Machines with personalized reasoning types
- Machines with or without anti-hallucination verification

---

## Difference from Meta-Cognitive Architect

There are two versions of the "machine factory":

| AIM (Co-Creation) | Meta-Cognitive Architect (Automatic) |
|-------------------|--------------------------------------|
| Guided dialogue with user | Initial questions, then automatic generation |
| 3 synchronization points | No intermediate synchronizations |
| Maximum control | Maximum speed |
| For complex machines | For standard machines |

**Recommendation:** Start with AIM. Use Meta-Cognitive Architect only when you have experience and know exactly what you want.

---

## What does AIM do concretely?

### Input
You describe what you want the new machine to do:
- "I want a machine that transforms business ideas into action plans"
- "I need a legal contract analyzer"
- "I want something that generates validated marketing strategies"

### Process
AIM guides you through 7 key questions:
1. What main purpose?
2. What type of input?
3. What output format?
4. What reasoning types?
5. What anti-hallucination filters?
6. Where sync points?
7. What constraints/success criteria?

After each group of questions, AIM does **synchronization** - shows you what it understood and asks for confirmation.

### Output
A complete, structured metaprompt ready to use - your own LLM machine.

---

## When to use AIM?

**Use AIM when:**
- You have a specific need that existing machines don't cover
- You want total control over how the machine works
- You're building for a client or specific project
- You want to learn how machines are built

**You don't need AIM when:**
- Existing machines solve your problem
- You want something quick, without customization

---

## Usage example

**You:** "I want to build a machine for risk analysis in IT projects"

**AIM:**
```
Question 1: What main purpose should this LLM Machine have?
```

**You:** "To receive an IT project description and identify potential risks with probabilities and mitigation strategies"

**AIM:**
```
[SYNCHRONIZATION POINT 1: General Vision]
I understood that the new LLM Machine will have the purpose of:
"risk analysis in IT projects with probability identification
and mitigation strategies"

Is this understanding correct?
```

[...dialogue continues...]

**Final output:** A complete metaprompt for "IT Risk Analyzer V1.0"

---

## Next step

→ [How AIM works in detail](how-it-works.md)
