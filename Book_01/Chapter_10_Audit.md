# Algorithms to Live By: The Computer Science of Human Decisions — Chapter 10: Networking — How We Connect
**Author:** Brian Christian and Tom Griffiths
**Type:** Audit
**Source:** sources/Algorithm.to.Live.By.pdf, PDF pages 265–291 (re-read against Chapter_10_Extraction.md)
**Date:** 2026-07-22

Adversarial re-read of the chapter text against the first-pass extraction. Findings grouped by type; the
"Recommended Changes" at the end are the subset applied back into the extraction.

---

## 1. Missing Items (present in the text but absent or thin in the extraction)

- **The "ilunga" epigraph.** The Exponential Backoff section opens with the BBC's claim that the hardest
  word to translate is "ilunga" (Tshiluba, DR Congo): "a person who is ready to forgive any abuse for
  the first time, to tolerate it a second time, but never a third time." This is a near-perfect encoding
  of finite-patience/three-strikes and belongs among the quotables — it was dropped.

- **Carrier pigeons / "Avian Carriers" (2001, Bergen).** The extraction mentions packet switching over
  "copper, satellite, radio" but omits the vivid 2001 Norwegian implementation over pigeons — a memorable
  proof of packet switching's medium-agnosticism. Added to the packet-switching example set.

- **ECN (Explicit Congestion Notification).** The extraction mentions ECN once (in the bufferbloat study
  card) but not clearly as "a new backchannel for TCP, the first such modification in many years." Minor;
  worth a phrase since it ties the buffer fix back to the backchannel/feedback theme.

- **"That's funny" (not "Eureka!").** The Gettys discovery quotes the adage that the phrase heralding new
  discoveries is not "Eureka!" but "That's funny." The extraction's Gettys case keeps "That's funny" but
  not the framed contrast; acceptable, flagging only.

- **The round-trip-time calibration point.** The text makes a specific claim — we start to worry over
  silence "in a matter of seconds over the phone, days over email, and weeks over postal mail," and the
  longer the round-trip time the more can be "in flight" before a problem is noticed. The extraction
  gestures at breakdown-detection but drops the concrete seconds/days/weeks scale. Worth a line.

- **Metacommunication.** The congestion section's precise term — sender and receiver must not only
  communicate but "metacommunicate" (figure out how fast to send) because nothing in the network reports
  congestion explicitly — is a nice concept the extraction folded into AIMD without naming. Minor.

## 2. Corrections Needed (statements that distort the text)

- **HOPE launch date.** The extraction's HOPE study card says "Program launched mid-2000s" — the chapter
  does not give a launch year (it says "the past decade" relative to the 2016 book and describes Alm
  "shortly after being sworn in"). Stating "mid-2000s" as fact overspecifies beyond the text. Corrected
  to "Not specified (described as within the decade before the 2016 book)."

- **Bell's first call date.** The extraction says "March 10, 1876" — this matches the text. Confirmed, no
  change. (Flagging because dates are easy to drift on; all checked: Morse 5/24/1844, Bell 3/10/1876,
  Cooper 4/3/1973, text 12/3/1992, ARPANET 10/29/1969 — all correct.)

## 3. Overgeneralizations (author hedges flattened)

- **"Reliability increases exponentially with size."** The extraction states this cleanly; the text does
  too, but it is a stylized claim about path proliferation, not a proved theorem with stated assumptions.
  The extraction already labels the parent claim "Theoretical" and Baran's design as the origin;
  acceptable, but the symmetry ("decreases exponentially" for circuit / "increases exponentially" for
  packet) is rhetorical shorthand and should not be read as a precise result. Noted; no text change
  required since the claim mirrors the book.

