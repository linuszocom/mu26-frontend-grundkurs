# 03 — Övningar

**Omfång det här paketet:** `.map()` för att rendera listan, `key` på list-syskon, `.filter()` i en avgränsad övning. Ingen full ta-bort-knapp per rad. Ingen markera-klar. Ingen CSS-layout i React. Du ska redan kunna lägga till (fält + knapp) så listan kan växa.

AI får hjälpa dig skriva. Du måste kunna **peka och förklara** varje rad du behåller.

---

## Uppgift 1 — Filmhyllan (stämpla varje kuvert)

**Mål:** Visa varje titel som egen rad med `.map()` och `key`.

**Problem först:** State har (eller får) fler filmer än tre. UI visar bara `films[0]`–`films[2]` eller en `join`-mening. Extra titlar syns inte som poster. Det är läget du ska ta dig ur.

```jsx
const [films, setFilms] = useState([
  "Fönster mot gården",
  "Källarvärme",
  "Sista bussen",
]);
```

**Krav:**
1. Vite igång. Tema film / podd / bakelser. Inga klar-bockar, ingen ta-bort-knapp.
2. Behåll lägg-till från förra paketet (fält + knapp, ny array) så du kan få fler än tre.
3. I JSX: `films.map((film) => …)` som returnerar en `<li>` (eller liten rad-komponent) **per** titel.
4. Varje barn har `key`. Unika strängar: `key={film}` duger som övning. Inga tomma keys.
5. Ta bort hårdkodade slots / `join` som *enda* visning.

**Klart-check (peka i DIN kod):**
- [ ] Fjärde tillagda titeln blir en egen rad utan att du skriver en ny `<li>` i filen  
- [ ] Peka på `.map(` och säg *varför* den returnerar JSX, inte `forEach`  
- [ ] Peka på `key` och säg *varför* den sitter där (streckkod, inte synlig text)  
- [ ] Ingen radera-knapp i den här uppgiften  

**Ägarskap:**
- Utan AI: skriv map-callback själv.  
- Med AI: spara prompt + **en mening** om vad du ändrade. Du ska kunna förklara varje rad.

---

## Uppgift 2 — Anmälningslista (silen)

**Mål:** Öva `.filter()` — ny array enligt villkor. Förberedelse för ta bort, utan ta-bort-UI.

Många tänker nu: “Filter = knappen Radera.” Nej. Filter = sil. Du kan visa resultatet utan en knapp per rad.

**Brief:** Namn till en workshop (minst fyra strängar i state, t.ex. `["Kim", "Alex", "Sam", "Rio"]`).  

**Krav:**
1. Räkna ut `const utanAlex = names.filter((n) => n !== "Alex")` (eller annat namn som *finns* i listan). Original-arrayen ska fortfarande kunna visas.  
2. Rendera **två** listor med `.map()`: “Alla anmälda” och “Utan [namn]”. Båda med `key`.  
3. Ingen `splice`. Ingen knapp “Ta bort” per rad.  
4. I anteckningar: tre meningar — (a) vad map gör, (b) vad filter gör, (c) varför båda ger ny array (koppla till state-mönstret du redan använder vid add).

**Klart-check (peka i DIN kod):**
- [ ] Peka på `.filter(` och säg villkoret högt  
- [ ] Originalistan syns fortfarande (silen tömde inte state i smyg)  
- [ ] Anteckningarna är *dina* ord  
- [ ] Ingen klar-checkbox, ingen CSS-övning  

**Ägarskap:** Samma regel som uppgift 1. Om AI bygger delete-knappar: ta bort dem. Sil + två visningar räcker.

---

## Uppgift 3 — Stretch (valfritt)

Byt strängar mot objekt `{ id, title }` i filmhyllan. `key={film.id}`. Lägg till sätter nytt `id` (t.ex. `crypto.randomUUID()` om miljön har det, eller `Date.now()`). Fortfarande ingen ta-bort-UI.

**Klart-check:** Kan du säga högt varför `id` är stabilare än index när du lägger till i mitten av kvällen?

---

## När du kört fast

1. Tom lista på skärmen: returnerar callbacken JSX? Parenteser kring `(film) => ( <li>…</li> )`.  
2. Varning om key: saknas eller dubbletter.  
3. Kör metoden högt: state → map → key. Filter = annan maskin.  
4. Jämför med [01-teoriguide](./01-teoriguide.md).  
5. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
