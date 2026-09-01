# dentflow-demo-site

A static demo/marketing site for **Dr. Aslan Diş Polikliniği**, the fictional
test clinic used to validate [DentFlow](https://github.com/KursatNurKutay/Dentflow)
(a product of Koby Soft). It exists to showcase the DentFlow chat widget in a
realistic clinic-website setting — not to represent a real clinic.

This is deliberately separate from Dentflow's future real marketing site
(that will live in its own repo) and from the DentFlow app itself.

## What's here

- `index.html` — single-page site: clinic info, services/prices, doctors,
  hours/location, FAQ, contact — plus the embedded DentFlow chat widget.
- `css/styles.css` — styling, no build step, no framework.
- `favicon.svg` — simple inline icon.

No build tooling, no dependencies — open `index.html` directly in a browser
to preview.

## Content source

All clinic content (name, address, hours, doctors, prices, FAQ) is copied
verbatim from `docs/clinic-profile.md` in the
[Dentflow](https://github.com/KursatNurKutay/Dentflow) repo, which is the
single source of truth shared with the DentFlow assistant's seed data. If
that file changes, update this site to match.

## Widget embed

The chat widget snippet at the bottom of `index.html` matches
`docs/embed.md` in the Dentflow repo: it points at
`draslandis.testsitehub.com` (DentFlow's backend, deployed on Railway) and
uses `data-ephemeral="true"` since this is a demo/showcase embed rather than
a real clinic's patient-facing site (per `docs/embed.md`'s guidance on when
to use that flag).

## Deployment

Not yet deployed. Per the Dentflow repo's `docs/PLAN.md`, this is meant to
go out on a `testsitehub.com` subdomain (same domain/pattern RentFlow uses
for its test companies) via CNAME, e.g. as a static site host (GitHub
Pages, Netlify, Railway static hosting, etc.) pointed at a `testsitehub.com`
subdomain. Exact host/subdomain still TBD.
