# Brazil (11,234 evidence record IDs)

[Open source explorer](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=BRA)

## Breakdown

| Record type | Distinct IDs |
|---|---:|
| Source records | 2,335 |
| Evidence passages | 611 |
| Recorded actions / responses | 8,234 |
| Curated policy positions | 5 |
| Authored policy applications | 4 |
| Prepared prompt / completion views | 3 |
| Linked decision cases | 2 |

Distinct record_id per country across source records, passages, actions, statistics and curated annotations. Excludes training-format copies, review/lineage, evaluation wrappers and profiles. Each ID is assigned once, preferring its canonical version. Translations and derived spans remain separate IDs; these are not independent training traces.

Breakdown rows include overlapping representations and must not be summed.

## Data sources

<details><summary>Brazil FUNAG (foreign-policy compendium) (261 records)</summary>

Compendium of attributed government positions. Preserve the original note’s speaker and date as well as the compendium date.

Languages: pt. Recorded dates: .

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 260 | Not present / measured | Not present / measured | 1837 / 2260 (n=260) |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | 461473 / 461473 (n=1) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=4efd7540ac8506b6b60d3c77abc46cda0b59e2dbd68a6df9b055db10ed345f4a)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=5e2bd260bbe63d2eddaa92027e718ea2c15dd77d48204d02b1320fadd0732536)

</details>

<details><summary>Brazil Ministry of Environment (climate commitment) (65 records)</summary>

Brazil’s nationally determined contribution, with Portuguese source text and derived evidence.

Languages: pt. Recorded dates: 2024-11-13 → 2024-11-13.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 64 | Not present / measured | Not present / measured | 2368.5 / 2520 (n=64) |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | 150781 / 150781 (n=1) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=e68e82addb81a8a7dfe31fe8118b468c8ed46abbb69e0021660486b6abc97163)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=83f3346e7807fc38917ec00680f994b5507f966b58361fde8590a62d5905738d)

</details>

<details><summary>OHCHR (Universal Human Rights Index) (2,198 records)</summary>

UPR recommendations, reviewed-state response labels and institutional evidence. A recommendation about a country is not necessarily a statement by that country.

Languages: en. Recorded dates: 2008-05-22 → 2026-01-08.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Recommendation from one state to another | 1,474 | 45 / 65 (n=1474) | 166 / 301 (n=1474) | Not present / measured |
| Recommendation → reviewed-state response | 724 | 183 / 320 (n=724) | 9 / 9 (n=724) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Recommendation from one state to another

Recommendation text and directed state roles exist; earlier review context may be incomplete.

**Prompt/context:** recommending_states → reviewed_states; review cycle, date and document; question / prior review evidence when available

**Output/target:** text: recorded recommendation

**Use:** Directed recommendation SFT or retrieval evidence.

**Scoring/environment:** Check attribution and recommendation grounding; no automatic quality reward is supplied.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=816834b88bd0ab99d9551f9a48ba8fe789dcd57f0bac92a911d30f6492e92eb3)

### Recommendation → reviewed-state response

Question contains recommendation; text contains the response label.

**Prompt/context:** reviewed_states, recommending_states, cycle and date; question: recommendation text; context: recommending-state information

**Output/target:** text: response such as Supported or Noted

**Use:** Response classification / SFT; possible offline verifiable task after validation.

**Scoring/environment:** Potential exact-match label check, subject to response-date and linkage validation; no reward implementation bundled.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=dc7a6fd1a19afbc895884dfae5753ca9ac2b84341e0eebc6217c7a43b6073927)

</details>

<details><summary>Project annotations (policy claims and applications) (13 records)</summary>

Project-authored claims and question–evidence–answer applications derived from linked official sources. These are review candidates, not authentic historical dialogue.

Languages: en, pt. Recorded dates: 2022-03-02 → 2025-07-08.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Curated policy claim | 5 | Not present / measured | Not present / measured | Not present / measured |
| Authored evidence → policy answer | 4 | 1153 / 3580 (n=4) | 284.5 / 339 (n=4) | Not present / measured |
| Source document / evidence passage | 4 | Not present / measured | Not present / measured | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Curated policy claim

Attributed claim and source spans; not a complete dialogue.

**Prompt/context:** claim plus source passages as dated context; a separately constructed application question

**Output/target:** No answer target in this claim record

**Use:** Retrieval / dossier context; parent evidence for authored applications.

**Scoring/environment:** Verify source support and scope; published policy does not establish behavior in every real project.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=b51987f18afb02860fecaa4f5f39f0949ec9b13b01de7102cf3d6c42252eb41a)

### Authored evidence → policy answer

Paired messages exist as review candidates; extension also has SFT export files.

**Prompt/context:** messages[0]: system instruction; messages[1]: institution/date, cited evidence and question

**Output/target:** messages[-1]: authored assistant answer

**Use:** Evidence-conditioned SFT candidate; possible later preferences from reviewed errors.

**Scoring/environment:** rubric, source spans, scope and unsupported-claim checks. Review is pending; no automated correctness oracle.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=5763eb0252ee7eec58cb0cb20cef6f8915124074fdfc4beda49a389f484793b8)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=15543bb9f15537d131f985ed85db0a151126085d84f26ae2920584d6834e5f64)

</details>

<details><summary>UN General Assembly (speech corpus) (849 records)</summary>

Upstream speech segments and derived country-attributed text. Some boundaries and speakers remain unverified; meeting text may include several speakers.

