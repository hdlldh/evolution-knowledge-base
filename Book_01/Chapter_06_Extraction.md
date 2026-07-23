# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 6: Bayes's Rule — Predicting the Future
**Author:** Brian Christian and Tom Griffiths
**Type:** Extraction
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 168–194 (book chapter 6, incl. footnotes)
**Date:** 2026-07-21
**Revision note:** Revised after Chapter_06_Audit.md; see that file for what changed and why.

```
BOOK:
Algorithms to Live By: The Computer Science of Human Decisions

AUTHOR:
Brian Christian and Tom Griffiths

CHAPTER:
6 — Bayes's Rule: Predicting the Future
```

---

## 1. Chapter Thesis

To predict the future from small data — often a single observation — you reason *backward* from what
you've seen to the most probable underlying reality, which requires reasoning *forward* from
hypotheticals (the likelihood) and combining it with a *prior*: your prior beliefs multiplied by the
evidence. Bayes's Rule shows that good predictions depend far more on having the right prior — knowing
which *distribution* your data comes from — than on having lots of data. Three distribution shapes give
three completely different prediction rules: power-law → Multiplicative (multiply what you've seen),
normal → Average (predict the natural average), Erlang/memoryless → Additive (always a constant amount
more). Humans are surprisingly good intuitive Bayesians because "small data is big data in disguise" —
our priors, absorbed from the world, are rich — which means our predictions reveal our experience, and
that media distorts our priors so badly that protecting them may mean turning off the news.

## 2. Key Concepts

```
Concept Name: Reasoning Backward (Bayesian Inference)
Definition: Inferring the hidden cause (the full ticket pool) from observed effects (the tickets you
drew), by first reasoning *forward* — computing how probable your observations would be under each
hypothesis (the "likelihood").
Why It Matters: Bayes's critical insight; it converts an intractable "what's really going on?" into a
comparison of how well each hypothesis predicts what you saw.
How the Author Uses It: The chapter's foundational move; the raffle, the coins, and the Berlin Wall are
all worked backward from observation to cause.
Related Concepts: Likelihood, prior, Bayes's Rule, Laplace's Law.
```

```
Concept Name: Likelihood
Definition: The probability you would have seen exactly your data if a given hypothesis were true.
Why It Matters: The engine of Bayesian reasoning — three winning tickets in a row is 100% likely if all
tickets win, 1/8 if half do, one-in-a-billion if 1/1000 do, so the evidence favors the generous
hypotheses in exactly those ratios.
How the Author Uses It: To quantify intuition — "exactly eight times likelier" — and as the forward
step that makes backward inference possible.
Related Concepts: Reasoning backward, prior, Bayes's Rule.
```

```
Concept Name: Laplace's Law
Definition: With no prior knowledge, after w wins in n attempts, estimate the true success rate as
(w+1)/(n+2).
Why It Matters: The first simple rule of thumb for small data — one win in one try → 2/3 (not 100%),
five in ten → 50% — and it works identically whether you have one data point or millions.
How the Author Uses It: To distill Bayes's infinite hypotheses into a single actionable number;
justifies Annie's faith the sun will rise (~1.6 trillion prior sunrises → ~100%).
Related Concepts: Uniform/uninformative prior, Bayes's Rule, small data.
```

```
Concept Name: Bayes's Rule (Prior × Evidence)
Definition: Combine preexisting beliefs with observed evidence by multiplying their probabilities:
posterior ∝ prior × likelihood.
Why It Matters: The general solution to combining what you already believed with what you just saw;
requires a prior, even a guessed one.
How the Author Uses It: The nine-fair-plus-one-two-headed-coin example (a fair coin is 9× likelier to
be drawn but half as likely to show heads → 4.5× likelier fair); the backbone of every prediction rule
that follows.
Related Concepts: Prior, likelihood, Copernican Principle, prediction rules.
```

```
Concept Name: The Prior (Prior Probability)
Definition: Your sense of how probable each hypothesis was before seeing any data — "what was in the
bag."
Why It Matters: Bayes's Rule always needs one; you can't multiply two probabilities when you're missing
one. The historically controversial ingredient (called biased, unscientific), yet a blank slate is rare.
How the Author Uses It: To argue that prediction quality hinges on prior quality, and to set up the
"uninformative prior" that yields the Copernican Principle.
Related Concepts: Uninformative prior, distribution shape, small data is big data in disguise.
```

```
Concept Name: The Copernican Principle
Definition: Assuming your moment of observation isn't special, you've probably arrived halfway through
something's life, so predict it will last exactly as long as it already has.
Why It Matters: A one-line prediction algorithm from a single data point (Berlin Wall at 8 years → 8
more); it is exactly Bayes's Rule with an uninformative prior.
How the Author Uses It: To predict institutions and relationships, and to expose when the method fails
(a 90-year-old → 180) because we actually have informative priors about human lifespans.
Related Concepts: Uninformative prior, power-law distribution, Multiplicative Rule, German tank problem.
```

```
Concept Name: Uninformative / Uniform Prior
Definition: Pleading total ignorance by treating every possibility (every ticket proportion, every
possible lifespan scale) as equally likely.
Why It Matters: It is what turns Bayes's Rule into the Copernican Principle — and it is itself a
power-law distribution over scales.
How the Author Uses It: To reconcile the Copernican Principle with Bayes, and to explain why it works
when we know nothing and fails when we know something.
Related Concepts: Copernican Principle, power-law, prior.
```

```
Concept Name: Distribution Shape as Prior (Normal / Power-Law / Erlang)
Definition: Three families of quantities: normal (cluster around a natural scale — lifespans, heights),
power-law/scale-free (most below the mean, a few enormous — town size, income, box office), and Erlang
(memoryless — intervals between independent events).
Why It Matters: Knowing which distribution you face is the single most important thing for prediction,
because each yields a completely different rule.
How the Author Uses It: The organizing scheme of the chapter's back half; each distribution gets a
prediction rule and a "surprise" behavior.
Related Concepts: Multiplicative/Average/Additive Rules, preferential attachment, memorylessness.
```

```
Concept Name: The Three Prediction Rules (Multiplicative / Average / Additive)
Definition: Power-law → multiply what you've observed by a constant (2 for uninformative, ~1.4 for
movies); normal → predict the distribution's natural average; Erlang/memoryless → always predict a
constant amount more.
Why It Matters: Simple, distinct rules of thumb that follow directly from the prior's shape and that
people apply implicitly, remarkably accurately.
How the Author Uses It: To make Bayesian prediction usable, and to explain gambling, the marshmallow
test, and Gould's cancer survival.
Related Concepts: Distribution shape, memorylessness, surprise.
```

```
Concept Name: Memorylessness
Definition: A distribution (Erlang) that gives the same prediction regardless of history or current
state — the chance of the event now is the same as an hour ago or an hour hence.
Why It Matters: Explains why some waits have no right moment to quit ("The Gambler" has no answer for a
memoryless game), which partly explains gambling's addictiveness.
How the Author Uses It: The Additive Rule; the blackjack "twenty more hands" that never changes; the
gambler stuck with no tipping point.
Related Concepts: Erlang distribution, Additive Rule, radioactive decay.
```

```
Concept Name: Small Data Is Big Data in Disguise
Definition: We predict well from one observation because our priors — absorbed unconsciously from the
world — are rich and accurate.
Why It Matters: Reframes human intuition as approximate Bayesian inference, and implies our predictions
reverse-engineer our priors (and thus our experience).
How the Author Uses It: The Tenenbaum experiments showing people match Bayes's Rule across domains
(and fail only where priors are poor, like pharaohs' reigns). Scope matters: the "good Bayesian" result
is bounded to domains where absorbed priors are accurate — it is *not* a blanket claim, and the chapter
itself shows it breaking exactly where priors are distorted (pharaohs; and, in the closing section,
media).
Related Concepts: Prior, distribution shape, protecting your priors.
```

```
Concept Name: Protecting Your Priors
Definition: Guarding the accuracy of your internal distributions against distortion — because language
and media report the interesting/rare, not the frequent.
Why It Matters: The hinge is subtle: direct experience is *automatically* frequency-calibrated (events
are experienced at their true frequencies) and even biased priors are usually locally adaptive — a
desert dweller overestimates sand, a polar dweller snow, but each is well tuned to its ecological niche.
What breaks calibration is *language* — we retell the rare (a snake bite, a lightning strike), not the
frequent — and mechanical reproduction (printing press, nightly news, social media) amplifies that
de-calibration. So bias per se is not the villain; the decoupling of talk from experience is. Media
representation doesn't track real-world frequency (murder down 20% but news gun violence up 600% in the
1990s), so being a good intuitive Bayesian may mean turning off the news (the authors' inference from
the distortion evidence, not a demonstrated result).
How the Author Uses It: The chapter's closing prescription; the plane-crash-vs-car-crash asymmetry.
Related Concepts: Small data, ecological niche, preferential attachment, availability heuristic.
```

## 3. Key Claims

```
Claim: Predicting from a single data point is not absurd — we do it constantly and can do it well.
Type: Theoretical / Interpretive
Evidence Provided: Gott at the Berlin Wall; the bus stop; the month-old relationship; Norvig's "big
data" contrasted with the "small data" of daily life.
Strength of Support: Strong as a framing; the specific methods are justified in what follows.
```

```
Claim: Backward inference requires forward reasoning from hypotheticals (the likelihood).
Type: Theoretical (Bayes's insight)
Evidence Provided: The three-winning-tickets calculation (100% / 1-in-8 / 1-in-a-billion under
all-win / half / 1-in-1000 hypotheses).
Strength of Support: Strong. A clean, checkable derivation.
```

```
Claim: Laplace's Law gives the estimate (w+1)/(n+2) with no prior knowledge.
Type: Theoretical (proved)
Evidence Provided: One win → 2/3; three wins → 4/5; five of ten → 50%. Footnote: a single losing
Powerball ticket → 1/3 chance next, which "faithfully reflects the odds in a raffle where you come in
knowing nothing at all."
Strength of Support: Strong. A named, proved result with worked cases.
```

```
Claim: Bayes's Rule combines prior and evidence by multiplying their probabilities, and always needs
a prior.
Type: Theoretical
Evidence Provided: The two-coin (2× two-headed) and nine-plus-one-coin (4.5× fair) examples; you can't
answer "is this a fair coin?" with no sense of what's in the bag.
Strength of Support: Strong. Worked examples plus the necessity argument.
```

```
Claim: The Copernican Principle — predict something lasts as long as it already has — is exactly Bayes's
Rule with an uninformative prior.
Type: Theoretical
Evidence Provided: Berlin Wall (8 → predicted 8 more, actually 20); the derivation via ruling out
spans < 8 years and treating very long spans as improbable coincidences; the uninformative prior is
itself a power-law.
Strength of Support: Strong. The reduction to Bayes is the chapter's key unification.
```

```
Claim: The Copernican Principle is reasonable when you know nothing and wrong when you know something.
Type: Interpretive
Evidence Provided: Works for the Berlin Wall (unknown timescale); fails absurdly for a 90-year-old
(→180) or 6-year-old (→12) because we have rich lifespan priors.
Strength of Support: Strong. The failure cases are precisely where informative priors exist.
```

```
Claim: The Copernican / doubling method has real historical precedents that worked.
Type: Empirical / Historical
Evidence Provided: Harold Jeffreys's tramcar estimate (double the serial number); the WWII German tank
problem — serial-number math predicted 246 tanks/month vs. 1,400 from risky aerial reconnaissance;
German records showed the true figure was 245.
Strength of Support: Strong. A striking, verified success (245 vs. the math's 246).
```

```
Claim: The world splits into things that cluster around a natural value (normal) and things that don't
(power-law/scale-free).
Type: Theoretical / Empirical
Evidence Provided: Normal — US male lifespan ~76, plus height, weight, blood pressure, temperature,
fruit diameter. Power-law — US town population averages 8,226 but far more are smaller (a few enormous);
movie grosses (Titanic); wealth and income (mean $55,688; two-thirds below the mean; top 1% ~10× the
mean; top 1% of the 1% ~10× that).
Strength of Support: Strong. Multiple concrete, quantified examples.
```

```
Claim: Preferential attachment ("the rich get richer") reliably produces power-law distributions.
Type: Theoretical / Empirical
Evidence Provided: Popular websites gain more links; followed celebrities gain more fans; prestigious
firms gain more clients; big cities gain more residents.
Strength of Support: Strong as a mechanism; stated as one of the surest ways to produce a power law.
```

```
Claim: Each distribution gives a different optimal prediction rule.
Type: Theoretical
Evidence Provided: Power-law → Multiplicative (×2 uninformative, ×1.4 movies: $6M→$8.4M, $90M→$126M);
normal → Average (90yo→94, 6yo→77); Erlang → Additive (constant amount more).
Strength of Support: Strong. Each rule is derived from applying Bayes's Rule to the corresponding
distribution.
```

```
Claim: Memoryless (Erlang) distributions have no right time to quit, which partly explains gambling
addiction.
Type: Interpretive
Evidence Provided: Blackjack "twenty more hands" never changes; a memoryless game offers no tipping
point to cut losses and no reward for holding on ("The Gambler" has no answer).
Strength of Support: Moderate to Strong. The math is exact; the addiction link is an interpretive
extension.
```

```
Claim: Knowing the distribution can change a life-or-death forecast (Gould's cancer).
Type: Interpretive (with a real case)
Evidence Provided: Stephen Jay Gould's cancer had a median survival of 8 months, but the distribution
was strongly right-skewed (power-law-like) with a long tail; the Multiplicative Rule implied the longer
he lived, the longer he'd likely live. He lived 20 more years.
Strength of Support: Strong as an illustration; a single case, but a vivid and consequential one.
```

```
Claim: People are remarkably good intuitive Bayesians because "small data is big data in disguise."
Type: Empirical (attributed to Griffiths & Tenenbaum)
Evidence Provided: In their experiment, people predicted lifespans, movie grosses, and congressional
tenure from a single data point, and their predictions were extremely close to Bayes's Rule applied to
real-world data — implicitly using the right rule for each distribution.
Strength of Support: Strong within the chapter's presentation; sample sizes/effect sizes not given.
```

```
Claim: Good predictions require good priors — where priors are poor, predictions fail.
Type: Empirical
Evidence Provided: People systematically diverged from Bayes only for pharaohs' reigns (an Erlang
distribution nobody has everyday exposure to); hold times were reverse-engineered as multiplicative
(~1.33× so far), implying a power-law prior.
Strength of Support: Strong. The single failure case cleanly isolates the role of priors.
```

```
Claim: Resisting temptation may be a matter of expectations, not just willpower.
Type: Interpretive / Empirical
Evidence Provided: McGuire & Kable — if adults' return time is power-law, cutting losses is rational
(the Multiplicative Rule says a long wait predicts an even longer one), so the "irrational" in-between
kids may be reasoning correctly. The Rochester study — kids who first experienced an unreliable
experimenter (broken art-supply promise) were more likely to eat the marshmallow.
Strength of Support: Moderate to Strong. The Rochester manipulation is genuinely causal about
reliability; the reinterpretation of Mischel is an inference.
```

```
Claim: Media distorts priors because language reports the interesting/rare, not the frequent.
Type: Interpretive / Empirical
Evidence Provided: You've seen ~as many crashed planes as cars, but the cars were next to you and the
planes were on another continent via TV/internet; US commercial-plane-crash deaths since 2000 wouldn't
half-fill Carnegie Hall, while car-crash deaths exceed the population of Wyoming; Glassner — 1990s
murder rate down 20% while news gun violence up 600%.
Strength of Support: Strong. Concrete, quantified asymmetries; the "turn off the news" prescription is
the authors' inference.
```

## 4. Frameworks, Models, and Mental Models

```
Name: Bayesian Inference (Reason Backward via Forward Likelihood)
Description: Infer hidden causes from observed effects by computing how likely the data is under each
hypothesis, then weighting by prior belief.
Components: Hypotheses; likelihood (forward probability of the data); prior; posterior ∝ prior ×
likelihood.
How It Works: Compare hypotheses by how well each predicts what you saw, scaled by how plausible each
was to begin with.
When It Is Useful: Any prediction under uncertainty with limited data — the "small data" of daily life.
Limitations: Requires a prior; garbage priors give garbage predictions.
```

```
Name: Laplace's Law — (w+1)/(n+2)
Description: A single-number success-rate estimate under an uninformative prior.
Components: w wins, n attempts; the +1/+2 "smoothing."
How It Works: Distills Bayes's infinite hypotheses into one expectation via calculus; pulls estimates
away from the 0% and 100% extremes that raw counts give on tiny samples.
When It Is Useful: Estimating a probability from a short history (bus lateness, a team's win rate) — and
it scales seamlessly to millions of data points.
Limitations: Its simplest form *is* the uniform-prior assumption (1% as likely as 10% as 50% as 100%),
which is often not true. This makes Laplace's Law and the Copernican Principle the chapter's two
uninformative-prior methods — both are wrong exactly when you actually hold an informative prior.
```

```
Name: The Copernican Principle / Doubling
Description: With no other information, predict the future duration equals the past duration.
Components: A single data point (current age t); the assumption you arrived at a non-special moment.
How It Works: On average you're halfway through, so total ≈ 2t, future ≈ t. It is Bayes's Rule with an
uninformative (power-law) prior. The derivation has two parts: the observed age *rules out* any
hypothesis predicting a shorter lifespan (just as the first tails rules out a two-headed coin), while
enormously long spans survive but are improbable coincidences (it would be a big coincidence to bump
into a million-year wall right at its start) — so the middle predictions dominate.
When It Is Useful: When you genuinely know nothing about the timescale (a foreign bus; an unfamiliar
artifact; the German tank problem).
Limitations: Absurd where you have informative priors (human lifespans); a single point gives only a
rough scale.
```

```
Name: The Three Prediction Rules
Description: Match the rule to the prior's distribution shape.
Components: Multiplicative (power-law: predict ×constant); Average (normal: predict the natural
average); Additive (Erlang/memoryless: predict +constant).
How It Works: Each falls directly out of applying Bayes's Rule to that distribution; they also dictate
how *surprised* to be (power-law events maximally surprising right before they happen; normal events
surprising only when early; Erlang never surprising).
When It Is Useful: Everyday forecasting — box office, lifespans, waits, tenures, poems, gambling.
Limitations: You must first correctly identify the distribution; the wrong shape gives the wrong rule.
```

```
Name: Preferential Attachment
Description: A generative mechanism where having more of something makes you likelier to gain more.
Components: An advantage that compounds (links, fans, clients, residents, wealth).
How It Works: Feedback concentrates the quantity, producing a power-law (scale-free) distribution.
When It Is Useful: Recognizing when a quantity will be power-law (and thus needs the Multiplicative
Rule).
Limitations: One of several routes to a power law, not the only one.
```

## 5. Research and Evidence

```
Study / Research: Bayes's essay on inverse probability
Researchers: Reverend Thomas Bayes; posthumously read to the Royal Society by his friend Richard Price
Year: Written ~1746–49; Bayes died 1761; Price presented it thereafter
Research Question: Given only the blanks and prizes you observe, what can you reasonably infer about a
lottery's composition?
Method: Reasoning backward via forward likelihoods.
Key Finding: You can rank hypotheses by how likely they render your observations; Price established that
a single winning ticket implies a 75% chance that at least half the tickets win.
How the Author Uses It: The origin of Bayesian inference; the "reasoning backward" foundation.
Important Limitations: It compares hypotheses but doesn't distill them into a single estimate — it
leaves you reasoning about "probabilities *of* probabilities" (Price's answer is a "75% metaprobability
of a 50% or greater chance"), which "can get a bit head-spinning" and still can't answer "what do you
think the odds *actually* are?" That gap is exactly what Laplace later filled. Bayes abandoned the paper
unpublished.
Replication or Controversy Mentioned: Bayes's own biography is "ironically uncertain" (birth 1701 or
1702; paper 1746–49). He had defended Newton's calculus (1736) against Bishop Berkeley; elected FRS
1742.
```

```
Study / Research: Laplace's Law / "Treatise on the Probability of the Causes of Events"
Researchers: Pierre-Simon Laplace
Year: 1774 (unaware of Bayes); later the "Philosophical Essay on Probabilities"
Research Question: How to distill infinitely many hypotheses into a single estimate (Bayes/Price had
left you unable to state one), and infer causes from effects.
Method: Calculus (which Bayes had earlier defended).
Key Finding: The (w+1)/(n+2) estimate; a way to weight some hypotheses as more probable than others.
Also applied his approach to show male infants are slightly more likely than female. His *Philosophical
Essay on Probabilities* is "arguably the first book about probability for a general audience and still
one of the best," applying the theory to law, the sciences, and everyday life.
How the Author Uses It: The practical completion of Bayes; the "first simple rule of thumb for small
data."
Important Limitations: Simplest form assumes a uniform prior.
Replication or Controversy Mentioned: None; the "Philosophical Essay" is called arguably the first
popular book on probability and still one of the best.
```

```
Study / Research: The WWII German tank problem
Researchers: Allied statisticians (unnamed); precedent noted in Harold Jeffreys's tramcar work
Year: World War II
Research Question: How many tanks is Germany producing?
Method: Statistical estimation from captured tanks' serial numbers vs. aerial reconnaissance.
Key Finding: Serial-number math predicted 246 tanks/month; risky aerial recon suggested ~1,400; postwar
German records showed the true figure was 245.
How the Author Uses It: A dramatic real-world validation of the doubling/Copernican family of estimates
from minimal data.
Important Limitations: A single historical instance.
Replication or Controversy Mentioned: Jeffreys had independently reached "double the serial number" for
tramcars.
```

```
Study / Research: The Erlang distribution
Researchers: Agner Krarup Erlang (Danish mathematician, Copenhagen Telephone Company)
Year: Early twentieth century
Research Question: How much time passes between successive independent events (phone calls on a network)?
Method: Formalizing the spread of intervals between independent events.
Key Finding: The Erlang distribution — a winglike curve, tail falling off faster than a power-law but
slower than a normal — models memoryless waits.
How the Author Uses It: The third distribution and the Additive Rule; later used for traffic, internet
infrastructure, radioactive decay (Geiger-counter ticks), and House of Representatives tenure.
Important Limitations: Applies where events are genuinely independent/memoryless.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Single-data-point prediction across everyday domains
Researchers: Tom Griffiths (this book's co-author, "Tom") and Josh Tenenbaum (MIT) — first-person
authorial work from Griffiths's grad-school years, not a neutral third-party citation
Year: Not specified (Griffiths's grad-school work)
Research Question: Do people's intuitive predictions match Bayesian predictions from real-world data?
Method: Participants predicted quantities (human lifespans, movie grosses, congressional tenure, hold
times, pharaohs' reigns) from a single data point; predictions compared to Bayes's Rule applied to
actual distributions.
Key Finding: Predictions were extremely close to Bayes's Rule and implicitly used the correct rule per
distribution — except pharaohs' reigns (Erlang, unfamiliar), where they faltered. Hold times were
reverse-engineered as multiplicative (~1.33×), implying a power-law prior.
How the Author Uses It: Evidence that "small data is big data in disguise" and that priors can be
reverse-engineered from human predictions.
Important Limitations: Sample sizes/effect sizes not given; the pharaoh failure is the key control.
Replication or Controversy Mentioned: Noted as part of a decade of work identifying human priors from
vision to language.
```

```
Study / Research: The Stanford marshmallow test and its reinterpretation
Researchers: Walter Mischel (original, Stanford, early 1970s); Joe McGuire & Joe Kable (UPenn,
reinterpretation); a University of Rochester team (reliability manipulation)
Year: Original early 1970s; follow-ups decades later
Research Question: What underlies the ability to delay gratification, and what does it predict?
Method: Children chose one treat now or two after a wait (~15 min); a decades-later follow-up tracked
outcomes; the Rochester study first exposed children to a reliable or unreliable experimenter (an
art-supplies promise kept or broken) before the marshmallow test.
Key Finding: Waiters were later more successful (higher SAT scores). But if adults' return time is
power-law, cutting losses is rational, so waiting may reflect expectations, not just willpower; and kids
who first met an *unreliable* experimenter were more likely to eat the marshmallow.
How the Author Uses It: To reframe self-control as (partly) calibrated expectations shaped by whether
one's environment is dependable.
Important Limitations: The willpower vs. expectations accounts aren't fully separated; the SAT
correlation is not decomposed.
Replication or Controversy Mentioned: The Rochester manipulation is presented as revising the classic
willpower interpretation.
```

```
Study / Research: Media frequency vs. real frequency
Researchers: Sociologist Barry Glassner (cited)
Year: 1990s data
Research Question: Does media coverage track real-world frequency?
Method: Comparison of crime statistics with news coverage.
Key Finding: US murder rate fell ~20% across the 1990s while gun violence on the news rose ~600%.
How the Author Uses It: Evidence that media systematically distorts priors, motivating "turn off the
news."
Important Limitations: A single cited comparison; the causal claim about priors is the authors'.
Replication or Controversy Mentioned: None identified.
```

## 6. Experiments

```
Experiment Name: Griffiths & Tenenbaum single-point prediction
Setup: Predict an everyday quantity from one data point (e.g., "a movie has grossed $X so far — what's
its total?").
Participants: Human participants (number not specified).
Procedure: Across domains with different real-world distributions (power-law grosses, normal lifespans,
Erlang tenures), collect single-point predictions and compare to Bayes's Rule on the true distributions.
Result: Predictions closely matched Bayesian optima and implicitly switched rules by domain — except
pharaohs' reigns, where unfamiliarity produced poor priors and poor predictions.
Interpretation: People carry accurate, unconsciously absorbed priors; "small data is big data in
disguise."
What It Demonstrates: Human intuition approximates Bayesian inference where priors are good, and fails
where they aren't.
Potential Alternative Explanation: Participants might use simple learned heuristics that coincide with
Bayes in familiar domains without representing full distributions; the match may be domain-specific
memory rather than probabilistic reasoning.
```

```
Experiment Name: The Rochester reliability-before-marshmallow study
Setup: An art project precedes the marshmallow test; an experimenter promises better supplies.
Participants: Preschool children, split into two groups.
Procedure: For one group the experimenter reliably returns with the promised supplies; for the other
she returns with only apologies. Then the standard marshmallow test.
Result: Children who had experienced an unreliable experimenter were more likely to eat the marshmallow
before she returned.
Interpretation: Marshmallow "failure" may reflect a rational prior that adults are undependable, not a
willpower deficit.
What It Demonstrates: Prior experience of reliability causally shifts delay-of-gratification behavior.
Potential Alternative Explanation: The manipulation could induce distrust or mood effects rather than a
recalibrated temporal prior; short-term framing rather than a durable belief about adults.
```

## 7. Cases and Stories

```
Case Title: J. Richard Gott at the Berlin Wall
People / Organization: J. Richard Gott III (later Princeton astrophysicist)
Context: In 1969, standing before the eight-year-old Berlin Wall, he asked "Where am I?" in the wall's
lifetime.
What Happened: Assuming his arrival wasn't special (on average, halfway through), he predicted the wall
would last about eight more years. It lasted twenty. He named this the Copernican Principle and
published it in Nature, drawing a "flurry of critical correspondence."
Outcome: A single-data-point prediction method — and a lens on when such predictions work.
Concept Illustrated: The Copernican Principle; Bayes with an uninformative prior.
Why This Case Is Useful: A vivid, historically resonant hook that makes single-point prediction
concrete and testable.
Potential for Reuse: High
```

```
Case Title: Reverend Bayes and the raffle
People / Organization: Thomas Bayes (Presbyterian minister, Tunbridge Wells); Richard Price
Context: The 18th-century problem of inferring a lottery's odds from what you observe.
What Happened: Bayes worked backward from observed wins/losses to the probable ticket pool by reasoning
forward from hypotheticals; three-in-a-row wins are 8× likelier if all tickets win than if half do. He
abandoned the paper; Price found it after Bayes's 1761 death ("has great merit, and deserves to be
preserved") and established that one winning ticket → 75% chance ≥half win. Bayes's own biography is
"ironically uncertain."
Outcome: The birth of Bayesian inference — with the ironic twist that a man who founded reasoning under
uncertainty has an uncertain life story, and that the heavy lifting was finished by Laplace.
Concept Illustrated: Reasoning backward; likelihood.
Why This Case Is Useful: A charming origin story (a gambling-obsessed clergyman) with a built-in irony.
Potential for Reuse: High
```

```
Case Title: The German tank problem
People / Organization: Allied statisticians in WWII; precedent by Harold Jeffreys (tramcars)
Context: Estimating German tank production from captured serial numbers.
What Happened: Serial-number math predicted 246 tanks/month; risky aerial reconnaissance suggested
~1,400; postwar records revealed the true figure was 245. Jeffreys had earlier reached "double the
serial number" for counting a city's tramcars.
Outcome: A minimal-data statistical estimate beat expensive, dangerous reconnaissance almost exactly.
Concept Illustrated: The Copernican/doubling family; the power of good inference from tiny data.
Why This Case Is Useful: A dramatic, verified real-world win (245 vs. 246) for statistical reasoning.
Potential for Reuse: High
```

```
Case Title: Stephen Jay Gould's cancer
People / Organization: Stephen Jay Gould (Harvard biologist and science popularizer)
Context: Diagnosed with a cancer whose median survival was eight months.
What Happened: Rather than despair, Gould read further and found the survival distribution was strongly
right-skewed (power-law-like), with a long tail extending years past the eight-month median. The
Multiplicative Rule implied the longer he lived, the longer he'd likely live. "I saw no reason why I
shouldn't be in that small tail, and I breathed a very long sigh of relief." He lived twenty more years.
Outcome: Knowing the distribution's shape, not just its median, transformed a death sentence into hope.
Concept Illustrated: Power-law vs. normal; the Multiplicative Rule; median ≠ distribution.
Why This Case Is Useful: Emotionally powerful, true, and it makes the abstract distinction between
median and distribution shape a matter of life and death.
Potential for Reuse: High
```

```
Case Title: Dean Young and the fourth section
People / Organization: Poet Dean Young
Context: Listening to a poem read in numbered sections.
What Happened: Young's heart sinks when the reader announces "section four" — more than three parts and
"all bets are off." Analysis shows poems, unlike movie running times (normal, ~100 min), follow closer
to a power-law: most short, a few epic. So his dread is "perfectly Bayesian."
Outcome: A power-law intuition, correctly applied to poetry length.
Concept Illustrated: Power-law vs. normal; the Multiplicative Rule (the longer it's gone, the longer to
expect).
Why This Case Is Useful: A charming, low-stakes illustration that the same math governs poems and
plane crashes.
Potential for Reuse: Medium
```

```
Case Title: The card shark's "twenty more hands"
People / Organization: A hypothetical casino card player
Context: Predicting when a memoryless event (a blackjack, ~20-to-1) will occur.
What Happened: He tells his spouse "I'll be done in about twenty more hands"; twenty unlucky hands
later, his answer is unchanged: "about twenty more hands." It sounds like memory loss, but it's exactly
correct — the wait is memoryless.
Outcome: The Additive Rule made vivid; the same prediction regardless of history.
Concept Illustrated: Erlang / memorylessness; why "just five more minutes" can be literally correct.
Why This Case Is Useful: A funny, memorable illustration of memorylessness and the Additive Rule.
Potential for Reuse: High
```

```
Case Title: Planes vs. cars (and the news)
People / Organization: The authors; sociologist Barry Glassner
Context: Why our fears don't track real risk.
What Happened: You've likely seen roughly as many crashed planes as cars — but the cars were beside you
and the planes were on another continent, delivered via TV/internet. US commercial-plane-crash deaths
since 2000 wouldn't half-fill Carnegie Hall; car-crash deaths exceed Wyoming's entire population. In the
1990s the US murder rate fell 20% while news gun violence rose 600%.
Outcome: Media frequency doesn't track world frequency, distorting priors; hence "turn off the news."
Concept Illustrated: Protecting your priors; language/media distortion.
Why This Case Is Useful: Quantified, counterintuitive, and immediately actionable; the chapter's
closing punch.
Potential for Reuse: High
```

```
Case Title: Little Annie and the sunrise
People / Organization: "Annie" (chapter epigraph); Laplace's Law
Context: A child's certainty that the sun will rise.
What Happened: The epigraph — "The sun'll come out tomorrow. You can bet your bottom dollar there'll be
sun" — is vindicated by Laplace's Law: with the Earth having seen ~1.6 trillion consecutive sunrises,
the chance of another is all but indistinguishable from 100%.
Outcome: A childlike faith turns out to be rigorously justified.
Concept Illustrated: Laplace's Law; the large-n behavior of (w+1)/(n+2).
Why This Case Is Useful: A warm, closed-loop payoff (epigraph → math) and the friendliest possible
illustration of Laplace's Law.
Potential for Reuse: High
```

```
Case Title: "7 days since the last accident"
People / Organization: The authors (a construction-site example)
Context: A common industrial safety sign.
What Happened: The Copernican Principle reads "7 days since the last industrial accident" as implying
another accident is likely within roughly 7 days — so "we might want to stay away, unless it's a
particularly short job we plan to do."
Outcome: A darkly funny, immediately graspable Copernican application to everyday signage.
Concept Illustrated: The Copernican Principle / doubling from a single data point.
Why This Case Is Useful: A memorable, slightly subversive hook that makes the doubling rule stick.
Potential for Reuse: High
```

```
Case Title: The bus-stop sign that shows the past
People / Organization: The authors (a transit-policy suggestion)
Context: Cities that can't afford real-time "next bus" prediction signs.
What Happened: The Copernican Principle suggests a cheap alternative — simply display how long since the
*previous* bus arrived, which offers a substantial hint about when the next one will come.
Outcome: A concrete public-infrastructure application of single-data-point prediction.
Concept Illustrated: The Copernican Principle as usable policy.
Why This Case Is Useful: Turns an abstract rule into a real, cheap civic design; shows the method's
practical reach.
Potential for Reuse: Medium
```

## 8. Best Teaching Examples

```
Concept: Likelihood / reasoning backward
Example: Three winning tickets in a row is 100% likely if all tickets win, 1/8 if half do, one-in-a-
billion if 1/1000 do — so all-win is exactly 8× likelier than half-win.
Why It Works: Turns an abstract "infer the cause" into three concrete multiplications you can check, and
the "exactly 8×" makes the quantification tangible.
Possible Alternative Domain: Mathematics
```

```
Concept: Bayes's Rule = prior × evidence
Example: Nine fair coins and one two-headed; a drawn coin shows heads. A fair coin is half as likely to
show heads but 9× likelier to have been drawn → 4.5× likelier it's fair.
Why It Works: Forces you to multiply two separate considerations, showing precisely what a prior adds
to evidence.
Possible Alternative Domain: Everyday Life
```

```
Concept: Laplace's Law vs. naive counting
Example: One win in one try is not 100% — it's 2/3. A single losing Powerball ticket leaves a 1/3
chance next time.
Why It Works: A one-line correction to the seductive but wrong "1-for-1 = 100%," memorable via the
lottery.
Possible Alternative Domain: Everyday Life
```

```
Concept: The Copernican Principle
Example: The Berlin Wall at eight years old → predict eight more (it lasted twenty); a 90-year-old →
180, which is absurd because we know human lifespans.
Why It Works: One rule, one success and one failure side by side, teaching both the method and its
scope in a sentence.
Possible Alternative Domain: Everyday Life
```

```
Concept: Distribution shape dictates the rule
Example: A movie that's grossed $6M → guess $8.4M (power-law, ×1.4); a 90-year-old → 94 (normal,
average); a blackjack in "twenty more hands," always (Erlang, additive).
Why It Works: Three domains, three rules, one underlying principle — the cleanest demonstration that
the prior's shape is everything.
Possible Alternative Domain: Business
```

```
Concept: Small data is big data in disguise
Example: You can predict a movie's total gross from one number because you carry an accurate prior
about box office — but you fail on pharaohs' reigns because you have no such prior.
Why It Works: The single failure case (pharaohs) isolates exactly what makes the successes work.
Possible Alternative Domain: Psychology
```

```
Concept: Protect your priors
Example: You've seen as many crashed planes as cars, but the planes came via screens from another
continent; plane deaths since 2000 wouldn't half-fill Carnegie Hall, car deaths exceed Wyoming.
Why It Works: A vivid, quantified asymmetry that makes an abstract point about media and priors
visceral and actionable.
Possible Alternative Domain: Psychology
```

## 9. Counterintuitive Insights

```
Insight: You can make a rational prediction from a single data point.
Common Belief: Prediction needs lots of data; one point is "mathematically laughable."
Author's Argument: With a prior — even an uninformative one — Bayes's Rule turns one observation into a
principled estimate (the Copernican doubling).
Evidence: The Berlin Wall; the German tank problem (245 vs. the math's 246).
Why It Is Surprising: It legitimizes exactly the everyday inferences (buses, relationships) that seem
statistically unfounded.
```

```
Insight: One win in one try means about 2/3, not 100%.
Common Belief: If it worked the one time you tried, the rate is 100%.
Author's Argument: Laplace's Law, (w+1)/(n+2), pulls tiny-sample estimates off the extremes; a single
losing lottery ticket still leaves a 1/3 chance.
Evidence: The Laplace derivation and Powerball footnote.
Why It Is Surprising: It corrects the near-universal error of over-reading small samples.
```

```
Insight: Predicting from ignorance puts you exactly at the center.
Common Belief: The Copernican move (nothing special about us) should make us feel un-central.
Author's Argument: Assuming your arrival time isn't special implies you're on average at the midpoint —
so "nothing special" ironically lands you at the very center of a thing's lifetime.
Evidence: The halfway-point derivation; the chapter's own footnoted irony.
Why It Is Surprising: The un-special assumption produces a maximally central conclusion.
```

```
Insight: The longer a power-law thing has lasted, the longer it will last.
Common Belief: The longer something's gone on, the more "overdue" its end.
Author's Argument: In a power-law, the past duration sets the scale, so more elapsed time predicts more
to come — the opposite of the normal-distribution intuition.
Evidence: The Multiplicative Rule; Gould's cancer; poems; institutions "always stunning when they
collapse."
Why It Is Surprising: It inverts the gambler's-fallacy-style intuition, and does so only for one
distribution family.
```

```
Insight: Some waits have no right time to quit.
Common Belief: There's always an optimal moment to cut your losses or hold on.
Author's Argument: For memoryless (Erlang) distributions the odds never change, so there's no tipping
point and no reward for persistence — which partly explains gambling's grip.
Evidence: Blackjack "twenty more hands"; "The Gambler" has no answer for a memoryless game.
Why It Is Surprising: It shows a whole class of situations where the beloved "know when to walk away"
advice is simply undefined.
Gambling contrast (the clearest illustration of why identifying the distribution matters): if a
roulette wait were *normal*, the Average Rule says your number is coming any second — press on to the
next win, then quit. If it were *power-law*, the Multiplicative Rule says wins cluster (keep playing
after a win) but droughts lengthen (give up after a losing streak). If it is *memoryless*, the Additive
Rule says nothing ever changes — no reward for holding on, no tipping point to cut losses.
```

```
Insight: Self-control might be calibrated expectation, not (only) willpower.
Common Belief: Delaying gratification is a fixed trait of willpower (the marshmallow test).
Author's Argument: If adults are unreliable (a power-law wait), eating the marshmallow is rational; kids
primed with an unreliable experimenter caved more. The chapter hedges carefully: resisting temptation
"may be, at least in part, a matter of expectations rather than willpower" — it does not claim willpower
plays no role, only that expectations also matter and the picture is "perhaps more poignant."
Evidence: McGuire & Kable; the Rochester study.
Why It Is Surprising: It reframes a famous willpower result as partly a rational response to a learned
prior about whether adults keep promises.
```

```
Insight: To predict the world accurately, consume less about it.
Common Belief: More information (news) makes you better informed.
Author's Argument: Media reports the rare/interesting, so it corrupts the frequency priors good
prediction depends on; "protect your priors" may mean turning off the news.
Evidence: Planes vs. cars; murder down 20% while news gun violence up 600%.
Why It Is Surprising: Being well-informed can make your intuitive predictions worse.
```

## 10. Unique or Unusual Ideas

```
Idea: An uninformative prior is itself a power-law distribution.
Why It Seems Unique: It quietly reveals that "assuming nothing" is not neutral — it commits you to a
specific, scale-free shape and thus to the Multiplicative Rule.
Potential Connection to Other Topics: Priors in machine learning; regularization; the impossibility of
truly assumption-free inference.
```

```
Idea: "Small data is big data in disguise."
Why It Seems Unique: It relocates human predictive skill from data volume to prior richness, reframing
intuition as approximate Bayesian inference.
Potential Connection to Other Topics: Few-shot learning; transfer learning; ecological rationality;
expertise.
```

```
Idea: Your predictions reverse-engineer your experience.
Why It Seems Unique: Because good predictions require good priors, what you forecast betrays what you've
lived — turning prediction into a diagnostic of a person's world.
Potential Connection to Other Topics: Cognitive science of priors (vision to language); assessing
someone's environment from their expectations; the Rochester reliability result.
```

```
Idea: Each distribution has a distinct "surprise signature."
Why It Seems Unique: Beyond a prediction rule, each shape tells you when to be surprised — power-law
events are maximally surprising just before they happen; normal events only when early; Erlang never.
Potential Connection to Other Topics: Anomaly detection; risk perception; why institutional collapses
shock us.
```

```
Idea: Language broke our priors.
Why It Seems Unique: It argues that experience is always sampled at true frequency, but *talking* about
experience over-samples the rare — so communication itself, amplified by mass media, systematically
miscalibrates a species' priors.
Potential Connection to Other Topics: Availability heuristic; media effects; the evolution of language;
misinformation.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: The Copernican Principle is "reasonable" and "completely wrong" depending on the case.
Author's Position: It works with an uninformative prior (unknown timescale) and fails where we have
informative priors (lifespans).
Possible Counterargument: This makes the "principle" less a prediction method than a diagnostic of your
own ignorance — its validity is entirely inherited from whether the uninformative prior happens to match
reality, which you often can't know in advance.
What Evidence Would Help Resolve It: A way to tell, before predicting, whether your situation is
genuinely uninformative or you're neglecting a prior you actually hold.
```

```
Issue: "People are remarkably good intuitive Bayesians" vs. the availability heuristic and biased
priors.
Author's Position: Human single-point predictions closely match Bayes because our absorbed priors are
rich and accurate.
Possible Counterargument: The chapter's own closing section argues media corrupts priors badly (plane
vs. car), and the behavioral-economics tradition (Kahneman/Tversky) documents systematic base-rate
neglect. The "good Bayesian" claim holds for domains with accurate absorbed priors and breaks exactly
where the chapter says priors are distorted — a tension it notes but doesn't fully reconcile.
What Evidence Would Help Resolve It: When do absorbed priors track reality vs. media, and how often is
each regime the relevant one?
```

```
Issue: The marshmallow reinterpretation risks over-rationalizing.
Author's Position: Eating the marshmallow can be a rational response to a power-law/unreliable prior,
not a willpower failure.
Possible Counterargument: The willpower and expectations accounts aren't cleanly separated; the SAT
correlation could still reflect self-control, environment, or both, and the chapter presents the
expectations story as "perhaps more poignant" without adjudicating. Both mechanisms likely operate.
What Evidence Would Help Resolve It: Designs that hold reliability constant while varying willpower
training, and vice versa.
```

```
Issue: Laplace's Law assumes a uniform prior that is "often not true."
Author's Position: (w+1)/(n+2) is the right estimate when you know nothing.
Possible Counterargument: The chapter also stresses that a blank slate is rare and that good priors
matter most — so the very rule offered as the "first rule of thumb" rests on the assumption the chapter
elsewhere warns against. When you do have a prior, Laplace's Law is the wrong tool.
What Evidence Would Help Resolve It: Guidance on recognizing when you're genuinely prior-free vs. when
you should use an informative prior.
```

```
Issue: "Turn off the news" as a prescription.
Author's Position: Media distorts frequency priors, so protecting them may mean turning off the news.
Possible Counterargument: News also conveys genuinely important low-frequency information (a pandemic, a
policy change) that priors *should* update on; wholesale avoidance could miss rare-but-consequential
signals. The chapter optimizes for calibrated frequency priors, not for catching the important tail.
What Evidence Would Help Resolve It: Whether selective/aggregate consumption can preserve calibration
while retaining important signals.
```

```
Issue: The distribution must be identified first, but identification is itself the hard part.
Author's Position: Match the rule (Multiplicative/Average/Additive) to the distribution.
Possible Counterargument: The chapter shows people fail exactly when they misjudge the distribution
(pharaohs); yet it offers no general method for telling normal from power-law from Erlang in a novel
situation — the crux of prediction is assumed rather than solved.
What Evidence Would Help Resolve It: Cues or heuristics for classifying an unfamiliar quantity's
distribution before predicting.
```

## 12. Quotable Ideas

```
Paraphrase (short): "All human knowledge is uncertain, inexact, and partial." (Bertrand Russell,
epigraph)
Why the Idea Matters: Frames prediction as the universal condition — we always reason from incomplete
data.
Source Location: Chapter epigraph (PDF p. 168).
```

```
Paraphrase (short): To reason backward from what you see to its cause, first reason forward from
hypotheticals.
Why the Idea Matters: Bayes's foundational insight and the whole chapter's method in one line.
Source Location: "Reasoning Backward with the Reverend Bayes" (PDF pp. 170–171).
```

```
Paraphrase (short): One win in one try means about two-thirds, not certainty.
Why the Idea Matters: Laplace's Law as a corrective to over-reading small samples.
Source Location: "Laplace's Law" (PDF p. 172).
```

```
Paraphrase (short): Bayes's Rule combines belief and evidence by multiplying — and it always needs a
prior, even a guess.
Why the Idea Matters: The operational core, and the reason prediction is never assumption-free.
Source Location: "Bayes's Rule and Prior Beliefs" (PDF p. 174).
```

```
Paraphrase (short): With no other knowledge, predict something will last as long as it already has.
Why the Idea Matters: The Copernican Principle — a full prediction algorithm from one data point.
Source Location: "The Copernican Principle" (PDF p. 176).
```

```
Paraphrase (short): The richer the prior you bring to Bayes's Rule, the more useful the prediction you
get out.
Why the Idea Matters: The chapter's thesis that priors, not data volume, drive prediction quality.
Source Location: "Bayes Meets Copernicus" (PDF p. 179).
```

```
Paraphrase (short): The longer something normal has gone on, the sooner it must end; the longer
something power-law has gone on, the longer it will keep going.
Why the Idea Matters: The single sentence that distinguishes the two most important distributions'
behavior.
Source Location: "… and Their Prediction Rules" (PDF p. 182).
```

```
Paraphrase (short): For a memoryless distribution there is no right time to quit — which may explain
why such games are addictive.
Why the Idea Matters: A precise account of a familiar trap; "The Gambler" has no answer here.
Source Location: "… and Their Prediction Rules" (PDF pp. 185–186).
```

```
Paraphrase (short): Small data is big data in disguise — we predict well from little because our priors
are rich.
Why the Idea Matters: The chapter's most memorable reframing of human intuition.
Source Location: "Small Data and the Mind" (PDF p. 187).
```

```
Paraphrase (short): Our judgments betray our expectations, and our expectations betray our experience.
Why the Idea Matters: Prediction as a mirror of a person's world.
Source Location: "Small Data and the Mind" (PDF p. 188).
```

```
Paraphrase (short): Resisting temptation may be less about willpower than about whether you expect
adults to keep their word.
Why the Idea Matters: The reinterpretation of the marshmallow test.
Source Location: "What Our Predictions Tell Us About Ourselves" (PDF pp. 189–190).
```

```
Paraphrase (short): To be a good intuitive Bayesian, protect your priors — which may mean turning off
the news.
Why the Idea Matters: The chapter's closing prescription.
Source Location: "Priors in the Age of Mechanical Reproduction" (PDF p. 192).
```

```
Paraphrase (short): "The sun'll come out tomorrow. You can bet your bottom dollar there'll be sun."
(Annie, epigraph)
Why the Idea Matters: A childlike certainty the chapter proves rigorously justified via Laplace's Law
(~1.6 trillion sunrises → ~100%) — the friendliest closed loop in the book.
Source Location: Chapter epigraph (PDF p. 168), paid off at "Laplace's Law" (PDF p. 172).
```

```
Paraphrase (short): If we trust past experience as the standard of future judgement, those arguments
can only be probable. (David Hume, epigraph)
Why the Idea Matters: The problem of induction — the philosophical question Bayes's Rule answers.
Source Location: Epigraph to "Reasoning Backward" (PDF p. 169).
```

```
Paraphrase (short): All these suppositions are consistent and conceivable — why prefer one, no more
conceivable than the rest? (David Hume, epigraph)
Why the Idea Matters: States exactly the puzzle the prior resolves — you need a reason to weight
hypotheses.
Source Location: Epigraph to "Bayes's Rule and Prior Beliefs" (PDF p. 173).
```

```
Paraphrase (short): "It's difficult to make predictions, especially about the future." (Danish proverb)
Why the Idea Matters: The wry framing for the Copernican section on predicting from one data point.
Source Location: Epigraph to "The Copernican Principle" (PDF p. 175).
```

```
Paraphrase (short): "As if someone were to buy several copies of the morning paper to assure himself
that what it said was true." (Wittgenstein, epigraph)
Why the Idea Matters: Why media repetition adds no evidential weight — directly supports "protect your
priors."
Source Location: Epigraph to "Priors in the Age of Mechanical Reproduction" (PDF p. 190).
```

## 13. Psychology Connections

- **The availability heuristic.** The plane-vs-car and news-distortion material is essentially an
  availability-heuristic argument grounded in Bayesian priors — vivid, media-amplified events inflate
  perceived frequency.
- **Base-rate neglect (and its opposite).** The chapter argues people *use* base rates well when priors
  are accurate — a partial counterpoint to the Kahneman/Tversky base-rate-neglect tradition.
- **Delay of gratification / self-control.** The marshmallow reinterpretation recasts a landmark
  self-control result as partly calibrated expectation, linking prediction to trust and environment.
- **Trust and environment.** The Rochester study ties delay behavior to experienced reliability — a
  developmental-psychology point about how dependable caregivers shape expectations.
- **Ecological rationality.** Priors "well tuned to their own ecological niche" (desert/sand,
  poles/snow) is a Gigerenzer-style ecological-rationality claim (inference; not named).
- **Few-shot human learning.** "Small data is big data in disguise" is a cognitive-science account of
  how people generalize from one example via rich priors.
- **Optimism and reframing.** Gould's survival story shows how understanding a distribution reshapes
  emotional response to the same statistic.

## 14. Mathematics and Decision Science Connections

- **Bayesian inference.** The chapter is a first-principles tour: likelihood, prior, posterior, and the
  multiply-to-combine rule.
- **Laplace's rule of succession.** (w+1)/(n+2) is the classic rule of succession / additive smoothing —
  directly the Laplace smoothing used in statistics and NLP.
- **Prior distributions.** Uniform/uninformative priors, and the recognition that "uninformative" is
  itself a modeling choice (a power-law over scales).
- **Distribution families.** Normal (Gaussian), power-law/scale-free, and Erlang, each with a
  characteristic shape and tail behavior; memorylessness (the exponential/Erlang property).
- **Preferential attachment.** A generative model for power laws (Yule–Simon/Barabási–Albert style),
  named here as "the rich get richer."
- **Estimation from minimal data.** The German tank problem is a textbook maximum-likelihood / minimum-
  variance estimation result.
- **Prediction rules as posterior expectations.** Multiplicative/Average/Additive are the posterior
  predictive means for their respective priors.
- **Reverse inference.** Reverse-engineering priors from behavior (hold times) is inverse Bayesian /
  computational-cognitive modeling.

## 15. Sports Connections

**Direct examples from the book:** One brief mention — using Laplace's Law to estimate "the chance your
softball team will win."

**Inferred applications (mine):**
- **Small-sample performance estimates.** Laplace's Law is a direct fix for over-reading early-season or
  small-sample records: a player who is 3-for-3 isn't a 100% hitter; (w+1)/(n+2) gives a saner estimate —
  the logic behind regression-to-the-mean and shrinkage in sports analytics.
- **Streaks and distribution shape.** Whether a hot streak predicts more success depends on the
  distribution: treating scoring runs as power-law (ride the hot hand) vs. normal (regression, expect a
  cold spell) vs. memoryless (no signal) maps onto real debates about the "hot hand."
- **Career length and the Copernican Principle.** Predicting how much longer a career, a manager's
  tenure, or a dynasty will last from how long it's already lasted — with the caveat that we usually have
  informative priors (typical career arcs) that beat the naive doubling.
- **Injury and event intervals as Erlang.** Time between independent events (certain injuries, penalties)
  may be memoryless, so "we're due" reasoning is a fallacy — the Additive Rule says the wait is unchanged.
- **Media-distorted fan priors.** Highlight reels and viral moments oversample the spectacular, skewing
  fans' (and pundits') priors about how often such plays actually happen — a sports version of "protect
  your priors."

