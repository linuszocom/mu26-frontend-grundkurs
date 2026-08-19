# 01 — Teoriguide: CSS, selektorer & Box Model

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när sidan bara är “naken HTML” — sedan bygger vi upp hur du pekar ut element och styr luft runt dem. Det är inte magi. Det är en metod.

Ingen Hero, inget arv, ingen Flexbox eller Grid här. Bara stylesheet, selektorer och Box Model.

---

## CSS vs HTML — smak och recept

Många tänker nu: “Kan jag inte bara färga i HTML?” Andas.

**Metafor:** HTML är *vad som ligger i lådan* (innehåll + betydelse). **CSS** är *hur lådan ser ut och hur tätt lådorna står* — färg, typsnitt, luft.

**Vad det är:** CSS (Cascading Style Sheets) = regler för utseende.  
**Varför det finns:** Så du inte blandar “vad det *är*” med “hur det *ser ut*”. Semantisk HTML behåller du; stylen bor i CSS.  
**Om det saknas / vad det INTE är:** CSS är INTE ett nytt strukturspråk. Utan CSS ser sidan “browser-naken” ut. Att slänga in `style="…"` överallt i HTML är samma slags röra — vi använder **extern** `style.css`.

**Målsvar (säg högt / skriv i README):**  
*“CSS styr utseendet — färg, typografi, spacing — medan HTML styr struktur och betydelse. Vi håller CSS i en egen fil (`style.css`) och länkar den från HTML.”*

---

## Fil + länk — två filer, en sida

```html
<head>
  <meta charset="UTF-8" />
  <title>Fliknamn</title>
  <link rel="stylesheet" href="style.css" />
</head>
```

`index.html` och `style.css` i **samma mapp**. `href="style.css"` = “hämta stylen härifrån”.

**Vad det är:** En länk från dokumentet till stylesheet.  
**Varför det finns:** En CSS-fil kan styla hela sidan (och senare fler sidor).  
**Om det saknas:** Du har regler i filen men sidan ändras inte — ofta fel sökväg eller glömd `link`. Det är INTE att “CSS är trasigt”.

---

## Selektorer — vem ska ha kläderna?

Många tänker: “Jag skriver `color: red` — men *vad* blir rött?” Just därför: selektorn först.

**Dåligt:** du vill bara färga *en* ruta, men stylar alla `section` — hela sidan blir samma.

```css
section {
  background: gold;
}
```

**Bättre när bara vissa ska träffas:** ge dem en **class** och peka på klassen.

```html
<section class="lapp">Stängt kl 15.</section>
```

```css
.lapp {
  background: gold;
}
```

| Typ | Syntax | Vad det är | När |
|-----|--------|------------|-----|
| Elementselektor | `h1 { … }` | Alla av den taggen | Gemensam typografi för alla `h1` |
| Klassselektor | `.lapp { … }` | Bara element med `class="lapp"` | Undantag / en utvald låda |

Prick före namnet = klass. I HTML: `class="lapp"` utan prick. I CSS: `.lapp` med prick.

**Vad det är:** En selektor = “vilka element gäller regeln?”  
**Varför det finns:** Annars stylar du antingen *allt* eller *inget du menade*.  
**Om det saknas / INTE:** Class-namn i HTML utan CSS-regel gör ingenting. CSS-klass utan `class` i HTML träffar inget. Det är INTE Flex/Grid.

**Målsvar (säg högt / skriv i README) — selektor:**  
*“En selektor pekar ut vilka HTML-element regeln gäller. Elementselektor = alla av en taggtyp. Klassselektor = bara element med den klassen.”*

**Målsvar (säg högt / skriv i README) — metod:**  
*“Vill jag styla alla av en tagg → elementselektor. Vill jag styla bara vissa → ge dem en class och styla `.klassnamn`.”*

---

## En regel — egenskap och värde

```css
p {
  color: #222;
  font-size: 1rem;
  line-height: 1.5;
}
```

`p` = vem. `color` = *vilken* ratt. `#222` = *vilket* värde. Semikolon efter varje deklaration.

Typografi och färg på grundnivå räcker: `font-family`, `font-size`, `color`, `line-height`, `background`.

---

## Box Model — matlådan (problem först)

Många tänker: “Jag satte `margin` men texten kuddade fortfarande mot kanten.” Andas. Då tog du fel lager.

**Dåligt:** texten sitter klistrad mot en synlig kant — du ser “ingen luft inuti”.

```css
.lapp {
  border: 2px solid #333;
  /* ingen padding → maten trycks mot väggen */
}
```

**Bättre:** luft *i facket* = padding. Avstånd *till nästa låda* = margin. Väggen = border. Maten = content.

**Metafor:** Varje HTML-element är en **matlåda**.

| Lager (inifrån) | Bild | CSS | Typiskt jobb |
|-----------------|------|-----|----------------|
| **content** | Maten | bredd/höjd, texten själv | Det som *är* innehållet |
| **padding** | Luft i facket | `padding` | Texten ska inte kuddra mot väggen |
| **border** | Fackets vägg | `border` | Synlig kant (valfritt) |
| **margin** | Avstånd till nästa låda | `margin` | Lådorna ska inte kuddra mot varandra |

**Vad det är:** Box Model = fyra lager runt innehållet.  
**Varför det finns:** Spacing är inte “en magisk luft-egenskap”. Inuti ≠ utanför.  
**Om det saknas / INTE:** Padding är INTE margin. Border är INTE “lite extra padding”. Box Model är INTE layoutverktyg som Flex/Grid.

**Målsvar (säg högt / skriv i README) — Box Model:**  
*“Varje element är som en matlåda: innerst content (maten), sedan padding (luft i facket), border (fackets vägg), margin (avståndet till nästa låda). Spacing styrs främst med padding och margin.”*

---

## Metod — vilken ratt när spacing strular?

1. **Sitter innehållet för nära den här lådans kant?** → `padding` (luft i facket).  
2. **Sitter två lådor för nära varandra?** → `margin` (plats mellan lådor).  
3. **Vill jag se en kant?** → `border`.

Peka i koden (eller i webbläsarens Inspect) och säg lagret högt. Det är färdigheten — inte att gissa pixlar.

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| CSS i HTML med `style="…"` överallt | Extern `style.css` + `link` |
| `h1 .lapp` när du menade klassen `lapp` | `.lapp` = klass. Mellanrum betyder något annat (senare) |
| Class i HTML, glömd prick i CSS | HTML: `class="lapp"`. CSS: `.lapp` |
| `margin` mot “texten kuddra i rutan” | Det är **padding** |
| Flex/Grid “för att det ska bli snyggt” | Inte i det här paketet |
| Glömd `link` | Sidan förblir naken — kolla `head` |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad är CSS till för, jämfört med HTML?  
2. En elementregel och en klassregel (påhittade, men giltiga)  
3. Box Model inifrån och ut — matlådan  
4. Text för nära kant — vilken egenskap?

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna.
