# 02 — Visuellt: event → state → UI

Samma ringklocka och postlåda som i teoriguiden — nu som flöde. Ingen ta-bort-karta: tangent synkar lappen, klick flyttar till bunten.

GitHub renderar diagrammen nedan automatiskt.

---

## Två displayytor

```mermaid
flowchart LR
  tangent["Tangent i fältet"] --> onChange["onChange"]
  onChange --> draft["draft — lappen"]
  draft --> fält["Input value=draft"]
  klick["Klick på knapp"] --> onClick["onClick"]
  onClick --> ny["Ny array ...items, text"]
  ny --> setItems["setItems"]
  setItems --> lista["items — bunten"]
  lista --> ui["UI: join + antal"]
```

**Vad diagrammet visar:** Fältet och listan är olika state. Klockan (`onChange`/`onClick`) är bara kopplingen.  
**Kom ihåg / INTE:** `onChange` lägger inte till. `push` ritar inte om pålitligt.

---

## Kedjan när du lägger till

```mermaid
flowchart TD
  A["Text i draft?"] -->|tom efter trim| B["Avbryt — ingen tom rad"]
  A -->|ja| C["setItems ...items, text"]
  C --> D["setDraft tom sträng"]
  D --> E["Re-render"]
  E --> F["Listan och fältet matchar state"]
```

**Om du hoppar till `push`:** samma låda, luddig signal. Gå tillbaka till ny array.

**Målsvar (säg högt / skriv i README):** *“Klick läser draft, skickar en ny array till set-funktionen, tömmer fältet — sen följer UI.”*

---

## Problem vs kopplad kassa

```mermaid
flowchart TD
  subgraph svagt [Svagt mot Exam 2]
    E1["Fält och knapp utan handlers"]
    E2["push på state-arrayen"]
  end
  subgraph bra [Tydligare]
    E3["value + onChange på fältet"]
    E4["onClick → spread-ny array"]
    E5["Töm draft efteråt"]
  end
```

Till vänster: det *kan* se ut som ett formulär. Till höger: det går att *peka* på vad klicket gör.

---

## Checkpoint (privat)

Utan att titta: säg kedjan högt (onChange → draft, onClick → ny array → töm). Jämför sen.

När kartan sitter: [03 — Övningar](./03-ovningar.md).