## 16. AI and Machine Learning Connections

**Direct from the book:** Norvig's "The Unreasonable Effectiveness of Data" (big data) is explicitly
contrasted with the "small data" the chapter is about; the Griffiths–Tenenbaum program is
computational-cognitive-science modeling of human priors.

**Inferred connections (mine):**
- **Laplace / additive smoothing.** (w+1)/(n+2) is exactly Laplace smoothing used to avoid zero
  probabilities in naive Bayes classifiers and n-gram language models.
- **Priors and regularization.** "Good priors matter more than data volume" is the Bayesian view of
  regularization and of why priors/inductive biases are essential; the uninformative-prior point warns
  that "no prior" is itself a strong assumption.
- **Few-shot / in-context learning.** "Small data is big data in disguise" is precisely why large
  pretrained models do few-shot learning well: a rich prior (pretraining) lets one or few examples
  suffice.
- **Distribution shape and heavy tails.** Recognizing power-law vs. normal vs. Erlang is central to
  modeling heavy-tailed data (incomes, web traffic, model failures) and to why mean-based methods
  mislead on power-law quantities.
- **Bayesian prediction / posterior predictive.** The three rules are posterior predictive means;
  Bayesian methods, conjugate priors, and calibration all sit here.
- **Data/distribution shift and prior corruption.** "Protect your priors" is a human analogue of
  training-data bias: a model (or mind) trained on media-skewed frequencies inherits skewed priors —
  the media asymmetry is a data-collection bias.
