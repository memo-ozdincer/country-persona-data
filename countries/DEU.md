# Germany — 13,561 evidence record IDs

[Open source explorer](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=DEU)

## Breakdown

| Record type | Distinct IDs |
|---|---:|
| Source records | 11,273 |
| Evidence passages | 1,413 |
| Recorded actions / responses | 825 |
| Curated policy positions | 3 |
| Authored policy applications | 2 |
| Prepared prompt / completion views | 5,473 |
| Linked decision cases | 2 |

Distinct record_id per country across source records, passages, actions, statistics and curated annotations. Excludes training-format copies, review/lineage, evaluation wrappers and profiles. Each ID is assigned once, preferring its canonical version. Translations and derived spans remain separate IDs; these are not independent training traces.

Breakdown rows include overlapping representations and must not be summed.

## Data sources

<details><summary>German Federal Foreign Office — policy documents — 1,336 records</summary>

Ministry documents and derived policy passages.

Languages: de, en. Recorded dates: 2023-02-13 → 2026-09-08.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 1,336 | Not present / measured | Not present / measured | 2612 / 8168 (n=1336) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=5948946bdfa28bfcd42465566a5a2abff05e7634ed4a8a30dea3d330d6615ad4)

</details>

<details><summary>German Federal Government — press conferences — 1,720 records</summary>

German-language conferences with questions and answers from multiple ministries. Preserve which spokesperson actually answered.

Languages: de. Recorded dates: 2024-09-24 → 2026-09-07.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Authentic question → answer | 1,541 | 31534 / 54820 (n=1541) | 374 / 1401 (n=1541) | Not present / measured |
| Full conference document | 179 | Not present / measured | Not present / measured | 52800 / 68754 (n=179) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Authentic question → answer

Existing paired fields; candidate for supervised adaptation after source and quality review.

**Prompt/context:** country_iso3, event_date, speaker; question; history: only turns preceding this answer; context, when available

**Output/target:** text: the actual spokesperson answer

**Use:** SFT or supervised distillation; useful baseline for a country-conditioned adapter.

**Scoring/environment:** Evidence-based review of accuracy, attribution and substantive policy content. No automatic verifier or RL environment supplied.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=c861bf859653361d8ebb0c82608b1f39a7c3e6df8157b79bf1adc799e3a29f78)

### Full conference document

Source document; individual Q&A extraction exists for part of this source.

**Prompt/context:** date, institution and speaker boundaries; earlier turns only, if constructing a dialogue

**Output/target:** A selected answer span after extraction; not the entire transcript by default

**Use:** Extract Q&A for SFT; optional continued pretraining after cleaning.

**Scoring/environment:** Check speaker segmentation and event/translation splits; exclude future answers from context.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=f01cd3540f7ad4c3237f4a19da9ef96f943c9147175bf0f21c4c662a56671094)

</details>

<details><summary>Germany Mission to the UN — statements — 452 records</summary>

Diplomatic statements with institutional role and date metadata.

Languages: en. Recorded dates: 2022-01-18 → 2026-09-01.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Statement / speech reconstruction | 452 | Not present / measured | 3133 / 6153 (n=452) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Statement / speech reconstruction

Observed statement text; an instruction may be constructed from metadata.

**Prompt/context:** country, institution, speaking_capacity, event_date; title / agenda and context, when present

**Output/target:** text: attributed statement

**Use:** Statement SFT, retrieval evidence, or optional domain-text training.

**Scoring/environment:** Review speaker, policy fidelity and unsupported commitments. No reward verifier or transition model exists.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=3caa1472b7c6ed116b8c490c035ad8463d9fb1842dd298a37a00493d846eb482)

</details>

<details><summary>National policy documents — China and Germany collection — 377 records</summary>

Strategy papers, white papers, WTO reports and derived passages in the initial country collection.

Languages: ar, de, en, es, fr, ja, pl, pt, ru, uk, zh. Recorded dates: 2023-06-14 → 2023-07-13.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 377 | Not present / measured | Not present / measured | 2974 / 2999 (n=377) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=bcfa96c3f157840716523698ec6763dd24c4199b899eecf188dd8fdf7d62f9b4)

