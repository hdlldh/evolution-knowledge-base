# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 4: Caching — Forget About It
**Author:** Brian Christian and Tom Griffiths
**Type:** Extraction
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 112–136 (book chapter 4, incl. footnotes)
**Date:** 2026-07-21
**Revision note:** Revised after Chapter_04_Audit.md; see that file for what changed and why.

```
BOOK:
Algorithms to Live By: The Computer Science of Human Decisions

AUTHOR:
Brian Christian and Tom Griffiths

CHAPTER:
4 — Caching: Forget About It
```

---

## 1. Chapter Thesis

Because fast memory is always scarce and expensive, both computers and minds are organized as a
*hierarchy of caches* — small-and-fast backed by large-and-slow — and the hard problem is deciding
what to keep close and what to evict. Computer science shows the optimal policy (evict what you'll
need furthest in the future) requires clairvoyance, and that the best achievable substitute is Least
Recently Used (LRU): assume the near future mirrors the recent past. Applied outward, this reorganizes
closets, warehouses, the geography of the internet, and — most strikingly — the human brain: forgetting
and "cognitive decline" may not be failures of a decaying organ but the unavoidable retrieval cost of
a memory that is optimally tuned to a world whose own statistics fade exactly like the forgetting
curve. Your messy pile of papers is already a near-optimal self-organizing structure.

## 2. Key Concepts

```
Concept Name: Caching
Definition: Keeping copies of frequently or recently used information in a small, fast, close store so
you don't have to fetch it from a large, slow, distant one.
Why It Matters: One of the most powerful and universal ideas in computing — it underlies chip layout,
hard drives, browsers, CDNs, and (the chapter argues) human memory and physical organization.
How the Author Uses It: The organizing frame for the whole chapter; every domain (closet, library,
internet, brain) is recast as a caching problem.
Related Concepts: Memory hierarchy, eviction policy, temporal locality, LRU.
```

```
Concept Name: The Memory Hierarchy
Definition: A pyramid of storage layers, each larger but slower than the one above (Burks, Goldstine &
von Neumann, 1946) — trading size against speed to approximate "the best of both."
Why It Matters: A fundamental principle of computing; modern devices have ~6 layers, and managing them
well "has never been as important." The library-plus-desk is the everyday analogue.
How the Author Uses It: To explain the size/speed tradeoff (hard disk vs. SSD; SRAM vs. flash), the
"memory wall," and multi-level home storage (closet → basement → storage locker).
Related Concepts: Moore's Law, memory wall, caching, LRU across levels.
```

```
Concept Name: Cache Eviction / Replacement Policy
Definition: The algorithm deciding what to overwrite when a full cache must make room; the goal is to
minimize "cache misses" (page faults) — times you must go to slow memory.
Why It Matters: The core computational problem of the chapter, and the direct analogue of "what to
throw away" when your closet overflows.
How the Author Uses It: To compare Random Eviction, FIFO, and LRU, and to translate the winner into
life advice about decluttering.
Related Concepts: Bélády's Algorithm, cache miss, LRU, FIFO.
```

```
Concept Name: Bélády's Algorithm (Clairvoyant / Optimal Eviction)
Definition: The provably optimal eviction rule — when the cache is full, evict whichever item you will
need again *furthest in the future*.
Why It Matters: Sets the theoretical ceiling; every practical policy is judged by how close it comes.
How the Author Uses It: As the unattainable ideal (it requires "clairvoyance" — data from the future),
against which LRU is shown to be the best real substitute. Engineers joke about "implementation
difficulties."
Related Concepts: Clairvoyant algorithms, LRU, offline optimum ("God's algorithm").
```

```
Concept Name: Least Recently Used (LRU)
Definition: Evict the item that has gone longest untouched; equivalently, keep what was used most
recently, and put newly used items at the front.
Why It Matters: The chapter's central practical result — LRU consistently performs closest to
clairvoyance and is the "overwhelming favorite" of computer scientists.
How the Author Uses It: To recommend a decluttering rule (keep what you still use), to propose turning
libraries inside out, and to prove the Noguchi filing system and the messy pile are optimal.
Related Concepts: Temporal locality, self-organizing lists, FIFO (the inferior rival), Z-order.
```

```
Concept Name: Temporal Locality
Definition: If a piece of information was called for once, it is likely to be needed again soon.
Why It Matters: The reason LRU works — it makes the recent past a good predictor of the near future.
The chapter presents its *two sources in parallel*: temporal locality arises both from how computers
solve problems (a loop making rapid related reads/writes) and from how people solve problems (switching
among email, browser, word processor). That parallel is the chapter's central "computers and minds face
the same problem" move.
How the Author Uses It: To justify LRU, and later to connect the forgetting curve to the statistics of
the real world.
Related Concepts: LRU, the forgetting curve, "history repeats itself — backward."
```

```
Concept Name: Geographic Caching (Proximity as the Scarce Resource)
Definition: Caching where the constraint is physical distance rather than hardware speed — store
in-demand items near where they're used.
Why It Matters: Extends caching from inside the chip to the whole internet and to warehouses; "distance
matters."
How the Author Uses It: Akamai/CDNs, Amazon's fulfillment centers and "anticipatory shipping" patent,
Netflix's regional "Local Favorites," and home advice ("exploit geography").
Related Concepts: CDN, memory hierarchy, cache, law of large numbers.
```

```
Concept Name: Self-Organizing Lists
Definition: A list you must search linearly from the front, but into which you may reinsert a found
item anywhere; the question is where to put it to minimize future search.
Why It Matters: Formalizes the Noguchi filing dilemma and yields the pile-on-top result; Sleator &
Tarjan (1985) proved LRU reinsertion stays within a factor of 2 of the offline optimum.
How the Author Uses It: To prove that always returning an item to the front (a pile) is not just
convenient but provably near-optimal — "a self-organizing mess."
Related Concepts: LRU, Noguchi filing system, the pile, clairvoyance.
```

```
Concept Name: The Forgetting Curve
Definition: Ebbinghaus's (1879) empirical curve of how recall declines with elapsed time.
Why It Matters: The chapter's bridge from machine caching to the mind; its shape turns out to match
the statistical decay of real-world information.
How the Author Uses It: Via Anderson & Schooler, to argue human forgetting is an optimal tuning of the
brain to the environment, not a defect.
Related Concepts: Temporal locality, memory as organization, tip-of-the-tongue.
```

```
Concept Name: Memory as Organization, Not Storage
Definition: John Anderson's reframing — the mind's problem isn't running out of space but taking finite
time to search an ever-growing store.
Why It Matters: Recasts forgetting and age-related slowdown as retrieval cost, not decay; "we say
'brain fart' when we should really say 'cache miss.'"
How the Author Uses It: To reinterpret "cognitive decline" (Ramscar) as the unavoidable consequence of
knowing more — "a lot of what is currently called decline is simply learning."
Related Concepts: Self-organizing lists (infinite shelf), the forgetting curve, the tyranny of
experience.
```

## 3. Key Claims

```
Claim: Managing limited fast memory is a fundamental, universal problem — computers face exactly the
same "what to keep and how to arrange it" dilemma as an overflowing closet.
Type: Theoretical / Interpretive
Evidence Provided: The parallel between home-organization advice and memory management; caching appears
"in every aspect of computation."
Strength of Support: Strong as a framing; the closet analogy is illustrative rather than empirical.
```

```
Claim: The size/speed tradeoff is unavoidable, so a memory hierarchy is the best available design.
Type: Theoretical / Historical
Evidence Provided: Burks, Goldstine & von Neumann's 1946 "memory organ" proposal; Atlas (1962); the
SRAM-vs-flash ~1000× cost gap; Moore's Law (Gordon Moore, 1975 — transistors doubling every two years)
outpacing memory speed, so the *relative* cost of a memory access rises exponentially, producing the
"memory wall" of the 1990s — "processors that twiddled their thumbs ever faster." Factory analogy:
doubling manufacturing speed while parts still arrive at the same sluggish pace just makes the factory
"twice as idle."
Strength of Support: Strong. Grounded in named designs and a specific cost figure.
```

```
Claim: The optimal eviction policy is to remove whatever you'll need furthest in the future — but this
requires clairvoyance.
Type: Theoretical (proved, essentially by definition)
Evidence Provided: Bélády's 1966 paper (most-cited CS research for fifteen years); the policy is
optimal "essentially by definition."
Strength of Support: Strong, with the explicit caveat that it is unimplementable without future data.
```

```
Claim: Just having a cache helps at all — a system is more efficient "regardless of how you maintain
it." (Random Eviction is the vehicle for the point, not an endorsement of Random: it is "not half bad"
precisely because the cache itself does the work, since frequently used items return to it soon anyway.)
Type: Theoretical / Empirical
Evidence Provided: A "startling early result in caching theory."
Strength of Support: Moderate to Strong. Stated as a known result; no specific study cited in-chapter.
```

```
Claim: LRU consistently performs closest to clairvoyance and is the dominant practical policy.
Type: Empirical (attributed to Bélády and later research)
Evidence Provided: Bélády compared Random, FIFO, and LRU variants across many scenarios; LRU won.
LRU works because of temporal locality. It remains the "overwhelming favorite" despite fancier schemes
that can beat it "under the right conditions."
Strength of Support: Strong within the chapter's presentation; the "can be beaten under the right
conditions" hedge is preserved.
```

