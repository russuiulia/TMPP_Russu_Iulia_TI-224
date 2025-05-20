# Șabloane Structurale (Structural Design Patterns)

Șabloanele structurale sunt utilizate pentru a compune clase și obiecte în structuri mai mari, menținând în același timp flexibilitatea și eficiența acestora. Ele ajută la stabilirea relațiilor între entități fără a afecta prea mult codul existent.

## 1. Adapter

**Problema:**  
Clasele cu interfețe incompatibile trebuie să colaboreze. Vrei să reutilizezi o clasă existentă, dar interfața ei nu corespunde celei a sistemului curent.

**Necesitatea utilizării:**  
Permite integrarea codului existent cu interfețe incompatibile, fără a-l modifica.

**Avantaje:**
- Reutilizarea claselor existente.
- Separarea codului client de detaliile de implementare.

**Dezavantaje:**
- Poate adăuga complexitate suplimentară.
- Nu funcționează bine cu toate limbajele (ex: cele fără moștenire multiplă).

---

## 2. Bridge

**Problema:**  
Ai o ierarhie de clase care crește în două dimensiuni (ex: forme și culori), iar combinarea acestora produce o explozie de subclase.

**Necesitatea utilizării:**  
Separă abstracția de implementare astfel încât ambele să poată evolua independent.

**Avantaje:**
- Scalabilitate și extensibilitate crescută.
- Separarea clară între abstracție și implementare.

**Dezavantaje:**
- Mai multă complexitate în design.
- Poate fi excesiv dacă nu este necesar un astfel de nivel de separare.

---

## 3. Composite

**Problema:**  
Vrei să tratezi obiecte individuale și compoziții de obiecte în același mod (ex: componentele unei interfețe grafice).

**Necesitatea utilizării:**  
Permite tratarea uniformă a obiectelor și grupurilor de obiecte.

**Avantaje:**
- Simplifică codul clientului.
- Oferă flexibilitate în tratarea structurii ierarhice.

**Dezavantaje:**
- Poate face dificilă restricționarea comportamentului componentelor.
- Navigarea în structură poate fi mai complexă.

---

## 4. Decorator

**Problema:**  
Vrei să adaugi responsabilități suplimentare unui obiect fără a schimba clasa sa.

**Necesitatea utilizării:**  
O alternativă flexibilă la moștenirea extensivă pentru funcționalități adiționale.

**Avantaje:**
- Adăugare dinamică de comportament.
- Fără moșteniri rigide.

**Dezavantaje:**
- Poate duce la o structură complicată cu multe obiecte.
- Ordinea decoratorilor poate influența rezultatul.

---

## 5. Facade

**Problema:**  
Un sistem are o interfață complexă cu multe clase și metode greu de utilizat direct.

**Necesitatea utilizării:**  
Oferă o interfață simplificată către un subsistem complex.

**Avantaje:**
- Simplifică utilizarea unui subsistem.
- Reduce dependențele dintre client și subsistem.

**Dezavantaje:**
- Poate deveni un *gode object* dacă nu este proiectat cu grijă.
- Maschează funcționalitățile detaliate ale subsistemului.

---

## 6. Flyweight

**Problema:**  
Crearea unui număr mare de obiecte identice consumă prea multă memorie.

**Necesitatea utilizării:**  
Partajează date între obiecte pentru a reduce consumul de memorie.

**Avantaje:**
- Eficiență ridicată în utilizarea memoriei.
- Potrivit pentru aplicații cu multe obiecte similare (ex: jocuri, editori de text).

**Dezavantaje:**
- Complică logica aplicației.
- Necesită distincția clară între starea internă (partajată) și cea externă (nepartajată).

---

## 7. Proxy

**Problema:**  
Accesul direct la un obiect este costisitor, nesigur sau necontrolat.

**Necesitatea utilizării:**  
Controlează accesul la obiecte, permițând diverse funcționalități (ex: lazy loading, control de acces, logging).

**Avantaje:**
- Control asupra modului de acces la obiect.
- Poate reduce costurile (ex: încărcare întârziată).

**Dezavantaje:**
- Adaugă nivel de indirectare.
- Poate complica codul dacă sunt multe tipuri de proxy.

---

> Aceste șabloane contribuie semnificativ la menținerea unui cod curat, reutilizabil și extensibil. Alegerea potrivită depinde de contextul aplicației și de nevoile arhitecturale.
