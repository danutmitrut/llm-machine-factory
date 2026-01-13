# AIM - Arhitectul inteligent de metaprompturi

## Ce este AIM?

AIM este **fabrica care construiește fabrici**.

Este un metaprompt care, prin dialog ghidat cu tine, generează alte metaprompturi (mașini LLM) personalizate pentru nevoile tale specifice.

---

## De ce AIM e piesa centrala?

Celelalte mașini din acest pachet (Arhitect de soluții, Auditor de veridicitate) sunt **exemple** de ce poate genera AIM.

Cu AIM poți crea:
- Mașini pentru industria ta specifică
- Mașini pentru workflow-uri unice
- Mașini cu tipuri de raționament personalizate
- Mașini cu sau fără verificare anti-halucinație

---

## Diferența față de Arhitectul meta-cognitive

Există două versiuni ale "fabricii de mașini":

| AIM (co-creare) | Arhitect meta-cognitive (automat) |
|-----------------|-----------------------------------|
| Dialog ghidat cu utilizatorul | Întrebări inițiale, apoi generare automată |
| 3 puncte de sincronizare | Fără sincronizări intermediare |
| Control maxim | Viteză maximă |
| Pentru mașini complexe | Pentru mașini standard |

**Recomandare:** Începe cu AIM. Folosește Arhitectul meta-cognitive doar când ai experiență și știi exact ce vrei.

---

## Ce face AIM concret?

### Input
Tu descrii ce vrei să facă noua mașină:
- "Vreau o mașină care să transforme idei de business în planuri de acțiune"
- "Am nevoie de un analizor de contracte juridice"
- "Vreau ceva care să-mi genereze strategii de marketing validate"

### Proces
AIM te ghidează prin 7 întrebări cheie:
1. Ce scop principal?
2. Ce tip de input?
3. Ce format de output?
4. Ce tipuri de raționament?
5. Ce filtre anti-halucinație?
6. Unde puncte de sincronizare?
7. Ce constrângeri/criterii de succes?

După fiecare grup de întrebări, AIM face **sincronizare** - îți arată ce a înțeles și cere confirmare.

### Output
Un metaprompt complet, structurat, gata de folosit - propria ta mașină LLM.

---

## Când să folosești AIM?

**Folosește AIM când:**
- Ai o nevoie specifică pe care mașinile existente nu o acoperă
- Vrei control total asupra cum funcționează mașina
- Construiești pentru un client sau un proiect specific
- Vrei să înveți cum se construiesc mașinile

**Nu ai nevoie de AIM când:**
- Mașinile existente îți rezolvă problema
- Vrei ceva rapid, fără personalizare

---

## Exemplu de utilizare

**Tu:** "Vreau să construiesc o mașină pentru analiza riscurilor în proiecte IT"

**AIM:**
```
Întrebarea 1: Ce scop principal ar trebui să aibă această Mașină LLM?
```

**Tu:** "Să primească descrierea unui proiect IT și să identifice riscurile potențiale cu probabilități și strategii de mitigare"

**AIM:**
```
[PUNCT DE SINCRONIZARE 1: Viziunea Generală]
Am înțeles că noua Mașină LLM va avea scopul de:
"analiza riscurilor în proiecte IT cu identificare de probabilități
și strategii de mitigare"

Aceasta este o înțelegere corectă?
```

[...continuă dialogul...]

**Output final:** Un metaprompt complet pentru "Analizor de riscuri IT V1.0"

---

## Următorul pas

→ [Cum funcționează AIM în detaliu](cum-functioneaza.md)
