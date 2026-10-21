# Vishwakarma Dhama · DKVS website

Static website for **Vishwakarma Dhama**, home of the Dakshina Kannada Vishwa Brahmana Sangha (DKVS), CA-21, Sector A, Satellite Town, Yelahanka, Bengaluru, Karnataka 560064.

Open `index.html` in a browser. There is no build step. It can be hosted on GitHub Pages, Netlify or any static host.

## Adding photos

Put photos in `images/gallery/` named `1.jpg` to `6.jpg`. They show up in the Gallery section on their own, and open full size when clicked. The current six came from visitor photos on the Google Maps listing (see the note under Background photos). To change captions or add more photos, edit the `photos` list near the end of `index.html`.

## Background photos

The photos behind the hero, the Activities section, the booking banner and the footer, and the sanctum photo in the Prarthana section, are in `images/bg/` (`shrine.jpg`, `pooja.jpg`, `diyas.jpg`, `exterior.jpg`, `sanctum.jpg`). They were taken from visitor photos on the DKVS Google Maps listing. Get permission from the photographers, or replace them with the Sangha's own photos, before relying on them. To swap one, keep the same file name.

## 3D effects

- **Hero:** a live 3D scene drawn with [Three.js](https://threejs.org/), loaded from the jsDelivr CDN (version 0.160.0). It shows a golden lotus holding a lit diya under a prabhavali arch, with floating diyas, falling marigold petals and rising embers. The camera follows the mouse and moves in as the page scrolls. The code is the `<script type="module">` at the end of `index.html`. If WebGL or the CDN isn't available, the photo hero with CSS petals shows instead.
- **Rest of the page:** a see-through 3D layer over the page puts ornaments beside each section: a kalasha, diyas, a turning chakra, a lotus lamp, swinging temple bells and a gopura. Marigold petals and embers drift with the scroll. On phones each section gets one ornament, peeking in at its top corner. The `plan` list in `startWorld()` sets which ornament goes where.
- **Sections:** each section leans back slightly in 3D as it moves away from the middle of the screen.
- **Gallery:** the photos sit on a turning 3D ring. Drag, swipe or use the arrows to turn it. Tapping the front photo opens it full size.
- **Cards:** sections swing into place in 3D as you scroll. Cards marked `data-tilt` lean towards the mouse (the number is the largest angle in degrees).

Visitors who set "reduce motion" on their device get a still scene and no tilt or auto-turning.

## English and Kannada

The EN / ಕನ್ನಡ switch in the header changes the page language and remembers the visitor's choice. Links ending in `?lang=kn` open the site in Kannada. English text lives in the HTML; the Kannada text is in the `KN` list near the start of the script in `index.html`. The Kannada translations should be checked by a fluent reader.

## Details to confirm

Online listings don't agree on some details. Please check these with the Sangha office:

- Darshan timings (shown as 6–9 AM and 5–8 PM)
- Office phone number (shown as 080 2271 4294)

## Hosting (GitHub Pages)

The site is served by GitHub Pages at **https://prasheelg.github.io/DKVS/**.

To turn it on (one time): open the repo's **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, pick branch `main` and folder `/ (root)`, then press **Save**. Every push to that branch updates the site within a minute or two.

`.nojekyll` tells GitHub to serve the files as they are, without running Jekyll.