</details>

<details><summary>OHCHR — Universal Human Rights Index — 2,797 records</summary>

UPR recommendations, reviewed-state response labels and institutional evidence. A recommendation about a country is not necessarily a statement by that country.

Languages: en. Recorded dates: 2008-05-22 → 2026-01-08.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Recommendation from one state to another | 1,973 | 46 / 64 (n=1973) | 173 / 329 (n=1973) | Not present / measured |
| Recommendation → reviewed-state response | 824 | 194 / 329 (n=824) | 9 / 9 (n=824) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Recommendation from one state to another

Recommendation text and directed state roles exist; earlier review context may be incomplete.

**Prompt/context:** recommending_states → reviewed_states; review cycle, date and document; question / prior review evidence when available

**Output/target:** text: recorded recommendation

**Use:** Directed recommendation SFT or retrieval evidence.

**Scoring/environment:** Check attribution and recommendation grounding; no automatic quality reward is supplied.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=1c3234e6d8a698f3d95b8d6b9a98a28d5ee1140884030b8b37456f4d0399b9e7)

### Recommendation → reviewed-state response

Question contains recommendation; text contains the response label.

**Prompt/context:** reviewed_states, recommending_states, cycle and date; question: recommendation text; context: recommending-state information

**Output/target:** text: response such as Supported or Noted

**Use:** Response classification / SFT; possible offline verifiable task after validation.

**Scoring/environment:** Potential exact-match label check, subject to response-date and linkage validation; no reward implementation bundled.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=0bd6b0bd048abbf86c57bb7928093cddb59b905ca301ab0562ea089af38fae33)

</details>

<details><summary>Project annotations — policy claims and applications — 6 records</summary>

Project-authored claims and question–evidence–answer applications derived from linked official sources. These are review candidates, not authentic historical dialogue.

Languages: en. Recorded dates: 2022-03-02 → 2023-07-13.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Curated policy claim | 3 | Not present / measured | Not present / measured | Not present / measured |
| Authored evidence → policy answer | 2 | 1947 / 3245 (n=2) | 375 / 497 (n=2) | Not present / measured |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Curated policy claim

Attributed claim and source spans; not a complete dialogue.

**Prompt/context:** claim plus source passages as dated context; a separately constructed application question

**Output/target:** No answer target in this claim record

**Use:** Retrieval / dossier context; parent evidence for authored applications.

**Scoring/environment:** Verify source support and scope; published policy does not establish behavior in every real project.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=b40a4fad8dda48dedf7ed1d71fd4e2efba1b35f92ce625fb2dfec0461ac69fdf)

### Authored evidence → policy answer

Paired messages exist as review candidates; extension also has SFT export files.

**Prompt/context:** messages[0]: system instruction; messages[1]: institution/date, cited evidence and question

**Output/target:** messages[-1]: authored assistant answer

**Use:** Evidence-conditioned SFT candidate; possible later preferences from reviewed errors.

**Scoring/environment:** rubric, source spans, scope and unsupported-claim checks. Review is pending; no automated correctness oracle.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=5aa85b5e1e2b19315d73a2d2045ff1e7b8543e4fb6d11971c4797401e68ea083)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=168d55999feeaf603b4d204142a16d2ec39da78e21b402c40a4fe521766a2b27)

</details>

<details><summary>UN General Assembly — speech corpus — 481 records</summary>

Upstream speech segments and derived country-attributed text. Some boundaries and speakers remain unverified; meeting text may include several speakers.

Languages: en. Recorded dates: 1993 → 2017-09-11.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Speech segment with unverified boundaries | 250 | Not present / measured | Not present / measured | 5133.5 / 14528 (n=250) |
| Statement / speech reconstruction | 231 | Not present / measured | 4835 / 14291 (n=231) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Speech segment with unverified boundaries

Text exists; speaker attribution and segment boundaries are not confirmed.

