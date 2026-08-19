# 03 — Övningar

**Omfång det här paketet:** extern `style.css`, element- och klassselektorer, Box Model (padding, border, margin, content). Ingen Flexbox, Grid, arv eller Hero. Ingen layout “som en hel startsida” — en enkel semantisk sida räcker.

AI får hjälpa dig skriva. Du måste kunna **peka och förklara** varje regel du behåller.

---

## Uppgift 1 — Naken sida (bibliotekslapp)

**Mål:** Länka stylesheet. Typografi + färg. Elementselektor.

**Problem först:** Sidan *har* innehåll, men ser ut som 1995-naken HTML — Times, blå länkar, ingen luft. Det är utseendet du ska rädda. Rör inte semantik-uppdraget: behåll taggarna, lägg till CSS.

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8" />
  <title>Biblioteket Kajen</title>
</head>
<body>
  <header>
    <h1>Biblioteket Kajen</h1>
    <p>Öppet tis–sön 11–18.</p>
  </header>
  <main>
    <section>
      <h2>Just nu</h2>
      <p>Barnbokstisdag 16.00. Ingen föranmälan.</p>
    </section>
  </main>
  <footer>
    <p>Kajen 4</p>
  </footer>
</body>
</html>
```

**Krav:**
1. Mapp `ovning-kajen` → Open Folder → `index.html` (ovan) + `style.css`.  
2. `link` i `head`.  
3. I CSS: styla `body` (t.ex. `font-family`, `color` eller `background`) **och** minst en rubrik med **elementselektor**.  
4. Ingen `style=""` i HTML.

**Klart-check (peka i DIN kod):**
- [ ] Sidan ändrar utseende efter spara + ladda om  
- [ ] Peka på `link` och säg *varför* den sitter i `head`  
- [ ] Peka på en elementselektor och säg *vilka* element den träffar  
- [ ] Ingen Flex/Grid  

**Ägarskap:** AI ok som bollplank — spara prompt + en mening om vad du ändrade. Du ska kunna förklara varje deklaration.

---

## Uppgift 2 — Matlådan (stängt-lapp)

**Mål:** Klassselektor + peka ut Box Model. Problem = text kuddra mot kanten.

**Scenario:** Du ska ha en tydlig “lapp” på sidan: *Stängt 12–13 pga personalmöte.* Först: **utan** padding — texten ska nästan sitta i kanten (så du *ser* problemet). Sedan: rätta med rätt lager.

**Krav:**
1. Samma mapp eller ny `ovning-lapp`. Semantisk HTML med minst `header` + `main` (eget tema — inte Kajen-kopian om du vill byta).  
2. Ett element med `class` (t.ex. `class="lapp"`).  
3. CSS:
   - klassregel med `border`  
   - först medvetet **utan** (eller med `padding: 0`) så felet syns  
   - sedan `padding` så texten får luft i facket  
   - `margin` så lappen inte kuddra mot rubriken  
4. Öppna Inspect i webbläsaren (högerklick → Inspect) och peka på padding vs margin för dig själv.

**Klart-check (peka i DIN kod):**
- [ ] Peka: content, padding, border, margin — *vilken rad*, och *varför* just den  
- [ ] Säg högt: varför padding och inte margin mot “text i kanten”  
- [ ] Säg högt: varför du valde **klass** och inte elementselektor på lappen  
- [ ] Ingen Hero, inget arv, ingen Flex/Grid  

**Ägarskap:** Samma regel som uppgift 1. Om AI slänger in `display: flex` — ta bort det innan du räknar uppgiften som klar.

---

## Uppgift 3 — Stretch (valfritt)

Lägg till en **andra** klass (t.ex. `class="tyst"` på ett `p`) med annan färg eller `font-size`. Två klassregler i samma `style.css`.

**Klart-check:** Motivera i anteckning: varför två klasser istället för att styla alla `p`?

---

## När du kört fast

1. Spara + hård-ladda om. Kolla att `style.css` ligger bredvid HTML och att `href` stämmer.  
2. Kör selektor-metoden högt: alla av taggen, eller bara vissa?  
3. Kör box-metoden: inuti / utanför / kant?  
4. Jämför med [01-teoriguide](./01-teoriguide.md).  
5. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
