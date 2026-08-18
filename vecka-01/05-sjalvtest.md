# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad är skillnaden mellan HTML och CSS på en mening?  
2. Vad är skillnaden mellan `head` och `header`? (Tänk butiken: följesedel vs namnskylt.)  
3. Vad betyder **semantisk HTML**? (Sikta mot Exam README-nivå — målsvaret.)  
4. Varför är det sämre att bygga hela sidan med bara `div`?  
5. Du har en bit text som är sidans viktigaste rubrik. Vilken tagg — och varför inte `p`?  
6. Beskriv metoden i tre steg när du är osäker på tagg.  
7. Vad ska en `img` alltid ha förutom `src` — och varför?  
8. Peka i *din* kod (café, podd eller bokklubb): nämn tre taggar och **varför** du valde dem (inte “för att det såg bra ut”).

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. **HTML** = struktur/betydelse; **CSS** = utseende (kommer mer senare i kursen).  
2. **`head`** = metadata *om* dokumentet (title, charset) — följesedeln. **`header`** = synligt sidhuvud i `body` — namnskylten. De är INTE samma sak.  
3. Semantisk HTML = välja taggar efter innehållets *betydelse* (t.ex. `header` för sidhuvud) så strukturen blir tydlig för människor och verktyg — inte bara `div` överallt.  
4. `div` saknar betydelse; koden blir svårare att läsa, underhålla och förstå för verktyg/andra — och du kan inte motivera den i Exam.  
5. **`h1`** — det är huvudrubrik. `p` är brödtext, inte sidans huvudämne.  
6. (1) Vad *är* innehållet? (2) Matcha tagg med samma betydelse. (3) Inte gissa “låda”/`div` — fråga hellre.  
7. **`alt`** — textalternativ om bilden inte syns / för skärmläsare. Utan `alt` saknas betydelsen för den som inte ser bilden.  
8. Subjektivt — rimligt om du kopplar tagg → betydelse (metodstegen). Fel om svaret bara är “AI skrev det” eller “det såg bra ut”.

</details>

---

## Klart för veckan?

Om dina svar ligger nära facit, övningarna är gjorda, och du kan peka i egen kod:

- [ ] Målsvar semantik — egna ord, högt  
- [ ] Målsvar metod — egna ord, högt  
- [ ] Tre taggar i din kod med *varför*

Då har du landat veckans mål. Nästa veckomaterial: Git & CSS — se `studentmaterial/vecka-02/` när det finns.
