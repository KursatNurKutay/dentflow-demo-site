# Image slots

| File | Used for |
|---|---|
| `clinic-exterior.jpg` | Hero section, right-side photo |
| `clinic-interio.jpg` | About section, clinic interior photo |
| `dentist-male-1.jpg` | Doctor card — Dr. Emre Aslan |
| `dentist-female-1.jpg` | Doctor card — Dr. Zeynep Kaya |
| `dentist-male-2.jpg` | Doctor card — Dr. Mehmet Yıldız |

These were uploaded as full-resolution PNGs (1.3–1.7MB each, ~7.5MB total)
and were the main cause of slow image loads on the live demo. They've been
resized to what's actually displayed (1200px wide for the two clinic
photos, 900px for doctor photos — plenty for retina at their rendered
size) and re-encoded as JPEG (quality 80), bringing the total down to
~330KB. If you add a new photo, resize/compress it the same way before
committing rather than dropping in a raw camera/stock-photo export:

```
convert source.png -resize '1200x>' -strip -sampling-factor 4:2:0 -quality 80 clinic-exterior.jpg
```

The two male doctor photos are visually interchangeable (no name/label in
the images themselves) — `dentist-male-1` was assigned to Dr. Emre Aslan
and `dentist-male-2` to Dr. Mehmet Yıldız in listing order. Swap the two
`<img src>` values in `index.html` if you'd rather match them the other
way.

If a file is ever removed, the site won't break — see `.photo-frame` /
`.photo-fallback` in `css/styles.css` for the graceful fallback shown in
its place.
