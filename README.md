# After the Fire

A single-page recovery guide for City of Denton residents after a house fire. It walks people through the first 24 hours, utilities, replacing vital documents, financial recovery, and the rebuilding and permit process, with local agency phone numbers and links throughout. It is built to be saved to a phone home screen so a resident can keep it handy during recovery.

**Live site:** https://dentonfire.github.io/After-the-Fire/

## Repo contents

- `index.html` - the recovery guide. This is the page served at the live URL.
- `incident-pdf.html` - a fill-in tool residents use to record their incident number, investigator name, and insurance details, then download a PDF for their records. It is linked from the guide ("My Info" and "Create My Incident Report PDF"). The resident's data stays on their own device.
- `README.md` - this file.

Note: drafts are sometimes named `after-the-fire.html`. The guide must be committed as `index.html` at the repo root to serve at the live URL.

## How it works

- Static HTML. No build step and no server code. GitHub Pages serves the files directly.
- Styling is Tailwind CSS loaded from a CDN, with a small custom color config (navy `#152a40`, red `#bf2726`, yellow `#f9c031`).
- Font is Inter, loaded from Google Fonts.
- The QR code is generated in the browser from an inlined copy of the qrcode-generator library. There is no external QR service. The floating QR button opens a popup with the code, the guide link, and a Copy Link button. If the code cannot draw for any reason, the popup shows the readable link instead.

## Editing and maintenance

- The site URL lives in one place. Search the page for `SITE_URL` and update that single constant if the address ever changes. The QR code, the Copy Link button, and the visible link text all read from it.
- If the URL changes, also update the `og:url` meta tag in the `<head>`. It controls the link preview when the page is shared in a text or on social media.
- The URL path is case-sensitive on GitHub Pages. `After-the-Fire` resolves; `after-the-fire` returns a 404. Keep the casing consistent everywhere.
- Phone numbers and agency links are written directly into the page sections. To change one, edit that section in `index.html`.

## Deployment

1. Commit the guide as `index.html` at the repo root.
2. In the repo, go to Settings, then Pages, and set the source to the main branch root.
3. Confirm the page loads at https://dentonfire.github.io/After-the-Fire/.

## Third-party components

- Tailwind CSS (MIT)
- Inter font (SIL Open Font License)
- qrcode-generator by Kazuhiko Arase (MIT), inlined into the page
- Icons by Icons8
- Background texture from transparenttextures.com

## Maintainer

Captain Hunter Lott
Community Risk Reduction Officer
Support Services Division
Denton Fire Department

Denton Fire Department, 332 E. Hickory St, Denton, TX 76201
Non-Emergency: (940) 349-8840
