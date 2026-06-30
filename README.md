# L'Altra Volta — Casa vacanze (San Pietro Vernotico, Salento)

Sito web statico della casa vacanze **L'Altra Volta**, a San Pietro Vernotico (BR), Puglia.
Singola pagina, **bilingue 🇮🇹 / 🇬🇧**, senza framework né build: solo HTML, CSS e un piccolo JavaScript. Si pubblica gratis su GitHub Pages, Cloudflare Pages o qualsiasi hosting statico.

## Struttura

```
laltravolta/
├── index.html        ← il sito (markup + stili + logica i18n/FAQ)
├── 404.html          ← pagina di errore
├── robots.txt        ← per i motori di ricerca
├── sitemap.xml       ← mappa del sito
├── assets/           ← logo nei vari formati
└── photos/           ← foto della casa (orig-01…orig-10)
```

## Anteprima in locale

Basta aprire `index.html` con un doppio clic nel browser.
(Per la mappa e i font serve la connessione a internet.)

## Contatti del sito

- WhatsApp / telefono: **+39 328 052 2050**
- Email: **prenotazioni@laltravolta.it**

## Note tecniche

- Lingua predefinita: italiano; pulsante **IT / EN** in alto a destra (la scelta viene ricordata).
- Colori: sabbia `#F5EEE0`, oliva `#8A7A3F`, testo scuro `#2A2417`.
- Font: Cormorant Garamond, Jost, Allura (Google Fonts).
- I riferimenti `https://laltravolta.it/` in `index.html`, `robots.txt` e `sitemap.xml`
  vanno aggiornati se il dominio finale sarà diverso.

Realizzato a partire dal design Claude (claude.ai/design).
