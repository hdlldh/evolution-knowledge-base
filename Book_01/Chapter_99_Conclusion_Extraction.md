# Algorithms to Live By: The Computer Science of Human Decisions — Conclusion: Computational Kindness
**Author:** Brian Christian and Tom Griffiths
**Type:** Extraction
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 324–331 (book Conclusion)
**Date:** 2026-07-22
**Revision note:** Revised after Chapter_99_Conclusion_Audit.md; see that file for what changed and why.

```
BOOK:
Algorithms to Live By: The Computer Science of Human Decisions

AUTHOR:
Brian Christian and Tom Griffiths

CHAPTER:
Conclusion — Computational Kindness
```

*Note: This is the book's short synthesizing Conclusion, not a full chapter. It gathers the book's
lessons into "three pieces of wisdom" and introduces one genuinely new idea — computational kindness. The
entry is scaled accordingly; empty sections are marked rather than padded.*

---

## 1. Chapter Thesis

Any system bound by space and time faces the same core computational problems, which makes computers "not
only our tools but also our comrades." From this the book distills three pieces of wisdom: (1) some
algorithms transfer straight to human life (the 37% Rule, LRU, the Upper Confidence Bound); (2) using an
optimal *process* should bring relief even when the *outcome* is bad — a "computational Stoicism"; and
(3) heuristics, approximation, and strategic randomness are how to handle the intractable, so "good
enough" often really is good enough, and we should choose tractable problems when we can. The
Conclusion's original contribution is a bridge from computer science to ethics — **computational
kindness**: because interacting with others hands them hard computational problems (above all, simulating
our minds), we should frame requests, options, and even physical environments to *minimize the labor of
thought* for others and ourselves. The closing reframe: making assumptions, favoring simpler solutions,
trading error against delay, and taking chances are "not the concessions we make when we can't be
rational — they're what being rational means."

## 2. Key Concepts

```
Concept Name: Computational Kindness
Definition: Framing problems — social requests, choices, and designs — so as to minimize the
computational (cognitive) load they impose on others and on ourselves.
Why It Matters: A bridge from computer science to ethics; because "computation is bad" (a good algorithm
minimizes the labor of thought), reducing others' mental labor is a genuine form of kindness — and often
diverges from conventional etiquette.
How the Author Uses It: The dinner-group and "I'm flexible" cases; the 18-cent coin; parking-lot design;
restaurant seating; the bus-stop display.
Related Concepts: Process vs. outcome, verification vs. search, spinning vs. blocking, simulating other
minds (ch. 11).
```

```
Concept Name: Process vs. Outcome ("Computational Stoicism")
Definition: Judge yourself by whether you followed the best available process, not by whether the outcome
happened to be good — since even optimal algorithms often yield bad results.
Why It Matters: The 37% Rule fails 63% of the time; LRU (or even clairvoyance) can't guarantee a cache
hit; UCB doesn't erase regret, only slows it. Following the best process is all you can do.
How the Author Uses It: The relief-not-guilt lesson, anchored in Bertrand Russell's "wisest act" (the one
that will *probably* be most fortunate).
Related Concepts: Outcome bias (ch. 1), 37% Rule, LRU, UCB, being kind to ourselves.
```

```
Concept Name: Verification vs. Search (the complexity gap)
Definition: Recognizing a good option is far easier than generating one — "as wide as the gap between
knowing a good song when you hear it and writing one on the spot."
Why It Matters: It explains why people prefer a *constrained* request ("next Tuesday, 1–2 p.m.") over an
open one ("whenever's convenient"), even when the constraints are arbitrary — accepting/declining is
verification; proposing is search.
How the Author Uses It: The interview-scheduling paradox and the case for offering concrete options.
Related Concepts: Computational kindness, intractability (ch. 8), the halting problem (ch. 11).
```

```
Concept Name: Spinning vs. Blocking (whose CPU pays?)
Definition: When a resource is unavailable, one can "spin" (keep checking in an "Is it ready yet?" loop)
or "block" (stop, do something else, and be notified when it's free).
Why It Matters: In shared human settings the CPUs being burned are other people's minds; open seating
"spins" customers, while take-a-name-and-notify "blocks" them — a computationally kinder design.
How the Author Uses It: Restaurant seating and the bus-stop display (a "cognitive subsidy").
Related Concepts: Computational kindness, design, scheduling (ch. 5).
```

## 3. Key Claims

```
Claim: Some computer-science algorithms transfer directly to human problems.
Type: Synthesis / Prescriptive
Evidence Provided: The 37% Rule (optimal stopping), the Least Recently Used criterion (caching), and the
Upper Confidence Bound (explore/exploit) are named as ready-to-transfer examples.
Strength of Support: Strong within the book — each was developed and defended in earlier chapters.
```

