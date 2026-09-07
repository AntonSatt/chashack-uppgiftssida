# Uppgifter: arbetslista

Arbetsfil för uppgiftsteamet (Anton, Victoria, Theo). Här lägger vi till, ändrar
och stryker uppgifter tills listan är spikad. Målet är klart senast avstämningen
måndag 7 september, då byggs listan in i `uppgiftssida.html`.

Så redigerar du: öppna filen på GitHub, pennan uppe till höger, ändra, committa.
En rad är en uppgift: bocka i rutan när den är spikad, radera raden om den stryks.
Mall för nya rader ligger längst ner.

**Läge just nu: 12 obligatoriska steg (145p) + 16 side quests (400p) = 545p möjliga.**

## Temat

Deltagarna bygger en **lagsida** i sitt eget repo, från tre tomma filer
(`index.html`, `style.css`, `script.js`) till en publicerad webbplats om laget.

- **Huvudspåret** är den obligatoriska kedjan. Lätt till medel. Varje steg bygger
  vidare på det förra och slutar i en färdig, deployad sida.
- **Side quests** är frivilliga extrauppdrag som plockas längs vägen. Medel till
  riktigt svår. De lägger till funktion, styling och skoj på samma sida.

**Vinstregel:** poängen avgör placeringen, men alla tolv steg i huvudspåret måste
vara godkända för att laget ska kunna vinna. Uppgiftssidan visar ett lag som inte
är klart med märket "Ej kvalificerad" och sorterar det under de kvalificerade.

Uppgifterna bor i `uppgiftssida.html` (arrayerna `MAIN` och `QUESTS`). Ändras en
rad här ska motsvarande post i den filen ändras också.

**Ledtrådar:** varje uppgift har en ledtråd som pekar ut rätt begrepp, tagg eller
funktion och vad man ska slå upp - men aldrig koden. Det finns med flit **inget
facit** någonstans. Ligger svaret en klick bort frågar lagen varken varandra
eller oss, och då tappar vi både samarbetet och lärandet. Kör ett lag fast är
det handledare på plats som gäller.

## Huvudspåret (12 steg, 145p, obligatoriskt)

- [x] **1. Ta ert repo** (10p, Lätt): Forka start-repot, gör det publikt, bjud in laget som collaborators, klona ner. Bevis: repo-URL som öppnas utan inloggning, med alla under Collaborators.
- [x] **2. Sidans skelett** (10p, Lätt): Fyll tomma index.html med doctype, html, head och body. Titeln blir lagnamnet. Bevis: index.html i repot, lagnamnet syns i fliken.
- [x] **3. Rubrik och pitch** (10p, Lätt): En h1 med lagnamnet och ett stycke som beskriver laget. Bevis: syns på sidan.
- [x] **4. Laget i en lista** (10p, Lätt): Punktlista med alla i laget. Bevis: alla namn syns på sidan.
- [x] **5. Koppla stilmallen** (10p, Lätt): Länka style.css, sätt egna färger och typsnitt. Bevis: sidan har egna färger, kodraderna i repot.
- [x] **6. Layout som håller ihop** (15p, Medel): Centrerad kolumn med max-width och luft runt. Bevis: innehållet ligger inte kant till kant.
- [x] **7. Lagets logga** (15p, Medel): Egen logga i repot, visad på sidan med beskrivande alt-text. Bevis: filen i repot, loggan syns, alt-texten finns.
- [x] **8. Liv i sidan** (15p, Medel): Koppla script.js och en knapp som gör något vid klick. Bevis: knappen fungerar, skärmdump eller GIF.
- [x] **9. Sidfot** (10p, Lätt): Footer med lagnamn och årtal, avgränsad med en linje. Bevis: syns längst ner på sidan.
- [x] **10. Publicera på nätet** (20p, Medel): GitHub Pages på repot. Bevis: publik URL som öppnas utan inloggning.
- [x] **11. Alla har committat** (10p, Lätt): Varje person minst en egen commit och push. Bevis: historiken visar flera namn.
- [x] **12. README som förklarar** (10p, Lätt): README med lagnamn, medlemmar och länk till live-sidan. Bevis: README.md i repot.

## Side quests (16 st, 400p, frivilliga)

### Styling (5 st, 100p)

- [x] **Egen favicon** (15p, Medel): Egen ikon i webbläsarfliken. Bevis: filen i repot, ikonen syns i fliken.
- [x] **Hover-effekter** (15p, Medel): Knappar och länkar reagerar på muspekaren. Bevis: skärmdump eller GIF.
- [x] **Egen färgpalett** (20p, Medel): Färgerna som CSS-variabler i :root, använda konsekvent. Bevis: variabler använda på minst tre ställen.
- [x] **Animerad entré** (25p, Svår): Rubrik eller logga glider in när sidan laddas. Bevis: GIF eller skärminspelning.
- [x] **Funkar i mobilen** (25p, Svår): Media query så sidan håller i mobilbredd. Bevis: skärmdump i smal vy där inget spricker.

### Funktion (7 st, 205p)

- [x] **Klickräknare** (20p, Medel): Knapp som räknar klick och visar siffran. Bevis: GIF eller skärmdump.
- [x] **Slumpat lagcitat** (20p, Medel): Knapp som slumpar fram citat ur en array. Bevis: texten byts vid klick.
- [x] **Mörkt och ljust läge** (30p, Svår): Knapp som växlar tema med classList.toggle. Bevis: GIF som visar båda lägena.
- [x] **Medlemskort ur en array** (30p, Svår): Medlemmarna byggs av JavaScript ur en array, inte handskriven HTML. Bevis: arrayen i script.js, korten på sidan.
- [x] **Nedräkning till redovisningen** (30p, Svår): Klocka som tickar i realtid med setInterval. Bevis: GIF som visar att den tickar.
- [x] **Sidan minns er** (35p, Riktigt svår): localStorage sparar ett val mellan besök. Bevis: GIF före och efter omladdning.
- [x] **Hämta data utifrån** (40p, Riktigt svår): fetch mot ett öppet API, med felhantering. Bevis: datan på sidan plus vad som händer när anropet misslyckas.

### Roligt (2 st, 55p)

- [x] **Easter egg** (25p, Svår): Hemlig tangent eller klick som utlöser något. Bevis: beskrivning i README plus GIF.
- [x] **Konfetti vid klick** (30p, Svår): Element skapade med JavaScript som regnar över sidan. Bevis: GIF eller skärminspelning.

### Samarbete (2 st, 40p)

- [x] **Lagbild på sidan** (15p, Medel): Riktig lagbild tagen på plats, publicerad på sidan. Bevis: bilden i repot och på sidan.
- [x] **Pull request med review** (25p, Svår): Branch, PR, review av lagkamrat, merge. Bevis: länk till merged PR med review.

## Öppna punkter

- Start-repot: uppgiftssidan länkar till `github.com/AntonSatt/chashack-starter`. Kontrollera att `index.html`, `style.css` och `script.js` ligger tomma där innan dagen.
- Vinstregeln behöver sägas muntligt vid uppstarten också, inte bara stå på sidan.
- Nedräkningen i side questen "Nedräkning till redovisningen" har måldatum 2026-09-11 15:00 i exempelkoden. Justera om tiden ändras.
- Serverversion med delad state (riktig granskningskö och leaderboard) byggs när uppgifterna är spikade. Just nu ligger allt i localStorage.

## Mall för ny uppgift

- [ ] **Titel** (10p, Lätt): Vad laget ska göra. Bevis: vad rättarlaget tittar efter.
