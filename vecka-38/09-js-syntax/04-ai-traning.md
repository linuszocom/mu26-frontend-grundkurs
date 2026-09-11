# 04 — AI-träning: JS-syntax & ägarskap

AI kan spotta ur sig JavaScript på sekunder. Det betyder inte att *du* äger burkarna. Här tränar du: **se vad som är svagt, ändra, förklara**.

Det är inte magi. Det är namnlapp + receptkort + dörr + hylla + logg.

---

## Scenario A — kvitto (problem först)

Du ber AI: *“Skriv JavaScript som räknar ett kvitto.”*  
Du får tillbaka något i stil med:

```javascript
var total = "0";
function add(a, b) {
  total = a + b;
}
document.querySelector("#sum").innerText = total;
const add = (a, b) => {
  document.body.innerHTML += a;
};
add();
```

Det *kan* råka “göra något”. Det är svagt mot det här paketet:

- `var` och strängen `"0"` — fel lapp, fel typ.  
- `document.querySelector` / `innerHTML` = DOM, inte konsolen.  
- Två `add` — krock. Arrow + `function` huller om buller.  
- `add()` utan argument. Inget `console.log` som bevis.  
- Ingen tydlig `const` för sånt som är klart.

**Vad du tränar:** Feedback + en kedja *du* äger i konsolen.  
**Varför:** Du ska peka: burk, typ, deklaration vs anrop.  
**Vad det INTE är:** “Den rörde DOM, alltså är det proffsigt.”

### Din uppgift A (ca 25–40 min)

**Steg 1 — Prompt.** Skriv en egen prompt där du ber om ett kvitto *i konsolen* med `const`/`let` och en namngiven `function`. Spara prompten.

**Steg 2 — Granska (checklist)**
- [ ] `var` eller blandade omdeklarationer?  
- [ ] Tal som strängar (`"0"`)?  
- [ ] DOM (`querySelector`, `innerHTML`, klick)?  
- [ ] Funktion som aldrig anropas — eller anrop utan data?  
- [ ] Finns `console.log` så du *ser* resultatet?  
- [ ] Kan du förklara varje rad muntligt?

Skriv **minst tre** rader:  
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

**Steg 3 — Anpassa.** En **ren version du äger** (gärna kopplad till [03](./03-ovningar.md)). Bara syntax + konsol.

---

## Scenario B — if som inte frågar (`==` vs `===`)

Du kör fast och ber AI: *“Varför blir min rabatt alltid fel? Fixa if-satsen.”*

AI ger tillbaka:

```javascript
const kod = "5";
let pris = 50;

if (kod == 5) {
  pris = 0;
}
console.log(pris);
```

Det *ser* ut att funka. `"5" == 5` är `true` — JS gissar. I det här paketet är det fällan.

**Vad du tränar:** Äga jämförelsen.  
**Varför:** Du ska kunna säga vad `===` gör som `==` inte gör.  
**Vad det INTE är:** “AI sa att == räcker.”

### Din uppgift B (ca 15–25 min)

**Steg 1 — Prompt.** Skriv en prompt där du ber om hjälp att *förklara* skillnaden `==` / `===` *eller* felsöka en `if` som alltid går in (eller aldrig). Be om svar i konsolen, namngiven `function` om det behövs — ingen DOM.

Exempel du får utgå från (ändra gärna):

> “Min if går in även när kod är strängen fem och jag jämför med talet fem. Förklara == vs ===. Visa en if med === i console.log. Ingen DOM.”

**Steg 2 — Granska**
- [ ] Använder förslaget `==` “för att det funkar”?  
- [ ] Finns en `if` utan fråga (`if (harRabatt = true)` fyller, frågar inte)?  
- [ ] Loggas båda utfallen så du *ser* dörren?  
- [ ] Kan du säga högt vad `"5" === 5` blir?

Minst **två** FEEDBACK-rader.

**Steg 3 — Anpassa.** Din `if` ska använda `===`. Testa med `true` och `false` (eller två olika `kod`). `console.log` efteråt.

---

## Scenario C — lista av rader med for...of

Du ber AI: *“Loopa mina todos och skriv ut dem.”*

Du får tillbaka något i stil med:

```javascript
const todos = [
  { text: "Mjölk", done: false },
  { text: "Committa", done: true }
];

for (let i = 0; i < todos.length; i++) {
  document.body.innerHTML += todos[i];
}
todos.forEach((t) => console.log(t));
```

Svagt mot paketet: DOM, `i++`-räkning du inte övat, `forEach`/pil, och `todos[i]` som hel objekt utan punkt.

**Vad du tränar:** Gå längs hyllan, läs fält med punkt.  
**Varför:** Du ska äga `for...of` + `rad.text`.  
**Vad det INTE är:** “Den loopade, alltså är det klart.” Array-metoder hör inte hit.

### Din uppgift C (ca 15–25 min)

**Steg 1 — Prompt.** Be om en array med **enkla objekt** (`text`, `done`) och en `for...of` som loggar `text` (och gärna `done`) i konsolen. Säg uttryckligen: ingen DOM, ingen `forEach`, namngiven `function` om AI vill wrappa.

Exempel:

> “Jag har en array av objekt { text, done }. Visa for...of som console.log:ar varje text. Ingen DOM. Ingen forEach.”

**Steg 2 — Granska**
- [ ] DOM eller sidskrivning?  
- [ ] `forEach` / pil-loop i stället för `for...of`?  
- [ ] Loggas hela objektet utan att du kan peka på `.text`?  
- [ ] Kan du peka: hyllan, en rad, punktnotation, loopen?

Minst **två** FEEDBACK-rader.

**Steg 3 — Anpassa.** `for (const rad of todos) { console.log(rad.text); }` — eller motsvarande *du* förklarar.

---

## Reflektion (3 meningar, efter A–C)

1. Vad var svagt i AI-förslagen (typ, `==`, DOM, fel loop)?  
2. Vad ändrade du?  
3. Varför spelar `===` och `for...of` roll när du ska *peka* i egen kod?

---

## Klart-check (peka i DIN fil)

- [ ] FEEDBACK-rader för A, B och C  
- [ ] Peka på en `const` och en `let` och säg varför  
- [ ] Peka på `===` i *din* `if` — vad hade `==` gjort?  
- [ ] Peka på `for...of` och ett `.text`  
- [ ] Peka på något du *tog bort* (DOM, `var`, `==`, `forEach`)  
- [ ] Reflektion klar  

---

## Facit-riktning (titta efter du granskat själv)

- `FEEDBACK: var + "0" → const/let och number 0.`  
- `FEEDBACK: querySelector/innerHTML → stryk; console.log.`  
- `FEEDBACK: add() utan värden → anropa med pris och antal.`  
- `FEEDBACK: två add → ett receptkort, ett namn.`  
- `FEEDBACK: kod == 5 → === så sträng och tal inte blir “lika på låtsas”.`  
- `FEEDBACK: if (x = true) → === (eller if (x)) — = fyller, frågar inte.`  
- `FEEDBACK: forEach / innerHTML → for...of + rad.text i konsolen.`  

**Målsvar (säg högt / skriv i README) — ägarskap:**  
*“Jag tar emot AI-JS som utkast, stryker DOM och gissande ==, och behåller burkar, dörrar och for...of jag kan förklara.”*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
