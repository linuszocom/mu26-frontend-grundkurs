# 03 — Övningar

**Omfång det här paketet:** `let` / `const`, sträng / number / boolean, namngiven `function`, `console.log`, `if` / `else`, `===`, array (`[]`, index, `.length`), objekt (`{}`, punktnotation), `for...of`. Arrow bara som valfri stretch. Allt i **konsolen**. Ingen React. Ingen DOM-manipulation (`querySelector`, `innerHTML`, klick). Ingen Vite. Inga array-metoder (`.map` / `.filter`). Ingen ToDo-app — den kommer senare.

AI får föreslå rader. Du måste kunna **peka och förklara** varje burk, varje anrop och varje dörr.

**Var du kör:** Webbläsarens DevTools → **Console**, eller en `script.js` som du öppnar via en minimal HTML bara för att *ladda* filen. Resultatet ska synas i konsolen.

---

## Uppgift 1 — Kassakvitto i konsolen

**Mål:** Burkar + ett receptkort som räknar en rad. Boolean som **styr** — inte bara loggas.

**Problem först:** Tre bakverk kostar 18 kr styck. Utan variabler skriver du `18` på tre ställen. Priset höjs — du missar en rad. `harRabatt` ligger i facket men koden räknar likadant om du bara *loggar* den.

**Krav:**
1. `const` för butiksnamn (sträng) och styckpris (number).  
2. `let` för löpande `summa` (börjar på `0`).  
3. En funktion `radSumma(pris, antal)` som `return`erar `pris * antal`.  
4. Lägg till minst två rader (t.ex. 2 bullar, 1 kaffe) genom att *anropa* funktionen och lägga på `summa`.  
5. En boolean `harRabatt` (`true` eller `false`). **Använd den i ett villkor:** om `harRabatt === true` sänk `summa` (t.ex. `summa = summa * 0.9`), annars logga att rabatt saknas.  
6. `console.log` av butiksnamn, varje rad och slutsumma efter villkoret.

**Klart-check (peka i DIN kod):**
- [ ] Peka på en `const` och säg *varför* den inte är `let`  
- [ ] Peka på `summa` och säg *varför* den är `let`  
- [ ] Peka på deklarationen och på **anropet** — två olika ställen  
- [ ] Peka på `if` och på `===` — boolean *frågas*, den bara ligger inte i facket  
- [ ] Konsolen visar tal, inte `NaN` och inte `"1818"`

**Ägarskap:** Utan AI: skriv själv. Med AI: spara prompten + en mening om vad du ändrade. Du ska kunna förklara varje rad.

---

## Uppgift 2 — Temperaturomvandling

**Mål:** Ett receptkort med parameter in och värde ut. Testa med logg.

**Brief:** `celsiusTillFahrenheit(c)` ska returnera `c * 9/5 + 32`. Anropa med minst två temperaturer (t.ex. `0` och `21`). Logga både C och F.

**Krav:**
1. Funktionen deklarerad med `function`.  
2. Minst två anrop.  
3. En `const` för en “fryspunkt” (`0`) som du skickar in — inte tre hårdkodade formler.  
4. I anteckningar: två meningar — (a) vad en funktion är, (b) varför `console.log` behövdes.

**Klart-check (peka i DIN kod):**
- [ ] `return` ger talet vidare — du räknar inte bara inuti `console.log` utan att kunna återanvända  
- [ ] Anteckningarna är *dina* ord  

**Ägarskap:** Samma regel som uppgift 1.

---

## Uppgift 3 — Hylla, rad, rundgång

**Mål:** Sammansatt data + en loop som *läser*. Ingen React. Inga `.map`.

**Brief:** Tre sysslor på en hylla. En av dem som objekt. Gå igenom hyllan.

**Krav:**
1. En array `todos` med **tre strängar**. Logga `todos[0]` och `todos.length`.  
2. Ett objekt `todo` med `text` (sträng) och `done` (boolean). Logga `todo.text` med punktnotation.  
3. En `for...of` som `console.log`:ar varje sträng i `todos`.  
4. I anteckningar: en mening om skillnaden array vs objekt, och en mening om vad `for...of` är (och att det inte är `.map`).

**Klart-check (peka i DIN kod):**
- [ ] Index `0` är första facket  
- [ ] `.length` är antal, inte sista numret  
- [ ] Ingen `.map` / `.filter` / `.push` som “lösning”

**Ägarskap:** Samma regel som uppgift 1.

---

## Uppgift 4 — Stretch (valfritt)

Skriv om `radSumma` *eller* `celsiusTillFahrenheit` som **arrow function**. Samma anrop, samma logg. En mening i anteckningar: vad som är likadant, vad som bara är kortare stavning.

**Klart-check:** Du kan peka på `=>` och säga att det inte är en ny sorts logik — och att live-kravet idag var namngiven `function`.

---

## När du kört fast

1. Titta i konsolen — röd felrad = ofta stavning, citattecken eller `const` som du försöker fylla om.  
2. Kör metoden högt: vad? data? steg? fråga (`if`)? logg?  
3. Jämför med [01-teoriguide](./01-teoriguide.md).  
4. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
