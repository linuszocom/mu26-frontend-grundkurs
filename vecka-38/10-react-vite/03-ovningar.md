# 03 — Övningar

**Omfång det här paketet:** Skapa ett Vite + React-projekt, öppna det i VS Code, en **statisk** komponent (namnskylt). Ingen `useState`. Ingen lista att lägga till/ta bort. Ingen Figma. Inte eventsidans HTML. **Examination 2** kommer senare.

AI får hjälpa till med kommandon. Du måste kunna **peka** `package.json`, `main.jsx` och `App.jsx`.

---

## Uppgift 1 — Kartongen på disk

**Mål:** Projektet finns, servern går, mappen är öppen i VS Code.

**Problem först:** En ensam `index.html` från eventsidan är *inte* den här kartongen. Utan create saknar du `package.json` och `src/`.

**Krav:**
1. Kolla att Node finns: `node -v` och `npm -v` i terminalen. Saknas Node: installera **LTS** från nodejs.org, öppna en **ny** terminal, kolla igen.  
2. Skapa projektet (JavaScript + React, inte TypeScript):

```bash
npm create vite@latest namnskylt -- --template react
cd namnskylt
npm install
```

3. **File → Open Folder** på mappen `namnskylt` (där `package.json` ligger).  
4. `npm run dev` — öppna URL:en i webbläsaren (ofta `http://localhost:5173`).  
5. I anteckningar: tre rader — vad `create` gav dig, vad `install` gjorde, vad `dev` gör.

**Klart-check (peka i DITT projekt):**
- [ ] `package.json` syns i VS Code  
- [ ] Peka på `src/main.jsx` och säg vad den är till för (tända appen)  
- [ ] Peka på `src/App.jsx` och säg vad den är till för (klossen du redigerar)  
- [ ] Webbläsaren visar Vite/React-startsidan (den får vara ful)

**Ägarskap:** Om AI ger extra flaggor (`--ts`, Redux, router): stryk. Template `react` räcker.

---

## Uppgift 2 — Statisk namnskylt (LEGO-kloss)

**Mål:** En komponent som visar namn + en rad text. Ingen klick-logik.

**Brief:** Ersätt välkomstskräpet i `App` med en namnskylt — ditt namn (eller påhittat), en rollrad t.ex. “Frontend-student”. Inte festival. Inte eventsidans hero.

Exempel på *riktning* (skriv om till dina ord):

```jsx
function Namnskylt() {
  return (
    <article>
      <h1>Kim Berg</h1>
      <p>Frontend-student</p>
    </article>
  );
}

function App() {
  return (
    <main>
      <Namnskylt />
    </main>
  );
}

export default App;
```

**Krav:**
1. En funktion med **stor bokstav** (`Namnskylt`).  
2. Den returnerar synlig markup.  
3. `App` sätter in klossen.  
4. Spara — se uppdatering i webbläsaren.  
5. En mening högt: vad en komponent är till för.

**Klart-check (peka i DIN kod):**
- [ ] Peka på klossen och på stället den *används* — två ställen  
- [ ] Ingen `useState`, ingen `onClick` som ändrar data  
- [ ] Du kan säga målsvaret för komponent utan att läsa innantill  

**Ägarskap:** AI ok som bollplank för “var ska export sitta?”. Du ska kunna peka utan att gömma dig bakom tutorial-CSS.

---

## Uppgift 3 — Stretch (valfritt)

En andra statisk kloss, t.ex. `Oppettider` med tre rader text (mån–fre). Fortfarande ingen state. En mening: varför två klossar slår en enda lång `App`.

---

## När du kört fast

1. Fel mapp → Open Folder där `package.json` finns.  
2. `command not found: npm` → Node LTS, ny terminal.  
3. Port upptagen → läs terminalraden, använd den URL Vite skriver ut.  
4. Jämför med [01-teoriguide](./01-teoriguide.md).  
5. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
