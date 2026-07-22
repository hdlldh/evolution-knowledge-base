# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 5: Scheduling — First Things First
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 137–167, re-read against Chapter_05_Extraction.md
**Date:** 2026-07-21

---

## Missing Items

**1. The Eugene Lawler epigraph — scheduling theory defeated its own theorist.** (PDF p. 137) The
chapter's second epigraph is Lawler's own rueful line: "'Why don't we write a book on scheduling
theory?' I asked… 'It shouldn't take much time!'… Fifteen years later, *Scheduling* is still
unfinished." This is a self-demonstrating joke — the world's leading scheduling expert catastrophically
mis-scheduled a book *about scheduling* — and it foreshadows both intractability and the Lawler/Lenstra
material. The extraction used the Dillard epigraph but dropped this one, which is more thematically
load-bearing.

**2. The Aristotle "we are what we repeatedly do" opening.** (PDF p. 137) The Monday-morning setup
quotes Aristotle ("We are what we repeatedly do") to frame scheduling as identity-forming, not clerical
— tying directly to the Dillard "how we spend our days is how we spend our lives" thesis. Minor but
reinforces the stakes.

**3. The Lao Tzu epigraph on doing hard things while small.** (PDF p. 142) "Do the difficult things
while they are easy and do the great things while they are small" frames "Getting Things Done." A
quotable that anticipates both SPT and precedence logic.

**4. The Ellen Ullman / needlepoint / Social Network / Kipling epigraphs.** The back half is studded
with framing quotes the extraction omitted: "The hurrieder I go / The behinder I get" (Boonville
needlepoint, framing the context-switch section); Ellen Ullman on why programmers must not be
interrupted ("Interruptions mean certain bugs… You must not get off the train"); the *Social Network*
"You have the minimum amount [of my attention]" framing thrashing; and Kipling's "If—" ("fill the
unforgiving minute / With sixty seconds' worth of distance run"), which the authors explicitly rebut
("If only. The truth is, there's always overhead"). The Kipling rebuttal in particular is a distinct
argumentative move — inherited time-management wisdom ignores overhead — that the extraction lost.

**5. The "one watch / two watches" proverb.** (PDF p. 144) "A man with one watch knows what time it
is; a man with two watches is never sure" opens "Picking Our Problems" and is the compression of the
whole metric-choice lesson (multiple objectives leave you unsure what optimal even means). The
extraction references metric-choice heavily but dropped this memorable framing.

**6. The UI-hypocrisy footnote.** (PDF p. 167) A pointed aside: computers "brashly pop up error
messages and cursor-stealing dialogue boxes" — "the user interface demands the user's attention in a
way that the CPU itself would rarely tolerate." This is a sharp, reusable critique of notification
design that complements the app-badge material and the interrupt-coalescing prescription.

**7. The specific psychophysics detail on redrawing the mouse.** (PDF pp. 160–161) The chapter's
concrete mechanism — OS programmers mine psychophysics papers for the exact millisecond threshold at
which a human registers lag/flicker, and attend to the user no more often than that, "redrawing the
mouse just in time" — is a vivid, teachable instance of responsiveness-vs-throughput that the
extraction generalized away.

**8. The "the machine scheduling and the machine scheduled are the same" point.** (PDF pp. 153–154)
The chapter makes an explicit structural observation: for people and OSes alike, the scheduler and the
scheduled are one machine, so "straightening out your to-do list [is] an item *on* your to-do list."
This self-reference is a distinct idea (planning competes with doing) that the extraction only implies.

## Corrections Needed

**1. The productivity anecdote is "more than twice as productive," attributed to a friend — keep it
anecdotal.**
- Extraction (§3, card 13): "16-hour days more than twice as productive as 8-hour days." Correct, but
  it should stay clearly marked as one software friend's self-report (PDF p. 154), not a measured
  finding — the extraction's §3 lists it among "evidence" without foregrounding that it is anecdote.

