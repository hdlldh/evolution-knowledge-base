# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 5: Scheduling — First Things First
**Author:** Brian Christian and Tom Griffiths
**Type:** Extraction
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 137–167 (book chapter 5, incl. footnotes)
**Date:** 2026-07-21
**Revision note:** Revised after Chapter_05_Audit.md; see that file for what changed and why.

```
BOOK:
Algorithms to Live By: The Computer Science of Human Decisions

AUTHOR:
Brian Christian and Tom Griffiths

CHAPTER:
5 — Scheduling: First Things First
```

---

## 1. Chapter Thesis

Before you can schedule well you must first choose a metric — "before you can have a plan, you must
first choose a metric" — because on a single machine (you) every ordering of your tasks takes the same
total time, so the order only matters relative to a goal. Computer science supplies provably optimal
algorithms for each goal (Earliest Due Date to minimize maximum lateness; Shortest Processing Time,
weighted by importance-per-unit-time, to shorten the to-do list or debt), but three deeper truths
reshape the advice: most scheduling problems are formally *intractable*, so struggling with your
calendar is genuinely hard; the metawork of switching tasks (the "context switch") is a real cost that
at the extreme collapses into "thrashing" — running full-tilt while accomplishing nothing; and the
cure is often to be *less* responsive on purpose — batching interruptions ("interrupt coalescing") so
you protect throughput. Procrastination, seen this way, is frequently an optimal solution to the wrong
problem.

## 2. Key Concepts

```
Concept Name: Single-Machine Scheduling
Definition: Ordering a set of tasks to be done by one processor — the case that matters most because
the single machine is ourselves.
Why It Matters: On one machine, if you do all your tasks, every ordering takes equally long; therefore
order only matters relative to a chosen metric.
How the Author Uses It: The chapter's central frame, forcing the "choose a metric first" lesson and
organizing every algorithm that follows.
Related Concepts: Metric choice, Earliest Due Date, Shortest Processing Time, weight.
```

```
Concept Name: Choosing a Metric ("make your goals explicit")
Definition: The prerequisite step of deciding how you'll keep score before you can call any schedule
best.
Why It Matters: "Before you can have a plan, you must first choose a metric." Which metric you pick
directly determines which algorithm is optimal — and different metrics give genuinely different plans.
How the Author Uses It: The organizing principle; the source of the procrastination reframing ("an
optimal solution to the wrong problem") and "live by the metric, die by the metric."
Related Concepts: Maximum lateness, sum of completion times, weight, one-watch/two-watches.
```

```
Concept Name: Earliest Due Date (EDD)
Definition: Do the task due soonest first, working toward the task due last.
Why It Matters: Provably optimal for minimizing maximum lateness; strikingly, task durations are
entirely irrelevant to the plan (you don't even need to know them).
How the Author Uses It: The first single-machine metric; extended to service (serve in arrival order),
to CSA produce, and — with modification — to precedence constraints and preemption.
Related Concepts: Maximum lateness, Moore's Algorithm, precedence constraints, preemption.
```

```
Concept Name: Shortest Processing Time (SPT) and Weighted SPT
Definition: Always do the quickest task you can (unweighted), or divide each task's weight (importance)
by its duration and work highest "density" first (weighted).
Why It Matters: SPT minimizes the sum of completion times (shortens the to-do list fastest) — a metric
framed from the *outsider's perspective*, minimizing others' collective waiting, which is why it's a
sensible objective given that your own total time is fixed. Weighted SPT is the chapter's "skeleton
key" — optimal for the weighted completion times and, *under certain assumptions*, several other
weighted metrics, and the best general-purpose strategy under uncertainty (but note: most other
scheduling metrics are intractable, so the key does not open every door).
How the Author Uses It: To justify the GTD two-minute rule, the debt snowball (unweighted) vs. debt
avalanche (weighted), consultant hourly rates, and animal foraging.
Related Concepts: Sum of completion times, weight/density, debt avalanche/snowball, preemption.
```

```
Concept Name: Weight (Importance) and Density
Definition: A per-task importance value; "density" is weight divided by duration (importance per unit
time).
Why It Matters: Yields the rule of thumb "only prioritize a task that takes twice as long if it's twice
as important," and unifies debts, dollars-per-hour, and calories-per-forage-time.
How the Author Uses It: Converts the unweighted SPT into the weighted skeleton key.
Related Concepts: Weighted SPT, debt avalanche, hourly rate, foraging.
```

```
Concept Name: Precedence Constraints
Definition: When one task can't start until another is finished.
Why It Matters: They can force you to treat an unimportant blocking task as maximally important; EDD
adapts easily (build the schedule back-to-front), but SPT-with-precedence is intractable.
How the Author Uses It: To explain priority inversion, the Mars Pathfinder failure, McLay's spoon, and
Lenstra's moving-van irony.
Related Concepts: Priority inversion, priority inheritance, intractability.
```

```
Concept Name: Priority Inversion and Priority Inheritance
Definition: Priority inversion — a low-priority task holding a resource blocks a high-priority task
while medium tasks run instead. Priority inheritance — the blocking task temporarily inherits the
priority of what it blocks.
Why It Matters: Shows that even devotion to "important things first" can produce something that looks
exactly like procrastination; the fix is counterintuitive (elevate the trivial blocker).
How the Author Uses It: Diagnoses and fixes the Mars Pathfinder rover; Hedberg's fire-exit joke.
Related Concepts: Precedence constraints, "matters most vs. matters least," blocking.
```

```
Concept Name: Intractability of Scheduling
Definition: Most scheduling problems have no efficient algorithm to find the optimal schedule in
reasonable time.
Why It Matters: A survey found ~7% of problems have unknown status; of the 93% understood, only 9% are
efficiently solvable and 84% are proven intractable. Subtle changes (adding weights, start-time
constraints) tip a tractable problem into intractability.
How the Author Uses It: To validate that managing your calendar really is overwhelming, and to set up
the surprising relief that uncertainty can restore tractability.
Related Concepts: Preemption, clairvoyance-as-burden, precedence constraints.
```

```
Concept Name: Preemption
Definition: The ability to stop a task partway through and switch to another.
Why It Matters: It "changes the game dramatically" — restoring efficient solutions to problems that
were intractable with fixed start times, and keeping EDD/SPT optimal (with a simple switch rule) even
under uncertainty about when tasks arrive.
How the Author Uses It: To show scheduling is more encouraging than intractability suggests, and to
reveal that clairvoyance can be a burden.
Related Concepts: Context switch, EDD/SPT preemptive versions, uncertainty.
```

```
Concept Name: The Context Switch (Metawork)
Definition: The overhead of switching tasks — bookmarking your place, choosing what's next, reloading
the new task's state. None of it is "real work."
Why It Matters: Preemption isn't free; humans pay in minutes (not microseconds), so being interrupted
more than a few times an hour risks doing no work at all.
How the Author Uses It: To temper the pro-preemption message and to explain thrashing; grounds the
writing-as-blacksmithing 90-minute-minimum intuition.
Related Concepts: Thrashing, responsiveness/throughput, interrupt coalescing.
```

```
Concept Name: Thrashing
Definition: A system running full-tilt while accomplishing essentially nothing, because it is entirely
consumed by metawork.
Why It Matters: Performance doesn't degrade gradually — it "falls off a cliff." One task too many
collapses the whole system (the over-loaded juggler drops everything, not just the extra ball).
How the Author Uses It: Names a recognizable human panic state; connects scheduling to caching (working
sets evicting each other) and motivates the escape strategies.
Related Concepts: Working set (caching), context switch, "work dumber," interrupt coalescing.
```

```
Concept Name: Responsiveness vs. Throughput
Definition: The tension between how quickly you can react and how much you get done overall.
Why It Matters: A hard responsiveness guarantee, unchecked, spends the whole time slice context-
switching; the fix is a minimum slice length — commit to any one task for a floor amount of time.
How the Author Uses It: To justify timeboxing/pomodoros and the counsel "be no more responsive than
you need to be."
Related Concepts: Minimum slice, interrupt coalescing, context switch.
```

```
Concept Name: Interrupt Coalescing
Definition: Batching interruptions and handling them together at a fixed interval instead of one by one.
Why It Matters: The chapter's key productivity prescription — protect throughput by refusing to
respond continuously; the post office gives it to us free.
How the Author Uses It: Bill-paying day, checking email once a day, office hours, the redeemed weekly
meeting, and Knuth's extreme batch-processing life.
Related Concepts: Responsiveness/throughput, minimum slice, batch processing, Do Not Disturb.
```

## 3. Key Claims

```
Claim: On a single machine, if you do all your tasks, every ordering takes the same total time.
Type: Theoretical
Evidence Provided: Structural argument, called "fundamental and counterintuitive" enough to repeat.
Strength of Support: Strong. True by construction, and the premise of the whole chapter.
```

```
Claim: You must choose a metric before you can call any schedule best.
Type: Theoretical / Prescriptive
Evidence Provided: The first lesson of single-machine scheduling; different metrics yield different
optimal algorithms.
Strength of Support: Strong. A definitional consequence of the previous claim.
```

```
Claim: Earliest Due Date is optimal for minimizing maximum lateness, and task durations are irrelevant
to it.
Type: Theoretical (proved)
Evidence Provided: Stated as optimal; the service analogy (serve in arrival order); the surprising
corollary that you needn't know how long tasks take.
Strength of Support: Strong. A proved result; the durations-irrelevant point is a genuine surprise.
```

```
Claim: To minimize the number of late/spoiled items, use Moore's Algorithm.
Type: Theoretical
Evidence Provided: Schedule by due date, then drop the largest already-scheduled item whenever you fall
behind (e.g. forgo the watermelon). Late/dropped items can then be done in any order at the end.
Strength of Support: Strong for equal-value items. Explicitly noted to become intractable once items
have different importance.
```

```
Claim: Shortest Processing Time minimizes the sum of completion times.
Type: Theoretical (proved)
Evidence Provided: The 4-day + 1-day project example: big-first = 9 client-days, small-first = 6, same
week for you either way.
Strength of Support: Strong. A clean worked proof of the metric.
```

