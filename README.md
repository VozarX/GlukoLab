# GlukoLab

GlukoLab je Android aplikacija namenjena korisnicima Libre 2 senzora, koja omogućava:

- Kontinuirano očitavanje i prikaz glukoze u realnom vremenu  
- Minimalistički i pregledan grafikon trendova glukoze  
- Prvi korak ka A/B testiranju uticaja različitih namirnica na glikemiju

---

## Zašto GlukoLab?

Na domaćem tržištu nema dovoljno lokalizovanih rešenja koja povezuju:
- **Libre 2 senzore** (bez kompleksnih setovanja)
- jednostavan prikaz podataka
- mogućnost eksperimentisanja sa ishranom (A/B testovi)

GlukoLab ima za cilj da bude jednostavan, pouzdan alat koji korisnicima pomaže da:
- bolje razumeju svoj organizam
- prate promene glukoze
- povežu hranu i glikemijske reakcije


---

## Funkcionalnosti (IN PROGRESS)

- BLE scan i povezivanje sa Libre 2 senzorom
- Očitavanje trend vrednosti
- Prikaz grafikona (MPAndroidChart ili Jetpack Compose Canvas)
- Lokalan rad, bez cloud servisa (u početnoj fazi)

---

## Planovi za budućnost

- A/B testiranje različitih obroka
- Statistička analiza korelacija hrane i glukoze
- Sinhronizacija podataka u cloud (opciono)
- Internacionalizacija (GlukoLab → GlucoLab)

---

## Napomena

Aplikacija nije medicinski proizvod. Namenjena je isključivo za lično informisanje korisnika. Za sve odluke vezane za zdravlje, konsultujte se sa lekarom.

---

## Architecture Overview

For details on the recommended project structure and technology stack, see [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md).

