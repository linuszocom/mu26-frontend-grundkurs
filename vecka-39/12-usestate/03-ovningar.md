# 03 — Övningar

**Omfång det här paketet:** `useState`, lista i state, re-render. En bevisknapp som byter till en ny array. Ingen input + lägg till. Ingen `.filter()` / ta bort. Ingen CSS-layout i React. Vite-projektet ska bara *köra* så du ser skärmen följa state.

AI får hjälpa dig knappa. Du måste kunna **peka och förklara** varje rad du behåller.

---

## Uppgift 1 — Rädda “tre limmade rader”

**Mål:** Se problemet när listan bara är JSX. Flytta den till `useState`. Visa den utifrån state.

**Problem först:** Du har den här komponenten. Den *ser* ut som en spellista. Den finns **inte** som data du kan byta. Det är läget du ska ta dig ur.

```jsx
function App() {
  return (
    <main>
      <h1>Spellista Loftet</h1>
      <p>Antal spår: 3</p>
      <ul>
        <li>Fönster mot gården</li>
        <li>Källarvärme</li>
        <li>Sista bussen</li>
      </ul>
    </main>
  );
}
```

**Krav:**
1. Öppna ditt Vite-projekt (`npm run dev`). Jobba i `App.jsx` (eller en ny komponent du importerar — inget nytt ramverk).
2. `import { useState } from "react"`.
3. `const [tracks, setTracks] = useState([ … minst två strängar, gärna tre … ])`. Spellista / kö / bakelser — ingen klar-bock, ingen ta-bort.
4. UI läser state: visa `{tracks.length}` (inte en hårdkodad `3`). Visa minst två poster via `tracks[0]`, `tracks[1]` (tredje om du har). **Inte** `.map()` som huvudnummer här.
5. Ingen textfält-lägg-till. Ingen CSS-övning.

**Klart-check (peka i DIN kod):**
- [ ] Antalet på skärmen kommer från `tracks.length`  
- [ ] Peka på `tracks` och `setTracks` — *varför* just den uppdelningen (läs vs skriv)  
- [ ] Peka: var startvärdet sitter, och *varför* listan inte längre är tre hårdkodade `<li>`  
- [ ] Du kan säga skillnaden state vs “jag skrev det i JSX” i en mening  

**Ägarskap:**
- Utan AI: skriv hooken och JSX själv.  
- Med AI: tillåtet som bollplank — spara prompten och **en mening** om vad du ändrade om AI gissade fel. Du ska kunna förklara varje rad.

---

## Uppgift 2 — Beviset: skärmen följer displayen

**Mål:** Bevisa re-render. Koppla klick → `setTracks` → ny array → UI.

Många tänker nu: “Listan ligger i state, då uppdateras den väl av sig själv.” Nej. Någon måste anropa set-funktionen med ett **nytt** värde.

**Brief:** En knapp. Vid klick: `setTracks` med en **ny** array som har en extra, redan skriven titel (ingen `input`). Visa att antal och den nya raden syns.

**Krav:**
1. Knapp `type="button"` som anropar din funktion.  
2. Funktionen bygger en **ny** array (skriv ut den, eller kopiera gamla värden + ett nytt i literal). Inte `tracks.push`.  
3. Efter klick: `{tracks.length}` ökar och den extra titeln syns (t.ex. `tracks[3]` eller en synlig text från sista platsen).  
4. I anteckningar: tre meningar — (a) vad state är, (b) vad re-render är och inte är, (c) varför `push` utan ny array/set inte är beviset.

**Klart-check (peka i DIN kod):**
- [ ] Klick ändrar skärmen utan att du redigerar filen mellan klicken  
- [ ] Peka på `setTracks(…)` och säg *varför* argumentet är en ny array  
- [ ] Peka på något UI som läser `tracks` efteråt — *varför* det följde med  
- [ ] Anteckningarnas tre meningar är *dina* ord, inte copy-paste från teoriguiden  

**Ägarskap:** Samma regel som uppgift 1. Om AI bygger ett formulär med “Lägg till”: ta bort fältet. Bevisknapp räcker.

---

## Uppgift 3 — Stretch (valfritt)

Andra klicket: `setTracks` till en **annan** ny array (t.ex. byt första titeln, eller gå tillbaka till två spår). Samma regel: ny array in, ingen `push`.

**Klart-check:** Kan du säga högt, utan att skämmas för att det är luddigt, *vilken* `setTracks`-rad som hör till vilket klick? Om ja: du har muntlig träning i mini-format.

---

## När du kört fast

1. Finns `import { useState } from "react"`?  
2. Kör metoden högt: vad ska skärmen följa? läs? set med nytt värde?  
3. Jämför med [01-teoriguide](./01-teoriguide.md) — särskilt tabellen och målsvaren.  
4. Klick gör inget: saknas `onClick`, fel funktionsnamn, eller du muterar samma array.  
5. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
