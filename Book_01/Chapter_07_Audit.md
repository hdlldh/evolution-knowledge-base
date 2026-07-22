# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 7: Overfitting — When to Think Less
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 195–219, re-read against Chapter_07_Extraction.md
**Date:** 2026-07-21

---

## Missing Items

**1. The two epigraphs, and their sly relevance.** (PDF pp. 195, 209) The chapter opens "The Case
Against Complexity" with the *Annie Get Your Gun* line "Anything you can do I can do better; I can do
anything better than you" — a wink at the "more/better" premise the chapter demolishes — and the
"How to Combat Overfitting" section with the anonymous "If you can't explain it simply, you don't
understand it well enough." The extraction captured the second in §12 but dropped the *Annie Get Your
Gun* epigraph entirely. The Revusky & Bedarf epigraph on "The Weight of History" — "Every food a living
rat has eaten has, necessarily, not killed it" — is a genuinely sharp survivorship/robustness framing
that the extraction also omitted; it is arguably the most on-theme of the three.

**2. Franklin's algorithm has an actual cancellation mechanic worth preserving.** (PDF pp. 195–196)
The extraction summarizes Franklin's method but the *specific striking-out rule* — "if I find a Reason
pro equal to some two Reasons con, I strike out the three… a two con equal to three pro, strike out
the five" — is the part that makes it "algebra," and it prefigures the Lasso's zeroing-out of terms.
Worth keeping the mechanic, not just the gist.

**3. The one-factor model's specific failure: "infinite misery."** The extraction has this, but the
paired contrast is sharper in the original: the *one-factor* straight line predicts the post-honeymoon
decline "will continue forever, ultimately resulting in infinite misery," while the *nine-factor* model
predicts a jagged roller coaster. The two failure modes (underfit = infinite straight-line
extrapolation; overfit = wild oscillation) are a cleaner pedagogical pair than the extraction's
emphasis on the nine-factor alone.

**4. The psychologists'/economists' explanation of the leveling-off.** (PDF p. 201) A nuance the
extraction mentions once but under-weights: the two-factor "leveling off" is corroborated *and*
explained — it "reflects a return to normalcy, to people's baseline level of satisfaction… rather than
any displeasure with marriage itself." That parenthetical is what makes the two-factor model the
*right* answer rather than just a smoother curve, and it's a reusable finding about marriage and
happiness.

**5. Gilbert's tattoo line is a distinct, quotable idea.** (PDF p. 203) "Our future selves often pay
good money to remove the tattoos that we paid good money to get" (Daniel Gilbert) is a self-contained
affective-forecasting gem. The extraction folds it into §3/§13 but it deserves a §12 quotable slot in
its own right.

**6. The "diminishing returns" distinction is explicit and important.** (PDF p. 203) The chapter is
careful that overfitting is *not* merely diminishing returns — "the issue is not just that the extra
factors might offer diminishing returns… Rather, they might make our predictions dramatically worse."
The extraction states this (§3) but it's worth flagging as the chapter's precise, counterintuitive
claim: extra complexity is not neutral-to-mildly-costly, it can be actively harmful.

**7. Neural networks are named as a direct AI hook.** (PDF pp. 210–211) The chapter explicitly says
artificial neural networks "can learn arbitrarily complex functions — even more flexible than our
nine-factor model — but precisely because of this very flexibility they are notoriously vulnerable to
overfitting," and that biological neural nets sidestep this by trading performance against maintenance
cost (minimizing neurons firing). The extraction captures the "minimize neurons firing" point but the
explicit ANN-overfitting statement is a direct (not inferred) AI connection that belongs in §16's
"direct from the book" list, which it is — but the vulnerability framing should be foregrounded.

**8. Darwin's balloon and Wales detail.** (PDF pp. 217–218) A small but delightful concreteness the
extraction dropped: his "When? Soon or Late" list weighed "everything from happiness to expenses to
'awkwardness' to his long-standing desire to travel in a hot air balloon and/or to Wales." The balloon
detail is exactly the kind of vivid, reusable specific the template prizes.

## Corrections Needed

**1. The Lasso penalty definition — keep the footnote's precision.**
- Extraction (card 8, §4): "sum of absolute values of coefficients." Correct, and the footnote (PDF
  p. 219) is the source ("the sum of the absolute values of the variables' coefficients"). Good — but
  the extraction should mark that this is the L1 norm specifically, since §14 correctly calls it "L1
  penalty" while card 8 just says "sum of absolute coefficients" without linking the two. Minor
  cross-reference tightening.

**2. Fencing etymology attribution.**
- Extraction (§7): "'defencing.'" The chapter says the original goal was self-defense in a duel,
  "hence the name: 'defencing.'" This is presented as the (folk) etymology in the book; the extraction
  reproduces it faithfully, but should not imply it's an established linguistic fact — the chapter
  itself offers it lightly. Keep it attributed to the book's framing.

