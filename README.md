# DCD Painting redesign

A single-page redesign of dcdpainting.ca, built as a pitch concept. It uses DCD's own services, FAQ answers, photos, logo, phone number and real customer reviews (shortened excerpts).

Concept: "The first coat". The page is a primed wall that DCD paints. The hero is a canvas paint roller that rolls the kitchen photo onto a primer-white wall in two coats. Painter's tape strips peel off at each section boundary as you scroll.

Run it locally:

    python3 -m http.server 8020 --bind 127.0.0.1

Then open http://localhost:8020.

- `index.html`: everything (CSS and JS inline; GSAP, ScrollTrigger and Lenis load from CDN).
- `assets/`: the logo and project photos, downloaded from dcdpainting.ca. The WebP files were converted to JPEG.

Check with DCD before going live:
- **The quote form has no backend, and the current site lists no email.** "Text us the details" opens the visitor's messaging app with a pre-filled text to (519) 890-3932. If DCD would rather get email, swap the `sms:` link in the form handler for a `mailto:` link, or connect a form service.
- The "4.9 from 45 reviews" figure comes from the review widget on their current site (October 2026). Update it as it changes.
- Review excerpts are quoted word for word but shortened, and names are cut to first name plus initial. Get permission or confirm that's fine.
- The Wenge and Cold Foam swatches in Sophia H.'s review card are approximations on screen, not exact paint matches.
- Service area: their pages name Windsor, LaSalle and Kingsville. Confirm whether they want other Essex County towns listed.
- Photo captions describe what's visible in each photo. Confirm them, especially which photos are commercial jobs.
