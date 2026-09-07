# dentflow-demo-site

A static demo/marketing site for **Dr. Aslan Diş Polikliniği**, the fictional
test clinic used to validate [DentFlow](https://github.com/KursatNurKutay/Dentflow)
(a product of Koby Soft). It exists to showcase the DentFlow chat widget in a
realistic clinic-website setting — not to represent a real clinic.

This is deliberately separate from Dentflow's future real marketing site
(that will live in its own repo) and from the DentFlow app itself.

## What's here

- `index.html` — single-page site: hero, clinic intro, treatments, doctors,
  "why us", hours/location, FAQ, contact — plus the embedded DentFlow chat
  widget.
- `css/styles.css` — styling, no build step, no framework.
- `favicon.svg` — simple inline icon.
- `assets/img/` — clinic/doctor photo slots (see that folder's `README.md`
  for exact filenames). Empty slots fall back to a CSS placeholder rather
  than a broken image.

No build tooling, no dependencies — open `index.html` directly in a browser
to preview.

## Content source

Clinic identity, address, hours, doctors, and FAQ content originate from
`docs/clinic-profile.md` in the
[Dentflow](https://github.com/KursatNurKutay/Dentflow) repo, which is the
single source of truth shared with the DentFlow assistant's seed data. The
site's copy has since been rewritten/reorganized for a more polished public
demo presentation (no price table, primarily Turkish, condensed language
list) — if `clinic-profile.md` changes on identity/contact details, update
this site to match.

## Widget embed

The chat widget snippet at the bottom of `index.html` matches
`docs/embed.md` in the Dentflow repo: it points at
`draslandis.testsitehub.com` (DentFlow's backend, deployed on Railway) and
uses `data-ephemeral="true"` since this is a demo/showcase embed rather than
a real clinic's patient-facing site (per `docs/embed.md`'s guidance on when
to use that flag).

## Deployment

Live at `draslandis-demo.testsitehub.com`, deployed on Vercel (project
`dentflow-demo-site` under the Koby Labs Vercel team), same pattern as
RentFlow's `coastlinedrive.testsitehub.com`: DNS lives at Hostinger
(a CNAME record for `draslandis-demo` pointing at Vercel's DNS target),
hosting/SSL is handled by Vercel. Pushing to `main` triggers a redeploy.
