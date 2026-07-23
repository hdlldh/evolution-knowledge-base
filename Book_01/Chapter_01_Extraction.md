# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 1: Optimal Stopping — When to Stop Looking
**Author:** Brian Christian and Tom Griffiths
**Type:** Extraction
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 17–46 (book chapter 1, incl. footnotes)
**Date:** 2026-07-19
**Revision note:** Revised after Chapter_01_Audit.md; see that file for what changed and why.

```
BOOK:
Algorithms to Live By: The Computer Science of Human Decisions

AUTHOR:
Brian Christian and Tom Griffiths

CHAPTER:
1 — Optimal Stopping: When to Stop Looking
```

---

## 1. Chapter Thesis

A large class of everyday dilemmas — dating, hiring, apartment hunting, house selling, parking,
quitting while ahead — share one mathematical structure: options arrive sequentially, and the real
question is never *which* option to pick but *how many options to consider before committing*.
Computer science has solved many of these "optimal stopping" problems, and the solutions are
explicit, computable, and often counterintuitive (look at 37% of options, then leap). The authors
argue that because time is strictly one-directional, optimal stopping is not a niche puzzle but the
implicit structure of being alive — and that high failure rates are an unavoidable property of these
problems rather than evidence of human irrationality.

## 2. Key Concepts

```
Concept Name: Optimal Stopping
Definition: The class of sequential decision problems concerned with choosing the right *time* to take
a given action, where options arrive one at a time and passing on one is (usually) irrevocable.
Why It Matters: Reframes "which should I choose?" as "when should I stop looking?" — a different and
tractable question.
How the Author Uses It: The organizing frame for the whole chapter; every case (love, real estate,
parking, crime, quitting) is presented as an instance of it.
Related Concepts: Secretary problem, 37% Rule, Look-Then-Leap Rule, Threshold Rule, explore/exploit
(chapter 2).
```

```
Concept Name: The Secretary Problem
Definition: Canonical optimal stopping puzzle — interview n applicants in random order, observe only
relative rank (ordinal, not cardinal), accept or reject irrevocably on the spot, goal is to maximize
the probability of selecting the single best applicant in the pool.
Why It Matters: Its assumptions are what make the 37% answer exact; relaxing each assumption generates
a family of different, also-solvable problems.
How the Author Uses It: Baseline model. The chapter proceeds by systematically breaking its
assumptions (rejection possible, recall possible, full information, cost of waiting) and showing how
the optimal strategy changes.
Related Concepts: No-information game, full-information game, ordinal vs. cardinal information.
```

```
Concept Name: The 37% Rule
Definition: In the classical secretary problem, look at (and reject) the first ~37% of applicants,
then accept the next applicant who is better than everyone seen so far. Precisely, the optimal
proportion is 1/e ≈ 0.3679.
Why It Matters: Converts a vague intuition ("balance looking and leaping") into a specific number.
How the Author Uses It: The chapter's headline result and its bridge from the introduction's apartment
example. The authors note the rule applies to *time* as well as to counts of applicants.
Related Concepts: Look-Then-Leap Rule, 1/e, the mathematical constant e.
```

```
Concept Name: Look-Then-Leap Rule
Definition: A two-phase strategy — a predetermined non-committal "look" phase in which nothing is
chosen regardless of quality, followed by a "leap" phase in which you instantly commit to the first
option that beats everything seen in the look phase.
Why It Matters: The structural form of the optimal solution across the no-information variants, not
just the 37% case.
How the Author Uses It: Bolded as a named algorithm (the book's convention for algorithms). Shown to
persist under the rejection and recall variants, and to govern optimal parking; replaced by the
Threshold Rule once full information is available.
Related Concepts: 37% Rule, Threshold Rule, exploration phase.
```

```
Concept Name: Threshold Rule
Definition: When you have full information (an objective, population-calibrated score for each
option), skip the look phase entirely and accept the first option above a pre-computed percentile
threshold — a threshold that falls as remaining options dwindle.
Why It Matters: Shows that the look phase exists only because of missing information, not because
"gathering data" is intrinsically wise.
How the Author Uses It: The pivot of the chapter's middle section; source of the "gold digging beats
a quest for love" line and the "lower your standards in slim pickings" advice.
Related Concepts: Full-information game, percentile, house-selling problem.
```

```
Concept Name: No-Information vs. Full-Information Games
Definition: No-information games give only relative rankings between observed options; full-information
games give each option's standing relative to the whole population (e.g. a percentile score).
Why It Matters: Information structure, not the domain, determines which algorithm is optimal and how
often you can expect to succeed (37% vs. 58%).
How the Author Uses It: The chapter's main axis of variation. Also used normatively: seek out
yardsticks that convert a no-information search into a full-information one.
Related Concepts: Ordinal vs. cardinal numbers, Threshold Rule, Look-Then-Leap Rule.
```

```
Concept Name: Endogenous Time Cost of Search
Definition: The cost of continuing to search that arises from the searcher's own life rather than from
the problem's stated rules — boredom, opportunity cost, work not done while interviewing.
Why It Matters: Offers a rationality-preserving explanation for the robust laboratory finding that
people leap too early.
How the Author Uses It: To reinterpret an apparent human failure as a rational response to a cost the
model omitted. Bearden is quoted noting it is "not irrational to get bored, but it's hard to model
that rigorously."
Related Concepts: Bounded rationality, cost of waiting in the house-selling problem, sunk cost.
```

```
Concept Name: Cost of Waiting / Stopping Price
Definition: In the house-selling problem, an explicit function converting the per-offer cost of waiting
into a fixed acceptance threshold; it depends only on the cost of search and the spread between the
highest and lowest likely offers.
Why It Matters: Yields the striking property that the threshold never changes during the search — set
once, then hold.
How the Author Uses It: To justify not lowering standards as rejections accumulate, and to derive the
"never go back to a passed-over offer" rule.
Related Concepts: Sunk cost, job search models, reservation wage.
```

```
Concept Name: Occupancy Rate (Parking)
Definition: The proportion of parking spots currently occupied; the single number that most determines
the difficulty and optimal strategy of a parking search.
Why It Matters: Turns a policy question (price of curb parking) into a search-cost question.
How the Author Uses It: Via Donald Shoup's work, to argue that near-100% occupancy is a policy failure
and that ~85% should be the target; and to parameterize the parking Look-Then-Leap distance.
Related Concepts: Congestion, adaptive pricing, externalities.
```

```
Concept Name: The Burglar Problem
Definition: A stopping problem in which each repetition yields a reward but carries a probability of
total loss; the optimal number of attempts is approximately (chance of success) / (chance of failure).
Why It Matters: Gives a computable form to the folk advice "quit while you're ahead."
How the Author Uses It: Applied — with explicit apology for the analogy — to Boris Berezovsky's
trajectory from mathematician to oligarch to exile.
Related Concepts: Ruin problems, risk of ruin, expected value.
```

```
Concept Name: Problems With No Optimal Stopping Rule
Definition: Sequential decision problems in which expected value strictly increases with each
additional round, so the math says always continue — even though continuing forever guarantees ruin.
Illustrated with "triple or nothing."
Why It Matters: A limit case marking the boundary of the chapter's own toolkit; the authors' response
is "some problems are better avoided than solved."
How the Author Uses It: As a coda to the Berezovsky story and a check on the chapter's optimism.
Related Concepts: St. Petersburg paradox (not named in the chapter), expected value vs. ruin,
Kelly criterion (not named in the chapter).
```

## 3. Key Claims

```
Claim: In optimal stopping problems, the crucial dilemma is how many options to consider, not which
option to pick.
Type: Theoretical
Evidence Provided: Structural argument plus worked cases across five domains.
Strength of Support: Strong (as a framing claim about the model class; it is definitional rather than
empirical).
```

```
Claim: The optimal strategy in the classical secretary problem is to look at the first 1/e (~37%) of
applicants and then take the next best-yet, yielding a ~37% success rate that is invariant to pool size.
Type: Theoretical (mathematical result)
Evidence Provided: Informal derivation via the 1-, 2-, 3-, 4-, 5-applicant cases; a table of optimal
strategies converging on 37%; footnote specifying 1/e and noting anything between 35% and 40% is
near-optimal. Full derivation deferred to the endnotes.
Strength of Support: Strong (a proved theorem, though the chapter itself presents only a sketch).
```

```
Claim: Even acting optimally, you fail 63% of the time in the classical secretary problem.
Type: Theoretical
Evidence Provided: Follows directly from the 37% result; presented as a "sobering fact" and as bad
news for framing romance as a search for "the one."
Strength of Support: Strong.
```

```
Claim: With a 50/50 chance of rejection, you should begin proposing after ~25% of the search and keep
proposing to every best-yet candidate; success rate is also 25%.
Type: Theoretical
Evidence Provided: Asserted as the output of the same kind of analysis; no derivation shown.
Strength of Support: Moderate (result stated, not demonstrated in-chapter).
```

```
Claim: If recall is possible (immediate proposals certain, belated proposals accepted half the time),
look until 61% of applicants, leap only in the remaining 39%, and fall back to the best one that got
away; success rate ~61%.
Type: Theoretical
Evidence Provided: Asserted; the strategy/outcome symmetry is noted but not explained.
Strength of Support: Moderate (result stated, not demonstrated).
```

```
Claim: Restlessness and doubt are not moral or psychological defects but part of the optimal strategy
when second chances exist.
Type: Interpretive
Evidence Provided: The recall-variant result, applied to Kepler's self-reproach.
Strength of Support: Moderate. The math licenses a longer look phase; recasting Kepler's stated
anguish as optimality is the authors' interpretive move, not a result.
```

```
Claim: With full information the Threshold Rule applies, no look phase is needed, and the success rate
rises to 58% even as the pool grows arbitrarily large.
Type: Theoretical
Evidence Provided: Backward-induction walkthrough (last applicant forced; next-to-last if >50th
percentile; third-to-last if >69th; fourth-to-last if >78th), plus a thresholds table. Cites the
"seminal 1966 paper" for the phrase about no buildup of experience being needed.
Strength of Support: Strong for the math; the 58% figure is asserted rather than derived.
```

```
Claim: "Gold digging is more likely to succeed than a quest for love."
Type: Interpretive (deliberately provocative)
Evidence Provided: The 58% vs. 37% gap, on the premise that income percentile is objectively knowable
while love is a "nebulous emotional response" requiring calibration.
Strength of Support: Weak as stated. It holds only under the model's assumptions (single criterion,
representative unskewed pool, goal of getting the single best). The authors flag it as "unexpected and
somewhat bizarre" and immediately generalize away from net worth to "any yardstick."
```