- **AIMD → careers/organizations.** The extraction's Peter-Principle card and §15 sports both extend
  AIMD to human hierarchies. The book itself makes the career-sawtooth proposal explicitly (so it's the
  authors', not over-reach), and §15 is correctly flagged as inferred. Fine.

## 4. Important Nuance Lost

- **Why the decrease is *multiplicative* (the two-reasons argument).** The extraction says halving is
  "conservative" and "essential," which is right, but the chapter gives Jacobson & Karels's *two* precise
  reasons: (1) the initial ramp doubled the rate each success, so halving on first failure exactly undoes
  the last doubling; (2) once underway, a new fault likely means a second connection has appeared taking
  half the resources — the most conservative read again implies halving. The extraction compresses this;
  worth preserving both reasons in the AIMD card for fidelity.

- **Buffers use delay to exploit later slow periods.** The extraction captures "latency for throughput"
  but the specific mechanism — buffers make packets/customers wait "to take advantage of later periods
  when things are slow" — is a good clarifying nuance, retained in Card 11's spirit. Adequate.

- **"Correspondence… the US Mail doesn't need to know about that."** The Cheshire quote's point that
  continuity is an endpoint fiction, not a network fact, is preserved. Good.

## 5. Additional Cases Worth Capturing

- **Carrier pigeons (2001, Bergen)** — see Missing Items; added to the packet-switching example.

- **The doughnut-shop queue.** The extraction leads the buffer explanation with Tom's crêpe (good), but
  the chapter first uses a doughnut shop (don't make a momentarily-overwhelmed cashier send a customer
  away and come back; queue so average throughput approaches maximum). The crêpe case covers the same
  ground more vividly, so this is adequately represented; noting for completeness.

## 6. Additional Research / Scholars Mentioned

- **Norman Abramson / ALOHAnet** — named in the extraction (Exponential Backoff, experiment card).
  Retained.

- **Kathleen Nichols** — co-author of the bufferbloat epigraph with Van Jacobson; named in the extraction's
  bufferbloat study card. Retained.

- **Ray Tomlinson** (email's inventor, "designed to overcome Tail Drop") — named in the Katy Perry case.
  Retained.

## 7. Potential Disagreements / Counterpoints the Chapter Doesn't Raise

- **HOPE's contested replications.** The chapter cites only the favorable five-year DOJ study; subsequent
  multi-site trials of HOPE-style "swift-certain-fair" supervision have produced mixed results, and
  critics raise net-widening and fairness concerns. The extraction's Tension #1 already flags this.
  Adequate.

- **Human agency vs. packet mechanics.** Applying Tail Drop / backoff literally to people risks treating
  relationships as throughput problems; the extraction's Tension #2 and #4 cover this, including the
  book's own "not a magic panacea" caveat. Adequate.

## 8. Additional Content Opportunities

- The "ilunga" word is a strong cold-open for the forgiveness video — one untranslatable word that
  encodes exactly the three-strikes instinct Exponential Backoff improves upon. Folded into the existing
  §17 "algorithm of forgiveness" hook rather than added as a new block.

## 9. Recommended Changes (applied back into Chapter_10_Extraction.md)

1. **§12 — Add the "ilunga" quotable** (forgive once, tolerate twice, never a third time) as the
   encoding of three-strikes that Exponential Backoff supersedes.

2. **§7 / §8 — Add carrier pigeons (2001, Bergen)** to the packet-switching example as proof of
   medium-agnosticism.

3. **§5 — Correct the HOPE launch date** from "mid-2000s" to "Not specified (within the decade before
   the 2016 book)."

4. **§4 / §18 — Preserve both of Jacobson & Karels's reasons for halving** (undoing the last doubling;
   assuming a new connection took half the resources) in the AIMD framework entry and Card B01-C10-08.

5. **§3 / §18 — Add the round-trip-time calibration** (worry in seconds over phone, days over email,
   weeks over mail; more data "in flight" the longer the round-trip) to the acknowledgment material.

All other first-pass content is confirmed accurate against the text. The separation of author-claim /
evidence / own-inference (esp. §15 sports and §16 AI, both explicitly inferred) holds up on re-read, as
does the flagging of HOPE's one-sided evidence.
