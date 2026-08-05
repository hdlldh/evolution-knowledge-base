# Prediction Machines — Chapter 9: The Value of Judgment
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Extraction
**Source:** Book pages 95–106 (PDF pages 108–119)
**Date:** 2026-08-04
**Revised:** Per Chapter_09_Audit.md — added the "rewards as givens" historical framing, added the platinum-cardholder payoff mechanism, added the chapter's meta-point about choosing a "well-defined... yet complicated" running example.

BOOK:
Prediction Machines: The Simple Economics of Artificial Intelligence

AUTHOR:
Ajay Agrawal, Joshua Gans, Avi Goldfarb

CHAPTER:
9 — The Value of Judgment

---

## 1. Chapter Thesis

Prediction machines don't provide judgment — only humans can express the relative rewards of taking different actions — so as AI takes over the prediction half of decision-making, humans increasingly specialize in the judgment half, and better prediction actually raises the returns to (and therefore the value of) judgment. But judgment is not free: figuring out the true payoffs of different action-outcome combinations has real cognitive costs, requiring either time-consuming deliberation/research or costly trial-and-error experimentation. When the number of possible action-situation combinations is small and stable enough, humans can pre-specify ("hard-code") their judgment into the system in advance — an activity the authors call "reward function engineering" — enabling full automation of the decision; when combinations are too numerous or uncertain to specify in advance, it's more efficient for a human to apply judgment case-by-case after the machine's prediction arrives. Uncertainty is what makes judgment costly in the first place: you need judgment specifically to know what to do when a prediction turns out to be wrong, not just when it's right.

## 2. Key Concepts

```
Concept Name: Prediction machines don't provide judgment
Definition: The chapter's foundational claim that judgment — the ability to express relative rewards/values for different possible actions and outcomes — is exclusively a human capability that AI prediction technology does not supply; better prediction is worthless without judgment to interpret what to do with it (echoing the umbrella example from Ch.8: knowing the likelihood of rain doesn't help if you don't know how much you like staying dry or hate carrying an umbrella).
Why It Matters: Establishes why AI's rise doesn't eliminate the human role in decision-making but reallocates it — humans do less of the "combined prediction-judgment routine" and instead specialize in judgment alone, interacting with machine prediction the way a person runs alternative queries against a spreadsheet or database.
How the Author Uses It: Stated directly as the chapter's opening premise, then developed through the credit-card fraud, Waze, and ZipRecruiter cases.
Related Concepts: Reward function, anatomy of a decision (Ch.8), reward function engineering
```

```
Concept Name: Judging fraud (the four-outcome credit-card decision tree)
Definition: An extension of the umbrella decision-tree tool (Ch.8) to a real commercial decision: a credit card network predicts whether a transaction is fraudulent, then must decide whether to accept or decline it, producing four possible outcome combinations (decline+fraudulent = saved recovery cost; decline+legitimate = unsatisfied customer; accept+fraudulent = incurred recovery cost; accept+legitimate = satisfied customer), each requiring a judged payoff.
Why It Matters: Demonstrates that even a decision that looks like "pure prediction" (is this transaction fraudulent?) actually contains a significant, separate judgment component (how costly is each of the four possible outcomes, and how should the network trade off fraud-recovery cost against customer dissatisfaction?) — creditworthiness itself is described as "a sliding scale," and the risk tolerance chosen leads to categorically different business models (e.g., American Express's high-end platinum card vs. an entry-level student card).
How the Author Uses It: Built into a fully worked numerical example: given a transaction predicted 90% likely fraudulent (i.e., prediction has a 10% error rate), a $100 transaction with a $20 recovery cost, the network should decline unless customer dissatisfaction is valued at $180 or more (since 90% × $20 = $18, the break-even dissatisfaction cost) — explicitly parallel to the earlier umbrella math, but with "fraud charges and customer satisfaction" replacing "wet/dry and burdened/unburdened."
Related Concepts: Reward function, Joshua's running-shoes anecdote, cognitive costs of judgment
```

```
Concept Name: The cognitive costs of judgment
Definition: The chapter's central economic caveat: judgment is not a free, instantaneous act — figuring out the true relative payoffs (rewards) of different action-outcome pairs requires costly cognitive work, via either (a) deliberation and thought (time spent reflecting, researching, or consulting others) or (b) experimentation (trying different actions in similar circumstances and observing/learning the actual resulting reward, at the cost of some trials turning out badly).
Why It Matters: Explains why judgment doesn't scale for free even as prediction becomes cheap — as the number of possible outcomes to judge grows (with more actions and more possible situations), the required judgment effort can become "overwhelming," creating a real trade-off between more careful (slower) decision-making and faster (less-informed) decision-making.
How the Author Uses It: Grounded in a historical framing point: economists studying decisions have traditionally treated rewards as exogenous "givens" not worth investigating — "You may like chocolate ice cream, while your friend may like mango gelato. How you two came to your different views is of little consequence" — and similarly took businesses' profit/shareholder-value-maximizing objectives "on faith." The rise of prediction machines changes this calculus by increasing the returns to actually understanding payoffs. Illustrated by escalating specificity in the credit-card context (does a high-net-worth platinum cardholder's payoff differ from an average customer's? does it change while they're on vacation? does work travel differ from vacation travel? does a trip to Rome differ from a trip to the Grand Canyon?) — each added distinction multiplies the number of payoffs needing to be judged; and by the "tasting new foods" analogy for experimentation-based judgment, explicitly noting that experimentation "necessarily means making what you will later regard as mistakes," so it too is costly (you'll try foods you don't like).
Related Concepts: Reward function engineering, ZipRecruiter pricing experiment
```