- **Inverse modeling of humans.** Reverse-engineering priors from single-point predictions is a template
  for inferring human beliefs/objectives from behavior (relevant to preference learning and RLHF).

## 17. Content Creation Opportunities

```
Idea Title: How to predict the future from a single clue
Format: YouTube Long-form
Application Domain: History
Hidden Principle: Bayesian Thinking
Story Hook (Layer 1): A physicist stood at the Berlin Wall and predicted how long it would last — from
one number; the same method cracked how many tanks the Nazis were building, almost exactly.
Principle Framework (Layer 2): The Copernican Principle is Bayes with an uninformative prior: absent other
information, assume you're seeing something at a random moment in its life, and a single data point yields
a real prediction. "No assumptions" is itself an assumption (a power-law prior).
Best Supporting Case: Gott at the Berlin Wall; the German tank problem (the estimate of 245 vs. the true
246).
Character Application: Nova: Strategist
Psychology Angle: Why single-point predictions feel absurd but aren't.
Math Angle: Bayes's Rule; the uninformative prior; the doubling rule.
Sports Angle: Predicting a career's remaining length from its current length.
Business Angle: Estimating a startup's remaining runway or a trend's lifespan from one age reading.
Investing Angle: Using time-in-existence as a crude prior on how long a fund or fad will last.
History Angle: The German tank problem as wartime statistics that beat spy estimates.
AI Angle: Priors / inductive biases; why "no assumptions" is itself an assumption.
```