```
Claim: FIFO and LRU are very different policies, and LRU clearly outperforms FIFO — so two of Martha
Stewart's four decluttering questions give conflicting advice, one much better than the other.
Type: Interpretive
Evidence Provided: Mapping Stewart's "How long have I had it?" to FIFO and "When did I last use it?" to
LRU; Bélády's comparison favors LRU.
Strength of Support: Strong as an application of the LRU result; the Stewart mapping is the authors'.
```

```
Claim: The best guide to the future is a backward mirror of the past — "assume history repeats
itself — backward."
Type: Interpretive
Evidence Provided: LRU's logic: the next thing needed is the last thing needed; the last thing you'll
need is what you've gone longest without.
Strength of Support: Moderate. A compelling gloss on LRU, explicitly hedged with "unless we have good
reason to think otherwise."
```

```
Claim: Libraries should be "turned inside out" — put recently *returned* books in the lobby, not
recently *acquired* ones.
Type: Prescriptive
Evidence Provided: LRU dominance plus the fact that recently returned books are the most likely to be
checked out next; current rough-sorting hides the most-wanted books; it would also be more socially
positive (a bottom-up "common book" effect).
Strength of Support: Moderate. A logical extension of LRU; presented as a suggestion, with the honest
caveat that popular books would then be split between stacks and lobby.
```

```
Claim: Caching works whenever the scarce resource is proximity, not just hardware speed.
Type: Theoretical
Evidence Provided: Akamai handles ~a quarter of internet traffic; CDNs keep copies worldwide (an
Australian streaming the BBC hits Sydney, never London); Amazon's warehouses randomize placement but
cache high-demand items; the "anticipatory shipping" patent is a physical CDN exploiting the law of
large numbers; Netflix caches region-set films where they're set/watched.
Strength of Support: Strong. Multiple concrete, named commercial instances.
```

```
Claim: Always returning a used item to the front of a list (the pile / Noguchi system) is not merely
convenient but provably near-optimal.
Type: Theoretical (proved)
Evidence Provided: Sleator & Tarjan's 1985 self-organizing-lists paper: LRU reinsertion keeps total
search time within a factor of 2 of the offline optimum ("the algorithm in the sky") — a guarantee no
other algorithm can make.
Strength of Support: Strong. A named theorem with a specific bound.
```

```
Claim: Your messy desk pile is a well-designed, self-organizing structure — you don't need to organize
it because you already have.
Type: Interpretive (of the Sleator-Tarjan result)
Evidence Provided: A pile is a Noguchi box on its side: you search top-to-bottom and return items to
the top, which is exactly LRU reinsertion.
Strength of Support: Strong given the theorem, though it assumes your search behavior actually matches
the model (top-down, return-to-top).
```

```
Claim: The Ebbinghaus forgetting curve matches the statistical decay of information in the real world.
Type: Empirical (attributed to Anderson & Schooler)
Evidence Provided: They analyzed three environments — NYT headlines, parents' speech to children, and
Anderson's email inbox — and found a word is most likely to recur right after use, with likelihood
falling over time, mirroring the Ebbinghaus curve.
Strength of Support: Moderate to Strong. Three independent domains converge; the chapter gives no
sample sizes or effect magnitudes, and the datasets are eclectic.
```

```
Claim: Human forgetting is an optimal tuning of the brain to the environment, not a defect.
Type: Interpretive (attributed to Anderson & Schooler)
Evidence Provided: If minds fade information on the same schedule the world does, forgetting keeps
exactly the most-likely-needed items available. "In any system responsible for managing a vast data
base there must be failures of retrieval."
Strength of Support: Moderate. A strong theoretical argument built on the curve-matching finding; it is
an inference to optimality, not a direct measurement of optimality.
```

```
Claim: "Cognitive decline" with age is largely the unavoidable cost of a bigger store to search, not a
failing mind.
Type: Interpretive / Empirical (attributed to Ramscar et al.)
Evidence Provided: Size alone slows retrieval (Hennessy: bigger city/library/pile = slower search);
Ramscar's Tübingen group ran simulations showing that simply knowing more makes recognizing words,
names, and even letters harder. Scale figures: a 2-year-old knows ~200 words, an adult ~30,000; every
year adds ~a third of a million waking minutes of experience. "A lot of what is currently called
decline is simply learning."
Strength of Support: Moderate. The simulations support the mechanism; the leap to explaining real
age-related lags is partial ("at least partly," the authors hedge). It does not claim all decline is
retrieval cost.
```

```
Claim: The delay of a memory lag is itself an indicator of the extent of your experience.
Type: Interpretive
Evidence Provided: Retrieval effort scales with how much you know; the rarity of lags reflects how well
you've arranged it (most important things closest to hand).
Strength of Support: Moderate. A consoling reframing that follows from the organization-not-storage
model rather than from direct evidence.
```

## 4. Frameworks, Models, and Mental Models

```
Name: The Memory Hierarchy
Description: Layered storage, each level larger and slower than the one above, approximating fast-and-
big.
Components: Fast/small caches at the top (e.g. L1, L2 on the chip; SRAM), progressively larger/slower
levels below (flash, disk, offsite archive). ~6 layers in modern consumer devices.
How It Works: Keep likely-needed data high in the hierarchy; fall through to slower levels only on a
miss. Applied to a home: closet → basement → storage locker, evicting downward by LRU.
When It Is Useful: Whenever fast storage is scarce/expensive relative to demand — i.e. always.
Limitations: Each level adds management complexity ("caches for caches for caches"); size itself slows
even a single level (the tyranny of experience).
```

```
Name: Bélády's Algorithm (Optimal Offline Eviction)
Description: Evict the item needed furthest in the future.
Components: A full cache; perfect knowledge of the future request sequence.
How It Works: By definition minimizes cache misses; the benchmark ceiling.
When It Is Useful: Only when the future is genuinely known; otherwise as a yardstick.
Limitations: Requires clairvoyance — "implementation difficulties." Unimplementable in general.
```

```
Name: LRU (Least Recently Used)
Description: Evict the longest-untouched item; reinsert used items at the front.
Components: A recency ordering of items; front = most recent, back = eviction candidate.
How It Works: Exploits temporal locality to approximate Bélády's rule using only the past. Provably
within a factor of 2 of the offline optimum for self-organizing lists.
When It Is Useful: Almost universally — decluttering, filing, library management, browser Z-order,
Alt/Command+Tab ordering.
Limitations: Beaten "under the right conditions" by frequency-aware or next-to-last-access schemes;
assumes the recent past predicts the near future.
```

```
Name: FIFO (First-In, First-Out)
Description: Evict whatever has been in the cache longest, regardless of use.
Components: An insertion-order queue.
How It Works: Maps to Stewart's "How long have I had it?"; the Moffitt lobby's new-acquisitions
display.
When It Is Useful: Simple bookkeeping; occasionally acceptable.
Limitations: Clearly inferior to LRU — it can evict something you use constantly just because you've
owned it a while.
```

```
Name: The Noguchi Filing System
Description: Don't group by content; file each document in a titled/dated folder and always reinsert at
the far left; search from the left.
Components: A single box; left-side insertion rule for both new and returned files.
How It Works: An unwitting implementation of LRU on a self-organizing list — most recently used files
migrate to the fast (left) end.
When It Is Useful: Any personal filing problem; turned on its side it becomes "the pile."
Limitations: Violates "group like with like," which unsettles people; optimality assumes recency-driven
access.
```

```
Name: Geographic Caching / CDN
Description: Store copies of in-demand content physically near its users.
Components: Distributed edge servers; a popularity signal; the law of large numbers for aggregate
demand.
How It Works: Serve from the nearest cache instead of the origin server (Akamai, Amazon staging
warehouses, Netflix regional files).
When It Is Useful: When latency/distance is the bottleneck; scales from millimeters on a chip to
thousands of miles.
Limitations: Predicting individual demand is hard; works because aggregate demand is predictable.
```

```
Name: Memory-as-Organization (Anderson) + the Forgetting Curve
Description: Treat the mind as an effectively unbounded store with finite search time, optimally tuned
to the world's own decay statistics.
Components: An "infinite shelf" (Noguchi at Library-of-Congress scale); recency-ordered retrieval; a
world whose reference frequencies fade like Ebbinghaus's curve.
How It Works: Forgetting/lags are retrieval cost, not decay; the brain keeps most-likely-needed items
at the front.
When It Is Useful: Reframing "cognitive decline" and the moralization of forgetting.
Limitations: An optimality inference, not a proof; explains lags "at least partly," not wholly.
```

## 5. Research and Evidence

