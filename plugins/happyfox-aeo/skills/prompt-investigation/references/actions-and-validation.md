# Actions and validation

## Develop actions that pass evidence prerequisites

Brand absence triggers investigation, not an automatic recommendation to create
content. Propose an action only when it has a concrete target, supporting evidence,
and a plausible mechanism for improving the desired outcome.

| Action type | Prerequisites and required specificity |
| --- | --- |
| update_owned_page | Identify and inspect the exact existing page; describe the missing, misleading, or insufficient material and the substantiated change |
| create_owned_page | Review relevant existing content and establish an unmet need; if inventory/discovery is incomplete, investigate before claiming a page is missing |
| propose_third_party_update | Inspect the exact source; identify a factual correction or editorially reasonable inclusion, supported by evidence; draft a proposal without sending it |
| fix_technical_issue | Identify a specific observed defect and affected URL or configuration; do not infer blocking or indexing failure from absence in an answer |
| add_product_evidence | Identify the unsupported claim, evidence needed, and intended destination; never invent examples, customer outcomes, or capabilities |
| review_product_fit | Identify the buyer requirement and verified product mismatch; propose targeting, positioning, or product review without concealing limitations |
| investigate_further | Specify missing evidence, the next check, and the decision that check will unlock |

No action is appropriate when the brand does not fit, the desired outcome is
already met, or no intervention is justified. Explain why. A citation gap alone
need not be a problem when the answer recommends the brand accurately using
independent evidence.

Consolidate actions with the same target and underlying problem, linking all
supporting engine observations. Keep different fixes separate. Prioritize by
buyer/business relevance, evidence strength, observed scope, recurrence only when
established, effort, and dependencies. Unknown business value stays unknown;
tracked prompt counts do not measure market search demand. Avoid projected uplift,
traffic/revenue promises, guaranteed ranking, and generic tasks such as "improve
authority" or "write more content."

## Define completion and effectiveness separately

For each action specify what must be delivered, and what subsequent observation
would support or weaken its hypothesis. A published edit completes implementation;
it does not resolve the visibility issue by itself.

Where possible, first establish whether updated content is being observed. Then
compare relevant retrieval, answer accuracy, citations, or recommendations across
comparable repeated observations. Keep engine/model, prompt, surface, and other
available conditions consistent. API observations do not automatically describe
consumer-app behavior. Use unchanged topics as a comparison where available.
Before/after movement is not proof that an intervention caused it.

Do not claim to have validated a result without the necessary follow-up evidence.
With only the latest reported scan available, describe future validation and its
data requirements. Distinguish implemented, observed improvement, inconclusive,
and contradicted hypotheses.

