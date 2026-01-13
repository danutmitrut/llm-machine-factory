# How to Combine Them - Advanced Workflows

The machines in this package are **modular** - they can be combined for better results.

---

## Combination 1: Verified Solution

**Scenario:** You have a complex problem and want a solution you can trust.

```
┌─────────────────────┐     ┌─────────────────────┐
│     Solutions       │ ──► │      Veracity       │
│     Architect       │     │       Auditor       │
│       V2.3          │     │                     │
└─────────────────────┘     └─────────────────────┘
     Generates                    Verifies
     the solution              for hallucinations
```

**Steps:**
1. Use the Solutions Architect for your problem
2. Copy the generated solution
3. Submit it to the Veracity Auditor
4. Receive a report on what's verified and what needs attention

**When:** Business decisions, client analyses, important reports

---

## Combination 2: Refinement Cycle

**Scenario:** You want to iterate until the solution is perfect.

```
┌─────────────────────┐
│     Solutions       │
│     Architect       │
│       V2.3          │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│      Veracity       │
│       Auditor       │
└─────────┬───────────┘
          │
          ▼ (if score > 2)
┌─────────────────────┐
│     Solutions       │◄─── With feedback
│     Architect       │     from audit
│   (re-generation)   │
└─────────────────────┘
```

**Steps:**
1. Generate the initial solution
2. Audit it
3. If risk score > 2, regenerate with context:
   - "The previous solution had these problems: [from audit]"
   - "Generate a corrected version that addresses: [problems]"
4. Audit again
5. Repeat until score < 2

**When:** Critical documents, research, irreversible decisions

---

## Combination 3: Factory + Production

**Scenario:** You build a new machine and test it immediately.

```
┌─────────────────────┐     ┌─────────────────────┐
│        AIM          │ ──► │     New Machine     │
│     (you build)     │     │     (you test)      │
└─────────────────────┘     └─────────────────────┘
          │                           │
          └───────────────────────────┘
                    feedback
            (adjust machine if needed)
```

**Steps:**
1. Use AIM to build a new machine
2. Test the machine with a real case
3. If the result isn't satisfactory:
   - Note what doesn't work
   - Return to AIM with feedback
   - Adjust specifications
4. Regenerate and retest

**When:** Developing machines for clients, new products

---

## Combination 4: Pre-Publication Audit

**Scenario:** You've generated content and want to verify it before publishing.

```
┌─────────────────────┐     ┌─────────────────────┐
│   Any AI content    │ ──► │      Veracity       │
│     generator       │     │       Auditor       │
└─────────────────────┘     └─────────────────────┘
```

**Works with:**
- Articles generated with ChatGPT
- Responses from Claude
- Any AI output

**Steps:**
1. Generate content with any AI tool
2. Copy the output
3. Send it to the Auditor
4. Manually correct what's flagged

**When:** Blogging, documentation, external communication

---

## Anti-patterns (What NOT to do)

### Don't combine in parallel
```
❌ Wrong: Send the same problem to 2 machines simultaneously
✓ Correct: Sequential - one after another
```
The machines are designed to work on each other's output, not on the same input.

### Don't skip audit for important decisions
```
❌ Wrong: Solutions Architect → Direct implementation
✓ Correct: Solutions Architect → Auditor → Implementation
```
5 minutes of auditing can prevent hours of corrections.

### Don't rebuild machines from scratch
```
❌ Wrong: You want a slightly different variant → build from scratch with AIM
✓ Correct: Manually modify the existing metaprompt
```
If the machine is 80% what you want, edit directly.

---

## Workflow templates

### For consulting:
```
Client problem → Solutions Architect → Auditor → Delivery
```

### For research:
```
Question → Solutions Architect → Auditor → Architect (refinement) → Auditor → Final Report
```

### For product development:
```
Need → AIM (build machine) → Test → Adjustment → Deliver to client
```

---

## Next Step

→ [Project History](../04-project-history/evolution.md) - how these machines were born
