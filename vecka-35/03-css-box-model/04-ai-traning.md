# 04 — AI-träning: CSS & ägarskap

AI kan spotta ur sig CSS på sekunder. Det betyder inte att *du* äger spacingen. Här tränar du: **se vad som är svagt, ändra, förklara** — samma ägarskap som examinationen kräver.

Det är inte magi. Det är selektor-metoden + matlådan.

---

## Scenario — problem först

Du ber AI: *“Gör sidan snygg med CSS.”*  
Du får tillbaka något i stil med:

```html
<section style="margin: 40px; display: flex; gap: 2rem;">
  <div class="card">Hej</div>
</section>
```

```css
div {
  padding: 0;
  margin: 40px;
  border: 1px solid #000;
}
h1 .card {
  color: red;
}
```

Det *kan* se “designat” ut. Det är svagt mot det här paketet:

- **Inline** `style=` blandar utseende in i HTML.  
- **`display: flex`** är layout du inte ska gömma dig bakom här.  
- **`div { margin: 40px }`** + text mot kanten: fel ratt (margin istället för padding), och den träffar *alla* div.  
- **`h1 .card`** (mellanslag) är inte samma sak som klassen på elementet du tror.

**Vad du tränar:** Feedback + omskrivning till `style.css` du äger.  
**Varför:** Du ska peka ut Box Model och selektorval — inte “AI gjorde den snygg”.  
**Vad det INTE är:** Flex, Grid, Hero eller arv “för att det såg proffsigt ut”.

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en egen prompt (eller jobba mot snutten) där du ber om styling för en liten info-sida, t.ex. en föreningslapp. Spara prompten.

### Steg 2 — Granska (checklist)
Kryssa mot koden du fick:

- [ ] Extern `style.css` + `link` — eller inline/style-tagg överallt?  
- [ ] Flex/Grid/position som du **inte** kan förklara i det här paketet?  
- [ ] Selektorer: träffar de *det du menade*?  
- [ ] Text nära kant: padding eller margin?  
- [ ] Kan du peka content / padding / border / margin?

Skriv **minst tre** rader:  
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Skriv om till `ovning-ai-css/index.html` + `style.css`. Minst en elementselektor, minst en klass, synlig box (border + padding + margin) på klassen. Inget Flex/Grid.

### Steg 4 — Reflektion (3 meningar)

1. Vad var svagt i förslaget?  
2. Vad ändrade du?  
3. Varför spelar ägarskap roll när eventsidan ska stylas senare?

---

## Klart-check (peka i DIN omskrivna kod)

- [ ] Tre FEEDBACK-rader  
- [ ] Peka på `link` + en klassregel + padding-raden — säg *varför*  
- [ ] Peka på något du *tog bort* från AI  
- [ ] Reflektion klar  

---

## Facit-riktning (titta efter du granskat själv)

- `FEEDBACK: style= på elementet → flytta till style.css och länka.`  
- `FEEDBACK: display flex → ta bort; inte det här paketet.`  
- `FEEDBACK: margin mot text-i-kant → padding (luft i facket).`  
- `FEEDBACK: h1 .card → antingen .card på rätt element, eller elementselektor utan mellanslag-fällan.`

**Målsvar (säg högt / skriv i README) — ägarskap:**  
*“Jag tar emot AI-CSS som utkast, granskar selektor och box-lager, och behåller bara det jag kan peka ut.”*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