```
Claim: In the house-selling problem the acceptance threshold depends only on the cost of search, is
set before the search begins, and should never be lowered as the search goes on.
Type: Theoretical
Evidence Provided: Worked example over a $400k–$500k offer range: $1 waiting cost → hold for
$499,552.79; $2,000 → $480,000; $10,000 → $455,279; $50,000 (half the range) → accept the first offer.
Strength of Support: Strong within the stated simplifying assumptions (known price range, uniform
offers, unlimited offers and savings). The authors explicitly note that if savings or offers will run
out, standards *should* fall as those limits approach.
```

```
Claim: In house selling and job hunting you should never return to a previously rejected offer, even
if it is guaranteed still available.
Type: Prescriptive
Evidence Provided: The constancy of the threshold plus a sunk-cost argument.
Strength of Support: Strong given the model; note it directly inverts the recall-variant advice given
for Kepler, and the chapter does not reconcile the two.
```

```
Claim: Parking is an optimal stopping problem solved by Look-Then-Leap, with the switch distance
determined by occupancy rate — at 99% occupancy you should be prepared to take the first spot you see
*starting at* almost 70 spots (more than a quarter mile) from the destination; at 85% you needn't
start seriously looking until half a block away.
Type: Theoretical
Evidence Provided: Model of an infinitely long road with evenly spaced spots and a table of distances
by occupancy.
Strength of Support: Moderate. The authors concede "most of us don't drive on perfectly straight,
infinitely long roads" and list studied tweaks (U-turns, spot density falling near the destination,
rival drivers).
```

```
Claim: Shoup argues the target occupancy should be "somewhere around 85%," achieved via
demand-responsive meter pricing; going from 90% to 95% occupancy accommodates 5% more cars but doubles
everyone's search length.
Type: Empirical / Prescriptive (attributed to Shoup)
Evidence Provided: Shoup's argument and his book *The High Cost of Free Parking*; noted as implemented
in downtown San Francisco. No study design, sample, or measured outcome is given.
Strength of Support: Moderate as reported. The doubling figure is stated without derivation or
citation in the chapter text.
```

```
Claim: The optimal number of robberies is roughly (chance of getting away) / (chance of getting
caught) — 9 for a 90% success rate, ~1 for 50/50.
Type: Theoretical
Evidence Provided: Stated as a result, called "pretty intuitive"; no derivation.
Strength of Support: Moderate. Note that when the authors apply this to Berezovsky they write "with
apologies to Russian oligarchs" — they signal the analogy is loose rather than claiming he faced a
burglar problem.
```

```
Claim: Some sequential problems have no optimal stopping rule; in "triple or nothing" the math says
always play, yet following it guarantees eventual ruin.
Type: Theoretical
Evidence Provided: Expected-value walkthrough ($1 → $1.50 expected; second bet → $4.50 expected).
Strength of Support: Strong, and notable because the authors use it against their own framework:
"Some problems are better avoided than solved."
```

```
Claim: People systematically stop too early — about a dozen studies agree.
Type: Empirical
Evidence Provided: Rapoport & Seale (1990s), 40- or 80-applicant pools, repeated trials: 31% success
(vs. 37% optimal), behavior broadly consistent with Look-Then-Leap, but leaping too soon more than
four-fifths of the time. The "about a dozen studies" is a summary count with no individual citations.
Strength of Support: Moderate to Strong for the direction of the effect; Weak for the specific
"dozen studies" figure as presented.
```

```
Claim: Early stopping may be rational rather than a bias, because searchers carry an endogenous time
cost the experiment does not impose.
Type: Interpretive / Empirical
Evidence Provided: Seale & Rapoport showed that assuming a per-applicant cost of 1% of the value of
finding the best secretary makes the optimal strategy align exactly with observed switch points.
Strength of Support: Moderate. The fit is post hoc — the cost parameter was chosen to reproduce
observed behavior, and the authors themselves note there was no actual search cost in the study.
```

```
Claim: Because time is strictly one-directional, all decision-making is ultimately optimal stopping.
Type: Interpretive / Speculative
Evidence Provided: Philosophical argument that seriality is the nature of time; no formal support.
Strength of Support: Weak as a literal claim, strong as a framing device. This is the chapter's
closing rhetorical move.
```

## 4. Frameworks, Models, and Mental Models

```
Name: The 37% Rule / Look-Then-Leap Rule
Description: Two-phase optimal stopping strategy for no-information sequential choice.
Components: (1) Look phase — a fixed fraction (~37%, or 1/e) of the pool or of the available time,
during which you reject everything and record the best seen. (2) Leap phase — accept the first option
exceeding that benchmark. (3) Fallback — if nothing qualifies, you are stuck with the last option.
How It Works: Balances two failure modes: stopping early (best applicant never seen) and stopping late
(holding out for someone who does not exist). Best-yet candidates get better but rarer as the search
proceeds; 1/e is where the two effects trade off optimally.
When It Is Useful: Sequential, irrevocable choice with a known horizon, no objective scale, and a goal
of the single best outcome. Applies to time windows as well as counts (Michael Trick converted an
18–40 dating window into age 26.1).
Limitations: Assumes applicants always accept, no recall, random order, known pool size, only relative
ranks observable, and that only the single best counts as success. Fails 63% of the time even when
followed exactly. Ignores any cost of search. Requires knowing the size of the pool or the length of
the search window — Trick had to *assume* an 18-to-40 range to compute 26.1, and not knowing the
horizon is the most common practical obstacle to applying the rule.
```

```
Name: The Threshold Rule (Full Information)
Description: Accept immediately anything above a pre-computed percentile cutoff that declines as
remaining options run out.
Components: An objective population-calibrated score per option; a schedule of declining thresholds
indexed to how many options remain.
How It Works: With full information you can compute directly the odds that a better option remains, so
the decision reduces to how many options are left. Derived by backward induction: last applicant —
forced; next-to-last — take if >50th percentile; third-to-last — >69th; fourth-to-last — >78th; and so
on, more selective the more remain.
When It Is Useful: Whenever any yardstick locates an option against the whole population — test scores,
income percentile, market comparables.
Limitations: The chapter states two premises explicitly and then drops them: the pool must be
representative of the population and "isn't skewed or self-selected in any way," and a single
criterion (typing speed) must be decided to be "the only thing that matters." Both are load-bearing
for the gold-digging claim, and a dating pool violates the first almost by construction. Still yields
only 58% success. Never hire below average unless
out of options; never hire someone who is not the best seen so far.
```

```
Name: House-Selling / Cost-of-Waiting Model
Description: Set a fixed reservation price from the cost of search, then hold it.
Components: Known offer range (min, max); uniform arrival of offers within it; a per-offer cost of
waiting; goal is total money, not the single best offer.
How It Works: Continue only if (probability of a better offer × size of the improvement) exceeds the
cost of waiting. Yields an explicit stopping price as a function of waiting cost. Depends only on the
spread between highest and lowest likely offers — not on the absolute value of the asset.
When It Is Useful: Any series of offers where waiting is costly — selling property, job search
(economists use it to explain simultaneous unemployment and unfilled vacancies).
Limitations: Assumes known range, uniform likelihood, no deadline, unlimited offers. Explicitly
requires lowering standards when savings or offers are about to run out. The "never look back" rule
follows from these assumptions, not from psychology.
```

```
Name: Parking Search Model (Shoup / Look-Then-Leap)
Description: On an infinitely long road with evenly spaced spots, pass all vacancies beyond a critical
distance from the destination, then take the first vacancy inside it.
Components: Occupancy rate; distance from destination; goal of minimizing walking distance.
How It Works: The switch distance is a function of occupancy — 99% occupancy → start taking spots ~70
spots (>¼ mile) out; 85% → about half a block out.
When It Is Useful: Directly for parking; more broadly as a template for "constant forward motion"
searches (restaurants, bathrooms on a road trip).
Limitations: Idealized geometry. Studied variants relax it (U-turns allowed, fewer spots near the
destination, competing drivers). Shoup also notes parking has a game-theoretic component (chapter 11).
```

```
Name: Burglar Problem (Quit-While-Ahead Model)
Description: Optimal number of repeated risky attempts ≈ (probability of success) / (probability of
ruin).
Components: Per-attempt reward; per-attempt probability of total loss of accumulated gains.
How It Works: 90% success rate → stop after ~9 attempts. 50/50 → essentially do it once and stop.
When It Is Useful: Repeated ventures with an absorbing failure state — reputational, legal, financial.
Limitations: Assumes constant per-attempt odds and total loss on failure. Says nothing about attempts
whose odds change with experience or notoriety.
```

## 5. Research and Evidence

```
Study / Research: Laboratory secretary-problem experiments
Researchers: Amnon Rapoport (UC Riverside) and Darryl Seale
Year: 1990s (exact year not specified)
Research Question: Do people follow the optimal stopping rule in the classical secretary problem?
Method: Repeated trials of the secretary problem with either 40 or 80 applicants per repetition.
Key Finding: Overall success rate ~31% (vs. 37% optimal). Behavior was mostly consistent with the
Look-Then-Leap Rule, but participants leapt earlier than optimal more than four-fifths of the time.
How the Author Uses It: As the chapter's main evidence that humans stop too early, and then as the
setup for the endogenous-time-cost reinterpretation.
Important Limitations: Laboratory task with no real stakes and no imposed search cost; participant
count, recruitment, and incentive structure are not specified in the chapter.
Replication or Controversy Mentioned: The authors state that "about a dozen studies have produced the
same result" (people stop early) but cite none of them individually.
```

```
Study / Research: Cost-adjusted model fit to the same experimental data
Researchers: Darryl Seale and Amnon Rapoport
Year: Not specified.
Research Question: Can an assumed cost of search reconcile observed early stopping with optimality?
Method: Re-analysis — imposing a hypothetical per-applicant cost of 1% of the value of finding the
best secretary and recomputing the optimal switch point.
Key Finding: The recomputed optimum aligned perfectly with where participants actually switched from
looking to leaping.
How the Author Uses It: To argue people import an endogenous time cost from their own lives into a
costless laboratory task.
Important Limitations: The chapter states there was no search cost in the study design. The 1% figure
appears to be fitted to the observed data rather than independently measured, so the fit is
post hoc — it demonstrates consistency, not that time cost is the actual cause.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Origins of the secretary problem (archival investigation)
Researchers: Brian Christian and Tom Griffiths (the authors), working in Martin Gardner's papers at
Stanford
Year: Problem circulated by ~1955; first known discovery of the 37% Rule by Merrill Flood in 1958;
first print appearance in Gardner's Scientific American column, February 1960; first appearance of the
name "secretary problem" in a 1964 paper.
Research Question: Where did the secretary problem come from?
Method: Reading one side of Gardner's mid-century correspondence — replies to Gardner's own inquiry
about the problem's origins.
Key Finding: The provenance is genuinely tangled. Frederick Mosteller (Harvard) heard it in 1955 from
Andrew Gleason, who heard it from someone else; Leo Moser (Alberta) read it in notes by R. E. Gaskell
of Boeing, who credited a colleague; Roger Pinkham (Rutgers) heard it in 1955 from J. Shoenfield
(Duke), who believed he heard it from "someone at Michigan" — almost certainly Merrill Flood, who
claims to have considered the problem since 1949 but himself points to other mathematicians.
How the Author Uses It: To establish the problem's history and to characterize Flood (also credited
with popularizing the traveling salesman problem, devising the prisoner's dilemma, and possibly
coining "software").
Important Limitations: The authors flag the method's weakness themselves — hearing only one side of a
correspondence and having to infer the other. Attribution to Flood is hedged ("almost certainly").
Replication or Controversy Mentioned: The disputed attribution *is* the finding.
```

