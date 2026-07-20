# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 2: Explore/Exploit — The Latest vs. the Greatest
**Author:** Brian Christian and Tom Griffiths
**Type:** Extraction
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 47–78 (book chapter 2, incl. footnote)
**Date:** 2026-07-19
**Revision note:** Revised after Chapter_02_Audit.md; see that file for what changed and why.

```
BOOK:
Algorithms to Live By: The Computer Science of Human Decisions

AUTHOR:
Brian Christian and Tom Griffiths

CHAPTER:
2 — Explore/Exploit: The Latest vs. the Greatest
```

---

## 1. Chapter Thesis

Every repeated choice between the new and the familiar is an instance of the explore/exploit tradeoff,
formalized in computer science as the multi-armed bandit problem. The chapter's central claim is that
the right balance is not a matter of temperament but of **interval**: how long you will be able to
enjoy what you learn. Optimal algorithms (the Gittins index, Upper Confidence Bound) show that
untried options deserve a systematic bonus — optimism about the unknown is mathematically justified,
not naive — and that regret can at best grow logarithmically. Applied to a life, this reframes
childhood as a rational exploration phase and old age as a rational exploitation phase, and it turns
A/B testing and adaptive clinical trials into the same problem with money and lives at stake.

## 2. Key Concepts

```
Concept Name: Explore/Exploit Tradeoff
Definition: The tension between gathering information (exploring) and using the information you
already have to get a known good result (exploiting). The authors stress that in computer science
these are neutral technical terms, stripped of their ordinary English connotations.
Why It Matters: Reframes "should I try something new?" from a personality question into a
computational one with an answer that depends on measurable circumstances.
How the Author Uses It: The chapter's organizing frame. They insist both failure modes are real:
never exploring is no way to live, but never exploiting is equally bad — many of life's best moments
(holidays with family, a band playing its greatest hits, a couple dancing to "their song") *are*
exploitation.
Related Concepts: Multi-armed bandit, interval, Gittins index, optimal stopping (chapter 1).
```

```
Concept Name: The Multi-Armed Bandit Problem
Definition: A casino full of slot machines with unknown payoff odds; you want to maximize total
winnings, which requires both testing machines and favoring the best ones found. Named after the
"one-armed bandit," slang for a slot machine.
Why It Matters: The formal home of the explore/exploit tension; Peter Whittle says it "embodies in
essential form a conflict evident in all human action."
How the Author Uses It: The chapter's central model, applied to restaurants, music, airlines, web
pages, drug trials, and the human lifespan.
Related Concepts: Expected value, Gittins index, UCB, restless bandit, A/B testing.
```

```
Concept Name: The Interval
Definition: The span of time over which you will be able to enjoy the results of what you learn.
Why It Matters: The chapter's single most load-bearing idea — "the interval makes the strategy."
The value of exploration can only go *down* over time as remaining opportunities dwindle; the value
of exploitation can only go *up*, since today's best-known café is by definition at least as good as
last month's.
How the Author Uses It: To explain Stucchio's restaurant behavior, Hollywood's sequel deluge,
Carstensen's findings on aging, and ultimately the whole arc of a human life. Also used in reverse:
by observing a strategy you can infer the actor's perceived interval.
Related Concepts: Discounting, socioemotional selectivity, optimal stopping horizon.
```

```
Concept Name: Win-Stay, Lose-Shift
Definition: Robbins's 1952 strategy for two machines — pick an arm at random and keep pulling it as
long as it pays off; switch on a failure.
Why It Matters: The first proven-better-than-chance strategy, and the origin of the durable "stay on
a winner" principle.
How the Author Uses It: As a historical first step that is instructive in both what it gets right
(win-stay is part of the optimal strategy under a wide range of conditions) and what it gets wrong
(lose-shift is rash, and the rule has no notion of interval).
Related Concepts: Gittins index, Zelen's play-the-winner algorithm.
```

```
Concept Name: The Gittins Index (Dynamic Allocation Index)
Definition: For each arm, the guaranteed payout rate that would make you content never to pull that
arm again — a single number capturing both its known value and its exploration value. Strategy:
always play the arm with the highest index.
Why It Matters: It completely solves the multi-armed bandit under geometric discounting, collapsing
the explore/exploit tension into maximizing one quantity. Crucially, each arm's index is computed
separately, so the number of arms doesn't matter.
How the Author Uses It: The chapter's mathematical centerpiece, and the source of its most striking
number: an untried 0–0 arm scores 0.7029, beating a machine known to pay out 70% of the time.
Related Concepts: Geometric discounting, Deal or No Deal bribe analogy, UCB, expected value.
```

```
Concept Name: Geometric Discounting
Definition: Valuing each future payoff at a constant fraction of the previous one — tomorrow's dinner
worth 90% (or 99%) of tonight's.
Why It Matters: The assumption that makes the Gittins index exactly optimal, and the assumption the
chapter itself flags as empirically shaky.
How the Author Uses It: Gittins's key modeling move — reframing the goal as maximizing payoffs over
an endless but discounted future rather than a fixed interval. The authors give the memorable
justification: if there's a 1% chance you'll be hit by a bus today, value tomorrow's dinner at 99%
of tonight's.
Related Concepts: Discount function, the interval, behavioral economics on hyperbolic discounting.
```

```
Concept Name: Regret (and Its Minimization)
Definition: The difference between the total payoff a strategy actually obtained and the payoff that
could have been obtained by pulling the best arm every time, had you known which it was.
Why It Matters: Converts an emotion into a measurable quantity that algorithms can be graded against;
Lai and Robbins proved the minimum achievable regret grows only logarithmically.
How the Author Uses It: To offer consolation with mathematical backing — you will accumulate regret
forever, but under a good strategy you should have fewer new regrets each year than the year before.
Related Concepts: Regret minimization framework (Bezos), UCB, Barnard's "inestimable loss."
```

```
Concept Name: Upper Confidence Bound (UCB) Algorithms
Definition: Pick the option whose confidence interval has the highest *top* — that is, the option
that could plausibly be best given current evidence, not the one that has performed best so far.
Why It Matters: Achieves near-minimal regret, is far easier to compute than the Gittins index, and
requires no geometric-discounting assumption.
How the Author Uses It: As the practical successor to Gittins, and as the formal grounding for
"optimism in the face of uncertainty" and for giving people and things the benefit of the doubt.
Related Concepts: Confidence interval, error bars, optimistic robots, Gittins index.
```

```
Concept Name: Optimism in the Face of Uncertainty
Definition: The principle underlying UCB — systematically evaluate unknowns at the best they could
reasonably be, which naturally injects exploration into decision-making.
Why It Matters: Shows optimism can be "perfectly rational" rather than a bias, and yields the
chapter's practical advice: assume the best about new people and things absent evidence otherwise.
How the Author Uses It: To connect the math to lived ethics — "in the long run, optimism is the best
prevention for regret." Cites Leslie Kaelbling's "optimistic robots," which explore by boosting the
value of uncharted terrain.
Related Concepts: UCB, benefit of the doubt, exploration bonus.
```

```
Concept Name: The Restless Bandit
Definition: A bandit problem in which the arms' payoff probabilities change over time.
Why It Matters: The realistic case, and it is intractable — the chapter states there is no tractable
algorithm for solving it completely and that it is believed there never will be.
How the Author Uses It: To limit the chapter's own toolkit and to license permanent exploration:
"to live in a restless world requires a certain restlessness in oneself." That disappointing
restaurant may be under new management.
Related Concepts: Non-stationarity, Thoreau's "Walking," Warhol's "A Coke is a Coke."
```

```
Concept Name: Adaptive (Bandit-Based) Clinical Trials
Definition: Trial designs that shift patient allocation toward the better-performing treatment while
the trial is still running, rather than holding fixed groups until the end.
Why It Matters: The chapter's highest-stakes application — conventional trials optimize for
decisively answering a question rather than for treating the patients in the trial.
How the Author Uses It: Through Zelen's play-the-winner algorithm and the ECMO controversy, to argue
that the standard design's ethics are not self-evident.
Related Concepts: A/B testing, Belmont Report, Win-Stay Lose-Shift, Don Berry.
```

```
Concept Name: A/B Testing
Definition: Randomly assigning users to different versions of a page and locking in the winner on a
chosen metric.
Why It Matters: Makes the internet, in the authors' phrase, "the world's largest controlled
experiment," and it is structurally identical to a clinical trial.
How the Author Uses It: Via the Obama campaign case, to show explore/exploit algorithms already run
much of the commercial internet — and to land the line that in this bandit problem "you're not the
gambler; you're the jackpot."
Related Concepts: Multi-armed bandit, clinical trials, exploration cost borne by users.
```

## 3. Key Claims

```
Claim: Decisions are almost never isolated, and expected value isn't the end of the story.
Type: Theoretical
Evidence Provided: The 1–1 versus 9–6 comparison, where ranking by expected value (50% vs. 60%) gives
the wrong answer once you account for all the future decisions you will make about the same options.
Strength of Support: Strong (definitional to the model class rather than empirical). This is the
premise the entire chapter rests on: people "tend to treat decisions in isolation," and that habit is
what the bandit framework corrects.
```

```
Claim: Pure exploitation is self-undermining, because every "best" you have began as something merely
"new" to you.
Type: Interpretive
Evidence Provided: Argued directly against Robert Pirsig's preference for "What's best?" over "What's
new?" in *Zen and the Art of Motorcycle Maintenance* (1974). No empirical evidence; the argument is
structural — there may be yet-unknown bests still out there, so the new deserves at least some
attention.
Strength of Support: Strong as an argument, and notable as the chapter's only explicit disagreement
with a named author.
```

```
Claim: The right explore/exploit balance depends on the interval over which you can enjoy what you
learn — "the interval makes the strategy."
Type: Theoretical
Evidence Provided: The structural argument that exploration's value can only decline and
exploitation's can only rise; illustrated by Stucchio's move-in/move-out restaurant behavior and by
Carstensen's experimental interval manipulations.
Strength of Support: Strong. Carstensen's twist conditions (imagining a cross-country move; imagining
20 extra years) give it genuine experimental support, not just illustration.
```

```
Claim: Strategy reveals interval — Hollywood's sequel deluge signals that the industry believes it is
near the end of its interval.
Type: Interpretive
Evidence Provided: Sequels among the top ten highest-grossing films: 2 in 1981, 3 in 1991, 5 in 2001,
8 in 2011, with records broken in 2011, 2012 and 2013; profits of the largest studios down 40%
between 2007 and 2011; ticket sales down in seven of the past ten years; an Economist quotation on
studios squeezed between rising costs and falling revenues.
Strength of Support: Moderate. The correlation is well documented and the reading is plausible, but
the industry's own strategic reasoning is inferred from behavior — the authors call it a "hunch" that
the economics "confirms."
```

```
Claim: Win-Stay, Lose-Shift performs reliably better than chance.
Type: Theoretical (proved)
Evidence Provided: Robbins's 1952 proof, described but not reproduced.
Strength of Support: Strong.
```

```
Claim: Win-stay is part of the optimal strategy under a wide range of conditions; lose-shift is not.
Type: Theoretical
Evidence Provided: A series of papers following Robbins; visible directly in the Gittins table, where
index scores always increase left-to-right along a row, and where a 9-wins-then-1-loss record still
scores 0.8695.
Strength of Support: Strong. The table makes the asymmetry concrete rather than asserted.
```

```
Claim: Under geometric discounting, the Gittins index completely solves the multi-armed bandit problem.
(Order matters: the condition is what makes the result true, and the chapter states it as a
restriction, not an aside.)
Type: Theoretical (theorem)
Evidence Provided: Stated as a theorem; Gittins's own modest framing ("It's not quite Fermat's Last
Theorem"). The derivation is not given; the Deal or No Deal bribe analogy stands in for it.
Strength of Support: Strong as a result, though the chapter presents no proof.
```

```
Claim: A completely untried option (0–0 record) is more attractive than a machine known to pay out
70% of the time.
Type: Theoretical
Evidence Provided: The Gittins table at a 0.9 discount rate: 0–0 scores 0.7029 against an expected
value of 0.5000. At a 0.99 discount rate the same 0–0 arm is worth a guaranteed 86.99% payout.
Strength of Support: Strong within the model's assumptions, and the chapter's most striking result.
Note that it is entirely a consequence of geometric discounting plus a long horizon.
```

```
Claim: The exploration bonus decays slowly — even a first-pull failure (0–1) leaves an index above
50%, and repeated 50% performance converges on 0.5000 only gradually (1–1 → 0.6346; 2–2 → 0.6010).
Type: Theoretical
Evidence Provided: The index table.
Strength of Support: Strong.
```

```
Claim: The math justifies the old adage that the grass is greener on the other side — the unknown has
a chance of being better even when you expect it to be no different or just as likely worse.
Type: Interpretive (of a formal result)
Evidence Provided: The Gittins index structure; the authors' example that an untested rookie is worth
more early in the season than a veteran of seemingly equal ability, precisely because less is known.
Strength of Support: Moderate to Strong. The formal point is solid; the "grass is greener" gloss is
rhetorical, and the chapter itself immediately warns that a greener-looking lawn doesn't warrant
climbing the fence, let alone a second mortgage.
```

```
Claim: The Gittins index is optimal only under strong assumptions and is impractical to apply by hand.
Type: Theoretical (the authors' own caveat)
Evidence Provided: Three named limits — (1) geometric discounting, which "a variety of experiments in
behavioral economics and psychology suggest people don't do"; (2) it is no longer optimal if there is
a cost to switching between options; (3) it is hard to compute on the fly, illustrated with a joke
about doing the arithmetic while everyone leaves the restaurant.
Strength of Support: Strong. This is the chapter policing its own headline result.
```

```
Claim: The minimum achievable regret grows logarithmically with each pull; total regret never stops
increasing, but a good strategy makes its growth rate decline over time.
Type: Theoretical (proved)
Evidence Provided: Lai and Robbins, 1985 — three results stated: regret probably never stops
increasing absent omniscience; it grows more slowly under the best strategy; the minimum possible
growth is logarithmic.
Strength of Support: Strong.
```

```
Claim: Logarithmic regret means you make as many mistakes in your first ten pulls as in the next
ninety, and as many in your first year as in the rest of the decade.
Type: Theoretical (illustration of the above)
Evidence Provided: Direct property of a logarithm.
Strength of Support: Strong as arithmetic; note it holds under a regret-minimizing algorithm, not
automatically for a human life.
```

```
Claim: UCB algorithms give recommendations similar to the Gittins index, are significantly easier to
compute, and require no geometric-discounting assumption.
Type: Theoretical
Evidence Provided: Stated; the mechanism (pick the highest upper confidence bound) is explained, and
the parallel to Gittins is noted — both assign one number per arm, both exceed expected value, both
converge toward expected value as evidence accumulates.
Strength of Support: Strong for the mechanism; the "similar recommendations" claim is asserted rather
than demonstrated.
```

```
Claim: Optimism can be perfectly rational, and "in the long run, optimism is the best prevention for
regret."
Type: Interpretive / Prescriptive
Evidence Provided: The regret guarantees of UCB algorithms; Kaelbling's optimistic robots as an
existence proof in engineering.
Strength of Support: Moderate. The formal claim (optimistic value estimates minimize regret in
bandits) is solid; the extension to how one should treat new people is the authors' inference, and
"assume the best about them" is prescriptive advice the math does not directly license outside the
model.
```

