# 01 — Teoriguide: HTML & semantik

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du veckan från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [veckans README](./README.md).

Vi börjar med **vad som går sönder** när HTML saknar betydelse — sedan bygger vi upp hur du väljer rätt tagg. Det är inte magi. Det är en metod.

---

## HTML vs utseende — vara och skyltfönster

Många tänker nu: “HTML… ska sidan se snygg ut redan?” Andas.

**Metafor:** En webbsida är som en butik. **HTML** är *vad som säljs* och *vilken avdelning det tillhör* (mejeri, kassa, skyltfönster). **CSS** (senare i kursen) är belysning, färg och hur det ser ut — inredningen.

**Vad det är:** HTML = struktur och *betydelse* (vad är det här för innehåll?).  
**Varför det finns:** Utan struktur blandar du ihop “vad det är” med “hur det ser ut”.  
**Om det saknas / vad det INTE är:** HTML är INTE designverktyget. Om du försöker “göra det snyggt” med bara HTML-taggar blandar du ihop lagren.

**Målsvar (säg högt / skriv i README):** *“HTML beskriver innehåll och betydelse; utseende kommer senare med CSS.”*

---

## Filstruktur — projekt = en lokal

**Metafor:** VS Code “står” i en mapp som du står i en butikslokal. Öppnar du fel mapp letar du efter varor i fel lokal.

1. Skapa en **mapp** för projektet (t.ex. `min-sida`).  
2. Öppna den i VS Code: **File → Open Folder**.  
3. Filen `index.html` — vanlig startsida (konvention).  
4. Arbetsflöde: skriv → **spara** → öppna/ladda om i webbläsaren.

**Vad det är:** En projektmapp + `index.html`.  
**Varför det finns:** Så alla filer hör ihop och webbläsaren/editorn vet var de ligger.  
**Om det saknas:** Utan “Open Folder” ser du ofta fel filer. Utan spara ser du gammal sida.

---

## Skelettet — butikens grundplan

Nästan varje HTML-sida har samma grundplan. Tänk planritning innan du fyller hyllorna.

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8" />
  <title>Fliknamn</title>
</head>
<body>
  <!-- synligt innehåll -->
</body>
</html>
```

| Del | Vad det är (+ bild) | Varför | Om saknas / INTE |
|-----|---------------------|--------|------------------|
| `DOCTYPE` | Deklaration: “modern HTML” | Webbläsaren tolkar rätt | Kan hamna i konstigt läge |
| `html` | Hela dokumentet / hela lokalen | Allt annat ligger här | Dokumentet saknar rot |
| `head` | Följesedel *om* sidan | Titel, teckenkodning | **INTE** synligt sidhuvud |
| `body` | Det kunden ser i butiken | Det användaren *ser* | Innehåll utanför syns fel |
| `header` (i body) | Namnskylten vid ingången | Visar vad sidan är | Blanda inte ihop med `head` |

---

## Semantisk HTML — fel först

Många tänker: “`div` funkar ju — varför krångla?” Just därför börjar vi i det svaga läget.

**Dåligt:** allt är `div` — tre kartonger utan avdelningsnamn.

```html
<div>
  <div>Café Sol</div>
  <div>Öppet 10–18</div>
</div>
```

Webbläsaren *kan* visa texten, men koden säger inte “det här är sidhuvud” eller “det här är huvudrubrik”. En klasskamrat, en skärmläsare och du själv om tre veckor får gissa. Det är problemet semantik löser.

**Bättre:** taggar efter betydelse — hyllskyltar på avdelningarna.

```html
<header>
  <h1>Café Sol</h1>
  <p>Öppet 10–18</p>
</header>
```

**Vad det är:** Semantisk HTML = välja tagg efter vad innehållet *betyder*.  
**Varför det finns:** Tydlig struktur för dig, andra och verktyg — och för Exam 1:s README-fråga.  
**Om det saknas / vad det INTE är:** Semantik är INTE “snygg design”. Design = CSS. `div` är en generisk kartong — den säger ingenting om betydelsen.

**Målsvar (säg högt / skriv i README) — semantik:**  
*“Semantisk HTML betyder att vi väljer taggar efter vad innehållet betyder — t.ex. header för sidhuvud — så strukturen blir tydlig för människor och verktyg. Det är bättre än bara div överallt, för div säger ingenting om betydelsen.”*

---

## Grundtaggar du ska kunna

| Tagg | Betydelse (kort) |
|------|------------------|
| `h1`–`h3` | Rubriker (hierarki; normalt **en** `h1` per sida) |
| `p` | Stycke brödtext |
| `a` | Länk (`href` = adress) |
| `img` | Bild (`src` + **`alt`**-text) |
| `header` | Sidhuvud / toppblock |
| `nav` | Navigationslänkar |
| `main` | Sidans huvudinnehåll |
| `section` | Tematisk sektion |
| `article` | Fristående bit (t.ex. ett inlägg) |
| `footer` | Sidfot |

---

## Metod — intervjuinnehållet (när du tvekar)

Många sitter nu och tänker: “Jag vet inte vilken tagg… då tar jag `div`.” Stopp. Det är inte magi — det är tre frågor.

1. **Intervjua biten:** Vad *är* det här? (sidhuvud? meny? huvudinnehåll? fristående inlägg? sidfot? rubrik? stycke? länk? bild?)  
2. **Matcha tagg** vars betydelse svarar på frågan.  
3. **Stopp vid “låda”:** Om du bara tänker “jag behöver en låda” — risk för `div`. Gå tillbaka till steg 1. Hellre fråga eller slå upp än gissa.

**Vad metoden är:** Ett sätt att välja tagg utan gissning.  
**Varför den finns:** Annars landar allt i `div` “tills vidare” — och “tills vidare” blir permanent.  
**Om den saknas:** Du bygger sidor som *ser* ut att funka men som du inte kan förklara.

**Målsvar (säg högt / skriv i README) — metod:**  
*“Jag frågar först vad innehållet är, sedan väljer jag en tagg som betyder samma sak. Om jag bara tänker ‘låda’ stannar jag — då är risken div.”*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| `head` = sidhuvud | `head` = om dokumentet; `header` i `body` = synligt sidhuvud |
| Semantik = snygg design | Semantik = betydelse i koden; design = CSS |
| Många `h1` | En tydlig `h1` för sidans huvudämne |
| `img` utan `alt` | Beskriv bilden kort för den som inte ser den |
| Allt i `div` “tills vidare” | Välj betydelse nu — det är det du tränar den här veckan |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad är semantisk HTML? (sikta på målsvaret)  
2. Skillnad `head` vs `header` i en mening  
3. Metodens tre steg

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna.
