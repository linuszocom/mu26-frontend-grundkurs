# 📖 Så använder du detta GitHub-repo för dina studier

Välkommen till din **digitala kursbok** för kursen *Grundläggande Frontend-programmering*. 

Detta repository innehåller alla teoriguider, visuella modeller, kodövningar, AI-granskningsuppgifter och självtester du behöver under kursens gång.

---

## 🛑 Grundprincip: Du behöver INTE ladda ner detta repo

Ett vanligt missförstånd bland nya studenter är att man måste "klona", "forka" eller ladda ner hela detta repository till sin dator. **Det behöver du inte göra!**

* **Läs direkt i webbläsaren:** Detta repo är en webbsida. Du klickar bara på mapparna och filerna här på GitHub precis som i en digital bok.
* **Koda på din egen dator:** När du gör övningarna skapar du egna mappar och filer lokalt i VS Code på din dator. Det är din *egen* kod du sparar och senare versionshanterar i dina *egna* repon på GitHub.

---

## 🗺️ Hur materialet är uppbyggt (`01` till `05`)

Varje ämne och vecka i repot följer alltid samma fasta struktur med fem filer:

| Fil | Vad det är | Hur du använder den under din studietid |
| :--- | :--- | :--- |
| **`01-teoriguide.md`** | **Läroboken** | Läs igenom när du vill förstå bakgrunden, metaforerna och *varför* tekniken fungerar som den gör. Här hittar du även de **målsvar** du ska kunna förklara vid examination. |
| **`02-visuell.md`** | **Kartan & Trädet** | Diagram och flödesscheman för dig som lär dig bäst visuellt och vill se hur koden hänger ihop i trädstrukturer. |
| **`03-ovningar.md`** | **Verkstaden** | Praktiska uppgifter där du kodar själv från grunden. Innehåller konkreta *Klart-checkar* så du vet när du är i mål. |
| **`04-ai-traning.md`** | **Kvalitetsgranskningen** | Övningar där du granskar färdig eller AI-genererad kod, hittar fel/brister och skriver om koden till din egen. |
| **`05-sjalvtest.md`** | **Kunskapskontrollen** | Korta frågor med dolda facit under flikar. Svara först för dig själv – klicka fram facit efteråt för att se om du kan motivera svaren. |

---

## 🎯 Välj ditt studiespår (Hur pluggar du idag?)

Du anpassar hur du använder GitHub utifrån din studiesituation:

### 🟢 Spår 1: Du var med live på Teams-lektionen (13:00–16:00)
1. Öppna veckans mapp (t.ex. `vecka-35/`).
2. Gå direkt till **`03-ovningar.md`** och koda uppgifterna i VS Code.
3. Gör **`04-ai-traning.md`** för att stärka ditt kodägarskap.
4. Testa dig själv i **`05-sjalvtest.md`** utan att titta på facit först.
*(Använd `01-teoriguide.md` som uppslagsverk endast om du kör fast.)*

### 🟡 Spår 2: Du missade lektionen eller var sjuk (Ta ikapp-spåret)
1. Börja från start: Läs **`01-teoriguide.md`** från topp till tå.
2. Titta på **`02-visuell.md`** för att förstå mentalmodellen och strukturen.
3. Koda alla uppgifter i **`03-ovningar.md`**.
4. Gör **`04-ai-traning.md`** och stäm av i **`05-sjalvtest.md`**.

### 🟣 Spår 3: Du siktar på VG / Vill fördjupa dig (Stretch)
1. Gör de markerade *Stretch-uppgifterna* längst ner i `03-ovningar.md`.
2. Skriv en egen `README.md` i dina övningsmappar där du dokumenterar och motiverar dina arkitektur- och kodval.

---

## ⏰ Schemat för din studievecka (Heltid 40 h)

| Dag | Typ av dag | Rekommenderat upplägg |
| :--- | :--- | :--- |
| **Måndag** | **Lektionsdag** | **13:00–16:00:** Lektion live i Teams. <br>**Före/Efter:** Öppna repot och börja med `03-ovningar.md`. |
| **Tisdag** | **Självstudiedag** | **09:00–17:00:** Koda klart måndagens övningar, gör `04-ai-traning.md` och förbered nästa pass. |
| **Onsdag** | **Lektionsdag** | **13:00–16:00:** Lektion live i Teams. <br>**Före/Efter:** Koda övningarna för onsdagens ämne. |
| **Torsdag** | **Självstudiedag** | **09:00–17:00:** Repetition, fördjupning, ta ikapp och laboration i VS Code. |
| **Fredag** | **Lektionsdag** | **13:00–16:00:** Lektion live i Teams. <br>**Helgmål:** Slutför veckans `05-sjalvtest.md` och bocka av checklistan. |

---

## 🗺️ Kurskarta (Vecka för vecka)

### Block 1 — Grundläggande webbutveckling & Examination 1
* **[Vecka 35 — HTML, Git & CSS](./vecka-35/)**
  * Mån: [01-html-semantik](./vecka-35/01-html-semantik/) (Skelett, taggar & semantik)
  * Ons: [02-git-github](./vecka-35/02-git-github/) (Versionshantering, repo, commit, push)
  * Fre: [03-css-box-model](./vecka-35/03-css-box-model/) (style.css, selektorer & Box Model)
* **[Vecka 36 — Layout & Examination 1-start](./vecka-36/)**
  * Mån: Hero-sektion & CSS-ärv
  * Ons: Flexbox (Highlights-kort) & kodfeedback
  * Fre: CSS Grid (Schema), Nav/Footer/Media Queries & Start av Exam 1
* **Vecka 37 — Handledning & Examination 1 (Eventsidan)**
  * Grupparbete med Eventsidan. Deadline: Fredag v37.

---

### Block 2 — JavaScript, React & Examination 2
* **Vecka 38 — JavaScript-grunder & React-intro**
  * Mån: JS-syntax (variabler, datatyper & funktioner)
  * Ons: DOM vs React & projektstart med Vite
  * Fre: Komponenter, JSX & props
* **Vecka 39 — State & Dynamiska listor**
  * Mån: `useState` & re-render
  * Ons: Eventhantering (`onChange`, `onClick`) & lägga till todos
  * Fre: `.map()` och `.filter()` för att rendera listor
* **Vecka 40 — Applogik & Examination 2-start**
  * Mån: Markera som klar & ta bort uppgifter (immutabel state)
  * Ons: CSS i React & visuell feedback (klar/oklar)
  * Fre: AI-kodgranskning & Start av Examination 2
* **Vecka 41 — Handledning & Examination 2 (ToDo App)**
  * Individuellt arbete, inlämning och muntlig redovisning i VS Code.

---

## 🤖 AI som studiepartner (Real Talk)

Det är tillåtet och bra att använda AI (som ChatGPT eller Google Gemini) som ett bollplank under dina självstudier:

* **Använd AI som hjälplärare:** Fråga *"Vad betyder den här felkoden?"* eller *"Förklara skillnaden mellan padding och margin i min kod"*.
* **Kopiera aldrig blint:** Du måste alltid förstå varje enskild rad du klistrar in i ditt projekt. Kan du inte förklara koden muntligt under examinationen räknas det som bristande ägarskap och kan leda till underkänt betyg.
* **Styr AI:n – låt inte AI:n styra dig:** Ju mer du tränar med hjälp av detta studentmaterial, desto tryggare blir du i att veta hur lösningen ska se ut.