```
Idea Title: One win doesn't mean 100% — the math of small samples
Format: YouTube Short
Application Domain: Everyday Life
Hidden Principle: Bayesian Thinking
Story Hook (Layer 1): If you try something once and it works, your real success rate isn't 100% — it's
about two-thirds.
Principle Framework (Layer 2): Laplace's Law, (w+1)/(n+2), pulls tiny-sample estimates toward the prior,
so "it worked once" is weak evidence; certainty should scale with how much data you actually have.
Best Supporting Case: Laplace's Law; the losing-Powerball-ticket footnote.
Character Application: Insight: Interpreter
Psychology Angle: Over-reading tiny samples; the seduction of "it worked once."
Math Angle: The rule of succession / additive smoothing.
Sports Angle: A 3-for-3 hitter isn't a 100% hitter; regression to the mean.
Business Angle: One successful pilot doesn't prove a repeatable process.
Investing Angle: A single winning trade is not a track record.
History Angle: Laplace's sunrise problem as the origin of the rule of succession.
AI Angle: Laplace smoothing in naive Bayes and language models.
```

```
Idea Title: Three kinds of things, three ways to predict them
Format: YouTube Long-form
Application Domain: Everyday Life
Hidden Principle: Bayesian Thinking
Story Hook (Layer 1): The longer a marriage lasts, the longer it'll last; the longer you've waited for a
bus, the sooner it'll come; and some things you'll wait for the same amount forever — here's how to tell
which is which.
Principle Framework (Layer 2): The shape of the distribution dictates the prediction rule: power-law →
Multiplicative (the longer it's lasted, the longer to go), normal → Average (things become "overdue"),
Erlang → Additive (memoryless, always the same wait). Identify the shape first.
Best Supporting Case: Movie grosses (×1.4); human lifespans (average); the blackjack "twenty more hands";
Gould's cancer.
Character Application: Sigma: Architect
Psychology Angle: Why institutional collapses always shock us (the power-law surprise signature).
Math Angle: Distribution shape dictates the prediction rule and the "surprise signature."
Sports Angle: Hot-hand debates as a distribution-identification problem.
Business Angle: Predicting a company's or product's remaining life by which distribution it lives in.
Investing Angle: Heavy-tailed returns — why average-based intuition mis-prices tail risk.
History Angle: Why dynasties and empires (power-law) shock everyone when they finally fall.
AI Angle: Heavy-tailed data and why mean-based methods mislead.
```

