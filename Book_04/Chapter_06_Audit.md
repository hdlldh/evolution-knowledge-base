# Prediction Machines — Chapter 6: Data Is the New Oil
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Audit
**Source:** Book pages 57–65 (PDF pages 70–78)
**Date:** 2026-08-03

## Missing Items

1. **Named examples of who collects data cheaply** (book p.57): The chapter states, "From large companies like Facebook and Microsoft to local governments and startups, data collection is cheaper and easier than ever before." This spread of named examples (Facebook, Microsoft, local governments, startups) illustrating the *breadth* of who now collects data cheaply was omitted from the extraction, which discussed the general trend without these specific anchors.
2. **The "uninitiated consumer cannot see the link" point** (book p.58–59): The chapter makes an explicit rhetorical point: "The uninitiated consumer cannot see the link between heart rate data and an abnormal heart rhythm from raw data. In contrast, Cardiogram can detect an irregular heart rhythm with 97 percent accuracy using its deep neural network." This framing — that the prediction machine's value lies precisely in surfacing a relationship invisible to an ordinary observer of the raw data — is a distinct point from simply reporting the 97% accuracy figure, and strengthens the "why does this require AI at all" argument. It was present only implicitly in the extraction.

## Corrections Needed

1. **The extraction mischaracterizes what serves as the "proxy" in the Cardiogram case.** The extraction's Section 4 (Statistical vs. economic returns... wait, actually Section 7, Cardiogram case) and Section 1 state that "heart rate was the specific, medically-validated proxy for its prediction target." This is incorrect. The chapter's actual chain of reasoning (book p.61) is: Cardiogram's ultimate goal is to predict **strokes**; it uses **irregular heart rhythms** as the medically validated *proxy* for stroke risk; it then uses **heart rate data** as the *input data* needed to detect that proxy (irregular heart rhythm). The extraction's phrasing collapses two distinct steps (target→proxy, and proxy→input signal) into one, incorrectly making heart rate "the proxy" rather than "the input data used to detect the proxy." This should be corrected wherever it appears (Section 2's "Data availability" concept discussion is fine, but the Cardiogram case entry in Section 7 needs the fix).

## Overgeneralizations

None identified beyond the correction above.

## Important Nuance Lost

- The chapter's explicit three-level chain (predict strokes → via proxy of irregular heart rhythm → via input signal of heart rate) is a clean illustration of how prediction targets, proxies, and input data can be distinct layers — a structurally important nuance for readers designing their own prediction systems, which the extraction's collapsed phrasing (see Corrections Needed) partially obscures.

## Additional Cases and Examples

```
Case Title: Data collection's spread across large companies, governments, and startups
People / Organization: Facebook, Microsoft (named); local governments; startups (referenced generally)
Context: Opening context for the chapter's claim that data collection has become cheap and easy.
What Happened: The chapter names Facebook and Microsoft as examples of large companies with extraordinary data collection capacity, alongside local governments and startups, to illustrate that cheap data collection is not limited to a handful of tech giants but spans organization types and sizes.
Outcome: Broadens the "data is abundant now" claim beyond a single-company anecdote (Google/Varian) to a general economy-wide trend.
Concept Illustrated: The breadth/ubiquity of cheap data collection across sectors.
Why This Case Is Useful: A quick, named-example list that adds credibility and breadth to the chapter's opening claim, useful for content that needs to establish "data collection is now cheap everywhere," not just at one famous example.
Potential for Reuse: Medium — useful as supporting color, thin as a standalone case.
```

## Additional Research Evidence

None identified beyond what's already captured in Section 5 and this audit.

## Potential Disagreements to Track Later

None newly identified in this chapter beyond what's already flagged in the extraction's Section 11 (tension between the "data is the new oil" title/framing and the chapter's actual targeted-data-strategy argument).

## Additional Content Opportunities

None beyond what's already captured in the extraction's Section 17 — the missing items above are supporting/grounding details rather than standalone content seeds.

## Recommended Changes to the Original Extraction

1. **Section 7, Cardiogram case entry** — correct the proxy chain: Cardiogram's target is predicting strokes; irregular heart rhythm is the medically-validated proxy for stroke risk; heart rate data is the input data used to detect that proxy. Remove the incorrect phrasing that called heart rate itself "the proxy."
2. **Section 1 (Chapter Thesis) or Section 3** — if the incorrect proxy phrasing appears there too, apply the same correction.
3. **Section 3 (Key Claims) or Section 7** — add the named examples (Facebook, Microsoft, local governments, startups) illustrating the breadth of cheap data collection.
4. **Section 7, Cardiogram case entry** — add the "uninitiated consumer cannot see the link" point to strengthen why the prediction machine's 97% accuracy is meaningful (it surfaces a relationship invisible in raw data).

All other sections are accurate as extracted; no further changes needed.
