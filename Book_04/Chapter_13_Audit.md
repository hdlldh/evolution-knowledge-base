# Prediction Machines — Chapter 13: What's at Stake?
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Audit
**Source:** Book pages 133–144 (PDF pages 146–157)
**Date:** 2026-08-04

## Missing Items

1. **The "flip side" analysis of the dog-bowl case — true negatives and potential false negatives among items NOT recommended** (book p.136): The chapter doesn't stop at analyzing the one bad recommendation as a false positive. It explicitly turns the classification framework around: "there is a flip-side to this evaluation: What about things it did not recommend? Amazon has hundreds of dog bowls available, and it did not recommend most (in terms of being high up in the search results). If these were 'true negatives,' then had they been recommended and bought, they would have resulted in low satisfaction. But what if there was a 'false negative,' a bowl that would have delighted this customer? Then Amazon would have got a favorable review." This completes the full 2×2 confusion-matrix framing (true positive/false positive/true negative/false negative) applied to a single concrete case — a more rigorous and complete treatment than the extraction captured, which focused only on the false positive (the bad recommendation actually made) without addressing the parallel, harder-to-see question of false negatives (better bowls that existed but were never surfaced).
2. **The precise "expected payoff shortfall of 10" calculation for Amazon** (book p.139): The chapter gives Amazon's side of the math as precisely as Facebook's: "In those cases, Amazon's payoff falls by half to 100 (rather than 200). Thus, in adopting the AI, there is always an expected payoff shortfall of 10 (= 0.1*100)." This creates a deliberate numerical echo with Facebook's "–10 on average" figure — both companies face a magnitude-10 expected cost from AI's imperfection, but Amazon's is a shortfall against a strongly positive baseline (worth bearing) while Facebook's is an outright negative payoff (not worth bearing). The extraction's Section 3/4 captured the general shape of the Amazon/Facebook contrast but not this precise, deliberately-parallel "10 vs. –10" framing, which is a sharper and more quotable version of the chapter's core point.

## Corrections Needed

None identified — spot-checked figures (Facebook's 96%/86%/38%, 15,000 moderators/~60,000 employees, Spotify's 2014 Discover Weekly launch, ~700-song editorial pool) all match the chapter text.

## Overgeneralizations

None identified.

## Important Nuance Lost

- As detailed in Missing Item #1, the extraction's treatment of the dog-bowl case is somewhat one-sided (false positives only), missing the chapter's own explicit acknowledgment that the *harder*, less visible risk in a recommendation system is false negatives — good matches that simply never get surfaced and therefore generate no complaint, no review, and no visible signal that anything went wrong at all. This is a meaningfully different (and arguably more important) risk category than the vivid, complained-about false positive the extraction emphasizes.

## Additional Cases and Examples

```
Case Title: The dog-bowl case's hidden false-negative question
People / Organization: Amazon; the same unnamed customer/reviewer already covered in the dog-bowl case
Context: A direct continuation of the dog-bowl case (Section 7 in the extraction), applying the full classification framework rather than stopping at the one visible complaint.
What Happened: The chapter notes Amazon had hundreds of dog bowls available and didn't surface most of them prominently. For the bowls it correctly chose not to recommend (true negatives), no harm was done. But the chapter raises the harder question: what if one of the un-recommended bowls would actually have been a better match (a false negative) — the customer would simply never have found out, Amazon would have lost a chance at a favorable review, and no one would ever have flagged the miss the way the one-star review flagged the false positive.
Outcome: Establishes that false negatives are structurally invisible in a way false positives aren't — a customer complains loudly about a bad recommendation actively made, but no one complains about a good recommendation that was silently never made.
Concept Illustrated: The asymmetric visibility of the two error types — false positives generate direct, attributable feedback (reviews, complaints), while false negatives generate no signal at all, making them systematically easier for a company to underweight or overlook entirely.
Why This Case Is Useful: A subtle but important extension of the already-strong dog-bowl case, useful for teaching that "we haven't gotten complaints" is not the same as "we aren't making costly false-negative errors."
Potential for Reuse: High — a valuable, underused framing for evaluating any recommendation/classification system's blind spots.
```

## Additional Research Evidence

None identified beyond what's already captured in Section 5 and this audit.

## Potential Disagreements to Track Later

None newly identified beyond what's already flagged in the extraction's Section 11.

## Additional Content Opportunities

```
Idea Title: "The Recommendation Algorithm's Invisible Mistake"
Format: YouTube Short | Visual Explainer
Application Domain: AI | Business | Everyday Life
Hidden Principle: Signal vs. Noise
Story Hook (Layer 1): One bad Amazon recommendation got a furious one-star review. But what about the perfect product Amazon never even showed you?
Principle Framework (Layer 2): False positives complain loudly; false negatives never complain at all — which means any system evaluated only by complaint volume will systematically underrate its most costly, silent category of error.
Best Supporting Case: The dog-bowl case's flip-side false-negative question (see Additional Cases above).
Character Application: Insight: Interpreter
Psychology Angle: Availability bias — visible complaints feel like the whole picture when they're actually only half of it.
Math Angle: Direct — completing the 2×2 confusion matrix (true/false positive/negative).
Sports Angle: None identified.
Business Angle: Direct — a caution against using complaint volume alone as an AI-quality metric.
Investing Angle: None identified.
History Angle: None identified.
AI Angle: Direct — recommendation-system evaluation methodology.
```

## Recommended Changes to the Original Extraction

1. **Section 7, Amazon dog-bowl case entry** — add the "flip side" true-negative/false-negative analysis, completing the full classification framework rather than stopping at the false positive.
2. **Section 3/4, Amazon/Facebook payoff comparison** — add the precise "expected payoff shortfall of 10 (= 0.1×100)" calculation for Amazon, making explicit the deliberate numerical parallel with Facebook's "–10 average" figure.
3. **Section 18 (Knowledge Cards)** — add a card for the false-negative visibility asymmetry (CARD ID B04-C13-09).
4. **Section 17 (Content Creation Opportunities)** — add "The Recommendation Algorithm's Invisible Mistake" (see Additional Content Opportunities above).

All other sections are accurate as extracted; no further changes needed.
