# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 9: Randomness — When to Leave It to Chance
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 236–264 (re-read against Chapter_09_Extraction.md)
**Date:** 2026-07-22

Adversarial re-read of the chapter text against the first-pass extraction. Findings below are grouped by
type; the "Recommended Changes" at the end are the subset applied back into the extraction.

---

## 1. Missing Items (concepts, examples, studies present in the text but absent or thin in the extraction)

- **Polynomial identity testing — the concrete worked case and the "push random buttons" intuition.** The
  extraction names polynomial identity testing as "the only known efficient route" but omits the actual
  example the authors give — testing whether 2x³ + 13x² + 22x + 8 equals (2x+1)(x+2)(x+4) by plugging in
  random x's, where agreement on several random inputs is an ever-bigger coincidence — and the everyday
  intuition pump: given two nondescript gadgets, most of us "start pushing random buttons rather than
  crack open the cases," and a TV drug lord "knifes open a few bundles at random" to check a shipment.
  These make the abstract point tangible and belong in the cases/examples.

- **The Metropolis Algorithm's physical origin.** The text notes the Metropolis Algorithm "had initially
  been designed to model random behavior in physical systems (in that case, nuclear explosions)" — the
  historical thread linking Monte Carlo, Metropolis, and simulated annealing back to Los Alamos weapons
  work. The extraction mentions the Los Alamos team but not that the algorithm itself modeled explosions.

- **"Temperature is really velocity."** Kirkpatrick's key conceptual move — that in physics "temperature"
  is random molecular motion (velocity), directly analogous to hill-climbing jitter — is the hinge of the
  whole analogy and was compressed to "temperature-as-randomness" without the velocity/molecular-motion
  content.