```
Idea Title: The marshmallow test was never really about willpower
Format: YouTube Long-form
Application Domain: Everyday Life
Hidden Principle: Bayesian Thinking
Story Hook (Layer 1): The famous marshmallow test predicted kids' success in life — but a follow-up
suggests it wasn't measuring willpower at all, but whether they'd learned adults keep their promises.
Principle Framework (Layer 2): Waiting is a rational bet on a prior about reliability: under a power-law
of possible delays, giving up can be optimal, so "self-control" is really calibrated expectation about
whether the reward will actually arrive.
Best Supporting Case: Mischel's original test; McGuire & Kable's power-law reinterpretation; the Rochester
reliability study (a broken promise first, then the marshmallow).
Character Application: Insight: Interpreter
Psychology Angle: Trust, environment, and delay of gratification.
Math Angle: Power-law waits make "cutting your losses" rational, not weak.
Sports Angle: "We're due" as a memoryless fallacy.
Business Angle: Employees "waiting it out" only if they trust the org to deliver on promises.
Investing Angle: Holding vs. cutting depends on your prior about whether the payoff will ever come.
History Angle: How environments of broken promises rationally teach short time-horizons.
AI Angle: Inferring beliefs / objectives from behaviour.
```

```
Idea Title: Why you should watch less news to understand the world better
Format: YouTube Short
Application Domain: Everyday Life
Hidden Principle: Cognitive Bias
Story Hook (Layer 1): You've seen about as many plane crashes as car crashes — and one of those numbers
is a lie your screen told you.
Principle Framework (Layer 2): Good prediction depends on priors calibrated to real frequencies, but media
reports the rare, not the frequent, so heavy news consumption corrupts the very priors it feels like it's
informing. Protect your priors.
Best Supporting Case: Planes vs. cars (Carnegie Hall vs. Wyoming); murder down 20% while news gun-violence
coverage rose 600%.
Character Application: Echo: Observer
Psychology Angle: The availability heuristic; media and fear.
Math Angle: Priors, frequency, and calibration.
Sports Angle: Highlight reels distorting how often the spectacular actually happens.
Business Angle: Dashboards that surface exceptions distorting a team's sense of the baseline.
Investing Angle: Financial media amplifying rare crashes and manias, warping risk priors.
History Angle: How each era's media diet reshaped what people feared most.
AI Angle: Training-data bias; skewed data → skewed priors.
```

