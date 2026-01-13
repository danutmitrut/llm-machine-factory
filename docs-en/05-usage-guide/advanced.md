# Advanced Guide

Customization, optimization, and advanced techniques.

---

## Customizing Machines

### Modification: Number of Iterations

**Default:** 5-15 iterations

**For simple problems:**
```
Iterative Internal Reasoning Generation (3-7 iterations)
```

**For very complex problems:**
```
Iterative Internal Reasoning Generation (10-20 iterations)
```

### Modification: Reasoning Types

**Add a new type:**
```
* Bayesian Reasoning: Update probabilities based on new
  evidence. What is the probability now vs. before?
```

**Remove a type** (if not relevant for the domain):
Delete the corresponding section from the workflow.

### Modification: Tone and Style

**Add at the end of instructions:**
```
**Style Constraints:**
- Tone: Professional but accessible
- Avoid: Unexplained technical jargon
- Maximum length: 1500 words
- Language: Clear, no unnecessary complexity
```

---

## Building Specialized Machines

### Base Template

Use this structure for any new machine:

```
**[Start Metaprompt - [NAME] V1.0]**

**Instructions for AI (You):**
You are a [ROLE], specialized in [SPECIALIZATION]. Your mission is
to [MISSION]. You will do this through [METHOD].

**Supreme Objective:** [WHAT IT MUST PRODUCE]

**Cognitive Continuity Principle:** [ALWAYS INCLUDE]

**Detailed Workflow:**
1. **Reception:** [HOW IT RECEIVES INPUT]
2. **Processing:** [REASONING STEPS]
3. **Verification:** [ANTI-HALLUCINATION FILTERS]
4. **Output:** [FINAL FORMAT]

**Final Output Format:** [STRUCTURE]

**[End Metaprompt - [NAME] V1.0]**
```

### Example: Competitive Analysis Machine

```
**[Start Metaprompt - Competitive Analyzer V1.0]**

**Instructions for AI (You):**
You are a Competitive Analyst, specialized in evaluating
companies' market position. Your mission is to identify
competitive advantages, vulnerabilities, and strategic opportunities.

**Supreme Objective:** Generating an actionable competitive analysis
report with concrete recommendations.

**Cognitive Continuity Principle:** Each conclusion is based
exclusively on previously analyzed data. Do not assume.

**Detailed Workflow:**

1. **Input Reception:**
   You receive: Company name + industry + 2-3 main competitors

2. **Iterative Analysis (7-10 iterations):**
   - Iterations 1-2: Identify value proposition
   - Iterations 3-4: Analyze strengths/weaknesses vs. competitors
   - Iterations 5-6: Identify market trends
   - Iterations 7-8: Synthesize opportunities and threats
   - Iterations 9-10: Formulate recommendations

3. **Verification:**
   [Action: Web Search] to validate key information

4. **Output:** Structured report with clear sections

**Final Output Format:**
- Executive Summary (3 bullet points)
- Detailed Analysis (comparative table)
- Strategic Recommendations (5 prioritized actions)
- Risks and Limitations

**[End Metaprompt - Competitive Analyzer V1.0]**
```

---

## Performance Optimization

### Reducing Hallucinations

**Add explicit instructions:**
```
**Anti-Hallucination Rules:**
1. If you don't know a fact, say "I don't have information about..."
2. Statistics require a source - if you don't have a source, don't cite statistics
3. Prefix uncertainties with "Probably..." or "Possibly..."
4. Clearly distinguish between verified facts and inferences
```

### Improving Relevance

**Add domain context:**
```
**Domain Context:**
This machine is intended for [INDUSTRY/DOMAIN].
Specific terms: [SHORT GLOSSARY]
Valid assumptions in this context: [LIST]
```

### Accelerating the Process

**For faster responses:**
```
**Speed Optimization:**
- Compact iterations (2-3 sentences per iteration)
- Group related iterations
- Skip synchronization point for clear problems
```

---

## Debugging Machines

### Problem: Output too generic

**Probable cause:** Instructions not specific enough

**Solution:** Add concrete examples:
```
**Example of Good Output:**
[Include a real example of what it should look like]
```

### Problem: Gets stuck / incomplete responses

**Probable cause:** Too many conflicting instructions

**Solution:** Simplify - remove redundant instructions

### Problem: Ignores synchronization point

**Probable cause:** Not explicit enough

**Solution:** Add:
```
**MANDATORY:** You will STOP at the synchronization point and
WAIT for the user's response before continuing.
Do not generate anything after synchronization until you receive input.
```

### Problem: Hallucinates despite filters

**Probable cause:** LLM doesn't have web search access

**Solution:** If using an LLM without web access, modify:
```
Instead of [Action: Web Search], declare:
"I cannot verify this information. I recommend independent
verification for: [list of elements to verify]"
```

---

## Versioning and Iteration

### Versioning Convention

```
V1.0 - First functional version
V1.1 - Bug fix / minor adjustment
V2.0 - Major functionality change
```

### Document Changes

For each new version, note:
```
**Changelog V1.1:**
- Added: [what was added]
- Modified: [what changed]
- Removed: [what was removed]
- Motivation: [why]
```

### Keep Previous Versions

Don't overwrite - keep V1.0 when making V1.1. You might need to go back.

---

## Next Step

→ [Integration in assistants and agents](integration.md)
