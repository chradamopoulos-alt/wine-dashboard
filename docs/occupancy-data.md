# Occupancy and guest nights — where the data lives

The season's occupancy is the denominator for every per-guest figure: wine
despatched, F&B cost, tasting programme reach. It is not in SharePoint and not
in the ERP. It arrives by email.

The result is in the dashboard as `OCCUPANCY_2026`, rendered by the
**Occupancy 2026** tab.

## The source

Every night the PMS sends a **Night Report** from
`iarnightauditor@ikosresorts.com`. Attached to it is a PDF called
`History and Forecast <Month>.pdf` — one page, the whole month, day by day.

Columns worth knowing:

| Column | Meaning |
| --- | --- |
| Total Occ. | rooms occupied that night |
| **Adl. & Chl.** | **guests in house that night — the guest-night figure** |
| Occ.% | occupancy |
| Average Rate | ADR |
| Arr. / Dep. Rooms | arrivals and departures |

The totals row at the top of the PDF gives the month in one line.

## The catch when pulling a past month

**A month's PDF stops being attached once the month closes.** The nightly report
carries the current month and the next one as forecast, not the previous ones.
So for a finished month, take the **last report issued inside that month** — it
holds actuals for all but the final day or two, with those last days as
forecast. At 95%+ occupancy that tail is a safe estimate; note it when you use
it.

September and October 2026 are the exception: both were regenerated after month
end and appear complete in the 1 November report.

## How to find one

The PDF text is indexed by Outlook search, so search the filter line rather than
the filename:

```
query: "From Date 01/06/26"
```

That returns every report carrying the June PDF. Pick the latest, read the
message to get the attachment URI, then read the attachment.

## Read the ratio with care

`Adl. & Chl.` counts **adults and children together**. The PMS does not split
them. This distorts any per-guest figure across the season:

- August runs **3.00** guests per room — the most children
- September runs **2.26** — the fewest

So a per-guest-night figure understates August and overstates September. August
2026 shows the fewest wine despatches since April on the most guests of the
year, and the child mix is the leading explanation.

The monthly Night Report `.xlsx` may split adults from children; worth checking
if the distinction ever has to be exact.

## Do not use the Night Report xlsx for this

`Night Report - <Month>.xlsx` attached to the same email is **a guest complaints
log** — names, room numbers, rates, full incident text. It is not occupancy
data. Do not read it, do not copy it, and keep it out of any file in this
repository.

## 2026 season, for reference

23 April to 31 October, 192 days open. 65,953 room nights, **174,246 guest
nights**, 908 guests in house on an average night. The per-month figures are in
`OCCUPANCY_2026` in `index.html`.

## The gap

`CONSUMPTION_2026` covers April to August only — the `ΑΝΑΛΩΣΕΙΣ` sheet of the
ERP export has five month columns. September and October hold 52,098 guest
nights, 30% of the season. Nothing about full-season consumption closes until
those are exported.

Related: [[wine-tasting-2027]] sizes the tasting programme against these numbers.