**2. The Linux minimum slice figure.**
- Extraction (§3, card 16): "Linux ~0.75 ms." The chapter says "about three-quarters of a millisecond"
  (PDF p. 159). Accurate, but it is the *minimum useful slice*, not the slice size in general — worth
  keeping the "minimum" qualifier attached so it isn't read as a typical quantum.

**3. "Answer in random order" is regime-specific (thrashing only).**
- Extraction handles this in §11 but card 15 presents "answer emails in random/on-screen order" fairly
  baldly. The chapter is explicit that this applies only *in a thrashing state* — "even doing tasks in
  the wrong order is better than doing nothing at all." The card should carry the "only when thrashing"
  condition so it isn't reused as general advice.

## Overgeneralizations

**1. Weighted SPT as "skeleton key" — the multi-metric optimality is conditional.** The chapter says
it minimizes the weighted completion times and, "under certain assumptions," the sum of weights of late
jobs and the weighted lateness of those jobs (PDF pp. 152–153). The extraction preserves the "under
certain assumptions" hedge in most places, but §19's top-claims and the §2 concept entry lean toward
presenting it as broadly optimal. The hedge should travel with every strong statement of the skeleton
key, because the very same section stresses that most metrics are intractable.

**2. "Interrupt coalescing protects throughput" stated without the responsiveness cost foregrounded.**
The chapter is careful that coalescing *trades away* responsiveness (you only get interrupted once per
interval, but you also can't respond faster than the interval). The extraction captures this in §2 and
§16 but the card and content ideas emphasize the upside; the cost (unsuitable when something needs a
fast response) should be visible wherever the benefit is.

**3. The Rosenbaum → procrastination leap.** The extraction flags this in §5/§11, but the pre-crastination
study is a hallway bucket task; generalizing it to "procrastination is optimizing task-count" is the
authors' interpretive bridge, and the two behaviors (rushing subgoals vs. deferring a big project) are
arguably opposite surface phenomena unified only by the underlying "reduce number of open subgoals"
account. Worth keeping that inferential seam explicit.

## Important Nuance Lost

**1. Johnson's deeper two points, not just the laundry rule.** (PDF p. 139) The chapter stresses that
Johnson's paper revealed two *foundational* things beyond the rule: that scheduling could be expressed
algorithmically at all, and that optimal solutions *exist*. That meta-point (scheduling is a solvable
science) is why the paper "kicked off a sprawling literature," and it's more important than the
inward-from-both-ends mechanic. The extraction has the mechanic but under-weights the meta-significance.

**2. Preemptive EDD/SPT need only a "fairly straightforward modification," and it's specified.** (PDF
p. 152) The chapter gives the exact switch rules (EDD: switch if the arriving task is due sooner than
the current one, else stay; SPT: switch if the new task finishes faster than the current one). The
extraction has these but they're the crux of "preemption restores tractability" and deserve to be
foregrounded as the operational recipe, not buried.

**3. The "sum of completion times" is explicitly an *outsider's* metric.** (PDF p. 142) The chapter
frames SPT's metric as taking a client's/waiting-party's perspective — minimizing others' collective
waiting — which is why it's about the *number* of open items and their *duration*, not your own total
time (which is fixed). The extraction states the metric but loses the "outsider's perspective" framing
that motivates why it's a sensible thing to optimize at all.

**4. Denning's "ounce of prevention" and the memory-management origin.** (PDF pp. 157–158) The
extraction has the prevention advice, but the chapter's ordering matters: Denning's *landmark 1960s
paper* framed prevention (more RAM; refuse jobs) as the primary lever, and the "work dumber" escape is
explicitly the fallback for when you're *already* thrashing and can't add capacity or say no. The
extraction lists all three escapes but slightly flattens this prevention-first / fallback structure.