```
Claim: Weighted Shortest Processing Time — order by weight ÷ duration — minimizes the sum of weighted
completion times, and is a near-universal "skeleton key."
Type: Theoretical (proved)
Evidence Provided: The density rule ("only prioritize a task that takes twice as long if it's twice as
important"); business hourly-rate translation; animal foraging by calories/time; debt avalanche
(highest interest rate first). Under certain assumptions it also minimizes the sum of weights of late
jobs and the weighted lateness of those jobs.
Strength of Support: Strong. Multiple domains; the multi-metric optimality is stated with the "under
certain assumptions" hedge preserved.
```

```
Claim: Debt-reduction: pay highest-interest first (avalanche, weighted) to minimize total burden, or
smallest-balance first (snowball, unweighted SPT) to minimize the number of debts.
Type: Prescriptive / Interpretive
Evidence Provided: Maps debts onto weighted vs. unweighted SPT.
Strength of Support: Moderate. The mapping is clean; the chapter explicitly notes which is better "in
practice… remains an active controversy" in both popular press and economics research.
```

```
Claim: Procrastination is often an optimal solution to the wrong problem — a great strategy for the
wrong metric.
Type: Interpretive
Evidence Provided: App badges give all tasks equal weight, so clearing the easy ones first (unweighted
SPT) rationally minimizes the visible number; the X-Files "ping/denial-of-service" vampire; Rosenbaum's
2014 pre-crastination study (people carried the near bucket the whole way rather than the far one a
short distance).
Strength of Support: Moderate to Strong. The reframing is well-supported by the badge logic and the
pre-crastination study; it's an interpretation, not a claim that all procrastination is optimal.
```

```
Claim: Devotion to doing the most important thing first is not enough — precedence constraints can make
a trivial task the thing you must do first.
Type: Theoretical / Interpretive
Evidence Provided: Priority inversion on Mars Pathfinder; "sometimes that which matters most cannot be
done until that which matters least is finished"; McLay's spoon; Lenstra's van.
Strength of Support: Strong. A named, documented engineering failure plus everyday illustrations.
```

```
Claim: Most scheduling problems are intractable.
Type: Empirical / Theoretical
Evidence Provided: A recent survey — ~7% unknown status; of the 93% understood, 9% efficiently
solvable, 84% intractable. Subtle changes (weights on Moore's Algorithm; start-time constraints) tip
problems into intractability.
Strength of Support: Strong, with the chapter's own caveat (footnote) that the 84% figure includes
multi-machine problems, "more like managing a group of employees than managing your calendar."
```

```
Claim: Preemption restores tractability and keeps EDD/SPT optimal even under uncertainty about start
times.
Type: Theoretical (proved)
Evidence Provided: The operational recipe is a "fairly straightforward modification" — preemptive EDD:
when a task arrives, switch to it only if it is due sooner than the one under way, else stay the course;
preemptive SPT: switch only if the new task finishes faster than the time left on the current one. Both
remain optimal and guarantee the best possible average performance under uncertainty.
Strength of Support: Strong. Stated as proved optimal-under-uncertainty results.
```

```
Claim: Clairvoyance can be a burden — knowing start times and durations in advance can make optimal
scheduling intractable, whereas reacting as jobs arrive is much easier to compute.
Type: Theoretical (counterintuitive)
Evidence Provided: The weighted-SPT metrics that are optimal online become intractable offline (with
full foreknowledge). Jason Fried: "Replace 'plan' with 'guess' and take it easy."
Strength of Support: Strong. A genuine and striking result — the online problem is easier than the
offline one here.
```

```
Claim: Preemption isn't free — the context switch is pure overhead ("metawork"), and for humans it
costs minutes, not microseconds.
Type: Theoretical / Empirical
Evidence Provided: Psychologists have shown task-switching causes delays and errors "at the scale of
minutes" (unnamed studies); anyone interrupted more than a few times an hour risks doing no work. The
productivity figures are explicitly anecdotal self-reports: *one software friend* says his 16-hour days
are more than twice as productive as 8-hour days; Brian's writing-as-blacksmithing (~30 min just to
heat up, so block ≥90 minutes); Pruhs's 35 minutes to get going.
Strength of Support: Moderate to Strong. The psychology is cited (unnamed studies); the productivity
figures are individual anecdotes, not measured.
```

```
Claim: Thrashing — full-tilt effort accomplishing nothing — happens when metawork consumes the system,
and performance collapses suddenly rather than gradually.
Type: Theoretical (attributed to Denning)
Evidence Provided: Denning's 1960s work; the juggler who drops everything with one ball too many;
"the presence of one additional program has caused a complete collapse of service"; scheduling meets
caching (working sets evict each other; Zijlstra: context switch "invalidates all caches").
Strength of Support: Strong. A named, foundational result with a vivid mechanism.
```

```
Claim: To escape thrashing you can add capacity, say no, or "work dumber."
Type: Prescriptive
Evidence Provided: Denning — get more RAM, or refuse a program if there isn't memory for its working
set. When you can't do either, work dumber: scanning an inbox of n for the most important message is
O(n²) (three times as full → nine times as long), so answer in random/on-screen order; Linux replaced
its scheduler with a "less smart but faster" one.
Strength of Support: Strong. The O(n²) point ties directly to chapter 3's sorting theory; the Linux
example is concrete.
```

```
Claim: The cure for over-switching is a minimum time-slice and deliberate under-responsiveness.
Type: Prescriptive
Evidence Provided: OS schedulers set a minimum slice (Linux ~0.75 ms; humans "at least several
minutes") so context-switching can never become the only activity; timeboxing/pomodoros embody it;
"be no more responsive than you need to be."
Strength of Support: Strong. A direct machine-to-human transfer with a concrete mechanism.
```

```
Claim: Interrupt coalescing — batching interruptions at a fixed interval — protects throughput.
Type: Prescriptive
Evidence Provided: Pay all bills on a "bill-paying day" (if none due in under 31 days); check email once
a day (if none require sub-24-hour response); office hours; the redeemed weekly meeting; the post office
gives free coalescing; Norvig's "one-line bug" of three separate downtown trips; Knuth's batch-
processing extreme (no email since 1990; TeX tuned every six years; mail every three months, faxes
every six).
Strength of Support: Strong. A rich set of concrete, transferable practices.
```

## 4. Frameworks, Models, and Mental Models

```
Name: Johnson's Rule (Two-Machine Scheduling)
Description: For jobs that must pass through machine A then machine B (bookbinding; laundry
washer→dryer), minimize total time.
Components: Each job's time on each machine; a schedule built inward from both ends.
How It Works: Find the single shortest step across all jobs; if it's on the first machine, do that job
first; if on the second, do it last. Repeat, working from the ends toward the middle. This maximizes
overlap (both machines running at once). "Start with the lightest wash, end with the smallest hamper."
When It Is Useful: Two-stage pipelines.
Limitations: Two machines only; the chapter pivots to single-machine because "the machine that matters
most is ourselves."
```

```
Name: Earliest Due Date (EDD)
Description: Schedule tasks in order of due date, soonest first.
Components: Due dates only (durations irrelevant).
How It Works: Minimizes the maximum lateness of any task. With precedence constraints, build
back-to-front: among tasks nothing depends on, place the latest-due one last, and repeat. Preemptive
version: when a task arrives due sooner than the current one, switch.
When It Is Useful: When your worst-case lateness is what matters (performance reviews, longest customer
wait).
Limitations: Optimizes only maximum lateness; indifferent to how late everything else is.
```

```
Name: Moore's Algorithm
Description: Minimize the number of late (or spoiled) items.
Components: Due/spoilage dates; item durations.
How It Works: Schedule by due date; whenever the next item can't be finished in time, look back and
drop the largest already-scheduled item. Repeat until all remaining items fit. Dropped items are done
last, in any order (they're all late anyway).
When It Is Useful: When the count of late items matters more than their severity (CSA produce; some
bureaucratic contexts).
Limitations: Assumes equal value; becomes intractable once items have different importance.
```

```
Name: Shortest Processing Time (SPT) / Weighted SPT
Description: Do the quickest task first (unweighted), or order by weight ÷ duration (weighted).
Components: Durations; optional weights (importance, money, calories).
How It Works: Unweighted SPT minimizes the sum of completion times (shortest to-do list fastest).
Weighted SPT minimizes the sum of weighted completion times and, under certain assumptions, several
other weighted metrics — the "skeleton key." Preemptive version: switch to a new job if its
weight/remaining-time density beats the current job's.
When It Is Useful: Clearing backlog; debts; foraging; the best general-purpose strategy under
uncertainty.
Limitations: SPT-with-precedence is intractable; unweighted SPT can trivialize genuinely important
long tasks.
```

```
Name: Priority Inheritance (fix for Priority Inversion)
Description: When a low-priority task blocks a high-priority one, the blocker temporarily inherits the
high priority.
Components: A blocked high-priority task; a blocking low-priority task; a shared resource.
How It Works: Elevating the blocker lets it finish and release the resource, unblocking the important
task — instead of medium tasks running while the top priority starves.
When It Is Useful: Any system where tasks compete for shared resources (real-time systems; households).
Limitations: Requires detecting the blocking relationship; the deeper lesson is that "matters most vs.
matters least" is not always a valid ordering.
```

```
Name: Interrupt Coalescing + Minimum Slice
Description: Handle batched interruptions at fixed intervals, and commit to any one task for a floor
amount of time.
Components: A period; a minimum slice; a fixed check-in interval.
How It Works: A minimum slice prevents context-switching from becoming the only activity; coalescing
converts many small interruptions into one scheduled batch (bill-paying day; once-a-day email; office
hours; weekly meetings).
When It Is Useful: Heterogeneous streams of short tasks; protecting deep work.
Limitations: Lowers responsiveness by design; requires that nothing needs faster response than the
interval allows.
```

## 5. Research and Evidence

