# Nordic Tube — Atelier / modulær statisk nettside

Refaktorert fra Atelier Expanded. Visuelt design, innhold, animasjoner og SEO-metadata er videreført. WordPress er ikke nødvendig.

## Mappestruktur

```text
index.html                 Forside (kun HTML og SEO-data)
illustrasjoner.html        Produktillustrasjoner og montasjevideoer
produkter/index.html       Produktoversikt
produkter/*.html           Individuelle produktsider
css/base.css               Felles CSS-tokens og reset for forsiden
css/frontpage.css          Forsidens layout og animasjoner
css/product-common.css     Delte stiler for produktseksjonen
css/product-list.css       Kun produktoversikten
css/product-detail.css     Kun individuelle produktsider
js/frontpage.js            Produktvelger, meny og scrolleffekter
assets/                    Originalbilder, videoer, SVG-illustrasjoner og OG-bilde
assets/media/              WebP-bilder i to størrelser og videoplakater
robots.txt / sitemap.xml   Søkemotorfiler
```

Det ligger **ikke inline CSS eller utførbar JavaScript** i HTML-filene. JSON-LD-strukturerte data ligger som `<script type="application/ld+json">` i HTML for korrekt søkemotorindeksering; dette er data, ikke utførbar JavaScript.

## Test lokalt

```bash
cd nordic-tube-atelier-modular
python -m http.server 8000
```
Åpne http://localhost:8000. Ingen npm eller byggesteg trengs.

## Videre anbefaling

Når nettstedet vokser, kan felles navigasjon og footer trekkes ut i komponenter ved overgang til Astro/Next.js eller statisk template-system. Med ren HTML beholdes noe gjentatt markup.

Merk: Produktillustrasjonene er fortsatt konseptillustrasjoner. SEO-score og nettleserytelse er ikke målt i denne refaktoreringen.

## Prosjektbilder og filmer

Forsiden og siden for ladefundamenter viser prosjekter fra Posten Bring Haugesund, RfD Mile i Mjøndalen og Frier Vest havneterminal. Bildegalleriene åpnes uten JavaScript. Originalene er beholdt; nettsiden bruker WebP-versjoner i 640 og 1280 piksler. Begge filmene har avspillingskontroller og lastes først ved avspilling.
