# What are Metacognitive Machines?

## Simple definition

A **Metacognitive Machine** is a structured set of instructions (metaprompt) that transforms an LLM from a text generator into a **transparent and verifiable reasoning system**.

---

## The analogy

Think about the difference between:

| Asking someone to answer | Asking someone to think in front of you and then answer |
|--------------------------|----------------------------------------------------------|
| "What's the solution?" | "Show me how you analyze the problem, step by step, and then give me the solution" |

Metacognitive Machines implement the second option - they force the LLM to **show the process**, not just the result.

---

## Why "Metacognitive"?

**Meta** = about itself
**Cognitive** = thinking

A metacognitive machine is a system that **thinks about how it thinks**:
- Asks itself questions
- Evaluates its answers
- Corrects its direction
- Declares its uncertainties

---

## Components of a Metacognitive Machine

Each machine contains:

### 1. Role and Context
Who the LLM "is" in this interaction and what it's trying to achieve.

### 2. Cognitive Continuity Principle
The rule that each step must build on previous steps - no "jumping" to conclusions.

### 3. Structured Workflow
The exact steps the LLM must follow:
- Reasoning iterations
- Verification checkpoints
- User synchronization moments

### 4. Reasoning Types
Instructions for how to think:
- Fundamental decomposition
- Cross-domain analogies
- Counterintuitive exploration
- Cause-effect reasoning

### 5. Anti-Hallucination Filters
Integrated mechanisms for:
- Internal verification (logical consistency)
- External verification (web search, evidence requests)
- Uncertainty declaration

### 6. Output Format
What the final result looks like - structured, actionable, transparent.

---

## Concrete example

**Classic prompt:**
```
What strategy should I use to launch my startup?
```

**With Metacognitive Machine (Solutions Architect V2.3):**
```
Iteration 1: Fundamental Decomposition
- Internal question: What are the essential components of a "launch"?
- Conclusion: Product, audience, channel, timing, message

Iteration 2: Constraint Identification
- Internal question: What don't I know about the specific context?
- Conclusion: Unknown: industry, budget, team, product stage

[SYNCHRONIZATION POINT]
I need clarifications: What industry are you in? What's your budget? ...

Iterations 3-7: [continues after user response]

Final Solution: [structured plan, with justification for each recommendation]
```

The difference is evident: instead of a generic answer, you get a **documented thinking process** leading to a personalized solution.

---

## Next step

→ [Why more than prompts?](why-more-than-prompts.md)
