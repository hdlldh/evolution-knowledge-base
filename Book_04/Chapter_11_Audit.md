# Prediction Machines — Chapter 11: Taming Complexity
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Audit
**Source:** Book pages 115–122 (PDF pages 128–135)
**Date:** 2026-08-04

## Missing Items

1. **The squirrel/cat interaction-effect example for "more ifs"** (book p.116–117): The chapter's most vivid, memorable illustration of how "ifs" multiply through interaction effects was entirely omitted from the extraction. The book walks through a hypothetical delivery robot whose motion depends on multiple interacting factors: "If a robot operates outside, it needs to move more slowly to avoid slipping when the ground is wet. Two possible situations (or states) arise—dry and wet. If the robot's motion is also influenced by whether it is light or dark, whether a human is moving in the vicinity or not, whether rush items are in that batch of mail, if it is okay to run over squirrels but not cats, and a variety of other factors, and if the rules are sensitive to interactions (it is okay to run over squirrels if it is dark, but not if it is light), then the number of situations—the number of 'ifs'—grows radically." The chapter then gives the direct payoff: "A prediction machine enables the robot to identify that wet dark environments with a human running twenty feet behind and a cat up ahead might require slowing down, but wet dark environments with a human standing twenty feet behind and a squirrel ahead might not." This is the chapter's clearest worked example of combinatorial "ifs" growth via interaction effects, directly paralleling the combinatorial-explosion concept from Chapter 6 (seven binary conditions → 128 combinations), and its absence is a meaningful gap — it's also the single most quotable/memorable passage in the "More Ifs" section (a robot that's programmed to distinguish squirrels from cats, and to care about lighting conditions when deciding whether to run over either).
2. **The list of other tasks being reframed as prediction problems** (book p.120): Immediately after the translation/Jelinek discussion, the chapter notes: "All sorts of other tasks—including image recognition, shopping, and conversation—are being identified as complex prediction problems that are amenable to the application of machine learning." This brief but useful list of parallel examples (beyond translation) showing the same "ifs are reframed as predictable" pattern spreading across domains was omitted from the extraction.

## Corrections Needed

None identified — spot-checked figures and attributions (Mailmobile pricing/speed, Stigler quote, Simon's Nobel/Turing Award, Jelinek quote) all match the chapter text.

## Overgeneralizations

None identified.

## Important Nuance Lost

None beyond what's captured in Missing Items above.

## Additional Cases and Examples

```
Case Title: The squirrel-vs-cat delivery robot thought experiment
People / Organization: Not specified (hypothetical illustrative robot)
Context: The chapter's central worked example for how "ifs" multiply combinatorially once interaction effects between situational factors are considered.
What Happened: A hypothetical outdoor delivery robot's correct behavior depends on multiple interacting factors: whether the ground is wet or dry, whether it's light or dark, whether a human is nearby, whether the cargo includes rush items, and whether it's acceptable to run over a squirrel but not a cat — with rules that are themselves interaction-sensitive (running over a squirrel is acceptable in the dark but not in daylight). Once interactions are considered, the number of distinct situations ("ifs") the robot must handle grows radically. A prediction machine resolves this by learning, for example, that wet/dark conditions with a human running twenty feet behind and a cat ahead call for slowing down, while the same wet/dark conditions with a human merely standing twenty feet behind and a squirrel ahead might not.
Outcome: Demonstrates concretely why hand-coding every "if" becomes infeasible as interacting factors multiply, and why a prediction machine (which learns from examples rather than requiring explicit rule enumeration) is the practical solution.
Concept Illustrated: Combinatorial growth in "ifs" from interacting situational variables — directly paralleling Chapter 6's seven-binary-conditions/128-combinations example, now applied to real-time robot behavior.
Why This Case Is Useful: Vivid, specific, and slightly humorous (a robot with a cat-vs-squirrel policy), making an abstract combinatorics point memorable and concrete — one of the strongest single teaching examples in the chapter.
Potential for Reuse: High
```

## Additional Research Evidence

None identified beyond what's already captured in Section 5 and this audit.

## Potential Disagreements to Track Later

None newly identified beyond what's already flagged in the extraction's Section 11 (the "eliminates" vs. "reduces" airport-lounge wording tension).

## Additional Content Opportunities

```
Idea Title: "The Delivery Robot That Has to Decide: Squirrel or Cat?"
Format: YouTube Short | Visual Explainer
Application Domain: AI | Everyday Life
Hidden Principle: Optimization / Signal vs. Noise
Story Hook (Layer 1): A delivery robot's rulebook: okay to run over a squirrel in the dark, not okay in daylight, never okay for a cat — and that's just three of dozens of interacting factors.
Principle Framework (Layer 2): Every added real-world factor doesn't just add one more rule — it multiplies against every existing rule, which is why hand-coded automation collapses under real-world complexity and prediction-based systems don't.
Best Supporting Case: The squirrel/cat delivery robot example (see Additional Cases above).
Character Application: Insight: Interpreter
Psychology Angle: None identified.
Math Angle: Direct — combinatorial explosion, echoing Chapter 6's 128-combinations example.
Sports Angle: None identified.
Business Angle: Any rules-engine-based system (fraud rules, pricing rules, compliance rules) faces the same combinatorial blowup as more conditions are added.
Investing Angle: None identified.
History Angle: None identified.
AI Angle: Direct — the core reason prediction/learning beats rule enumeration at scale.
```

## Recommended Changes to the Original Extraction

1. **Section 2 (Key Concepts, "More ifs") or Section 7** — add the squirrel/cat delivery robot thought experiment as the chapter's primary worked illustration of combinatorial "ifs" growth from interacting factors.
2. **Section 3 (Key Claims) or Section 7, translation case** — add the brief list of other tasks (image recognition, shopping, conversation) the chapter cites as being reframed as prediction problems, alongside translation.
3. **Section 18 (Knowledge Cards)** — add a card for the squirrel/cat example (CARD ID B04-C11-07).
4. **Section 17 (Content Creation Opportunities)** — add "The Delivery Robot That Has to Decide: Squirrel or Cat?" (see Additional Content Opportunities above).

All other sections are accurate as extracted; no further changes needed.
