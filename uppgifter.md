# Uppgifter: arbetslista

Arbetsfil för uppgiftsteamet (Anton, Victoria, Theo). Här lägger vi till, ändrar
och stryker uppgifter tills listan är spikad. Målet är klart senast avstämningen
måndag 7 september, då byggs listan in i `uppgiftssida.html`.

Så redigerar du: öppna filen på GitHub, pennan uppe till höger, ändra, committa.
En rad är en uppgift: bocka i rutan när den är spikad, radera raden om den stryks.
Mall för nya rader ligger längst ner.

**Läge just nu: 12 obligatoriska steg (145p) + 30 side quests (750p) = 895p möjliga.**

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

- [x] **1. Skapa ert repo** (10p, Lätt): Forka start-repot till laget, gör kopian publik och bjud in alla i laget som collaborators. Klona sen ner det och öppna mappen i VS Code. Bevis: Repo-URL som öppnas i ett privat fönster utan inloggning, med alla i laget under Collaborators.
- [x] **2. Sidans skelett** (10p, Lätt): Fyll den tomma index.html med grunden som varje webbsida behöver. Titeln i fliken ska vara lagets namn. Bevis: index.html i repot, och lagnamnet syns i webbläsarens flik när sidan öppnas.
- [x] **3. Rubrik och pitch** (10p, Lätt): Sätt en rubrik med lagets namn och ett stycke under som beskriver laget i två till tre meningar. Vilka är ni och vad gör ni här? Bevis: Rubriken och texten syns på sidan när man öppnar index.html.
- [x] **4. Laget i en lista** (10p, Lätt): Lista alla i laget med en punktlista. En rad per person. Alla ska vara med. Bevis: Alla lagmedlemmars namn syns i en lista på sidan.
- [x] **5. Koppla stilmallen** (10p, Lätt): Länka in style.css i head och ge sidan egna färger och ett eget typsnitt. Nu slutar den se ut som ett dokument från 1995. Bevis: style.css är länkad och sidan har egna färger. Kodraderna syns i repot.
- [x] **6. Layout som håller ihop** (15p, Medel): Innehållet ska inte ligga kant till kant. Samla det i en kolumn med luft runt, centrerad på sidan. Bevis: Sidan har en centrerad kolumn med marginaler, inte text som går ut i kanterna.
- [x] **7. Lagets logga** (15p, Medel): Gör en logga för laget, lägg bildfilen i repot och visa den på sidan. Den ska ha en alt-text som beskriver vad bilden föreställer. TIPS: Låt AI generera en logga eller designa er egen. Bevis: Bildfilen ligger i repot, loggan syns på sidan och img-taggen har en beskrivande alt-text.
- [x] **8. Liv i sidan** (15p, Medel): Koppla in script.js och lägg till en knapp som gör något när man klickar på den. Vad som helst - en hälsning, en färg som byts, en text som dyker upp. Bevis: På sidan: klicka på knappen, något synligt ska hända. I repot: script.js inkopplad med en script-tagg sist i body.
- [x] **9. Sidfot** (10p, Lätt): Avsluta sidan med en footer som visar lagets namn och årtal. Ge den en tunn linje ovanför så den känns som ett avslut. Bevis: Footern syns längst ner på sidan med lagnamn och årtal.
- [x] **10. Publicera på nätet** (20p, Medel): Lägg upp sidan med GitHub Pages så att vem som helst kan öppna den. Det här är steget som gör den till en riktig webbplats. Bevis: En publik URL som öppnas i ett privat fönster utan inloggning och visar lagets sida.
- [x] **11. README som förklarar** (10p, Lätt): Skriv en README som berättar vilka ni är, vad sidan är, och länkar till den publicerade versionen. Det är första någon läser om ert projekt. Bevis: README.md i repot med lagnamn, medlemmar och en fungerande länk till den publicerade sidan.
- [x] **12. Post på LinkedIn** (10p, Lätt): Minst en i gruppen gör ett inlägg på LinkedIn om dagens hackathon. Inlägget måste innehålla länk till lagets publicerade Github pages sida. Tagga @ChasHack, @Chasacademy samt alla lagmedlemmar Bevis: Lägg till länken till ert LinkedIn post innuti README.md filen i ert Github repo.

