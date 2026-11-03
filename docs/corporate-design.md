# Ikos corporate design — colour, logos, type

Recovered from the 2026 Wine Tasting deck (`IAR Wine Tasting Concept 1.pptx`)
by unzipping it and reading `ppt/theme/theme1.xml`, the slide masters and
`ppt/media/`. Used for the 2027 concept deck.

## There is no corporate theme in the file

The PowerPoint theme is the stock Office 2007 one — accent1 `#4F81BD`, Calibri,
untouched. Do **not** take the theme colours as corporate. The corporate
identity is carried by the slide content, not the theme.

## The real tokens

| Token | Value | Where it came from |
| --- | --- | --- |
| Ground | white | slide master background, solid `bg1` |
| Primary | `#002060` | the logo's own pixels — a deep navy |
| Body type | Calibri | theme minor font, used throughout |

The logo sits **top right** on every content slide, about 1.86 × 0.54 inches on
a 10 × 7.5 inch page — roughly 19% of the page width.

Two versions exist in the deck:

- navy `#002060` — for white backgrounds
- light `#F0F0F0` — for dark or coloured backgrounds

Both were uploaded to the 2027 deck artifact as assets.

## What was chosen on top, and why

The corporate base is plain, so the 2027 deck keeps it and adds restraint
rather than decoration:

- **Carlito** for body text. It is metric-compatible with Calibri — same
  widths, same rhythm — so the deck stays corporate while using a face that
  loads on any machine. Only weights 400 and 700 exist; do not ask for 500.
- **Cormorant Garamond** for headings. The contrast between a dry corporate
  sans and an elegant serif is the whole visual idea.
- Accents: garnet `#8C2A3E` for wine, sweet wines and the Deluxe Collection;
  gold `#C9A24B` for rules and bars. Gold has too little contrast to be text on
  white — keep it to fills and to navy grounds, where `#D9B45F` works.

## The deck is 4:3

The 2026 original is 10 × 7.5 inches. The 2027 deck was rebuilt at 16:9. If the
corporate template requires 4:3, that has to change.

## The cost tables are linked, not embedded

Slides 22 and 23 hold OLE objects linked to a spreadsheet on a personal
OneDrive. The numbers are not in the file. They survive only as cached `.emf`
renderings in `ppt/media/`, whose text can be extracted by walking the EMF
records for `EMR_EXTTEXTOUTW` (type 84; `nChars` at record offset 44,
`offString` at 48).

That is how the food costing was recovered before the SharePoint workbook was
found. The authoritative copy is the `WINE TASTING` sheet of
`IR MASTER WINE LISTS ALLOCATION 2026.xlsx` — see [[wine-tasting-2027]].
