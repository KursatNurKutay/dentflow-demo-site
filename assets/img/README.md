# Image slots

Drop files with these exact names into this folder and the site will pick
them up automatically — no HTML/CSS changes needed.

| File | Used for |
|---|---|
| `clinic-hero.jpg` | Hero section, right-side photo |
| `clinic-interior.jpg` | About section, clinic interior photo |
| `dr-emre-aslan.jpg` | Doctor card — Dr. Emre Aslan |
| `dr-zeynep-kaya.jpg` | Doctor card — Dr. Zeynep Kaya |
| `dr-mehmet-yildiz.jpg` | Doctor card — Dr. Mehmet Yıldız |

Until a file exists, each slot shows an elegant CSS placeholder instead of a
broken image (see `.photo-frame` / `.photo-fallback` in `css/styles.css`).
Recommended aspect ratios: 4:5 for the hero photo, 4:3 for the interior
photo, 1:1 for doctor photos — matching what's already set in the CSS, so
images will crop via `object-fit: cover` without needing layout changes.
