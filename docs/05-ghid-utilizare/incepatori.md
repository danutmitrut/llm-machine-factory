# Ghid pentru începători

Primii pași cu Mașinile Metacognitive.

---

## Înainte de a începe

### Ce ai nevoie:
- Acces la Claude sau ChatGPT (funcționează cu ambele)
- O problemă de rezolvat sau un text de verificat
- 5-10 minute pentru prima testare

### Ce NU ai nevoie:
- Cunoștințe tehnice
- Experiență cu prompt engineering
- Abonament plătit (merge și cu versiunile gratuite)

---

## Primul tău test: Arhitect de Soluții

### Pasul 1: Copiază mașina
Du-te la [Arhitect de Soluții V2.3](../03-masinile-din-fabrica/arhitect-solutii.md) și copiază tot textul dintre `[Început Metaprompt]` și `[Sfârșit Metaprompt]`.

### Pasul 2: Deschide Claude sau ChatGPT
Folosește interfața web sau aplicația.

### Pasul 3: Lipește metapromptul
Ca primul mesaj în conversație, lipește tot textul copiat.

### Pasul 4: Introdu problema ta
Când AI-ul te întreabă "te rog să introduci problema", scrie problema ta.

**Exemple de probleme bune pentru început:**
- "Cum să-mi cresc vânzările online cu 20% în 3 luni?"
- "Ar trebui să-mi schimb cariera din X în Y?"
- "Cum să automatizez [proces specific] în afacerea mea?"

### Pasul 5: Urmărește procesul
Vei vedea iterațiile de gândire - fiecare cu întrebare, răspuns, tip de raționament.

### Pasul 6: Răspunde la sincronizare
Când apare `[PUNCT DE SINCRONIZARE]`, AI-ul te întreabă ce direcție preferați. Răspunde și continuă.

### Pasul 7: Primește soluția
La final, vei avea o soluție structurată, cu justificare pentru fiecare recomandare.

---

## Al doilea test: Auditor de Veridicitate

Acum că ai o soluție, hai s-o verificăm.

### Pasul 1: Copiază soluția
Din conversația anterioară, copiază soluția finală generată.

### Pasul 2: Deschide o conversație nouă
Important: conversație nouă, nu continuare.

### Pasul 3: Lipește Auditorul
Copiază metapromptul de la [Auditor de Veridicitate](../03-masinile-din-fabrica/auditor-veridicitate.md) și lipește-l.

### Pasul 4: Trimite soluția de verificat
Când AI-ul cere textul de auditat, lipește soluția.

### Pasul 5: Analizează raportul
Vei primi:
- Scor general de risc (0-5)
- Verdict pentru fiecare afirmație
- Sugestii de corecție

---

## Greșeli comune de evitat

### 1. Nu modifica metapromptul
La început, folosește-l exact cum e. Modificările pot strica funcționarea.

### 2. Nu sări peste sincronizări
Când AI-ul întreabă, răspunde. Sincronizările există cu un scop.

### 3. Nu te aștepta la magie
Mașinile îmbunătățesc semnificativ output-ul, dar nu-l fac perfect. Folosește judecata critică.

### 4. Nu folosi pentru task-uri simple
Pentru "scrie-mi un email", folosește un prompt simplu. Mașinile sunt pentru probleme complexe.

### 5. Nu ignora limitările declarate
Dacă AI-ul spune "Nu am suficiente informații despre X", oferă-i informațiile.

---

## Când să folosești care mașină

| Situație | Mașină |
|----------|--------|
| Am o problemă complexă de rezolvat | Arhitect de Soluții |
| Am un text și vreau să-l verific | Auditor de Veridicitate |
| Vreau să construiesc propria mașină | AIM |
| Am folosit AI și nu sunt sigur de răspuns | Auditor de Veridicitate |
| Am nevoie de analiză profundă | Arhitect de Soluții |

---

## Exerciții practice

### Exercițiul 1: Prima problemă
Folosește Arhitectul de Soluții pentru:
> "Care sunt cele mai importante 3 lucruri pe care ar trebui să le fac pentru a-mi îmbunătăți productivitatea?"

Observă cum gândește, cum ajunge la concluzii.

### Exercițiul 2: Verificare
Ia răspunsul de la Exercițiul 1 și verifică-l cu Auditorul.
Ce scor a primit? Ce trebuie verificat?

### Exercițiul 3: Problemă din domeniul tău
Alege o problemă reală din munca sau viața ta.
Folosește Arhitectul de Soluții.
Compară răspunsul cu ce ai fi primit de la un prompt simplu.

---

## Întrebări frecvente

### "Funcționează cu ChatGPT sau doar cu Claude?"
Ambele. Metaprompturile sunt agnostice - funcționează cu orice LLM suficient de capabil.

### "Pot să modific mașina?"
Da, după ce înțelegi cum funcționează. Începe prin a o folosi așa cum e.

### "Cât durează să primesc răspuns?"
Mai mult decât un prompt simplu (iterațiile cer timp), dar calitatea e semnificativ mai bună. Estimare: 2-5 minute pentru o problemă medie.

### "Ce fac dacă se blochează?"
Începe o conversație nouă și re-încearcă. Uneori contextul se "murdărește".

---

## Următorul pas

Ai parcurs baza. Acum:
- → [Ghid pentru avansați](avansati.md) - personalizare și optimizare
- → [Integrare în asistenți](integrare-asistenti.md) - cum să le folosești în tools și agenți
