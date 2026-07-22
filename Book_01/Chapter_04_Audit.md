# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 4: Caching — Forget About It
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 112–136, re-read against Chapter_04_Extraction.md
**Date:** 2026-07-21

---

## Missing Items

**1. The Sherlock Holmes epigraph on the limited-attic theory of memory.** (PDF p. 116) The "Eviction
and Clairvoyance" section opens with Holmes: "there comes a time when for every addition of knowledge
you forget something that you knew before. It is of the highest importance, therefore, not to have
useless facts elbowing out the useful ones." This is the *folk theory the chapter overturns* — the
"memory as limited storage" view that Anderson later replaces with "organization, not storage." The
extraction captured the James epigraph but dropped Holmes, which is arguably the more load-bearing one
because the whole Anderson section is an argument against it.

**2. The Lewis Carroll "map on the scale of a mile to the mile" epigraph.** (PDF p. 121) The CDN
section opens with Carroll's fable of a map so detailed it covers the whole country and blocks the
sunlight, so "we now use the country itself, as its own map." This is a witty statement of *why you
can't cache everything* — a perfect-fidelity copy is as unwieldy as the original — and it frames the
proximity/geography argument. Omitted.

**3. The Lydia Davis epigraph on sharp consciousness / almost no memory.** (PDF p. 113) "A certain
woman had a very sharp consciousness but almost no memory.… She remembered enough to work, and she
worked hard." Frames the memory-hierarchy section and reappears as a motif (Davis also gave chapter 2's
rereading epigraph). Minor but reusable.

**4. The Callimachus and Steven Wright epigraphs.** (PDF p. 132) "A big book is a big nuisance"
(Callimachus, librarian at Alexandria, given as 305–410 BC) and "Why don't they make the whole plane
out of that black box stuff?" (Steven Wright) frame "The Tyranny of Experience." Callimachus is a
neat ancient statement of "bigger is slower / a bigger store is a burden," directly on-theme.

**5. The full author roster of the library "cache" shelf.** (PDF p. 119) The extraction abstracts this
as "recently used books by major authors," but the chapter lists ~two dozen names (Cormac McCarthy,
Pynchon, Salinger, Sontag, Morrison, Plath, DFW, Gaiman…) precisely to make vivid that the *cache holds
the good stuff*. Not essential, but the concreteness is part of the rhetorical point.

**6. The Z-order / Alt+Tab interface detail and Aza Raskin quote.** (PDF p. 118) The extraction
mentions Z-order and Alt/Command+Tab in passing in §4, but the chapter's actual point — that LRU is
*already built into the interfaces we use*, with windows stacked most-recent-on-top and task-switchers
listing most-to-least recent — is a distinct and reusable observation, with Aza Raskin's line that
"much of your time using a modern browser is spent in the digital equivalent of shuffling papers." The
extraction under-weights this as evidence that LRU is ubiquitous and intuitive.

**7. The footnote on displaying files by "Last Opened."** (PDF p. 136) A concrete, immediately
actionable takeaway: override the default alphabetical folder browsing and sort by "Last Opened" rather
than "Name," because "what you're looking for will almost always be at or near the top." This is the
single most directly usable computer tip in the chapter and the extraction omitted it.

**8. The "memory wall" mechanism, and the factory analogy.** The extraction names the memory wall but
drops the vivid mechanism: Moore's Law doubled processor speed (transistors doubling every two years,
Gordon Moore 1975) while memory speed lagged, so the *relative* cost of a memory access rises
exponentially — "processors that twiddled their thumbs ever faster." The factory analogy (double
manufacturing speed but parts arrive at the same sluggish pace = "twice as idle") is a strong teaching
image the extraction lost.

**9. Anderson's own framing that his theories (including his own) were wrong.** (PDF p. 129) The quote
"there was something missing in the existing theories of human memory, including my own… all of these
theories characterize memory as an arbitrary and non-optimal configuration" is a notable instance of a
researcher overturning his own prior work — a stronger version of the "against the prevailing view"
note in the extraction.

## Corrections Needed

**1. "Random Eviction is not half bad" — the claim is about having a cache at all, not about Random
specifically being good.**
- Extraction (§3, card 5): mostly correct, but the phrasing "even Random Eviction is not half bad"
  could be read as endorsing Random. The chapter's actual point (PDF pp. 117–118) is subtler: *just
  having a cache* makes a system more efficient "regardless of how you maintain it," because used items
  return soon anyway. Random is the vehicle for showing the cache itself is what helps. The extraction's
  card 5 gets this right in the summary but the §3 headline should foreground "having a cache helps,"
  not "Random is fine."

