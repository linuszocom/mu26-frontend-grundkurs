# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad är skillnaden mellan Git och GitHub på en mening?  
2. Vad är en **commit**?  
3. Vad gör `git add` som `git commit` *inte* gör?  
4. Du har committat men github.com är tomt. Vilket steg saknas — och varför räcker inte VS Code-Spara?  
5. Beskriv metoden när du tvekar: ska jag spara i Git nu?  
6. Varför ska commits visa **vem** som jobbat? (Exam 1)  
7. Ni sitter två vid samma dator. Hur gör ni så båda syns?  
8. Peka i *ditt* repo: nämn tre steg du körde (add/commit/push eller status) och **varför** — inte “AI sa åt mig”.

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. **Git** = historik/checkpoints på din dator. **GitHub** = kopian på nätet där andra och examinationen kan se den.  
2. En commit = sparad ögonblicksbild + meddelande — en punkt i historiken.  
3. **`add`** = välj vilka filer som ska med i *nästa* ögonblicksbild. **`commit`** = spara den bilden. Add laddar inte upp.  
4. **`git push`**. Spara i editorn = fil på disk, ingen GitHub-kopia.  
5. (1) Liten, begriplig ändring? (2) `git add` de filerna. (3) `git commit -m "…"` sedan `git push`.  
6. Exam 1: gemensamt repo där det ska synas att **alla** kodat — inte bara att zip:en “finns”.  
7. Skriv bådas namn i commit-meddelandet (den inloggade Git-användaren är annars ensam författare).  
8. Subjektivt — rimligt om du kopplar kommando → effekt. Fel om svaret bara är “AI skrev det” eller “jag klickade runt”.

</details>

---

## Klart för paketet?

Om dina svar ligger nära facit, övningarna är gjorda, och du kan peka i eget repo:

- [ ] Målsvar commit — egna ord, högt  
- [ ] Målsvar synlig medverkan — egna ord, högt  
- [ ] Målsvar metod — egna ord, högt  
- [ ] Add / commit / push pekade i ditt flöde  

Då har du landat Git-målet. Nästa paket: [03-css-box-model](../03-css-box-model/).