```
Study / Research: The "memory organ" hierarchy proposal
Researchers: Arthur Burks, Herman Goldstine, John von Neumann (Institute for Advanced Study, Princeton)
Year: 1946
Research Question: How to approximate limitless fast memory given real hardware limits?
Method: Design proposal.
Key Finding: Proposed "a hierarchy of memories, each of which has greater capacity than the preceding
but which is less quickly accessible."
How the Author Uses It: Origin of the memory-hierarchy principle.
Important Limitations: A proposal, not an empirical study.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: The Atlas supercomputer and the invention of the cache
Researchers: Atlas team (Manchester, England); Maurice Wilkes (Cambridge)
Year: Atlas 1962; Wilkes's insight shortly after; implemented in the IBM 360/85 later in the 1960s
(where the name "cache" was coined)
Research Question: Can a small fast memory anticipate future requests, not just stage current work?
Method: Hardware development and design insight.
Key Finding: A small fast memory can "automatically accumulate" words from slow memory and keep them
for reuse, avoiding repeated slow-memory penalties. The conceptual move: the fast memory was *first*
merely a convenient staging place to work on data before writing it back; Wilkes's insight was that it
could *deliberately hold on to* likely-future data — staging became anticipation, and that is what
makes it a cache rather than a workspace.
How the Author Uses It: The historical birth of caching.
Important Limitations: Historical narrative.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Foundational caching-algorithm research
Researchers: László "Les" Bélády (IBM); born Hungary 1928, fled the 1956 revolution, immigrated to the
US in 1961
Year: 1966 paper
Research Question: What is the optimal cache eviction policy, and which practical policy comes closest?
Method: Defined the optimal (clairvoyant) policy; compared Random Eviction, FIFO, and LRU variants
across many scenarios.
Key Finding: Optimal = evict the item needed furthest in the future (Bélády's Algorithm); among
practical policies, LRU consistently comes closest to clairvoyance.
How the Author Uses It: The theoretical and empirical backbone of the chapter.
Important Limitations: The optimal policy is unimplementable (needs the future); fancier schemes can
beat LRU under some conditions.
Replication or Controversy Mentioned: Noted as the most-cited CS research for fifteen years.
```

```
Study / Research: Self-organizing lists
Researchers: Daniel Sleator and Robert Tarjan
Year: 1985
Research Question: Where should you reinsert a found item in a linearly searched list to minimize
worst-case total search time?
Method: Worst-case analysis over all possible request sequences.
Key Finding: Simple self-adjusting schemes come "within a constant factor" of the offline optimum;
specifically, LRU reinsertion (always to the front) keeps total search time within a factor of 2 of
clairvoyance — a guarantee no other algorithm can make.
How the Author Uses It: To prove the Noguchi system and the pile are near-optimal, not just tidy or
lazy.
Important Limitations: Worst-case guarantee; assumes the search-and-reinsert model.
Replication or Controversy Mentioned: None identified. Tarjan calls the offline optimum "God's
algorithm… the algorithm in the sky."
```

```
Study / Research: The forgetting curve
Researchers: Hermann Ebbinghaus (University of Berlin)
Year: 1879 onward (self-experiments over about a year)
Research Question: Can memory be studied with the mathematical rigor of the physical sciences?
Method: Daily memorization of lists of nonsense syllables, then self-testing on prior lists.
Key Finding: Repetition increases persistence; recall declines with elapsed time along a characteristic
curve (the forgetting curve).
How the Author Uses It: Establishes a quantitative science of memory and poses the mystery Anderson
later resolves.
Important Limitations: A single self-experimenting subject; the curve's *meaning* was left open for a
century.
Replication or Controversy Mentioned: Framed as the origin point of memory science.
```

```
Study / Research: Memory as an optimal information-retrieval system
Researchers: John Anderson (Carnegie Mellon) with Lael Schooler
Year: Anderson's realization 1987; the environmental analysis with Schooler thereafter
Research Question: Why does memory have the shape it does — is it non-optimal, or tuned to the world?
Method: Ebbinghaus-like analysis applied to *human environments* rather than minds: New York Times
headlines, recordings of parents talking to their children, and Anderson's own email inbox.
Key Finding: In all three domains a word is most likely to appear again right after use, with
likelihood falling over time — the world's statistics mimic the Ebbinghaus curve — implying human
forgetting is an optimal tuning to the environment.
How the Author Uses It: The chapter's central bridge from machine caching to human memory.
Important Limitations: Corpus/observational analysis, not an experiment. Eclectic datasets (NYT
headlines, some parent-child recordings, one email inbox); no sample sizes/effect sizes given.
Optimality is inferred from curve-matching, not directly measured, and the chapter's line "reality
itself has a statistical structure that mimics the Ebbinghaus curve" is the authors' extrapolation from
three idiosyncratic corpora to the world at large.
Replication or Controversy Mentioned: Positioned against the prevailing view that memory is "arbitrary
and non-optimal."
```

```
Study / Research: Cognitive "decline" as the cost of knowing more
Researchers: Michael Ramscar and colleagues (psychologists and linguists, University of Tübingen)
Year: Not specified (recent).
Research Question: Is age-related cognitive slowdown deterioration, or the consequence of a larger
memory store?
Method: A series of computational simulations focused on language (recognizing words, names, letters).
Key Finding: Simply knowing more makes recognition slower regardless of organization scheme; "a lot of
what is currently called decline is simply learning." Older brains "are literally solving harder
computational problems."
How the Author Uses It: To reinterpret cognitive aging as retrieval cost ("cache miss," not "brain
fart").
Important Limitations: Simulations, not human-performance experiments in the chapter; the authors hedge
("at least partly"). Does not claim all decline is benign.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Netflix regional "Local Favorites" map
Researchers: Micah Mertes (film critic)
Year: 2011
Research Question: What films are uncommonly popular in each US state?
Method: Mapped each state's Netflix "Local Favorites."
Key Finding: People overwhelmingly love movies set where they live (Washington → *Singles*; Louisiana
→ *The Big Easy*; Los Angeles → *L.A. Story*; etc.; footnote oddity: *My Own Private Idaho* is best
loved in Maine).
How the Author Uses It: To show local caching of region-set video is both natural and efficient.
Important Limitations: An informal map, not a controlled study.
Replication or Controversy Mentioned: None identified.
```

## 6. Experiments

```
Experiment Name: Ebbinghaus's nonsense-syllable self-experiments
Setup: A single subject (Ebbinghaus) memorizing lists of nonsense syllables daily and self-testing.
Participants: One (the experimenter).
Procedure: Memorize a fresh list each day; test recall of earlier lists after varying delays; repeat
over about a year.
Result: Practice improves persistence; recall falls with elapsed time along the forgetting curve.
Interpretation: Memory is amenable to quantitative, physics-like study.
What It Demonstrates: The existence of a lawful decay of recall over time.
Potential Alternative Explanation: N-of-1 design and nonsense syllables limit generality; the curve
could reflect the artificial materials rather than natural memory.
```

```
Experiment Name: Anderson & Schooler's environmental "forgetting" analysis
Setup: Statistical analysis of how references recur and fade in three real environments.
Participants: N/A — corpora (NYT headlines, parent-child speech recordings, Anderson's email).
Procedure: Measure the probability a word recurs as a function of time since last appearance.
Result: Recurrence is highest just after use and declines over time, matching the Ebbinghaus curve
across all three domains.
Interpretation: The brain's forgetting schedule mirrors the world's decay schedule — evidence of
optimal tuning.
What It Demonstrates: A structural correspondence between memory and environment.
Potential Alternative Explanation: Curve-matching is correlational; a match doesn't prove the brain is
optimizing for these statistics, and the three corpora are idiosyncratic.
```

```
Experiment Name: Ramscar's language simulations
Setup: Computational models of recognition as vocabulary/knowledge grows.
Participants: N/A — simulations.
Procedure: Simulate recognizing words, names, and letters at different amounts of accumulated knowledge.
Result: More knowledge → slower recognition, independent of the organization scheme.
Interpretation: Age-related lags are (at least partly) the search cost of a bigger store, not decay.
What It Demonstrates: That "decline" can arise from information load alone.
Potential Alternative Explanation: Simulations may not capture real neural decline that coexists with
load effects; the chapter itself only claims "at least partly."
```

## 7. Cases and Stories

```
Case Title: Martha Stewart's four questions (and the one that matters)
People / Organization: Martha Stewart; also Francine Jay, Andrew Mellen ("The Most Organized Man in
America")
Context: The home-organization industry's advice on what to keep and how to arrange it.
What Happened: Stewart asks four questions — how long owned, still functions, a duplicate, when last
used — and recommends "grouping like things together." Computer science reveals these embed *different,
incompatible* policies: "How long have I had it?" is FIFO; "When did I last use it?" is LRU.
Outcome: LRU (last-used) is far better than FIFO (owned-longest); one of her four questions is much
more critical than the others.
Concept Illustrated: FIFO vs. LRU eviction; the hidden non-compatibility of folk advice.
Why This Case Is Useful: A recognizable authority whose advice CS both validates and corrects — a clean
hook for the whole chapter.
Potential for Reuse: High
```

```
Case Title: László Bélády's own "what to keep" story
People / Organization: László "Les" Bélády (IBM)
Context: The father of caching-algorithm research.
What Happened: Fleeing the 1956 Hungarian Revolution, he escaped to Germany with "one change of
underwear and my graduation paper," then reached the US in 1961 with his wife, an infant son, and
"$1,000 in my pocket, and that's it." He went on to define optimal cache eviction.
Outcome: His 1966 paper was the most-cited CS research for fifteen years.
Concept Illustrated: What to keep and what to leave behind — a life that literally rehearsed the
problem.
Why This Case Is Useful: A poignant, ironic biographical hook tying the researcher to his subject.
Potential for Reuse: High
```