```
Claim: A/B testing produced $57 million in additional donations for the 2008 Obama campaign.
Type: Empirical
Evidence Provided: Attributed to Dan Siroker's work as head of New Media Analytics; specific winning
variants reported (DONATE AND GET A GIFT for first-time visitors, even net of gift costs; PLEASE
DONATE for longtime non-donating subscribers; CONTRIBUTE for prior donors; a black-and-white family
photo beating every other image or video).
Strength of Support: Moderate. A single reported figure with no methodology given for how the
counterfactual was computed; the mechanism-level findings are more informative than the headline
number.
```

```
Claim: The canonical A/B setup — even split, fixed duration, then all traffic to the winner — may not
be the best algorithm, because half the users get the inferior option for the whole test.
Type: Theoretical / Prescriptive
Evidence Provided: Structural argument; the stakes are quantified (over 90% of Google's ~$50 billion
annual revenue from paid advertising; online commerce in the hundreds of billions).
Strength of Support: Moderate. The authors explicitly note the best algorithms "remain hotly
contested" among statisticians, engineers and bloggers — they do not claim the question is settled.
```

```
Claim: Conventional clinical trials optimize for resolving the question rather than for treating the
patients in the trial, and should arguably be run as bandit problems.
Type: Prescriptive
Evidence Provided: The structural parallel to A/B testing; the Belmont Report's own acknowledgment
that avoiding harm requires learning what is harmful; the ECMO studies; Don Berry's position; the
FDA's February 2010 "Adaptive Design Clinical Trials for Drugs and Biologics" guidance.
Strength of Support: Moderate. The chapter is careful to present this as the position of "a growing
community of doctors and statisticians" and reports the counterarguments (Ware's objection that the
Michigan data did not justify routine use; the UK study's rationale that the evidence was subject to
varying interpretation). It also notes that conventional trials are not wholly inflexible — "only in
exceptional cases does a trial get stopped early," so stopping rules exist and the argument is that
they are insufficient.
```

```
Claim: There is a real cost to changing accepted statistical practice, beyond any individual trial.
Type: Interpretive (the chapter's own steelman of the conservative position)
Evidence Provided: The observation that part of what statistics did for medicine at the start of the
twentieth century was to transform it "from a field in which doctors had to persuade each other in ad
hoc ways about every new treatment into one where they had clear guidelines about what sorts of
evidence were and were not persuasive." Changes to that standard "have the potential to upset this
balance, at least temporarily."
Strength of Support: Moderate as argument, and important for balance: this is the chapter explaining
why the resistance to adaptive designs is rational rather than merely obstinate. Any use of the ECMO
material that omits this misrepresents the chapter.
```

```
Claim: People tend to over-explore — favoring the new disproportionately over the best.
Type: Empirical
Evidence Provided: Three studies. (1) Tversky & Edwards, 1966: with a 60/40 light, participants
observed 505 times on average and bet 495, when the math says bet after 38 observations. (2) Meyer &
Shi, 1990s: participants used the untried airline too little when it was good and too much when it
was bad, and failed to make clean breaks. (3) Steyvers, Lee & Wagenmakers, four-armed bandit over
fifteen pulls: 30% closest to optimal, 47% resembling Win-Stay Lose-Shift, 22% moving at random
between a new arm and the best-so-far.
Strength of Support: Moderate. Three independent studies point the same way, but each is thin: the
1966 design forbids learning from your own bets (unlike a real bandit); the Meyer & Shi result is
two-sided (under-use when the new option was good, over-use when it was bad) and the chapter's actual
grounds for counting it are the *failure to break cleanly* and the continued alternation, not the
misuse itself; and the Steyvers classification is inferred from behavior over only fifteen pulls with
no stated sample size.
```

```
Claim: People over-explore in bandits while stopping too early in secretary problems.
Type: Interpretive
Evidence Provided: The juxtaposition of chapter 1's premature stopping with this chapter's
over-exploration: "while we tend to commit to a new secretary too soon, it seems like we tend to stop
trying new airlines too late."
Strength of Support: Moderate. Both findings are supported individually; the chapter notes but does
not resolve the apparent inconsistency, and immediately offers a partial reconciliation — the world
might change, so late exploration has a value the static model ignores.
```

```
Claim: The restless bandit has no tractable complete solution, and it is believed there never will be.
Type: Theoretical
Evidence Provided: Stated without citation or proof sketch.
Strength of Support: Moderate as presented — an important negative result asserted rather than
supported.
```

```
Claim: Childhood's extended dependence exists to solve the explore/exploit tradeoff developmentally.
Type: Theoretical (attributed to Gopnik)
Evidence Provided: Gopnik's argument, quoted directly: good bandit algorithms explore early, but the
disadvantage is poor payoffs during exploration — so childhood provides a period where payoffs are
"taken care of by the mamas and the papas and the grandmas and the babysitters." Contrasted with
caribou and gazelles, which must run from predators on day one.
Strength of Support: Moderate. A compelling functional explanation, but it is a hypothesis about why
human development has this shape; no test distinguishing it from rival accounts is presented.
```

```
Claim: Children are not cognitively deficient; they are optimized for exploration.
Type: Interpretive (attributed to Gopnik)
Evidence Provided: Gopnik's observation that children look terrible on exploit capacities (tying
shoes, long-term planning, focused attention) but excel at exactly what exploration requires —
pressing buttons at random, interest in new toys, jumping between activities. The authors add that a
baby putting every object in the house in its mouth is "studiously pulling all the handles at the
casino."
Strength of Support: Moderate. A genuine reframing, but it rests on a functional interpretation of
behaviors rather than on evidence that children are executing a good algorithm.
```

```
Claim: Our intuitions about rationality are informed too much by exploitation; emphasizing the new,
the exciting and the random is actually rational for many choices, particularly earlier in life.
Type: Interpretive / Prescriptive
Evidence Provided: The interval argument plus the childhood reframing.
Strength of Support: Moderate. Follows from the model given a long interval; the chapter's own
over-exploration findings sit in tension with the prescription.
```

```
Claim: Shrinking social networks in old age reflect deliberate selection, not decline.
Type: Empirical (attributed to Carstensen)
Evidence Provided: Carstensen's characterization of the decrease as "the result of lifelong selection
processes by which people strategically and adaptively cultivate their social networks"; the finding
that shrinkage comes primarily from pruning peripheral relationships while focusing on a core of
close friends and family.
Strength of Support: Strong within the chapter's presentation — this is the chapter's best-evidenced
empirical claim, and the interval manipulations (below) are what make it more than an interpretation.
```

```
Claim: Social preferences track perceived interval, not age as such.
Type: Empirical
Evidence Provided: Carstensen & Fredrickson's choice task (thirty minutes with an immediate family
member, the author of a recently read book, or a promising new acquaintance): older people chose
family, young people were equally excited by the author or the new friend. But young people asked to
imagine moving across the country also chose family; and older people asked to imagine a medical
breakthrough granting twenty extra years became indistinguishable from the young.
Strength of Support: Strong. The bidirectional manipulation is what makes this genuinely causal about
interval rather than correlational about age.
```

```
Claim: Life should get better over time, because exploration necessarily means being let down on most
occasions and old age shifts attention to favorites.
Type: Interpretive, with empirical support
Evidence Provided: The structural argument (Gittins and UCB inflate the appeal of lesser-known
options beyond expectation, so exploration usually disappoints), plus Carstensen's finding that older
people are generally more satisfied with their social networks and often report higher emotional
well-being than younger adults.
Strength of Support: Moderate to Strong. The well-being finding supports the conclusion; the causal
chain running through "exploration necessarily disappoints" is the authors' synthesis.
```

## 4. Frameworks, Models, and Mental Models

```
Name: The Multi-Armed Bandit
Description: Repeated choice among options with unknown payoff rates, maximizing cumulative reward.
Components: Arms (options); unknown payoff probabilities; a sequence of pulls; a horizon or discount
function.
How It Works: Every pull is simultaneously a test and a bet. Optimal play requires valuing each arm's
information content alongside its expected payoff.
When It Is Useful: Any repeated decision where the outcome teaches you something you will use again —
restaurants, hiring, dating, product features, treatments, content recommendations.
Limitations: The classical version assumes fixed payoff probabilities, no switching costs, and
immediate observable feedback. Whittle: it "quickly became a classic, and a byword for intransigence."
```

```
Name: Win-Stay, Lose-Shift
Description: Keep pulling an arm while it pays; switch on any failure.
Components: Two arms; a binary outcome per pull.
How It Works: Random initial choice, then a purely reactive switching rule.
When It Is Useful: When you need something simple and provably better than chance; the win-stay half
generalizes far beyond the original setting.
Limitations: Lose-shift is rash — one bad meal shouldn't undo a hundred good ones, and "good options
shouldn't be penalized too strongly for being imperfect." The rule has no notion of interval, so it
tells you to switch even on your last night in town.
```

```
Name: Bellman's Backward Induction Solution
Description: Exact solution for the case where the total number of options and opportunities is known
in advance.
Components: A known finite horizon; enumeration of possible futures.
How It Works: Start from the final pull, determine the best choice given every possible history, then
work backward to the beginning — the same trick as the full-information secretary problem in
chapter 1.
When It Is Useful: Small, fully specified problems.
Limitations: "Ironclad" but computationally explosive — with many options and a long visit it requires
a dizzying or impossible amount of work, and you rarely know the horizon anyway. This is why the
problem stayed effectively unsolved.
```

```
Name: The Gittins Index
Description: Reduce each arm to a single number — the guaranteed payout that would make you content
never to pull it again — and always play the highest.
Components: Each arm's win/loss record; a geometric discount rate; the resulting index table.
How It Works: Gittins imagined a bribe, exactly like the Banker on Deal or No Deal offering money not
to open the briefcase. The price at which you'd accept the sure thing *is* the arm's value. Because
each index is computed separately, the number of arms is irrelevant.
When It Is Useful: Repeated choices with geometric discounting and no switching cost; the table can
be precomputed once for a given discount rate and reused for any problem of that form.
Limitations: The authors name three: geometric discounting is empirically doubtful; switching costs
break optimality; and on-the-fly computation is impractical for humans.
Why discounting rather than a horizon: the chapter motivates the move by noting that for drug
companies and doctors "it's not entirely clear what the relevant interval ought to be" — companies
intend to exist indefinitely and a breakthrough could help people not yet born, yet a patient cured
today counts for more than one cured next year. Discounting handles an endless-but-weighted future
that no fixed interval could represent.
Key values (0.9 discount): 0–0 → 0.7029; 0–1 → still above 0.5; 1–1 → 0.6346; 2–2 → 0.6010; 9–6 →
0.6300; nine wins then a loss → 0.8695. At a 0.99 discount, 0–0 → 0.8699.
```

```
Name: Upper Confidence Bound (UCB)
Description: Choose the arm whose confidence interval reaches highest, i.e. the arm that *could*
reasonably be best.
Components: An estimate plus an uncertainty range (error bars) per arm; the interval shrinks with
data.
How It Works: Ranks by optimistic potential rather than observed mean. A restaurant with one mediocre
review retains a potential for greatness that a restaurant with hundreds of mediocre reviews does not.
When It Is Useful: Practically everywhere Gittins is too hard — no discounting assumption needed,
much cheaper to compute, near-minimal regret.
Limitations: The chapter gives none explicitly; it presents UCB as the pragmatic winner. (Inference:
the "similar to Gittins" claim is asserted, and UCB still assumes stationary payoffs.)
```

```
Name: Regret Minimization Framework (Bezos)
Description: Project yourself to age 80 and choose the option that minimizes the regrets you will
have looking back.
Components: A long imagined horizon; an inventory of anticipated regrets; asymmetry between regretting
failure and regretting not trying.
How It Works: Bezos knew he would not regret trying and failing at an internet bookstore, but would
regret never having tried — "that would haunt me every day" — which made leaving a secure position at
D. E. Shaw "an incredibly easy decision."
When It Is Useful: One-off high-stakes choices where the interval is long and the downside of failure
is recoverable.
Limitations: Not itself a bandit algorithm — it is a heuristic that happens to bias toward
exploration. The chapter offers it as what computer science can formalize, not as a proven method,
and note it is a single survivorship-heavy anecdote.
```

```
Name: Zelen's Randomized Play-the-Winner (Adaptive Trial)
Description: A bandit-flavored clinical trial design proposed in 1969.
Components: A hat containing one ball per treatment; balls drawn with replacement to assign each
patient.
How It Works: Draw a ball to select the treatment. On a success, add another ball for that treatment;
on a failure, add a ball for the *other* treatment. Allocation drifts toward whichever treatment is
winning.
When It Is Useful: Trials where withholding a potentially lifesaving treatment is ethically fraught.
Limitations: Deviates sharply from standard methodology, which produced exactly the controversy the
ECMO case documents — too few patients on the conventional arm to satisfy critics.
```

```
Name: A/B Testing as a Bandit
Description: Randomized assignment of users to page variants, monitored on a chosen metric.
Components: Variants; a traffic split; a metric; a stopping point; a winner locked in or promoted to
control for the next round.
How It Works: Canonically an even split for a fixed period, then all traffic to the winner.
When It Is Useful: High-volume, low-stakes-per-user decisions with fast feedback.
Limitations: The even split means half of users receive the inferior option for the entire test — the
same structural objection the chapter raises against conventional clinical trials. Better algorithms
are "hotly contested."
```

## 5. Research and Evidence

```
Study / Research: Win-Stay, Lose-Shift
Researchers: Herbert Robbins (Columbia)
Year: 1952
Research Question: Is there a simple strategy for the two-armed bandit that beats chance?
Method: Mathematical proof.
Key Finding: Win-Stay, Lose-Shift performs reliably better than chance.
How the Author Uses It: The first step out of intractability, and the origin of the "stay on a winner"
principle that survives into optimal strategies.
Important Limitations: Restricted to two machines; no notion of interval; lose-shift is too reactive.
Replication or Controversy Mentioned: A series of subsequent papers examined "stay on a winner"
further; the authors report win-stay is vindicated and lose-shift is not.
```

```
Study / Research: Exact solution for known finite horizons
Researchers: Richard Bellman (RAND Corporation)
Year: Not specified (post-WWII era).
Research Question: How to play optimally when the number of options and opportunities is known in
advance?
Method: Backward induction from the final pull.
Key Finding: An exact solution exists for this restricted case.
How the Author Uses It: To show the problem was solvable only under unrealistic knowledge, leaving
the general case open.
Important Limitations: Computationally infeasible for many options or long horizons; requires knowing
the horizon.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: The Gittins index (dynamic allocation index)
Researchers: John Gittins, now professor of statistics at Oxford; commissioned by Unilever
Year: 1970s
Research Question: Given several chemical compounds, what is the quickest way to determine which is
likely to be effective against a disease? Gittins generalized this to: multiple options, different
reward probabilities, a fixed amount of effort/money/time to allocate.
Method: Reframed the goal as maximizing payoffs over an endless but geometrically discounted future;
evaluated each arm independently via the bribe/indifference-price construction.
Key Finding: The index strategy completely solves the multi-armed bandit under geometric discounting.
How the Author Uses It: The chapter's mathematical centerpiece; also as a story about how an applied
industrial question cracked a problem "that had gone unsolved for a generation."
Important Limitations: Optimal only under geometric discounting; breaks under switching costs; hard
to compute on the fly.
Replication or Controversy Mentioned: The authors note behavioral economics and psychology experiments
suggest people do not discount geometrically. Gittins's own assessment: "It's not quite Fermat's Last
Theorem."
```

