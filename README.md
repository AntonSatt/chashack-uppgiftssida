# ChasHack: uppgiftssidan

<p align="center"><img src="sources/assets/ChasHackForRookiesLogo.svg" alt="ChasHack for rookies" width="220"></p>

Bygg-repo för uppgiftsteamet (Anton, Victoria, Theo) inför ChasHack på Chas
Academy, fredag 11 september 2026. Här finns bara det trion bygger: sidan,
planen, design-assets och skelettet. Planeringsunderlag och möten ligger i det
interna arkiv-repot, inte här.

## Temat

Deltagarna bygger en **lagsida** i sitt eget repo, från tre tomma filer
(`index.html`, `style.css`, `script.js`) till en publicerad webbplats om laget.

- **Huvudspåret** - tolv obligatoriska steg, lätt till medel, i ordning. Slutar
  i en färdig sida på GitHub Pages. 145p.
- **Side quests** - trettio frivilliga extrauppdrag, medel till riktigt svår, som
  plockas längs vägen och bygger vidare på samma sida. 750p. Medvetet fler än
  något lag hinner, så att lagen väljer i stället för att beta av.

Poängen avgör placeringen, men **alla tolv steg i huvudspåret måste vara
godkända för att ett lag ska kunna vinna**. Topplistan märker lag som inte är
klara med "Ej kvalificerad" och sorterar dem under de kvalificerade.

Uppgifterna bor i `uppgiftssida.html`, i arrayerna `MAIN` och `QUESTS`.
`uppgifter.md` är teamets arbetslista över samma innehåll.

## Innehåll

- `uppgiftssida.html` - deltagarsidan: huvudspåret som en stig med
  framstegsmätare, side quests i ett filtrerbart rutnät, granskningsvy, live
  topplista med kvalificeringsregel, adminpanel och väggläge (`?wall=1`).
  All delad data ligger i Supabase. Det här är filen som publiceras till Pages.
- `uppgifter.md` - arbetslistan för uppgiftsteamet. Samma uppgifter i markdown,
  lätt att redigera på GitHub.
- `plan-ny-uppgiftssida.html` - plan v3: designriktning, granskningsflöde,
  tidsplan och öppna frågor. Granska i webbläsaren.
- `sources/assets/` - ChasHack-bannrarna och logotypen som designen bygger på.
- `starter/` - utkastet som det publika skelett-repot byggdes på
  (github.com/AntonSatt/chashack-starter).
- `.github/workflows/deploy-pages.yml` - publicerar `uppgiftssida.html` som
  `index.html` på GitHub Pages vid push till `main`.

## Kör lokalt

Öppna `uppgiftssida.html` i VS Code Live Server, eller:

```bash
npx --yes http-server . -p 8123 -c-1
```

Sidan pratar med Supabase även lokalt, så den delar data med den publicerade
versionen. Testa gärna med låtsaslag och nollställ efteråt.

## Delad data: Supabase

Sidan är statisk, men lag, avbockningar, granskningspar och topplista ligger i
ett Supabase-projekt så att alla lag ser samma sak i realtid.

- Projekt: **chashack-rookies**, region eu-north-1 (Stockholm)
- API-URL och publik nyckel ligger överst i skriptet i `uppgiftssida.html`

### Tabeller

| Tabell | Innehåll |
| --- | --- |
| `teams` | Ett lag. Namnet är unikt och är det lagen skriver in högst upp. |
| `claims` | En rad per avbockad uppgift: `pending`, `approved` eller `rejected`. |
| `assignments` | Vem granskar vem. Ett lag granskar exakt ett annat. |
| `settings` | Nyckeln `phase`: `build`, `review` eller `done`. |
| `admin_secret` | Admin-PIN. Har RLS på men **ingen policy**, så den är oåtkomlig via API:et. |

Vyn `leaderboard` summerar godkända och väntande poäng per lag.

### Faser

- **build** - lagen bockar av. Poäng syns som väntande på topplistan.
- **review** - avbockning låst, granskningen öppen. Lagen bedömer varandra.
- **done** - allt låst, slutresultatet står fast.

### Så kör ni dagen

1. Lagen skriver in sitt lagnamn högst upp på sidan. Ett namn = ett lag, och
   flera datorer går med i samma lag genom att skriva samma namn.
2. Lagen jobbar och bockar av. Topplistan tickar live i gult.
3. När alla lag är registrerade och dagen börjar ta slut: gå till **Admin**,
   skriv PIN och tryck **Dela ut**. Varje lag får ett annat lag att granska.
   Lagen läggs i en slumpad ring, så ingen granskar sig själv.
4. Byt fas till **Granska**. Avbockningen låses och granskningsknapparna dyker
   upp under fliken Granska.
5. När granskningen är klar: byt fas till **Klart**. Gröna poäng är facit.

### Admin-PIN

PIN är från början `chas2026`. **Byt den innan dagen.** I Supabase SQL Editor:

```sql
select set_admin_pin('chas2026', 'er-nya-pin');
```

### Nollställa inför skarp körning

```sql
delete from assignments where reviewer_team_id is not null;
delete from claims where id is not null;
delete from teams where id is not null;
update settings set value = '"build"' where key = 'phase';
```

WHERE-villkoren är inte pynt: Supabase kör `pg_safeupdate`, som stoppar
obetingade DELETE och UPDATE.

Webbläsare som redan gått med i ett borttaget lag släpper det automatiskt och
får upp lagvalet igen.

### Vad skyddet faktiskt är

Nyckeln i sidan är publik, precis som den ska vara i Supabase. Skyddet ligger i
databasens regler, och vald nivå är "bara admin-PIN":

- Att dela ut granskningspar och byta fas kräver PIN. Det går inte runt, och
  PIN:en går inte att läsa via API:et.
- Lagen litas på i övrigt. Någon som öppnar devtools kan i teorin bocka av åt
  ett annat lag eller godkänna sina egna uppgifter. För ett skolhackathon är
  det rimligt, men det är värt att känna till.

## Status och nästa steg

- Uppgifterna är omgjorda till lagsidetemat: huvudspår plus side quests.
  De gamla kategoriuppgifterna och `.NET`-spåret är borttagna, men finns kvar
  i git-historiken om något ska återanvändas.
- Kontrollera att `index.html`, `style.css` och `script.js` ligger tomma i
  start-repot innan dagen.
- Byt admin-PIN från `chas2026` innan den 11:e.
- Kör en genrepetition med två låtsaslag och nollställ efteråt.