```
Case Title: The library's hidden cache (and rough-sorting paradox)
People / Organization: UC Berkeley library system; Beth Dupuis (oversees the process)
Context: The Gardner Stacks hold a locked, "Staff Only" shelf of recently used books by major authors —
the library's cache.
What Happened: Libraries use LRU to decide what to send offsite ("if an item hasn't been used in twelve
years, that's the cutoff"). The chapter-3 "rough-sorting" area holds the most recently used — i.e. the
most-wanted — books, yet staff diligently reshelve them away, arguably making the collection *less*
useful. Meanwhile Moffitt's lobby shows recent *acquisitions* (FIFO).
Outcome: Suggestion to "turn the library inside out": recently returned books in the lobby (LRU),
acquisitions in the back.
Concept Illustrated: LRU vs. FIFO in a physical institution; temporal locality; the cache you're hiding.
Why This Case Is Useful: A vivid, counterintuitive real-world misapplication of caching, with a
concrete fix and a social upside (grassroots "common books").
Potential for Reuse: High
```

```
Case Title: Akamai and the physical internet
People / Organization: Akamai (Massachusetts); chief architect Stephen Ludin
Context: The internet is imagined as placeless "cloud," but is really wires and racks tied to geography.
What Happened: Akamai handles ~a quarter of all internet traffic while staying out of the headlines,
running the largest CDN; content providers pay to be "Akamaized." An Australian streaming the BBC hits
Sydney servers — "the request never makes it to London at all." "Distance matters."
Outcome: A hidden company proving caching is about proximity, not just hardware speed.
Concept Illustrated: Geographic caching / CDNs; the material geography of "the cloud."
Why This Case Is Useful: Surprising scale, a hidden giant, and a quotable design creed.
Potential for Reuse: High
```

```
Case Title: Amazon's warehouses and "anticipatory shipping"
People / Organization: Amazon
Context: How to store and pre-position physical goods.
What Happened: Fulfillment centers deliberately shun human-legible organization — items go "wherever
they can find space" (batteries next to pencil sharpeners, diapers, grills, dobro DVDs), tagged by
barcode — except that high-demand items get a faster-access area: Amazon's cache. Amazon patented
"anticipatory package shipping," which the press misread as mailing items before purchase; it actually
pre-ships regionally popular items to local staging warehouses (a physical CDN), relying on the law of
large numbers.
Outcome: A physical caching system that makes ordered items "just down the street."
Concept Illustrated: Cache + geography + law of large numbers; Bélády-like clairvoyance approximated.
Why This Case Is Useful: Counterintuitive (deliberate disorder is optimal) and connects prediction,
aggregation, and proximity.
Potential for Reuse: High
```

```
Case Title: Netflix and movies set where you live
People / Organization: Netflix; Micah Mertes (2011 map)
Context: When the popular thing in a region is also *from* that region.
What Happened: Mertes's map of state "Local Favorites" showed people overwhelmingly prefer films set
where they live (Seattle's *Singles* in Washington, *L.A. Story* in LA, *Montana Sky* in Montana);
Netflix caches the huge HD files where the fans are — L.A. Story's files live in Los Angeles "just like
its characters."
Outcome: A geography of the cloud that mirrors the geography of taste.
Concept Illustrated: Local caching of large files; demand tied to place.
Why This Case Is Useful: Charming, data-driven, and it makes CDN logic emotionally intuitive.
Potential for Reuse: High
```

```
Case Title: Home caching — vacuum bags behind the couch, and the valet stand
People / Organization: John Hennessy (Stanford president, caching pioneer); a doctor quoted in William
Jones's *Keeping Found Things Found*; Julie Morgenstern's *Organizing from the Inside Out*; Rik Belew
(UC San Diego); Tom Griffiths
Context: Applying caching to physical home organization.
What Happened: Hennessy sees the parallel instantly (desk → files → day-long archive). Advice follows:
use LRU over FIFO (keep the college T-shirt you still wear; ditch the plaid pants); exploit geography
(running gear by the front door; a doctor keeps spare vacuum bags behind the living-room couch because
that's where the vacuum is used); use a multi-level hierarchy. Tom's pile of clothes by the bed (a
disputed but efficient cache) is redeemed by Rik Belew's suggestion of a valet stand — "a one-outfit
closet."
Outcome: "Computer scientists won't only save you time; they might also save your marriage."
Concept Illustrated: LRU eviction, geographic caching, multi-level hierarchy — all at home.
Why This Case Is Useful: Warm, funny, and full of concrete, immediately usable tactics.
Potential for Reuse: High
```

```
Case Title: The Noguchi filing system and the vindicated pile
People / Organization: Yukio Noguchi (economist, University of Tokyo), author of *Super Organized
Method*
Context: A filing method that defies "group like with like."
What Happened: Noguchi files documents in titled/dated folders and always reinserts at the far left
(and searches from the left) — discovered in the early 1990s because returning files to the left was
simply easier. He only later realized it was "startlingly efficient." CS shows it is an instance of
LRU; on its side, the box becomes a pile you search top-down and return to the top.
Outcome: The messy desk pile is "a self-organizing mess" — near-optimal. "You don't need to organize
it. You already have."
Concept Illustrated: LRU / self-organizing lists; provable near-optimality of the pile.
Why This Case Is Useful: A liberating, counterintuitive, guilt-dissolving result with a real theorem
behind it.
Potential for Reuse: High
```

```
Case Title: LRU is already in your interface (Z-order and Alt+Tab)
People / Organization: Aza Raskin (former creative lead for Firefox)
Context: Whether LRU is exotic or something we already live inside.
What Happened: On-screen windows have a "Z-order" (simulated depth) with least-recently-used windows at
the bottom; Windows/Mac task-switchers (Alt+Tab / Command+Tab) list applications most-recently to
least-recently used. Raskin: "Much of your time using a modern browser (computer) is spent in the
digital equivalent of shuffling papers."
Outcome: LRU isn't a proposal to adopt — it's already the invisible logic of everyday computing.
Concept Illustrated: LRU / temporal locality embedded in UI.
Why This Case Is Useful: Shows the abstract policy is intuitive and ubiquitous; a relatable "you're
already doing this" hook.
Potential for Reuse: High
```

```
Case Title: Sort your files by "Last Opened," not "Name"
People / Organization: The authors (chapter footnote)
Context: A directly actionable computer tip — the most usable takeaway in the chapter.
What Happened: Default file browsers force you through folders alphabetically, but LRU implies you should
display files by "Last Opened" instead — "what you're looking for will almost always be at or near the
top." This turns your file browser into a pile.
Outcome: A one-setting change that operationalizes the whole chapter.
Concept Illustrated: LRU / the pile applied to digital files.
Why This Case Is Useful: The single most usable takeaway; perfect Short/tip content.
Potential for Reuse: High
```

```
Case Title: The map on the scale of a mile to the mile
People / Organization: Lewis Carroll (section epigraph)
Context: Framing the CDN/geography section.
What Happened: In Carroll's fable, cartographers make a map "on the scale of a mile to the mile"; the
farmers object it would blot out the sunlight, so "we now use the country itself, as its own map, and it
does nearly as well."
Outcome: A comic proof that a perfect-fidelity copy is as unwieldy as the original — hence you cache
selectively and by proximity.
Concept Illustrated: Why you can't cache everything; the point of a cache is that it's smaller/closer.
Why This Case Is Useful: A memorable literary hook for the whole idea of selective, local caching.
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: The memory hierarchy
Example: The library-plus-desk — check out the books you'll reuse and work at home; the fewer trips
back to the stacks, the faster your week.
Why It Works: Everyone has lived the fast-local/slow-distant tradeoff; it maps cache levels onto a
familiar routine before any hardware is mentioned.
Possible Alternative Domain: Everyday Life
```

```
Concept: LRU as near-clairvoyance
Example: "The nearest thing to clairvoyance is to assume that history repeats itself — backward" — the
next thing you'll need is the last thing you needed.
Why It Works: Compresses the whole eviction result into one memorable, slightly paradoxical maxim.
Possible Alternative Domain: Psychology
```

```
Concept: FIFO vs. LRU
Example: Martha Stewart's "How long have I had it?" (FIFO) vs. "When did I last use it?" (LRU) — keep
the still-worn college T-shirt, ditch the long-unworn plaid pants.
Why It Works: Turns an abstract policy comparison into a wardrobe decision anyone can make, and shows
folk advice contains a hidden bug.
Possible Alternative Domain: Everyday Life
```

```
Concept: Geographic caching
Example: The doctor's spare vacuum-cleaner bags stored *behind the living-room couch* — because that's
where the vacuum is used and where a bag runs out.
Why It Works: A perfect, slightly absurd instance of "store it near where it's used" that overrides
"group like with like."
Possible Alternative Domain: Everyday Life
```

```
Concept: The self-organizing pile
Example: A box of Noguchi files tipped on its side is a pile — search top to bottom, return to the top
— which is exactly LRU, hence within 2× of optimal.
Why It Works: Reframes the guilt-inducing desk pile as a proven near-optimal data structure with a
single vivid transformation.
Possible Alternative Domain: Business
```

```
Concept: Forgetting as optimal tuning
Example: A word is likeliest to appear in tomorrow's NYT headlines right after it last appeared, then
fades — the same curve as Ebbinghaus's recall.
Why It Works: Places two curves side by side (mind and world) so the "optimal tuning" claim is seen,
not just asserted.
Possible Alternative Domain: Psychology
```

```
Concept: Cognitive aging as load, not decay
Example: A 2-year-old knows ~200 words; an adult ~30,000. "It's not that we're forgetting; it's that
we're remembering. We're becoming archives."
Why It Works: A single number contrast reframes a feared decline as an accumulation, and the "archives"
line lands the reinterpretation.
Possible Alternative Domain: Psychology
```