```
Claim: Judge decisions by process, not outcome — even optimal strategies often fail.
Type: Prescriptive / Interpretive
Evidence Provided: The 37% Rule fails 63% of the time; LRU and even clairvoyance can't guarantee cache
hits; UCB only slows the accumulation of regret. Russell: the "wisest act" is the one that will
*probably* be most fortunate.
Strength of Support: Strong. Grounded in the book's own earlier results plus a philosophical warrant.
```

```
Claim: For intractable problems, heuristics, approximation, and strategic randomness make "good enough"
genuinely good enough — and we should choose tractable problems when we can.
Type: Synthesis / Prescriptive
Evidence Provided: A recurring interview theme among computer scientists; the tractable/intractable line
drawn across the book (esp. ch. 8).
Strength of Support: Strong within the book's framework.
```

```
Claim: Interacting with others imposes computational problems on them, so we can be "computationally
kind" by lowering that load.
Type: Interpretive (the book's original bridge to ethics)
Evidence Provided: The interview-scheduling paradox (people prefer a constrained request); "computation
is bad" as an implicit CS directive; the dinner-group and "I'm flexible" cases; concrete design examples.
Strength of Support: Moderate to Strong. A compelling, well-illustrated principle, explicitly framed as a
bridge/analogy rather than a proven law.
```

```
Claim: Design can radically change the cognitive problem it poses — so designers should minimize mental
labor.
Type: Prescriptive
Evidence Provided: Shallit's 18-cent coin (mathematically optimal for change but "at least as hard as the
traveling salesman problem"; a 2- or 3-cent piece is computationally kinder); helix parking garages (zero
computational load); spinning vs. blocking restaurant seating; the bus-stop countdown as a "cognitive
subsidy."
Strength of Support: Strong. Several concrete, vivid design cases with a named study.
```

```
Claim: Bounded, "good enough" rationality is not a concession — it is what rationality actually is.
Type: Interpretive (the book's redemptive thesis)
Evidence Provided: The picture of computers grinding to perfect answers is "a luxury afforded by an easy
problem"; in hard cases (which people almost always face) the best algorithms make assumptions, favor
simpler solutions, trade error against delay, and take chances.
Strength of Support: Strong as the book's culminating argument; interpretive by nature.
```

## 4. Frameworks, Models, and Mental Models

```
Name: The Three Pieces of Wisdom
Description: The book's closing synthesis of what computational thinking offers human life.
Components: (1) transferable algorithms (37% Rule, LRU, UCB); (2) process-over-outcome / computational
Stoicism; (3) embrace heuristics/approximation/randomness for the intractable, and choose tractable
problems.
How It Works: Any space-and-time-bound system faces the same computational problems, so computers'
solutions become guides for living.
When It Is Useful: A high-level checklist for applying the whole book.
Limitations: A synthesis, not a new result; each piece is defended earlier, not here.
```

```
Name: Computational Kindness
Description: An ethic and a design principle: minimize the labor of thought you impose on others.
Components: The insight that "computation is bad"; the verification-vs-search gap; a divergence from mere
etiquette.
How It Works: Assert your preferences rather than withhold them; offer few concrete options rather than
many open ones; design environments (coins, parking, seating, signage) that pose easy computational
problems.
When It Is Useful: Social coordination and any design that people must reason through.
Limitations: Can feel "impolite"; the boundary between kind constraint and imposed constraint is
unspecified.
```

```
Name: Spinning vs. Blocking
Description: Two ways to wait for a scarce resource, and a lens on whose attention a design consumes.
Components: Spin (poll repeatedly) vs. block (stop and be notified); the cost of polling vs. the cost of
a context switch.
How It Works: In computing it's a time tradeoff; in human settings, "spinning" burns other people's
attention (open seating, squinting for the bus), while "blocking" frees it (name-and-notify, a countdown
display).
When It Is Useful: Designing queues, waiting rooms, notifications, transit.
Limitations: Blocking needs infrastructure (a notification system, arrival prediction) that may not
exist.
```

## 5. Research and Evidence

