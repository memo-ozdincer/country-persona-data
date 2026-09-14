# France: data and training examples

[Open annotated example](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=FRA)

## Available records by type

| Type | Distinct record IDs |
|---|---:|
| Source records | 3,163 |
| Evidence passages | 746 |
| Recorded actions / responses | 8,354 |
| Curated policy positions | 4 |
| Authored policy applications | 3 |
| Prepared prompt / completion views | 2 |
| Linked decision cases | 2 |

Distinct record IDs within each type and country, across indexed releases. Review/lineage objects are excluded. Translations, segments and derived views can overlap: do not add the rows or treat them as independent trajectories. Shared institutional records appear under each relevant country.

Source languages: ar, de, en, es, fr, ru, zh.

## Actual authored applications

These are dated, source-grounded review candidates, not authentic historical Q&A or model outputs. None of these new applications is admitted to training.

### What combination of European and Atlantic defence priorities does this review support?

Policy date: 2025-07-14. Source language: en.

**Authored target:** The review combines a stronger European pillar within the Atlantic Alliance with greater European capabilities and a preference for European-made solutions. European autonomy and Atlantic cooperation are presented together. [FRA-european-defence-2025]

**Inspect:** Preserves European capability and procurement priorities; Does not equate autonomy with leaving NATO.

[Official source for FRA-european-defence-2025](https://www.sgdsn.gouv.fr/files/files/Publications/20250713_NP_SGDSN_RNS2025_EN_1_0.pdf)

### Record the climate commitment relevant to France, preserving its institutional scope, metric and dates.

Policy date: 2023. Source language: en.

**Authored target:** The report describes an EU collective target: at least 55% lower net greenhouse-gas emissions by 2030 relative to 1990. It is relevant context for France, but it does not establish a separate, identical French national pledge. [FRA-EU-climate-2030-2023]

**Inspect:** Retains EU attribution; Preserves metric, baseline and target year.

[Official source for FRA-EU-climate-2030-2023](https://www.wto.org/english/tratop_e/tpr_e/g442_e.pdf)

### Does this document let us specify an exact French nuclear-use threshold?

Policy date: 2025-07-14. Source language: en.

**Authored target:** No. It assigns the decision to the President and describes extreme self-defence, while deliberately retaining ambiguity about exact circumstances. A precise trigger would go beyond the published doctrine. [FRA-nuclear-doctrine-2025]

**Inspect:** Separates published doctrine from private decision rules; Does not invent an operational trigger.

[Official source for FRA-nuclear-doctrine-2025](https://www.sgdsn.gouv.fr/files/files/Publications/20250713_NP_SGDSN_RNS2025_EN_1_0.pdf)

## Training representation

[Inspect the field-by-field training format](../docs/EXPLORER_PRESENTATION.md): blue prompt and evidence provide context, green completion receives supervised loss, and review metadata stays alongside the example. Public JSON previews omit source passages; full originals remain in the owner view.
