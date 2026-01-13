# Cum le combini - workflow-uri avansate

Mașinile din acest pachet sunt **modulare** - pot fi combinate pentru rezultate mai bune.

---

## Combinația 1: soluție verificată

**Scenariu:** ai o problemă complexă și vrei o soluție în care poți avea încredere.

```
┌─────────────────────┐     ┌─────────────────────┐
│  Arhitect soluții   │ ──► │     Auditor de      │
│       V2.3          │     │    veridicitate     │
└─────────────────────┘     └─────────────────────┘
     Generează                   Verifică
      soluția                  pentru halucinații
```

**Pași:**
1. Folosești Arhitectul de soluții pentru problema ta
2. Copiezi soluția generată
3. O dai la Auditorul de veridicitate
4. Primești raport cu ce e verificat și ce necesită atenție

**Când:** decizii de business, analize pentru clienți, rapoarte importante

---

## Combinația 2: ciclu de rafinare

**Scenariu:** vrei să iterezi până când soluția e perfectă.

```
┌─────────────────────┐
│  Arhitect soluții   │
│       V2.3          │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│     Auditor de      │
│    veridicitate     │
└─────────┬───────────┘
          │
          ▼ (dacă scor > 2)
┌─────────────────────┐
│  Arhitect soluții   │◄─── cu feedback-ul
│    (re-generare)    │     din audit
└─────────────────────┘
```

**Pași:**
1. Generezi soluția inițială
2. Auditezi
3. Dacă scorul de risc > 2, re-generezi cu contextul:
   - "Soluția anterioară avea aceste probleme: [din audit]"
   - "Generează o versiune corectată care adresează: [probleme]"
4. Auditezi din nou
5. Repetă până scor < 2

**Când:** documente critice, cercetare, decizii ireversibile

---

## Combinația 3: fabrică + producție

**Scenariu:** construiești o mașină nouă și o testezi imediat.

```
┌─────────────────────┐     ┌─────────────────────┐
│        AIM          │ ──► │    Mașina nouă      │
│  (construiești)     │     │    (testezi)        │
└─────────────────────┘     └─────────────────────┘
          │                           │
          └───────────────────────────┘
                    feedback
            (ajustezi mașina dacă e nevoie)
```

**Pași:**
1. Folosești AIM pentru a construi o mașină nouă
2. Testezi mașina cu un caz real
3. Dacă rezultatul nu e satisfăcător:
   - Notezi ce nu funcționează
   - Revii la AIM cu feedback
   - Ajustezi specificațiile
4. Re-generezi și re-testezi

**Când:** dezvoltare de mașini pentru clienți, produse noi

---

## Combinația 4: audit pre-publicare

**Scenariu:** ai generat conținut și vrei să-l verifici înainte de publicare.

```
┌─────────────────────┐     ┌─────────────────────┐
│   Orice generator   │ ──► │     Auditor de      │
│   de conținut AI    │     │    Veridicitate     │
└─────────────────────┘     └─────────────────────┘
```

**Funcționează cu:**
- Articole generate cu ChatGPT
- Răspunsuri de la Claude
- Orice output AI

**Pași:**
1. Generezi conținut cu orice tool AI
2. Copiezi output-ul
3. Îl trimiți la Auditor
4. Corectezi manual ce e semnalat

**Când:** blogging, documentație, comunicare externă

---

## Anti-pattern-uri (ce să NU faci)

### Nu combina în paralel
```
❌ Greșit: trimiți aceeași problemă la 2 mașini simultan
✓ Corect: secvențial - una după alta
```
Mașinile sunt proiectate să lucreze pe output-ul celeilalte, nu pe același input.

### Nu sări peste audit pentru decizii importante
```
❌ Greșit: Arhitect soluții → Implementare directă
✓ Corect: Arhitect soluții → Auditor → Implementare
```
5 minute de audit pot preveni ore de corecții.

### Nu reconstrui mașini de la zero
```
❌ Greșit: vrei o variantă ușor diferită → construiești de la zero cu AIM
✓ Corect: modifici manual metapromptul existent
```
Dacă mașina e 80% ce vrei, editează direct.

---

## Template-uri de workflow

### Pentru consultanță:
```
Problemă client → Arhitect soluții → Auditor → Livrare
```

### Pentru cercetare:
```
Întrebare → Arhitect soluții → Auditor → Arhitect (rafinare) → Auditor → Raport final
```

### Pentru product development:
```
Nevoie → AIM (construiești mașina) → Test → Ajustare → Livrare la client
```

---

## Următorul pas

→ [Istoria proiectului](../04-istoria-proiectului/evolutia.md) - cum s-au născut aceste mașini