```
Study / Research: Shallit's optimal-denomination analysis
Researchers: Jeffrey Shallit (University of Waterloo)
Year: 2003
Research Question: What single new US coin would most reduce the average number of coins needed to make
change?
Method: Combinatorial/algorithmic analysis of denominations.
Key Finding: An 18-cent piece minimizes coins on average — but it makes change-making "at least as hard
as the traveling salesman problem" (the simple greedy algorithm stops being optimal). Accounting for ease
of computation, a 2-cent or 3-cent piece is nearly as good and far "computationally kinder."
How the Author Uses It: The flagship example that design should weigh users' *computational* cost, not
just materials and money.
Important Limitations: A theoretical currency-design result, not an implemented policy.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: The "constrained request" / scope-insensitivity parallels
Researchers: Not specified (the authors' own interview observation; "celebrated studies" cited without
attribution)
Year: Not specified.
Research Question: Why do people accommodate an arbitrarily constrained request more readily than an open
one?
Method: The authors' informal observation while scheduling interviews, framed alongside well-known
scope-insensitivity findings.
Key Finding: Interviewees were more available for "next Tuesday, 1–2 p.m. PST" than "a convenient time
this week"; likewise people reportedly donate more to save one penguin than eight thousand, and worry
more about dying from terrorism than from all causes including terrorism.
How the Author Uses It: To motivate the verification-vs-search gap and computational kindness.
Important Limitations: The penguin/terrorism "studies" are cited without sources — anecdotal here; per the
book's own rule, treat as illustrative, not established data.
Replication or Controversy Mentioned: None; attribution not given.
```

## 6. Experiments

None identified. (The Conclusion synthesizes rather than presenting new experiments; the Shallit result
is an analysis, not an experiment.)

## 7. Cases and Stories

```
Case Title: The interview-scheduling paradox
People / Organization: Brian Christian and Tom Griffiths
Context: Scheduling the interviews for the book.
What Happened: Interviewees were, on average, more likely to be available when asked for a specific slot
("next Tuesday between 1:00 and 2:00 p.m. PST") than for "a convenient time this coming week." Accepting
or declining a concrete proposal is verification; generating a good time is search — a far harder
computation.
Outcome: A concrete constraint, even an arbitrary one, is a kindness.
Concept Illustrated: Verification vs. search; computational kindness.
Why This Case Is Useful: A relatable, immediately actionable illustration of the whole principle.
Potential for Reuse: High
```

```
Case Title: Brian's Spain trip and the bullfight nobody wanted
People / Organization: Brian Christian and two friends
Context: Negotiating a trip itinerary on the fly the summer after college.
What Happened: When it became clear they'd miss a bullfight they'd researched, each tried to console the
others — only to discover none of them had wanted to go. Each had "gamely adopted what they'd perceived
to be the others' level of enthusiasm," thereby producing that very enthusiasm in a feedback loop.
Outcome: Politely withholding preferences manufactured a phantom consensus.
Concept Illustrated: The cost of not stating preferences; simulating other minds; computational kindness.
Why This Case Is Useful: A vivid, funny, universal illustration of etiquette's hidden computational harm.
Potential for Reuse: High
```

```
Case Title: "Oh, I'm flexible" — the dark computational underbelly
People / Organization: The authors
Context: A friend group deciding where to eat.
What Happened: Seemingly kind phrases like "I'm flexible" or "What do you want to do tonight?" do two
alarming things: they pass the cognitive buck ("here's a problem, you handle it"), and by withholding
preferences they force others to *simulate* yours — one of the hardest computations a mind can attempt.
Computational kindness instead asserts preferences ("I'm inclined toward x — what do you think?") or
offers two or three concrete options.
Outcome: Kindness and etiquette diverge; asserting preferences shoulders the cognitive load.
Concept Illustrated: Computational kindness vs. conventional etiquette.
Why This Case Is Useful: The chapter's most quotable, behavior-changing lesson.
Potential for Reuse: High
```

```
Case Title: The 18-cent coin
People / Organization: Jeffrey Shallit (University of Waterloo)
Context: What new coin would minimize coins needed to make change.
What Happened: An 18-cent piece is mathematically optimal, but it breaks the simple greedy change-making
algorithm (54¢ becomes three 18-cent pieces, no quarters) and makes change-making "at least as hard as
the traveling salesman problem." A 2- or 3-cent piece is almost as good and vastly kinder to cashiers.
Outcome: The mathematically optimal design can be the cognitively cruelest.
Concept Illustrated: Computational kindness as a design principle.
Why This Case Is Useful: A precise, surprising case that separates "optimal" from "usable."
Potential for Reuse: High
```

