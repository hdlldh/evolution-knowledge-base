# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 3: Sorting — Making Order
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 79–111, re-read against Chapter_03_Extraction.md
**Date:** 2026-07-20

---

## Missing Items

**1. The Robert Cawdrey epigraph (1604) — the first English dictionary.** (PDF p. 79) The chapter opens
with Cawdrey's *A Table Alphabeticall* instructions on how to use alphabetical order ("if thy word
beginne with (ca) looke in the beginning of the letter (c)…"). This is not decoration: it dates the
*need to teach people what sorted order even is* to 1604, when alphabetization was novel enough to
require instructions. A strong, reusable historical hook that the extraction omitted entirely.

**2. The 2013 Stack Overflow sock debate.** (PDF pp. 79–80) A question about how to sort socks, posted
to Stack Overflow in 2013, "prompted some twelve thousand words of debate." A concrete, quotable data
point about how genuinely unsettled even trivial sorting is among experts — omitted.

**3. Two vivid Hollerith-era quotations.** (PDF pp. 80–81) The awestruck observer — the machine "works
as unerringly as the mills of the Gods, but beats them hollow as to speed" — and the wrong prediction
that "as no one will ever use it but governments, the inventor will not likely get very rich," which
Hollerith *clipped and saved*. The extraction has the prediction paraphrased but drops the "mills of
the Gods" line, which is the more reusable of the two.

**4. Sorting is analyzed as "glimpsing God's blueprints" — the metaphysics framing.** (PDF pp. 87–88)
Before Mergesort, the authors reframe "is faster sorting possible?" as a question "closer to
metaphysics — akin to thinking about the speed of light, time travel, superconductors, or
thermodynamic entropy… What is the minimum effort required to make order?" This is the chapter's
statement of *why lower bounds matter* — that computer scientists are probing fundamental limits of
the universe, not just productivity. A significant framing the extraction flattened into "proven lower
bound."

**5. The IBM 1936 "collators."** (PDF pp. 88–89) The extraction jumps from Hollerith to von Neumann,
but the chapter's actual bridge is IBM's 1936 line of "collators" that merged two already-sorted card
stacks in linear time. This is the physical ancestor of Mergesort's merge step and the reason
Mergesort "was hiding in plain sight." Worth its own line in §5.

**6. The riffle-shuffle image.** (PDF p. 89) Mergesort's final merge is described as "like a riffle
shuffle's order-creating twin." A neat teaching image (a shuffle that creates rather than destroys
order) that the extraction dropped.

**7. The boxing double-bronze footnote, and Bradáč's underwater handcuff record.** (PDF pp. 108, 110)
Two footnotes: in boxing, two bronzes are sometimes awarded because it is "medically unsafe for a
boxer to fight again after being recently knocked out"; and Bradáč "can escape from three pairs of
handcuffs while underwater in roughly the same amount of time" as his card record. The boxing detail
sharpens the noise/robustness point (the format bends to physical reality); the Bradáč detail is a
reusable aside. Both omitted.

**8. Steve Whittaker's timing detail.** The extraction notes the 1996 "email overload" paper "before
many people even had email," but frames it only parenthetically; the chapter uses it to establish
Whittaker as having studied personal information management "for almost two decades." Minor, but the
authority-establishing detail matters for how much weight the study carries.

**9. "We search with our quick eyes and sort with slow hands."** (PDF p. 95) This specific asymmetry
— the reason searching is cheap and sorting is dear for physical objects — is the mechanism behind the
bookshelf verdict, and it is a genuinely quotable line. The extraction states the bookshelf conclusion
but drops this crisp causal phrasing. Added to §12 candidates.

## Corrections Needed

**1. The parallelized Mergesort is domestic, not just industrial.**
- Extraction (§4, card 5): frames Mergesort's parallelizability as the "pizza party" for a bookshelf.
This is accurate, but the extraction's §4 "When It Is Useful" says "large-scale industrial sorting,"
while the chapter explicitly says Mergesort "also has real applications in small-scale domestic
sorting problems" *because* it parallelizes. The domestic use is a distinct point, not just a cute
illustration.

