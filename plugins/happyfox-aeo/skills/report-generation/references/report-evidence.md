## Report evidence

### Collect the measured answers

1. Resolve the accessible brand with `list_brands`. Record its name, domain,
   category, configured competitors, and readable engine names. Fetch
   `get_brand_performance`, `compare_competitors`, and `get_aeo_methodology`.
   Use the latest fully analyzed scan and its completion date. Explain any
   missing connection or scan. A measured report requires an accessible, fully
   analyzed scan.
2. Fetch all unfiltered pages of `list_prompt_performance` with `limit: 50`,
   following `page.nextCursor` until null. Deduplicate by `promptId` and keep
   text, stage, intent, and `engineOutcomes`. Incomplete pagination rules out
   full-set totals and rankings. Reconcile collected outcomes with
   `summary.latest.answerCount`. Historical answers from deleted or inaccessible
   prompts may still contribute to that total. If counts differ, label derived
   figures as the available-question subset. Calculate rates using that subset
   and report its share of the scan separately. For example, after fetching
   all pages, you have 80 of the scan’s 100 answers and 20 recommend the brand.
   Report a recommendation rate of 20/80 (25%) and coverage of 80/100.
3. Fetch `get_prompt_evidence` for each exact question, quotation, or claim about
   an engine's answer. Reuse that evidence for subsequent calculations. When
   reporting citations, use `list_citation_sources` with the relevant scope
   and filters. Follow every page for a complete inventory. Narrower claims
   about segments or brand-absent answers require matching answer-level evidence.
4. Match scan ID and `completedAt` across contributing scan responses. If either
   changes during collection, discard the mixed results and recollect. Omit a
   derived analysis if a coherent set is unavailable.
5. Calculate with code and keep a private ledger of responses, IDs, timestamps,
   classifications, counts, exclusions, and external sources. Use readable scope
   labels in the report. Distinguish observations, inference, supplied facts,
   public research, and proposed work.

### Group questions by meaning

Classify prompts before examining outcomes. Use recurring attributes supported
by the wording or metadata, such as explicit location, industry, use case,
buyer type, company size, requirement, comparison target, or stored journey
stage. Normalize clear synonyms and stage IDs. Keep the prompt IDs and wording
behind each assignment. Leave ambiguous attributes unclassified. A location in
a question describes its subject, not the location of the test or buyer.

A branded question names the tracked brand, a verified alias, or its domain.
Competitor-only questions remain non-branded for the tracked brand. Exclude and
disclose unresolved classifications, or use labeled all-question figures.

Compare one dimension per table with consistent membership rules. Deduplicate
within each group, disclose overlap, and calculate overall totals independently.
Each displayed group needs at least three distinct questions with observed
outcomes. This is a reporting heuristic. Show question counts and observed-answer
denominators. Use the actual outcomes available for each question. Multiplying
question counts by configured engines would include missing answers. If engine
coverage differs materially, restrict to a common
observed engine set and label it, or omit the comparison. Explain selected and
unclassified coverage. A ranking applies only to the comparable measured groups.

### Calculate rates from observed outcomes

Keep scan, question set, engine set, and branded scope consistent within a
comparison. Count each observed answer once. Omit affected metrics when duplicate
prompt-engine entries cannot be reconciled. A missing answer is unavailable.
A zero numerator with observed answers is measured zero. A zero denominator is
unavailable. Use answer-level fields and exact counts. Rounded percentages and
prompt-level `status` or `bestPosition` cannot reconstruct individual outcomes.
For a segment rate, sum the qualifying answers across its prompts and divide by
the segment’s total observed answers. Averaging prompt percentages gives each
prompt equal weight even when their answer counts differ.

| Measure | Calculation |
| --- | --- |
| Visibility | Outcomes with `mentioned: true` / observed answers in scope |
| Explicit recommendation rate | Outcomes with `mentionType: "recommended"` / observed answers in scope. For a segment, restrict both counts to its prompt IDs. |
| Recognition | Visibility on questions naming the brand. Compare with non-branded discovery only when both populations have observations. |
| Top-three appearance | Outcomes with `mentioned: true` and position 1–3 / observed answers in scope |
| Competitors fill the gap | Brand-absent answers with at least one configured competitor explicitly recommended / all observed brand-absent answers in scope |
| Per-competitor recommendation rate | Answers explicitly recommending that competitor / observed answers in the stated comparison |
| Owned citation share | Owned citation occurrences / all citation occurrences in scope |

For competitor rates, match prompt evidence to every denominator answer by
prompt and engine. For gap coverage, inspect each brand-absent answer and count
it once even when several rivals qualify. For per-competitor comparisons,
inspect all answers in scope, including ones mentioning the brand unless the
comparison explicitly covers brand absence. Match configured IDs, names, or
domains and require both `isConfiguredCompetitor: true` and
`mentionType: "recommended"` in `mentions`. Count each competitor once per
answer and show ties. Calculate the brand’s rate and each competitor’s rate over
the exact same observed answers. Label any comparison restricted to brand-absent
answers. Rates may sum above 100%.
Missing or conflicting evidence makes the affected metric unavailable.
`compare_competitors` supplies overall mentions and cannot establish segment
recommendation rates.
