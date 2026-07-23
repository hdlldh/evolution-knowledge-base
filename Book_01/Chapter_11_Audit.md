# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 11: Game Theory — The Minds of Others
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 292–323 (re-read against Chapter_11_Extraction.md)
**Date:** 2026-07-22

Adversarial re-read of the chapter text against the first-pass extraction. Findings grouped by type; the
"Recommended Changes" at the end are the subset applied back into the extraction.

---

## 1. Missing Items (present in the text but absent or thin in the extraction)

- **The three auction formats (Dutch/descending, English/ascending, sealed-bid first-price).** The
  extraction jumps from "auctions" to the Vickrey (second-price) auction, but the chapter carefully walks
  through the sealed-bid first-price auction (winner overpays; must shade bids → recursion), the Dutch/
  descending auction (Aalsmeer Flower Auction; store markdowns; landlords), and the English/ascending
  auction (the familiar one; lets the $25-valuer win at just over $10). These set up *why* mixing private
  valuations with public bidding is toxic. The §16 math list mentions them, but they deserve a framework/
  example presence since they carry the cascade argument. Added.

- **The Kant / categorical imperative footnote.** Binmore's footnote notes that the prisoner's dilemma
  "obliterates" Kant's categorical imperative (acting as you'd wish everyone to act would beat the
  equilibrium, but that outcome isn't stable). The extraction's Tension #1 alludes to Kant but doesn't
  anchor it to the footnote; worth a clean line since it's a genuine philosophical stake.

- **The halting-problem → Turing-machine footnote.** The chapter footnotes that the halting problem is
  literally what inspired Turing to define computation (the Turing machine). The extraction's §14 mentions
  this parenthetically; fine, flagging for completeness — no change needed.

- **Sartre's "Hell is other people" and its revision.** The extraction's thesis and cards capture "seek
  games where honesty is dominant, then be yourself," but omit the Sartre frame the chapter uses to close
  (others complicate our self-knowledge; interacting need not be a nightmare — in the wrong game it can
  be). A quotable-worthy hinge; added.

- **Fundamental vs. technical investors; high-frequency trading critique.** The chapter distinguishes
  "fundamental" investors (trading on underlying value) from "technical" investors (trading on
  fluctuations), and notes the complaint that algorithmic trading worsens market irrationality — but "the
  fault is often not with the players but the game." The extraction folds the flash crash into cascades
  but drops this distinction. Minor; a phrase added to the cascade material.

## 2. Corrections Needed (statements that distort the text)

- **Self-driving-cars congestion figure.** The extraction's Card B01-C11-04 says self-driving cars "can
  cut congestion by at most ~25%." The book's exact logic: since anarchy is only 4/3 as congested as
  perfect coordination, perfectly coordinated commutes would be "only 3/4 as congested as they are now" —
  i.e., a ~25% reduction *at best from perfect coordination*, not specifically from self-driving cars
  (which also reduce accidents and can platoon). The paraphrase is defensible but slightly overstates
  what the book attributes to self-driving cars specifically. Softened to match the book's "3/4 as
  congested" framing.

- **Roughgarden & Tardos institutions.** The extraction lists Roughgarden at Stanford and Tardos at
  Cornell — both correct per the text. Confirmed, no change.

- **"$479,500" Dwan bet and "2–7."** Confirmed against the text (Texas Hold 'Em's worst hand, deuce-
  seven; opponent Sammy George). No change.

## 3. Overgeneralizations (author hedges flattened)

- **"Emotions are evolution's mechanism design."** Stated by the authors as an interpretive claim
  ("emotion is mechanism design in the species," a deliberate paraphrase of Nietzsche). The extraction
  labels this claim "Interpretive / Theoretical" and flags the mechanism as interpretive — good. But
  Card B01-C11-07's title states it flatly as fact; acceptable given the body's hedge and that it mirrors
  the book's own phrasing. Noted; no change.

- **"If your laptop cannot find it, neither can the market."** A vivid Jain quote used as a thesis line.
  The extraction correctly attributes it and frames the underlying claim as "Theoretical (proved)." The
  leap from worst-case intractability to real markets is exactly what Tension #2 flags. Adequate.

## 4. Important Nuance Lost