**2. "Star sorter" Jordan Ho aims for ~25 books, not the 150-book cart, before final ordering.**
- Extraction (§6, Jordan Ho): says "gather ~25 books, then finish with an Insertion Sort" — correct —
but also says "A cart of 150 books in under 40 minutes," which could read as if he Insertion-Sorts 150
at once. The chapter is explicit: the 150-book cart is bucket-sorted down, and he does the final
Insertion Sort on groups of ~25. The extraction's field ordering slightly blurs this; worth tightening.

**3. The 52-mile figure is Doe and Moffitt Libraries specifically.**
- Extraction (§6) attributes "52 miles of shelving" to the setup generally. The chapter locates it at
UC Berkeley's Doe and Moffitt Libraries. Minor attribution precision.

## Overgeneralizations

**1. "Fully sorting cannot be done in fewer than O(n log n)" — scope of the proof.** The extraction
(§3) does say "applies only to comparison-based, full-ordering sorts" in the limitations field, which
is correct. But the headline claim as stated ("a fundamental law of the universe, and there are no two
ways around it" — the chapter's own words) is immediately *circumvented* by Bucket Sort on the next
page. The extraction should make explicit that the "law" holds only for comparison sorts, so the
Bucket Sort result isn't read as a contradiction. Currently the two claims sit adjacent without the
reconciling clause foregrounded.

**2. "The single most robust sorting algorithm known."** The chapter says Comparison Counting Sort is
"the single most robust sorting algorithm known, quadratic or better." The extraction reproduces
"single most robust known" but occasionally drops the "quadratic or better" qualifier (e.g. card 12).
The qualifier matters — it is not claiming robustness beats all conceivable algorithms, only within
the practical class considered.

**3. Round-Robin/ladder game counts for 64 teams.** The extraction gives "63 rounds (2,016 games)" for
a ladder or round-robin. The chapter's 2,016 is the round-robin pairing count (64×63/2). Calling it
"63 rounds" conflates the ladder's round structure with the round-robin's game count; the chapter's
own text lists both together but they are different objects. Worth a note so the numbers aren't
misattributed.

## Important Nuance Lost

**1. Big-O ignores constant factors — the "three-month remodel" example.** (PDF p. 85) The extraction
mentions this in §4 but it deserves emphasis: Big-O treats "passing the roast once" and "remodeling
your dining room for three months and then passing the roast once" as *equivalent*, because for large
n any linear term swamps any constant. This is the single most counterintuitive property of Big-O and
the extraction states it without the concrete, memorable example that makes it land.

**2. The distribution-knowledge requirement is the whole point of Bucket Sort, and it's a Bayesian
hook.** The extraction captures that buckets must be well-chosen, but the deeper point — that beating
the linearithmic barrier *requires knowing the distribution the items are drawn from* — is a direct
bridge to chapter 6 (Bayes) and to priors generally. The extraction notes it in §14 but under-weights
it as the *mechanism*, not just a caveat.

**3. "The verdict is clear" bookshelf conclusion is explicitly hedged to *most domestic* shelves.**
(PDF p. 95) The chapter says "for most domestic bookshelves, almost none of the conditions that make
sorting worthwhile are true," and lists the conditions (rare search, low unsorted-search cost, small
sorted-vs-unsorted time gap). The extraction gives the conclusion but not the explicit condition-list,
which is what makes the advice falsifiable/applicable rather than a blanket "don't sort."

**4. Aggression subsides "after a period of some weeks."** The extraction has this, but the *reason it
matters* — it "corroborat[es] the idea that the group is sorting itself," because a completed sort
should end the fighting — is the actual evidentiary logic and should be foregrounded, not just noted.

**5. NCAA seeding footnote is stronger evidence than the body text.** (PDF p. 111) The seeding
mitigation is in a footnote, and the "16-seed has never beaten a 1-seed in March Madness history" is
presented as evidence that seeding "appears to be reliable at least in the most extreme case." The
extraction has the fact but not the framing that it is offered as *empirical validation of a
noise-mitigation design*, which is a nice closed loop (noise → design response → evidence).

