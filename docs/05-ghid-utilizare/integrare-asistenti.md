# Integrare în asistenți și agenți

Cum să folosești mașinile metacognitive în tools, asistenți custom și agenți AI.

---

## Custom GPTs (OpenAI)

### Cum să creezi un GPT cu mașina integrată

1. **Du-te la** chat.openai.com → Explore GPTs → Create
2. **În "Instructions"**, lipește metapromptul complet
3. **În "Conversation starters"**, adaugă:
   - "Am o problemă de rezolvat"
   - "Vreau să analizăm ceva împreună"
   - "Ajută-mă să iau o decizie"
4. **Salvează** și publică (sau păstrează privat)

### Tips pentru Custom GPTs

**Adaugă la începutul instrucțiunilor:**
```
Tu ești [NUME GPT]. Folosești metoda Mașinilor Metacognitive
pentru a oferi răspunsuri de calitate superioară.

Când utilizatorul începe o conversație, salută-l și întreabă
cu ce problemă îl poți ajuta.
```

**Pentru a forța folosirea mașinii:**
```
IMPORTANT: Pentru ORICE întrebare complexă, TREBUIE să folosești
procesul iterativ descris mai jos. Nu răspunde direct.
```

---

## Claude Projects

### Integrare în Project Knowledge

1. **Creează un proiect nou** în Claude
2. **În Project Knowledge**, uploadează metapromptul ca fișier .txt
3. **În Project Instructions**, scrie:
   ```
   Când utilizatorul are o problemă complexă, folosește
   metodologia din fișierul "masina-X.txt" atașat.
   ```

### Custom Instructions pentru Claude

În setările de Custom Instructions, poți adăuga:
```
Pentru probleme complexe, folosesc metoda raționamentului
iterativ cu verificare. Fiecare concluzie se bazează pe
pașii anteriori. Includ puncte de sincronizare pentru
a mă asigura că sunt pe direcția corectă.
```

---

## API integration

### OpenAI API

```python
import openai

# Metapromptul ca system message
system_prompt = """
[LIPESTE METAPROMPTUL COMPLET AICI]
"""

response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": system_prompt},
        {"role": "user", "content": "Problema mea este: ..."}
    ],
    temperature=0.7,  # balanță creativitate/consistență
    max_tokens=4000   # suficient pentru iterații
)
```

### Anthropic API (Claude)

```python
import anthropic

client = anthropic.Anthropic()

system_prompt = """
[LIPESTE METAPROMPTUL COMPLET AICI]
"""

message = client.messages.create(
    model="claude-3-opus-20240229",
    max_tokens=4000,
    system=system_prompt,
    messages=[
        {"role": "user", "content": "Problema mea este: ..."}
    ]
)
```

---

## Agenți AI

### LangChain

```python
from langchain.agents import initialize_agent
from langchain.chat_models import ChatOpenAI

# Mașina ca tool
masina_solutii = Tool(
    name="Arhitect solutii",
    description="Folosește pentru probleme complexe care necesită raționament profund",
    func=lambda x: run_masina(x, METAPROMPT_ARHITECT)
)

# Agent cu mașina integrată
agent = initialize_agent(
    tools=[masina_solutii, masina_auditor],
    llm=ChatOpenAI(model="gpt-4"),
    agent="zero-shot-react-description"
)
```

### Workflow tipic pentru agenți

```
┌─────────────────────────────────────────────────────────────┐
│                        AGENT                                │
├─────────────────────────────────────────────────────────────┤
│  1. Primește task de la user                                │
│  2. Decide: e simplu sau complex?                           │
│     │                                                       │
│     ├─ Simplu → răspunde direct                            │
│     │                                                       │
│     └─ Complex → invocă mașina metacognitivă               │
│                 │                                           │
│                 ├─ Arhitect soluții (rezolvare)            │
│                 │                                           │
│                 └─ auditor (verificare)                    │
│                                                             │
│  3. Returnează rezultat verificat                           │
└─────────────────────────────────────────────────────────────┘
```

---

## Automatizări (Make, Zapier, n8n)

### Make.com

1. **HTTP Module** → POST la OpenAI/Anthropic API
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
3. **Parse response** și trimite mai departe

### n8n

Similar cu Make, dar cu noduri native pentru OpenAI:
- Node: OpenAI Chat
- System Prompt: [metapromptul]
- User Message: [variabilă din trigger]

---

## Considerații pentru producție

### Token usage

Mașinile consumă mai mulți tokeni decât prompturi simple:
- Input: ~1500-2500 tokeni (metapromptul)
- Output: ~2000-4000 tokeni (iterații + soluție)

**Optimizare:**
- folosește versiuni "lite" pentru cazuri simple
- cache-uiește metapromptul dacă API-ul permite

### Rate limiting

Iterațiile pot dura 30-60 secunde pentru probleme complexe.
- setează timeout-uri adecvate
- implementează retry logic

### Cost estimation

Per request cu mașină metacognitivă:
- GPT-4: ~$0.15-0.30
- Claude Opus: ~$0.20-0.40
- GPT-3.5/Claude Haiku: ~$0.01-0.03 (dar calitate inferioară)

---

## Template: system prompt pentru asistent

```
# Asistent cu mașini metacognitive

Tu ești un asistent inteligent care folosește tehnici avansate
de raționament pentru a oferi răspunsuri de calitate superioară.

## Cum funcționezi

1. Pentru întrebări SIMPLE (definiții, informații factuale):
   - răspunde direct și concis
   - nu folosi procesul iterativ

2. Pentru probleme COMPLEXE (decizii, analize, strategii):
   - folosește procesul de raționament iterativ
   - arată-mi gândirea pas cu pas
   - include punct de sincronizare dacă sunt bifurcații
   - verifică afirmațiile cheie

## Proces pentru probleme complexe

[LIPESTE AICI WORKFLOW-UL DIN ARHITECT SOLUTII]

## Cum să mă adresezi

- fii profesional dar prietenos
- explică jargonul când îl folosești
- oferă exemple concrete
- declară explicit incertitudinile
```

---

## Următorul pas

→ [Glosar de termeni](../06-referinte/glosar.md)