```
Concept Name: Multi-dimensional objectives and idiosyncratic human weighting (the Waze case)
Definition: The observation that real human objectives are rarely single-dimensional (e.g., "just minimize travel time") — humans have their own explicit and implicit knowledge of *why* they're doing something, which gives them idiosyncratic, subjective weightings across multiple goals that a machine prediction, optimized on a narrower objective, cannot fully capture or anticipate.
Why It Matters: Explains a very common, everyday pattern of human-machine interaction: the machine predicts confidently along its programmed dimension (e.g., fastest route), but the human retains final judgment because their true objective includes dimensions (needing gas, wanting a scenic road, wanting to pass a good place to eat) the machine wasn't told to weigh.
How the Author Uses It: Illustrated via Waze (acquired by Google; originally built by Israeli startup Waze using crowdsourced driver route data to generate real-time traffic maps and optimize routing): when a Waze user overrides a suggested route because they need gas (something the app doesn't know), they aren't disagreeing with the app's prediction — they're applying judgment based on an additional objective dimension the app's optimization didn't include. The chapter notes some such gaps are solvable (e.g., a future version could ask about fuel needs, or Tesla's built-in navigation already accounts for charging-station needs since EVs must recharge), but others are harder to codify (preferring scenic/winding roads, wanting to pass certain "good areas" to stop and eat) — a machine has "fundamental limitations about how much it can learn to predict your preferences."
Related Concepts: Reward function, hard-coding judgment
```

```
Concept Name: Hard-coding judgment (the Ada Support case)
Definition: The practice of pre-specifying judgment in advance — in the form of software code — for situations where the correct action given a particular prediction is already well understood, so that a machine can act immediately upon generating its prediction without needing to consult a human case-by-case.
Why It Matters: Describes the mechanism by which decisions can become progressively more automated as machine prediction improves: routine, well-understood cases get their judgment "enshrined and programmed" in advance, freeing humans to focus their judgment-application effort only on genuinely difficult or novel cases.
How the Author Uses It: Illustrated with Ada Support (an AI-powered technical-support startup) that lets AI answer the easy, frequently-repeated customer questions (where the correct answer is well established) while routing difficult/unusual questions to human agents; Ada matches individual customer characteristics (technical competence history, phone type, past call history) to improve its assessment of which bucket a question falls into, reducing customer frustration and the need to pay for costlier human call-center operators, while humans specialize in the unusual/difficult cases.
Related Concepts: Reward function engineering, McAfee/Brynjolfsson's tacit-knowledge limitation
```

```
Concept Name: The limits of codifiable judgment (tacit knowledge)
Definition: Not all judgment can be pre-specified as code, because much human judgment is based on tacit knowledge — understanding that people apply effortlessly and intuitively but cannot fully articulate as explicit rules or procedures, even to themselves.
Why It Matters: Sets a boundary condition on how far hard-coding/automation of judgment can go — some decisions will remain reliant on real-time human judgment not because of technology limitations in prediction, but because the relevant human knowledge itself resists articulation.
How the Author Uses It: Directly quotes economists Andrew McAfee and Erik Brynjolfsson: "[S]ubstitution (of computers for people) is bounded because there are many tasks that people understand tacitly and accomplish effortlessly but for which neither computer programmers nor anyone else can enunciate the explicit 'rules' or procedures." The chapter immediately qualifies this is "not true of all tasks" — for many decisions, the requisite judgment *can* be articulated and expressed as code (since people routinely explain their thinking to others), effectively filling in the "then" part of an "if-then" statement.
Related Concepts: Hard-coding judgment, reward function engineering
```

```
Concept Name: Reward function engineering
Definition: The named job/discipline of figuring out how to best use machine predictions by determining (in advance, where feasible) the rewards associated with various actions given the predictions an AI produces — requiring understanding of both the organization's true needs/objectives and the machine's technical capabilities.
Why It Matters: Names and formalizes what was previously an implicit, undifferentiated part of human decision-making (since humans always combined prediction and judgment together) as its own distinct professional/organizational function, expected to grow in importance as machine prediction improves and proliferates.
How the Author Uses It: Distinguished into two cases: (1) hard-coded reward function engineering, where rewards are programmed in advance of predictions to fully automate the resulting action (illustrated by self-driving vehicles, where the reward function must be set before deployment since the action must be instant once a prediction is made, and where getting the reward function wrong risks the AI "over-optimizing" on one success metric in ways inconsistent with the organization's broader goals — noted as an active area of dedicated committee work for self-driving cars); and (2) cases where the sheer number of possible predictions makes it too costly to judge all possible payoffs in advance, so a human instead waits for each prediction and assesses the payoff case-by-case (which the chapter notes is close to how most current decision-making already works, with or without machine-generated predictions) — with a forward pointer noting that machines are increasingly encroaching on this second category too, by learning to predict human judgment itself (previewing Chapter 10).
Related Concepts: Hard-coding judgment, human reward-function engineers (parents/mentors/managers), ZipRecruiter case
```

```
Concept Name: Humans as existing (informal) reward function engineers
Definition: The observation that humans already routinely perform reward function engineering for other humans, not just for machines — parents teaching children values, mentors teaching new workers how a system operates, managers setting and then adjusting objectives for staff to improve performance — but because this activity is normally bundled together with prediction and judgment in ordinary human-to-human interaction, it isn't usually recognized as a distinct role.
Why It Matters: Normalizes and grounds the more novel-sounding "reward function engineering for AI" concept by showing it's structurally the same activity humans already do for each other constantly; also predicts that as machines improve at prediction, this previously implicit human activity will need to become an explicit, increasingly important discipline.
How the Author Uses It: Used as a transition/bridge ("Putting It All Together") from the abstract discussion of reward function engineering to the chapter's culminating real-business case (ZipRecruiter).
Related Concepts: Reward function engineering, ZipRecruiter pricing case
```

## 3. Key Claims

```
Claim: Better prediction raises the value of judgment, because improved prediction creates more opportunities to consider the rewards of various actions — meaning better, faster, and cheaper prediction gives us more decisions to make (echoing and reinforcing Ch.8's complements-gain-value claim).
Type: Theoretical
Evidence Provided: Direct assertion as the chapter's opening premise, illustrated via the umbrella callback and developed through the chapter's subsequent cases.
Strength of Support: Moderate — a clear logical extension of the economic framework built in earlier chapters, presented as a foundational premise rather than independently tested with new evidence in this chapter.
```