```
Study / Research: Seminal full-information secretary problem paper
Researchers: Not specified.
Year: 1966
Research Question: How should one stop when applicants' absolute standing is known?
Method: Not specified.
Key Finding: Quoted to the effect that no buildup of experience is needed to set a standard and a
profitable choice can *sometimes* be made immediately. The hedge is load-bearing — the Threshold Rule
is precisely the specification of when "sometimes" applies.
How the Author Uses It: To introduce the Threshold Rule.
Important Limitations: Cited only by year and description; no authors named in the chapter text.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Berezovsky's monograph on the secretary problem
Researchers: Boris Berezovsky
Year: Not specified.
Research Question: Not specified.
Method: Not specified.
Key Finding: Described as the first and so far only book devoted entirely to the secretary problem.
How the Author Uses It: For the irony that the man who literally wrote the book on optimal stopping
failed to stop.
Important Limitations: No content from the book is discussed.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Shoup's parking research
Researchers: Donald Shoup (UCLA, Distinguished Professor of Urban Planning); book *The High Cost of
Free Parking*
Year: Not specified.
Research Question: What determines the real cost of parking, and what occupancy rate should cities
target?
Method: Not specified in the chapter — a model of the ideal space balancing sticker price, walking
time and inconvenience, search time, and fuel burned, adjusted for number of passengers (who split
money cost but not search or walking time).
Key Finding: Underpriced curb parking drives occupancy toward 100%, producing cruising, wasted fuel,
congestion, and pollution. Target ~85% occupancy via demand-responsive digital meters. Moving from
90% to 95% occupancy accommodates 5% more cars but doubles search length.
How the Author Uses It: To turn parking from a utilization problem into a search-process problem, and
to argue that empty spots on desirable blocks are a sign of success rather than waste.
Important Limitations: No study design, data, or measured outcome is given in the chapter. Presented
as expert argument.
Replication or Controversy Mentioned: Noted as implemented in downtown San Francisco; no evaluation
results are reported.
```

```
Study / Research: Economists' use of the cost-of-waiting model for job search
Researchers: Not specified.
Year: Not specified.
Research Question: Why do unemployed workers and unfilled vacancies coexist?
Method: Not specified.
Key Finding: The optimal-stopping/reservation-threshold model reportedly explains this apparent
paradox "handily."
How the Author Uses It: To generalize the house-selling result beyond real estate.
Important Limitations: No citation, data, or named economist.
Replication or Controversy Mentioned: None identified.
```

## 6. Experiments

```
Experiment Name: Rapoport & Seale repeated secretary problem
Setup: Computer-based repeated secretary problems, 40 or 80 applicants per instance, run in the 1990s.
Participants: Not specified.
Procedure: Participants went through numerous repetitions, each time observing applicants sequentially
and choosing when to stop.
Result: ~31% success rate; strategies broadly matched the Look-Then-Leap form; participants leapt
prematurely in more than four-fifths of trials.
Interpretation: Authors' primary reading is that people are impatient and stop too early; their
secondary and preferred reading is that an unmodeled endogenous time cost makes early stopping
rational.
What It Demonstrates: That untrained human behavior approximates the right *form* of the optimal
algorithm while mis-setting its parameter.
Potential Alternative Explanation: Risk aversion (a decent bird in hand vs. the near-certainty of
ending with the last applicant); misperception of how many good candidates remain; fatigue or boredom
within a repeated laboratory task; the fact that in the real world "second best" is usually fine
whereas the task scores only the single best.
```

```
Experiment Name: The three-applicant enumeration (thought experiment / proof sketch)
Setup: Three applicants, all six possible orderings enumerated: 1-2-3, 1-3-2, 2-1-3, 2-3-1, 3-1-2,
3-2-1.
Participants: N/A — a worked derivation.
Procedure: Look at the first applicant only, then leap for whoever surpasses her.
Result: Succeeds in three of six orderings (2-1-3, 2-3-1, 3-1-2). Fails in the other three: twice by
being overly choosy (1-2-3, 1-3-2), once by not being choosy enough (3-2-1). A 33% risk of dismissing
the best applicant and a 16% risk of never meeting her.
Interpretation: With three applicants you can still succeed exactly half the time — as well as with
two — by exploiting the second applicant's unique position of having both information and agency.
What It Demonstrates: Why the optimal solution takes the Look-Then-Leap form at all, and why the first
applicant carries information but no basis for action while the last carries no agency.
Potential Alternative Explanation: None identified — it is an exhaustive enumeration.
```

## 7. Cases and Stories

```
Case Title: The Turkey Drop / Brian's freshman-year advice
People / Organization: Brian Christian; his college guidance counselor
Context: High-school couples separated by college; counselors have slang for the Thanksgiving-weekend
breakup. Brian's girlfriend was several states away and neither had a benchmark for judging the
relationship.
What Happened: The counselor gave the deadpan advice: "Gather data."
Outcome: Not stated. Used as the chapter's opening hook.
Concept Illustrated: The look phase; the no-information problem (you cannot rate a relationship
without comparisons).
Why This Case Is Useful: Universally relatable, personal, and it states the algorithm's first phase in
two words.
Potential for Reuse: High
```

```
Case Title: Michael Trick runs the numbers on marriage
People / Organization: Michael Trick, later professor of operations research at Carnegie Mellon
Context: A graduate student recognized his own dating life as the secretary problem — "I had a
position to fill [and] a series of applicants."
What Happened: Not knowing how many women he would meet, he applied the 37% Rule to *time* instead,
assuming a search from age 18 to 40. That gave age 26.1 as the switch point — exactly his age. On
meeting a better match than anyone before, he proposed.
Outcome: She turned him down. Later, after finishing his degree and moving to Germany, he met someone
in a bar, moved in together three weeks later, invited her to the US "for a while," and they married
six years afterward.
Concept Illustrated: The 37% Rule applied to time; and the failure of the classical model's assumption
that offers are always accepted.
Why This Case Is Useful: Funny, self-deprecating, and it delivers the model's limitation through
narrative rather than caveat. The happy ending arrived by a route the algorithm never described.
Potential for Reuse: High
```

```
Case Title: Kepler's eleven courtships
People / Organization: Johannes Kepler
Context: After his first wife died in 1611, Kepler undertook a long search to remarry, courting eleven
women in total.
What Happened: Of the first four he preferred the fourth ("because of her tall build and athletic
body") but did not stop. The fifth won him over — "love, humble loyalty, economy of household,
diligence, and the love she gave the stepchildren" — and yet, he wrote, "However, I continued." His
thoughts stayed with number five through six further courtships. He then returned to her, declared
himself, and was accepted.
Outcome: Kepler married Susanna Reuttinger; they had six children, and biographies describe the rest
of his domestic life as particularly peaceful and joyous. Kepler nonetheless reproached his own
"restlessness and doubtfulness."
Concept Illustrated: The recall variant — a longer look phase (61%) plus a fallback to the best one
that got away.
Why This Case Is Useful: A famous scientist, a documented first-person account of the anguish, and an
exact structural match to a named algorithm. Pairs with Trick as the mirror-image failure of the
classical assumptions (Kepler recalled; Trick was rejected).
Potential for Reuse: High
```

```
Case Title: Laura Albert McLay sells her house
People / Organization: Laura Albert McLay, optimization expert, University of Wisconsin–Madison
Context: Selling her own home, she applied her knowledge of optimal stopping.
What Happened: The first offer was great but carried a large hidden cost — the buyers wanted her out a
month before she was ready. There was another competitive offer. She held out for the right one.
Outcome: She got the offer she wanted, and credits the math for her nerve: it would have been "really,
really hard" without knowing the math was on her side.
Concept Illustrated: A fixed reservation threshold; not lowering standards under pressure; counting
non-monetary costs inside the offer's value.
Why This Case Is Useful: Shows the algorithm's real payoff is emotional — the confidence to endure the
waiting — rather than a better number.
Potential for Reuse: High
```

```
Case Title: Donald Shoup, the "parking rock star," rides a bike
People / Organization: Donald Shoup, UCLA; the Los Angeles Times gave him the nickname
Context: The authors drove down from Northern California to interview him, promising to leave time for
"unexpected traffic." He replied that they should plan on *expected* traffic.
What Happened: Asked whether the world's leading parking expert had a secret weapon for optimizing his
own LA commute, he answered: "I ride my bike."
Outcome: A punchline that reframes the problem — the best solution to a hard optimization problem is
sometimes to exit it.
Concept Illustrated: Problem avoidance over problem solving; echoes the chapter's later "some problems
are better avoided than solved."
Why This Case Is Useful: Short, quotable, and structurally important — one of two places the chapter
undercuts its own optimize-everything premise.
Potential for Reuse: High
```

```
Case Title: Boris Berezovsky — the man who wrote the book on stopping and did not stop
People / Organization: Boris Berezovsky; AvtoVAZ; ORT Television; Sibneft; Boris Yeltsin; Vladimir
Putin
Context: Ten years before being named Russia's richest man by Forbes in 1997 (~$3 billion), Berezovsky
lived on a mathematician's salary at the USSR Academy of Sciences — where he worked on optimal
stopping and authored the first and only book devoted to the secretary problem.
What Happened: He used industrial relationships from his research to found a company linking foreign
carmakers with AvtoVAZ, became a large-scale dealer using an installment scheme that exploited ruble
hyperinflation, then bought into AvtoVAZ, ORT, and Sibneft. He entered politics, backing Yeltsin's
1996 re-election and Putin's succession in 1999. He then publicly opposed constitutional reforms
expanding presidential power. In October 2000 Putin warned of a "cudgel" the state had not yet used.
Berezovsky left Russia the following month for exile in England and kept criticizing the regime.
Outcome: He died in March 2013, found by a bodyguard in a locked bathroom with a ligature around his
neck, after losing much of his wealth in high-profile legal cases. The postmortem concluded suicide.
The authors speculate he should have stopped at a few tens of millions and stayed out of politics —
"but, alas, that was not his style."
Concept Illustrated: The burglar problem; failure to quit while ahead; expertise not transferring to
one's own life.
Why This Case Is Useful: Dramatic, high-stakes, and deeply ironic. Also the chapter's darkest material
and the one requiring the most careful handling — the authors' "perhaps he should have stopped
sooner" is speculation about a real death.
Potential for Reuse: High (with care)
```

