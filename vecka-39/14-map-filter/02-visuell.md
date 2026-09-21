# 02 — Visuellt: map stämplar, filter silar

Samma kuvert och sil som i teoriguiden — nu som bild. Ingen karta över klar-bockar: en rad per sak, och en ny hög utan vissa.

GitHub renderar diagrammen nedan automatiskt.

---

## Från state till rader

```mermaid
flowchart LR
  state["films i state"] --> map["map — stämpel på varje kuvert"]
  map --> jsx["Ny array av JSX-rader"]
  jsx --> ui["UI: en rad per film"]
```

**Vad diagrammet visar:** Skärmen läser inte tre fasta stolar. Den får en stämplad rad per element.  
**Kom ihåg / INTE:** Map tar inte bort. Utan `key` saknar kuverten streckkod.

---

## filter är en annan maskin

```mermaid
flowchart TD
  A["Hela arrayen"] --> B["filter — sil"]
  B --> C["Ny array som klarade villkoret"]
  C --> D["Valfritt: map den silade till JSX"]
  A --> E["Originalet oförändrat"]
```

**Om du `splice`:ar state:** du muterar samma låda. Silen ger en ny skål.

**Målsvar (säg högt / skriv i README):** *“map omvandlar varje element (ofta till JSX). filter behåller vissa. Båda returnerar ny array.”*

---

## key när högen ändras

```mermaid
flowchart TD
  subgraph svagt [Ömtåligt]
    E1["Ingen key"]
    E2["key = index när listan växer/krymper"]
  end
  subgraph bra [Stabilare]
    E3["key = unikt id"]
    E4["Samma sak behåller samma kod"]
  end
```

Till vänster: React kan blanda ihop raderna. Till höger: streckkoden följer kuvertet.

---

## Checkpoint (privat)

Utan att titta: säg map vs filter högt (stämpel vs sil) och var `key` sitter. Jämför sen.

När kartan sitter: [03 — Övningar](./03-ovningar.md).
