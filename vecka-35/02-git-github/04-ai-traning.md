# 04 — AI-träning: Git-kedjan & ägarskap

AI kan klistra in Git-kommandon på sekunder. Det betyder inte att *du* äger historiken. Här tränar du samma färdighet som Exam 1 kräver: **se vad som är svagt, ändra, förklara**.

Det är inte magi att “granska AI”. Det är samma metod som i teoriguiden — tre steg + push.

---

## Scenario — problem först

Du ber AI: *“Hjälp mig lägga upp mitt projekt på GitHub.”*  
Du får tillbaka något i stil med:

```text
git init
git add .
git commit -m "update"
git branch -M main
git remote add origin https://github.com/någon/okänt-repo.git
git push -u origin main
git checkout -b feature/styling
```

Det *kan* råka fungera. Det är ändå svagt mot det här paketets krav:

- `git add .` tar **allt** i mappen (ibland skräp du inte menade).  
- `"update"` säger ingenting i historiken.  
- Branch/checkout hör **inte** hit — extra knappar du inte kan försvara.  
- `remote` mot fel URL = push till någon annans (eller ett påhittat) repo.

**Vad du tränar:** Feedback på AI-råd + en kedja *du* äger.  
**Varför:** Muntligt och Exam 1 kräver att *du* kan peka: add vs commit vs push, och vem som syns.  
**Vad det INTE är:** “AI sa att jag skulle göra en branch, alltså är det proffsigt.”

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en egen prompt till AI (eller jobba bara mot snutten ovan utan ny AI) där du ber om hjälp att publicera en enkel HTML-sida. Spara prompten.

### Steg 2 — Granska (checklist)
Gå igenom svaret (AI:ns eller snutten) och kryssa:

- [ ] Tar `add` *specifika* filer — eller `.` / hela världen?  
- [ ] Är commit-meddelandet konkret?  
- [ ] Finns steg du **inte** behöver (branch, merge, pull request)?  
- [ ] Pekar `remote`/`clone` på **ditt** repo?  
- [ ] Förklaras skillnaden Git vs GitHub — eller bara en kommandolista?  
- [ ] Kan du förklara varje rad muntligt?

Skriv **minst tre** konkreta feedback-punkter i formen:  
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Kör (eller skriv upp) en **ren kedja du äger** mot *ditt* övningsrepo från [03](./03-ovningar.md) — eller ett nytt mini-repo. Inga branches. Tydligt meddelande. Spara kommandona du faktiskt körde i `GIT-KEDJA.md` i mappen (en lista, inga hemligheter/tokens).

### Steg 4 — Reflektion (3 meningar)
Skriv i anteckningar eller samma `GIT-KEDJA.md`:

1. Vad var fel eller svagt i AI-förslaget (eller snutten)?  
2. Vad ändrade du?  
3. Varför är det viktigt inför Exam 1 (synlig historik / ägarskap)?

---

## Klart-check (peka i DITT repo)

- [ ] Tre FEEDBACK-rader sparade  
- [ ] Peka på en commit på GitHub och säg *varför* meddelandet duger  
- [ ] Peka på något du *tog bort* från AI-listan — varför behövdes det inte?  
- [ ] Reflektionens tre meningar klara  

---

## Facit-riktning (titta efter du granskat själv)

Exempel på giltig feedback (dina egna ord får skilja sig):

- `FEEDBACK: git add . → lägg bara till de filer jag menar, t.ex. index.html.`  
- `FEEDBACK: meddelandet "update" → skriv vad som ändrades.`  
- `FEEDBACK: branch/checkout → stryk; repo + add/commit/push räcker här.`  
- `FEEDBACK: origin-URL:en är inte mitt repo → clone/push mot min GitHub-adress.`

**Målsvar (säg högt / skriv i README) — ägarskap:**  
*“Jag tar emot AI-förslag som utkast, granskar kommando för kommando, och behåller bara det jag kan förklara.”*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