```
Claim: A decision task that appears to be "pure prediction" (e.g., is a credit card transaction fraudulent?) typically contains a significant, separate judgment component (how should the network weigh the cost of fraud recovery against the cost of a false decline and an unsatisfied customer?), and different judgment choices lead to categorically different business models.
Type: Interpretive/Empirical
Evidence Provided: The credit card fraud decision tree (Figure 9-1) with a fully worked numerical example ($100 transaction, $20 recovery cost, 90% predicted fraud probability, $180 break-even customer-dissatisfaction cost); the observation that different risk tolerances produce different real products (American Express's platinum card vs. a student entry-level card).
Strength of Support: Strong — a clean, internally consistent numerical example with a concrete, checkable business-model consequence (the AmEx platinum/student-card contrast). The chapter explains the mechanism behind this segmentation concretely: a high-net-worth platinum cardholder is judged to carry a higher dissatisfaction payoff because they likely have other card options and might simply stop using the declined card, and because they may be on an expensive vacation, risking the network losing all expenditures associated with that entire trip, not just the single transaction. The chapter also makes an explicit meta-point about choosing this example: "Credit card fraud is a well-defined decision process, which is one reason we keep coming back to it, yet it's still complicated."
```

```
Claim: Prediction machines can become significantly more precise by combining generic factors (transaction type) with personalized/individual-level factors (a specific cardholder's own transaction history and patterns), enabling more confident, more targeted fraud-flagging decisions than either type of factor could achieve alone.
Type: Empirical/Interpretive
Evidence Provided: Joshua Goldfarb's personal anecdote (his card routinely declined for running-shoe purchases at outlet malls, roughly once a year, on vacation) and the explanation that a prediction machine given years of his transaction data could learn this is a *usual* event for him specifically, rather than classifying it as unusual based on generic factors alone (transaction type, mall purchases, easy-to-resell goods being common fraud patterns).
Strength of Support: Moderate — grounded in a specific, verifiable-feeling personal anecdote from a named author, plus a plausible general mechanism (combining generic and personalized signals), though not an independently cited empirical study.
```

```
Claim: As machine-learning-based fraud prediction becomes more precise, credit card companies become more confident in fully codifying ("hard-coding") the accept/decline decision itself, removing the need for ongoing case-by-case human judgment about how costly it might be to offend a particular customer.
Type: Interpretive
Evidence Provided: General assertion connecting improved prediction precision to reduced practical need for judgment in that specific domain, framed as something "already happening" (referencing the earlier claim that Joshua's most recent outlet-mall running-shoe purchase went smoothly).
Strength of Support: Moderate — a plausible mechanism consistent with the chapter's broader argument, illustrated narratively rather than with a controlled before/after study.
```

```
Claim: ZipRecruiter's data-driven pricing experiment found that increasing prices for some categories of new customers would increase day-to-day profit by over 50%, but the company deliberately delayed fully implementing the change for four months to assess longer-term risk (specifically, whether higher-paying customers would leave), only proceeding once it judged that waiting longer would forgo profits without adding meaningfully more information.
Type: Empirical
Evidence Provided: A pricing study conducted by economists J. P. Dubé and Sanjog Misra (University of Chicago Booth School of Business), using randomized assignment of different prices to different customer leads to estimate purchase likelihood by price point (a randomized experiment, cited to endnote 2); the specific finding of a >50% short-run profit increase for some new-customer segments; the company's four-month monitoring period before broader rollout.
Strength of Support: Strong — named, credentialed academic researchers, an explicit randomized experimental design, and a specific quantified headline finding (over 50% profit increase), plus a concrete account of the judgment process (weighing short-run profit against longer-term customer-retention risk) used to decide implementation timing.
```

```
Claim: Determining what "best" means for a pricing decision (or any complex business decision) is itself a nontrivial judgment problem, because naively maximizing one metric (e.g., short-run revenue via high prices) can produce worse outcomes on other dimensions that matter to the business (fewer customers, less word-of-mouth, fewer job postings, reduced platform usage, and long-run customer attrition to competitors).
Type: Theoretical/Interpretive
Evidence Provided: The ZipRecruiter case's explicit enumeration of these competing considerations as the reason the "right" price wasn't obvious even after the short-run profit-maximizing price was identified experimentally.
Strength of Support: Moderate — a well-reasoned application of the chapter's judgment/reward-function framework to a real case, though the specific magnitude of each competing effect (word-of-mouth loss, long-run attrition) is not separately quantified in the visible chapter text.
```

## 4. Frameworks, Models, and Mental Models

```
Name: The four-outcome fraud decision tree (Figure 9-1)
Description: A direct extension of Chapter 8's umbrella decision tree to a business fraud-detection context, separating the prediction (probability a transaction is fraudulent) from the judgment (relative payoffs of the four possible action×true-state combinations).
Components: Two actions (decline / accept); two possible true states (fraudulent / legitimate), weighted by predicted probability; four resulting outcomes, each with a distinct payoff (decline+fraudulent = saved recovery cost; decline+legitimate = unsatisfied customer cost; accept+fraudulent = incurred recovery cost; accept+legitimate = satisfied customer benefit).
How It Works: Given a predicted fraud probability (e.g., 90%) and specific dollar-value payoffs (e.g., $20 recovery cost, some dissatisfaction cost threshold), the network computes the break-even judgment threshold (decline unless dissatisfaction cost exceeds a computed value — $180 in the worked example) to determine the profit-maximizing action.
When It Is Useful: As a template for any binary accept/decline-style decision under a probabilistic prediction, generalizing directly from the umbrella example to any "insurance-like" business risk decision.
Limitations: The chapter explicitly notes this scales poorly — even this "well-defined" fraud example gets complicated when segmenting by customer type (e.g., high-net-worth vs. general), and more general decisions with more actions (e.g., ten) and more situations (e.g., twenty) quickly produce an "overwhelming" number of payoffs to judge (two hundred, in that example).
```

