# Germany: data and training examples

[Open annotated example](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=DEU)

## Available records by type

| Type | Distinct record IDs |
|---|---:|
| Source records | 11,273 |
| Evidence passages | 1,413 |
| Recorded actions / responses | 825 |
| Curated policy positions | 3 |
| Authored policy applications | 2 |
| Prepared prompt / completion views | 5,473 |
| Linked decision cases | 2 |

Distinct record IDs within each type and country, across indexed releases. Review/lineage objects are excluded. Translations, segments and derived views can overlap: do not add the rows or treat them as independent trajectories. Shared institutional records appear under each relevant country.

Source languages: ar, de, en, es, fr, ja, pl, pt, ru, uk, zh.

## Actual authored applications

These are dated, source-grounded review candidates, not authentic historical Q&A or model outputs. None of these new applications is admitted to training.

### Assess a proposal to source all critical energy-transition inputs from a single Chinese supplier. Would the stated strategy instead require ending all economic and climate cooperation with China?

Policy date: 2023-07-13. Source language: en.

**Authored target:** The proposal would raise a critical-dependency concern under our 2023 China Strategy: energy-transition inputs are among the areas it identifies for reducing dependence. Diversification would be consistent with that policy, but the source does not determine approval of this particular contract. The strategy seeks to preserve economic ties and cooperate on climate; it does not call for ending all cooperation with China. [DEU-china-economic-dependencies-2023; DEU-china-climate-cooperation-2023]

**Inspect:** Identifies concentration risk as an application of the strategy; Distinguishes de-risking from blanket decoupling; Preserves climate cooperation; Does not invent contract approval or a numeric concentration limit.

[Official source for DEU-china-economic-dependencies-2023](https://www.auswaertiges-amt.de/resource/blob/2608580/49d50fecc479304c3da2e2079c55e106/china-strategie-en-data.pdf)
[Official source for DEU-china-climate-cooperation-2023](https://www.auswaertiges-amt.de/resource/blob/2608580/49d50fecc479304c3da2e2079c55e106/china-strategie-en-data.pdf)

### Record the climate commitment relevant to France, preserving its institutional scope, metric and dates.

Policy date: 2023. Source language: en.

**Authored target:** The report describes an EU collective target: at least 55% lower net greenhouse-gas emissions by 2030 relative to 1990. It is relevant context for France, but it does not establish a separate, identical French national pledge. [FRA-EU-climate-2030-2023]

**Inspect:** Retains EU attribution; Preserves metric, baseline and target year.

[Official source for FRA-EU-climate-2030-2023](https://www.wto.org/english/tratop_e/tpr_e/g442_e.pdf)

## Training representation

[Inspect the field-by-field training format](../docs/EXPLORER_PRESENTATION.md): blue prompt and evidence provide context, green completion receives supervised loss, and review metadata stays alongside the example. Public JSON previews omit source passages; full originals remain in the owner view.
