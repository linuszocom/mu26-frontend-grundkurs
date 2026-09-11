# 04 — AI-träning: props & ägarskap

AI kan spotta ur sig JSX som *ser* ut som tre kort. Ofta saknas följesedeln — eller så smyger state och festival in. Här tränar du: **se svag skylt, skriv om, peka**.

Det är inte magi. Det är kloss + skylt + sedel.

---

## Scenario — problem först

Du ber AI: *“Gör React-komponenter som visar en lista.”*  
Du får tillbaka något i stil med:

```jsx
import { useState } from "react";

export default function FestivalHero() {
  const [items, setItems] = useState(["Artist 1", "Artist 2"]);
  return (
    <div class="hero">
      <div>Artist 1</div>
      <div>Artist 2</div>
      <button onClick={() => setItems([...items, "Ny"])}>Add</button>
    </div>
  );
}
```

Det *kan* rendera. Det är svagt mot det här paketet:

- `useState` + Add = inte idag.  
- Festival/hero = fel tema (och eventsidan är ett annat projekt).  
- `class=` i JSX.  
- Ingen återanvänd kloss med props — två hårdkodade `div`.  
- `div` överallt utan att du kan säga varför.

**Vad du tränar:** Feedback + kort *du* äger.  
**Varför:** Props ska synas: förälder skriver, barn läser.  
**Vad det INTE är:** “Den har useState, alltså är den Exam 2 redan.” Exam 2 kommer senare.

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en prompt om *statiska* växt- eller receptkort med props, utan state. Spara prompten. Eller granska bara snutten.

### Steg 2 — Granska (checklist)
- [ ] `useState` / onClick som ändrar lista?  
- [ ] Festival / eventsida / Hero från Exam 1?  
- [ ] `class` vs `className`?  
- [ ] Finns props — eller bara hårdkodad text i en jättefil?  
- [ ] Kan du peka: var sedeln skrivs, var den läses?

Skriv **minst tre** rader:  
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Uppdatera **din** kod från [03](./03-ovningar.md) så den bara använder kloss + props. Ingen state. Spara en kort `PROPS.md` med tre FEEDBACK-rader (valfritt i anteckningar istället).

### Steg 4 — Reflektion (3 meningar)
1. Vad var svagt i AI-JSX?  
2. Vad ändrade du?  
3. Varför väntar knappen “lägg till” till nästa paket?

---

## Klart-check (peka i DIN kod)

- [ ] Tre FEEDBACK-rader  
- [ ] Peka på en prop-kedja (App → barn)  
- [ ] Peka på något du *strök* (state, festival, `class=`)  
- [ ] Reflektion klar  

---

## Facit-riktning (titta efter du granskat själv)

- `FEEDBACK: useState + Add → stryk; statiska props.`  
- `FEEDBACK: FestivalHero → Vaxtkort/Receptkort.`  
- `FEEDBACK: class= → className.`  
- `FEEDBACK: två hårdkodade div → en kloss, två följesedlar.`

**Målsvar (säg högt / skriv i README) — ägarskap:**  
*“Jag tar emot AI-JSX som utkast, stryker state och hårdkod, och behåller kloss plus följesedel jag kan peka på.”*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
