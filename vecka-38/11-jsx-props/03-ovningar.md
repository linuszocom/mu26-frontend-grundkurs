# 03 — Övningar

**Omfång det här paketet:** Funktionskomponenter, JSX, props, **statisk** lista/kort. Ingen `useState`. Ingen fungerande lägg-till. Inte festival/eventsida. **Examination 2 (ToDo)** kommer senare — bygg inte den appen här.

Jobba i **ditt** Vite-projekt från förra paketet (eller skapa ett nytt med samma kommando om det saknas).

AI får föreslå JSX. Du måste kunna **peka** var sedeln skrivs och var den läses.

---

## Uppgift 1 — Växtkort med följesedel

**Mål:** En kloss. Minst två följesedlar. Skylten använder props.

**Problem först:** Två `<article>` med basilika/mynta utskrivna för hand i `App` (som i teoriguiden). Fungerar — tills du ändrar strukturen.

**Krav:**
1. Fil eller samma fil: funktion `Vaxtkort` (stor bokstav).  
2. Props minst `namn` och `ljus` (strängar). Visa dem med `{props.namn}` (eller motsvarande).  
3. I `App`: minst **tre** kort (t.ex. basilika, mynta, chili) — tre `<Vaxtkort … />`, inte tre kopierade article-block.  
4. Ett rot-element per return. Inget `useState`.  
5. Spara och se tre olika skyltar i webbläsaren.

**Klart-check (peka i DIN kod):**
- [ ] Peka på **skrivningen** av en prop i `App`  
- [ ] Peka på **läsningen** i `Vaxtkort`  
- [ ] Säg *varför* tre klossar slår tre copy-paste-article  
- [ ] Ingen klicklogik som ändrar listan  

**Ägarskap:** Utan AI: skriv själv. Med AI: stryk `useState` och `.map` om de smög in — du ska kunna förklara varje prop.

---

## Uppgift 2 — Statisk lista (samma mönster)

**Mål:** Se att “rad i en lista” är samma idé som kortet — fortfarande stilla.

**Brief:** Under korten: en `<ul>` med tre `<li>` *eller* tre små komponenter `Vattning` med prop `text` (t.ex. “Basilika — mån”, “Mynta — ons”). Statiskt. Ingen checkbox som funkar.

**Krav:**
1. Minst tre rader, olika text via props *eller* tre `<Vattning text="…" />`.  
2. En mening i anteckningar: det här är strukturen — listan *lever* när state kommer (nästa paket), inte nu.

**Klart-check:**
- [ ] Du kan peka på props även på den “tråkiga” raden  
- [ ] Anteckningen blandar inte in Exam 2-bygge  

**Ägarskap:** Samma regel som uppgift 1.

---

## Uppgift 3 — Stretch (valfritt)

`Receptkort` med props `titel`, `tid`, `portioner` — minst två recept (t.ex. havregröt, pasta). Inte festival. Extra prop får finnas om du kan förklara den. Fortfarande ingen state.

**Klart-check:** Två följesedlar, en kloss, skylten visar alla tre fält.

---

## När du kört fast

1. Vit skärm / röd overlay: ofta stor bokstav, ostängd tagg, eller flera rötter utan wrapper.  
2. Skylten visar inget: glömde `{props.namn}` eller skrev fel prop-namn (`name` vs `namn`).  
3. Jämför med [01-teoriguide](./01-teoriguide.md).  
4. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
