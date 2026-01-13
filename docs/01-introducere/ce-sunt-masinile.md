# Ce sunt mașinile metacognitive?

## Definiție simplă

O **mașină metacognitivă** este un set structurat de instrucțiuni (metaprompt) care transformă un LLM dintr-un generator de text într-un **sistem de raționament transparent și verificabil**.

---

## Analogia

Gândește-te la diferența dintre:

| A cere cuiva să răspundă | A cere cuiva să gândească în fața ta și apoi să răspundă |
|--------------------------|----------------------------------------------------------|
| "Care e soluția?" | "Arată-mi cum analizezi problema, pas cu pas, și apoi dă-mi soluția" |

Mașinile metacognitive implementează a doua variantă - forțează LLM-ul să **arate procesul**, nu doar rezultatul.

---

## De ce "metacognitive"?

**Meta** = despre sine
**Cognitive** = gândire

O mașină metacognitivă este un sistem care **gândește despre cum gândește**:
- Își pune întrebări
- Își evaluează răspunsurile
- Își corectează direcția
- Își declară incertitudinile

---

## Componentele unei mașini metacognitive

Fiecare mașină conține:

### 1. Rol și context
Cine "este" LLM-ul în această interacțiune și ce încearcă să realizeze.

### 2. Principiul continuității cognitive
Regula că fiecare pas trebuie să se construiască pe pașii anteriori - fără "săriri" la concluzie.

### 3. Workflow structurat
Pașii exacți pe care LLM-ul trebuie să-i urmeze:
- Iterații de raționament
- Puncte de verificare
- Momente de sincronizare cu utilizatorul

### 4. Tipuri de raționament
Instrucțiuni pentru cum să gândească:
- Descompunere fundamentală
- Analogii inter-domenii
- Explorare contraintuitivă
- Raționament cauză-efect

### 5. Filtre anti-halucinație
Mecanisme integrate pentru:
- Verificare internă (consistență logică)
- Verificare externă (căutare web, cerere de dovezi)
- Declararea incertitudinilor

### 6. Format de output
Cum arată rezultatul final - structurat, acționabil, transparent.

---

## Exemplu concret

**Prompt clasic:**
```
Ce strategie ar trebui să folosesc pentru a-mi lansa startup-ul?
```

**Cu mașină metacognitivă (Arhitect de soluții V2.3):**
```
Iterația 1: descompunere fundamentală
- Întrebare internă: care sunt componentele esențiale ale unui "launch"?
- Concluzie: produs, audiență, canal, timing, mesaj

Iterația 2: identificare constrângeri
- Întrebare internă: ce nu știu despre contextul specific?
- Concluzie: nu cunosc: industria, bugetul, echipa, stadiul produsului

[PUNCT DE SINCRONIZARE]
Am nevoie de clarificări: în ce industrie ești? Ce buget ai? ...

Iterația 3-7: [continuă după răspunsul utilizatorului]

Soluție finală: [plan structurat, cu justificare pentru fiecare recomandare]
```

Diferența e evidentă: în loc de un răspuns generic, primești un **proces de gândire documentat** care duce la o soluție personalizată.

---

## Următorul pas

→ [De ce sunt mai mult decât prompturi?](de-ce-mai-mult.md)
