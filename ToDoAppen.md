# Individuell examination: ToDo-appen

Du ska på egen hand bygga en fungerande och interaktiv ToDo-applikation i React. Projektet ska lämnas in via GitHub och redovisas muntligt via en kort video.

Målet är att uppgifterna finns i state och att sidan uppdateras när användaren lägger till, markerar klar eller tar bort. Gränssnittet ska vara lätt att förstå.

---

### Förutsättningar
* **Teknikstack:** Appen byggs med React och valfri styling (vanlig CSS räcker hela vägen till VG).
* **Fil- och kodstruktur:** All kod (komponenter, funktioner, variabler) namnges på engelska. Texter i gränssnittet får vara på svenska.
* **Flexibilitet:** Kraven nedan beskriver vad appen **minst** ska klara av. Du är fri att lägga till fler funktioner (t.ex. filter för klara/ogjorda eller redigering) om du vill bygga vidare.
* **Behöver du stöd?** Kör du fast på hur kraven ska lösas i React, ta hjälp under schemalagd handledningstid för att bolla lösningar innan inlämning.

---

### Kravspecifikation (Vad appen minst ska klara)

#### 1. Hantera uppgifter
Varje uppgift representerar en post i listan med en text och en status (klar/ogjord):
* **Skapa uppgift:** Användaren ska kunna skriva in en text i ett inputfält och lägga till den i listan via en knapp eller Enter-tangenten.
* **Indatavalidering:** Tomma uppgifter (eller fält som bara innehåller mellanslag) ska inte gå att lägga till.
* **Markera som klar:** Användaren ska kunna ändra status på en specifik uppgift från ogjord till klar (och gärna tillbaka).
* **Visuell åtskillnad:** Gränssnittet ska tydligt visa skillnad på vad som är klart och vad som är ogjort (t.ex. genomstruken text, en bock eller dämpad färg).
* **Ta bort:** Varje uppgift ska ha en radera-knapp som tar bort enbart den valda uppgiften medan resten av listan förblir intakt.

#### 2. Reaktivitet och Gränssnitt
* **Dynamisk rendering:** Listan ska uppdateras och ritas ut direkt på skärmen så fort data ändras, utan att webbläsarsidan laddas om.
* **Layout:** Användaren ska mötas av ett städat och begripligt gränssnitt där knappar, textfält och listor är lätta att använda.

---

### GitHub & Versionshantering
* Skapa ett **eget, nytt och publikt GitHub-repo.**
* Gör **minst 5 commits** som visar hur applikationen byggts upp steg för steg under utvecklingen.
* Projektet ska vara helt eget arbete.

---

### Skriv i `README.md`
Besvara följande delar kort med egna ord i ditt repo:

#### 1. Frågor om koden (ca 2–4 meningar per fråga)
1. **State-hantering:** Hur håller din app reda på vilka uppgifter som finns och om de är klara? Vad händer med gränssnittet när datan uppdateras?
2. **Oföränderlighet (Immutability):** Varför får man inte ändra en befintlig array direkt med t.ex. `.push()` i React? Hur gör du istället när du lägger till eller tar bort en uppgift?

#### 2. Kodgranskning
Nedan är en funktion från en annan utvecklares lösning. Klistra inte in den i din app, utan förklara i din README vad som är felaktigt med koden i ett React-sammanhang och hur du skulle skriva om den för att den ska bli korrekt:
```javascript
function addTodo(todos, text) {
  todos.push(text);
  return todos;
}
```

🔗 [Koddetektiven](koddetektiven.md) - Läs denna innan du gör din kodgranskning.

#### 3. Problemlösning & Reflektion (3–5 meningar)
Hur gjorde du när du körde fast eller stötte på ett problem? Om du använde verktyg som AI, Google eller React-dokumentationen: ge ett konkret exempel på hur du tog hjälp för att förstå och lösa problemet själv.

---

### Muntlig redovisning (Video via Teams)
Spela in en kort skärminspelning (**3–5 minuter**) via Teams där du delar VS Code och din webbläsare:
1. **Kort demo (ca 30–60 sek):** Visa snabbt i webbläsaren att appen fungerar (lägg till, bocka av och ta bort).
2. **Källkoden:** Öppna källkoden i VS Code. Välj ut **2–3 funktioner/händelser** (t.ex. hur en uppgift skapas, hur status uppdateras eller hur en raderas) och förklara vad som händer med markören pekande på koden.

🔗 [Instruktion för muntlig redovisning](instruktion_redovisning.md)

---

### Inlämning
Inlämningen sker via moodle, under vecka 41 har ni länk till inlämningssidan, där lämnar ni en länk (url) till erat repo.
Länk till den muntliga redovisningen ska ligga i eran README i ert repo.

Senast inlämningsdag är Fredag 9:e oktober.

---

### Betygskriterier

#### Godkänt (G)
* Appen uppfyller kraven i specifikationen och fungerar utan krascher.
* Repot är publikt med minst 5 commits och en ifylld `README.md`.
* **Muntligt (Vad koden gör):** Du visar ocj förklarar i din video hur dina utvalda funktioner hänger ihop.

#### Väl godkänt (VG)
* Alla krav för Godkänt (G) är uppfyllda.
* **I koden:** Appen är uppdelad i **minst två egna återanvändbara komponenter** (utöver `App`) som kommunicerar via props (t.ex. separat komponent för inmatning och för enskild uppgift).
* **Muntligt (Varför och bakom kulisserna):** Du förklarar hur Reacts reaktivitet fungerar under huven. Du förklarar varför kopior av state skapas vid uppdateringar och hur data flödar mellan dina komponenter.

---

### Snabbcheck innan du lämnar in
- [ ] Det går att lägga till uppgifter (tomma rader stoppas).
- [ ] Det går att markera som klar med synlig skillnad.
- [ ] En enskild uppgift kan raderas utan att resten av listan påverkas.
- [ ] Sidan uppdateras utan att webbläsaren laddas om.
- [ ] Minst 5 commits finns på GitHub.
- [ ] `README.md` är ifylld (state-frågor, kodgranskning och reflektion).
- [ ] Videolänken (Teams/OneDrive) är inlagd, testad och inställd så att läraren har behörighet att titta.
