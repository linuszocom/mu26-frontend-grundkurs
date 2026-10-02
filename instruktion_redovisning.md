# Muntlig redovisning (video via Teams)

Spela in en kort skärminspelning (ca **3–5 minuter**) där du visar din app och förklarar din kod.

---

## 1. Så spelar du in i Teams

1. Gå till fliken **Kalender** i Teams → **Möt nu** (Meet now) → **Starta möte**.
2. Välj mikrofon och anslut. Kamera på ansiktet är valfritt.
3. Klicka **Dela** och dela hela din skärm (eller ha webbläsaren och VS Code synliga bredvid varandra).
4. Klicka på **Mer** (...) → **Spela in och transkribera** → **Starta inspelning**.
5. Genomför din presentation (se punkt 2 & 3 nedan). Avsluta sedan mötet för att stoppa inspelningen.

---

## 2. Upplägget i videon

1. **Snabb demo i webbläsaren (ca 30–60 sekunder):**
   * Visa snabbt att appen fungerar: lägg till en uppgift, markera den som klar och ta bort en uppgift.
2. **Källkoden i VS Code (resten av tiden):**
   * Gå över till VS Code och välj ut **2–3 funktioner/händelser** att förklara med muspekaren pekande på koden (t.ex. hur en uppgift läggs till, hur status togglas eller hur en uppgift raderas).

---

## 3. Vad du ska förklara i VS Code

### För godkänt (G) — vad koden gör
- Peka på dina valda funktioner och beskriv dataflödet med egna ord: vilken knapp/händelse startar koden, vad som skickas in och hur state uppdateras.
- Du kan peka ut grundläggande delar som `useState`, din array och var `.map()` ritar ut listan.

### För väl godkänt (VG) — varför och bakom kulisserna
- Du förklarar tanken bakom hur koden är uppbyggd och vad som sker under huven:
  - Hur fungerar Reacts reaktivitet (varför ritas sidan om vid state-ändring)?
  - Varför skapar du en ny kopia av arrayen (immutabilitet med spread/filter/map) istället för att ändra direkt med `.push()` eller `.splice()`?
  - Om du har delat upp appen i egna komponenter: hur flödar datan och funktionerna via `props`?

---

## 4. Lämna in länken

Inspelningen sparas automatiskt i Teams/OneDrive.

1. Gå till mötets chatt, eller till OneDrive-mappen **Inspelningar** (Recordings).
2. Klicka **...** vid videon → **Kopiera länk**.
3. **Kontrollera behörigheten:** Länken måste kunna öppnas av läraren (välj t.ex. **Personer inom organisationen** eller kontrollera att länken inte är låst som privat).
4. Klistra in länken längst upp i din `README.md` i ditt repo.

⬅️ [Tillbaka till uppgiftsbeskrivningen](ToDoAppen.md)
