# Prediction Machines — Chapter 20: Managing AI Risk
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Audit
**Source:** Book pages 221–232 (PDF pages 234–245)
**Date:** 2026-08-04

## Missing Items

1. **The vivid diabetic/insulin-manipulation example of input data risk (book p.226)**: The chapter gives a specific, high-stakes illustrative example the extraction omitted entirely: "a diabetic using an AI to optimize insulin intake could end up in serious jeopardy if the AI has incorrect data about that person and then offers predictions that suggest lowering insulin intake when it should be increased. If harming a person is someone's objective, then this is one way to do it effectively." This is a vivid, safety-critical example of input data manipulation as a potential attack vector, distinct from the more abstract discussion already captured, and deserves its own case/example entry.
2. **The Nymi startup case and other identity-verification methods (book p.227)**: A distinct real case is missing entirely: "Nymi, a startup we worked with, developed a technology that uses machine learning to identify individuals via their heartbeat. Others are using retina scans, faces, or fingerprint identification. Companies can also confirm an identity by using the characteristics of a smartphone user's walking patterns." This is a first-hand, CDL-adjacent startup case (in the same vein as Kindred in Ch.16) illustrating how identity verification is co-developing with personalized AI to mitigate individual-level manipulation risk — a genuinely useful, concrete case entirely absent from the extraction.
3. **The "garbage in, garbage out" adage (book p.226)**: The chapter explicitly invokes this classic, quotable computer science adage to frame input data risk: "just like the old computer adage—'garbage in, garbage out'—prediction machines fail if they have poor data or a bad model." Worth including as a quotable idea given its concision and immediate recognizability.
4. **The crash-versus-silent-manipulation distinction (book p.226)**: The chapter draws a specific, useful distinction the extraction's input-data-risk concept doesn't capture: "One type of failure is a crash. Crashes might seem bad, but at least you know when they have occurred. When someone manipulates a prediction machine, you may not know about it (at least not until too late)." This reframes visible failures as actually less dangerous than invisible, successful manipulation — a genuinely counterintuitive point about risk visibility.
5. **"Attacks leave a trail" as a defensive mitigation for training data risk (book p.230)**: The extraction's training-data-risk discussion captures the vulnerability (model extraction via repeated querying) but omits the chapter's own constructive counterpoint: "such attacks leave a trail. It is necessary to query the prediction machine many times to understand it. Unusual quantities of queries or an unusual diversity of queries should raise red flags. Once raised, then protecting the prediction machine becomes easier, although not easy." This is a genuinely actionable defensive insight that balances the otherwise purely risk-focused discussion.
6. **Short-term operational benefit versus long-term strategic/legal risk from the same discriminatory pattern (book p.224)**: The chapter makes a sharper point than the extraction's general "algorithmic discrimination" framing conveys: "Showing the STEM ads to men and not women bolstered short-term performance (in that the ads the men saw cost less) but created risks due to the resulting discrimination. The consequences of increasing risks may not become apparent until too late." This identifies a specific tension — the very discriminatory pattern that looks like good short-term performance is simultaneously accumulating legal/reputational risk — which is a distinct, more precise claim than simply noting discrimination occurred.

## Corrections Needed

1. **Misattributed initial discovery in the Sweeney case (book p.221)**: The extraction's Section 3 and Section 7 state that Sweeney "discovered that Googling her own name produced ads suggesting she had been arrested," implying she made the initial discovery herself. The chapter actually states: "Latanya Sweeney... was surprised when **a colleague** Googled her name to find one of her papers and discovered ads suggesting she had been arrested." The colleague made the initial discovery (while searching for one of Sweeney's papers); Sweeney then clicked the ad, paid the fee, confirmed the ad was false, and proceeded to investigate systematically (including testing colleague Adam Tanner's name). This should be corrected in both the extraction's narrative and its case entry.

## Overgeneralizations

None identified.

## Important Nuance Lost

- As detailed in Missing Item #6, the extraction's discrimination discussion doesn't fully capture that the STEM-ad discriminatory pattern was simultaneously a short-term operational win (lower ad cost) and an accumulating strategic/legal risk — flattening this into a single "discrimination occurred" framing loses the chapter's sharper point about how such risks can hide behind good-looking short-term metrics.
- As detailed in Missing Item #4, presenting input data risk only in general terms loses the chapter's specific point that *visible* failures (crashes) are actually the less dangerous case precisely because they're visible — the more dangerous case is successful, undetected manipulation.

## Additional Cases and Examples

```
Case Title: Nymi's heartbeat-based identity verification
People / Organization: Nymi (startup); other companies using retina, face, fingerprint, and smartphone gait-pattern identification
Context: Directly follows the input-data/identity-manipulation risk discussion (extraction Section 2, "security risk taxonomy" concept), illustrating how identity-verification technology is co-developing with AI personalization specifically to mitigate this risk.
What Happened: The chapter states AI technologies will develop "hand-in-hand" with identity verification, citing Nymi (a startup the authors worked with, presumably via the CDL) as developing machine-learning-based heartbeat identification, alongside other companies using retina scans, facial recognition, fingerprints, or smartphone-detected walking-gait patterns.
Outcome: Presented as an emerging, hopeful convergence — "a happy confluence in technologies may emerge that allows us to simultaneously personalize AI and safeguard identity" — rather than a solved problem.
Concept Illustrated: The security risk taxonomy's input-data/identity dimension, and a real-world mitigation approach co-evolving alongside the risk itself.
Why This Case Is Useful: A first-hand, concrete startup example (consistent with the book's established CDL-vantage-point sourcing) that grounds an otherwise abstract risk-mitigation discussion in a specific, real technology.
Potential for Reuse: High
```

## Additional Research Evidence

None identified beyond what's already captured in Section 5 and this audit.

## Potential Disagreements to Track Later

None newly identified beyond what's already flagged in the extraction's Section 11.

## Additional Content Opportunities

None identified beyond what's already captured in Section 17 — the missing items above refine existing captured content rather than introduce net-new teachable material.

## Recommended Changes to the Original Extraction

1. **Section 3 and Section 7, Sweeney case** — correct the discovery narrative: a colleague first discovered the ad while searching for Sweeney's name to find one of her papers; Sweeney then confirmed it was false and investigated systematically.
2. **Section 3 or 7, input data risk** — add the diabetic/insulin-manipulation example as a vivid, safety-critical illustration.
3. **Section 7 (new case)** — add the Nymi startup case and related identity-verification methods.
4. **Section 12 (Quotable Ideas)** — add the "garbage in, garbage out" adage.
5. **Section 2, security risk taxonomy concept** — add the crash-versus-silent-manipulation distinction.
6. **Section 2 or 4, training data risk discussion** — add "attacks leave a trail" as a defensive mitigation insight.
7. **Section 2, algorithmic discrimination concept** — sharpen to note that the discriminatory STEM-ad pattern simultaneously bolstered short-term operational performance while accumulating strategic/legal risk.

All other sections are accurate as extracted; no further changes needed.
