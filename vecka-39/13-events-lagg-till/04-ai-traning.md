# 04 — AI-träning: events, push & ägarskap

AI kan spotta ur sig ett formulär på sekunder. Det betyder inte att *du* äger klicket. Här tränar du: **se vad som är svagt, ändra, förklara** — samma ägarskap som Exam 2 kräver muntligt.

Det är inte magi. Det är ringklockan + ny array.

---

## Scenario — problem först

Du ber AI: *“Hjälp mig lägga till rader i min React-lista från ett textfält.”*  
Du får tillbaka något i stil med:

```jsx
import { useState } from "react";

function App() {
  const [items, setItems] = useState(["Mjölk"]);

  function add() {
    const el = document.querySelector("input");
    items.push(el.value);
    setItems(items);
  }

  return (
    <main>
      <input />
      <button onClick={add}>OK</button>
      <p>{items}</p>
    </main>
  );
}
```

Det *kan* råka visa något. Det är ändå svagt mot det här paketets krav:

- **`push`** muterar samma array; `setItems(items)` skickar ofta **samma referens**.  
- **`document.querySelector`** går bakvägen — React ska äga fältet via state (`draft` + `value`/`onChange`).  
- Inget `trim`, ingen tom-check.  
- Inget `type="button"`. Inget tömning av fältet.  
- `{items}` som objekt i JSX blir sällan en läsbar lista.

**Vad du tränar:** Feedback + ett add-flöde *du* äger.  
**Varför:** Muntligt kräver att du pekar: onChange, onClick, spread.  
**Vad det INTE är:** “AI använde setItems, alltså är det immutabelt.”

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en egen prompt (eller jobba mot snutten) där du ber om lägg-till från fält i React. Spara prompten.

### Steg 2 — Granska (checklist)
Kryssa mot koden du fick:

- [ ] Finns `draft`-state + `value`/`onChange` — eller querySelector/DOM?  
- [ ] Ny array (`[...items, text]`) — eller `push`?  
- [ ] Töm fältet efteråt?  
- [ ] Finns ta-bort, filter, CSS-layout du **inte** behöver här?  
- [ ] Kan du förklara varje rad muntligt?

Skriv **minst tre** konkreta feedback-punkter i formen:  
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Skriv om till en **ren kedja du äger** i inköps- eller gästlistan från [03](./03-ovningar.md). Spara handlers + en kort `ADD-KEDJA.md` (onChange / onClick / spread — en rad var).

### Steg 4 — Reflektion (3 meningar)
Skriv i anteckningar eller samma fil:

1. Vad var fel eller svagt i AI-förslaget (eller snutten)?  
2. Vad ändrade du?  
3. Varför är `push` vs ny array viktigt inför Exam 2 / muntligt?

---

## Klart-check (peka i DIN kod)

- [ ] Tre FEEDBACK-rader sparade  
- [ ] Peka på spread-raden och säg *varför* den duger  
- [ ] Peka på något du *tog bort* från AI — varför behövdes det inte?  
- [ ] Reflektionens tre meningar klara  

---

## Facit-riktning (titta efter du granskat själv)

Exempel på giltig feedback (dina egna ord får skilja sig):

- `FEEDBACK: items.push + setItems(items) → setItems([...items, text]) så arrayen är ny.`  
- `FEEDBACK: querySelector → draft-state, value och onChange.`  
- `FEEDBACK: fältet töms inte → setDraft("") efter lyckat add.`  
- `FEEDBACK: ingen trim/tom-check → hoppa över tomma rader.`

**Målsvar (säg högt / skriv i README) — ägarskap:**  
*“Jag tar emot AI-förslag som utkast, granskar rad för rad, och behåller bara det jag kan förklara.”*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
