# About this one-pager

**This one-pager was drafted by Claude, Anthropic's AI model.** Owen Hughes asked for it, set the questions, directed the revisions and decided what to keep. No person outside the project has reviewed it. It is not peer reviewed.

Read it as a practical explainer that can still contain errors, not as an authoritative guide. Corrections are welcome.

## How it was produced

1. **Draft.** Claude wrote the first version from general knowledge, with no searches and no sources opened.
2. **Integrity read (research-integrity skill).** The same Claude session that wrote the draft then checked it, so this was not an independent review. It flagged seven claims that went further than their evidence. These included an example figure that could be read as a real result, pass thresholds that looked like standards, an unsourced claim about bias in AI judges, and an unsourced regulatory claim.
3. **Sourcing.** Claude searched for and read two sources: Zheng et al. (2023) §3.3 on judge biases, and McHugh (2012) on interpreting kappa. The first copy of McHugh tried (PubMed Central) was blocked by a browser check, so the publisher's copy was read instead. Its Table 3 is an image and was not read.
4. **Revision.** Claims were rewritten to match those sources, illustrative figures and estimates were labelled, and the regulatory claim was removed. Two sections were added after discussion: evals without manual coding, and evals vs hardening skills.

## What to trust, and how much

- **Read directly:** the judge-bias findings (Zheng et al.) and the kappa threshold (McHugh).
- **Claude's own reasoning, not sourced:**
  - the definition and parts of an eval
  - the pros and cons
  - the use-case table and its other pass criteria
  - the no-code methods and their time estimates
  - the pilot plan

## What this one-pager does not claim

- It does not show that evals improve research quality. Nothing here measured that.
- The pass criteria, other than the kappa threshold, are not industry standards.
- The methods for evals without manual coding are a suggested approach, not a published or validated method.

*Tools: Claude (Anthropic) for drafting, the integrity read and revision; web search and web fetch for sources. Last updated 17 November 2026.*
