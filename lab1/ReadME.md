# Design Patterns in C# - Implementări

## Patterne Implementate

1. **Singleton**  
2. **Factory Method**  
3. **Abstract Factory**  
4. **Prototype**  
5. **Builder**

## Descrierea Fiecărui Pattern

### 1. **Singleton**

#### Descriere:
Patternul **Singleton** garantează că o clasă are o singură instanță și oferă un punct global de acces la aceasta. Este util atunci când vrei să te asiguri că există o singură instanță a unei clase (de exemplu, o conexiune la o bază de date sau un logger) pe durata întregii aplicații.

#### Avantaje:
- Asigură controlul asupra instanței unui obiect.
- Reduce utilizarea de resurse, evitând instanțierea multiplă a aceleași clase.
- Permite accesul global la instanța unică.

#### Dezavantaje:
- Este greu de testat, mai ales în cazul testării unitare.
- Poate duce la dependențe globale, care pot afecta modularitatea aplicației.
- Poate fi greu de utilizat în aplicații cu multă concurență.

---

### 2. **Factory Method**

#### Descriere:
Patternul **Factory Method** definește o metodă pentru crearea obiectelor, dar permite subclaselor să decidă ce clasă să instanțieze. Este util când nu vrei ca un client să depindă de tipul concret al unui obiect pe care îl creează.

#### Avantaje:
- Permite decuplarea clientului de clasa concretă.
- Îmbunătățește extensibilitatea, deoarece noi tipuri de obiecte pot fi adăugate fără a modifica codul clientului.
- Favorizează extensiunea ușoară a codului fără a face modificări majore.

#### Dezavantaje:
- Crește complexitatea sistemului, deoarece necesită crearea de clase suplimentare (subclase).
- Poate duce la o ierarhie de clase complicată.

---

### 3. **Abstract Factory**

#### Descriere:
Patternul **Abstract Factory** furnizează o interfață pentru crearea de obiecte de o anumită familie de produse, fără a specifica clasele lor concrete. Este folosit atunci când vrei să creezi o familie de obiecte interdependente, dar să le controlezi instanțierea fără a lega clientul de implementările lor.

#### Avantaje:
- Permite crearea de obiecte interdependente, care sunt garantate a fi compatibile.
- Favorizează extensibilitatea, deoarece se pot adăuga noi familii de produse fără a modifica clientul.
- Oferă un nivel de abstractizare care face codul mai flexibil.

#### Dezavantaje:
- Necesită mai multe clase pentru a gestiona crearea de obiecte, ceea ce poate duce la un cod mai greu de întreținut.
- Poate introduce complexitate suplimentară pentru aplicații simple.

---

### 4. **Prototype**

#### Descriere:
Patternul **Prototype** permite clonarea unui obiect existent pentru a crea un nou obiect similar, fără a depinde de constructorul său. Este util atunci când crearea unui obiect de la zero poate fi costisitoare și se dorește reutilizarea unui obiect existent.

#### Avantaje:
- Permite crearea rapidă a unor noi instanțe fără a necesita reconstrucția acestora.
- Este eficient atunci când există obiecte complexe care trebuie replicate rapid.
- Permite personalizarea obiectelor clonate.

#### Dezavantaje:
- Poate deveni complicat în cazul obiectelor care au dependențe complexe sau referințe circulare.
- Poate duce la probleme de performanță în cazul clonării unor obiecte mari sau complexe.

---

### 5. **Builder**

#### Descriere:
Patternul **Builder** separă procesul de construcție a unui obiect complex de reprezentarea sa finală. Acesta permite crearea treptată a unui obiect complex, oferind un control mai mare asupra procesului de construcție.

#### Avantaje:
- Permite construirea unor obiecte complexe pas cu pas.
- Separă logica de construcție de logica aplicației.
- Este foarte util atunci când obiectul are multe părți opționale.

#### Dezavantaje:
- Poate introduce complexitate suplimentară, mai ales în cazuri simple.
- Necesită mai multe clase pentru gestionarea construcției obiectelor.

---