**3. "As brainy as we have needed to be."**
- Extraction (card 9, §3): paraphrases correctly, but the chapter's actual inference is two-directional
  and worth preserving exactly: the brain's contributions "must somehow more than pay for that sizable
  fuel bill," *and* a substantially more complex brain "probably didn't provide sufficient dividends" —
  so we're "as brainy as we have needed to be, but not extravagantly more so." The extraction has the
  conclusion but flattens the two-sided cost-benefit reasoning.

## Overgeneralizations

**1. "Think less" risks being read as a universal prescription.** The chapter is explicit and
symmetric: "If you have all the facts, they're free of all error and uncertainty, and you can directly
assess whatever is important to you, then *don't stop early. Think long and hard*." The extraction
carries this in §3 and §11, but the framing throughout (title, §1, content ideas) tilts strongly toward
"think less," and the conditional — think less *only when* uncertainty is high and the proxy gap wide —
should ride with every strong statement, or the chapter's actual balanced rule gets lost.

**2. The training-scar and taste/fitness claims are illustrative, not evidenced.** The extraction
mostly flags this (§3, §5, §11), but the confident phrasing in the cases (card 6, card 4) could read as
established fact. The chapter's own hedging ("there are stories," "officers were shocked to discover")
should survive — these are vivid anecdotes and evolutionary-mismatch arguments, not studies.

**3. Markowitz's 50/50 is a single self-report, and the chapter says 50/50 isn't the sweet spot.** The
extraction does note both, but the "less is more" framing in §9 and the content ideas is punchy enough
that the caveat ("not necessarily the complexity sweet spot"; use the optimal scheme when you *can*
estimate well) should stay firmly attached — the point is *regularize when estimates are untrustworthy*,
not *simpler is always better*.

## Important Nuance Lost

**1. The precondition for using the complex model is stated crisply and should be preserved.** (PDF
p. 203) "If we had copious data, drawn from a perfectly representative sample, completely mistake-free,
and representing exactly what we're trying to evaluate, then using the most complex model available
would indeed be the best approach." This is the chapter's exact statement of *when complexity is
right*, and it's the mirror image of the whole argument — the extraction gestures at it but the
four-part precondition (copious, representative, mistake-free, valid-measure) is a reusable checklist.

**2. Cross-validation "paradoxically may involve using less data."** (PDF p. 208) The chapter
highlights the counterintuitive twist that detecting overfitting means *withholding* data you have —
fitting to eight of ten points on purpose. The extraction has the held-back mechanic but not the framed
paradox ("this may involve using less data"), which is the memorable hook.

**3. The two distinct early-stopping mechanisms.** (PDF p. 214) The chapter names two: (a) algorithms
that add the most-important factor first and stop before adding more, and (b) algorithms that add one
data point at a time and stop before processing all of them. The extraction lists both but blurs them;
they're genuinely different (feature-wise vs. data-wise incremental complexity) and both map to real ML
practice.

**4. "Regularizing to the page" is explicitly likened to *both* Early Stopping and the Lasso.** (PDF
p. 218) The chapter says Darwin's page limit "is reminiscent of both Early Stopping and the Lasso." The
extraction files it under early stopping; the dual mapping (a hard cap on total content = Lasso-like;
a stop-when-you-run-out = early-stopping-like) is the richer reading.

## Additional Cases and Examples

```
Case Title: "Every food a living rat has eaten has not killed it"
People / Organization: Samuel Revusky and Erwin Bedarf (epigraph)
Context: The epigraph to "The Weight of History."
What Happened: The line — a rat's dietary history is, by survivorship, a record of non-lethal foods —
frames why history/constraint carries information: what has persisted has, necessarily, survived.
Outcome: A compact statement of survivorship and the informational value of the past.
Concept Illustrated: The weight of history; constraint as robustness; survivorship.
Why This Case Is Useful: A quotable, slightly eerie framing of "the past is a filter," perfect for the
tradition-as-regularization argument.
Potential for Reuse: High
```

```
Case Title: Franklin's cancellation algebra
People / Organization: Benjamin Franklin
Context: The precise mechanic of his "Moral or Prudential Algebra."
What Happened: Beyond listing pros and cons, Franklin *cancels* them: strike a pro against an equal
con; strike one pro against two cons it equals; strike two cons against three pros; proceed until the
balance is clear. "I have found great Advantage from this kind of Equation."
Outcome: A genuine algorithm — and an unwitting precursor to the Lasso's driving of terms to zero.
Concept Illustrated: Decision-as-computation; term cancellation prefiguring regularization.
Why This Case Is Useful: Shows the "more factors" premise as a real procedure, and the cancellation
mechanic is a neat bridge to the Lasso.
Potential for Reuse: Medium
```

## Additional Research Evidence

None materially missing. The re-read confirms the evidentiary base — the (unnamed) German marriage
survey, Ridgway (1950s), Tikhonov (1960s), the Lasso (Tibshirani, 1996), Markowitz's self-report,
Gigerenzer & Brighton, and Grossman's anecdotes — is fully captured. One sharpening: the chapter's
four-part precondition for when the complex model *is* best (copious, representative, mistake-free,
valid measure) should be recorded as the positive counterpart to the overfitting warning.

## Potential Disagreements to Track Later

