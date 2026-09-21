# 04 — AI-träning: useState & ägarskap

AI kan klistra in en lista på sekunder. Det betyder inte att *du* äger var datan bor. Här tränar du samma färdighet som Exam 2 kräver muntligt: **se vad som är svagt, ändra, förklara**.

Det är inte magi att “granska AI”. Det är samma metod som i teoriguiden — displayen, inte ficklappen.

---

## Scenario — problem först

Du ber AI: *“Gör en React-lista som kan uppdateras.”*  
Du får tillbaka något i stil med:

```jsx
import { useState } from "react";

let tracks = ["Intro", "Verse"];

function App() {
  const [count, setCount] = useState(2);

  function demo() {
    tracks.push("Outro");
    setCount(tracks.length);
  }

  return (
    <main>
      <h1>Spellista</h1>
      <p>{count} spår</p>
      <ul>
        <li>Intro</li>
        <li>Verse</li>
        <li>Outro</li>
      </ul>
      <button type="button" onClick={demo}>
        Uppdatera
      </button>
    </main>
  );
}
```

Det *kan* råka se ut att “något händer”. Det är ändå svagt mot det här paketets krav:

- Listan bor i `let tracks` — **inte** i `useState`.  
- `push` muterar samma array.  
- `<li>`-raderna är **hårdkodade** — de läser inte `tracks[0]` / state.  
- `count` är en parallell siffra som kan ljuga om listan.  
- Tredje `<li>Outro</li>` fanns redan — “uppdateringen” är teater.

**Vad du tränar:** Feedback på AI-kod + en lista *du* äger i state.  
**Varför:** Muntligt och Exam 2 kräver att *du* kan peka: var listan bor, vad `set…` gör, vad re-render är.  
**Vad det INTE är:** “AI la in useState, alltså är listan dynamisk.”

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en egen prompt till AI (eller jobba bara mot snutten ovan utan ny AI) där du ber om en liten lista i React som skärmen kan följa. Spara prompten.

### Steg 2 — Granska (checklist)
Gå igenom svaret (AI:ns eller snutten) och kryssa:

- [ ] Bor listan i `useState` — eller i `let` / hårdkodad JSX?  
- [ ] Anropas set-funktionen med ett **nytt** värde — eller `push` på samma array?  
- [ ] Läser UI `tracks` / `items` (antal + innehåll) — eller en död siffra + limmade rader?  
- [ ] Finns textfält + lägg till / filter-ta bort du **inte** ska ha här?  
- [ ] Kan du förklara varje rad muntligt?

Skriv **minst tre** konkreta feedback-punkter i formen:  
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Skriv om till en **ren version du äger** i övningsprojektet från [03](./03-ovningar.md): array i `useState`, UI läser den, bevisknapp med ny array. Ingen input-lägg-till. Spara en kort `STATE-FLÖDE.md` i mappen (tre rader: var listan bor, vad klick gör, vad re-render är).

### Steg 4 — Reflektion (3 meningar)
Skriv i anteckningar eller samma `STATE-FLÖDE.md`:

1. Vad var fel eller svagt i AI-förslaget (eller snutten)?  
2. Vad ändrade du?  
3. Varför är det viktigt inför Exam 2 (dynamisk lista / ägarskap)?

---

## Klart-check (peka i DIN kod)

- [ ] Tre FEEDBACK-rader sparade  
- [ ] Peka på `useState` och säg *varför* listan ska sitta där  
- [ ] Peka på något du *tog bort* från AI — varför behövdes det inte / var det fel?  
- [ ] Reflektionens tre meningar klara  

---

## Facit-riktning (titta efter du granskat själv)

Exempel på giltig feedback (dina egna ord får skilja sig):

- `FEEDBACK: let tracks + push → lägg arrayen i useState och skicka en ny array till setTracks.`  
- `FEEDBACK: hårdkodade li → läs tracks[0] / tracks[1] (och length) från state.`  
- `FEEDBACK: separat count som kan ljuga → visa tracks.length.`  
- `FEEDBACK: Outro redan i JSX → ta bort teatern; extra raden ska komma från ny state.`

**Målsvar (säg högt / skriv i README) — ägarskap:**  
*“Jag tar emot AI-förslag som utkast, granskar rad för rad, och behåller bara det jag kan förklara.”*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