**5. The postal system's *two* gifts.** (PDF pp. 161–162) Interrupt coalescing from the post office has
two distinct benefits the chapter names: (a) you can be interrupted by mail at most once a day, and (b)
the 24-hour rhythm *demands minimal responsiveness* (it makes no difference whether you reply five
minutes or five hours after receipt). The extraction captures (a) but not (b), which is the subtler and
more transferable point.

## Additional Cases and Examples

```
Case Title: Lawler's unfinishable book on scheduling
People / Organization: Eugene "Gene" Lawler (chapter epigraph)
Context: A self-demonstrating epigraph.
What Happened: Lawler recalls proposing, "'Why don't we write a book on scheduling theory?… It
shouldn't take much time!' … Fifteen years later, Scheduling is still unfinished."
Outcome: The century's foremost expert on scheduling badly mis-scheduled a book about scheduling.
Concept Illustrated: Intractability; the gap between planning and doing; precedence/estimation failure.
Why This Case Is Useful: A perfect, ironic hook for the whole chapter, and it personalizes the
intractability result through the very researcher who mapped it.
Potential for Reuse: High
```

```
Case Title: Kipling's "unforgiving minute" — and the overhead that refutes it
People / Organization: Rudyard Kipling, "If—" (1910); the authors
Context: Inherited time-management wisdom vs. the reality of metawork.
What Happened: Kipling's poem exhorts filling "the unforgiving minute / With sixty seconds' worth of
distance run." The authors reply: "If only. The truth is, there's always overhead — time lost to
metawork."
Outcome: A century-old ideal of perfect time-use is rebutted by the fundamental cost of the context
switch.
Concept Illustrated: Context switch / overhead; the impossibility of 100% "real work."
Why This Case Is Useful: Pits a beloved poem against a hard computational fact — a strong rhetorical
beat for any content on productivity.
Potential for Reuse: High
```

```
Case Title: The hypocritical user interface
People / Organization: The authors (footnote)
Context: Notification design vs. what a CPU would tolerate.
What Happened: Computers "brashly pop up error messages and cursor-stealing dialogue boxes whenever
they want something from us… The user interface demands the user's attention in a way that the CPU
itself would rarely tolerate."
Outcome: The same machines that carefully avoid interrupting themselves interrupt us constantly.
Concept Illustrated: Interrupt coalescing; the cost of interruption; notification design critique.
Why This Case Is Useful: A sharp, quotable indictment of app/notification design that complements the
badge material.
Potential for Reuse: High
```

## Additional Research Evidence

None materially missing. The re-read confirms the chapter's empirical base is a handful of named results
(Johnson 1954, Lawler 1968, the complexity survey, Rosenbaum 2014, Denning 1960s) plus unnamed
task-switching psychology and productivity anecdotes — which the extraction reflects. One sharpening:
the "task-switching costs minutes not microseconds" and "interrupted more than a few times an hour = no
work" claims rest on unnamed psychology and should stay tagged as such.

## Potential Disagreements to Track Later

1. **Goodhart's law / metric gaming.** "Procrastination is optimizing the wrong metric" and "live by
   the metric, die by the metric" are Goodhart in disguise; any book on metrics/incentives (Muller,
   *The Tyranny of Metrics*) collides here — a recurring cross-chapter theme (chs. 3, 4, 5).
2. **The GTD / Eat That Frog / self-help productivity canon.** The chapter explicitly adjudicates among
   these bestsellers by reframing each as optimizing a different metric — a direct, marketable cross-book
   tension with the entire time-management genre.
3. **Deep work (Cal Newport).** Interrupt coalescing, minimum slices, and the writing-as-blacksmithing
   90-minute block align strongly with the deep-work literature; a natural ally rather than opponent, but
   worth mapping.