## Additional Cases and Examples

```
Case Title: A Table Alphabeticall (1604) — teaching people what "sorted" means
People / Organization: Robert Cawdrey, first English dictionary
Context: The chapter's epigraph.
What Happened: Cawdrey's 1604 dictionary opens with instructions on how to *use* alphabetical order,
because readers couldn't be assumed to know it: "if thy word beginne with (ca) looke in the beginning
of the letter (c) but if with (cu) then looke toward the end of that letter."
Outcome: Documentary evidence that sorted order was once a novel technology requiring a manual.
Concept Illustrated: Sorting as invisible-but-learned infrastructure ("what is water?").
Why This Case Is Useful: A striking historical hook — the idea that alphabetical order once needed
explaining — for any piece on how sorting became invisible.
Potential for Reuse: High
```

```
Case Title: IBM's 1936 collators — Mergesort hiding in plain sight
People / Organization: IBM
Context: The physical bridge between punch-card sorting and Mergesort.
What Happened: In 1936 IBM produced "collators" that merged two already-sorted card stacks into one in
linear time — compare the two top cards, move the smaller, repeat. Von Neumann's 1945 program took this
"to its beautiful and ultimate conclusion."
Outcome: The merge operation existed in hardware a decade before Mergesort was written as code.
Concept Illustrated: Mergesort's merge step; the linear-time merge of sorted stacks.
Why This Case Is Useful: Grounds an abstract algorithm in a physical machine and shows theory
formalizing existing practice.
Potential for Reuse: Medium
```

```
Case Title: The boxing double-bronze exception
People / Organization: Olympic boxing
Context: A footnote on why some sports award two bronzes.
What Happened: Because it is "medically unsafe for a boxer to fight again after being recently knocked
out," boxing sometimes awards two bronze medals rather than holding a third-place match.
Outcome: A sport bending its sorting format to physical/medical reality.
Concept Illustrated: Real constraints override the tidy tournament sort; a concrete face of the
noise/robustness theme.
Why This Case Is Useful: A surprising rules-trivia hook that reinforces "formats aren't pure sorts."
Potential for Reuse: Medium
```

## Additional Research Evidence

None fully missing, but two §5 entries should be sharpened rather than added:
- **The comparison-sort lower bound** should be explicitly tagged as information-theoretic and
  comparison-restricted, so its circumvention by Bucket Sort reads as changing the problem, not
  breaking a law.
- **The hen agonistic-behavior studies** remain unnamed in the chapter; the extraction correctly marks
  them `Not specified`, but the audit confirms there is no citation to recover — this is a genuine
  evidentiary thinness, not an extraction gap.

## Potential Disagreements to Track Later