```
Case Title: Parking lots, restaurant seating, and the bus-stop display
People / Organization: The authors
Context: Everyday designs that impose or relieve computation.
What Happened: A multi-lane lot forces an optimal-stopping problem; a single-helix garage reduces the
computational load to zero (take the first space). Open restaurant seating makes customers "spin"
(vigilant polling); name-and-notify lets them "block." A bus-stop countdown ("arriving in 10 minutes")
lets you decide *once* instead of re-deciding moment by moment — a "cognitive subsidy" that could boost
ridership as much as cheaper fares.
Outcome: Design structures the computational problems people must solve; good design minimizes them —
"one of the chief goals of design ought to be protecting people from unnecessary tension, friction, and
mental labor." This isn't merely abstract: when mall parking becomes a source of stress, shoppers may
spend less money and return less frequently — computational unkindness has a commercial cost.
Concept Illustrated: Computational kindness in design; spinning vs. blocking; optimal stopping (ch. 1);
Bayesian inference (ch. 6).
Why This Case Is Useful: A cluster of concrete, adoptable design lessons tying the whole book together.
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: Computational kindness (assert, don't withhold)
Example: "Oh, I'm flexible" secretly passes the cognitive buck and forces others to simulate your
preferences; "I'm inclined toward x — what do you think?" shoulders the load instead.
Why It Works: It reveals a everyday "polite" phrase as an act of hidden imposition — instantly
behavior-changing.
Possible Alternative Domain: Business
```

```
Concept: Verification vs. search
Example: People accept "next Tuesday, 1–2 p.m." more readily than "whenever's convenient" — judging a
proposal is far easier than generating one, like knowing a good song vs. writing one on the spot.
Why It Works: A familiar scheduling annoyance exposes a deep complexity gap.
Possible Alternative Domain: Psychology
```

```
Concept: Optimal design can be cognitively cruel
Example: The mathematically optimal 18-cent coin turns making change into a traveling-salesman problem;
a 2- or 3-cent coin is nearly as good and far kinder.
Why It Works: A crisp, counterintuitive case that "best on paper" ≠ "best for people."
Possible Alternative Domain: Business
```

```
Concept: Process over outcome (computational Stoicism)
Example: The 37% Rule fails 63% of the time — following it is still all you can do; judge the process,
not the luck.
Why It Works: A hard number turns a Stoic maxim into a decision rule.
Possible Alternative Domain: Sports
```

```
Concept: Spinning vs. blocking
Example: Open seating makes customers "spin" in tedious vigilance; take-a-name-and-notify lets them
"block" and relax — same table, kinder to their attention.
Why It Works: Maps a computing tradeoff onto an experience everyone has had.
Possible Alternative Domain: Business
```

## 9. Counterintuitive Insights

```
Insight: Computation is "bad" — a good algorithm minimizes the labor of thought.
Common Belief: More thorough deliberation is better.
Author's Argument: The point of a good algorithm is to think as little as necessary; imposing thought on
others (or yourself) is a cost, so minimizing it is a kindness.
Evidence: The verification-vs-search gap; the constrained-request paradox.
Why It Is Surprising: It reframes "less thinking" as the goal, not a shortcut.
```

```
Insight: Being "polite" can be computationally unkind.
Common Belief: Withholding your preferences ("I'm flexible") is considerate.
Author's Argument: It passes the cognitive buck and forces others to simulate your mind — a huge
computation; asserting your preference is the real kindness.
Evidence: The dinner group; Brian's phantom-consensus bullfight.
Why It Is Surprising: Etiquette and kindness diverge.
```

```
Insight: The mathematically optimal design can be the worst for people.
Common Belief: Optimizing the numbers optimizes the experience.
Author's Argument: The optimal 18-cent coin makes change-making NP-hard; good design must weigh users'
*computational* cost, not just materials and money.
Evidence: Shallit's analysis; helix parking; countdown signage.
Why It Is Surprising: "Optimal" and "usable" can be opposites.
```

```
Insight: Cutting corners is what rationality *is*, not a failure of it.
Common Belief: Rationality means weighing every option fully and choosing the best.
Author's Argument: That's a luxury of easy problems; in the hard cases people actually face, the best
algorithms assume, simplify, trade error against delay, and take chances.
Evidence: The book's cumulative results across all chapters.
Why It Is Surprising: It redeems "good enough" as the definition of rational, not a concession.
```

## 10. Unique or Unusual Ideas

```
Idea: Computational kindness as an ethics.
Why It Seems Unique: It derives a moral/design principle directly from complexity theory — treat others'
attention as a scarce computational resource.
Potential Connection to Other Topics: UX and choice architecture; the ethics of attention; nudges;
accessibility.
```

```
Idea: A "cognitive subsidy."
Why It Seems Unique: It reframes public-service design (a bus countdown) as subsidizing citizens' mental
effort — potentially as effective as subsidizing fares.
Potential Connection to Other Topics: Public policy, transit design, behavioral economics.
```

