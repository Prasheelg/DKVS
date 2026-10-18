# Vishwakarma Dhama · DKVS website

Static website for **Vishwakarma Dhama**, home of the Dakshina Kannada Vishwa Brahmana Sangha (DKVS), CA-21, Sector A, Satellite Town, Yelahanka, Bengaluru, Karnataka 560064.

Open `index.html` in a browser. There is no build step. It can be hosted on GitHub Pages, Netlify or any static host.

## Adding photos

Put photos in `images/gallery/` named `1.jpg` to `6.jpg`. They show up in the Gallery section on their own. To change captions or add more photos, edit the `photos` list near the end of `index.html`.

## Details to confirm

Online listings don't agree on some details. Please check these with the Sangha office:

- Darshan timings (shown as 6–9 AM and 5–8 PM)
- Office phone number (shown as 080 2271 4294)

## Hosting (GitHub Pages)

The site is served by GitHub Pages at **https://prasheelg.github.io/DKVS/**.

To turn it on (one time): open the repo's **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, pick branch `main` and folder `/ (root)`, then press **Save**. Every push to that branch updates the site within a minute or two.

`.nojekyll` tells GitHub to serve the files as they are, without running Jekyll.
