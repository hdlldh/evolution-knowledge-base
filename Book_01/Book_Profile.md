# Book Profile — Algorithms to Live By: The Computer Science of Human Decisions
**Author:** Brian Christian and Tom Griffiths
**Type:** Book Profile (Stage 3 synthesis)
**Source:** Synthesized from the English chapter extractions (Chapters 1–11 + Conclusion) in Book_01/
**Date:** 2026-07-22

```
BOOK:
Algorithms to Live By: The Computer Science of Human Decisions

AUTHOR:
Brian Christian and Tom Griffiths
```

---

## 1. Core Thesis

The fundamental problems of human decision-making are *computational* in nature — any agent bound by
limited space, limited time, and incomplete information faces the same core challenges — so the
algorithms computer science developed for machines are directly transferable guides for living. The book
argues three things at once: (1) specific algorithms port straight onto human problems (when to stop
looking, when to try something new, how much to sort, what to keep, how to schedule, how to predict, how
much to model, when to relax a problem, when to use chance, how to coordinate); (2) knowing the *optimal
process* brings relief even when the *outcome* is bad, because even the best algorithm often fails; and
(3) most profoundly, bounded rationality — making assumptions, favoring simplicity, using randomness,
trading error against delay, settling for "good enough" — is not a concession we make when we can't be
rational; it is *what being rational actually means*. The closing turn from computation to ethics —
**computational kindness** — extends the whole project: because interacting with others hands them hard
computational problems, we should design requests, choices, and environments to minimize the labor of
thought.

## 2. Argument Structure

The book moves outward in three concentric rings.

