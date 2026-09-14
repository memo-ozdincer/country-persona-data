# India — 10,609 evidence record IDs

[Open source explorer](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=IND)

## Breakdown

| Record type | Distinct IDs |
|---|---:|
| Source records | 2,019 |
| Evidence passages | 272 |
| Recorded actions / responses | 8,265 |
| Curated policy positions | 5 |
| Authored policy applications | 3 |
| Prepared prompt / completion views | 3 |
| Linked decision cases | 2 |

Distinct record_id per country across source records, passages, actions, statistics and curated annotations. Excludes training-format copies, review/lineage, evaluation wrappers and profiles. Each ID is assigned once, preferring its canonical version. Translations and derived spans remain separate IDs; these are not independent training traces.

Breakdown rows include overlapping representations and must not be summed.

## Data sources

<details><summary>India Mission to the UN — statements — 5 records</summary>

Official UN statements and extracted evidence.

Languages: en. Recorded dates: 2025-09-27 → 2025-09-27.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 4 | Not present / measured | Not present / measured | 2800 / 2800 (n=4) |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | 10564 / 10564 (n=1) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=7f62641372c748aa40b34836862a89ab3f28bc54e84d892a2b983e4ede6883c8)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=c398e4f36274ddbea834b28428542ccaf7bd845093313079e274abe290722e39)

</details>

<details><summary>India Press Information Bureau — government releases — 4 records</summary>

Government announcements, including the updated climate commitment.

Languages: en. Recorded dates: 2022-08-03 → 2022-08-03.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 3 | Not present / measured | Not present / measured | 2800 / 2800 (n=3) |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | 5806 / 5806 (n=1) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=bcde3d0ad8d240ff24fc6a0860fb61011743126ad46c8f784dd1cc8976c8ac18)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=940399ee56ad51ac42e3d092b4c1e22b23a7500ec4ed15b27aa7e34a58926d34)

</details>

<details><summary>OHCHR — Universal Human Rights Index — 1,718 records</summary>

UPR recommendations, reviewed-state response labels and institutional evidence. A recommendation about a country is not necessarily a statement by that country.

Languages: en. Recorded dates: 2008-05-23 → 2026-01-08.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Recommendation from one state to another | 963 | 45 / 64 (n=963) | 130 / 232 (n=963) | Not present / measured |
| Recommendation → reviewed-state response | 755 | 183 / 330 (n=755) | 9 / 9 (n=755) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Recommendation from one state to another

Recommendation text and directed state roles exist; earlier review context may be incomplete.

**Prompt/context:** recommending_states → reviewed_states; review cycle, date and document; question / prior review evidence when available

**Output/target:** text: recorded recommendation

**Use:** Directed recommendation SFT or retrieval evidence.

**Scoring/environment:** Check attribution and recommendation grounding; no automatic quality reward is supplied.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=62bea4f673afed0761e4422fe2ca3d1469aa2a203e2a086ad82753258753d2dc)

### Recommendation → reviewed-state response

Question contains recommendation; text contains the response label.

**Prompt/context:** reviewed_states, recommending_states, cycle and date; question: recommendation text; context: recommending-state information

**Output/target:** text: response such as Supported or Noted

**Use:** Response classification / SFT; possible offline verifiable task after validation.

**Scoring/environment:** Potential exact-match label check, subject to response-date and linkage validation; no reward implementation bundled.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=beec4368daf700495c21991b49061535358dc507edd38224ad92c1a376fade5d)

</details>

<details><summary>Project annotations — policy claims and applications — 9 records</summary>

Project-authored claims and question–evidence–answer applications derived from linked official sources. These are review candidates, not authentic historical dialogue.

Languages: en. Recorded dates: 2020-11-25 → 2025-07-08.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Curated policy claim | 5 | Not present / measured | Not present / measured | Not present / measured |
| Authored evidence → policy answer | 3 | 1448 / 1834 (n=3) | 287 / 298 (n=3) | Not present / measured |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Curated policy claim

Attributed claim and source spans; not a complete dialogue.

**Prompt/context:** claim plus source passages as dated context; a separately constructed application question

**Output/target:** No answer target in this claim record

**Use:** Retrieval / dossier context; parent evidence for authored applications.

**Scoring/environment:** Verify source support and scope; published policy does not establish behavior in every real project.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=6dc24d4c3e26e872f18f45120f538f1441a54f47c113c2168ac198bcebc15313)