```
Idea Title: The sign that tells you when to walk away from a job
Format: YouTube Short
Application Domain: Business
Hidden Principle: Bayesian Thinking
Story Hook (Layer 1): A construction site proudly displays "7 days since the last accident" — a
statistician reads that and quietly walks away.
Principle Framework (Layer 2): A single "time since last event" number, via Bayes with an uninformative
prior, implies the whole timescale: a short count implies short intervals (frequent accidents). One
figure can betray the base rate it was meant to reassure you about.
Best Supporting Case: The "7 days since last accident" sign; the bus-stop "time since last bus" sign; the
Berlin Wall.
Character Application: Nova: Strategist
Psychology Angle: How a single number implies a whole timescale we don't consciously compute.
Math Angle: The doubling rule; Bayes with an uninformative prior.
Sports Angle: "We're due" reasoning; predicting a streak's remaining length.
Business Angle: Reading "days since last incident/outage" as a hidden base-rate signal.
Investing Angle: Inferring a strategy's fragility from how recently it last blew up.
History Angle: Safety-signage culture and what those tallies unintentionally reveal.
AI Angle: Priors from one data point; why "no assumptions" is an assumption.
```

```
Idea Title: Little orphan Annie was a great statistician
Format: YouTube Short
Application Domain: Everyday Life
Hidden Principle: Bayesian Thinking
Story Hook (Layer 1): "The sun'll come out tomorrow" — a cheesy showtune, and a mathematically airtight
prediction.
Principle Framework (Layer 2): The flip side of small-sample humility: Laplace's Law, (w+1)/(n+2),
approaches certainty as n grows enormous, so childlike confidence backed by a trillion confirmations is
fully justified. Certainty should track your data.
Best Supporting Case: The Annie epigraph; ~1.6 trillion sunrises → ~100%.
Character Application: Insight: Interpreter
Psychology Angle: When childlike certainty is actually justified.
Math Angle: (w+1)/(n+2) as n grows huge.
Sports Angle: Long track records vs. rookie small samples.
Business Angle: A decades-proven process earns near-certainty a new one hasn't.
Investing Angle: A long, deep track record vs. one hot quarter.
History Angle: Laplace using the sunrise as his own worked example of the rule.
AI Angle: Laplace smoothing; confidence with lots vs. little data.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B01-C06-01
Title: Reasoning backward via forward likelihoods (Bayes's insight)
Type: Concept
Summary: To infer a hidden cause from what you observe, first reason forward: compute how likely your
data would be under each hypothesis (the "likelihood"), then favor hypotheses accordingly. Three
winning tickets in a row is 100% likely if all tickets win, 1/8 if half do, one-in-a-billion if 1/1000
— so all-win is exactly 8× likelier than half-win.
Source: Algorithms to Live By, ch. 6, "Reasoning Backward" (PDF pp. 170–171)
Tags: bayes, likelihood, inference, core-concept
Related Concepts: Prior, Bayes's Rule, Laplace's Law
```