- **Why the English auction seems "closer to what we want."** The extraction's Vickrey card is strong,
  but the chapter's point is comparative: the English/ascending auction *already* lets the true high-
  valuer win near the second price without full strategizing — the Vickrey auction achieves this in
  sealed-bid form. Preserving the auction ladder (see Missing Items) restores this nuance.

- **"Revenue equivalence" is an expectation, not a per-auction guarantee.** The extraction's §5 and Card
  11 both note this correctly ("on average, not per case"). Good — retained.

- **The commitment problem's link back to chapter 1 (optimal stopping / secretary problem).** The chapter
  explicitly ties marriage's commitment problem to the optimal-stopping discussion of dating/apartments in
  ch. 1 (continuing to see options after deciding). The extraction's love card mentions the commitment
  problem but not the ch. 1 callback; worth a cross-reference line for the knowledge base.

## 5. Additional Cases Worth Capturing

- **The auction ladder (first-price / Dutch / English)** — see Missing Items; added as a framework entry
  and a teaching example, since it's the mechanical setup for both the cascade and the Vickrey payoff.

- **Parasites (lancet liver fluke; Toxoplasma gondii).** The extraction mentions these inside the emotions
  claim but not as a standalone illustration. They're a memorable "individuals hijacked to serve another's
  ends" analogy for emotion-as-mechanism. Adequately represented in Claim #8 and Card 7; noting only.

## 6. Additional Research / Scholars Mentioned

- **Roger Myerson** (revelation principle; Nash-equilibrium "DNA double helix" quote) — named in the
  extraction. Retained.
- **Christos Papadimitriou, Tim Roughgarden, Scott Aaronson, Kamal Jain, Éva Tardos, Ken Binmore, Avrim
  Blum, Noam Nisan, Paul Milgrom, Robert Frank** — all named and correctly placed. Retained.
- **James Branch Cabell** (the optimist/pessimist "best of all possible worlds" line) — used in the
  price-of-anarchy passage; dropped from the extraction. Minor; a nice quotable, optionally added.

## 7. Potential Disagreements / Counterpoints the Chapter Doesn't Raise

- **Repeated games and reputation.** The one-shot prisoner's dilemma ignores that repeated interaction,
  reputation, and tit-for-tat can sustain cooperation without an external designer. The extraction's
  Tension #1 raises this. Adequate.

- **Who designs the designer?** Mechanism design presumes a benevolent authority; designers can exploit
  players. The extraction's Tension #4 covers this. Adequate.

- **Approximate/learned equilibria.** Worst-case intractability may not prevent markets/agents reaching
  approximate equilibria via adaptation. The extraction's Tension #2 covers this. Adequate.

## 8. Additional Content Opportunities

- Sartre's "Hell is other people," revised into "seek games where honesty is dominant, then just be
  yourself," is a strong closing beat for the mechanism-design or the love video. Folded into the existing
  §17 hooks rather than added as a new block.

## 9. Recommended Changes (applied back into Chapter_11_Extraction.md)

1. **§4 / §8 — Add the auction ladder** (sealed-bid first-price → Dutch/descending → English/ascending)
   as a framework entry and teaching example, since it carries both the information-cascade and the
   Vickrey arguments.

2. **§18 — Soften the self-driving-cars figure in Card B01-C11-04** to the book's own framing (perfectly
   coordinated commutes "only 3/4 as congested as they are now"), not a specific self-driving-car claim.

3. **§12 — Add the Sartre "Hell is other people" quotable** and its revision (interacting need not be a
   nightmare; in the wrong game it can be).

4. **§11 — Anchor the Kant/categorical-imperative footnote** in Tension #1 (the prisoner's dilemma
   "obliterates" Kant because the categorical-imperative outcome, though better, isn't stable).

5. **§18 — Add a ch. 1 cross-reference** in the love card (marriage's commitment problem continues the
   optimal-stopping/secretary-problem discussion of dating and apartment-hunting).

All other first-pass content is confirmed accurate against the text. The separation of author-claim /
evidence / own-inference (esp. §15 sports and §16 AI, both explicitly inferred) holds up on re-read, as
do the flags on intractability's practical limits and mechanism design's assumed designer.
