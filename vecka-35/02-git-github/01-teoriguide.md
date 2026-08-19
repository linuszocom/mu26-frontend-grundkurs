# 01 — Teoriguide: Git & GitHub

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när du bara trycker Spara i editorn — sedan bygger vi upp hur du tar en riktig ögonblicksbild och får den till GitHub. Det är inte magi. Det är en metod.

---

## Problemet först — “jag sparade ju”

Många tänker nu: “Filen ligger på min dator. Det räcker.” Andas.

**Dåligt läge:** Du har en `index.html` i VS Code. Du sparar. Datorn kraschar, du byter laptop, eller en gruppkompis ska lämna in — och på GitHub finns **ingenting**. Eller: tre personer har kodat, men historiken visar bara ett namn.

Det är två olika problem:

1. **Ingen ögonblicksbild** — bara “senaste filen på disken”.  
2. **Ingen synlig medverkan** — Exam 1 kräver att det syns *vem* som kodat.

Git löser (1). GitHub + ärliga commit-meddelanden löser (2).

---

## Git vs GitHub — checkpoint och delad server

**Metafor:** Tänk ett spel. **Git** är *checkpoint-systemet på din dator* — du sparar en punkt du kan peka på: “här funkade sidan”. **GitHub** är *den delade servern* där samma checkpoints syns för andra, och dit du lämnar inlämningslänken.

**Vad det är:** Git = versionshantering lokalt. GitHub = remote (kopian på nätet).  
**Varför det finns:** Så du inte bara har “senaste filen”, och så gruppen (och du själv om tre veckor) kan se historiken.  
**Om det saknas / vad det INTE är:** Git är INTE GitHub. Utan push finns checkpointen bara hos dig. GitHub är INTE “spara i VS Code”. Det är INTE branches, merge eller pull requests i det här paketet — bara repo, add, commit, push.

**Målsvar (säg högt / skriv i README):** *“Git sparar historiken på min dator. GitHub är kopian på nätet där andra (och examinationen) kan se den.”*

---

## Repository — spelet måste ha en sparfil

**Vad det är:** Ett **repo** (repository) = projektet under Git: mappen + historiken.  
**Varför det finns:** Annars vet Git inte *vilket* projekt du sparar i.  
**Om det saknas:** `not a git repository` — du står i fel mapp, eller har inte kopplat mappen till Git än. Det är INTE att Git “är trasigt”.

Två vanliga sätt att få ett repo på datorn:

1. Skapa tomt repo på GitHub → **`git clone`** URL:en (hämtar mappen + kopplingen dit).  
2. (Senare, om du redan har en mapp) `git init` + koppla remote — du behöver inte det i första övningen.

**Identitet:** `git config user.name` och `user.email` = namnet/mejlen som syns på *dina* checkpoints. Utan dem blir historiken anonym eller varnande. Det är INTE inloggningen till github.com i webbläsaren.

---

## Kedjan — tre knappar, inte en

Många tänker: “Jag vill bara få upp det på GitHub.” Stopp. Det är tre steg med olika jobb.

| Steg | Kommando | Vad det är (+ bild) | Varför | Om saknas / INTE |
|------|----------|---------------------|--------|------------------|
| Kolla | `git status` | Kartan: vad är nytt, vad är valt | Du gissar inte | INTE samma sak som push |
| Välj | `git add …` | Markera *vilka* filer som ska med i nästa checkpoint | Du styr innehållet | INTE att spara ögonblicksbilden än |
| Spara | `git commit -m "…"` | Skriv checkpoint + lapp (meddelande) | Historiken ska gå att läsa | Fortfarande **lokalt** — INTE GitHub |
| Publicera | `git push` | Skicka sparade checkpoints till GitHub | Annars syns inget på github.com | INTE samma sak som Spara i VS Code |

**Problem först:** Bara `commit` utan `add` → ofta “nothing to commit”. Bara `add` utan `commit` → filerna är valda men ingen punkt i historiken. Bara `commit` utan `push` → du har checkpoints, men GitHub (och gruppen) ser dem inte.

**Målsvar (säg högt / skriv i README) — commit:**  
*“En commit är en sparad ögonblicksbild av projektet med ett meddelande om vad som ändrats. Den blir en punkt i historiken.”*

---

## Metod — när du tvekar “ska jag spara i Git nu?”

Det är inte magi. Tre frågor:

1. **Har jag en liten, begriplig ändring?** (en grej du kan beskriva i en mening — inte allt på en gång)  
2. **`git add` just de filerna.** Kolla `git status`.  
3. **`git commit -m "tydligt meddelande"`.** Sedan **`git push`** så GitHub får dem.

Meddelandet: konkret (“Lade till index.html med h1”), inte `asdf`.  
**Par på samma dator:** skriv namnen i meddelandet, t.ex. `"Fixade header — Kim och Alex"`. Annars syns bara den som är inloggad i Git.

**Vad metoden är:** Ett sätt att spara utan att dumpa allt eller glömma push.  
**Varför den finns:** Exam 1 bedömer synlig historik, inte bara att filerna “finns någonstans”.  
**Om den saknas:** Du pushar aldrig, eller gör en enda jättecommit som ingen kan läsa.

**Målsvar (säg högt / skriv i README) — metod:**  
*“Har jag en liten, begriplig ändring? Då: git add de filerna, git commit med tydligt meddelande (+ namn om par), sedan git push så GitHub får dem.”*

---

## Synlig medverkan — Exam 1-kravet

**Vad det är:** I GitHub **Commits** ska det synas att **alla i gruppen** har kodat.  
**Varför det finns:** Gemensamt repo ≠ en person som laddar upp allas zip.  
**Om det saknas / vad det INTE är:** Det räcker INTE att “vi satt tillsammans”. Utan commits (eller namn i meddelandet vid gemensam dator) ser det ut som att bara en gjort jobbet.

**Målsvar (säg högt / skriv i README) — synlig medverkan:**  
*“I Exam 1 ska det synas i GitHub-historiken att alla i gruppen kodat. Jobbar ni på samma dator skriver ni namnen i commit-meddelandet — annars syns bara den som är inloggad i Git.”*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| Spara i VS Code = versionshanterat | Spara = fil på disk. Git = checkpoint. GitHub = efter push |
| Git och GitHub är samma sak | Git lokalt, GitHub på nätet |
| `git add` = uppladdning | Add = välj. Commit = spara. Push = skicka |
| Meddelandet `update` / `asdf` | Skriv vad som ändrades, så historiken går att läsa |
| En person pushar hela gruppens kod | Alla ska synas — eller namn i meddelandet vid samma dator |
| Kör Git i fel mapp | `cd` in i projektmappen först. `status` när du är osäker |
| Branches, merge, pull request “för att göra rätt” | Inte i det här paketet. Repo + kedjan räcker |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad är en commit? (sikta på målsvaret)  
2. Skillnad Git vs GitHub i en mening  
3. Metodens tre steg + var `push` sitter  
4. Varför synlig medverkan (Exam 1)

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna.
