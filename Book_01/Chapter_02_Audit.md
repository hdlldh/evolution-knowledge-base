# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 2: Explore/Exploit — The Latest vs. the Greatest
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 47–78, re-read against Chapter_02_Extraction.md
**Date:** 2026-07-19

---

## Missing Items

**1. The Pirsig frame — "What's new?" versus "What's best?"** (PDF p. 47) The chapter opens its
intellectual argument with Robert Pirsig's *Zen and the Art of Motorcycle Maintenance* (1974), which
decries the conversational opener "What's new?" as producing "only an endless parade of trivia and
fashion, the silt of tomorrow," and endorses "What's best?" as vastly superior. The authors then
rebut him: every "best" song and restaurant you have began as something merely "new" to you, so
there may be yet-unknown bests still out there. **This is the chapter's thesis in miniature, stated
as a disagreement with a named author, and the extraction omitted it entirely.** It is also the
chapter's clearest cross-book collision point — an explicit argument against a canonical text.

**2. The Lydia Davis epigraph.** (PDF p. 75, epigraph to "… And Exploit") Davis describes reaching a
juncture in her reading life: in the time left to her, should she read more and more new books, or
"cease with that vain consumption—vain because it is endless—and begin to reread those books that had
given me the intensest pleasure in my past." This is a first-person statement of the interval problem
by a writer, positioned exactly where the chapter turns to aging. Highly reusable and completely
absent from the extraction.

**3. The Carpe Diem material.** (PDF p. 50) The "Seize the Interval" section opens on Robin Williams
in *Dead Poets Society* (1989) — "Seize the day, boys. Make your lives extraordinary" — and the
authors call the advice "incredibly important" but "somewhat self-contradictory," since seizing a day
and seizing a lifetime are entirely different endeavors. They then propose an inverse to "Eat, drink,
and be merry, for tomorrow we die": *"Start learning a new language or an instrument, and make small
talk with a stranger, because life is long, and who knows what joy could blossom over many years'
time."* That invented aphorism is the single most quotable sentence in the section and the extraction
dropped it.

**4. The statistics-as-shared-standard defense of conventional trials.** (PDF p. 70) After the ECMO
sequence the authors write that part of what statistics did for medicine at the start of the
twentieth century was "to transform it from a field in which doctors had to persuade each other in ad
hoc ways about every new treatment into one where they had clear guidelines about what sorts of
evidence were and were not persuasive. Changes to accepted standard statistical practice have the
potential to upset this balance, at least temporarily." **This is the chapter's own steelman of the
resistance to adaptive designs, and the extraction omitted it** — which made §3 and §9 read as more
one-sided against conventional trials than the chapter actually is. The most consequential omission
in this audit.

**5. "Decisions are almost never isolated."** (PDF p. 50) "People tend to treat decisions in
isolation, to focus on finding each time the outcome with the highest expected value. But decisions
are almost never isolated, and expected value isn't the end of the story." This is a distinct
foundational claim — the reason the whole bandit apparatus is needed — and it appears in the
extraction only implicitly inside the 1–1 versus 9–6 card. It deserves its own entry in §3.

**6. The Sinatra and Churchill epigraphs.** (PDF pp. 59–60) "Regrets, I've had a few. But then again,
too few to mention" (Frank Sinatra) and "For myself I am an optimist. It does not seem to be much use
being anything else" (Winston Churchill) frame the regret/optimism section. Churchill's line in
particular is a pre-mathematical statement of exactly what UCB proves.

**7. The chapter's stated roadmap.** (PDF p. 50) Explore/exploit "provides fundamental insights into
how our goals should change as we age, and why the most rational course of action isn't always trying
to choose the best. And it turns out to be at the heart of, among other things, web design and
clinical trials—two topics that normally aren't mentioned in the same sentence." Worth recording as
the authors' own account of the chapter's scope, and the "web design and clinical trials" pairing is
a ready-made hook.

**8. The evolutionary mismatch note.** (PDF p. 73) Alongside Warhol's "A Coke is a Coke," the authors
write that "having instincts tuned by evolution for a world in constant flux isn't necessarily helpful
in an era of industrial standardization," and use the image of a berry patch ripe one week and rotten
the next. The extraction captured the Warhol line in a card but dropped the evolutionary argument —
which is directly relevant to this knowledge base's evolution/behaviour theme and is the chapter's
only explicit evolutionary-mismatch claim.