```
Study / Research: Regret bounds for the multi-armed bandit
Researchers: Tze Leung Lai and Herbert Robbins (both Columbia)
Year: 1985
Research Question: How little regret can any strategy guarantee?
Method: Mathematical proof.
Key Finding: Absent omniscience, total regret probably never stops increasing; regret grows more
slowly under the best strategy and its growth rate declines with experience; the minimum possible
regret grows logarithmically per pull.
How the Author Uses It: To turn an emotion into a measurable quantity and to offer consolation —
fewer new regrets each year than the year before.
Important Limitations: A guarantee about algorithms, not about human lives; the chapter's
year-by-year gloss is an extrapolation.
Replication or Controversy Mentioned: None identified. Noted as the start of the modern search for
minimal-regret algorithms, of which UCB is the most popular family.
```

```
Study / Research: Optimistic robots
Researchers: Leslie Kaelbling (MIT)
Year: Not specified.
Research Question: Not specified.
Method: Robots that explore by boosting the assessed value of uncharted terrain.
Key Finding: Not specified beyond the design principle working as an exploration mechanism.
How the Author Uses It: As an engineering existence proof for "optimism in the face of uncertainty."
Important Limitations: No results, metrics, or comparison are reported in the chapter.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Obama campaign A/B testing
Researchers: Dan Siroker (Google product manager on leave, heading "New Media Analytics")
Year: 2007–2008 campaign
Research Question: Which donation-page variants maximize donations?
Method: Live A/B tests on the campaign site's DONATE button, images, and copy, segmented by visitor
type.
Key Finding: $57 million in additional donations attributed to the work. DONATE AND GET A GIFT won for
first-time visitors even net of gift costs; PLEASE DONATE won for longtime subscribers who had never
given; CONTRIBUTE won for prior donors; a plain black-and-white photo of the Obama family beat every
other photo or video the team produced.
How the Author Uses It: To show explore/exploit algorithms operating at scale with real money, and to
introduce A/B testing as a bandit problem.
Important Limitations: No methodology given for the $57 million counterfactual; single campaign; the
segment-level explanations offered (guilt, "donated" vs "contribute") are speculative glosses the
authors mark with "perhaps."
Replication or Controversy Mentioned: None. Siroker later co-founded Optimizely with Pete Koomen; by
2012 its clients included both the Obama re-election campaign and Mitt Romney's campaign.
```

```
Study / Research: The Tuskegee Syphilis Study
Researchers: US Public Health Service
Year: 1932–1972; whistleblower protests 1966 and 1968; press disclosure July 25, 1972 (Washington
Star), New York Times front page the next day
Research Question: N/A — an unethical natural-course study.
Method: Several hundred African-American men with syphilis in Macon County, Alabama, were
deliberately left untreated for forty years.
Key Finding: N/A. The study was halted only after Peter Buxtun went to the press; his two internal
protests had failed.
How the Author Uses It: As the historical trigger for the Belmont Report, and to establish that the
ethics of experimentation on humans is not an abstract question.
Important Limitations: N/A — presented as history, not evidence for a claim.
Replication or Controversy Mentioned: N/A.
```

```
Study / Research: The Belmont Report
Researchers: A commission at the Belmont Conference Center, Maryland
Year: 1979
Research Question: What are the ethical principles governing medical experimentation?
Method: Commission report.
Key Finding: Quoted acknowledging that "even avoiding harm requires learning what is harmful; and, in
the process of obtaining this information, persons may be exposed to risk of harm." Also quoted on
research on childhood diseases presenting more than minimal risk without direct benefit to the
children involved — some argue such research is inadmissible, others that this limit would rule out
much research promising great future benefit.
How the Author Uses It: To show that the explore/exploit tension is written into the foundational
document of research ethics, and that the document acknowledges but does not resolve it.
Important Limitations: A normative document, not evidence.
Replication or Controversy Mentioned: The report itself notes beneficence is "not always so
unambiguous."
```

```
Study / Research: Zelen's adaptive "play the winner" design
Researchers: Marvin Zelen, biostatistician, now at Harvard
Year: 1969 (proposed); first used in a clinical trial sixteen years later
Research Question: Can trial allocation adapt to accumulating evidence?
Method: Randomized urn scheme — one ball per treatment, drawn with replacement; a success adds a ball
for that treatment, a failure adds a ball for the other.
Key Finding: A workable adaptive design, a version of Win-Stay Lose-Shift.
How the Author Uses It: The bridge from bandit algorithms to clinical practice.
Important Limitations: Sixteen-year gap between proposal and first use; the design's deviation from
standard methodology is what later drew criticism.
Replication or Controversy Mentioned: See the ECMO entries below.
```

```
Study / Research: University of Michigan ECMO trial
Researchers: Robert Bartlett and colleagues, University of Michigan. ECMO (extracorporeal membrane
oxygenation) developed by Bartlett in the 1970s.
Year: Study 1982–1984; follow-on observations April–November 1984
Research Question: Does ECMO improve survival in newborns with respiratory failure?
Method: Zelen's randomized play-the-winner algorithm. The team stated they wanted to address "the
ethical issue of withholding an unproven but potentially lifesaving treatment" and were "reluctant to
withhold a lifesaving treatment from alternate patients simply to meet conventional random assignment
technique."
Key Finding: One infant assigned conventional treatment died; eleven consecutive infants assigned
ECMO all survived. In the post-study period, eight of eight ECMO-treated infants survived and both
conventionally treated infants died.
How the Author Uses It: The chapter's central case that adaptive designs can save lives inside the
trial itself.
Important Limitations: Very few patients on the conventional arm, a significant deviation from
standard methodology; ECMO is highly invasive with its own risks including embolism; earlier adult
studies had shown no benefit over conventional treatment. Tiny sample.
Replication or Controversy Mentioned: Extensive. Jim Ware (Harvard School of Public Health) and
colleagues concluded the data "did not justify routine use of ECMO without further study."
```

```
Study / Research: Ware's ECMO trial
Researchers: Jim Ware, professor of biostatistics, Harvard School of Public Health, and medical
colleagues
Year: Not specified (after the Michigan study).
Research Question: Does ECMO improve survival, under a less radical adaptive design?
Method: Randomize to ECMO or conventional treatment until a prespecified number of deaths occurred in
one group, then switch all patients to the more effective treatment.
Key Finding: Phase one — four of ten conventional-treatment infants died; all nine of nine ECMO
infants survived. The four deaths triggered phase two, in which all twenty patients received ECMO and
nineteen survived. Ware and colleagues concluded "it is difficult to defend further randomization
ethically."
How the Author Uses It: As the middle position between conventional and fully adaptive design — and
as a case that even a compromise design drew ethical objection.
Important Limitations: Small samples; the design still assigned infants to a treatment its designers
suspected was worse until a death threshold was reached.
Replication or Controversy Mentioned: Don Berry, a leading multi-armed bandit expert, wrote in a
comment published alongside the study in Statistical Science that "randomizing patients to non-ECMO
therapy as in the Ware study was unethical.… In my view, the Ware study should not have been
conducted."
```

```
Study / Research: UK ECMO trial
Researchers: Not specified.
Year: 1990s
Research Question: Does ECMO reduce risk of death in infants?
Method: Traditional design — nearly two hundred UK infants split randomly into two equal groups,
explicitly not using adaptive algorithms. Justified on the grounds that ECMO's usefulness "is
controversial because of varying interpretation of the available evidence."
Key Finding: The treatment difference was less pronounced than in the two American studies, but
results were declared "in accord with the earlier preliminary findings that a policy of ECMO support
reduces the risk of death." Twenty-four more infants died in the conventional group than in the ECMO
group.
How the Author Uses It: To quantify the human cost of insisting on a conventional design — "the cost
of that knowledge."
Important Limitations: The authors present the 24 excess deaths as the price of the design; note that
the smaller UK effect size is itself a reason the earlier American results were doubted, which
complicates the framing.
Replication or Controversy Mentioned: This study *is* the replication, and it partially disagreed with
the American effect size.
```

```
Study / Research: FDA guidance on adaptive trials
Researchers: US Food and Drug Administration
Year: February 2010
Research Question: N/A — a regulatory guidance document, "Adaptive Design Clinical Trials for Drugs
and Biologics."
Method: N/A.
Key Finding: The authors read it as a signal that the FDA "might at last be willing to explore
alternatives," despite a long history of sticking to a trusted option.
How the Author Uses It: Evidence that adaptive designs are entering the mainstream.
Important Limitations: Guidance documents are not mandates; the chapter reports no uptake data.
Replication or Controversy Mentioned: Don Berry moved from the University of Minnesota statistics
department to MD Anderson Cancer Center in Houston, where he designs bandit-based cancer trials; he
remains a vocal critic of randomized clinical trials, and the authors note he is not the only one.
```

```
Study / Research: Observation vs. betting with two lights
Researchers: Amos Tversky and Ward Edwards
Year: 1966
Research Question: Do people balance information-gathering against information-use optimally?
Method: Participants saw a box with two lights, each turning on a fixed but unknown percentage of the
time, and had 1,000 opportunities either to observe which light came on or to bet on the outcome
without observing. Unusually for a bandit, a pull could not be both wager and observation; bets were
not resolved until the end.
Key Finding: People adopted a sensible observe-then-bet structure but observed far too long — 505
observations and 495 bets on average with a 60/40 split, where the math prescribes betting after 38
observations.
How the Author Uses It: The chapter's cleanest demonstration of over-exploration.
Important Limitations: The forced separation of observation and wager makes this "pure" exploration
vs. exploitation but also unlike a real bandit, where every action informs. Sample size and
participant details are not specified.
Replication or Controversy Mentioned: Described as one of several studies producing similar
conclusions.
```

```
Study / Research: Known vs. unknown airline choice
Researchers: Robert Meyer and Yong Shi (Wharton)
Year: 1990s
Research Question: How do people choose between a known-payoff option and an unknown one?
Method: Repeated choice between an established carrier with a known on-time rate and a new company
with no track record, maximizing on-time arrivals over a period.
Key Finding: Participants used the untried airline too little when it was good and too much when it
was bad, and failed to make clean breaks, often continuing to alternate — particularly when neither
airline was departing on time.
How the Author Uses It: As further evidence of over-exploration, and to state the optimal policy: fly
only the new airline initially as long as the established one isn't clearly better, then switch hard
and never look back once the new option's Gittins index falls below the familiar carrier's on-time
rate.
Important Limitations: The finding is two-sided (under-use when good, over-use when bad), so it
supports "poor calibration" more cleanly than "over-exploration" alone. Participant details not
specified.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Four-armed bandit strategy classification
Researchers: Mark Steyvers, Michael Lee, and E.-J. Wagenmakers
Year: Not specified.
Research Question: Which strategies do people actually use in a bandit task?
Method: Participants chose among four arms over a sequence of fifteen opportunities; observed
behavior was then classified into strategy types.
Key Finding: 30% closest to the optimal strategy; 47% most resembling Win-Stay, Lose-Shift; 22%
moving at random between a new arm and the best found so far.
How the Author Uses It: Consistent with over-exploration, since both Win-Stay Lose-Shift and random
arm-trying lead people to try non-best options late in the game when they should be purely exploiting.
Important Limitations: Strategy assignment is inferred from behavior, not observed directly; fifteen
pulls is a very short horizon; sample size not specified.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Socioemotional selectivity and social network pruning
Researchers: Laura Carstensen (Stanford), with Barbara Fredrickson and colleagues
Year: Not specified.
Research Question: Why do social networks shrink with age?
Method: Program of research; the chapter details one choice experiment with two interval
manipulations — participants chose whom to spend thirty minutes with (an immediate family member, the
author of a book they'd recently read, or a promising new acquaintance); young participants were then
asked to imagine moving across the country, and older participants to imagine a medical breakthrough
granting twenty extra years.
Key Finding: Network shrinkage comes primarily from deliberately pruning peripheral relationships to
focus on a core of close friends and family. Older people chose family; young people were equally
drawn to the author or new acquaintance — but young people imagining a move chose family too, and
older people imagining twenty extra years became indistinguishable from the young. Separately, older
people are generally more satisfied with their social networks and often report higher emotional
well-being than younger adults.
How the Author Uses It: The chapter's empirical anchor for "the interval makes the strategy," and the
basis for its closing claim that life should get better over time.
Important Limitations: Sample sizes, populations, and dates are not specified in the chapter. The
imagination manipulations establish that perceived interval shifts preferences, but they are
hypothetical scenarios rather than real changes in circumstance.
Replication or Controversy Mentioned: Presented as overturning the traditional decline-based
explanation of shrinking networks; that traditional view is named but not defended.
```

```
Study / Research: Alison Gopnik on childhood as an exploration period
Researchers: Alison Gopnik, professor of developmental psychology, UC Berkeley, author of *The
Scientist in the Crib*
Year: Not specified.
Research Question: Why do humans have such an extended period of dependence?
Method: Not specified — presented as argument and interview quotation.
Key Finding: Extended childhood "gives you a developmental way of solving the
exploration/exploitation tradeoff," with caregivers absorbing the poor payoffs that the exploration
phase entails.
How the Author Uses It: To extend the bandit frame across the lifespan and to reframe children's
apparent cognitive deficits as exploration competence.
Important Limitations: A functional hypothesis; no comparative or experimental test is reported in
the chapter.
Replication or Controversy Mentioned: Positioned against the historical view that children are
"cognitively deficient in various ways."
```

## 6. Experiments

```
Experiment Name: Tversky & Edwards two-light observation/betting task
Setup: A box with two lights, each illuminating a fixed but unknown percentage of the time; 1,000
opportunities.
Participants: Not specified.
Procedure: On each opportunity a participant chose either to observe which light came on (gaining
information but no payoff) or to place a bet without observing (payoff but no information). Bets were
not resolved until the end of the session.
Result: With a 60/40 split, participants averaged 505 observations and 495 bets. The optimal policy
was to switch to betting after 38 observations, leaving 962 chances to cash in.
Interpretation: People over-explore substantially — by more than an order of magnitude in the
observation phase.
What It Demonstrates: That the observe-then-bet *structure* is intuitive to people while the
*quantity* of exploration is badly miscalibrated — the same form-right/parameter-wrong pattern seen
with the secretary problem in chapter 1.
Potential Alternative Explanation: The design forbids learning from your own bets, which is unnatural
and may make observation feel more necessary than it is; participants may distrust small samples, or
may be uncertain about the true split rather than merely under-confident; with no stated payoff
structure, they may not have been optimizing what the experimenters assumed.
```

```
Experiment Name: Meyer & Shi airline choice
Setup: Two options — an established carrier with a known on-time rate and a new carrier with no track
record.
Participants: Not specified.
Procedure: Repeated choice, maximizing on-time arrivals over a period. Once the new airline is
abandoned, no further information about it can be obtained.
Result: The new airline was used too little when it was good and too much when it was bad;
participants failed to make clean breaks, often alternating, especially when neither airline was
performing.
Interpretation: Read by the authors as consistent with over-exploration.
What It Demonstrates: Poor calibration in both directions, and a specific failure to execute the
"switch hard and never look back" component of the optimal policy.
Potential Alternative Explanation: Alternating under joint poor performance may reflect a reasonable
suspicion that conditions are non-stationary (a restless bandit), in which case continued exploration
is not a mistake — a possibility the chapter itself raises a page later.
```

```
Experiment Name: Steyvers, Lee & Wagenmakers four-armed bandit
Setup: Four arms, fifteen sequential choices.
Participants: A group of people; number not specified.
Procedure: Participants chose arms; their behavior was classified into strategy types post hoc.
Result: 30% optimal-like, 47% Win-Stay Lose-Shift-like, 22% random alternation between a new arm and
the best so far.
Interpretation: The non-optimal majority behaves in ways that produce late-game exploration when pure
exploitation is called for.
What It Demonstrates: That simple heuristics dominate human bandit play, and that the specific
heuristics used tilt toward exploration.
Potential Alternative Explanation: With only fifteen pulls and four arms, the exploration phase should
occupy a large share of the horizon anyway, so the classification may overstate suboptimality;
strategies inferred from short behavioral sequences are weakly identified.
```

