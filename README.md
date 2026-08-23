# Job Finder — site

The public site. One static page, no build step, no framework — it is `index.html`
and nothing else, which is the right amount of machinery for a landing page.

## What it is right now

**A waiting list, not a download page.** That is deliberate.

The app currently needs each user to supply their own Anthropic API key, because
the relay that holds the key server-side is not live yet. A public download today
would hand strangers something that does not work and cannot be paid for, and
every one of them would email you about it.

So the page collects addresses instead. When the closed beta opens, the download
button replaces the email box — the rest of the page does not change.

## Before it goes live

Three things, all small:

1. **The form does nothing yet.** Create a free form (Tally, Formspree, Brevo)
   and paste its address into the `action="#"` on the `<form>` in `index.html`.
   It is marked with a comment. That is the only line that needs changing.
2. **The footer links point at pages that do not exist.** The four French legal
   documents already exist in the app at `templates/legal.html` — they need
   copying out to `mentions-legales.html`, `confidentialite.html` and `cgv.html`,
   and the 13 `[À COMPLÉTER]` placeholders filling in.
3. **`contact@example.fr`** in the footer is a placeholder. French law requires a
   real contact route on a commercial site.

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
