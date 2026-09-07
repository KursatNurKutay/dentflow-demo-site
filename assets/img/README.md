# Image slots

| File | Used for |
|---|---|
| `clinic-exterior.png` | Hero section, right-side photo |
| `clinic-interio.png` | About section, clinic interior photo |
| `dentist-male-1.png` | Doctor card — Dr. Emre Aslan |
| `dentist-female-1.png` | Doctor card — Dr. Zeynep Kaya |
| `dentist-male-2.png` | Doctor card — Dr. Mehmet Yıldız |

The two male doctor photos are visually interchangeable (no name/label in
the images themselves) — `dentist-male-1` was assigned to Dr. Emre Aslan
and `dentist-male-2` to Dr. Mehmet Yıldız in listing order. Swap the two
`<img src>` values in `index.html` if you'd rather match them the other
way.

If a file is ever removed, the site won't break — see `.photo-frame` /
`.photo-fallback` in `css/styles.css` for the graceful fallback shown in
its place.