**9. The footnote pun.** (PDF p. 78) The section's summary footnote: "git while the Gittins's good."
Trivial in content, but it is the chapter's only joke of that kind and worth a line in §12.

**10. The two aphorisms quoted in full.** (PDF p. 48) "Make new friends, but keep the old / Those are
silver, these are gold" and "There is no life so rich and rare / But one more friend could enter
there." The extraction paraphrased the authors' *response* to these (that aphorisms never give the
ratio) without recording the aphorisms themselves, which are the concrete objects the argument is
about.

## Corrections Needed

**1. The Meyer & Shi finding is mislabelled as over-exploration support.**
- Extraction (§3, §5, card 17): lists it under "people tend to over-explore."
- Chapter (PDF pp. 71–72): participants "tended to use the untried airline too little when it was
  good and too much when it was bad," and failed to make clean breaks.
The extraction *does* flag this as two-sided in the limitations field, but it still sits under the
over-exploration claim in three places. The chapter's own justification for counting it is narrower:
it is the *failure to break cleanly* and the continued alternation that indicate over-exploration,
not the two-sided misuse. That reasoning should be stated rather than left implicit.

**2. "The interval makes the strategy" — the chapter's causal claim about Carstensen is narrower than
the extraction implies.**
- Extraction (§3): "Social preferences track perceived interval, not age as such."
- Chapter (PDF p. 76): "these differences in social preference are not about age as such—they're
  about where people perceive themselves to be on the interval relevant to their decision."
These match, but the extraction elsewhere (§19, card 20) uses the manipulations to describe the
result as experimentally causal about interval. The manipulations are *imagined* scenarios; they
establish that manipulating perceived interval shifts stated preference in a hypothetical choice, not
that real interval changes drive real network pruning. The extraction's own limitations field says
this; the summary sections should not overstate it.

**3. Bellman's date is left vaguer than necessary.**
- Extraction (§5): "Not specified (post-WWII era)."
The chapter says the first steps came "in the years after the war," attributes Win-Stay Lose-Shift to
Robbins with a 1952 proof, and then says "researchers made significant progress over the next few
years" before introducing Bellman. So the chapter implies the 1950s. `Not specified.` remains the
correct entry for the year, but the sequencing should be noted rather than lost.

## Overgeneralizations

**1. "The Gittins index completely solves the multi-armed bandit."** The extraction says this in §3,
§4 and card 5 before the qualification arrives. The chapter's actual sentence is that it "completely
solves the multi-armed bandit **with geometrically discounted payoffs**." The extraction carries the
qualifier in most places but card 5's summary states the solution first and the condition second,
which is the order most likely to be misread in a cross-book comparison.

**2. "People over-explore" as a settled finding.** §19 lists it among top claims without the
qualifications the body carries. The evidence is one 1966 study with an unusual design that forbids
learning from your own bets, one 1990s study with two-sided results, and one strategy-classification
study over fifteen pulls with unstated sample size. The direction is consistent; the strength is not
what the summary implies.

**3. "In the long run, optimism is the best prevention for regret."** Reported in the extraction as an
insight and a quotable without noting that the chapter's regret theorems concern *algorithms choosing
among arms with stationary payoffs*, not dispositions toward people. The chapter makes the leap in one
sentence ("it clearly has implications for human lives as well"); the extraction should preserve the
visible seam rather than smoothing it.

**4. The restless bandit's intractability is stated more flatly than the chapter warrants.** Extraction
(§3, card 18): "no tractable algorithm... and it is believed there never will be." The chapter says
exactly this, with no citation — so the extraction is faithful, but it should be marked as an asserted
negative result. A reader comparing against another book's treatment of non-stationary bandits needs
to know this came with no support attached.

## Important Nuance Lost

**1. The interval is genuinely unclear in the medical case.** (PDF p. 54) The chapter notes that for
drug companies and doctors "it's not entirely clear what the relevant interval ought to be" — companies
want to exist forever, and a medical breakthrough could help people not yet born, yet the present is
weighted more heavily. This is precisely why Gittins reframed the problem in terms of discounting
rather than a horizon. The extraction records the discounting move but not the motivating difficulty,
which is what makes the reframing non-arbitrary.