## 9. Counterintuitive Insights

```
Insight: Forgetting is a feature, not a bug — even the ideal memory must fail to retrieve sometimes.
Common Belief: A good memory remembers everything; forgetting is failure.
Author's Argument: Any system managing a vast store must have retrieval failures; keeping unbounded
access is "just too expensive." Forgetting is the price of an optimally organized memory.
Evidence: Anderson & Schooler; the William James epigraph ("forgetting is as important as
remembering").
Why It Is Surprising: It inverts the moralization of memory, making forgetting rational rather than
defective.
```

```
Insight: The best predictor of the future is the recent past, run backward.
Common Belief: Predicting what you'll need requires foresight or sophisticated modeling.
Author's Argument: LRU — assume you'll next need what you just needed — comes closest to clairvoyance
and beats fancier schemes in practice.
Evidence: Bélády's comparisons; Sleator-Tarjan's factor-of-2 guarantee.
Why It Is Surprising: A near-trivial rule (keep what you just used) is provably near-optimal.
```

```
Insight: Your messy pile of papers is already near-optimal.
Common Belief: A pile is chaos and a moral failing; you should file everything neatly.
Author's Argument: Searching top-down and tossing back on top is LRU on a self-organizing list — within
a factor of 2 of clairvoyance. "You don't need to organize it. You already have."
Evidence: Sleator & Tarjan (1985); the Noguchi system.
Why It Is Surprising: It dissolves the guilt of clutter with a theorem, and (unlike chapter 3's
messiness-is-efficient point) says the mess is a *self-organizing* mess — not merely unsorted, but
already arranged near-optimally by the act of use.
```

```
Insight: One setting turns your file browser into a mind-reader.
Common Belief: Files should be browsed alphabetically, by name.
Author's Argument: LRU says display files by "Last Opened," not "Name" — what you want will almost always
be at or near the top, because the recent past predicts the near future.
Evidence: The chapter footnote; the self-organizing-list result.
Why It Is Surprising: A trivial default change operationalizes a deep theorem and beats the built-in
alphabetical ordering everyone accepts.
```

```
Insight: Deliberate disorder can be the optimal storage scheme.
Common Belief: Warehouses (and closets) should be neatly categorized.
Author's Argument: Amazon stores items "wherever there's space" (indexed by barcode) plus a cache for
high-demand items — faster than human-legible organization.
Evidence: Amazon fulfillment centers; the anticipatory-shipping patent.
Why It Is Surprising: The world's most efficient retailer embraces what looks like chaos.
```

```
Insight: The library is hiding its best shelf and eroding it on purpose.
Common Belief: Reshelving returned books is obviously good librarianship.
Author's Argument: Recently returned books are the most likely to be wanted next; the rough-sorting
shelf is therefore the most valuable in the building, yet it's locked away and constantly cleared.
Evidence: Temporal locality; LRU dominance; UC Berkeley practice.
Why It Is Surprising: Diligent tidying actively degrades usefulness; the fix ("turn the library inside
out") is both more efficient and more social.
```

```
Insight: "Cognitive decline" may be learning, not deterioration.
Common Belief: Slower recall with age means the brain is failing.
Author's Argument: Retrieval slows because the store is bigger; older brains solve harder search
problems. "We say 'brain fart' when we should really say 'cache miss.'"
Evidence: Ramscar's simulations; Hennessy on size impairing speed; vocabulary and experience growth
figures.
Why It Is Surprising: It reframes an aging fear as a badge of accumulated knowledge — a lag is "an
indicator of the extent of your experience."
```

```
Insight: Bigger is inherently slower, even with the best hardware.
Common Belief: With enough money you could build one huge, uniformly fast memory and skip caching.
Author's Argument: Size alone impairs speed (bigger city/library/pile = longer search), so you'd still
need caches even with all-SRAM memory.
Evidence: Hennessy; the on-chip L1/L2 caches; SRAM ~1000× flash cost.
Why It Is Surprising: The need for hierarchy is physical/geometric, not merely economic.
```

## 10. Unique or Unusual Ideas

```
Idea: "History repeats itself — backward" as a design principle.
Why It Seems Unique: A crisp inversion of the usual proverb that captures LRU's whole logic — the mirror
image of the past is your best map of the future.
Potential Connection to Other Topics: Forecasting; recency heuristics; base rates; the availability
heuristic.
```

```
Idea: The mind has infinite storage but finite search time.
Why It Seems Unique: It relocates the bottleneck of human memory from capacity to organization/retrieval,
overturning the "running out of space" folk model.
Potential Connection to Other Topics: Information retrieval; the tip-of-the-tongue phenomenon; the
economics of attention.
```

```
Idea: Forgetting is the brain optimally tuned to a forgetting world.
Why It Seems Unique: It grounds a psychological phenomenon (the forgetting curve) in the *external*
statistics of the environment, not internal decay — an ecological-rationality move.
Potential Connection to Other Topics: Ecological rationality (Gigerenzer); Bayesian priors; adaptive
memory.
```

```
Idea: A pile is a provably near-optimal data structure.
Why It Seems Unique: It elevates the archetype of disorganization to a theorem-backed optimum, and
distinguishes "self-organizing mess" from mere mess.
Potential Connection to Other Topics: Self-organizing systems; lazy evaluation; the value of not
pre-optimizing.
```

```
Idea: "The cloud" is intensely geographic.
Why It Seems Unique: It punctures the dominant metaphor — data is placeless — by showing a quarter of
traffic runs through one caching company and files physically live near their fans.
Potential Connection to Other Topics: Infrastructure studies; latency economics; edge computing;
data sovereignty.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: Chapter 3 says "err on the side of messiness"; chapter 4 says the pile is already optimally
organized. Which is it?
Author's Position: The chapter explicitly distinguishes them — chapter 3's point was that sorting isn't
worth the effort; here the reason you needn't organize is different: the pile *is* self-organizing.
Possible Counterargument: The two "don't organize" conclusions rest on different mechanisms (search-sort
tradeoff vs. LRU near-optimality), but a reader could conflate them. The chapter's own sharper framing
is worth preserving: the pile is not merely "already organized" but a *self-organizing mess* — "what
might appear to others to be an unorganized mess is, in fact, a self-organizing mess." The word
"self-organizing" (not just "organized") is doing the work: the act of use keeps arranging it. Still,
the pile's optimality assumes you actually search top-down and return to top, which real desk behavior
may violate.
What Evidence Would Help Resolve It: Observations of how people actually search physical piles vs. the
self-organizing-list model.
```

```
Issue: LRU is "the overwhelming favorite," yet the chapter concedes fancier schemes beat it "under the
right conditions."
Author's Position: LRU is the robust default; frequency-aware and next-to-last-access variants exist and
can win in specific cases.
Possible Counterargument: The life advice ("use LRU") is given without the conditions under which it's
suboptimal — a rarely-used-but-critical item (a passport, a fire extinguisher) is exactly what LRU would
evict. Recency is a poor proxy for importance.
What Evidence Would Help Resolve It: When importance/frequency diverges from recency, and how often that
matters in home vs. machine contexts.
```

```
Issue: Optimality of human forgetting is inferred from curve-matching.
Author's Position: The brain's forgetting schedule mirrors the world's decay schedule, so forgetting is
optimal tuning.
Possible Counterargument: A correlation between two curves doesn't establish that the brain is optimizing
for those statistics; the three corpora (NYT, parent speech, one email inbox) are idiosyncratic and may
not represent "the world." Alternative accounts (decay, interference) aren't ruled out.
What Evidence Would Help Resolve It: Direct tests that manipulating environmental statistics shifts the
forgetting curve as the optimality account predicts.
```

```
Issue: "Cognitive decline is really learning" risks overclaiming.
Author's Position: Age-related lags are "at least partly" the search cost of a bigger store, not
deterioration.
Possible Counterargument: The chapter's own hedge ("at least partly") concedes real decline coexists;
the reassuring framing could be read as denying genuine neurological aging. Simulations of recognition
aren't the same as measured human decline.
What Evidence Would Help Resolve It: Studies separating load-driven slowdown from age-related neural
change in the same individuals.
```

```
Issue: "Turn the library inside out" ignores non-recency reasons for shelving.
Author's Position: Recently returned = most-wanted, so put them in the lobby.
Possible Counterargument: Libraries also serve findability by subject, preservation, and browsing by
topic; an LRU lobby helps serendipity but not a patron seeking a specific unpopular title, and popular
books split between lobby and stacks (the chapter concedes this) could confuse.
What Evidence Would Help Resolve It: A trial measuring retrieval time and patron satisfaction under an
LRU-lobby scheme.
```

```
Issue: The home advice mixes provable results with anecdote.
Author's Position: Apply LRU, exploit geography, use multi-level hierarchies.
Possible Counterargument: LRU has a theorem behind it; "exploit geography" is supported only by
practitioner anecdotes (vacuum bags, running gear), which "consistently turn up" but aren't tested. The
strength of endorsement outruns the evidence for some tactics.
What Evidence Would Help Resolve It: Controlled comparisons of geographic vs. categorical home storage.
```

## 12. Quotable Ideas

```
Paraphrase (short): "In the practical use of our intellect, forgetting is as important a function as
remembering." (William James, epigraph)
Why the Idea Matters: States the chapter's thesis before any computer science — forgetting is a
function, not a failure.
Source Location: Chapter epigraph (PDF p. 112).
```