**Ring 1 — problems the world poses to a single mind (chs. 1–5).** It opens with the cleanest cases,
where the enemy is the structure of reality and our limited capacity, not other people. *Optimal
stopping* (ch. 1) is the irreversibility of time; *explore/exploit* (ch. 2) is time's limited supply;
*sorting* (ch. 3) and *caching* (ch. 4) are the costs of order and memory; *scheduling* (ch. 5) is the
management of time itself. These chapters establish the book's signature move — a named CS problem, a
provably optimal (or best-known) algorithm, and a translation to daily life — and its recurring humbling
lesson: the optimal amount of effort is often surprisingly *low* (err on the side of messiness; do the
shortest job; don't over-sort).

**Ring 2 — problems of prediction and intractability (chs. 6–9).** The argument escalates from *acting*
to *knowing*. *Bayes's Rule* (ch. 6) shows how to predict from tiny data given the right prior;
*overfitting* (ch. 7) warns that more data and more thinking can make you worse; *relaxation* (ch. 8)
confronts problems no computer can solve perfectly; *randomness* (ch. 9) shows that when reasoning fails,
chance succeeds. Here the book's tone shifts from "here's the optimal answer" to "here's why there often
*is* no computable optimal answer — and why that's fine." This is the philosophical hinge: complexity,
not truth, is the object of study, and "good enough" becomes a rigorous, not lazy, standard.

**Ring 3 — problems we pose each other (chs. 10–11).** The focus turns to interaction. *Networking* (ch.
10) treats communication protocols — and finds in them an ethics of forgiveness (exponential backoff) and
a diagnosis of modern overload (bufferbloat, "always buffered"). *Game theory* (ch. 11) treats strategy —
recursion, bad equilibria, and the redesign of games so honesty wins. The **Conclusion** gathers
everything into three pieces of wisdom and the ethical bridge of computational kindness, then delivers the
redemptive thesis: cutting corners *is* rationality.

The argument thus escalates from "the world is hard" → "knowledge is hard" → "other people are hard," and
across all three it repeatedly *lowers* the bar we should hold ourselves to, reframing that lowering not
as defeat but as wisdom.

## 3. Major Concepts

```
Concept: Optimal stopping and the explore/exploit tradeoff (the economics of time)
Definition: When to commit to a choice (37% Rule) and how to balance the new against the known (bandit
problems), governed by how long you can use what you learn ("the interval").
Importance to the Book: The opening and defining pair; establishes that time's irreversibility and
scarcity structure decision-making, and that failure rates are properties of the problem, not of you.
Key Chapters: 1, 2 (recurs in the Conclusion's "37% Rule / UCB" transferables).
Related Concepts: The interval, regret minimization, computational Stoicism.
```

```
Concept: Bounded rationality as real rationality ("good enough" / process over outcome)
Definition: Under real constraints, the rational act is to make assumptions, prefer simpler solutions,
use chance, and trade the cost of error against the cost of delay — not to optimize exhaustively.
Importance to the Book: The book's overarching thesis, stated explicitly in the Conclusion but enacted in
every chapter (err on the side of messiness; shortest job first; think less; relax the problem).
Key Chapters: Conclusion, 1, 5, 7, 8, 9 (nearly all).
Related Concepts: Intractability, overfitting, relaxation, computational Stoicism, satisficing.
```

```
Concept: Intractability and the tractable/intractable line
Definition: Many real problems (TSP, scheduling, finding Nash equilibria) admit no efficient exact
solution; "math studies truth, CS studies complexity." Alias: NP-hardness, combinatorial explosion.
Importance to the Book: The structural reason "good enough" is mandatory, not optional; it links
scheduling (ch. 5), relaxation (ch. 8), randomness (ch. 9), and game theory (ch. 11: "if your laptop
cannot find it, neither can the market").
Key Chapters: 5, 8, 9, 11.
Related Concepts: Relaxation, randomized algorithms, price of anarchy, Cobham–Edmonds thesis.
```

```
Concept: Priors and the right model (Bayesian prediction; overfitting; regularization)
Definition: Good prediction depends more on the right prior/distribution than on data volume; a model
tuned too finely to available data generalizes terribly (overfitting), curable by penalizing complexity.
Importance to the Book: The knowledge-side core; unifies "small data is big data in disguise" (ch. 6) with
"more data/thinking can hurt" (ch. 7) — two sides of getting the model right.
Key Chapters: 6, 7.
Related Concepts: Idolatry of data / proxy metrics, less-is-more, the Lasso, Goodhart's law.
```

```
Concept: Caching, memory, and forgetting as optimization (not decay)
Definition: Minds and machines are caching hierarchies; the best practical rule is LRU (recent past
predicts near future), and human forgetting is memory optimally tuned to a world that itself forgets on
the same curve.
Importance to the Book: The most emotionally resonant reframe — "cognitive decline" as the retrieval cost
of an ever-growing, well-tuned memory.
Key Chapters: 4 (LRU recurs in the Conclusion's transferables).
Related Concepts: The forgetting curve, temporal locality, self-organizing lists.
```

```
Concept: Randomness as a deliberate tool
Definition: Sampling (Monte Carlo), randomized checking (Miller-Rabin), and tactical randomness (jitter,
restarts, the Metropolis Algorithm, simulated annealing) solve problems reasoning can't — and reveal
certainty as a third resource tradeable against time and space.
Importance to the Book: The turning point where chance stops being "giving up" and becomes optimal; also
the mechanism (breaking symmetry) that makes networking possible.
Key Chapters: 9 (feeds 10's exponential backoff).
Related Concepts: Simulated annealing, error probability, escaping local maxima, the three life-rules.
```

```
Concept: Coordination — protocol, forgiveness, and game theory
Definition: How agents connect (packet switching, acknowledgment, exponential backoff, AIMD) and compete
(recursion, Nash equilibrium, prisoner's dilemma, mechanism design).
Importance to the Book: The outermost ring — the problems we pose each other; yields the humane
"algorithm of forgiveness" and the redesign of games so honesty is dominant.
Key Chapters: 10, 11.
Related Concepts: Exponential backoff, mechanism design, information cascades, computational kindness.
```

```
Concept: Computational kindness (the bridge to ethics)
Definition: Because interacting with others (and designing their environments) imposes hard computational
problems on them — above all simulating our minds — we should minimize the labor of thought we create.
Importance to the Book: The book's original contribution and moral payoff; turns the whole framework into
a design and behavioral ethic.
Key Chapters: Conclusion (draws on ch. 11's "simulating other minds" and ch. 1's optimal stopping).
Related Concepts: Verification vs. search, spinning vs. blocking, cognitive load.
```

## 4. Major Claims

```
Claim: Bounded, corner-cutting rationality is what rationality actually is — not a concession.
Evidence: The whole book: 37% Rule's 63% failure being a property of the problem; SPT and relaxation and
sampling as optimal responses to intractability; the Conclusion's explicit statement.
Confidence: High as the book's synthesizing thesis (interpretive, but well-supported by the cumulative
results).
Potential Criticism: "Rational" is being redefined mid-argument; a critic could say the book relabels
heuristics as optimality without always proving the heuristic is optimal for the real objective.
```

```
Claim: Many everyday problems have a known optimal algorithm you can simply adopt.
Evidence: The 37% Rule (optimal stopping), LRU (caching), Upper Confidence Bound (explore/exploit),
Earliest Due Date and weighted Shortest Processing Time (scheduling).
Confidence: High for the named algorithms within their stated assumptions.
Potential Criticism: The clean optimality holds only under idealized assumptions (no switching costs,
known distributions, a single objective) that the book's own examples routinely violate.
```

```
Claim: Getting the prior/model right matters more than having more data — and more data or thinking can
hurt.
Evidence: Single-point Bayesian prediction (ch. 6); overfitting and the nine-factor marriage model,
Markowitz's 50/50 split, "less-is-more" (ch. 7).
Confidence: High within the book; the two chapters reinforce each other.
Potential Criticism: The book can't operationalize "the right prior" or "the right complexity" for a
novel problem — it diagnoses the failure better than it prevents it.
```

```
Claim: Some problems are intractable, so the rational response is to relax, approximate, or randomize.
Evidence: TSP and wedding seating (~11¹⁰⁷ plans); 84% of scheduling problems intractable; finding Nash
equilibria intractable; Monte Carlo and Miller-Rabin.
Confidence: High (with the honest caveat that P vs. NP is open, so "permanently hard" is belief, not
proof).
Potential Criticism: Rests on the unproven assumption that hard problems stay hard; and gives no general
rule for which relaxation/approximation to use on a novel problem.
```

```
Claim: The stable outcome of rational self-interest can be terrible for everyone — fix it by changing the
game, not the strategy.
Evidence: The prisoner's dilemma and tragedy of the commons; the price of anarchy; mechanism design (the
Godfather; compulsory vacation; the Vickrey auction).
Confidence: High for the game-theoretic results; interpretive for the social prescriptions.
Potential Criticism: The prisoner's dilemma may over-represent human conflict (Binmore: it "loads the
dice against cooperation"); mechanism design assumes a benevolent, powerful designer.
```

```
Claim: We can be "computationally kind" — minimizing the cognitive load we impose on others is a genuine
ethic and design principle.
Evidence: The scheduling paradox (constrained > open requests); "I'm flexible" as passing the cognitive
buck; the 18-cent coin; helix parking; spinning vs. blocking.
Confidence: Moderate–High; a compelling, well-illustrated bridge, explicitly offered as analogy rather
than proven law.
Potential Criticism: The line between kind constraint and autonomy-overriding imposition is unspecified.
```

```
Claim: Forgetting and "cognitive decline" are largely optimization, not decay.
Evidence: LRU as best practical eviction; Anderson & Schooler's curve-matching; Ramscar on aging as
retrieval cost of a larger store.
Confidence: Moderate; inferred from curve-matching on a few corpora, and hedged ("at least partly").
Potential Criticism: Real neurological aging exists and isn't measured; the ecological story is
suggestive, not demonstrated.
```

## 5. Core Frameworks and Models

- **The 37% Rule / Look-Then-Leap vs. Threshold Rule** (ch. 1) — optimal stopping; explore a fixed
  fraction, then take the next best-yet.
- **The interval, the Gittins index, and Upper Confidence Bound / "optimism"** (ch. 2) — explore/exploit;
  give untried options a systematic bonus; minimize regret (which grows only logarithmically).
- **Big-O complexity and the search–sort tradeoff** (ch. 3) — sort only to make future search cheaper;
  ordinal→cardinal ("a race instead of a fight").
- **The memory hierarchy, Bélády's optimum, and LRU** (ch. 4) — caching; the recent past predicts the
  near future; the pile is near-optimal.
- **Choose-a-metric-first, EDD, weighted SPT, and context-switch→thrashing→interrupt-coalescing** (ch. 5)
  — single-machine scheduling.
- **Bayes's Rule, Laplace's Law, the Copernican Principle, and the three prediction rules
  (Multiplicative / Average / Additive)** (ch. 6) — prediction from small data; distribution shape sets
  the rule.
- **Cross-validation, regularization / the Lasso, and early stopping** (ch. 7) — combat overfitting;
  penalize complexity.
- **The three relaxations — Constraint, Continuous (round), Lagrangian (penalize)** (ch. 8) — make
  intractable problems tractable; get a lower bound and a "within X%" guarantee.
- **Monte Carlo sampling, Miller-Rabin, hill climbing, the Metropolis Algorithm, and simulated
  annealing** (ch. 9) — randomness; front-load it, then cool down (the three life-rules).
- **Packet switching, ACKs, exponential backoff, and AIMD / the TCP sawtooth** (ch. 10) — networking; the
  "algorithm of forgiveness"; push to failure then halve.
- **Recursion/leveling, Nash equilibrium, the prisoner's dilemma, the price of anarchy, mechanism design,
  and the Vickrey auction / revelation principle** (ch. 11) — game theory.
- **The three pieces of wisdom, computational kindness, and spinning vs. blocking** (Conclusion).

## 6. Strongest Research Evidence

Studies the book leans on structurally (not just once):

- **The mathematical results themselves** — the 1/e (37%) optimal-stopping result; Lai & Robbins's (1985)
  logarithmic regret bound and the Gittins index; Bélády (1966) and Sleator & Tarjan (1985, within 2× of
  clairvoyance); Selmer Johnson (1954, first optimal scheduling algorithm); the Lasso (Tibshirani, 1996)
  and Tikhonov regularization; Nash's existence theorem (1951) and Papadimitriou et al. (2005–2008,
  intractability of finding equilibria); Roughgarden & Tardos (2002, price of anarchy 4/3). These
  provably-optimal or provably-hard results are the book's evidentiary backbone and are its strongest
  ground.
