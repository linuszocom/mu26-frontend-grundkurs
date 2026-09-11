# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad är en **variabel**, med burk-bilden?  
2. När väljer du `const` och när `let`?  
3. Ge ett exempel var på **sträng**, **number** och **boolean**.  
4. Vad är skillnaden mellan att *deklarera* en funktion och att *anropa* den?  
5. Vad gör `console.log` — och vad gör den **inte** i det här paketet?  
6. Beskriv metoden när du ska räkna ut något i kod.  
7. Vad returnerar `"5" === 5` jämfört med `"5" == 5`?  
   - a) båda `true`  
   - b) `false` och `true`  
   - c) båda `false`  
8. `lista = ["a", "b"]`. Vad skrivs ut av `lista[0]`?  
9. Du har `{ namn: "Ada" }` i burken `person`. Hur läser du ut `"Ada"`?  
10. `if (villkor) { console.log("ja"); }` — villkoret är `false`, ingen `else`. Vad händer?  
11. Vad är skillnaden mellan en **array** och ett **objekt** i en mening?  
12. Vad gör `for...of` över en array — och vad är den **inte** i det här paketet?  
13. Peka i *din* övningskod: en burk, ett receptkort, en `if` med `===`, en hylla, ett fält med punkt, en `for...of` — och **varför**.  
14. *(Känna igen, inte krav.)* Vad är en arrow (`=>`) på en mening?

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. Namngiven burk: lappen är namnet, inuti ligger värdet så du slipper skriva om det överallt.  
2. `const` när namnet inte ska peka på något nytt. `let` när du tilldelar om (t.ex. summa).  
3. t.ex. `"Bulle"`, `12`, `false`.  
4. Deklarera = skriva receptkortet. Anropa = `namn(...)` så stegen körs. Utan anrop: inget.  
5. Skriver värdet till **konsolen** så du ser det. Den ritar inte sidan (det vore DOM — inte här).  
6. Vad ska hända? Vilken data? Vilka steg (recept / `if` / `for...of`)? Testa med `console.log`.  
7. **b)** `"5" === 5` är `false` (text vs tal). `"5" == 5` är `true` (JS gissar). I din kod: `===`.  
8. `"a"` — första facket heter `0`.  
9. Punktnotation: `person.namn`.  
10. Inget loggas. `if`-blocket hoppas över. Utan `else` finns ingen andra dörr — programmet fortsätter efter `if`.  
11. Array = numrerad hylla (`[0]`, `.length`). Objekt = en rad med namngivna fält (`todo.text`).  
12. Går igenom hyllan en sak i taget och låter dig t.ex. logga. INTE tre handskrivna index-rader. INTE array-metoder.  
13. Subjektivt — rimligt om du kopplar rad → effekt (dörr, hylla, punkt). Fel om “AI skrev det” utan pekning.  
14. Samma idé som `function`, kortare stavning. Inte ny logik. Inte krav att skriva här.

</details>

---

## Klart för paketet?

Om dina svar ligger nära facit, övningarna körts i konsolen, och du kan peka i egen kod:

- [ ] Målsvar variabel — egna ord, högt  
- [ ] Målsvar funktion — egna ord, högt  
- [ ] Målsvar `if` / `===` — egna ord, högt  
- [ ] Målsvar array / objekt / `for...of` — egna ord, högt  
- [ ] Målsvar metod — egna ord, högt  
- [ ] `const` / `let` pekade  

Då har du landat JS-syntax. Nästa paket: [10-react-vite](../10-react-vite/). **Examination 2** kommer senare.
