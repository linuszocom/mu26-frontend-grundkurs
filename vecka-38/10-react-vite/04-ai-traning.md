# 04 — AI-träning: Vite-setup & ägarskap

AI kan klistra in “skapa React-app” på sekunder. Ofta följer **extra grejer** du inte kan försvara. Här tränar du: **se spill, stryk, peka i din kartong**.

Det är inte magi. Det är pincett vs mall + rätt create.

---

## Scenario — problem först

Du ber AI: *“Skapa ett React-projekt och en komponent.”*  
Du får tillbaka något i stil med:

```text
npx create-react-app my-app --template typescript
cd my-app
npm install redux react-router-dom
```

```jsx
import { useState } from "react";

function App() {
  const [todos, setTodos] = useState([]);
  return <input onChange={() => {}} placeholder="New task" />;
}
```

Plus: “Importera från Figma” / `document.getElementById("root").innerHTML = ...` i samma fil.

Det *kan* råka starta. Det är svagt mot det här paketet:

- CRA + TypeScript + Redux + router = andra kartonger.  
- `useState` + todo-input = nästa kapitel, inte idag.  
- Figma finns inte i kursen.  
- Pincett (`getElementById`) mitt i React-klossen blandar två sätt.

**Vad du tränar:** Feedback + ett projekt *du* äger.  
**Varför:** Du ska veta vad Vite är och vad en kloss är — utan crud.  
**Vad det INTE är:** “Ju fler paket desto mer proffsigt.”

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en prompt där du ber om Vite + React (JS) och en *statisk* namnskylt. Spara prompten. Eller granska bara snutten ovan.

### Steg 2 — Granska (checklist)
- [ ] `create vite` + `template react` — eller CRA/TS/andra mallar?  
- [ ] Extra bibliotek (router, Redux, UI-kit)?  
- [ ] `useState` / todo / events?  
- [ ] Figma eller designverktyg?  
- [ ] DOM-pincett (`querySelector`, `innerHTML`) i komponenten?  
- [ ] Kan du förklara varje steg muntligt?

Skriv **minst tre** rader:  
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Utgå från **ditt** projekt i [03](./03-ovningar.md). Behåll statisk `Namnskylt`. Inga extra paket. Skriv kommandona du *faktiskt* körde i `SETUP.md` i mappen (inga tokens).

### Steg 4 — Reflektion (3 meningar)
1. Vad var spill i AI-förslaget?  
2. Vad strök du?  
3. Varför väntar `useState` och ToDo (Exam 2 kommer senare)?

---

## Klart-check (peka i DITT projekt)

- [ ] Tre FEEDBACK-rader  
- [ ] Peka på `create`-kommandot du körde  
- [ ] Peka på något du *inte* installerade  
- [ ] Reflektion klar  

---

## Facit-riktning (titta efter du granskat själv)

- `FEEDBACK: create-react-app + TS → Vite med --template react.`  
- `FEEDBACK: redux/router → stryk; inte i paketet.`  
- `FEEDBACK: useState/todos → statisk namnskylt.`  
- `FEEDBACK: getElementById i App → låt React visa klossen.`

**Målsvar (säg högt / skriv i README) — ägarskap:**  
*“Jag tar emot AI-setup som utkast, stryker extra paket och state, och behåller Vite-kartongen plus klossen jag kan peka på.”*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
