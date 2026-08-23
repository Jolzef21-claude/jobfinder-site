# Job Finder — site

The public site. One static page, no build step, no framework — it is `index.html`
and nothing else, which is the right amount of machinery for a landing page.

## What it is right now

**A waiting list.** Job Finder opens to a small group first, so the page collects
addresses rather than serving a download. When the beta opens, the download
button replaces the email box — the rest of the page does not change.

## To do

1. **Wire up the form.** Create a form (Tally, Formspree, Brevo) and paste its
   address into the `action="#"` on the `<form>` in `index.html`. It is marked
   with a comment, and it is the only line that needs changing.
2. **Add the legal pages** the footer links to: `mentions-legales.html`,
   `confidentialite.html`, `cgv.html`.
3. **Set a real contact address** in the footer, in place of the placeholder.

## Publishing it

GitHub Pages, free, no server to rent:

1. Push this repo to GitHub.
2. Settings → Pages → Source: `main`, folder `/ (root)`.
3. It appears at `https://<username>.github.io/<repo>/` within a minute or two.
4. To use a real domain: add a file called `CNAME` containing just the domain,
   then point the domain's DNS at GitHub. Pages issues the HTTPS certificate
   itself, for free.

## Design

Matches the app on purpose: `#D4FF3F` on `#111111`, Inter, and the same mark —
the two ears and the body triangle, in near-black on its lime tile. That glyph
only reads correctly on lime, so do not put it on a dark background.

Fonts load from Google Fonts here. The app itself bundles Inter locally, because
it has to work offline; a website does not.