1. **Goodhart's law / the metrics-critique literature (Muller, *The Tyranny of Metrics*).** The
   idolatry-of-data section is Goodhart by another name; a direct cross-book collision, and a recurring
   theme across chs. 3, 5, 6, 7. Muller would agree; a pro-measurement management text would push back.
2. **Deep learning and double descent.** The chapter's "more capacity → more overfitting" is the
   classical view; modern overparameterized models (double descent, grokking) complicate it and would
   read as a partial counterexample to the nine-factor story.
3. **Gladwell / the "10,000 hours" and deliberate-practice tradition.** "Training scars" and "more prep
   = worse class" sit in tension with the practice-makes-perfect canon; a sharp cross-book pairing on
   when repetition helps vs. harms.
4. **Kahneman & Tversky vs. Gigerenzer (again).** "Less is more" and heuristics-as-rational is
   Gigerenzer's side of the long-running debate with the heuristics-and-biases tradition — the same
   fault line flagged in chs. 2 and 6.
5. **Chesterton's fence / Burkean conservatism.** "Tradition as robustness / don't overfit the present"
   overlaps with Chesterton's fence and Burke; also invites the counter that it can rationalize harmful
   inertia (already noted in §11).

## Additional Content Opportunities

```
Idea: The past is a filter — why old things that survive are worth trusting
Format: YouTube Short
Core Concept: Survivorship and the weight of history.
Hook: "Every food a rat has eaten hasn't killed it." That one sentence explains why tradition beats the
latest fad more often than you'd think.
Best Supporting Case: The Revusky & Bedarf epigraph; food fads (kale, coconut water); decussation.
Psychology Angle: Survivorship bias — and its rational flip side.
Math Angle: The past as a filter / prior; damped updating.
Sports Angle: Time-tested tactics vs. fad formations.
AI Angle: Inductive bias; why constraints improve generalization.
```

```
Idea: Ben Franklin invented an algorithm — and it was wrong
Format: YouTube Short
Core Concept: The pro/con list as overfitting.
Hook: Ben Franklin's famous decision-making method — list every pro and con, weigh them all — is exactly
the thing machine learning warns you not to do.
Best Supporting Case: Franklin's cancellation algebra; the nine-factor marriage model; Darwin
regularizing to the page.
Psychology Angle: Overthinking; when more factors hurt.
Math Angle: Overfitting; regularization; the Lasso's zeroing of terms.
Sports Angle: Over-analysis in game planning.
AI Angle: Feature selection and complexity penalties.
```

---

## Recommended Changes to the Original Extraction

1. **§12 (Quotable Ideas)** — add the *Annie Get Your Gun* epigraph, the Revusky & Bedarf "every food a
   rat has eaten" epigraph (the highest-value addition — the sharpest robustness framing), and Gilbert's
   tattoo line as a standalone quotable.

2. **§7 (Cases and Stories)** — add the Revusky & Bedarf survivorship framing and Franklin's
   cancellation algebra (with the Lasso-prefiguring mechanic).

3. **§3 / §9 (underfit vs. overfit pairing)** — sharpen the two failure modes: one-factor → infinite
   straight-line misery (underfit), nine-factor → wild oscillation (overfit); they're a cleaner
   pedagogical pair than the nine-factor alone.

4. **§5 / §3 (the positive precondition)** — record the chapter's four-part condition for when the
   complex model *is* best: copious data, perfectly representative sample, mistake-free, representing
   exactly what you're evaluating. It's the mirror of the whole argument and a reusable checklist.

5. **§4 / §7 (cross-validation paradox)** — foreground "detecting overfitting may paradoxically involve
   using *less* data" (fitting to eight of ten on purpose).

6. **§4 / card 13 (two early-stopping mechanisms)** — distinguish feature-wise (add most-important
   factor first, then stop) from data-wise (add one point at a time, then stop) incremental complexity.

7. **card 16 / §7 (Darwin dual mapping)** — note that "regularizing to the page" is likened to *both*
   Early Stopping *and* the Lasso, and add the balloon/Wales detail.

8. **§1 / §17 (balance the "think less" tilt)** — attach the conditional to strong "think less"
   statements: think long and hard when data are clean, complete, and valid; think less only under high
   uncertainty and a wide proxy gap.

9. **card 9 / §3 (two-sided brain-cost reasoning)** — preserve the bidirectional inference: the brain
   must more than pay its fuel bill, *and* a much bigger brain wouldn't have paid enough — hence "as
   brainy as needed, not extravagantly more."

10. **§16 (neural-net overfitting)** — foreground that the chapter *directly* states ANNs are
    "notoriously vulnerable to overfitting" due to their flexibility, and that biological nets regularize
    via metabolic cost.

**Sections that are fine as they stand:** §1 (thesis), §6 (experiments — the alternative-explanation
fields do real work, especially the "which two points held back matters / k-fold" note), §8 (teaching
examples), §10 (unique ideas), §14 (mathematics — the bias–variance and Goodhart mappings are precise),
§15 (sports — correctly identifies fencing and training scars as the two direct examples and separates
inferred applications).
