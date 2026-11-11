# One-page AI visibility report (v1.0.0)

Use this playbook when a user asks for a one-page brand report. You, the AI
client, collaborate on the story first, then create and return the final PDF
with your own document and CLI tools. Follow the collaboration checkpoints below
before generating the finished report.
The HappyFox AEO MCP server supplies live evidence; it does not render or
store your output. Before drafting, open and inspect the bundled
[HTML layout](../assets/one-page.html). Use the design template as the visual
starting point and use applicable components wherever needed. If the user
supplies another design, use that instead. Adapt or omit sections
to suit the story and available evidence.
All reference names, dates, figures, questions, and outcomes are example data.
Replace them completely with live evidence; never retain fictional prospect
facts or prospect logos. Keep the HappyFox AEO publisher identity.
Use the report-content rules below for the scope line, method note, and footer,
even when the illustrative HTML shows different copy.

Use the [component catalog](../assets/report-components.md) for optional reusable snippets and scoped styles. The HTML layout is authoritative for the current design.

## Report purpose

Default to a marketing agency preparing a prospect pitch: help the prospect
understand a relevant finding and see a credible reason for a follow-up
conversation. Answer: where does AI recommend this brand, where is it missing,
and who appears instead? Let the agency help choose the emphasis and proposed
next step. Adapt when the user specifies a different purpose or audience.
Lead with one defensible finding, supported by a primary visual, a few numbers,
and one exact question. Do not force the sample's healthcare, geographic, or
small-team story onto another brand.

## Collaborate before generating

The default sequence is prospect context -> evidence -> pitch-angle selection
-> visual storyboard review -> final artifact. A request to "create a report"
starts this sequence; it is not approval of an unseen story or layout. These
are client conversation instructions, not server-enforced approval gates. The
MCP server does not store a report session or the user's decisions.

### 1. Establish prospect context

Reuse information already supplied in this conversation. Ask one compact
question for missing context: what matters to the prospect, which services the
agency offers, and what next step the report should invite. Do not ask the user
to identify the audience again when an agency prospect pitch is already clear.
Brand resolution and evidence collection can proceed while context is pending;
optional business details must not block investigation. If they are unknown,
label business priorities as provisional and propose a discovery conversation
without inventing agency capabilities, prospect goals, contact details, or links.

### 2. Gather evidence and offer pitch angles — first checkpoint

Apply the [report evidence rules](report-evidence.md) before
proposing factual claims. Offer the strongest angle in chat and explain why you
recommend it. Add one or two alternatives if the evidence supports them and
they would lead to a different conversation with the prospect. For each angle,
give a possible headline, the measurement behind it, a caveat or contrary
finding, and the decision it could inform.

Invite the user to choose, combine, or redirect the angles, then wait for their
response before committing to a story or producing the storyboard.
Include positive or mixed results when they matter to the finding. If no measured finding is available, explain
the evidence gap instead of creating a pitch from fictional data.

If the requested framing conflicts with the evidence, explain the conflict and
offer a supported revision. Business context does not alter measured outcomes
or establish that a proposed service will fix an observed gap.

### 3. Review a visual storyboard — second checkpoint

After the user selects a direction, show a compact proposed one-page storyboard:

- **Main takeaway:** the proposed headline and why it matters to this prospect.
- **Primary visual:** the comparison or pattern to show, with verified values,
  scope, labels, and chart type; use a simpler evidence panel if no chart helps.
- **Supporting facts:** at most 2-3 useful metrics, without repeating the visual.
- **Concrete example:** an exact tracked question and verified observed outcome;
  explain whether it illustrates the broader finding or is a limited example.
- **Next step:** one action supported by the finding and the agreed invitation.
- **Material caveat:** the limitation the reader needs to interpret the finding.

Invite edits to the emphasis, visual, example, and next step. Wait for the
user's approval or revision before creating the final HTML/PDF. A storyboard
can be concise text; do not render a finished report just to obtain feedback.

### 4. Carry decisions forward and render

