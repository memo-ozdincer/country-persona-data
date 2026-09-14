# China: data and training examples

[Open annotated example](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=CHN)

## Available records by type

| Type | Distinct record IDs |
|---|---:|
| Source records | 34,330 |
| Evidence passages | 6,165 |
| Recorded actions / responses | 1,089 |
| Curated policy positions | 2 |
| Authored policy applications | 1 |
| Prepared prompt / completion views | 20,428 |
| Linked decision cases | 2 |

Distinct record IDs within each type and country, across indexed releases. Review/lineage objects are excluded. Translations, segments and derived views can overlap: do not add the rows or treat them as independent trajectories. Shared institutional records appear under each relevant country.

Source languages: ar, en, es, fr, ru, zh.

## Actual authored applications

These are dated, source-grounded review candidates, not authentic historical Q&A or model outputs. None of these new applications is admitted to training.

### A proposed development agreement requires the recipient to change its domestic political system. How does that compare with the white paper's stated approach, and can we infer that every Chinese project complies?

Policy date: 2021-01-10. Source language: en.

**Authored target:** That requirement conflicts with the white paper's stated opposition to political strings and interference in a recipient's chosen development path. It also emphasizes recipient leadership of projects. These are published principles; they do not establish the terms or conduct of every Chinese-financed project. [CHN-development-conditions-2021; CHN-development-recipient-leadership-2021]

**Inspect:** Applies the stated condition to the proposal; Attributes the principle to the white paper; Does not turn a government statement into independent proof of compliance.

[Official source for CHN-development-conditions-2021](https://english.mee.gov.cn/Resources/publications/Whitep/202101/P020210122374486901993.pdf)
[Official source for CHN-development-recipient-leadership-2021](https://english.mee.gov.cn/Resources/publications/Whitep/202101/P020210122374486901993.pdf)

## Training representation

[Inspect the field-by-field training format](../docs/EXPLORER_PRESENTATION.md): blue prompt and evidence provide context, green completion receives supervised loss, and review metadata stays alongside the example. Public JSON previews omit source passages; full originals remain in the owner view.