```
Study / Research: The first optimal scheduling algorithm
Researchers: Selmer Johnson (RAND Corporation)
Year: 1954
Research Question: What is the best way to sequence jobs through two machines (bookbinding: print then
bind; laundry: wash then dry)?
Method: Mathematical analysis.
Key Finding: Do the shortest step first if it's on machine one, last if on machine two; work inward
from both ends. This maximizes overlap and minimizes total time — scheduling's first optimal algorithm.
But the paper's *deeper* significance is two meta-points beyond the laundry rule: that scheduling could
be expressed algorithmically at all, and that optimal solutions *exist* — which is why it "kicked off a
sprawling literature" and made scheduling a solvable science.
How the Author Uses It: To show scheduling can be expressed algorithmically and that optimal solutions
exist, launching the whole field.
Important Limitations: Two-machine case only.
Replication or Controversy Mentioned: None; kicked off a "sprawling literature."
```

```
Study / Research: Scientific Management and the planning board
Researchers: Frederick Taylor (Midvale Steel); Henry Gantt (Gantt charts)
Year: Taylor from 1874; Gantt charts in the 1910s
Research Question: How to use the time of machines and people well?
Method: Industrial practice — a bulletin board showing each machine's current and waiting tasks; later
Gantt charts.
Key Finding: Scheduling could be given visual/conceptual form (used on the Hoover Dam, Interstate
Highway System; still at Amazon, IKEA, SpaceX) — but Taylor and Gantt did not solve which schedules are
best.
How the Author Uses It: The prehistory of scheduling science, before Johnson made it solvable.
Important Limitations: Descriptive/organizational, not optimization.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Precedence constraints and intractability in scheduling
Researchers: Eugene "Gene" Lawler (Berkeley), with Jan Karel Lenstra and others
Year: Lawler's EDD-with-precedence result 1968; the landscape-mapping effort through the 1970s onward
Research Question: How do precedence constraints affect optimal scheduling, and which problems are
tractable?
Method: Algorithm design and complexity analysis.
Key Finding: EDD-with-precedence is easily solved (build back-to-front), but SPT-with-precedence is
intractable; even subtle changes tip problems over the tractable/intractable line.
How the Author Uses It: To establish scheduling theory's "brick wall," and to introduce Lawler (whose
own life supplied a priority-inversion anecdote).
Important Limitations: "Intractable" is defined loosely here; detailed treatment deferred to chapter 8.
Replication or Controversy Mentioned: The ACM established a humanitarian award in Lawler's name after
his 1994 death.
```

```
Study / Research: Survey of scheduling-problem complexity
Researchers: Not specified ("a recent survey").
Year: Not specified.
Research Question: What proportion of scheduling problems is tractable?
Method: Survey/classification of known scheduling problems.
Key Finding: ~7% of problems have unknown status; of the 93% understood, only 9% are efficiently
solvable and 84% are proven intractable.
How the Author Uses It: To validate that perfect calendar management really is overwhelming.
Important Limitations: Footnote caveat — the count includes multi-machine problems ("more like managing
a group of employees than managing your calendar"), so single-machine life is not quite this dire.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: The Mars Pathfinder priority-inversion failure
Researchers: Jet Propulsion Laboratory (JPL) engineers; software team leader Glenn Reeves
Year: 1997
Research Question: N/A — a real engineering incident.
Method: Diagnosis and remote patch of a $150M spacecraft.
Key Finding: The rover repeatedly reset because its highest-priority task (the information bus) was
blocked by a low-priority task while medium-priority tasks ran — classic priority inversion. Fix:
priority inheritance, beamed across millions of miles.
How the Author Uses It: The dramatic centerpiece proving that "important things first" can look exactly
like procrastination.
Important Limitations: A single incident.
Replication or Controversy Mentioned: Footnote irony — Reeves blamed the bug on "deadline pressures"
and on fixing it having been deemed "lower priority," so the root cause mirrored the problem.
```

```
Study / Research: Pre-crastination bucket experiment
Researchers: David Rosenbaum and colleagues (Penn State)
Year: 2014
Research Question: Do people rush to complete subgoals even at extra physical cost?
Method: Participants carried one of two heavy buckets to the far end of a hallway; one bucket was near
them, the other partway down.
Key Finding: People immediately grabbed the near bucket and carried it the whole way, passing the
other bucket they could have carried a fraction of the distance — "pre-crastination," the hastening of
subgoal completion at the expense of extra effort.
How the Author Uses It: To reframe procrastination as optimizing the wrong metric (reducing the number
of open subgoals) rather than laziness.
Important Limitations: A single hallway task; generalization to procrastination is the authors'
interpretive extension.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Thrashing and multiprogramming
Researchers: Peter Denning (MIT doctoral work in the 1960s); later Peter Zijlstra (Linux scheduler)
Year: 1960s (Denning's landmark paper); Zijlstra contemporary
Research Question: How to share memory/CPU among many jobs without collapse?
Method: Analysis of multiprogramming systems.
Key Finding: Adding one job past a critical (unpredictable) threshold causes a sudden complete collapse
of service — thrashing — not gradual degradation; caused by working sets evicting each other so the
system spends all its time swapping. Prevention beats cure (more RAM; refuse jobs without room for their
working set).
How the Author Uses It: To name a recognizable human panic state and connect scheduling to caching.
Important Limitations: Denning's original context was memory management; the term is now used broadly.
Replication or Controversy Mentioned: None identified.
```

```
Study / Research: Task-switching costs in humans
Researchers: Not specified ("psychologists have shown").
Year: Not specified.
Research Question: What does switching tasks cost people?
Method: Not specified.
Key Finding: Task switching produces both delays and errors "at the scale of minutes rather than
microseconds"; anyone interrupted more than a few times an hour risks doing no real work.
How the Author Uses It: To establish that human context switches are expensive, motivating slice
minimums and coalescing.
Important Limitations: Unnamed studies; no effect sizes given.
Replication or Controversy Mentioned: None identified.
```

## 6. Experiments

```
Experiment Name: Rosenbaum's pre-crastination hallway task
Setup: Two heavy buckets in a hallway — one next to the participant, one partway toward the goal end.
Participants: Human participants (number not specified), Penn State, 2014.
Procedure: Carry either bucket to the far end.
Result: People overwhelmingly grabbed the near bucket and lugged it the entire length, passing the
farther bucket they could have carried only a short distance.
Interpretation: A tendency to "pre-crastinate" — hasten subgoal completion even at the cost of extra
physical effort — which the authors map onto procrastination as optimizing the count of open tasks.
What It Demonstrates: That the urge to reduce the number of outstanding subgoals can override overall
efficiency.
Potential Alternative Explanation: Grabbing the near bucket may reduce working-memory load (one less
thing to track) rather than reflecting subgoal-completion urgency; the physical-effort cost may be
under-perceived rather than knowingly accepted.
```

```
Experiment Name: The multiprogramming collapse (thrashing)
Setup: A shared-memory computer running an increasing number of concurrent jobs.
Participants: N/A — a systems phenomenon.
Procedure: Add jobs to the multiprogramming mix one at a time.
Result: Past an unpredictable critical threshold, adding a single job causes a sudden complete collapse
of service, not gradual slowdown.
Interpretation: Working sets evict each other, so the system spends all its time swapping memory rather
than working — thrashing.
What It Demonstrates: That overload failure is a cliff, not a slope, in both machines and (by analogy)
minds.
Potential Alternative Explanation: The threshold depends on specific memory/working-set sizes; the
human analogy is illustrative, not a measured equivalence.
```

## 7. Cases and Stories

```
Case Title: The conflicting gospels of time management
People / Organization: Getting Things Done; Eat That Frog!; The Now Habit; William James; Frank
Partnoy's Wait
Context: The perennial bestseller status of time-management guides, whose advice is "divergent and
inconsistent."
What Happened: GTD says do any task under two minutes immediately; Eat That Frog! says start with the
hardest; The Now Habit says schedule leisure first and fill gaps with work; William James says
"there's nothing so fatiguing as the eternal hanging on of an uncompleted task"; Partnoy argues for
deliberately not doing things right away.
Outcome: "Every guru has a different system, and it's hard to know who to listen to" — the problem the
chapter's metric-first framing dissolves (each guru optimizes a different metric).
Concept Illustrated: Why you must choose a metric first; different metrics → different optimal advice.
Why This Case Is Useful: Instantly relatable; frames the whole chapter and shows CS adjudicating a
self-help war.
Potential for Reuse: High
```

```
Case Title: Taylor's board and Gantt's charts
People / Organization: Frederick Taylor (Midvale Steel); Henry Gantt
Context: The industrial-revolution birth of scheduling as a discipline.
What Happened: Taylor turned down Harvard in 1874 to apprentice as a machinist, rose to chief engineer,
and invented "Scientific Management," centered on a planning board showing each machine's current and
waiting tasks. Gantt turned this into the Gantt chart (1910s), used on the Hoover Dam and Interstate
Highway System and still on the walls of Amazon, IKEA, and SpaceX.
Outcome: Scheduling got visual and conceptual form — but not yet a way to know which schedule is best.
Concept Illustrated: Scheduling as an object of study; the prehistory before optimization.
Why This Case Is Useful: A crisp origin story linking a 19th-century machine shop to modern
project management.
Potential for Reuse: High
```

```
Case Title: Johnson's laundry
People / Organization: Selmer Johnson (RAND)
Context: The first solvable scheduling problem, framed as two machines in sequence.
What Happened: For loads that must wash then dry, Johnson proved you should start with the load with
the shortest washing time and end with the shortest drying time, working inward — maximizing the
overlap when both machines run at once.
Outcome: Scheduling's first optimal algorithm (1954): "start with the lightest wash, end with the
smallest hamper."
Concept Illustrated: Two-machine scheduling; overlap maximization.
Why This Case Is Useful: A universally familiar chore made rigorous; a clean, memorable rule.
Potential for Reuse: High
```

```
Case Title: The Mars Pathfinder that procrastinated
People / Organization: NASA/JPL; software team leader Glenn Reeves
Context: Summer 1997 — humanity's first rover on Mars, a $150M craft that had crossed 309 million miles.
What Happened: Pathfinder began neglecting its highest-priority task (the information bus) while doing
middling work, then reset itself, losing nearly a day — twice. JPL diagnosed a classic priority
inversion: a low-priority task held a resource, blocking the high-priority task, while medium-priority
tasks ran instead. They beamed a fix across the solar system: priority inheritance.
Outcome: The rover recovered. Footnote irony: Reeves blamed the bug on "deadline pressures" and on the
fix having been deemed "lower priority" — the root cause mirrored the problem.
Concept Illustrated: Priority inversion; priority inheritance; why "important first" can look like
procrastination.
Why This Case Is Useful: High-stakes, dramatic, globally watched, with a perfect self-referential
twist; the marquee case of the chapter.
Potential for Reuse: High
```