Keep a short working story brief in the conversation or local working notes:
prospect context, selected angle, approved storyboard, call to action, evidence
scope, and unresolved assumptions. Reuse it across turns alongside the private
evidence ledger. Do not claim these decisions are saved in AEO or available in
another client session. Do not repeat questions or checkpoints already resolved
in the conversation. Apply clear requested edits without asking the user to
approve those same edits again. If new evidence invalidates the agreed claim,
return with a supported revision before rendering; do not silently switch stories.

An explicit request such as "choose the angle and layout yourself" or "skip
review and generate it now" delegates the relevant choices. State the chosen
direction and assumptions, then proceed without those checkpoints. Delegation
does not relax evidence or output checks. Silence is not approval or delegation.
If the client cannot support a follow-up conversation and no delegation exists,
return the pitch options or pending storyboard rather than a finished report.

## Select the main comparison

Prefer 2–4 relevant groups that meet the evidence requirements. Choose groups
by business relevance, sample size, and measured contrast. Omit segmentation
when fewer than two groups qualify, pagination or outcomes are incomplete,
classification or coverage is uncertain, or the comparison adds little. Small differences in rounded rates alone cannot
establish a winner.

### Fallback hierarchy

If semantic segments are unsuitable, use a meaningful stored buyer-journey
breakdown or engine comparison from `get_brand_performance`, with its actual
scope and counts. These are all-prompt aggregates unless recomputed from a
verified subset; never label them non-branded by assumption. If those breakdowns
are also unhelpful or unavailable, replace the comparison area with a compact
overall brand/configured-competitor visibility table from `compare_competitors`,
or omit it and give the measured overview and exact evidence more space.
Explain any limitation that affects the finding in the method note.

## Select supporting metrics

Prefer non-branded discovery and shortlist metrics when the split is reliable.
Otherwise label cards “Across all tracked questions.” Use “Competitors fill the
gap” as the third card and “Most recommended competitor” per segment only when
the corresponding denominator is fully covered.

If complete competitor evidence is impractical or unavailable, **omit the
competitor recommendation column** and use a two-column segment table. Replace
the third card with a verified measure such as top-three appearance rate or
owned citation share from `get_brand_performance`, clearly labeled with its
actual scope and metric denominator. If no useful third measure is available,
use two cards. Owned citation share is a share of citations, not answers. Do not
reverse-engineer exact counts from rounded percentages.

## Report content

Include each section that supports the approved story and has evidence behind it.
Use the storyboard to decide the order. An exact buyer question may open the story when it helps explain
the finding.

1. **Brand and publisher:** actual brand name and HappyFox AEO attribution.
   Use an authorized logo only when available; text is sufficient.
2. **Measured date and category:** actual category and scan completion date.
3. **Finding-led headline:** 1-2 short lines describing the most defensible
   pattern or contrast, followed by at most two short explanatory sentences.
   If segmentation is omitted, use a supported overall, journey, or engine
   finding. Never manufacture a contrast to imitate the example.
4. **Scope line:** one compact line with the actual measured question count,
   analyzed-answer count, and readable engine names. For example, "30 questions
   yielding 90 AI answers across ChatGPT, Claude, and Gemini." Distinguish all
   tracked questions from an analyzed or selected subset; include the count of
   questions that do not name the brand only when needed to understand the
   metrics. Use customer-facing wording rather than "scan" or "audited."
5. **Metric cards:** select at most three metrics that support the agreed story, such
   as discovery visibility, recommendation rate, or competitor gap coverage,
   with short labels and exact fractions when available. Apply the fallback
   rules above. A recognition sentence may follow; do not mix named-brand
   presence into a discovery claim.
6. **Primary visual:** the approved comparison, using a dynamic segment table
   when eligible or the appropriate fallback. Use one measure, consistent
   denominators, and 2-4 rows. Consolidate material coverage/overlap caveats in
   the method note below. Optional competitor recommendations need the complete
   evidence specified in the shared report evidence rules.
7. **One question behind the finding:** one exact tracked question and a short
   observed outcome, with verified engine names. Fetch `get_prompt_evidence`;
   do not fabricate quotes, example questions, or answer descriptions. Say "all
   three observed answers" only if all three have been checked; report missing
   configured engines where material. If no exact evidence is available, omit
   this section rather than inventing proof.
