# Country Persona Data

**Created and maintained by Memo Ozdincer.**

Dated evidence, public policy positions and recorded decisions for country-persona research.

**[Open the interactive explorer](https://huggingface.co/spaces/memo-ozdincer/country-persona-explorer)** · [Download the tables](https://huggingface.co/datasets/memo-ozdincer/country-persona-data) · [Full research view (owner login)](https://huggingface.co/spaces/memo-ozdincer/country-persona-research)

## Start with substance

- [Compare six countries on the same UN decisions](https://memo-ozdincer-country-persona-explorer.hf.space/#view=compare)
- [Read actual policy positions](https://memo-ozdincer-country-persona-explorer.hf.space/#kind=policy_positions&view=explore)
- [Inspect country statistics](https://memo-ozdincer-country-persona-explorer.hf.space/#kind=country_statistics&view=explore)
- [Read the 12 policy applications](docs/COUNTRY_EXTENSION_EXAMPLES.md)
- [Understand the decision-case format](docs/DECISION_CASE_SCHEMA.md)

## Browse by country

| Country | Distinct record objects with that attribution | Browse |
|---|---:|---|
| [China](countries/CHN.md) | 116,703 | [Open](https://memo-ozdincer-country-persona-explorer.hf.space/#country=CHN&view=explore) |
| [Germany](countries/DEU.md) | 40,071 | [Open](https://memo-ozdincer-country-persona-explorer.hf.space/#country=DEU&view=explore) |
| [France](countries/FRA.md) | 12,341 | [Open](https://memo-ozdincer-country-persona-explorer.hf.space/#country=FRA&view=explore) |
| [United Kingdom](countries/GBR.md) | 11,084 | [Open](https://memo-ozdincer-country-persona-explorer.hf.space/#country=GBR&view=explore) |
| [India](countries/IND.md) | 10,636 | [Open](https://memo-ozdincer-country-persona-explorer.hf.space/#country=IND&view=explore) |
| [Brazil](countries/BRA.md) | 11,258 | [Open](https://memo-ozdincer-country-persona-explorer.hf.space/#country=BRA&view=explore) |

## Coverage and limitations

The catalog indexes **303,951 exact distinct JSON record objects** from **528,093 row occurrences** across **238 files**, plus an inventory of **11,901 source and prepared files**. These counts include overlapping translations, review manifests and alternative training views; they are not independent examples.

**12 decision cases** cover two UN resolutions and six countries. Seven have an attributed statement; five still lack one. Twenty policy records and fifteen authored applications are available across the prototype and extension. New cases are quarantined retrospective demonstrations, not a hidden benchmark or proof of persona quality.

Public downloads contain metadata, factual values and project-authored summaries. Original source bodies and original QA remain in the account-only research view where reuse is unresolved or reserved. Publisher links and attribution remain visible for everyone.

## Documentation

- [Exploration guide, counts and update workflow](docs/DATA_EXPLORER.md)
- [Attribution and source credits](ATTRIBUTION.md)
- [Source registry](data/source_registry.json)
- [Four-country official-source registry](data/country_extension_registry.json)
- [Source-use status](data/rights_registry.json)
- [Generated coverage report](reports/data-catalog.json)

The hosted explorer is static and read-only; it requires no paid compute. It does not call a model or launch training. This is a presentation companion to the original research workspace. Rebuilding requires its private source snapshots and preparation library.
