# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 8: Relaxation — Let It Slide
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 220–235, re-read against Chapter_08_Extraction.md
**Date:** 2026-07-21

---

## Missing Items

**1. The Princess Bride epigraph — "I do not think it means what you think it means."** (PDF p. 230) The
"Just a Speeding Ticket" section opens with Vizzini's "Inconceivable!" and Inigo Montoya's rejoinder.
This is not decoration: the whole Lagrangian point is that "the inconceivable" becomes merely "the
undesirable" — the epigraph literally sets up "downgrading the impossible to costly." The extraction
captured the Voltaire epigraph but dropped this one, which is the more on-theme of the two. The chapter
even echoes it later: Lagrangian Relaxation turns "the inconceivable to the undesirable."

**2. The section title pun "Uncountably Many Shades of Gray."** The Continuous Relaxation section's
title is a math joke (continuous = uncountably many values / shades of gray between the discrete
either/or). Worth noting as the chapter's framing of discrete-vs-continuous, and a reusable hook.

**3. Merrill Flood's cross-chapter link.** (PDF p. 223) The chapter explicitly reminds the reader that
Merrill Flood — who lodged the TSP in his brain from Whitney's 1934 talk and spread it at RAND — "is
also credited with circulating the first solution to the secretary problem" (chapter 1) and, from
chapter 1, the 37% Rule and possibly coining "software." The extraction names Flood but drops the
deliberate callback, which is a genuine cross-book/cross-chapter thread the knowledge base should track.

**4. Lenstra's "serious enemy, but you still have to fight it."** (PDF p. 224) Jan Karel Lenstra's line
— "When the problem is hard, it doesn't mean that you can forget about it… It's a serious enemy, but you
still have to fight it" — is the emotional hinge between "the problem is intractable" and "so relax it."
The extraction omitted it entirely; it's a strong, quotable statement of the chapter's core stance
(neither toil nor surrender).

**5. The Arnold Palmer example is the cleanest teaching image and belongs in the concept, not only §8.**
(PDF p. 233) "When deciding between iced tea and lemonade, first imagine a 50–50 'Arnold Palmer' blend
and then round it up or down" is the chapter's own one-line definition of Continuous Relaxation. The
extraction has it in §8 but the recap in "Learning to Relax" gives the crispest three-technique
summary (Constraint = remove; Continuous = Arnold Palmer; Lagrangian = penalties), which is worth
preserving as a unit.

**6. "Impossibility results would also be valuable" (Flood, 1956).** (PDF p. 223) The extraction quotes
Flood's "no general method" but the second half — that a proof of impossibility "would also be valuable"
— is a notable methodological point (a negative result is real progress), and it foreshadows the P vs.
NP framing. Worth keeping.

**7. The footnote's precise polynomial-vs-exponential crossover.** (PDF p. 235) The footnote gives a
concrete, teachable detail: O(2ⁿ) with a small base overtakes even n¹⁰ "if you're sorting more than
several dozen items," and the polynomial/exponential chasm is "the field's de facto out-of-bounds
marker." The extraction has the gist in §3/card 3 but the "several dozen items" concreteness and the
explicit tie-back to sorting (ch. 3, where O(n²) was odious but here counts as efficient) is a nice
cross-chapter nuance.

## Corrections Needed

