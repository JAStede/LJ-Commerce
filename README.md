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
