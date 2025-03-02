# Haladó Szoftverfejlesztés Féléves Feladat

## 2024/25/2 félév

A tantárgy féléves feladatában minden hallgatónak egy saját adatbázisra épülő rétegzett alkalmazást kell fejlesztenie. A féléves feladat alapvető elvárásai alább kerülnek ismertetésre. A kötelezően elvárt részeknek maradéktalanul meg kell felelni, különben a féléves feladat nem fogadható el.

## Az alapvető elvárások a projekttel kapcsolatban

A kész feladatot a Moodle rendszerre kell feltölteni. Az előadás kurzus alatt kell keresni a feltöltési lehetőséget. Feltöltési lehetőségek közül mindenkinek a saját laborvezetőjének nevét kell keresni és az alá feltölteni.

## Az alapvető elvárások az üre solution felépítésével kapcsolatban:

A féléves feladat kezdetekor el kell indítani a Visual Studio-t (VS) és létre kell hozni egy új Console Appot .NET 8.0-ben! A solution neve legyen: `ABC123_HSZF_2024252` (ahol `ABC123` helyére a saját neptun kódot kell írni). A projekt neve legyen: `ABC123_HSZF_2024252.Console`.

### Létre kell hozni a solution-ben az alábbi projekteket:

- `ABC123_HSZF_2024252.Application` (Class Library)
- `ABC123_HSZF_2024252.Model` (Class Library)
- `ABC123_HSZF_2024252.Persistence.MsSql` (Class Library)
- `ABC123_HSZF_2024252.Console` (Console App)
- `ABC123_HSZF_2024252.Test` (Class Library)

### Solution folder-ek létrehozása:

A solution neévére kattintva (Add) 5 solution folder-t kell létrehozni, és ezekbe drag-and-drop módszerrel áthúzni a megfelelő projekteket:

- **Application** (`Application`)
- **Domain** (`Model`)
- **Infrastructure** (`MsSql`)
- **Presentation** (`Console`)
- **Tests** (`Test`)

### Szükséges beállítani a függőségeket!

Egy adott projekten jobb kattintás > Add > Project Reference. Az alábbi függőségeket kell beállítani:

- `Console` projekthez: `Application`, `Infrastructure` és `Model`
- `Test` projekthez: `Application`, `Infrastructure`, `Model`
- `Application` projekthez: `Model`, `MsSql`
- `MsSql` projekthez: `Model`

## Az alapvető elvárások a szoftverrel kapcsolatban:

- A szoftvernek fordulnia kell a javító tanár számítógépén.
- **.NET 8.0 verzióban** kell írni és **adatbázist kell használni Entity Framework Core felett**.
- A C# program osztályait, metódusait, változóit **angol nyelven** kell elnevezni.
- **Függőségeket csak interfészen át (Dependency Injection)**, konstruktor paraméterként lehet megkapni.
- **A Console projekt IoC konténert használ** a függőségek beszúrásához.
- **Minimum 10 db Unit teszt** készül, melyek az üzleti logikát fedik le, és mindnek sikeresen kell futnia.
- A felhasználó interakció szempontjából legalább alapszintű beviteli lehetőséget kell biztosítani.

## Határidő:

- Leadás: 12. hét **Május 4. 23:59:59**
- Pótleadás: 13. hét **Május 11. 23:59:59**

A Moodle rendszerbe kell feltölteni az elkészült megoldást és a laborvezetőnél kell megvédeni a labor idejében.