```
Experiment Name: Carstensen & Fredrickson thirty-minute companion choice
Setup: A forced choice of whom to spend thirty minutes with: an immediate family member, the author of
a book recently read, or someone recently met who seemed to share the participant's interests.
Participants: Younger and older adults; numbers not specified.
Procedure: Baseline choice, then two interval manipulations — young people asked to imagine they were
about to move across the country; older people asked to imagine a medical breakthrough granting them
twenty additional years.
Result: Baseline — older people chose the family member, younger people were equally excited by the
author or the new acquaintance. Under manipulation — young people imagining a move chose family;
older people imagining twenty extra years became indistinguishable from the young.
Interpretation: Social preferences track perceived remaining time, not chronological age.
What It Demonstrates: The clearest causal evidence in the chapter that the interval, not the trait,
drives explore/exploit behavior — and it works in both directions.
Potential Alternative Explanation: Hypothetical scenarios may cue demand characteristics or simple
priming of "endings" rather than genuinely changing perceived interval; imagining twenty extra years
also changes health expectations, not just time.
```

## 7. Cases and Stories

```
Case Title: The music journalist's hell
People / Organization: Scott Plagenhoef, former editor in chief of Pitchfork
Context: Music criticism requires turning the exploration dial "all the way to 11" — nothing but new
things, all the time.
What Happened: Plagenhoef's urge to stop wading through unheard music of dubious quality and simply
listen to what he loved was so strong that he loaded only new music onto his iPod, making himself
physically incapable of defecting to the Smiths in a weak moment.
Outcome: A functioning commitment device. "You try to find spaces when you're working to listen to
something that you just want to listen to."
Concept Illustrated: That forced exploration is a genuine cost, not a privilege — "journalists are
martyrs, exploring so that others may exploit." The sharper point is that constant exploration means
"you can never enjoy the fruits of your connoisseurship": expertise is only cashed in during
exploitation, which is why a life of pure exploration is impoverished rather than merely exhausting.
Why This Case Is Useful: Concrete, funny, and it inverts the reader's assumption that a job full of
novelty is paradise. Also a real-world commitment device, pairing with McLay and Rapoport in
chapter 1.
Potential for Reuse: High
```

```
Case Title: Chris Stucchio's restaurants, moving in and moving out
People / Organization: Chris Stucchio, data scientist and blogger
Context: A practitioner who has grappled with explore/exploit in both work and life.
What Happened: On moving to Pune, India, he ate "friggin' everywhere that didn't look like it was
gonna kill me." As he left the city he returned to old favorites instead of trying new places. Now,
knowing he will leave New York soon, he mostly goes to restaurants he already knows and loves.
Outcome: A behavioral signature of the interval. His stated reasoning: "Even if I find a slightly
better place, I'm only going to go there once or twice, so why take the risk?"
Concept Illustrated: The interval makes the strategy; the value of exploration declines as remaining
opportunities dwindle.
Why This Case Is Useful: The single cleanest illustration of the chapter's core idea, in a form any
reader can immediately test against their own behavior.
Potential for Reuse: High
```

```
Case Title: Hollywood's sequel deluge
People / Organization: The major film studios; journalist Nick Allen; the Economist
Context: Sequels among the top ten highest-grossing films rose from 2 (1981) to 3 (1991) to 5 (2001)
to 8 (2011); 2011 set a record for the share of sequels among major studio releases, immediately
broken in 2012 and again in 2013.
What Happened: In December 2012 Nick Allen listed the year ahead with palpable fatigue — a sixth
X-Men, Fast and Furious 6, Die Hard 5, Scary Movie 5, Paranormal Activity 5, Iron Man 3, The Hangover
3, and second outings for the Muppets, the Smurfs, GI Joe and Bad Santa. Meanwhile studio profits fell
40% between 2007 and 2011 and ticket sales declined in seven of ten years.
Outcome: The authors read the exploit-only posture as the industry signalling it believes it is near
the end of its interval — "pulling the arms of the best machines they've got before the casino turns
them out."
Concept Illustrated: Inferring interval from observed strategy; sequels as guaranteed-fanbase exploits.
Why This Case Is Useful: A large, public, quantified example where the behavioral signature and the
financial data line up, and it invites the follow-up question the authors pose — where will the
beloved franchises of the future come from?
Potential for Reuse: High
```

```
Case Title: Jeff Bezos and the regret minimization framework
People / Organization: Jeff Bezos; D. E. Shaw & Co.; Amazon.com
Context: Bezos held a secure, well-paid position in New York; his boss advised him to think carefully
about leaving to start an online bookstore in Seattle.
What Happened: He projected himself to age 80 and asked which choice minimized lifetime regret. He
knew he would not regret trying and failing, but that never having tried "would haunt me every day."
Outcome: "When I thought about it that way it was an incredibly easy decision." He self-deprecatingly
notes only a nerd would call it a "regret minimization framework."
Concept Illustrated: Regret minimization; the long interval favoring exploration.
Why This Case Is Useful: A famous, first-person, quotable articulation of a formal principle by
someone who is not a mathematician — and the framework transfers to any listener's own decision.
Potential for Reuse: High
```

```
Case Title: The Obama DONATE button
People / Organization: Dan Siroker; the 2008 Obama presidential campaign; later Optimizely (co-founded
with Pete Koomen)
Context: A Google product manager took a leave of absence to head New Media Analytics in Chicago.
What Happened: He A/B tested the campaign's bright-red DONATE button — colors, images, headlines,
copy, segmented by visitor history. DONATE AND GET A GIFT won for first-time visitors even net of gift
costs; PLEASE DONATE won for longtime subscribers who had never donated; CONTRIBUTE won for previous
donors. To the team's astonishment, a simple black-and-white photo of the Obama family beat every
other photo or video they produced.
Outcome: $57 million in additional donations attributed to the work. By the 2012 cycle, Siroker's
company Optimizely counted both the Obama re-election campaign and Mitt Romney's campaign as clients.
Concept Illustrated: A/B testing as an industrial-scale bandit problem.
Why This Case Is Useful: Large dollar figure, recognizable event, counterintuitive winner (the plain
family photo), and a wry coda in Optimizely serving both sides of the next election.
Potential for Reuse: High
```

```
Case Title: Forty-one shades of blue
People / Organization: Google
Context: The scale and granularity of commercial A/B testing.
What Happened: Google "infamously" tested forty-one shades of blue for one of its toolbars in 2009.
Outcome: Cited as emblematic — there is no longer "the" Google search algorithm or "the" Amazon
checkout flow, but untold subtle permutations; in some cases no two users may have the same
experience.
Concept Illustrated: Exploration at industrial scale, and users as the experimental substrate.
Why This Case Is Useful: One absurd number that conveys the whole phenomenon instantly.
Potential for Reuse: High
```

```
Case Title: The best minds of my generation
People / Organization: Jeff Hammerbacher, former manager of the Data group at Facebook; quoted in
Bloomberg Businessweek
Context: Reflecting on where analytical talent goes.
What Happened: "The best minds of my generation are thinking about how to make people click ads." The
authors frame it as the millennials' *Howl*, against Ginsberg's "I saw the best minds of my generation
destroyed by madness." Hammerbacher's own verdict on the situation was that it "sucks."
Outcome: A cultural indictment sitting inside a chapter otherwise admiring of the technique.
Concept Illustrated: The moral ambivalence of the explore/exploit industry.
Why This Case Is Useful: Highly quotable, and it gives the section its critical counterweight — useful
whenever the A/B testing material risks sounding celebratory.
Potential for Reuse: High
```

```
Case Title: The Tuskegee Syphilis Study and the Belmont Report
People / Organization: US Public Health Service; whistleblower Peter Buxtun; the Washington Star and
New York Times; the Belmont Conference Center commission
Context: Between 1932 and 1972 several hundred African-American men with syphilis in Macon County,
Alabama were deliberately left untreated as part of a forty-year experiment.
What Happened: Buxtun filed protests in 1966 and again in 1968 without effect. Only when he took the
story to the press — the Washington Star on July 25, 1972, and the New York Times front page the next
day — did the government halt the study. Public outcry and a congressional hearing led to the 1979
Belmont Report.
Outcome: A foundational framework for research ethics that nonetheless explicitly acknowledges the
difficulty of drawing the line, noting that avoiding harm requires learning what is harmful.
Concept Illustrated: That the explore/exploit tension is embedded in medical ethics itself, and that
internal channels failed where publicity worked.
Why This Case Is Useful: Grave, historically important, and it establishes the stakes before the ECMO
argument. Handle with care — the authors use it as context, not as an argument for adaptive trials.
Potential for Reuse: High (with care)
```

```
Case Title: The ECMO trials
People / Organization: Robert Bartlett (University of Michigan); Marvin Zelen; Jim Ware (Harvard
School of Public Health); Don Berry (then University of Minnesota, later MD Anderson Cancer Center)
Context: ECMO routes blood destined for the lungs out of the body, oxygenates it by machine and
returns it to the heart — a drastic measure with its own risks including embolism, for cases where
nothing else remained. In 1975 it saved a newborn girl in Orange County, California, for whom even a
ventilator was insufficient; she has now celebrated her fortieth birthday and is married with children.
Early adult studies had shown no benefit.
What Happened: Bartlett's 1982–84 study used Zelen's play-the-winner algorithm: one infant on
conventional treatment died, then eleven consecutive ECMO infants all survived; afterward eight of
eight ECMO infants survived and two of two conventional infants died. Ware, unconvinced, ran a less
radical design — randomize until a prespecified number of deaths, then switch everyone. Four of ten
conventional infants died; nine of nine ECMO infants survived; all twenty phase-two ECMO patients were
treated and nineteen survived. Berry argued in Statistical Science that the Ware study itself was
unethical and should not have been conducted. A 1990s UK study of nearly two hundred infants reverted
to a conventional even split; twenty-four more infants died in the conventional group.
Outcome: Each study convinced its own authors and failed to convince the field. Berry moved to MD
Anderson to design bandit-based cancer trials; in February 2010 the FDA issued adaptive-design
guidance.
Concept Illustrated: Explore/exploit with lives as the payoff; the cost of insisting on clean evidence.
Why This Case Is Useful: The chapter's most consequential case, with a real body count attached to a
methodological choice, and genuine expert disagreement on all sides rather than a tidy moral.
Potential for Reuse: High
```

```
Case Title: The problem as intellectual sabotage
People / Organization: Allied analysts in World War II; recounted by Peter Whittle
Context: Attempts to solve the multi-armed bandit problem during the war.
What Happened: The effort "so sapped the energies and minds of Allied analysts … that the suggestion
was made that the problem be dropped over Germany, as the ultimate instrument of intellectual
sabotage."
Outcome: An apocryphal-sounding but widely repeated anecdote; Whittle also called the problem "a
classic, and a byword for intransigence."
Concept Illustrated: The difficulty of the problem before Gittins.
Why This Case Is Useful: A perfect one-line hook for how hard the problem was, with wartime color.
Potential for Reuse: High
```

```
Case Title: Unilever's drug question becomes a theorem
People / Organization: Unilever; John Gittins, now professor of statistics at Oxford
Context: In the 1970s Unilever asked a young mathematician to help optimize some of their drug trials
— given several chemical compounds, what is the quickest way to determine which is likely to be
effective?
What Happened: Gittins generalized the question to its most abstract form (multiple options, different
reward probabilities, finite effort to allocate), recognized it as the multi-armed bandit, and solved
it under geometric discounting.
Outcome: "Unexpectedly, what they got was the answer to a mathematical riddle that had gone unsolved
for a generation." Gittins on the achievement: "It's not quite Fermat's Last Theorem."
Concept Illustrated: That "the particular is the gateway to the universal" — an applied industrial
question cracking a famous open problem.
Why This Case Is Useful: A clean origin story with a modest, quotable protagonist, useful for any
argument that applied work drives theory.
Potential for Reuse: High
```

```
Case Title: Thoreau's ten-mile radius
People / Organization: Henry David Thoreau, essay "Walking"
Context: Thoreau preferred to travel close to home and never tired of the Massachusetts landscape.
What Happened: He wrote of "a sort of harmony discoverable between the capabilities of the landscape
within a circle of ten miles' radius, or the limits of an afternoon walk, and the threescore years and
ten of human life." "It will never become quite familiar to you."
Outcome: Used as the literary expression of the restless bandit — in a changing world, exploration
never fully ends.
Concept Illustrated: Restless bandits; the impossibility of exhausting a non-stationary environment.
Why This Case Is Useful: Gives the chapter's most technical idea (non-stationarity) a warm, concrete
image, and pairs the math with the humanistic tradition as the book habitually does.
Potential for Reuse: Medium
```

```
Case Title: Gopnik's preschoolers (and Tom's)
People / Organization: Alison Gopnik, UC Berkeley; Tom Griffiths (co-author)
Context: Explaining why humans take more than a year to walk while caribou and gazelles must run from
predators on day one.
What Happened: Gopnik's account: childhood is a period in which you can explore possibilities without
worrying about payoffs, "because payoffs are being taken care of by the mamas and the papas and the
grandmas and the babysitters." The authors add, parenthetically, that Tom has two highly exploratory
preschool-age daughters and hopes they are following an algorithm with minimal regret.
Outcome: A reframing of children's apparent deficits — they can't tie their shoes or plan long-term or
focus attention, but they excel at pressing buttons at random and jumping between novelties, which is
exactly what exploration requires.
Concept Illustrated: The lifespan as a single bandit algorithm; exploration subsidized by caregivers.
Why This Case Is Useful: Warm, funny, and it delivers a genuinely counterintuitive claim — a baby
mouthing every object in the house is "studiously pulling all the handles at the casino."
Potential for Reuse: High
```

```
Case Title: Carstensen's older adults and the twenty extra years
People / Organization: Laura Carstensen (Stanford); Barbara Fredrickson
Context: Investigating why social networks shrink with age, against the traditional explanation of
decline and disengagement.
What Happened: In the thirty-minute companion choice, older people preferred an immediate family
member while young people were equally drawn to a book's author or a promising new acquaintance. Young
people imagining a cross-country move chose family too; older people imagining a medical breakthrough
granting twenty extra years became indistinguishable from the young.
Outcome: The difference is about perceived interval, not age. Older people are also generally more
satisfied with their social networks and often report higher emotional well-being than younger adults.
Concept Illustrated: The interval makes the strategy, demonstrated experimentally in both directions.
Why This Case Is Useful: The chapter's strongest evidence, and it converts a stereotype (the old are
set in their ways; the young are fickle) into rational behavior on both sides.
Potential for Reuse: High
```

```
Case Title: College versus the retirement home
People / Organization: None — an observation by the authors
Context: Two structurally identical situations: a new social environment full of people you haven't met.
What Happened: Going to college is typically positive and exciting; entering a retirement home can be
painful.
Outcome: The difference is attributed partly to where one sits on the explore/exploit continuum.
Concept Illustrated: The interval determining whether novelty reads as opportunity or as loss.
Why This Case Is Useful: A single sentence that makes the interval idea emotionally legible; strong
material for any piece on aging.
Potential for Reuse: High
```

