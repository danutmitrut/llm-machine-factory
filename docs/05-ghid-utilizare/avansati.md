# Ghid pentru avansați

Personalizare, optimizare și tehnici avansate.

---

## Personalizarea mașinilor

### Modificare: Număr de iterații

**Default:** 5-15 iterații

**Pentru probleme simple:**
```
Generare Iterativă de Raționament Intern (3-7 iterații)
```

**Pentru probleme foarte complexe:**
```
Generare Iterativă de Raționament Intern (10-20 iterații)
```

### Modificare: Tipuri de raționament

**Adaugă un tip nou:**
```
* Raționament Bayesian: Actualizează probabilitățile pe baza
  dovezilor noi. Care e probabilitatea acum vs. înainte?
```

**Elimină un tip** (dacă nu e relevant pentru domeniu):
Șterge secțiunea corespunzătoare din workflow.

### Modificare: Ton și stil

**Adaugă la sfârșitul instrucțiunilor:**
```
**Constrângeri de Stil:**
- Ton: Profesional dar accesibil
- Evită: Jargon tehnic ne-explicat
- Lungime maximă: 1500 cuvinte
- Limbă: Română, fără anglicisme inutile
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

**Principiul Continuității Cognitive:** [INCLUDE MEREU]

**Workflow Detaliat:**
1. **Receptare:** [CUM PRIMEȘTE INPUT]
2. **Procesare:** [PAȘII DE RAȚIONAMENT]
3. **Verificare:** [FILTRE ANTI-HALUCINAȚIE]
4. **Output:** [FORMAT FINAL]

**Formatul Output-ului Final:** [STRUCTURĂ]

**[Sfârșit Metaprompt - [NUME] V1.0]**
```

### Exemplu: Mașină de Analiză Competitivă

```
**[Început Metaprompt - Analizor Competitiv V1.0]**

**Instrucțiuni pentru AI (Tu):**
Ești un Analist Competitiv, specializat în evaluarea poziției
de piață a companiilor. Misiunea ta este să identifici avantaje
competitive, vulnerabilități și oportunități strategice.

**Obiectivul Suprem:** Generarea unui raport de analiză competitivă
acționabil, cu recomandări concrete.

**Principiul Continuității Cognitive:** Fiecare concluzie se
bazează exclusiv pe datele analizate anterior. Nu presupune.

**Workflow Detaliat:**

1. **Receptare Input:**
   Primești: Numele companiei + industria + 2-3 competitori principali

2. **Analiză Iterativă (7-10 iterații):**
   - Iterația 1-2: Identificare propunere de valoare
   - Iterația 3-4: Analiză puncte forte/slabe vs. competitori
   - Iterația 5-6: Identificare tendințe de piață
   - Iterația 7-8: Sinteză oportunități și amenințări
   - Iterația 9-10: Formulare recomandări

3. **Verificare:**
   [Acțiune: Căutare Web] pentru validarea informațiilor cheie

4. **Output:** Raport structurat cu secțiuni clare

**Formatul Output-ului Final:**
- Executive Summary (3 bullet points)
- Analiză Detaliată (tabel comparativ)
- Recomandări Strategice (5 acțiuni prioritizate)
- Riscuri și Limitări

**[Sfârșit Metaprompt - Analizor Competitiv V1.0]**
```

---

## Optimizarea performanței

### Reducerea halucinațiilor

**Adaugă instrucțiuni explicite:**
```
**Reguli Anti-Halucinație:**
1. Dacă nu știi un fapt, spune "Nu am informații despre..."
2. Statisticile necesită sursă - dacă nu ai sursă, nu cita statistici
3. Prefixează incertitudinile cu "Probabil..." sau "Posibil..."
4. Distinge clar între fapte verificate și inferențe
```

### Îmbunătățirea relevanței

**Adaugă context de domeniu:**
```
**Context de Domeniu:**
Această mașină e destinată pentru [INDUSTRIE/DOMENIU].
Termeni specifici: [GLOSAR SCURT]
Presupuneri valide în acest context: [LISTA]
```

### Accelerarea procesului

**Pentru răspunsuri mai rapide:**
```
**Optimizare Viteză:**
- Iterații compacte (2-3 propoziții per iterație)
- Grupează iterațiile conexe
- Sări punctul de sincronizare pentru probleme clare
```

---

## Debugging mașini

### Problema: Output prea generic

**Cauză probabilă:** Instrucțiuni insuficient de specifice

**Soluție:** Adaugă exemple concrete:
```
**Exemplu de Output Bun:**
[Include un exemplu real de cum ar trebui să arate]
```

### Problema: Se blochează / răspunsuri incomplete

**Cauză probabilă:** Prea multe instrucțiuni conflictuale

**Soluție:** Simplifică - elimină instrucțiunile redundante

### Problema: Ignoră punctul de sincronizare

**Cauză probabilă:** Nu e suficient de explicit

**Soluție:** Adaugă:
```
**OBLIGATORIU:** Te vei OPRI la punctul de sincronizare și
vei AȘTEPTA răspunsul utilizatorului înainte de a continua.
Nu genera nimic după sincronizare până nu primești input.
```

### Problema: Halucinează în ciuda filtrelor

**Cauză probabilă:** LLM-ul nu are acces la căutare web

**Soluție:** Dacă folosești un LLM fără web access, modifică:
```
În loc de [Acțiune: Căutare Web], declară:
"Nu pot verifica această informație. Recomand verificare
independentă pentru: [lista elementelor de verificat]"
```

---

## Versionare și iterație

### Convenție de versionare

```
V1.0 - Prima versiune funcțională
V1.1 - Bug fix / ajustare minoră
V2.0 - Schimbare majoră de funcționalitate
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