4. **Behavioral accounts of procrastination (emotion regulation; Steel's "The Procrastination
   Equation").** The chapter's computational account competes with the dominant affect-regulation model;
   track whether the book ever engages the emotional side it mostly brackets.
5. **Behavioral finance on the debt snowball (the "small victories" literature).** The chapter concedes
   the snowball's edge is motivational; a cross-book comparison with behavioral-economics defenses of
   the snowball would be sharp.

## Additional Content Opportunities

```
Idea: The expert who couldn't schedule his own book
Format: YouTube Short
Core Concept: Intractability; planning vs. doing.
Hook: The single greatest expert on scheduling theory once said writing a book about it "shouldn't take
much time." Fifteen years later it still wasn't finished.
Best Supporting Case: The Lawler epigraph; the 84%-intractable survey.
Psychology Angle: Planning fallacy; the gap between estimate and reality.
Math Angle: Why most scheduling problems have no efficient optimal solution.
Sports Angle: None core.
AI Angle: Why "just plan it perfectly" fails for hard combinatorial problems.
```

```
Idea: Your phone is a hypocrite
Format: YouTube Short
Core Concept: Interrupt coalescing; notification design.
Hook: Your computer would never let its own apps interrupt it the way its apps interrupt you. It
batches everything internally — and then throws pop-ups in your face.
Best Supporting Case: The UI-hypocrisy footnote; app badges; the post office as free coalescing.
Psychology Angle: The cost of interruption; attention as a scarce resource.
Math Angle: Responsiveness vs. throughput; minimum slice.
Sports Angle: None core.
AI Angle: Batching in inference serving; when to interrupt an agent.
```

---

## Recommended Changes to the Original Extraction

1. **§7 (Cases and Stories)** — add three cases: Lawler's unfinishable book (the highest-value
   addition — a self-demonstrating hook the first pass missed), Kipling's "unforgiving minute" rebutted
   by overhead, and the hypocritical user interface footnote.

2. **§12 (Quotable Ideas)** — add the Lawler epigraph, the "one watch / two watches" proverb, Lao Tzu's
   "do the difficult things while they are easy," Ullman on interruption ("you must not get off the
   train"), and the Kipling rebuttal ("there's always overhead").

3. **§5 (Johnson) / §2** — foreground Johnson's two *meta*-points (scheduling is expressible
   algorithmically; optimal solutions exist), not just the laundry rule, since that is why the field
   exists.

4. **§4 / §3 (preemption)** — foreground the exact preemptive switch rules (EDD: switch if arriving
   task is due sooner; SPT: switch if it finishes faster) as the operational recipe for "preemption
   restores tractability."

5. **§2 / §3 (SPT metric)** — restore the "outsider's perspective" framing: the sum of completion times
   minimizes others' collective waiting, which is *why* it's a sensible objective given that your own
   total time is fixed.

6. **§3 / card 13** — mark the "16-hour days twice as productive" line explicitly as one software
   friend's self-report, not a measured result.

7. **card 15 / §3** — attach the "only in a thrashing state" condition to "answer emails in random
   order," so it isn't reused as general advice.

8. **§2 / cards 6, 17** — carry the conditionals with the strong claims: weighted SPT's multi-metric
   optimality holds "under certain assumptions"; interrupt coalescing *trades away* responsiveness.

9. **§13 / §17** — add the postal system's *second* gift (the 24-hour rhythm demands minimal
   responsiveness — reply timing within the day is irrelevant), and the "scheduler and scheduled are the
   same machine" self-reference (planning competes with doing).

10. **§17** — add the "expert who couldn't schedule his own book" and "your phone is a hypocrite" short
    ideas.

**Sections that are fine as they stand:** §1 (thesis), §6 (experiments — the alternative-explanation
fields do real work, especially the working-memory reading of pre-crastination), §8 (teaching examples),
§9 (counterintuitive insights), §10 (unique ideas), §14 (mathematics), §16 (AI — the reward-
misspecification and over-parallelization mappings are strong and accurate). §15 (sports) is correctly
marked as containing no direct examples.