**1. The dominating set / set cover naming is the audit's, not the book's.**
- Extraction (§4, §5, card 6, card 11): labels the party-invitation problem "dominating set" and the
  fire-truck problem "set cover." The chapter does *not* use these technical names — it describes the
  structures ("the smallest subgroup of your friends that knows all the rest"; "the minimal set of
  locations such that all houses are covered") without naming them. The extraction should mark these as
  the extractor's identification, not the book's terminology, to keep the "what the author says vs. what
  I inferred" separation clean.

**2. Bellows's scoring — the "10" is the sister's special prerogative, applied to whomever she wants.**
- Extraction (§5, §7) has this right ("sister-of-bride prerogative = 10"), but the phrasing should be
  precise: the sister could "give a score of 10 to all the people she wanted to sit with" — it's a
  one-person override, not a general couple/relationship tier. Minor, but keep it exact.

**3. The 0.05% Earth-scale result is "to within less than 0.05% of the (unknown) optimal solution."**
- Extraction (card 5, §7) says "to within 0.05%." The chapter says "less than 0.05%," and crucially the
  optimum is *unknown* — the bound is what makes the 0.05% claim meaningful (you know you're within
  0.05% without knowing the optimum). Keep "unknown" attached; it's the whole epistemic point.

## Overgeneralizations

**1. "Most computer scientists believe none exists" is stated as near-certainty in places.** The
extraction (§1, §3) is mostly careful, and §11 flags P vs. NP as open — good. But card 2 ("most believe
none exists") and the thesis lean toward treating intractability as settled. The chapter is explicit
that this is belief, not proof ("have not yet been definitively proven to be either efficiently solvable
or not"), and that Flood thought an impossibility *result* was still needed. Carry the "not proven"
qualifier wherever the strong claim appears.

**2. Continuous Relaxation's "at most twice as many" is specific to the invitation/covering structure.**
The extraction mostly scopes this correctly, but the guarantee ("at most twice as many invitations as
the brute-force optimum") is a property of that particular rounding on that problem class, not a general
law of continuous relaxation. The fire-truck version is "within a comfortable bound," not the same 2×.
Keep the two bounds distinct and problem-specific.

**3. Lagrangian "every rule is a cost you can pay" as life philosophy.** The extraction (§9, §10, §11)
already flags the tension, but the framing in card 7 and the content ideas is punchy enough that the
descriptive-not-normative caveat ("there are consequences" describes, it doesn't license) should ride
with the strong statements. The book presents it as empowering; it doesn't adjudicate which rules are
okay to break.

## Important Nuance Lost

**1. Relaxation's *two* distinct advantages are enumerated by the chapter.** (PDF p. 234) The chapter
explicitly lists them: (1) a bound on the quality of the true solution (the "teleport" fantasy shows 8
one-hour meetings is the daily max — an *upper* bound on what's achievable), and (2) relaxations
designed to be reconciled with reality give bounds *from the other direction* (round fractional vaccines
→ "at worst twice as many"). The extraction captures both in card 10 but the chapter's own explicit
enumeration ("For one… Second…") is worth preserving as a clean two-part structure.

**2. The minimum spanning tree has an alternative, more intuitive definition.** (PDF p. 225) The chapter
offers two ways to see it: the TSP relaxed to allow free revisiting, *and* "the fewest miles of road
needed to connect every town to at least one other town." The extraction has both, but the second
(connection, not routing) is the more intuitive entry point and should be foregrounded for teaching.

**3. Constraint Relaxation's life mantras are a *set*, and their variety is the point.** (PDF p. 227)
The chapter lists several — "What would you do if you weren't afraid? … if you could not fail? … if you
won the lottery? … if all jobs paid the same?" — each relaxing a *different* constraint (fear, failure,
money, income equality). The extraction lists them but the point that each removes a different constraint
(and thus models a different idealization) is the reusable insight.

**4. "Not necessarily the optimum matchup. But it's close."** (PDF p. 231) The chapter's exact framing
of Trick's schedules — every televised game is "not necessarily the optimum matchup, but it's close" —
is a memorable, concrete statement of "good enough at industrial scale" that the extraction paraphrases
but could quote more sharply.

## Additional Cases and Examples

```
Case Title: "Inconceivable!" — the impossible becomes the undesirable
People / Organization: The Princess Bride (Vizzini and Inigo Montoya, epigraph)
Context: The epigraph to the Lagrangian Relaxation section.
What Happened: Vizzini keeps calling things "Inconceivable!"; Inigo replies, "I do not think it means
what you think it means." The chapter uses this to frame Lagrangian Relaxation, which "turns the
inconceivable to the undesirable" — what looked impossible is really just costly.
Outcome: A pop-culture setup for the core Lagrangian move.
Concept Illustrated: Lagrangian Relaxation; reclassifying the impossible as merely expensive.
Why This Case Is Useful: A widely-recognized, funny hook that makes "downgrade the impossible to costly"
instantly memorable.
Potential for Reuse: High
```

```
Case Title: Merrill Flood, the connective tissue of hard problems
People / Organization: Merrill Flood
Context: A recurring figure across the book's hard-problem chapters.
What Happened: Flood absorbed the traveling salesman problem from Whitney's 1934 Princeton talk, spread
it at RAND, and is *also* credited (ch. 1) with circulating the first solution to the secretary problem
and the 37% Rule — and possibly with coining the word "software."
Outcome: One mathematician links the secretary problem (ch. 1) and the traveling salesman problem
(ch. 8) — the two emblematic hard problems of the book.
Concept Illustrated: The mid-20th-century emergence of algorithmic thinking; cross-chapter thread.
Why This Case Is Useful: A human throughline connecting the book's two most famous problems, good for a
"cast of characters" content angle.
Potential for Reuse: Medium
```

## Additional Research Evidence

None materially missing. The re-read confirms the evidentiary base — the TSP history (Menger through
Karp), the Cobham–Edmonds thesis, Bellows's wedding computation, and Trick's sports scheduling — is
captured. One sharpening: Flood's "impossibility results would also be valuable" should be recorded as a
methodological point (negative results are progress), and the P-vs-NP openness kept attached to every
"most believe none exists" claim.

## Potential Disagreements to Track Later

1. **P vs. NP resolution.** The chapter's entire practical program assumes hard problems are permanently
   hard. A future P = NP proof would overturn "relax instead of optimize"; the chapter honestly flags this
   as belief, and any complexity-theory text will engage the open question.
2. **The ethics of "every rule is a cost you can pay."** Legal/moral philosophy would push hard on
   treating law as a Lagrangian penalty; a cross-book collision with any deontological ethics or
   rule-of-law argument. The chapter is descriptive; critics would call it corrosive.
3. **Optimization vs. satisficing (Simon, again).** "Perfect is the enemy of the good" and "how close
   can you get?" are satisficing by another route; a natural alliance with Herbert Simon and a tension
   with pure-optimization traditions — recurring across chs. 1, 7, 8.
4. **Exact solvers and modern hardware.** Practitioners note that many "intractable" instances (including
   large TSPs) are now solved exactly by branch-and-bound/cutting-plane solvers; the chapter's "beyond
   reach" framing is worst-case asymptotic, and a cross-reference to real solver performance would
   complicate it.

## Additional Content Opportunities

```
Idea: "Inconceivable!" — the math of impossible problems
Format: YouTube Short
Core Concept: Lagrangian Relaxation reclassifies the impossible as merely costly.
Hook: "You keep using that word. I do not think it means what you think it means." Computer scientists
agree: most "impossible" constraints are really just expensive ones.
Best Supporting Case: The Princess Bride epigraph; Brian's mother; playing past curfew.
Psychology Angle: Reframing the impossible as a price.
Math Angle: Lagrangian Relaxation; constraints into penalties.
Sports Angle: Salary caps as relaxable penalties.
AI Angle: Soft constraints and penalty terms in constrained optimization.
```

```
Idea: The one mathematician behind computer science's two hardest problems
Format: YouTube Short
Core Concept: Merrill Flood's throughline (secretary problem + traveling salesman problem).
Hook: One man circulated both the "when to stop dating" formula and the "shortest possible road trip"
problem — and maybe coined the word "software."
Best Supporting Case: Flood at RAND; the 37% Rule (ch. 1); the TSP (ch. 8).
Psychology Angle: How ideas spread through a small community.
Math Angle: The secretary problem and the traveling salesman problem as the two emblematic hard problems.
Sports Angle: None core.
AI Angle: The mid-century roots of algorithmic thinking.
```

---

## Recommended Changes to the Original Extraction

1. **§12 (Quotable Ideas)** — add the Princess Bride epigraph ("I do not think it means what you think it
   means" / "the inconceivable to the undesirable") and Lenstra's "It's a serious enemy, but you still
   have to fight it." Both are high-value; Lenstra's is the emotional hinge of the chapter and was
   omitted entirely.

2. **§7 (Cases and Stories)** — add the Princess Bride "inconceivable" framing and the Merrill Flood
   cross-chapter throughline (secretary problem ↔ TSP).

3. **§4, §5, card 6, card 11** — mark "dominating set" and "set cover" as the extractor's identification,
   not the book's terminology (the chapter describes but doesn't name these problems).

4. **§3 / card 2 / §1** — carry the "not proven" qualifier with every "most believe none exists"
   statement; add Flood's point that an impossibility *result* "would also be valuable" (negative results
   are progress).

5. **card 5 / §7** — restore "less than 0.05%" and, crucially, that the optimum is *unknown* (the bound
   is what makes the number meaningful).

6. **§4 / §5 (MST)** — foreground the more intuitive definition ("fewest miles of road to connect every
   town to at least one other") alongside the "TSP with free revisiting" one.

7. **§2 / §4 (Constraint Relaxation mantras)** — note that the life mantras each relax a *different*
   constraint (fear / failure / money / income equality), which is the reusable insight.

8. **card 10 / §4** — preserve the chapter's explicit two-part enumeration of relaxation's advantages
   (an upper bound on what's achievable; a reconcilable-with-reality bound from the other direction).

9. **card 6** — keep the two continuous-relaxation bounds distinct: "at most twice as many" for
   invitations/vaccines, "within a comfortable bound" for fire trucks — not one general guarantee.

10. **footnote / §3** — add the "several dozen items" crossover concreteness and the cross-chapter tie
    that O(n²), odious in sorting (ch. 3), counts as efficient here.

**Sections that are fine as they stand:** §1 (thesis), §6 (experiments — the alternative-explanation
correctly notes a smarter algorithm would beat brute-force churning, which is the chapter's own point),
§8 (teaching examples), §9 (counterintuitive insights), §10 (unique ideas), §14 (mathematics — the LP
relaxation / Lagrangian duality / randomized rounding mappings are precise), §15 (sports — Trick is a
genuinely central direct example and the inferred applications are well-separated), §16 (AI — the
randomized-rounding and constrained-RL mappings are strong).
