# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 7: Overfitting — When to Think Less
**Author:** Brian Christian and Tom Griffiths
**Type:** Extraction
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 195–219 (book chapter 7, incl. footnote)
**Date:** 2026-07-21
**Revision note:** Revised after Chapter_07_Audit.md; see that file for what changed and why.

```
BOOK:
Algorithms to Live By: The Computer Science of Human Decisions

AUTHOR:
Brian Christian and Tom Griffiths

CHAPTER:
7 — Overfitting: When to Think Less
```

---

## 1. Chapter Thesis

More thinking, more factors, and more effort do not reliably produce better decisions — because every
decision is a prediction, and a model tuned too finely to the data you happen to have will fit that
data perfectly yet generalize terribly. This is "overfitting," and since our data are almost always
noisy proxies for what we actually care about, overfitting is a form of "idolatry of data": ruthlessly
optimizing the measurable wrong thing. The remedies are to detect it (cross-validation against
held-back or different data), to penalize complexity (regularization — the Lasso, Occam's razor, and
nature's own caloric/attentional brakes), and to stop early (don't give a model, or your mind, the
time to grow too complex). The rule is conditional and symmetric, not a blanket "think less":
when data are copious, clean, and a valid measure of what matters, you *should* think long and hard —
the complexity is appropriate. It is only under high uncertainty and a wide measure-vs-matters gap that
you should prefer simplicity and stop thinking sooner — and then, sometimes, going with your first
instinct *is* the rational choice.

## 2. Key Concepts

```
Concept Name: Overfitting
Definition: When a model is so finely tuned to the specific data observed that it captures noise as if
it were signal, fitting the available data perfectly but predicting future/unseen data badly.
Why It Matters: The chapter's central idea; it overturns the intuition that "more factors → better
predictions" and shows extra complexity can make predictions *dramatically worse*, not just yield
diminishing returns.
How the Author Uses It: The organizing frame; the German marriage data (one/two/nine-factor models)
demonstrates it, and every later domain (taste, fitness, business, training) is an instance.
Related Concepts: Idolatry of data, proxy metric, regularization, cross-validation, early stopping.
```

```
Concept Name: Every Decision Is a Prediction
Definition: Any choice is an attempt to formulate a theory that both accounts for past experience and
says something about future experience you're guessing at.
Why It Matters: This double duty creates the unavoidable tension between fitting what you know and
generalizing to what you don't — the root of overfitting.
How the Author Uses It: To frame decisions (marriage, stocks, even writing an email) as modeling
problems subject to the fit-vs-generalize tradeoff.
Related Concepts: Overfitting, proxy metric, model complexity.
```

```
Concept Name: Idolatry of Data / Proxy Metrics
Definition: Optimizing for what you can measure rather than what actually matters — worshipping "the
bronze snake of data" rather than the force behind it.
Why It Matters: Because our data are almost always noisy proxies (taste for health, test scores for
learning, KPIs for value), aggressive fitting optimizes the wrong target.
How the Author Uses It: The unifying diagnosis for taste, fitness, business incentives, and training
scars; the reason overfitting is "everywhere."
Related Concepts: Overfitting, Goodhart-style incentive failure, cross-validation.
```

```
Concept Name: Cross-Validation
Definition: Assessing not just how well a model fits its given data but how well it generalizes to data
it hasn't seen — often by holding back some points, or testing against a different form of evaluation.
Why It Matters: The primary way to *detect* overfitting, which is otherwise insidious because an
overfit model looks like a perfect fit.
How the Author Uses It: Held-back marriage points as "canaries in the coal mine"; random essay/oral
exams to cross-validate standardized tests; unfamiliar "cross-training" to catch training scars.
Related Concepts: Overfitting, teaching to the test, proxy metrics.
```

```
Concept Name: Regularization (Penalizing Complexity)
Definition: Adding a term to the optimization that penalizes complexity, so a more complex model must
be *significantly*, not just slightly, better to be chosen.
Why It Matters: The chief remedy for overfitting; formalizes Occam's razor mathematically (Tikhonov,
1960s).
How the Author Uses It: The bridge from diagnosis to cure; instantiated by the Lasso and by nature's
own constraints.
Related Concepts: Lasso, Occam's razor, early stopping, "less is more."
```

```
Concept Name: The Lasso
Definition: A regularization algorithm (Tibshirani, 1996) whose penalty is the total weight (sum of
absolute values of coefficients) of a model's factors, driving as many factors as possible to zero.
Why It Matters: It turns an overfit nine-factor model into a simpler, more robust one keeping only the
few most impactful factors.
How the Author Uses It: The canonical complexity penalty, and the template for "natural Lassos" —
metabolism, neural firing, language, memory.
Related Concepts: Regularization, complexity penalty, natural Lassos.
```

```
Concept Name: Natural Lassos (Complexity Penalties in Nature)
Definition: Real-world constraints that automatically push toward simplicity — time, memory, energy,
attention.
Why It Matters: Simplicity isn't just a statistical trick; biology and culture enforce it, which is why
heuristics can be adaptive.
How the Author Uses It: Metabolism as a caloric brake (the brain burns ~1/5 of daily calories);
minimizing neurons firing; language penalized by speaking length and listener attention; memory as an
inherent Lasso.
Related Concepts: The Lasso, heuristics, evolutionary constraint.
```

```
Concept Name: Early Stopping
Definition: A regularization technique that limits complexity by cutting the tuning/search process
short before a model grows too complex — because more time means more complexity.
Why It Matters: You can prevent overfitting not only by penalizing final complexity but by controlling
how long a model adapts; it grounds "a reasoned argument against reasoning."
How the Author Uses It: Prediction algorithms that add the most important factor first, then stop;
Darwin "regularizing to the page"; Tom's over-prepared first lecture.
Related Concepts: Regularization, "when to think less," heuristics.
```

```
Concept Name: The Weight of History (Constraint as Anti-Overfitting)
Definition: Being constrained by the past — evolutionary baggage, tradition — makes an organism or a
culture less perfectly fit to the present but more robust to an unknown future.
Why It Matters: Slow change is a feature: fully optimizing to a current niche would make you dangerously
sensitive to any shift.
How the Author Uses It: Decussation (cross-wired nerves), the repurposed reptile jawbones in the human
ear, and tradition as a buffer against fads ("jump toward the bandwagon, but not on it").
Related Concepts: Early stopping, regularization, fads, robustness.
```

```
Concept Name: "Less Is More" / The Upside of Heuristics
Definition: With high uncertainty and untrustworthy estimates, using less information, computation, and
time can improve accuracy — a simple heuristic can be the rational choice.
Why It Matters: Reframes shortcuts not as irrational fallback but as regularization; when the model
leans heavily on quantities you can't estimate well, "it's time to regularize."
How the Author Uses It: Markowitz's 50/50 retirement split (can't overfit it); Gigerenzer & Brighton's
argument that less processing can improve accuracy.
Related Concepts: Regularization, overfitting, judgment vs. measurement.
```

## 3. Key Claims

```
Claim: A better fit for available data does not necessarily mean a better prediction.
Type: Theoretical (proved / demonstrated)
Evidence Provided: The German marriage data — the nine-factor model passes through every point yet
predicts absurd out-of-sample behavior (misery at the altar, a roller coaster, a sheer drop after year
10), while the two-factor model's "leveling off" matches what psychologists and economists actually
find. The two failure modes form a clean pedagogical pair: the *one-factor* straight line underfits,
extrapolating the post-honeymoon decline forever into "infinite misery"; the *nine-factor* model
overfits, oscillating wildly. And the two-factor answer is not just smoother but *right* — experts
explain the leveling-off as "a return to normalcy, to people's baseline level of satisfaction… rather
than any displeasure with marriage itself."
Strength of Support: Strong. A clean, visual demonstration; the two-factor forecast is independently
corroborated and mechanistically explained.
```

```
Claim: More complex models are not just subject to diminishing returns — they can make predictions
dramatically worse.
Type: Theoretical
Evidence Provided: Adding small random noise (simulating a repeat survey) makes the nine-factor model
"gyrate wildly" while the one- and two-factor models stay stable.
Strength of Support: Strong. The instability under resampling is the core mechanism of overfitting.
```

```
Claim: Overfitting is a danger any time there is noise or mismeasurement — which is almost always.
Type: Theoretical / Interpretive
Evidence Provided: Data collection/reporting errors; hard-to-define phenomena (happiness); flexible
models fit "phantoms and mirages in the noise." Our own daily data are noisy proxies too (email
read-through; Gilbert's tattoos we later pay to remove).
Strength of Support: Strong. The ubiquity of proxy metrics makes the claim broadly applicable.
```

```
Claim: Overfitting is "idolatry of data" — optimizing the measurable proxy rather than what matters.
Type: Interpretive
Evidence Provided: The bronze-snake / First-Commandment analogy; the gap between measured data and
desired predictions "virtually everywhere."
Strength of Support: Moderate to Strong as a framing; the religious analogy is illustrative, the
underlying proxy-metric point is rigorous.
```

```
Claim: Taste is an overfittable proxy for nutrition.
Type: Interpretive / Empirical
Evidence Provided: Fat, sugar, and salt were reasonable health signals for hundreds of thousands of
years; the ability to modify foods broke the relationship, so we can now "overfit taste" — human agency
becomes a curse.
Strength of Support: Moderate to Strong. A compelling evolutionary-mismatch account; no specific study
cited here.
```

```
Claim: Visible fitness markers (low body fat, high muscle) are overfittable proxies for health.
Type: Interpretive
Evidence Provided: An extreme diet plus steroids can make you "the picture of good health, but only the
picture."
Strength of Support: Moderate. A plausible illustration rather than an evidenced claim.
```

