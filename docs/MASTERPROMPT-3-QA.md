# LJ Commerce — Masterprompt 3.0 kwaliteitscontrole

## Implemented in the demo
- Responsive layout, semantic main/nav, viewport, Dutch language, one H1 on homepage
- Demo SEO title and description, noindex,nofollow (mandatory while unofficial), robots.txt Disallow: /, deliberately empty sitemap.xml
- SVG favicon, 404 page, privacy/cookie demo page
- Consent: necessary-only or all, preference change, GA4 disabled unless both valid client G-ID and consent; no marketing scripts
- Browser QA helper: open devtools and run `LJCommerceQA.run()`; check console errors and responsive layouts
- All catalogue prices and availability are provisional; real checkout disabled

## Before production: must complete and verify
- Obtain owner permission for brand, logo, images, texts and catalogue; verify each price and stock record
- Decide final domain and generate valid canonical URL on every indexable page; remove demo noindex and robots disallow only after approval
- Build server-rendered or pre-rendered **unique URLs** for every category and product; unique title, description, H1, image alt, breadcrumb and internal links
- Add Product, Offer (only with verified price/availability), BreadcrumbList, Organization/LocalBusiness JSON-LD with verified company details
- Build complete sitemap.xml from actual canonical URLs and submit to Search Console; test robots, 404, redirects, Open Graph and social previews
- Configure GA4 property and measurement ID for the actual customer; verify consent mode and that no analytics requests occur before consent; provide withdrawal mechanism
- Complete client-specific legal privacy, cookies, terms, returns, warranty, delivery, installation and contact details
- Production backend: authentication, least-privilege access, payment provider with webhooks and signature verification, server-side pricing, stock concurrency, CSRF/XSS protection, validation, rate limits, updates, TLS, backups and restoration tests
- Test keyboard navigation, screen readers, iOS/Android/tablet/desktop, all buttons, image loading, search, filter, cart math, order flow, security and Core Web Vitals
- Add deployment checks, dependency scans and automated tests once the actual backend is chosen

## Current limitations
Static demo, not a production webshop. No backend, payment or live GA4. QA helper is a manual diagnostic, not a substitute for automated tests or a security audit. Privacy copy is not a final legal document. There is no canonical domain for this private demo.
