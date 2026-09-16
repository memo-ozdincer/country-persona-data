# United Kingdom (11,054 evidence record IDs)

[Open source explorer](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=GBR)

## Breakdown

| Record type | Distinct IDs |
|---|---:|
| Source records | 2,296 |
| Evidence passages | 520 |
| Recorded actions / responses | 8,186 |
| Curated policy positions | 4 |
| Authored policy applications | 3 |
| Prepared prompt / completion views | 3 |
| Linked decision cases | 2 |

Distinct record_id per country across source records, passages, actions, statistics and curated annotations. Excludes training-format copies, review/lineage, evaluation wrappers and profiles. Each ID is assigned once, preferring its canonical version. Translations and derived spans remain separate IDs; these are not independent training traces.

Breakdown rows include overlapping representations and must not be summed.

## Data sources

<details><summary>OHCHR (Universal Human Rights Index) (2,447 records)</summary>

UPR recommendations, reviewed-state response labels and institutional evidence. A recommendation about a country is not necessarily a statement by that country.

Languages: en. Recorded dates: 2008-05-13 → 2026-01-08.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Recommendation from one state to another | 1,771 | 45 / 64 (n=1771) | 209 / 342 (n=1771) | Not present / measured |
| Recommendation → reviewed-state response | 676 | 185.5 / 337 (n=676) | 5 / 9 (n=676) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Recommendation from one state to another

Recommendation text and directed state roles exist; earlier review context may be incomplete.

**Prompt/context:** recommending_states → reviewed_states; review cycle, date and document; question / prior review evidence when available

**Output/target:** text: recorded recommendation

**Use:** Directed recommendation SFT or retrieval evidence.

**Scoring/environment:** Check attribution and recommendation grounding; no automatic quality reward is supplied.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=c217042af235a8d0e8a195e11348733f34a84aaef17691f0884b102e31fac8aa)

### Recommendation → reviewed-state response

Question contains recommendation; text contains the response label.

**Prompt/context:** reviewed_states, recommending_states, cycle and date; question: recommendation text; context: recommending-state information

**Output/target:** text: response such as Supported or Noted

**Use:** Response classification / SFT; possible offline verifiable task after validation.

**Scoring/environment:** Potential exact-match label check, subject to response-date and linkage validation; no reward implementation bundled.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=fe212f5328d4f2c3de3d68c17c0f1e444f4d22556adf2e3a668f6312534e6963)

</details>

<details><summary>Project annotations (policy claims and applications) (10 records)</summary>

Project-authored claims and question–evidence–answer applications derived from linked official sources. These are review candidates, not authentic historical dialogue.

Languages: en. Recorded dates: 2022-03-02 → 2025-06-24.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Curated policy claim | 4 | Not present / measured | Not present / measured | Not present / measured |
| Authored evidence → policy answer | 3 | 738 / 1884 (n=3) | 247 / 297 (n=3) | Not present / measured |
| Source document / evidence passage | 3 | Not present / measured | Not present / measured | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Curated policy claim

Attributed claim and source spans; not a complete dialogue.

**Prompt/context:** claim plus source passages as dated context; a separately constructed application question

**Output/target:** No answer target in this claim record

**Use:** Retrieval / dossier context; parent evidence for authored applications.

**Scoring/environment:** Verify source support and scope; published policy does not establish behavior in every real project.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=fa47e7305bb9bbabfb985cb985e8f4ca19e962e359ffc4a738f491502b9a3bfd)

### Authored evidence → policy answer

Paired messages exist as review candidates; extension also has SFT export files.

**Prompt/context:** messages[0]: system instruction; messages[1]: institution/date, cited evidence and question

**Output/target:** messages[-1]: authored assistant answer

**Use:** Evidence-conditioned SFT candidate; possible later preferences from reviewed errors.

**Scoring/environment:** rubric, source spans, scope and unsupported-claim checks. Review is pending; no automated correctness oracle.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=8d1ab83541cf9dbe82286ee22cba1684f11c66b0b97ebedd04d2c26e492f89a9)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=ca621550947a30039c90de039fd0f83d6fa2e45e055d7f0367a85e9d35b9b69c)

</details>

<details><summary>UK Cabinet Office (national security strategy) (64 records)</summary>

National security strategy and derived evidence.

Languages: en. Recorded dates: 2025-06-24 → 2025-06-24.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 63 | Not present / measured | Not present / measured | 1650 / 2800 (n=63) |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | 104013 / 104013 (n=1) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=0206a3c7226cedc50097b4fb6c7888258f98c521a85f2dd278ccba51967bc32e)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=fe8dda44d7afa1fd87f682f739be87fade7e2563d3daa26d75446f6f88251801)

</details>

<details><summary>UK Foreign, Commonwealth & Development Office (5 records)</summary>

Official diplomatic statements and evidence passages.

Languages: en. Recorded dates: 2025-09-26 → 2025-09-26.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 4 | Not present / measured | Not present / measured | 2800 / 2800 (n=4) |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | 10209 / 10209 (n=1) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=cdb083b3edf74932bdc90fbfb7077f3b5427051cbae9c9122a18cf0da82c32df)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=5a960c025af4dca258dec2f81ca89d6567062040eb3a3654a69ad5a78eb8e9fb)

</details>

<details><summary>UK government (climate commitment) (162 records)</summary>

UK nationally determined contribution and associated evidence passages.

Languages: en. Recorded dates: 2025-01-30 → 2025-01-30.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 161 | Not present / measured | Not present / measured | 873 / 1048 (n=161) |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | 134451 / 134451 (n=1) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=4ad155adf90bebe2b27ea96d225acf47f3efc7cf424ab7c0c1b30e2e19b10ed8)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=c964e1ba9513360f6ebbb2739026f45ec95151d15abc49821daf5f1cfd236c41)