```
Claim: Incentives and metrics reliably produce perverse effects — the "ruthless and clever optimization
of the wrong thing."
Type: Empirical / Interpretive
Evidence Provided: Steve Jobs ("incentive structures work… create consequences you can't anticipate")
and Sam Altman ("the company will build whatever the CEO decides to measure"); V. F. Ridgway's 1950s
catalog of "Dysfunctional Consequences of Performance Measurements" — job-placement staff rushing
interviews, agents picking easy end-of-month cases, factory supervisors neglecting maintenance;
Kaushik's "Friends don't let friends measure Page Views."
Strength of Support: Strong. Multiple named sources and concrete cases; a canonical Goodhart-style
result.
```

```
Claim: Overfitting one's own training can be lethal — "training scars."
Type: Empirical (anecdotal, attributed)
Evidence Provided: Dave Grossman — officers pocketing spent brass mid-gunfight; dead cops with brass in
hand; the FBI changing training after agents reflexively fired two shots then holstered regardless of
threat; an officer who disarmed an assailant then instinctively handed the gun back.
Strength of Support: Moderate to Strong. Vivid, attributed anecdotes ("there are stories"); not
systematically quantified.
```

```
Claim: Overfitting is detectable via cross-validation.
Type: Theoretical / Prescriptive
Evidence Provided: Hold back points as "canaries" (nail the eight training points but miss the two test
points → overfitting); cross-validate a proxy against a different measure (standardized tests vs. random
essays/orals to catch "teaching to the test"); "cross-training" to catch training scars.
Strength of Support: Strong. A standard, well-motivated machine-learning method with clear real-world
transfers.
```

```
Claim: Penalizing complexity (regularization) combats overfitting; the Lasso is a canonical instance.
Type: Theoretical
Evidence Provided: Occam's razor formalized by Tikhonov (1960s); the Lasso (Tibshirani, 1996) penalizes
the total weight of factors and drives many to zero, keeping only high-impact ones.
Strength of Support: Strong. Named, dated results; the Lasso is a real and widely used algorithm.
```

```
Claim: Nature, brains, and language all implement Lasso-like complexity penalties.
Type: Interpretive / Empirical
Evidence Provided: Metabolism as a caloric brake, with two-sided reasoning: the brain burns ~1/5 of
daily calories, so its contributions "must somehow more than pay for that sizable fuel bill" — *and* a
substantially more complex brain "probably didn't provide sufficient dividends," so we're "as brainy as
we've needed to be, but not extravagantly more." Brains minimizing neurons firing; language penalized
by length and listener attention; memory as an inherent Lasso.
Strength of Support: Moderate to Strong. The metabolism and language points are well-argued; the
"minimize neurons firing" is attributed to neuroscientists' suggestion.
```

```
Claim: A simple heuristic can be the rational choice under uncertainty — "less is more."
Type: Empirical / Interpretive
Evidence Provided: Harry Markowitz (1990 Nobel for mean-variance optimization) split his own retirement
50/50 to minimize regret — and a 50/50 split "can't overfit" because it ignores unreliable estimates.
Applying his optimal scheme requires good statistical estimates; errors in them can increase risk.
Gigerenzer & Brighton: "less information, computation, and time can in fact improve accuracy."
Strength of Support: Strong. The Markowitz case is striking and the argument (don't lean on estimates
you can't trust) is rigorous; the chapter notes 50/50 is "not necessarily the complexity sweet spot."
```

```
Claim: Evolutionary/historical constraint is anti-overfitting — it trades present-fit for future
robustness.
Type: Interpretive
Evidence Provided: Decussation (cross-wired nervous system from an ancestral 180° body twist); the human
ear's malleus/incus/stapes repurposed from reptilian jawbones; both reflect history as much as the
problem being solved. Fully optimizing to a niche would make an organism "extremely sensitive to further
environmental changes."
Strength of Support: Moderate to Strong. The biology is real; the framing of constraint as beneficial
regularization is the authors' interpretation.
```

```
Claim: Tradition buffers culture against fads, as evolutionary constraint buffers organisms.
Type: Interpretive
Evidence Provided: The rapid rise/fall of food fads — soy milk quadrupled then eclipsed by almond milk;
coconut water (Vita Coco up ~300× since 2004); kale up 40% in 2013 (Pizza Hut's prior top use: salad-bar
decoration). Culture changes fast; evolution slow. "Jump toward the bandwagon… but not necessarily on
it."
Strength of Support: Moderate. The fad data are vivid; the prescription (a bias toward history) is an
inference.
```

```
Claim: Early Stopping prevents overfitting because more time means more complexity.
Type: Theoretical / Prescriptive
Evidence Provided: Algorithms that add the most important factor first, then stop; adding one data point
at a time and stopping short; Tom's teaching (10+ hours/lecture the first semester produced a worse
class than the under-prepared second, because extra detail confused students — he was overfitting his
own taste as a proxy for theirs).
Strength of Support: Strong for the algorithmic claim; the teaching anecdote is illustrative.
```

```
Claim: How early to stop depends on the gap between what you can measure and what matters.
Type: Prescriptive
Evidence Provided: If you have all the facts, error-free, and can assess what's important — don't stop
early. Otherwise, with high uncertainty and limited data, stop early; prefer simplicity; use a broad
brush (Fried & Hansson's thick Sharpie); Mintzberg — "we can't measure what matters… we'd have to use
something very scary: judgment."
Strength of Support: Strong as a decision rule; it correctly makes the prescription conditional on
uncertainty.
```

```
Claim: Darwin "regularized to the page" — he decided exactly when his notes reached the bottom of the
diary sheet.
Type: Interpretive (from a primary source)
Evidence Provided: The facsimile of Darwin's July 1838 diary; the first points he listed (children,
companionship) were what swayed him; "anything that doesn't make the page doesn't make the decision."
His follow-up "When? Soon or Late" list ended in "Never mind, trust to chance," and he proposed within
months.
Strength of Support: Moderate to Strong. A charming, evidenced reading; the "regularizing to the page"
interpretation is the authors'.
```

## 4. Frameworks, Models, and Mental Models

```
Name: Model Complexity and the Fit–Generalize Tradeoff
Description: Choosing how many factors a predictive model should use.
Components: Data points; candidate models of increasing complexity (one-, two-, …, nine-factor);
in-sample fit vs. out-of-sample prediction.
How It Works: More factors always improve in-sample fit but past a point degrade out-of-sample
prediction, because the model starts fitting noise. Too simple misses the real pattern; too complex
becomes unstable under resampling.
When It Is Useful: Any prediction from noisy data — which is almost all real prediction.
Limitations: The "right" complexity depends on data quality and the measure-vs-matters gap; there is no
universal number of factors.
```

```
Name: Cross-Validation
Description: Test a model on data it wasn't fit to.
Components: A training set; a held-back test set (or a different evaluation method entirely).
How It Works: Fit on the training data, then check generalization on the held-back points; a big gap
signals overfitting. Paradoxically, detecting overfitting "may involve using *less* data" — you fit to
eight of ten points on purpose to test on the other two. Alternatively, cross-validate a proxy metric
against an independent measure.
When It Is Useful: Detecting overfitting; auditing proxy metrics (test scores, KPIs, training drills).
Limitations: Requires holding back scarce data or maintaining a second, often costlier evaluation.
```

```
Name: Regularization / The Lasso
Description: Add a complexity penalty so simpler models are preferred unless a complex one is much
better.
Components: A fit term plus a penalty term; the Lasso's penalty is the sum of absolute values of the
coefficients.
How It Works: Downward pressure on factor weights drives many to exactly zero, leaving only high-impact
factors — turning an overfit model into a robust one.
When It Is Useful: Whenever estimates are noisy and the model would otherwise lean on untrustworthy
quantities.
Limitations: Requires choosing the penalty strength; too much penalty underfits.
```

```
Name: Early Stopping
Description: Halt the tuning/search process before complexity grows too high.
Components: An incremental fitting process; a stopping point. The chapter names *two distinct*
mechanisms: (a) feature-wise — add the most-important factor first, then the next, and stop before
adding more; (b) data-wise — add one data point at a time, tweaking the model for each, and stop before
processing all of them. Both grow complexity gradually.
How It Works: Because complexity accrues with time/iterations, stopping early keeps the model simple
without an explicit penalty — a temporal form of regularization.
When It Is Useful: When more deliberation would add marginal, noisy factors; time-boxed decisions.
Limitations: Stopping too early underfits; you must judge when the important factors are in.
```

```
Name: "Regularizing to the Page" / Broad-Brush Simplification
Description: Constrain the medium so it can't hold too much detail.
Components: A physical limit (a diary page; a thick Sharpie) that caps resolution.
How It Works: A bounded medium forces you to keep only what fits — Darwin deciding when the page ran
out; Fried & Hansson sketching with a marker too thick to draw fine detail.
When It Is Useful: Early-stage decisions and brainstorming under uncertainty.
Limitations: The bound is arbitrary; it approximates rather than computes the right complexity.
```

```
Name: The Uncertainty-Dependent Stopping Rule
Description: Match how hard to think to the gap between measure and matters.
Components: Data quality; error/uncertainty level; the measure-vs-matters gap.
How It Works: Low uncertainty and a small gap → think long and hard (complexity is appropriate). High
uncertainty and a big gap → stop early, prefer simplicity, sometimes trust first instinct.
When It Is Useful: Deciding when more analysis helps vs. hurts.
Limitations: Estimating your own uncertainty and the size of the gap is itself a judgment call.
```

## 5. Research and Evidence

