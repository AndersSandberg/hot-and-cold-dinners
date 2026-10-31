# Hot and Cold Dinners

Companion website for the paper *Hot and Cold Dinners: Poverty Food and Future
Climates*, written for the **Oxford Food and Cookery Symposium 2026** (theme:
poverty food).

The argument: the foods most likely to sustain people through a climate
catastrophe are overwhelmingly the same foods that sustained the world's poorest
for centuries. Hardiness, caloric efficiency, growing in marginal ground and
keeping without refrigeration are what made a food "poverty food", and they are
also what makes a food climate-resilient. Both futures examined here invert the
medieval food hierarchy.

Warming scenarios are presented by Len Fisher; rapid-cooling scenarios by Anders
Sandberg (board member, [ALLFED](https://allfed.info)).

## Pages

| File | Status | Contents |
|---|---|---|
| `index.html` | done | Overview, the thesis, the fish diptych, what both futures share |
| `hot.html` | done | Ingredient table, SSP3-7.0 warming to ~3.6°C by 2100 |
| `cold.html` | done | Ingredient table, abrupt sunlight reduction across four severity tiers |
| `hot-scenario.html` | **to write** | What SSP3-7.0 does and does not say; model caveats |
| `cold-scenario.html` | **to write** | What the ASRS literature does and does not say; model caveats |

The two unwritten pages appear in the navigation marked "(soon)" and are not
clickable on any page, so nothing 404s. Making them live means writing the file
and turning `<a class="soon">` back into an `href` in the three existing pages.

## Structure

```
index.html          overview
hot.html            warming ingredients
cold.html           cooling ingredients
assets/base.css     shared stylesheet — all structural CSS lives here
sources/            the two scenario dossiers the commentary pages draw on
```

Each page carries a short inline `<style>` block setting only its accent
tokens (`--accent`, `--header-bg`, `--row-hover`, `--cat-bg`). Everything else
is in `assets/base.css`, so a new page needs about six lines of CSS. Warm
browns for the hot pages, cool blues for the cold ones, same paper and
typefaces throughout.

Static HTML with no build step. Open a file in a browser, or serve the
directory:

```sh
python3 -m http.server 8000
```

Typefaces (Newsreader, JetBrains Mono) load from Google Fonts; the pages
degrade to Georgia and a default monospace offline.

## Conventions

**Hot page.** Three analytical columns — what the climate allows, what the
system delivers, what reaches the plate. Verdicts are *Gains*, *Declines*,
*Mixed*, *New arrival*, and *Latent*. Latent is reserved for cases where the
barrier is sustained institutional patience rather than knowledge or seed:
orchard lead times, maintained breeding programmes, capital-intensive
processing. It is **not** used for annual field crops, since seed is a one-off
acquisition that multiplies domestically and seventy-five years is ample time
to learn to mill a grain.

Suitability figures in the small monospace lines are index-point changes (0–100
scale) from Redhead et al. (2025), measuring climatic suitability for rain-fed
open-field cultivation at +4 °C. They are **not** yields and **not** production,
and the underlying model excludes irrigation, pests, labour, seed availability,
processing and all protected cropping.

**Cold page.** Four severity tiers from baseline through ~150 Tg soot, with a
status word per cell. Every entry assumes an unprepared, fragmented response;
where preparation or continued trade would change the answer, the cell says so.

Both pages follow the paper's convention that figures quoted per person per day
describe *modelled diet compositions* from global optimisations, not statements
about where the food is grown.

## Corrections carried from earlier drafts

- **Seaweed.** The widely quoted "45% of food supply" figure describes *tropical*
  seaweed farmed at global scale. UK kelp growth under severe cooling was never
  demonstrated, and ocean primary production falls around 37%. Severe-tier
  seaweed is an import.
- **Wheat.** Under low light it lodges — stems collapse — rather than declining
  gradually, and machine-recoverable yield approaches zero even where grain sets.
- **Australia.** The "last breadbasket" result comes from a model that explicitly
  excludes export bans, so the lifeline exists only in the cooperative case.
- **Sorghum** added to the warming table. It is the highest-scoring crop in the
  entire UK suitability study and was absent from every earlier draft.

## Licence

Not yet chosen. Text and tables © the authors pending a decision; source
citations are listed at the foot of each page.