```
Idea: "Computational Stoicism."
Why It Seems Unique: It fuses ancient Stoic process-over-outcome ethics with the algorithmic fact that
optimal strategies routinely fail — a modern warrant for self-forgiveness.
Potential Connection to Other Topics: Stoicism, outcome bias, mental health, decision hygiene.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: Where is the line between kind constraint and imposed constraint?
Author's Position: Offering a concrete slot or a short menu is computationally kind.
Possible Counterargument: The same act can be controlling or presumptuous; the Conclusion doesn't say
when reducing others' options becomes overriding their autonomy.
What Evidence Would Help Resolve It: When people experience constraint as relief vs. as imposition.
```

```
Issue: The scope-insensitivity "studies" are cited without sources.
Author's Position: People donate more to save one penguin than eight thousand, and fear terrorism more
than all-cause death.
Possible Counterargument: Per the book's own non-invention rule, these are unattributed here and function
as illustration, not evidence; the penguin figure in particular is presented anecdotally.
What Evidence Would Help Resolve It: The primary scope-insensitivity literature (not provided in the
text).
```

## 12. Quotable Ideas

```
Paraphrase (short): Relief by machines from our demanding intellectual functions may finally give us time
and incentive to learn to live well together. (Merrill Flood, epigraph)
Why the Idea Matters: The humane frame for the whole book — computation in service of living well.
Source Location: Conclusion epigraph (PDF p. 324).
```

```
Paraphrase (short): The wisest act is the one that will *probably* be most fortunate — we hope to be
fortunate, but should strive to be wise. (after Bertrand Russell)
Why the Idea Matters: The process-over-outcome ethic ("computational Stoicism").
Source Location: Conclusion (PDF p. 325).
```

```
Paraphrase (short): Computation is bad — the underlying directive of any good algorithm is to minimize
the labor of thought.
Why the Idea Matters: The premise from which computational kindness follows.
Source Location: Conclusion (PDF p. 326).
```

```
Paraphrase (short): "I'm flexible" has a dark computational underbelly: it passes the cognitive buck and
makes others simulate your mind.
Why the Idea Matters: The chapter's sharpest, most actionable behavioral lesson.
Source Location: Conclusion (PDF p. 327).
```

```
Paraphrase (short): Think of a bus-stop countdown as a cognitive subsidy — it can do as much for
ridership as cutting the fare.
Why the Idea Matters: Computational kindness as public-policy design.
Source Location: Conclusion (PDF pp. 329–330).
```

```
Paraphrase (short): Making assumptions, favoring simpler solutions, trading error against delay, and
taking chances aren't concessions we make when we can't be rational — they're what being rational means.
Why the Idea Matters: The book's redemptive final sentence.
Source Location: Conclusion (PDF pp. 330–331).
```

## 13. Psychology Connections

- **Process vs. outcome / outcome bias.** "Computational Stoicism" is a direct antidote to outcome bias
  (judging a decision by its result) — echoing chapter 1's treatment and Russell's "wisest act."
- **Scope insensitivity.** The penguin and terrorism examples invoke the well-known failure to scale
  emotional responses to magnitude.
- **Cognitive load and choice overload.** Reducing options and offering concrete proposals connects to
  choice-overload and decision-fatigue research.
- **Theory of mind.** "Simulating the minds of others" as the hardest computation ties the Conclusion
  back to chapter 11's recursion.
- **Self-compassion.** "Being kinder to ourselves" — forgiving bounded rationality — is a mental-health-
  relevant reframing of what it means to decide well.

## 14. Mathematics and Decision Science Connections

- **Verification vs. search (P vs. NP flavor).** Recognizing a good solution vs. generating one — the
  complexity gap underlying the constrained-request paradox.
- **Tractability and heuristics.** The tractable/intractable line (ch. 5, 8) and the legitimacy of
  approximation and "good enough."
- **Optimal denominations / change-making.** Shallit's result linking currency design to the traveling
  salesman problem.
- **Optimal stopping.** The parking-lot design as an applied optimal-stopping problem (ch. 1).
- **Bayesian inference.** Using "when the last bus left" as a proxy for the next arrival (ch. 6).
- **Bounded rationality.** The redefinition of rationality as making sensible tradeoffs under time and
  information limits.

## 15. Sports Connections

**Direct examples from the book:** None identified.

**Inferred applications (mine):**
- **Judge the process, not the scoreboard.** "Computational Stoicism" is the analytics-era coaching
  creed: a well-designed play or a +EV decision (going for it on 4th down, a sound shot selection) is
  correct even when it fails, because outcomes are noisy — evaluate the decision, not the result.
- **Computationally kind play-calling.** Simple, rehearsed schemes reduce players' in-the-moment
  cognitive load (fewer options, faster reads), much like offering a short menu instead of an open field
  of choices.
