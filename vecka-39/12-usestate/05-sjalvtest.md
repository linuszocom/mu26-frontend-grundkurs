# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad är **state** i React, på en mening?  
2. Vad gör `useState` — vad får du tillbaka?  
3. Vad är **re-render** — och vad är det INTE?  
4. Du har tre `<li>` hårdkodade i JSX. Varför räcker inte det när listan ska kunna ändras?  
5. Beskriv metoden när du tvekar: ska det här in i `useState`?  
6. Du gör `items.push("Ny")` och hoppas att skärmen följer. Vad saknas / vad är fel?  
7. Varför ska listan läsas från state inför Exam 2?  
8. Peka i *din* kod: `useState`, `set…`, och ett ställe UI läser värdet — **varför** varje, inte “AI sa åt mig”.

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. State = data React håller i komponenten. När den ändras med set-funktionen renderas UI om så skärmen matchar.  
2. `useState(start)` ger ett par: nuvarande värde (t.ex. `items`) + funktion som sätter nytt värde (`setItems`). Import krävs.  
3. Re-render = React kör JSX igen efter ny state. INTE att du skriver om DOM för hand, INTE sidomladdning.  
4. Hårdkodade rader har ingen gemensam data att uppdatera — du jagar JSX. Exam 2 kräver dynamisk lista.  
5. (1) Vad ska skärmen följa? (2) Läs från state. (3) Skriv bara via set-funktionen med ett nytt värde.  
6. `push` muterar samma array; utan `setItems` med **ny** array får React ofta ingen tydlig signal. Displayen kan ligga kvar.  
7. Visa listan dynamiskt = UI måste läsa den lista som kan växa. Den listan hör hemma i state.  
8. Subjektivt — rimligt om du kopplar rad → effekt. Fel om svaret bara är “AI skrev det” eller “jag klickade runt”.

</details>

---

## Klart för paketet?

Om dina svar ligger nära facit, övningarna är gjorda, och du kan peka i egen kod:

- [ ] Målsvar state — egna ord, högt  
- [ ] Målsvar re-render — egna ord, högt  
- [ ] Målsvar listan i state — egna ord, högt  
- [ ] Målsvar metod — egna ord, högt  
- [ ] `useState` / `set…` / UI-läsning pekade i din fil  

Då har du landat useState-målet. Nästa paket: [13-events-lagg-till](../13-events-lagg-till/).