- **The F. Scott Fitzgerald quote.** In the solitaire passage, the authors quote Fitzgerald ("the test of
  a first-rate intelligence is the ability to hold two opposing ideas in mind…") to set up that no
  intelligence can hold 80 unvigintillion deck orders — a nice quotable that was dropped.

- **The "what the meaning of 'is' is" philosophical aside.** The authors explicitly raise the philosophical
  jolt that a number can be "probably prime" or "almost definitely prime" — the meaning of mathematical
  "is." Present in the counterintuitive-insights section in spirit, but the memorable framing was cut.

- **Aaronson's "failure to communicate."** The extraction cites Aaronson's complexity-as-philosophy point
  but omits his diagnosis of *why* computer scientists haven't influenced philosophy: their "failure to
  communicate what they can add to philosophy's conceptual arsenal." Minor but it's his actual thesis.

- **Twin primes definition (footnote).** A footnote defines twin primes as "consecutive odd numbers that
  are both prime, like 5 and 7." The extraction uses "twin primes" without the definition.

- **The √n footnote reasoning.** The extraction states you divide "by primes up to √n" but omits the
  reason given in the footnote (a factor above √n must be paired with one below it, so you'd already have
  caught it). Worth a one-line note since it's the crux of why the sieve check stops at √n.

## 2. Corrections Needed (statements in the extraction that distort or overstate the text)

- **Luria–Delbrück attribution.** The extraction's study card names the "Luria–Delbrück 'fluctuation'
  insight" and parenthetically flags Delbrück as "implied collaborator… not named in the chapter." The
  chapter names *only* Luria and never mentions Delbrück or the term "fluctuation test." Importing the
  standard textbook name/collaborator is exactly the kind of outside detail the skill says to avoid.
  Corrected below to attribute only what the chapter states.

- **"Los Alamos… during World War II."** The extraction's Monte Carlo study card dates the method "1946
  onward," which is correct, but the sampling narrative says the enabling computer was "developed in Los
  Alamos during World War II." Both are in the text and consistent; no change needed — flagging only to
  confirm the 1946 date (Ulam's return) is the method's origin, not WWII.

## 3. Overgeneralizations (author hedges flattened into confident claims)

- **"Sampling is the best way… including public policy."** The chapter's claim is carefully hedged — a
  "Monte Carlo–informed computer scientist *would propose*" sampling as "*one of* the simplest, and also
  the best, ways." The extraction's Key Claim #9 mostly preserves this ("interpretive… the authors'
  proposal") but the Knowledge Card B01-C09-07 title ("Sampling beats anecdotes and aggregates") reads as
  settled fact. Acceptable as a card title given the body hedges, but worth noting the "best" is the
  authors' advocacy, not a demonstrated result.

- **AKS as simply "slower."** The extraction says the 2002 deterministic test "is slower." The text says
  randomized algorithms "are much faster and thus are still the ones used in practice" — same meaning,
  fine. No change.

## 4. Important Nuance Lost

- **"Better" ≠ "more precise" (Ulam).** The extraction does capture this (Claim #3, Tension #1), which is
  good — this is the single most important nuance in the sampling section and it survived. No fix needed;
  noting it as correctly retained.

- **The sampling-error caveat is doubly stated.** Ulam's "better" and the π-estimation footnote both
  stress error. Retained.

- **GiveDirectly footnote — "the very first story."** The extraction's GiveDirectly case *does* include
  the footnote (they deliberately took the first story, not a chosen one), which is the whole
  methodological point. Retained. Good.

## 5. Additional Cases Worth Capturing

- **The polynomial-identity / gadgets / drug-lord cluster** (see Missing Items) — a compact case
  illustrating "sample the behavior rather than dissect the mechanism." Added as an example under §8 and
  folded into the sampling discussion.

- **Cockcroft's "Brownian slow motion."** The extraction captures Cockcroft settling into a local maximum
  but the vivid phrase "a kind of Brownian slow motion" (nomadic sailboat life) is a nice detail already
  partly present; ensure it stays.

## 6. Additional Research / Scholars Mentioned

- **Ernst Mach and Henri Poincaré** are cited alongside James and Campbell as offering the same
  variation-and-selection account of discovery; the extraction includes them in the research card and
  Card B01-C09-13. Retained.

- **Burton H. Bloom** (Bloom filter inventor) — named in the extraction. Retained.

## 7. Potential Disagreements / Counterpoints the Chapter Doesn't Raise

- **Randomness quality is assumed.** The chapter's guarantees (Miller-Rabin's error bound, Monte Carlo's
  convergence) all presuppose access to genuine randomness. Real systems use pseudo-random generators; a
  compromised or biased RNG breaks the guarantees. The extraction's Tension #2 gestures at this ("a bad
  RNG"); adequate.

- **Sampling can entrench bias.** A "random" sample from a biased frame (GiveDirectly's own recipient
  list, or which policy outcomes you choose to measure) is only as representative as the frame. The
  extraction's Tension #3 covers this. Adequate.

## 8. Additional Content Opportunities

- The polynomial-identity "push random buttons instead of opening the box" idea is a strong standalone
  short: *"When it's smarter to test than to understand."* Noted here; not added as a full §17 block to
  avoid inflating an already-rich section, but flagged for the profile stage.

## 9. Recommended Changes (applied back into Chapter_09_Extraction.md)

1. **§7 / §8 — Add the polynomial-identity / gadgets / drug-lord example.** Add a short example under §8
   (Best Teaching Examples) capturing "sample the behavior, don't dissect the mechanism," with the
   2x³+13x²+22x+8 = (2x+1)(x+2)(x+4) case and the drug-lord/gadgets intuition.

2. **§4 / §18 — Add the Metropolis Algorithm's origin (modeling nuclear explosions) and "temperature is
   really velocity."** Fold both into the Metropolis and Simulated Annealing framework entries and Card
   B01-C09-11 so the physics analogy is complete.

3. **§5 — Correct the Luria study card:** remove the "Luria–Delbrück / fluctuation test" naming and the
   Delbrück attribution; attribute only what the chapter states (Luria, 1943).

4. **§12 — Add the Fitzgerald quote** ("hold two opposing ideas… and still function") as a quotable,
   tied to the solitaire combinatorial-explosion setup.

5. **§4 — Add the √n footnote reasoning** (a factor above √n pairs with one below) as a one-line note in
   the Sieve/one-way-function context (Card B01-C09-04).

All other first-pass content is confirmed accurate against the text. The extraction's separation of
author-claim / evidence / own-inference (esp. §15 sports, §16 AI) holds up on re-read.
