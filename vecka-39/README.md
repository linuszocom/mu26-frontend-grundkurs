# Vecka 39 — State, events & dynamiska listor

> **📖 Hur du använder detta material:** Detta GitHub-repo är din digitala kursbok. Du behöver inte ladda ner eller klona repot för att läsa – klicka bara på länkarna i webbläsaren. Följ körschemat dag för dag för att hålla studietakten.

**Förkunskap:** Vecka 38 (JS-syntax, Vite/React, JSX & props). Ha ditt Vite React-projekt öppet och `npm run dev` igång.

---

## 🗺️ Veckans Roadmap (Dag för dag)

### 🔵 Måndag 21/9 — useState & re-render
Mapp: [12-usestate](./12-usestate/)

* **Före kl 13:00 (Förberedelse):** Skumma [01 — Teoriguide](./12-usestate/01-teoriguide.md) (max ~15 min). Ha Vite-projektet öppet (`npm run dev`).
* **Kl 13:00–16:00 (Live i Teams):** `useState`, re-render och lista i state. Ingen input + “lägg till” ännu.
* **Efter lektionen (Välj din väg):**

> 🟢 **Du var med på passet:** Gå direkt på [03 — Övningar](./12-usestate/03-ovningar.md) och stäm av med [05 — Självtest](./12-usestate/05-sjalvtest.md). [01 — Teoriguide](./12-usestate/01-teoriguide.md) är uppslagsverk om du kör fast.

> 🟡 **Om du missade passet:** Gör hela kedjan **01 (Teori) → 02 (Visuellt) → 03 (Övningar) → 04 (AI) → 05 (Självtest)** i [12-usestate](./12-usestate/): [01](./12-usestate/01-teoriguide.md) → [02](./12-usestate/02-visuell.md) → [03](./12-usestate/03-ovningar.md) → [04](./12-usestate/04-ai-traning.md) → [05](./12-usestate/05-sjalvtest.md).

---

### ⚪ Tisdag 22/9 — Eget arbete & Fördjupning
*Helstudiedag på egen hand:*
* [ ] **Repetition / Ta ikapp:** Slutför övningarna i [12-usestate/03-ovningar.md](./12-usestate/03-ovningar.md) om du inte hann klart i måndags.
* [ ] **AI-träning:** Träna på att granska AI-state i [12-usestate/04-ai-traning.md](./12-usestate/04-ai-traning.md).
* [ ] **Förbered inför onsdag:** Ha listan i state. Skumma events i [13-events-lagg-till/01-teoriguide.md](./13-events-lagg-till/01-teoriguide.md) (max ~10 min).

---

### 🔵 Onsdag 23/9 — Events & lägg till
Mapp: [13-events-lagg-till](./13-events-lagg-till/)

* **Före kl 13:00 (Förberedelse):** Ha listan i `useState` från måndagen. Skumma [01 — Teoriguide](./13-events-lagg-till/01-teoriguide.md) (max ~15 min).
* **Kl 13:00–16:00 (Live i Teams):** `onChange`, `onClick` och immutabel lägg-till (input + knapp).
* **Efter lektionen (Välj din väg):**

> 🟢 **Du var med på passet:** Gör [03 — Övningar](./13-events-lagg-till/03-ovningar.md) och testa dig själv i [05 — Självtest](./13-events-lagg-till/05-sjalvtest.md). [01 — Teoriguide](./13-events-lagg-till/01-teoriguide.md) är uppslagsverk om du kör fast.

> 🟡 **Om du missade passet:** Gör hela kedjan **01 (Teori) → 02 (Visuellt) → 03 (Övningar) → 04 (AI) → 05 (Självtest)** i [13-events-lagg-till](./13-events-lagg-till/): [01](./13-events-lagg-till/01-teoriguide.md) → [02](./13-events-lagg-till/02-visuell.md) → [03](./13-events-lagg-till/03-ovningar.md) → [04](./13-events-lagg-till/04-ai-traning.md) → [05](./13-events-lagg-till/05-sjalvtest.md).

---

### ⚪ Torsdag 24/9 — Eget arbete & Fördjupning
*Helstudiedag på egen hand:*
* [ ] **Repetition / Ta ikapp:** Se till att du kan skriva i fältet och lägga till en rad i listan.
* [ ] **AI-träning:** Gör AI-övningen i [13-events-lagg-till/04-ai-traning.md](./13-events-lagg-till/04-ai-traning.md).
* [ ] **Förbered inför fredag:** Ha tillägg igång. Skumma map/filter i [14-map-filter/01-teoriguide.md](./14-map-filter/01-teoriguide.md) (max ~10 min).

---

### 🔵 Fredag 25/9 — map & filter
Mapp: [14-map-filter](./14-map-filter/)

* **Före kl 13:00 (Förberedelse):** Ha lista i state + lägg till. Skumma [01 — Teoriguide](./14-map-filter/01-teoriguide.md) (max ~15 min).
* **Kl 13:00–16:00 (Live i Teams):** Rendera listan med `.map()` och `key`; öva `.filter()`.
* **Efter lektionen / Helgens mål:**

> 🟢 **Du var med på passet:** Gör [03 — Övningar](./14-map-filter/03-ovningar.md) och kör [05 — Självtest](./14-map-filter/05-sjalvtest.md). [01 — Teoriguide](./14-map-filter/01-teoriguide.md) är uppslagsverk om du kör fast.

> 🟡 **Om du missade passet:** Gör hela kedjan **01 (Teori) → 02 (Visuellt) → 03 (Övningar) → 04 (AI) → 05 (Självtest)** i [14-map-filter](./14-map-filter/): [01](./14-map-filter/01-teoriguide.md) → [02](./14-map-filter/02-visuell.md) → [03](./14-map-filter/03-ovningar.md) → [04](./14-map-filter/04-ai-traning.md) → [05](./14-map-filter/05-sjalvtest.md).

---

## 🎯 Veckans Checklista (Klar inför nästa vecka?)

När veckan är slut ska du ha bockat av:
- [ ] Jag kan använda `useState` och förklara vad re-render betyder med egna ord
- [ ] Jag har en lista i state (inte bara hårdkodade JSX-rader)
- [ ] Jag kan lägga till via textfält + knapp (`onChange` / `onClick`) utan att mutera med `push`
- [ ] Jag kan rendera listan med `.map()` och ge varje rad en stabil `key`
- [ ] Jag kan filtrera en lista med `.filter()` (öva, inte obligatorisk ta-bort-UI än)
- [ ] Jag kan målsvaren för **state**, **event** och **map** utantill

**Nästa droppe (fre 25/9):** [Vecka 40](../vecka-40/) — markera klar, ta bort och CSS i React.