```
Study / Research: German marriage / life-satisfaction survey
Researchers: Not specified ("a recent study conducted in Germany")
Year: Not specified.
Research Question: How does life satisfaction change over the first ten years of marriage?
Method: Survey data; the authors fit one-, two-, and nine-factor polynomial models to it.
Key Finding: The nine-factor model fits every point but makes absurd out-of-sample predictions; the
two-factor "leveling off" matches the psychological/economic consensus (a return to baseline, not
displeasure with marriage). Adding noise makes the nine-factor model gyrate wildly.
Positive precondition (the mirror image of the whole argument): the chapter states crisply that the
most complex model *would* be best "if we had copious data, drawn from a perfectly representative
sample, completely mistake-free, and representing exactly what we're trying to evaluate." That four-part
checklist — copious, representative, mistake-free, valid measure — is when complexity is warranted.
How the Author Uses It: The chapter's central demonstration of overfitting.
Important Limitations: The study is not named; the models are the authors' illustration, not the study's
own analysis.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Dysfunctional Consequences of Performance Measurements
Researchers: V. F. Ridgway (Cornell management professor)
Year: 1950s
Research Question: What perverse effects do performance metrics produce?
Method: A catalog of documented cases.
Key Finding: Metrics reliably distort behavior — rushed interviews, easy end-of-month cases, neglected
factory maintenance — as the "ruthless and clever optimization of the wrong thing."
How the Author Uses It: The empirical backbone of the business/incentives section (a Goodhart-style
result).
Important Limitations: Mid-century case catalog; not quantified here.
Replication or Controversy Mentioned: Echoed by Jobs, Altman, and Kaushik in the modern era.
```

```
Study / Research: The Lasso
Researchers: Robert Tibshirani (biostatistician)
Year: 1996
Research Question: How to penalize model complexity to prevent overfitting?
Method: A regularization algorithm penalizing the sum of absolute coefficient values.
Key Finding: Drives many factor weights to zero, keeping only high-impact factors.
How the Author Uses It: The canonical complexity penalty and template for "natural Lassos."
Important Limitations: Requires tuning the penalty strength.
Replication or Controversy Mentioned: Now "ubiquitous in machine learning."
```

```
Study / Research: Complexity penalties / mathematical Occam's razor
Researchers: Andrey Tikhonov (Russian mathematician)
Year: 1960s
Research Question: How to apply Occam's razor in a mathematical context?
Method: Introduce a term penalizing more complex solutions (Tikhonov regularization).
Key Finding: Complex models must be significantly better, not just slightly, to be justified.
How the Author Uses It: The origin of regularization.
Important Limitations: None discussed.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Markowitz's own retirement allocation
Researchers: Harry Markowitz (1990 Nobel laureate, modern portfolio theory)
Year: Not specified.
Research Question: How should the inventor of optimal portfolio allocation invest his own savings?
Method: Self-report; he split 50/50 between bonds and equities to minimize anticipated regret.
Key Finding: A 50/50 split can't overfit because it ignores unreliable market estimates; his optimal
scheme requires good estimates, and errors in them can increase risk.
How the Author Uses It: The marquee "less is more" case — regularization as rationality under
uncertainty.
Important Limitations: A single self-reported anecdote; the chapter notes 50/50 is "not necessarily the
complexity sweet spot."
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Heuristics and the "less-is-more" effect
Researchers: Gerd Gigerenzer and Henry Brighton
Year: Not specified.
Research Question: Do simple heuristics reduce accuracy, or can they improve it?
Method: Study of heuristics (referenced, not detailed).
Key Finding: "Less information, computation, and time can in fact improve accuracy" — contradicting the
view that less processing reduces accuracy.
How the Author Uses It: Theoretical grounding for treating heuristics as regularization.
Important Limitations: Cited as a conclusion; specific studies not detailed in-chapter.
Replication or Controversy Mentioned: Framed against the "widely held view" that less processing reduces
accuracy.
```

```
Study / Research: Training scars in law enforcement / military
Researchers: Dave Grossman (former Army Ranger, West Point psychology professor)
Year: Not specified.
Research Question: How does rote training produce dangerous automaticity?
Method: Documented anecdotes/reports from real gunfights.
Key Finding: Overfit training produces "training scars" — pocketing brass, holstering after two shots
regardless of threat, handing a disarmed weapon back — sometimes fatal.
How the Author Uses It: The life-and-death illustration of overfitting one's own preparation, and the
motivation for cross-training.
Important Limitations: Anecdotal ("there are stories"); not systematically quantified.
Replication or Controversy Mentioned: The FBI reportedly changed its training in response.
```

## 6. Experiments

```
Experiment Name: Fitting one-, two-, and nine-factor models to marriage data
Setup: Life-satisfaction data over ten years of marriage from a German survey.
Participants: N/A — a modeling demonstration by the authors.
Procedure: Fit polynomial models of increasing complexity; compare in-sample fit and out-of-sample
predictions; then add small random noise (simulating a repeat with different participants) and observe
stability.
Result: One-factor captures the trend but predicts infinite misery; two-factor levels off (matching
expert consensus); nine-factor fits every point but predicts absurd behavior and gyrates wildly under
noise.
Interpretation: Better in-sample fit ≠ better prediction; excess complexity captures noise and becomes
unstable.
What It Demonstrates: The definition and danger of overfitting in one picture.
Potential Alternative Explanation: The specific "nine factors" is a didactic choice; real model
selection would use principled criteria — but the qualitative lesson (instability under resampling) is
robust.
```

```
Experiment Name: Cross-validation by holding back points ("canaries")
Setup: The same marriage data.
Participants: N/A.
Procedure: Randomly hold back two of ten points; fit models to the other eight; test predictions on the
two held-back points.
Result: A complex model that nails the eight but misses the two held-back points is almost certainly
overfitting.
Interpretation: Generalization to unseen data, not fit to seen data, is the true test.
What It Demonstrates: A concrete, usable method to detect overfitting.
Potential Alternative Explanation: With very few points, which two are held back matters; repeated
/k-fold cross-validation is the fuller method (not detailed here).
```

## 7. Cases and Stories

```
Case Title: Darwin's "Marry—Marry—Marry Q.E.D."
People / Organization: Charles Darwin; Emma Wedgwood; (precedent) Benjamin Franklin
Context: In July 1838 Darwin used a pro/con list to decide whether to propose.
What Happened: For marriage he listed children, companionship, "charms of music & female chit-chat";
against, "terrible loss of time," less freedom, expense and anxiety of children, less money for books.
A narrow margin, ending "Marry—Marry—Marry Q.E.D." The first points he listed (children, companionship)
were what actually swayed him; "it is intolerable to think of spending one's whole life like a neuter
bee." He decided exactly when his notes reached the bottom of the page — "regularizing to the page." A
second "When? Soon or Late" list ended in "Never mind, trust to chance"; he proposed within months.
Outcome: A happy marriage and family — reached by his first few reasons, not his last.
Concept Illustrated: Early stopping; regularizing to the page; the book budget as an overfit
distraction.
Why This Case Is Useful: A famous, primary-sourced, oddly relatable hook that both opens and closes the
chapter.
Potential for Reuse: High
```

```
Case Title: Franklin's "Moral or Prudential Algebra"
People / Organization: Benjamin Franklin
Context: A century before Darwin, Franklin endorsed the pro/con list as a formal method.
What Happened: Divide a half-sheet into Pro and Con columns; over three or four days jot motives as they
occur; estimate their weights; strike out equal reasons on each side (one pro = two cons → strike all
three); when nothing new of importance appears, decide. "I have found great Advantage from this kind of
Equation, in what may be called Moral or Prudential Algebra."
Outcome: The archetype of "more factors = better decision" — the premise the chapter dismantles.
Concept Illustrated: The pro/con list as an algorithm; the intuition that overfitting overturns.
Why This Case Is Useful: A historical anchor for the "more is better" premise, quotable and precise.
Potential for Reuse: High
```

```
Case Title: The nine-factor marriage model
People / Organization: The authors; a German life-satisfaction survey
Context: Fitting models of increasing complexity to real happiness data.
What Happened: The nine-factor model fit every data point perfectly but predicted misery at the altar,
a giddy rise, a roller coaster, and a cliff after year ten; the two-factor model's leveling off matched
the expert consensus. Adding noise made the nine-factor model gyrate wildly.
Outcome: A single, vivid demonstration that a perfect fit can be a terrible predictor.
Concept Illustrated: Overfitting; fit vs. generalization; instability under resampling.
Why This Case Is Useful: The chapter's core teaching example; visual and unforgettable.
Potential for Reuse: High
```

```
Case Title: The bronze snake (idolatry of data)
People / Organization: Biblical reference (Book of Kings; First Commandment)
Context: A metaphor for optimizing the proxy instead of the goal.
What Happened: A bronze snake made at God's order becomes an object of worship in place of God. The
authors: overfitting is "idolatry of data," offering prayers to the bronze snake of data rather than the
force behind it.
Outcome: A memorable frame for proxy-metric failure.
Concept Illustrated: Proxy metrics; optimizing the measurable wrong thing.
Why This Case Is Useful: A vivid, culturally resonant metaphor that names the core error.
Potential for Reuse: Medium
```

```
Case Title: Overfitting the palate, fitness, and fencing
People / Organization: The authors; Tom Griffiths (fencer)
Context: Everyday domains where a proxy is gamed.
What Happened: Taste evolved as a proxy for nutrition (fat/sugar/salt), but modifiable foods let us
"overfit taste." Visible fitness markers (low body fat, high muscle) are proxies for health, gameable by
extreme diets and steroids — "the picture of good health, but only the picture." Fencing ("defencing")
once trained dueling skill, but electronic scoring rewards a "flick" of the flexible blade — techniques
useless in a real duel — so athletes overfit tactics to scorekeeping quirks.
Outcome: Three domains where optimizing the measurable proxy corrupts the real goal.
Concept Illustrated: Proxy metrics; evolutionary mismatch (taste); overfitting to scoring rules.
Why This Case Is Useful: Relatable, varied, and the fencing case is a rare direct sports example.
Potential for Reuse: High
```

