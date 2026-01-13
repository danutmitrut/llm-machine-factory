# Cum le combini - Workflow-uri Avansate

Mașinile din acest pachet sunt **modulare** - pot fi combinate pentru rezultate mai bune.

---

## Combinația 1: Soluție Verificată

**Scenariu:** Ai o problemă complexă și vrei o soluție în care poți avea încredere.

```
┌─────────────────────┐     ┌─────────────────────┐
│  Arhitect Soluții   │ ──► │     Auditor de      │
│       V2.3          │     │    Veridicitate     │
└─────────────────────┘     └─────────────────────┘
     Generează                   Verifică
      soluția                  pentru halucinații
```

**Pași:**
1. Folosești Arhitectul de Soluții pentru problema ta
2. Copiezi soluția generată
3. O dai la Auditorul de Veridicitate
4. Primești raport cu ce e verificat și ce necesită atenție

**Când:** Decizii de business, analize pentru clienți, rapoarte importante

---

## Combinația 2: Ciclu de Rafinare

**Scenariu:** Vrei să iterezi până când soluția e perfectă.

```
┌─────────────────────┐
│  Arhitect Soluții   │
│       V2.3          │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│     Auditor de      │
│    Veridicitate     │
└─────────┬───────────┘
          │
          ▼ (dacă scor > 2)
┌─────────────────────┐
│  Arhitect Soluții   │◄─── Cu feedback-ul
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

**Când:** Documente critice, cercetare, decizii ireversibile

---

## Combinația 3: Fabrică + Producție

**Scenariu:** Construiești o mașină nouă și o testezi imediat.

```
┌─────────────────────┐     ┌─────────────────────┐
│        AIM          │ ──► │    Mașina Nouă      │
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

**Când:** Dezvoltare de mașini pentru clienți, produse noi

---

## Combinația 4: Audit Pre-Publicare

**Scenariu:** Ai generat conținut și vrei să-l verifici înainte de publicare.

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

**Când:** Blogging, documentație, comunicare externă

---

## Anti-pattern-uri (Ce să NU faci)

### Nu combina în paralel
```
❌ Greșit: Trimiți aceeași problemă la 2 mașini simultan
✓ Corect: Secvențial - una după alta
```
Mașinile sunt proiectate să lucreze pe output-ul celeilalte, nu pe același input.

### Nu sări peste audit pentru decizii importante
```
❌ Greșit: Arhitect Soluții → Implementare directă
✓ Corect: Arhitect Soluții → Auditor → Implementare
```
5 minute de audit pot preveni ore de corecții.

### Nu reconstrui mașini de la zero
```
❌ Greșit: Vrei o variantă ușor diferită → construiești de la zero cu AIM
✓ Corect: Modifici manual metapromptul existent
```
Dacă mașina e 80% ce vrei, editează direct.

---

## Template-uri de workflow

### Pentru consultanță:
```
Problemă client → Arhitect Soluții → Auditor → Livrare
```

### Pentru cercetare:
```
Întrebare → Arhitect Soluții → Auditor → Arhitect (rafinare) → Auditor → Raport final
```

### Pentru product development:
```
Nevoie → AIM (construiești mașina) → Test → Ajustare → Livrare la client
```

---

## Următorul pas

→ [Istoria Proiectului](../04-istoria-proiectului/evolutia.md) - cum s-au născut aceste mașini