**Prompt/context:** meeting/document metadata; speaker identity must be checked

**Output/target:** No verified target until speaker segmentation is resolved

**Use:** Evidence discovery; not a ready country-specific supervised trace.

**Scoring/environment:** Speaker and boundary verification is a prerequisite.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=d51b6b4dd7023416024eb6ea4572340cd53d370d6a73f26f4f77482f2b6459f5)

### Statement / speech reconstruction

Observed statement text; an instruction may be constructed from metadata.

**Prompt/context:** country, institution, speaking_capacity, event_date; title / agenda and context, when present

**Output/target:** text: attributed statement

**Use:** Statement SFT, retrieval evidence, or optional domain-text training.

**Scoring/environment:** Review speaker, policy fidelity and unsupported commitments. No reward verifier or transition model exists.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=a0b0564c54690abbe6c3f0b7514397694910937c68611c46c6b314019fadee7b)

</details>

<details><summary>UN General Assembly — voting data (UNGA-DM) — 6,139 records</summary>

Recorded vote labels and resolution identifiers. Most rows still lack joined proposal text; they are not complete decision-making environments.

Languages: en. Recorded dates: 1973-10-26 → 2023-09-01.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Recorded vote label | 6,139 | Not present / measured | Not present / measured | 8 / 10 (n=6139) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Recorded vote label

Action label exists; proposal text is generally missing.

**Prompt/context:** country and decision date; decision / draft identifier; MISSING for most rows: actual proposal and contemporaneous context

**Output/target:** original_vote / text: observed vote

**Use:** Classification / SFT after joining context; possible offline verifiable task, not an existing RLVR environment.

**Scoring/environment:** Exact-match scoring is possible only after validating labels and proposal joins. A correct historical vote does not verify a generated explanation.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=f2b0cbe31a372a818d772623a811e1eebc8afff9690b4e01d043c5799d6a9623)

</details>

<details><summary>UN General Debate Corpus — 50 records</summary>

General Debate speeches. Keep country, session and speech date together; whole speeches are not dialogue trajectories.

Languages: en. Recorded dates: 1973 → 2022.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Whole speech / domain text | 50 | Not present / measured | Not present / measured | 21933.5 / 34836 (n=50) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Whole speech / domain text

Source text exists; no instruction–answer pair is inherent in the document.

**Prompt/context:** text: cleaned speech or document; country, speaker, event and language as attribution metadata

**Output/target:** Next-token text continuation if used for continued pretraining; no separate assistant answer provided

**Use:** Retrieval or optional continued pretraining; construct and review tasks before SFT.

**Scoring/environment:** Language-model loss measures text prediction, not policy correctness or negotiation quality. Check attribution and held-out event overlap.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=a35759a4e5340c77d7beee959a0852d2d435a6d889b8ccefb8b049f6bf05e9d5)

</details>

<details><summary>UN Human Rights Council — UPR national reports — 158 records</summary>

Country reports and multilingual passages. These are evidence, not automatically verified policy behavior.

Languages: ar, en, es, fr, ru, zh. Recorded dates: 2023-09-01 → 2023-09-01.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 158 | Not present / measured | Not present / measured | 2958.5 / 2998 (n=158) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=f3e162679c706269946658063e6a47d1b34633e50504a7692d6bab63029facf3)

</details>

<details><summary>UN records — joined decision cases — 2 records</summary>

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

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=772621d9bbf2cb35fcd4d7bd7f1b7a276da6fad8d5a4761ec6b86bded6a6b92b)

</details>

<details><summary>World Bank — World Development Indicators — 43 records</summary>

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

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=c4643f0632540b0e45e7385559b60a06fcd9e25914481051ebc16221ff37bda3)

</details>

## Post-training examples

[Inspect task templates and a worked evidence-conditioned candidate](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=DEU)

No interactive environments, multi-agent trajectories, training reward verifiers or preference pairs are prepared. Some vote/response labels can support future verifiable tasks after validation. New curated applications remain review candidates.