**2. Exploitation is where connoisseurship pays off.** (PDF p. 49) The Plagenhoef material contains a
sharper point than "exploration is tiring": when you constantly have to explore, "you can never enjoy
the fruits of your connoisseurship." Expertise is only cashed in during exploitation. The extraction
has the commitment device but not this idea, which is the chapter's implicit argument for why a life
of pure exploration is impoverished rather than merely exhausting.

**3. The chapter hedges the segment-level A/B explanations.** (PDF pp. 63–64) The reasons offered for
why PLEASE DONATE or CONTRIBUTE won are marked "perhaps appealing to their guilt" and "the logic being
perhaps that…" The extraction notes this in the limitations field but reproduces the explanations
confidently in the case entry and card 12. The hedges should survive.

**4. "Only in exceptional cases does a trial get stopped early."** (PDF p. 67) A small parenthetical
that matters: conventional trials are not entirely inflexible, and the chapter acknowledges the
existence of stopping rules before arguing they are insufficient. Dropping it makes the conventional
design sound more rigid than the chapter says it is.

**5. ECMO's own risks and the negative adult studies.** The extraction captures both (embolism risk;
"early studies in adults showed no benefit compared to conventional treatments") in the case entry,
but neither appears in card 16 or in §9's "the standard clinical trial may be the less ethical design"
insight. Anyone reusing the card alone would get a one-sided picture: the strongest argument for
randomizing was precisely that the adult evidence pointed the other way.

## Additional Cases and Examples

```
Case Title: Pirsig's "What's best?" — and the authors' rebuttal
People / Organization: Robert Pirsig, *Zen and the Art of Motorcycle Maintenance* (1974)
Context: Pirsig objects to the conversational opener "What's new?" and endorses "What's best?" instead.
What Happened: He argues that pursuing "What's new?" exclusively "results only in an endless parade of
trivia and fashion, the silt of tomorrow." The authors counter that every "best" song and restaurant
among your favourites began humbly as something merely "new" to you — so there may be yet-unknown
bests still out there, and the new deserves at least some of our attention.
Outcome: The chapter's founding argument, framed as a disagreement with a named literary authority.
Concept Illustrated: Why pure exploitation is self-undermining; the necessity of exploration for
exploitation to have anything to work with.
Why This Case Is Useful: A named, canonical opponent to argue against, which is far more engaging than
arguing against a generic intuition. It is also the chapter's clearest external disagreement and
should feed the book profile's cross-book comparison.
Potential for Reuse: High
```

```
Case Title: Lydia Davis on rereading
People / Organization: Lydia Davis (epigraph)
Context: Epigraph to "… And Exploit," the section on aging.
What Happened: Davis describes a familiar juncture in a reading life: with limited time left, should
she read more and more new books, or "cease with that vain consumption—vain because it is endless—and
begin to reread those books that had given me the intensest pleasure in my past."
Outcome: N/A — a statement of the dilemma, not a resolution.
Concept Illustrated: The interval, articulated from the inside by someone living it; the finite
lifetime as the binding constraint on exploration.
Why This Case Is Useful: The most affecting statement of the chapter's central idea, and it arrives
from literature rather than mathematics — ideal for opening or closing a piece on the topic.
Potential for Reuse: High
```

```
Case Title: Carpe diem is self-contradictory
People / Organization: Robin Williams in *Dead Poets Society* (1989); the authors
Context: Opening the "Seize the Interval" section.
What Happened: Against "Seize the day, boys. Make your lives extraordinary," the authors observe that
seizing a day and seizing a lifetime are entirely different endeavors. They propose an inverse to
"Eat, drink, and be merry, for tomorrow we die": "Start learning a new language or an instrument, and
make small talk with a stranger, because life is long, and who knows what joy could blossom over many
years' time."
Outcome: A reframing of famous advice as interval-dependent rather than universally correct.
Concept Illustrated: That inherited wisdom encodes a particular interval and is wrong outside it.
Why This Case Is Useful: A recognizable cultural touchstone turned into a teaching example, plus an
original aphorism that works as a standalone quote or a video ending.
Potential for Reuse: High
```

