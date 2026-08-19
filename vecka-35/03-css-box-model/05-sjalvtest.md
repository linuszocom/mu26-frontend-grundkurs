# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad är skillnaden mellan HTML och CSS på en mening?  
2. Varför en separat `style.css` + `link` i stället för `style=""` överallt?  
3. Vad är en **selektor**?  
4. När elementselektor vs klassselektor? (metoden)  
5. Lista Box Model **inifrån och ut** (gärna matlådan).  
6. Texten sitter klistrad mot en ram. Padding eller margin — och varför?  
7. Två block sitter klistrade mot varandra. Vilken ratt?  
8. Peka i *din* kod (Kajen, lapp eller AI-övning): en selektor och tre box-delar med **varför** (inte “det såg bra ut”).

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. **HTML** = struktur/betydelse. **CSS** = utseende (färg, typografi, spacing).  
2. En fil för utseende, återanvändbar, HTML hålls semantisk. `link` kopplar dem. Inline blir rörigt att äga.  
3. En selektor pekar ut **vilka** element en regel gäller.  
4. Alla av en tagg → elementselektor. Bara vissa → `class` + `.klassnamn`.  
5. Content (maten) → padding (luft i facket) → border (vägg) → margin (avstånd till nästa låda).  
6. **Padding** — luft *inuti* lådan. Margin flyttar hela lådan, inte texten inuti.  
7. **Margin** — luft *mellan* lådor.  
8. Subjektivt — rimligt om du kopplar egenskap → lager / selektor → vilka element. Fel om “AI skrev det” eller Flex som förklaring.

</details>

---

## Klart för paketet?

Om dina svar ligger nära facit, övningarna är gjorda, och du kan peka i egen CSS:

- [ ] Målsvar CSS vs HTML — egna ord, högt  
- [ ] Målsvar selektor + metod — egna ord, högt  
- [ ] Målsvar Box Model — egna ord, högt  
- [ ] Padding vs margin pekad i din kod  

Då har du landat CSS-grunden. Nästa publicerade del: CSS-ärv och Hero.