- **The ecological-rationality studies** — Anderson & Schooler (forgetting curve mirrors the world's decay
  statistics) and Griffiths & Tenenbaum (people match Bayesian single-point prediction) — used to argue
  human cognition is well-tuned, not flawed.
- **The behavioral decision studies** — Rapoport & Seale (1990s, repeated secretary problems, ~31%
  success, premature leaping); Carstensen & Fredrickson (bidirectional interval manipulation);
  Tversky & Edwards (1966, 505 observations where 38 sufficed).
- **The applied/engineering evidence** — the 1986 Berkeley congestion collapse → AIMD; the HOPE probation
  program (5-year DOJ study); Shallit's optimal-denomination analysis (2003).

The weakest links are the behavioral/psychological claims that ride on small studies or post-hoc fits
(Seale & Rapoport's cost-adjusted reanalysis; the ECMO clinical-trial argument on very small samples; the
forgetting-is-optimal inference from three idiosyncratic corpora; the unattributed penguin/terrorism
scope-insensitivity examples in the Conclusion).

## 7. Best Experiments

- **The Luria fluctuation test** (ch. 9) — bacterial-resistance distributions (uniform = reaction vs.
  jackpot-uneven = random mutation) show that the *shape* of an outcome reveals its mechanism; a Nobel
  discovery *about* and *due to* chance.
- **Carstensen & Fredrickson's companion-choice experiment** (ch. 2) — manipulating the perceived interval
  in both directions flips explore/exploit behavior, grounding "the interval makes the strategy."
- **Rapoport & Seale's repeated secretary problems** (ch. 1) — people leap prematurely in >80% of trials
  (~31% success), the empirical anchor for "we stop too early — or do we?"
- **Bavelas's distracted-listener study** (ch. 10) — poor feedback makes a story fall apart at its climax:
  "a poor listener destroys the tale."
- **The $23.7M textbook** (ch. 11) — two Amazon pricing algorithms with no ceiling, a real-world
  information cascade / feedback runaway.
- **Nakamura vs. Rybka** (ch. 11) — a grandmaster beats a chess engine by baiting it into fruitless
  recursion (deliberately meaningless moves).

## 8. Best Cases and Stories

Ranked by combined teaching / storytelling / content / cross-domain value (all High unless noted):

1. **Kepler's eleven courtships** (ch. 1) — optimal stopping made human; a scientist agonizing over the
   37% Rule three centuries before it existed. *Teaching: High · Story: High · Content: High · Reuse:
   High.*
2. **The prisoner's dilemma + the Godfather** (ch. 11) — the single most load-bearing game, plus the
   counterintuitive fix (worsen every payoff to help everyone). *All High.*
3. **The $23.7M fly-biology textbook / the 2010 flash crash** (ch. 11) — information cascades; catastrophe
   with no one at fault. *All High.*
4. **HOPE probation** (ch. 10) — exponential backoff as the "algorithm of forgiveness" in criminal
   justice (rearrests halved, drug use −72%). *All High.*
5. **Stan Ulam's solitaire → the Monte Carlo Method → the atom bomb** (ch. 9) — a convalescent's card game
   becomes a pillar of science. *All High.*
6. **The 18-cent coin** (Conclusion) — the mathematically optimal design is the cognitively cruelest.
   *Teaching: High · Reuse: High.*
7. **"The silver medal is a lie" — Dodgson/Lewis Carroll's 1883 tennis proof** (ch. 3) — Single
   Elimination reveals only the winner; noise makes even gold unreliable. *All High.*
8. **Your messy desk is near-optimal — Noguchi + Sleator-Tarjan** (ch. 4) — the pile within 2× of
   clairvoyance; the vindicated mess. *All High.*
9. **Stephen Jay Gould's cancer** (ch. 6) — median vs. distribution shape; the Multiplicative Rule and
   "twenty more years." *Teaching/Story: High.*
10. **Meghan Bellows's wedding seating** (ch. 8) — ~11¹⁰⁷ plans solved with protein-design optimization;
    intractability made vivid. *All High.*
11. **Mars Pathfinder's priority inversion** (ch. 5) — a spacecraft nearly lost to a scheduling bug;
    "important things first" can look like procrastination. *Teaching: High.*
12. **The ECMO trials** (ch. 2) — adaptive vs. conventional design with infant lives as the payoff; the
    ethics of explore/exploit. *Story: High.*
13. **Kleinrock vs. AT&T ("Little boy, go away")** (ch. 10) — the birth of packet switching. *Story:
    High.*
14. **Kirkpatrick's simulated annealing beats the IBM chip-layout "guru"** (ch. 9) — front-load
    randomness, cool down; openness beats hoarding. *Teaching: High.*
15. **Brian's phantom-consensus bullfight** (Conclusion) — three friends each adopt the others' perceived
    enthusiasm for a bullfight none wanted; computational unkindness of "I'm flexible." *All High.*

## 9. Recurring Themes

- **The optimal amount of effort is surprisingly low.** Err on the side of messiness (3), don't
  over-organize memory (4), do the shortest job (5), think less / simplify (7), relax the problem (8),
  "good enough" (Conclusion). The book repeatedly argues *against* thoroughness.
- **Process over outcome.** Even optimal strategies fail often (37% Rule fails 63%; LRU no guarantee; UCB
  only slows regret) — judge the process (chs. 1, 2, 4; crystallized as "computational Stoicism" in the
  Conclusion).
- **Intractability is the norm, and the response is to bend the problem.** Scheduling (5), relaxation (8),
  randomness (9), game theory (11) — "consciously driven wishful thinking."
- **Randomness and ignorance can beat reasoning and foreknowledge.** Clairvoyance as burden (5), sampling
  beats analysis (9), first instinct beats deliberation (7), guess instead of plan (5).
- **The right model/prior matters more than more data.** Chs. 6 and 7 are mirror images (too little vs.
  too much model).
- **Human cognition is well-tuned, not broken.** Ecological rationality: forgetting (4), intuitive
  Bayesianism (6), less-is-more (7), rational early-stopping (1).
- **Constraints and "baggage" are protective.** Regularization by tradition, biology, and law (7); rules
  as robustness; religion and mechanism design as beneficial constraint (11).
- **The recurring cast of characters.** Merrill Flood (chs. 1, 8, Conclusion), Michael Trick (chs. 1, 3,
  8), von Neumann (chs. 3, 4, 9), and Laplace (chs. 6, 9) thread through the book, signaling how the same
  handful of ideas and people underlie disparate domains.

## 10. Unique Ideas

(Distinctive framings this book foregrounds; not claims of global originality.)

- **"Small data is big data in disguise"** (ch. 6) — human predictive skill as rich, unconsciously
  absorbed priors.
- **Human forgetting as optimal ecological tuning** (ch. 4) — the Ebbinghaus curve as a match to the
  world's own decay statistics.
- **"Idolatry of data"** and nature/brains/tradition as "Lassos" (ch. 7) — regularization operating across
  biology and culture.
- **"Relax the problem, not yourself"** and the epistemics of knowing how close you are to an answer you
  can never compute (ch. 8).
