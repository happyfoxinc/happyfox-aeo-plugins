# Engine evidence and search interpretation

Call get_prompt_evidence with the selected brand_id and prompt_id before making
recommendations. Use get_aeo_methodology for metric and outcome definitions.
Use list_citation_sources and compare_competitors only when they help resolve a
specific question. Check scan IDs before combining outputs from different tools.
If a scan changes during the investigation, disclose the mismatch or refresh the
necessary evidence to establish a consistent observation.

For every available engine, read the answer and compare its actual recommendation
language with the audited outcome. Report an audit/answer discrepancy explicitly;
do not turn a measurement error into a content recommendation. Record:

- Brand outcome, competing recommendations, and stated selection criteria.
- Reported searches: broad discovery, category/use-case research, vendor-specific
  verification, comparison, or a mixture. These classifications are agent inference.
- Brand-owned and relevant third-party sources in the exposed results and citations.
- Which answer passages the citations support, where that association is exposed.
- Missing engines, answer truncation, and per-section search-evidence limitations.

Interpret searchEvidence according to its contract:

- Check availability separately for searchCalls, searchQueries, and searchResults.
  Unavailable, not_observed, error, and explicit_none have different meanings;
  missing telemetry never establishes that no search occurred. An explicit empty
  reported section describes that section, not all internal engine activity.
- complete_as_reported covers the recognized reported section, not the full
  retrieval pool or hidden provider reasoning. Partial, unknown, and truncated
  evidence constrain absence claims to the exposed records.
- countsAreLowerBounds means records were omitted. Text-only truncation may
  remove crucial qualifications. Inline evidence is capped and cannot be
  exhausted by pagination; do not repeatedly request it expecting more records.
- Resolve searchCallId against searchCalls when present. A null association is
  unknown; a call with multiple queries does not establish which query returned
  a particular source, even if truncation leaves only one query visible. Preserve
  domain restrictions and repeated occurrences. Apply the provider-specific
  grouping rules below before interpreting a call or association.
- responseOrder is not search rank. Use providerRank only when reported, and
  retain its source-list context instead of inventing one global ranking.
- search_result, consulted_source, grounding_source, answer citation, brand
  mention, and brand recommendation are distinct observations. An owned source
  can support a competitor recommendation. Inspect the relevant passage before
  attributing value.

### Provider-specific interpretation

Use each answer's availability and limitations as the authority for what is
exposed; provider support does not guarantee every stored answer has these fields.

- ChatGPT and Grok: reported search actions populate searchCalls. Sources in an
  action are consulted_source records linked to that call when present. Answer
  citations or annotations do not substitute for missing search results. Query
  evidence can be available while source evidence is unavailable.
- Gemini: searchCalls contains a normalized group for the first answer candidate's
  reported queries and web grounding sources. Its sequence of 1 and null
  providerCallId do not establish one actual search request, its timing, or search
  effort. A source's searchCallId links to this answer group; it never establishes
  an individual query-to-source association, even with only one reported query.
  A source-only group can have no available query strings. grounding_source records
  are reported grounding references, not the full search result pool. Snippets
  and provider ranks are not exposed for these records; grounding-support passages
  are not included and must not be invented from the query/source grouping.
- Gemini grounding URLs may be redirects. Preserve the reported URL. If public
  research resolves it, record the destination and inspection date separately;
  determine ownership from the verified destination rather than the redirect
  host. If it cannot be resolved, leave ownership uncertain.
- Claude: sources can link to reported web_search calls when their provider IDs
  match. Plaintext snippets may be absent. A tool error differs from an explicitly
  empty result list; retain that distinction.
- Perplexity Sonar: reported results are answer-level evidence. Internal queries
  and call associations are unavailable; do not reconstruct them from titles,
  citations, or snippets.

Compare buyer interpretation and the available queries, sources, and outcomes
across engines. Do not compare searchCalls counts as equivalent search effort
across providers or treat richer telemetry as better retrieval performance.

The current tool provides the latest reported scan, not selectable historical
evidence. A single run cannot establish recurrence. Several engines in one scan
are separate observations, not a repeated measurement of the same engine.

