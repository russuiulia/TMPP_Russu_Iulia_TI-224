# Laboratorul nr.3 TMPP 

# Șabloane de Comportament 

Șabloanele de comportament se ocupă cu modul în care obiectele interacționează și comunică între ele. Ele ajută la organizarea fluxurilor de control și a schimbului de mesaje într-un mod flexibil și reutilizabil.

---

## 1. Chain of Responsibility

**Problema:**  
Ai mai mulți handleri care pot procesa o solicitare, dar nu vrei să codifici direct ce handler răspunde.

**Necesitatea utilizării:**  
Permite trimiterea cererilor printr-un lanț de handleri până când unul o procesează.

**Avantaje:**
- Reduce cuplarea dintre emitentul și receptorul cererii.
- Adaugă sau elimină handleri ușor.

**Dezavantaje:**
- Nu e clar ce handler va procesa cererea.
- Poate fi ineficient dacă lanțul este lung.

---

## 2. Command

**Problema:**  
Ai nevoie să decuplezi obiectul care emite o cerere de cel care o execută.

**Necesitatea utilizării:**  
Încapsulează cererile ca obiecte, permițând parametrizarea, stocarea sau anularea acestora.

**Avantaje:**
- Decuplare completă între client și executant.
- Ușor de implementat undo/redo.

**Dezavantaje:**
- Poate duce la proliferarea de clase.
- Poate adăuga complexitate pentru cereri simple.

---

## 3. Iterator

**Problema:**  
Vrei să parcurgi o colecție fără a expune detaliile interne ale structurii.

**Necesitatea utilizării:**  
Furnizează un mod uniform de a accesa elementele unei colecții.

**Avantaje:**
- Separă logica de parcurgere de structură.
- Oferă o interfață unificată pentru colecții diferite.

**Dezavantaje:**
- Poate necesita mai multă memorie (dacă iteratorul stochează stare internă).
- Ineficient pentru structuri mari dacă nu e implementat optim.

---

## 4. Mediator

**Problema:**  
Multe obiecte comunică direct, ducând la o rețea complexă de dependențe.

**Necesitatea utilizării:**  
Centralizează comunicarea între obiecte, reducând dependențele directe.

**Avantaje:**
- Simplifică comunicarea între obiecte.
- Promovează separarea responsabilităților.

**Dezavantaje:**
- Mediatorul poate deveni un obiect prea complex (*god object*).
- Ascunde relațiile reale dintre componente.

---

## 5. Memento

**Problema:**  
Vrei să salvezi și să restaurezi starea unui obiect fără a-i încălca încapsularea.

**Necesitatea utilizării:**  
Permite salvarea/restaurarea stării interne a unui obiect în mod sigur.

**Avantaje:**
- Menține încapsularea.
- Permite funcționalități de undo/redo.

**Dezavantaje:**
- Consum de memorie (stocare multiple versiuni).
- Gestionarea corectă a mementourilor poate deveni dificilă.

---

## 6. Observer

**Problema:**  
Mai multe obiecte trebuie notificate atunci când un obiect se schimbă.

**Necesitatea utilizării:**  
Definește o dependență de tip 1-la-n între obiecte.

**Avantaje:**
- Actualizare automată a observatorilor.
- Decuplare între subiect și observatori.

**Dezavantaje:**
- Notificările pot deveni greu de controlat în sisteme mari.
- Ordinea notificărilor poate fi imprevizibilă.

---

## 7. State

**Problema:**  
Comportamentul unui obiect se schimbă în funcție de starea sa internă.

**Necesitatea utilizării:**  
Permite obiectului să-și schimbe comportamentul fără structuri mari de control (ex: switch-uri).

**Avantaje:**
- Elimină structuri condiționale masive.
- Permite adăugarea de noi stări fără a modifica clasa principală.

**Dezavantaje:**
- Poate necesita multe clase.
- Crește complexitatea dacă sunt prea multe stări.

---

## 8. Strategy

**Problema:**  
Ai mai multe variante de algoritmi pentru o operație și vrei să le poți schimba dinamic.

**Necesitatea utilizării:**  
Permite definirea unei familii de algoritmi și schimbarea lor la runtime.

**Avantaje:**
- Separă algoritmul de codul care îl folosește.
- Ușor de extins cu noi comportamente.

**Dezavantaje:**
- Poate adăuga complexitate (multe clase).
- Clientul trebuie să cunoască strategiile disponibile.

---

## 9. Template Method

**Problema:**  
Vrei să definești scheletul unui algoritm, permițând subclaselor să modifice anumite etape.

**Necesitatea utilizării:**  
Permite reutilizarea codului comun și personalizarea pașilor algoritmului.

**Avantaje:**
- Reutilizare prin moștenire.
- Structură clară a pașilor algoritmului.

**Dezavantaje:**
- Legătură puternică între clasă de bază și subclase.
- Dificil de modificat algoritmul fără a afecta toate subclasele.

---

## 10. Visitor

**Problema:**  
Ai de efectuat operații diferite asupra obiectelor dintr-o structură complexă fără a le modifica clasele.

**Necesitatea utilizării:**  
Separă algoritmul de structura obiectelor, permițând adăugarea de noi operații fără a modifica obiectele.

**Avantaje:**
- Adaugă ușor noi comportamente.
- Separă clar logica algoritmului.

**Dezavantaje:**
- Greu de adăugat noi tipuri de obiecte.
- Poate încălca principiul deschidere-închidere pentru tipuri.

---

> Aceste șabloane sunt esențiale pentru a crea un sistem flexibil și ușor de întreținut, în special în aplicații cu logici complexe și interacțiuni frecvente între obiecte.
