# 01 — Teoriguide: JavaScript-syntax

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när du kopierar samma siffra överallt — sedan sätter vi namnlappar på burkar, skriver receptkort, *frågar* en boolean och går igenom en hylla. Det är inte magi. Det är en metod. Ingen React. Ingen DOM. Ingen Vite. Inga array-metoder i det här paketet.

---

## Problemet först — “jag skriver om 89 tre gånger”

Många tänker nu: “JavaScript… det är appar och knappar.” Andas. Idag är det **värden** och **steg du kan köra om**. Du tittar i **konsolen** (DevTools → Console), inte på en snygg sida.

**Dåligt läge:**

```javascript
console.log(12 + 12 + 12);
console.log("Tre varor à 12 kr");
```

Priset ändras till 15. Du jagar varje `12`. Det är därför burken finns.

---

## Variabel — namnlapp på en burk

**Metafor:** I ett skafferi står burkar. På locket sitter en **namnlapp** (`pris`, `momsKlar`). Inuti ligger innehållet. Du säger lappens namn — du släpar inte om burken med händerna varje gång.

**Vad det är:** En **variabel** = namngiven plats för ett värde.  
**Varför den finns:** Ett ställe att läsa och (ibland) byta, i stället för copy-paste.  
**Om den saknas / vad den INTE är:** INTE en webbsida. INTE React. Utan variabel jagar du samma siffra på tre rader.

Tre sorters innehåll i burken idag:

| Typ | Vad som ligger i burken | Exempel |
|-----|-------------------------|---------|
| **sträng** | text | `"Kanelbulle"` (citattecken) |
| **number** | tal | `12` (utan citattecken) |
| **boolean** | av/på | `true` / `false` |

Två lappar du sätter på burken:

- **`const`** — lappen sitter fast. Du byter inte *vilken burk namnet pekar på*. Standard när värdet är klart.  
- **`let`** — du får fylla om (t.ex. en löpande summa).  
- **`var`** — inte i det här paketet.

**Målsvar (säg högt / skriv i README):**  
*“En variabel är en burk med namnlapp. Inuti ligger ett värde — text, tal eller true/false — så jag kan återanvända det utan att skriva om samma sak överallt.”*

**Målsvar (säg högt / skriv i README) — const vs let:**  
*“const när värdet är klart och inte ska bytas ut. let när jag behöver tilldela om, till exempel en summa som växer.”*

---

## console.log — titta i burken

**Vad det är:** En utskrift till **konsolen** så du *ser* värdet.  
**Varför den finns:** Annars händer koden tyst. Du gissar.  
**Om den saknas / vad den INTE är:** INTE text på webbsidan. INTE “spara filen”. Utan logg ser du inte om burken innehåller `12` eller `"12"`.

```javascript
const produkt = "Kanelbulle";
let summa = 0;
console.log(produkt);
console.log(summa);
```

---

## Funktion — receptkortet

**Metafor:** Ett **receptkort** på kylskåpet: namn överst, ingredienser inom parentes, steg i mitten. Du *skriver* kortet en gång (deklarerar). Du *lagar* när du är hungrig (anropar med `()`). Kortet i lådan lagar ingen mat.

**Vad det är:** Ett namngivet kodblock du deklarerar och anropar. Det kan ta emot data (parametrar) och ge tillbaka resultat (`return`).  
**Varför den finns:** Samma steg igen — utan att kopiera blocket.  
**Om den saknas / vad den INTE är:** INTE matte-skräck. INTE en komponent. Utan `namn()` körs den inte — oavsett hur snyggt kortet är.

```javascript
function radTotal(pris, antal) {
  return pris * antal;
}

const rad = radTotal(12, 3);
console.log(rad);
```

**Målsvar (säg högt / skriv i README):**  
*“En funktion är ett receptkort: jag skriver stegen en gång och kör dem när jag behöver resultatet. Utan anrop händer ingenting.”*

**Känna igen — pilen `=>`:** Du kommer se `const namn = (x) => …` i kod du läser. Samma recept, kortare lapp. I det här paketet *skriver* du namngiven `function`. Pilen är inte ny logik och inte ett krav.

---

## if / else — dörren som frågar

Många tänker nu: “Jag har ju `true` i burken — då händer rabatten väl av sig själv?” Andas. En boolean som bara *ligger där* gör ingenting.

**Dåligt läge:**

```javascript
const harRabatt = true;
let summa = 54;
console.log(harRabatt);
console.log(summa);
```

`true` loggas. Summan är fortfarande 54. Lappen lästes aldrig som en fråga.

**Metafor:** En **dörr**. `if` öppnar den ena vägen när svaret är true. `else` är den andra dörren — inte en extra fråga.

**Vad det är:** Ett vägval. Parentesen efter `if` måste bli `true` eller `false`.  
**Varför den finns:** Samma kod ska kunna göra *olika* saker beroende på data.  
**Om den saknas / vad den INTE är:** INTE en loop. INTE magi. Utan `if` körs alltid samma rader, oavsett boolean.

```javascript
const harRabatt = true;
let summa = 54;

if (harRabatt) {
  summa = summa * 0.9;
} else {
  console.log("Ingen rabatt");
}
console.log(summa);
```

**`else if` — fler än två zoner.** Smalaste frågan först, annars dör en gren:

```javascript
if (text === "") {
  console.log("tom");
} else if (text.length < 3) {
  console.log("kort");
} else {
  console.log("ok");
}
```

