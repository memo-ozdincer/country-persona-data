# China (41,632 evidence record IDs)

[Open source explorer](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=CHN)

## Breakdown

| Record type | Distinct IDs |
|---|---:|
| Source records | 34,330 |
| Evidence passages | 6,165 |
| Recorded actions / responses | 1,089 |
| Curated policy positions | 2 |
| Authored policy applications | 1 |
| Prepared prompt / completion views | 20,428 |
| Linked decision cases | 2 |

Distinct record_id per country across source records, passages, actions, statistics and curated annotations. Excludes training-format copies, review/lineage, evaluation wrappers and profiles. Each ID is assigned once, preferring its canonical version. Translations and derived spans remain separate IDs; these are not independent training traces.

Breakdown rows include overlapping representations and must not be summed.

## Data sources

<details><summary>China Ministry of Foreign Affairs (press conferences) (30,034 records)</summary>

Full press-conference transcripts and extracted reporter–spokesperson Q&A. Translations of one conference belong to the same event family.

Languages: en, es, fr, ru, zh. Recorded dates: 2022-06-14 → 2026-09-11.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Authentic question → answer | 21,935 | 5010 / 14955 (n=21935) | 524 / 2382 (n=21935) | Not present / measured |
| Source document / evidence passage | 5,594 | Not present / measured | Not present / measured | 2655.5 / 2972 (n=5594) |
| Full conference document | 2,505 | Not present / measured | Not present / measured | 9582 / 19615 (n=2505) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Authentic question → answer

Existing paired fields; candidate for supervised adaptation after source and quality review.

**Prompt/context:** country_iso3, event_date, speaker; question; history: only turns preceding this answer; context, when available

**Output/target:** text: the actual spokesperson answer

**Use:** SFT or supervised distillation; useful baseline for a country-conditioned adapter.

**Scoring/environment:** Evidence-based review of accuracy, attribution and substantive policy content. No automatic verifier or RL environment supplied.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=8ffa0b1929309fa9f7882192e7231d00685aba1a0251fe76cff232de6532befd)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=ffbe299946105362ee08a3d179595d8d6181b8058477327b0646bd5a51ff2f59)

### Full conference document

Source document; individual Q&A extraction exists for part of this source.

**Prompt/context:** date, institution and speaker boundaries; earlier turns only, if constructing a dialogue

**Output/target:** A selected answer span after extraction; not the entire transcript by default

**Use:** Extract Q&A for SFT; optional continued pretraining after cleaning.

**Scoring/environment:** Check speaker segmentation and event/translation splits; exclude future answers from context.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=c69a25f8d6f13c7c1081554acf9ce7ebb11b80a69e34844ede007db3f8d530e4)

</details>

<details><summary>China Mission to the UN (statements) (1,762 records)</summary>

Published diplomatic statements. A speech is an observed output; its original prompting situation is not necessarily reconstructed.

Languages: en, zh. Recorded dates: 2022-11-30 → 2026-09-11.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Statement / speech reconstruction | 962 | Not present / measured | 3834.5 / 6950 (n=962) | Not present / measured |
| Source document / evidence passage | 800 | Not present / measured | Not present / measured | 847 / 1517 (n=800) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Statement / speech reconstruction

Observed statement text; an instruction may be constructed from metadata.

**Prompt/context:** country, institution, speaking_capacity, event_date; title / agenda and context, when present

**Output/target:** text: attributed statement

**Use:** Statement SFT, retrieval evidence, or optional domain-text training.

**Scoring/environment:** Review speaker, policy fidelity and unsupported commitments. No reward verifier or transition model exists.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=7e365fdcf6f0f5a9e46bcfa49dcc327c424435962d636bdac330d5f4ccbb5852)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=fa64fdc9b6a76f7065eded1e5d51b20a00c4b4b4d2a7762547676a1c1d06edd4)

</details>

<details><summary>National policy documents (China and Germany collection) (77 records)</summary>

Strategy papers, white papers, WTO reports and derived passages in the initial country collection.

Languages: en. Recorded dates: 2021-01-10 → 2024-06-12.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 77 | Not present / measured | Not present / measured | 2960 / 2998 (n=77) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=c524db668d39ccdd76128245951ebd7c79cacf9778d3169d2d26fe5b62ea72dd)

</details>

<details><summary>OHCHR (Universal Human Rights Index) (2,259 records)</summary>

UPR recommendations, reviewed-state response labels and institutional evidence. A recommendation about a country is not necessarily a statement by that country.