```
Case Title: The berry patch and the Coke
People / Organization: Andy Warhol (quoted); the authors
Context: Assessing how much the restless-bandit problem actually bites in modern life.
What Happened: "A berry patch might be ripe one week and rotten the next, but as Andy Warhol put it,
'A Coke is a Coke.'" The authors add that "having instincts tuned by evolution for a world in constant
flux isn't necessarily helpful in an era of industrial standardization."
Outcome: An argument that modern payoffs are unusually stationary, so the classical algorithms transfer
better than they otherwise would.
Concept Illustrated: Evolutionary mismatch; non-stationarity as a feature of ancestral rather than
industrial environments.
Why This Case Is Useful: The chapter's only explicit evolutionary-mismatch claim, and directly on-theme
for a knowledge base about evolution and decision-making. Also a neat two-image contrast.
Potential for Reuse: High
```

## Additional Research Evidence

None identified. The re-read surfaced no study, dataset, or citation absent from §5. What it did
surface is that several §5 entries rest on thinner support than their prominence in the chapter
suggests — specifically Kaelbling's optimistic robots (no results reported), the restless-bandit
intractability claim (no citation), the "$57 million" figure (no methodology), and the behavioral
economics literature on non-geometric discounting (referenced as "a variety of experiments" with no
names). Those are correctly marked in the extraction; the pattern across them is worth noting for the
book profile.

## Potential Disagreements to Track Later

1. **Robert Pirsig, *Zen and the Art of Motorcycle Maintenance*.** The chapter explicitly argues
   against Pirsig's preference for "What's best?" over "What's new?" This is a live, named
   disagreement — the only one of its kind so far in the book — and belongs in the profile's
   cross-book section.
2. **Barry Schwartz and the choice-overload literature (again).** Chapter 1 collided with it via
   pool-size invariance; chapter 2 collides differently, arguing novelty-seeking is rational. Track
   whether the book ever engages the satisfaction costs of exploration directly — so far it treats
   exploration's cost as forgone payoff only, never as decision fatigue, which the chapter's own
   opening paragraph vividly describes and then never returns to.
3. **Hyperbolic discounting (Ainslie, Laibson, Thaler).** The chapter concedes people don't discount
   geometrically and proceeds anyway. Any book arguing from hyperbolic discounting will produce
   different numbers from the same framework.
4. **Gigerenzer on ecological rationality.** The Steyvers finding that 47% of people use Win-Stay
   Lose-Shift would be read by Gigerenzer as evidence of an adaptive heuristic, not a shortfall from
   optimality — the same partial alignment flagged in chapter 1's audit, now with a concrete data
   point to test it against.
5. **Randomized controlled trial orthodoxy (Cochrane tradition, evidence-based medicine).** The
   chapter's adaptive-trial argument is a minority position within a field that treats the RCT as
   foundational. The chapter reports the counterarguments fairly, but a cross-book comparison against
   any evidence-based-medicine text will be sharp.
6. **Socioemotional selectivity vs. disengagement theory.** The chapter names the traditional
   decline-based explanation of shrinking networks only to dismiss it; it does not cite or engage its
   proponents.
7. **Research ethics on live experimentation.** The chapter draws the A/B-testing/clinical-trial
   parallel and then declines to apply the Belmont standards to A/B testing. Any book on tech ethics
   will press exactly there.

## Additional Content Opportunities

```
Idea: "What's new?" vs "What's best?" — the argument at the heart of every recommendation feed
Format: YouTube Long-form
Core Concept: Pirsig's objection and the authors' rebuttal
Hook: A famous philosopher said asking "what's new?" gives you nothing but "the silt of tomorrow." He
was wrong, and the math shows why: every favourite you have was once merely new.
Best Supporting Case: Pirsig's *Zen and the Art of Motorcycle Maintenance* against the Gittins
exploration bonus.
Psychology Angle: Nostalgia and the sense that things used to be better; the paradox that your canon
was built by the behaviour you now disdain.
Math Angle: Pure exploitation starves itself — you can only exploit what exploration found.
Sports Angle: A club that never bloods youth eventually has no veterans worth exploiting.
AI Angle: Recommender systems that collapse into filter bubbles are exploiting a set exploration built.
```

```
Idea: Carpe diem is bad advice — or rather, it's advice for one specific day
Format: YouTube Short
Core Concept: Inherited wisdom encodes an interval
Hook: "Seize the day" and "life is long, go learn an instrument" are opposite advice. Both are right.
The math tells you which one applies to you today.
Best Supporting Case: The Dead Poets Society scene against the authors' invented inverse aphorism.
Psychology Angle: Why the same advice inspires one person and misleads another.
Math Angle: Exploration value falls with remaining time; exploitation value rises.
Sports Angle: "Leave everything out there" is correct in a final, disastrous in preseason.
AI Angle: Annealing an exploration schedule instead of fixing it.
```