```
CARD ID: B01-C06-02
Title: Laplace's Law — (w+1)/(n+2)
Type: Model
Summary: With no prior knowledge, estimate a success rate as (wins+1)/(attempts+2). One win in one try
→ 2/3 (not 100%); five of ten → 50%. A single losing Powerball ticket → 1/3 chance next. Works
identically from one data point to millions.
Source: Algorithms to Live By, ch. 6, "Laplace's Law" (PDF pp. 172–173, footnote p. 194)
Tags: laplace, rule-of-succession, small-data, smoothing, model
Related Concepts: Uniform prior, Bayes's Rule, additive smoothing
```

```
CARD ID: B01-C06-03
Title: Bayes's Rule — prior × evidence
Type: Model
Summary: Combine preexisting belief with observed evidence by multiplying probabilities (posterior ∝
prior × likelihood). Nine fair coins + one two-headed, drawn coin shows heads: fair is half as likely
to show heads but 9× likelier drawn → 4.5× likelier fair. Always needs a prior — you can't multiply a
missing probability.
Source: Algorithms to Live By, ch. 6, "Bayes's Rule and Prior Beliefs" (PDF pp. 173–175)
Tags: bayes-rule, prior, posterior, multiplication, model
Related Concepts: Likelihood, uninformative prior, prediction rules
```

```
CARD ID: B01-C06-04
Title: The prior — the historically controversial ingredient
Type: Concept
Summary: The prior is your sense of how probable each hypothesis was before any data ("what's in the
bag"). Bayes's Rule always needs one, even a guess. Priors were once called biased and unscientific,
but a true blank slate is rare — and prediction quality depends more on prior quality than on data
volume.
Source: Algorithms to Live By, ch. 6, "Bayes's Rule and Prior Beliefs" (PDF pp. 174–175)
Tags: prior, controversy, calibration, concept
Related Concepts: Uninformative prior, small data, distribution shape
```

```
CARD ID: B01-C06-05
Title: The Copernican Principle = Bayes with an uninformative prior
Type: Model
Summary: Assuming your observation moment isn't special, you're on average halfway through, so predict a
thing lasts as long as it already has (Berlin Wall at 8 → 8 more; actually 20). It is exactly Bayes's
Rule with an uninformative prior — which is itself a power-law. Reasonable when you know nothing; absurd
when you don't (90-year-old → 180).
Source: Algorithms to Live By, ch. 6, "The Copernican Principle" / "Bayes Meets Copernicus" (PDF
pp. 175–179)
Tags: copernican-principle, uninformative-prior, doubling, single-data-point, model
Related Concepts: Power-law, Multiplicative Rule, German tank problem
```

```
CARD ID: B01-C06-06
Title: The German tank problem
Type: Case
Summary: In WWII, Allied statisticians estimated German tank output from captured serial numbers: the
math said 246/month; risky aerial reconnaissance said ~1,400; postwar records showed 245. Harold
Jeffreys had earlier reached "double the serial number" for counting a city's tramcars. Minimal-data
inference beat expensive, dangerous reconnaissance almost exactly.
Source: Algorithms to Live By, ch. 6, "Bayes Meets Copernicus" (PDF p. 178)
Tags: german-tank-problem, estimation, minimal-data, WWII, case
Related Concepts: Copernican Principle, Jeffreys tramcars, MLE
```

```
CARD ID: B01-C06-07
Title: Normal vs. power-law distributions
Type: Concept
Summary: Normal (Gaussian/bell curve) quantities cluster around a natural scale — US male lifespan ~76,
plus height, weight, blood pressure, temperature, fruit size. Power-law (scale-free) quantities have
most below the mean and a few enormous ones above — town population (avg 8,226, most smaller), movie
grosses (Titanic), income (mean $55,688; two-thirds below; top 1% ~10× mean; top 1% of 1% ~10× that).
Source: Algorithms to Live By, ch. 6, "Real-World Priors" (PDF pp. 179–180)
Tags: normal, power-law, scale-free, distributions, concept
Related Concepts: Preferential attachment, prediction rules, heavy tails
```