**`===` vs `==`:** `===` frågar “samma värde *och* samma typ?”. `==` gissar och tvingar typ — `"5" == 5` blir `true`. I din kod: bara `===`.

| Uttryck | Resultat | Varför |
|---------|----------|--------|
| `"5" === 5` | `false` | text vs tal |
| `"5" == 5` | `true` | JS gissar — fällan |

**Målsvar (säg högt / skriv i README):**  
*“if frågar en boolean och väljer väg. else är den andra dörren. === jämför värde och typ — == gissar och använder jag inte.”*

---

## Array — numrerad hylla

**Problem först:** Tre sysslor som tre lösa burkar. Du vill peka på “första” och veta *hur många*.

**Metafor:** En **hylla med nummer**. Första facket heter `0`, inte `1`. `.length` är hur många som *står där* — inte sista numret.

**Vad det är:** En lista i hakparenteser: `[]`. Du läser med index: `todos[0]`.  
**Varför den finns:** Flera värden av samma sort, ett namn.  
**Om den saknas / vad den INTE är:** INTE tre lösa variabler du jagar. INTE array-metoder i det här paketet. En hylla. Ett index. En längd.

```javascript
const todos = ["Köp mjölk", "Öppna VS Code", "Committa"];
console.log(todos[0]);
console.log(todos.length);
```

Konsolen: `"Köp mjölk"` och `3`.

**Målsvar (säg högt / skriv i README):**  
*“En array är en numrerad hylla. Första facket heter 0. .length är antal saker — inte sista indexet.”*

---

## Objekt — en rad med namn

**Metafor:** Hyllan är *många* saker. Objektet är **en** sak med flera lappar på samma kort: `text`, `done`.

**Vad det är:** Nyckel/värde i klamrar: `{ text: "Köp mjölk", done: false }`. Du läser med **punktnotation**: `todo.text`.  
**Varför den finns:** En rad behöver mer än en sträng — t.ex. text *och* av/på.  
**Om den saknas / vad den INTE är:** INTE en array (ingen numrering 0, 1, 2). INTE att du ska skriva över listor i smyg. En rad. Namngivna fält.

```javascript
const todo = {
  text: "Köp mjölk",
  done: false
};
console.log(todo.text);
console.log(todo.done);
```

**Målsvar (säg högt / skriv i README):**  
*“Ett objekt är en rad med namngivna fält. Jag läser med punkt: todo.text.”*

---

## for...of — gå längs hyllan

**Problem först:** Tre `console.log(todos[0])`, `todos[1]`, `todos[2]`. Hyllan växer — du jagar rader.

**Metafor:** Du går **fack för fack** och tittar i varje. Inte magi. En rundgång.

**Vad det är:** `for (const rad of todos) { … }` — en sak i taget ur arrayen.  
**Varför den finns:** Samma steg för varje grej, utan att räkna index för hand.  
**Om den saknas / vad den INTE är:** INTE tre copy-paste-loggar. INTE array-metoder. `for...of` *läser* hyllan. Senare möter du sätt att gå igenom listan som *bygger en ny lista* — samma rundgång, annat jobb. Först äger du läsningen.

```javascript
const todos = ["Köp mjölk", "Öppna VS Code", "Committa"];

for (const rad of todos) {
  console.log(rad);
}
```

**Målsvar (säg högt / skriv i README):**  
*“for...of går igenom hyllan en sak i taget. Jag läser. Jag skriver inte tre identiska loggar för hand.”*

---

## Metod — när du tvekar “hur bryter jag ner det här?”

Det är inte magi. Fyra frågor:

1. **Vad ska hända?** (en mening)  
2. **Vilken data?** (burkar — `const` / `let`, rätt typ; hylla eller rad?)  
3. **Vilka steg?** (receptkort? fråga med `if`? gå längs hyllan?)  
4. **Testa** varje steg med `console.log`.

**Vad metoden är:** Dela upp, namnge, titta.  
**Varför den finns:** Annars klistrar du tre formler i varandra och vet inte vilken som ljuger.  
**Om den saknas:** Du ser “NaN” eller fel text och har ingen logg som visar *vilken* burk.

**Målsvar (säg högt / skriv i README) — metod:**  
*“Vad ska hända? Vilken data? Vilka steg — recept, if-dörr eller for...of? Testa varje steg med console.log.”*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| `"12" + 3` ser ut som tal | Citattecken → sträng. Tal skrivs utan |
| `const summa = 0` sen `summa = summa + 12` kraschar | Löpande summa → `let` |
| Skriva funktionen men aldrig `namn()` | Deklaration ≠ anrop |
| `console.log` = visa på sidan | Konsolen. Sidan är inte jobbet här |
| `var` “för att gamla tutorials” | `const` / `let` |
| `harRabatt` bara loggas | Fråga den med `if` |
| `"5" == 5` | `===` — typen räknas |
| `todos[1]` som “första” | Index börjar på `0` |
| `.length` som sista numret | Antal saker. Sista index = längd minus ett |
| `todo[text]` utan citat / fel nyckel | Punkt: `todo.text` |
| Tre `console.log(todos[0])` … `[2]` | `for...of` |
| React / `document.querySelector` / array-metoder | Inte i det här paketet |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad är en variabel? (sikta på burken)  
2. `const` vs `let` i en mening  
3. Vad gör en funktion — och vad händer utan anrop?  
4. Vad gör `if` — och varför `===` inte `==`?  
5. Array vs objekt i en mening. Vad gör `for...of`?  
6. Varför `console.log` när du lär dig?

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna i konsolen.