- **"Good enough" under a clock.** Athletes almost always face the "hard cases" — decisions under time
  and uncertainty — where heuristics and quick, biased-toward-simple choices beat exhaustive deliberation.

## 16. AI and Machine Learning Connections

**Direct from the book:** The Conclusion names transferable algorithms (37% Rule / optimal stopping, LRU
caching, UCB for explore/exploit) and the spinning-vs-blocking systems tradeoff; "computation is bad" is
an explicit algorithm-design directive.

**Inferred connections (mine):**
- **Human-centered / kind interface design.** Computational kindness is essentially UX and choice
  architecture for AI systems: an assistant should propose concrete options (verification) rather than
  demand the user articulate an underspecified goal (search) — reducing the human's cognitive load.
- **Cost-of-computation as an objective.** "Minimize the labor of thought" parallels anytime algorithms,
  bounded/meta-reasoning, and latency-vs-quality tradeoffs — spending compute (human or machine) only
  where it pays.
- **Process vs. outcome in evaluation.** Judging a policy by its decision quality rather than a noisy
  single outcome mirrors off-policy evaluation and reward-vs-return distinctions in RL.
- **Spinning vs. blocking.** A direct systems concept (polling vs. interrupt/callback) relevant to
  scheduling, serving, and agent orchestration.
- **Reducing the option space.** Offering a small, curated set of choices connects to constrained
  decoding, candidate generation + reranking, and interfaces that surface a few good options rather than
  an open field.

## 17. Content Creation Opportunities

```
Idea Title: The kindest thing you can say is "I'm NOT flexible"
Format: YouTube Long-form
Application Domain: Everyday Life
Hidden Principle: Decision Making
Story Hook (Layer 1): The most "polite" thing you say — "Oh, I'm flexible, whatever works" — is secretly
one of the cruelest, and computer science can prove it.
Principle Framework (Layer 2): Computational kindness: interacting with others hands them hard computa-
tional problems (above all, simulating your mind), so minimizing their labor of thought is a real ethic.
Assert a concrete option — verification is easy, open-ended search is hard.
Best Supporting Case: The interview-scheduling paradox (a constrained request beats an open one); Brian's
phantom-consensus bullfight; the 18-cent coin; the bus-stop "cognitive subsidy."
Character Application: Insight: Interpreter
Psychology Angle: Cognitive load; theory of mind; choice overload.
Math Angle: Verification vs. search; change-making as a traveling-salesman problem.
Sports Angle: Simple play-calling to cut players' in-the-moment load.
Business Angle: Proposing two options over "what do you all think?" to unblock a meeting.
Investing Angle: Bringing a concrete recommendation, not an open menu, to a decision committee.
History Angle: Etiquette norms of "deference" reread as offloading cognitive cost onto others.
AI Angle: Kind interface design — propose options, don't demand an underspecified goal.
```

```
Idea Title: Even the best strategy fails most of the time (and that's fine)
Format: YouTube Short
Application Domain: Everyday Life
Hidden Principle: Decision Making
Story Hook (Layer 1): The optimal way to find a partner or an apartment fails 63% of the time — and here's
why that means you did everything right.
Principle Framework (Layer 2): Judge the process, not the outcome ("computational Stoicism"): even optimal
algorithms routinely fail, so following the best available process is all you can do — hope to be
fortunate, but strive to be wise.
Best Supporting Case: The 37% Rule's 63% failure rate; Russell's "wisest act"; LRU and UCB never
guaranteeing success.
Character Application: Nova: Strategist
Psychology Angle: Outcome bias; self-compassion.
Math Angle: Optimal stopping; expected value vs. realized outcome.
Sports Angle: Judge the 4th-down decision, not whether the play worked.
Business Angle: Rewarding good decisions that lost, not lucky bets that won.
Investing Angle: Process-based evaluation over a single quarter's return.
History Angle: Stoic process-focus meeting the modern math of unavoidable failure rates.
AI Angle: Decision-quality vs. single-outcome (single-rollout) evaluation.
```