```
Name: Reward function engineering (formalized as two sub-cases)
Description: A framework distinguishing two structurally different approaches to supplying judgment once machine prediction is available, based on whether the number of possible action-situation combinations is manageable enough to pre-specify.
Components: Case 1 — Hard-coded/pre-specified reward function: judgment is programmed in advance of any specific prediction, enabling instant, fully automated action once a prediction is generated (appropriate when actions must be instant, as in self-driving cars, and when the combination space is tractable). Case 2 — Post hoc human judgment: the reward function is too costly to fully specify in advance (too many possible predictions/situations), so a human waits for each specific prediction and judges the payoff case-by-case.
How It Works: The choice between the two cases is driven by a cost-benefit trade-off: pre-specifying judgment has an upfront cost (time/effort to enumerate and value all plausible situations) but enables speed and scale afterward; case-by-case human judgment avoids that upfront cost but is slower and doesn't scale as well per-decision.
When It Is Useful: As a decision-design framework for any organization deploying AI predictions — helping identify which decisions are good candidates for full automation (self-driving-car-style hard-coded rewards) versus which should remain human-in-the-loop (ZipRecruiter-style case-by-case judgment, at least until patterns stabilize enough to hard-code).
Limitations: The chapter flags a real risk within Case 1 — hard-coded reward functions can cause an AI to "over-optimize" on one specific success metric in ways that conflict with an organization's broader, harder-to-formalize goals, a problem serious enough that (per the chapter) "entire committees are working on this for self-driving cars."
```

## 5. Research and Evidence

```
Study / Research: ZipRecruiter pricing experiment
Researchers: J. P. Dubé, Sanjog Misra (economists, University of Chicago Booth School of Business)
Year: Not specified precisely (cited via endnote 2)
Research Question: What prices should ZipRecruiter charge different customer segments to best serve the company's true objective (not simply short-run revenue maximization)?
Method: A randomized experiment in which different prices were randomly assigned to different customer leads, allowing the researchers to estimate the likelihood of purchase at each price point for different customer types.
Key Finding: Increasing prices for some categories of new customers would increase day-to-day profit by over 50%. ZipRecruiter did not act on this immediately; it monitored for four months to check whether higher-paying customers would leave (a longer-term risk), and after confirming the price increase remained highly profitable, judged four months sufficient to proceed with implementation rather than continuing to forgo the higher profits.
How the Author Uses It: The chapter's culminating real-world case, used to show reward-function-engineering judgment in action at a real company — not just determining the short-run profit-maximizing price (the "easy," experimentally-answerable part) but judging how to weigh that finding against harder-to-quantify longer-term risks (customer attrition, reduced word-of-mouth, fewer postings, reduced platform usage by job seekers).
Important Limitations: Exact experiment sample size, specific customer segments, and precise timeframe are not detailed in the visible chapter text.
Replication or Controversy Mentioned: Not specified.
```

## 6. Experiments

```
Experiment Name: ZipRecruiter randomized pricing experiment (see also Section 5)
Setup: A field experiment conducted within ZipRecruiter's real commercial operations, testing customer price sensitivity.
Participants: ZipRecruiter customer leads (companies seeking to post job openings and find candidates via ZipRecruiter's matching algorithm).
Procedure: Different prices were randomly assigned to different customer leads; researchers observed and compared purchase likelihood across price points and customer segments.
Result: Some new-customer segments showed a >50% short-run profit increase from higher prices; ZipRecruiter then delayed broad implementation for four months to monitor whether higher-paying customers churned before concluding the price increase was durably profitable.
Interpretation: The experiment cleanly answered the "prediction" question (how will customers at different price points respond in the short run) but left the harder "judgment" question (how much weight to give short-run profit versus longer-term retention/word-of-mouth/platform-usage risk, and how long to wait before trusting the short-run result) to human decision-makers.
What It Demonstrates: Real-world reward function engineering requires combining a clean experimental/predictive answer with a separate, non-experimental judgment call about time horizon and competing objectives — prediction (via the RCT) did not by itself resolve the pricing decision.
Potential Alternative Explanation: The chapter doesn't address whether four months was empirically validated as sufficient (versus a judgment call that could have been wrong), leaving open whether even longer-term risks (beyond four months) might have been missed.
```

## 7. Cases and Stories

```
Case Title: Judging fraud at credit card networks (Mastercard, Visa, American Express)
People / Organization: Mastercard, Visa, American Express (named as examples); credit card networks generally
Context: The chapter's opening extended case, immediately following the introductory claim that prediction machines don't provide judgment.
What Happened: Credit card networks predict both applicant creditworthiness (a "sliding scale" decision, not binary, since the network must decide how much default/interest risk it's willing to accept) and, separately, whether any given transaction is legitimate or fraudulent — the latter decision requiring the four-outcome decision tree described in Section 4.
Outcome: Different risk-tolerance judgments about creditworthiness produce fundamentally different real business models (contrasted explicitly: American Express's high-end platinum card vs. an entry-level card marketed to college students).
Concept Illustrated: Judgment as a distinct, consequential business decision layered on top of (not replaced by) prediction, with direct product/business-model implications.
Why This Case Is Useful: A universally familiar consumer financial context that makes an abstract "judgment vs. prediction" distinction immediately concrete and relatable, while also demonstrating real strategic stakes (different card products/target markets).
Potential for Reuse: High
```