## Side quests (30 st, 750p, frivilliga)

Medvetet fler än något lag hinner. Poängen är att de ska välja, inte beta av.

### Styling (8 st, 170p)

- [x] **Egen favicon** (15p, Medel): Egen ikon i webbläsarfliken. Bevis: På sidan: er egen ikon syns i webbläsarfliken i stället för standardikonen. Bildfilen ligger också i repot.
- [x] **Hover-effekter** (15p, Medel): Knappar och länkar reagerar på muspekaren. Bevis: På sidan: håll muspekaren över en knapp eller länk, utseendet ska ändras. I repot: minst en :hover-regel i style.css.
- [x] **Egen färgpalett** (20p, Medel): Färgerna som CSS-variabler i :root, använda konsekvent. Bevis: I repot: variabler deklarerade i :root och använda med var() på minst tre ställen i style.css. På sidan: ändra en variabel i devtools, då ska flera saker byta färg samtidigt.
- [x] **Egen typsnittskombination** (20p, Medel): Två typsnitt från Google Fonts, ett till rubriker och ett till brödtext. Bevis: På sidan: rubriker och brödtext har tydligt olika typsnitt, och inget av dem är webbläsarens standard. I repot: Google Fonts inkopplat i head.
- [x] **Kort med djup** (20p, Medel): box-shadow och border-radius som lyfter något från platt text till ett kort. Bevis: På sidan: minst ett kort med mjuk skugga och rundade hörn som ser ut att ligga ovanpå bakgrunden.
- [x] **Animerad entré** (25p, Svår): Rubrik eller logga glider in när sidan laddas. Bevis: På sidan: ladda om med F5, något ska glida eller tona in. Går det för fort att hinna se, titta på @keyframes-regeln i style.css.
- [x] **Funkar i mobilen** (25p, Svår): Media query så sidan håller i mobilbredd. Bevis: På sidan: dra ihop fönstret tills det är smalt, eller öppna sidan i mobilen. Inget ska spricka eller sticka ut utanför kanten.
- [x] **Grid-galleri** (30p, Svår): CSS Grid med auto-fit och minmax, lägger om sig utan media queries. Bevis: På sidan: dra ihop fönstret, antalet kolumner ska ändra sig av sig självt. I repot: grid-template-columns i style.css.

### Funktion (10 st, 305p)

- [x] **Klickräknare** (20p, Medel): Knapp som räknar klick och visar siffran. Bevis: På sidan: klicka på knappen flera gånger, siffran ska räknas upp för varje klick.
- [x] **Slumpat lagcitat** (20p, Medel): Knapp som slumpar fram citat ur en array. Bevis: På sidan: klicka flera gånger tills ni sett minst två olika citat.
- [x] **Mörkt och ljust läge** (30p, Svår): Knapp som växlar tema med classList.toggle. Bevis: På sidan: klicka på temaknappen fram och tillbaka, hela sidans färger ska växla åt båda håll.
- [x] **Medlemskort ur en array** (30p, Svår): Medlemmarna byggs av JavaScript ur en array, inte handskriven HTML. Bevis: På sidan: medlemmarna syns som kort. I repot: namnen finns bara i arrayen i script.js, inte handskrivna i index.html.
- [x] **Nedräkning till redovisningen** (30p, Svår): Klocka som tickar i realtid med setInterval. Bevis: På sidan: nedräkningen syns. Stå kvar i tio sekunder och se att siffrorna ändrar sig.
- [x] **Formulär med validering** (30p, Svår): preventDefault plus egna kontroller, fel visas vid fältet. Bevis: På sidan: skicka formuläret tomt, ett felmeddelande ska visas utan att sidan laddas om. Fyll i rätt och skicka igen, då ska felet försvinna.
- [x] **Sidan minns er** (35p, Riktigt svår): localStorage sparar ett val mellan besök. Bevis: På sidan: ändra det som sparas, ladda om med F5, valet ska finnas kvar. I README: vad det är som sparas.
- [x] **Filtrera medlemmarna** (35p, Riktigt svår): Sökfält som filtrerar listan medan man skriver. Bevis: På sidan: skriv några bokstäver i sökfältet. Listan ska smalna av medan man skriver och komma tillbaka när man raderar.
- [x] **Bildkarusell** (35p, Riktigt svår): Fram och bakåt genom en array av bilder, med varv runt. Bevis: På sidan: klicka framåt förbi sista bilden, ni ska hamna på den första igen. Testa bakåt från den första också.
- [x] **Hämta data utifrån** (40p, Riktigt svår): fetch mot ett öppet API, med felhantering. Bevis: På sidan: datan från API:et syns och byts när man laddar om eller klickar. I README: vilket API ni använder och vad som visas när anropet misslyckas.

