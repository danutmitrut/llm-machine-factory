# Mașinile din Fabrică - Overview

## Ecosistemul de Mașini

LLM Machine Factory include **3 mașini principale** + **1 fabrică** (AIM):

```
┌─────────────────────────────────────────────────────────────┐
│                    LLM MACHINE FACTORY                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│   ┌─────────────────────────────────────────────────────┐   │
│   │          AIM - Fabrica de Mașini                    │   │
│   │     (Arhitectul Inteligent de Metaprompturi)        │   │
│   └──────────────────────┬──────────────────────────────┘   │
│                          │                                  │
│            ┌─────────────┼─────────────┐                    │
│            ▼             ▼             ▼                    │
│   ┌────────────┐ ┌──────────────┐ ┌────────────┐            │
│   │ Arhitect   │ │  Auditor de  │ │ Arhitect   │            │
│   │ de Soluții │ │ Veridicitate │ │ Meta-      │            │
│   │   V2.3     │ │    V1.0      │ │ Cognitive  │            │
│   └────────────┘ └──────────────┘ └────────────┘            │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## Când să folosești fiecare mașină

| Ai nevoie să... | Folosește |
|-----------------|-----------|
| Rezolvi o problemă complexă | [Arhitect de Soluții V2.3](arhitect-solutii.md) |
| Verifici un text pentru halucinații | [Auditor de Veridicitate V1.0](auditor-veridicitate.md) |
| Construiești o mașină nouă (rapid) | [Arhitect Meta-Cognitive V1.0](arhitect-meta-cognitive.md) |
| Construiești o mașină nouă (cu control) | [AIM](../02-piesa-centrala-aim/aim-complet.md) |

---

## Descriere scurtă a fiecărei mașini

### Arhitect de Soluții V2.3
**Motorul principal de raționament**

- Primește o problemă complexă
- Execută 5-15 iterații de raționament intern
- Include punct de sincronizare cu utilizatorul
- Generează soluție originală, acționabilă, ancorată în realitate

**Caracteristici cheie:**
- Principiul Continuității Cognitive
- Căutare web integrată
- Raționament vizibil (vezi fiecare iterație)

---

### Auditor de Veridicitate V1.0
**Verificator anti-halucinație**

- Primește un text de auditat
- Îl segmentează în unități verificabile
- Verifică fiecare: afirmații factuale, concepte, concluzii
- Generează raport de audit cu scoruri

**Caracteristici cheie:**
- Căutare web pentru verificare factuală
- Scor de risc de halucinație (0-5)
- Sugestii de corecție

---

### Arhitect Meta-Cognitive V1.0
**Generator automat de mașini**

- Primește descrierea unei mașini dorite
- Pune 7 întrebări cheie
- Generează metaprompt complet

**Diferența față de AIM:**
- Fără puncte de sincronizare intermediare
- Mai rapid, mai puțin control
- Pentru utilizatori experimentați

---

## Combinații recomandate

### Pentru analiză riguroasă:
```
Arhitect de Soluții → Auditor de Veridicitate
```
Generezi soluția, apoi o verifici pentru halucinații.

### Pentru construcție de mașini:
```
AIM (pentru prima dată) → Arhitect Meta-Cognitive (pentru iterații rapide)
```
Înveți procesul cu AIM, apoi accelerezi cu Arhitectul Meta-Cognitive.

### Pentru decizii importante:
```
Arhitect de Soluții → Auditor → Arhitect de Soluții (cu feedback)
```
Ciclu de rafinare: generare → verificare → regenerare.

---

## Următorul pas

Alege mașina de care ai nevoie:
- → [Arhitect de Soluții V2.3](arhitect-solutii.md) - rezolvă probleme
- → [Auditor de Veridicitate V1.0](auditor-veridicitate.md) - verifică texte
- → [Arhitect Meta-Cognitive V1.0](arhitect-meta-cognitive.md) - construiește mașini rapid
- → [Cum le combini](cum-le-combini.md) - workflow-uri avansate