```
Case Title: Joshua's running-shoe purchases and credit card false declines
People / Organization: Joshua Gans (author); his credit card company (unnamed)
Context: A personal anecdote grounding the abstract fraud-prediction discussion in a concrete, relatable example of a false-positive fraud flag.
What Happened: Joshua routinely had his credit card transactions declined when buying running shoes at an outlet mall roughly once a year while on vacation, requiring him to call his credit card company to lift the restriction, for years. The chapter explains this occurs because credit card theft often happens at malls, and early fraudulent purchases are often easily-resold items like shoes and clothing — combined with Joshua's own atypical (infrequent) shopping pattern, the company's prediction reasonably (if incorrectly, in his case) flagged the purchase as likely stolen-card use.
Outcome: Used to set up the claim that richer, more personalized transaction-history data (specific to Joshua's own pattern of once-a-year outlet purchases) could let a prediction machine learn this is a *usual* event for him specifically, rather than an unusual one — and the chapter notes this improvement is "already happening," since Joshua's most recent such purchase went smoothly.
Concept Illustrated: The combination of generic (transaction-type-based) and personalized (individual-history-based) prediction factors, and how richer data resolves what looks like an intractable prediction/judgment trade-off.
Why This Case Is Useful: A relatable, mildly humorous personal anecdote (a common real-world annoyance many readers will recognize) that makes the abstract "generic vs. personalized prediction factors" concept concrete and memorable.
Potential for Reuse: High
```

```
Case Title: Waze and the multi-dimensional objective problem
People / Organization: Waze (Israeli startup, later acquired by Google); Tesla (mentioned for contrast, regarding EV charging-aware navigation)
Context: The chapter's central illustration of why human judgment remains necessary even when machine prediction is confident and technically accurate along its programmed dimension.
What Happened: Before being acquired by Google, Waze generated accurate real-time traffic maps by tracking the actual routes chosen by its own drivers (a data flywheel effect), using this to optimize suggested routes for speed, and could even forecast how traffic conditions might evolve to suggest better routes mid-trip. However, users sometimes override Waze's suggested route not because they disagree with its speed prediction, but because their true objective includes dimensions the app doesn't account for — most concretely, needing to stop for gas. The chapter notes this particular gap is solvable (a future version could ask about fuel needs, or infer it directly from car data; Tesla's built-in navigation already accounts for the analogous need to recharge, since EVs must do so periodically) — but other preference dimensions are harder to codify: wanting to pass certain good rest/food stops, disliking winding roads even if marginally faster, or valuing back-road quiet over the one-or-two-minutes saved by a suggested route.
Outcome: Used to establish the general principle that "a machine has fundamental limitations about how much it can learn to predict your preferences," because human objectives are typically multi-dimensional and weighted idiosyncratically/subjectively based on personal, often implicit reasoning the human alone possesses.
Concept Illustrated: The persistent gap between what a machine's prediction optimizes for and a human's full, often-idiosyncratic true objective function — and how this gap manifests as humans "overruling" machine suggestions, not because the machine's core prediction is wrong, but because judgment incorporates dimensions the prediction never included.
Why This Case Is Useful: An extremely relatable, near-universal modern experience (using/overriding a GPS navigation app) that makes an abstract point about multi-dimensional objectives immediately intuitive, with a natural, concrete contrast case (Tesla) showing how some such gaps do get closed over time.
Potential for Reuse: High
```

```
Case Title: Ada Support and hard-coded customer service judgment
People / Organization: Ada Support (AI-powered technical-support startup)
Context: The chapter's central illustration of successfully hard-coding judgment for well-understood, routine cases while reserving human judgment for genuinely difficult ones.
What Happened: For a typical mobile phone service provider, the vast majority of customer support questions have been asked (and correctly answered) many times before by other customers — the technical challenge isn't typing the answer, but predicting what the consumer actually wants and judging which stored answer to provide. Rather than simply directing customers to a static FAQ page, Ada's AI identifies and directly answers these frequent questions in real time, matching individual customer characteristics (technical competence history, phone type, past call history) to select the best-fitting answer, while routing unusual/difficult questions to human agents.
Outcome: Reduces customer frustration, handles a large volume of interactions quickly, and reduces the need to pay for costlier human call-center operators for routine questions — while humans specialize their (costlier, scarcer) judgment on the unusual/difficult cases that resist hard-coding.
Concept Illustrated: Hard-coding judgment for well-understood, high-frequency, low-uncertainty cases as a form of hybrid human-machine division of labor, directly paralleling the "prediction by exception" pattern introduced in Chapter 7.
Why This Case Is Useful: A concrete SaaS/customer-service business example that makes the abstract "hard-coding judgment" concept tangible via a familiar consumer-facing use case (tech support chatbots), and explicitly ties judgment-codification to real cost savings.
Potential for Reuse: High
```

```
Case Title: ZipRecruiter's data-driven pricing decision (see also Section 5/6)
People / Organization: ZipRecruiter (online job board); J. P. Dubé, Sanjog Misra (University of Chicago Booth School of Business economists)
Context: The chapter's culminating "putting it all together" case, showing reward function engineering applied to a genuine, high-stakes business pricing decision.
What Happened / Outcome: See Sections 5 and 6.
Concept Illustrated: The complete reward-function-engineering process in a real organization: (1) using a rigorous prediction/experimental method (RCT) to answer the tractable, short-run question cleanly; (2) recognizing that "best" is not self-evident and involves weighing multiple, partially-competing objectives (short-run profit, customer retention, word-of-mouth, platform liquidity/usage by job seekers); (3) exercising human judgment about how long to wait, and how much risk to tolerate, before committing to a decision based on the prediction.
Why This Case Is Useful: A complete, real, quantified (>50% profit finding, four-month monitoring window), business-relevant case that ties together nearly every concept in the chapter — arguably the chapter's most reusable teaching example for illustrating reward function engineering end-to-end.
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: Even "pure prediction" tasks contain a hidden judgment layer
Example: The credit card fraud decision tree — predicting fraud probability is separate from judging how to weigh recovery costs against customer dissatisfaction.
Why It Works: A fully worked numerical example (90% fraud probability, $20 recovery cost, $180 break-even dissatisfaction threshold) makes an abstract distinction mechanically concrete and directly computable.
Possible Alternative Domain: Business, Mathematics
```