Languages: en. Recorded dates: 2008-05-23 → 2026-01-08.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Recommendation from one state to another | 1,171 | 45 / 64 (n=1171) | 136 / 216 (n=1171) | Not present / measured |
| Recommendation → reviewed-state response | 1,088 | 174 / 311 (n=1088) | 9 / 9 (n=1088) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Recommendation from one state to another

Recommendation text and directed state roles exist; earlier review context may be incomplete.

**Prompt/context:** recommending_states → reviewed_states; review cycle, date and document; question / prior review evidence when available

**Output/target:** text: recorded recommendation

**Use:** Directed recommendation SFT or retrieval evidence.

**Scoring/environment:** Check attribution and recommendation grounding; no automatic quality reward is supplied.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=a521e381f4eef3ab025ef78b96fab6a6e1f7d6d598c832e88bc7d89e6b27428c)

### Recommendation → reviewed-state response

Question contains recommendation; text contains the response label.

**Prompt/context:** reviewed_states, recommending_states, cycle and date; question: recommendation text; context: recommending-state information

**Output/target:** text: response such as Supported or Noted

**Use:** Response classification / SFT; possible offline verifiable task after validation.

**Scoring/environment:** Potential exact-match label check, subject to response-date and linkage validation; no reward implementation bundled.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=0a05ae1e041923d3132c18f2939ec6daa7ce623c30b9a74658846600a9a61a7d)

</details>

<details><summary>Project annotations (policy claims and applications) (4 records)</summary>

Project-authored claims and question–evidence–answer applications derived from linked official sources. These are review candidates, not authentic historical dialogue.

Languages: . Recorded dates: 2021-01-10 → 2022-03-02.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Curated policy claim | 2 | Not present / measured | Not present / measured | Not present / measured |
| Authored evidence → policy answer | 1 | 2125 / 2125 (n=1) | 387 / 387 (n=1) | Not present / measured |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Curated policy claim

Attributed claim and source spans; not a complete dialogue.

**Prompt/context:** claim plus source passages as dated context; a separately constructed application question

**Output/target:** No answer target in this claim record

**Use:** Retrieval / dossier context; parent evidence for authored applications.

**Scoring/environment:** Verify source support and scope; published policy does not establish behavior in every real project.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=ef6956bdb20378fd95ff98efd72329225eaa7322dc3aeafa59dd0ea7069294dd)

### Authored evidence → policy answer

Paired messages exist as review candidates; extension also has SFT export files.

**Prompt/context:** messages[0]: system instruction; messages[1]: institution/date, cited evidence and question

**Output/target:** messages[-1]: authored assistant answer

**Use:** Evidence-conditioned SFT candidate; possible later preferences from reviewed errors.

**Scoring/environment:** rubric, source spans, scope and unsupported-claim checks. Review is pending; no automated correctness oracle.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=b6eee3285d84a035b4960a0d2bc02849ad5be275df9d58b2597c938204911434)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=5589ff2d8619f5c0a247fe163459bbdd8bea97ef3b63fe0cd4d6c80486dbb508)

</details>

<details><summary>UN General Assembly (speech corpus) (915 records)</summary>

Upstream speech segments and derived country-attributed text. Some boundaries and speakers remain unverified; meeting text may include several speakers.

Languages: en. Recorded dates: 1993 → 2017-12-20.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Speech segment with unverified boundaries | 466 | Not present / measured | Not present / measured | 4709 / 14179 (n=466) |
| Statement / speech reconstruction | 449 | Not present / measured | 4545 / 12161 (n=449) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Speech segment with unverified boundaries

Text exists; speaker attribution and segment boundaries are not confirmed.

**Prompt/context:** meeting/document metadata; speaker identity must be checked

**Output/target:** No verified target until speaker segmentation is resolved

**Use:** Evidence discovery; not a ready country-specific supervised trace.

**Scoring/environment:** Speaker and boundary verification is a prerequisite.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=73a30cccbbbb1b761976d23b5545665efd656e94845dd74b6f0e2b9cd69c857f)

### Statement / speech reconstruction

Observed statement text; an instruction may be constructed from metadata.

**Prompt/context:** country, institution, speaking_capacity, event_date; title / agenda and context, when present

**Output/target:** text: attributed statement

**Use:** Statement SFT, retrieval evidence, or optional domain-text training.

**Scoring/environment:** Review speaker, policy fidelity and unsupported commitments. No reward verifier or transition model exists.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=0414e2a38f51feef551845c0d21933f1a62811722fb9bc0d8e43a4cbef107eeb)

</details>

<details><summary>UN General Assembly (voting data: UNGA-DM) (6,354 records)</summary>