```
Case Title: Mitch Hedberg and the fire exit
People / Organization: Comedian Mitch Hedberg
Context: A joke that happens to encode priority inversion and inheritance.
What Happened: A bouncer told Hedberg to move because he was "blocking the fire exit." Hedberg: "As
though if there was a fire, I wasn't gonna run… If you're flammable and have legs, you are never
blocking a fire exit."
Outcome: The bouncer's worry is priority inversion; Hedberg's rebuttal is priority inheritance (an
onrushing mob makes you inherit their priority fast).
Concept Illustrated: Priority inheritance in one joke.
Why This Case Is Useful: A memorable, funny mnemonic for an abstract systems concept.
Potential for Reuse: High
```

```
Case Title: McLay's spoon and Lenstra's moving van
People / Organization: Laura Albert McLay (operations research); Jan Karel Lenstra; Eugene Lawler
Context: Everyday precedence constraints.
What Happened: McLay, running a household with three kids, notes she can't get out the door unless the
kids eat breakfast, and they can't eat unless she remembers a spoon — "something very simple that you
forget that just delays everything." In 1978 Lenstra helped his friend Gene move: they needed to return
a van, but needed the van to return equipment, which they needed to fix the apartment; the non-urgent
apartment fix was actually the most urgent. The delicious irony: Gene was Eugene Lawler, the century's
greatest expert on precedence constraints.
Outcome: Naming the blocking prerequisite and keeping it moving is how work gets done.
Concept Illustrated: Precedence constraints; priority inversion in ordinary life.
Why This Case Is Useful: Homey, funny, and it makes an abstract constraint immediately usable; the
Lawler irony is a bonus.
Potential for Reuse: High
```

```
Case Title: The X-Files vampire and the denial-of-service attack
People / Organization: The X-Files (Mulder)
Context: Procrastination as a system exploit.
What Happened: Bedridden Mulder, about to be eaten by an obsessive-compulsive vampire, spills sunflower
seeds; the vampire compulsively picks them up one by one until dawn saves Mulder.
Outcome: A "ping attack" / denial-of-service: overwhelm a system with trivial tasks and the important
one is lost.
Concept Illustrated: How a flood of small tasks starves the important one; procrastination-by-overload.
Why This Case Is Useful: A vivid pop-culture illustration of DoS/priority starvation.
Potential for Reuse: High
```

```
Case Title: Donald Knuth, patron saint of batch processing
People / Organization: Donald Knuth
Context: The extreme of the minimal-context-switching life.
What Happened: "I do one thing at a time… I don't swap in and out." Knuth has had no email address since
1990 ("my role is to be on the bottom of things… long hours of uninterruptible concentration"). On
Jan 1, 2014 he did "The TeX Tuneup of 2014," fixing six years' worth of reported bugs at once, signing
off "Stay tuned for The TeX Tuneup of 2021!" He reviews postal mail every three months and faxes every
six.
Outcome: A working life engineered around interrupt coalescing and zero context switching.
Concept Illustrated: Batch processing; interrupt coalescing taken to its logical extreme.
Why This Case Is Useful: A memorable, extreme exemplar that makes the principle concrete and aspirational
(or cautionary).
Potential for Reuse: High
```

```
Case Title: Norvig's downtown trips
People / Organization: Peter Norvig (Google director of research)
Context: Noticing the absence of interrupt coalescing in one's own life.
What Happened: "I had to go downtown three times today to run errands, and I said, 'Oh, well, that's
just a one-line bug in your algorithm. You should have just waited, or added it to the to-do queue,
rather than executing them sequentially as they got added one at a time.'"
Outcome: A researcher diagnosing his own day as a scheduling bug.
Concept Illustrated: Interrupt coalescing; batching errands.
Why This Case Is Useful: A quotable, self-deprecating instance of applying CS to one's own logistics.
Potential for Reuse: Medium
```

```
Case Title: Lawler's unfinishable book on scheduling
People / Organization: Eugene "Gene" Lawler (chapter epigraph)
Context: A self-demonstrating epigraph.
What Happened: Lawler recalls proposing, "'Why don't we write a book on scheduling theory?… It
shouldn't take much time!' … Fifteen years later, *Scheduling* is still unfinished."
Outcome: The century's foremost expert on scheduling badly mis-scheduled a book about scheduling.
Concept Illustrated: Intractability; the gap between planning and doing; the planning fallacy.
Why This Case Is Useful: A perfect, ironic hook for the whole chapter, personalizing the intractability
result through the very researcher who mapped it.
Potential for Reuse: High
```

```
Case Title: Kipling's "unforgiving minute" — refuted by overhead
People / Organization: Rudyard Kipling, "If—" (1910); the authors
Context: Inherited time-management wisdom vs. the reality of metawork.
What Happened: Kipling's poem exhorts filling "the unforgiving minute / With sixty seconds' worth of
distance run." The authors reply: "If only. The truth is, there's always overhead — time lost to
metawork."
Outcome: A century-old ideal of perfect time-use is rebutted by the fundamental cost of the context
switch.
Concept Illustrated: Context switch / overhead; the impossibility of 100% "real work."
Why This Case Is Useful: Pits a beloved poem against a hard computational fact — a strong rhetorical
beat for productivity content.
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
Concept Illustrated: Interrupt coalescing; the cost of interruption; notification-design critique.
Why This Case Is Useful: A sharp, quotable indictment of app/notification design that complements the
badge material.
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: Order is irrelevant on a single machine
Example: If you'll do all your tasks on one machine, every ordering takes the same total time — so the
order only matters relative to a metric.
Why It Works: A "fundamental and counterintuitive" fact that instantly justifies the whole "choose a
metric first" program.
Possible Alternative Domain: Mathematics
```

```
Concept: Sum of completion times (SPT)
Example: A 4-day and a 1-day project: big-first makes clients wait 4+5 = 9 days; small-first, 1+5 = 6
days — same workweek for you, three days saved for them.
Why It Works: One tiny arithmetic swap makes an abstract metric and its optimal rule obvious.
Possible Alternative Domain: Business
```

```
Concept: Weighted SPT / density rule
Example: "Only prioritize a task that takes twice as long if it's twice as important" — weight ÷
duration, highest first; consultants just use hourly rate.
Why It Works: Turns a proof into a one-line heuristic anyone can apply to a to-do list or a client list.
Possible Alternative Domain: Business
```

```
Concept: Priority inversion / inheritance
Example: Hedberg blocking the fire exit — "if you're flammable and have legs, you are never blocking a
fire exit."
Why It Works: A joke that encodes both the failure (inversion) and the fix (inheritance) in one image.
Possible Alternative Domain: Everyday Life
```

```
Concept: Precedence constraints
Example: You can't leave until the kids eat breakfast, and they can't eat until you remember a spoon —
so the spoon is momentarily the most important thing in the house.
Why It Works: A trivial object (a spoon) made maximally important makes the abstract constraint
visceral.
Possible Alternative Domain: Everyday Life
```

```
Concept: Thrashing
Example: A juggler given one ball too many doesn't drop that ball — he drops everything; the system
"falls off a cliff."
Why It Works: Captures the sudden, total nature of overload collapse in a single physical image.
Possible Alternative Domain: Everyday Life
```

```
Concept: Interrupt coalescing
Example: Pay all five credit-card bills on one "bill-paying day"; check email once a day; Knuth's TeX
tuneup every six years.
Why It Works: Concrete, adoptable practices that make an OS technique immediately actionable for a
person.
Possible Alternative Domain: Everyday Life
```

## 9. Counterintuitive Insights

```
Insight: On a single machine, the order you do your tasks in doesn't change how long they take.
Common Belief: A better order gets everything done faster.
Author's Argument: If you'll do all tasks, total time is fixed; order only affects a metric (lateness,
sum of completion times, weighted burden), so you must decide what you're optimizing.
Evidence: Structural proof.
Why It Is Surprising: It dissolves the premise of most time-management advice and relocates the whole
problem to metric choice.
```

```
Insight: For minimizing maximum lateness, how long each task takes is completely irrelevant.
Common Belief: You need to estimate task durations to plan well.
Author's Argument: Earliest Due Date is optimal for maximum lateness using due dates alone — you don't
even need to know the durations.
Evidence: The EDD optimality result.
Why It Is Surprising: A key input everyone assumes is essential turns out to be unnecessary for this
goal.
```

```
Insight: Procrastination can be an optimal solution — to the wrong problem.
Common Belief: Procrastination is laziness or a broken strategy.
Author's Argument: Clearing many trivial tasks first (unweighted SPT) optimally minimizes the number of
open items — a great strategy for a metric (task count) you didn't mean to choose; app badges and
pre-crastination push us into it.
Evidence: The badge logic; Rosenbaum's bucket study; the X-Files DoS.
Why It Is Surprising: It reframes a moral failing as a rational algorithm aimed at the wrong target.
```

```
Insight: Doing the most important thing first can look exactly like procrastination.
Common Belief: Always attack the highest-priority task and you can't go wrong (Goethe: "things which
matter most must never be at the mercy of things which matter least").
Author's Argument: Precedence constraints and priority inversion mean the most important task can be
blocked by a trivial one, so you must sometimes treat the trivial blocker as maximally important.
Evidence: Mars Pathfinder; McLay's spoon; Lenstra's van.
Why It Is Surprising: It falsifies a revered maxim and inverts the "important first" rule in specific
cases.
```

```
Insight: Clairvoyance can be a burden — knowing the future can make scheduling harder, not easier.
Common Belief: More foreknowledge always yields a better plan.
Author's Argument: Several metrics are intractable to optimize offline (with full knowledge of start
times and durations) yet have efficient optimal online strategies (react as jobs arrive).
Evidence: The offline-intractable / online-tractable contrast; Jason Fried's "replace 'plan' with
'guess.'"
Why It Is Surprising: Uncertainty, usually a handicap, here makes the problem computationally easier.
```

