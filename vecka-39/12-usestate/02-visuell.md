# 02 — Visuellt: state → UI

Samma kassadisplay som i teoriguiden — nu som flöde. Ingen karta över input-fält eller `.map()`: state byts → JSX körs om → skärmen följer.

GitHub renderar diagrammen nedan automatiskt.

---

## Var sakerna bor

```mermaid
flowchart LR
  fil["JSX i filen<br/>hårdkodade rader"]
  state["State — kassadisplayen<br/>items + setItems"]
  ui["UI på skärmen"]

  fil -->|"första gången: startvärde"| state
  state -->|"skärmen läser items"| ui
  state -->|"setItems(nytt värde)"| state
```

**Vad diagrammet visar:** Hårdkodade rader stannar i filen tills du flyttar dem till displayen. Efter det är det `items` skärmen ska titta på.  
**Kom ihåg / INTE:** En lapp i fickan (`let` + `push`) är inte displayen. Utan `setItems` ritas den inte om.

---

## Kedjan när state ändras

```mermaid
flowchart TD
  A["Nytt värde? Ny array?"] --> B["setItems(...)"]
  B --> C["React: ny state"]
  C --> D["Re-render — JSX körs igen"]
  D --> E["UI läser items<br/>antal + rader stämmer"]
```

**Om du hoppar över set-funktionen:** du kanske har ändrat en array i minnet, men kassadisplayen (och kunden) ser samma sak.

**Målsvar (säg högt / skriv i README):** *“setItems ger ny state → React kör JSX igen → skärmen speglar datan.”*

---

## Problem vs display

```mermaid
flowchart TD
  subgraph svagt [Svagt mot Exam 2]
    E1["Tre hårdkodade JSX-rader"]
  end
  subgraph bra [Tydligare]
    E2["Array i useState"]
    E3["UI läser items / items.length"]
    E4["Bevis: setItems med ny array"]
  end
```

Till vänster: det *kan* se ut som en lista — men det finns inget att uppdatera.  
Till höger: det går att *peka* på var listan bor och varför skärmen följde efter ett klick.

---

## Checkpoint (privat)

Utan att titta på teoriguiden: säg kedjan högt (set → ny state → re-render → UI) och vad som saknas om du bara gör `push`. Jämför sen med diagrammen.

När kartan sitter: [03 — Övningar](./03-ovningar.md).
