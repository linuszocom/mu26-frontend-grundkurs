# 03 — Övningar

**Omfång det här paketet:** GitHub-repo, `add` → `commit` → `push`, synlig medverkan. Ingen CSS. Inga branches, merge eller pull requests. HTML-sidan ska bara *finnas* så kedjan har något att spara — semantik räcker på grundnivå.

AI får hjälpa dig knappa kommandon. Du måste kunna **peka och förklara** varje steg du kör.

---

## Uppgift 1 — Rädda “det ligger ju på datorn”

**Mål:** Förstå problemet när Spara ≠ GitHub. Köra kedjan tills filen syns på github.com.

**Problem först:** Du har den här sidan lokalt. Den *finns* i VS Code. Den finns **inte** som checkpoint och **inte** på GitHub. Det är läget du ska ta dig ur.

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8" />
  <title>Växthyllan</title>
</head>
<body>
  <header>
    <h1>Växthyllan</h1>
    <p>En enkel lista över sticklingar.</p>
  </header>
  <main>
    <p>Basilika — fönsterbräda.</p>
  </main>
</body>
</html>
```

**Krav:**
1. Skapa ett **nytt publikt** repo på GitHub (t.ex. `fornamn-vaxthyllan`). Gärna **utan** README, så clone ger en tom mapp.
2. `git clone` → **File → Open Folder** i VS Code på den mappen.
3. Sätt `user.name` och `user.email` om de saknas (`git config --global …`).
4. Skapa `index.html` med innehållet ovan (eller eget tema — inte en kopia av HTML-paketets café/podd).
5. Kör: `git status` → `git add` → `git commit -m "…"` → `git push`.
6. Öppna github.com: filen syns **och** fliken Commits visar meddelandet + ditt namn.

**Klart-check (peka i DITT flöde):**
- [ ] Repo-URL fungerar i webbläsaren  
- [ ] Peka: vilket kommando var *välj*, vilket var *spara checkpoint*, vilket var *skicka* — och *varför* den ordningen  
- [ ] Peka i Commits: meddelandet går att förstå (inte `asdf`)  
- [ ] Du kan säga skillnaden Git vs GitHub i en mening  

**Ägarskap:**
- Utan AI: skriv kommandona själv.  
- Med AI: tillåtet som bollplank — spara prompten och **en mening** om vad du ändrade om AI gissade fel. Du ska kunna förklara varje kommando.

---

## Uppgift 2 — Andra checkpointen + Exam-regeln

**Mål:** Upprepa kedjan. Träna meddelanden. Koppla till Exam 1.

Många tänker nu: “En commit räcker för alltid.” Nej. En begriplig ändring = en ny checkpoint.

**Brief:** Lägg till en andra växt (eller en `footer` med “Uppdaterad 2026”) i samma `index.html`. Ingen ny teknik.

**Krav:**
1. Ändra → spara i VS Code → `status` → `add` → `commit` → `push`.  
2. Två commits syns på GitHub.  
3. I anteckningar: tre meningar — (a) vad en commit är, (b) varför push behövdes *igen*, (c) varför Exam 1 bryr sig om *vem* som syns i historiken.  
4. **Simulera par:** gör *en* av commitarna med meddelande i stil med `"Lade till footer — [ditt namn] och [påhittat namn]"`. (Du är ensam nu — poängen är formatet inför grupparbetet.)

**Klart-check (peka i DIN historik):**
- [ ] Två synliga commits  
- [ ] Minst ett meddelande med två namn (övning inför samma dator)  
- [ ] Anteckningarnas tre meningar är *dina* ord, inte copy-paste från teoriguiden  

**Ägarskap:** Samma regel som uppgift 1. Om AI skriver meddelandena åt dig: skriv om dem så *du* kan stå för dem.

---

## Uppgift 3 — Stretch (valfritt)

Lägg till en kort `README.md` i övningsrepot med tre rubriker: **Commit**, **Git vs GitHub**, **Synlig medverkan**. En mening under varje — målsvar-nivå. Commit + push.

**Klart-check:** Öppna README på GitHub. Kan du läsa meningarna högt utan att skämmas för att de är luddiga? Om ja: du har Exam-träning i mini-format.

---

## När du kört fast

1. `git status` — läs vad den faktiskt säger.  
2. Kör metoden högt: liten ändring? add? commit? push?  
3. Jämför med [01-teoriguide](./01-teoriguide.md) — särskilt tabellen och målsvaren.  
4. Autentisering / “failed to push”: det är inloggning, inte att kedjan är fel. Testa logga in på github.com och kör `push` igen.  
5. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