### Authored evidence → policy answer

Paired messages exist as review candidates; extension also has SFT export files.

**Prompt/context:** messages[0]: system instruction; messages[1]: institution/date, cited evidence and question

**Output/target:** messages[-1]: authored assistant answer

**Use:** Evidence-conditioned SFT candidate; possible later preferences from reviewed errors.

**Scoring/environment:** rubric, source spans, scope and unsupported-claim checks. Review is pending; no automated correctness oracle.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=ffb2d2c26a216b450ac8b7a00d4b38dda55a36c11b14f1aaf6f06841b44c9a1b)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=697154df8efd5697b37821b33453fed89f632eda37f244acd2ffd137d2c68182)

</details>

<details><summary>UN General Assembly — speech corpus — 1,047 records</summary>

Upstream speech segments and derived country-attributed text. Some boundaries and speakers remain unverified; meeting text may include several speakers.

Languages: en. Recorded dates: 1993 → 2017-12-05.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Speech segment with unverified boundaries | 536 | Not present / measured | Not present / measured | 6411.5 / 16933 (n=536) |
| Statement / speech reconstruction | 511 | Not present / measured | 6173 / 16006 (n=511) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Speech segment with unverified boundaries

Text exists; speaker attribution and segment boundaries are not confirmed.

**Prompt/context:** meeting/document metadata; speaker identity must be checked

**Output/target:** No verified target until speaker segmentation is resolved

**Use:** Evidence discovery; not a ready country-specific supervised trace.

**Scoring/environment:** Speaker and boundary verification is a prerequisite.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=343a15ed3642963c63266c15d5ffbd9ed97d87338c2566ed77cfe38ff3534225)

### Statement / speech reconstruction

Observed statement text; an instruction may be constructed from metadata.

**Prompt/context:** country, institution, speaking_capacity, event_date; title / agenda and context, when present

**Output/target:** text: attributed statement

**Use:** Statement SFT, retrieval evidence, or optional domain-text training.

**Scoring/environment:** Review speaker, policy fidelity and unsupported commitments. No reward verifier or transition model exists.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=700746b73881f52fa5c47978ed364f8ef659526772b298a668bd8494dbc3b0ba)

</details>

<details><summary>UN General Assembly — voting data (UNGA-DM) — 7,509 records</summary>

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

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=1993b029b61002136e3d74135ee14aa90c7f1ee6f573969b4608e19dd995d5d1)

</details>

<details><summary>UN Human Rights Council — UPR national reports — 231 records</summary>

Country reports and multilingual passages. These are evidence, not automatically verified policy behavior.

Languages: ar, en, es, fr, ru, zh. Recorded dates: 2022-08-17 → 2022-08-17.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 225 | Not present / measured | Not present / measured | 1762 / 2800 (n=225) |
| Source document / evidence passage | 6 | Not present / measured | Not present / measured | 84142 / 87690 (n=6) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=6188b6ee7c1f3cc758274d26db45ce646b7eaa71b50587980bee8c0b68330e2e)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=22b59ab5777f7f905ddea46cf1030735f3fb9706fcb05b5f8f3268d7facd8de3)

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

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=d4620affd5968667b19e0638743e30aa82451bc18dafda89fd3b337cd3fdf15b)

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

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=9990e00566a2c6e90366458d1b73489dcd5b9bd8d0ebf4c2a25e4d98363ea907)

</details>

<details><summary>World Trade Organization — government policy reports — 41 records</summary>

Government reports supplied for WTO trade-policy reviews. Preserve the government’s stated position and its publication date.

Languages: en. Recorded dates: 2021 → 2021.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 40 | Not present / measured | Not present / measured | 2018 / 2800 (n=40) |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | 78991 / 78991 (n=1) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=4f8ca90e1b5c1ead0745e47d22296d5c2cd7c57e9233fa60d1dcde6ea0504a3a)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=3b55d5176453a6df61dfb9443cc602cbb7ef4a086a6f7803823ee5be3ad86584)

</details>

## Post-training examples

[Inspect task templates and a worked evidence-conditioned candidate](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=IND)

No interactive environments, multi-agent trajectories, training reward verifiers or preference pairs are prepared. Some vote/response labels can support future verifiable tasks after validation. New curated applications remain review candidates.
