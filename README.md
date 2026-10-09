# Inline NTE forms

Eleven complete forms for pasting into Squarespace HTML Code blocks, plus the staff-form chooser and two thank-you pages. Each `.txt` file contains its HTML, CSS, configuration and JavaScript.

**Current target: Mission Motorsport MMUAT Salesforce sandbox.**

[Download and open the forms](https://stevostar1234.github.io/inline-nte-forms/) · [Download all code blocks](https://stevostar1234.github.io/inline-nte-forms/nte-squarespace-code-blocks.zip) · [Installation instructions](INSTALL.txt)

The form fields, validation, prices, declarations, booking references, payload mapping and submission engine come from the existing [NTE forms](https://github.com/stevostar1234/nte27-web-to-lead-demo). Logo URLs keep using that site's public PNGs. Demo email-preview panels are excluded from the blocks supplied for applicant pages.

## Files

- `code-blocks/`: paste the whole contents of the required `.txt` file.
- `previews/`: the exact same blocks wrapped in ordinary pages for inspection.
- `source/`: the frozen public form source used to generate the blocks.
- `source-manifest.json`: source commit and SHA-256 hashes.
- `hosting.json`: optional final page URLs and per-page thank-you URLs.
- `scripts/`: repeatable build and packaging tools.
- `tests/`: source parity and real-browser comparison checks.
- `docs/`: supplier maintenance and verification notes.

## Rebuild

Node.js 22 or later and Python 3 are sufficient for the build and ZIP; no build dependencies are downloaded.

```sh
node scripts/build.mjs
node tests/parity.mjs
python3 scripts/package.py
```

Browser tests additionally use Playwright and pngjs. Serve the repository over loopback, then run `node tests/browser.mjs`. Set `NTE_TEST_URL` if the server is not at `http://127.0.0.1:8766`, and `NTE_BROWSER_EXECUTABLE` to use an installed browser. These tests intercept native form submissions and block Salesforce requests.

The final published Squarespace installation still needs a check on the actual client site; local previews do not establish its plan, page layout or navigation settings. See [verification](docs/VERIFICATION.md) and [production handover](docs/MAINTENANCE.md).
