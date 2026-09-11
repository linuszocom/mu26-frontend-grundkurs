# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad är en **funktionskomponent** i en mening?  
2. Vad är **JSX** — skylt-bilden, inte bara “HTML i JS”?  
3. Varför `className` och inte `class`?  
4. Vad är **props** (följesedel / namnbricka)?  
5. Vem *skickar* props och vem *läser* dem?  
6. När gör du en egen kloss + props, enligt metoden?  
7. Varför ingen `useState` i det här paketet?  
8. Peka i *din* kod: en prop i `App` och samma värde i barnet — **varför** den kedjan.

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. En funktion (stor bokstav) som returnerar det som ska synas — en UI-bit du återanvänder.  
2. Skylten på klossen: taggar som beskriver utseendet, inne i JS-filen — inte en separat `.html` i Explorer.  
3. `class` är reserverat i JavaScript; JSX använder `className`.  
4. In-data till klossen så samma komponent kan visa olika innehåll.  
5. Föräldern skickar (i JSX-attribut). Barnet läser (`props.namn` / klamrar).  
6. Upprepad UI-bit → kloss. Olika innehåll → props. Växa vid klick → state senare.  
7. Listan ska stå still så du äger props först. State kommer i nästa paket. Exam 2 kommer senare.  
8. Subjektivt — rimligt om du pekar båda ändarna. Fel om “det bara syntes”.

</details>

---

## Klart för paketet?

Om dina svar ligger nära facit, korten har props, och du kan peka i egen kod:

- [ ] Målsvar komponent — egna ord, högt  
- [ ] Målsvar JSX — egna ord, högt  
- [ ] Målsvar props — egna ord, högt  
- [ ] Förälder → barn pekad  

Då har du landat JSX/props. Nästa paket: [12-usestate](../vecka-39/12-usestate/).