```
Insight: Working full-tilt can accomplish nothing at all.
Common Belief: Maximum effort yields maximum output.
Author's Argument: When metawork consumes the system, it thrashes — running flat-out while real work
drops to zero, and collapsing suddenly rather than gradually.
Evidence: Denning's multiprogramming collapse; the over-loaded juggler.
Why It Is Surprising: Effort and output decouple entirely, and the failure is a cliff, not a slope.
```

```
Insight: To get more done, be less responsive on purpose.
Common Belief: Responsiveness is a virtue; answer quickly.
Author's Argument: A hard responsiveness guarantee can consume all your time in context switches;
minimum time-slices and interrupt coalescing protect throughput. "Be no more responsive than you need
to be."
Evidence: OS minimum slices; the post office; Knuth; office hours.
Why It Is Surprising: The productivity fix is to deliberately delay and batch, not to react faster.
```

## 10. Unique or Unusual Ideas

```
Idea: "Before you can have a plan, you must first choose a metric."
Why It Seems Unique: It relocates the hardest part of time management from execution to goal
definition, and explains why self-help gurus contradict each other (they optimize different metrics).
Potential Connection to Other Topics: Goal-setting; decision theory; OKRs; the "what gets measured gets
managed" tradition.
```

```
Idea: Procrastination as an optimal algorithm for the wrong metric.
Why It Seems Unique: It replaces a moral/psychological account of procrastination with a computational
one — the strategy is fine, the objective is mis-specified.
Potential Connection to Other Topics: Behavioral economics; goal-substitution; metric gaming
(Goodhart's law).
```

```
Idea: Clairvoyance as a burden (offline harder than online).
Why It Seems Unique: It inverts the usual value of information — full foreknowledge can make the
computation intractable while ignorance keeps it easy.
Potential Connection to Other Topics: Online vs. offline algorithms; the value (and cost) of
information; planning vs. improvisation.
```

```
Idea: Thrashing as a named human state.
Why It Seems Unique: It gives a precise systems vocabulary to the panic of being too busy to organize
being busy, including its cliff-edge onset.
Potential Connection to Other Topics: Burnout; cognitive load; overwhelm; caching (working sets).
```

```
Idea: Interrupt coalescing as a life design principle.
Why It Seems Unique: It reframes revered/despised rituals (weekly meetings, office hours, the postal
cycle) as throughput-protecting batching, and argues our devices should offer it explicitly.
Potential Connection to Other Topics: Deep work; attention economics; notification design; batch vs.
stream processing.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: The chapter praises weighted SPT as a near-universal "skeleton key," but most scheduling
problems are intractable.
Author's Position: Weighted SPT is optimal for many metrics and the best general-purpose strategy under
uncertainty; yet 84% of understood problems are intractable.
Possible Counterargument: The skeleton key's guarantees hold "under certain assumptions" and largely in
the online/uncertain regime; the reader could over-generalize it to problems (weighted Moore's,
precedence-plus-SPT, start-time constraints) where no efficient optimum exists. The chapter states both
but doesn't sharply delimit where the key works.
What Evidence Would Help Resolve It: A clear map of which real-life scheduling situations fall in the
tractable vs. intractable regions.
```

```
Issue: Is procrastination a bug or an optimal algorithm?
Author's Position: Often an optimal solution to the wrong problem (minimizing task count), driven by
badges and pre-crastination.
Possible Counterargument: This risks over-rationalizing genuine avoidance behavior; the chapter grants
procrastination "can just as easily spring up in people… trying earnestly," but doesn't distinguish
metric-misalignment procrastination from affect-driven avoidance, which the psychology literature
treats as distinct.
What Evidence Would Help Resolve It: Studies separating "wrong-metric" delay from emotion-regulation
avoidance, and whether fixing the metric (e.g. turning badges off) actually reduces procrastination.
```

```
Issue: Preemption is optimal in theory but "isn't free" in practice.
Author's Position: Preemptive EDD/SPT are optimal and restore tractability, but context switches cost
minutes for humans and cause thrashing.
Possible Counterargument: The two halves cut against each other — the algorithmically optimal strategy
(switch whenever a denser job arrives) is exactly what generates costly context switches; the chapter's
own advice (minimum slices, coalescing) is a partial retreat from pure preemption. The reconciliation
(switch, but not below a minimum slice) is stated but the tension between "always switch to the denser
job" and "commit to a minimum slice" is left informal.
What Evidence Would Help Resolve It: The optimal slice size as a function of switching cost and job
density variance — the chapter gestures at it but gives no formula for humans.
```

```
Issue: "Work dumber" (answer emails in random order) vs. "do the weighty things."
Author's Position: In a thrashing state, doing tasks in the wrong order beats doing nothing; but
otherwise you should prioritize by weight.
Possible Counterargument: These are regime-dependent (thrashing vs. normal) but a reader could take
"answer randomly" as general advice; the boundary — when you're thrashing enough that prioritization
itself is the bottleneck — is qualitative.
What Evidence Would Help Resolve It: A threshold for when the O(n²) cost of prioritizing exceeds the
benefit; the chapter names the mechanism but not the trigger point.
```

```
Issue: The debt snowball vs. avalanche controversy is acknowledged but not resolved.
Author's Position: Avalanche (highest interest) minimizes total burden; snowball (smallest balance)
minimizes the number of debts; which is better "in practice… remains an active controversy."
Possible Counterargument: The chapter treats this as a pure metric choice, but the snowball's
popularity rests on motivational/behavioral effects (momentum from early wins) that sit outside the
scheduling model entirely.
What Evidence Would Help Resolve It: Whether the behavioral benefit of early wins outweighs the interest
cost — an empirical question the chapter flags but doesn't answer.
```

```
Issue: The 84%-intractable figure is dramatic but partly an artifact.
Author's Position: Most scheduling problems are intractable, so calendar management really is hard.
Possible Counterargument: The chapter's own footnote concedes the figure includes multi-machine
problems ("managing a group of employees"), so single-machine personal scheduling is meaningfully less
dire than 84% implies — a caveat easy to lose.
What Evidence Would Help Resolve It: The tractability breakdown restricted to single-machine problems.
```

## 12. Quotable Ideas

```
Paraphrase (short): "How we spend our days is, of course, how we spend our lives." (Annie Dillard,
epigraph)
Why the Idea Matters: Stakes the whole chapter — scheduling isn't clerical, it's how a life is lived.
Source Location: Chapter epigraph (PDF p. 137).
```

```
Paraphrase (short): Before you can have a plan, you must first choose a metric.
Why the Idea Matters: The chapter's central lesson and the resolution of the self-help contradictions.
Source Location: "Handling Deadlines" (PDF p. 140).
```

```
Paraphrase (short): For minimizing maximum lateness, how long each task takes doesn't matter — you
don't even need to know.
Why the Idea Matters: The clean, surprising signature of Earliest Due Date.
Source Location: "Handling Deadlines" (PDF p. 141).
```

```
Paraphrase (short): Only prioritize a task that takes twice as long if it's twice as important.
Why the Idea Matters: The weighted-SPT density rule compressed into one memorable heuristic.
Source Location: "Getting Things Done" (PDF p. 143).
```

```
Paraphrase (short): Procrastination can be a great strategy for the wrong metric — an optimal solution
to the wrong problem.
Why the Idea Matters: The chapter's most quotable reframing of a universal affliction.
Source Location: "Picking Our Problems" (PDF pp. 145–146).
```

```
Paraphrase (short): Live by the metric, die by the metric — if you can't make app badges reflect your
priorities, turn them off.
Why the Idea Matters: A concrete defense against letting an interface pick your goals for you.
Source Location: "Picking Our Problems" (PDF p. 146).
```

```
Paraphrase (short): Sometimes what matters most can't be done until what matters least is finished, so
the trivial thing becomes as important as what it blocks.
Why the Idea Matters: The precedence-constraint insight that overturns Goethe's maxim.
Source Location: "Priority Inversion" (PDF p. 148).
```

```
Paraphrase (short): There are cases where clairvoyance is a burden — even complete foreknowledge can't
make the perfect schedule practical.
Why the Idea Matters: The counterintuitive heart of the uncertainty section.
Source Location: "Drop Everything" (PDF p. 153).
```

```
Paraphrase (short): "Replace 'plan' with 'guess' and take it easy." (Jason Fried)
Why the Idea Matters: The practical face of "clairvoyance is a burden" — a to-do list beats a calendar
when the future is foggy.
Source Location: "Drop Everything" (PDF p. 153).
```

```
Paraphrase (short): Every context switch is wasted time — metawork, not real work.
Why the Idea Matters: Names the hidden tax on multitasking that the whole back half of the chapter is
about.
Source Location: "Preemption Isn't Free" (PDF p. 154).
```

```
Paraphrase (short): Thrashing — a system running full-tilt and accomplishing nothing at all; it doesn't
bog down gradually, it falls off a cliff.
Why the Idea Matters: The chapter's name for overwhelm, with its defining cliff-edge dynamic.
Source Location: "Thrashing" (PDF p. 157).
```

```
Paraphrase (short): Be no more responsive than you need to be; decide how responsive you must be, then
stop there.
Why the Idea Matters: The throughput-protecting counsel that inverts the cult of responsiveness.
Source Location: "Interrupt Coalescing" (PDF p. 160).
```

```
Paraphrase (short): Knuth — "I do one thing at a time… I don't swap in and out"; no email since 1990.
Why the Idea Matters: The patron-saint image of a batch-processed, coalesced working life.
Source Location: "Interrupt Coalescing" (PDF p. 162).
```

```
Paraphrase (short): "Why don't we write a book on scheduling theory? It shouldn't take much time!"
Fifteen years later, *Scheduling* is still unfinished. (Eugene Lawler, epigraph)
Why the Idea Matters: A self-demonstrating joke — the greatest scheduling expert mis-scheduled a book
on scheduling — foreshadowing intractability and the planning fallacy.
Source Location: Chapter epigraph (PDF p. 137).
```

