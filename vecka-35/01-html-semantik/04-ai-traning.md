# 04 — AI-träning: semantik & ägarskap

AI kan skriva HTML på sekunder. Det betyder inte att *du* äger den. Här tränar du samma färdighet som Exam 1 kräver: **se vad som är svagt, ändra, förklara**.

Det är inte magi att “granska AI”. Det är samma metod som i teoriguiden — intervjua varje bit.

---

## Scenario — problem först

Du ber AI: *“Gör en HTML-sida för en liten bokklubb.”*  
Du får tillbaka något i stil med:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Bokklubb</title>
</head>
<body>
  <div class="top">
    <div class="title">Bokklubben Ordet</div>
    <div class="sub">Vi läser klart på torsdag</div>
  </div>
  <div class="content">
    <div class="heading">Nästa bok</div>
    <div>En roman om havet</div>
    <div><a href="#">Mer</a></div>
  </div>
  <div class="bottom">Kontakt: bok@example.com</div>
</body>
</html>
```

Det *kan* se okej ut i webbläsaren. Class-namn (`top`, `title`) *låtsas* vara struktur — men taggen är fortfarande bara `div`. Det är kartonger utan avdelningsnamn. Svagt mot kursens krav på semantik.

**Vad du tränar:** Feedback på AI-kod + omskrivning du äger.  
**Varför:** Muntligt och README kräver att *du* kan motivera taggarna.  
**Vad det INTE är:** “AI skrev det, alltså är det klart.”

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en egen prompt till AI (eller jobba bara mot snutten ovan utan ny AI) där du ber om en bokklubb-sida. Spara prompten.

### Steg 2 — Granska (checklist)
Gå igenom koden (AI:ns eller snutten) och kryssa:

- [ ] Finns `lang` på `html`?  
- [ ] Finns `charset` / vettig `head`?  
- [ ] Används `header` / `main` / `footer` (eller liknande) där det passar?  
- [ ] Finns riktig `h1` (inte bara `div` som ser ut som rubrik)?  
- [ ] Saknas betydelse — bara `div` + class-namn som låtsas vara struktur?  
- [ ] Kan du förklara varje tagg muntligt?

Skriv **minst tre** konkreta feedback-punkter i formen:  
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Skriv om sidan till semantisk HTML **du äger**. Spara som `ovning-ai-bokklubb/index.html`.

### Steg 4 — Reflektion (3 meningar)
Skriv i anteckningar eller en `REFLEKTION.md` i mappen:

1. Vad var fel eller svagt i AI-förslaget (eller snutten)?  
2. Vad ändrade du?  
3. Varför är det viktigt inför Exam 1 README / muntligt ägarskap?

---

## Klart-check (peka i DIN omskrivna kod)

- [ ] Tre FEEDBACK-rader sparade  
- [ ] Peka på `h1` / `header` / `main` (eller motsvarande) och säg *varför*  
- [ ] Peka på något du *tog bort eller ändrade* från AI — varför dög det inte?  
- [ ] Reflektionens tre meningar klara  

---

## Facit-riktning (titta efter du granskat själv)

Exempel på giltig feedback (dina egna ord får skilja sig):

- `FEEDBACK: Rubriken är en div → använd h1 (sidans huvudämne).`  
- `FEEDBACK: topp/bottom är generiska div → header respektive footer.`  
- `FEEDBACK: saknar lang/charset → lägg till så språket och åäö hanteras rätt.`  
- `FEEDBACK: class-namn ersätter inte semantik → taggen ska bära betydelsen.`

**Målsvar (säg högt / skriv i README) — ägarskap:**  
*“Jag tar emot AI-förslag som utkast, granskar tagg för tagg, och behåller bara det jag kan förklara.”*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
