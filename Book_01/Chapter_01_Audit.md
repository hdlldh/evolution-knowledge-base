# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 1: Optimal Stopping — When to Stop Looking
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 17–46, re-read against Chapter_01_Extraction.md
**Date:** 2026-07-19

---

## Missing Items

**1. The Barbara Bush epigraph is an unremarked counterexample.** (PDF p. 24, epigraph to "Lover's
Leap") "I married the first man I ever kissed. When I tell this to my children they just about throw
up." The extraction captured no epigraphs at all, but this one is not decoration — it is a real-world
case of a *zero-percent look phase* producing a long successful marriage, placed by the authors
immediately before the section arguing for a 37% look phase. The chapter never addresses the tension;
neither did the extraction. This is the single most reusable thing the first pass dropped.

**2. The epigraph structure generally.** Each section is framed by literary/historical quotations —
Kepler and Jane Austen (*Emma*, "why should you hesitate?") open the chapter; Malthus and Barbara Bush
open "Lover's Leap"; Clark Kerr (UC Berkeley president, 1958–67) opens "When to Park" with "the three
major administrative problems on a campus are sex for the students, athletics for the alumni, and
parking for the faculty"; Stephen Grellet and Annie Dillard ("Spend the afternoon. You can't take it
with you.") open "Always Be Stopping." This is a deliberate rhetorical device — pairing formal results
with the humanistic tradition that got there first, or didn't. Section 10 (unique ideas) missed it and
section 12 has no epigraph entries.

**3. The authors' own hedge on the burglar analogy.** (PDF p. 38) They write "with apologies to
Russian oligarchs" when applying the burglar problem to Berezovsky. The extraction flagged the
Berezovsky reading as interpretive in section 11 but did not record that the *authors themselves*
signal the analogy is loose. That matters for evidence-strength bookkeeping: the chapter is not
claiming Berezovsky was solving a burglar problem.

**4. Kepler's fuller lament.** (PDF p. 26) "Was there no other way for my uneasy heart to be content
with its fate than by realizing the impossibility of the fulfillment of so many other desires?" The
extraction has his "restlessness and doubtfulness" but not this, which is a sharper statement of the
psychological cost of an extended look phase — the searcher only settles by conceding that most options
are unreachable. Reusable for section 13.

**5. The "motivated seller" aside.** (PDF p. 31) "There's a reason why home buyers look for
'motivated' sellers." A one-line concrete illustration that deadlines force thresholds down, which the
extraction states abstractly but doesn't illustrate.

**6. The heist-movie line.** (PDF p. 38) "The fact that this problem has a solution is bad news for
heist movie screenplays: when the team is trying to lure the old burglar out of retirement for one
last job, the canny thief need only crunch the numbers." Minor, but a ready-made hook and the most
naturally viral framing of the burglar problem in the chapter.

**7. The scope list of applications.** (PDF p. 18) Optimal stopping is said to have implications "not
only for lovers and renters, but also for drivers, homeowners, burglars, and beyond" — the chapter's
own table of contents for its case selection. Worth recording as the author's claimed scope.

**8. Michael Trick's epistemic caveat.** (PDF p. 25) "I didn't know if she was Perfect (the
assumptions of the model don't allow me to determine that), but there was no doubt that she met the
qualifications for this step of the algorithm." The extraction has the proposal but not this line,
which is Trick correctly noting the model gives a *procedure*, not a verdict about the person. It is
the cleanest statement in the chapter of what an algorithm does and doesn't deliver.

## Corrections Needed

**1. Parking distance at 99% occupancy — dropped hedge.**
- Extraction (§3, §4, card 13): "~70 spots (over a quarter mile)".
- Chapter (PDF p. 36): "you should take the first spot you see starting at *almost* 70 spots—more
  than a quarter mile—from your destination."
"Almost 70" became "~70," which is fine, but "starting at" was compressed into a point estimate. The
chapter describes where the leap phase *begins*, not where you park.

**2. The 85% parking figure is Shoup's target, not a derived optimum.**
- Extraction (§9, card 13) reads close to "85% is the efficient target."
- Chapter (PDF p. 35): "Shoup *argues* that this rate should be somewhere around 85%."
The extraction does attribute it to Shoup, but the hedge "somewhere around" and the fact that it is an
argued policy position rather than a computed result should be explicit.

**3. Section 5, "seminal 1966 paper" — the quotation's scope.**
The extraction says it was quoted "to the effect that no buildup of experience is needed." The chapter
gives the actual quoted words, and the quotation is doing more work than the extraction implies: it is
the source of the claim that a profitable choice can *sometimes* be made immediately — "sometimes"
being the load-bearing word that the Threshold Rule then makes precise. Not wrong, but under-specified.

## Overgeneralizations

**1. "Success rate is invariant to pool size" needs its convergence caveat.** The extraction (§9,
card 5) states 37% flatly for 100 and for a million. The chapter's own table (PDF p. 23) shows the
success rate *converging* on 37% as applicants increase — for small pools it is higher (50% at n=2 and
n=3). The extraction's framing is accurate for large pools and wrong for small ones, which are exactly
the pools most real decisions have.

**2. "People stop too early — about a dozen studies."** The extraction's §3 entry marks the dozen-study
count as weakly supported, which is right, but §19 ("Top 3 Claims") and card 18 present premature
stopping as settled. The chapter's actual evidentiary base in-text is one study plus an uncited count.

**3. "Never look back" stated without its domain.** Card 11 and §9 give the rule crisply. The chapter
attaches it specifically to "house selling and job hunting" — cost-of-waiting problems with a
total-value objective. The extraction does note the tension with the recall variant, but the rule
itself should carry its domain restriction wherever it appears, or it will be miscompared against other
books' advice on reconsidering decisions.

## Important Nuance Lost

**1. The 37% Rule requires knowing the horizon.** Trick had to *assume* a search window of ages 18–40
to get 26.1. The chapter shows this in the narrative but never states it as an assumption; the
extraction inherited the omission. In practice, not knowing n (or the time window) is the most common
reason the rule can't be applied as stated.

**2. The full-information game's two premises are stated once and then dropped.** (PDF pp. 27–28) The
chapter explicitly supposes (a) the applicant pool is representative of the population and "isn't
skewed or self-selected in any way," and (b) that we "decide that typing speed is the *only* thing
that matters." The extraction records these under the Threshold Rule's limitations but does not attach
them to the "gold digging" claim, which is where they matter most — a dating pool is self-selected
almost by definition.

**3. The house-selling model's cost structure is a simplification the authors flag.** (PDF p. 31)
"Here we'll analyze one of the simplest cases: where we know for certain the price range in which
offers will come, and where all offers within that range are equally likely." The extraction has this,
but the authors' framing — this is the *simplest* case, chosen for tractability — should be preserved
so the $499,552.79 precision isn't mistaken for realism.

**4. Rapoport & Seale's participants got the *form* right.** "Most people acted in a way that was
consistent with the Look-Then-Leap Rule" (PDF p. 40). The extraction captures this, but the framing
throughout leans on "people stop too early"; the more interesting and better-supported finding is that
untrained humans spontaneously adopt the right algorithmic structure and miscalibrate only its single
parameter. That inversion is under-weighted in §19 and in the content ideas.

**5. Berezovsky's death is reported with the postmortem's conclusion, not as fact.** The chapter says
"the official conclusion of a postmortem examination was that he had committed suicide." The extraction
reproduces this correctly in §7 but card 16 says "a death ruled suicide," which is fine — flagging only
so it stays hedged in translation and in any downstream content.

## Additional Cases and Examples

```
Case Title: Barbara Bush married the first man she ever kissed
People / Organization: Barbara Bush (epigraph)
Context: Placed as an epigraph to "Lover's Leap," the section that derives the 37% Rule's application
to courtship.
What Happened: "I married the first man I ever kissed. When I tell this to my children they just about
throw up."
Outcome: Not stated in the chapter; the quotation's tone implies a marriage she was happy with. A
zero-look-phase search that evidently succeeded.
Concept Illustrated: The gap between an optimal *strategy* and a good *outcome*; the 37% Rule maximizes
the probability of the best match, and its 63% failure rate means individual counterexamples are
expected rather than disconfirming.
Why This Case Is Useful: It is the chapter's own counterexample, sitting in plain sight and never
addressed. Perfect for a "but what about…" beat in any content built on the 37% Rule, and it teaches
the process-vs-outcome distinction better than an abstraction can.
Potential for Reuse: High
```

```
Case Title: Clark Kerr on the three problems of a university
People / Organization: Clark Kerr, President of UC Berkeley, 1958–1967 (epigraph)
Context: Epigraph to "When to Park."
What Happened: "I find that the three major administrative problems on a campus are sex for the
students, athletics for the alumni, and parking for the faculty."
Outcome: N/A — an aphorism.
Concept Illustrated: That parking is a genuinely hard and universally felt problem, setting up the
section's claim that it deserves real analysis.
Why This Case Is Useful: A ready-made laugh line to open a segment on parking, from a credible
institutional source.
Potential for Reuse: Medium
```

```
Case Title: The one-last-job trope, solved
People / Organization: None — a genre observation
Context: Introducing the burglar problem.
What Happened: The authors observe that the existence of a solution is "bad news for heist movie
screenplays" — the retired thief being lured into one last job need only crunch the numbers.
Outcome: N/A.
Concept Illustrated: The burglar problem; quit-while-ahead.
Why This Case Is Useful: The most immediately graspable framing of the burglar problem in the chapter,
and it borrows an audience's existing familiarity with the trope. Strong short-form hook.
Potential for Reuse: High
```

## Additional Research Evidence

None identified. The re-read surfaced no study, dataset, or citation absent from section 5. The
chapter's evidentiary base is genuinely thin relative to its number of claims — two experimental
findings (both Rapoport/Seale), one archival investigation by the authors themselves, and several
mathematical results asserted without derivation. That thinness is itself the finding, and section 3
of the extraction reflects it correctly.

## Potential Disagreements to Track Later

1. **Herbert Simon / satisficing.** The chapter's entire classical analysis assumes a maximizing
   objective (only the single best counts). Simon's argument is that real agents satisfice, and under a
   satisficing objective the prescription changes substantially. The chapter never mentions Simon
   despite this being the most direct challenge to its setup.
2. **Barry Schwartz, *The Paradox of Choice*.** Schwartz argues more options degrade both outcomes and
   satisfaction; the chapter's pool-size invariance result is a formal counterweight. A direct
   cross-book collision.
3. **Gerd Gigerenzer and the fast-and-frugal heuristics program.** Gigerenzer argues simple heuristics
   are ecologically rational and that optimization models are the wrong normative standard. The
   chapter's endogenous-time-cost argument is *sympathetic* to Gigerenzer while its overall framing
   (compute the optimum, then follow it) is not — an interesting partial alignment rather than a clean
   disagreement.
4. **Kahneman and Tversky / behavioral economics.** The chapter explicitly pushes back on the
   "buggy brain" narrative, continuing the introduction's argument. Track how consistently the book
   sustains this across chapters — chapter 7 (Overfitting) and chapter 9 (Randomness) are likely to
   revisit it.
5. **Two-sided matching theory (Gale–Shapley, deferred acceptance).** The courtship application models
   partners as passive applicants. Matching theory models both sides as searching agents and produces
   quite different prescriptions. The chapter acknowledges rejection as a variant but not two-sidedness
   as a structural fact.
6. **Behavioral finance on sunk cost and loss aversion.** "Never look back" is a strong prescriptive
   claim about ignoring sunk costs; the descriptive literature says people cannot, and some of that
   literature argues the persistence has adaptive value.

## Additional Content Opportunities

```
Idea: The First Kiss Problem — when the math says look, and the person who didn't look was happy
Format: YouTube Short
Core Concept: Good process vs. good outcome; the 63% failure rate
Hook: Barbara Bush married the first man she ever kissed. The math says she had almost no chance of
finding her best match. It worked out anyway.
Note: the chapter gives only the quotation — any biographical detail beyond it would need sourcing
outside this book.
Best Supporting Case: The Bush epigraph against the Kepler and Trick stories.
Psychology Angle: Outcome bias — we judge decisions by how they turned out.
Math Angle: A strategy that fails 63% of the time will produce a great many happy counterexamples.
Sports Angle: Judging a manager's in-game decision by whether the shot went in.
AI Angle: Evaluating a policy by a single rollout rather than expected return.
```

```
Idea: The epigraph game — poets got there first, but without the number
Format: Community Post
Core Concept: The chapter's own rhetorical device
Hook: Jane Austen: "why should you hesitate?" Annie Dillard: "Spend the afternoon. You can't take it
with you." Computer science: 37%.
Best Supporting Case: The chapter's epigraph set as a whole.
Psychology Angle: Why quantified advice feels different from identical advice given qualitatively.
Math Angle: The introduction's own line — the therapist says find the balance, the algorithm says the
balance is 37%.
Sports Angle: None identified.
AI Angle: None identified.
```

---

## Recommended Changes to the Original Extraction

1. **§7 (Cases and Stories)** — add the three cases above: Barbara Bush, Clark Kerr, and the
   heist-movie trope. The Bush case is the highest-value addition in this audit.

2. **§9 (Counterintuitive Insights)** — amend the pool-size invariance entry to state that the 37%
   figure is a *limit* the success rate converges to as the pool grows; for two or three applicants the
   optimal success rate is 50%. Add: "The invariance claim holds for large pools."

3. **§11 (Tensions)** — add a new entry: the Barbara Bush epigraph is an unremarked counterexample
   placed by the authors themselves directly above the argument it complicates. Author's position:
   never addressed. Counterargument: none needed — a 63% failure rate predicts abundant happy
   counterexamples, but the chapter never uses the epigraph to make that point, leaving a reader to
   experience it as a contradiction rather than as an illustration.

4. **§3 (Key Claims)** — on the burglar-problem/Berezovsky claim, record that the authors write "with
   apologies to Russian oligarchs," i.e. they signal the analogy is loose. Downgrade nothing; add the
   hedge.

5. **§3 and §4** — on the parking claims, restore "almost 70 spots" and "starting at," and change the
   85% phrasing to "Shoup argues it should be somewhere around 85%."

6. **§4 (Frameworks)** — add to the 37% Rule's limitations: "Requires knowing the size of the pool or
   the length of the search window; Trick had to assume an 18–40 range to compute 26.1."

7. **§4 (Threshold Rule) and §9 (gold digging)** — attach the two stated premises to the gold-digging
   insight specifically: a representative, non-self-selected pool and a single criterion that is
   genuinely all that matters. Note that a dating pool violates the first almost by construction.

8. **§12 (Quotable Ideas)** — add Trick's "the assumptions of the model don't allow me to determine
   that," Kepler's "was there no other way for my uneasy heart," and Dillard's "Spend the afternoon.
   You can't take it with you."

9. **§13 (Psychology Connections)** — add outcome bias, prompted by the Bush counterexample: the
   chapter's 63% failure rate is precisely an argument for separating decision quality from outcome
   quality, and the chapter never names the bias.

10. **§19 (Cross-Book Summary)** — under "Biggest Weakness," add that the chapter's evidentiary base is
    two findings from a single research pair plus asserted mathematical results, which is thin relative
    to the number and breadth of its prescriptions.

11. **§17 (Content Opportunities)** — add the "First Kiss Problem" short; it is the strongest new seed
    the re-read produced.

**Sections that are fine as they stand:** §1 (thesis), §5 (research — genuinely complete), §6
(experiments), §14 (mathematics), §18 cards other than 5, 11, 13, and 16. §15 (sports) is correctly
marked as containing no direct examples from the book.