```
Concept: Machine predictions optimize a narrower objective than a human's true, multi-dimensional preferences
Example: Overriding a Waze route suggestion because you need gas — an objective dimension the app's optimization doesn't include.
Why It Works: An almost universally shared, easily visualized modern experience that makes an abstract "multi-dimensional objective function" concept immediately intuitive without any math required.
Possible Alternative Domain: Everyday Life, AI
```

```
Concept: Hard-coding judgment for routine cases, reserving human judgment for exceptions
Example: Ada Support's AI answering frequent, well-understood tech-support questions while routing unusual questions to humans.
Why It Works: A relatable, familiar business context (customer support chatbots) that cleanly demonstrates the "codify the routine, escalate the exceptional" pattern in action, connecting directly back to Chapter 7's "prediction by exception" concept.
Possible Alternative Domain: Business, AI
```

## 9. Counterintuitive Insights

```
Insight: Improving a prediction machine's accuracy can, somewhat paradoxically, make it *easier* to remove humans from a decision loop entirely — precise-enough prediction lets an organization codify (hard-code) the accompanying judgment in advance, eliminating the need for ongoing case-by-case human review, as illustrated by increasingly confident credit-card fraud codification.
Common Belief: Better AI prediction should mean humans need to apply more careful, more frequent judgment to interpret increasingly complex/voluminous machine outputs.
Author's Argument: For well-understood, low-uncertainty decisions, sufficiently precise prediction can instead *reduce* the practical need for ongoing human judgment, because the judgment itself can be pre-specified once the range of likely predictions and appropriate responses becomes narrow and well-characterized enough.
Evidence: The credit-card fraud codification example, and the general Case 1 (hard-coded reward function) framework.
Why It Is Surprising: It seems to cut against the book's broader "judgment becomes more valuable" thesis (Ch.8/9's opening claims) — revealing that the judgment-value-increase effect applies unevenly, concentrating human judgment on harder/rarer cases while routine judgment gets automated away, rather than uniformly increasing demand for human judgment everywhere.
```

```
Insight: Uncertainty is precisely what makes judgment costly and necessary — you need judgment specifically to determine what to do when a prediction turns out to be *wrong*, not (only) when it's right, meaning the harder the prediction problem, the more valuable (and costly) judgment becomes.
Common Belief: Judgment is primarily about deciding what to do given an expected/likely outcome.
Author's Argument: The chapter's Key Points explicitly reframe judgment's core function around handling prediction failure: "uncertainty increases the cost of judging the payoffs for a given decision," precisely because you must weigh the costs of being wrong, not just the rewards of being right.
Evidence: The fraud decision tree's core logic (weighing the cost of a false decline against the cost of a missed fraud), which only matters because the prediction is imperfect (10% error rate in the worked example).
Why It Is Surprising: It reframes judgment as fundamentally a risk-management/error-cost-weighing activity rather than simply a preference-expression activity, tightly linking judgment's value to the specific unreliability of the prediction it's paired with.
```

## 10. Unique or Unusual Ideas

```
Idea: Naming "reward function engineering" as a distinct professional discipline/job category, by recognizing that humans already do this constantly and informally for other humans (parents raising children, mentors onboarding new workers, managers setting staff objectives) but have never needed to formalize it because it was always bundled with prediction and judgment in ordinary human interaction.
Why It Seems Unique: Draws a direct, somewhat startling parallel between mundane human socialization/management activities and a technical AI-engineering discipline, suggesting the underlying skill (helping another agent understand what actually matters and why) transfers directly from human-raising-human contexts to human-programming-machine contexts.
Potential Connection to Other Topics: Organizational behavior, parenting/pedagogy research, machine learning reward modeling and alignment (though the chapter doesn't use "alignment" terminology).
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: The chapter's opening and closing framing (better prediction raises the value of judgment) sits in some tension with its own hard-coding/reward-function-engineering discussion, which shows that sufficiently good prediction can instead eliminate the need for ongoing human judgment in specific, well-understood decisions (as in the credit-card fraud codification example) — a more nuanced, uneven pattern than a simple "judgment value goes up" headline suggests.
Author's Position: Not fully reconciled within this chapter; both claims are presented as true without explicitly mapping out which decisions fall into the "judgment value rises" category versus the "judgment gets automated away" category.
Possible Counterargument: A skeptical reader might argue the chapter's true claim is narrower than its framing suggests: judgment's *aggregate* value may rise (more total decisions receive some judgment, as some previously-defaulted decisions become worth deciding) even as judgment's *per-decision* value falls toward zero for an increasing share of well-understood, hard-codable decisions — these are compatible but meaningfully different claims that the chapter doesn't clearly disambiguate.
What Evidence Would Help Resolve It: Chapter 10 ("Predicting Judgment") and Chapter 12 ("Fully Automated Decision-Making") should clarify this further, particularly since this chapter explicitly forward-references Chapter 10's theme (machines learning to predict human judgment itself) as an encroachment on the "too costly to hard-code in advance" category.
```

## 12. Quotable Ideas

```
Paraphrase (short): Prediction machines don't provide judgment. Only humans do, because only humans can express the relative rewards from taking different actions.
Why the Idea Matters: The chapter's foundational, most-quotable claim, establishing the human role that persists even as AI takes over prediction.
Source Location: Book p.95
```

```
Paraphrase (short): Substitution of computers for people is bounded because there are many tasks people understand tacitly and accomplish effortlessly but cannot enunciate as explicit rules (McAfee and Brynjolfsson).
Why the Idea Matters: A precise, expert-sourced articulation of why full automation of judgment has real limits, grounding the chapter's hard-coding discussion in established economics-of-technology research.
Source Location: Book p.102–103, quoting Andrew McAfee and Erik Brynjolfsson
```

