# Beginner's Guide

First steps with Metacognitive Machines.

---

## Before You Start

### What you need:
- Access to Claude or ChatGPT (works with both)
- A problem to solve or text to verify
- 5-10 minutes for the first test

### What you DON'T need:
- Technical knowledge
- Prompt engineering experience
- Paid subscription (works with free versions too)

---

## Your First Test: Solutions Architect

### Step 1: Copy the machine
Go to [Solutions Architect V2.3](../03-factory-machines/solutions-architect.md) and copy all the text between `[Start Metaprompt]` and `[End Metaprompt]`.

### Step 2: Open Claude or ChatGPT
Use the web interface or app.

### Step 3: Paste the metaprompt
As the first message in the conversation, paste all the copied text.

### Step 4: Enter your problem
When the AI asks "please introduce the problem," write your problem.

**Examples of good problems to start:**
- "How can I increase my online sales by 20% in 3 months?"
- "Should I change my career from X to Y?"
- "How can I automate [specific process] in my business?"

### Step 5: Follow the process
You'll see the thinking iterations - each with question, answer, reasoning type.

### Step 6: Respond to synchronization
When `[SYNCHRONIZATION POINT]` appears, the AI asks which direction you prefer. Respond and continue.

### Step 7: Receive the solution
At the end, you'll have a structured solution with justification for each recommendation.

---

## Second Test: Veracity Auditor

Now that you have a solution, let's verify it.

### Step 1: Copy the solution
From the previous conversation, copy the final generated solution.

### Step 2: Open a new conversation
Important: new conversation, not continuation.

### Step 3: Paste the Auditor
Copy the metaprompt from [Veracity Auditor](../03-factory-machines/veracity-auditor.md) and paste it.

### Step 4: Submit the solution for verification
When the AI asks for the text to audit, paste the solution.

### Step 5: Analyze the report
You'll receive:
- General risk score (0-5)
- Verdict for each claim
- Correction suggestions

---

## Common Mistakes to Avoid

### 1. Don't modify the metaprompt
At the beginning, use it exactly as is. Modifications can break functionality.

### 2. Don't skip synchronizations
When the AI asks, answer. Synchronizations exist for a reason.

### 3. Don't expect magic
The machines significantly improve output, but don't make it perfect. Use critical judgment.

### 4. Don't use for simple tasks
For "write me an email," use a simple prompt. Machines are for complex problems.

### 5. Don't ignore declared limitations
If the AI says "I don't have enough information about X," provide the information.

---

## When to Use Which Machine

| Situation | Machine |
|-----------|---------|
| I have a complex problem to solve | Solutions Architect |
| I have text and want to verify it | Veracity Auditor |
| I want to build my own machine | AIM |
| I used AI and I'm not sure about the answer | Veracity Auditor |
| I need deep analysis | Solutions Architect |

---

## Practical Exercises

### Exercise 1: First problem
Use the Solutions Architect for:
> "What are the 3 most important things I should do to improve my productivity?"

Observe how it thinks, how it reaches conclusions.

### Exercise 2: Verification
Take the response from Exercise 1 and verify it with the Auditor.
What score did it get? What needs verification?

### Exercise 3: Problem from your domain
Choose a real problem from your work or life.
Use the Solutions Architect.
Compare the response with what you would have gotten from a simple prompt.

---

## Frequently Asked Questions

### "Does it work with ChatGPT or only Claude?"
Both. The metaprompts are agnostic - they work with any sufficiently capable LLM.

### "Can I modify the machine?"
Yes, after you understand how it works. Start by using it as is.

### "How long does it take to get a response?"
More than a simple prompt (iterations take time), but quality is significantly better. Estimate: 2-5 minutes for a medium problem.

### "What do I do if it gets stuck?"
Start a new conversation and try again. Sometimes the context gets "dirty."

---

## Next Step

You've covered the basics. Now:
- → [Advanced Guide](advanced.md) - customization and optimization
- → [Integration in assistants](integration.md) - how to use them in tools and agents
