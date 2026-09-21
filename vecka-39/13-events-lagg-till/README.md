# 13 — Events & lägg till

> **📖 Hur du använder materialet:** Detta GitHub-repo fungerar som din digitala kursbok. Du behöver inte klona något för att läsa — klicka på länkarna i webbläsaren.

**Den här mappen täcker:** `onChange`, `onClick` och immutabel lägg-till, **onsdag 23 september**.  
Pass i samma kalendervecka utan filer här får en rad i körschemat.

Förutsättning: lista i `useState` från [12-usestate](../12-usestate/). Ingen markera-klar, ingen ta-bort-UI. Ingen CSS-layout i React. `.map()` som huvudnummer kommer i [14-map-filter](../14-map-filter/).

---

## 🗺️ Veckans körschema

| Dag / Tillfälle | Före passet (Förberedelse) | Live i Teams | Efter passet (Eget arbete) |
| :--- | :--- | :--- | :--- |
| **Mån 21/9 — useState** | Skumma [01 — Teoriguide](../12-usestate/01-teoriguide.md) ~15 min. Ha Vite-projektet öppet (`npm run dev`). | State + lista | [12-usestate](../12-usestate/) |
| **Ons 23/9 — events** | Ha listan i state. Skumma [01 — Teoriguide](../13-events-lagg-till/01-teoriguide.md) ~15 min. | Input + knapp, lägg till | [13-events-lagg-till](../13-events-lagg-till/) |
| **Fre 25/9 — map/filter** | Ha tillägg. Skumma [01 — Teoriguide](../14-map-filter/01-teoriguide.md) ~15 min. | Rendera med map; öva filter | [14-map-filter](../14-map-filter/) |

**Den här mappen är onsdagen.** Efter passet: spåren nedan (~4–6 h).

---

## 🎯 Välj din väg i materialet

### 🟢 1. Du var med på live-passet (Repetition & Praktik)
*Om du hängde med på skärmen och förstod koncepten:*
1. [ ] **Bygg med fingrarna:** [03 — Övningar](./03-ovningar.md)
2. [ ] **Träna kritiskt tänkande:** [04 — AI-träning](./04-ai-traning.md)
3. [ ] **Kontrollera dina målsvar:** [05 — Självtest](./05-sjalvtest.md) utan facit först  
*( [01 — Teoriguide](./01-teoriguide.md) som uppslagsverk bara om du kör fast.)*

---

### 🟡 2. Du missade passet eller börjar från noll (Ta ikapp-spåret)
*Om du var sjuk, hade förhinder eller känner att grunderna inte sitter:*
1. [ ] **Förstå koncepten:** [01 — Teoriguide](./01-teoriguide.md) från start till mål
2. [ ] **Få överblick:** [02 — Visuellt](./02-visuell.md)
3. [ ] **Koda själv:** [03 — Övningar](./03-ovningar.md)
4. [ ] **Granska & anpassa:** [04 — AI-träning](./04-ai-traning.md)
5. [ ] **Slutkontroll:** [05 — Självtest](./05-sjalvtest.md)

---

### 🟣 3. Du siktar på VG / vill fördjupa dig (Stretch)
*Om du blev klar snabbt — frivilligt, inom kursplanen:*
- [ ] **Stretch i övningarna:** tom-sträng-skydd + trim i [03 — Övningar](./03-ovningar.md)
- [ ] **README-träning:** tre meningar: vad ett event gör, varför ny array (inte `push`), varför två state (fält vs lista)
- [ ] **Dokumentera:** i anteckningar: “Jag klickade Lägg till — då kördes **min** funktion, som läste fältet och skickade en **ny** array till set-funktionen.”

---

## 🗣️ Målsvar att kunna utantill inför examinationen

När mappen är klar ska du kunna återge dessa med egna ord:

> **Event:** "onChange och onClick kopplar användarens handling till din funktion. Där läser du värdet och uppdaterar state — då re-renderar UI."

> **Immutabel uppdatering:** "Du skapar en ny array med det nya innehållet och skickar den till set-funktionen. Du muterar inte den gamla state-arrayen med push."

> **Två state:** "Ett state för texten i fältet just nu, ett för den sparade listan. Vid Lägg till flyttar du text från fältet till listan och tömmer fältet."

> **Metoden:** "onChange sparar det som står i fältet. onClick: om text finns → ny array via spread → töm fältet."

---

## 📝 Examination

**Examination 2 (ToDo)** kräver att användaren skriver i ett textfält och lägger till med en knapp. Det här paketet är just det flödet. Markera klar och ta bort kommer senare. Bygg inte CSS-layout här.

## 🏁 Nästa steg

När du är klar här: [14-map-filter](../14-map-filter/) — rendera med `.map()`, öva `.filter()` (fre 25/9).
