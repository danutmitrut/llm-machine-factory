# Cum funcționează AIM

## Arhitectura AIM

AIM este structurat în **7 module** care se execută secvențial:

```
┌─────────────────────────────────────────────────────────────┐
│                         AIM V1.0                            │
├─────────────────────────────────────────────────────────────┤
│  Modul 1: Colectare Necesități (Întrebări 1-3)             │
│     ↓                                                       │
│  Modul 2: Sincronizare 1 - Viziunea Generală               │
│     ↓                                                       │
│  Modul 3: Definire Raționament & Filtre (Întrebări 4-5)    │
│     ↓                                                       │
│  Modul 4: Sincronizare 2 - Arhitectura Cognitivă           │
│     ↓                                                       │
│  Modul 5: Detalii Operaționale (Întrebări 6-7)             │
│     ↓                                                       │
│  Modul 6: Sincronizare 3 - Confirmare Finală               │
│     ↓                                                       │
│  Modul 7: Generare Finală Metaprompt                       │
└─────────────────────────────────────────────────────────────┘
```

---

## Detaliu pe module

### Modul 1: Colectare Necesități Inițiale

AIM adresează primele 3 întrebări fundamentale:

**Întrebarea 1:** Ce scop principal?
- Ce trebuie să facă mașina?
- Ce rezultat final vrei?

**Întrebarea 2:** Ce tip de input?
- Ce va primi mașina de la utilizator?
- Text liber? Date structurate? Documente?

**Întrebarea 3:** Ce format de output?
- Cum vrei să arate rezultatul?
- Listă? Tabel? JSON? Raport structurat?

---

### Modul 2: Sincronizare 1 - Viziunea Generală

```
[PUNCT DE SINCRONIZARE 1: Viziunea Generală a Mașinii LLM]

Sumar Progres: Am înțeles că noua Mașină LLM va avea scopul de:
"[răspuns întrebare 1]". Va primi input de tip: "[răspuns întrebare 2]"
și va genera un output în format: "[răspuns întrebare 3]".

Întrebare: Aceasta este o înțelegere corectă? Există ajustări
sau clarificări pe care dorești să le faci?
```

**De ce e important:** Previne divergența. Dacă AIM a înțeles greșit, corectezi acum, nu la final.

---

### Modul 3: Definire Raționament și Filtre

**Întrebarea 4:** Ce tipuri de raționament avansat?

Opțiuni disponibile:
- Analogii inter-domenii
- Explorare contraintuitivă
- Raționament cauză-efect
- Descompunere fundamentală
- Sinteză creativă
- Toate cele de mai sus

**Întrebarea 5:** Ce filtre anti-halucinație?

Opțiuni:
- Filtre proactive (din "Generare Sigură") - verificare în timp real
- Module de verificare (din "Auditor de Veridicitate") - audit post-generare
- Ambele
- Niciunul (pentru task-uri creative unde precizia e mai puțin critică)

---

### Modul 4: Sincronizare 2 - Arhitectura Cognitivă

```
[PUNCT DE SINCRONIZARE 2: Arhitectura Cognitivă]

Sumar Progres: Am stabilit că Mașina LLM va prioritiza raționamentul
de tip: "[răspuns întrebare 4]". De asemenea, va include:
"[răspuns întrebare 5]".

Întrebare: Este aceasta configurația dorită pentru procesul de
gândire și validare al Mașinii LLM?
```

---

### Modul 5: Detalii Operaționale

**Întrebarea 6:** Puncte de sincronizare?

- Vrei ca mașina generată să aibă puncte de sincronizare?
- Dacă da, unde în workflow?
  - După analiza inițială?
  - Înainte de soluția finală?
  - La bifurcații majore?

**Întrebarea 7:** Constrângeri și criterii de succes?

- Lungime maximă răspuns?
- Ton formal/informal?
- Resurse disponibile?
- Cum măsori succesul output-ului?

---

### Modul 6: Sincronizare 3 - Confirmare Finală

```
[PUNCT DE SINCRONIZARE 3: Confirmarea Designului Final]

Sumar General al Mașinii LLM:
Am consolidat toate deciziile privind:
- Scopul: [...]
- Inputul: [...]
- Outputul: [...]
- Raționamentul: [...]
- Filtrele: [...]
- Sincronizările: [...]
- Constrângerile: [...]

Întrebare: Ești de acord cu designul final? Ești gata să
generăm metapromptul complet?
```

---

### Modul 7: Generare Finală

După confirmare, AIM generează:

1. **Metapromptul complet** - structurat, formatat, gata de copiat
2. **Instrucțiuni de utilizare** - cum să-l folosești
3. **Numele mașinii** - generat automat (ex: "Analizor Riscuri IT V1.0")

---

## Principii de design

### De ce 3 sincronizări?

- **Sincronizarea 1:** Previne divergența fundamentală
- **Sincronizarea 2:** Confirmă "creierul" mașinii
- **Sincronizarea 3:** Ultima șansă de ajustare înainte de generare

### De ce întrebări secvențiale?

Fiecare întrebare construiește pe răspunsurile anterioare. Nu poți defini raționamentul (întrebarea 4) fără să știi scopul (întrebarea 1).

---

## Următorul pas

→ [AIM - Mașina completă (copy-paste ready)](aim-complet.md)
