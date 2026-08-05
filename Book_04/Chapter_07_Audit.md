# Prediction Machines — Chapter 7: The New Division of Labor
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Audit
**Source:** Book pages 67–82 (PDF pages 80–95)
**Date:** 2026-08-03

## Missing Items

1. **Scale and clarity of the bail-decision problem** (book p.70): The chapter states there are "10 million such decisions each year" in the US, that bail decisions are "very consequential for family, job, and other personal issues, not to mention the cost of prison for the government," and — importantly — that "the decision criteria are clear and well defined" (judges must judge flight/reoffense risk, not eventual guilt). This last point matters: the chapter isn't describing an ambiguous task where poor human performance is unsurprising; it's a well-defined task at massive scale (10 million/year) where humans still underperform badly. The extraction's Section 5/7 entries capture the outcome data but omit the annual volume figure, the government cost dimension, and the explicit "clear and well defined" framing.
2. **The Smith (physical) vs. Babbage (cognitive) division-of-labor distinction** (book p.78): The chapter is precise on this point: "This is a classic division of labor, but not physically as Adam Smith described. Rather, it is a cognitive division of labor that economist and computer pioneer Charles Babbage initially described in the nineteenth century." The extraction's Section 2 (Concept 1) blends these into "in the spirit of Adam Smith and Charles Babbage" without preserving the chapter's explicit distinction — that Smith's classic division of labor was physical/manual, while Babbage is credited as the more directly relevant precedent because his version was specifically cognitive/mental. This is a meaningful nuance: the chapter opens with Smith as a familiar hook but closes by correcting/refining that reference toward the less-famous but more precisely applicable Babbage.
3. **"Prediction with confidence, unaware they are doing a poor job"** (book p.71): Between the expert-bias discussion and the hiring study, the chapter states: "Economists have found that managers and workers often engage in prediction—and prediction with confidence—unaware they are doing a poor job." This is a distinct, general claim (professionals confidently making bad predictions without realizing it) that bridges the chapter's expert-bias examples to the hiring study, and thematically previews the "unknown knowns" danger (confident wrongness) discussed later. It was not captured as its own claim in the extraction.

## Corrections Needed

None identified — spot-checked figures (52%/60% X-O experiment, 84%/50% physician framing, 750,000 bail cases, 62%/63%/5% bail figures, 15% tenure improvement, 92.5%/96.6%/99.5% Camelyon figures) all match the chapter text.

## Overgeneralizations

None identified — the extraction consistently preserves the chapter's hedges (e.g., "reasonably accurate," "the study provides plenty of additional evidence" flagged as not detailed further).

## Important Nuance Lost

- As noted in Missing Item #2, the extraction's blending of Smith and Babbage into a single "spirit of" attribution loses the chapter's actual, more precise point: Smith is the familiar opening reference (physical division of labor), but Babbage is the corrected, more accurate closing attribution (cognitive division of labor) — the chapter is making a small but deliberate correction to the reader's likely assumption that Smith is the relevant precedent.

## Additional Cases and Examples

```
Case Title: The scale and stakes of US bail decisions
People / Organization: US court system generally
Context: Establishes why the bail-decision study (Section 5/7) is not a niche or low-stakes example, before the machine-vs-judge comparison begins.
What Happened: The chapter notes that US judges make roughly 10 million bail-granting decisions each year, that the outcome is highly consequential for defendants' family, job, and other personal circumstances, that it also carries a direct cost to government (imprisonment costs), and that — unlike many prediction problems — the decision criteria judges are supposed to apply are clear and well defined (flight/reoffense risk, not likelihood of eventual conviction).
Outcome: Frames the subsequent finding (judges dramatically underperforming a machine-learning algorithm) as especially striking, since it isn't attributable to task ambiguity or low stakes.
Concept Illustrated: A well-defined, high-volume, high-stakes prediction task as an unusually clean setting for measuring the human-machine performance gap.
Why This Case Is Useful: Strengthens the bail-decision case's rhetorical force — removes the easy objection that judges do badly because the task is inherently vague or low-stakes.
Potential for Reuse: Medium — a supporting framing detail rather than an independent teaching case.
```

## Additional Research Evidence

None identified beyond what's already captured in Section 5 and this audit.

## Potential Disagreements to Track Later

None newly identified beyond what's already flagged in the extraction's Section 11 (bail-algorithm fairness/bias controversy; tension between prediction-by-exception and unknown-knowns).

## Additional Content Opportunities

None beyond what's already captured in the extraction's Section 17 — the missing items above are supporting/grounding details rather than standalone content seeds.

## Recommended Changes to the Original Extraction

1. **Section 7, NYC bail-decision study entry** — add the annual volume (10 million bail decisions/year in the US), the government cost dimension, and the "decision criteria are clear and well defined" framing.
2. **Section 2 (Concept 1, Division of labor)** — correct the Smith/Babbage attribution: Smith's classic division of labor was physical; the chapter explicitly credits Babbage's 19th-century concept of *cognitive* division of labor as the more precise precedent for human-machine prediction collaboration.
3. **Section 3 (Key Claims)** — add the claim that managers and workers often engage in prediction "with confidence," unaware they're doing a poor job, bridging the expert-bias discussion to the hiring study and previewing the "unknown knowns" theme.

All other sections are accurate as extracted; no further changes needed.
