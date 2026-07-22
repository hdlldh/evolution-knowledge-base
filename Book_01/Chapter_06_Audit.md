# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 6: Bayes's Rule — Predicting the Future
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 168–194, re-read against Chapter_06_Extraction.md
**Date:** 2026-07-21

---

## Missing Items

**1. The Annie / "Tomorrow" epigraph.** (PDF p. 168) The chapter's second epigraph is "The sun'll come
out tomorrow. You can bet your bottom dollar there'll be sun." (Annie) — which the chapter later pays
off directly: little Annie's faith is *justified* by Laplace's Law (~1.6 trillion prior sunrises →
~100%). The extraction has the sunrise payoff but dropped the epigraph itself, which is the setup for
one of the chapter's best closed loops.

**2. The three David Hume epigraphs.** (PDF pp. 169, 173) Two Hume quotations frame the Bayes and prior
sections: "If we be… engaged by arguments to put trust in past experience… these arguments must be
probable only," and "All these suppositions are consistent and conceivable. Why should we give the
preference to one…?" Hume is the philosophical backdrop for the whole problem of induction the chapter
is answering with Bayes — a significant framing the extraction omitted. The Danish proverb "It's
difficult to make predictions, especially about the future" (p. 175) and the Ben Lerner and Wittgenstein
epigraphs also went uncaptured.

**3. The bus-stop real-time-sign application.** (PDF pp. 176–177) A concrete, clever policy suggestion:
a transit system that can't afford real-time "next bus" signs could instead cheaply display *how long
since the previous bus* — the Copernican Principle turned into public infrastructure. The extraction
lists the Berlin Wall and relationships but dropped this genuinely actionable civic example.

**4. The "7 days since the last industrial accident" example.** (PDF p. 176) A vivid, slightly dark
Copernican application: a construction sign reading "7 days since the last accident" implies (Copernican)
another accident is likely within ~7 days — "stay away, unless it's a particularly short job." Reusable
and memorable; omitted.

**5. The New Yorker "2525" smartphone cover.** (PDF p. 176) The Copernican skepticism example — a cover
depicting a familiar smartphone captioned "2525," when the smartphone is "barely a decade old," so it's
unlikely to survive even to 2025 ("By 2525 it'd be mildly surprising if there were even a New York
City"). A funny, teachable instance the extraction skipped.

**6. Laplace's specific achievements.** (PDF p. 172) The extraction notes Laplace showed male infants
slightly more likely, but omits that the *Philosophical Essay on Probabilities* is called "arguably the
first book about probability for a general audience and still one of the best," applying the theory to
"law, the sciences, and everyday life." Minor but part of Laplace's stature.

**7. Price's exact "metaprobability" framing.** (PDF p. 171) The chapter's point that Price's answer
(75% chance of ≥50% win rate) is *less actionable* than Laplace's single number — "a 75% metaprobability
of a 50% or greater chance of success" — is the precise reason Laplace's Law matters. The extraction has
the 75% figure but not the "metaprobability" contrast that motivates the whole move to Laplace.

**8. The uninformative-prior footnote on Laplace's Law.** (PDF p. 194) The chapter's footnote makes
explicit that Laplace's Law in its simplest form *is* the uniform-prior assumption (1% as likely as 10%
as 50% as 100%), and that a single losing Powerball ticket → 1/3 "faithfully reflects the odds in a
raffle where you come in knowing nothing at all." The extraction captured the 1/3 figure in card 2 but
should tie it explicitly to the uniform-prior assumption, since that connects Laplace's Law to the
Copernican Principle (both uninformative-prior methods).

**9. The Wittgenstein epigraph on self-confirmation.** (PDF p. 190) "As if someone were to buy several
copies of the morning paper to assure himself that what it said was true" — a sharp image for why
media repetition doesn't add evidential weight, directly relevant to "protect your priors." Omitted.

## Corrections Needed

