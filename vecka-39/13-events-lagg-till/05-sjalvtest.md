# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad gör `onChange` på ett textfält — och vad gör det **inte**?  
2. Vad gör `onClick` på lägg-till-knappen?  
3. Varför två state (fält vs lista)?  
4. Vad betyder `e.target.value`?  
5. Beskriv metoden när du tvekar: hur får jag in raden i listan?  
6. Varför `[...items, text]` och inte `items.push(text)` när listan är state?  
7. Varför tömma fältet efter ett lyckat tillägg?  
8. Peka i *din* kod: `onChange`, `onClick`, spread — **varför** varje, inte “AI sa åt mig”.

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. `onChange` synkar det du skriver till `draft` (lappen). Den lägger **inte** till i listan.  
2. `onClick` kör din add-funktion: läs text, ny array, töm fält — sen re-render.  
3. Det du skriver nu och det som redan är sparat är olika data. Ett state för varje.  
4. Texten som står i fältet just då. Inte magi.  
5. (1) `onChange` → `setDraft`. (2) `onClick`. (3) Om text finns: `setItems([...items, text])`, töm draft.  
6. `push` muterar samma array; React får ofta ingen tydlig ny lista. Spread bygger ny array.  
7. Annars ligger gammal text kvar och nästa klick kan dubbla eller förvirra.  
8. Subjektivt — rimligt om du kopplar handler → effekt. Fel om “AI skrev det” eller querySelector som förklaring.

</details>

---

## Klart för paketet?

Om dina svar ligger nära facit, övningarna är gjorda, och du kan peka i egen kod:

- [ ] Målsvar event — egna ord, högt  
- [ ] Målsvar immutabel — egna ord, högt  
- [ ] Målsvar två state — egna ord, högt  
- [ ] Målsvar metod — egna ord, högt  
- [ ] onChange / onClick / spread pekade i din fil  

Då har du landat lägg-till-målet. Nästa paket: [14-map-filter](../14-map-filter/).
