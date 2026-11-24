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
{ id: 'hkd5', group: 'Hong Kong coins', name: 'HK$5 coin', shape: 'circle', d: 27.0, metal: SILVER, label: '5', src: SRC_HK_COINS },
{ id: 'card', group: 'Cards', name: 'Credit card', shape: 'rect', w: 85.60, h: 53.98, r: 3.18, fill: ['#3b6fd8', '#22408c'], label: 'ISO ID-1 card', src: { text: 'ISO/IEC 7810 ID-1', url: 'https://en.wikipedia.org/wiki/ISO/IEC_7810' } },
```

Every object needs a `src` (`text`, optional `url`); it feeds the in-page Sources list.

Shapes: `circle` (`d`), `scallop` (`d` across the bumps, `dMin` across the dips, `n` bumps), `rect` (`w`, `h`, corner radius `r`).

## Sources, credits and why there are no photos

Every size, its source and the reason the objects are drawn rather than photographed are recorded in [CREDITS.md](CREDITS.md). The page shows the same list under **ⓘ Sources**. When you add an object, fill in its `src` field and add a row to CREDITS.md.

## Your own photo

Press **📷 Photo** to take or pick a photo of the object you're holding. Drag and pinch it until its edge sits on the red outline, then press **Done**. The photo is kept in this browser only (localStorage, downscaled to 1200 px) and never uploaded.

## Hosting

Open the file directly, or turn on GitHub Pages for this repo (Settings → Pages → deploy from branch, root).