```
Paraphrase (short): The apparent tidiness of a computer's nested folders hides a highly engineered
chaos underneath — what's really happening is caching.
Why the Idea Matters: Signals that visible organization and underlying efficient organization are
different things.
Source Location: Opening (PDF p. 113).
```

```
Paraphrase (short): The nearest thing to clairvoyance is to assume history repeats itself — backward.
Why the Idea Matters: The chapter's single most memorable line and the essence of LRU.
Source Location: "Eviction and Clairvoyance" (PDF p. 118).
```

```
Paraphrase (short): Turn the library inside out — put recently returned books in the lobby, acquisitions
in the back.
Why the Idea Matters: A concrete, provocative institutional redesign following straight from LRU.
Source Location: "Turning the Library Inside Out" (PDF p. 120).
```

```
Paraphrase (short): "Distance matters" — the cloud is wires and racks, and a quarter of internet
traffic runs through one caching company you've never heard of.
Why the Idea Matters: Punctures the placeless-cloud metaphor and grounds caching in geography.
Source Location: "The Cloud at the End of the Street" (PDF p. 122).
```

```
Paraphrase (short): The big pile of papers on your desk isn't a fester of chaos — it's a self-organizing
mess. You don't need to organize it. You already have.
Why the Idea Matters: The chapter's most liberating claim, backed by the Sleator-Tarjan theorem.
Source Location: "Filing and Piling" (PDF p. 128).
```

```
Paraphrase (short): We say "brain fart" when we should really say "cache miss."
Why the Idea Matters: A one-line reframing of memory lapses as retrieval cost.
Source Location: "The Tyranny of Experience" (PDF p. 134).
```

```
Paraphrase (short): It's not that we're forgetting; it's that we're remembering. We're becoming archives.
Why the Idea Matters: Reinterprets cognitive aging as accumulation, not loss.
Source Location: "The Tyranny of Experience" (PDF p. 133).
```

```
Paraphrase (short): "A lot of what is currently called decline is simply learning." (Michael Ramscar)
Why the Idea Matters: The chapter's consoling, research-anchored thesis about aging minds.
Source Location: "The Tyranny of Experience" (PDF p. 134).
```

```
Paraphrase (short): The length of a retrieval delay is partly an indicator of the extent of your
experience.
Why the Idea Matters: Turns a frustrating lag into evidence of how much you know and how well you've
arranged it.
Source Location: "The Tyranny of Experience" (PDF p. 134).
```

```
Paraphrase (short): "Depend upon it there comes a time when for every addition of knowledge you forget
something that you knew before… not to have useless facts elbowing out the useful ones." (Sherlock
Holmes, epigraph)
Why the Idea Matters: The "limited attic" folk theory of memory the chapter explicitly overturns —
Anderson replaces "running out of space" with "organization, not storage."
Source Location: Epigraph to "Eviction and Clairvoyance" (PDF p. 116).
```

```
Paraphrase (short): They made a map on the scale of a mile to the mile; it would blot out the sun, so
they use the country itself as its own map. (Lewis Carroll, epigraph)
Why the Idea Matters: A perfect-fidelity copy is as unwieldy as the original — the case for caching
selectively and by proximity.
Source Location: Epigraph to "The Cloud at the End of the Street" (PDF p. 121).
```

```
Paraphrase (short): "A big book is a big nuisance." (Callimachus, librarian at Alexandria)
Why the Idea Matters: An ancient statement of "bigger is slower" — a large store is itself a burden.
Source Location: Epigraph to "The Tyranny of Experience" (PDF p. 132).
```

```
Paraphrase (short): Display your files by "Last Opened" rather than "Name" — what you're looking for
will almost always be at or near the top.
Why the Idea Matters: The chapter's single most actionable tip, operationalizing LRU/the pile in one
setting.
Source Location: Footnote (PDF p. 136).
```

## 13. Psychology Connections

- **Memory science.** The chapter is built on core memory research — Ebbinghaus's forgetting curve,
  Anderson's ACT-style adaptive memory, and Ramscar's work on aging and language.
- **Forgetting as adaptive.** Reframes forgetting from failure to optimal management — an
  ecological-rationality stance aligned with Gigerenzer (inference; not named).
- **Tip-of-the-tongue phenomenon.** The "on the tip of the tongue" lag is recast as a cache miss, tying
  a classic memory phenomenon to retrieval cost.
- **Cognitive aging.** A direct, consoling reinterpretation of age-related slowdown as load rather than
  decay — with an explicit hedge that real decline may coexist.
- **The moralization of memory and tidiness.** As in chapter 3, the chapter challenges the guilt
  attached to forgetting and to messy desks, offering permission grounded in math.
- **Recency and availability.** LRU is essentially a recency heuristic; the connection to the
  availability heuristic and recency bias is close (inference).
- **Serendipity and social cognition.** "Turn the library inside out" invokes shared reference points
  and grassroots common culture — social-psychological benefits of a caching redesign.

## 14. Mathematics and Decision Science Connections

- **Optimization under uncertainty.** Bélády's optimal-but-clairvoyant policy vs. the best online
  approximation is a canonical offline-vs-online optimization problem.
- **Competitive analysis / approximation ratios.** Sleator & Tarjan's "within a factor of 2" is a
  competitive-ratio guarantee — worst-case performance relative to the offline optimum.
- **The law of large numbers.** Amazon's anticipatory shipping works because aggregate regional demand
  is predictable even when individual demand isn't.
- **Time-series / decay statistics.** The Ebbinghaus curve and the environmental recurrence curves are
  hazard/decay functions; matching them is a statistical claim about the world.
- **Prediction and recency.** LRU formalizes recency as a predictor; connects to base rates and to
  exponentially weighted forecasting.
- **Cost hierarchies and tradeoffs.** Size-vs-speed and price-per-byte across memory tiers is an
  explicit cost-optimization structure (SRAM ~1000× flash).
- **Geometry of search.** "Bigger is slower" is a claim about search cost scaling with store size —
  linking to the sorting/search complexity of chapter 3.

## 15. Sports Connections

**Direct examples from the book:** None identified. This chapter contains no sports material.

**Inferred applications (mine):**
- **Scouting databases and match prep.** A coaching staff's "cache" should hold the most recently
  relevant opponents/plays at the front (LRU), with deep archives offsite — but note LRU's weakness: a
  rarely faced but decisive opponent (a cup draw against a lower league) is exactly what recency would
  evict, so importance-weighting matters.
- **Muscle memory and skill retrieval.** The forgetting curve and retrieval-cost framing map onto skill
  decay during layoffs and the value of spaced practice to keep key skills "at the front."
- **Home-field / logistics as geographic caching.** Pre-positioning equipment and staff near venues,
  and training-ground layout (most-used gear nearest the pitch), are literal geographic caching.
- **Veteran "slowness" as load.** An experienced player reading more patterns may act on a larger store;
  the Ramscar reframing cautions against mistaking a bigger search space for decline.

## 16. AI and Machine Learning Connections

**Direct from the book:** CDNs, browser/OS/processor caches, and the memory hierarchy are all computing
infrastructure the chapter describes; Anderson's account explicitly imports information-retrieval theory
into cognitive modeling.

**Inferred connections (mine):**
- **KV caching in LLM inference.** Transformer key/value caches are exactly this chapter's idea — keep
  recomputed state close to avoid recomputation; eviction policies for long-context KV caches are an
  active area, and LRU-style and attention-informed eviction are direct analogues.
- **Prompt / embedding / semantic caches.** Caching model responses and retrieved embeddings by
  recency and frequency is LRU/LFU applied to AI serving.
- **Retrieval-augmented generation (RAG).** "Memory as organization, not storage" is the RAG thesis:
  unbounded external store, finite retrieval budget, ranking what to bring to the front of context.
- **The forgetting curve as spaced-repetition and continual learning.** Ebbinghaus underlies
  spaced-repetition algorithms; catastrophic forgetting and replay buffers in continual learning are
  the ML face of "what to keep."
- **Optimality-of-forgetting for memory in agents.** Anderson-style environmental tuning argues agent
  memories should decay on the schedule the environment does — a design principle for long-running
  agents.
- **Edge inference / model caching.** Geographic caching maps onto serving models and content from
  edge nodes near users (latency, the "distance matters" creed).
- **Competitive ratios for online algorithms.** The Sleator-Tarjan factor-of-2 result is foundational
  online-algorithm theory underlying cache-replacement policies in real systems.

## 17. Content Creation Opportunities

```
Idea: Your messy desk is mathematically optimal
Format: YouTube Long-form
Core Concept: Self-organizing lists; the pile as LRU.
Hook: The guilt-inducing pile of papers on your desk is one of the best-designed data structures in
computer science. You don't need to organize it — you already have.
Best Supporting Case: The Noguchi filing system tipped on its side; Sleator & Tarjan's factor-of-2
guarantee.
Psychology Angle: The moralization of tidiness; permission from a theorem.
Math Angle: Competitive ratio / near-optimality vs. clairvoyance.
Sports Angle: None core.
AI Angle: KV caches and RAG as the same "keep what's recent at the front" idea.
```