</details>

<details><summary>UN General Assembly (speech corpus) (508 records)</summary>

Upstream speech segments and derived country-attributed text. Some boundaries and speakers remain unverified; meeting text may include several speakers.

Languages: en. Recorded dates: 1993 → 2018.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Speech segment with unverified boundaries | 259 | Not present / measured | Not present / measured | 4062 / 14958 (n=259) |
| Statement / speech reconstruction | 249 | Not present / measured | 3729 / 13607 (n=249) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Speech segment with unverified boundaries

Text exists; speaker attribution and segment boundaries are not confirmed.

**Prompt/context:** meeting/document metadata; speaker identity must be checked

**Output/target:** No verified target until speaker segmentation is resolved

**Use:** Evidence discovery; not a ready country-specific supervised trace.

**Scoring/environment:** Speaker and boundary verification is a prerequisite.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=b22caf01e3d295022efcc1106f36e211952d2ba5227843fafebcc637611a7a71)

### Statement / speech reconstruction

Observed statement text; an instruction may be constructed from metadata.

**Prompt/context:** country, institution, speaking_capacity, event_date; title / agenda and context, when present

**Output/target:** text: attributed statement

**Use:** Statement SFT, retrieval evidence, or optional domain-text training.

**Scoring/environment:** Review speaker, policy fidelity and unsupported commitments. No reward verifier or transition model exists.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=f2ddf91d4f99321c8be10aaa0d771fd35986e1eb7cf154d4bccb3b089b399ac6)

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

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=3d5d65ecf76de2b1d4486cd1b259ae4f9db76217f21710b3a57bf421f0c70c7a)

</details>

<details><summary>UN Human Rights Council (UPR national reports) (242 records)</summary>

Country reports and multilingual passages. These are evidence, not automatically verified policy behavior.

Languages: ar, en, es, fr, ru, zh. Recorded dates: 2022-08-17 → 2022-08-17.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 236 | Not present / measured | Not present / measured | 1906.5 / 2800 (n=236) |
| Source document / evidence passage | 6 | Not present / measured | Not present / measured | 84378.5 / 95773 (n=6) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=eb69eca7f4f58b115c7abde716a084a16147b36c2c3c73d0cad1bbb47dd05fa1)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=7172789c9aa5317c04c6364b7d0a71eab46749ac3c7b95ef5813fd7192c27b19)

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

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=325f2a66eb7de7d118d3d1fc3cb1d05bc0a074863c406edfbd4fbc1396e39b52)

</details>

<details><summary>UNBench (linked diplomatic task samples) (5 records)</summary>

Acquired sample records with some draft text and observed outputs. This is not the full upstream benchmark or an interactive environment.

Languages: en. Recorded dates: 2016-12-23 → 2020-05-29.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Proposal → recorded vote | 5 | 6327 / 54335 (n=5) | 3 / 3 (n=5) | Not present / measured |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Proposal → recorded vote

Sample has question/context fields and a recorded vote; validate joins and historical leakage.

**Prompt/context:** country and event_date; question; context: joined draft text

**Output/target:** text: observed vote label

**Use:** Label SFT or evaluation; a candidate for an offline verifier, not a prepared RL rollout environment.

**Scoring/environment:** Exact match to the recorded label, after verifying final versus procedural votes. No inference about hidden motives.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=123d9c5206f6cf7d24ea2205eb671df9ee0877320947960a20eafaa0c9b02338)

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

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=2b3d2f05c58c1620477bf8a4b08344386ba68720e983725878e0ae18854a8104)

</details>

<details><summary>World Trade Organization (government policy reports) (57 records)</summary>

Government reports supplied for WTO trade-policy reviews. Preserve the government’s stated position and its publication date.

Languages: en. Recorded dates: 2025-10-28 → 2025-10-28.

| Trace / record type | Count | Input chars, median / p95 | Target chars, median / p95 | Body chars, median / p95 |
|---|---:|---|---|---|
| Source document / evidence passage | 56 | Not present / measured | Not present / measured | 2310 / 2800 (n=56) |
| Source document / evidence passage | 1 | Not present / measured | Not present / measured | 117416 / 117416 (n=1) |

Exact character counts of stored question/context/history fields, target text, or document body; before adding metadata and the chat template. No tokenizer estimates. n is the number with that field present; missing fields are not zero-length observations.

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=0abe2d215fe22285718dad01021b5d60ed47fb2ea8c9d2e79a25c7cca2a83e1b)

### Source document / evidence passage

Source evidence exists; a task and answer are not inherent in a document.

**Prompt/context:** text / source passage, country or institution, policy date; a separately constructed question

**Output/target:** A reviewed, source-grounded answer must be authored or selected

**Use:** Retrieval first; evidence-conditioned SFT once targets exist; optional continued pretraining.

**Scoring/environment:** Check exact source spans and institutional scope. The text itself is not an automatic reward function.

[Actual record reference](https://memo-ozdincer-country-persona-explorer.static.hf.space/advanced.html#view=explore&id=78bb85bd46e472ddacd6575741089399d534e433d8bbac605a5c3833b36c294c)

</details>

## Post-training examples

[Inspect task templates and a worked evidence-conditioned candidate](https://memo-ozdincer-country-persona-explorer.static.hf.space/index.html#country=GBR)

No interactive environments, multi-agent trajectories, training reward verifiers or preference pairs are prepared. Some vote/response labels can support future verifiable tasks after validation. New curated applications remain review candidates.
