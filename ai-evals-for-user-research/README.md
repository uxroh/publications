# AI Evals for User Research — One-Pager

> **AI-written explainer.** Claude (Anthropic's AI) drafted this one-pager with Owen and checked it against the research-integrity rules; it has not been peer reviewed. See [About this report](about-this-report.md) for how it was made and what it does not claim.

*15 November 2026 · Owen Hughes*

## What AI evals are

An eval is a repeatable test that checks whether an AI system's output is good enough for a specific job. It is usability testing for a model or prompt: define the task, define what "good" looks like, run it against real cases, and score the result.

Every eval has four parts:

1. **A test set** — real inputs, such as interview transcripts, survey verbatims or support tickets.
2. **A reference or rubric** — what a good answer looks like, ideally agreed by a human expert.
3. **A grader** — a human, a code check (e.g. "cites a participant ID"), or another model acting as judge ("LLM-as-judge").
4. **A score you track over time** — so you can see if a prompt, model or workflow change made things better or worse.

For a researcher, the key shift is moving from "this AI summary looks fine" to "this AI summary matched human coding on 87% of themes across 20 transcripts" (an illustrative figure, not a real result).

## Pros

- **Trust you can defend.** You can show stakeholders evidence that AI-assisted synthesis is reliable, rather than asking them to take it on faith.
- **Catches silent failures.** Hallucinated quotes, dropped minority views and over-confident themes show up as scores, not surprises in a readout.
- **Safe iteration.** Change a prompt or switch models and re-run the same test set to see whether quality went up or down.
- **Scales your judgement.** Your expert rubric becomes reusable, so squads using AI tools inherit your quality bar.
- **Plays to research skills.** Defining criteria, coding data and checking inter-rater agreement are things researchers already do well.
- **Governance-friendly.** A documented eval record shows how AI outputs were checked. Confirm with compliance what evidence they would actually want.

## Cons and risks

- **Upfront effort.** Building a good test set and rubric likely takes several days (an estimate), and needs refreshing as your questions change.
- **"Good" is subjective.** Qualitative synthesis rarely has one right answer, so evals measure agreement with a reference, not truth.
- **Judge models have biases.** A 2023 study found LLM judges show position bias (favouring the first answer shown) and verbosity bias (favouring longer answers). It could not confirm whether models favour their own answers (Zheng et al., see Sources).
- **Metric gaming.** Teams can optimise for the score and lose sight of insight quality (Goodhart's law).
- **Small samples.** Research datasets are small, so a score shift of a few points may be noise.
- **Data handling.** Transcripts from affluent and HNW clients are sensitive; test sets need anonymising and must stay within approved tools.

## Evals vs hardening skills

A hardening skill changes how the AI does the work; an eval measures whether the work came out right. One prevents errors, the other detects them, and a skill cannot show on its own that it is working.

| | Hardening skill | AI eval |
| --- | --- | --- |
| What it is | Instructions the AI follows: rules, checklists, required formats | A repeatable test applied to the output |
| When it acts | During the work | After the work |
| What it does | Shapes behaviour, e.g. "cite a quote for every claim" | Scores results, e.g. "92% of claims supported, 2 overstated" (illustrative) |
| Research analogy | A research protocol or discussion guide | Inter-rater reliability or an analysis audit |
| Failure mode | The AI can follow the rules on the surface and still be wrong | It only measures what the test set and rubric cover |

For example, a research-integrity skill can make the AI label every claim and admit what it didn't read, but it cannot show that errors went down. Use them as a loop:

1. Run the eval to get a baseline score.
2. Add or adjust the skill, e.g. require verbatim quotes and proportional wording ("3 of 8", not "many").
3. Re-run the same eval. Keep the skill if the score improves; change or drop it if not.
4. Keep the eval running to catch a model update quietly weakening the skill.

## How to apply it in research practice and analysis

There are two angles: evaluating the AI *you* use for research, and helping squads evaluate the AI features they *ship*.

| Use case | What you test | Grader | Example pass criteria |
| --- | --- | --- | --- |
| Interview synthesis | AI-generated themes vs your manual coding | Human + LLM-as-judge | Covers ≥ 80% of human-coded themes; no invented themes |
| Quote extraction | Quotes pulled to support each insight | Code check | Every quote appears verbatim in the source transcript |
| Survey verbatim coding | AI tagging of open-text responses | Human sample | Agreement with a human coder (e.g. Cohen's kappa above 0.6) |
| JTBD / persona drafts | Job statements from interview data | Rubric scored by you | Each job is evidenced by ≥ 2 participants |
| SUS / SUPR-Q analysis | AI-written interpretation of scores | Code + human | Numbers match the source; benchmarks stated correctly |
| Shipped AI features (e.g. a savings assistant) | Answers to real client questions | Rubric from user research | Accurate, compliant, matches tone HNW clients expect |

Pass criteria are starting points to agree as a team, not industry standards. The one with a source is kappa: McHugh (2012) treats any kappa below 0.60 as inadequate agreement between raters ([source](https://biochemia-medica.com/en/journal/22/3/10.11613/BM.2012.031/fullArticle)).

The last row is where research has the most strategic leverage. Your JTBD and usability work defines what "good" means for clients, which becomes the rubric product and engineering test against. That moves research from executing studies to setting the quality bar for AI products.

It also fits your TRACE work: evals give any AI-assisted research loop a measurable feedback step.

## Evals without manual coding

You don't need to code every transcript; you need a small human reference to check the AI against. Without any, the AI is only measured against itself and drift goes unnoticed.

| Method | What you do | What it catches | Time per study (estimate) |
| --- | --- | --- | --- |
| Quote check | Require verbatim quotes + participant IDs for every claim; Ctrl+F a sample in the transcripts | Invented or misattributed quotes | ~15 min |
| Run it twice | Re-run the synthesis in a fresh chat or a different model; compare themes | Themes that don't repeat are shaky | ~15 min |
| Planted check | Add a known item before analysis (e.g. a dummy transcript with a distinctive view) | Whether the AI surfaces what is really there | ~20 min |
| Spot audit | Pick 3–5 claims at random; read only the cited passages + skim 1–2 transcripts | Overstatement and missed negative cases | ~30–45 min |
| Calibration set | Hand-code 3–5 transcripts once; re-run them when the prompt, model or tool changes | A trackable score over time | A few hours, once |

Recommended default: quote check and spot audit on every study, plus a calibration set re-run only when something in the setup changes. Coding becomes a small reference set, not a daily task.

For checking that interpretation matches the data, grade each claim Supported / Overstated / Unsupported / Contradicted, with a quote required for every grade. Before trusting an AI judge, plant 2–3 known errors in a copy of the analysis and confirm it flags them all. Tally any counts ("7 of 12 said X") in a spreadsheet rather than trusting the AI's count.

## Suggested first step

Run a two-week pilot on one workflow: AI interview synthesis.

1. Pick 10–15 past, anonymised transcripts and hand-code 3–5 of them as your calibration set.
2. Write a 4–5 point rubric: theme coverage, no invented claims, quotes verbatim, minority views kept, insight is actionable.
3. Run your current AI synthesis prompt and score each output against the rubric and your coding.
4. Change one thing (prompt, model or chunking), re-run, and compare scores.
5. Share a one-slide result with product leadership: baseline score, what improved it, and where human review is still required.

If the pilot holds up, turn the test set and rubric into a shared asset for squads using AI in research.

## Sources

- [Zheng et al. (2023), Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/html/2306.05685v4) — §3.3 on judge biases read.
- [McHugh (2012), Interrater reliability: the kappa statistic, Biochemia Medica 22(3)](https://biochemia-medica.com/en/journal/22/3/10.11613/BM.2012.031/fullArticle) — sections on interpreting kappa read; Table 3 is an image and was not read.

Everything else in this page is general explanation or the author's judgement, not sourced. The time estimates and remaining pass criteria are estimates.
