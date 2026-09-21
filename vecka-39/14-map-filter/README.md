# 14 — map & filter

> **📖 Hur du använder materialet:** Detta GitHub-repo fungerar som din digitala kursbok. Du behöver inte klona något för att läsa — klicka på länkarna i webbläsaren.

**Den här mappen täcker:** `.map()`, `key` och `.filter()`, **fredag 25 september**.  
Pass i samma kalendervecka utan filer här får en rad i körschemat.

Förutsättning: lista i state + lägg till från [12-usestate](../12-usestate/) och [13-events-lagg-till](../13-events-lagg-till/). Ingen full ta-bort-UI (det kommer i [15-todo-klar-ta-bort](../vecka-40/15-todo-klar-ta-bort/)). Ingen CSS-layout i React.

---

## 🗺️ Veckans körschema

| Dag / Tillfälle | Före passet (Förberedelse) | Live i Teams | Efter passet (Eget arbete) |
| :--- | :--- | :--- | :--- |
| **Mån 21/9 — useState** | Skumma [01 — Teoriguide](../12-usestate/01-teoriguide.md) ~15 min. Ha Vite-projektet öppet (`npm run dev`). | State + lista | [12-usestate](../12-usestate/) |
| **Ons 23/9 — events** | Ha listan i state. Skumma [01 — Teoriguide](../13-events-lagg-till/01-teoriguide.md) ~15 min. | Input + knapp, lägg till | [13-events-lagg-till](../13-events-lagg-till/) |
| **Fre 25/9 — map/filter** | Ha tillägg. Skumma [01 — Teoriguide](../14-map-filter/01-teoriguide.md) ~15 min. | Rendera med map; öva filter | [14-map-filter](../14-map-filter/) |

**Den här mappen är fredagen.** Efter passet: spåren nedan (~4–6 h).

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
- [ ] **Stretch i övningarna:** objekt med `id` + `key={film.id}` i [03 — Övningar](./03-ovningar.md)
- [ ] **README-träning:** tre meningar: map vs filter, varför `key`, varför ny array (inte `splice`)
- [ ] **Dokumentera:** i anteckningar: “Listan växer i state — **map** stämplar en rad per sak. **filter** silar fram en *ny* lista. Det är array-metoder, inte trolleri.”

---

## 🗣️ Målsvar att kunna utantill inför examinationen

När mappen är klar ska du kunna återge dessa med egna ord:

> **map:** ".map() går igenom varje element och returnerar en ny array — i React ofta en JSX-rad per sak i listan."

> **filter:** ".filter() skapar en ny array med bara de element som klarar ett villkor."

> **key:** "key är ett unikt id per list-syskon så React kan matcha rätt rad när listan ändras."

> **Metoden:** "Data finns i state. map till JSX, key på varje barn. Behöver du en lista utan vissa → filter (ny array), inte splice på state."

---

## 📝 Examination

**Examination 2 (ToDo)** ska visa alla skapade uppgifter dynamiskt — det är `.map()` på listan i state. `.filter()` övar du nu; knappar för ta bort och markera klar kommer i nästa veckas paket. Ingen ny Exam 2-genomgång här.

## 🏁 Nästa steg

När du är klar här: [15-todo-klar-ta-bort](../vecka-40/15-todo-klar-ta-bort/) — markera klar och ta bort (mån 28/9).