```
Case Title: Berezovsky and the broken outboard motor
People / Organization: Boris Berezovsky and Leonid Boguslavsky, as told by David Hoffman in
*The Oligarchs*
Context: A water-skiing trip to a lake near Moscow when both were young researchers; the boat's motor
broke down.
What Happened: While their friends went to the beach and lit a bonfire, the two spent three hours
taking the motor apart and reassembling it. It stayed dead. They missed most of the party. Berezovsky
insisted they had to keep trying and would not give up.
Outcome: The motor was never fixed. Used as a character portrait foreshadowing his life.
Concept Illustrated: A disposition never to stop; the personal counterpart of "no optimal stopping
rule."
Why This Case Is Useful: A small, concrete, vivid scene that carries a whole personality — far more
memorable than the abstract claim.
Potential for Reuse: High
```

```
Case Title: Amnon Rapoport fights his own impatience
People / Organization: Amnon Rapoport, UC Riverside; running optimal stopping experiments for over
forty years
Context: Asked whether knowing the research changes his own behavior.
What Happened: In apartment searches he resists his urge to commit immediately: "Despite the fact that
by nature I am very impatient and I want to take the first apartment, I try to control myself!"
Outcome: Not stated.
Concept Illustrated: Knowing the algorithm does not remove the impulse; it gives you something to
argue against.
Why This Case Is Useful: The researcher-as-subject angle; pairs with McLay ("the math was on my side")
to make the point that these algorithms function as psychological permission.
Potential for Reuse: Medium
```

```
Case Title: The anthropology of the secretary problem's name
People / Organization: Not applicable — a historical observation
Context: The authors note how cultures stamp their own imagery on formal systems.
What Happened: Chess reads as medieval European but originated in eighth-century India and was
"Europeanized" in the fifteenth century — shahs became kings, viziers became queens, elephants became
bishops. Likewise optimal stopping problems were framed in the nineteenth century as baroque lotteries
and women choosing suitors; in the early twentieth as holidaying motorists seeking hotels and male
suitors choosing women; and in the mid-twentieth, male bosses choosing female assistants. The name
"secretary problem" first appears in print in 1964.
Outcome: The name stuck.
Concept Illustrated: That the framing of a formal problem is historically contingent while the math is
not.
Why This Case Is Useful: A ready-made aside on how culture dresses up mathematics; the chess detail is
independently reusable.
Potential for Reuse: Medium
```

```
Case Title: Barbara Bush married the first man she ever kissed
People / Organization: Barbara Bush (chapter epigraph)
Context: Placed as an epigraph to "Lover's Leap" — the section that derives the 37% Rule's application
to courtship — alongside a Malthus quotation.
What Happened: "I married the first man I ever kissed. When I tell this to my children they just about
throw up."
Outcome: Not stated in the chapter; the tone implies a marriage she was happy with.
Concept Illustrated: A zero-look-phase search that succeeded — and, read charitably, the gap between a
good process and a good outcome, since a strategy failing 63% of the time produces abundant happy
counterexamples.
Why This Case Is Useful: It is the chapter's own counterexample, sitting directly above the argument it
complicates, and the authors never address it. Ideal for the "but what about…" beat in any content
built on the 37% Rule.
Potential for Reuse: High
```

```
Case Title: Clark Kerr on the three problems of a university
People / Organization: Clark Kerr, President of UC Berkeley, 1958–1967 (chapter epigraph)
Context: Epigraph to "When to Park."
What Happened: "I find that the three major administrative problems on a campus are sex for the
students, athletics for the alumni, and parking for the faculty."
Outcome: N/A — an aphorism.
Concept Illustrated: That parking is a genuinely hard, universally felt problem worth formal analysis.
Why This Case Is Useful: A credible institutional source delivering a laugh line that opens a parking
segment.
Potential for Reuse: Medium
```

```
Case Title: The "one last job" trope, already solved
People / Organization: None — a genre observation by the authors
Context: Introducing the burglar problem.
What Happened: The authors note that a solution existing is "bad news for heist movie screenplays":
when the team tries to lure the old burglar out of retirement for one last job, the canny thief need
only crunch the numbers.
Outcome: N/A.
Concept Illustrated: The burglar problem; quitting while ahead.
Why This Case Is Useful: The most immediately graspable framing of the burglar problem in the chapter,
borrowing an audience's existing familiarity with the trope.
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: Why a look phase must exist at all
Example: The three-applicant enumeration — six orderings, three wins, with the failures split into
"too choosy" (twice) and "not choosy enough" (once).
Why It Works: Small enough to verify by hand, so the reader proves the result rather than trusting it,
and the symmetric failure modes make the tightrope metaphor concrete.
Possible Alternative Domain: Mathematics
```

```
Concept: The 37% Rule applied to time rather than count
Example: Michael Trick converting an assumed 18–40 dating window into age 26.1 — and finding it was
exactly his current age.
Why It Works: The coincidence makes it memorable, and it silently teaches the more useful lesson that
the rule takes a *proportion*, so it works on any measure of the search.
Possible Alternative Domain: Everyday Life
```

```
Concept: Success rate is invariant to pool size
Example: The contrast with random hiring — 1% success in a pool of 100, 0.0001% in a pool of a
million, versus a flat 37% under optimal stopping in both.
Why It Works: The gap between the two numbers grows enormous, which converts an abstract invariance
into a visible argument that the algorithm matters *more* as the problem gets bigger. The "best defense
against the haystack" line lands the point.
Possible Alternative Domain: Business
```

```
Concept: Full information removes the need to look
Example: The typing test scored by percentile — a 95th-percentile applicant can be hired on the spot
(assuming you don't think a 96th-percentile candidate is out there).
Why It Works: Makes the abstract distinction between ordinal and cardinal information tangible with a
familiar object (an SAT-style percentile), and shows immediately what changes.
Possible Alternative Domain: Psychology
```

```
Concept: Threshold depends only on the cost of waiting
Example: The $400k–$500k house with four waiting costs: $1 → $499,552.79; $2,000 → $480,000; $10,000
→ $455,279; $50,000 → take the first offer.
Why It Works: The absurd precision of $499,552.79 is the teaching device — it shows the model produces
an exact number, and the descent to "beggars can't be choosers" shows the whole range of behavior in
one table.
Possible Alternative Domain: Business
```

```
Concept: Occupancy rate governs search cost
Example: 90% → 95% occupancy accommodates 5% more cars but doubles everyone's search length.
Why It Works: One sentence, two numbers, and a counterintuitive nonlinearity that instantly justifies
an unpopular policy (charge more for parking, leave spots empty).
Possible Alternative Domain: Everyday Life
```

```
Concept: Problems with no stopping rule
Example: Triple or nothing — $1 becomes an expected $1.50, then an expected $4.50; the math says
always play; playing always ends in ruin.
Why It Works: Arithmetic simple enough to follow in one's head, with a conclusion that visibly
contradicts the intuition that expected value should be a sufficient guide.
Possible Alternative Domain: Mathematics
```

## 9. Counterintuitive Insights

```
Insight: Your odds of finding the very best option are 37% whether the pool has 100 candidates or a
million.
Common Belief: More options means a proportionally worse chance of picking the best one.
Author's Argument: The optimal strategy's success rate converges to 1/e and stays there; only the
random-choice baseline collapses with pool size.
Evidence: The mathematical result plus the 1% / 0.0001% random-hiring comparison.
Why It Is Surprising: It implies the value of knowing the algorithm *increases* with the size of the
problem, which inverts the usual intuition that big searches are hopeless.
Qualification: 37% is a *limit* the success rate converges down to as the pool grows — the chapter's
own table shows small pools do better (50% at two and at three applicants). The invariance claim holds
for large pools, which are not the pools most real decisions involve.
```

```
Insight: Even perfect play fails 63% of the time.
Common Belief: An optimal strategy should usually work.
Author's Argument: 37% is the ceiling, not the floor; high failure is a property of the problem, not
of the decision-maker.
Evidence: Direct consequence of the 37% result.
Why It Is Surprising: It separates good decisions from good outcomes, and undercuts the romantic
premise of searching for "the one."
```

```
Insight: Gold digging is more likely to succeed than a quest for love.
Common Belief: Choosing a partner on an objective metric is shallow and probably foolish.
Author's Argument: An objective yardstick converts a no-information game into a full-information one,
lifting success from 37% to 58%.
Evidence: The two success rates, under the model's assumptions.
Why It Is Surprising: It attaches a mathematical advantage to a socially disparaged strategy. The
authors call it "unexpected and somewhat bizarre" and immediately widen it from net worth to any
yardstick — the insight is really about information, not money.
Qualification: It inherits the full-information game's two stated premises — a pool "representative of
the population at large" that "isn't skewed or self-selected in any way," and a single criterion
decided to be "the only thing that matters." A dating pool violates the first almost by construction,
and the second is the assumption most people would reject outright.
```

```
Insight: Restlessness and doubt can be optimal rather than defects of character.
Common Belief: Inability to settle is a psychological or moral failing (Kepler's own view of himself).
Author's Argument: When second chances exist, the optimal algorithm prescribes a *longer* look phase
(61%) plus a fallback — exactly the behavior that felt like weakness.
Evidence: The recall-variant result, applied retrospectively to Kepler.
Why It Is Surprising: It converts self-reproach into strategy. Note this is an interpretive move: the
math does not show Kepler was optimizing.
```

```
Insight: Never reconsider an offer you already rejected, even if it is still available.
Common Belief: If nothing better turned up, going back to the good offer is the sensible correction.
Author's Argument: The threshold depends only on search cost, which has not changed; what you spent
searching is a sunk cost. If it wasn't above threshold then, it isn't now.
Evidence: The constancy of the reservation price in the house-selling model.
Why It Is Surprising: It flatly contradicts the recall advice that rescued Kepler — and the chapter
does not flag the tension.
```

```
Insight: Empty parking spots on the most desirable blocks are a sign the system is working.
Common Belief: A resource is being wasted if it isn't fully used; full curbs mean popular streets.
Author's Argument: Parking is a process, not just a resource. Occupancy near 100% imposes search time,
fuel, congestion, and pollution on everyone; ~85% occupancy is the efficient target.
Evidence: Shoup's argument and the 90%→95% doubling figure.
Why It Is Surprising: It reframes visible slack as efficiency rather than waste.
```

```
Insight: People who stop too early may not be irrational — they may be pricing in a cost the model
forgot.
Common Belief: Deviation from an optimal algorithm is a cognitive bias.
Author's Argument: Assume a 1% per-applicant cost and the observed behavior *is* optimal; humans carry
that cost in from their lives even when the experiment does not impose it.
Evidence: Seale & Rapoport's cost-adjusted fit.
Why It Is Surprising: It reverses the standard behavioral-economics reading, consistent with the
book's introduction: mistakes often reveal the difficulty of the problem rather than a buggy brain.
Note the fit is post hoc.
```

