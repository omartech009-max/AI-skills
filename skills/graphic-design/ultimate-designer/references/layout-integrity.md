# Layout integrity: non-negotiable gates

For every page, export, size variant, and language variant, check the **rendered output**, not just source markup. A browser screenshot can reveal problems but cannot certify a print PDF.

## Content integrity

- Every mandatory field from the approved source data appears, with the right product ID, value, units, currency, and image. No invented prices or unapproved rewritten claims.
- Headings, paragraphs, tables, and footnotes are complete. No missing glyphs, widows/orphans that obscure meaning, accidental truncation, or clipped rows. Check long and multilingual strings.
- Headers, page numbers, references, and any cross-page continuation are correct. Verify spread order and product-to-price pairing.

## Geometry and readability

- Set the final page or artboard dimensions *before* composing; derive grids, margins, safe zones, and page-break rules from the actual format and vendor brief.
- Measure bounding boxes and inspect rasterized exports for collisions, overflow, crop of important subjects, missing fonts, and content behind decorative layers.
- A long title or dense specification must trigger a deliberate reflow or additional page. Never solve overflow by silently dropping content, hiding it, or shrinking it below the agreed readable minimum.
- Inspect every page at final size, plus an overview of the whole publication to catch rhythm and consistency errors. Validate pages at content extremes, not only a sample cover.

## Proof versus production

Digital: verify exact pixel dimensions, color profile/export format where specified, transparency, readability at delivery scale, and output weight if constrained.

Print: obtain vendor specifications for trim, bleed, safe area, color space/profile, PDF standard, embedded fonts, spot colors, and minimum effective image resolution. Check the **final PDF** against them, including page boxes and actual placed-image resolution. A 300-DPI tag on a small image does not make an enlarged placement sharp; nominal DPI and automatic CMYK conversion do not establish print readiness.

Stickers: obtain the vendor's cut-line naming/color/offset specification; verify a separate closed vector contour, safe distance between art and cut, and whether white ink or spot layers are required. Do not assume a generic `CutContour` name works for every printer.

If a suitable renderer, PDF inspector, or vendor specification is unavailable, state which gate could not be verified and deliver a clearly labeled proof only. Never report that validation passed without performing it.
