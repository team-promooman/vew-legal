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