```
Paraphrase (short): Uncertainty means you need judgment when the prediction turns out to be wrong, not just when the prediction is right.
Why the Idea Matters: A sharp reframing of what judgment is actually for, tightly linking its value to a prediction's specific unreliability rather than treating it as a generic preference-expression activity.
Source Location: Book p.103
```

## 13. Psychology Connections

```
Connection: The Waze case's discussion of multi-dimensional, idiosyncratic, partly-implicit human objectives connects to psychological research on preference formation and the difficulty of fully introspecting or articulating one's own decision criteria, though the chapter does not cite this literature directly.
```

## 14. Mathematics and Decision Science Connections

```
Connection: The four-outcome fraud decision tree and its break-even threshold calculation (Section 4) is a direct application of expected-value decision theory, structurally identical to the umbrella example from Chapter 8 but applied to a real business context with dollar-denominated payoffs.
Connection: Reward function engineering, and specifically the discussion of an AI "over-optimizing" on a narrow success metric at the expense of broader organizational goals, is a plain-language description of a core challenge in reinforcement learning and objective/reward specification, closely related to what ML researchers call "reward hacking" or "specification gaming," though the chapter doesn't use this technical vocabulary.
Connection: The ZipRecruiter case's randomized pricing experiment is a direct, real-world application of randomized controlled trial methodology to a business optimization/causal-inference problem (price elasticity estimation).
```

## 15. Sports Connections

None identified in the chapter's direct examples; no forced inference added.

## 16. AI and Machine Learning Connections

```
Direct examples from the book: Credit card network fraud-prediction systems (Mastercard, Visa, American Express); Waze's crowdsourced traffic-prediction and route-optimization system; Tesla's charging-aware navigation; Ada Support's AI-powered customer-service triage system; self-driving vehicles as an example of hard-coded reward functions requiring instant action; ZipRecruiter's matching algorithm (mentioned briefly as the company's core product, distinct from the pricing-judgment case itself).
Inferred connection (my own): The chapter's discussion of reward function engineering and the risk of an AI "over-optimizing" on one metric inconsistently with broader goals directly parallels the modern machine learning/AI safety concept of reward misspecification or reward hacking (an agent optimizing a proxy reward in ways that diverge from the true intended objective) — a connection highly relevant to AI alignment discourse, though the chapter (published before this vocabulary became mainstream in public discussion) doesn't use these specific terms.
```

## 17. Content Creation Opportunities

```
Idea Title: "Why Your Credit Card Keeps Declining Your Favorite Purchase"
Format: YouTube Short | Visual Explainer
Application Domain: AI | Business | Everyday Life
Hidden Principle: Bayesian Thinking / Signal vs. Noise
Story Hook (Layer 1): One of this book's own authors couldn't buy running shoes on vacation for years — because his card kept getting flagged as stolen.
Principle Framework (Layer 2): "Pure prediction" problems (is this fraud?) always hide a second, separate judgment problem (how much does a false alarm cost versus a missed fraud?) — and richer personal data can resolve both at once.
Best Supporting Case: Joshua's running-shoe anecdote and the fraud decision tree (Section 7).
Character Application: Insight: Interpreter
Psychology Angle: None identified.
Math Angle: Direct — the break-even threshold calculation.
Sports Angle: None identified.
Business Angle: Direct — risk-tolerance decisions shaping entire product lines (AmEx platinum vs. student card).
Investing Angle: None identified.
History Angle: None identified.
AI Angle: Direct — generic vs. personalized prediction factors combining for better accuracy.
```

```
Idea Title: "Your GPS Isn't Wrong — It Just Doesn't Know You Need Gas"
Format: YouTube Short | Community Post
Application Domain: AI | Everyday Life
Hidden Principle: Optimization
Story Hook (Layer 1): You ignore Waze's "fastest route" all the time — and you're not disagreeing with the app, you're doing something it can't.
Principle Framework (Layer 2): Every optimization system solves for a narrower objective than your actual, multi-dimensional goals — and the gap between the two is exactly where human judgment lives.
Best Supporting Case: The Waze/Tesla case (Section 7).
Character Application: Insight: Interpreter
Psychology Angle: Multi-dimensional, idiosyncratic personal preferences that resist full articulation.
Math Angle: Single-objective optimization vs. multi-objective human decision-making.
Sports Angle: None identified.
Business Angle: Direct — any recommendation engine faces the same narrow-objective problem.
Investing Angle: None identified.
History Angle: None identified.
AI Angle: Direct — a clean, relatable illustration of why "the AI is technically right but still overruled" happens constantly.
```

```
Idea Title: "The Hiring Site That Found a 50% Profit Boost — Then Waited 4 Months to Use It"
Format: YouTube Long-form
Application Domain: Business | AI
Hidden Principle: Expected Value / Optimization
Story Hook (Layer 1): An experiment proved ZipRecruiter could raise prices and make 50% more profit overnight — so why didn't they do it immediately?
Principle Framework (Layer 2): Prediction can answer "what happens if" cleanly, but "is this actually the right call" requires judgment about competing goals and time horizons that no experiment alone can resolve.
Best Supporting Case: The ZipRecruiter pricing case (Section 5/6/7).
Character Application: Sigma: Architect
Psychology Angle: None identified.
Math Angle: Direct — randomized pricing experiments, short-run vs. long-run trade-offs.
Sports Angle: None identified.
Business Angle: Direct — a complete, real pricing-strategy case study.
Investing Angle: Inferred — analogous to any business decision requiring balancing an experimentally-clean short-term signal against unmeasured long-term risk.
History Angle: None identified.
AI Angle: Direct — reward function engineering in a real commercial deployment.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B04-C09-01
Title: Prediction machines don't provide judgment
Type: Claim
Summary: Only humans can express the relative rewards of different actions; as AI takes over prediction, humans increasingly specialize in judgment alone, interacting with machine predictions much like running queries against a spreadsheet.
Source: Book p.95
Tags: judgment, definition, human-AI division of labor
Related Concepts: Anatomy of a decision (Ch.8), reward function
```

