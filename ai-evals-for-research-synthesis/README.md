# Evals for AI-assisted research synthesis: a one-pager

> **AI-drafted note.** Claude (Anthropic's AI) drafted this from a working conversation with Owen Hughes, who set the question and decided what to publish. It is a practical framework, not a study: the thresholds and time estimates below are working rules of thumb, not tested figures.

**The problem.** Many researchers no longer hand-code transcripts; AI does the tagging and synthesis. That removes the step where a human checked the interpretation against the data. Teams already say that trust in AI outputs is their main blocker. Evals put a check back in that is cheap enough to run on every study.

**The question every eval answers:** *can each finding be traced back to the data, at the strength it claims?*

## Example

12 interviews with affluent savers about how they decide where to move cash when rates change. The AI pipeline produces 6 findings, each with supporting quotes.

## 1. Build a failure taxonomy (once, about 2 hours)

Take one or two past studies you know well, read the AI output against the transcripts and log every way it went wrong. Typical categories:

| Failure | What it looks like |
|---|---|
| Fabricated or altered quote | A near-paraphrase presented as verbatim |
| Overstated prevalence | "Most participants…" when 3 of 12 said it |
| Misattribution | P4's view credited to P7, or the moderator's words treated as a participant's |
| Lost nuance | "Distrusts notifications" when they meant notifications *about rate changes* |
| Flattened dissent | A strong minority view dropped because it didn't fit a theme |
| Hypothesis pull | Findings drift towards the hypotheses the AI was given |

**Consensus is not an eval.** Several AI agents agreeing on a finding does not make it correct. If they share the same prompt, the same hypotheses and the same model, they can share the same blind spots.

## 2. Turn each failure into a check

| Check | Method | Catches |
|---|---|---|
| Quote existence | **Script:** each quote must appear verbatim in the named participant's transcript | Fabricated quotes, misattribution |
| Claim support | **LLM judge:** does this evidence support this claim? Pass/Fail plus reason | Lost nuance, unsupported claims |
| Prevalence | **LLM judge** lists supporting participants; **script** compares the count with the wording ("most", "several", "a few") | Overstated prevalence |
| Counter-evidence | **LLM judge** searches all transcripts for evidence that contradicts or complicates each finding | Flattened dissent |
| Hypothesis blind test | **LLM judge** sees findings and transcripts *without* the hypotheses: would it reach the same findings? | Hypothesis pull |

Use deterministic code wherever you can. A script that string-matches quotes can't hallucinate, so it is the cheapest, highest-trust check you have.

## 3. Calibrate the judge against a human (the step people skip)

An LLM judge is only useful if it agrees with you. For each study, or each quarter, mark about 20 claims Pass/Fail yourself, without looking at what the judge said, then compare. If you agree on roughly 85–90% of them, trust it for routine runs. If you don't, rewrite the judge prompt using the claims you disagreed on. This takes 30–40 minutes, not a return to full coding.

## 4. Ship a scorecard with every study

> 6 findings · 41 quotes · 41/41 verbatim ✓ · 5/6 claims supported · 1 prevalence overstated (F3: "most" → 4/12) · 2 counter-evidence flags reviewed

The scorecard turns "the AI seems fine" into evidence a stakeholder can check, and it records the limits of each finding next to the finding.

## Beyond synthesis

The same method applies to AI features in a product. Read about 100 real conversations, code the failures (implied financial advice, misstated rates or protection limits, the wrong tone for the audience), and turn each one into a check. The researcher's error analysis becomes the quality specification that product, risk and compliance sign off on. That makes it strategy-layer work, not just QA.

## Limits

- An LLM judge can share the blind spots of the model that did the synthesis. If you can, use a different model or a differently framed prompt for judging.
- Evals check that findings are faithful to the data. They don't check that the study asked the right questions or recruited the right people.
- A small calibration sample tells you roughly how far to trust the judge, not exactly.

*Last updated 17 November 2026.*
