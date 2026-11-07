# VeyraTools

A responsive, privacy-friendly collection of **120 free online tools** for text, developers, math, unit conversions, and generators. This is a lightweight static site with no framework, build step, backend, or external runtime dependencies.

## Run locally

Open `index.html` in a modern browser, or serve this directory over HTTP (recommended for browser cryptography APIs):

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Included tools

- **Text:** character/word/line counters, case conversion, reverse, whitespace cleanup, line sorting/deduplication, slug, URL and Base64 encode/decode, HTML entities, JSON formatting, email/URL extraction, ROT13.
- **Developer:** JSON validation and CSV conversion, XML escaping, regex matching/escaping, UUID/password generation, JWT decoding (no signature verification), CSS/JS minification helpers, SQL formatting, timestamps, color conversion, URL parsing, basic Markdown-to-HTML, SHA-256, metadata, robots.txt, JSON-to-XML, query-string parsing.
- **Math:** percentage, average, median, sorting, range, standard deviation, GCD/LCM, prime, factorial, random number, tip/discount/interest, BMI, geometry, and temperature/distance conversions.
- **Converters:** length, weight, volume, speed, time, data size, angle, area, pressure, and energy.
- **Generators:** Lorem Ipsum, random numbers/colors, UUIDs/passwords, username/slug, email signature, HTML boilerplate, CSS reset/shadow/gradient, SEO/Open Graph/schema tags, robots.txt, SQL insert, Markdown table, HTML link, QR payload text, date stamp, palette.

All processing is local to the browser. The SHA-256 tool uses the browser Web Crypto API and therefore requires HTTPS or localhost. Utilities are intentionally lightweight; for example, the JavaScript minifier and Markdown renderer are basic helpers, not full language compilers/spec-complete parsers. JWT decoding does not authenticate or validate a token.

## Deploy

This is a static website and can be deployed to GitHub Pages or any static hosting provider. Configure the host to serve `index.html` at the site root.