```
Insight: Some problems have no optimal stopping rule, and the right response is not to play.
Common Belief: Every well-posed decision problem has a best strategy.
Author's Argument: In triple-or-nothing, expected value rises every round so the math says always
continue — yet always continuing guarantees ruin. "Some problems are better avoided than solved."
Evidence: The expected-value walkthrough.
Why It Is Surprising: The authors turn their own optimization framework against itself, in a chapter
otherwise devoted to solvable problems.
```

## 10. Unique or Unusual Ideas

```
Idea: Optimal stopping is the mathematical form of mortality — "we truly pass this way but once."
Why It Seems Unique: The chapter escalates a hiring puzzle into a claim that the secretary problem's
least believable assumption (strict seriality, no going back) is simply time itself, so that hesitation
is as irrevocable as action.
Potential Connection to Other Topics: Existential philosophy; the Grellet and Dillard epigraphs;
regret theory; time preference and discounting.
```

```
Idea: The look phase is a symptom of missing information, not a virtue.
Why It Seems Unique: Cuts against generic "do your research" advice — the exploration period is a tax
you pay for lacking a yardstick, and finding a yardstick is worth more than exploring longer.
Potential Connection to Other Topics: Measurement and metrics design; standardized testing; the
explore/exploit tradeoff in chapter 2.
```

```
Idea: Formal problems get culturally redressed while their mathematics stays fixed.
Why It Seems Unique: The chess-Europeanization parallel and the 150-year drift of optimal stopping's
cover story (lotteries → suitors → motorists and hotels → bosses and secretaries) is a genuine aside
about the sociology of mathematics.
Potential Connection to Other Topics: History of science; how framing affects which problems get
studied.
```

```
Idea: The real deliverable of an algorithm can be emotional permission rather than a better decision.
Why It Seems Unique: McLay ("if I didn't know the math was on my side") and Rapoport ("I try to control
myself!") both describe using the math to withstand an impulse, not to compute an answer.
Potential Connection to Other Topics: Commitment devices; precommitment; self-control research;
decision hygiene.
```

```
Idea: The expert who opts out — Shoup rides a bike.
Why It Seems Unique: Placed as a punchline rather than an argument, but it is the chapter's own
evidence that redesigning or exiting a problem can dominate solving it.
Potential Connection to Other Topics: Problem framing; the book's own conclusion on computational
kindness; mechanism design.
```

```
Idea: Pairing every formal result with a literary epigraph.
Why It Seems Unique: Each section is framed by writers and figures who reached the same territory
without the math — Kepler and Jane Austen ("why should you hesitate?") open the chapter; Malthus and
Barbara Bush open the courtship section; Clark Kerr opens parking; Grellet and Annie Dillard ("Spend
the afternoon. You can't take it with you.") open the closing meditation on time. The device stages the
book's core argument structurally: the humanistic tradition identified these dilemmas, and computer
science supplies the number.
Potential Connection to Other Topics: Rhetoric of popular science; the introduction's "they don't need
a therapist, they need an algorithm"; why quantified advice lands differently from identical
qualitative advice.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: Recall is either your salvation (Kepler) or forbidden (house selling), within one chapter.
Author's Position: Both, depending on the problem — the recall variant rewards going back to the one
that got away; the cost-of-waiting model says never revisit a rejected offer.
Possible Counterargument: The chapter never states the condition that separates them. The distinction
appears to be the goal (single best vs. maximize total value) and whether the threshold is
information-dependent or cost-dependent, but a reader is left with two flatly opposed prescriptions.
What Evidence Would Help Resolve It: An explicit statement of which model applies to which real
situation, and a test of whether people can classify their own situations correctly.
```

```
Issue: "Success" is defined as getting the single best option in the pool.
Author's Position: Accepted as the objective throughout the classical analysis; the house-selling
section changes it to total value and gets a different algorithm.
Possible Counterargument: Almost nobody actually requires the single best partner or apartment; under
a "top 10% is fine" objective, optimal look fractions and success rates change dramatically, and
stopping early may be near-optimal. The chapter does not analyze satisficing objectives.
What Evidence Would Help Resolve It: The same analysis under expected-rank or top-k objectives, and
evidence on what objective people actually hold.
```

```
Issue: Is early stopping a bias or a rational response to unmodeled cost?
Author's Position: Leans to the latter — the endogenous time cost explanation, in keeping with the
book's anti-"buggy brain" stance.
Possible Counterargument: The 1% cost was chosen to reproduce the observed data, which makes the
explanation unfalsifiable as presented — almost any deviation can be rationalized by positing the
right cost. Risk aversion and misperception of remaining candidates are untested rivals.
What Evidence Would Help Resolve It: Independent measurement of subjects' time cost, or manipulating
imposed search cost and checking whether behavior shifts as the model predicts.
```

```
Issue: Applying courtship models to real people's lives.
Author's Position: Treats dating as a search over "applicants" and calls Kepler's outcome a happy
ending under the algorithm.
Possible Counterargument: Partners are agents with their own search, not applicants in a queue; the
pool is not randomly ordered; preferences change during the search; and options are not independent.
The chapter acknowledges rejection and recall but not endogenous or shifting preferences.
What Evidence Would Help Resolve It: Two-sided matching analyses (deferred acceptance), and evidence
on preference change over the course of a long search.
```

```
Issue: The Berezovsky reading.
Author's Position: Presents his exile and death as a failure to stop, speculating he should have
stopped at tens of millions and avoided politics.
Possible Counterargument: This is retrospective narrative fitted to a model — his fate turned on
political conflict with a head of state, not on a miscalibrated number of "robberies." The burglar
problem assumes constant independent odds per attempt, which political conflict violates.
What Evidence Would Help Resolve It: Not resolvable; it is an interpretive frame. Worth flagging as
storytelling rather than analysis.
```

```
Issue: The parking model's idealization.
Author's Position: Concedes the infinite straight road is unrealistic and notes studied variants, but
still presents the occupancy-indexed distances as guidance.
Possible Counterargument: Real urban parking involves one-way networks, garages, competing drivers,
and uneven spot density — the authors mention these tweaks exist but report no results from them.
What Evidence Would Help Resolve It: Results from the variant models, or field data on cruising times.
```

```
Issue: "Gold digging is more likely to succeed than a quest for love" rests on questionable premises.
Author's Position: Stated as a takeaway, then immediately widened to "any yardstick."
Possible Counterargument: It requires that a single measurable criterion is what you actually want and
that the pool is representative and unskewed — the two conditions least likely to hold in partner
search. It compares success rates at *different objectives*, not the same one.
What Evidence Would Help Resolve It: Whether full-information searchers report better long-run
outcomes, not just higher probability of picking the pool's maximum on their chosen metric.
```

```
Issue: The chapter's own framework has exceptions it does not integrate.
Author's Position: Two undercutting moments — Shoup's bicycle and "some problems are better avoided
than solved" — are delivered as punchlines rather than developed.
Possible Counterargument: If problem avoidance sometimes dominates optimization, that deserves a
criterion for when, which the chapter does not supply.
What Evidence Would Help Resolve It: A treatment of problem selection/reframing alongside problem
solving; the book's conclusion on computational kindness may address this.
```

```
Issue: The chapter prints a counterexample to its own thesis and never mentions it.
Author's Position: None — the Barbara Bush epigraph ("I married the first man I ever kissed") sits
directly above the section deriving the 37% Rule for courtship, and is never referenced again.
Possible Counterargument: None is strictly needed — a 63% failure rate predicts many happy
counterexamples, and one anecdote cannot disconfirm a probabilistic claim. But because the chapter
never makes that argument, an attentive reader experiences the epigraph as an unanswered objection
rather than an illustration. The omission is rhetorical, not mathematical.
What Evidence Would Help Resolve It: Nothing empirical; this is a gap in exposition. The fix is the
process-versus-outcome distinction the chapter has the material for but doesn't state.
```

## 12. Quotable Ideas

```
Paraphrase (short): They don't need a therapist; they need an algorithm — the therapist says find the
right balance, the algorithm says the balance is 37%.
Why the Idea Matters: The book's whole promise in one contrast: vague advice replaced by a number.
Source Location: Introduction, carried into ch. 1 (PDF p. 11).
```

```
Paraphrase (short): In an optimal stopping problem the hard question isn't which option to pick, it's
how many options to consider.
Why the Idea Matters: The reframing that makes the whole chapter possible.
Source Location: "The Secretary Problem" (PDF p. 18).
```

```
Paraphrase (short): You're unlikely to find the needle most of the time, but optimal stopping is your
best defense against the haystack, however large.
Why the Idea Matters: Sets the honest expectation — the algorithm reduces regret, it doesn't promise
the best outcome.
Source Location: "Whence 37%?" (PDF p. 24).
```

```
Paraphrase (short): With slim pickings, lower your standards; with more fish in the sea, raise them —
and the math tells you exactly by how much.
Why the Idea Matters: The full-information takeaway, and the clearest statement of what quantification
adds to folk wisdom.
Source Location: "Knowing a Good Thing When You See It" (PDF p. 28).
```

```
Paraphrase (short): What you paid to keep searching is a sunk cost — don't compromise, don't
second-guess, and don't look back.
Why the Idea Matters: The prescriptive core of the house-selling model, and the chapter's sharpest
piece of advice.
Source Location: "When to Sell" (PDF p. 33).
```

```
Paraphrase (short): Asked how the world's top parking expert optimizes his own commute, Shoup said:
"I ride my bike."
Why the Idea Matters: The best move in a hard optimization problem is sometimes to leave it.
Source Location: "When to Park" (PDF p. 37).
```

```
Paraphrase (short): Some problems are better avoided than solved.
Why the Idea Matters: The chapter's own limiting principle, arriving right after a proof that the math
would have you play until you lose everything.
Source Location: "When to Quit" (PDF p. 39).
```

```
Paraphrase (short): It's not irrational to get bored, but it's hard to model that rigorously.
(Neil Bearden)
Why the Idea Matters: Names the gap between formal models and lived decision-making without dismissing
either.
Source Location: "Always Be Stopping" (PDF p. 41).
```

```
Paraphrase (short): The flow of time turns all decision-making into optimal stopping; no choice
recurs, and hesitation is as irrevocable as action.
Why the Idea Matters: The chapter's thesis at its widest, and its most quotable line.
Source Location: "Always Be Stopping" (PDF pp. 41–42).
```

```
Paraphrase (short): Trick on his own proposal — the model's assumptions don't let me determine whether
she's Perfect, but there was no doubt she met the qualifications for this step of the algorithm.
Why the Idea Matters: The clearest statement in the chapter of what an algorithm delivers: a
procedure, not a verdict about a person.
Source Location: "Lover's Leap" (PDF p. 25).
```

