# United Kingdom: data and training examples

[Open annotated example](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=GBR)

## Available records by type

| Type | Distinct record IDs |
|---|---:|
| Source records | 2,294 |
| Evidence passages | 520 |
| Recorded actions / responses | 8,186 |
| Curated policy positions | 4 |
| Authored policy applications | 3 |
| Prepared prompt / completion views | 3 |
| Linked decision cases | 2 |

Distinct record IDs within each type and country, across indexed releases. Review/lineage objects are excluded. Translations, segments and derived views can overlap: do not add the rows or treat them as independent trajectories. Shared institutional records appear under each relevant country.

Source languages: ar, en, es, fr, ru, zh.

## Actual authored applications

These are dated, source-grounded review candidates, not authentic historical Q&A or model outputs. None of these new applications is admitted to training.

### State the target precisely, including the baseline and exclusions. Is it a GDP-intensity target?

Policy date: 2025-01-30. Source language: en.

**Authored target:** The target is at least an 81% reduction in greenhouse-gas emissions by 2035 relative to 1990, excluding international aviation and shipping. It is an emissions-reduction target, not a reduction in emissions per unit of GDP. [GBR-climate-2035-2025]

**Inspect:** Preserves 81%, 1990 and 2035; Retains aviation/shipping exclusion; Does not confuse emissions with GDP intensity.

[Official source for GBR-climate-2035-2025](https://assets.publishing.service.gov.uk/media/679b655f6bb4c44f0805e7bc/uk-2035-nationally-determined-contribution-large-print.pdf)

### Describe the conditions on cooperation with China in this strategy. What should a policy simulation preserve?

Policy date: 2025-06-24. Source language: en.

**Authored target:** The strategy supports direct engagement and pragmatic cooperation where these serve UK interests, alongside a threat-driven security response. A simulation should preserve the aim of resilient economic growth as well as continuing disagreements and protective measures. [GBR-china-engagement-2025]

**Inspect:** Preserves both engagement and security concerns; Does not invent a blanket disengagement policy.

[Official source for GBR-china-engagement-2025](https://assets.publishing.service.gov.uk/media/685ab0da72588f418862075c/E03360428_National_Security_Strategy_Accessible.pdf)

### What concrete organizational priority does the strategy's NATO-first approach establish?

Policy date: 2025-06-24. Source language: en.

**Authored target:** It prioritizes NATO in how the armed forces plan, invest, train and equip themselves. The passage establishes that organizing priority; it does not determine the answer to every individual procurement or deployment decision. [GBR-nato-first-2025]

**Inspect:** Names concrete planning implications; Does not invent an individual operational decision.

[Official source for GBR-nato-first-2025](https://assets.publishing.service.gov.uk/media/685ab0da72588f418862075c/E03360428_National_Security_Strategy_Accessible.pdf)

## Training representation

[Inspect the field-by-field training format](../docs/EXPLORER_PRESENTATION.md): blue prompt and evidence provide context, green completion receives supervised loss, and review metadata stays alongside the example. Public JSON previews omit source passages; full originals remain in the owner view.