```
Idea: The defence nobody makes for boring old randomized trials
Format: Community Post
Core Concept: Statistics as a shared standard of persuasion
Hook: Before statistics, doctors argued about every new treatment ad hoc. The rulebook people are now
attacking is the thing that ended that.
Best Supporting Case: The chapter's own concession (PDF p. 70) placed against the ECMO death counts.
Psychology Angle: Institutional trust as a coordination device rather than mere conservatism.
Math Angle: Why changing accepted statistical practice has costs beyond the individual trial.
Sports Angle: None identified.
AI Angle: Benchmarks as shared evidentiary standards, and what breaks when everyone uses their own.
```

---

## Recommended Changes to the Original Extraction

1. **§7 (Cases and Stories)** — add the four cases above: Pirsig's "What's best?", the Lydia Davis
   epigraph, the Carpe Diem/Dead Poets material, and the berry patch/Coke evolutionary-mismatch
   passage. Pirsig is the highest-value addition; it is the chapter's founding argument and the
   extraction had no trace of it.

2. **§3 (Key Claims)** — add a new claim: "Decisions are almost never isolated, and expected value
   isn't the end of the story." Type: Theoretical. Evidence: the 1–1 vs. 9–6 comparison. Strength:
   Strong (definitional to the model class). This is the premise the whole chapter rests on and it was
   only implicit.

3. **§3 and §11** — add the chapter's steelman of conventional trials: statistics transformed medicine
   from ad hoc persuasion into shared evidentiary standards, and changing accepted practice risks
   upsetting that balance. Without it the extraction misrepresents the chapter as one-sided.

4. **§9 (Counterintuitive Insights)** — amend "The standard clinical trial may be the less ethical
   design" to carry (a) the statistics-as-shared-standard counterargument, (b) ECMO's own risks
   including embolism, and (c) the fact that early adult studies showed no benefit — which is the
   strongest reason randomization was defensible.

5. **§3, card 5** — reorder the Gittins claim so the condition precedes the result: "Under geometric
   discounting, the Gittins index completely solves the multi-armed bandit."

6. **§3, §5, card 17** — state the chapter's actual reasoning for counting Meyer & Shi as
   over-exploration evidence: it is the failure to break cleanly and the continued alternation, not
   the two-sided misuse.

7. **§4 (Gittins index limitations)** — add the motivating difficulty: for drug companies and doctors
   the relevant interval is genuinely unclear (an indefinite future, but with the present weighted
   more heavily), which is *why* Gittins reframed the problem as discounting rather than a horizon.

8. **§12 (Quotable Ideas)** — add Churchill ("It does not seem to be much use being anything else"),
   the authors' invented inverse aphorism ("Start learning a new language or an instrument…"), Pirsig's
   "the silt of tomorrow," and the footnote pun "git while the Gittins's good."

9. **§2 or §7 (Plagenhoef)** — add the sharper point: constant exploration means "you can never enjoy
   the fruits of your connoisseurship." Expertise is only cashed in during exploitation.

10. **§7 and card 12** — restore the authors' hedges on the A/B segment explanations ("perhaps
    appealing to their guilt," "the logic being perhaps that…").

11. **§13 (Psychology Connections)** — add decision fatigue. The chapter's opening paragraph is a
    vivid description of choice exhaustion ("You're already exhausted before you get to the first
    bite") and the chapter never returns to it, treating exploration's cost purely as forgone payoff.
    That gap is worth recording.

12. **§14 or §16** — add the evolutionary-mismatch claim: instincts tuned for a world in constant flux
    are not necessarily helpful under industrial standardization. On-theme for this knowledge base and
    currently absent.

13. **§19 (Cross-Book Summary)** — soften "people over-explore" to reflect the actual evidence base,
    and add Pirsig to the disagreements the book profile will need.

**Sections that are fine as they stand:** §1 (thesis), §6 (experiments — the alternative-explanation
fields are doing real work, particularly the non-stationarity reading of the airline alternation),
§10 (unique ideas), §15 (sports — correctly identifies the rookie/veteran line as the one direct
example), §17 (content opportunities), and §18 cards other than 5, 12, 16 and 17.
