# Project notes

Findings, methods and decisions for the IKOS Aria wine dashboard — the things
that would otherwise be re-derived from scratch every session.

`CLAUDE.md` at the root holds the **rules**: what to do, how to test, where to
commit. These notes hold the **knowledge**: how something was worked out, where
the data came from, what was decided and why.

This folder is plain Markdown. It can be opened directly in Obsidian with
*Open folder as vault* — same files, no copy, no sync. `[[wiki links]]` between
the notes work there; on GitHub they render as plain text.

## The notes

- [[deluxe-collection]] — the 30 labels fenced to the deluxe area, and how to
  identify them from the data
- [[occupancy-data]] — where the season's occupancy and guest nights come from,
  and how to pull a month
- [[corporate-design]] — the Ikos corporate colour, logos and typefaces, and
  where they were recovered from
- [[booklet-review]] — what is wrong with the 2025 guest booklet and what the
  2027 edition needs
- [[wine-tasting-2027]] — the five concepts, the week, and the costings behind
  the Tasting tab

## What does not belong here

**This repository is public.** GitHub Pages serves it, and anyone with the link
can read these files. Keep out of this folder:

- guest names and room numbers
- supplier names tied to prices
- anything from the special-requests data

Those belong in Notion. What belongs here is rules, methods, sources and design
decisions — things that are useless to an outsider and essential to the next
session.

Prices are deliberately not listed in these notes. Where a figure matters, the
note points at the code in `index.html` instead.
