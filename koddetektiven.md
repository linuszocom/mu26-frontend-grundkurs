# Koddetektiven: Så bryter du ner och förstår kod

En enkel metod för dig som är i början av din utvecklarresa. Använd den här guiden när du tittar på kod du inte skrivit själv – oavsett om källan är en kurskamrat, dokumentation eller ett förslag från en AI.

---

## Steg 1: Helikopterblicken – Vad vill vi ska hända?

Innan du ens tittar på variabelnamn, måsvingar `{}` eller metoder: ta ett steg tillbaka från skärmen.

Formulera målet på vanlig svenska med en enda mening:
* *"Vad är den här funktionens uppgift i appen?"*
* *Exempel:* *"När användaren klickar på ta bort-knappen vill jag att just den valda raden ska raderas och försvinna från skärmen."*

Den här meningen blir ditt **facit**. Resten av analysen går bara ut på att ta reda på om koden faktiskt gör det du nyss bestämde.

---

## Steg 2: Peka med fingret – Följ datans resa rad för rad

Nu öppnar du koden. Läs den uppifrån och ner, precis som en dator gör, och ställ tre enkla frågor längs vägen:

1. **Vad åker in?**
   * Tar funktionen emot något utifrån när den anropas? (Ett ID-nummer, lite text från ett formulär eller en hel lista?)
2. **Vad händer med datan på vägen?**
   * Skapar koden en ny kopia av datan, eller försöker den ändra direkt i befintligt minne?
3. **Vad skickas ut / Vad visas på skärmen?**
   * Returneras ett värde, eller uppdateras appens state så att vyn ritas om på skärmen?

---

## Steg 3: Kontrollfrågan – Matchar koden din mening?

Jämför vad koden faktiskt gjorde med meningen du skrev i **Steg 1**:
* Löser koden uppgiften på ett säkert sätt?
* Eller uppstår ett sidoproblem (t.ex. att koden klipper direkt i en array istället för att skapa en ny lista, så att appen missar att uppdatera skärmen)?

---

## Så formulerar du enkel feedback (på 2 meningar)

När du ska ge feedback till en kamrat eller förklara en AI-ändring i din `README.md` behöver du inte skriva en uppsats. Använd denna enkla mall:

> **Mallen:**  
> 1. *"Koden försöker att `[vad koden vill göra]`, men problemet är att `[vad som blir fel]`."*  
> 2. *"Ett bättre sätt är att `[hur du löser det enklare/bättre]`."*

### Exempel på hur det kan se ut:
> *"Koden försöker ta bort en uppgift med `.splice()`, men problemet är att den ändrar direkt i befintligt state så att React inte upptäcker ändringen. Ett bättre sätt är att använda `.filter()` som skapar en helt ny lista."*

⬅️ [Tillbaka till uppgiftsbeskrivningen](ToDoAppen.md)
