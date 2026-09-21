# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad gör `.map()` — och vad är det INTE?  
2. Vad gör `.filter()` — och vad är det INTE?  
3. Varför `key` på list-syskon?  
4. Varför är `key={index}` ömtåligt när listan kan ändras?  
5. Beskriv metoden när du tvekar: hur visar jag alla rader?  
6. Varför inte `forEach` för att bygga listan i JSX?  
7. Varför `.filter()` (ny array) och inte `splice` på state?  
8. Peka i *din* kod: `map`, `key`, och filter-övningen — **varför** varje, inte “AI sa åt mig”.

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. Map går igenom varje element och returnerar en **ny** array — i React ofta JSX per sak. INTE filter, INTE magi.  
2. Filter skapar en ny array med element som klarar ett villkor. INTE map. INTE samma sak som en färdig ta-bort-knapp.  
3. Unikt id så React matchar rätt rad när listan ändras. Inte synlig text.  
4. Index följer *platsen*. När du lägger till/tar bort kan fel rad få fel identitet.  
5. (1) Data i state. (2) `map` till JSX med return. (3) `key` på varje barn.  
6. `forEach` returnerar inte arrayen du ska rita. Map gör det. innerHTML är att skriva DOM för hand.  
7. `splice` muterar samma array — luddig signal till React. Filter ger ny lista, samma idé som spread vid add.  
8. Subjektivt — rimligt om du kopplar metod → effekt. Fel om “AI skrev det” eller “React fixar listor själv”.

</details>

---

## Klart för paketet?

Om dina svar ligger nära facit, övningarna är gjorda, och du kan peka i egen kod:

- [ ] Målsvar map — egna ord, högt  
- [ ] Målsvar filter — egna ord, högt  
- [ ] Målsvar key — egna ord, högt  
- [ ] Målsvar metod — egna ord, högt  
- [ ] map / key / filter pekade i din fil  

Då har du landat array-målet. Nästa paket: [15-todo-klar-ta-bort](../vecka-40/15-todo-klar-ta-bort/) (mån 28/9).
