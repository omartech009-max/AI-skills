---
name: ultimate-designer
description: Art-direct and produce brand-consistent, data-rich still graphics: catalogs, flyers, posters, stickers, product images, and standalone visual components. Use when planning, creating, or reviewing these deliverables; not for websites, interfaces, video, or animation.
license: MIT
---

# Ultimate Designer

This is a graphic-design skill, not an instruction to start production automatically. When the user is gathering ideas, reviewing references, or shaping a brand guide, stay in planning mode. Only generate assets or spend credits after the user requests production.

## Source of truth

1. Read the current project brief, company guide, approved brand assets, and printer/export specifications. The company guide overrides this skill's example directions. Never invent a logo, brand palette, font license, product fact, price, or claim.
2. Read `references/art-direction.md` to establish a visual concept and consistent design tokens. Read `references/layout-integrity.md` for every data-rich or multi-page layout; use `references/output-specs.md` for deliverable requirements.
3. If a necessary source is missing, ask for it or mark the corresponding output as a concept/proof rather than brand-approved or print-ready.

## Choose the right production path

| Need | Preferred path |
|---|---|
| Invent a product or create hero imagery | Explore concepts with local ComfyUI; use OpenArt for selected high-value image generations when available. Keep product identity consistent across views. |
| Repeatable angles, lighting, and materials | If actual 3D is needed, generate an asset with Meshy when available; stage and render stills with Blender Python. Do not spend 3D credits for a flat graphic. |
| Editable vector art, icons, or sticker illustration | Generate real SVG with Recraft when available; validate/edit it locally with Inkscape. A traced raster is a fallback, not proof of clean editable vector art. |
| Finish images | Use Pillow or ImageMagick for crop, compositing, transparency, outlines, size variants, and compression. Do not use raster processing to pretend an image is vector or print-ready. |
| Catalog, flyer, poster, or data-rich composition | Keep text, prices, tables, logos, and required labels as editable layout elements; generate imagery separately. HTML/CSS with a paged-PDF renderer is one possible production route, **not** a website. Choose a renderer that meets the actual output specification. |

These are planned tool roles, not a claim that any API, MCP tool, package, subscription, or print pipeline is installed or verified. Check actual availability and terms before use. Prefer local tools for iteration; estimate paid usage and obtain approval before costly batches. Keep credentials outside source files.

## Brief before composition

Record deliverable type; intended audience; brand guide version; exact copy and data source; required imagery; physical trim size or digital dimensions; output format; printer requirements if any; deadline; and approval point. For invented products, distinguish fictional concept details from supplied product specifications. Ask when facts cannot be verified; do not make a fictional product claim look factual.

Present a small number of distinct art directions grounded in the brief, then agree on a direction before producing a long catalog or a paid batch. Establish one visual system (type roles, palette roles, grid, spacing, imagery treatment, logo rules) with deliberate variations for different formats.

## Data-rich catalog workflow

1. Build a content inventory from the supplied data. Give each product a stable ID and record its image, name, description, price/currency (if supplied), variants, specifications, legal copy, and required disclosures. Track which fields are mandatory; never silently fill gaps.
2. Plan pages and spreads around content capacity: cover, category navigation, product groups, comparison tables, callouts, credits, and back matter as needed. Define reusable page templates and rules for page numbers, running headers, image slots, and item ordering.
3. Compose real text and data in editable layout elements. Generated images are assets, not complete catalog pages with embedded copy. Leave content-linked product images identifiable so the wrong product cannot be paired with a price.
4. Fit without damage: if content overflows, reflow, resize a nonessential image, choose a higher-capacity template, or add a page. Do not clip, hide, omit, rewrite factual copy, or reduce required text to illegibility to force a fit.
5. Render every page and review both individual pages and adjacent spreads at final size. Apply the hard gates in `references/layout-integrity.md`; correct failures and render again. Approval is required before marking a proof final.

For flyers and posters, retain the same brand and information-integrity gates, but optimize for viewing distance and one clear hierarchy. For stickers, distinguish artwork from the cutter's required path and verify both.

## Handoff

Keep editable source, exported proof, and final deliverable distinct. Provide a manifest tying source data IDs to pages/assets and record any missing or unverified requirements. Do not call a file print-ready based only on appearance or a successful screenshot export. Check the actual PDF and printer specifications, or say clearly that production preflight remains pending.

This skill was adapted from the `design`, `brand`, `design-system`, and `banner-design` material in nextlevelbuilder/ui-ux-pro-max-skill. See `LICENSE` for the upstream copyright and permission notice.
