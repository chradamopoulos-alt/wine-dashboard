# Wine Tasting 2027 — the programme

Five concepts for the 2027 season, replacing a 2026 deck that was prepared but
never ran. In the dashboard as `TASTING_2027`, rendered by the **Tasting 2027**
tab. The concept deck is a separate published artifact.

## What is different from 2026

The 2026 concept failed on sourcing — it named wines the cellar did not hold.
This one starts from the **Ikos Private Cellar**, nineteen labels across France,
Italy, Spain and Greece that are contracted and always in the building.

And the guest builds the flight: one concept, then any five wines from its
list, rather than a fixed sequence.

## The five concepts

| # | Name | Countries | Labels |
| --- | --- | --- | --- |
| 1 | The Regions | France | 16 |
| 2 | Three Coasts | Greece, Italy, Spain | 25 |
| 3 | The Andes | Chile, Argentina, United States | 10 |
| 4 | Southern Ocean | Australia, New Zealand, South Africa | 7 |
| 5 | Deluxe Collection | seven countries | 30 |

Concept five is the fenced set — see [[deluxe-collection]].

**Concept 3 is badly named.** It holds five American wines that are not Andean.
Either rename it or move those wines. Flagged by the sommelier, not yet decided.

## The session

Twelve guests, two sessions a day at 13:00–14:30 and 15:00–17:00, five pours of
50 ml each. That is four bottles a session.

**No Sunday — the sommelier is off.** Saturday is changeover. That leaves five
days for five concepts, so Friday runs two concepts, one per session. Ten
sessions a week, 120 guests, 40 bottles.

Venues: the Deluxe Lobby and Oliva, twice a week for the Deluxe Collection.
Oliva was chosen for a Sunday, when it is quiet; a weekday needs checking
against the restaurant's own service.

## The side plate

Nine bites, 145 g, taken unchanged from the 2026 costing: the `WINE TASTING`
sheet of `IR MASTER WINE LISTS ALLOCATION 2026.xlsx` on SharePoint, rows 3–13.
One plate per guest, the same for every concept.

The **beef carpaccio is 41% of the plate cost** in one line. If the plate ever
has to come down, that is the only line worth touching.

A discrepancy to resolve before printing: the bites slide in the old deck says
15 g of smoked salmon and 15 g of beef carpaccio; the costing says 10 g of each,
and 10 g is what adds up to the stated 145 g total. The costing is right.

## A formula bug in the workbook

`WINE TASTING!F23` reads `=SUM(F17:F21)` where it should read `=SUM(F18:F22)`.
It sums the header row and misses the last wine, understating that scenario by
one serving line per session. The other three scenarios use correct ranges.

Not fixed — it is the user's workbook. Still open.

## Everything is derived

`renderTasting()` computes every figure — label counts, average bottle cost,
cost per guest, Private Cellar counts, weekly totals, food totals — from the
wine and food rows at render time. Nothing is hard-coded. Change a price or add
a label and the totals follow.

The same holds for the Occupancy tab, which sizes this programme against the
season — see [[occupancy-data]].

## Guest material

The printed booklet is reproduced in the same tab, with its problems documented
in [[booklet-review]]. The deck's visual identity comes from
[[corporate-design]].
