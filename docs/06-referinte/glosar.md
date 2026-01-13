# Glosar de termeni

Termenii cheie folosiți în acest pachet.

---

## A

### AIM (Arhitectul Inteligent de Metaprompturi)
Mașina centrală din acest pachet. Generează alte mașini LLM prin dialog ghidat cu utilizatorul. Include 3 puncte de sincronizare pentru control maxim.

### Anti-halucinație
Tehnici și instrucțiuni menite să reducă generarea de informații false de către LLM. Include filtre proactive (în timpul generării) și verificare post-factum.

### Ancorare în realitate
Principiul că output-ul trebuie să fie legat de date și exemple concrete, nu doar de raționament abstract. Se realizează prin căutare web și cerere de dovezi.

---

## B

### Bifurcație strategică
Moment în procesul de raționament unde există două sau mai multe direcții valide de urmat. Utilizatorul alege direcția la punctul de sincronizare.

### Bootstrapping
Proces prin care un sistem se îmbunătățește singur. În acest context: mașinile au fost folosite pentru a-și genera propriile îmbunătățiri.

---

## C

### Chain of Thought (CoT)
Tehnică de prompting unde LLM-ul este instruit să-și arate pașii de raționament. Baza teoretică pentru Mașinile Metacognitive.

### Continuitate cognitivă (Principiu)
Regula fundamentală că fiecare pas de raționament se bazează EXCLUSIV pe pașii anteriori. Previne pre-calcularea răspunsului și justificarea retroactivă.

### Co-creare
Model de interacțiune unde utilizatorul și AI-ul construiesc împreună soluția, prin dialog, nu prin delegare completă.

---

## D

### Descompunere fundamentală
Tip de raționament: fragmentarea unei probleme complexe în componente mai simple, analizabile individual.

---

## E

### Explorare contraintuitivă
Tip de raționament: examinarea ipotezelor care contravin logicii inițiale sau intuiției comune. "Ce dacă opusul e adevărat?"

---

## H

### Halucinație
Generarea de informații false, inventate sau nefondate de către un LLM, prezentate ca fapte. Include: statistici inventate, concepte inexistente, concluzii nejustificate.

---

## I

### Iterație
Un ciclu complet de întrebare internă → răspuns → concluzie în procesul de raționament. Mașinile folosesc 5-15 iterații per problemă.

---

## L

### LLM (Large Language Model)
Model de limbaj de mari dimensiuni (ex: GPT-4, Claude). Baza pe care rulează Mașinile Metacognitive.

---

## M

### Mașină LLM / Mașină Metacognitivă
Termen informal pentru un metaprompt complex care transformă un LLM într-un sistem de raționament structurat cu capabilități specifice.

### Meta-cogniție
Literal: "gândire despre gândire". Capacitatea unui sistem de a-și analiza și evalua propriul proces de raționament.

### Metaprompt
Un prompt de nivel superior care definește cum să funcționeze un LLM pentru o categorie de task-uri, nu doar pentru un task specific.

---

## P

### Punct de sincronizare
Moment predefinit în workflow unde procesul se oprește și AI-ul cere input de la utilizator. Transformă monologul în dialog.

### Pre-calculare
Anti-pattern: când LLM-ul "știe" răspunsul dinainte și fabrică o justificare retroactivă. Prevenit prin Principiul Continuității Cognitive.

---

## R

### Raționament cauză-efect
Tip de raționament: investigarea lanțurilor de cauzalitate pentru a identifica cauze rădăcină, nu doar simptome.

### Raționament vizibil
Principiul că utilizatorul vede procesul de gândire (iterațiile), nu doar rezultatul final. Creează transparență și încredere.

### Reflecție și ajustare
Tip de raționament: oprirea periodică pentru a evalua progresul și a ajusta direcția dacă e necesar.

---

## S

### Scor de risc de halucinație
Metrică (0-5) care indică probabilitatea ca o informație să fie halucinată. 0 = verificat, 5 = clar inventat.

### Sinteză creativă
Tip de raționament: combinarea elementelor disparate într-o soluție nouă și inovatoare.

### Simulare vs. gândire
Distincție critică: LLM-urile pot "simula" că gândesc (fabricare retroactivă) sau pot "gândi" autentic (construcție progresivă). Mașinile forțează varianta a doua.

---

## V

### Validare internă
Verificarea consistenței logice a unei afirmații fără surse externe. "Are sens logic?"

### Validare externă
Verificarea unei afirmații prin căutare web sau cerere de dovezi. "Există dovezi?"

### Veridicitate
Gradul în care o afirmație corespunde realității. Măsurată prin Auditorul de Veridicitate.

---

## Următorul pas

→ [Resurse suplimentare](resurse.md)
