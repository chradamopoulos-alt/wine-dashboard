# The Deluxe Collection — the 30 fenced labels

Thirty expensive labels were held for the deluxe area for the 2026 season and
were not meant to be poured anywhere else. Through the summer they drifted
outward to the other outlets. They are the basis of concept five in
[[wine-tasting-2027]].

## How to identify them from the data

A label belongs to the Deluxe Collection when its `outlets` array in `MASTER`
contains **`SEASONS` and nothing else**. SEASONS is the deluxe restaurant.

```js
const MASS = ['KOS','OUZO','PROVENCE','FLAVORS','OLIVA','FRESCO','ANAYA'];
MASTER.filter(x => (x.outlets||[]).includes('SEASONS')
               && !(x.outlets||[]).some(o => MASS.includes(o)));
```

That returns exactly 30 rows, which matches the count the user gave
independently. Forty-eight labels list SEASONS in total; the other eighteen are
Ikos Private Cellar bottles poured in six to ten outlets, so they are **not**
part of the collection.

Do not identify them by price. The collection spans €4.15 to €14.44 and several
cheaper labels sit above that floor without being fenced.

## The Peyrassol trap

Two labels share the Peyrassol Méditerranée name and only one is Deluxe:

| Code | Label | Outlets | Deluxe |
| --- | --- | --- | --- |
| `F24001545` | Méditerranée Cinsault-Grenache-Syrah **red** | PROVENCE, FLAVORS, SEASONS | **yes** |
| `F24200379` | Méditerranée Cinsault-Grenache **rosé** | nine outlets | no |

Both carry *IKOS PRIVATE CELLAR* in their ERP description, so the name is not a
guide. The outlets field is. This was got wrong once — the rosé was taken for
the Deluxe one — and the user corrected it.

A third Peyrassol, `Château Peyrassol Côtes de Provence`, is in the collection.
Same house, three labels, four to ten euros: the clearest step-up story on the
list.

## The codes

```
F24300534  F24300535  F24300536  F24102508  F24102509  F24102506
F24102510  F24102507  F24102516  F24102517  F24102521  F24102505
F2410009   F24200379* F24200735  F2420073   F24200737  F24200736
F24002435  F24002437  F24002436  F24002438  F24002289  F24002439
F24002442  F24002441  F24002443  F24002444  F24002434  F24102504
```

\* The list as given by the user contains `F24200379`, but he then corrected it
to `F24001545`. The dashboard and the deck both use the corrected pairing. If
this list is ever used verbatim, make that swap.

Seven countries: France, Italy, Spain, Greece, Germany, New Zealand, Argentina.

## Why it matters operationally

The fence only means something if the collection has somewhere of its own to be
poured. That is the argument for giving it a separate tasting concept rather
than folding its labels into the other four.
