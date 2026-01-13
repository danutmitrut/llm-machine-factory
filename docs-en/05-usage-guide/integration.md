# Integration in Assistants and Agents

How to use Metacognitive Machines in tools, custom assistants, and AI agents.

---

## Custom GPTs (OpenAI)

### How to create a GPT with integrated machine

1. **Go to** chat.openai.com → Explore GPTs → Create
2. **In "Instructions"**, paste the complete metaprompt
3. **In "Conversation starters"**, add:
   - "I have a problem to solve"
   - "I want to analyze something together"
   - "Help me make a decision"
4. **Save** and publish (or keep private)

### Tips for Custom GPTs

**Add at the beginning of instructions:**
```
You are [GPT NAME]. You use the Metacognitive Machines method
to provide superior quality responses.

When the user starts a conversation, greet them and ask
what problem you can help with.
```

**To force machine usage:**
```
IMPORTANT: For ANY complex question, you MUST use the
iterative process described below. Do not respond directly.
```

---

## Claude Projects

### Integration in Project Knowledge

1. **Create a new project** in Claude
2. **In Project Knowledge**, upload the metaprompt as a .txt file
3. **In Project Instructions**, write:
   ```
   When the user has a complex problem, use the
   methodology from the attached "machine-X.txt" file.
   ```

### Custom Instructions for Claude

In Custom Instructions settings, you can add:
```
For complex problems, I use the iterative reasoning method
with verification. Each conclusion builds on previous
steps. I include synchronization points to
ensure I'm on the right track.
```

---

## API Integration

### OpenAI API

```python
import openai

# Metaprompt as system message
system_prompt = """
[PASTE COMPLETE METAPROMPT HERE]
"""

response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": system_prompt},
        {"role": "user", "content": "My problem is: ..."}
    ],
    temperature=0.7,  # Balance creativity/consistency
    max_tokens=4000   # Enough for iterations
)
```

### Anthropic API (Claude)

```python
import anthropic

client = anthropic.Anthropic()

system_prompt = """
[PASTE COMPLETE METAPROMPT HERE]
"""

message = client.messages.create(
    model="claude-3-opus-20240229",
    max_tokens=4000,
    system=system_prompt,
    messages=[
        {"role": "user", "content": "My problem is: ..."}
    ]
)
```

---

## AI Agents

### LangChain

```python
from langchain.agents import initialize_agent
from langchain.chat_models import ChatOpenAI

# Machine as tool
solutions_machine = Tool(
    name="Solutions Architect",
    description="Use for complex problems requiring deep reasoning",
    func=lambda x: run_machine(x, METAPROMPT_ARCHITECT)
)

# Agent with integrated machine
agent = initialize_agent(
    tools=[solutions_machine, auditor_machine],
    llm=ChatOpenAI(model="gpt-4"),
    agent="zero-shot-react-description"
)
```

### Typical workflow for agents

```
┌─────────────────────────────────────────────────────────────┐
│                        AGENT                                │
├─────────────────────────────────────────────────────────────┤
│  1. Receives task from user                                 │
│  2. Decides: Is it simple or complex?                       │
│     │                                                       │
│     ├─ Simple → Respond directly                            │
│     │                                                       │
│     └─ Complex → Invoke Metacognitive Machine               │
│                 │                                           │
│                 ├─ Solutions Architect (solving)            │
│                 │                                           │
│                 └─ Auditor (verification)                   │
│                                                             │
│  3. Return verified result                                  │
└─────────────────────────────────────────────────────────────┘
```

---

## Automations (Make, Zapier, n8n)

### Make.com

1. **HTTP Module** → POST to OpenAI/Anthropic API
2. **Body:**
   ```json
   {
     "model": "gpt-4",
     "messages": [
       {"role": "system", "content": "{{METAPROMPT}}"},
       {"role": "user", "content": "{{INPUT_FROM_TRIGGER}}"}
     ]
   }
   ```
3. **Parse response** and send forward

### n8n

Similar to Make, but with native nodes for OpenAI:
- Node: OpenAI Chat
- System Prompt: [The metaprompt]
- User Message: [Variable from trigger]

---

## Production Considerations

### Token usage

Machines consume more tokens than simple prompts:
- Input: ~1500-2500 tokens (the metaprompt)
- Output: ~2000-4000 tokens (iterations + solution)

**Optimization:**
- Use "lite" versions for simple cases
- Cache the metaprompt if the API allows

### Rate limiting

Iterations can take 30-60 seconds for complex problems.
- Set appropriate timeouts
- Implement retry logic

### Cost estimation

Per request with Metacognitive Machine:
- GPT-4: ~$0.15-0.30
- Claude Opus: ~$0.20-0.40
- GPT-3.5/Claude Haiku: ~$0.01-0.03 (but lower quality)

---

## Template: System Prompt for Assistant

```
# Assistant with Metacognitive Machines

You are an intelligent assistant that uses advanced
reasoning techniques to provide superior quality responses.

## How you work

1. For SIMPLE questions (definitions, factual information):
   - Respond directly and concisely
   - Don't use the iterative process

2. For COMPLEX problems (decisions, analyses, strategies):
   - Use the iterative reasoning process
   - Show me the thinking step by step
   - Include synchronization point if there are forks
   - Verify key claims

## Process for complex problems

[PASTE WORKFLOW FROM SOLUTIONS ARCHITECT HERE]

## How to address me

- Be professional but friendly
- Explain jargon when you use it
- Provide concrete examples
- Explicitly declare uncertainties
```

---

## Next Step

→ [Glossary of terms](../06-reference/glossary.md)
