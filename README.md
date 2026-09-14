# Country Persona Data

**Created and maintained by Memo Ozdincer.**

Dated government positions, concrete policy questions and the evidence behind each answer.

**[Open the country overview](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html)** · [Download public tables](https://huggingface.co/datasets/memo-ozdincer/country-persona-data) · [Full research view (owner login)](https://huggingface.co/spaces/memo-ozdincer/country-persona-research)

## Characteristic examples

| Country | Featured policy question | Authored application records |
|---|---|---:|
| [China](countries/CHN.md) | A proposed development agreement requires the recipient to change its domestic political system. How does that compare with the white paper's stated approach, and can we infer that every Chinese project complies? | 1 |
| [Germany](countries/DEU.md) | Assess a proposal to source all critical energy-transition inputs from a single Chinese supplier. Would the stated strategy instead require ending all economic and climate cooperation with China? | 2 |
| [France](countries/FRA.md) | What combination of European and Atlantic defence priorities does this review support? | 3 |
| [United Kingdom](countries/GBR.md) | State the target precisely, including the baseline and exclusions. Is it a GDP-intensity target? | 3 |
| [India](countries/IND.md) | What qualifications would India seek to preserve when considering disciplines on harmful fisheries subsidies, according to this report? | 3 |
| [Brazil](countries/BRA.md) | Distinguish the position this report describes for Brazil itself from the treatment it supports for other developing members. | 4 |

There are **15 distinct authored applications** and **20 policy positions** across the six countries. A joint EU application appears under both France and Germany; do not sum country rows. More authored examples appear on each country page.

## What is ready, and what is missing

Source records, evidence passages, observed actions and prepared training views have different units and overlap. The country pages show distinct record IDs by type, excluding review/lineage objects from the displayed counts. They are not counts of independent training trajectories.

**The Ukraine-only comparison was a presentation problem:** only 12 fully joined country–decision cases exist, covering two Ukraine resolutions. That limited subset no longer defines the landing page. It remains available in the full catalog with explicit coverage labeling. No additional decision events are claimed.

The new authored examples are not admitted to training. No preference pairs or multi-agent trajectories are prepared. The next evidence-conditioned LoRA experiment should follow review, a retrieval baseline, and evaluation on separate event families. The earlier China/Germany pilot is a separate release.

## Inspect the recipe and data

- [Annotated training fields and count definitions](docs/EXPLORER_PRESENTATION.md)
- [Public overview JSON, including redacted format previews](explorer/overview.json)
- [Full searchable catalog](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html)
- [Exploration guide](docs/DATA_EXPLORER.md)
- [Four-country authored examples](docs/COUNTRY_EXTENSION_EXAMPLES.md)
- [Attribution](ATTRIBUTION.md) · [Source registry](data/source_registry.json) · [Source-use status](data/rights_registry.json)

Public downloads contain metadata, factual values and project-authored summaries. Original source bodies remain in the account-only research view where reuse is unresolved or reserved. Publisher links remain visible. Static hosting uses no GPU compute.