**1. Tom Griffiths is the co-author; the experiment is "Tom, along with… Josh Tenenbaum."**
- Extraction (§5, §16) correctly names Griffiths & Tenenbaum, but should make explicit (as the chapter
  does, PDF p. 186) that "Tom" is co-author Tom Griffiths and this is his own graduate-school work — a
  first-person authorial stake worth flagging, not a neutral third-party citation.

**2. The mean-income figure and the "top 1% of the 1%."**
- Extraction (§3, card 7): "top 1% ~10× the mean; top 1% of the 1% ~10× that." The chapter says the top
  1% make "almost ten times the mean," and the top 1% *of* the 1% make "ten times more than that" (PDF
  p. 180). Accurate, but "almost ten times" for the first should keep the "almost" — a small hedge the
  extraction dropped in card 7.

**3. Human lifespan figure attribution.**
- Extraction (§3, card 7): "US male lifespan ~76." The chapter says "the average life span for men in
  the United States… is centered at about 76 years" (PDF p. 179) — correct, but it is specifically the
  *men's* average and used as the center of a normal distribution, which the extraction preserves; no
  change needed beyond confirming the "men" qualifier is present (it is).

## Overgeneralizations

**1. "People are remarkably good intuitive Bayesians" needs its scope stated up front.** The chapter's
claim is bounded: people match Bayes *in domains where their absorbed priors are accurate*, and fail
where they aren't (pharaohs). The extraction flags this in §3/§11, but §2's concept entry and §19's
top-claims state the "good Bayesian" result more broadly than the chapter's own "except pharaohs'
reigns" qualification. Carry the boundary with the claim.

**2. The marshmallow reinterpretation is presented by the chapter as a *possibility*, hedged.** The
chapter says resisting temptation "may be, at least in part, a matter of expectations rather than
willpower" and calls the expectations story "perhaps more poignant" — explicitly not a replacement of
the willpower account. The extraction's §9 insight and card 15 lean toward "was never really about
willpower" (which is fine as a content hook) but the analytic entries should preserve the "at least in
part / may be" hedge, since the chapter does not claim willpower plays no role.

**3. "Turn off the news" is the authors' prescription, stated as counterintuitive advice, not an
established finding.** The extraction mostly frames it correctly, but should ensure it reads as the
authors' inference from the frequency-distortion evidence (Glassner) rather than a demonstrated result —
the evidence shows distortion; the behavioral recommendation is a leap.

## Important Nuance Lost