Recorded vote labels and resolution identifiers. Most rows still lack joined proposal text; they are not complete decision-making environments.

Languages: en. Recorded dates: 1971-11-09 → 2023-09-01.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Recorded vote label | 6,354 | Not present / measured | Not present / measured | 8 / 10 (n=6354) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Recorded vote label

Action label exists; proposal text is generally missing.

**Prompt/context:** country and decision date; decision / draft identifier; MISSING for most rows: actual proposal and contemporaneous context

**Output/target:** original_vote / text: observed vote

**Use:** Classification / SFT after joining context; possible offline verifiable task, not an existing RLVR environment.

**Scoring/environment:** Exact-match scoring is possible only after validating labels and proposal joins. A correct historical vote does not verify a generated explanation.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=b63b991533f7b859cfa623277e207507cccdac968bebd3209ea50f090d4f1836)

</details>

<details><summary>UN General Debate Corpus (76 records)</summary>

General Debate speeches. Keep country, session and speech date together; whole speeches are not dialogue trajectories.

Languages: en. Recorded dates: 1946 → 2022.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Whole speech / domain text | 76 | Not present / measured | Not present / measured | 19612 / 40523 (n=76) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Whole speech / domain text

Source text exists; no instruction–answer pair is inherent in the document.

**Prompt/context:** text: cleaned speech or document; country, speaker, event and language as attribution metadata

**Output/target:** Next-token text continuation if used for continued pretraining; no separate assistant answer provided

**Use:** Retrieval or optional continued pretraining; construct and review tasks before SFT.

**Scoring/environment:** Language-model loss measures text prediction, not policy correctness or negotiation quality. Check attribution and held-out event overlap.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=3cac0e1401136df5c8b13c67fed8863d904d9dfa78459b9085c969c56844397f)

</details>

<details><summary>UN Human Rights Council (UPR national reports) (102 records)</summary>

Country reports and multilingual passages. These are evidence, not automatically verified policy behavior.

Languages: ar, en, es, fr, ru, zh. Recorded dates: 2023-11-03 → 2023-11-03.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 102 | Not present / measured | Not present / measured | 2965.5 / 12658 (n=102) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=5902a876aad9e3735b0751219b9cefd0fe4b8f345871b1771955e2c34810f2b7)

</details>

<details><summary>UN records (joined decision cases) (2 records)</summary>

Twelve country views of two Ukraine resolutions, joining proposals, final votes and available public explanations. Retrospective cases, not a hidden forecast benchmark.

Languages: en. Recorded dates: 2022-03-02 → 2022-10-12.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Proposal → action + public explanation | 2 | Not present / measured | Not present / measured | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Proposal → action + public explanation

Joined retrospective cases; some explanation fields remain missing.

**Prompt/context:** proposal, country and decision date; only information available before the vote for a forecasting task

**Output/target:** observed final vote; public explanation, where available, as a separate retrospective target

**Use:** Supervised decision/explanation tasks after review; offline evaluation, not an interactive environment.

**Scoring/environment:** Vote-label comparison plus evidence-based explanation review. No simulator, transitions or validated negotiation reward supplied.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=6b1f7d46ff43b9539ce5e7607ba6567b2813f761e72f2cbb134844984d711ee8)

</details>

<details><summary>UNBench (linked diplomatic task samples) (4 records)</summary>

Acquired sample records with some draft text and observed outputs. This is not the full upstream benchmark or an interactive environment.

Languages: en. Recorded dates: 2024-10-30 → 2024-11-01.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Statement / speech reconstruction | 4 | 10209 / 21019 (n=4) | 2140 / 4082 (n=4) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Statement / speech reconstruction

Observed statement text; an instruction may be constructed from metadata.

**Prompt/context:** country, institution, speaking_capacity, event_date; title / agenda and context, when present

**Output/target:** text: attributed statement

**Use:** Statement SFT, retrieval evidence, or optional domain-text training.

**Scoring/environment:** Review speaker, policy fidelity and unsupported commitments. No reward verifier or transition model exists.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=da432fc692e27c3e29b6dd61a8cdc4794db1d7b6765dcdd2a5724b2026b0242e)

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

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=5fa0627095121a7c82d30e68bf45ff8929bee8f7e6da479e03acbf472a2412f5)

</details>

## Post-training examples

[Inspect task templates and a worked evidence-conditioned candidate](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=CHN)

No interactive environments, multi-agent trajectories, training reward verifiers or preference pairs are prepared. Some vote/response labels can support future verifiable tasks after validation. New curated applications remain review candidates.