1. **Goodhart's law / metric gaming.** The chapter praises cardinal benchmarks (money, GDP, tonnage)
   as violence-avoidance but only glances at their pathologies. Any book on metrics, incentives, or
   measurement (e.g. Muller's *The Tyranny of Metrics*) will collide here — the ordinal→cardinal move
   that averts fights also enables Goodhart-style gaming and legitimizes unjust orders.
2. **The moralization of tidiness (Marie Kondo, organizing culture).** "Err on the side of messiness"
   directly contradicts the popular decluttering/organizing movement; a sharp, marketable cross-book
   tension.
3. **Meritocracy critiques.** "The rat race is a race, not a fight" frames cardinal ranking as
   civilizational progress; critics of meritocracy (Sandel, Markovits) would read the same benchmark
   as manufacturing new forms of hierarchy and resentment. The chapter even concedes people "resent the
   basis of this hierarchy" — an opening to track.
4. **Dominance vs. prestige hierarchies (Henrich, anthropology).** The chapter treats hierarchy as
   dominance (fighting/displacement); the prestige-hierarchy literature argues human status often works
   by freely conferred deference, not contest — a substantive alternative model to track against the
   pecking-order framing.
5. **Animal-welfare science on beak-trimming.** The debeaking claim is deduced, not evidenced; the
   actual welfare literature is mixed and will either support or complicate it.

## Additional Content Opportunities

```
Idea: Alphabetical order used to come with an instruction manual
Format: YouTube Short
Core Concept: Sorting as invisible, learned infrastructure
Hook: In 1604, the first English dictionary had to teach people how to use alphabetical order. They'd
never seen it before.
Best Supporting Case: Cawdrey's A Table Alphabeticall; "search engines are really sort engines."
Psychology Angle: How thoroughly we internalize invented conventions ("what is water?").
Math Angle: Sorted lists as the universal interface.
Sports Angle: None identified.
AI Angle: Ranking as the default UI of information systems.
```

```
Idea: The most important skill in poker is knowing how good you are
Format: YouTube Short
Core Concept: Self-assessment as the key to decentralized sorting
Hook: The best cash-game poker players say the #1 skill isn't playing well — it's accurately rating
yourself. Get it wrong and you go broke.
Best Supporting Case: Haxton on heads-up no-limit; the macaque displacement parallel.
Psychology Angle: Calibration and self-knowledge; Dunning-Kruger.
Math Angle: Dominance hierarchies as information hierarchies (Flack).
Sports Angle: Seat-jockeying as a bottom-up sorting algorithm.
AI Angle: Confidence calibration in models; knowing what you don't know.
```

---

## Recommended Changes to the Original Extraction

1. **§7 (Cases and Stories)** — add three cases: Cawdrey's *A Table Alphabeticall* (1604), IBM's 1936
   collators, and the boxing double-bronze exception. Cawdrey is the highest-value addition — a
   memorable historical hook the first pass missed entirely.

2. **§3 and §4** — make the comparison-sort lower bound's scope explicit *at the claim*, not only in a
   limitations field: it is an information-theoretic bound for comparison-based full sorts, which is
   exactly why Bucket Sort can beat it by changing the problem. Prevents the adjacent claims from
   reading as a contradiction.

3. **§4 (Mergesort) / §3** — record that Mergesort's parallelizability gives it *domestic* as well as
   industrial use (the pizza party is a real application, not just an illustration).

4. **§4 (Big-O)** — add the "three-month remodel then pass the roast once ≈ passing the roast once"
   example as the concrete face of "linear swamps constant." It is Big-O's most counterintuitive
   property.

5. **§3 / §9 (messiness)** — add the explicit condition-list for when sorting *isn't* worth it (rare
   search, cheap unsorted search, small time gap, quick eyes vs. slow hands), so the advice is
   applicable rather than blanket.

6. **§6 (Jordan Ho)** — tighten so it is unambiguous that he bucket-sorts the 150-book cart down to
   groups of ~25 and Insertion-Sorts those, not the whole cart; attribute the 52 miles to Doe and
   Moffitt.

7. **§5 (Whittaker)** — carry the "almost two decades" authority detail into the study entry, not just
   the coined-term aside.

8. **§12 (Quotable Ideas)** — add "we search with our quick eyes and sort with slow hands," the "mills
   of the Gods" Hollerith line, and the metaphysics framing ("glimpsing God's blueprints… what is the
   minimum effort required to make order?").

9. **§3 / §5 (championship noise)** — flag more explicitly that the 70% figure is an *assumption* and
   Murphy's soccer model is unspecified, so the "near-random" conclusion is not overstated. (The
   extraction notes this; the audit asks it be foregrounded given the claim's rhetorical weight.)

10. **§11 (Tensions)** — add the NCAA seeding footnote as a *resolution attempt* to the Single
    Elimination brittleness problem (noise → seeding → the 16-vs-1 evidence), closing a loop the body
    leaves open.

11. **§13 / §16** — strengthen the distribution-knowledge point: beating the linearithmic barrier
    *requires knowing the input distribution*, an explicit bridge to Bayesian priors (ch. 6) and to
    distribution shift in ML.

**Sections that are fine as they stand:** §1 (thesis), §8 (teaching examples), §10 (unique ideas),
§15 (sports — genuinely the richest applied section and accurately captured), §17 (content
opportunities), and §18 cards other than 5 and 12 (which need the qualifier tightening above).
