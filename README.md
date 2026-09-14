# Data explorer for persona fine-tuning

A living inventory of country-attributed sources, available trace types and possible training uses.

**[Open the explorer](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html)** · [Contribute](CONTRIBUTING.md) · [Download catalog tables](https://huggingface.co/datasets/memo-ozdincer/country-persona-data)

| Country | Evidence record IDs | Source collections |
|---|---:|---:|
| [China](countries/CHN.md) | 41,632 | 12 |
| [Germany](countries/DEU.md) | 13,561 | 12 |
| [France](countries/FRA.md) | 12,315 | 10 |
| [United Kingdom](countries/GBR.md) | 11,052 | 12 |
| [India](countries/IND.md) | 10,609 | 10 |
| [Brazil](countries/BRA.md) | 11,231 | 10 |

Distinct record_id per country across source records, passages, actions, statistics and curated annotations. Excludes training-format copies, review/lineage, evaluation wrappers and profiles. Each ID is assigned once, preferring its canonical version. Translations and derived spans remain separate IDs; these are not independent training traces.

## Trace and environment inventory

Sources include authentic Q&A, full transcripts, statements, policy evidence, directed UPR recommendations/responses, vote labels and statistics. Expand a source to see its actual field structure and character-length distribution.

**Available:** source records, some question–answer pairs, observed labels, source-grounded authored candidates and sample linked decision cases. **Not built:** interactive environments, multi-agent trajectories, training reward verifiers and preference pairs. A proposed SFT or RLVR mapping is not a ready environment.

## Contribute without cluster access

The public overview runs from committed static files. Source descriptions and trace mappings are editable JSON; generated counts retain their definitions and provenance. See [CONTRIBUTING.md](CONTRIBUTING.md) for local preview, source proposals, corrections and validation.

- [Source descriptions](explorer/source_profiles.json)
- [Trace recipes and field mappings](explorer/trace_types.json)
- [Measured inventory](explorer/sources.json)
- [Data priorities / TODO](TODO.md)
- [Explorer methodology](docs/EXPLORER_PRESENTATION.md)
- [Attribution](ATTRIBUTION.md) · [Source registry](data/source_registry.json) · [Source-use status](data/rights_registry.json)

Original publishers retain attribution. Public previews omit restricted source bodies; source links and record references remain available. The two-event Ukraine decision subset is one small source collection, not the whole corpus.
