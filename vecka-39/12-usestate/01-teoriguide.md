# 01 — Teoriguide: useState & re-render

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när listan bara är hårdkodad JSX — sedan flyttar vi den till state så skärmen kan följa efter. Det är inte magi. Det är en metod.

---

## Problemet först — “det ser ju ut som en lista”

Många tänker nu: “Jag har tre rader i JSX. Klart. Listan finns.” Andas.

**Dåligt läge:** Tre titlar inklistrade i `App`. Det *syns* som en lista. Men det finns ingen enda plats att uppdatera. Vill du ha en fjärde rad måste du redigera JSX för hand. Byter du en titel på ett ställe och glömmer ett annat ljuger skärmen.

Det är två olika problem:

1. **Ingen föränderlig data** — bara “det jag skrev i filen”.  
2. **Skärmen vet inte när datan ändrats** — inget som säger “måla om”.

`useState` löser båda: datan bor i komponenten, och set-funktionen är signalen.

Det här paketet stannar där. **Inte** input + lägg till. **Inte** sila bort rader. En liten knapp som *bevisar* att skärmen följer state räcker.

---

## State — kassalådans display

**Metafor:** Tänk **displayen på en kassalåda**. Det som står där är det kassören och kunden tittar på — den enda listan/siffran som räknas just nu. Kladdar du på en lapp i fickan ändras inte displayen. Skriver du ett nytt belopp *på displayen* tittar alla dit och ser det nya.

I React kallas den displayen **state**. Listan ska bo där. Det som syns i UI ska spegla displayen.

**Props** = en prislapp någon annan klistrat på varan (data inifrån en förälder).  
**State** = det kassan *äger* och kan byta över tid (displayen).

**Vad det är:** State = data React håller i komponenten.  
**Varför det finns:** Så UI kan ändras över tid utan att du redigerar JSX för hand varje gång.  
**Om det saknas / vad det INTE är:** State är INTE props. Utan state är listan statisk. State är INTE “spara i en `let` utanför React” — då saknas signalen till skärmen. Det är INTE CSS, och INTE färdigt lägg-till-flöde.

**Målsvar (säg högt / skriv i README):** *“State är data React håller i komponenten. När du ändrar den med set-funktionen renderas UI om så skärmen matchar den nya datan.”*

---

## useState — två grejer i ett paket

Många tänker: “Hakparenteserna… låter som magi.” Andas. Det är inte magi. Det är en array som plockas isär.

```jsx
import { useState } from "react";

const [items, setItems] = useState(["Ost", "Bröd"]);
```

| Del | Vad det är (+ bild) | Varför | Om saknas / INTE |
|------|---------------------|--------|------------------|
| `import { useState }` | Verktyget som skapar displayen | Annars finns inte funktionen | `useState is not defined` — saknad import, inte “React trasigt” |
| Startvärdet `["Ost", "Bröd"]` | Första som står på displayen | Appen måste ha ett läge att visa | INTE “evig sanning” — du får byta sen |
| `items` | Läs: vad står där *nu* | UI ska läsa här | INTE något du ska skriva över med `items = …` |
| `setItems` | Skriv: byt det som står på displayen | Signalen till React | Utan den: skärmen får ingen anledning att följa efter |

**Vad det är:** `useState(start)` ger ett par: nuvarande värde + funktion som sätter nytt värde.  
**Varför det finns:** Läs och skriv ska inte blandas ihop.  
**Om det saknas / vad det INTE är:** `setItems` är INTE samma sak som att mutera arrayen i smyg. Du anropar den med ett **nytt** värde.

---

## Re-render — displayen ritas om

**Vad det är:** Re-render = React kör komponentens JSX **igen** efter ny state, så skärmen speglar datan.  
**Varför det finns:** Annars hade du fått jaga DOM-noder för hand (det React just slipper dig).  
**Om det saknas / vad det INTE är:** Re-render är INTE att du skriver `document.querySelector` och klistrar in HTML. Det är INTE “sidan laddas om”. Utan `setItems` (om du bara gör `items.push(...)`) kan displayen ligga kvar — React fick ingen tydlig “nytt värde”.

**Bevis, inte kassaflöde:** En knapp som anropar `setItems` med en **ny array** (en extra, redan skriven rad). Du ska *se* att antal och text följer efter. Det är INTE “lägg till från textfält” — det kommer i nästa paket.

```jsx
function bevis() {
  setItems(["Ost", "Bröd", "Mjölk"]);
}
```

Klick → ny array i state → JSX körs om → `{items.length}` och raderna som läser `items` uppdateras.

**Målsvar (säg högt / skriv i README) — re-render:**  
*“Re-render betyder att React kör JSX igen efter ny state. Det är inte att du skriver om DOM för hand.”*

---

## Listan ska läsas från state

**Vad det är:** Det som syns (titlar, antal, rader) hämtas från `items` — inte från tre hårdkodade JSX-barn du glömmer synka.  
**Varför det finns:** Exam 2 ska visa listan dynamiskt. Då måste det finnas *en* lista att visa.  
**Om det saknas / vad det INTE är:** Tre `<li>Köp mjölk</li>` i filen är INTE en React-lista du kan växa. Index-slots (`items[0]`, `items[1]`) räcker som **övning** här. `.map()` över hela listan får eget paket.

**Målsvar (säg högt / skriv i README) — listan:**  
*“Det som syns i listan ska läsas från state — inte från hårdkodade JSX-rader du glömmer uppdatera.”*

---

## Metod — när du tvekar “ska det här in i useState?”

Det är inte magi. Tre frågor:

1. **Vad ska skärmen följa över tid?** (en lista, ett tal, en text) → det hör hemma i `useState`.  
2. **Läs** från första namnet (`items`). Visa `{items.length}` och innehållet.  
3. **Skriv** bara via `setItems` med ett **nytt** värde. Titta på skärmen. Följde den efter?

**Vad metoden är:** Ett sätt att inte blanda “filen jag skrev” med “datan just nu”.  
**Varför den finns:** Utan den hårdkodar du, eller muterar en array som React inte reagerar på.  
**Om den saknas:** Knappen “funkar” i huvudet men UI ligger kvar.

**Målsvar (säg högt / skriv i README) — metod:**  
*“Vad ska skärmen följa? Lägg det i useState. Läs värdet, skriv bara via set-funktionen, skicka in ett nytt värde (t.ex. en ny array).”*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| Tre hårdkodade JSX-rader = “lista i React” | Det syns. Det går inte att uppdatera från ett ställe. Flytta till state |
| `let lista = […]` + `lista.push` | Ingen React-state. Displayen får ingen signal |
| `items.push("Ny")` sen inget / samma array in i set | Muterar samma låda. Skicka en **ny** array till `setItems` |
| Glömma `import { useState }` | Inte magi som slutar funka — saknad import |
| Re-render = jag rör DOM | React kör om din JSX. Du byter state |
| Bygga textfält + lägg till “för att bli klar” | Nästa paket. Idag: lista i state + bevis |
| Styla layouten “på riktigt” | Ingen CSS-i-React-guide här. Fokus = state |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad är state? (sikta på målsvaret, tänk kassadisplayen)  
2. Vad händer när du anropar set-funktionen?  
3. Vad är re-render — och vad är det INTE?  
4. Varför ska listan läsas från state? (Exam 2: visa listan)

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna.
