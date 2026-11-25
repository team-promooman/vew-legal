# Vew · فيو — legal pages

Public hosting for the app's privacy policy, terms of use and support page, in
Arabic and English. Required by App Store guideline 5.1.1(i): "All apps must
include a link to their privacy policy in the App Store Connect metadata field
and within the app in an easily accessible manner."

These files are **generated, not written here.** The source is the mobile and
admin applications in the private `vew` repository: the privacy and
terms text lives as data in `@vew/core` so that the site and the app cannot
disagree about what the reader agreed to, and the support page is rendered by
its own route. `scripts/freeze-legal-pages.mjs` renders the real pages and
saves what came back.

**Edit the source, then re-run the generator.** Changes made directly to the
HTML here will be overwritten and will make the site disagree with the app.

Each file is self-contained — stylesheet and images inlined — so any static
host serves them with no build step.

**The home pages and the 404 page** (`index.html` in Arabic, `index-en.html`
in English, `404.html`) come from
`scripts/build-site.mjs` in the same repository. The home page carries the
essential links: the three documents in both languages, account deletion,
the note for stores, and the support email and WhatsApp number as the
support page lists them. `404.html` answers any path that does not exist
on `vew-om.com` with the same links; its links are written from the root,
so it is meant for the custom domain, not the github.io address.

**For search engines.** `robots.txt`, `sitemap.xml`, `favicon.ico` and
`icon-192.png` come from `scripts/build-site.mjs` too, which also gives every
page its one address and both of its languages in the head. The text file with
a long hexadecimal name is the site's IndexNow key: it shows Bing that a list
of changed pages comes from the site itself. `scripts/check-site-search.mjs
--live` checks all of it.

`google5cc2fde05f3e572f.html` is the file Google Search Console asked for
when the site was registered there: it proves that the owner's Google account
controls the site. It has to stay; removing it loses the verification.
