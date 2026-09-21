# 01 — Teoriguide: map, key & filter

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när listan i state växer men UI fortfarande har tre fasta rader — sedan stämplar vi en rad per sak och silar med filter. Det är inte magi. Det är två array-metoder.

Du behöver en lista du kan lägga till i. Här gör vi renderingen skalbar.

---

## Problemet först — “tre stolar oavsett kö”

Många tänker nu: “Jag har `join` och `length`. Listan syns.” Andas.

**Dåligt läge:** State har fem filmer. JSX visar `films[0]` … `films[2]` eller en enda sammanfogad mening. Extra rader syns inte som egna poster. Exam 2 kräver att **varje** uppgift renderas ut. Det är problemet `.map()` löser.

`.filter()` är ett annat verktyg: en **ny** lista med bara det som klarar ett villkor. Du övar det nu. Full ta-bort-knapp i UI är nästa paket.

---

## .map() — stämpel på varje kuvert

**Metafor:** En hög **kuvert**. `.map()` är stämpeln: varje kuvert åker förbi och får *samma sorts behandling* — här: blir en JSX-rad. Du får tillbaka en **ny** hög (nu med stämplade kuvert). Originalhögen lämnas.

```jsx
{films.map((film) => (
  <li key={film}>{film}</li>
))}
```

Låter tekniskt — betyder: *för varje sak i arrayen, returnera en UI-bit*.

**Vad det är:** `.map()` går igenom varje element och returnerar en **ny** array. I React: ofta en rad JSX per element.  
**Varför det finns:** Listan i state kan växa. Du ska inte skriva en `<li>` för hand per framtida rad.  
**Om det saknas / vad det INTE är:** Map är INTE filter (den tar inte bort). Map är INTE “React tänker åt dig”. Utan return i callback: `undefined`-hål i listan. `.forEach` returnerar inget användbart för JSX — fel verktyg här.

**Målsvar (säg högt / skriv i README):** *“.map() går igenom varje element och returnerar en ny array — i React ofta en JSX-rad per sak i listan.”*

---

## key — streckkod på kuvertet

**Metafor:** Varje kuvert får en **streckkod / trackingnummer** som inte byter identitet bara för att högen sorteras om. React använder `key` för att veta *vilket barn som är vilket* när listan ändras.

**Vad det är:** `key` = unikt id bland **syskon** i listan.  
**Varför det finns:** Annars kan fel rad “hänga kvar” i React när du lägger till eller (senare) tar bort.  
**Om det saknas / vad det INTE är:** `key` är INTE synlig text för användaren. Index som key (`key={i}`) är ömtåligt när listan kan ändras — brickan följer platsen, inte saken. Bättre: ett `id` på objektet. I övning med unika strängar kan texten duga tillfälligt.

**Målsvar (säg högt / skriv i README) — key:**  
*“key är ett unikt id per list-syskon så React kan matcha rätt rad när listan ändras.”*

---

## .filter() — silen

**Metafor:** En **sil**. Du häller listan genom. Bara det som klarar villkoret stannar i den **nya** skålen. Originalet ligger kvar om du inte ersätter state.

```javascript
const utan = ["Kim", "Alex", "Sam"].filter((namn) => namn !== "Alex");
// utan === ["Kim", "Sam"]
```

**Vad det är:** `.filter()` skapar en ny array med element som ger `true` i villkoret.  
**Varför det finns:** ES6+ sätt att *välja ut* utan att mutera med `splice`. Samma idé du senare behöver för “ta bort en rad ur state”.  
**Om det saknas / vad det INTE är:** Filter är INTE map (den omvandlar inte varje element till JSX). Filter är INTE en radera-knapp. `splice` på state-arrayen är fel mönster — samma push-problem som förut: muterad låda.

I det här paketet: gör en sil-övning (visa en silad lista, eller `console.log`). Du behöver **inte** bygga en ta-bort-knapp per rad.

**Målsvar (säg högt / skriv i README) — filter:**  
*“.filter() skapar en ny array med bara de element som klarar ett villkor.”*

---

## Metod — när du tvekar “hur visar jag alla rader?”

Det är inte magi. Tre steg:

1. **Data finns i state** (`films`, `guests`, …).  
2. **`lista.map((sak) => <li key={…}>{…}</li>)`** inne i JSX. Callback **returnerar** elementet.  
3. **`key`** som är unikt bland syskonen (helst `id`).

Behöver du “alla utom X” i en övning: `lista.filter((sak) => sak !== x)` — ny array. Visa den med map. Spara inte genom att `splice`:a state.

**Målsvar (säg högt / skriv i README) — metod:**  
*“Data finns i state. map till JSX, key på varje barn. Behöver du en lista utan vissa → filter (ny array), inte splice på state.”*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| `films[0]` … `films[3]` när listan kan växa | map stämplar varje kuvert |
| `forEach` i JSX | forEach returnerar inte arrayen React ska rita. map gör det |
| Glömt `return` / glömda parenteser i arrow | Utan return: tomma hål. `(x) => <li>…</li>` returnerar JSX |
| Ingen `key` / `key={index}` när listan ändras | Streckkod som följer saken, inte platsen |
| `splice` / mutera för att “filtrera” | filter → ny array |
| Map och filter är “samma loop” | Map omvandlar. Filter väljer bort. Båda ger ny array |
| Full ta-bort-UI “för att bli klar” | Nästa paket. Sil-övning räcker nu |
| CSS-layout i React | Inte det här paketet |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad gör `.map()` vs `.filter()` i en mening vardera?  
2. Varför `key`?  
3. Varför ny array (inte splice) när du silar?  
4. Varför map mot Exam 2 (visa listan)?

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna.
