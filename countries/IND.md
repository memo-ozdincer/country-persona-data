# India: data and training examples

[Open annotated example](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=IND)

## Available records by type

| Type | Distinct record IDs |
|---|---:|
| Source records | 2,019 |
| Evidence passages | 272 |
| Recorded actions / responses | 8,265 |
| Curated policy positions | 5 |
| Authored policy applications | 3 |
| Prepared prompt / completion views | 3 |
| Linked decision cases | 2 |

Distinct record IDs within each type and country, across indexed releases. Review/lineage objects are excluded. Translations, segments and derived views can overlap: do not add the rows or treat them as independent trajectories. Shared institutional records appear under each relevant country.

Source languages: ar, en, es, fr, ru, zh.

## Actual authored applications

These are dated, source-grounded review candidates, not authentic historical Q&A or model outputs. None of these new applications is admitted to training.

### What qualifications would India seek to preserve when considering disciplines on harmful fisheries subsidies, according to this report?

Policy date: 2020-11-25. Source language: en.

**Authored target:** The report accepts the need for disciplines on harmful subsidies while emphasizing livelihood protections and policy space for subsistence, artisanal and small-scale fishers. A useful representation must preserve both the discipline and that qualification. [IND-fisheries-subsidies-2020]

**Inspect:** Preserves support for disciplines; Preserves the livelihood and policy-space qualification.

[Official source for IND-fisheries-subsidies-2020](https://www.wto.org/english/tratop_e/tpr_e/g403_e.pdf)

### Does this announcement promise 45% lower total emissions and 50% renewable electricity generation?

Policy date: 2022-08-03. Source language: en.

**Authored target:** No. The 45% target concerns emissions intensity of GDP relative to 2005, not total emissions. The roughly 50% target concerns installed electric-power capacity from non-fossil resources, not the share of electricity generated or renewables alone. Both targets refer to 2030. [IND-climate-2030-2022]

**Inspect:** Distinguishes intensity from absolute emissions; Distinguishes installed capacity from actual generation; Distinguishes non-fossil from renewables-only.

[Official source for IND-climate-2030-2022](https://www.pib.gov.in/Pressreleaseshare.aspx?PRID=1847813&lang=2&reg=48)

### Would requiring every developing country to give up special treatment match this report's position?

Policy date: 2020-11-25. Source language: en.

**Authored target:** No. The report argues that special and differential treatment should remain available to developing countries. It treats voluntary decisions by members able to forgo it as more acceptable, which is different from a universal mandatory waiver. [IND-wto-differential-treatment-2020]

**Inspect:** Preserves voluntary versus mandatory distinction; Attributes the position to this dated report.

[Official source for IND-wto-differential-treatment-2020](https://www.wto.org/english/tratop_e/tpr_e/g403_e.pdf)

## Training representation

[Inspect the field-by-field training format](../docs/EXPLORER_PRESENTATION.md): blue prompt and evidence provide context, green completion receives supervised loss, and review metadata stays alongside the example. Public JSON previews omit source passages; full originals remain in the owner view.