```
Case Title: Your grandfather's restaurant
People / Organization: None — an illustrative rule of thumb
Context: How to weigh advice from elders.
What Happened: The authors advise: when your grandfather tells you which restaurants are good, listen
— those are pearls gleaned from decades of searching. But when he only goes to the same restaurant at
5:00 p.m. every day, feel free to explore other options, even though they'll likely be worse.
Outcome: A clean separation between an elder's accumulated *data* (valuable) and their current
*policy* (calibrated to a different interval than yours).
Concept Illustrated: Interval-dependence of optimal policy; transferability of information but not of
strategy.
Why This Case Is Useful: Immediately actionable, memorable, and it resolves a common intergenerational
friction with the chapter's own machinery.
Potential for Reuse: High
```

```
Case Title: Pirsig's "What's best?" — and the authors' rebuttal
People / Organization: Robert Pirsig, *Zen and the Art of Motorcycle Maintenance* (1974)
Context: The chapter's opening argument. Pirsig decries the conversational opener "What's new?"
What Happened: Pirsig argues the question, "if pursued exclusively, results only in an endless parade
of trivia and fashion, the silt of tomorrow," and endorses "What's best?" as vastly superior. The
authors counter that every "best" song and restaurant among your favorites began humbly as something
merely "new" to you — a reminder that there may be yet-unknown bests still out there, so the new is
worthy of at least some attention.
Outcome: The chapter's founding argument, staged as a disagreement with a named literary authority.
Concept Illustrated: Why pure exploitation is self-undermining — you can only exploit what exploration
has already found.
Why This Case Is Useful: A named, canonical opponent is far more engaging to argue against than a
generic intuition, and this is the chapter's only explicit disagreement with another author.
Potential for Reuse: High
```

```
Case Title: Lydia Davis on rereading
People / Organization: Lydia Davis (epigraph to "… And Exploit")
Context: Positioned exactly where the chapter turns to aging.
What Happened: Davis describes reaching a juncture familiar to lifelong readers: in the time left to
her, should she read more and more new books, or "cease with that vain consumption—vain because it is
endless—and begin to reread those books that had given me the intensest pleasure in my past."
Outcome: N/A — a statement of the dilemma rather than a resolution.
Concept Illustrated: The interval, articulated from the inside by someone living it.
Why This Case Is Useful: The most affecting statement of the chapter's central idea, arriving from
literature rather than mathematics. Ideal for opening or closing a piece on the topic.
Potential for Reuse: High
```

```
Case Title: Carpe diem is self-contradictory
People / Organization: Robin Williams in *Dead Poets Society* (1989); the authors
Context: Opening the "Seize the Interval" section.
What Happened: Against "Seize the day, boys. Make your lives extraordinary," the authors call the
advice "incredibly important" but "somewhat self-contradictory" — seizing a day and seizing a lifetime
are entirely different endeavors. They propose an inverse to "Eat, drink, and be merry, for tomorrow we
die": "Start learning a new language or an instrument, and make small talk with a stranger, because
life is long, and who knows what joy could blossom over many years' time."
Outcome: Famous advice reframed as interval-dependent rather than universally correct.
Concept Illustrated: That inherited wisdom silently encodes a particular interval, and is wrong
outside it.
Why This Case Is Useful: A recognizable cultural touchstone turned into a teaching example, plus an
original aphorism that stands alone as a quote or a closing line.
Potential for Reuse: High
```

```
Case Title: The berry patch and the Coke
People / Organization: Andy Warhol (quoted); the authors
Context: Assessing how much the restless-bandit problem actually bites in modern life.
What Happened: "A berry patch might be ripe one week and rotten the next, but as Andy Warhol put it,
'A Coke is a Coke.'" The authors add that "having instincts tuned by evolution for a world in constant
flux isn't necessarily helpful in an era of industrial standardization."
Outcome: An argument that many modern payoffs are unusually stationary, so the classical stationary
algorithms transfer better than they otherwise would.
Concept Illustrated: Evolutionary mismatch; non-stationarity as a feature of ancestral rather than
industrial environments.
Why This Case Is Useful: The chapter's only explicit evolutionary-mismatch claim, and a neat two-image
contrast.
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: Exploitation is not a vice
Example: A family gathering on the holidays, a bookworm with coffee and a beloved favorite, a band
playing its greatest hits, a couple dancing to "their song."
Why It Works: Preempts the reader's assumption that "exploit" is the bad word by naming four scenes
nobody would give up, which makes the neutrality of the technical vocabulary felt rather than asserted.
Possible Alternative Domain: Everyday Life
```

```
Concept: The exploration bonus
Example: The Gittins table's top-left cell — a 0–0 record has an expected value of 0.5000 but an index
of 0.7029, beating a machine known to pay out seven times in ten.
Why It Works: One number in one cell overturns the reader's default that a proven 70% option must beat
a total unknown, and it is checkable against the table rather than taken on faith.
Possible Alternative Domain: Mathematics
```

```
Concept: The Gittins index as an indifference price
Example: The Banker on Deal or No Deal offering money not to open the briefcase; the price at which
you'd take the sure thing is the briefcase's value to you.
Why It Works: Converts an abstract index into a familiar transaction with a number attached, and the
game show format means most audiences already have the intuition.
Possible Alternative Domain: Business
```

```
Concept: Why the interval governs the strategy
Example: Stucchio eating everywhere in Pune on arrival and returning to old favorites on departure —
"even if I find a slightly better place, I'm only going to go there once or twice, so why take the
risk?"
Why It Works: Same person, same city, opposite strategies, with the only changed variable being time
remaining. It is a natural controlled experiment the reader can run on themselves.
Possible Alternative Domain: Everyday Life
```

```
Concept: Upper confidence bounds
Example: A restaurant with a single mediocre review still retains a potential for greatness absent in
a restaurant with hundreds of mediocre reviews.
Why It Works: Teaches that uncertainty itself is the asset, using a comparison where both options have
identical means and only the sample size differs.
Possible Alternative Domain: Everyday Life
```

```
Concept: Logarithmic regret
Example: You'll make as many mistakes in your first ten pulls as in the following ninety, and as many
in your first year as in the rest of the decade combined.
Why It Works: Translates a growth rate into a lived timeline, and delivers genuine consolation without
overpromising — regret keeps accumulating, just ever more slowly.
Possible Alternative Domain: Psychology
```

```
Concept: Children as exploration machines
Example: A baby putting every object in the house into its mouth is "studiously pulling all the handles
at the casino."
Why It Works: Maps an exasperating everyday behavior onto the formal model in one image, and flips the
valence from deficit to competence.
Possible Alternative Domain: Psychology
```

```
Concept: The user as the payoff, not the player
Example: "In this particular multi-armed bandit problem, you're not the gambler; you're the jackpot."
Why It Works: A perspective inversion in nine words; it reframes the entire A/B testing section from
a technique the reader might adopt into something being done to them.
Possible Alternative Domain: Business
```

## 9. Counterintuitive Insights

```
Insight: A completely untried option can be more attractive than one known to be good.
Common Belief: Between an unknown and a proven 70% performer, take the proven one.
Author's Argument: The Gittins index assigns a 0–0 record 0.7029 (against an expected value of
0.5000), because information has value when you will act again. At a 0.99 discount rate the unknown is
worth a guaranteed 86.99%.
Evidence: The index tables at 0.9 and 0.99 discount rates.
Why It Is Surprising: It makes "the grass is greener" mathematically correct rather than a cognitive
error — the unknown has upside even when its expected value is lower.
Qualification: This depends entirely on geometric discounting and a long horizon; with a short
interval, switching costs, or one-shot stakes it does not hold.
```

```
Insight: Optimism is rational, not naive.
Common Belief: Realism means judging options by what they have actually delivered.
Author's Argument: UCB algorithms deliberately evaluate options at the best they could reasonably be,
and this is precisely what achieves near-minimal regret. "Optimism is the best prevention for regret."
Evidence: The regret guarantees of UCB; Kaelbling's optimistic robots.
Why It Is Surprising: It gives a formal defense of the benefit of the doubt, converting a disposition
usually treated as a bias into an algorithmic virtue.
```

```
Insight: You will never stop accumulating regret — and that is the good news.
Common Belief: A sufficiently wise person eventually gets past regret.
Author's Argument: Lai and Robbins proved total regret never stops increasing absent omniscience, but
the best strategies make it grow logarithmically, so each year brings fewer new regrets than the last.
Evidence: The 1985 proof.
Why It Is Surprising: It replaces an unattainable goal (no regrets) with an attainable one (a
declining rate), which is both more honest and more consoling.
```

```
Insight: People over-explore, even though we normally accuse ourselves of being stuck in our ways.
Common Belief: Humans are creatures of habit who under-sample novelty.
Author's Argument: Three studies find the opposite in repeated-choice settings — most strikingly,
505 observations where 38 sufficed.
Evidence: Tversky & Edwards 1966; Meyer & Shi 1990s; Steyvers, Lee & Wagenmakers.
Why It Is Surprising: It contradicts both folk psychology and the chapter's own advice to explore
more, a tension the chapter notes and only partly resolves via non-stationarity.
```

```
Insight: The elderly are not withdrawing; they are optimizing.
Common Belief: Shrinking social circles in old age reflect decline, fragility, and disengagement.
Author's Argument: Carstensen shows the shrinkage is deliberate pruning of peripheral ties to
concentrate on a meaningful core, and that it tracks perceived interval rather than age — young people
facing a move behave the same way, and older people imagining twenty extra years behave like the young.
Evidence: The Carstensen & Fredrickson choice experiment with bidirectional interval manipulation, and
the finding that older adults report higher emotional well-being.
Why It Is Surprising: It converts a deficit narrative into a rational-strategy narrative, and the
manipulation in both directions rules out the obvious alternative.
```

```
Insight: Life should get better over time.
Common Belief: Youth is the peak; aging is decline.
Author's Argument: Exploration necessarily disappoints most of the time — the Gittins index and UCB
inflate the appeal of unknowns beyond expectation — so a life that shifts toward favorites should
improve in quality.
Evidence: The structure of the exploration bonus, plus Carstensen's well-being findings.
Why It Is Surprising: It derives an optimistic conclusion about aging from the same math that
recommends youthful novelty-seeking.
```

```
Insight: Children's caprice may be wiser than adult judgment.
Common Belief: Children are cognitively deficient versions of adults.
Author's Argument: They look terrible on exploit capacities and excellent on exploration capacities —
which is exactly right for their position in the interval. Our intuitions about rationality are
"too often informed by exploitation rather than exploration."
Evidence: Gopnik's functional argument; the contrast with precocial animals like caribou and gazelles.
Why It Is Surprising: It reverses the developmental deficit model, and implicates the reader's own
definition of rationality as parochial.
```

```
Insight: The standard clinical trial may be the less ethical design.
Common Belief: Randomized controlled trials with fixed arms are the ethical gold standard.
Author's Argument: They optimize for resolving the question rather than for treating the patients
enrolled, and information accruing mid-trial could be used to help those patients.
Evidence: The ECMO sequence; Berry's published objection to the Ware study; the 24 excess deaths in
the conventional arm of the UK study; the FDA's 2010 adaptive-design guidance.
Why It Is Surprising: It turns the methodological conservative into the party with something to
justify. The chapter is careful, however, to report that this remains a minority-but-growing position
and that the adaptive studies were themselves criticized as uninformative.
Counterarguments the chapter itself supplies (do not reuse this insight without them): (1) statistics
transformed medicine from ad hoc persuasion into shared standards of what evidence is persuasive, and
changing accepted practice risks upsetting that balance; (2) ECMO is highly invasive with its own
risks including embolism; (3) early studies in adults showed no benefit over conventional treatment —
which is the strongest reason randomizing was defensible; (4) the largest replication, the UK study,
found a smaller effect than the American ones.
```

## 10. Unique or Unusual Ideas

```
Idea: You can infer someone's perceived interval by watching their explore/exploit ratio.
Why It Seems Unique: The chapter runs the causal arrow backwards — normally you'd predict behavior
from circumstances, but here an observed strategy diagnoses a hidden belief about remaining time.
Applied to Hollywood, it turns a genre complaint into an economic reading; applied to a person, it
turns a habit into a disclosure.
Potential Connection to Other Topics: Revealed preference; corporate short-termism; organizational
decline; reading strategy as signal in competition.
```

```
Idea: Exploration is a cost borne by someone, and the question is who.
Why It Seems Unique: "Journalists are martyrs, exploring so that others may exploit" and "you're not
the gambler; you're the jackpot" and the ECMO control group are three faces of one idea the chapter
never names: exploration's costs and benefits often land on different people.
Potential Connection to Other Topics: Research ethics; the economics of reviewers and critics; open
source and public goods; who bears the cost of experimentation in AI deployment.
```

```
Idea: Childhood is a life stage engineered by evolution to solve a computational problem.
Why It Seems Unique: It explains a striking biological fact (uniquely prolonged human helplessness)
by reference to an algorithmic requirement, with caregivers functioning as a subsidy that makes the
exploration phase survivable.
Potential Connection to Other Topics: Evolutionary developmental biology; neoteny; play; the design of
training curricula for both humans and machines.
```

```
Idea: Old age as the rational payoff phase rather than a decline.
Why It Seems Unique: It reverses the standard framing not by disputing the facts (networks do shrink)
but by reinterpreting the same facts as strategy, with experimental support in both directions.
Potential Connection to Other Topics: Socioemotional selectivity theory; end-of-life care; retirement
planning; the "positivity effect" in aging research.
```

```
Idea: Regret as a quantity with a provable minimum growth rate.
Why It Seems Unique: Most treatments of regret are therapeutic or philosophical; here it is a number
with a theorem attached, and the theorem's content ("logarithmic") delivers a specific and unusual
form of consolation.
Potential Connection to Other Topics: Regret theory in economics; counterfactual thinking; online
learning theory.
```

```
Idea: The problem as a weapon — dropping it over Germany as intellectual sabotage.
Why It Seems Unique: A rare instance of a mathematical problem being characterized as dangerous to
the people who work on it.
Potential Connection to Other Topics: History of operations research; wartime mathematics; the
sociology of open problems.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: The chapter says people over-explore, then spends its second half urging more exploration.
Author's Position: Both. The lab evidence shows over-exploration; the lifespan argument says our
intuitions about rationality are skewed toward exploitation and that emphasizing novelty is rational,
especially earlier in life.
Possible Counterargument: These can be reconciled — lab tasks have short, known horizons where
exploitation should dominate sooner, while life has long ones — but the chapter never states the
reconciliation explicitly. As written, a reader is told both that they explore too much and that they
should explore more.
What Evidence Would Help Resolve It: Bandit experiments with genuinely long or open-ended horizons; or
direct measurement of whether people's exploration rates track their actual remaining intervals.
```

```
Issue: The Gittins index is presented as the solution and then substantially undercut.
Author's Position: It "completely solves" the problem under geometric discounting, but is optimal only
under strong assumptions, breaks with switching costs, and is impractical to compute.
Possible Counterargument: Given that people demonstrably don't discount geometrically and that
switching costs are ubiquitous in the chapter's own examples (moving cities, changing airlines,
changing treatments), the headline numbers — including the famous 0.7029 — may not transfer to any of
the everyday situations they're used to illuminate.
What Evidence Would Help Resolve It: How much the optimal policy actually changes under hyperbolic
discounting and realistic switching costs; whether UCB's recommendations diverge from Gittins's in
practice, which the chapter asserts they don't but does not show.
```