```
Case Title: Metrics gone wrong in business
People / Organization: Steve Jobs; Sam Altman (Y Combinator); V. F. Ridgway; Avinash Kaushik (Google)
Context: Incentive and measurement failures.
What Happened: Jobs — "incentive structures work… create consequences you can't anticipate"; Altman —
"the company will build whatever the CEO decides to measure"; Ridgway's 1950s catalog (rushed
interviews, easy end-of-month cases, neglected maintenance); Kaushik on cost-per-impression driving
ad-crammed clickbait — "Friends don't let friends measure Page Views. Ever."
Outcome: A chorus of practitioners confirming that metrics get ruthlessly, cleverly optimized — for the
wrong thing.
Concept Illustrated: Idolatry of data; Goodhart-style incentive failure.
Why This Case Is Useful: Quotable, authoritative, immediately applicable to any organization.
Potential for Reuse: High
```

```
Case Title: Training scars
People / Organization: Dave Grossman; the FBI; unnamed police officers
Context: When life-or-death training overfits its own drills.
What Happened: Officers pocketed spent brass mid-gunfight (good range etiquette); dead cops were found
with brass in hand; the FBI changed training after agents reflexively fired two shots and holstered
regardless of threat; one officer disarmed an assailant then instinctively handed the gun back — exactly
as drilled.
Outcome: Overfit preparation that proved dangerous, even fatal.
Concept Illustrated: Overfitting one's own training; the case for cross-training.
Why This Case Is Useful: Dramatic, high-stakes, and it makes an abstract idea viscerally memorable.
Potential for Reuse: High
```

```
Case Title: Markowitz's 50/50 retirement split
People / Organization: Harry Markowitz (1990 Nobel, modern portfolio theory)
Context: The inventor of optimal portfolio allocation investing his own savings.
What Happened: "I should have computed the historical covariances… and drawn an efficient frontier.
Instead, I visualized my grief if the stock market went way up and I wasn't in it — or… way down and I
was completely in it. My intention was to minimize my future regret. So I split my contributions
fifty-fifty between bonds and equities."
Outcome: A Nobel optimizer choosing a heuristic — because a 50/50 split can't overfit unreliable
estimates, and under uncertainty that can be the rational move.
Concept Illustrated: "Less is more"; regularization as rationality; regret minimization (echoing
chapter 2).
Why This Case Is Useful: Delicious irony plus a rigorous point; the single best hook for the chapter's
practical thesis.
Potential for Reuse: High
```

```
Case Title: Food fads vs. evolutionary slowness
People / Organization: The soy/almond/coconut/kale markets; Larry Finkel; Vita Coco; Pizza Hut
Context: How fast culture changes vs. how slow evolution does.
What Happened: Soy milk quadrupled then lost to almond milk ("Soy sounds more like old-fashioned health
food"); coconut water (Vita Coco) up ~300× since 2004, "invisible to unavoidable"; kale up 40% in 2013,
whose biggest prior buyer, Pizza Hut, used it as salad-bar decoration. Meanwhile evolution moves slowly
— decussation (cross-wired nerves) and the ear's repurposed reptilian jawbones are "evolutionary
baggage."
Outcome: A contrast that reframes tradition and evolutionary constraint as anti-overfitting robustness.
Concept Illustrated: The weight of history; constraint as regularization; "jump toward the bandwagon,
not on it."
Why This Case Is Useful: Funny, concrete fad data plus a surprising evolutionary payoff.
Potential for Reuse: High
```

```
Case Title: Tom's over-prepared first lecture
People / Organization: Tom Griffiths
Context: His first semester as a professor.
What Happened: He spent 10+ hours preparing each hour of his first class; the next semester, with far
less prep time, he feared disaster — but students liked the second class *more*. The extra hours had
nailed nitty-gritty details that only confused students (and were later cut). He'd been overfitting his
own taste as a proxy for his students'.
Outcome: Less preparation produced a better class — early stopping in action.
Concept Illustrated: Early stopping; proxy metrics (his taste ≠ students' needs); diminishing/negative
returns to effort.
Why This Case Is Useful: A relatable, self-deprecating case that makes "think less" concrete for
anyone who over-prepares.
Potential for Reuse: High
```

```
Case Title: "Every food a living rat has eaten has not killed it"
People / Organization: Samuel Revusky and Erwin Bedarf (epigraph to "The Weight of History")
Context: A survivorship framing for why the past carries information.
What Happened: The line — a rat's dietary history is, by survivorship, a record of non-lethal foods —
frames why history and constraint carry information: what has persisted has, necessarily, survived.
Outcome: A compact statement of survivorship and the informational value of the past.
Concept Illustrated: The weight of history; constraint as robustness; survivorship.
Why This Case Is Useful: A quotable, slightly eerie framing of "the past is a filter," ideal for the
tradition-as-regularization argument.
Potential for Reuse: High
```

```
Case Title: Franklin's cancellation algebra
People / Organization: Benjamin Franklin
Context: The precise mechanic inside his "Moral or Prudential Algebra."
What Happened: Beyond listing pros and cons, Franklin *cancels* them: strike a pro against an equal con;
strike one pro against two cons it equals; strike two cons against three pros; proceed until the balance
is clear. "I have found great Advantage from this kind of Equation."
Outcome: A genuine algorithm — and an unwitting precursor to the Lasso's driving of terms to zero.
Concept Illustrated: Decision-as-computation; term cancellation prefiguring regularization.
Why This Case Is Useful: Shows the "more factors" premise as a real procedure, and the cancellation
mechanic is a neat bridge to the Lasso.
Potential for Reuse: Medium
```

## 8. Best Teaching Examples

```
Concept: Overfitting
Example: The nine-factor marriage model fits every data point yet predicts misery at the altar and a
cliff after year ten, and gyrates wildly when you add a little noise.
Why It Works: One picture shows both faces of overfitting — perfect fit *and* absurd, unstable
prediction.
Possible Alternative Domain: Mathematics
```

```
Concept: Idolatry of data / proxy metrics
Example: Taste is the body's proxy for nutrition; modifiable foods let us "overfit taste," so the tastiest
foods became the unhealthiest.
Why It Works: Explains a familiar paradox (why bad-for-you food tastes best) with a single clean idea.
Possible Alternative Domain: Everyday Life
```

```
Concept: Regularization / "less is more"
Example: Markowitz, the Nobel inventor of optimal allocation, split his own savings 50/50 — because a
50/50 split can't overfit unreliable estimates.
Why It Works: The irony forces the point that under uncertainty, ignoring information can beat using it.
Possible Alternative Domain: Business
```

```
Concept: Training scars / overfitting your own preparation
Example: Officers pocketing spent brass mid-gunfight, or handing a disarmed weapon back — exactly as
drilled.
Why It Works: A life-or-death image makes "you can overfit your own training" impossible to forget.
Possible Alternative Domain: Sports
```

```
Concept: Cross-validation
Example: Randomly give one student per class an essay or oral exam alongside the standardized test; if
standardized scores rise while the essays fall, "teaching to the test" has set in.
Why It Works: A concrete, cheap protocol that anyone running a metric can picture adopting.
Possible Alternative Domain: Business
```

```
Concept: Early stopping / regularizing to the page
Example: Darwin decided to marry exactly when his pro/con notes reached the bottom of the diary page —
"anything that doesn't make the page doesn't make the decision."
Why It Works: A primary-source image that turns an algorithm into a human habit.
Possible Alternative Domain: Everyday Life
```

```
Concept: Broad-brush simplification under uncertainty
Example: Fried & Hansson brainstorm with a Sharpie too thick to draw fine detail, so they can only think
in shapes and boxes.
Why It Works: A physical constraint literally embodies "don't optimize what should still be out of
focus."
Possible Alternative Domain: Business
```

## 9. Counterintuitive Insights

```
Insight: A model that fits your data perfectly can be your worst predictor.
Common Belief: The closer a model matches the data, the better it is.
Author's Argument: Perfect in-sample fit means the model has absorbed the noise; it then predicts
unseen data terribly and swings wildly under resampling.
Evidence: The nine-factor marriage model.
Why It Is Surprising: It severs "fit" from "truth," the intuition behind most careful analysis.
```

```
Insight: More thinking can produce worse decisions.
Common Belief: The more factors you weigh and the longer you deliberate, the better your choice.
Author's Argument: Beyond a point, extra factors are noisy and the first factors you find are usually
the most important; more deliberation overfits.
Evidence: Darwin (first reasons decided it); Tom's lectures (more prep = worse class); early stopping.
Why It Is Surprising: It inverts the premise of Franklin's Moral Algebra and of careful reasoning
itself.
```

```
Insight: Ignoring information can beat using it.
Common Belief: More information always helps.
Author's Argument: When your estimates are untrustworthy and the model leans on them heavily, a
heuristic that ignores them (a 50/50 split) avoids overfitting and can be more accurate.
Evidence: Markowitz; Gigerenzer & Brighton's "less is more."
Why It Is Surprising: It makes deliberate ignorance a rational, not lazy, strategy.
```

```
Insight: Optimizing a metric can make everything worse.
Common Belief: Measuring and optimizing performance improves it.
Author's Argument: Metrics are proxies; ruthlessly optimizing the proxy ("idolatry of data") corrupts
the real goal — rushed interviews, clickbait, neglected maintenance, teaching to the test.
Evidence: Ridgway; Jobs; Altman; Kaushik.
Why It Is Surprising: It reframes diligent optimization as the *cause* of failure, not the cure.
```

