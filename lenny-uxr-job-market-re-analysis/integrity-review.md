An in-project reading by a separate AI session. It is not an outside review.

# Integrity review: "Lenny's UXR collapse is real but mismeasured"

Reviewed 14 Nov 2026. Report: `/home/claude/reports/Scrutinising Lennys UXR job figures.md` (line numbers below refer to that file). Checked against Lenny's source text (`_source_lenny_report_text.txt`), the four note files in this folder, and live fetches of cited pages.

**Access labels used:**
- **read-directly**: the page was fetched in this review. WebFetch returns a model summary of the page, so a phrase reported as "not found" means not found in that summary. It does not prove the phrase is absent.
- **notes-only**: the claim was checked only against the research notes.
- **reasoning**: the point is my own arithmetic or logic.
- **BLOCKED**: the page could not be loaded.

---

## Must-fix

### M1. The layoff comparison does not compare like with like, and the "mechanism" built on it does not hold
**Report text:**
- L27: "21% of companies laid off UX researchers … Layoff rates for researchers were *lower* than for design (26%) and engineering (24%)"
- L29: "That points to **a collapse in backfill and new requisitions**"
- L57: "researchers' layoff rate *below* design and engineering"
- L87: "The decline appears to come mainly from requisitions that were not refilled, not from layoffs"

**Problems:**
1. **Two different measures are mixed.**
   - The User Interviews page gives the 21% as the share of *respondents* who said their company laid off user/UX researchers.
   - The design (26%), engineering (24%) and PM (21%) figures come from a separate per-department breakdown, "Functions affected by layoffs in the last 12 months".
   - In that breakdown, UXR is described only as "slightly below" those three departments. The page also gives the average across departments as 20%.
   - So the UXR number set against 26% and 24% is not from the same series. The report also leaves out that PM was 21% and the average was 20%. On the source's own framing, UXR sits at about the average, not clearly "lower".
   - The question wording and denominator are not published. UserTesting's summary does not say how the peer figures were measured either.
2. **It is not a layoff "rate".**
   - The figure is the share of respondents whose company laid off *anyone* in that function. That is a prevalence measure, not the share of staff who lost their jobs.
   - Bigger departments are mechanically more likely to report at least one layoff. A company with 2 researchers and 40 designers is far more likely to report design cuts.
   - About 14% of respondents' companies have no dedicated UXRs at all, so they cannot report UXR layoffs.
   - The figures therefore cannot show that UXRs were fired at a similar or lower rate than other functions.