```
Issue: The ethical argument about clinical trials rests on studies too small to settle the question.
Author's Position: Adaptive designs got better treatment to patients inside the trial; the UK's
conventional design cost 24 additional infant lives.
Possible Counterargument: The Michigan study's near-absence of a control arm is exactly why it failed
to convince, and the UK study found a smaller effect — which suggests the American estimates may have
been inflated. If the true effect is smaller, the "cost of that knowledge" framing is doing rhetorical
work that the evidence doesn't fully carry. Ware and the UK investigators were responding to genuine
uncertainty, not merely to convention.
What Evidence Would Help Resolve It: Simulation studies comparing expected lives lost under adaptive
versus conventional designs across a range of true effect sizes; and evidence on how often adaptive
trials produce results the field accepts.
```

```
Issue: Whose regret is being minimized in A/B testing and clinical trials?
Author's Position: The chapter notes the structural identity of the two and observes that half of A/B
test users get the inferior option, and that you are "the jackpot."
Possible Counterargument: The bandit framing optimizes the *experimenter's* cumulative payoff. For
users and patients the relevant question is consent and distribution, not aggregate regret — a point
the Belmont Report material raises and the A/B testing section does not return to. The Hammerbacher
quotation gestures at this but the chapter does not pursue it.
What Evidence Would Help Resolve It: Not empirical — it is a normative question about whose objective
function the algorithm should encode.
```

```
Issue: Geometric discounting is assumed, acknowledged to be empirically false, and then used anyway.
Author's Position: Explicitly flagged: behavioral economics and psychology suggest people don't
discount geometrically.
Possible Counterargument: The chapter presents the 0–0 index values as guidance for everyday decisions
while conceding the assumption generating them doesn't describe people. Either the numbers are
normative (this is how you *should* discount) — which is a separate argument the chapter doesn't make
— or they are descriptive and therefore wrong.
What Evidence Would Help Resolve It: Index values computed under hyperbolic discounting, for
comparison.
```

```
Issue: The restless bandit is declared intractable, which undercuts most of the chapter's applications.
Author's Position: No tractable algorithm exists and it is believed none ever will; nevertheless
Gittins and UCB provide "reasonably good approximate solutions," particularly if payoffs don't change
much — and the authors argue modern payoffs are unusually static ("A Coke is a Coke").
Possible Counterargument: Restaurants change chefs, people change, treatments interact with evolving
pathogens, and web users' preferences shift — the chapter's own examples are mostly non-stationary.
The Warhol line is an assertion about industrial standardization, not evidence about the stability of
the payoffs that matter in the examples used.
What Evidence Would Help Resolve It: Measurement of how quickly payoffs actually drift in the chapter's
domains, and how much the stationary algorithms lose under that drift.
```

```
Issue: Gopnik's account of childhood is a functional story without a discriminating test.
Author's Position: Extended dependence exists to permit exploration while caregivers absorb the cost.
Possible Counterargument: Prolonged human immaturity has several competing explanations — brain size
versus pelvic constraints, the demands of learning a complex culture, extended social learning. The
explore/exploit account is compatible with these rather than competing with them, and no evidence is
offered that would favor it.
What Evidence Would Help Resolve It: Cross-species comparison relating length of dependence to the
breadth of the environmental "arm space" a species must learn.
```

```
Issue: Bezos's regret minimization is a survivorship-biased anecdote used as a framework.
Author's Position: Offered as an example of what computer science can formalize — "a life with minimal
regret."
Possible Counterargument: The framework is illustrated by someone for whom it worked spectacularly.
The same reasoning at age 80 would have endorsed countless failed ventures, and regret minimization
does not distinguish between explorations that are cheap to reverse and ones that are not — a
distinction that matters more than the framework's own logic admits.
What Evidence Would Help Resolve It: Whether people who apply anticipated-regret framing make better
decisions on average, not just whether famous successes report having used it.
```

## 12. Quotable Ideas

```
Paraphrase (short): Exploration is gathering information; exploitation is using what you already know
to get a known good result.
Why the Idea Matters: The definitional move that strips the moral loading off both words and makes the
whole framework usable.
Source Location: "Explore/Exploit" (PDF p. 48).
```

```
Paraphrase (short): Aphorisms admit the tension between new friends and old but never tell us the
ratio of silver to gold that makes the best alloy of a life.
Why the Idea Matters: The chapter's statement of what quantification adds to inherited wisdom —
parallel to chapter 1's therapist-versus-algorithm line.
Source Location: Opening section (PDF p. 48).
```

```
Paraphrase (short): The value of exploration can only fall over time; the value of exploitation can
only rise. The interval makes the strategy.
Why the Idea Matters: The chapter's core principle in two clauses, and the basis for everything from
Hollywood to old age.
Source Location: "Seize the Interval" (PDF p. 51).
```

```
Paraphrase (short): Journalists are martyrs, exploring so that others may exploit.
Why the Idea Matters: Names the fact that exploration is a cost, and that it is often borne by
someone other than the beneficiary.
Source Location: "Explore/Exploit" (PDF p. 49).
```

```
Paraphrase (short): A completely unknown option can outscore one you know pays off seven times in ten.
Why the Idea Matters: The chapter's most surprising single result, and the formal warrant for
preferring the unknown.
Source Location: "The Gittins Index" (PDF p. 57).
```

```
Paraphrase (short): The math explains why the grass looks greener: the unknown has a chance of being
better, even when you expect it to be no different.
Why the Idea Matters: Converts a proverb about self-deception into a description of correct reasoning.
Source Location: "The Gittins Index" (PDF p. 58).
```

```
Paraphrase (short): Barnard — to try and fail is at least to learn; to fail to try is to suffer the
inestimable loss of what might have been.
Why the Idea Matters: The pre-mathematical statement of regret that the chapter then makes measurable.
Source Location: "Regret and Optimism" (PDF p. 60).
```

```
Paraphrase (short): Under a regret-minimizing algorithm you'll have fewer new regrets each year than
the year before.
Why the Idea Matters: The most usable consolation in the chapter, and it is a theorem rather than
sentiment.
Source Location: "Regret and Optimism" (PDF p. 61).
```

```
Paraphrase (short): In the long run, optimism is the best prevention for regret.
Why the Idea Matters: The chapter's thesis about disposition, earned by the UCB result rather than
asserted.
Source Location: "Regret and Optimism" (PDF p. 63).
```

```
Paraphrase (short): In this multi-armed bandit problem, you're not the gambler; you're the jackpot.
Why the Idea Matters: The single sharpest line in the chapter, and its main critical note about the
commercial internet.
Source Location: "Bandits Online" (PDF p. 65).
```

```
Paraphrase (short): Hammerbacher — the best minds of my generation are thinking about how to make
people click ads.
Why the Idea Matters: The moral counterweight to the chapter's admiration of A/B testing; the authors
frame it as the millennials' *Howl*.
Source Location: "Bandits Online" (PDF p. 64).
```

```
Paraphrase (short): The Belmont Report concedes that avoiding harm requires learning what is harmful,
and that acquiring that knowledge can expose people to risk.
Why the Idea Matters: The explore/exploit tradeoff written into the founding document of research
ethics, acknowledged and left unresolved.
Source Location: "Clinical Trials on Trial" (PDF p. 66).
```

```
Paraphrase (short): To live in a restless world requires a certain restlessness in oneself.
Why the Idea Matters: The chapter's answer to non-stationarity, and its most quotable sentence about
never fully settling.
Source Location: "The Restless World" (PDF p. 73).
```

```
Paraphrase (short): A baby putting every object in the house into its mouth is studiously pulling all
the handles at the casino.
Why the Idea Matters: Reframes infant behavior as systematic search rather than chaos.
Source Location: "Explore …" (PDF p. 74).
```

```
Paraphrase (short): What we take to be the caprice of children may be wiser than we know.
Why the Idea Matters: The section's closing line, and a compact statement of the chapter's challenge
to exploitation-centric definitions of rationality.
Source Location: "Explore …" (PDF p. 75).
```

```
Paraphrase (short): Listen to your grandfather about which restaurants are good; feel free to ignore
him about which one to go to tonight.
Why the Idea Matters: Separates transferable information from non-transferable strategy in one image.
Source Location: "… And Exploit" (PDF p. 77).
```

```
Paraphrase (short): What an explorer trades off for knowledge is pleasure — exploration necessarily
means being let down most of the time.
Why the Idea Matters: The honest cost of the chapter's own advice, and the premise of its claim that
life improves with age.
Source Location: "… And Exploit" (PDF p. 77).
```

```
Paraphrase (short): Pirsig warned that asking "what's new?" yields only an endless parade of trivia
and fashion — "the silt of tomorrow." The authors' reply: every "best" you have was once merely new.
Why the Idea Matters: The chapter's founding argument, and its only direct disagreement with a named
author.
Source Location: Opening section (PDF p. 47).
```

```
Paraphrase (short): The authors' invented counter-aphorism — start learning a new language or an
instrument and make small talk with a stranger, because life is long and who knows what joy could
blossom over many years.
Why the Idea Matters: The inverse of "eat, drink, and be merry, for tomorrow we die," and the
chapter's demonstration that inherited wisdom silently assumes an interval.
Source Location: "Seize the Interval" (PDF p. 50).
```

```
Paraphrase (short): Churchill — for myself I am an optimist; it does not seem to be much use being
anything else.
Why the Idea Matters: A pre-mathematical statement of precisely what the UCB results prove.
Source Location: Epigraph to "Regret and Optimism" (PDF p. 60).
```

```
Paraphrase (short): Lydia Davis, on whether to keep reading new books or begin rereading the ones that
gave her the greatest pleasure — "vain because it is endless."
Why the Idea Matters: The interval problem stated from the inside, by someone living it.
Source Location: Epigraph to "… And Exploit" (PDF p. 75).
```

```
Paraphrase (short): "Git while the Gittins's good."
Why the Idea Matters: The chapter's own footnote summary of the section — worth keeping for tone, and
the only pun of its kind in the chapter.
Source Location: Footnote (PDF p. 78).
```

## 13. Psychology Connections

- **Developmental psychology.** Gopnik's account of prolonged childhood as an exploration phase, and
  the reframing of children's "deficits" (no long-term planning, no focused attention) as exploration
  competence.
- **Socioemotional selectivity theory.** Carstensen's research program is the chapter's empirical
  anchor; the bidirectional interval manipulation is a model of how to test a motivational account.
- **Aging and emotional well-being.** Older adults report higher satisfaction with their social
  networks and often higher emotional well-being than younger adults — the chapter's evidence that
  exploitation pays.
- **Regret and counterfactual thinking.** Barnard's "inestimable loss of what might have been," Bezos's
  age-80 projection, and the formal regret definition all address the same psychological object from
  different directions; the chapter's distinctive move is making it measurable.
- **Anticipated regret as a motivational device.** Bezos used projection rather than calculation, which
  is closer to prospective hindsight / premortem techniques than to any bandit algorithm (inference).
- **Discounting.** Geometric versus hyperbolic discounting is named explicitly as the point where the
  model and human psychology diverge — the chapter cites "a variety of experiments in behavioral
  economics and psychology" without naming them.
- **Over-exploration as a systematic bias.** Three studies converge; notable because it points opposite
  to the more familiar status quo bias and habit literature (inference: the chapter does not engage
  that literature).
- **Optimism as adaptive rather than biased.** UCB provides a normative defense of optimistic priors,
  which sits interestingly against the depressive-realism and optimism-bias traditions (inference).
- **Commitment devices and self-control.** Plagenhoef loading only new music onto his iPod is a
  textbook commitment device, and it appears here in service of forcing exploration rather than
  restraining impulse — the inverse of the usual case.
- **Novelty seeking and boredom.** The chapter treats the pull toward the new as rational given a long
  interval, offering a functional account of a trait usually discussed as temperament.
