# Prediction Machines — Chapter 9: The Value of Judgment
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Audit
**Source:** Book pages 95–106 (PDF pages 108–119)
**Date:** 2026-08-04

## Missing Items

1. **"Rewards as givens" — the historical economic treatment of preferences** (book p.99): Before discussing the cognitive costs of judgment, the chapter notes: "People who have studied decisions in the past have generally taken rewards as givens—they simply exist. You may like chocolate ice cream, while your friend may like mango gelato. How you two came to your different views is of little consequence. Similarly, we assume most businesses are maximizing profit or shareholder value. Economists looking at why firms choose certain prices for their products have found it useful to take those objectives on faith." This is a distinct, important framing point — it explains *why* judgment/payoffs were traditionally treated as exogenous and unexamined in economics, setting up the chapter's contrasting claim that the rise of prediction machines now makes it worthwhile to actually investigate and understand payoffs rather than take them on faith. The extraction's Section 3 (cognitive costs of judgment) jumps directly to the escalating-specificity credit-card example without capturing this important methodological/historical framing.
2. **Why high-net-worth customers' payoffs specifically differ** (book p.98): The chapter gives a concrete reason for judgment heterogeneity across customer segments: "a high-net-worth platinum cardholder may have other credit card options and might stop using that particular card if declined. And that person may be on an expensive vacation, so the card network could lose all of the expenditures associated with that trip." This concrete mechanism (multi-homing risk + total-trip-spend-at-stake) explaining *why* a platinum cardholder's dissatisfaction payoff is judged differently from an average customer's was omitted from the extraction's fraud decision tree discussion, which mentions customer-type segmentation abstractly but not this specific reasoning.
3. **"Credit card fraud is a well-defined decision process... yet it's still complicated"** (book p.98): The chapter makes an explicit meta-point about its own choice of running example: "Credit card fraud is a well-defined decision process, which is one reason we keep coming back to it, yet it's still complicated." This mirrors a technique used elsewhere in the book (e.g., Ch.7's point that bail-decision criteria are "clear and well defined" yet judges still fail) — deliberately choosing a clean, well-specified example to show that even the *best case* for tractable judgment quickly becomes complicated, which strengthens (rather than undermines) the chapter's broader point about judgment's cognitive costs. This authorial self-awareness about example selection was not captured in the extraction.

## Corrections Needed

None identified — spot-checked figures and attributions ($100/$20/$180 fraud math, >50% ZipRecruiter profit finding, McAfee/Brynjolfsson quote, Dubé/Misra as Booth School economists) all match the chapter text.

## Overgeneralizations

None identified.

## Important Nuance Lost

- As detailed in Missing Item #1, the extraction's discussion of judgment's cognitive costs loses the chapter's important contrast between the historical economic practice of treating preferences/rewards as exogenous "givens" (not worth investigating) and the new economic incentive, created by cheap prediction, to actually invest in understanding payoffs — this contrast is part of *why* the chapter frames reward function engineering as a newly valuable discipline rather than a pre-existing one.

## Additional Cases and Examples

```
Case Title: Why platinum cardholders' dissatisfaction payoff differs
People / Organization: Not specified (generic high-net-worth cardholder example)
Context: Elaborates on the credit-card fraud decision tree's judgment component, explaining why customer segmentation matters for judging payoffs.
What Happened: The chapter explains that a high-net-worth platinum cardholder is judged to have a higher dissatisfaction payoff (from a false decline) than an average customer for two concrete reasons: (1) they likely have other credit card options and might simply stop using the declined card ("multi-homing" risk), and (2) they may be on an expensive vacation at the time, meaning a false decline risks losing the network all future expenditures associated with that entire trip, not just the single declined transaction.
Outcome: Justifies why credit card networks apply different (higher) dissatisfaction-cost judgments to high-net-worth customers specifically, rather than a uniform payoff across all customers.
Concept Illustrated: Concrete mechanisms driving judgment heterogeneity across customer segments — not an arbitrary distinction, but grounded in specific behavioral/financial reasoning.
Why This Case Is Useful: Makes the abstract "different customers need different judged payoffs" point mechanistically concrete rather than merely asserted, useful for any content about customer-segmented risk/pricing decisions.
Potential for Reuse: Medium — a good supporting detail for the fraud decision tree case, though not a standalone teaching example.
```

## Additional Research Evidence

None identified beyond what's already captured in Section 5 and this audit.

## Potential Disagreements to Track Later

None newly identified beyond what's already flagged in the extraction's Section 11 (judgment-value-increases vs. judgment-gets-hard-coded-away tension).

## Additional Content Opportunities

```
Idea Title: "Economists Used to Just Assume You Know What You Want — Not Anymore"
Format: YouTube Short | Community Post
Application Domain: AI | Business | Everyday Life
Hidden Principle: Optimization
Story Hook (Layer 1): For decades, economists didn't bother asking why you prefer chocolate over mango gelato — they just took it as a given. AI just made that lazy assumption expensive.
Principle Framework (Layer 2): Cheap prediction shifts the bottleneck to judgment, and once judgment becomes the bottleneck, understanding *why* people value what they value stops being a philosophical afterthought and becomes an economically valuable investment.
Best Supporting Case: The "rewards as givens" framing (see Missing Items above).
Character Application: Sigma: Architect
Psychology Angle: Preference formation, historically treated as exogenous in economics.
Math Angle: None identified.
Sports Angle: None identified.
Business Angle: Direct — explains why reward function engineering is a newly valuable discipline, not a pre-existing one.
Investing Angle: None identified.
History Angle: A shift in economic methodology prompted by a technological change.
AI Angle: Direct — cheap prediction creating new economic incentive to formalize judgment.
```

## Recommended Changes to the Original Extraction

1. **Section 3 (Key Claims) or Section 12 (Quotable Ideas)** — add the "rewards as givens" historical framing (ice cream/mango gelato example; economists taking profit-maximization "on faith"), explaining why judgment/payoffs were traditionally unexamined and why prediction machines change that calculus.
2. **Section 7, fraud decision tree case** — add the specific mechanism for why platinum cardholders' payoffs are judged differently (multi-homing risk to other cards; risk of losing an entire vacation's worth of expenditures).
3. **Section 7, fraud decision tree case** — add the chapter's explicit meta-point that credit card fraud is chosen as a running example precisely because it's a "well-defined decision process... yet it's still complicated," reinforcing rather than undermining the chapter's broader argument about judgment's difficulty.

All other sections are accurate as extracted; no further changes needed.
