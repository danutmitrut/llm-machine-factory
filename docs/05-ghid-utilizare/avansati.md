# Ghid pentru avansați

Personalizare, optimizare și tehnici avansate.

---

## Personalizarea mașinilor

### Modificare: număr de iterații

**Default:** 5-15 iterații

**Pentru probleme simple:**
```
Generare Iterativă de Raționament Intern (3-7 iterații)
```

**Pentru probleme foarte complexe:**
```
Generare Iterativă de Raționament Intern (10-20 iterații)
```

### Modificare: tipuri de raționament

**Adaugă un tip nou:**
```
* Raționament bayesian: actualizează probabilitățile pe baza
  dovezilor noi. Care e probabilitatea acum vs. înainte?
```

**Elimină un tip** (dacă nu e relevant pentru domeniu):
Șterge secțiunea corespunzătoare din workflow.

### Modificare: ton și stil

**Adaugă la sfârșitul instrucțiunilor:**
```
**Constrângeri de stil:**
- Ton: profesional dar accesibil
- Evită: jargon tehnic ne-explicat
- Lungime maximă: 1500 cuvinte
- Limbă: română, fără anglicisme inutile
```

---

## Construirea de mașini specializate

### Template de bază

Folosește această structură pentru orice mașină nouă:

```
**[Început Metaprompt - [NUME] V1.0]**

**Instrucțiuni pentru AI (Tu):**
Ești un [ROL], specializat în [SPECIALIZARE]. Misiunea ta este
să [MISIUNE]. Vei face acest lucru prin [METODĂ].

**Obiectivul Suprem:** [CE TREBUIE SĂ PRODUCĂ]

**Principiul continuității cognitive:** [INCLUDE MEREU]

**Workflow Detaliat:**
1. **Receptare:** [CUM PRIMEȘTE INPUT]
2. **Procesare:** [PAȘII DE RAȚIONAMENT]
3. **Verificare:** [FILTRE ANTI-HALUCINAȚIE]
4. **Output:** [FORMAT FINAL]

**Formatul Output-ului Final:** [STRUCTURĂ]

**[Sfârșit Metaprompt - [NUME] V1.0]**
```

### Exemplu: mașină de analiză competitivă

```
**[Început Metaprompt - Analizor competitiv V1.0]**

**Instrucțiuni pentru AI (Tu):**
Ești un analist competitiv, specializat în evaluarea poziției
de piață a companiilor. Misiunea ta este să identifici avantaje
competitive, vulnerabilități și oportunități strategice.

**Obiectivul suprem:** generarea unui raport de analiză competitivă
acționabil, cu recomandări concrete.

**Principiul continuității cognitive:** fiecare concluzie se
bazează exclusiv pe datele analizate anterior. Nu presupune.

**Workflow detaliat:**

1. **Receptare input:**
   Primești: numele companiei + industria + 2-3 competitori principali

2. **Analiză iterativă (7-10 iterații):**
   - Iterația 1-2: identificare propunere de valoare
   - Iterația 3-4: analiză puncte forte/slabe vs. competitori
   - Iterația 5-6: identificare tendințe de piață
   - Iterația 7-8: sinteză oportunități și amenințări
   - Iterația 9-10: formulare recomandări

3. **Verificare:**
   [Acțiune: căutare web] pentru validarea informațiilor cheie

4. **Output:** raport structurat cu secțiuni clare

**Formatul output-ului final:**
- Executive summary (3 bullet points)
- Analiză detaliată (tabel comparativ)
- Recomandări strategice (5 acțiuni prioritizate)
- Riscuri și limitări

**[Sfârșit Metaprompt - Analizor competitiv V1.0]**
```

---

## Optimizarea performanței

### Reducerea halucinațiilor

**Adaugă instrucțiuni explicite:**
```
**Reguli anti-halucinație:**
1. Dacă nu știi un fapt, spune "Nu am informații despre..."
2. Statisticile necesită sursă - dacă nu ai sursă, nu cita statistici
3. Prefixează incertitudinile cu "Probabil..." sau "Posibil..."
4. Distinge clar între fapte verificate și inferențe
```

### Îmbunătățirea relevanței

**Adaugă context de domeniu:**
```
**Context de domeniu:**
Această mașină e destinată pentru [INDUSTRIE/DOMENIU].
Termeni specifici: [GLOSAR SCURT]
Presupuneri valide în acest context: [LISTA]
```

### Accelerarea procesului

**Pentru răspunsuri mai rapide:**
```
**Optimizare viteză:**
- Iterații compacte (2-3 propoziții per iterație)
- Grupează iterațiile conexe
- Sări punctul de sincronizare pentru probleme clare
```

---

## Debugging mașini

### Problema: output prea generic

**Cauză probabilă:** instrucțiuni insuficient de specifice

**Soluție:** adaugă exemple concrete:
```
**Exemplu de output bun:**
[Include un exemplu real de cum ar trebui să arate]
```

### Problema: se blochează / răspunsuri incomplete

**Cauză probabilă:** prea multe instrucțiuni conflictuale

**Soluție:** simplifică - elimină instrucțiunile redundante

### Problema: ignoră punctul de sincronizare

**Cauză probabilă:** nu e suficient de explicit

**Soluție:** adaugă:
```
**OBLIGATORIU:** Te vei OPRI la punctul de sincronizare și
vei AȘTEPTA răspunsul utilizatorului înainte de a continua.
Nu genera nimic după sincronizare până nu primești input.
```

### Problema: halucinează în ciuda filtrelor

**Cauză probabilă:** LLM-ul nu are acces la căutare web

**Soluție:** dacă folosești un LLM fără web access, modifică:
```
În loc de [Acțiune: căutare web], declară:
"Nu pot verifica această informație. Recomand verificare
independentă pentru: [lista elementelor de verificat]"
```

---

## Versionare și iterație

### Convenție de versionare

```
V1.0 - prima versiune funcțională
V1.1 - bug fix / ajustare minoră
V2.0 - schimbare majoră de funcționalitate
```

### Documentează schimbările

La fiecare versiune nouă, notează:
```
**Changelog V1.1:**
- Adăugat: [ce s-a adăugat]
- Modificat: [ce s-a schimbat]
- Eliminat: [ce s-a scos]
- Motivație: [de ce]
```

### Păstrează versiunile anterioare

Nu suprascrie - păstrează V1.0 când faci V1.1. S-ar putea să ai nevoie să revii.

---

## Următorul pas

→ [Integrare în asistenți și agenți](integrare-asistenti.md)