```
CARD ID: B01-C06-08
Title: Preferential attachment — "the rich get richer"
Type: Concept
Summary: When having more of something makes you likelier to gain more — popular sites get more links,
followed celebrities gain more fans, big cities draw more residents — you reliably get a power-law
distribution. One of the surest generators of scale-free quantities.
Source: Algorithms to Live By, ch. 6, "Real-World Priors" (PDF p. 180)
Tags: preferential-attachment, power-law, mechanism, concept
Related Concepts: Power-law, Multiplicative Rule, inequality
```

```
CARD ID: B01-C06-09
Title: The three prediction rules (Multiplicative / Average / Additive)
Type: Model
Summary: Match the rule to the prior's shape. Power-law → Multiplicative: multiply what you've seen by a
constant (×2 uninformative; ×1.4 movies — $6M→$8.4M, $90M→$126M). Normal → Average: predict the natural
average (90yo→94, 6yo→77). Erlang/memoryless → Additive: predict a constant amount more.
Source: Algorithms to Live By, ch. 6, "… and Their Prediction Rules" (PDF pp. 180–183)
Tags: prediction-rules, multiplicative, average, additive, model
Related Concepts: Distribution shape, memorylessness, surprise signature
```

```
CARD ID: B01-C06-10
Title: The Erlang distribution and memorylessness
Type: Concept
Summary: The Erlang distribution (Agner Krarup Erlang, Copenhagen Telephone Co.) models intervals
between independent events — a winglike curve, tail between power-law and normal. It is "memoryless":
the same prediction regardless of history (a blackjack always "twenty more hands" away). Models
radioactive decay/Geiger ticks, traffic, internet infrastructure, and House tenure. No right time to
quit → partly explains gambling's grip.
Source: Algorithms to Live By, ch. 6, "… and Their Prediction Rules" (PDF pp. 182–186)
Tags: erlang, memoryless, additive-rule, gambling, concept
Related Concepts: Additive Rule, radioactive decay, "The Gambler"
```

```
CARD ID: B01-C06-11
Title: Each distribution's "surprise signature"
Type: Insight
Summary: Power-law events grow more surprising the longer you wait — maximally surprising right before
they happen (so institutional collapse always shocks). Normal events are surprising only when early
(later they seem overdue). Erlang events are never any more or less surprising, whenever they occur.
Source: Algorithms to Live By, ch. 6, "… and Their Prediction Rules" (PDF p. 185)
Tags: surprise, distributions, risk-perception, insight
Related Concepts: Power-law, normal, Erlang, prediction rules
```

```
CARD ID: B01-C06-12
Title: Stephen Jay Gould's cancer — median ≠ distribution
Type: Case
Summary: Gould's cancer had a median survival of 8 months, but the distribution was strongly
right-skewed (power-law-like) with a long tail. The Multiplicative Rule implied the longer he lived, the
longer he'd likely live: "I saw no reason why I shouldn't be in that small tail." He lived 20 more
years. Knowing the distribution's shape, not just its median, changed everything.
Source: Algorithms to Live By, ch. 6, "… and Their Prediction Rules" (PDF pp. 185–186)
Tags: gould, cancer, power-law, median-vs-distribution, case
Related Concepts: Multiplicative Rule, right-skew, hope
```

```
CARD ID: B01-C06-13
Title: Small data is big data in disguise
Type: Insight
Summary: People predict everyday quantities well from a single data point (Griffiths & Tenenbaum)
because our priors — absorbed unconsciously from the world — are rich and accurate, implicitly using the
right rule per distribution. We fail only where priors are poor (pharaohs' reigns, an unfamiliar Erlang).
Good predictions require good priors.
Source: Algorithms to Live By, ch. 6, "Small Data and the Mind" (PDF pp. 186–188)
Tags: small-data, priors, intuition, few-shot, insight
Related Concepts: Reverse-engineering priors, distribution shape, protect-your-priors
```

```
CARD ID: B01-C06-14
Title: Your predictions reverse-engineer your experience
Type: Insight
Summary: Because good predictions require good priors, what you forecast betrays what you've lived — so
prediction is a diagnostic of a person's world. Cognitive scientists reverse-engineer people's priors
across domains (hold times → multiplicative ~1.33×, a power-law prior); "our judgments betray our
expectations, and our expectations betray our experience."
Source: Algorithms to Live By, ch. 6, "Small Data and the Mind" (PDF pp. 187–188)
Tags: reverse-inference, priors, experience, insight
Related Concepts: Small data, Rochester study, inverse modeling
```

```
CARD ID: B01-C06-15
Title: The marshmallow test reinterpreted — expectation, not willpower
Type: Case
Summary: If adults' return time is power-law/unreliable, eating the marshmallow is rational (McGuire &
Kable). A Rochester study primed kids with a reliable or unreliable experimenter (a kept vs. broken
art-supplies promise); those who met an unreliable one ate the marshmallow sooner. So delay of
gratification may be partly calibrated expectation shaped by whether adults keep their word — not a fixed
willpower trait.
Source: Algorithms to Live By, ch. 6, "What Our Predictions Tell Us About Ourselves" (PDF pp. 188–190)
Tags: marshmallow-test, self-control, expectations, trust, case
Related Concepts: Power-law waits, Multiplicative Rule, environment
```

```
CARD ID: B01-C06-16
Title: Protect your priors — turn off the news
Type: Insight
Summary: Experience is sampled at true frequency, but language and media over-sample the rare and
interesting, corrupting priors. You've seen ~as many crashed planes as cars, but planes came via screens
from another continent; US plane-crash deaths since 2000 wouldn't half-fill Carnegie Hall while
car-crash deaths exceed Wyoming's population; 1990s murder fell 20% as news gun violence rose 600%. To
be a good intuitive Bayesian, protect your priors — perhaps by turning off the news.
Source: Algorithms to Live By, ch. 6, "Priors in the Age of Mechanical Reproduction" (PDF pp. 190–192)
Tags: protect-priors, media, availability, calibration, insight
Related Concepts: Small data, ecological niche, distribution shape
```

```
CARD ID: B01-C06-17
Title: Reverend Bayes and the raffle
Type: Case
Summary: An 18th-century Presbyterian minister in Tunbridge Wells worked backward from observed
wins/losses to a lottery's likely composition by reasoning forward from hypotheticals. He abandoned the
paper; his friend Richard Price found it after Bayes's 1761 death and showed one winning ticket → 75%
chance ≥half the tickets win. The founder of reasoning under uncertainty has an "ironically uncertain"
biography, and Laplace did the real heavy lifting.
Source: Algorithms to Live By, ch. 6, "Reasoning Backward" (PDF pp. 169–171)
Tags: bayes, history, raffle, price, case
Related Concepts: Likelihood, Laplace's Law, reasoning backward
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: To predict from small data — often a single observation — reason backward from evidence to
the most probable cause by reasoning forward from hypotheticals (likelihood) and multiplying by a prior
(Bayes's Rule). Good prediction depends far more on having the right prior — knowing the distribution
your data comes from — than on data volume. Power-law, normal, and Erlang distributions give three
different rules (Multiplicative, Average, Additive); humans are strong intuitive Bayesians because
"small data is big data in disguise," which makes predictions a mirror of experience and makes
media-distorted priors dangerous.

Top 5 Concepts:
1. Reasoning backward via forward likelihoods (Bayesian inference)
2. Bayes's Rule = prior × evidence; the necessity of a prior
3. Laplace's Law, (w+1)/(n+2), for small data
4. The Copernican Principle = Bayes with an uninformative prior
5. Distribution shape → prediction rule (Multiplicative / Average / Additive) and "small data is big
   data in disguise"

Top 3 Claims:
1. You can rationally predict from a single data point if your prior is good; the doubling/Copernican
   rule works when you know nothing (German tank problem: 245 vs. the math's 246) and fails when you
   know something.
2. Each distribution has a distinct optimal prediction rule and surprise signature; power-law things
   last longer the longer they've lasted, normal things become overdue, Erlang things never change.
3. Media reports the rare, not the frequent, so it corrupts the priors good prediction depends on —
   protecting your priors may mean turning off the news.

Top 3 Cases:
1. Gott at the Berlin Wall (the Copernican Principle) and the German tank problem
2. Stephen Jay Gould's cancer (median vs. distribution shape; the Multiplicative Rule and 20 more years)
3. The marshmallow test reinterpreted (Rochester reliability study; expectation vs. willpower)

Top 3 Studies:
1. Bayes's essay + Laplace's Law (the foundations of inverse probability)
2. Griffiths & Tenenbaum single-point prediction (people match Bayes; fail on pharaohs)
3. The Rochester reliability-before-marshmallow study (reliability causally shifts delay behavior)

Most Unique Idea: "Small data is big data in disguise" — human predictive skill comes from rich,
unconsciously absorbed priors, so predictions reverse-engineer a person's experience, and "an
uninformative prior is itself a power-law" (assuming nothing is not neutral).

Most Counterintuitive Idea: Consuming more news can make your intuitive predictions worse, because media
frequency doesn't track world frequency and corrupts your priors.

Biggest Weakness or Open Question: The chapter's method depends entirely on identifying the right
distribution/prior, but it offers no general way to do so in a novel situation (people fail exactly when
they misjudge it, as with pharaohs); it calls humans "remarkably good Bayesians" while also arguing
media badly distorts priors, a tension it notes but doesn't reconcile; and "turn off the news"
optimizes for calibrated frequency priors at the risk of missing rare-but-important signals.

Best Content Opportunity: A long-form video on the three prediction rules — power-law/normal/Erlang, the
Multiplicative/Average/Additive rules, and their surprise signatures — anchored by Gould's cancer and
the blackjack "twenty more hands," landing on "small data is big data in disguise."
```