```
Paraphrase (short): A man with one watch knows what time it is; a man with two watches is never sure.
Why the Idea Matters: The compression of the whole metric-choice lesson — multiple objectives leave you
unsure what "optimal" even means.
Source Location: "Picking Our Problems" (PDF p. 144).
```

```
Paraphrase (short): "Do the difficult things while they are easy and do the great things while they are
small." (Lao Tzu, epigraph)
Why the Idea Matters: Anticipates both Shortest Processing Time and precedence logic.
Source Location: Epigraph to "Getting Things Done" (PDF p. 142).
```

```
Paraphrase (short): Programmers must not be interrupted — "Interruptions mean certain bugs. You must
not get off the train." (Ellen Ullman, epigraph)
Why the Idea Matters: The human face of the context-switch cost that the back half of the chapter
formalizes.
Source Location: Epigraph to "Preemption Isn't Free" (PDF p. 153).
```

```
Paraphrase (short): Kipling exhorts filling "the unforgiving minute / With sixty seconds' worth of
distance run." The authors: "If only. The truth is, there's always overhead."
Why the Idea Matters: Inherited time-management wisdom ignores the metawork tax; a direct rebuttal of a
revered ideal.
Source Location: "Preemption Isn't Free" (PDF pp. 154–155).
```

## 13. Psychology Connections

- **Procrastination and pre-crastination.** The chapter's central psychological move: recasting
  procrastination as optimizing task-count, and citing Rosenbaum's pre-crastination — the opposite urge
  to complete subgoals early even at extra cost.
- **Goal-setting and metric choice.** "Choose a metric first" is a goal-definition problem; ties to
  goal-substitution and to the moralization of productivity.
