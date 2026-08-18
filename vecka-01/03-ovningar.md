# 03 — Övningar

**Omfång den här veckan:** HTML-struktur och semantik. Ingen CSS-layout/design. Ingen Flex/Grid. Fokusera på betydelse i taggarna — hyllskyltarna, inte hur det ser ut.

AI får hjälpa dig skriva. Du måste kunna **peka och förklara** varje tagg du behåller.

---

## Uppgift 1 — Rädda div-soppan (café)

**Mål:** Semantisk HTML + grundtaggar; metod vid taggval.

**Problem först:** Någon lämnat den här filen. Den *syns* i webbläsaren men koden saknar betydelse — bara kartonger utan avdelningsnamn. Det är behoven du ska lösa.

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8" />
  <title>Café</title>
</head>
<body>
  <div>
    <div>Café Bryggan</div>
    <div>Kaffe och bullar vid ån</div>
  </div>
  <div>
    <div>Dagens lunch</div>
    <div>Soppa + bröd — 95 kr</div>
    <div>Mer info</div>
  </div>
  <div>
    <div>Öppet mån–fre 08–16</div>
    <div>Instagram</div>
  </div>
</body>
</html>
```

**Krav:**
1. Skapa mapp `ovning-cafe` → **File → Open Folder** i VS Code → filen `index.html`.
2. Skriv om till giltigt skelett + **semantiska** områden (minst tre av: `header`, `main`, `section`/`article`, `footer`; gärna `nav` om du har en länk-meny).
3. Använd `h1`/`h2`, `p`, minst en `a` med `href` (t.ex. `#` eller en påhittad URL).
4. Valfritt: en `img` med `alt` (placeholder-URL eller lokal fil).

**Klart-check (peka i DIN kod):**
- [ ] Sidan öppnas i webbläsaren efter spara  
- [ ] Peka på tre taggar och säg *varför* (metod: vad *är* det? → matcha tagg)  
- [ ] Peka på minst ett ställe där du *medvetet* undvek `div` — varför?  
- [ ] Inga onödiga `div` där en semantisk tagg passar  

**Ägarskap:**
- Utan AI: skriv om själv.  
- Med AI: tillåtet som bollplank — spara din prompt och **en mening** om vad du ändrade efteråt. Du ska kunna förklara varje tagg.

---

## Uppgift 2 — Från brief till taggar (podd-landning)

**Mål:** Metod “intervjuinnehållet”; minst tre semantiska områden; förklara semantik.

Många tänker nu: “Ingen färdig kod — var börjar jag?” Börja i briefen. Intervjua varje bit innan du skriver en enda tagg.

**Brief (ingen färdig kod):**  
Bygg en enkelsida för podcasten *“Kod & Kaffe”*, avsnitt 12. Sidan ska ha: show-namn + avsnittsrubrik högst upp; kort intro; en sektion “I det här avsnittet” med tre punkter (du får använda `ul`/`li` eller tre `p`); länk “Lyssna” (kan peka på `#`); sidfot med “© Kod & Kaffe”.

**Krav:**
1. Ny mapp `ovning-podd` + `index.html`.  
2. Semantisk struktur — eget tema (podd), inte en kopia av café-sidan.  
3. En `h1`, logisk rubrikhierarki.  
4. Skriv i en HTML-kommentar högst upp i filen din metod i en mening: hur du valde tagg för toppblocket.  
   Använd HTML-syntax: `<!-- din metod här -->`.  
   **Inte** `// …` — det är JavaScript-kommentar. I en `.html`-fil syns `//` som vanlig text på sidan.

**Klart-check (peka i DIN kod):**
- [ ] Briefens innehåll finns  
- [ ] Minst tre semantiska områden — peka och säg rollen för varje  
- [ ] Kommentaren högst upp beskriver metoden (inte “jag valde header för att det såg bra ut”)  
- [ ] Du kan förklara semantik med egna ord (skriv 2–3 meningar i anteckningar — träning inför examinationens README)

**Ägarskap:** Samma regel som uppgift 1. Om AI genererar sidan: ta bort allt du inte förstår innan du räknar den som klar.

---

## Uppgift 3 — Stretch (valfritt)

Lägg till två `article` (t.ex. “Avsnitt 11” och “Avsnitt 12”) inuti `main`, var med `h2` + `p`.

**Klart-check:** Motivera i anteckning: varför `article` och inte bara `div`? (Vad *är* biten? Vad säger taggen? Vad skulle saknas med bara `div`?)

---

## När du kört fast

1. Spara + ladda om.  
2. Kör metoden högt: “Vad *är* den här biten?”  
3. Jämför med [01-teoriguide](./01-teoriguide.md) — särskilt målsvaren.  
4. Gå vidare till [04 — AI-träning](./04-ai-traning.md) — den tränar just “förslag med bara div”.
