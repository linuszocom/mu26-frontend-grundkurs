# 02 — Visuellt: pincett vs LEGO-kartong

Samma bilder som i teoriguiden — nu som flöde. Ingen `useState`. GitHub renderar diagrammen automatiskt.

---

## Två sätt att röra UI

```mermaid
flowchart TD
  subgraph pincett [Pincett — DOM]
    D1["Hitta nod"] --> D2["Ändra text/element"]
    D2 --> D3["Upprepa för nästa ställe"]
  end

  subgraph mall [Mall — React]
    R1["Beskriv vad som ska synas"] --> R2["Komponent = LEGO-kloss"]
    R2 --> R3["React sätter ihop det som syns"]
  end
```

**Kom ihåg / INTE:** Pincett är inte “fel”. Den skalar dåligt när samma data ska synas många gånger.

---

## Kartongen (Vite) → klossen du redigerar

```mermaid
flowchart LR
  create["npm create vite"] --> install["npm install"]
  install --> folder["Open Folder i VS Code"]
  folder --> dev["npm run dev"]
  dev --> app["src/App.jsx — din kloss"]
```

`main.jsx` tänder lampan. `App.jsx` är klossen du börjar skruva i.

**Målsvar (säg högt / skriv i README):** *“Vite skapar kartongen. App.jsx är LEGO-klossen jag redigerar först.”*

---

## Checkpoint (privat)

Säg högt: pincett vs mall, komponent = kloss, create → install → Open Folder → dev. Jämför sen med diagrammen.

När kartan sitter: [03 — Övningar](./03-ovningar.md).
