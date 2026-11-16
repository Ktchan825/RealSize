# RealSize

See any dimension at true size on your screen. One self-contained `index.html`, no build step.

1. Enter a width and height (mm, cm or in), or pick a preset (A4, Letter, 4R photo…).
2. Pick a reference object you have in hand, e.g. a HK$5 coin (Ø 27.0 mm) or a credit card.
3. Hold the real object against the screen and zoom (slider, −/+, pinch, or mouse wheel) until the on-screen one matches exactly.
4. Press **Lock**. The paper is now drawn at real size. Drag the reference around the paper to compare.

The scale (CSS px per mm) is saved in `localStorage`, so you only calibrate once per device and browser zoom level.

## Adding reference objects

Edit the `REFS` array near the top of the script. Sizes are in millimetres:

```js
{ id: 'hkd5', group: 'Hong Kong coins', name: 'HK$5 coin', shape: 'circle', d: 27.0, metal: SILVER, label: '5' },
{ id: 'card', group: 'Cards', name: 'Credit card', shape: 'rect', w: 85.60, h: 53.98, r: 3.18, fill: ['#3b6fd8', '#22408c'], label: 'ISO ID-1 card' },
```

Shapes: `circle` (`d`), `scallop` (`d` across the bumps, `dMin` across the dips, `n` bumps), `rect` (`w`, `h`, corner radius `r`).

## Where the sizes come from

| Object | Size | Source |
|---|---|---|
| HK coins | 10¢ 17.5, 20¢ 18.0–19.0, 50¢ 22.5, $1 25.5, $2 26.3–28.0, $5 27.0, $10 24.0 mm | [Wikipedia: Coins of the Hong Kong dollar](https://en.wikipedia.org/wiki/Coins_of_the_Hong_Kong_dollar). HKMA doesn't publish diameters online. Metals and edges checked against the [HKMA security features leaflet](https://www.hkma.gov.hk/media/eng/doc/key-functions/monetary-stability/notes-and-coins/Leaflet_e.pdf). |
| HK$100 note (2018 series) | 153 × 76.5 mm | [HKMA 2018 New Series leaflet](https://www.hkma.gov.hk/media/eng/doc/key-functions/money/notes-and-coins/design-and-security/2018/Leaflet_Eng.pdf) |
| Credit / ID card | 85.60 × 53.98 mm, r 3.18 mm | ISO/IEC 7810 ID-1 |
| iPhone 16 | 147.6 × 71.6 mm | [Apple tech specs](https://support.apple.com/121029). Corner radius is an estimate. |

## Your own photo

Press **📷 Photo** to take or pick a photo of the object you're holding. Drag and pinch it until its edge sits on the red outline, then press **Done**. The photo is kept in this browser only (localStorage, downscaled to 1200 px) and never uploaded.

## Why there are no bundled photos

Reference objects are drawn, not photographed. The HK coin designs belong to the HKSAR Government, and using their image needs an application to the Information Services Department ([HKMA](https://www.hkma.gov.hk/eng/key-functions/money/hong-kong-currency/reproduction-of-hong-kong-currency/reproduction-of-hong-kong-coins)). Banknote images need consent from the issuing bank ([HKMA](https://www.hkma.gov.hk/eng/key-functions/money/hong-kong-currency/reproduction-of-hong-kong-currency/reproduction-of-hong-kong-notes/)). Apple product photos are Apple's copyright. I also looked for public-domain or CC0 photos of common objects (cards, cans, paper) and found none usable: calibration needs a straight-down shot cropped exactly to the edge, and free stock photos are angled, padded, or carry brand marks.

## Hosting

Open the file directly, or turn on GitHub Pages for this repo (Settings → Pages → deploy from branch, root).