- **Decision fatigue — raised and abandoned.** The chapter's opening paragraph is a vivid description
  of choice exhaustion (Italian or the new Thai place, best friend or new acquaintance, "you're already
  exhausted before you get to the first bite," and putting on a record no longer feels relaxing). The
  chapter never returns to it: throughout, exploration's cost is modeled purely as forgone payoff,
  never as cognitive depletion. That gap is worth recording, since it is where the choice-overload
  literature would attack.

## 14. Mathematics and Decision Science Connections

- **Multi-armed bandits.** The chapter's central formalism, and the canonical framing of the
  exploration-exploitation problem in sequential decision theory.
- **Expected value and its insufficiency.** The 9–6 versus 1–1 comparison shows that ranking by
  expected value alone (60% vs. 50%) gives the wrong answer once future decisions are counted.
- **Index policies.** The Gittins index is the archetypal index policy — decomposing a coupled
  multi-arm problem into independent per-arm computations is the theorem's real content.
- **Discounted infinite horizons.** Gittins's reframing from a fixed interval to an endless but
  geometrically discounted future is what makes the problem tractable; the discount factor plays the
  role that the horizon plays in chapter 1's secretary problem.
- **Dynamic programming / backward induction.** Bellman's exact solution, explicitly linked back to the
  full-information secretary problem.
- **Regret bounds and online learning.** Lai & Robbins's logarithmic lower bound is a foundational
  result in online learning theory; UCB is the standard family of algorithms achieving it.
- **Confidence intervals and uncertainty quantification.** UCB's mechanism is a direct application of
  interval estimation — with the twist that the interval's upper end, not its center, drives the
  decision.
- **Optimism under uncertainty as a design principle.** A general technique in optimization and
  reinforcement learning, here given its plain-language name.
- **Non-stationarity and intractability.** The restless bandit as a stated negative result — a case
  where the chapter's own framework admits no tractable solution.
- **Sequential experimental design.** Adaptive trials, play-the-winner allocation, and A/B testing are
  all sequential design problems; the chapter's contribution is showing they are the same problem.
- **Urn schemes.** Zelen's ball-and-hat mechanism is a randomized urn model, a classical probabilistic
  construction.
- **Evolutionary mismatch (the chapter's only such claim).** "Having instincts tuned by evolution for
  a world in constant flux isn't necessarily helpful in an era of industrial standardization" — a berry
  patch is ripe one week and rotten the next, but "a Coke is a Coke." The argument is that ancestral
  environments were restless bandits while many modern payoffs are stationary, so our exploration
  instincts may be calibrated to the wrong problem class.

## 15. Sports Connections

**Direct examples from the book:** One. The authors write that "the untested rookie is worth more
(early in the season, anyway) than the veteran of seemingly equal ability, precisely because we know
less about him" — a direct application of the exploration bonus to roster decisions.

**Inferred applications (mine):**

- **Squad rotation and youth minutes.** Playing an academy graduate is exploration with a real cost in
  expected points; the interval is the club's competitive horizon. A team out of title contention in
  March has a long interval and should explore; a team in a title race has a short one and should
  exploit. This explains why giving debuts late in a dead season is not sentimentality but correct play.
- **Interval as the read on a manager's job security.** A manager who suddenly stops rotating and
  fields the same eleven every week is revealing a short perceived interval — the Hollywood-sequel
  signature applied to a dugout.
- **The rookie premium is quantifiable.** The Gittins logic says a player with a 1–1 record should be
  preferred over one with a 9–6 record; in scouting terms, a small sample of promising output has
  option value that a longer mediocre record does not. This is an argument against over-weighting
  career averages for young players.
- **Set-piece and tactical variation.** Trying an unusual routine is exploration; the payoff is
  information about how opponents respond, which has value only if there are matches remaining to use
  it. Late in a cup run, exploit.
- **In-season versus off-season learning.** Training is a subsidized exploration phase in exactly
  Gopnik's sense — the caregivers absorbing the cost of poor payoffs are the coaching staff and the
  friendly fixture list.
- **Restless bandits in opposition scouting.** Opponents adapt, so a tactic that stopped working two
  seasons ago may work now — the "under new management" restaurant, applied to a rival's back line.
- **Adaptive designs in sports science.** Testing a training intervention on half a squad for a full
  season is an A/B test with the same objection: half the squad gets the worse protocol throughout.
  Play-the-winner allocation would move athletes toward the better protocol mid-season.
- **Career arc.** An athlete's own explore/exploit curve — positional experimentation early, refinement
  of a signature game late — mirrors the chapter's lifespan argument.

## 16. AI and Machine Learning Connections

**Direct from the book:** Leslie Kaelbling's "optimistic robots," which explore by boosting the
assessed value of uncharted terrain, are the chapter's one explicit AI example. The chapter also
notes that explore/exploit algorithms "effectively power, both economically and technologically, a
significant fraction of the Internet itself."

**Inferred connections (mine):**

- **Reinforcement learning.** The explore/exploit tradeoff is RL's defining problem; the discount
  factor γ is exactly the chapter's geometric discounting, and the interval is the effective horizon
  1/(1−γ). ε-greedy, Boltzmann exploration, UCB and Thompson sampling are the standard families.
- **UCB and Thompson sampling in production.** Bandit algorithms are the standard replacement for
  fixed-split A/B tests in recommendation, ad serving and layout optimization — precisely the
  improvement the chapter says is "hotly contested."
- **Optimistic initialization.** Setting initial value estimates high to force exploration is the
  chapter's Gittins-bonus intuition implemented in one line of code.
- **Exploration in LLM agents.** An agent choosing among tools, search queries, or candidate plans
  faces a bandit; the interval is how many more times it will face this task — which argues for
  cheaper exploitation in one-shot user requests and more exploration in long-running or repeated
  workflows.
- **Sample efficiency and cold start.** The 0–0 index formalizes why recommender systems should
  promote unrated items: an item with no data has option value, which is the principled version of
  cold-start heuristics.
- **Non-stationarity in deployed models.** The restless bandit is distribution shift by another name;
  continual retraining and sliding-window statistics are the practical response to the chapter's
  intractability result.
- **RLHF and evaluation.** Deciding how much labelling budget to spend on new prompt distributions
  versus refining known ones is a bandit over data collection, not just over model outputs.
- **Curriculum learning and developmental AI.** Gopnik's childhood argument maps onto curricula that
  front-load broad, low-stakes exploration before task-specific optimization — the caregiver subsidy
  becomes the safety of a training environment.
- **The ethics of live experimentation.** The chapter's clinical-trial argument transfers directly to
  A/B testing model variants on users: the same question of who bears the exploration cost, with far
  weaker consent norms than medicine's.
- **Regret as the standard metric.** Cumulative regret is the primary theoretical yardstick for online
  learning algorithms; the Lai–Robbins logarithmic bound is the benchmark against which new algorithms
  are still measured.

## 17. Content Creation Opportunities

```
Idea: Why a total unknown beats a sure thing
Format: YouTube Long-form
Core Concept: The Gittins index and the exploration bonus
Hook: A slot machine you've never touched is mathematically more attractive than one you know pays out
70% of the time. The math says the grass really is greener.
Best Supporting Case: The Gittins table — 0–0 scores 0.7029 against an expected value of 0.5000 — and
Unilever's drug question accidentally solving a problem a generation of mathematicians couldn't.
Psychology Angle: Optimism as rational rather than biased; the benefit of the doubt, formalized.
Math Angle: Index policies, geometric discounting, why 0.99 discounting pushes the unknown to 86.99%.
Sports Angle: The untested rookie is worth more than the equally rated veteran, precisely because we
know less.
AI Angle: Optimistic initialization; cold start in recommender systems.
```

```
Idea: The interval — one number that decides whether to try something new
Format: YouTube Long-form
Core Concept: "The interval makes the strategy"
Hook: Whether you should try the new restaurant has almost nothing to do with the restaurant. It
depends on how long you're staying in town.
Best Supporting Case: Stucchio eating everywhere in Pune on arrival and returning to old favorites on
his way out — same person, same city, opposite strategy.
Psychology Angle: Carstensen's older adults becoming indistinguishable from the young once they
imagine twenty extra years.
Math Angle: Exploration value monotonically falls, exploitation value monotonically rises.
Sports Angle: A club out of contention should be handing out debuts; a club in a title race shouldn't.
AI Angle: The discount factor γ as the effective horizon in reinforcement learning.
```

```
Idea: Hollywood is telling you it thinks it's dying
Format: YouTube Short
Core Concept: Inferring interval from observed strategy
Hook: Sequels in the top ten: two in 1981, eight in 2011. That's not laziness. That's an industry
betting it doesn't have long left.
Best Supporting Case: The sequel counts, plus studio profits down 40% between 2007 and 2011.
Psychology Angle: Short-termism as a readable signal rather than a character flaw.
Math Angle: Exploit-only behavior implies a short perceived interval.
Sports Angle: A manager who stops rotating is telling you what he thinks of his job security.
AI Angle: Greedy policies as evidence of a low discount factor.
```

```
Idea: Your toddler is running the correct algorithm
Format: YouTube Long-form
Core Concept: Childhood as a subsidized exploration phase
Hook: Your kid can't tie their shoes, can't plan, can't focus — and is executing exactly the strategy
a well-designed algorithm would.
Best Supporting Case: Gopnik on caregivers absorbing the poor payoffs of exploration; the baby putting
every object in the house in its mouth as "studiously pulling all the handles at the casino."
Psychology Angle: The developmental deficit model, inverted.
Math Angle: Bandit algorithms explore early and exploit late; a long interval justifies heavy
exploration.
Sports Angle: Academy years as the subsidized exploration phase of a career.
AI Angle: Curriculum learning; broad low-stakes exploration before task-specific optimization.
```

```
Idea: Grandpa is right about restaurants and wrong about tonight
Format: YouTube Short
Core Concept: Information transfers across intervals; strategy doesn't
Hook: Take your grandfather's restaurant recommendations. Ignore his restaurant habits. Both are
correct.
Best Supporting Case: The chapter's own 5:00 p.m. regular.
Psychology Angle: Why intergenerational advice conflicts are structural rather than personal.
Math Angle: Optimal policy depends on interval; accumulated data does not.
Sports Angle: A veteran's read on opponents is transferable; his risk appetite isn't.
AI Angle: Transferring a learned value function without transferring the exploration schedule.
```

```
Idea: You are not the gambler. You are the jackpot.
Format: YouTube Long-form
Core Concept: A/B testing and who bears the cost of exploration
Hook: Every colour, price, and headline you saw online today was chosen by an algorithm running an
experiment on you. Google once tested forty-one shades of blue.
Best Supporting Case: The Obama DONATE button and its $57 million, against Hammerbacher's "the best
minds of my generation are thinking about how to make people click ads."
Psychology Angle: The plain black-and-white family photo beating everything the professionals produced.
Math Angle: Why the even-split A/B test is a bad bandit algorithm — half your users get the worse
option for the whole test.
Sports Angle: Testing a training protocol on half a squad all season has the same flaw.
AI Angle: Live experimentation on users; consent norms far weaker than medicine's.
```

```
Idea: The trial design that may have cost twenty-four babies
Format: YouTube Long-form
Core Concept: Adaptive clinical trials as bandit problems
Hook: Eleven infants in a row got the experimental treatment and all eleven lived. The medical
community's response was that the study was badly designed.
Best Supporting Case: The full ECMO sequence — Bartlett, Ware, Berry's published objection, and the UK
study's 24 excess deaths in the conventional arm.
Psychology Angle: Why institutions defend procedures against outcomes, and what statistics did for
medicine that made this rational.
Math Angle: Play-the-winner urn schemes; the cost of clean evidence.
Sports Angle: None identified.
AI Angle: Deploying a model you believe is better while still collecting comparison data.
Note: Handle carefully — real infant deaths, and the chapter genuinely reports expert disagreement
rather than a settled verdict. The UK study found a smaller effect, which complicates the framing.
```

```
Idea: You will never run out of regret — and that's the good news
Format: YouTube Short
Core Concept: Logarithmic regret
Hook: Math can't give you a life with no regrets. It can promise you fewer new ones every year than
the year before.
Best Supporting Case: Lai & Robbins 1985; Bezos projecting to age 80 before leaving D. E. Shaw.
Psychology Angle: Replacing an unattainable goal with an attainable rate.
Math Angle: You make as many mistakes in your first ten pulls as in the next ninety.
Sports Angle: Early-career errors as the bulk of a career's total.
AI Angle: Cumulative regret as the standard yardstick for online learning algorithms.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B01-C02-01
Title: The explore/exploit tradeoff
Type: Concept
Summary: Exploration is gathering information; exploitation is using what you know to get a known good
result. Both are neutral technical terms — never exploring is no way to live, but never exploiting
forfeits many of life's best moments (holidays with family, a band's greatest hits, "their song").
Source: Algorithms to Live By, ch. 2, "Explore/Exploit" (PDF pp. 48–49)
Tags: explore-exploit, decision-making, core-concept, framing
Related Concepts: Multi-armed bandit, interval, optimal stopping (ch. 1)
```

```
CARD ID: B01-C02-02
Title: The multi-armed bandit problem
Type: Concept
Summary: A casino of slot machines with unknown payoff rates; maximize total winnings by combining
testing and exploiting. Peter Whittle: it "embodies in essential form a conflict evident in all human
action," and was "a byword for intransigence" before Gittins.
Source: Algorithms to Live By, ch. 2 (PDF pp. 49–50, 54)
Tags: multi-armed-bandit, sequential-decision, formalism
Related Concepts: Gittins index, UCB, restless bandit, A/B testing
```

```
CARD ID: B01-C02-03
Title: The interval makes the strategy
Type: Insight
Summary: The value of exploration can only fall over time as remaining opportunities dwindle; the
value of exploitation can only rise, since today's best-known option is by definition at least as good
as last month's. Explore when you'll have time to use what you learn; exploit when you're ready to
cash in. Works in reverse too: an observed strategy reveals a perceived interval.
Source: Algorithms to Live By, ch. 2, "Seize the Interval" (PDF pp. 50–51)
Tags: interval, horizon, core-principle, revealed-preference
Related Concepts: Discounting, Carstensen, Hollywood sequels, Stucchio
```

```
CARD ID: B01-C02-04
Title: Win-Stay, Lose-Shift
Type: Model
Summary: Robbins, 1952 — pick an arm at random, keep pulling while it pays, switch on a failure.
Proved reliably better than chance. Win-stay is part of the optimal strategy across a wide range of
conditions; lose-shift is rash (one bad meal shouldn't undo a hundred good ones) and the rule has no
notion of interval.
Source: Algorithms to Live By, ch. 2, "Win-Stay" (PDF pp. 52–53)
Tags: model, heuristic, Robbins, bandit-strategy
Related Concepts: Gittins index, Zelen's play-the-winner
```

```
CARD ID: B01-C02-05
Title: The Gittins index
Type: Model
Summary: For each arm, the guaranteed payout rate that would make you content never to pull it again —
the Deal or No Deal Banker's bribe. Always play the highest index. **Under geometric discounting** it
completely solves the bandit; outside that assumption, and whenever switching between options has a
cost, it is no longer optimal. Each arm's index is computed independently so the number of arms is
irrelevant. Commissioned by Unilever in the 1970s to optimize drug trials.
Source: Algorithms to Live By, ch. 2, "The Gittins Index" (PDF pp. 54–56)
Tags: model, index-policy, Gittins, geometric-discounting, theorem
Related Concepts: UCB, expected value, Bellman
```

```
CARD ID: B01-C02-06
Title: The 0–0 exploration bonus
Type: Insight
Summary: At a 0.9 discount rate an untried arm (0–0) has an expected value of 0.5000 but a Gittins
index of 0.7029 — more attractive than a machine known to pay out seven times in ten. At 0.99
discounting it is worth a guaranteed 86.99%. Even a 0–1 record stays above 50%; 1–1 → 0.6346, 2–2 →
0.6010, converging on 0.5000 only slowly.
Source: Algorithms to Live By, ch. 2 (PDF pp. 56–58)
Tags: exploration-bonus, gittins-index, counterintuitive, uncertainty-as-asset
Related Concepts: UCB, cold start, the untested rookie
```

```
CARD ID: B01-C02-07
Title: 1–1 beats 9–6
Type: Claim
Summary: A machine played twice (one win, one loss; expected value 50%) should be chosen over one
played fifteen times (nine wins, six losses; expected value 60%) — indices 0.6346 versus 0.6300.
Expected value alone gives the wrong answer once you count future decisions.
Source: Algorithms to Live By, ch. 2 (PDF pp. 49, 56)
Tags: expected-value, gittins-index, sample-size, worked-example
Related Concepts: Exploration bonus, confidence intervals
```

```
CARD ID: B01-C02-08
Title: Geometric discounting — and its problems
Type: Concept
Summary: Valuing each future payoff at a constant fraction of the last (a 1% daily chance of being hit
by a bus justifies discounting tomorrow's dinner to 99%). It is what makes the Gittins index exactly
optimal — and the authors concede behavioral economics and psychology suggest people don't discount
this way. Switching costs also break optimality.
Source: Algorithms to Live By, ch. 2 (PDF pp. 55, 58–59)
Tags: discounting, assumption, limitation, behavioral-economics
Related Concepts: Hyperbolic discounting, the interval, RL discount factor
```

```
CARD ID: B01-C02-09
Title: Logarithmic regret
Type: Study
Summary: Lai & Robbins, 1985 — absent omniscience total regret never stops rising; it grows more
slowly under the best strategy and its growth rate declines with experience; the minimum possible
growth is logarithmic. So you make as many mistakes in your first ten pulls as in the next ninety, and
under a regret-minimizing algorithm you should have fewer new regrets each year than the year before.
Source: Algorithms to Live By, ch. 2, "Regret and Optimism" (PDF pp. 60–61)
Tags: regret, theorem, Lai-Robbins, online-learning, consolation
Related Concepts: UCB, Bezos regret minimization
```

```
CARD ID: B01-C02-10
Title: Upper Confidence Bound and optimism
Type: Model
Summary: Choose the arm whose confidence interval reaches highest — the option that *could*
reasonably be best, not the one that *has* been best. Achieves near-minimal regret, is far cheaper to
compute than Gittins, and needs no discounting assumption. Implements "optimism in the face of
uncertainty"; Kaelbling's optimistic robots explore by inflating the value of uncharted terrain.
Source: Algorithms to Live By, ch. 2, "Regret and Optimism" (PDF pp. 61–63)
Tags: model, UCB, optimism, confidence-interval, regret-minimization
Related Concepts: Gittins index, benefit of the doubt, Thompson sampling (inferred)
```

```
CARD ID: B01-C02-11
Title: Bezos's regret minimization framework
Type: Case
Summary: Deciding whether to leave a secure position at D. E. Shaw to start Amazon, Bezos projected
himself to age 80 and asked which choice minimized lifetime regret. He knew he wouldn't regret trying
and failing, but that never having tried "would haunt me every day" — which made it "an incredibly
easy decision."
Source: Algorithms to Live By, ch. 2, "Regret and Optimism" (PDF p. 60)
Tags: case, regret, entrepreneurship, decision-framework, survivorship-bias
Related Concepts: Logarithmic regret, Barnard's "inestimable loss"
```

```
CARD ID: B01-C02-12
Title: The Obama DONATE button
Type: Case
Summary: Dan Siroker took leave from Google to run New Media Analytics for the 2008 campaign and A/B
tested the donation page: $57 million in additional donations attributed (no methodology given for the
counterfactual). DONATE AND GET A GIFT won for first-time visitors even net of gift costs; PLEASE
DONATE for longtime non-donating subscribers, "perhaps appealing to their guilt"; CONTRIBUTE for prior
donors, "the logic being perhaps" that someone who has donated can always contribute more — both
explanations are the authors' hedged speculation, not findings. A plain black-and-white family photo
beat every other image or video.
Siroker later co-founded Optimizely, which by 2012 served both the Obama and Romney campaigns.
Source: Algorithms to Live By, ch. 2, "Bandits Online" (PDF pp. 63–65)
Tags: case, A/B-testing, politics, optimization, business
Related Concepts: Multi-armed bandit, forty-one shades of blue
```

```
CARD ID: B01-C02-13
Title: You're not the gambler; you're the jackpot
Type: Insight
Summary: Big tech firms began live A/B testing users around 2000, making the internet the world's
largest controlled experiment. Google tested forty-one shades of blue in 2009; in some cases no two
users have the same experience. Over 90% of Google's ~$50bn annual revenue is paid advertising, so
explore/exploit algorithms economically power a significant fraction of the internet.
Source: Algorithms to Live By, ch. 2, "Bandits Online" (PDF pp. 64–65)
Tags: A/B-testing, internet-economics, quotable, exploration-cost
Related Concepts: Hammerbacher critique, clinical trials parallel
```

```
CARD ID: B01-C02-14
Title: The Belmont Report's unresolved tension
Type: Study
Summary: Prompted by the Tuskegee Syphilis Study (1932–72, halted only after Peter Buxtun went to the
press in July 1972 after two failed internal protests), the 1979 Belmont Report concedes that "even
avoiding harm requires learning what is harmful; and, in the process of obtaining this information,
persons may be exposed to risk of harm." It acknowledges the explore/exploit tension without resolving
it.
Source: Algorithms to Live By, ch. 2, "Clinical Trials on Trial" (PDF pp. 66–67)
Tags: research-ethics, Belmont, Tuskegee, exploration-cost, history
Related Concepts: Adaptive trials, A/B testing ethics
```

```
CARD ID: B01-C02-15
Title: Zelen's play-the-winner algorithm
Type: Model
Summary: Proposed 1969, first used sixteen years later. A hat holds one ball per treatment; draw with
replacement to assign each patient. A success adds another ball for that treatment; a failure adds a
ball for the other. Allocation drifts toward whichever treatment is winning — a randomized version of
Win-Stay, Lose-Shift.
Source: Algorithms to Live By, ch. 2, "Clinical Trials on Trial" (PDF pp. 67–68)
Tags: model, adaptive-trials, urn-scheme, Zelen, medicine
Related Concepts: Win-Stay Lose-Shift, ECMO trials
```

```
CARD ID: B01-C02-16
Title: The ECMO controversy
Type: Case
Summary: Bartlett's 1982–84 Michigan trial used Zelen's algorithm: one conventional-treatment infant
died, then eleven consecutive ECMO infants survived; afterward eight of eight ECMO infants lived and
two of two conventional infants died. Ware's less radical design: four of ten conventional infants
died, nine of nine ECMO infants survived, then nineteen of twenty in phase two. Don Berry argued in
Statistical Science that even the Ware study was unethical and should not have been conducted. A 1990s
UK study of ~200 infants reverted to an even split and found a smaller effect; 24 more infants died in
the conventional group. Context that must travel with this card: ECMO is highly invasive with its own
risks including embolism, early adult studies had shown no benefit over conventional treatment, and the
chapter's own defense of the conservative position is that shared statistical standards are what ended
ad hoc persuasion in medicine.
Source: Algorithms to Live By, ch. 2, "Clinical Trials on Trial" (PDF pp. 68–70)
Tags: case, adaptive-trials, medical-ethics, ECMO, expert-disagreement, handle-with-care
Related Concepts: Zelen's algorithm, Belmont Report, FDA 2010 guidance
```

```
CARD ID: B01-C02-17
Title: People over-explore
Type: Experiment
Summary: Tversky & Edwards (1966): with a 60/40 two-light task and 1,000 opportunities, participants
averaged 505 observations and 495 bets — where the math says start betting after 38. Meyer & Shi
(1990s): the untried airline was used too little when good and too much when bad, with no clean breaks.
Steyvers, Lee & Wagenmakers (four arms, fifteen pulls): 30% optimal-like, 47% Win-Stay Lose-Shift-like,
22% random. Caveats: the 1966 design forbids learning from your own bets; the Meyer & Shi result is
two-sided, and the grounds for counting it are the failure to break cleanly rather than the misuse
itself; strategy classifications are inferred from short sequences. Direction consistent, strength
moderate.
Source: Algorithms to Live By, ch. 2, "The Restless World" (PDF pp. 70–72)
Tags: experiment, over-exploration, behavioral, calibration
Related Concepts: Premature stopping (ch. 1), restless bandit
```

```
CARD ID: B01-C02-18
Title: The restless bandit
Type: Concept
Summary: When payoff probabilities change over time the problem becomes much harder — no tractable
algorithm solves it completely, and it is believed there never will be one. Continued exploration can
therefore be correct: that disappointing restaurant may be under new management. "To live in a restless
world requires a certain restlessness in oneself." Gittins and UCB remain decent approximations if
payoffs drift slowly — and Warhol's "A Coke is a Coke" suggests modern payoffs are unusually static.
Source: Algorithms to Live By, ch. 2, "The Restless World" (PDF pp. 72–73)
Tags: non-stationarity, intractability, restless-bandit, limitation
Related Concepts: Distribution shift, Thoreau's "Walking"
```

```
CARD ID: B01-C02-19
Title: Childhood as subsidized exploration
Type: Claim
Summary: Gopnik's account of why humans take years to become competent while caribou run on day one:
extended dependence "gives you a developmental way of solving the exploration/exploitation tradeoff,"
with caregivers absorbing the poor payoffs of the exploration phase. Children look deficient on
exploit capacities (shoelaces, planning, focused attention) and excel at exactly what exploration
requires. A baby mouthing every object is "studiously pulling all the handles at the casino."
Source: Algorithms to Live By, ch. 2, "Explore …" (PDF pp. 73–75)
Tags: development, Gopnik, exploration, lifespan, reframing
Related Concepts: Curriculum learning, the interval, neoteny
```

```
CARD ID: B01-C02-20
Title: Carstensen — social networks shrink by choice
Type: Study
Summary: Network shrinkage in age comes from deliberately pruning peripheral ties to focus on a core
of close friends and family, not from decline. In the Carstensen & Fredrickson choice task older
people chose an immediate family member while young people were equally drawn to a book's author or a
new acquaintance — but young people imagining a cross-country move chose family too, and older people
imagining a twenty-year medical breakthrough became indistinguishable from the young. Older adults
also report higher satisfaction and often higher emotional well-being.
Source: Algorithms to Live By, ch. 2, "… And Exploit" (PDF pp. 75–77)
Tags: study, aging, socioemotional-selectivity, interval, experiment
Related Concepts: The interval, life should get better over time
```

```
CARD ID: B01-C02-21
Title: Life should get better over time
Type: Insight
Summary: Exploration necessarily disappoints most of the time, because Gittins and UCB inflate the
appeal of unknowns beyond what we actually expect. Shifting attention toward favorites should
therefore raise quality of life — and Carstensen finds older adults do report higher emotional
well-being. There is a lot to look forward to in being the late-afternoon restaurant regular.
Source: Algorithms to Live By, ch. 2, "… And Exploit" (PDF p. 77)
Tags: aging, exploitation, well-being, optimistic-conclusion
Related Concepts: Exploration bonus, Carstensen, the interval
```

```
CARD ID: B01-C02-22
Title: Listen to grandpa's data, not his policy
Type: Insight
Summary: When your grandfather tells you which restaurants are good, listen — those are pearls from
decades of searching. When he only goes to the same one at 5:00 p.m. daily, explore freely, even
though your alternatives will likely be worse. Accumulated information transfers across intervals;
optimal strategy does not.
Source: Algorithms to Live By, ch. 2, "… And Exploit" (PDF p. 77)
Tags: interval, advice, intergenerational, actionable
Related Concepts: The interval makes the strategy, exploitation in age
```

```
CARD ID: B01-C02-23
Title: Hollywood's sequels reveal a short interval
Type: Case
Summary: Sequels among the top ten highest-grossing films: 2 (1981), 3 (1991), 5 (2001), 8 (2011),
with the share record broken in 2011, 2012 and 2013. Studio profits fell 40% between 2007 and 2011 and
ticket sales declined in seven of ten years. A pure-exploit posture signals a belief that the interval
is nearly over — pulling the best arms before the casino turns you out.
Source: Algorithms to Live By, ch. 2, "Seize the Interval" (PDF pp. 51–52)
Tags: case, business, interval, short-termism, revealed-strategy
Related Concepts: The interval makes the strategy, Stucchio
```

```
CARD ID: B01-C02-24
Title: Exploration is a cost someone else often pays
Type: Insight
Summary: Three faces of one unnamed idea: "journalists are martyrs, exploring so that others may
exploit" (Plagenhoef loading only new music onto his iPod); "you're not the gambler; you're the
jackpot" (A/B tested users); and the control arm of a clinical trial. The chapter never names the
pattern, but the distribution of exploration's costs and benefits across different people is the
thread linking its three applied sections.
Source: Algorithms to Live By, ch. 2, "Explore/Exploit," "Bandits Online," "Clinical Trials on Trial"
(PDF pp. 49, 65, 66–70)
Tags: exploration-cost, ethics, synthesis, inferred-pattern
Related Concepts: Belmont Report, Hammerbacher, A/B testing
```

```
CARD ID: B01-C02-25
Title: Pirsig's "What's best?" and the authors' rebuttal
Type: Claim
Summary: Robert Pirsig (*Zen and the Art of Motorcycle Maintenance*, 1974) attacked "What's new?" as
producing "an endless parade of trivia and fashion, the silt of tomorrow," and endorsed "What's best?"
The authors reply that every "best" among your favorites began as something merely "new" to you, so
yet-unknown bests may still be out there. Pure exploitation is self-undermining — you can only exploit
what exploration found.
Source: Algorithms to Live By, ch. 2, opening (PDF p. 47)
Tags: disagreement, Pirsig, cross-book, founding-argument, exploration
Related Concepts: Explore/exploit tradeoff, filter bubbles, exploration bonus
```

```
CARD ID: B01-C02-26
Title: Inherited wisdom encodes an interval
Type: Insight
Summary: "Carpe diem" and "eat, drink, and be merry, for tomorrow we die" are advice for a short
interval; the authors propose the inverse for a long one — "start learning a new language or an
instrument, and make small talk with a stranger, because life is long, and who knows what joy could
blossom over many years' time." Seizing a day and seizing a lifetime are entirely different endeavors.
Lydia Davis states the same dilemma from the inside: keep reading new books, or reread the ones that
gave the most pleasure?
Source: Algorithms to Live By, ch. 2, "Seize the Interval" and epigraph to "… And Exploit" (PDF pp. 50,
75)
Tags: interval, aphorism, quotable, reframing, literature
Related Concepts: The interval makes the strategy, Carstensen, Stucchio
```

```
CARD ID: B01-C02-27
Title: Statistics as a shared standard of persuasion
Type: Claim
Summary: The chapter's own steelman for conventional trials: statistics transformed medicine at the
start of the twentieth century "from a field in which doctors had to persuade each other in ad hoc
ways about every new treatment into one where they had clear guidelines about what sorts of evidence
were and were not persuasive." Changing accepted practice risks upsetting that balance, at least
temporarily — so resistance to adaptive designs is a defense of a coordination device, not mere
obstinacy.
Source: Algorithms to Live By, ch. 2, "Clinical Trials on Trial" (PDF p. 70)
Tags: research-methods, institutions, steelman, evidence-standards, balance
Related Concepts: ECMO controversy, adaptive trials, benchmarks in AI (inferred)
```

```
CARD ID: B01-C02-28
Title: Evolutionary mismatch — the berry patch and the Coke
Type: Insight
Summary: "A berry patch might be ripe one week and rotten the next, but as Andy Warhol put it, 'A Coke
is a Coke.'" Ancestral environments were restless bandits with drifting payoffs; many modern payoffs
are standardized and stationary. "Having instincts tuned by evolution for a world in constant flux
isn't necessarily helpful in an era of industrial standardization" — our exploration instincts may be
calibrated to the wrong problem class.
Source: Algorithms to Live By, ch. 2, "The Restless World" (PDF p. 73)
Tags: evolutionary-mismatch, non-stationarity, restless-bandit, instincts
Related Concepts: Restless bandit, over-exploration, industrial standardization
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: The choice between the new and the familiar is the multi-armed bandit problem, and its
answer is governed by the interval over which you can use what you learn. Optimal algorithms give
untried options a systematic bonus, making optimism mathematically rational, and the same structure
governs A/B tests, clinical trials, childhood, and old age.

Top 5 Concepts:
1. The explore/exploit tradeoff
2. The multi-armed bandit problem
3. The interval ("the interval makes the strategy")
4. The Gittins index and the exploration bonus
5. Regret minimization and Upper Confidence Bound / optimism under uncertainty

Top 3 Claims:
1. The value of exploration only falls with time and the value of exploitation only rises, so interval
   determines strategy — demonstrated experimentally in both directions by Carstensen.
2. A completely untried option can be worth more than a known 70% performer (Gittins index 0.7029 for
   a 0–0 record), so preferring the unknown is rational, not naive.
3. The minimum achievable regret grows only logarithmically, so a good strategy yields fewer new
   regrets each year than the last.

Top 3 Cases:
1. The ECMO trials — adaptive versus conventional design with infant lives as the payoff
2. Stucchio's restaurants in Pune and New York — the interval visible in one person's behavior
3. The Obama DONATE button and its $57 million (with Hammerbacher's "best minds" line as counterweight)

Top 3 Studies:
1. Carstensen & Fredrickson's companion-choice experiment with bidirectional interval manipulation
2. Tversky & Edwards, 1966 — 505 observations where 38 sufficed
3. Lai & Robbins, 1985 — the logarithmic regret bound

Most Unique Idea: That an observed explore/exploit ratio discloses the actor's perceived remaining
interval — so Hollywood's sequel deluge, a grandfather's fixed dinner hour, and an older adult's
smaller social circle are all readable as the same statement about time.

Most Counterintuitive Idea: An option you know nothing about can be strictly more attractive than one
you know to be good — the exploration bonus makes "the grass is greener" a correct inference rather
than a cognitive error.

Biggest Weakness or Open Question: The chapter reports that people over-explore — on an evidence base
thinner than the claim's prominence suggests — and then urges readers to explore more, without stating
the reconciliation. It concedes that its central result depends on geometric discounting, which it says
people don't do, and on the absence of switching costs, which its own examples all have, while the
realistic non-stationary case is declared permanently intractable on no cited authority. The
clinical-trial argument, its most consequential, rests on very small studies whose largest replication
found a smaller effect. And the chapter opens with a vivid description of decision fatigue that it
then never models: exploration's cost is treated throughout as forgone payoff, never as depletion.

Named Disagreements (for the book profile): Robert Pirsig, *Zen and the Art of Motorcycle Maintenance*
— the chapter's only explicit argument against a named author.

Best Content Opportunity: A long-form video on the exploration bonus built around the Gittins table's
top-left cell (0.7029 beating a known 70% machine) and the Unilever origin story, landing on optimism
as a provably rational disposition rather than a temperament.
```
