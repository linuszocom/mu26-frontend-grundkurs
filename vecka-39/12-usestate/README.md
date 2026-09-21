# 12 — useState & re-render

> **📖 Hur du använder materialet:** Detta GitHub-repo fungerar som din digitala kursbok. Du behöver inte klona något för att läsa — klicka på länkarna i webbläsaren.

**Den här mappen täcker:** `useState`, re-render och lista i state, **måndag 21 september**.  
Pass i samma kalendervecka utan filer här får en rad i körschemat.

Ingen input + “lägg till” i det här paketet — det kommer i [13-events-lagg-till](../13-events-lagg-till/). Ingen `.map()`-djupdykning, ingen filter/ta bort.

---

## 🗺️ Veckans körschema

| Dag / Tillfälle | Före passet (Förberedelse) | Live i Teams | Efter passet (Eget arbete) |
| :--- | :--- | :--- | :--- |
| **Mån 21/9 — useState** | Skumma [01 — Teoriguide](../12-usestate/01-teoriguide.md) ~15 min. Ha Vite-projektet öppet (`npm run dev`). | State + lista | [12-usestate](../12-usestate/) |
| **Ons 23/9 — events** | Ha listan i state. Skumma [01 — Teoriguide](../13-events-lagg-till/01-teoriguide.md) ~15 min. | Input + knapp, lägg till | [13-events-lagg-till](../13-events-lagg-till/) |
| **Fre 25/9 — map/filter** | Ha tillägg. Skumma [01 — Teoriguide](../14-map-filter/01-teoriguide.md) ~15 min. | Rendera med map; öva filter | [14-map-filter](../14-map-filter/) |

**Den här mappen är måndagen.** Efter passet: spåren nedan (~4–6 h).

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
- [ ] **Stretch i övningarna:** andra `set…`-uppdatering i [03 — Övningar](./03-ovningar.md)
- [ ] **README-träning:** tre meningar: vad state är, vad re-render är (och inte är), varför listan ska läsas från state
- [ ] **Dokumentera:** i anteckningar: “Jag klickade — skärmen följde efter eftersom jag anropade **set-funktionen** med en **ny** array, inte för att jag redigerade DOM.”

---

## 🗣️ Målsvar att kunna utantill inför examinationen

När mappen är klar ska du kunna återge dessa med egna ord:

> **State:** "State är data React håller i komponenten. När du ändrar den med set-funktionen renderas UI om så skärmen matchar den nya datan."

> **Re-render:** "Re-render betyder att React kör JSX igen efter ny state. Det är inte att du skriver om DOM för hand."

> **Listan i state:** "Det som syns i listan ska läsas från state — inte från hårdkodade JSX-rader du glömmer uppdatera."

> **Metoden:** "Vad ska skärmen följa? Lägg det i useState. Läs värdet, skriv bara via set-funktionen, skicka in ett nytt värde (t.ex. en ny array)."

---

## 📝 Examination

**Examination 2 (ToDo)** ska visa listan dynamiskt. Grunden är den här: uppgifterna bor i state, UI läser därifrån. Lägga till via fält, `.map()`, markera klar och ta bort kommer i senare mappar — bygg inte det här.

## 🏁 Nästa steg

När du är klar här: [13-events-lagg-till](../13-events-lagg-till/) — input, knapp och lägg till (ons 23/9).