8. **Proposed next step:** suggest one action supported by the finding. Validate product fit
   before proposing industry or requirement positioning; a visibility gap does
   not prove missing content or lack of capability. For prospect outreach, use
   the agreed invitation, such as a discovery call or comprehensive analysis.
   For an existing customer, use a relevant further investigation instead. Do
   not claim a detailed report already exists, invent a URL, or send outreach.
9. **Method note and footer:** one short note containing only caveats that
   materially affect interpretation, such as inferred question groups, missing
   answers, selected or excluded questions, overlapping groups, or multiple
   brands recommended in one answer. Combine applicable caveats rather than
   scattering them across table notes and the footer. Do not repeat the global
   scope counts or engine list already given above; retain each metric's own
   fraction and denominator beside it. Avoid a generic boilerplate disclaimer
   when a specific caveat explains the limitation. Keep the footer limited to
   HappyFox AEO attribution and page number; omit internal identifiers.

## Output requirements

Follow the selected HTML template and reuse applicable components for styling.
If the user supplies another design, use that instead.

- Use US Letter portrait (8.5 × 11 inches), exactly one printed page. Remove
  repetition or optional blocks before reducing type; keep core content readable.
  Do not clip overflowing text or use a fixed height to conceal a second page.
- Label chart values, populations, and denominators. Use consistent comparison
  scales and clear legends; never depict recognition and discovery as sequential
  conversion steps. Use a question/outcome panel when a chart adds no useful
  information. Pair supported change or status colors with explanatory text;
  a low rate alone does not establish a negative status.
- Use semantic headings and tables, selectable text, and count labels alongside
  bars. Keep the HTML self-contained and responsive, with visible keyboard focus
  and labeled controls. Escape all tool-sourced text before embedding it in HTML.
- Keep report blocks together where possible, preserve background colors, and
  hide preview/print controls in print output. Inspect the final layout with the
  font actually used, including table wrapping and one-page fit.

## Evidence and writing rules

- "Absent" means absent from tested answers for the specified prompt, engines,
  and scan, not absent from every AI assistant everywhere.
- AEO does not measure leads, calls, revenue, search demand, or causation.
  Never present those as measured outcomes, claim projected uplift, or imply
  that a competitor took customers. A citation does not prove why a brand won.
- Distinguish observed measurements, AI-inferred prompt groups, interpretation,
  and proposed actions. Label groupings as inferred from tracked questions in
  the method note. Public-web research is optional and must be labeled separately;
  it cannot supply missing measured outcomes or segmentation counts.
- Avoid generic recommendations, unsupported market-wide claims, and choosing
  only bad questions for prospect outreach. The report should remain useful
  when results are positive, mixed, or there is insufficient segmentation.
- Prefer concise American English and buyer-relevant labels. "Recommended"
  means recommended by an answer engine; label proposed actions separately.
- Keep internal references out of every visible part of the report, including
  its title, body, captions, method note, and footer. Do not display scan IDs or
  shortened scan identifiers, prompt/answer/audit IDs, engine keys, MCP tool
  names, resource URIs, or other implementation references. Use the measurement
  date, readable engine names, exact question wording, and relevant public source
  names or URLs to give the reader useful context instead. Preserve internal
  references in the working evidence for verification.

## Client-side output checks

Confirm that pitch-angle selection and storyboard review were completed, already
resolved in context, or explicitly delegated. Check the final headline, visual,
example, and invitation against the working story brief. Do not substitute a
different pitch during rendering or include private agency discussion in the PDF.

Before finalizing, verify that every number has a source, scope, numerator and
denominator (where available), and same-scan evidence; every group has its
prompt-ID membership; and competitor rollups have complete prompt evidence.
Check unclassified questions, overlaps, missing engines, zero denominators,
and pagination. Remove every sample fact and revise headlines after fallbacks.
Check that the scope appears in one compact line, material caveats are
consolidated in one short method note, and no internal references are visible.

Create the PDF locally, render it to an image, and inspect for clipped text,
overlap, unreadable type, and accidental second pages. Verify exactly one page,
not just a screenshot of the first page. Return the PDF artifact to the user.
If the user requested HTML, return the self-contained HTML instead and verify
its screen and print layouts; do not claim a PDF was created when it was not.
