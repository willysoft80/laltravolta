# L'altra Volta — Casa vacanze (San Pietro Vernotico, Salento)

Sito web statico della casa vacanze **L'altra Volta**, a San Pietro Vernotico (BR), Puglia.
Nessun framework né build: solo HTML, CSS e un piccolo JavaScript.

Pubblicato su **GitHub Pages** (branch `main`) con dominio personalizzato:
**https://www.laltravolta.it** (primario, con redirect dall'apex `laltravolta.it`).
Il file `CNAME` nel repo contiene il dominio.

## Struttura

```
laltravolta/
├── index.html         ← il sito principale, singola pagina bilingue IT/EN
├── 404.html           ← pagina di errore
├── CNAME              ← dominio custom per GitHub Pages (www.laltravolta.it)
├── robots.txt         ← per i motori di ricerca
├── sitemap.xml        ← mappa del sito (8 URL: home + hub guide + 6 guide)
├── guide/             ← hub (index.html) + 6 guide SEO, una per cartella
│   ├── adriatico-o-ionio-salento/
│   ├── spiagge-vicino-san-pietro-vernotico/
│   ├── dormire-vicino-carrisiland/
│   ├── salento-con-bambini/
│   ├── cosa-vedere-dintorni-san-pietro-vernotico/
│   └── cosa-mangiare-salento/
├── assets/            ← loghi e icone (vedi sotto)
├── photos/            ← foto della casa e hero delle guide
└── google-business/   ← foto per il profilo Google Business (non linkate dal sito)
```

### `assets/`

- Wordmark del logo come **SVG pre-renderizzato**: `logo-word-olive.svg` e `logo-word-light.svg`.
- Marchi raster: `logo-art.png`, `logo-art-light.png`, `logo-mark.png`.
- Icone: `favicon-48.png`, `apple-touch-icon.png`.
- `vault.png`: grafica della volta a stella usata nell'animazione di apertura di `index.html`.
- `og-cover.jpg`: immagine di anteprima per i social (Open Graph / Twitter card).
- `logo-full.jpg` e `logo-casa-vacanze.jpg`: **sorgenti per il profilo Google Business**;
  restano nel repo anche se non sono linkati dalle pagine.

### `photos/`

- Foto della casa: `orig-01` … `orig-10` con varianti responsive `-800`
  (e `-1280` per alcune).
- Immagini hero delle guide (`guide-*.jpg`), provenienti da **Wikimedia Commons**;
  i crediti CC sono indicati nelle didascalie delle rispettive pagine.

### `google-business/`

Foto e loghi preparati per il profilo Google Business. Non sono referenziati
dalle pagine del sito: servono solo come materiale da caricare sul profilo.

## Anteprima in locale

Per la sola home basta aprire `index.html` nel browser. Le guide usano percorsi
assoluti (`/assets/…`, `/photos/…`), quindi conviene un piccolo server locale, ad esempio:

```
python -m http.server 8000
```

e poi visitare `http://localhost:8000/`. (Per mappa e font serve la connessione a internet.)

## Contatti del sito

- WhatsApp / telefono: **+39 328 052 2050**
- Email: **prenotazioni@laltravolta.it**

## Note tecniche

- `index.html` è una singola pagina **bilingue IT/EN**: lingua predefinita italiano,
  pulsante IT/EN in alto a destra (la scelta viene ricordata).
- Le guide sono pagine statiche autonome, ognuna con propri meta SEO,
  dati strutturati e breadcrumb.
- Palette: sabbia `#F5EEE0`, oliva `#8A7A3F` (nelle guide il testo oliva usa la
  variante più scura `#6E6132` per il contrasto), testo scuro `#2A2417`.
- Font: **Cormorant Garamond** e **Jost** via Google Fonts.
  Il wordmark del logo è un SVG pre-renderizzato, quindi non richiede font dedicati.
- Tutti gli URL canonici puntano a `https://www.laltravolta.it/` e sono allineati
  in `index.html`, `robots.txt` e `sitemap.xml`.

Realizzato a partire dal design Claude (claude.ai/design).