```
Insight: You can overfit your own training — sometimes fatally.
Common Belief: Repetition until automatic is pure preparation.
Author's Argument: Drilling to automaticity can encode the drill's artifacts (range etiquette,
two-shot cadence) that fail catastrophically in reality.
Evidence: Grossman's training scars; the FBI's changed training.
Why It Is Surprising: The very thoroughness meant to prepare you becomes the thing that gets you killed.
```

```
Insight: Evolutionary "baggage" and tradition are features, not bugs.
Common Belief: Suboptimal historical holdovers (cross-wired nerves, repurposed jawbones, old customs)
should be optimized away.
Author's Argument: Constraint by history is anti-overfitting — it prevents drastic over-adaptation to a
present that will change, keeping you robust for an unknown future.
Evidence: Decussation; the ear's jawbones; food fads vs. slow evolution.
Why It Is Surprising: It defends conservatism and imperfection on rigorous statistical grounds.
```

```
Insight: Going with your first instinct can be the rational choice.
Common Belief: Rationality means overriding gut feeling with thorough analysis.
Author's Argument: The more complex, unstable, and uncertain the decision, the more early stopping and
simple heuristics outperform exhaustive analysis.
Evidence: The uncertainty-dependent stopping rule; Mintzberg on judgment; Darwin.
Why It Is Surprising: It reconciles "trust your gut" with rationality instead of opposing them.
```

## 10. Unique or Unusual Ideas

```
Idea: "Idolatry of data" — worshipping the bronze snake of the metric.
Why It Seems Unique: A religious metaphor precisely names a technical failure (proxy optimization),
giving Goodhart's law a memorable moral valence.
Potential Connection to Other Topics: Goodhart's law; measurement culture; the ethics of metrics.
```

```
Idea: Nature, brains, language, and memory are all "Lassos."
Why It Seems Unique: It unifies a statistical technique with metabolism, neural firing, elevator
pitches, and proverbs as the same complexity penalty operating across substrates.
Potential Connection to Other Topics: Metabolic constraints on cognition; compression; the evolution of
concise language.
```

```
Idea: Evolutionary constraint as beneficial regularization.
Why It Seems Unique: It reframes "suboptimal" evolutionary holdovers as robustness-preserving, arguing
we shouldn't want organisms perfectly optimized to a transient niche.
Potential Connection to Other Topics: Evolvability; robustness vs. optimality; developmental
constraints.
```

```
Idea: "Regularizing to the page."
Why It Seems Unique: It reads a physical medium (a diary sheet, a thick marker) as a regularizer,
turning early stopping into a design principle for tools.
Potential Connection to Other Topics: Constraint-based creativity; interface design; time-boxing.
```

```
Idea: "Jump toward the bandwagon, but not necessarily on it."
Why It Seems Unique: A crisp rule for updating on new data without over-adapting to fads — partial,
damped updating as a life strategy.
Potential Connection to Other Topics: Learning rates; exponential smoothing; conservatism as a prior.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: "Think less" vs. the book's many chapters on careful computation.
Author's Position: Under uncertainty and noisy proxies, stop early and simplify; with clean, complete
data, think long and hard.
Possible Counterargument: The rule is correct but its inputs — your own uncertainty and the
measure-vs-matters gap — are themselves hard to estimate, so "when to think less" can smuggle in exactly
the overthinking it warns against. The chapter gives a direction, not a threshold.
What Evidence Would Help Resolve It: A way to gauge, before deciding, how noisy your data and how large
the gap actually are.
```

```
Issue: Simplicity is prescribed, but "too simple" also fails.
Author's Position: Too complex overfits; too simple (the one-factor line predicting infinite misery)
misses the real pattern.
Possible Counterargument: The chapter leans hard toward simplicity ("prefer simplicity, stop earlier")
without an equally sharp warning about underfitting; 50/50 is conceded to be "not necessarily the
complexity sweet spot," but no method for finding the sweet spot is given beyond cross-validation.
What Evidence Would Help Resolve It: A concrete procedure (e.g., cross-validated model selection) for
locating the right complexity rather than defaulting to "simpler."
```

```
Issue: Heuristics as rational — how far does "less is more" generalize?
Author's Position: When estimates are untrustworthy, ignoring information improves accuracy.
Possible Counterargument: This holds precisely when estimates are poor; in data-rich, low-noise domains
the optimal complex model wins, and the chapter says so — but the "less is more" framing is catchier and
risks being over-applied. The condition (untrustworthy estimates, high model weight on them) is the
whole ballgame and easy to drop.
What Evidence Would Help Resolve It: Explicit criteria for when a domain is "estimate-poor" enough to
warrant heuristics over optimization.
```

```
Issue: Training scars argue against drilling — but drilling also builds real skill.
Author's Position: Rote training can overfit; cross-training detects it.
Possible Counterargument: The chapter's vivid failures don't quantify how often drilling helps vs.
harms; automaticity is genuinely life-saving in most cases, and the anecdotes ("there are stories,"
"officers were shocked") are selected for drama. The prescription (cross-train) is sound, but the risk
magnitude is unestablished.
What Evidence Would Help Resolve It: Rates of training-scar incidents relative to the benefits of
automatized skill.
```

```
Issue: Tradition-as-robustness can rationalize any status quo.
Author's Position: A bias toward history buffers against fads.
Possible Counterargument: The same argument could defend genuinely harmful traditions; "don't overfit to
the present" gives no criterion distinguishing protective conservatism from mere inertia. The chapter's
"jump toward the bandwagon, not on it" is a direction, not a discriminator.
What Evidence Would Help Resolve It: A principle for which traditions are robustness-preserving vs.
which are outdated overfits to a vanished environment.
```

## 12. Quotable Ideas

```
Paraphrase (short): Darwin's ledger ended "Marry—Marry—Marry Q.E.D. — It being proved necessary to
Marry."
Why the Idea Matters: The archetype of decision-as-computation, which the chapter both honors and
undercuts.
Source Location: Opening (PDF p. 195).
```

```
Paraphrase (short): Franklin called the pro/con list "Moral or Prudential Algebra."
Why the Idea Matters: Names the "more factors = better" premise the chapter dismantles.
Source Location: Opening (PDF pp. 195–196).
```

```
Paraphrase (short): "Anything you can do I can do better; I can do anything better than you." (Annie Get
Your Gun, epigraph)
Why the Idea Matters: A wink at the "more/better" premise the chapter demolishes.
Source Location: Epigraph to "The Case Against Complexity" (PDF p. 198).
```

```
Paraphrase (short): "Every food a living rat has eaten has, necessarily, not killed it." (Revusky &
Bedarf, epigraph)
Why the Idea Matters: A compact survivorship framing — the past is a filter, which is why constraint and
tradition carry information.
Source Location: Epigraph to "The Weight of History" (PDF p. 213).
```

```
Paraphrase (short): Our future selves often pay good money to remove the tattoos we paid good money to
get. (Daniel Gilbert)
Why the Idea Matters: Present preferences are noisy proxies for our future selves' satisfaction — the
proxy problem, made personal.
Source Location: "The Idolatry of Data" (PDF p. 203).
```

```
Paraphrase (short): A better fit for the data you have does not necessarily mean a better prediction.
Why the Idea Matters: The chapter's thesis in one sentence.
Source Location: "The Case Against Complexity" (PDF p. 201).
```

```
Paraphrase (short): Overfitting is a kind of idolatry of data — optimizing what we can measure rather
than what matters.
Why the Idea Matters: The moral frame that unifies every case in the chapter.
Source Location: "The Idolatry of Data" (PDF pp. 203–204).
```

```
Paraphrase (short): The company will build whatever the CEO decides to measure. (Sam Altman)
Why the Idea Matters: The sharpest statement of metric-driven overfitting in organizations.
Source Location: "Overfitting Everywhere" (PDF p. 206).
```

```
Paraphrase (short): "Friends don't let friends measure Page Views. Ever." (Avinash Kaushik)
Why the Idea Matters: A memorable rallying cry against optimizing a bad proxy.
Source Location: "Overfitting Everywhere" (PDF pp. 206–207).
```

```
Paraphrase (short): If you can't explain it simply, you don't understand it well enough. (Anonymous,
epigraph)
Why the Idea Matters: The intuitive case for penalizing complexity.
Source Location: Epigraph to "How to Combat Overfitting" (PDF p. 209).
```

```
Paraphrase (short): Markowitz split his own savings 50/50 to minimize future regret — because a split
can't overfit.
Why the Idea Matters: The Nobel-optimizer-turned-heuristic that anchors "less is more."
Source Location: "The Upside of Heuristics" (PDF p. 211).
```

```
Paraphrase (short): Less information, computation, and time can in fact improve accuracy. (Gigerenzer &
Brighton)
Why the Idea Matters: The research statement of the chapter's counterintuitive core.
Source Location: "The Upside of Heuristics" (PDF p. 212).
```

```
Paraphrase (short): Jump toward the bandwagon, by all means — but not necessarily on it.
Why the Idea Matters: A damped-updating rule for resisting fads without ignoring new data.
Source Location: "The Weight of History" (PDF pp. 214–215).
```

```
Paraphrase (short): Going with our first instinct can be the rational solution — the more complex and
uncertain the decision, the more so.
Why the Idea Matters: The chapter's reconciliation of instinct and rationality.
Source Location: "When to Think Less" (PDF p. 217).
```