Languages: en. Recorded dates: 1993 → 2018.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Speech segment with unverified boundaries | 435 | Not present / measured | Not present / measured | 4976 / 14150 (n=435) |
| Statement / speech reconstruction | 414 | Not present / measured | 4877 / 12609 (n=414) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Speech segment with unverified boundaries

Text exists; speaker attribution and segment boundaries are not confirmed.

**Prompt/context:** meeting/document metadata; speaker identity must be checked

**Output/target:** No verified target until speaker segmentation is resolved

**Use:** Evidence discovery; not a ready country-specific supervised trace.

**Scoring/environment:** Speaker and boundary verification is a prerequisite.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=5385dbf801212046f08b27d80759455e7ebd73286139e9e223796d6d7e04810a)

### Statement / speech reconstruction

Observed statement text; an instruction may be constructed from metadata.

**Prompt/context:** country, institution, speaking_capacity, event_date; title / agenda and context, when present

**Output/target:** text: attributed statement

**Use:** Statement SFT, retrieval evidence, or optional domain-text training.

**Scoring/environment:** Review speaker, policy fidelity and unsupported commitments. No reward verifier or transition model exists.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=5424dc135c77400485fc5be23d7936b797427702e3ebbfef88cfdfcf1a94029c)

</details>

<details><summary>UN General Assembly (voting data: UNGA-DM) (7,509 records)</summary>

Recorded vote labels and resolution identifiers. Most rows still lack joined proposal text; they are not complete decision-making environments.

Languages: en. Recorded dates: 1946-01-26 → 2023-09-01.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Recorded vote label | 7,509 | Not present / measured | Not present / measured | 8 / 10 (n=7509) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Recorded vote label

Action label exists; proposal text is generally missing.

**Prompt/context:** country and decision date; decision / draft identifier; MISSING for most rows: actual proposal and contemporaneous context

**Output/target:** original_vote / text: observed vote

**Use:** Classification / SFT after joining context; possible offline verifiable task, not an existing RLVR environment.

**Scoring/environment:** Exact-match scoring is possible only after validating labels and proposal joins. A correct historical vote does not verify a generated explanation.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=492d45b4d2baf4d18c5a1fb50fc30e43b269feb09e6d027fcde11c905f0009f1)

</details>

<details><summary>UN Human Rights Council (UPR national reports) (197 records)</summary>

Country reports and multilingual passages. These are evidence, not automatically verified policy behavior.

Languages: ar, en, es, fr, ru, zh. Recorded dates: 2022-09-01 → 2022-09-01.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 191 | Not present / measured | Not present / measured | 1844 / 2800 (n=191) |
| Source document / evidence passage | 6 | Not present / measured | Not present / measured | 67556 / 73272 (n=6) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=b83a9fc652e886c4d962a0a22eee72c18ef2a939d50a96085412615ff837f672)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=88038b67f9431650d70460065a0f461ee489bc96c3af779308b3ad24580dfd06)

</details>

<details><summary>UN records (joined decision cases) (2 records)</summary>

Twelve country views of two Ukraine resolutions, joining proposals, final votes and available public explanations. Retrospective cases, not a hidden forecast benchmark.

Languages: en. Recorded dates: 2022-03-02 → 2022-10-12.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Proposal → vote + optional statement | 2 | Not present / measured | Not present / measured | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Proposal → vote + optional statement

Joined retrospective cases; some explanation fields remain missing.

**Prompt/context:** proposal, country and decision date; only information available before the vote for a forecasting task

**Output/target:** observed final vote; attributed statement, where available and correctly classified, in a separate retrospective task

**Use:** Supervised decision/explanation tasks after review; offline evaluation, not an interactive environment.

**Scoring/environment:** Vote-label comparison plus evidence-based explanation review. No simulator, transitions or validated negotiation reward supplied.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=3ede541b9a969e8011bbc82548efba11442dfe96b9403d210fe14cd2abd2e840)

</details>

<details><summary>World Bank (World Development Indicators) (43 records)</summary>

Country–indicator–year observations, including missing cells. Values are dated facts, not preference or action labels.

Languages: . Recorded dates: 2020 → 2024.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Country–indicator–year observation | 43 | Not present / measured | Not present / measured | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Country–indicator–year observation

Structured values and missingness flags; not a conversational trace.

**Prompt/context:** indicator definition, country, reference_year, unit and database vintage; value as evidence, unless that value is the prediction target

**Output/target:** No policy-action target; a numeric extraction task could use value as the target

**Use:** Structured retrieval; candidate factual extraction exercises, not a country-preference reward.

**Scoring/environment:** Potential numeric/unit checks for newly constructed tasks. No RLVR task generator or evaluator is implemented.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=af49ed81ceb309f26efd22fb5a8e38537cbd84388862b7c6f01e3858afc7d566)

</details>

<details><summary>World Trade Organization (government policy reports) (97 records)</summary>

Government reports supplied for WTO trade-policy reviews. Preserve the government’s stated position and its publication date.

Languages: en. Recorded dates: 2022-10-19 → 2022-10-19.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 96 | Not present / measured | Not present / measured | 2319 / 2800 (n=96) |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | 209685 / 209685 (n=1) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=db2a9ec27ecf1d6f9d66d2250bf4152723ddcf646195adeb681e11b214a504df)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=68eb1bd1d45cd8bccd3f20adb6e52e86a6f69b6b37b9ffe0bba0654d94a3d819)

</details>

## Post-training examples

[Inspect task templates and a worked evidence-conditioned candidate](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=BRA)

No interactive environments, multi-agent trajectories, training reward verifiers or preference pairs are prepared. Some vote/response labels can support future verifiable tasks after validation. New curated applications remain review candidates.