```
Idea: Your bad memory is a perfectly tuned instrument
Format: YouTube Long-form
Core Concept: The forgetting curve as optimal tuning to the world.
Hook: You're not forgetting because your brain is failing. You're forgetting because the world itself
forgets — on exactly the same curve.
Best Supporting Case: Ebbinghaus + Anderson & Schooler's NYT-headlines / parent-speech / email analysis.
Psychology Angle: Forgetting as adaptive; ecological rationality.
Math Angle: Decay/hazard curves; matching mind to environment.
Sports Angle: Skill decay and spaced practice.
AI Angle: Spaced repetition, continual learning, and agent memory decay.
```

```
Idea: Getting older isn't decline — it's a bigger database
Format: YouTube Long-form
Core Concept: Memory as organization, not storage; the tyranny of experience.
Hook: When you blank on a name, that's not a failing brain. That's a cache miss — and the lag is a
measure of how much you know.
Best Supporting Case: Ramscar's simulations; 200 words at age two vs. 30,000 as an adult; "we're
becoming archives."
Psychology Angle: Reframing cognitive aging as accumulation.
Math Angle: Search cost scaling with store size ("bigger is slower").
Sports Angle: Veteran "slowness" as reading a larger playbook.
AI Angle: Context-window search cost; why bigger stores need better retrieval.
```

```
Idea: The cloud is a lie — the internet has a street address
Format: YouTube Short
Core Concept: Geographic caching / CDNs.
Hook: A quarter of all internet traffic runs through one company you've never heard of — and the movie
you stream tonight is probably cached in your own city.
Best Supporting Case: Akamai ("distance matters"); the Australian who never reaches London; Netflix's
region-set films.
Psychology Angle: How metaphors ("cloud") hide reality.
Math Angle: Latency and proximity; law of large numbers for regional demand.
Sports Angle: Pre-positioning gear/logistics near venues.
AI Angle: Edge inference and model caching.
```

```
Idea: The one closet-cleaning question that actually matters
Format: YouTube Short
Core Concept: LRU beats FIFO for eviction.
Hook: Martha Stewart gives you four questions for what to throw out. Computer science says three of
them are the wrong question.
Best Supporting Case: "How long have I had it?" (FIFO) vs. "When did I last use it?" (LRU); Bélády's
comparison.
Psychology Angle: Why "I've had it forever" is a bad reason to keep — or toss.
Math Angle: FIFO vs. LRU; near-clairvoyance of recency.
Sports Angle: None core.
AI Angle: LRU/LFU in caches; recency vs. frequency eviction.
```

```
Idea: Change one setting and your computer reads your mind
Format: YouTube Short
Core Concept: LRU / the pile applied to files.
Hook: There's a single setting that makes what you're looking for appear at the top of the list almost
every time. Computer scientists have known why for decades.
Best Supporting Case: The "Last Opened" footnote; Z-order and Alt+Tab as built-in LRU.
Psychology Angle: Recency as your best predictor.
Math Angle: Sleator-Tarjan factor-of-2 near-optimality.
Sports Angle: None core.
AI Angle: LRU eviction in real caches; recency vs. frequency.
```

```
Idea: The map the size of the country
Format: YouTube Short
Core Concept: Why you can't cache everything; selective, local caching.
Hook: A map on the scale of one mile to the mile would blot out the sun. That's why "the cloud" keeps a
copy of your favorite movie down the street instead.
Best Supporting Case: Lewis Carroll's fable + Akamai/Netflix geographic caching.
Psychology Angle: Fidelity vs. usefulness; the cost of remembering everything.
Math Angle: Compression and selective retention.
Sports Angle: Pre-positioning logistics.
AI Angle: Why RAG retrieves a few chunks instead of the whole corpus.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B01-C04-01
Title: Caching and the memory hierarchy
Type: Concept
Summary: Fast memory is scarce and expensive, so computers (and minds) use a hierarchy of caches —
small/fast backed by large/slow (Burks, Goldstine & von Neumann, 1946; Atlas 1962; Wilkes; IBM 360/85
coined "cache"). Modern devices have ~6 layers. The library-plus-desk is the everyday analogue.
Source: Algorithms to Live By, ch. 4, "The Memory Hierarchy" (PDF pp. 113–116)
Tags: caching, memory-hierarchy, computing-history, core-concept
Related Concepts: LRU, eviction, memory wall, geographic caching
```

```
CARD ID: B01-C04-02
Title: Bélády's Algorithm — optimal but clairvoyant
Type: Model
Summary: The provably optimal eviction policy is to remove whatever you'll need furthest in the future
(Bélády, 1966 — most-cited CS research for 15 years). It requires "clairvoyance" (future data), so it's
unimplementable; every real policy is judged by how close it comes. The offline ideal is "God's
algorithm."
Source: Algorithms to Live By, ch. 4, "Eviction and Clairvoyance" (PDF pp. 116–117)
Tags: belady, optimal-eviction, clairvoyant, offline-optimum, model
Related Concepts: LRU, cache miss, competitive ratio
```

```
CARD ID: B01-C04-03
Title: LRU — history repeats itself, backward
Type: Model
Summary: Least Recently Used evicts the longest-untouched item and keeps what was used most recently.
It performs closest to clairvoyance (Bélády) because of temporal locality, and is the "overwhelming
favorite" of computer scientists. "The nearest thing to clairvoyance is to assume that history repeats
itself — backward." Fancier schemes can beat it under the right conditions.
Source: Algorithms to Live By, ch. 4, "Eviction and Clairvoyance" (PDF pp. 117–118)
Tags: LRU, temporal-locality, recency, eviction, model
Related Concepts: FIFO, Bélády's Algorithm, self-organizing lists
```

```
CARD ID: B01-C04-04
Title: FIFO vs. LRU — Martha Stewart's incompatible advice
Type: Insight
Summary: "How long have I had it?" is FIFO; "When did I last use it?" is LRU. Bélády's comparison shows
LRU clearly beats FIFO, so two of Stewart's four decluttering questions conflict and one matters much
more. Keep the still-worn college T-shirt (LRU); ditch the long-unworn plaid pants.
Source: Algorithms to Live By, ch. 4, "Eviction and Clairvoyance" (PDF pp. 117–118, 124)
Tags: FIFO, LRU, decluttering, everyday, insight
Related Concepts: Eviction policy, temporal locality
```

```
CARD ID: B01-C04-05
Title: Just having a cache helps at all
Type: Claim
Summary: A startling early result: even Random Eviction is "not half bad" — merely having a cache makes
a system more efficient regardless of policy, because frequently used items return to it soon anyway.
Source: Algorithms to Live By, ch. 4, "Eviction and Clairvoyance" (PDF pp. 117–118)
Tags: caching, random-eviction, robustness, claim
Related Concepts: LRU, FIFO, temporal locality
```

```
CARD ID: B01-C04-06
Title: Turn the library inside out
Type: Insight
Summary: Recently returned books are the most likely to be checked out next (temporal locality), so the
locked "rough-sorting" shelf holds the building's most-wanted books — yet staff reshelve them away.
Libraries use LRU for offsite cutoffs (UC Berkeley: 12 years unused). Fix: put recently returned books
in the lobby (LRU), acquisitions in the back — more efficient and more socially positive.
Source: Algorithms to Live By, ch. 4, "Turning the Library Inside Out" (PDF pp. 119–121)
Tags: LRU, libraries, temporal-locality, redesign, insight
Related Concepts: FIFO (acquisitions display), serendipity, rough-sorting (ch. 3)
```

```
CARD ID: B01-C04-07
Title: The cloud is geographic — Akamai and CDNs
Type: Case
Summary: Caching works when proximity, not speed, is scarce. Akamai (Massachusetts) handles ~a quarter
of internet traffic via the largest CDN; an Australian streaming the BBC hits Sydney, "never London."
"Distance matters." The placeless "cloud" is really wires, racks, and geography.
Source: Algorithms to Live By, ch. 4, "The Cloud at the End of the Street" (PDF pp. 121–122)
Tags: CDN, Akamai, geographic-caching, internet-infrastructure, case
Related Concepts: Memory hierarchy, edge computing, proximity
```

```
CARD ID: B01-C04-08
Title: Amazon's disorder + anticipatory shipping
Type: Case
Summary: Fulfillment centers shelve items "wherever there's space" (barcode-indexed) — except
high-demand items get a fast-access cache. Amazon's "anticipatory package shipping" patent pre-ships
regionally popular items to local staging warehouses (a physical CDN), relying on the law of large
numbers so an ordered item is "just down the street."
Source: Algorithms to Live By, ch. 4, "The Cloud at the End of the Street" (PDF pp. 122–123)
Tags: Amazon, geographic-caching, law-of-large-numbers, deliberate-disorder, case
Related Concepts: CDN, Bélády clairvoyance approximated, cache
```

```
CARD ID: B01-C04-09
Title: Netflix — people love movies set where they live
Type: Case
Summary: Micah Mertes's 2011 map of state "Local Favorites" found people overwhelmingly prefer
region-set films (Washington → Singles, LA → L.A. Story, Montana → Montana Sky). Netflix caches the
huge HD files where the fans are — L.A. Story's files live in Los Angeles. (Oddity: My Own Private Idaho
is best loved in Maine.)
Source: Algorithms to Live By, ch. 4 (PDF pp. 123–124)
Tags: Netflix, local-caching, geography-of-taste, case
Related Concepts: CDN, large-file caching, proximity
```

