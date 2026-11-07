# VeyraTools

VeyraTools is a responsive, static website with **120 browser-based tools** for text, developers, math, unit conversions, and generators.

## Run locally

Open `index.html` in a modern browser, or serve this directory over HTTP (recommended for browser cryptography APIs):

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deploy

The site has no build step, framework, backend, or external runtime dependencies. To deploy with GitHub Pages:

1. In the repository settings, enable Pages and select the `main` branch and `/ (root)` as the publishing source.
2. Add a custom domain only if you own and have configured that domain. The canonical links, sitemap, and robots file currently use `https://veyra.tools/`; update those URLs to your actual public domain before publishing if it differs.
3. Wait for the Pages deployment, then check the site and its `/privacy.html`, `/terms.html`, `/contact.html`, `/sitemap.xml`, and `/robots.txt` URLs.

The repository includes a custom 404 page, SVG favicon, sitemap, robots file, privacy policy, terms of use, and contact page. Static hosting serves `index.html` from the root. Tool views use hash URLs (for example `/#tool/word-counter`), so they work on static hosts without server-side route configuration; search engines generally index the homepage rather than each hash-based tool view as a separate page.

## Tool categories

- **Text:** character/word/line counters, case conversion, reverse, whitespace cleanup, line sorting/deduplication, slug, URL and Base64 encode/decode, HTML entities, JSON formatting, email/URL extraction, ROT13.
- **Developer:** JSON validation and CSV conversion, XML escaping, regex matching/escaping, UUID/password generation, JWT decoding (without signature verification), CSS/JS minification helpers, SQL formatting, timestamps, color conversion, URL parsing, basic Markdown-to-HTML, SHA-256, metadata, robots.txt, JSON-to-XML, query-string parsing.
- **Math:** percentage, average, median, sorting, range, standard deviation, GCD/LCM, prime, factorial, random number, tip/discount/interest, BMI, geometry, and common calculations.
- **Converters:** length, weight, volume, speed, time, data size, angle, area, pressure, and energy.
- **Generators:** Lorem Ipsum, random numbers/colors, UUIDs/passwords, username/slug, email signature, HTML boilerplate, CSS reset/shadow/gradient, SEO/Open Graph/schema tags, robots.txt, SQL insert, Markdown table, HTML link, QR payload text, date stamp, palette.

## Privacy and limitations

Tool inputs are processed in the browser and are not uploaded to a VeyraTools application server. Hosting providers may still process standard server request logs. The site does not require accounts. SHA-256 uses the browser Web Crypto API and requires HTTPS or localhost. Utilities are intentionally lightweight: for example, the JavaScript minifier and Markdown renderer are not full language compilers or spec-compliant parsers, and the JWT decoder does not authenticate or validate a token. Check important outputs independently.