```
Paraphrase (short): Kepler asked whether there was any way for his uneasy heart to be content with its
fate other than by realizing that so many other desires could never be fulfilled.
Why the Idea Matters: Names the psychological cost of a long look phase — you settle by conceding that
most options were always out of reach.
Source Location: "Lover's Leap" (PDF p. 26).
```

```
Paraphrase (short): "Spend the afternoon. You can't take it with you." (Annie Dillard, epigraph)
Why the Idea Matters: The chapter's humanistic counterpart to its closing argument that time's
one-way flow makes every decision a stopping problem.
Source Location: Epigraph to "Always Be Stopping" (PDF pp. 39–40).
```

## 13. Psychology Connections

- **Impatience and premature closure.** The robust finding that people leap too early (Rapoport &
  Seale) is the chapter's central behavioral result. Rapoport reports fighting the same impulse in his
  own apartment searches.
- **Boredom as a decision variable.** Bearden's remark treats boredom as an unmodeled but real cost
  rather than noise — a bridge between affect and formal decision theory.
- **Sunk cost fallacy, inverted.** The "never look back" rule is a direct application of sunk-cost
  reasoning done *correctly*; the chapter uses the concept prescriptively rather than as a bias.
- **Regret and counterfactual thinking.** The framing of "the one that got away" versus holding out
  too long maps onto the two regret types in regret theory; the introduction names them as
  Scylla-and-Charybdis regrets.
- **Self-reproach reframed.** Kepler's "restlessness and doubtfulness" is recast as strategy — an
  externalizing reattribution of a trait the subject experienced as a flaw.
- **Algorithms as commitment devices / emotional permission.** McLay and Rapoport both use the math to
  resist an impulse, not to compute an answer. This is closer to self-control research than to
  optimization.
- **Choice overload, contradicted.** Standard psychology says more options degrade satisfaction and
  decision quality; the invariance of the 37% success rate to pool size is at least a partial formal
  counterweight (inference: the chapter does not cite that literature).
- **Behavioral economics, pushed back on.** The endogenous-cost argument continues the introduction's
  thesis that human error often reflects hard problems rather than defective hardware.
- **Outcome bias.** The 63% failure rate is precisely an argument for judging decisions by process
  rather than result, and the Barbara Bush epigraph is a live example of an outcome that flatters a
  strategy the math disfavors. The chapter has all the material and never names the bias (inference).
- **Satisficing vs. maximizing.** The chapter assumes maximizing (single best only) throughout the
  classical analysis; the Simon satisficing tradition is the obvious point of contact and is not
  mentioned (inference).

## 14. Mathematics and Decision Science Connections

- **The constant e.** The optimal look fraction is exactly 1/e ≈ 0.3679, the same e as in compound
  interest; the chapter notes anything between 35% and 40% is near-optimal, so the result is robust to
  imprecision.
- **Ordinal vs. cardinal information.** Explicitly named; the entire difference between the 37% and
  58% success rates is an information-structure difference, not a strategy-cleverness difference.
- **Backward induction / dynamic programming.** The full-information thresholds (50th, 69th, 78th
  percentile as you count backward from the last applicant) are derived by starting at the end and
  working back.
- **Expected value and its limits.** Triple-or-nothing shows expected value can prescribe a strategy
  that guarantees ruin — the classic gap between expectation and almost-sure outcome.
- **Reservation price / optimal stopping in economics.** The house-selling threshold is a reservation
  price; the chapter notes economists use it to model job search and to explain coexisting
  unemployment and vacancies.
- **Risk of ruin.** The burglar problem's ratio (success odds ÷ failure odds) is a ruin-problem result.
- **Sunk cost as a formal result.** "Don't look back" falls out of the model rather than being imported
  as advice.
- **Game theory.** Parking is flagged as having a game-theoretic component (competing drivers), with a
  forward reference to chapter 11; Flood, the likely originator of the 37% Rule, also devised the
  prisoner's dilemma and popularized the traveling salesman problem (chapter 8).
- **Convergence and invariance.** Both the optimal look point and the success probability converge to
  1/e as n grows — a symmetry the authors call "curious."
- **Uniform distributions and closed-form solutions.** The house-selling result assumes a known range
  with uniformly likely offers, which is what makes the stopping price a clean explicit function.

## 15. Sports Connections

**Direct examples from the book:** None identified. (Clark Kerr's epigraph mentions "athletics for the
alumni" as an administrative problem, and Kepler admired a candidate's "athletic body" — neither is a
sports application.)

**Inferred applications (mine):**

- **Transfer windows and scouting.** A club with a fixed window and a stream of available players faces
  a near-textbook secretary problem — irrevocable decisions, sequential availability, competition
  meaning a passed player is gone. But scouting data (xG, percentile ranks vs. league) converts it into
  a *full-information* problem, so the Threshold Rule applies and the club should be prepared to sign
  an outstanding target immediately rather than "seeing who else comes up."
- **Contract negotiation and the reservation price.** A free agent fielding offers over time is the
  house-selling problem: set a number before the process starts based on the cost of waiting (lost
  wages, injury risk, declining market), then hold it — and never circle back to an offer already
  refused.
- **When to substitute.** A manager watching a struggling player decides not *whom* to bring on but
  *when* to stop waiting for the performance to turn — a stopping problem with an endogenous time cost
  (minutes remaining) exactly analogous to the one that makes lab subjects leap early.
- **Retirement timing.** The burglar problem maps almost directly onto an athlete's career: each extra
  season carries a reward and a probability of a catastrophic injury or reputational decline that wipes
  out accumulated standing. The "one last job" trope is the same as the one-more-season decision.
- **In-game risk with no stopping rule.** Chasing an equalizer by pushing more players forward
  increases expected goals while raising the chance of conceding on the break — a triple-or-nothing
  structure where the expected-value logic keeps saying continue.
- **Draft strategy.** Rounds where teams pick sequentially with no recall are structurally the
  secretary problem; teams with strong analytics operate under full information and should threshold,
  while teams relying on comparative eye-test judgment are stuck in the no-information game.
- **Occupancy-rate analogue.** Shoup's insight that 95% utilization doubles search cost maps onto squad
  rotation and roster slack — a fully utilized squad has no capacity to absorb an injury.

## 16. AI and Machine Learning Connections

**Direct from the book:** The chapter is itself an argument that computer-science algorithms transfer
to human decisions; it forward-references the explore/exploit tradeoff (chapter 2), the traveling
salesman problem (chapter 8), and game theory (chapter 11). No machine learning is discussed.

**Inferred connections (mine):**

- **Explore/exploit and multi-armed bandits.** The look/leap split is the purest form of an
  exploration-then-exploitation schedule; ε-greedy and epsilon-decay strategies are the same shape with
  a softer boundary.
- **Early stopping in training.** The name is shared and the structure is real: deciding when to stop
  training a model is a sequential decision under uncertainty where continuing has a cost and the best
  checkpoint may already be behind you — and unlike the secretary problem, checkpointing gives you
  *recall*, which is why the recall variant is the better analogy.
- **Hyperparameter search.** Random search over a configuration budget is a stopping problem;
  successive halving and Hyperband are essentially threshold rules that get more selective as budget
  remains.
- **Reinforcement learning.** The endogenous time cost is a discount factor by another name; the
  burglar problem is an episodic RL task with an absorbing failure state.
- **Ranking and retrieval.** Ordinal-only feedback (pairwise preferences) versus cardinal scores is
  exactly the distinction that separates learning-to-rank from regression — and RLHF preference data is
  ordinal, which means preference-based training operates in the chapter's no-information regime.
- **LLM agent design.** Agents that search, browse, or sample candidate solutions need explicit
  stopping criteria; best-of-n sampling with a reward model is a full-information stopping problem,
  while an agent with only pairwise self-comparison is in the no-information one. The 37% failure rate
  is a useful prior on how often "pick the best candidate" search can succeed at all.
- **Threshold-setting in deployed classifiers.** The "lower your standards as options dwindle" result
  is the same logic as adjusting a decision threshold when the candidate pool shrinks.
- **The unfalsifiability warning generalizes.** Fitting a 1% cost parameter to reproduce human behavior
  is exactly the failure mode of post-hoc reward modeling — a model that can rationalize any observed
  behavior explains none of it.

## 17. Content Creation Opportunities

```
Idea Title: The 37% Rule — the mathematically optimal moment to stop looking
Format: YouTube Long-form
Application Domain: Everyday Life
Hidden Principle: Optimization
Story Hook (Layer 1): A mathematician calculated the exact age he should stop dating and propose
(26.1), worked up the nerve, did it — and was turned down on the spot.
Principle Framework (Layer 2): Optimal stopping — in any irreversible sequential search, spend a fixed
fraction (37%) building a benchmark, then commit to the next option that beats everything seen so far;
the high failure rate is a property of the problem, not a failure of yours.
Best Supporting Case: Michael Trick calculating age 26.1, proposing, and being rejected; then finding
his wife by a route the algorithm never described.
Character Application: Nova: Strategist
Psychology Angle: People leap too early in over 80% of trials — which may be rational once search costs
are counted, not a bias.
Math Angle: 1/e, and the odd symmetry that the strategy and its success rate are the same number (37%).
Sports Angle: Transfer windows as sequential, irrevocable choice under a deadline.
Business Angle: Hiring — stop interviewing and make the offer once the field is calibrated.
Investing Angle: Deal sourcing — fix a "look" window, then commit to the first option that clears the
bar.
History Angle: Kepler's and Trick's real courtship decisions as pre- and post-algorithm case studies.
AI Angle: Explore/exploit; early stopping; best-of-n sampling.
```

```
Idea Title: Kepler vs. Trick — two ways the love algorithm breaks
Format: YouTube Long-form
Application Domain: History
Hidden Principle: Optimization
Story Hook (Layer 1): Two mathematicians used the same equation to find a wife. One was rejected on the
spot; the other courted eleven women, hated himself for it — and it turned out he was doing it right.
Principle Framework (Layer 2): The same optimal-stopping rule bends with the rules of the game: if
options can reject you, look less (37% → 25%); if you can revisit past options, look more (37% → 61%).
Match the schedule to whether choices are one-way.
Best Supporting Case: Kepler's eleven courtships and his own written self-reproach.
Character Application: Insight: Interpreter
Psychology Angle: Recasting restlessness and indecision as strategy rather than defect.
Math Angle: 37% → 25% under rejection; 37% → 61% when you can go back.
Sports Angle: A club that can re-approach a player it passed on plays a different search than one that
can't.
Business Angle: Negotiations where the counterparty can walk (look less) vs. options you can reopen
(look more).
Investing Angle: Exploding-offer term sheets (rejection variant) vs. deals you can circle back to
(recall variant).
History Angle: Kepler as a documented, self-aware case of the recall variant three centuries early.
AI Angle: Checkpointing gives you recall — which changes the optimal stopping schedule.
```

