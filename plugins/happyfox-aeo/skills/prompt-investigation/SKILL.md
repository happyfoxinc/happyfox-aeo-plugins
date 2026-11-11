---
name: prompt-investigation
description: Investigate why AI engines omitted, recommended, or misrepresented a brand in answers to one tracked prompt. Use recorded HappyFox AEO answers and relevant public sources to decide what action is justified.
---

# Investigate a tracked prompt

Start with one prompt the user selected. Reuse the brand and prompt from the
conversation. If needed, use `list_brands` and `list_prompt_performance` to
offer candidates with an observed reason for each, then let the user choose.

Identify the buyer's requirements, constraints, and buying stage. Label inferred
requirements. Check brand fit against current product documentation and supplied
facts, distinguishing published claims from independently demonstrated evidence.
Decide what success means for this buyer, such as an accurate comparison,
a recommendation, or a supporting citation.

After selection, work through the following steps autonomously.

1. Read [Engine evidence](references/engine-evidence.md) before interpreting
   `get_prompt_evidence`. Compare each available answer with its audited outcome.
2. Follow [Diagnosis and public research](references/diagnosis-and-research.md)
   to test explanations against the recorded answers and current sources.
3. Use [Actions and validation](references/actions-and-validation.md) to decide
   what the evidence justifies, including further investigation or no action.
4. Use [Investigation report](references/investigation-report.md) to explain what
   happened, what remains uncertain, and which evidence supports any proposed action.

Ask for business context only when public sources and facts already supplied
leave a material decision unresolved. Explain which decision depends on the
answer, continue independent work, and mark dependent conclusions provisional.
Record missing telemetry or inaccessible sources as limitations. Deliver proposals
only. Publishing content, contacting third parties, changing product data, or
submitting to providers requires separate authorization.
