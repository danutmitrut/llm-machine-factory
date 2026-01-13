# Ce sunt Mașinile Metacognitive?

## Definiție simplă

O **Mașină Metacognitivă** este un set structurat de instrucțiuni (metaprompt) care transformă un LLM dintr-un generator de text într-un **sistem de raționament transparent și verificabil**.

---

## Analogia

Gândește-te la diferența dintre:

| A cere cuiva să răspundă | A cere cuiva să gândească în fața ta și apoi să răspundă |
|--------------------------|----------------------------------------------------------|
| "Care e soluția?" | "Arată-mi cum analizezi problema, pas cu pas, și apoi dă-mi soluția" |

Mașinile Metacognitive implementează a doua variantă - forțează LLM-ul să **arate procesul**, nu doar rezultatul.

---

## De ce "Metacognitive"?

**Meta** = despre sine
**Cognitive** = gândire

O mașină metacognitivă este un sistem care **gândește despre cum gândește**:
- Își pune întrebări
- Își evaluează răspunsurile
- Își corectează direcția
- Își declară incertitudinile

---

## Componentele unei Mașini Metacognitive

Fiecare mașină conține:

### 1. Rol și Context
Cine "este" LLM-ul în această interacțiune și ce încearcă să realizeze.

### 2. Principiul Continuității Cognitive
Regula că fiecare pas trebuie să se construiască pe pașii anteriori - fără "săriri" la concluzie.

### 3. Workflow Structurat
Pașii exacți pe care LLM-ul trebuie să-i urmeze:
- Iterații de raționament
- Puncte de verificare
- Momente de sincronizare cu utilizatorul

### 4. Tipuri de Raționament
Instrucțiuni pentru cum să gândească:
- Descompunere fundamentală
- Analogii inter-domenii
- Explorare contraintuitivă
- Raționament cauză-efect

### 5. Filtre Anti-Halucinație
Mecanisme integrate pentru:
- Verificare internă (consistență logică)
- Verificare externă (căutare web, cerere de dovezi)
- Declararea incertitudinilor

### 6. Format de Output
Cum arată rezultatul final - structurat, acționabil, transparent.

---

## Exemplu concret

**Prompt clasic:**
```
Ce strategie ar trebui să folosesc pentru a-mi lansa startup-ul?
```

**Cu Mașină Metacognitivă (Arhitect de Soluții V2.3):**
```
Iterația 1: Descompunere Fundamentală
- Întrebare internă: Care sunt componentele esențiale ale unui "launch"?
- Concluzie: Produs, audiență, canal, timing, mesaj

Iterația 2: Identificare Constrângeri
- Întrebare internă: Ce nu știu despre contextul specific?
- Concluzie: Nu cunosc: industria, bugetul, echipa, stadiul produsului

[PUNCT DE SINCRONIZARE]
Am nevoie de clarificări: În ce industrie ești? Ce buget ai? ...

Iterația 3-7: [continuă după răspunsul utilizatorului]

Soluție Finală: [plan structurat, cu justificare pentru fiecare recomandare]
```

Diferența e evidentă: în loc de un răspuns generic, primești un **proces de gândire documentat** care duce la o soluție personalizată.

---

## Următorul pas

→ [De ce sunt mai mult decât prompturi?](de-ce-mai-mult.md)
