# 02 — Visuellt: skylt och följesedel

Samma bilder som i teoriguiden — nu som flöde. Ingen `useState`. GitHub renderar diagrammen automatiskt.

---

## Vem skriver sedeln, vem läser den?

```mermaid
flowchart LR
  app["App — föräldern"]
  sedel["Följesedel<br/>namn / ljus"]
  kort["Vaxtkort — barnet"]
  skylt["JSX-skylten<br/>det som syns"]

  app -->|"skickar props"| sedel
  sedel --> kort
  kort --> skylt
```

**Kom ihåg / INTE:** Barnet hittar inte på “Basilika” själv om du vill återanvända klossen. Sedeln kommer utifrån.

---

## Copy-paste vs en kloss

```mermaid
flowchart TD
  subgraph svagt [Svagt]
    A1["Tre article-block i App"]
  end
  subgraph bra [Tydligare]
    B1["En Vaxtkort-funktion"]
    B2["Tre följesedlar i App"]
  end
```

Till vänster: tre ställen att laga skylten. Till höger: en skylt, tre namnbrickor.

**Målsvar (säg högt / skriv i README):** *“Föräldern skickar props. Barnet läser dem i JSX med klamrar.”*

---

## Checkpoint (privat)

Säg kedjan högt: kloss → skylt (JSX) → följesedel (props). Jämför sen med diagrammen.

När kartan sitter: [03 — Övningar](./03-ovningar.md).
