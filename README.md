# FORK — Fork any runner.

Landningssida + fungerande Fork Studio för $FORK. Allt ligger i `index.html` (en fil, ingen build).

## Vad sajten gör
- **Hero:** flytande krom-skulptur (egen WebGL-raymarcher, inga bibliotek). En droppe (runnern, grafit) knoppar av en ny droppe (din fork) i forkens färg.
- **Running now:** hämtar live-runners från DexScreener (gratis, ingen nyckel).
- **One runner. Two branches:** låst scroll-sekvens i 5 steg (läs → strippa identitet → motorn stannar → ny gren).
- **Fork Studio (fungerar på riktigt):** klistra in CA, pump.fun-/DexScreener-länk eller ticker → läser runnern live → välj namn, ticker, vibe (Clean/Night/Loud/Luxe) och motor (Agent/Launchpad/Tool/Meme) → färdig coin-sajt i förhandsvisning.
  - Ladda ner `index.html` för forken, logga som PNG 1000×1000 (pump.fun-bild) och ett Fork Card för X.
  - Spärrar: namn/ticker som liknar förälderns blockeras (t.ex. GHOST vs GH0ST), förälderns bild används aldrig, all text skrivs ny, varje fork signeras "forked from $X".
  - De genererade sajterna har riktiga moduler: agent-konsol och launch-feed (live pump.fun-ström), CA-scanner (DexScreener), meme lab (canvas → PNG).
- **Forks have families:** låst sekvens där skulpturen växer till ett släktträd (exempeldata, märkt som exempel).
- **$FORK:** tokenfakta, CA, avgiftsflöde, roadmap. FAQ och footer.

## Fyll i vid launch (överst i sista `<script>`, `CONFIG`)
```js
ca: "",          // $FORK mint-adressen
x: "",           // https://x.com/dittkonto
dexscreener: "", // valfritt
site: "",        // t.ex. "fork.fun" – skrivs på Fork Cards och i varje forks footer
fees: [...]      // fördelningen av creator fees (cents per $1)
```
Tom `ca` visar "Posted here and on X at launch" – aldrig en påhittad adress. Köpknapparna går till `https://pump.fun/coin/<ca>`.

## Deploy
GitHub → Vercel, Framework: **Other**, ingen build command, output = roten. Lägg `index.html`, `og.jpg` och `README.md` i repo-roten.

## Kolla efter deploy
1. Intron: droppen formas och knoppar av den gröna forken (riktig GPU = mjukt och skarpt).
2. Typsnitten: Schibsted Grotesk, Fraunces (kursiva ord), Spline Sans Mono.
3. "Running now" fylls med live-runners och studion byter automatiskt till den första.
4. Studion: klistra in en CA, tryck Fork it, testa Download site / Logo PNG / Fork Card.
5. Agent-/Launchpad-motorn i förhandsvisningen ska visa live launches från pump.fun.
6. X-förhandsvisning (og.jpg) när du klistrar in länken.

Not financial advice. FORK never copies a brand.
