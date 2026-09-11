# 02 — Visuellt: burkar, dörr, hylla

Samma bilder som i teoriguiden — nu som flöde. Ingen React, ingen DOM, inga array-metoder. GitHub renderar diagrammen automatiskt.

---

## Värdet måste ligga någonstans

```mermaid
flowchart LR
  lapp["Namnlapp<br/>produkt"]
  burk["Burk<br/>Kanelbulle"]
  logg["console.log<br/>du SER innehållet"]

  lapp --> burk
  burk --> logg
```

**Vad diagrammet visar:** Lappen är namnet. Burken är värdet. Loggen är beviset.  
**Kom ihåg / INTE:** `console.log` är inte sidans synliga text.

---

## Receptkortet måste anropas

```mermaid
flowchart TD
  A["Skriv receptkortet<br/>function radTotal(...)"] --> B["Kortet ligger i lådan"]
  B --> C["Anropa: radTotal(12, 3)"]
  C --> D["return / console.log"]
```

Utan C: inget resultat. Kortet är inte magi.

**Målsvar (säg högt / skriv i README):** *“Deklarera = skriva receptkortet. Anropa = laga med namn().”*

---

## Dörren — vägvalet

Boolean i burken räcker inte. Koden måste *fråga*.

```mermaid
flowchart TD
  Q["if (harRabatt)"] -->|true| A["Öppen dörr<br/>sänk summan"]
  Q -->|false| B["Andra dörren else<br/>logga: ingen rabatt"]
```

**Vad diagrammet visar:** En fråga, två vägar. `else` är inte en extra fråga — det är den stängda dörren.  
**Kom ihåg / INTE:** Utan `if` är `true` bara en lapp. `===` frågar värde och typ. `==` gissar.

**Målsvar (säg högt / skriv i README):** *“if öppnar en dörr när svaret är true. else är den andra vägen.”*

---

## Hyllan — numrerad lista

```mermaid
flowchart LR
  subgraph hylla ["todos — tre fack"]
    i0["[0]<br/>Köp mjölk"]
    i1["[1]<br/>Öppna VS Code"]
    i2["[2]<br/>Committa"]
  end
```

Första facket heter **0**. `.length` är **3** (antal), inte 2.

**Vad diagrammet visar:** En array är en hylla med nummer.  
**Kom ihåg / INTE:** `[1]` är andra saken. Array-metoder hör inte hit — du pekar med index.

**Målsvar (säg högt / skriv i README):** *“Array = hylla. Index från 0. .length = hur många som står där.”*

---

## Etikettlådan — ett objekt

Hyllan är många saker. Kortet är *en* rad med namngivna lappar.

```mermaid
flowchart TD
  O["todo"]
  O --> T["text → Köp mjölk"]
  O --> D["done → false"]
```

Du läser med punkt: `todo.text`, `todo.done`.

**Vad diagrammet visar:** Nyckel till vänster, värde till höger — samma låda.  
**Kom ihåg / INTE:** Det är inte en array. Ingen `[0]` på fälten. Punktnotation, inte gissa nyckelnamnet.

**Målsvar (säg högt / skriv i README):** *“Objekt = en rad med namn. Jag läser todo.text.”*

---

## Rullbandet — for...of

Samma hylla. En sak i taget. Du tittar, loggar, går vidare.

```mermaid
flowchart LR
  A["todos[0]"] --> B["todos[1]"] --> C["todos[2]"]
```

```javascript
for (const rad of todos) {
  console.log(rad);
}
```

**Vad diagrammet visar:** Rundgång längs hyllan — inte tre handskrivna loggar.  
**Kom ihåg / INTE:** `for...of` *läser*. Senare finns sätt att gå igenom listan som *bygger en ny lista*. Först äger du stegen.

**Målsvar (säg högt / skriv i README):** *“for...of går fack för fack. En sak i taget.”*

---

## Metod när något ska räknas

```mermaid
flowchart TD
  Q1["Vad ska hända?"] --> Q2["Vilka burkar / hylla / rad?"]
  Q2 --> Q3["Receptkort? if-dörr? for...of?"]
  Q3 --> Q4["console.log varje steg"]
```

---

## Checkpoint (privat)

Säg högt: burk, tre typer, `const`/`let`, receptkort + anrop, dörren (`if`/`===`), hyllan (`[0]` / `.length`), etikettlådan (`todo.text`), rullbandet (`for...of`), var loggen syns. Jämför sen med diagrammen.

När kartan sitter: [03 — Övningar](./03-ovningar.md).
