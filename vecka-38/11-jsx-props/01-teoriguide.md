# 01 — Teoriguide: JSX & props

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när samma kort är copy-paste tre gånger — sedan skriver vi skylten på klossen och fäster en följesedel. Det är inte magi. Ingen `useState`.

---

## Problemet först — tre identiska kort, tre ställen att laga

Många tänker nu: “JSX… är det HTML eller JS?” Andas. Du har en Vite-app. Utan uppdelning blir `App` en lapp med tre nästan likadana block. Byter du rubrikstil jagar du tre ställen.

```jsx
function App() {
  return (
    <main>
      <article>
        <h2>Basilika</h2>
        <p>Soligt fönster</p>
      </article>
      <article>
        <h2>Mynta</h2>
        <p>Halvskugga</p>
      </article>
    </main>
  );
}
```

Det *fungerar*. Det skalar inte. Det är därför klossen + följesedeln finns.

---

## Funktionskomponent — klossen med namn

**Vad det är:** En funktion (stor bokstav, t.ex. `Vaxtkort`) som **returnerar** det som ska synas.  
**Varför den finns:** En UI-bit, många gånger.  
**Om den saknas / vad den INTE är:** INTE `useState`. INTE en `.html`-fil. Utan komponent: copy-paste. Det är INTE ett anrop förrän du skriver `<Vaxtkort />`.

**Målsvar (säg högt / skriv i README):**  
*“En funktionskomponent är en UI-bit med namn — en funktion som returnerar det som ska synas — så jag bygger i delar i stället för en enda lång fil.”*

---

## JSX — skylten på klossen

**Metafor:** Klossen har en **skylt** du fyller i: rubrik, stycke, lista. Du känner igen `<h2>` och `<p>`. Skylten sitter *på klossen* (i `.jsx`), inte i en separat HTML-fil i Explorer. Under huven blir det JavaScript — du behöver inte den omvandlingen utantill idag.

**Vad det är:** Så du beskriver hur komponenten ser ut, med taggar inne i JS-filen.  
**Varför det finns:** Så UI och logik kan bo i samma komponent utan att du öppnar två världar.  
**Om det saknas / vad det INTE är:** INTE “HTML i JS” som enda förklaring utan bild. INTE att du slutat använda HTML-idéer. INTE att du kan slänga `index.html` från eventsidan in i `src/` och “det är React”.

Regler du behöver *nu* (inte hela handboken):

- Returnera **ett** rot-element (t.ex. `<article>…</article>` eller en wrapper).  
- `className` i stället för `class` (`class` är reserverat i JS).  
- Taggar ska stängas.  
- Värden från JS i skylten: klamrar, `{namn}`.

**Målsvar (säg högt / skriv i README):**  
*“JSX är skylten på klossen: jag skriver hur biten ska se ut med bekanta taggar, inne i JavaScript-filen. Det är inte en separat .html jag öppnar i Explorer.”*

---

## Props — följesedel / namnbricka

**Metafor:** Samma kartong (samma komponent). På locket sitter en **följesedel** eller **namnbricka**: den här går till “Basilika / soligt fönster”, den andra till “Mynta / halvskugga”. Föräldern *skriver* sedeln. Barnet *läser* den och visar. Utan sedel: antingen hårdkodad text inne i klossen (inte återanvändbar) eller tre nästan-identiska funktioner.

**Vad det är:** In-data till komponenten — som argument till en funktion, skrivet i JSX: `namn="Basilika"`.  
**Varför det finns:** Samma kloss, olika innehåll.  
**Om det saknas / vad det INTE är:** INTE state (det som *ändras över tid* — nästa paket). INTE CSS. Utan props duplicerar du klossen.

```jsx
function Vaxtkort(props) {
  return (
    <article>
      <h2>{props.namn}</h2>
      <p>{props.ljus}</p>
    </article>
  );
}

<Vaxtkort namn="Basilika" ljus="Soligt fönster" />
```

**Målsvar (säg högt / skriv i README):**  
*“Props är följesedeln / namnbrickan som skickas in i klossen så samma komponent kan visa olika innehåll.”*

---

## Statisk lista — första strukturen

Flera `<Vaxtkort … />` under varandra = en lista som **står still**. Det är med flit. När listan ska växa vid klick behövs state — **Examination 2 kommer senare**. Idag: strukturen.

**Vad det är:** Hårdkodade rader/kort i `App`.  
**Varför det finns:** Så du ser props *innan* datan rör sig.  
**Om det saknas / INTE:** INTE `.map` som huvudnummer. INTE `useState`.

---

## Metod — när du tvekar “egen kloss + props?”

Det är inte magi. Tre frågor:

1. Ser jag en **upprepad UI-bit** (kort, rad)? → egen komponent.  
2. Skiljer sig texten/siffran åt? → skicka skillnaden som **props**.  
3. Ska listan växa när någon klickar? → **inte idag** — `useState` nästa paket.

**Målsvar (säg högt / skriv i README) — metod:**  
*“Upprepad bit → kloss. Olika innehåll → följesedel (props). Växa vid klick → state senare.”*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| `vaxtkort` med liten bokstav | Komponent = stor bokstav |
| `class=` i JSX | `className=` |
| Tre funktioner `BasilikaKort`, `MyntaKort` | En kloss + två följesedlar |
| Props “som CSS” | Props = data in, inte styling-verktyg |
| `useState` för att visa två kort | Statiska props räcker |
| Festival-eventsida i React | Annat projekt; här: växter/recept |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad är JSX (skylten)?  
2. Vad är props (följesedeln)?  
3. Var skrivs namnet — hos föräldern eller i barnet?  
4. Varför ingen `useState` än?

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan korten i övningarna.
