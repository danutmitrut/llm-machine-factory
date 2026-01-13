# How AIM Works

## AIM Architecture

AIM is structured into **7 modules** that execute sequentially:

```
┌─────────────────────────────────────────────────────────────┐
│                         AIM V1.0                            │
├─────────────────────────────────────────────────────────────┤
│  Module 1: Requirements Collection (Questions 1-3)          │
│     ↓                                                       │
│  Module 2: Sync Point 1 - General Vision                   │
│     ↓                                                       │
│  Module 3: Define Reasoning & Filters (Questions 4-5)       │
│     ↓                                                       │
│  Module 4: Sync Point 2 - Cognitive Architecture           │
│     ↓                                                       │
│  Module 5: Operational Details (Questions 6-7)              │
│     ↓                                                       │
│  Module 6: Sync Point 3 - Final Confirmation               │
│     ↓                                                       │
│  Module 7: Final Metaprompt Generation                      │
└─────────────────────────────────────────────────────────────┘
```

---

## Module Details

### Module 1: Initial Requirements Collection

AIM asks the first 3 fundamental questions:

**Question 1:** What is the main purpose?
- What should the machine do?
- What final result do you want?

**Question 2:** What type of input?
- What will the machine receive from the user?
- Free text? Structured data? Documents?

**Question 3:** What output format?
- How do you want the result to look?
- List? Table? JSON? Structured report?

---

### Module 2: Sync Point 1 - General Vision

```
[SYNCHRONIZATION POINT 1: General Vision of the LLM Machine]

Progress Summary: I understand that the new LLM Machine will have
the purpose of: "[answer to question 1]". It will receive input
of type: "[answer to question 2]" and will generate output in
format: "[answer to question 3]".

Question: Is this understanding correct? Are there adjustments
or clarifications you'd like to make?
```

**Why it matters:** Prevents divergence. If AIM misunderstood something, you correct it now, not at the end.

---

### Module 3: Define Reasoning and Filters

**Question 4:** What types of advanced reasoning?

Available options:
- Cross-domain analogies
- Counterintuitive exploration
- Cause-effect reasoning
- Fundamental decomposition
- Creative synthesis
- All of the above

**Question 5:** What anti-hallucination filters?

Options:
- Proactive filters (from "Safe Generation") - real-time verification
- Verification modules (from "Veracity Auditor") - post-generation audit
- Both
- None (for creative tasks where precision is less critical)

---

### Module 4: Sync Point 2 - Cognitive Architecture

```
[SYNCHRONIZATION POINT 2: Cognitive Architecture]

Progress Summary: We've established that the LLM Machine will
prioritize reasoning of type: "[answer to question 4]".
Additionally, it will include: "[answer to question 5]".

Question: Is this the desired configuration for the thinking
and validation process of the LLM Machine?
```

---

### Module 5: Operational Details

**Question 6:** Synchronization points?

- Do you want the generated machine to have sync points?
- If yes, where in the workflow?
  - After initial analysis?
  - Before the final solution?
  - At major decision forks?

**Question 7:** Constraints and success criteria?

- Maximum response length?
- Formal/informal tone?
- Available resources?
- How do you measure output success?

---

### Module 6: Sync Point 3 - Final Confirmation

```
[SYNCHRONIZATION POINT 3: Final Design Confirmation]

General Summary of the LLM Machine:
I've consolidated all decisions regarding:
- Purpose: [...]
- Input: [...]
- Output: [...]
- Reasoning: [...]
- Filters: [...]
- Synchronizations: [...]
- Constraints: [...]

Question: Do you agree with the final design? Are you ready
for us to generate the complete metaprompt?
```

---

### Module 7: Final Generation

After confirmation, AIM generates:

1. **Complete metaprompt** - structured, formatted, ready to copy
2. **Usage instructions** - how to use it
3. **Machine name** - auto-generated (e.g., "IT Risk Analyzer V1.0")

---

## Design Principles

### Why 3 synchronizations?

- **Sync 1:** Prevents fundamental divergence
- **Sync 2:** Confirms the machine's "brain"
- **Sync 3:** Last chance for adjustment before generation

### Why sequential questions?

Each question builds on previous answers. You can't define reasoning (question 4) without knowing the purpose (question 1).

---

## Next Step

→ [AIM - Complete Machine (copy-paste ready)](aim-complete.md)
