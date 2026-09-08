# cntx-pricing

Configuratore di listino Contix. Pagina statica singola: apri `index.html`, nessuna build.

## Design system

Lo stile segue i token del preset `forest-alkemy+` di
[`@matteoaliano/forest-ui`](https://www.npmjs.com/package/@matteoaliano/forest-ui),
estratti dal pacchetto e ricopiati come variabili CSS in `index.html` (ogni
variabile riporta in commento il token di origine). La pagina non usa la
libreria React: è un allineamento visivo, quindi i token vanno riallineati a
mano quando il design system cambia.

## Font

I font del design system (Aeonik, Aeonik Mono, AlkemyBETA) sono proprietari e
**non sono versionati** — questo repo è pubblico. Senza di essi la pagina resta
corretta in colori, spaziature, scala tipografica e dark mode, ma ripiega sui
caratteri di sistema.

Per la resa corretta in locale, copia i font dal pacchetto npm:

```sh
npm pack @matteoaliano/forest-ui
tar -xzf matteoaliano-forest-ui-*.tgz
cp -r package/fonts/aeonik package/fonts/aeonik-mono package/fonts/alkemy-beta fonts/
```

`index.html` si aspetta `fonts/aeonik/aeonik.css`, `fonts/aeonik-mono/aeonik-mono.css`
e `fonts/alkemy-beta/alkemy-beta.css`.
