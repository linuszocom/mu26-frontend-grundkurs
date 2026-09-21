# 04 — AI-träning: map, filter & ägarskap

AI kan loopa en array på sekunder. Det betyder inte att *du* äger raderna. Här tränar du: **se vad som är svagt, ändra, förklara**.

Det är inte magi. Det är stämpel, streckkod och sil.

---

## Scenario — problem först

Du ber AI: *“Visa min lista i React och ta bort namn som inte ska med.”*  
Du får tillbaka något i stil med:

```jsx
function App() {
  const [names, setNames] = useState(["Kim", "Alex", "Sam"]);

  function render() {
    names.forEach((n, i) => {
      document.body.innerHTML += "<p>" + n + "</p>";
    });
  }

  function drop() {
    names.splice(1, 1);
    setNames(names);
  }

  return (
    <main>
      {names.map((n, i) => (
        <li>{n}</li>
      ))}
      <button onClick={drop}>fixa</button>
      <button onClick={render}>rita</button>
    </main>
  );
}
```

Det *kan* råka rita något. Det är svagt mot det här paketet:

- **`forEach` + `innerHTML`** = du skriver DOM för hand. Map i JSX är metoden.  
- **Ingen `key`.**  
- **`splice` + samma referens** till `setNames` — muterad låda.  
- En “fixa”-knapp är ta-bort-UI du **inte** behöver färdigställa här.  
- `map` till `<li>` utan `<ul>` är slarvigt, men sekundärt mot key/forEach/splice.

**Vad du tränar:** Feedback + map/filter *du* äger.  
**Varför:** Exam 2 visar listan med map; filter är förberedelse. Muntligt: peka och förklara.  
**Vad det INTE är:** “AI loopade, alltså är det ES6.”

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en egen prompt (eller jobba mot snutten) där du ber om att rendera en namnlista i React och sila bort ett namn. Spara prompten.

### Steg 2 — Granska (checklist)
Kryssa mot koden du fick:

- [ ] JSX använder `.map()` som **returnerar** element — inte `forEach`/`innerHTML`?  
- [ ] Finns `key` som inte är index (om listan kan ändras)?  
- [ ] Filter/ny array — eller `splice` / mutera?  
- [ ] Full delete-UI du inte ska äga än?  
- [ ] Kan du förklara varje rad muntligt?

Skriv **minst tre** konkreta feedback-punkter i formen:  
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Skriv om till en **ren version du äger** i film- eller workshop-övningen från [03](./03-ovningar.md): map + key, filter som *visad* ny lista (inte splice). Kort `MAP-FILTER.md`: tre rader (map / key / filter).

### Steg 4 — Reflektion (3 meningar)
Skriv i anteckningar eller samma fil:

1. Vad var fel eller svagt i AI-förslaget (eller snutten)?  
2. Vad ändrade du?  
3. Varför är map vs filter vs splice viktigt inför Exam 2 (visa listan / senare ta bort)?

---

## Klart-check (peka i DIN kod)

- [ ] Tre FEEDBACK-rader sparade  
- [ ] Peka på `map` och `key` och säg *varför*  
- [ ] Peka på något du *tog bort* från AI — varför behövdes det inte / var det fel?  
- [ ] Reflektionens tre meningar klara  

---

## Facit-riktning (titta efter du granskat själv)

Exempel på giltig feedback (dina egna ord får skilja sig):

- `FEEDBACK: forEach + innerHTML → map i JSX som returnerar <li>.`  
- `FEEDBACK: saknar key → unikt key per syskon, inte index om listan växer.`  
- `FEEDBACK: splice på names → filter till ny array, visa den.`  
- `FEEDBACK: delete-knapp “fixa” → stryk; sil-övning räcker i det här paketet.`

**Målsvar (säg högt / skriv i README) — ägarskap:**  
*“Jag tar emot AI-förslag som utkast, granskar rad för rad, och behåller bara det jag kan förklara.”*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