**2. The factor-of-2 guarantee is a worst-case competitive ratio, and applies to the whole request
sequence.**
- Extraction (§3, §5, card 12): states "within a factor of 2 of the offline optimum," which is correct,
  but should specify it is the *total* search time over the entire sequence and a *worst-case* bound
  (Sleator & Tarjan analyzed worst case over all possible request sequences). The extraction says
  "worst-case guarantee" in §5's limitations but the claim entries state it more flatly. Minor
  tightening for cross-book precision.

**3. Ebbinghaus's date and duration.**
- Extraction dates the forgetting curve "1879 onward (self-experiments over about a year)." The chapter
  says the science of memory "is said to have begun in 1879" and that Ebbinghaus pursued the habit "over
  the course of a year." Accurate, but "1879" is the founding date of the field per the chapter, not
  necessarily the precise publication date of the curve — the extraction should not imply 1879 is when
  the curve itself was published.

## Overgeneralizations

**1. "LRU is the overwhelming favorite" stated more absolutely than the hedge warrants.** The chapter
says LRU "and minor tweaks thereof" is the overwhelming favorite, and that "some [schemes] can beat LRU
under the right conditions." The extraction preserves the hedge in card 3 and §3 but §19's top-claims
list ("LRU is the best practical eviction policy") drops the "and minor tweaks" and the conditional.
Worth carrying the qualifier into the summary so cross-book comparison doesn't overstate LRU's
supremacy.

**2. "People love movies set where they live" — one informal map.** The extraction mostly flags this
(§5 "informal map, not a controlled study"), but the Netflix claim is stated confidently in the case
and card. It is a single blogger's 2011 map of "Local Favorites," not a study; the strength of the
"overwhelmingly" should be attributed to Mertes's map, not treated as an established finding.

**3. Anderson & Schooler generalized from three corpora to "reality itself."** The chapter's line
"reality itself has a statistical structure that mimics the Ebbinghaus curve" is a large generalization
from NYT headlines, some parent-child recordings, and one email inbox. The extraction flags the eclectic
datasets in §5/§11, but the confident "reality itself" framing (which the chapter itself uses) should be
explicitly marked as the authors' extrapolation, not a measured universal.

## Important Nuance Lost

**1. Caching's original purpose was staging, not anticipation — Wilkes's insight was the twist.** (PDF
p. 115) The chapter is careful that the small fast memory was *first* just a convenient place to work on
data before writing it back; Wilkes's contribution was realizing it could *deliberately hold on to*
likely-future data. The extraction collapses this into "the birth of caching" and loses the
staging-vs-anticipation distinction that is the actual conceptual move.

**2. The "temporal locality" mechanism has two sources.** (PDF p. 118) The chapter says temporal
locality arises *both* from how computers solve problems (loops making rapid related reads/writes) *and*
from how people solve problems (switching among email/browser/word-processor). The extraction gives the
human example but under-states that the machine and human sources are presented as parallel — which is
the chapter's core "computers and minds face the same problem" move.

**3. The library redesign's honest downside.** (PDF p. 121) The chapter concedes students "might be
puzzled" that popular books appear sometimes in the stacks and sometimes in the lobby, and answers it
(returned books are missing from the stacks either way during reshelving limbo). The extraction notes
the caveat but drops the chapter's own resolution of it, which is what makes the proposal defensible.

**4. Hennessy's archive detail (a whole day to retrieve).** (PDF p. 124) Hennessy's quote specifies that
the deepest level — the university archives — takes "a whole day to get stuff out of it." This concrete
latency figure makes the multi-level hierarchy tangible and the extraction generalized it away.

**5. The "self-organizing mess" vs. "unorganized mess" distinction.** (PDF p. 128) The chapter's exact
phrasing — "What might appear to others to be an unorganized mess is, in fact, a self-organizing mess" —
is the precise conceptual payoff, and it's sharper than the extraction's paraphrase. The word
"self-organizing" (not merely "already organized") is doing the work.

