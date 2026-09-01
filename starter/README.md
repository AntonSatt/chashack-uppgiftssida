# Frontend-snabbstart för ChasHack-lag

Åtta steg från en tom mapp till en färdig lagsida. Varje steg avslutas med en commit –
på så vis lär ni er Git-flödet *genom* att bygga sidan i stället för vid sidan av.

Mappen är uppgiftsteamets (Anton, Victoria, Theo) förslag och kan lyftas ut som
deltagarernas grundrepo. `index.html`, `style.css` och `script.js` är ett skelett med
tips i kommentarerna; lag som hellre börjar från noll skapar filerna själva. Båda
sätten räknas.

## Stegen

| Steg | Mål | Tips | Commit-meddelande |
| --- | --- | --- | --- |
| 1. Skeleton | En `index.html` med titel och en rubrik (`<h1>`) | Redan gjort i skeletonen – gör bara detta om ni börjar från scratch | `feat: skapar sidans skelett` |
| 2. Struktur | Ett `<p>` med text under rubriken och en meny (`<nav>`) med tre länkar | Länkarna behöver inte fungera ännu | `feat: lägger till introtext och meny` |
| 3. Stil | Länka in `style.css`, byt bakgrundsfärg och rubrikens typsnitt | Skeletonen har redan länkat filen – skriv era regler i den | `style: byter bakgrund och typsnitt` |
| 4. Layout | Centrera rubriken och lägg menylänkarna i en horisontell rad | `margin: 0 auto` centrerar; flexbox radordnar länkarna | `feat: centrerar rubrik och radlägger menyn` |
| 5. Bild | En logo/bild högst upp, lagom stor, med alt-text | `max-width: 200px` räcker ofta | `feat: lägger till logon` |
| 6. Knapp | En knapp under stycket med egen färg och runda hörn | `border-radius: 999px` ger hela rundningar | `feat: lägger till en knapp med stil` |
| 7. Levande JS | Klick visar en hälsning och byter bakgrundsfärg | `querySelector`, `addEventListener("click", …)` och `classList.toggle` | `feat: knappen byter tema och hälsar` |
| 8. Polish | Footer med lagnamnet och hover-effekt på menylänkarna | `:hover` ändrar färg eller understrykning | `feat: lägger till footer och hover` |

## Git-trappan (samma steg, ett flyt)

Stegen överlappar med poängbankens Git-uppgifter, så att flödet uppstår naturligt:

1. **Klona grundrepot och få det att köra** – innan steg 1. Öppna `index.html` i
   webbläsaren.
2. **En commit var** – minst en meningsfull commit per person, alltså minst ett steg
   var som görs av alla.
3. **Feature-branch och kontrollerad merge** – steg 3–4: gör stilen på en branch med
   ett begripligt namn och slå ihop den kontrollerat.
4. **Pull request med review** – steg 5–6: öppna en PR för bild- och knappstegen och
   låt en lagkompis granska innan merge.
5. **Planera med issues** – inför steg 7: skapa tre små issues och stäng dem via
   commits eller PR:er.
6. **README som nästa lag kan starta från** – i steg 8: beskriv hur projektet körs,
   vad ni byggt och vad ni skulle göra härnäst.

## DevOps-spåret (om ni vill fortsätta)

- Lös en liten merge-konflikt tillsammans utan att tappa innehåll.
- Låt CI köra en enkel kontroll på varje push.
- Publicera sidan på en delbar URL.
- Kör sidan i en container med ett enda kommando från ren miljö.

## Efter steget 8

Ta en lagbild, koppla ihop laget på LinkedIn och skriv – först när alla sagt okej –
ett kort inlägg om dagen. Se uppgiftsbanken på ChasHack-sidan för poängen.