```
CARD ID: B01-C04-10
Title: Home caching — geography and multi-level hierarchy
Type: Case
Summary: Apply LRU (keep what you still use), and "exploit geography" — store things in the cache
nearest where they're used: running gear by the front door; a doctor's spare vacuum bags behind the
living-room couch. Use a multi-level hierarchy (closet → basement → storage), evicting downward by LRU.
A valet stand is a tiny fast cache — "computer scientists might also save your marriage."
Source: Algorithms to Live By, ch. 4, "Caching on the Home Front" (PDF pp. 124–125)
Tags: home-organization, geographic-caching, multi-level, LRU, case
Related Concepts: Hennessy, memory hierarchy, eviction
```

```
CARD ID: B01-C04-11
Title: The Noguchi filing system = LRU
Type: Model
Summary: Yukio Noguchi files documents in titled/dated folders and always reinserts at the far left,
searching from the left — deliberately not grouping by content. Discovered because left-return was
simply easier; it's an unwitting implementation of LRU on a self-organizing list, so most-used files
migrate to the fast end.
Source: Algorithms to Live By, ch. 4, "Filing and Piling" (PDF pp. 125–127)
Tags: Noguchi, filing, LRU, self-organizing-lists, model
Related Concepts: The pile, Sleator-Tarjan, temporal locality
```

```
CARD ID: B01-C04-12
Title: Your pile is a self-organizing near-optimal structure
Type: Claim
Summary: Sleator & Tarjan (1985) proved that reinserting a found item at the front of a linearly
searched list (LRU) keeps total search time within a factor of 2 of the offline optimum — a guarantee
no other algorithm makes. A pile is a Noguchi box on its side (search top-down, return to top), so the
messy desk pile is "a self-organizing mess." "You don't need to organize it. You already have."
Source: Algorithms to Live By, ch. 4, "Filing and Piling" (PDF pp. 126–128)
Tags: self-organizing-lists, Sleator-Tarjan, competitive-ratio, the-pile, claim
Related Concepts: Noguchi, LRU, messiness (ch. 3, different mechanism)
```

```
CARD ID: B01-C04-13
Title: The forgetting curve
Type: Study
Summary: Hermann Ebbinghaus (1879) memorized nonsense syllables daily and self-tested, establishing
that repetition aids persistence and recall declines with time along "the forgetting curve" —
founding a quantitative science of memory. Its *meaning* stayed a mystery for a century.
Source: Algorithms to Live By, ch. 4, "The Forgetting Curve" (PDF pp. 128–129)
Tags: Ebbinghaus, forgetting-curve, memory-science, study
Related Concepts: Anderson & Schooler, temporal locality, spaced repetition
```

```
CARD ID: B01-C04-14
Title: Memory mirrors the world's decay (Anderson & Schooler)
Type: Study
Summary: John Anderson (1987) reframed memory as organization, not storage — infinite capacity, finite
search time. With Lael Schooler he analyzed NYT headlines, parent-child speech, and his own email:
a word is likeliest to recur right after use and fades over time, matching the Ebbinghaus curve. So
forgetting is an optimal tuning of the brain to the environment, not a defect.
Source: Algorithms to Live By, ch. 4, "The Forgetting Curve" (PDF pp. 128–131)
Tags: Anderson, Schooler, adaptive-memory, ecological-rationality, study
Related Concepts: Forgetting curve, memory-as-organization, temporal locality
```

```
CARD ID: B01-C04-15
Title: Cognitive "decline" is largely learning
Type: Claim
Summary: Size alone impairs speed (Hennessy: bigger city/library/pile = slower search). Ramscar's
Tübingen simulations show that knowing more makes recognizing words/names/letters harder regardless of
organization. A 2-year-old knows ~200 words, an adult ~30,000; each year adds ~⅓ million waking minutes.
"A lot of what is currently called decline is simply learning" — but the authors hedge "at least
partly."
Source: Algorithms to Live By, ch. 4, "The Tyranny of Experience" (PDF pp. 131–134)
Tags: aging, Ramscar, retrieval-cost, cognitive-load, claim
Related Concepts: Memory-as-organization, tip-of-the-tongue, "bigger is slower"
```

```
CARD ID: B01-C04-16
Title: Brain fart = cache miss
Type: Insight
Summary: "We say 'brain fart' when we should really say 'cache miss.'" A memory lag is retrieval cost,
and its length is partly an indicator of the extent of your experience; the rarity of lags shows how
well you've arranged your memory — most important things closest to hand. "It's not that we're
forgetting; it's that we're remembering. We're becoming archives."
Source: Algorithms to Live By, ch. 4, "The Tyranny of Experience" (PDF pp. 133–134)
Tags: memory-lag, reframing, aging, quotable, insight
Related Concepts: Cognitive load, tip-of-the-tongue, cache miss
```

```
CARD ID: B01-C04-17
Title: Bigger is inherently slower
Type: Insight
Summary: Even with unlimited money for the fastest memory, you'd still need caches, because size alone
impairs speed — a bigger city, library, or paper pile takes longer to search. This is why processors
carry both an L1 and an L2 cache on the chip. The need for a hierarchy is geometric, not just economic.
SRAM costs ~1000× flash per byte.
Source: Algorithms to Live By, ch. 4, "The Tyranny of Experience" (PDF pp. 131–132)
Tags: memory-hierarchy, search-cost, scale, Hennessy, insight
Related Concepts: Memory wall, sorting/search scaling (ch. 3), caching
```

```
CARD ID: B01-C04-18
Title: László Bélády's "what to keep" life
Type: Case
Summary: The father of caching-algorithm research fled the 1956 Hungarian Revolution with "one change
of underwear and my graduation paper," reaching the US in 1961 with his wife, an infant son, and "$1,000
in my pocket, and that's it." He then defined optimal cache eviction — a life that literally rehearsed
what to keep and what to leave behind.
Source: Algorithms to Live By, ch. 4, "Eviction and Clairvoyance" (PDF pp. 116–117)
Tags: Belady, biography, what-to-keep, irony, case
Related Concepts: Bélády's Algorithm, eviction
```

```
CARD ID: B01-C04-19
Title: Sort files by "Last Opened," not "Name"
Type: Insight
Summary: The chapter's most actionable tip: override your file browser's default alphabetical ordering
and display files by "Last Opened" instead — LRU implies what you want will almost always be at or near
the top. LRU is already built into interfaces (window Z-order, Alt/Command+Tab list most-to-least
recent; Aza Raskin: using a browser is "the digital equivalent of shuffling papers").
Source: Algorithms to Live By, ch. 4 (footnote, PDF p. 136; Z-order PDF p. 118)
Tags: LRU, actionable-tip, files, UI, insight
Related Concepts: The pile, self-organizing lists, temporal locality
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: Fast memory is always scarce, so computers and minds alike are organized as caching
hierarchies whose hard problem is what to keep close and what to evict. The optimal rule (evict what
you'll need furthest in the future) needs clairvoyance; the best real substitute is LRU — assume the
near future mirrors the recent past. Extended outward, caching reorganizes closets, warehouses, and the
geography of the internet, and reinterprets human forgetting and "cognitive decline" as the retrieval
cost of a memory optimally tuned to a world that itself forgets on the same curve.

Top 5 Concepts:
1. Caching and the memory hierarchy
2. Bélády's optimal (clairvoyant) eviction and the offline optimum
3. LRU and temporal locality ("history repeats itself — backward")
4. Self-organizing lists / the pile as near-optimal (Sleator-Tarjan factor of 2)
5. Memory as organization not storage; the forgetting curve as optimal environmental tuning

Top 3 Claims:
1. LRU (and minor tweaks thereof) is the best practical eviction policy because the recent past predicts
   the near future — though fancier frequency-aware schemes can beat it under the right conditions, and
   recency is a poor proxy for importance (a rarely used but critical item — a passport — is exactly
   what LRU would evict).
2. A messy pile is a provably near-optimal self-organizing structure — you needn't organize it.
3. Human forgetting and age-related lags are largely retrieval cost of an optimally tuned, ever-growing
   memory, not decay.

Top 3 Cases:
1. The Noguchi filing system / the vindicated desk pile
2. Akamai and Amazon's anticipatory shipping — geographic caching at internet and warehouse scale
3. "Turn the library inside out" — LRU vs. FIFO in a physical institution

Top 3 Studies:
1. Bélády (1966) — optimal eviction and the dominance of LRU
2. Sleator & Tarjan (1985) — self-organizing lists within a factor of 2 of clairvoyance
3. Anderson & Schooler — the forgetting curve mirrors the world's decay statistics (with Ebbinghaus 1879
   as origin and Ramscar on aging)

Most Unique Idea: Human forgetting is not a flaw but the brain optimally tuned to an environment whose
own reference frequencies fade exactly like the Ebbinghaus curve — an ecological explanation of memory.

Most Counterintuitive Idea: Your messy pile is already near-optimally organized (within 2× of
clairvoyance), and "cognitive decline" may be learning — a lag is a measure of how much you know.

Biggest Weakness or Open Question: The optimality-of-forgetting claim is inferred from curve-matching on
three idiosyncratic corpora rather than demonstrated; LRU is recommended for life without flagging that
recency is a poor proxy for importance (a rarely used passport is exactly what LRU evicts); and the
"decline is learning" reframing is hedged to "at least partly," conceding real neural aging it doesn't
measure.

Best Content Opportunity: A long-form video on "your messy desk is mathematically optimal" (Noguchi +
Sleator-Tarjan), paired with the memory reframing ("cache miss," "we're becoming archives") for an
emotionally resonant close about forgetting and aging.
```
