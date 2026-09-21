# 01 — Teoriguide: events & lägg till

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när fält och knapp inte är kopplade — sedan kopplar vi tangent och klick till state. Det är inte magi. Det är en metod.

Du behöver en lista i `useState` från förra paketet. Här får användaren en väg in i den.

---

## Problemet först — “knappen finns ju”

Många tänker nu: “Jag har ett input och en knapp. Då kan man väl lägga till.” Andas.

**Dåligt läge:** Ett textfält som lever sitt eget liv. En knapp som inte anropar något. Listan i state ligger kvar. Du klickar — tyst. Det är två olika problem:

1. **Ingen koppling** — UI är dekoration.  
2. **Fel sorts uppdatering** — du muterar samma array och React får ingen tydlig “ny lista”.

Events löser (1). Ny array till set-funktionen löser (2).

Det här paketet stannar vid **lägg till**. Ingen sila-bort-rad. Ingen klar-bock. Visa gärna listan med `{items.join(" · ")}` och `{items.length}` så du *ser* tillägget — rad-för-rad med `.map()` får nästa paket.

---

## Event — ringklocka på cykeln

**Metafor:** En **ringklocka på styret**. Du trycker — det ska hända något (folk hör). Själva klockan är bara metall tills den är kopplad till en rörelse. `onClick` / `onChange` är den kopplingen: *när det här händer, kör den här funktionen*.

En annan bild: **flaggan på en postlåda**. Någon fäller upp den = en signal. Utan flagga (utan `onChange`/`onClick`) vet koden inte att något hänt.

**Vad det är:** Ett event = något användaren gör (tangent, klick). I React: `onChange={funktion}`, `onClick={funktion}`.  
**Varför det finns:** Annars är fält och knapp bara dekoration — Exam 2 kräver att klick faktiskt lägger till.  
**Om det saknas / vad det INTE är:** Event är INTE “kalender-event”. Det är INTE CSS. Utan handler: du trycker på klockan, ingen ljuder. `onChange` är INTE samma sak som “lägg till i listan” — det synkar bara det du skriver just nu.

**Målsvar (säg högt / skriv i README):** *“onChange och onClick kopplar användarens handling till din funktion. Där läser du värdet och uppdaterar state — då re-renderar UI.”*

---

## Två state — lappen vs högen i lådan

Många tänker: “Ett state räcker, det är ju en lista.” Stopp. Det du *skriver* och det som *redan ligger i listan* är två sanningar.

**Metafor:** **Postlådan.** Lappen du fyller i *nu* (namn, adress) är inte samma sak som bunten redan i lådan. `draft` = lappen. `items` = bunten. Vid “posta” / Lägg till: flytta texten från lappen till bunten, sudda lappen.

| State | Vad det är (+ bild) | Varför | Om saknas / INTE |
|-------|---------------------|--------|------------------|
| `items` / `guests` | Sparad lista (bunten) | Det Exam 2 ska visa och växa | INTE texten i fältet |
| `draft` | Texten i fältet just nu (lappen) | Du måste veta *vad* som ska in | Utan den gissar du, eller läser DOM i smyg |
| `value={draft}` | Fältet *styrs* av state | Du äger det som står där | Fältet “lever sitt liv” |
| `onChange` → `setDraft(e.target.value)` | Varje tangent uppdaterar lappen | Synk | INTE lägg till än |
| `onClick` → lägg till + `setDraft("")` | Kassaknapp: registrera, nollställ | Ett klick = ett tillägg | Glömmer du tömma: nästa klick dubblar |

`e.target.value` låter tekniskt — betyder: *texten som står i fältet*. Inte magi.

**Målsvar (säg högt / skriv i README) — två state:**  
*“Ett state för texten i fältet just nu, ett för den sparade listan. Vid Lägg till flyttar du text från fältet till listan och tömmer fältet.”*

---

## Immutabel uppdatering — ny bunt, inte tryck in i den gamla

**Vad det är:** Du bygger en **ny** array och skickar den till `setItems`. Spread: `setItems([...items, text])` = kopiera det som fanns, lägg den nya sist.  
**Varför det finns:** React jämför “fick jag ett nytt värde?”. Samma array-referens efter `push` är en luddig signal — UI kan ligga kvar.  
**Om det saknas / vad det INTE är:** `items.push(text)` muterar den gamla lådan. Det är INTE “snabbare och därför proffsigt” här. `push` är INTE förbjudet i vanligt JS — det är fel **mönster för React-state**.

```jsx
function handleAdd() {
  const text = draft.trim();
  if (text === "") return;
  setItems([...items, text]);
  setDraft("");
}
```

`trim` + tom-check: tom klockringning ska inte skapa tomma rader.

**Målsvar (säg högt / skriv i README) — immutabel:**  
*“Du skapar en ny array med det nya innehållet och skickar den till set-funktionen. Du muterar inte den gamla state-arrayen med push.”*

---

## Kedjan vid klick

1. Läs `draft` (lappen).  
2. Bygg ny array, `setItems`.  
3. `setDraft("")`.  
4. React re-renderar — listan (t.ex. `join`) och fältet följer.

**Vad kedjan är:** Event → läs → ny state → UI.  
**Varför den finns:** Exam 2: skriva + knapp → ny uppgift syns.  
**Om den saknas:** Klick utan `setItems`, eller `push`, eller fältet töms inte.

---

## Metod — när du tvekar “hur får jag in raden i listan?”

Det är inte magi. Tre steg:

1. **`onChange`** → `setDraft(e.target.value)`. Fältet har `value={draft}`.  
2. **`onClick`** på knappen (`type="button"` så sidan inte laddas om av misstag).  
3. **Om text finns:** `setItems([...items, text])`, sedan töm draft.

**Målsvar (säg högt / skriv i README) — metod:**  
*“onChange sparar det som står i fältet. onClick: om text finns → ny array via spread → töm fältet.”*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| Input + knapp utan `onChange`/`onClick` | Ringklocka utan koppling. Koppla funktioner |
| Ett enda state för både fält och lista | Lappen ≠ bunten. Två state |
| `items.push(draft)` sedan `setItems(items)` | Samma array. Spread: ny array |
| Fält utan `value={draft}` | Du styr inte vad som står där |
| Tomma rader | `trim` + `if (text === "") return` |
| `type="submit"` i form → sidan laddas om | `type="button"` på lägg-till |
| Bygga ta bort / klar / CSS-layout | Inte det här paketet |
| `.map()` som hela uppgiften | Nästa paket. `join` + `length` räcker för att se add |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad gör `onChange` vs `onClick`?  
2. Varför två state?  
3. Varför `[...items, text]` och inte `push`?  
4. Kedjan vid klick, tre steg.

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna.