**1. Why Price's answer wasn't enough — the "probabilities of probabilities" head-spin.** (PDF p. 171)
The chapter emphasizes that Bayes/Price left you reasoning about "probabilities *of* probabilities,"
which "can get a bit head-spinning," and crucially couldn't answer "what do you think the odds *actually
are*?" This is the precise gap Laplace filled — the extraction states Laplace "distilled" the hypotheses
but loses *why* the distillation was needed (you literally couldn't state a single expectation before).

**2. The uninformative prior "rules out" hypotheses via the data.** (PDF pp. 177–178) The chapter's
mechanism for the Copernican result is worth preserving precisely: the 8-year observation *immediately
rules out* any hypothesis predicting a lifespan < 8 years (just as the first tails rules out a
two-headed coin), while enormously long spans aren't ruled out but are improbable coincidences. The
extraction gestures at this but the "ruling out" + "improbable coincidence" two-part mechanism is the
actual derivation and deserves to be explicit.

**3. Normal vs. power-law "surprise" tied to gambling strategy.** (PDF p. 185) The chapter works
through what each distribution would imply for a roulette/gambling wait — normal (Average Rule: your
number's coming, then quit), power-law (Multiplicative: keep playing after a win, give up after a
drought), memoryless (Additive: nothing ever changes, no right time to quit). The extraction has the
memoryless conclusion but drops the *contrast across all three* applied to gambling, which is the
clearest single illustration of why identifying the distribution matters.

**4. "Both are well tuned to their own ecological niche."** (PDF pp. 190–191) The chapter's setup for
the media argument is that even *biased* priors usually reflect the specific world you live in (desert
dweller overestimates sand; polar dweller overestimates snow) — so priors are locally adaptive, and it
is *language/media* that breaks this, not bias per se. The extraction has the niche examples but
under-states that this is the hinge: the problem is decoupling experience from talk, not bias itself.

**5. "Events are always experienced at their proper frequencies."** (PDF p. 191) The precise
formulation of the media argument: direct experience is *automatically* correctly frequency-weighted,
but language is not, because we retell the rare (snake bite, lightning). This asymmetry — experience
self-calibrates, language de-calibrates — is sharper than the extraction's "media reports the
interesting/rare."

## Additional Cases and Examples

```
Case Title: Little Annie and the sunrise
People / Organization: "Annie" (epigraph); Laplace's Law
Context: A child's certainty that the sun will rise.
What Happened: The epigraph — "The sun'll come out tomorrow. You can bet your bottom dollar there'll be
sun" — is vindicated by Laplace's Law: with the Earth having seen ~1.6 trillion consecutive sunrises,
the chance of another is all but indistinguishable from 100%.
Outcome: A childlike faith turns out to be rigorously justified.
Concept Illustrated: Laplace's Law; large-n behavior of (w+1)/(n+2).
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
particularly short job."
Outcome: A darkly funny, immediately graspable Copernican application to everyday signage.
Concept Illustrated: The Copernican Principle / doubling from a single data point.
Why This Case Is Useful: A memorable, slightly subversive hook that makes the doubling rule stick.
Potential for Reuse: High
```

```
Case Title: The bus-stop sign that shows the past
People / Organization: The authors (a transit-policy suggestion)
Context: Cities that can't afford real-time "next bus" prediction signs.
What Happened: The Copernican Principle suggests a cheap alternative: simply display how long since the
*previous* bus arrived, which gives a substantial hint about when the next will come.
Outcome: A concrete public-infrastructure application of single-data-point prediction.
Concept Illustrated: The Copernican Principle as usable policy.
Why This Case Is Useful: Turns an abstract rule into a real, cheap civic design — great for showing the
method's practical reach.
Potential for Reuse: Medium
```

## Additional Research Evidence

None materially missing. The re-read confirms the empirical spine is Bayes/Laplace (historical), the
German tank problem (verified: 245 vs. 246), Griffiths & Tenenbaum (people match Bayes; fail on
pharaohs), the marshmallow trio (Mischel; McGuire & Kable; Rochester), and Glassner's media/crime
figures — all captured. One sharpening already noted: tie Laplace's Law explicitly to its uniform-prior
assumption (the footnote), which links it to the Copernican Principle as the chapter's *two*
uninformative-prior methods.

## Potential Disagreements to Track Later

1. **Kahneman & Tversky / base-rate neglect and the availability heuristic.** The chapter's "people are
   remarkably good Bayesians" directly collides with the heuristics-and-biases tradition; yet its own
   closing "protect your priors" section *is* an availability-heuristic argument. A cross-book comparison
   with *Thinking, Fast and Slow* would be sharp — the book argues good priors where K&T argue biased
   ones, and both are partly right in different regimes.
2. **Gigerenzer / ecological rationality.** The "priors tuned to your ecological niche" framing aligns
   with Gigerenzer's ecological rationality and against a purely deficit view of intuition — a recurring
   alliance across chapters (2, 4, 6).
3. **Nassim Taleb / heavy tails and Black Swans.** The power-law material and "institutions are always
   stunning when they collapse" overlap heavily with Taleb's fat-tail / Black Swan work; a natural
   cross-book pairing (and a place the book is more optimistic than Taleb about predictability).
4. **The frequentist/Bayesian foundations debate.** The chapter's history nods to the prior being
   called "unscientific"; any statistics or philosophy-of-science text will engage this old controversy.
5. **Media-effects and cultivation theory (Glassner, Gerbner).** "Protect your priors / turn off the
   news" connects to a large media-studies literature on how coverage shapes perceived risk.

## Additional Content Opportunities

```
Idea: The sign that tells you when to walk away from a job
Format: YouTube Short
Core Concept: The Copernican Principle in everyday signage.
Hook: A construction site proudly displays "7 days since the last accident." A statistician reads that
and quietly walks away.
Best Supporting Case: The "7 days" example; the bus-stop "time since last bus" sign; the Berlin Wall.
Psychology Angle: How a single number implies a whole timescale.
Math Angle: The doubling rule; Bayes with an uninformative prior.
Sports Angle: "We're due" reasoning; predicting a streak's remaining length.
AI Angle: Priors from one data point; why "no assumptions" is an assumption.
```

```
Idea: Little orphan Annie was a great statistician
Format: YouTube Short
Core Concept: Laplace's Law and large-n certainty.
Hook: "The sun'll come out tomorrow." A cheesy showtune — and a mathematically airtight prediction.
Best Supporting Case: The Annie epigraph; ~1.6 trillion sunrises → ~100%.
Psychology Angle: When childlike certainty is actually justified.
Math Angle: (w+1)/(n+2) as n grows huge.
Sports Angle: Long track records vs. rookie small samples.
AI Angle: Laplace smoothing; confidence with lots vs. little data.
```

---

## Recommended Changes to the Original Extraction

1. **§7 (Cases and Stories)** — add three cases: Little Annie and the sunrise (the epigraph → Laplace
   payoff loop), "7 days since the last accident," and the bus-stop "time since last bus" sign. The Annie
   loop and the accident sign are the highest-value additions.

2. **§12 (Quotable Ideas)** — add the Annie "sun'll come out tomorrow" epigraph, the two Hume epigraphs
   (the problem of induction), the Danish "difficult to make predictions… about the future" proverb, and
   the Wittgenstein "buy several copies of the morning paper" image.

3. **§3 / §5 (Bayes → Laplace)** — foreground *why* Laplace was needed: Bayes/Price left you with
   "probabilities of probabilities" and couldn't answer "what are the odds *actually*?" — the metaprobability
   head-spin that Laplace's single number resolved.

4. **§3 / card 5 (Copernican mechanism)** — make the two-part derivation explicit: the observation
   *rules out* hypotheses shorter than the observed age (like tails ruling out a two-headed coin), while
   very long spans survive but are improbable coincidences.

5. **§2 / card 2 (Laplace ↔ uninformative prior)** — tie Laplace's Law explicitly to its uniform-prior
   assumption (per the footnote), connecting it to the Copernican Principle as the chapter's two
   uninformative-prior methods.

6. **§9 / §11 (gambling contrast)** — add the full three-distribution gambling illustration (normal →
   your number's coming then quit; power-law → keep after a win, quit after a drought; memoryless →
   nothing changes, no right time to quit) as the single clearest "why the distribution matters" example.

7. **§13 / §16 (media argument nuance)** — sharpen: direct experience is *automatically*
   frequency-calibrated and priors are locally adaptive to one's ecological niche; it is *language/media*
   that decouples talk from experience and de-calibrates priors — bias per se is not the villain.

8. **§2 / §19 (scope of "good Bayesians")** — carry the "except where priors are poor (pharaohs)"
   boundary with every strong statement that people are good intuitive Bayesians.

9. **§9 / card 15 (marshmallow hedge)** — preserve the chapter's "may be, at least in part" hedge in the
   analytic entries (keep the strong version only for content hooks).

10. **§5 (Tenenbaum experiment attribution)** — flag that "Tom" is co-author Tom Griffiths; this is
    first-person authorial work, not a neutral citation.

**Sections that are fine as they stand:** §1 (thesis), §6 (experiments — the alternative-explanation
fields do real work, especially the "learned heuristic vs. full distribution" reading), §8 (teaching
examples), §10 (unique ideas), §14 (mathematics — the Laplace-smoothing and preferential-attachment
mappings are precise), §17 (content opportunities). §15 (sports) correctly notes the one direct mention
(softball) and separates inferred applications.