```
Paraphrase (short): What if we started from the premise that we can't measure what matters — then we'd
have to use something scary: judgment. (Henry Mintzberg)
Why the Idea Matters: The closing case for judgment over measurement.
Source Location: "When to Think Less" (PDF p. 217).
```

```
Paraphrase (short): Darwin was "regularizing to the page" — anything that doesn't make the page doesn't
make the decision.
Why the Idea Matters: The chapter's most elegant image of early stopping in a human life.
Source Location: "When to Think Less" (PDF p. 218).
```

## 13. Psychology Connections

- **Judgment and decision-making.** The chapter is a direct challenge to the "more analysis is better"
  model of good decisions, in dialogue with Franklin's Moral Algebra.
- **Ecological rationality (Gigerenzer).** "Less is more" and heuristics-as-regularization are explicitly
  Gigerenzer & Brighton's program — a recurring ally across the book (chs. 2, 4, 6, 7).
- **Affective forecasting (Gilbert).** "We pay good money to remove the tattoos we paid good money to
  get" — our present preferences are noisy proxies for our future selves' satisfaction.
- **Regret minimization.** Markowitz's 50/50 split is explicitly regret-minimizing, echoing Bezos and the
  regret material in chapter 2.
- **Automaticity and skill.** Training scars connect to the psychology of overlearning, procedural
  memory, and stress-induced reversion to drilled behavior.
- **Analysis paralysis / overthinking.** Early stopping formalizes when deliberation stops helping — a
  rigorous account of a familiar failure mode.