## Additional Cases and Examples

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
People / Organization: The authors (footnote)
Context: A directly actionable computer tip.
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
People / Organization: Lewis Carroll (epigraph)
Context: Framing the CDN/geography section.
What Happened: In Carroll's fable, cartographers make a map "on the scale of a mile to the mile"; the
farmers object that it would blot out the sunlight, so "we now use the country itself, as its own map,
and it does nearly as well."
Outcome: A comic proof that a perfect-fidelity copy is as unwieldy as the original — hence you cache
selectively and by proximity.
Concept Illustrated: Why you can't cache everything; the point of a cache is that it's smaller/closer.
Why This Case Is Useful: A memorable literary hook for the whole idea of selective, local caching.
Potential for Reuse: High
```

## Additional Research Evidence

None materially missing. The re-read confirms the chapter's evidence is heavier on named designs and
practitioner anecdote than on controlled studies, which the extraction reflects. One sharpening: the
Anderson & Schooler analysis should be tagged explicitly as *corpus/observational* rather than
experimental, so it isn't cross-compared as a controlled study.

## Potential Disagreements to Track Later

1. **Gigerenzer / ecological rationality.** The "forgetting is optimal tuning to the environment" thesis
   is squarely in the ecological-rationality tradition; it will align with Gigerenzer and clash with
   accounts (interference theory, decay theory) that treat forgetting as a byproduct of a lossy store.
2. **The "extended mind" / externalized memory literature (Clark & Chalmers; Sparrow's "Google
   effect").** Turning the pile, the file box, and the library into memory devices is an externalized-
   cognition claim; a cross-book comparison with the "digital memory makes us forget" literature would
   be sharp.
3. **Behavioral-economics recency bias.** LRU is a normative endorsement of recency; behavioral
   economics treats recency bias as an error. As in earlier chapters, the book will argue a "bias" is
   actually rational — track this recurring move.
4. **Marie Kondo / decluttering culture (again).** "Keep what you last used" (LRU) and "your pile is
   optimal" directly contradict "group like with like" and spark-joy tidying — a continuation of
   chapter 3's tension.
5. **Aging and neuroscience.** "Decline is learning" will collide with clinical neuroscience on genuine
   age-related cognitive decline; the authors hedge, but the framing invites disagreement worth
   tracking.

## Additional Content Opportunities

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

---

## Recommended Changes to the Original Extraction

1. **§7 (Cases and Stories)** — add three cases: LRU-in-your-interface (Z-order/Alt+Tab, Aza Raskin);
   "sort files by Last Opened" (the footnote tip); and the Lewis Carroll "mile to the mile" map. The
   Carroll fable and the Last-Opened tip are the highest-value additions.

2. **§3, card 5** — reframe the Random Eviction claim so the headline is "just having a cache helps,
   regardless of policy," not "Random Eviction is fine."

3. **§4 / §2 (temporal locality)** — state explicitly that temporal locality has *two parallel sources*
   (machine loops and human task-switching), since that parallel is the chapter's central "same problem"
   move.

4. **§5 (caching history)** — restore the staging-vs-anticipation distinction: the fast memory was first
   just a workspace; Wilkes's insight was to deliberately retain likely-future data.

5. **§12 (Quotable Ideas)** — add the Sherlock Holmes epigraph (the limited-attic theory the chapter
   overturns), the Lewis Carroll map fable, and Callimachus's "a big book is a big nuisance."

6. **§9 / §17** — add the "Last Opened" file-sorting tip as the chapter's most actionable takeaway
   (currently missing from insights and content ideas).

7. **§3 / §5 (Anderson & Schooler)** — mark "reality itself has a statistical structure" as the authors'
   extrapolation from three eclectic corpora, and tag the analysis as corpus/observational, not
   experimental.

8. **§19 (Cross-Book Summary)** — carry the LRU hedge ("and minor tweaks; can be beaten under the right
   conditions") into the top-claims list so LRU's supremacy isn't overstated; and note that recency is a
   poor proxy for importance (the rarely-used-but-critical item problem) as a standing weakness.

9. **§4 (memory hierarchy) / §5** — add the memory-wall mechanism (Moore's Law outpacing memory; the
   "twice as idle factory" analogy) and Hennessy's "a whole day" archive latency for concreteness.

10. **§11 (Tensions)** — sharpen the chapter-3-vs-chapter-4 messiness distinction using the chapter's own
    "self-organizing mess" (not merely "already organized") phrasing.

**Sections that are fine as they stand:** §1 (thesis), §6 (experiments — the alternative-explanation
fields are doing real work, especially the curve-matching-is-correlational caveat), §8 (teaching
examples), §10 (unique ideas), §14 (mathematics), §16 (AI — the KV-cache/RAG mapping is the strongest
inferred link and is accurate). §15 (sports) is correctly marked as containing no direct examples.
