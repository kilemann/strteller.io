# Størrelsen teller
Fartstest for internett (ping, jitter, ned, opp) mot Cloudflare. Én HTML-fil (`index.html`). Sperret på mobilnett.
Nettside: https://kilemann.github.io/strteller.io/

## Regler for alt arbeid i dette repoet
- Svar brukeren på norsk. Commit-meldinger på norsk, med versjon først (f.eks. «Appnavn 1.4.0: kort beskrivelse»).
- Hver endring får nytt versjonsnummer (MAJOR.MINOR.PATCH) og en linje i endringsloggen. Versjonen skal være lik på alle stedene under.
- Lever rett på `main` når resultatet er godt nok og testene er grønne. Kjør `git fetch origin main` og rebase før push.
- Testdrevet utvikling (TDD) bare når brukeren ber om det. Eksisterende tester kjøres alltid før push.
- Tekniske påstander skal sjekkes mot dokumentasjon eller kilde, ikke gjettes.
- Appen står på samlesida (kilemann.github.io). Den skal vise navn, versjon og en (i)-knapp øverst til venstre. (i) åpner info-vinduet med bruksanvisning og versjonsliste. Oppdater versjonslista der ved hver ny versjon.
- Publiseres med GitHub Pages fra `main` (rot). Det tar noen minutter før endringen er ute.

## Versjon står her
- `package.json`
- `index.html`: `<span class="ai-ver">vX.Y.Z</span>` i overskriften, kommentaren øverst i skriptet (`/* Størrelsen teller vX.Y.Z` + changelog-linje), `const VERSION`, versjonslista i info-vinduet
- `README.md`: tittel og «Versjoner»

## Tester
`npm test` (Node 22). Simulert nettleser, nett og klokke i `test/harness.js`. `test/release.test.js` sjekker versjonen.
