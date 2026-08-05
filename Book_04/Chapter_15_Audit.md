# Prediction Machines — Chapter 15: Decomposing Decisions
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Audit
**Source:** Book pages 157–164 (PDF pages 170–177)
**Date:** 2026-08-04

## Missing Items

1. **The precise operationalization of "ROI" in Key Points bullet 1 (book p.164)**: The chapter's Key Points state: "Tasks need to be decomposed in order to see where prediction machines can be inserted. This allows you to estimate the benefit of the enhanced prediction and the cost of generating that prediction. Once you have generated reasonable estimates, rank-order the AIs from highest to lowest ROI..." The extraction's Section 4 (AI Canvas) and Section 19 summary reference "ROI" generically without capturing that the chapter specifically defines it here as benefit-of-enhanced-prediction minus cost-of-generating-that-prediction — a more precise operationalization than the extraction conveys, and one that directly echoes Chapter 14's ROI-ranking methodology (worth cross-referencing explicitly).
2. **"Identifying the core prediction... can require AI insight" as its own explicit point (book p.164, Key Points bullet 3)**: "At the center of the AI canvas is prediction. You need to identify the core prediction at the heart of the task, and this can require AI insight." The extraction linked "AI Insight" as a related concept in Section 2's third concept card, but did not capture this as a distinct claim in its own right — that pinpointing exactly what a task's core prediction *is* (not just specifying it precisely once found) can itself require the AI Insight skill introduced in Ch.2, directly tying the canvas's central box back to that earlier framework.
3. **More precise phrasing in the Atomwise element-by-element walkthrough (book p.160)**: The extraction's Atomwise case (Section 7) and canvas summary render Action generically as "conduct the test." The chapter's own walkthrough is more specific: "ACTION: What are you trying to do? For Atomwise, it is to test molecules to help cure or prevent disease" — i.e., Action is framed by its ultimate purpose (curing/preventing disease), not merely the mechanical step of testing. Similarly, the walkthrough's Feedback answer is more specific than the extraction conveys: "FEEDBACK: ...Atomwise uses test outcomes, regardless of their success, to improve future predictions" — explicitly noting that both successful and failed test outcomes feed back into the model, a nuance ("regardless of their success") the extraction's feedback description omitted.
4. **Specific qualifiers dropped from the "best students" ambiguity list (book p.164, Key Points bullet 3)**: The chapter's actual list is more precise than the extraction's paraphrase: "highest salary offer **upon graduation**? Most likely to assume a CEO role **within five years**? Most diverse? Most likely to donate to the school **after graduation**?" The extraction's Section 2 (Concept 3) and Section 9 render this as "highest starting salary, most likely to become a CEO, most diverse, or most likely to donate later," dropping the specific time-bound qualifiers ("within five years," "upon/after graduation") that make the ambiguity example sharper and more concrete.

## Corrections Needed

1. **Misattribution of "(expensive)" in the Atomwise AI canvas (Figure 15-2, book p.161)**: The extraction's Atomwise case (Section 7) and Section 19 write: "Judgment = balancing binding affinity to the disease protein against potential side effects (expensive to weigh)." The chapter's actual Figure 15-2 attaches "(expensive)" to the **Action** box, not Judgment: Action = "Conduct test **(expensive)**." The expense being flagged is the cost of physically conducting the test (an action-level cost), not a claim that the judgment/trade-off assessment itself is expensive to weigh. This should be corrected: "(expensive)" belongs to the Action element ("conduct the test") in both the case narrative and the CARD/summary sections that repeat this detail.

## Overgeneralizations

None identified.

## Important Nuance Lost

- As detailed in Missing Item #3, the extraction's rendering of Atomwise's Feedback element drops the chapter's explicit "regardless of their success" qualifier — the point that failed tests are just as valuable as successful ones for improving future predictions (a general machine-learning point about the value of negative/failure data) is present in the source but not surfaced in the extraction.
- As detailed in Missing Item #4, collapsing "highest salary offer upon graduation" and "most likely to assume a CEO role within five years" into "highest starting salary" and "most likely to become a CEO" loses the specific time-bound framing that is precisely what makes these examples illustrate genuine prediction-target ambiguity (a prediction target must specify not just an outcome but a time horizon for it).

## Additional Cases and Examples

None identified beyond what's already captured in Section 7.

## Additional Research Evidence

None identified beyond what's already captured in Section 5 and this audit.

## Potential Disagreements to Track Later

None newly identified beyond what's already flagged in the extraction's Section 11.

## Additional Content Opportunities

None identified beyond what's already captured in Section 17 — the missing items above are refinements to existing captured content rather than net-new teachable material.

## Recommended Changes to the Original Extraction

1. **Section 7, Atomwise case + Section 19 summary** — correct "(expensive)" to attach to the Action element ("conduct the test (expensive)"), not the Judgment element.
2. **Section 7, Atomwise case** — sharpen Action to "test molecules to help cure or prevent disease" and Feedback to explicitly note test outcomes are used "regardless of their success."
3. **Section 2 (Concept 3) and Section 9** — restore the specific qualifiers in the "best students" ambiguity example: "highest salary offer upon graduation," "most likely to assume a CEO role within five years," "most likely to donate to the school after graduation."
4. **Section 4 (AI Canvas framework) or Section 3 (Key Claims)** — add the precise ROI operationalization (benefit of enhanced prediction minus cost of generating it) from Key Points bullet 1, cross-referenced to Ch.14's ROI-ranking methodology.
5. **Section 2 or Section 3** — add an explicit claim that identifying a task's core prediction can itself require "AI insight" (Ch.2), not just that AI Insight is a loosely related concept.
6. **Section 18 (Knowledge Cards)** — no new cards strictly required; existing cards B04-C15-02 and B04-C15-03 should be updated to reflect the Action/Judgment expense correction.

All other sections are accurate as extracted; no further changes needed.