```
Idea Title: Why the "perfect" coin would ruin your day
Format: YouTube Short
Application Domain: Business
Hidden Principle: Optimization
Story Hook (Layer 1): A mathematician found the perfect new coin to minimize the change in your pocket —
and it would also turn every cash register into a traveling-salesman problem.
Principle Framework (Layer 2): The mathematically optimal design can be the cognitively cruelest; good
design minimizes the user's computational load, not just materials or money. Optimize for usable, not
just optimal.
Best Supporting Case: Shallit's 18-cent coin vs. a 2- or 3-cent piece; single-helix parking garages;
countdown bus signs as a "cognitive subsidy."
Character Application: Sigma: Architect
Psychology Angle: Cognitive load in everyday environments.
Math Angle: Change-making; greedy algorithms; NP-hardness.
Sports Angle: None core.
Business Angle: UX and pricing that trade a little "optimality" for a lot of usability.
Investing Angle: A simple, followable plan beating a theoretically optimal one no one executes.
History Angle: Currency and standards designed (or not) for the humans who must compute with them.
AI Angle: Cost-of-computation as a first-class design objective.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B01-C99-01
Title: Three pieces of wisdom from computational thinking
Type: Insight
Summary: Any space-and-time-bound system faces the same computational problems, making computers "not
only our tools but also our comrades." Three lessons: (1) some algorithms transfer straight to life — the
37% Rule, LRU caching, the Upper Confidence Bound; (2) judge yourself by *process*, not *outcome*, since
even optimal strategies often fail; (3) for the intractable, heuristics, approximation, and strategic
randomness make "good enough" genuinely good enough — and choose tractable problems when you can.
Source: Algorithms to Live By, Conclusion (PDF pp. 324–325)
Tags: synthesis, 37-percent-rule, LRU, UCB, good-enough, insight
Related Concepts: computational kindness, process vs. outcome, intractability (ch. 8)
```

```
CARD ID: B01-C99-02
Title: Process over outcome — computational Stoicism
Type: Insight
Summary: Even the best algorithm often yields bad results, so distinguish "process" from "outcome": the
37% Rule fails 63% of the time; LRU (or even clairvoyance) can't guarantee a cache hit; UCB only slows
the accumulation of regret. If you followed the best process, you've done all you can — don't blame
yourself for bad luck. Russell: the "wisest act" is the one that will *probably* be most fortunate. Hope
to be fortunate; strive to be wise.
Source: Algorithms to Live By, Conclusion (PDF pp. 324–325)
Tags: process-vs-outcome, computational-stoicism, outcome-bias, regret, insight
Related Concepts: 37% Rule (ch. 1), UCB (ch. 2), self-forgiveness
```

```
CARD ID: B01-C99-03
Title: Computational kindness
Type: Concept
Summary: Because "computation is bad" (a good algorithm minimizes the labor of thought), and because
interacting with others hands them hard computational problems — above all, simulating our minds — we
can be *computationally kind* by framing issues to make those problems easier. This bridges computer
science to ethics, and often diverges from etiquette: politely withholding preferences dumps the
inference burden on others; politely asserting them shoulders the load.
Source: Algorithms to Live By, Conclusion (PDF pp. 325–327)
Tags: computational-kindness, ethics, cognitive-load, etiquette, concept
Related Concepts: verification vs. search, simulating other minds (ch. 11), design
```

```
CARD ID: B01-C99-04
Title: Verification vs. search — why constraints are a kindness
Type: Insight
Summary: Recognizing a good option is far easier than generating one — "as wide as the gap between
knowing a good song when you hear it and writing one on the spot." That's why people accept "next
Tuesday, 1–2 p.m. PST" more readily than "a convenient time this week," even when the constraints are
arbitrary: accepting/declining is verification; proposing is search. So offer concrete options or a short
menu rather than an open field.
Source: Algorithms to Live By, Conclusion (PDF pp. 325–326)
Tags: verification-vs-search, scheduling, cognitive-load, complexity-gap, insight
Related Concepts: computational kindness, intractability (ch. 8), choice overload
```

```
CARD ID: B01-C99-05
Title: "I'm flexible" is computationally unkind
Type: Insight
Summary: Seemingly kind phrases ("Oh, I'm flexible"; "What do you want to do tonight?") do two alarming
things: they pass the cognitive buck, and by withholding your preferences they force others to *simulate*
your mind — one of the hardest computations a mind can face. Brian's Spain trip: three friends each
adopted the others' *perceived* enthusiasm for a bullfight none of them wanted, manufacturing a phantom
consensus. Kindness: assert your preference ("I'm inclined toward x — what do you think?") or offer two
or three options.
Source: Algorithms to Live By, Conclusion (PDF pp. 326–327)
Tags: computational-kindness, preferences, theory-of-mind, etiquette, insight
Related Concepts: simulating other minds (ch. 11), verification vs. search
```