```
CARD ID: B04-C09-02
Title: The credit card fraud decision tree
Type: Model
Summary: A four-outcome decision tree (decline/accept × fraudulent/legitimate) showing that "predicting fraud" hides a separate judgment problem — weighing recovery cost against customer dissatisfaction — with a worked example yielding a $180 break-even dissatisfaction threshold for a $100/$20-recovery-cost transaction at 90% predicted fraud probability.
Source: Book p.96–99
Tags: decision tree, judgment, fraud, credit cards
Related Concepts: Umbrella decision tree (Ch.8), reward function
```

```
CARD ID: B04-C09-03
Title: The cognitive costs of judgment
Type: Concept
Summary: Judgment requires costly cognitive work — via deliberation/research or trial-and-error experimentation — and the number of payoffs needing judgment multiplies quickly as actions and situations increase, creating a real trade-off between careful and fast decision-making.
Source: Book p.99–100
Tags: judgment, cognitive cost, decision-making
Related Concepts: Reward function engineering
```

```
CARD ID: B04-C09-04
Title: Waze and multi-dimensional objectives
Type: Case
Summary: Waze users override "fastest route" suggestions not because the prediction is wrong, but because their true objective includes dimensions (needing gas, wanting scenic roads) the app's optimization doesn't capture — illustrating that machines have fundamental limits on learning idiosyncratic human preferences.
Source: Book p.100–102
Tags: AI, navigation, multi-dimensional objectives, judgment
Related Concepts: Reward function, hard-coding judgment
```

```
CARD ID: B04-C09-05
Title: Ada Support — hard-coding judgment for routine cases
Type: Case
Summary: Ada Support's AI directly answers frequent, well-understood tech-support questions (matching customer characteristics to select answers) while routing unusual questions to human agents — a real example of hard-coded judgment paired with prediction-by-exception.
Source: Book p.102
Tags: AI, customer service, hard-coding judgment, case
Related Concepts: Prediction by exception (Ch.7), tacit knowledge limits
```

```
CARD ID: B04-C09-06
Title: Reward function engineering
Type: Model
Summary: The discipline of determining rewards for actions given AI predictions, split into hard-coded (pre-specified, enabling full automation, as in self-driving cars) and post hoc (human judges each prediction case-by-case, when combinations are too numerous to pre-specify) approaches; humans already informally perform this role for other humans (parents, mentors, managers).
Source: Book p.103–105
Tags: framework, reward function, automation, judgment
Related Concepts: Hard-coding judgment, ZipRecruiter case
```

```
CARD ID: B04-C09-07
Title: ZipRecruiter's pricing experiment and judgment call
Type: Study
Summary: A randomized pricing experiment by economists Dubé and Misra found raising prices for some new-customer segments would boost short-run profit over 50%; ZipRecruiter then applied human judgment, waiting four months to confirm no longer-term customer attrition before fully implementing the change.
Source: Book p.104–105
Tags: RCT, pricing, judgment, business case
Related Concepts: Reward function engineering, cognitive costs of judgment
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: Prediction machines supply only the prediction half of decision-making — judgment (expressing the relative rewards of different actions and outcomes) remains an exclusively human capability, and better prediction increases the value of judgment by creating more opportunities to apply it; but judgment itself is costly to produce (via deliberation or experimentation), so organizations face a real design choice between hard-coding judgment in advance ("reward function engineering") for well-understood, high-volume decisions, versus reserving case-by-case human judgment for decisions too numerous, uncertain, or idiosyncratic to pre-specify.
Top 5 Concepts: (1) Prediction machines don't provide judgment. (2) The four-outcome fraud decision tree, extending Ch.8's umbrella tree to a business context. (3) The cognitive costs of judgment (deliberation vs. experimentation). (4) Multi-dimensional, idiosyncratic human objectives (the Waze gas-station problem). (5) Reward function engineering, split into hard-coded and post hoc human-judgment approaches.
Top 3 Claims: (1) Better prediction raises the value of judgment by creating more decisions worth deciding. (2) Even "pure prediction" tasks (fraud detection) hide a distinct, consequential judgment layer with real business-model implications. (3) Uncertainty specifically drives judgment's cost and value — you need judgment for when predictions are wrong, not just when they're right.
Top 3 Cases: (1) ZipRecruiter's randomized pricing experiment and four-month judgment-driven rollout delay. (2) Waze and the multi-dimensional objective problem (needing gas). (3) Ada Support's hard-coded customer-service judgment paired with human escalation for hard cases.
Top 3 Studies: (1) The ZipRecruiter/Dubé-Misra randomized pricing experiment (>50% short-run profit finding). (2) [No second independently detailed formal study identified — the credit-card fraud and Joshua's anecdote are illustrative, not cited research.] (3) [No third formal study identified.]
Most Unique Idea: Naming "reward function engineering" as a formal discipline by recognizing it as the same activity humans already perform informally for other humans (parenting, mentoring, managing) — just newly needing to be made explicit for machines.
Most Counterintuitive Idea: Sufficiently precise prediction can eliminate the need for ongoing human judgment in specific decisions (via hard-coding) even as, in aggregate, better prediction is said to increase judgment's total value — a tension between per-decision automation and aggregate demand growth the chapter doesn't fully resolve.
Biggest Weakness or Open Question: The chapter's "judgment becomes more valuable" thesis and its "judgment gets hard-coded away" mechanism sit in unreconciled tension — it's unclear from this chapter alone which decisions end up in which category, or how an organization should predict in advance whether a given decision domain will trend toward more human judgment or toward full automation.
Best Content Opportunity: "The Hiring Site That Found a 50% Profit Boost — Then Waited 4 Months to Use It" (Section 17) — a complete, quantified, real business case that demonstrates the full prediction-then-judgment pipeline end-to-end.
```
