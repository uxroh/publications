# About this report

**This re-analysis was researched and written by Claude, Anthropic's AI model.** Owen Hughes commissioned it, set the questions, directed the revisions and decided what to publish. Its figures were checked by separate AI sessions against the sources and the downloaded data. No person has independently checked them all, and no one outside the project has reviewed the report. It is not peer reviewed.

Read it as a structured, sourced analysis that can still contain errors, not as an authoritative study. Corrections are welcome.

## Conflict of interest

The report assesses researchers' responses to Lenny Rachitsky's job-market report. One of those responses, the uxroh Substack post "Reading Lenny's job market data as a user researcher", is Owen's own. The report was asked to treat that post like any other source and to say where the evidence strengthens it and where it complicates it. Readers should still weigh the report with that connection in mind.

## How it was produced

1. **Question.** How robust are the user research figures in Lenny Rachitsky's "State of the tech job market: late 2026" (10 Nov 2026)? What do they measure and exclude, how do they compare with independent evidence, and how well supported is his interpretation?
2. **Research (deep-research skill).** Four AI research sessions worked in parallel, each on one strand:
   - researchers' published responses
   - how the two data sources (TrueUp and Live Data Technologies) work
   - independent job-market data
   - the evidence behind Lenny's explanations

   Each saved notes with sources and recorded what it could not access.
3. **Drafting.** A separate AI session wrote the report from those notes, checking Lenny's figures and quotes against the full text of his post.
4. **Integrity review (research-integrity skill).** This step followed rules that each claim stays within its evidence, that sources that failed to load are recorded, and that AI review is labelled as AI review.
   - **Adversarial review.** A separate AI session checked every number and quote against the sources and looked for claims that outran their evidence. It raised 2 must-fix and 14 should-fix findings.
   - **Refutation pass.** Another session tried to disprove each finding. None was fully refuted; several were narrowed.
   - **Revision.** A further session applied only the findings that survived.
   - **Confirmation.** A third reviewing session confirmed the fixes and recalculated the new arithmetic.
5. **Longer-term data (15 Nov 2026).**
   - **Older Indeed posting data:** Indeed posting data back to 2018 was gathered from Indeed Design articles and Jakob Nielsen's reporting.
   - **Indeed tracker:** Indeed Hiring Lab's public job-postings tracker was downloaded from GitHub and its figures recalculated directly.
   - **Review:** A separate AI session checked the new sections and corrected several overstatements. The later rewrite of the Interpretation section, a reordering of figures already in the report, was not separately reviewed.
6. **Charts.** The charts were drawn with Python and matplotlib from figures in the report or the downloaded Indeed data. Values that are Claude's own arithmetic are marked as such in the chart notes and the report.

The full review log, with every finding, the refutation attempts and the confirmation reads, is in [integrity-review.md](integrity-review.md). It is a working file and rougher than the report.

## What to trust, and how much

- **Read directly:**
  - Lenny's figures and quotes
  - the Indeed Design and Nielsen figures
  - the User Interviews survey
  - IT Jobs Watch
  - the funding dates for Listen Labs and Simile
- **Calculated from downloaded data:** the Indeed Hiring Lab tracker figures.
- **Known only second-hand or from search summaries:**
  - Inna Tsirlin's analysis, and Lenny's comment reply (both via the uxroh post)
  - the January 2026 Brookshier and Altenhoff update
  - Pybus's −89%
  - the ratio of research to design job ads

  The report labels each of these where it is used.
- **Not accessible at all:**
  - TrueUp's and Live Data Technologies' own methodology pages
  - the LinkedIn posts in the debate
  - Lenny's paywalled earlier reports
  - Judd Antin's original essay

  What the report says about the vendors' methods comes from secondary descriptions.
- **Claude's own reasoning, not published figures:** derived numbers (retention ratios, prior-year counts, sensitivity scenarios, the ~85% share). These are labelled in the text.
- **Claude's interpretation, not a finding:** the "Interpretation" section is Claude's reading of the evidence, with a support level marked on each point. It is not necessarily Owen's view.

The "How this report was produced and checked" section at the end of the report has the claim-by-claim access table and the full list of blocked sources.

## What this report does not claim

- It does not show the true size of the UX research job market in the US, the UK or globally.
- It does not establish what caused the decline.
- It does not measure how much research work is done or by whom.
- It does not show that Lenny's figures are wrong. It argues they measure something narrower than the headline suggests.

*Tools: Claude (Anthropic) for research, writing, review and charts; web search and web fetch for sources; Python for data and charts. Last updated 15 November 2026.*