- **The measurement/motivation trap.** The metric-distortion cases are choice-architecture and
  incentive-design psychology (Goodhart's law by another name).

## 14. Mathematics and Decision Science Connections

- **Bias–variance tradeoff.** Overfitting is the high-variance end; too-simple is the high-bias end — the
  chapter's whole fit-vs-generalize story is the bias–variance tradeoff without the jargon.
- **Regularization.** Tikhonov regularization and the Lasso (L1 penalty = sum of absolute coefficients)
  are named; ridge/L2 and the general penalty framework sit here.
- **Cross-validation.** Hold-out and (implicitly) k-fold validation as the standard overfitting detector.
- **Occam's razor / model selection.** The chapter is applied model selection — choosing complexity to
  optimize generalization, not fit.
- **Goodhart's law.** "When a measure becomes a target, it ceases to be a good measure" is the exact
  content of the idolatry-of-data section, though not named.
- **Portfolio theory.** Mean-variance optimization (Markowitz) and its estimation-error fragility — the
  "1/N" naive-diversification result is the formal version of his 50/50 anecdote.
- **Learning rates / early stopping.** Early stopping and damped updating ("toward the bandwagon, not on
  it") are the same idea as small learning rates and gradual adaptation.

## 15. Sports Connections

**Direct examples from the book:** Two. (1) Fencing — Tom's own sport; electronic scoring made the
"flick" a winning technique that would fail in a real duel, so athletes overfit tactics to scorekeeping
quirks. (2) Training scars in law-enforcement/military drilling (a close analogue to athletic
overtraining of specific patterns).

**Inferred applications (mine):**
- **Overfitting to a scoring system or ruleset.** Any sport where athletes optimize the *rules* rather
  than the underlying skill — free-throw routines, diving degree-of-difficulty gaming, drawing fouls,
  "flopping" — is overfitting the proxy (points) over the real contest.
- **Overtraining a specific pattern.** Drilling one move to automaticity (a set-piece routine, a serve
  toss) can produce a "training scar" that an opponent exploits by presenting an unfamiliar look; the
  fix is cross-training against varied, unscripted scenarios.
- **Analytics overfitting.** A model tuned to a small sample of a player's past performance (a hot
  streak, a favorable schedule) predicts future performance badly — the marriage-model lesson applied to
  scouting; regularize toward priors (regression to the mean).
- **Coaching "less is more."** Over-coaching — too many cues, too complex a game plan — can degrade
  performance like Tom's over-prepared lecture; the simplest plan is often the most robust under the
  uncertainty of a live match.
- **Tradition vs. innovation.** A dose of tactical conservatism buffers a team against fad formations
  that opponents quickly counter — "jump toward the bandwagon, not on it" applied to tactical trends.

## 16. AI and Machine Learning Connections

**Direct from the book:** The chapter *is* machine-learning material — overfitting, cross-validation,
regularization, the Lasso, Tikhonov regularization, and early stopping are all core ML concepts
described directly. The chapter states outright that artificial neural networks "can learn arbitrarily
complex functions — even more flexible than our nine-factor model — but precisely because of this very
flexibility they are notoriously vulnerable to overfitting," and that *biological* neural nets sidestep
this by trading performance against maintenance cost (minimizing neurons firing) — a direct
metabolism-as-regularizer link, not an inferred one.

**Inferred connections (mine):**
- **The bias–variance tradeoff and modern deep learning.** The chapter's account predates the
  "double-descent"/overparameterization era; today's large models overfit-and-then-generalize in ways
  that complicate the simple "more capacity = more overfitting" story, an interesting cross-reference.
- **Regularization techniques.** L1 (Lasso)/L2 (ridge), dropout, weight decay, and data augmentation are
  the practical descendants of the chapter's "penalize complexity."
- **Early stopping in training.** Literally a standard technique — halt training when validation loss
  rises — exactly the chapter's temporal regularization.
- **Reward misspecification / Goodhart in RL.** "Idolatry of data" is reward hacking: an agent
  perfectly optimizing a proxy reward corrupts the true objective — the training-scar/metric-distortion
  problem in AI alignment.
- **Test-set contamination / "teaching to the test."** Cross-validation and held-out evaluation are the
  ML answer to the standardized-test analogy; benchmark overfitting in LLM evaluation is the same
  failure.
- **Inductive bias as constraint.** "Evolutionary baggage as beneficial regularization" maps onto
  inductive biases and architectural priors that trade some flexibility for better generalization.
- **Simplicity priors.** Occam's-razor / minimum-description-length principles underlie model selection
  and are the theoretical root of the chapter's complexity penalties.

## 17. Content Creation Opportunities

```
Idea Title: Why thinking harder gives you worse answers
Format: YouTube Long-form
Application Domain: Everyday Life
Hidden Principle: Signal vs. Noise
Story Hook (Layer 1): There's a mathematical reason your most carefully reasoned decisions can be your
worst — and it's the same reason the tastiest food is the worst for you.
Principle Framework (Layer 2): Overfitting: a model (or mind) tuned too finely to the data you happen to
have fits it perfectly but generalizes terribly. Because data are noisy proxies, more factors and more
thought can fit the noise, not the signal.
Best Supporting Case: The nine-factor marriage model; taste as an overfittable proxy for nutrition;
Darwin "regularizing to the page."
Character Application: Insight: Interpreter
Psychology Angle: Overthinking and analysis paralysis, formalized.
Math Angle: Fit vs. generalization; the bias–variance tradeoff.
Sports Angle: Over-coaching and overtraining a single move.
Business Angle: Elaborate models that fit last quarter and miss next quarter.
Investing Angle: Curve-fit backtests that blow up out of sample.
History Angle: Why over-precise forecasts have a worse track record than simple rules.
AI Angle: Overfitting, regularization, early stopping.
```

```
Idea Title: A Nobel Prize winner's dumb-looking investment
Format: YouTube Short
Application Domain: Investing
Hidden Principle: Signal vs. Noise
Story Hook (Layer 1): The man who won the Nobel Prize for the math of optimal investing put his own money
in the dumbest possible split — 50/50 — and he was right.
Principle Framework (Layer 2): When your inputs are unreliable estimates, a simple rule that can't overfit
them beats the "optimal" model that does; naive diversification is regularization — deliberately refusing
to trust noisy precision.
Best Supporting Case: Harry Markowitz splitting 50/50; why a fixed split can't overfit unreliable
estimates.
Character Application: Nova: Strategist
Psychology Angle: Regret minimization; when ignoring information is smart.
Math Angle: Estimation error; naive diversification beating mean-variance optimization.
Sports Angle: Simple game plans beating over-engineered ones.
Business Angle: A blunt, robust policy over a finely-tuned one built on shaky forecasts.
Investing Angle: 1/N allocation vs. optimizers that overfit historical covariances.
History Angle: The gap between elegant theory and what its own author did with his money.
AI Angle: When a simpler model generalizes better than a tuned one.
```

```
Idea Title: The metric that's quietly ruining your company
Format: YouTube Long-form
Application Domain: Business
Hidden Principle: Feedback Loops
Story Hook (Layer 1): "The company will build whatever the CEO decides to measure" — pick the wrong number
and you'll optimize your business straight into the ground.
Principle Framework (Layer 2): Goodhart's law / idolatry of data: ruthlessly optimizing a proxy metric
corrupts the real goal, because the measure and what matters diverge and the incentive loop chases the
measure. Cross-validate any metric against an independent read of the true objective.
Best Supporting Case: Ridgway's 1950s catalog of metric dysfunctions; Kaushik's "Friends don't let
friends measure Page Views"; Altman and Jobs.
Character Application: Sigma: Architect
Psychology Angle: Incentive design; optimizing the proxy over the goal.
Math Angle: Proxy metrics; cross-validating a metric against an independent measure.
Sports Angle: Gaming a scoring system instead of winning the real contest.
Business Angle: KPIs and OKRs that get hit while the business gets worse.
Investing Angle: Managing to a benchmark's quirks instead of real risk-adjusted return.
History Angle: Ridgway's 1956 "Dysfunctional Consequences of Performance Measurements" as the founding
warning.
AI Angle: Reward hacking and benchmark overfitting in AI.
```

```
Idea Title: Training that gets you killed
Format: YouTube Short
Application Domain: Everyday Life
Hidden Principle: Signal vs. Noise
Story Hook (Layer 1): Police officers have been found dead in gunfights with their spent shell casings
neatly in their pockets — because that's what they'd practiced on the range.
Principle Framework (Layer 2): You can overfit your own preparation ("training scars"): drilling an
incidental detail until stress makes you execute it automatically, even when it's fatal. Practise the
signal (the goal), not the noise (the range routine).
Best Supporting Case: Grossman's training scars; the FBI's two-shot-then-holster habit; the officer who
disarmed an assailant and handed the gun back.
Character Application: Blaze: Executor
Psychology Angle: Overlearning; stress-induced reversion to drilled behaviour.
Math Angle: Overfitting; cross-training as cross-validation.
Sports Angle: Drilling one pattern until an opponent exploits it.
Business Angle: Process trained so rigidly it fails the moment reality differs from the manual.
Investing Angle: A strategy drilled for one regime that executes on autopilot into a different one.
History Angle: Military and police training reforms after fatal "training scar" incidents.
AI Angle: Models that fail on any input unlike their training data.
```

```
Idea Title: Why old, imperfect designs survive — and should
Format: YouTube Long-form
Application Domain: History
Hidden Principle: Evolution
Story Hook (Layer 1): Your brain is cross-wired and the bones in your ear used to be a reptile's jaw —
and these "flaws" are exactly why you're robust.
Principle Framework (Layer 2): Constraints, baggage, and tradition are regularization: they penalize
complexity and damp overreaction to a transient present, so evolved and inherited "imperfections" protect
against overfitting the current moment. Jump toward the bandwagon, not on it.
Best Supporting Case: Decussation (the cross-wired brain); the ear's former jawbones; food fads (kale,
coconut water).
Character Application: Insight: Interpreter
Psychology Angle: Conservatism and the fear of missing out.
Math Angle: Robustness vs. optimality; damped updating / learning rates.
Sports Angle: Tactical conservatism vs. chasing fad formations.
Business Angle: Legacy constraints and "the way we've always done it" as accidental robustness.
Investing Angle: Boring, time-tested allocations vs. the newest hot strategy.
History Angle: Institutions and traditions as slow, robust regularizers against fads.
AI Angle: Inductive bias; why constraints improve generalization.
```

```
Idea Title: The past is a filter — why old things that survive are worth trusting
Format: YouTube Short
Application Domain: Everyday Life
Hidden Principle: Evolution
Story Hook (Layer 1): "Every food a rat has eaten hasn't killed it" — that one sentence explains why
tradition beats the latest fad more often than you'd think.
Principle Framework (Layer 2): Age is evidence: something that has survived a long exposure has already
passed a filter the newest option hasn't, so the weight of history is a rational prior (the Lindy
effect), not mere nostalgia.
Best Supporting Case: The Revusky & Bedarf epigraph; food fads (kale, coconut water); decussation.
Character Application: Echo: Observer
Psychology Angle: Survivorship bias — and its rational flip side.
Math Angle: The past as a filter / prior; damped updating.
Sports Angle: Time-tested tactics vs. fad formations.
Business Angle: Long-lived products and practices as pre-filtered by survival.
Investing Angle: The Lindy effect — how long something's lasted as a prior on how long it will.
History Angle: Why customs that survive centuries usually encode something worth keeping.
AI Angle: Inductive bias; why constraints improve generalization.
```

```
Idea Title: Ben Franklin invented an algorithm — and it was wrong
Format: YouTube Short
Application Domain: History
Hidden Principle: Signal vs. Noise
Story Hook (Layer 1): Ben Franklin's famous method — list every pro and con and weigh them all — is
exactly the thing machine learning warns you not to do.
Principle Framework (Layer 2): A long weighted pro/con list overfits: adding marginal factors fits the
noise and swamps the few that matter. Regularization (à la the Lasso, which zeroes out weak terms) says
decide on the handful of dominant reasons.
Best Supporting Case: Franklin's "moral algebra" of cancelling pros and cons; the nine-factor marriage
model; Darwin regularizing to the page.
Character Application: Nova: Strategist
Psychology Angle: Overthinking; when more factors hurt.
Math Angle: Overfitting; regularization; the Lasso's zeroing of terms.
Sports Angle: Over-analysis in game planning.
Business Angle: Decision matrices with twenty weighted criteria that obscure the two that decide it.
Investing Angle: A thesis with a dozen bullet points vs. the one or two that actually drive it.
History Angle: Franklin's 1772 "moral algebra" letter as a beloved but flawed decision heuristic.
AI Angle: Feature selection and complexity penalties.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B01-C07-01
Title: Overfitting — a perfect fit can be a terrible predictor
Type: Concept
Summary: A model tuned too finely to observed data captures noise as signal: it fits the available data
perfectly but predicts unseen data badly and swings wildly under resampling. The nine-factor marriage
model hits every point yet predicts misery at the altar and a cliff after year ten; the two-factor
"leveling off" matches the expert consensus. A better fit for available data ≠ a better prediction.
Source: Algorithms to Live By, ch. 7, "The Case Against Complexity" (PDF pp. 198–203)
Tags: overfitting, model-complexity, fit-vs-generalize, core-concept
Related Concepts: Cross-validation, regularization, idolatry of data
```

```
CARD ID: B01-C07-02
Title: Every decision is a prediction
Type: Concept
Summary: Any choice is a theory that must both account for past experience and say something about
future experience you're guessing at. That double duty creates the unavoidable tension between fitting
what you know and generalizing to what you don't — the root of overfitting.
Source: Algorithms to Live By, ch. 7, "The Case Against Complexity" (PDF p. 198)
Tags: decision-as-prediction, generalization, framing, concept
Related Concepts: Overfitting, proxy metric, model complexity
```

```
CARD ID: B01-C07-03
Title: Idolatry of data — optimizing the proxy
Type: Insight
Summary: Overfitting is "a kind of idolatry of data": worshipping the measurable proxy (taste for
health, KPIs for value, test scores for learning) rather than what actually matters — offering prayers
to "the bronze snake of data" instead of the force behind it. Our own daily data are noisy proxies too
(Gilbert: "we pay good money to remove the tattoos we paid good money to get").
Source: Algorithms to Live By, ch. 7, "The Idolatry of Data" (PDF pp. 203–204)
Tags: proxy-metric, goodhart, idolatry-of-data, insight
Related Concepts: Overfitting, incentive failure, cross-validation
```

```
CARD ID: B01-C07-04
Title: Taste, fitness, and fencing — everyday overfitting
Type: Case
Summary: Taste evolved as a proxy for nutrition (fat/sugar/salt); modifiable foods let us "overfit
taste," so the tastiest foods became the unhealthiest. Visible fitness markers are gameable by extreme
diets and steroids ("the picture of good health, but only the picture"). Electronic fencing rewards a
"flick" useless in a real duel — athletes overfit tactics to scorekeeping.
Source: Algorithms to Live By, ch. 7, "Overfitting Everywhere" (PDF pp. 204–205)
Tags: proxy-metric, evolutionary-mismatch, sports, everyday, case
Related Concepts: Idolatry of data, overfitting, scoring rules
```

```
CARD ID: B01-C07-05
Title: Metrics get ruthlessly optimized — for the wrong thing
Type: Study
Summary: V. F. Ridgway's 1950s "Dysfunctional Consequences of Performance Measurements" cataloged
perverse effects: rushed interviews, easy end-of-month cases, neglected factory maintenance. Steve Jobs:
"incentive structures work… create consequences you can't anticipate." Sam Altman: "the company will
build whatever the CEO decides to measure." Kaushik: "Friends don't let friends measure Page Views."
Source: Algorithms to Live By, ch. 7, "Overfitting Everywhere" (PDF pp. 205–207)
Tags: metrics, goodhart, incentives, business, study
Related Concepts: Idolatry of data, cross-validation, proxy metrics
```

```
CARD ID: B01-C07-06
Title: Training scars — overfitting your own preparation
Type: Case
Summary: Rote drilling can encode the drill's artifacts. Grossman: officers pocketed spent brass
mid-gunfight; dead cops were found with brass in hand; the FBI changed training after agents reflexively
fired two shots and holstered regardless of threat; one officer disarmed an assailant then instinctively
handed the gun back. You can overfit your own training — sometimes fatally.
Source: Algorithms to Live By, ch. 7, "Overfitting Everywhere" (PDF pp. 205–207)
Tags: training-scars, automaticity, overfitting, life-and-death, case
Related Concepts: Cross-training, cross-validation, overlearning
```

```
CARD ID: B01-C07-07
Title: Cross-validation — test on data you didn't fit
Type: Model
Summary: Assess how well a model generalizes to unseen data, not just how well it fits its own. Hold
back points as "canaries" (nailing the training points but missing held-out ones signals overfitting),
or cross-validate a proxy against a different measure — e.g. random essay/oral exams alongside
standardized tests to catch "teaching to the test," or unfamiliar "cross-training" to catch training
scars.
Source: Algorithms to Live By, ch. 7, "Detecting Overfitting" (PDF pp. 207–209)
Tags: cross-validation, generalization, detection, model
Related Concepts: Overfitting, proxy metrics, teaching to the test
```

```
CARD ID: B01-C07-08
Title: Regularization and the Lasso
Type: Model
Summary: Add a complexity penalty so a complex model must be *significantly* better to be chosen —
Tikhonov's 1960s mathematical Occam's razor. The Lasso (Tibshirani, 1996) penalizes the total weight
(sum of absolute coefficients — the L1 norm; see §14) of a model's factors, driving many to zero and
keeping only high-impact ones — turning an overfit nine-factor model into a robust few-factor one.
Source: Algorithms to Live By, ch. 7, "How to Combat Overfitting" (PDF pp. 209–210, footnote p. 219)
Tags: regularization, lasso, occams-razor, complexity-penalty, model
Related Concepts: Overfitting, early stopping, natural Lassos
```

```
CARD ID: B01-C07-09
Title: Nature, brains, and language are all "Lassos"
Type: Insight
Summary: Complexity penalties appear across substrates. Metabolism is a caloric brake — the brain burns
~1/5 of daily calories, so we're "as brainy as we've needed to be, but not extravagantly more." Brains
minimize neurons firing. Language is penalized by length and listener attention (elevator pitches,
proverbs); memory is an inherent Lasso.
Source: Algorithms to Live By, ch. 7, "How to Combat Overfitting" (PDF pp. 210–211)
Tags: natural-lasso, metabolism, language, evolution, insight
Related Concepts: The Lasso, regularization, heuristics
```

```
CARD ID: B01-C07-10
Title: Markowitz's 50/50 — "less is more"
Type: Case
Summary: Harry Markowitz (1990 Nobel for mean-variance optimization) split his own retirement 50/50 to
minimize regret. His optimal scheme needs good statistical estimates; errors in them can increase risk,
while a 50/50 split "can't overfit" because it ignores the estimates. Under uncertainty, a simple
heuristic can be the rational choice. Gigerenzer & Brighton: "less information, computation, and time
can in fact improve accuracy."
Source: Algorithms to Live By, ch. 7, "The Upside of Heuristics" (PDF pp. 211–212)
Tags: less-is-more, heuristics, portfolio, regret, case
Related Concepts: Regularization, estimation error, judgment
```

```
CARD ID: B01-C07-11
Title: The weight of history — constraint as robustness
Type: Insight
Summary: Being constrained by the past makes an organism or culture less perfectly fit to the present
but more robust to an unknown future — fully optimizing to a niche makes you dangerously sensitive to
change. Decussation (cross-wired nerves) and the ear's malleus/incus/stapes (repurposed reptilian
jawbones) are "evolutionary baggage" that resists overfitting. Culture changes fast, evolution slow.
Source: Algorithms to Live By, ch. 7, "The Weight of History" (PDF pp. 213–215)
Tags: robustness, evolutionary-constraint, tradition, anti-overfitting, insight
Related Concepts: Early stopping, regularization, fads
```

```
CARD ID: B01-C07-12
Title: Fads vs. slow evolution — jump toward the bandwagon, not on it
Type: Case
Summary: Food fads rise and fall fast: soy milk quadrupled then lost to almond milk; coconut water
(Vita Coco) rose ~300× since 2004; kale grew 40% in 2013 (Pizza Hut's prior top use: salad-bar
decoration). Evolution, by contrast, is slow — a buffer. Tradition plays evolution's role for culture:
a bias toward history buffers against boom-and-bust fads. "Jump toward the bandwagon… but not
necessarily on it."
Source: Algorithms to Live By, ch. 7, "The Weight of History" (PDF pp. 213–215)
Tags: fads, tradition, damped-updating, culture, case
Related Concepts: Weight of history, learning rate, robustness
```

```
CARD ID: B01-C07-13
Title: Early Stopping — more time means more complexity
Type: Model
Summary: Prevent overfitting by cutting the tuning/search short before a model grows too complex. Many
algorithms add the most important factor first, then the next — stopping short keeps them simple; others
add one data point at a time. More deliberation guarantees more factors and hypotheticals, hence more
overfitting risk. It grounds "a reasoned argument against reasoning."
Source: Algorithms to Live By, ch. 7, "The Weight of History" (PDF pp. 214–216)
Tags: early-stopping, regularization, think-less, model
Related Concepts: Regularization, the Lasso, uncertainty
```

```
CARD ID: B01-C07-14
Title: Tom's over-prepared lecture
Type: Case
Summary: Tom spent 10+ hours preparing each hour of his first class; the next semester, with far less
prep, he feared disaster — but students liked that class *more*. The extra hours nailed nitty-gritty
details that only confused students (later cut). He'd been overfitting his own taste as a proxy for his
students'. Less preparation produced a better result — early stopping in a life.
Source: Algorithms to Live By, ch. 7, "The Weight of History" (PDF pp. 215–216)
Tags: early-stopping, proxy-metric, over-preparation, teaching, case
Related Concepts: Idolatry of data, diminishing returns, think less
```

```
CARD ID: B01-C07-15
Title: When to think less — match effort to uncertainty
Type: Insight
Summary: How early to stop depends on the gap between what you can measure and what matters. Complete,
error-free data you can assess directly → think long and hard. High uncertainty, limited data, an
unclear read on how you'll be evaluated → stop early, prefer simplicity, use a broad brush (Fried &
Hansson's thick Sharpie). Mintzberg: if we can't measure what matters, we must use "something very
scary: judgment." The more uncertain the decision, the more rational it is to trust first instinct.
Source: Algorithms to Live By, ch. 7, "When to Think Less" (PDF pp. 216–217)
Tags: stopping-rule, uncertainty, judgment, simplicity, insight
Related Concepts: Early stopping, heuristics, cross-validation
```

```
CARD ID: B01-C07-16
Title: Darwin regularizing to the page
Type: Case
Summary: Darwin decided to marry exactly when his pro/con notes reached the bottom of the diary sheet —
"anything that doesn't make the page doesn't make the decision." The chapter likens the page limit to
*both* Early Stopping (a stop-when-you-run-out) *and* the Lasso (a hard cap on total content). The first
points he listed (children, companionship) swayed him; the book budget was a distraction. His follow-up
"When? Soon or Late" list weighed everything from happiness to expenses to "awkwardness" to his
long-standing desire to travel by hot air balloon and/or to Wales — then ended "Never mind, trust to
chance," and he proposed within months.
Source: Algorithms to Live By, ch. 7, "When to Think Less" (PDF pp. 217–218)
Tags: darwin, regularizing-to-the-page, early-stopping, primary-source, case
Related Concepts: Early stopping, the Lasso, first instinct
```

```
CARD ID: B01-C07-17
Title: Broad-brush simplification under uncertainty
Type: Model
Summary: Constrain the medium so it can't hold too much detail. Fried & Hansson brainstorm with a
Sharpie too thick to draw fine detail, forcing thinking in shapes and boxes — "the big picture is all
you should be worrying about in the beginning." A physical bound as a regularizer for early-stage,
uncertain decisions.
Source: Algorithms to Live By, ch. 7, "When to Think Less" (PDF p. 217)
Tags: simplification, broad-brush, constraint, brainstorming, model
Related Concepts: Regularizing to the page, early stopping, uncertainty
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: Every decision is a prediction, and a model (or mind) tuned too finely to the data you
happen to have fits it perfectly but generalizes terribly — overfitting. Because our data are almost
always noisy proxies for what matters, overfitting is "idolatry of data": ruthlessly optimizing the
wrong, measurable thing. Detect it with cross-validation, combat it by penalizing complexity
(regularization / the Lasso / Occam's razor) and by stopping early, and remember that the greater the
uncertainty and the wider the measure-vs-matters gap, the more you should simplify and think less —
sometimes your first instinct is the rational choice.

Top 5 Concepts:
1. Overfitting (a perfect fit can be a terrible predictor)
2. Idolatry of data / proxy metrics (optimizing the measurable wrong thing)
3. Cross-validation (test generalization to unseen or different data)
4. Regularization / the Lasso / early stopping (penalize complexity; stop early)
5. "Less is more" heuristics and the weight of history (constraint as robustness)

Top 3 Claims:
1. A better fit for available data does not mean a better prediction — extra complexity can make
   predictions dramatically worse, not just yield diminishing returns.
2. Ruthlessly optimizing a proxy metric corrupts the real goal (Goodhart-style), from taste and test
   scores to KPIs and training drills.
3. Under high uncertainty and untrustworthy estimates, simpler heuristics (and stopping early) can be
   more accurate than the "optimal" complex model — sometimes first instinct is rational.

Top 3 Cases:
1. The nine-factor marriage model (overfitting in one picture) and Darwin regularizing to the page
2. Markowitz's 50/50 retirement split ("less is more"; regularization as rationality)
3. Training scars (Grossman) and metric distortion (Ridgway/Jobs/Altman/Kaushik)

Top 3 Studies:
1. The Lasso (Tibshirani, 1996) and Tikhonov regularization (1960s)
2. Ridgway's "Dysfunctional Consequences of Performance Measurements" (1950s)
3. Gigerenzer & Brighton on the "less-is-more" effect

Most Unique Idea: "Idolatry of data" and the recognition that nature, brains, language, memory, and
tradition are all "Lassos" — complexity penalties operating across biology and culture, so evolutionary
"baggage" and conservatism are beneficial regularization against overfitting a transient present.

Most Counterintuitive Idea: More thinking, more factors, and more data can make your decisions
dramatically worse; ignoring information and going with your first instinct can be the rational choice.

Biggest Weakness or Open Question: The prescription ("prefer simplicity, stop earlier") depends on
correctly gauging your own uncertainty and the measure-vs-matters gap, which the chapter can't
operationalize; it leans hard toward simplicity without an equally sharp warning about underfitting or a
concrete method (beyond cross-validation) for finding the complexity sweet spot; and "tradition as
robustness" gives no criterion distinguishing protective conservatism from mere inertia.

Best Content Opportunity: A long-form video on "why thinking harder gives you worse answers" — the
nine-factor marriage model, taste as an overfittable proxy, Markowitz's 50/50 split, and Darwin
regularizing to the page — landing on "when to think less" and the Goodhart/idolatry-of-data frame.
```
