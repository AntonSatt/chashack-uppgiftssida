# ChasHack: uppgiftssidan

Bygg-repo för uppgiftsteamet (Anton, Victoria, Theo) inför ChasHack på Chas
Academy, fredag 11 september 2026. Här finns bara det trion bygger: sidan,
planen, design-assets och skelettet. Planeringsunderlag och möten ligger i det
interna arkiv-repot, inte här.

## Innehåll

- `uppgiftssida.html` - prototyp v1 av deltagarsidan: uppgiftsrutnät, bocka-av,
  inlämning av repo-länk, granskningsflöde, topplista, väggläge (`?wall=1`)
  och leaderboard-vy (`?org=1`). Kör helt lokalt i webbläsaren (localStorage),
  inget skickas någonstans.
- `plan-ny-uppgiftssida.html` - plan v3: designriktning, granskningsflöde,
  tidsplan och öppna frågor. Granska i webbläsaren.
- `sources/assets/` - ChasHack-bannrarna som hela designen bygger på.
- `uppgifter/` - uppgiftsfilerna deltagarna jobbar i. En mapp per kategori,
  en fil per uppgift, instruktionerna högst upp i varje fil. `.NET`-uppgifterna
  körs som file-based apps (`dotnet run fil.cs`), utan projekt eller csproj.
- `starter/` - utkastet som det publika skelett-repot byggdes på
  (github.com/AntonSatt/chashack-starter).

## Kör lokalt

```bash
python3 -m http.server 8123
```

Öppna `http://127.0.0.1:8123/uppgiftssida.html`. Server behövs bara för att
slippa filbehörigheter; allt körs i webbläsaren.

## Status och nästa steg

- Uppgiftslistorna från Discord väntar på att klistras in i rutnätet.
- .NET-uppgifterna spikas av Victoria och Theo inför avstämningen 7 september.
- Serverversion med delad state (riktig granskningskö och leaderboard) byggs
  när uppgifterna är på plats.
- Publikt skelett-repo för ettorna: klart på
  github.com/AntonSatt/chashack-starter (fork-flöde, minimalt, inget
  internt innehåll).