- **The three life-rules for randomness** and "emotion is mechanism design in the species" (chs. 9, 11).
- **"Finite patience and infinite mercy"** — exponential backoff as an algorithm of forgiveness (ch. 10).
- **"We're not always connected; we're always buffered"** (ch. 10) — overload as a queuing problem.
- **"If your laptop cannot find it, neither can the market"** (ch. 11) — computational tractability as a
  precondition for economic prediction.
- **Computational kindness and the "cognitive subsidy"** (Conclusion) — an ethics derived from complexity
  theory.
- **Ordinal→cardinal as a violence-avoidance technology** (ch. 3) — shared benchmarks that turn fights
  into races.

## 11. Counterintuitive Insights

Ranked by strength:

1. **Cutting corners is what rationality *is*, not a failure of it** (Conclusion) — the book's redemptive
   reframe.
2. **Your success rate at finding the best option is 37% whether the pool is 100 or a million** (ch. 1) —
   the algorithm gets *more* valuable as search grows.
3. **A bigger buffer / more memory can make things worse** (ch. 10, bufferbloat) and **more data/thinking
   can make decisions worse** (ch. 7, overfitting).
4. **Making every outcome worse can make everyone better off** (ch. 11, mechanism design) — and being
   reliably "irrational" (costly revenge, helpless love) is a rational, population-level advantage.
5. **You can settle a strictly yes/no question (is this prime?) by rolling dice**, faster than reasoning
   (ch. 9) — and "probably prime" secures the internet.
6. **An option you know nothing about can be strictly better than a known good one** (ch. 2) — the
   exploration bonus makes "the grass is greener" a correct inference.
7. **"Cognitive decline" may be learning** (ch. 4) — a slower lookup is a measure of how much you know.
8. **You should often deliberately not sort** (ch. 3) — mess can be optimal; and the "worst" sort becomes
   best under noise.
9. **Being "polite" (saying "I'm flexible") is computationally cruel** (Conclusion) — it forces others to
   simulate your mind.
10. **Consuming more news can make your predictions worse** (ch. 6) — media frequency corrupts priors.

## 12. Internal Tensions

- **"Explore more" vs. "people over-explore."** Ch. 2 reports that people explore too much *and* urges
  readers to explore more, without stating the reconciliation.
- **"Human cognition is well-tuned" vs. "your priors are corrupted / you leap too early."** The book
  praises humans as intuitive Bayesians and ecologically rational (chs. 4, 6, 7) while also documenting
  systematic errors (premature stopping in ch. 1; media-distorted priors in ch. 6). It notes but doesn't
  resolve this.
- **"Optimal algorithm" vs. its own violated assumptions.** Clean optima (37% Rule, weighted SPT,
  Gittins) assume no switching costs, known distributions, and a single objective — assumptions the
  book's own examples routinely break (ch. 2 concedes its result depends on geometric discounting "people
  don't do"; ch. 5's SPT vs. minimum-slice tension).
- **Simplicity vs. the missing sweet-spot rule.** Ch. 7 leans hard toward "simplify / think less" without
  an equally sharp warning about underfitting or a concrete method (beyond cross-validation) for locating
  the complexity sweet spot; ch. 8 similarly gives no general rule for which relaxation to use.
- **"Never look back" vs. Kepler's fallback.** Ch. 1 gives directly opposed prescriptions on revisiting
  past options without stating the condition that separates them.
- **Randomness as optimal vs. "push to failure."** Ch. 9's "temper yourself" and ch. 10's AIMD both
  advocate courting failure — sound where failure is cheap (a dropped packet), reckless where it isn't;
  the boundary is left implicit.

## 13. Potential External Disagreements

- **vs. classical/rational-choice economics.** The book's "if your laptop cannot find it, neither can the
  market" (ch. 11) and its bounded-rationality thesis directly challenge equilibrium-based, fully-rational
  models. Opposing position: efficient-markets / rational-expectations economics.