```
Idea Title: Why empty parking spots mean the city is working
Format: YouTube Short
Application Domain: Business
Hidden Principle: Optimization
Story Hook (Layer 1): The economist who fixed city parking rides a bike to work — and says a curb that
looks "full" is a curb that's underpriced.
Principle Framework (Layer 2): Near-total utilization is a trap: pushing a shared resource from 90% to
95% full lets in 5% more users but can double everyone's search cost. Deliberate slack is efficiency,
not waste.
Best Supporting Case: Donald Shoup, "the parking rock star," and dynamic-priced curbs that keep a spot
or two open.
Character Application: Sigma: Architect
Psychology Angle: Slack looks like waste; the feeling of a full curb is the feeling of an underpriced
resource.
Math Angle: The nonlinear relationship between occupancy and expected search length.
Sports Angle: Squad rotation — a 100%-utilized roster can't absorb an injury.
Business Angle: Server/capacity planning and just-in-time inventory — running "hot" hides fragility.
Investing Angle: Cash buffers and leverage — a fully deployed portfolio can't absorb a shock.
History Angle: The rise of congestion pricing as a policy correction to over-utilization.
AI Angle: Utilization vs. latency in scheduling and load balancing.
```

```
Idea Title: The man who wrote the book on quitting — and didn't
Format: YouTube Long-form
Application Domain: Investing
Hidden Principle: Decision Making
Story Hook (Layer 1): He literally wrote the only book on the mathematics of when to stop. Then, in his
own life, he didn't.
Principle Framework (Layer 2): Knowing the optimal stopping rule is not the same as being disposed to
follow it; with an absorbing "ruin" state, the right number of attempts scales with the odds of success
over the odds of ruin — but temperament, not knowledge, decides whether you stop.
Best Supporting Case: Boris Berezovsky — including the three hours spent on a dead outboard motor while
everyone else was at the bonfire.
Character Application: Blaze: Executor
Psychology Angle: Expertise does not transfer to one's own life; disposition beats knowledge.
Math Angle: Optimal attempts ≈ odds of success ÷ odds of ruin.
Sports Angle: When to retire — each extra season adds reward and the risk of a career-ending injury.
Business Angle: Founders who can't stop scaling past the point of ruin.
Investing Angle: Position sizing and knowing when to cash out before a martingale wipes you out.
History Angle: The oligarch era as a real-world laboratory of risk-of-ruin decisions.
AI Angle: Episodic tasks with absorbing failure states.
Note: Handle with care — a real person's death, and the authors' "he should have stopped sooner" is
speculation.
```

```
Idea Title: The game the math says to play until you lose everything
Format: YouTube Short
Application Domain: Investing
Hidden Principle: Expected Value
Story Hook (Layer 1): Every round, the math says keep playing. Follow the math, and you are guaranteed
to end with nothing.
Principle Framework (Layer 2): Positive expected value is not a stopping rule. When each bet risks total
ruin, an ever-rising expectation coexists with almost-sure bankruptcy — you must optimize survival, not
just the average.
Best Supporting Case: Triple-or-nothing — $1 → expected $1.50 → expected $4.50 → … → $0.
Character Application: Nova: Strategist
Psychology Angle: Why "positive expected value" feels like it should be enough — and isn't.
Math Angle: Expected value versus almost-sure ruin (the St. Petersburg family of paradoxes).
Sports Angle: Pushing every player forward for the equalizer and conceding the game-ending goal.
Business Angle: Betting the company repeatedly on "+EV" gambles until one loss ends it.
Investing Angle: Martingale/all-in strategies; the Kelly criterion as the survival-aware correction.
History Angle: Classic ruinous doubling schemes across gambling history.
AI Angle: Reward hacking — optimizing a metric that keeps rising while the true outcome deteriorates.
```

```
Idea Title: Stop gathering data — get a yardstick instead
Format: Visual Explainer
Application Domain: Business
Hidden Principle: Information Theory
Story Hook (Layer 1): The reason you have to "look before you leap" isn't wisdom — it's that you have no
measuring stick. Get one, and your odds jump from 37% to 58%.
Principle Framework (Layer 2): The value of information depends on its type: with only rankings (ordinal
info) you must waste a look phase; with a calibrated scale (cardinal info) you can commit immediately to
anything above a computed threshold. Change the information, not just the effort.
Best Supporting Case: The percentile typing test — hire the 95th-percentile applicant on the spot.
Character Application: Sigma: Architect
Psychology Angle: "Do your research" as advice that misdiagnoses the real problem (missing yardstick,
not missing data).
Math Angle: Ordinal vs. cardinal information; backward-induction thresholds (50th, 69th, 78th…).
Sports Angle: Scouting analytics converting recruitment into a full-information problem.
Business Angle: Rubrics and benchmarks that let you hire the first candidate over the bar.
Investing Angle: Absolute valuation models vs. "compare to the last deal we saw."
History Angle: The spread of standardized testing and percentile scoring.
AI Angle: Pairwise preference data vs. absolute reward scores in RLHF.
```

```
Idea Title: The First Kiss Problem — when the math says look, and the person who didn't was happy
Format: YouTube Short
Application Domain: Everyday Life
Hidden Principle: Cognitive Bias
Story Hook (Layer 1): Barbara Bush married the first man she ever kissed. The math says she had almost
no chance of finding her best possible match. It worked out anyway.
Principle Framework (Layer 2): Judge the process, not the outcome. A strategy that fails 63% of the time
still produces countless happy counterexamples — so a single good result is not evidence of a good
decision.
Best Supporting Case: The Barbara Bush epigraph set against the Kepler and Trick stories.
Character Application: Echo: Observer
Psychology Angle: Outcome bias — we grade decisions by how they happened to turn out.
Math Angle: A strategy that fails 63% of the time necessarily produces many happy counterexamples.
Sports Angle: Judging a manager's substitution purely by whether the shot went in.
Business Angle: Rewarding a reckless bet that paid off; punishing a sound bet that lost.
Investing Angle: Crediting a lucky trade as skill (results-orientation vs. decision quality).
History Angle: Survivorship narratives — the happy first-marriage stories we remember.
AI Angle: Evaluating a policy from a single rollout instead of expected return.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B01-C01-01
Title: The 37% Rule
Type: Model
Summary: In the classical secretary problem, reject the first 1/e (~37%) of options, then take the
first one better than all of those. Success rate ~37%, invariant to pool size. Anything between 35%
and 40% is near-optimal.
Source: Algorithms to Live By, ch. 1, "Whence 37%?" (PDF pp. 20–24, footnote p. 45)
Tags: optimal-stopping, secretary-problem, decision-rule, 1/e
Related Concepts: Look-Then-Leap Rule, Threshold Rule, explore/exploit
```

```
CARD ID: B01-C01-02
Title: Look-Then-Leap Rule
Type: Model
Summary: Two-phase strategy — a fixed non-committal look phase where nothing is chosen regardless of
quality, then instant commitment to the first option beating the look-phase best. The structural form
of the optimal solution across no-information variants and for parking.
Source: Algorithms to Live By, ch. 1 (PDF p. 21)
Tags: optimal-stopping, exploration, algorithm, two-phase
Related Concepts: 37% Rule, Threshold Rule, parking model
```

```
CARD ID: B01-C01-03
Title: Threshold Rule (Full Information)
Type: Model
Summary: With population-calibrated scores, skip the look phase and accept the first option above a
declining percentile threshold — 50th for the next-to-last option, 69th for third-to-last, 78th for
fourth-to-last, more selective the more remain. Success rate 58%.
Source: Algorithms to Live By, ch. 1, "Knowing a Good Thing When You See It" (PDF pp. 27–29)
Tags: optimal-stopping, full-information, threshold, backward-induction
Related Concepts: No-information game, ordinal vs. cardinal, reservation price
```

```
CARD ID: B01-C01-04
Title: 63% failure even when playing optimally
Type: Insight
Summary: The best possible strategy in the classical secretary problem still misses the top option
almost two-thirds of the time. High failure is a property of the problem, not the decision-maker.
Source: Algorithms to Live By, ch. 1 (PDF p. 23)
Tags: optimal-stopping, decision-quality, outcome-vs-process, regret
Related Concepts: 37% Rule, good decisions vs. good outcomes
```

```
CARD ID: B01-C01-05
Title: Success rate is invariant to pool size
Type: Claim
Summary: Optimal stopping yields ~37% whether there are 100 or a million candidates, while random
choice collapses from 1% to 0.0001%. The algorithm's value therefore grows with the size of the
search. Caveat: 37% is the limit the rate converges *down* to — small pools do better (50% at two or
three applicants).
Source: Algorithms to Live By, ch. 1 (PDF p. 24)
Tags: optimal-stopping, scaling, invariance, choice-overload
Related Concepts: 37% Rule, needle-in-haystack framing
```

```
CARD ID: B01-C01-06
Title: Rejection variant — propose early and often
Type: Model
Summary: With a 50/50 chance of being rejected, start making offers after ~25% of the search and keep
offering to every best-yet candidate. Overall success ~25%.
Source: Algorithms to Live By, ch. 1, "Lover's Leap" (PDF p. 26)
Tags: optimal-stopping, variant, rejection, two-sided
Related Concepts: 37% Rule, Michael Trick case
```

```
CARD ID: B01-C01-07
Title: Recall variant — 61% rule and the fallback
Type: Model
Summary: If belated proposals succeed half the time, look until 61% of candidates, leap only in the
remaining 39%, and if still unmatched go back to the best one that got away. Success ~61%.
Source: Algorithms to Live By, ch. 1, "Lover's Leap" (PDF p. 26)
Tags: optimal-stopping, variant, recall, second-chances
Related Concepts: Kepler case, "never look back" (contrast)
```

```
CARD ID: B01-C01-08
Title: Kepler's eleven courtships
Type: Case
Summary: After his first wife died in 1611, Kepler courted eleven women, preferred the fifth but kept
searching, reproached himself for "restlessness and doubtfulness," then returned to her and was
accepted. Married Susanna Reuttinger; six children; biographies describe a peaceful, joyous domestic
life thereafter. A structural match to the recall variant.
Source: Algorithms to Live By, ch. 1 (PDF pp. 25–26)
Tags: case, history-of-science, dating, recall-variant, self-reproach
Related Concepts: Recall variant, restlessness-as-strategy
```

```
CARD ID: B01-C01-09
Title: Michael Trick's 26.1
Type: Case
Summary: A graduate student applied the 37% Rule to time rather than count — an 18-to-40 search window
gave age 26.1, exactly his age. He proposed to the first woman who beat all previous. She said no. He
later met his wife by chance in a bar in Germany.
Source: Algorithms to Live By, ch. 1, "Lover's Leap" (PDF pp. 24–25, 27)
Tags: case, dating, time-based-application, model-limitation, humor
Related Concepts: 37% Rule applied to time, rejection variant
```

