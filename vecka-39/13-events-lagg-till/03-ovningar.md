# 03 — Övningar

**Omfång det här paketet:** `onChange` på textfält, `onClick` på knapp, immutabel array-uppdatering (ny array, inte `push`). Lägga till syns i UI. Ingen markera-klar, ingen ta-bort-knapp, ingen CSS-layout i React. Ingen `.map()`-uppgift — `join` + `length` räcker för att se tillägget.

AI får hjälpa dig skriva. Du måste kunna **peka och förklara** varje rad du behåller.

---

## Uppgift 1 — Inköpslista Hörnet

**Mål:** Koppla fält + knapp till en lista i state. Ny array vid lägg till.

**Problem först:** Du har en lista i `useState` (från förra paketet eller ny). Ett fält och en knapp *syns*. Ingenting hamnar i listan när du klickar. Det är läget du ska ta dig ur.

Startläge att utgå från (bygg vidare — koppla events):

```jsx
import { useState } from "react";

function App() {
  const [items, setItems] = useState(["Havregryn", "Äpplen"]);
  const [draft, setDraft] = useState("");

  return (
    <main>
      <h1>Inköpslista Hörnet</h1>
      <input placeholder="Ny vara" />
      <button type="button">Lägg till</button>
      <p>Antal: {items.length}</p>
      <p>{items.join(" · ")}</p>
    </main>
  );
}
```

**Krav:**
1. Vite igång. Inköpstema (varor, butik). Inga klar-bockar, ingen ta-bort.
2. `value={draft}` och `onChange` som gör `setDraft(e.target.value)`.
3. `onClick` som: `trim` → avbryt om tomt → `setItems([...items, text])` → `setDraft("")`.
4. Efter klick: antal ökar, den nya varan syns i `join`-texten, fältet är tomt.
5. Ingen `push` på `items`. Ingen filter-rad. Ingen extra CSS-övning.

**Klart-check (peka i DIN kod):**
- [ ] Peka på `onChange` och säg *varför* den inte lägger till i listan  
- [ ] Peka på `onClick` och säg kedjan (läs draft → ny array → töm)  
- [ ] Peka på `[...items, text]` och säg *varför* inte `push`  
- [ ] Tom knapptryckning skapar inte en tom vara  

**Ägarskap:**
- Utan AI: skriv handlers själv.  
- Med AI: spara prompt + **en mening** om vad du ändrade. Du ska kunna förklara varje rad.

---

## Uppgift 2 — Gästlista Ateljén

**Mål:** Upprepa mönstret i ett annat tema. Träna två state + immutabilitet.

Många tänker nu: “Jag kopierar inköpslistan och byter rubrik.” Gör det — men byt namn (`guests`, `nameDraft`) så *du* äger identifierarna, och skriv kedjan högt innan du kodar.

**Brief:** Gästlista till en vernissage. Starta med minst en inbjuden i state. Fält för namn + knapp “Skriv upp”. Visa antal och namnen med `join`. Samma immutabla add. Inga klar-bockar.

**Krav:**
1. Ny komponent eller samma fil, tydligt gästtema.  
2. Två state. Kontrollerat input. Spread-ny array. Töm fält.  
3. I anteckningar: tre meningar — (a) vad ett event är, (b) varför två state, (c) varför Exam 2 bryr sig om just fält + knapp.  
4. **Simulera tom input:** tryck lägg till med tomt fält — listan ska vara oförändrad.

**Klart-check (peka i DIN kod):**
- [ ] Namn du skrivit syns i bunten efter klick  
- [ ] `value` och `onChange` sitter på samma fält  
- [ ] Anteckningarnas tre meningar är *dina* ord  
- [ ] Ingen `push`, ingen radera-knapp  

**Ägarskap:** Samma regel som uppgift 1. Om AI slänger in `.map().filter().delete` — stryk det som inte hör hit.

---

## Uppgift 3 — Stretch (valfritt)

Blockera dubbletter: om namnet redan finns i listan, lägg inte till igen (jämför strängar). Fortfarande ny array när du *väl* lägger till. Ingen CSS.

**Klart-check:** Kan du peka på `if` som stoppar tomt *och* (om du gjorde stretch) dubblett, och säga varför det inte är “React-magi”?

---

## När du kört fast

1. Lever fältet sitt liv? Saknas `value` + `onChange`.  
2. Klick tyst? Saknas `onClick` eller `setItems`.  
3. Kör metoden högt: onChange → onClick → spread → töm.  
4. Jämför med [01-teoriguide](./01-teoriguide.md).  
5. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