3. **The timing does not match.**
   - The comparison covers only the 12 months to mid-2025.
   - Most of the fall in hires was 2022–24 (the report's own claim at L41).
   - The 2024 survey gives 22% for researchers but no departmental comparison, as far as the notes record.
   - The notes also record contrary evidence the report leaves out. MeasuringU/UXPA (via User Interviews' job-market guide) found that 35% of organisations reduced UX staff, about twice recent rates, and called it the worst year on record. Dovetail describes UXRs as hit disproportionately in 2022–23, though without figures.
4. **The inference does not follow.**
   - Lenny's figure counts *hires*. Layoffs do not lower a hire count, so a fall in hires is a fall in filled requisitions by definition.
   - Comparing layoff prevalence across functions cannot show that the decline came "from requisitions … not from layoffs". Neither dataset measures the stock of UX researchers, or how it is shrinking.

**Evidence:**
- User Interviews 2025 page, read-directly: "slightly below Product/UX Design (26%), Engineering (24%), and Product Management (21%)"; average 20%.
- UserTesting summary, read-directly: researchers "less affected" than design and engineering, with no method given.
- Notes `alternative_market_data.md` L63–67 and L87–91 (UXPA 35%, second-hand).
- Points 2 and 4 are reasoning.

**Suggested correction:**
- Report the figure as "21% of respondents said their company laid off UX researchers".
- Describe the department breakdown as UXR roughly in line with the 20% average and slightly below design, engineering and PM. Note that this is a measure of whether any layoff happened, not a rate, and that it covers 2025 only.
- Mention the UXPA 35% figure.
- Turn the "mechanism" paragraph (L29), the L57 point and the L87 conclusion into a hypothesis. For example: "Survey data cannot tell whether the function shrank mainly through layoffs or through not backfilling; the hiring fall itself reflects fewer filled requisitions by definition."

### M2. "12–13 percentage points" is the wrong way to compare the declines, and it understates the UXR-specific gap
**Report text:**
- L3: "roughly 12–13 percentage points that need a research-specific explanation, not the full two-thirds"
- L53: "only 12–13 points smaller"
- L66 table verdict: "margin modest"

**Problem:**
- Subtracting percentage declines is not the right way to take out a shared correction.
- Since 2022, UXR kept 34% of its hires, design 46% and engineering 47%.
- Measured against the path design and engineering followed, UXR hiring is about 26–28% lower than it would have been. That is roughly a quarter of the remaining level.
- So the UXR-specific shortfall is substantial. "Modest" and "only 12–13 points" downplay it. They also clash with the report's own point that UXR is in the same correction as other roles.

**Evidence:**
- Reasoning on Lenny's figures, source text L97–99, 154–156, 175–177:
  - UXR: 1,800/5,300 = 0.340
  - Design: 12,600/27,600 = 0.457
  - Engineering: 113,000/239,000 = 0.473
  - Relative gap: 0.340/0.457 = 0.74 and 0.340/0.473 = 0.72

**Suggested correction:**
- State that UXR hires fell about a quarter further than design and engineering hires, in relative terms.
- Keep the point that most of the fall is shared with other roles.
- Change the table verdict to something like "literally true; UXR-specific gap is real but much smaller than −66% implies".

---

## Should-fix

### S1. The ratio restatement is counted as a second, "quiet" precedent
**Report text:**
- L11: "the historical series was quietly recalculated backwards"
- L53: "two documented precedents … the PM-to-design ratio was quietly restated from 1.27 to 2.6"

**Problem:**
- The 1.27 → 2.6 restatement follows directly from the design regrouping that Lenny's footnote discloses.
- PM openings come out the same under both groupings: 1.27 × 5,700 ≈ 7,240 in March, and 3.8 × 1,900 ≈ 7,220 now.
- That makes this one disclosed redefinition with a knock-on effect, not two precedents, and it was not "quiet".
- The fair point that survives is narrower: the footnote does not mention that past ratios changed.

**Evidence:**
- March 2026 post, read-directly: "currently 1.27x", about 5,700 design roles, non-tech companies excluded.
- Lenny's footnote 1 and L158–160 of the source text.
- The arithmetic is reasoning.

**Suggested correction:** Call it one disclosed redefinition that retroactively changed published ratios without saying so explicitly.

### S2. Small-base arithmetic confuses the level with the rate
**Report text:** L21: "One large employer opening or freezing 20–30 requisitions would shift the headline rate by 20–30%."

**Problem:**
- 20–30 postings is about 20–28% of the 108 *level*.
- Against the derived base of about 196, the *rate* would move from −45% to about −35% or −30%. That is a shift of 10–15 points.
- The notes say "national figure" (meaning the level). The report changed this to "headline rate".

**Evidence:** Reasoning; `data_methodology.md` L155.

**Suggested correction:** "…would change the count by about a fifth to a quarter and move the −45% by 10–15 points."

### S3. The concentration claim outruns the evidence
**Report text:**
- L21: "a budget decision at two firms explains a large share of the total"
- L87: "concentrated in a handful of Big Tech budgets"

**Problem:**
- One in eight is 12.5% of 2025 hires, so seven-eighths came from elsewhere.
- No data shows how much of the *decline* came from Meta and Google.
- The "Google only 50+" figure for 2026 is partial-year data, and the report itself calls it fragile.

**Evidence:** Source text L178–180; reasoning.

**Suggested correction:** "Meta and Google made about one in eight hires, so a few firms' decisions matter, but the data does not show how much of the decline they drove." Drop "concentrated in a handful of Big Tech budgets" from the conclusion.

### S4. Two phrases are quoted as if verbatim but do not match the source
**Report text:**
- L27: Headcount and team structure were described as "largely consistent".
- L43: MeasuringU concluding results are "directional rather than precise".

**Problem:**
- The User Interviews page says headcount and team sizes "stayed consistent", with some movement "around the margins". It does not say "largely consistent". That phrase came from the notes.
- The fetched MeasuringU text says synthetic results "can provide directional signals" but are "often imprecise". The exact quoted phrase was not found.

**Evidence:** Both pages read-directly (fetch summaries).

**Suggested correction:** Remove the quotation marks or use the source wording.

### S5. A Lenny paraphrase is presented as a quote
**Report text:** L23: he reads that gap as "landing great people is getting harder".

**Problem:** Lenny writes "landing great PMs is getting harder" and "landing great engineers is getting harder too". The quoted phrase does not appear.

**Evidence:** Source text L85 and L105–106, read-directly.

**Suggested correction:** Quote one of his actual phrases, or remove the quotation marks.

### S6. The unit is wrong: "companies" should be "respondents"
**Report text:**
- L27: "21% of companies laid off UX researchers"
- L31: "share of companies with zero dedicated UXRs"

**Problem:**
- Both figures are shares of survey respondents, and the respondents are UXRs. The 2019 figure is worded as "19% of UXRs said that their company had zero dedicated UXRs".
- Several respondents can come from one company.
- The 2019, 2022 and 2025 samples were also recruited differently, so comparing across years is rough.

**Evidence:** User Interviews 2025, read-directly.

**Suggested correction:** Say "respondents' companies", and add a one-clause comparability caveat.

### S7. Sample shrinkage is treated as evidence that the field is shrinking
**Report text:** L27: the respondent pool shrank 36%, "which is itself a sign of a field losing people"

**Problem:**
- A volunteer survey can shrink because of recruitment and response rates.
- The notes say only that this "may" signal contraction.

**Evidence:** `causal_claims_context.md` L124; reasoning.

**Suggested correction:** "…which may reflect a smaller field, though it could also reflect recruitment."

### S8. The timing argument rebuts the two named tools, not "better tooling" in general
**Report text:**
- L41: "Timing is the strongest objection to the tooling explanation"
- L55: "The tools Lenny names cannot have caused most of the drop"
- L72: "Unsupported as main cause"

**Problem:**
- Lenny gives Listen Labs and Simile as examples ("e.g.") of "better UXR tooling".
- General-purpose LLMs (ChatGPT from late 2022) and earlier research platforms were available during the 2023–24 fall.
- The funding dates rule out the two examples as the cause. They do not rule out tooling as a cause.
- Tsirlin's point that LLMs became part of everyday work only in 2025 is the relevant counter. It is known only through the uxroh summary.

**Evidence:** Source text L190–191; reasoning.

**Suggested correction:**
- Narrow the claim to the named tools.
- Address broader AI tooling separately, citing Tsirlin's timeline point with its second-hand label.
- Note that the prior-year hiring window (May 2024–Apr 2025) overlaps Listen Labs' April 2025 round.

### S9. LDT's source is stated as fact when it is inferred
**Report text:**
- L3: "The hiring data comes from public professional profiles, which update late and get rewritten"
- L19 applies the NBER and Revelio LinkedIn findings directly to LDT.

**Problem:**
- LDT describes its source as "public information on the open web" gathered by prompt-engineering search engines.
- The notes say profiles are *likely* the main source, but LinkedIn is unconfirmed.
- The NBER and Revelio results are about LinkedIn data, so applying them to LDT is an inference.

**Evidence:**
- Pacific Business Times, read-directly.
- `data_methodology.md` L59 and L104.

**Suggested correction:** "…appears to be derived largely from public professional profiles…" Label the transfer of the NBER and Revelio findings to LDT as an inference.

### S10. The alternative explanations are not held to the standard used against Lenny's
**Report text:**
- L45: "these explanations cover the timing far better than 2025-era tools do"
- L87: "That makes it a question of perceived value, the territory of Antin's critique"

**Problem:**
- The report rightly says Lenny's causes are untested.
- Antin's value-proof thesis, the end of near-zero interest rates and retitling are untested by any data here as well.
- Fitting the timing is not the same as being shown to be the cause.
- The L87 conclusion rests on M1 and S3, which do not hold.

**Evidence:** Reasoning.

**Suggested correction:** "fit the timing better, but are also untested here". Recast L87 as one candidate explanation, not a conclusion.

### S11. The boom-baseline evidence is second-hand and its windows are not stated
**Report text:**
- L17: "Indeed Design found UX researcher postings rose 566% across 2020–21"
- L53: "Indeed's 566% boom"

**Problem:**
- Dovetail credits the 566% to "Indeed Design data". It gives no measurement window or base year.
- "2020–21" is inferred from the surrounding paragraph.
- Pybus's dataset covers only June 2021 to September 2022 (15 months). It shows a February 2022 peak within that window. It does not compare against pre-boom levels.

**Evidence:**
- Dovetail, read-directly.
- UX Collective (Pybus), read-directly: 21,639 descriptions, peak of 2,990 in February 2022.

**Suggested correction:**
- Write "Dovetail, citing Indeed Design data (window unspecified), reports…"
- Give the Pybus window.

### S12. The conclusion states unmeasured directions as fact
**Report text:**
- L85: headcount data "will understate how much research gets done and overstate how far the discipline has shrunk"
- L85: "compatible with stable or even growing demand"

**Problem:**
- The report presents no measure of research activity, as it says itself at L57.
- The direction is plausible but not established.
- "Even growing" has no supporting evidence.

**Evidence:** Reasoning; report L57.

**Suggested correction:** "is likely to understate…". Drop "or even growing", or label it as speculation.

### S13. The "speed argument proves too much" rebuttal is weak
**Report text:** L39: the speed argument "would hit engineering hard too, yet … engineering openings up 44% since January 2024"

**Problem:**
- Lenny's speed claim is about research and design *process*. Faster shipping could plausibly raise demand for engineers.
- The rebuttal uses engineering *openings*. Engineering *hires* fell 17% over the same period and 53% since 2022.
- Lenny also says engineering openings have now stalled (+2.5% this year).

**Evidence:** Source text L90–91 and L104–105.

**Suggested correction:** Remove this rebuttal, or weaken it to "the report offers no measure of release speed to test it".

### S14. The 86% figure is weaker than presented, yet it carries a verdict
**Report text:**
- L73: "86% of organisations retain UXRs (second-hand)", used to support "contradicted by available evidence"
- L57: "the most-cited figures"

**Problem:**
- The public User Interviews page (fetched) shows no 86% figure and no "people who do research" 71% figure. The 71% on the page refers to something else.
- The only source found for these figures is Perspective AI, an AI-interviewer vendor.
- "Most-cited" has no support: one citing source was found.
- Lenny poses extinction as a question ("I wonder if"). "Contradicted" is stronger than the evidence allows.

**Evidence:**
- User Interviews, read-directly (figures not found in summary).
- Perspective AI, read-directly.

**Suggested correction:**
- Change the verdict to "Speculative; not supported by available evidence".
- Remove "most-cited".
- Say the figures could not be found on the public report page.

---

## Minor

1. **IT Jobs Watch denominator** (L33): The page gives the share as a percentage of all permanent jobs in its sample, not of "all IT ads". The year-earlier figure (59) was itself a trough, below 2024's 76. Against 2024 the rise is about 68%, not a doubling. Source: IT Jobs Watch, read-directly.
2. **Volatility claim** (L23): "A smaller population is also expected to swing further." At about 1,800 hires, pure counting noise is around 2%, so it cannot explain the gap. Only concentration in a few employers could. Reasoning.
3. **Internal tension:** L3 says independent "job-board data agree on the direction", but L33 says UK data "runs against Lenny's direction". Say "US job-board data".
4. **LinkedIn access wording** (L59): the posts are described as "largely unindexed". The notes record that they were blocked by the session allowlist. Say "could not be accessed".
5. **Hiring window** (L9): "May 2025 to April 2026" is stated for engineering. For UXR, Lenny says only "over the past year". Applying the same window to UXR is a reasonable inference, but it should be labelled as one.
6. **Lag wording** (L19): "fully complete earlier one" should be "more complete".
7. **Sponsors** (L47): "his audience and sponsors are PMs and AI tool companies" is cited only to Lenny's post. The notes' sponsors page lists research tools (Dovetail, Sprig), which cuts against the "specialists get automated" incentive story. The Insider bundle is a set of perks, not sponsors.
8. **Pre-boom baseline** (L17): a method unchanged since 2019 does not mean coverage was unchanged. The panel grew from about 70M to 124M, and earlier records are exposed to retrospective edits.
9. **Anthropic role** (L35): correct, but the posting is now closed (posted 9 Sept 2026). Adding "since closed" would help. The OpenAI postings are undated. Say so.
10. **Notes disagree on the Antin date:** `community_critiques.md` says it was unverified. Read-directly confirms 4 Jan 2024, so the report's "early 2024" is correct.
11. **NN/g "agrees with this picture"** (L29): NN/g describes the timeline and says senior roles are recovering faster. It says nothing about backfill versus layoffs. Narrow to "is consistent with the timeline".
12. **Retitling evidence** (L53): "63% … had held one" covers promotions and moves into other functions, not only retitling. The base for the 20% figure is not stated on the page.

---

## Claims checked and found correct

| Claim (report line) | How checked |
|---|---|
| Lenny's quotes: 1,800; −66%; 5,300; "steepest drop"; −22%; 1 in 8 Meta/Google; "Google is the only company to have hired 50 or more"; 108 at tech companies globally (L7) | Source text L175–181 |
| UXR openings −45%; design −28% (L7, L70) | Source text L287–288 |
| Engineering 239k→113k, design 27.6k→12.6k (L23); −53% and −54% derived correctly | Source text L97–99, 154–156; reasoning |
| Engineering openings +44% since Jan 2024 (L39) | Source text L104–105 |
| Derived about 196 openings, about 88 fall, about 2,300 prior-year hires (L21, L75) | Reasoning: 108/0.55 = 196; 1,800/0.78 = 2,308 |
| 124M panel; LDT hiring numbers US-only; TrueUp powers Lenny's Jobs (L9, L47) | Source text L47–51 |
| Footnote: design about 5,000 → about 2,000; illustrator, creative director and brand designer removed (L11) | Source text L335–338 |
| 2.6 "earlier this year" (L11) | Source text L159–160 |
| March 2026: 1.27x, about 5,700 design roles, non-tech companies and agencies excluded (L9, L11) | Lenny March 2026, read-directly |
| Lenny's causal quotes and "going extinct" (L39) | Source text L186–192 |
| TrueUp "Big Tech companies and 'top' startups" (L9) | Pragmatic Engineer, read-directly |
| LDT prompt-engineers search engines; 70M panel; white-collar focus (L9) | Pacific Business Times, read-directly |
| LDT-affiliated newsletter separates company and internal changes (L9) | Human Capitalist, read-directly (95M+ vs 55M+) |
| LDT revalidates about every 10 days, by its own description, via a competitor (L19) | Signalbase, read-directly |
| NBER 19.7% of established US (LinkedIn) users edit past jobs (L19) | NBER w35546 abstract, read-directly |
| Revelio "nearly one in three" among tech workers (L19) | Revelio blog, read-directly |
| Pybus: 21,639 Indeed postings, peak February 2022 (L17) | UX Collective, read-directly (window caveat in S11) |
| 566% vs 265% from Indeed Design data (L17) | Dovetail, read-directly (window caveat in S11) |
| User Interviews: 485 responses; sample −36%; 49% (+26 points); 67%; zero-UXR 19% / 6% / about 14%; 63%; 20% (L27, L31, L53) | User Interviews 2025, read-directly |
| IT Jobs Watch: 128 vs 59; £60,500 (+17.5%); 0.10% vs 0.11%; rank 605→717 (L33) | IT Jobs Watch UX Research, read-directly |
| User Experience Researcher title ads tagged Digital Banking (8 of 33), Fintech (3), Wealth Management (3) (L33) | IT Jobs Watch, read-directly |
| BLS market research analysts profile does not mention UX (L33) | BLS OOH, read-directly |
| Anthropic UXR, Platform, US$305k–385k, September 2026 (L35) | General Catalyst board, read-directly (posted 9 Sept 2026, now closed) |
| Listen Labs $27M seed and Series A led by Sequoia, April 2025; buyer turned out to be marketing (L41, L43) | Fortune, read-directly (23 Apr 2025) |
| Listen Labs $69M Series B, January 2026 (L41) | VentureBeat, read-directly (16 Jan 2026, Ribbit, $500M valuation) |
| Simile $100M Series A and >$200M Series B, both 2026; 85% of two-week test–retest consistency (1,052 people); named customers (L41, L43) | Unite.AI, read-directly (30 July 2026; Series A about five months earlier, roughly February 2026, inferred from the article) |
| NN/g synthetic users: over-reported good behaviour, sycophancy, supplement not replace (L43) | NN/g, read-directly |
| MeasuringU: 12 studies, compressed variance (L43) | MeasuringU, read-directly (quote issue in S4) |
| Antin, Lenny's Podcast, 4 Jan 2024, "middle-range" research (L45) | Lenny's Newsletter, read-directly |
| NN/g State of UX 2026: timeline; senior and generalist roles recovering faster; story "convenient in a cost-cutting environment" (L29, L45) | NN/g, read-directly |
| uxroh: Hughes's framing; Lenny's reply as paraphrased; Tsirlin summary; Layoffs.fyi founder via Crunchbase; Yitty comment (L17, L51, L57) | uxroh, read-directly (all second-hand relays, correctly labelled as such) |
| Lena Kul: retired design recruiter; "tech and tech-ish"; method "since 2019"; 1 of 17 roles; ChatGPT-generated figures (L17, L51) | Lena Kul, read-directly |
| Perspective AI cites 71% / 86% to User Interviews 2025 (L57) | Perspective AI, read-directly (1 Jun 2026) |
| Vendor methodology not read first-hand; paywalls; second-hand democratisation figures disclosed (L13, L59, L75) | Matches the access caveats in the notes |

**Not re-checked in this review (notes-only):**
- NFX Signal (behind login, per notes)
- Stripes OpenAI posting
- Revelio methodology page
- Lenny's podcast sponsors page
- GOV.UK user research blog (January 2025)
- Crunchbase layoffs article
- Indeed Design Medium piece

---

## BLOCKED sources

| Source | Status |
|---|---|
| trueup.io (methodology and company pages) | BLOCKED per notes (client errors); not re-attempted |
| livedatatechnologies.com | BLOCKED per notes (not on allowlist); not re-attempted |
| DDaT framework: user-researcher page (L33) | BLOCKED in this review. Redirects to understand-digital-data-roles-skills.service.gov.uk, which is not on the allowlist. Its date claim rests on the notes and the GOV.UK blog, which were not re-checked. |
| LinkedIn posts: Tsirlin, Constantine, Loosbrock, Zeng, Venkat | BLOCKED per notes; known only via uxroh |
| Lenny comment permalink (/comment/384428098) | BLOCKED per notes; known only via Hughes's paraphrase |
| The Voice of User, "Is UXR going extinct?" | BLOCKED per notes |
| Great Question survey page | BLOCKED per notes |
| NFX Signal and CB Insights portfolio detail | Behind login, per notes |
| Paywalled parts of the Lenny reports (July 2024, May 2025, March 2026) and the 29 comments on the late-2026 post | Not visible, per notes |
| AI Weekly and Optimixed summaries | Not fetched, per notes |

The report discloses the vendor-site, LinkedIn, comment and paywall gaps accurately (L13, L59, L75). It does not mention the DDaT redirect. It also describes the LinkedIn gap as "unindexed" rather than blocked (minor item 4).

---

## Refutation pass (second separate AI session; not an outside review)

Done 14 Nov 2026. A second AI session tried to refute each M and S finding above. This is still an in-project check, not an outside review. The same access labels apply: WebFetch returns a model summary, so "not found" means not found in that summary.

**Re-fetched in this pass (read-directly):**
- User Interviews 2025 report
- User Interviews job-market guide (UXPA 35%)
- MeasuringU synthetic-users review
- Dovetail "Responding to the reckoning"
- Lenny March 2026 design section
- Perspective AI
- UX Collective (Pybus)

**BLOCKED in this pass:** none. Sources the first pass marked BLOCKED were not re-attempted.

### Verdicts

**M1: SURVIVES, with sub-point 1 narrowed and sub-point 3 qualified.**
- **Sub-point 1 is overstated.**
  - The UI page says UXR layoff prevalence was "slightly below" design (26%), engineering (24%) and PM (21%).
  - So the report's *direction* ("lower than design and engineering") is supported by the source's own departmental comparison. The report is not comparing across mismatched series on that point.
  - What survives:
    - The report pairs that comparison with the separate headline 21%.
    - It omits PM (21%) and the 20% average.
    - "Lower" overstates what the source calls "slightly below".
- **Sub-points 2 and 4 survive, and sub-point 2 cuts harder than the first pass said.**
  - The measure is prevalence: did the company lay off anyone in that function. Prevalence is biased upwards for larger departments.
  - So UXR roughly matching much larger design and engineering departments suggests per-capita UXR layoff exposure may be *higher*, not lower (reasoning).
  - The L29/L57/L87 "backfill not layoffs" mechanism therefore lacks support. A fall in hires is a fall in filled requisitions by definition.
- **Sub-point 3 needs a qualifier.**
  - The UXPA/MeasuringU 35% is about *UX staff* in general, not UXRs.
  - The guide gives no year for it explicitly; the linked URL implies 2025.
  - It contradicts the report's "steady attrition" framing. It does not contradict the UXR-versus-design comparison specifically.
- **Fix:** as the first pass proposed, but describe the UXR figure as "slightly below design, engineering and PM; near the 20% average". Do not imply the 21% and the 26/24% come from different series.

**M2: PARTLY. Downgrade to should-fix.**
- **My arithmetic:**
  - Retention since 2022: UXR 1,800/5,300 = 0.340; design 12,600/27,600 = 0.457; engineering 113,000/239,000 = 0.473.
  - Percentage-point gap: 66.0 − 54.3 = 11.7, and 66.0 − 52.7 = 13.3. So "12–13 points" is arithmetically correct.
  - Relative gap: 0.340/0.457 = 0.74, and 0.340/0.473 = 0.72. UXR is about 26–28% below the level it would have reached on the design/engineering path.
  - Log decomposition: ln 0.340 = −1.079 and ln 0.457 = −0.784. About 27% of UXR's log decline is UXR-specific.
  - Additive version: UXR on the design path would be at about 2,420 hires. The shortfall of about 620 is 11.7% of the 2022 base, or about 18% of UXR's 66-point fall.
- **Why the finding is overstated:**
  - Subtracting percentage changes is a standard additive decomposition, not "the wrong way".
  - The report's core claim survives under every decomposition: most of the fall is shared, and only roughly a fifth to a quarter is UXR-specific.
  - The report's key sentence ("12–13 points that need a research-specific explanation, not the full two-thirds") is defensible.
- **What survives:** "margin modest" (L66) and "only" (L53) undersell a shortfall of about a quarter of the level.
- **Fix:** add one clause giving the relative framing, and change "margin modest" to "real but much smaller than −66% implies". L3 can stay.

**S1: PARTLY.**
- **The arithmetic holds (reasoning).**
  - March 2026: about 7,300 PM roles and about 5,700 design roles (read-directly), so 7,300/5,700 = 1.28.
  - November: 3.8 × 1,900 = 7,220 PM roles. A restated March design count of about 7,300/2.6 ≈ 2,800 fits the regrouping.
  - So this is one redefinition, and "two precedents" double-counts it.
- **"Quietly" is defensible, though.**
  - The footnote discusses only absolute design counts and asserts "the trends are the same".
  - Yet the restated series turns the early-2023 ratio into 1.9. The March post said PM overtook design only in mid-2023.
  - So the regrouping silently erased a previously published finding (the "flip").
- **Fix:** merge into one precedent. Keep wording that the knock-on change to the ratio, including the mid-2023 flip, was not flagged.

**S2: PARTLY.**
- My arithmetic:
  - Prior base 196. Adding 20–30 openings to today's 108 gives −35% to −30%, a move of 10–15 points.
  - As a *relative* change in the rate, that is about 23–34%.
- So "shift the headline rate by 20–30%" is literally defensible as a relative change. It is ambiguous, though, and drifts from the notes' "national figure".
- **Fix:** clarify the wording as the first pass suggests. This is a clarity fix, not an error fix.

**S3: SURVIVES for L87; PARTLY for L21.**
- Lenny himself says remaining hiring is "concentrated at a few big companies", so a concentration point at L21 is fair. "Explains a large share of the total" for 12.5% is loose.
- L87's "decline … concentrated in a handful of Big Tech budgets" has no support: no data apportions the *decline* by employer.

**S4: SURVIVES.**
- The UI page says "stayed consistent" and does not use "largely consistent". It also answers "Possibly" to whether there are fewer researchers, which the report omits.
- MeasuringU does not contain "directional rather than precise". It says synthetic users "can provide directional signals" but are "often imprecise". The quote came from the notes.

**S5: SURVIVES.** The source has "landing great PMs is getting harder" and "landing great engineers is getting harder too". The report's quoted phrase is a paraphrase. This is trivial to fix.

**S6: SURVIVES.** The UI wording is "21% of respondents said their companies laid off". The zero-UXR figures are framed as UXRs reporting on their own company.

**S7: SURVIVES.** The UI page itself hedges, asking whether there are fewer researchers and answering "Possibly". The report should not be more certain than its source.

**S8: PARTLY.**
- L55 ("The tools Lenny names") and the L72 table row ("Tools (Listen Labs, Simile)") are already scoped to the named tools, so those parts are fine.
- Only L41's "the tooling explanation" and the L3 summary generalise beyond the named tools. Those need narrowing.
- The prior-year window overlap with the April 2025 round is about one month, which is negligible. L41 already allows a contribution to the latest −22%.
- **Fix:** narrow L41 and mention general-purpose LLMs as untested.

**S9: SURVIVES (minor).**
- L9 correctly says "public web information".
- L3 and L19 state "professional profiles" as fact, and the notes say this is likely but unconfirmed.
- **Fix:** add "appears to". Label the transfer of the NBER and Revelio findings to LDT as an inference.

**S10: PARTLY.**
- L45 says the alternatives "cover the timing" better. That is a claim about fitting the timing, and it holds: rates rose from 2022, and Antin spoke in January 2024. It does not assert they caused the decline. Adding "also untested here" is optional.
- L87 ("That makes it a question of perceived value") is a conclusion resting on the M1 mechanism and S3. It needs recasting as one candidate explanation.

**S11: PARTLY.**
- Dovetail (read-directly) gives no window. But its preceding sentence places the surge in 2020 and 2021, so "across 2020–21" is a reasonable reading. It should still be labelled "Dovetail, citing Indeed Design; window not stated".
- Pybus (read-directly) covers June 2021 to September 2022: 21,639 descriptions, with a peak of 2,990 in February 2022, and no pre-2020 comparison.
- The report's L17 sentence is accurate, but L53 uses Pybus as "baseline" backing, which a 15-month window cannot give.
- **Fix:** add the window caveats. Use Pybus only for "2022 was a local peak".

**S12: PARTLY.**
- "Compatible with stable or even growing demand" is a weak logical-compatibility claim and is literally true, so it can stay if the report marks it as possibility, not evidence.
- "Will understate … and overstate" is stated as certain without any activity measure. Change it to "is likely to".

**S13: SURVIVES.**
- Lenny applies the speed theory to design and research *process*, so the design decline is consistent with his theory.
- Faster shipping plausibly raises engineering demand.
- Engineering hires fell 17% since January 2024 (source L104–105), and openings grew only 2.5% this year.
- The rebuttal does not hold. Remove it, or replace it with "no measure of release speed".

**S14: PARTLY. Part of the finding is refuted.**
- **The 86% is not unsupported.** It is the complement of the public page's "nearly 14%" of UXR respondents reporting zero dedicated UXRs: 100 − 14 = 86 (reasoning on the read-directly page).
- So the figure is effectively verifiable from the primary report, as a share of *respondents' companies*, not organisations.
- The report's "not verified in the primary report" (L57) is too cautious for the 86%. It remains true for the 71% people-who-do-research (PwDR) figure: the page's only 71% refers to sharing insights.
- **What survives:**
  - "Most-cited" is unsupported: one source was found (Perspective AI).
  - "Contradicted" is too strong. Lenny's extinction remark is a forward-looking question. A current 86% presence does not contradict a trend, and the zero-UXR share itself rose from 6% to 14%, which is the direction extinction would predict.
- **Fix:**
  - Verdict: "Speculative; not supported by available evidence."
  - Restate the 86% as the complement of the 14% zero-UXR figure among respondents.
  - Keep the 71% flagged as second-hand.

### Net effect
- **Both must-fixes stand in narrower form.**
  - M1 stays must-fix. The "backfill not layoffs" mechanism and the "layoff rate" wording are unsupported, and the prevalence measure may even point the other way.
  - M2 should be downgraded to should-fix. The 12–13 points is correct arithmetic, and only the "modest" framing needs adjusting.
- **Survive as written:** S3 (L87), S4, S5, S6, S7, S9, S13.
- **Narrower fixes:** S1, S2, S8, S10, S11, S12, S14.
- **Refuted:** no finding is fully refuted. The 86% sub-point of S14 and the "mismatched series" sub-point of M1 are refuted.

---

## Confirmation reading (third separate AI session; not an outside review)

Done 14 Nov 2026. A third AI session, which wrote neither the report nor the fixes, compared the revised report with the pre-revision copy, this review, the refutation pass (which governs where it disagrees with the first pass) and Lenny's source text. No pages were re-fetched; quotes from web pages were checked against the wording recorded in this review and the notes (notes-only), and Lenny quotes against the source text (read-directly).

### Status per finding
- **M1: FIXED.** "21% of respondents said their company had laid off"; UXR "slightly below" design, engineering and PM and "near the 20% average", without implying separate series; incidence-not-rate and large-department bias explained ("could mean the reverse"); 2025-only noted; UXPA 35% added with the all-UX-roles and year qualifiers; "steady attrition" removed. L29, L57 and L87 now present the backfill account as an untested hypothesis. No leftover statement of it as fact (L3 now says the data cannot say).
- **M2: FIXED** (as downgraded). L3 keeps "12–13 points" and adds the relative framing; "only" removed at L53; table verdict changed; L23 adds the 34% vs 46–47% retention view.
- **S1: FIXED.** Merged into one redefinition; the unflagged erasure of the mid-2023 flip is kept, as the refutation pass required.
- **S2: FIXED.** Count and rate now separated.
- **S3: FIXED.** L21 loosened claim removed; concentration dropped from the conclusion.
- **S4: FIXED.** Both phrases now unquoted paraphrases of source wording; "Possibly" added.
- **S5: FIXED.** Uses Lenny's actual phrase.
- **S6: FIXED.** "Respondents" wording at L27/L31; cross-year comparability caveat added.
- **S7: FIXED.**
- **S8: FIXED.** L3 and L41 narrowed to the named tools; general-purpose LLMs flagged as untested; Tsirlin labelled second-hand. L55 and the L72 row correctly left as they were.
- **S9: FIXED.** "Appears to" at L3 and in the table; NBER/Revelio transfer labelled as inference. (L19 "LDT re-checks profiles" still says "profiles"; trivial.)
- **S10: FIXED.** L45 "also untested here"; L87 recast as one candidate explanation.
- **S11: FIXED.** Dovetail window "not stated"; Pybus window given and used only for "at least a local peak".
- **S12: FIXED.** "Is likely to understate"; "in principle even growing demand, though nothing here measures that demand".
- **S13: FIXED.** Rebuttal removed from L39 and from the table.
- **S14: FIXED, not over-corrected.** Verdict changed; "most-cited" removed; 86% restated as the complement of the 14% zero-UXR share among respondents (per the refutation pass), 71% kept second-hand; 6%→14% rise noted in the table.

### Arithmetic rechecked (reasoning)
1,800/5,300 = 0.340; 12,600/27,600 = 0.457; 113,000/239,000 = 0.473; ratios 0.74 and 0.72, so 26–28% below. 66.0 − 54.3 = 11.7 and 66.0 − 52.7 = 13.3. 7,300/5,700 = 1.28; 3.8 × 1,900 = 7,220; 7,300/2.6 ≈ 2,810. 108/0.55 = 196; fall ≈ 88. ±20–30 postings: 128/196 and 138/196 give −35% and −30%; 88/196 and 78/196 give −55% and −60%; 20–30 is 19–28% of 108. 1,800/0.78 ≈ 2,310. All match the report.

### Quotes rechecked
Lenny quotes ("the steepest drop of any role we looked at", "My theory is…", "releasing products earlier", "learning and iterating post-launch", "non-UXR people … do user research themselves", "I wonder if…", "landing great PMs is getting harder", "2.6 earlier this year") are verbatim against the source text and under ~15 words. Web-page quotes ("Possibly", "Big Tech companies and 'top' startups", "prompt-engineering", "middle-range", "tech and tech-ish") match the wording recorded in this review and the notes.

### Fixes made directly in this pass
1. L21: the sensitivity parenthetical gave only the "added" direction although the sentence covers opening or freezing. Now reads "(to about −35% or −30% if added, or about −55% or −60% if removed)".
2. Methods section, blocked list: added "NFX Signal and CB Insights portfolio detail (behind login)", which the notes and this review record but the list omitted, although L47 relies on NFX Signal.

### Remaining issues (not changed; for the author)
- **Blocked list includes "Judd Antin's original essay".** Neither the notes nor this review record it as blocked or attempted (the notes cite the Medium link without an access status). Either confirm it was blocked or remove it.
- **Minor 3 unresolved:** L3 still says independent "job-board data agree on the direction", while L33 says UK data runs against it. "US job-board data" would fix it.
- **Minor 5 and 6 unresolved:** the May 2025–April 2026 window is applied to UXR without an inference label (L9), and L19 still says "fully complete earlier one".
- **Methods section:** it opens correctly ("in-project reading by separate AI sessions… not an outside or peer review"), and its access labels match this review and the refutation pass. "Four research sessions" matches the four note files but is not otherwise recorded. AI Weekly and Optimixed summaries (not fetched, per notes) are not listed, which is acceptable because the report does not rely on them.

## Coordinator note (2026-11-14)
- Antin essay: the causal-claims research session reported in its hand-back that Judd Antin's original essay could not be fetched (blocked); this was not written into causal_claims_context.md. Recorded here so the report's blocked list has a record in the tree.
- Applied minor items 3 and 6 and the S9 leftover: "US job-board data"; "more complete earlier one"; "LDT reportedly re-checks its sources". Also shortened the 35-word Lenny quote in the first section to a paraphrase plus a short verbatim phrase (quote length limit). Minor item 5 (hiring window applied to UXR by inference) left as is.