```
CARD ID: B01-C01-10
Title: House-selling reservation price
Type: Model
Summary: With a known offer range and a per-offer cost of waiting, set a stopping price before you
begin and never lower it. On a $400k–$500k range: $1 waiting cost → $499,552.79; $2,000 → $480,000;
$10,000 → $455,279; $50,000 → take the first offer. Depends only on search cost and the spread. Lower
standards only if savings or offers will actually run out.
Source: Algorithms to Live By, ch. 1, "When to Sell" (PDF pp. 30–32)
Tags: optimal-stopping, reservation-price, cost-of-waiting, real-estate, job-search
Related Concepts: Sunk cost, never look back, job search models
```

```
CARD ID: B01-C01-11
Title: Never revisit a rejected offer
Type: Insight
Summary: In cost-of-waiting problems specifically — the chapter names house selling and job hunting —
an earlier offer that is still available should still be refused: the threshold hasn't moved and what
you spent searching is a sunk cost. Domain-restricted; it directly contradicts the recall variant's
advice, and the chapter does not reconcile the two.
Source: Algorithms to Live By, ch. 1, "When to Sell" (PDF p. 33)
Tags: sunk-cost, reservation-price, internal-tension, prescriptive
Related Concepts: Recall variant, Kepler case
```

```
CARD ID: B01-C01-12
Title: Laura Albert McLay holds her price
Type: Case
Summary: An optimization expert selling her own house turned down a strong first offer carrying a
large non-monetary cost (moving out a month early), held her threshold, and got the offer she wanted.
"That would have been really, really hard if I didn't know the math was on my side."
Source: Algorithms to Live By, ch. 1, "When to Sell" (PDF pp. 32–33)
Tags: case, reservation-price, emotional-permission, expert-practitioner
Related Concepts: House-selling model, algorithms as commitment devices
```

```
CARD ID: B01-C01-13
Title: Parking, occupancy rate, and the 85% target
Type: Model
Summary: Parking is a Look-Then-Leap problem whose switch distance is set by occupancy: at 99%, be
ready to take the first spot you see starting at almost 70 spaces (over ¼ mile) out; at 85%, don't
start seriously looking until half a block away. Shoup argues cities should price curb parking to hold
occupancy "somewhere around 85%" — going 90%→95% adds 5% more cars but doubles everyone's search.
Source: Algorithms to Live By, ch. 1, "When to Park" (PDF pp. 33–37)
Tags: optimal-stopping, urban-policy, occupancy, search-cost, Shoup
Related Concepts: Look-Then-Leap, congestion, game theory (ch. 11)
```

```
CARD ID: B01-C01-14
Title: Shoup rides a bike
Type: Insight
Summary: Asked how the world's leading parking expert optimizes his own LA commute, Shoup answered "I
ride my bike." The best response to a hard optimization problem is sometimes to exit it.
Source: Algorithms to Live By, ch. 1, "When to Park" (PDF p. 37)
Tags: problem-framing, avoidance-over-optimization, quotable
Related Concepts: "Some problems are better avoided than solved"
```

```
CARD ID: B01-C01-15
Title: The burglar problem
Type: Model
Summary: For repeated risky ventures with total loss on failure, the optimal number of attempts ≈
(chance of success) / (chance of ruin). 90% success → stop after ~9; 50/50 → essentially once.
Source: Algorithms to Live By, ch. 1, "When to Quit" (PDF p. 38)
Tags: optimal-stopping, risk-of-ruin, quit-while-ahead, expected-value
Related Concepts: Berezovsky case, retirement timing
```

```
CARD ID: B01-C01-16
Title: Boris Berezovsky — expertise that didn't transfer
Type: Case
Summary: The author of the first and only book on the secretary problem went from a mathematician's
salary to Forbes' richest man in Russia ($3bn, 1997), then fell out with Putin, went into exile in
2000, lost most of his fortune in litigation, and died in 2013 in a death ruled suicide. Told
alongside a scene of him spending three hours failing to fix an outboard motor rather than give up.
Source: Algorithms to Live By, ch. 1, "When to Quit" (PDF pp. 37–39)
Tags: case, quit-while-ahead, irony, risk-of-ruin, handle-with-care
Related Concepts: Burglar problem, no-stopping-rule problems
```

```
CARD ID: B01-C01-17
Title: Triple or nothing — a problem with no stopping rule
Type: Insight
Summary: Bet everything at 50/50 for triple; expected value rises every round ($1 → $1.50 → $4.50), so
the math says always play — and always playing guarantees eventual ruin. "Some problems are better
avoided than solved."
Source: Algorithms to Live By, ch. 1, "When to Quit" (PDF p. 39)
Tags: expected-value, ruin, limits-of-optimization, paradox
Related Concepts: Burglar problem, risk of ruin, Kelly criterion (inferred)
```

```
CARD ID: B01-C01-18
Title: Rapoport & Seale — people leap too early
Type: Experiment
Summary: 1990s repeated secretary problems with 40 or 80 applicants. Success ~31% vs. 37% optimal;
behavior matched the Look-Then-Leap form but participants leapt prematurely in over four-fifths of
trials. The authors report "about a dozen studies" agreeing, without individual citations.
Source: Algorithms to Live By, ch. 1, "Always Be Stopping" (PDF p. 40)
Tags: experiment, behavioral, premature-stopping, secretary-problem
Related Concepts: Endogenous time cost, impatience
```

```
CARD ID: B01-C01-19
Title: Endogenous time cost
Type: Claim
Summary: Seale & Rapoport showed that assuming a per-applicant cost of 1% of the prize makes the
optimal switch point match observed behavior exactly — even though the experiment imposed no search
cost. Bearden: "It's not irrational to get bored, but it's hard to model that rigorously." Note the
cost parameter is fitted post hoc.
Source: Algorithms to Live By, ch. 1, "Always Be Stopping" (PDF pp. 40–41)
Tags: rationality, unmodeled-costs, behavioral-economics-critique, post-hoc-fit
Related Concepts: Bounded rationality, cost of waiting
```

```
CARD ID: B01-C01-20
Title: Time makes everything a stopping problem
Type: Insight
Summary: The secretary problem's least believable assumption — strict one-way seriality — is just
time. No choice recurs; hesitation is as irrevocable as action. Hence when to stop is among the most
important aspects of any decision.
Source: Algorithms to Live By, ch. 1, "Always Be Stopping" (PDF pp. 41–42)
Tags: philosophy, irreversibility, thesis, mortality
Related Concepts: Regret, time preference, computational kindness (conclusion)
```

```
CARD ID: B01-C01-21
Title: The tangled origins of the secretary problem
Type: Study
Summary: Traced by the authors through Martin Gardner's correspondence at Stanford. Circulating by
1955 (Mosteller ← Gleason ← ?; Moser ← Gaskell of Boeing ← a colleague; Pinkham ← Shoenfield ←
"someone at Michigan"). Merrill Flood made the first known discovery of the 37% Rule in 1958 and
claimed to have considered it since 1949. First print appearance: Gardner's Scientific American
column, February 1960. Named "secretary problem" in a 1964 paper.
Source: Algorithms to Live By, ch. 1, "The Secretary Problem" (PDF pp. 18–20)
Tags: history-of-mathematics, attribution, Gardner, Flood, archival
Related Concepts: Traveling salesman (ch. 8), prisoner's dilemma (ch. 11)
```

```
CARD ID: B01-C01-22
Title: Formal problems get culturally redressed
Type: Insight
Summary: Chess reads as medieval European but came from eighth-century India and was "Europeanized" in
the fifteenth century — shahs to kings, viziers to queens, elephants to bishops. Optimal stopping
likewise moved from nineteenth-century lotteries and women choosing suitors, to early-twentieth-century
motorists seeking hotels, to mid-century male bosses choosing female assistants.
Source: Algorithms to Live By, ch. 1 (PDF p. 20)
Tags: sociology-of-mathematics, framing, history, aside
Related Concepts: Problem framing, history of science
```

```
CARD ID: B01-C01-23
Title: The Barbara Bush counterexample
Type: Case
Summary: "I married the first man I ever kissed. When I tell this to my children they just about throw
up." — printed as an epigraph directly above the section deriving the 37% Rule for courtship, and never
addressed. A zero-look-phase search that succeeded. Consistent with the math (63% of optimal players
fail; many non-optimal players get lucky) but the chapter never draws that distinction.
Source: Algorithms to Live By, ch. 1, epigraph to "Lover's Leap" (PDF p. 24)
Tags: case, counterexample, outcome-bias, process-vs-outcome, epigraph
Related Concepts: 63% failure rate, outcome bias, satisficing
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: A wide range of everyday irreversible sequential decisions share the structure of optimal
stopping, which computer science has solved; the answer is usually to explore a fixed fraction and then
commit, and high failure rates are a property of the problem rather than of human reasoning.

Top 5 Concepts:
1. Optimal stopping (the class of "when to act" problems)
2. The secretary problem and the 37% Rule (1/e)
3. Look-Then-Leap Rule vs. Threshold Rule
4. No-information vs. full-information games
5. Endogenous time cost of search

Top 3 Claims:
1. Look at 37% of options, then take the next best-yet — success rate 37%, invariant to pool size.
2. Objective, population-calibrated information eliminates the look phase and lifts success to 58%.
3. Human early-stopping may be rational once the searcher's own time costs are counted.

Top 3 Cases:
1. Kepler's eleven courtships and his self-reproach (recall variant)
2. Michael Trick's age-26.1 calculation, proposal, and rejection (rejection variant)
3. Boris Berezovsky — the man who wrote the only book on the secretary problem and never stopped

Top 3 Studies:
1. Rapoport & Seale, 1990s repeated secretary problems (31% success; premature leaping in >80% of
   trials)
2. Seale & Rapoport's cost-adjusted reanalysis (1% per-applicant cost reproduces observed behavior;
   post hoc fit)
3. The authors' archival reconstruction of the problem's origins in Gardner's papers (Flood, 1958)

Most Unique Idea: That strict one-way seriality — the secretary problem's least believable
assumption — is simply what time is, so all decision-making is optimal stopping and hesitation is as
irrevocable as action.

Most Counterintuitive Idea: Your chance of finding the single best option is 37% whether the pool holds
a hundred candidates or a million — so the algorithm becomes more valuable, not less, as the search
gets bigger.

Biggest Weakness or Open Question: The chapter's models define success as obtaining the single best
option, which almost nobody actually requires; it never analyses satisficing objectives, and it gives
directly opposed prescriptions on revisiting past options (Kepler's fallback vs. "never look back")
without stating the condition that separates them. Its evidentiary base is also thin relative to the
breadth of its prescriptions — two findings from a single research pair (Rapoport & Seale), one
archival investigation by the authors themselves, and a series of mathematical results asserted
without derivation in-chapter.

Best Content Opportunity: A long-form video on the 37% Rule built around Kepler and Trick as
mirror-image failures of the model's assumptions, with the 63% failure rate as the honest twist.
```