### Roligt (5 st, 130p)

- [x] **Ljud vid klick** (20p, Medel): new Audio kopplat till en knapp. Bevis: På sidan: klicka på knappen, ett kort ljud ska spelas. I README: vilken knapp det är, så granskarna hittar rätt även utan ljud på.
- [x] **Easter egg** (25p, Svår): Hemlig tangent eller klick som utlöser något. Bevis: I README: hur man utlöser det. På sidan: gör som README säger, då ska det hända.
- [x] **Skrivmaskinseffekt** (25p, Svår): Text som skriver ut sig själv tecken för tecken. Bevis: På sidan: ladda om med F5, texten ska skriva ut sig själv tecken för tecken.
- [x] **Konfetti vid klick** (30p, Svår): Element skapade med JavaScript som regnar över sidan. Bevis: På sidan: klicka på det som utlöser konfettin, den ska falla över sidan och sedan städas bort.
- [x] **Muspekaren lämnar spår** (30p, Svår): mousemove som skapar och städar bort element. Bevis: På sidan: rör muspekaren över sidan, spåret ska följa efter och försvinna av sig självt.

### Samarbete (4 st, 75p)

- [x] **Lagbild på sidan** (15p, Medel): Riktig lagbild tagen på plats, publicerad på sidan. Bevis: På sidan: lagbilden syns. Bildfilen ligger i repot.
- [x] **Allas favoritverktyg** (15p, Medel): En rad per person om ett verktyg de inte klarar sig utan, en commit var. Bevis: På sidan: en rad per lagmedlem. I repot: historiken under Commits visar en commit per person.
- [x] **Loggbok över dagen** (20p, Medel): Tidslinje över vad ni byggde och vad som gick snett. Bevis: På sidan: en loggbokssektion med minst fem poster med klockslag.
- [x] **Pull request med review** (25p, Svår): Branch, PR, review av lagkamrat, merge. Bevis: I repot: en merged pull request under fliken Pull requests, med en review från någon annan i laget.

### Tillgänglighet (3 st, 70p)

- [x] **Alt-text på allt** (15p, Medel): Varje bild har en beskrivande alt-text. Bevis: I repot: varje img-tagg har ett alt-attribut som beskriver bilden. På sidan: högerklicka en bild och välj Inspektera, alt-texten ska stå där.
- [x] **Kontrast som håller** (25p, Svår): Text mot bakgrund klarar 4.5:1. Bevis: På sidan: högerklicka på brödtexten, välj Inspektera och klicka färgrutan vid color. Kontrasten ska vara minst 4.5. I README: vad ni ändrade.
- [x] **Tangentbordet räcker** (30p, Svår): Hela sidan går att nå med Tab och markeringen syns. Bevis: På sidan: tryck Tab upprepade gånger. Allt klickbart ska gå att nå i en ordning som följer sidan, och markeringen ska synas hela vägen.

## Öppna punkter

- Start-repot: uppgiftssidan länkar till `github.com/AntonSatt/chashack-starter`. Kontrollera att `index.html`, `style.css` och `script.js` ligger tomma där innan dagen.
- Vinstregeln behöver sägas muntligt vid uppstarten också, inte bara stå på sidan.
- Nedräkningen i side questen "Nedräkning till redovisningen" har måldatum 2026-09-11 15:00 i exempelkoden. Justera om tiden ändras.
- Serverversion med delad state (riktig granskningskö och leaderboard) byggs när uppgifterna är spikade. Just nu ligger allt i localStorage.

## Mall för ny uppgift

- [ ] **Titel** (10p, Lätt): Vad laget ska göra. Bevis: vad rättarlaget tittar efter.
