# Credits and sources

This file records where every asset and every size in RealSize comes from, so the project can show it has the right to use each one. The in-page **ⓘ Sources** dialog is generated from the `src` field of each object in `REFS` (in `index.html`); keep this file and that field in step.

## Bundled assets

| Asset | Made by | Licence / permission | Notes |
|---|---|---|---|
| Reference object drawings (coins, card, banknote, phone, custom) | RealSize, drawn in code as inline SVG | Original work of this project | Plain outlines, flat colours and a number label only. No coin, banknote, card or product artwork is traced or copied. |
| Paper, grid, rulers, UI | RealSize | Original work of this project | |
| Fonts | None bundled | n/a | Uses the device's own system font (`system-ui`). |
| Icons (📷 ⟳ 🔓 ⓘ) | None bundled | n/a | Unicode characters drawn by the device's own emoji font. |
| Photos | None bundled | n/a | See "User photos" below. |
| Third-party code | None | n/a | No scripts, stylesheets or images are loaded from other sites. |

## Size sources

Sizes are facts and are not protected by copyright, but each one is recorded here so it can be re-checked.

| Object | Size (mm) | Source | Checked |
|---|---|---|---|
| HK$5 coin | Ø 27.0 | [Wikipedia: Coins of the Hong Kong dollar](https://en.wikipedia.org/wiki/Coins_of_the_Hong_Kong_dollar). HKMA does not publish diameters online. Metals and edges checked against the [HKMA security features leaflet](https://www.hkma.gov.hk/media/eng/doc/key-functions/monetary-stability/notes-and-coins/Leaflet_e.pdf). | 2026-11-16 |
| HK$10 coin | Ø 24.0 (inner brass Ø 17.0) | same as above | 2026-11-16 |
| HK$2 coin | Ø 26.3–28.0 (scalloped) | same as above | 2026-11-16 |
| HK$1 coin | Ø 25.5 | same as above | 2026-11-16 |
| HK 50¢ coin | Ø 22.5 | same as above | 2026-11-16 |
| HK 20¢ coin | Ø 18.0–19.0 (scalloped) | same as above | 2026-11-16 |
| HK 10¢ coin | Ø 17.5 | same as above | 2026-11-16 |
| Credit / Octopus / ID card | 85.60 × 53.98, corner r 3.18 | ISO/IEC 7810 ID-1 ([summary](https://en.wikipedia.org/wiki/ISO/IEC_7810)) | 2026-11-16 |
| HK$100 note, 2018 series | 153 × 76.5 | [HKMA 2018 New Series leaflet](https://www.hkma.gov.hk/media/eng/doc/key-functions/money/notes-and-coins/design-and-security/2018/Leaflet_Eng.pdf) | 2026-11-16 |
| iPhone 16 | 147.6 × 71.6 | [Apple tech specs](https://support.apple.com/121029). Corner radius is not published; 10 mm is an estimate. | 2026-11-16 |

## Why the drawings are plain

- **Coins.** HK coin designs belong to the HKSAR Government. Reproducing them needs an application to the Information Services Department ([HKMA: reproduction of coins](https://www.hkma.gov.hk/eng/key-functions/money/hong-kong-currency/reproduction-of-hong-kong-currency/reproduction-of-hong-kong-coins)). RealSize draws only a circle (or scalloped outline) in silver or brass with the face value as a number.
- **Banknotes.** Reproducing HK banknotes needs consent from the issuing bank ([HKMA: reproduction of notes](https://www.hkma.gov.hk/eng/key-functions/money/hong-kong-currency/reproduction-of-hong-kong-currency/reproduction-of-hong-kong-notes/)). RealSize draws a plain red rectangle labelled "HK$100" with no note artwork, so it is not a reproduction of the note.
- **Phones and cards.** Product photos and logos belong to their makers. RealSize draws a plain rounded rectangle. No Apple, bank or Octopus logos are shown.

## Trademarks

iPhone is a trademark of Apple Inc. Octopus is a trademark of Octopus Cards Limited. These names are used only to identify which real object to hold against the screen. RealSize is not affiliated with or endorsed by Apple, Octopus Cards Limited, the HKMA or the HKSAR Government.

## User photos

The 📷 Photo button lets a user add their own photo of the object they hold. The photo is downscaled and kept only in that browser's `localStorage`; it is never uploaded or shared by RealSize. For banknotes, the page reminds the user not to print or share a real-size copy.

## Adding a new reference object

1. Take the size from an official source (maker's spec sheet, issuing authority, or a standard). Use an encyclopedia only when no official figure is published, and say so.
2. Draw it as a plain shape in `REFS`. Don't trace or embed photos, logos or artwork.
3. Fill in its `src` field (text and URL) in `index.html`.
4. Add a row to the "Size sources" table above with the date you checked it.
5. If you ever bundle an image, font or library, add a row to "Bundled assets" with its source URL, author and licence, and keep a copy of the licence page (or its archive.org link).
