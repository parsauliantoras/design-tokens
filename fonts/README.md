# Font files

| File | Typeface | Subset | Source | Size | SHA-256 | Licence |
|---|---|---|---|---|---|---|
| BricolageGrotesque-latin.woff2 | Bricolage Grotesque, variable: weight 200–800, optical size 12–96, width fixed at 100% | latin (Google Fonts) | https://fonts.gstatic.com/s/bricolagegrotesque/v9/3y9K6as8bTXq_nANBjzKo3IeZx8z6up5BeSl9D4dj_x9PpZBMlGIInHWVyNJ.woff2, downloaded 2026-10-14; Google Fonts release v9, source commit 84745e5b96261ae5f8c6c856e262fe78d1d6efdd of https://github.com/ateliertriay/bricolage | 76,868 B | 85f55a58a31e61a2e19e8bb25fed503181bf2a6b4cab76c589992cfaac377447 | SIL OFL 1.1, `OFL.txt` |
| Geist-latin.woff2 | Geist, variable: weight 100–900 | latin (Google Fonts) | https://fonts.gstatic.com/s/geist/v5/gyByhwUxId8gMEwcGFWNOITd.woff2, downloaded 2026-10-14; Google Fonts release v5, source commit a6d260e6cbc07eafdfad438f33601fe3c38b1e6f of https://github.com/vercel/geist-font | 29,288 B | 9b6f5ff45b278c744b5f379a2c4ecbaf858a842b8eaf82ac8d21b699ca16c608 | SIL OFL 1.1, `Geist-OFL.txt` |
| JetBrainsMono-400-latin.woff2 | JetBrains Mono, static weight 400 (the variable face is 40,404 B, over the font budget) | latin (fontsource) | https://cdn.jsdelivr.net/fontsource/fonts/jetbrains-mono@latest/latin-400-normal.woff2, downloaded 2026-10-17 | 21,168 B | 14425ba9c695763c1547f48a206b7aa60350a33ae23de09f0407877f3fcd89eb | SIL OFL 1.1, `JetBrainsMono-OFL.txt` |
| GeistMono-400-latin.woff2 | Geist Mono, static weight 400 (the monospace face of Pipeline Lab, its ADR-0024) | the characters of JetBrainsMono-400-latin.woff2 plus U+2192 (→), subset with fontTools | `dist/fonts/geist-mono/GeistMono-Regular.woff2` of the npm package `geist` 1.8.1 (https://www.npmjs.com/package/geist, Vercel), taken 2026-10-18 | 24,884 B | 59ed65aae41746d323f9130e1c485f827f6f8fe1444e839dbeb5231992c5b225 | SIL OFL 1.1, `GeistMono-OFL.txt` |

To replace a file: download the latin block again, update this table, and run each site's
tests. A new display or body file can have other letter widths, so each site measures its
fallback `size-adjust` again.