- **Task-switching and cognitive load.** Human context-switching costs (delays and errors "at the scale
  of minutes") connect to attention research and working-memory limits.
- **Overwhelm / burnout as thrashing.** A precise vocabulary for the panic of being too busy to organize
  being busy; the cliff-edge onset maps onto sudden burnout.
- **Zeigarnik-style tension of open tasks.** William James's "nothing so fatiguing as the eternal
  hanging on of an uncompleted task," and the felt "weight" of open items, connect to the Zeigarnik
  effect (inference; not named).
- **Motivation in debt reduction.** The snowball's popularity rests on early-win momentum — a
  behavioral/motivational effect outside the scheduling math.
- **Interface-driven behavior.** App badges imposing an implicit equal-weight metric — a case of choice
  architecture and nudging shaping what we do. The chapter's UI-hypocrisy footnote sharpens this:
  interfaces demand attention in ways a CPU would never tolerate of its own components.
- **The scheduler is the scheduled.** For people (and OSes), the machine doing the planning and the
  machine being planned are one and the same — so "straightening out your to-do list is an item *on*
  your to-do list." Planning competes with doing for the same finite resource, a distinct
  self-reference underlying overwhelm.
- **Minimal responsiveness demanded by rhythms.** The postal system gives interrupt coalescing two
  ways: you can be interrupted at most once a day, *and* the 24-hour rhythm demands minimal
  responsiveness — it makes no difference whether you reply five minutes or five hours after receipt.
  A cue for designing low-responsiveness-tolerant routines.

## 14. Mathematics and Decision Science Connections

- **Scheduling theory / operations research.** The chapter is a tour of classic single-machine
  scheduling results (Johnson, EDD, Moore, SPT, weighted SPT).
- **Computational complexity / intractability.** The tractable-vs-intractable landscape (9% vs. 84%),
  with a forward reference to chapter 8; subtle changes flipping complexity class.
- **Online vs. offline algorithms.** "Clairvoyance is a burden" is precisely the online/offline
  distinction — and a rare case where the online problem is the easier one.
- **Optimization metrics.** Maximum lateness, sum of (weighted) completion times, number of late jobs —
  each a distinct objective with its own optimum, illustrating that "optimal" is meaningless without an
  objective.
- **Ratio/greedy heuristics.** Weight ÷ duration (density) is a greedy ratio rule, mirrored in the debt
  avalanche and in optimal foraging's calories/time.
- **Real-time systems theory.** Priority inversion/inheritance, responsiveness/throughput, and minimum
  slices are core real-time scheduling concepts.
- **Connection to caching (ch. 4) and sorting (ch. 3).** Thrashing is a working-set/caching phenomenon;
  the O(n²) cost of repeatedly scanning an inbox is sorting theory applied to attention.

## 15. Sports Connections

**Direct examples from the book:** None identified. (Animal foraging appears, but not sports.)

**Inferred applications (mine):**
- **In-game clock and substitution scheduling.** A coach with fixed subs and a running clock faces a
  single-machine scheduling problem under preemption — swap a player in only if their "density"
  (impact per remaining minute) beats the player on the pitch, exactly the weighted-SPT switch rule.
- **Training-load periodization as precedence constraints.** Some adaptations can't begin until others
  are consolidated (base fitness before speed work); mis-ordering is a priority-inversion that stalls
  the whole block, McLay's-spoon style.
- **Fixture congestion as thrashing.** A club juggling league, cup, and continental fixtures past a
  threshold can "drop everything" — squad fatigue collapses results across all competitions at once
  rather than gradually, the over-loaded juggler.
- **Recovery windows as minimum slices / interrupt coalescing.** Protecting a floor of uninterrupted
  recovery (and batching media/commercial obligations into set windows) is timeboxing applied to
  athletes' throughput.
- **Rest-vs-rust as responsiveness/throughput.** Resting stars (throughput over a season) trades against
  match-sharpness (responsiveness) — the same tradeoff, and the "be no more responsive than you need to
  be" counsel argues for rotation.

## 16. AI and Machine Learning Connections

**Direct from the book:** OS schedulers, threading, context switches, the Linux scheduler (replaced with
a "less smart but faster" one), and Denning's multiprogramming/thrashing work are all core systems
material the chapter describes.

**Inferred connections (mine):**
- **LLM agent task scheduling.** An agent juggling sub-tasks faces single-machine scheduling: weighted
  SPT (value ÷ expected steps) is a strong default policy for ordering tool calls or sub-goals, and
  "clairvoyance is a burden" warns against over-planning when the environment is uncertain.
- **Context switching = KV-cache/context reloading.** Switching an agent between tasks invalidates its
  working context (Zijlstra's "context switch invalidates all caches"), an argument for batching
  related sub-tasks — interrupt coalescing for agents.
- **Thrashing as over-parallelization.** Spawning too many concurrent agents/threads that contend for
  shared memory or rate limits can collapse throughput suddenly — the multiprogramming cliff, applied
  to multi-agent systems.
- **Inference serving: responsiveness vs. throughput.** Batch size in model serving is exactly the
  minimum-slice/latency-vs-throughput tradeoff; larger batches raise throughput at the cost of
  responsiveness.
- **Reward/metric misspecification.** "Procrastination is optimizing the wrong metric" is the
  reward-hacking/Goodhart problem in RL: an agent perfectly optimizing a badly chosen objective looks
  pathological.
- **Online scheduling and regret.** Preemptive EDD/SPT-under-uncertainty are online algorithms with
  average-case optimality — the same family as the bandit/regret material in chapter 2.

## 17. Content Creation Opportunities

```
Idea Title: Procrastination is not laziness — it's the wrong math
Format: YouTube Long-form
Application Domain: Everyday Life
Hidden Principle: Optimization
Story Hook (Layer 1): You're not a bad procrastinator — you're an excellent optimizer of the wrong
problem, and your phone's little red badges chose that problem for you.
Principle Framework (Layer 2): On a single machine, every ordering takes the same total time, so you must
choose a metric before any schedule can be "best." Procrastination is often the optimal answer to a
badly-chosen metric (like task count), not a character flaw.
Best Supporting Case: App-badge logic; Rosenbaum's pre-crastination bucket study; the X-Files DoS
vampire.
Character Application: Insight: Interpreter
Psychology Angle: Pre-crastination; goal-substitution; the moralization of productivity.
Math Angle: Single-machine scheduling; unweighted SPT minimizes task count, not importance.
Sports Angle: None core.
Business Angle: Teams "busy" clearing small tickets while the strategic work slips.
Investing Angle: Churning small trades (activity) instead of the few decisions that matter.
History Angle: The productivity-metric fads that made "activity" look like progress.
AI Angle: Reward misspecification / Goodhart — perfectly optimizing a bad objective.
```

```
Idea Title: The Mars rover that procrastinated
Format: YouTube Long-form
Application Domain: History
Hidden Principle: Optimization
Story Hook (Layer 1): A $150 million spacecraft crossed 300 million miles to reach Mars — and then
started procrastinating, ignoring its most important job to do busywork.
Principle Framework (Layer 2): Priority inversion: a high-priority task stalls waiting on a resource held
by a low-priority one. The fix, priority inheritance, means a critical task lends its urgency to whatever
is blocking it — clear the blocker, not the queue.
Best Supporting Case: Mars Pathfinder (1997), with the footnote irony that the fix itself was first
deemed "lower priority"; Hedberg's fire-exit joke; McLay's spoon.
Character Application: Sigma: Architect
Psychology Angle: Why "important things first" can look exactly like procrastination.
Math Angle: Precedence constraints; priority inheritance.
Sports Angle: Training-load ordering as precedence constraints.
Business Angle: A key project stalled behind a trivial approval nobody prioritized.
Investing Angle: A big decision blocked by a small unresolved dependency.
History Angle: The near-loss of Pathfinder as a landmark real-time-systems lesson.
AI Angle: Resource contention and deadlock in multi-agent / real-time systems.
```

```
Idea Title: Working full-tilt and getting nothing done — the science of thrashing
Format: YouTube Long-form
Application Domain: Everyday Life
Hidden Principle: Feedback Loops
Story Hook (Layer 1): There's a specific state where you work as hard as you possibly can and accomplish
literally nothing — computers have a name for it, and a way out.
Principle Framework (Layer 2): Past a load threshold, the overhead of switching between tasks (the context
switch) exceeds the work done, so throughput collapses to zero — a cliff, not a slope. The escape is a
minimum time-slice: commit to one thing long enough to finish it.
Best Supporting Case: The over-loaded juggler; Denning's multiprogramming collapse; Knuth's no-email
batch-processing life.
Character Application: Echo: Observer
Psychology Angle: Overwhelm/burnout as a cliff, not a slope; the panic of being too busy to plan.
Math Angle: The O(n²) cost of re-prioritizing an overflowing inbox; the minimum time-slice.
Sports Angle: Fixture congestion collapsing a whole season at once.
Business Angle: A team so overloaded that coordination consumes all its capacity.
Investing Angle: Over-monitoring a portfolio until you trade on noise and net nothing.
History Angle: The 1960s discovery of thrashing in multiprogramming systems.
AI Angle: Over-parallelization collapsing multi-agent throughput.
```

```
Idea Title: To get more done, be less responsive
Format: YouTube Short
Application Domain: Business
Hidden Principle: Optimization
Story Hook (Layer 1): The most productive thing you can do today is answer people slower — computers
figured this out decades ago.
Principle Framework (Layer 2): Responsiveness and throughput trade off; batching interruptions ("interrupt
coalescing") sacrifices instant replies to protect the long, uninterrupted blocks where real work
happens.
Best Supporting Case: The post office as free interrupt coalescing; a monthly bill-paying day; Knuth
reviewing mail every three months.
Character Application: Blaze: Executor
Psychology Angle: The cult of responsiveness; deep work.
Math Angle: The minimum slice; batching to protect throughput.
Sports Angle: Rest-vs-rust as responsiveness vs. throughput.
Business Angle: Office-hours and batched Slack over always-on availability.
Investing Angle: Checking the market on a schedule instead of reacting tick-by-tick.
History Angle: The pre-email cadence of letters and set correspondence days.
AI Angle: Batch size in inference serving.
```

```
Idea Title: The one question that ends every time-management argument
Format: YouTube Short
Application Domain: Everyday Life
Hidden Principle: Decision Making
Story Hook (Layer 1): Getting Things Done, Eat That Frog, The Now Habit — they all contradict each other,
and it's not because some of them are wrong.
Principle Framework (Layer 2): "Before you can have a plan, you must first choose a metric." Each guru is
optimal for a different objective (fewest late tasks vs. most tasks done vs. highest-weighted first), so
the argument dissolves once you name what you're optimizing.
Best Supporting Case: The conflicting self-help gospels; EDD vs. SPT vs. weighted SPT.
Character Application: Nova: Strategist
Psychology Angle: Goal definition before execution.
Math Angle: Different metrics → different optimal algorithms.
Sports Angle: Season-long throughput vs. next-match sharpness.
Business Angle: OKRs that conflict because no one named the single metric that ranks them.
Investing Angle: "Best strategy" is undefined until you fix the objective (return, drawdown, income).
History Angle: The self-help industry's contradictory gospels, reconciled by one question.
AI Angle: You can't call a policy optimal without first specifying an objective function.
```

```
Idea Title: The expert who couldn't schedule his own book
Format: YouTube Short
Application Domain: Everyday Life
Hidden Principle: Cognitive Bias
Story Hook (Layer 1): The single greatest expert on scheduling theory once said writing a book about it
"shouldn't take much time" — fifteen years later it still wasn't finished.
Principle Framework (Layer 2): Most scheduling problems are intractable (no efficient optimal solution
exists), and the planning fallacy is the human echo: estimates ignore the combinatorial explosion of
dependencies, so plans systematically run long.
Best Supporting Case: The Eugene Lawler epigraph; the survey finding 84% of scheduling problems
intractable.
Character Application: Insight: Interpreter
Psychology Angle: The planning fallacy; the gap between estimate and reality.
Math Angle: Why most scheduling problems have no efficient optimal solution.
Sports Angle: None core.
Business Angle: Why big projects overrun no matter how experienced the planner.
Investing Angle: Underestimating how long a "simple" integration or turnaround will take.
History Angle: Famous overruns as instances of the planning fallacy meeting intractability.
AI Angle: Why "just plan it perfectly" fails for hard combinatorial problems.
```

```
Idea Title: Your phone is a hypocrite
Format: YouTube Short
Application Domain: Business
Hidden Principle: Optimization
Story Hook (Layer 1): Your computer would never let its own apps interrupt it the way its apps interrupt
you — it batches everything internally, then throws pop-ups in your face.
Principle Framework (Layer 2): Internally, systems coalesce interrupts to protect throughput; the notif-
ication design pointed at you does the opposite, optimizing for engagement, not your productivity. The
same principle, applied to two different objectives.
Best Supporting Case: The UI-hypocrisy footnote; app badges; the post office as free interrupt coalescing.
Character Application: Echo: Observer
Psychology Angle: The cost of interruption; attention as a scarce resource.
Math Angle: Responsiveness vs. throughput; the minimum slice.
Sports Angle: None core.
Business Angle: Engagement-optimized product design vs. the user's actual interests.
Investing Angle: Trading apps engineered to trigger reactions, not returns.
History Angle: The attention-economy turn in software design.
AI Angle: Batching in inference serving; deciding when to interrupt an agent.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B01-C05-01
Title: Choose a metric before you plan
Type: Insight
Summary: On a single machine, if you do all your tasks, every ordering takes the same total time — so
order only matters relative to a goal. "Before you can have a plan, you must first choose a metric."
Different metrics yield different optimal algorithms, which is why time-management gurus contradict each
other.
Source: Algorithms to Live By, ch. 5, "Handling Deadlines" (PDF pp. 139–140)
Tags: scheduling, metric-choice, single-machine, core-insight
Related Concepts: EDD, SPT, weighted SPT, procrastination
```

```
CARD ID: B01-C05-02
Title: Johnson's Rule (two-machine scheduling)
Type: Model
Summary: Selmer Johnson (1954), the first optimal scheduling algorithm: for jobs that pass through
machine A then B (laundry: wash→dry), do the shortest step first if it's on the first machine, last if
on the second, working inward from both ends to maximize overlap. "Start with the lightest wash, end
with the smallest hamper."
Source: Algorithms to Live By, ch. 5, "Spending Time Becomes a Science" (PDF pp. 138–139)
Tags: Johnson, two-machine, scheduling-history, model
Related Concepts: Single-machine scheduling, overlap
```

```
CARD ID: B01-C05-03
Title: Earliest Due Date (EDD)
Type: Model
Summary: Do the soonest-due task first to minimize maximum lateness — provably optimal. Strikingly,
task durations are irrelevant (you needn't know them). With precedence, build back-to-front (latest-due
among unblocked tasks goes last); preemptive version switches to an arriving task only if it's due
sooner.
Source: Algorithms to Live By, ch. 5, "Handling Deadlines" (PDF pp. 140–141)
Tags: EDD, maximum-lateness, optimal, model
Related Concepts: Moore's Algorithm, precedence constraints, preemption
```

```
CARD ID: B01-C05-04
Title: Moore's Algorithm — minimize the number of late items
Type: Model
Summary: To minimize how many items spoil/go late (CSA produce), schedule by due date and drop the
largest already-scheduled item whenever you fall behind (forgo the watermelon); dropped items are done
last in any order. Optimal for equal-value items; becomes intractable once items differ in importance.
Source: Algorithms to Live By, ch. 5, "Handling Deadlines" (PDF pp. 141–142)
Tags: Moore, number-of-late, produce, model
Related Concepts: EDD, weight, intractability
```

```
CARD ID: B01-C05-05
Title: Shortest Processing Time and the density rule
Type: Model
Summary: Do the quickest task first to minimize the sum of completion times — shortens the to-do list
fastest (4-day+1-day: small-first saves clients 3 days). Weighted version: order by weight ÷ duration —
"only prioritize a task that takes twice as long if it's twice as important." Consultants: work highest
hourly rate first.
Source: Algorithms to Live By, ch. 5, "Getting Things Done" (PDF pp. 142–144)
Tags: SPT, sum-of-completion-times, density, weight, model
Related Concepts: Weighted SPT skeleton key, debt avalanche/snowball, foraging
```

```
CARD ID: B01-C05-06
Title: Weighted SPT — the skeleton key
Type: Model
Summary: Ordering by weight ÷ duration minimizes the sum of weighted completion times and, *under
certain assumptions*, several other weighted metrics too — scheduling theory's closest thing to a Swiss
Army knife, and the best general-purpose strategy under uncertainty. But it is not universal: most other
scheduling metrics are intractable, so the key does not open every door. Preemptive: switch if an
arriving job's density beats the current one.
Source: Algorithms to Live By, ch. 5, "Drop Everything" (PDF pp. 152–153)
Tags: weighted-SPT, skeleton-key, uncertainty, model
Related Concepts: Density rule, preemption, clairvoyance-as-burden
```

```
CARD ID: B01-C05-07
Title: Debt avalanche vs. debt snowball
Type: Case
Summary: Avalanche = pay the highest-interest debt first (weighted SPT) to minimize total burden fastest;
snowball = pay the smallest balance first (unweighted SPT) to minimize the number of debts. Which is
better "in practice remains an active controversy" — the snowball's edge is motivational (early wins),
outside the scheduling math.
Source: Algorithms to Live By, ch. 5, "Getting Things Done" (PDF p. 144)
Tags: debt, avalanche, snowball, weighted-vs-unweighted, case
Related Concepts: SPT, weight, metric choice
```

```
CARD ID: B01-C05-08
Title: Procrastination is optimizing the wrong metric
Type: Insight
Summary: Clearing many trivial tasks first (unweighted SPT) optimally minimizes the number of open
items — a great strategy for a metric you didn't mean to choose. App badges impose an implicit
equal-weight metric ("live by the metric, die by the metric"; if you can't fix them, turn them off).
The X-Files vampire is a denial-of-service attack; Rosenbaum's "pre-crastination" shows people hasten
subgoals even at extra cost.
Source: Algorithms to Live By, ch. 5, "Picking Our Problems" (PDF pp. 144–146)
Tags: procrastination, pre-crastination, metric-gaming, badges, insight
Related Concepts: SPT, choose-a-metric, Goodhart (inferred)
```

```
CARD ID: B01-C05-09
Title: Priority inversion and priority inheritance (Mars Pathfinder)
Type: Case
Summary: In 1997 the $150M Mars Pathfinder rover kept resetting because a low-priority task blocked a
resource the highest-priority task needed, while medium tasks ran — priority inversion. JPL beamed a
fix: priority inheritance (the blocker temporarily inherits the blocked task's priority). Footnote
irony: the bug fix had itself been deemed "lower priority." Hedberg: "if you're flammable and have legs,
you are never blocking a fire exit."
Source: Algorithms to Live By, ch. 5, "Priority Inversion" (PDF pp. 146–148)
Tags: priority-inversion, priority-inheritance, Mars-Pathfinder, real-time, case
Related Concepts: Precedence constraints, blocking, "matters most vs. least"
```

```
CARD ID: B01-C05-10
Title: Precedence constraints — the trivial thing must come first
Type: Concept
Summary: When a task can't start until another finishes, the trivial blocker becomes as important as
what it blocks — overturning Goethe's "things which matter most must never be at the mercy of things
which matter least." McLay: can't leave until kids eat, can't eat without a spoon. EDD adapts easily
(build back-to-front); SPT-with-precedence is intractable.
Source: Algorithms to Live By, ch. 5, "Priority Inversion" / "The Speed Bump" (PDF pp. 148–150)
Tags: precedence-constraints, blocking, intractability, concept
Related Concepts: Priority inversion, EDD back-to-front, Lawler
```

```
CARD ID: B01-C05-11
Title: Most scheduling problems are intractable
Type: Study
Summary: A survey found ~7% of scheduling problems have unknown status; of the 93% understood, only 9%
are efficiently solvable and 84% are proven intractable. Subtle changes tip problems over the line
(weights on Moore's Algorithm; start-time constraints). So struggling with your calendar is genuinely
hard. Caveat: the 84% includes multi-machine problems ("managing a group of employees").
Source: Algorithms to Live By, ch. 5, "The Speed Bump" (PDF pp. 150–151)
Tags: intractability, complexity, scheduling-landscape, study
Related Concepts: Precedence constraints, preemption restoring tractability, ch. 8
```

```
CARD ID: B01-C05-12
Title: Preemption changes the game — and clairvoyance can be a burden
Type: Insight
Summary: Preemption (stopping a task midway) restores efficient solutions to otherwise-intractable
problems, and keeps EDD/SPT optimal even when you don't know when tasks will arrive. Counterintuitively,
several metrics are intractable to optimize offline (full foreknowledge) yet easy online — so knowing
the future can be a burden. Jason Fried: "Replace 'plan' with 'guess' and take it easy."
Source: Algorithms to Live By, ch. 5, "Drop Everything" (PDF pp. 151–153)
Tags: preemption, uncertainty, online-vs-offline, clairvoyance-burden, insight
Related Concepts: Weighted SPT, to-do list vs. calendar, intractability
```

```
CARD ID: B01-C05-13
Title: The context switch is metawork
Type: Concept
Summary: Preemption isn't free: every task switch costs overhead (bookmark, choose next, reload state)
that is not real work. For humans it costs minutes, not microseconds — anyone interrupted more than a
few times an hour risks doing no work at all. Writing is "blacksmithing": ~30–35 minutes just to heat
up, so block ≥90 minutes.
Source: Algorithms to Live By, ch. 5, "Preemption Isn't Free" (PDF pp. 153–155)
Tags: context-switch, metawork, deep-work, interruption, concept
Related Concepts: Thrashing, minimum slice, responsiveness/throughput
```

```
CARD ID: B01-C05-14
Title: Thrashing — full-tilt, accomplishing nothing
Type: Insight
Summary: When metawork consumes a system it thrashes: running flat-out while real work drops to ~zero,
and performance collapses off a cliff rather than degrading gradually (the juggler with one ball too
many drops everything). Denning (1960s) diagnosed it in memory management; scheduling meets caching as
working sets evict each other (Zijlstra: "context switch invalidates all caches").
Source: Algorithms to Live By, ch. 5, "Thrashing" (PDF pp. 155–157)
Tags: thrashing, overwhelm, Denning, working-set, insight
Related Concepts: Context switch, caching (ch. 4), interrupt coalescing
```

```
CARD ID: B01-C05-15
Title: Escaping thrashing — say no, or work dumber
Type: Insight
Summary: Denning's landmark 1960s paper frames prevention as the primary lever — add capacity (more
RAM) or say no (refuse a job without room for its working set). "Work dumber" is the fallback *only when
you are already thrashing* and can't do either: scanning an inbox of n for the most important message is
O(n²) (3× as full → 9× as long), so in a thrashing state answer emails in random/on-screen order rather
than prioritizing (doing tasks in the wrong order beats doing nothing). Linux replaced its scheduler
with a "less smart but faster" one.
Source: Algorithms to Live By, ch. 5, "Thrashing" (PDF pp. 157–158)
Tags: thrashing, work-dumber, say-no, O(n-squared), insight
Related Concepts: Sorting (ch. 3), context switch, minimum slice
```

```
CARD ID: B01-C05-16
Title: Responsiveness vs. throughput, and the minimum slice
Type: Model
Summary: Real-time scheduling negotiates responsiveness (react fast) against throughput (get more
done). A hard responsiveness guarantee can spend the whole slice context-switching, so OSes set a
minimum slice (Linux ~0.75 ms; humans "at least several minutes") — the principle behind
timeboxing/pomodoros. "Be no more responsive than you need to be."
Source: Algorithms to Live By, ch. 5, "Interrupt Coalescing" (PDF pp. 159–160)
Tags: responsiveness, throughput, minimum-slice, timeboxing, model
Related Concepts: Interrupt coalescing, context switch, thrashing
```

```
CARD ID: B01-C05-17
Title: Interrupt coalescing
Type: Insight
Summary: Batch interruptions and handle them at a fixed interval instead of one by one, to protect
throughput — but note it *trades away* responsiveness (you can't respond faster than the interval, so
it's unsuitable when something needs a fast reply). Pay all bills on a "bill-paying day"; check email
once a day; hold office hours; the weekly meeting is redeemed as batched interruption; the post office
gives coalescing for free (and its 24-hour rhythm also demands minimal responsiveness — reply timing
within the day is irrelevant). Knuth is the patron saint (no email since 1990; TeX tuned every six
years). Norvig: three separate downtown trips are "a one-line bug in your algorithm."
Source: Algorithms to Live By, ch. 5, "Interrupt Coalescing" (PDF pp. 159–162)
Tags: interrupt-coalescing, batching, deep-work, Knuth, insight
Related Concepts: Minimum slice, responsiveness/throughput, Do Not Disturb
```

```
CARD ID: B01-C05-18
Title: Scientific Management and the Gantt chart
Type: Study
Summary: Frederick Taylor (from 1874, Midvale Steel) invented "Scientific Management," centered on a
planning board showing each machine's current and waiting tasks; Henry Gantt turned it into the Gantt
chart (1910s), used on the Hoover Dam and Interstate Highway System and still on the walls at Amazon,
IKEA, and SpaceX. They made scheduling an object of study but didn't solve which schedule is best.
Source: Algorithms to Live By, ch. 5, "Spending Time Becomes a Science" (PDF pp. 138–139)
Tags: Taylor, Gantt, scheduling-history, project-management, study
Related Concepts: Johnson's Rule, optimization
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: Good scheduling starts with choosing a metric, because on a single machine (you) every
ordering of all your tasks takes the same total time. Computer science gives provably optimal
algorithms per metric — Earliest Due Date for maximum lateness, Shortest Processing Time (weighted by
importance ÷ duration) for the to-do list — but most scheduling problems are intractable, the metawork
of switching tasks ("context switch") is a real cost that at the extreme becomes "thrashing," and the
cure is often to be deliberately less responsive by batching interruptions ("interrupt coalescing").
Procrastination is frequently an optimal solution to the wrong problem.

Top 5 Concepts:
1. Choose a metric first (single-machine scheduling)
2. Earliest Due Date (maximum lateness) and Shortest / weighted Processing Time (the "skeleton key")
3. Precedence constraints, priority inversion, and priority inheritance
4. Intractability of most scheduling problems; preemption and clairvoyance-as-burden
5. Context switch → thrashing → interrupt coalescing / minimum slice

Top 3 Claims:
1. On one machine every ordering takes equally long, so you must choose a metric before any schedule can
   be "best."
2. Weighted SPT (weight ÷ duration) is a near-universal optimal strategy and the best default under
   uncertainty; yet 84% of understood scheduling problems are intractable.
3. Preemption isn't free — the context switch is real overhead that collapses into thrashing, curable by
   minimum slices and interrupt coalescing.

Top 3 Cases:
1. Mars Pathfinder's priority inversion (and its self-referential "lower priority" bug)
2. Donald Knuth's batch-processing, no-email-since-1990 life (interrupt coalescing to the extreme)
3. The conflicting time-management bestsellers, dissolved by "choose a metric first"

Top 3 Studies:
1. Selmer Johnson (1954) — the first optimal scheduling algorithm
2. Rosenbaum et al. (2014) — pre-crastination (hastening subgoals at extra cost)
3. Peter Denning (1960s) — thrashing / multiprogramming collapse

Most Unique Idea: Clairvoyance can be a burden — several scheduling metrics are intractable to optimize
with full foreknowledge yet easy to handle online, so ignorance-plus-reaction beats planning; "replace
'plan' with 'guess.'"

Most Counterintuitive Idea: Procrastination is often an optimal algorithm for the wrong metric (and,
relatedly, devotion to "important things first" can look exactly like procrastination via priority
inversion).

Biggest Weakness or Open Question: The chapter promotes weighted SPT as a "skeleton key" and preemption
as optimal while conceding 84% intractability and that context switches make preemption costly —
without sharply delimiting where the key works or resolving the tension between "always switch to the
denser job" and "commit to a minimum slice"; and it flags but doesn't settle the snowball-vs-avalanche
and metric-vs-emotion accounts of debt and procrastination.

Best Content Opportunity: A long-form video on "procrastination is optimizing the wrong metric" — app
badges, pre-crastination, and the X-Files DoS vampire — landing on "choose a metric first" and the
Goodhart/reward-hacking parallel.
```