```
CARD ID: B01-C99-06
Title: Computationally kind design — the 18-cent coin and beyond
Type: Case
Summary: Design structures the computational problems people must solve, so minimize their mental labor.
Jeffrey Shallit (2003) found an 18-cent coin would minimize coins for change — but it breaks the simple
greedy algorithm and makes change-making "at least as hard as the traveling salesman problem"; a 2- or
3-cent piece is nearly as good and far kinder. Likewise: helix parking garages (take the first space,
zero load) vs. multi-lane lots (an optimal-stopping problem); restaurant "name-and-notify" vs. open
seating; a bus-stop countdown as a "cognitive subsidy." "One of the chief goals of design ought to be
protecting people from unnecessary tension, friction, and mental labor" — and it pays: stressful mall
parking makes shoppers spend less and return less often.
Source: Algorithms to Live By, Conclusion (PDF pp. 327–330)
Tags: design, computational-kindness, 18-cent-coin, spinning-vs-blocking, case
Related Concepts: optimal stopping (ch. 1), Bayesian inference (ch. 6), UX
```

```
CARD ID: B01-C99-07
Title: Spinning vs. blocking — whose attention does the design burn?
Type: Model
Summary: When a resource is unavailable, a system can "spin" (poll in an "Is it ready yet?" loop) or
"block" (stop, do other work, be notified when it's free) — in computing, a tradeoff between polling time
and context-switch time. In human settings the CPUs burned are other people's minds: open restaurant
seating makes customers spin in tedious vigilance, while name-and-notify lets them block and relax; a
live bus countdown lets you decide *once* rather than re-deciding moment by moment.
Source: Algorithms to Live By, Conclusion (PDF pp. 328–330)
Tags: spinning-vs-blocking, design, attention, scheduling, model
Related Concepts: computational kindness, context switching (ch. 5)
```

```
CARD ID: B01-C99-08
Title: Good-enough is what rationality actually means
Type: Insight
Summary: The picture of computers grinding to perfect answers is "a luxury afforded by an easy problem."
People almost always face the hard cases, where the best algorithms make assumptions, favor simpler
solutions, trade the cost of error against the cost of delay, and take chances. "These aren't the
concessions we make when we can't be rational. They're what being rational means." The book's redemptive
close — and a warrant to be kinder, and more forgiving, to ourselves.
Source: Algorithms to Live By, Conclusion (PDF pp. 330–331)
Tags: bounded-rationality, good-enough, self-compassion, redefinition, insight
Related Concepts: intractability (ch. 8), heuristics, randomness (ch. 9)
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: Every space-and-time-bound system faces the same computational problems, so computers are
"comrades," not just tools. The book's lessons condense into three pieces of wisdom — transferable
algorithms (37% Rule, LRU, UCB); process over outcome ("computational Stoicism"); and heuristics/
approximation/randomness for the intractable, where "good enough" really is good enough. The Conclusion's
original contribution is computational kindness: since interacting with others (and designing their
environments) hands them hard computational problems — above all simulating our minds — we should frame
requests, options, and designs to minimize the labor of thought. And bounded, corner-cutting rationality
isn't a concession; it is what being rational means.

Top 5 Concepts:
1. Computational kindness (an ethic and a design principle)
2. Process vs. outcome ("computational Stoicism")
3. Verification vs. search (why concrete constraints are a kindness)
4. Spinning vs. blocking (whose attention a design consumes)
5. The three pieces of wisdom / bounded rationality as real rationality

Top 3 Claims:
1. Interacting with others imposes computational problems on them; we can be "computationally kind" by
   lowering that load.
2. Judge decisions by process, not outcome — even optimal strategies routinely fail.
3. Cutting corners (assumptions, simpler solutions, error-vs-delay tradeoffs, chance) is what rationality
   is, not a failure of it.

Top 3 Cases:
1. The interview-scheduling paradox (constrained request > open request)
2. "I'm flexible" and Brian's phantom-consensus bullfight
3. The 18-cent coin and computationally kind design (parking helixes, name-and-notify, bus countdowns)

Top 3 Studies:
1. Shallit's optimal-denomination analysis (2003)
2. (Cited, unattributed) scope-insensitivity parallels — penguins, terrorism
3. None further (the Conclusion synthesizes rather than presenting new studies)

Most Unique Idea: Computational kindness — deriving an ethics and a design principle directly from
complexity theory (treat others' attention as a scarce computational resource), including the "cognitive
subsidy."

Most Counterintuitive Idea: Being "polite" (saying "I'm flexible") can be computationally cruel, and the
mathematically optimal design (an 18-cent coin) can be the worst for people — because minimizing the labor
of thought, not the numbers, is the real goal.

Biggest Weakness or Open Question: The scope-insensitivity "studies" (penguins, terrorism) are cited
without attribution and function as illustration, not evidence; and the Conclusion doesn't mark the line
between computationally kind constraint and autonomy-overriding imposition.

Best Content Opportunity: "The kindest thing you can say is 'I'm NOT flexible'" — computational kindness
via the scheduling paradox, the phantom-consensus bullfight, the 18-cent coin, and the bus-stop cognitive
subsidy.
```
