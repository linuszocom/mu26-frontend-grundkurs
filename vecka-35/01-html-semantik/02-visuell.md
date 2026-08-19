# 02 — Visuellt: dokumentets karta

Samma butiksmetafor som i teoriguiden — nu som bild. Ingen design-guide den här veckan: struktur räcker att se som träd.

GitHub renderar diagrammen nedan automatiskt.

---

## Dokumentträd — grundplan och avdelningar

```mermaid
flowchart TD
  DOCTYPE["!DOCTYPE html"]
  HTML["html — hela lokalen"]
  HEAD["head — följesedel OM sidan"]
  BODY["body — det kunden SER"]
  TITLE["title — fliknamn"]
  META["meta charset"]
  HEADER["header — namnskylt vid ingången"]
  MAIN["main — huvudinnehåll"]
  FOOTER["footer — sidfot"]

  DOCTYPE --> HTML
  HTML --> HEAD
  HTML --> BODY
  HEAD --> META
  HEAD --> TITLE
  BODY --> HEADER
  BODY --> MAIN
  BODY --> FOOTER
```

**Vad diagrammet visar:** Var metadata respektive synligt innehåll bor.  
**Varför det hjälper:** Du ser att `head` och `header` ligger på olika ställen.  
**Kom ihåg / INTE:** `head` ≠ `header`. Head är följesedeln. Header är namnskylten i body.

---

## Betydelse vs generisk kartong — problemet som bild

```mermaid
flowchart LR
  subgraph svagt [Svagt — inga avdelningsnamn]
    D1[div]
    D2[div]
    D3[div]
  end
  subgraph bra [Tydligare — roller]
    H[header]
    M[main]
    F[footer]
  end
```

Till vänster: tre kartonger utan betydelse — sidan *kan* synas, men koden säger inget.  
Till höger: tre roller du (och verktyg) kan läsa. Det är semantik i en bild.

**Målsvar (säg högt / skriv i README):** *“Semantiska taggar bär betydelse; div är bara en låda utan lapp.”*

---

## Metod som flöde

När du tvekar — följ pilarna. Det är inte magi; det är intervjun.

```mermaid
flowchart TD
  A[Vad ÄR den här biten?] --> B{Finns tagg med samma betydelse?}
  B -->|Ja| C[Använd den taggen]
  B -->|Nej / osäker| D[Fråga eller slå upp — gissa inte div]
  C --> E[Nästa bit]
  D --> A
```

**Om du hoppar till “låda”:** risken är `div` överallt. Gå tillbaka till “Vad *är* det?”.

---

## Checkpoint (privat)

Utan att titta på teoriguiden: rita (eller skriv) skillnaden `head` vs `header` i en mening. Jämför sen med diagrammet ovan.

När kartan sitter: [03 — Övningar](./03-ovningar.md).
