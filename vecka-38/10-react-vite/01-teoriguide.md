# 01 — Teoriguide: DOM vs React & Vite

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när du petar i sidan nod för nod — sedan öppnar vi kartongen och sätter ihop klossar. Det är inte magi. Ingen `useState`. Ingen ToDo. Ingen Figma.

---

## Problemet först — “hitta noden, ändra texten, igen”

Många tänker nu: “React… det är ett nytt språk.” Andas. Du har redan JavaScript. Frågan är *hur UI:t hålls i takt* när samma sak ska synas på flera ställen.

**Dåligt läge:** En rubrik ska säga samma sak som en namnlist. Med pincett: hitta nod A, skriv text; hitta nod B, skriv samma text. Glöm en — sidan ljuger.

---

## DOM — pincett på HTML-noder

**Metafor:** Sidan är redan ihopsatt i webbläsaren. **DOM** är noderna du kan ta i. Vanlig JS = **pincett**: nyp fast en nod, byt text, lägg till en bit. Det funkar för en engångsändring.

**Vad det är:** Webbläsarens modell av sidans element, som du kan peta i steg för steg.  
**Varför det finns:** Små ingrepp, en nod, en gång.  
**Om det saknas / vad det INTE är:** INTE “förbjudet”. INTE CSS. När många ställen ska följa *samma* data blir pincetten copy-paste och “vilken nod var det nu?”.

**Målsvar (säg högt / skriv i README):**  
*“DOM är sidans HTML-noder i webbläsaren. Med vanlig JS plockar jag dem med pincett och ändrar en i taget.”*

---

## React — skruva efter mall, inte pincett överallt

**Metafor:** I stället för att nypa i varje skruvhål med pincett får du en **mall** (så ska det se ut) och en **färdig möbel i kartong**. Du beskriver vad som ska synas. React sätter ihop det som syns. Du jagar inte varje nod för hand.

**Vad det är:** Ett sätt att bygga UI av **komponenter** — beskrivningen av vad som ska synas, utifrån data.  
**Varför det finns:** Interaktiva appar (listor, formulär) där UI ska följa data.  
**Om det saknas / vad det INTE är:** INTE “deklarativt” som tomt modeord. INTE en ersättning för HTML-kunskap. INTE `useState` än. INTE Figma.

**Målsvar (säg högt / skriv i README):**  
*“Med React beskriver jag vad som ska synas — som att skruva ihop en möbel efter mall — i stället för att peta i varje nod för hand.”*

---

## Komponent — LEGO-kloss

**Metafor:** En **LEGO-kloss**: samma sorts bit (en namnskylt, ett kort). Du formger klossen en gång. Sen sätter du in den där den behövs. Utan klossar: en enda lång fil där allt sitter fast.

**Vad det är:** En återanvändbar UI-bit (ofta en funktion som returnerar det som ska synas).  
**Varför den finns:** Samma UI-mönster flera gånger, utan copy-paste.  
**Om den saknas / vad den INTE är:** INTE en hel app. INTE props-djup än (nästa paket). En mening räcker idag.

**Målsvar (säg högt / skriv i README):**  
*“En komponent är en LEGO-kloss: en återanvändbar UI-bit jag bygger en gång och sätter in där den behövs.”*

---

## Vite — kartongen med skruvar

**Vad det är:** Verktyget som **skapar** React-projektet på disk och kör utvecklingsservern (`npm run dev`).  
**Varför det finns:** Annars bygger du mappstruktur, bundling och startfil för hand.  
**Om det saknas / vad det INTE är:** INTE React självt. INTE “spara i VS Code”. Utan create: ingen stomme. Det är INTE eventsidans `index.html`-projekt.

Två filer att kunna peka på (grundnivå):

- `src/main.jsx` — här tänds appen (React kopplas till en rot i sidan).  
- `src/App.jsx` — klossen du oftast börjar redigera.

**Målsvar (säg högt / skriv i README):**  
*“Vite ger mig den färdiga kartongen med projektmappar och en dev-server, så jag inte bygger stomme från en tom mapp.”*

---

## Metod — när du tvekar “pincett eller kloss?”

Det är inte magi. Tre frågor:

1. Ska UI följa data som ändras (lista, formulär)? → React-tänk (mall), inte pincett överallt.  
2. Samma UI-bit flera gånger? → **komponent**.  
3. Behöver jag projektet på disk? → `create` med Vite, öppna mappen i VS Code, `npm run dev`.

**Vad metoden är:** Välj verktyg efter problemet, sen kartongen.  
**Varför den finns:** Exam 2 (kommer senare) byggs i Vite+React — inte som eventsidans HTML-fil.  
**Om den saknas:** Du mixar `querySelector` i en React-fil “för att det kändes bekant”, eller skippar create.

**Målsvar (säg högt / skriv i README) — metod:**  
*“Pincett för en engångsnod. Mall + LEGO-kloss när UI ska återanvändas och följa data. Vite när jag behöver projektstomme.”*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| React = Vite | React = klossarna. Vite = kartongen + servern |
| `useState` “redan nu” | Inte i det här paketet |
| Bygga eventsidans HTML i Vite | Annat projekt, annat mål |
| Figma-export | Inte i kursen |
| Öppna fel mapp i VS Code | **File → Open Folder** på projektmappen (där `package.json` finns) |
| `npm run dev` utan `npm install` | Installera beroenden först |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. DOM vs React i en mening (pincett vs mall)  
2. Vad är en komponent till för? (en mening)  
3. Vad gör Vite?  
4. Vilken fil redigerar du först — `main` eller `App`?

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan skapa projektet i övningarna.