- **vs. Kahneman–Tversky heuristics-and-biases.** The book leans toward *ecological rationality*
  (Gigerenzer's camp — humans as well-adapted, less-is-more) over the "flawed heuristics" reading, though
  it uses biases findings too. Opposing position: the heuristics-and-biases tradition treating deviations
  as errors.
- **vs. Chomskyan linguistics.** Ch. 10 explicitly favors the backchannel/collaborative view of language
  over Chomsky's idealized, feedback-free competence.
- **vs. "big data" maximalism.** Chs. 6–7 ("small data is big data in disguise"; more data can hurt)
  oppose the more-data-is-always-better ethos. Opposing position: data-maximalist ML/analytics culture.
- **vs. Kant's categorical imperative.** Ch. 11's footnote holds the prisoner's dilemma "obliterates"
  Kantian rationality (the categorical-imperative outcome is better but unstable).
- **vs. Robert Pirsig** (*Zen and the Art of Motorcycle Maintenance*) — ch. 2's one explicit argument
  against a named author, on the value of exploration/quality.

## 14. Weaknesses and Limitations

- **Evidence quality is uneven.** The mathematical results are ironclad, but many behavioral bridges rest
  on small studies, post-hoc fits, or (in the Conclusion) unattributed "celebrated studies" (penguins,
  terrorism). The ECMO clinical-trial argument leans on very small samples with a weaker largest
  replication; forgetting-is-optimal is inferred from curve-matching on three idiosyncratic corpora.
- **Replication-era caution.** Several psychology hooks (the marshmallow test — reinterpreted but still
  invoked; decision fatigue, mentioned then never modeled; scope-insensitivity) touch findings that have
  faced replication scrutiny. The book's reinterpretations are often sound, but the underlying studies
  should be flagged.
- **Generalizability.** Clean algorithmic optima hold under idealized assumptions the real world violates
  (no switching costs, known distributions, single objectives, cheap failure). The book is candid about
  this in places but still ports the tidy rule to messy life.
- **Prescriptive gaps.** Repeatedly diagnoses better than it prescribes: no general rule for the right
  prior (6), the complexity sweet spot (7), which relaxation to use (8), how much randomness for a life
  (9), or where kind constraint becomes imposition (Conclusion).
- **Causal reasoning.** The ecological-rationality claims (forgetting, intuitive Bayes) are correlational
  curve-matching presented as near-explanatory; "decline is learning" is hedged to "at least partly."
- **Selection of examples.** Vivid cases carry heavy argumentative load; the book sometimes generalizes
  from a single striking anecdote (Berezovsky, the desk pile, the phantom bullfight).

## 15. Psychology Connections

**Direct (the book makes them):** ecological rationality and intuitive Bayesianism (6); the interval and
socioemotional selectivity across the lifespan (2); memory, forgetting, and "cognitive decline" (4);
decision fatigue and procrastination/pre-crastination (5); outcome bias vs. process (1, Conclusion);
theory of mind and recursion (11); emotions as commitment devices, attachment, and love (11); herd
behavior and information cascades (11); acknowledgment anxiety and active listening (10); cognitive load,
choice overload, and self-compassion (Conclusion).

**Inferred (mine):** the whole book is a de facto treatise on *bounded rationality* and *ecological
rationality* (Simon, Gigerenzer); "computational Stoicism" links directly to Stoic and CBT process-focus;
computational kindness is choice architecture / nudge-adjacent; the explore/exploit and regularization
material connects to curiosity, wisdom-with-age, and the psychology of expertise.

## 16. Mathematics and Decision Science Connections

**Direct:** optimal stopping and the 1/e law (1); multi-armed bandits, the Gittins index, regret bounds,
UCB (2); Big-O complexity and sorting theory (3); caching theory and competitive ratios (4); scheduling
theory and its intractability (5); Bayesian inference, Laplace's Law, power-law/normal/Erlang
distributions (6); regularization, cross-validation, the bias-variance tradeoff (7); computational
complexity, the Cobham–Edmonds thesis, LP/Lagrangian relaxation, approximation guarantees (8); Monte Carlo
methods, randomized algorithms, simulated annealing (9); queueing theory, control theory (AIMD), and
impossibility results (10); game theory, mechanism design, auction theory, the revelation principle (11);
verification vs. search / P-vs-NP flavor (Conclusion).

**Inferred (mine):** the book is an accessible tour of *decision theory under bounded resources* — the
through-line is expected value vs. realized outcome, tractability as a first-class constraint, and the
tradeoff frontier (time / space / error / certainty) as the real object of rational choice.

## 17. Sports Connections

**Direct (the book makes them):** tournament structures as sorting algorithms — Single Elimination,
Round-Robin, Ladder, brackets — and "the silver medal is a lie" (3); Michael Trick engineering
league-schedule tension for MLB/NCAA (3, 8); heads-up poker as a sorting ladder and as recursion/leveling
(3, 11); man-vs-machine chess (Nakamura vs. Rybka, 11); a league commissioner and Wall Street's daily
close as mechanism design (11); the regular season as a near-perfect sort (3, flagged as outrunning the
evidence).

**Inferred (mine):** process-over-outcome as the analytics-era coaching creed (judge the +EV decision,
not the result — chs. 1, Conclusion); randomized/mixed strategies as unexploitable play in
serve/pitch/penalty selection (9, 11); AIMD-style roster/cap management and promotion-relegation as
dynamic hierarchies (10); regression-to-the-mean and distribution-over-average in scouting (6, 9);
progressive-overload training as push-to-failure-then-back-off (10); salary caps and anti-doping as
tragedy-of-the-commons mechanism design (11).

## 18. AI and Machine Learning Connections

**Direct (the book makes them):** UCB and bandit algorithms (2); caching and LRU (4); scheduling,
preemption, context switching (5); Bayesian inference and priors (6); overfitting, cross-validation,
regularization, the Lasso, early stopping, neural nets (7); computational complexity and approximation
(8); Monte Carlo, randomized algorithms, simulated annealing, the Metropolis Algorithm (9); packet
routing, congestion control (10); algorithmic game theory, selfish routing, spectrum/ad auctions, matching
markets (11); "computation is bad" as a design directive (Conclusion).

**Inferred (mine):** explore/exploit → RL exploration (ε-greedy, entropy regularization); simulated
annealing / Metropolis → stochastic optimization, temperature in sampling/decoding, learning-rate
schedules; Monte Carlo → MCMC, MCTS (AlphaGo), Monte Carlo dropout; overfitting/regularization is core ML;
mechanism design & the revelation principle → incentive-compatible and aligned AI, ad/data markets;
information cascades → recommender feedback loops and automated-pricing runaways; the price of anarchy →
bounds on decentralized/federated multi-agent systems; computational kindness → human-centered AI/UX
(propose options rather than demand underspecified goals); cost-of-computation → anytime algorithms and
meta-reasoning; spinning vs. blocking → polling vs. interrupt/callback in serving and agent orchestration.

## 19. Top Reusable Cases

```
Case ID: B01-C01 (Kepler)
Case: Kepler's eleven courtships
Concept: Optimal stopping / the 37% Rule
Short Description: The astronomer agonized over eleven candidates and reproached himself for hesitation —
optimal stopping lived three centuries before it was named.
Why It Is Valuable: Humanizes an abstract math rule; embodies the "recall/look-back" variant.
Best Content Use: Long-form video anchor on the 37% Rule.
Tags: optimal-stopping, dating, 37-percent-rule, history
```

```
Case ID: B01-C01 (Trick)
Case: Michael Trick's age-26.1 proposal (and rejection)
Concept: The 37% Rule applied to a lifespan; the "rejection" variant
Short Description: A researcher computed his own optimal stopping age, proposed — and was turned down,
exposing the model's rejection-blind assumption.
Why It Is Valuable: The counterexample that shows the model's limits; funny and self-aware.
Best Content Use: The honest twist in a 37% Rule piece.
Tags: optimal-stopping, rejection, model-limits
```

```
Case ID: B01-C02 (ECMO)
Case: The ECMO clinical trials
Concept: Explore/exploit; adaptive vs. conventional trial design
Short Description: "Play-the-winner" adaptive designs vs. randomized trials, with infant survival as the
payoff — the ethics of exploration in the starkest terms.
Why It Is Valuable: High stakes make the explore/exploit tradeoff viscerally real.
Best Content Use: The moral heart of an explore/exploit video.
Tags: explore-exploit, clinical-trials, ethics, adaptive-design
```

```
Case ID: B01-C02 (Gittins)
Case: The Gittins index top-left cell (0.7029 beats a known 70%)
Concept: The exploration bonus
Short Description: A never-tried option scores higher than a machine known to pay out 70% of the time —
so "the grass is greener" can be a correct inference.
Why It Is Valuable: A single number that proves optimism is rational.
Best Content Use: Short on why untried options deserve a bonus.
Tags: explore-exploit, gittins-index, optimism
```

```
Case ID: B01-C03 (Dodgson)
Case: "The silver medal is a lie" — Dodgson/Lewis Carroll's 1883 tennis proof
Concept: Single Elimination reveals only the winner; noise
Short Description: Lewis Carroll proved a knockout bracket's second-place finisher usually isn't the
second-best player; noise makes even the champion unreliable.
Why It Is Valuable: Overturns a universal intuition about tournaments with a rigorous proof.
Best Content Use: Long-form on sorting/ranking and "races beat fights."
Tags: sorting, tournaments, noise, ranking
```

```
Case ID: B01-C04 (Noguchi)
Case: The Noguchi filing system / the vindicated desk pile
Concept: LRU and self-organizing lists
Short Description: A "just put it on top" pile is provably within 2× of clairvoyant optimality — your
mess is nearly optimal.
Why It Is Valuable: Permission-giving, counterintuitive, instantly relatable.
Best Content Use: "Your messy desk is mathematically optimal."
Tags: caching, LRU, organization, self-organizing-lists
```

```
Case ID: B01-C05 (Pathfinder)
Case: Mars Pathfinder's priority inversion
Concept: Scheduling; priority inversion / inheritance
Short Description: A Mars lander nearly failed because a low-priority task blocked a high-priority one —
"important things first" can masquerade as procrastination.
Why It Is Valuable: Dramatic, concrete, and reframes procrastination.
Best Content Use: Scheduling video; "procrastination is optimizing the wrong metric."
Tags: scheduling, priority-inversion, procrastination
```

```
Case ID: B01-C06 (Gould)
Case: Stephen Jay Gould's cancer diagnosis
Concept: Distribution shape vs. median; the Multiplicative Rule
Short Description: Told his cancer had an 8-month median survival, Gould read the right-skewed
distribution and lived 20 more years — the shape, not the average, was the story.
Why It Is Valuable: Emotionally powerful; teaches distribution literacy in one story.
Best Content Use: The three-prediction-rules video.
Tags: bayes, distributions, prediction, power-law
```

```
Case ID: B01-C07 (marriage-model)
Case: The nine-factor marriage model and Darwin "regularizing to the page"
Concept: Overfitting; regularization
Short Description: A model with more factors fit the data perfectly but predicted worse; Darwin decided by
a simple pro/con list — complexity penalties as rationality.
Why It Is Valuable: Overfitting in one picture, plus a historical hero deciding simply.
Best Content Use: "Why thinking harder gives worse answers."
Tags: overfitting, regularization, less-is-more, decision-making
```

```
Case ID: B01-C08 (Bellows)
Case: Meghan Bellows's wedding seating chart
Concept: Intractability; constrained optimization
Short Description: A bride used protein-design optimization to seat her wedding — ~11¹⁰⁷ possible plans,
a 36-hour run — because the problem is genuinely intractable.
Why It Is Valuable: Makes NP-hardness tangible and charming.
Best Content Use: "The seating chart no supercomputer can solve."
Tags: intractability, TSP, optimization, relaxation
```

```
Case ID: B01-C09-02 (Ulam)
Case: Ulam's solitaire → the Monte Carlo Method → the atom bomb
Concept: Sampling; Monte Carlo
Short Description: A convalescing mathematician, unable to compute solitaire odds, just played hands and
counted — birthing a pillar of scientific computing used on the bomb.
Why It Is Valuable: A vivid, human origin story for "simulate instead of enumerate."
Best Content Use: "Why the smartest move is sometimes to roll the dice."
Tags: randomness, monte-carlo, sampling, history
```

```
Case ID: B01-C09-11 (Kirkpatrick)
Case: Simulated annealing beats the IBM chip-layout "guru"
Concept: Simulated annealing; front-load randomness then cool
Short Description: A physicist mapped "temperature" onto optimization, beat IBM's secretive human expert,
and published — openness plus randomness winning.
Why It Is Valuable: David-vs-guru story with a clean method and moral.
Best Content Use: "How to get unstuck" (local maxima) video.
Tags: randomness, simulated-annealing, optimization, local-maxima
```

```
Case ID: B01-C10-07 (HOPE)
Case: HOPE probation in Honolulu
Concept: Exponential backoff — the algorithm of forgiveness
Short Description: Immediate, small, escalating penalties (one day in jail, then more) cut rearrests by
half and drug use by 72% — "finite patience and infinite mercy."
Why It Is Valuable: A networking algorithm reshaping criminal justice; high stakes, real results.
Best Content Use: "The algorithm of forgiveness."
Tags: exponential-backoff, forgiveness, criminal-justice, policy
```

```
Case ID: B01-C10-11 (bufferbloat)
Case: Jim Gettys and the discovery of bufferbloat
Concept: Bufferbloat; latency vs. throughput; "always buffered"
Short Description: A dad investigating slow home wifi uncovered oversized buffers in every router, phone,
and the Internet's backbone — and a diagnosis of modern overload.
Why It Is Valuable: Detective story reframing a universal frustration ("always buffered").
Best Content Use: "You're not always connected — you're always buffered."
Tags: networking, bufferbloat, latency, attention
```

```
Case ID: B01-C11-03 (prisoners-dilemma)
Case: The prisoner's dilemma + the Godfather
Concept: Dominant strategy; mechanism design
Short Description: Rational defection dooms both prisoners; adding a Godfather (informing = death) worsens
payoffs yet makes everyone better off — change the game, not the strategy.
Why It Is Valuable: The book's most load-bearing game plus its most paradoxical fix.
Best Content Use: "The math of why everyone's miserable (and how to fix it)."
Tags: game-theory, prisoners-dilemma, mechanism-design, equilibrium
```

```
Case ID: B01-C11-09 (fly-textbook)
Case: The $23.7M textbook and the 2010 flash crash
Concept: Information cascades
Short Description: Two Amazon pricing algorithms with no ceiling drove a used textbook to $23.7M — the
same runaway-feedback mechanism behind the flash crash that erased ~$1T in minutes.
Why It Is Valuable: An absurd real number that explains every bubble.
Best Content Use: "How a $23M textbook explains every bubble."
Tags: game-theory, information-cascade, bubbles, algorithmic-pricing
```

```
Case ID: B01-C11-08 (love)
Case: Love as organized crime / "happiness is the lock"
Concept: Emotions as evolution's mechanism design; the commitment problem
Short Description: Involuntary love changes the marriage game's payoffs so staying is the equilibrium —
the most "irrational" feeling is what a game theorist would engineer.
Why It Is Valuable: Turns cold game theory into a moving account of attachment.
Best Content Use: "Why falling in love is a game-theory power move."
Tags: game-theory, emotions, love, commitment-device
```

```
Case ID: B01-C99-06 (18-cent-coin)
Case: The 18-cent coin and computationally kind design
Concept: Computational kindness in design
Short Description: The coin that mathematically minimizes change would turn every cash register into a
traveling-salesman problem — optimal ≠ usable.
Why It Is Valuable: Crisp, surprising separation of "best on paper" from "best for people."
Best Content Use: "Why the perfect coin would ruin your day."
Tags: computational-kindness, design, change-making, usability
```

```
Case ID: B01-C99 (bullfight)
Case: Brian's phantom-consensus bullfight (Spain)
Concept: Computational kindness; simulating other minds
Short Description: Three friends each adopted the others' perceived enthusiasm for a bullfight none
actually wanted — the hidden cost of "I'm flexible."
Why It Is Valuable: Universal, funny, immediately behavior-changing.
Best Content Use: "The kindest thing you can say is 'I'm NOT flexible.'"
Tags: computational-kindness, preferences, theory-of-mind
```

## 20. Top Content Seeds

```
Title Idea: The 37% Rule — the math of when to stop looking
Core Question: When should you stop searching and commit?
Concept: Optimal stopping
Hook: There's a provably optimal moment to stop dating, apartment-hunting, or hiring — and it's exactly
37% of the way through.
Supporting Case: Kepler's courtships; Trick's age-26.1 proposal-and-rejection.
Potential Conflict or Surprise: The optimal rule still fails 63% of the time — and works the same for 100
or a million options.
Psychology Angle: Outcome bias; the anxiety of irreversible choice.
Math Angle: The 1/e law; Look-Then-Leap vs. Threshold.
Sports Angle: Judge the decision, not the result.
AI Angle: Secretary/prophet problems in online algorithms.
```

```
Title Idea: Why thinking harder gives you worse answers
Core Question: Can more data and more deliberation hurt?
Concept: Overfitting and regularization
Hook: A model with more factors fit the data perfectly — and predicted the future terribly.
Supporting Case: The nine-factor marriage model; Markowitz's 50/50 split; Darwin's pro/con page.
Potential Conflict or Surprise: Your first instinct can be the rational choice; more information can be
worse than less.
Psychology Angle: Less-is-more; ecological rationality.
Math Angle: Bias-variance; the Lasso; early stopping.
Sports Angle: Overcoached teams; simple heuristics under pressure.
AI Angle: Regularization, cross-validation — core ML.
```

```
Title Idea: You're not always connected — you're always buffered
Core Question: Why does modern life feel like an infinite inbox?
Concept: Bufferbloat, latency, Tail Drop
Hook: A dad fixing his kids' slow wifi found a flaw in every device on Earth — and it explains your
overwhelm.
Supporting Case: Jim Gettys and bufferbloat; the 40-minute crêpe; Katy Perry's inbox.
Potential Conflict or Surprise: A bigger buffer makes things worse; dropping balls on purpose is good
management.
Psychology Angle: Attention as a queue; the relief of Tail Drop.
Math Angle: Queueing theory; latency vs. throughput.
Sports Angle: Tactical fouling / conceding to protect the whole.
AI Angle: Load-shedding and latency-vs-throughput in serving.
```

```
Title Idea: The algorithm of forgiveness
Core Question: How do you keep giving someone chances without being a doormat?
Concept: Exponential backoff
Hook: The internet's trick for surviving failure is also the humane way to handle a flaky friend, an
addicted relative, and a repeat offender.
Supporting Case: ALOHAnet's collapse; the HOPE probation program.
Potential Conflict or Surprise: "Finite patience and infinite mercy" — you never fully give up, yet the
retry rate falls to near zero.
Psychology Angle: Forgiveness without martyrdom; behavior change by immediate escalation.
Math Angle: Doubling delays; breaking symmetry with randomness.
Sports Angle: Progressive overload; three-strikes reconsidered.
AI Angle: Backoff-with-jitter in distributed systems.
```

```
Title Idea: The math of why everyone's miserable (and how to fix it)
Core Question: Why do rational, well-meaning people arrive at outcomes terrible for everyone?
Concept: Prisoner's dilemma, tragedy of the commons, mechanism design
Hook: From unlimited vacation no one takes to a planet we're all torching — game theory explains the
trap, and how to escape it.
Supporting Case: The prisoner's dilemma + the Godfather; unlimited-vacation "race to the bottom."
Potential Conflict or Surprise: Making every outcome worse can make everyone better off.
Psychology Angle: Social comparison; overwork.
Math Angle: Dominant strategy; Nash equilibrium; price of anarchy.
Sports Angle: Salary caps and anti-doping as mechanism design.
AI Angle: Mechanism design for ad auctions and multi-agent systems.
```

```
Title Idea: Why the smartest move is sometimes to roll the dice
Core Question: Can randomness beat reasoning?
Concept: Monte Carlo and randomized algorithms
Hook: A mathematician stopped trying to solve his card game and just played it — inventing a pillar of
modern science.
Supporting Case: Ulam's solitaire → Monte Carlo → the bomb; Miller-Rabin.
Potential Conflict or Surprise: You can answer a strict yes/no question (is this prime?) by chance, faster
than by proof.
Psychology Angle: When analysis paralyzes and sampling frees.
Math Angle: Monte Carlo; primality testing; simulated annealing.
Sports Angle: Mixed strategies as unexploitable play.
AI Angle: MCMC, MCTS, stochastic training.
```

```
Title Idea: Your messy desk is mathematically optimal
Core Question: Should you organize, or embrace the pile?
Concept: Caching, LRU, self-organizing lists
Hook: Computer science says the "just put it on top" pile is within 2× of a psychic's perfect filing.
Supporting Case: The Noguchi system; Sleator-Tarjan; "turn the library inside out."
Potential Conflict or Surprise: "Cognitive decline" may just be learning — a slow lookup measures how much
you know.
Psychology Angle: Memory as organization; the forgetting curve; aging.
Math Angle: Competitive ratios; temporal locality.
Sports Angle: N/A core.
AI Angle: Cache-eviction policies; retrieval.
```

```
Title Idea: The kindest thing you can say is "I'm NOT flexible"
Core Question: Is being accommodating actually cruel?
Concept: Computational kindness
Hook: "Oh, I'm flexible, whatever works" is one of the most inconsiderate things you can say — and
computer science can prove it.
Supporting Case: The scheduling paradox; the phantom-consensus bullfight; the 18-cent coin.
Potential Conflict or Surprise: Politeness and kindness diverge; the optimal design can be the cruelest.
Psychology Angle: Cognitive load; theory of mind; choice overload.
Math Angle: Verification vs. search; change-making as TSP.
Sports Angle: Simple play-calling to cut cognitive load.
AI Angle: Kind interfaces — propose options, don't demand goals.
```

```
Title Idea: Small data is big data in disguise
Core Question: How can you predict from a single data point?
Concept: Bayesian prediction and priors
Hook: Tell me how long something's already lasted and I'll predict its future — if I know which of three
"shapes" the world it lives in has.
Supporting Case: Gould's cancer; the German tank problem; the Copernican Principle at the Berlin Wall.
Potential Conflict or Surprise: Watching more news can make your predictions worse.
Psychology Angle: Humans as intuitive Bayesians; corrupted priors.
Math Angle: Power-law/normal/Erlang; Multiplicative/Average/Additive rules.
Sports Angle: Regression to the mean; distribution over average.
AI Angle: Priors, Bayesian ML, single-shot prediction.
```

```
Title Idea: The seating chart no supercomputer can solve
Core Question: What do you do when a problem is genuinely impossible to solve perfectly?
Concept: Intractability and relaxation
Hook: A bride used protein-folding software to seat her wedding — because the problem has more
arrangements than atoms you'd care to count.
Supporting Case: Bellows's wedding; the traveling salesman problem; the three relaxations.
Potential Conflict or Surprise: The rational move is to "cheat" — consciously bend the rules.
Psychology Angle: Perfectionism vs. "the perfect is the enemy of the good."
Math Angle: NP-hardness; lower bounds; Lagrangian relaxation.
Sports Angle: League scheduling (Trick).
AI Angle: Approximation algorithms; constraint solvers.
```

```
Title Idea: Even the best strategy fails most of the time (and that's fine)
Core Question: How should you judge a decision that turned out badly?
Concept: Process over outcome — computational Stoicism
Hook: The optimal way to find a partner fails 63% of the time — which means bad luck isn't your fault.
Supporting Case: The 37% Rule's failure rate; Russell's "wisest act"; LRU/UCB never guaranteeing success.
Potential Conflict or Surprise: "Good enough" is the definition of rational, not a concession.
Psychology Angle: Outcome bias; self-compassion.
Math Angle: Expected value vs. realized outcome.
Sports Angle: Judge the +EV call, not the scoreboard.
AI Angle: Decision-quality vs. single-outcome evaluation.
```

```
Title Idea: How to get unstuck (the lobster-trap trick)
Core Question: Why do you get stuck in "good but not best," and how do you escape?
Concept: Local maxima and simulated annealing
Hook: A lobster dies in the trap because escaping means going deeper first — your career and code have the
same trap.
Supporting Case: The lobster trap; the ten-city vacation; Kirkpatrick beating the IBM guru.
Potential Conflict or Surprise: To improve you must sometimes deliberately get worse.
Psychology Angle: The courage to worsen before improving; escaping ruts.
Math Angle: Hill climbing; Metropolis; cooling schedules.
Sports Angle: Tearing up a good system to find a better one.
AI Angle: SGD, random restarts, temperature/exploration schedules.
```

## 21. Book Fingerprint

```
Primary Topic: Applying computer-science algorithms to human decision-making under limited time, space,
and information.
Core Thesis: The hard problems of living are computational, so algorithms are transferable guides — and
bounded, "good enough" rationality is what rationality actually is.
Dominant Perspective: Optimistic, ecological-rationality computationalism — humans (and machines) as
well-adapted bounded agents; warm, witty, humane.
Most Important Concept: Bounded rationality as real rationality (process over outcome; "good enough").
Most Unique Idea: Computational kindness — an ethics and design principle derived from complexity theory.
Strongest Evidence: The provably-optimal and provably-hard mathematical results (37% law, Gittins/regret
bounds, Bélády/LRU, Nash + intractability, price of anarchy, Vickrey).
Best Case: The prisoner's dilemma + the Godfather (ch. 11) — most load-bearing, most paradoxical fix;
runner-up, Kepler's courtships (ch. 1).
Most Controversial Claim: "If your laptop cannot find it, neither can the market" — computational
intractability undermines equilibrium-based economics.
Biggest Weakness: Repeatedly diagnoses better than it prescribes (no general rule for the right prior, the
complexity sweet spot, which relaxation, or how much randomness), and several behavioral bridges rest on
thin or replication-shadowed evidence.
Best YouTube Opportunity: "The algorithm of forgiveness" (exponential backoff → HOPE) or "The math of why
everyone's miserable (and how to fix it)" (prisoner's dilemma → mechanism design).
```

## 22. Cross-Book Comparison Preparation

```
Concept: Bounded rationality / ecological rationality
This Book's Position: Cutting corners under real constraints IS rationality; humans are well-adapted
bounded agents, and "good enough" is a rigorous standard.
Key Supporting Evidence: 37% Rule's failure being a problem-property; SPT/relaxation/sampling as optimal
responses to intractability; ecological studies of forgetting and intuitive Bayes.
Confidence: High (as the book's thesis).
Possible Competing Position: Heuristics-and-biases tradition (deviations = errors); classical
rational-choice theory (unbounded optimization).
Keywords for Cross-Book Search: bounded rationality, ecological rationality, satisficing, good enough,
heuristics, Herbert Simon, Gigerenzer
```

```
Concept: Explore/exploit tradeoff
This Book's Position: The new-vs-familiar choice is a multi-armed bandit governed by "the interval";
optimism (an exploration bonus) is provably rational, and exploration's value falls with time.
Key Supporting Evidence: Gittins index (0.7029 > known 70%); logarithmic regret bound; Carstensen's
interval manipulation.
Confidence: High for the math; moderate for the human applications.
Possible Competing Position: Accounts treating novelty-seeking as temperament/personality, or as
irrational variety-seeking.
Keywords for Cross-Book Search: explore-exploit, multi-armed bandit, curiosity, novelty, regret, Gittins
index, exploration bonus
```

```
Concept: Optimal stopping / commitment under irreversibility
This Book's Position: A large class of "when to act" decisions is optimal stopping; explore a fixed
fraction, then commit; failure rates are problem-properties.
Key Supporting Evidence: The 1/e (37%) result; full-information 58% threshold; Kepler and Trick.
Confidence: High for the math; the "success = the single best" objective is a stated limitation.
Possible Competing Position: Satisficing accounts (Simon) that reject "the single best" as the goal;
decision-under-uncertainty frameworks emphasizing reversibility.
Keywords for Cross-Book Search: optimal stopping, secretary problem, 37 percent rule, commitment,
irreversibility, satisficing
```

```
Concept: Prediction from priors vs. data volume (Bayesian)
This Book's Position: The right prior/distribution matters more than data volume; "small data is big data
in disguise"; more data/thinking can hurt (overfitting).
Key Supporting Evidence: Single-point Bayesian prediction; Laplace's Law; the nine-factor marriage model;
the Lasso.
Confidence: High within the book; can't operationalize "the right prior" for novel cases.
Possible Competing Position: Big-data/frequentist maximalism (more data is always better); pure empiricism.
Keywords for Cross-Book Search: Bayesian inference, priors, small data, overfitting, regularization,
prediction, big data
```

```
Concept: Intractability and "good enough" (relaxation, approximation, randomness)
This Book's Position: Many real problems are intractable, so relax/approximate/randomize; you can know
you're within X% of an optimum you can never compute.
Key Supporting Evidence: TSP and ~11¹⁰⁷ seating; 84% of scheduling intractable; Monte Carlo; Miller-Rabin.
Confidence: High (with P-vs-NP openness flagged honestly).
Possible Competing Position: Optimization-maximalism / faith that more compute yields exact answers;
rational-choice models assuming costless computation.
Keywords for Cross-Book Search: intractability, NP-hard, approximation, relaxation, randomized algorithms,
P vs NP, complexity
```

```
Concept: Game theory, cooperation, and mechanism design
This Book's Position: Rational self-interest can be collectively ruinous; you fix bad equilibria by
changing the game (mechanism design), and evolution does this via emotions; seek games where honesty is
dominant.
Key Supporting Evidence: Prisoner's dilemma; price of anarchy; the Vickrey auction/revelation principle;
emotions as commitment devices (Frank).
Confidence: High for the game theory; interpretive for "emotion as mechanism design."
Possible Competing Position: Pure self-interest / rational-actor models; accounts of cooperation via
repeated games and reputation rather than emotion or design.
Keywords for Cross-Book Search: game theory, prisoners dilemma, Nash equilibrium, mechanism design,
cooperation, tragedy of the commons, commitment device
```

```
Concept: Computation as a lens on ethics and design (computational kindness)
This Book's Position: Interacting with and designing for others imposes computational load; minimizing
that labor of thought is a genuine ethic and design principle.
Key Supporting Evidence: The scheduling paradox (constrained > open); "I'm flexible" as passing the
cognitive buck; the 18-cent coin; spinning vs. blocking.
Confidence: Moderate–High (explicitly a bridge/analogy).
Possible Competing Position: Choice architecture / nudge (Thaler & Sunstein) as an alternative framing;
etiquette traditions that value withholding preferences.
Keywords for Cross-Book Search: cognitive load, choice architecture, nudge, design, computational
kindness, verification vs search, decision fatigue
```

```
Concept: Memory, forgetting, and aging as optimization
This Book's Position: Minds are caches; forgetting and age-related slowdown are largely optimization and
retrieval cost, not decay.
Key Supporting Evidence: LRU as best practical eviction; Anderson & Schooler curve-matching; Ramscar on
aging.
Confidence: Moderate (inferred from curve-matching; hedged "at least partly").
Possible Competing Position: Neurological-decline accounts of aging; decay theories of forgetting.
Keywords for Cross-Book Search: memory, forgetting curve, caching, aging, cognitive decline, retrieval,
LRU
```
