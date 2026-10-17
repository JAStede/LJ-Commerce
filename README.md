# LJ Commerce — herbruikbare webshopbasis

Private LJ Studio-repository. Eerste concept: onafhankelijke Anto Elektra-demo, niet officieel en niet geschikt voor echte bestellingen.

## Versie 0.1
- 30 modelvermeldingen uit publiek toegankelijke categoriepagina's (niet het volledige assortiment)
- Responsieve productcatalogus, zoeken, filters, sorteren, productdetails
- Interactieve winkelwagen: aantallen wijzigen, verwijderen, subtotalen en voorbeeldverzending
- Demo-verzendregel: gratis vanaf €50, anders €5,95; geen echte Anto Elektra-verzendvoorwaarden
- Geen betalingen, echte orders, productfoto's of persoonsgegevens

## Nog vereist voor productie
- Toestemming voor branding, productteksten en foto's; actuele catalogus, prijzen en voorraad controleren
- Productfoto's, specificaties, product-URL's, SEO-redirects en contentreview
- Beheerde webshopbackend, iDEAL/Mollie, order- en voorraadbeheer, veilige adminaccounts
- TLS, updates, autorisatie, rate limiting, logging, back-ups, securitytests
- AVG/privacy, cookies, consumentenrecht, voorwaarden, retouren en wettelijke garantie
- Echte bezorg-/installatieprijzen en volledige end-to-end testbestellingen

## Bronnen
https://www.antoelektra.nl/assortiment-wassen-drogen/wasmachines/
https://www.antoelektra.nl/assortiment-wassen-drogen/drogers/
https://www.antoelektra.nl/assortiment-wassen-drogen/vaatwassers/

## Starten
Gebruik een lokale webserver, bijvoorbeeld `python -m http.server 8000`, en open http://localhost:8000. De JSON-catalogus wordt via fetch geladen en werkt niet betrouwbaar als file://.

De huidige illustraties zijn generieke SVG's. Dit is een eerste technische en visuele basis, geen afgeronde webshop.


## Masterprompt 3.0 — demo foundation (17 oktober 2026)

Nieuwe bestanden: `assets/consent.js`, `assets/config.js`, `assets/qa.js`, `assets/favicon.svg`, `privacy.html`, `404.html`, `robots.txt`, `sitemap.xml` en `docs/MASTERPROMPT-3-QA.md`.

Cookiekeuze: noodzakelijk of alles toestaan, later wijzigbaar via de footer. GA4 laadt alleen na toestemming en alleen als `assets/config.js` een geldig klant-meet-ID bevat; standaard is dit leeg. De demo blijft `noindex,nofollow` en `robots.txt` blokkeert crawlers; sitemap is daarom bewust leeg. De privacytekst is een technische demo-uitleg en geen klantspecifiek juridisch document.

**Controle:** Open de site via een webserver en voer in de browserconsole `LJCommerceQA.run()` uit. Dit geeft eenvoudige controles en browserfouten weer. Voer daarnaast de handmatige controles uit `docs/MASTERPROMPT-3-QA.md` uit. Dit vervangt geen securitytest of live browsercheck.

**Nog open:** unieke indexeerbare categorie- en productpagina's, canonical URL's op het echte domein, JSON-LD met geverifieerde productgegevens, volledige sitemap, GA4-klant-ID, live privacy/voorwaarden, backend, betalingen, beveiliging, tests en deploycontrole.
