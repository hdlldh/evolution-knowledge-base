# Prediction Machines — Chapter 15: Decomposing Decisions
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Extraction
**Source:** Book pages 157–164 (PDF pages 170–177)
**Date:** 2026-08-04
**Revised:** Per Chapter_15_Audit.md — corrected the Action/Judgment "(expensive)" misattribution in the Atomwise canvas; sharpened the Atomwise Action/Feedback wording; restored specific time-bound qualifiers in the "best students" example; added the precise ROI operationalization and the "core prediction can require AI insight" claim.

BOOK:
Prediction Machines: The Simple Economics of Artificial Intelligence

AUTHOR:
Ajay Agrawal, Joshua Gans, Avi Goldfarb

CHAPTER:
15 — Decomposing Decisions

---

## 1. Chapter Thesis

Today's AI tools are narrow prediction engines, not general intelligences — each delivers a single predictive component that empowers a human decision rather than performing an entire workflow end to end. Having established in Chapter 14 that the task is the right unit for locating where AI can help, this chapter goes one level deeper: within a task, the decision itself must be decomposed into its constituent elements (prediction, judgment, action, outcome, input, training, feedback) before anyone can evaluate, design, or build an AI tool for it. The authors formalize this decomposition as a practical instrument — the "AI canvas" — and demonstrate it on two worked examples (the biotech company Atomwise and a hypothetical MBA-recruiting AI), showing that the discipline of filling out the canvas often exposes a harder, prior problem: organizations frequently don't have a sufficiently specific objective (what counts as "best," what trade-off governs an error) for a prediction machine to be built around at all.

## 2. Key Concepts

```
Concept Name: AI tools as predictive components, not full workflows
Definition: The observation that current-generation AI tools — Amazon's Echo (predicting the intention of speech), Apple's Siri (predicting command context), Amazon's recommendations (predicting what you want to buy), Google search (predicting which links connect you to the information you want), Tesla's Autopilot (predicting when to apply the brakes), Facebook's newsfeed (predicting the news you want to read) — do not perform an entire workflow; each delivers a single predictive component that makes it easier for a human (or a larger automated system) to make one decision.
Why It Matters: Grounds the chapter's central move — since AI's actual unit of contribution is a decision's predictive element, not a whole workflow or task, the correct level of analysis for designing or evaluating an AI tool is the decision itself, decomposed into its parts.
How the Author Uses It: Opens the chapter with six concrete named-product examples spanning consumer and enterprise contexts, paired with Steve Jobs's "bicycle for the mind" framing of computers as tools (not competitors to human intelligence), to establish that "AI empowers" rather than replaces.
Related Concepts: Anatomy of a decision (Ch.8), the workflow-task-decision hierarchy (Ch.14)
```

```
Concept Name: The AI Canvas
Definition: A seven-box template (Figure 15-1) for decomposing a task's decision into its constituent elements, directly derived from the anatomy-of-a-decision framework (Figure 8-1): Prediction, Judgment, Action, and Outcome across the top row; Input, Training, and Feedback across the bottom row. Filling out the canvas for a task forces explicit answers to: what data is needed to run the algorithm (Input); what data is needed to train it (Training); what action follows the decision (Action); how outcomes feed back to improve the algorithm (Feedback); what the algorithm needs to predict (Prediction); how different outcomes/errors are valued (Judgment); and what the metric for task success is (Outcome).
Why It Matters: Provides the chapter's central practical tool — a repeatable, disciplined method any team can use to move from "we think AI could help here" to a concrete specification of what needs to be built, trained, and evaluated, forcing clarity about each component rather than leaving any of them implicit.
How the Author Uses It: Introduced as a product of the authors' experience advising CDL startups; presented via Figure 15-1 (the blank canvas) and then demonstrated fully filled-out for two cases — Atomwise (Figure 15-2) and a hypothetical MBA-recruiting AI (Figure 15-3).
Related Concepts: Anatomy of a decision (Ch.8), reward function engineering (Ch.9)
```

```
Concept Name: The prior problem of specifying the objective ("what is our real objective, anyway?")
Definition: The recurring finding that attempting to fill in the Prediction and Outcome boxes of the AI canvas exposes that many organizations' stated goals (mission statements, strategy documents) are too vague or multifaceted to specify what an AI should actually predict — e.g., a business school saying it wants the "best" students doesn't specify whether "best" means the highest salary offer upon graduation, most likely to assume a CEO role within five years, most diverse, or most likely to donate to the school after graduation — and even a seemingly crisp goal like "maximize profit" is ambiguous over what time horizon (this week, this quarter, this year, this decade).
Why It Matters: Reveals that the hardest part of deploying an AI tool is often not a technical problem at all but an organizational one — forcing leadership to resolve genuine ambiguity or disagreement about objectives that was previously left comfortably unresolved because no decision-making process required this level of precision.
How the Author Uses It: Framed as an "existential discussion" that the AI canvas exercise often triggers among a leadership team, illustrated with the business-school "best students" example and generalized to the profit-maximization time-horizon problem in the chapter's Key Points.
Related Concepts: Reward function engineering (Ch.9), AI Insight (Ch.2)
```

## 3. Key Claims

```
Claim: None of the six named real-world AI tools discussed at the chapter's opening (Amazon Echo, Siri, Amazon recommendations, Google search, Tesla Autopilot, Facebook newsfeed) perform an entire workflow — each delivers only a predictive component that empowers a human or downstream system to make a decision.
Type: Empirical/Interpretive
Evidence Provided: Six concrete named products with their specific predictive function stated (Echo predicts intention of speech; Siri predicts command context; Amazon recommendations predict purchase intent; Google search predicts relevant links; Tesla Autopilot predicts when to brake; Facebook newsfeed predicts desired news).
Strength of Support: Strong as a descriptive claim about well-known, verifiable products' actual function as of the book's writing; functions as the chapter's foundational premise rather than a claim requiring further evidentiary support.
```

```
Claim: Atomwise's AI tool dramatically lowers the cost and accelerates the speed of the first task in drug discovery (identifying candidate molecules) by predicting the binding affinity of millions of possible molecules to a target disease protein, but the drug company still needs to test and verify candidates through a combination of human and machine judgments and actions — AI does not replace the full drug-discovery workflow, only its molecule-identification task.
Type: Empirical
Evidence Provided: A direct quote from Atomwise CEO Abraham Heifets explaining the underlying science ("For a drug to work, it has to bind the disease target, and it has to fail to bind proteins in your liver, your kidneys, your heart, your brain... It comes down to 'stick to the things you want to stick to, fail to stick to the things you don't.'"); a concrete example (Atomwise providing the top twenty molecules with highest binding affinity for a target such as the Ebola virus protein); the stated data scale (38 million public binding-affinity data points as of July 2017, plus additional purchased or self-generated data).
Strength of Support: Strong — grounded in a named company, a named CEO quote, and a specific, dated data-scale figure, consistent with the book's established use of concrete CDL-adjacent case studies.
```

```
Claim: Judgment in the Atomwise case takes the specific form of weighing the aggregate value of a candidate molecule to the pharmaceutical industry, which requires balancing the payoff of successfully targeting the disease against the cost of potential side effects — and this trade-off is not fixed but context-dependent (the tolerance for side effects differs by application).
Type: Empirical/Interpretive
Evidence Provided: A direct quote from Heifets illustrating the context-dependence of the trade-off: "You are more tolerant of side effects for chemotherapy than for an acne cream."
Strength of Support: Strong — a specific, quotable, intuitively verifiable example (chemotherapy's life-or-death stakes justify higher side-effect tolerance than a cosmetic treatment) that clearly illustrates why judgment must be set by humans (the company and its customers) rather than derived from the prediction itself.
```

```
Claim: For the hypothetical MBA-recruiting AI canvas (Figure 15-3), the prediction task is defined as predicting whether an applicant would be among the 50 most influential alumni 10 years after graduation, with judgment set by weighing the cost of a false positive (accepting a candidate who turns out not to be a top-50 alumnus) against the cost of a false negative (rejecting/not targeting a candidate who would have been top-50) — and the resulting canvas requires input data (application forms, résumés, GMAT scores, social media), training data (the same inputs plus the outcome/impact measure), and annual feedback updates using applicant and career outcomes.
Type: Theoretical (hypothetical worked example)
Evidence Provided: A fully filled-out AI canvas (Figure 15-3) walking through all seven elements for this specific hypothetical, with the school's chosen strategic proxy (global business impact of alumni, operationalized as identifying the 50 most impactful alumni per graduating class) explicitly flagged as one subjective but not impossible choice among several the school could have made.
Strength of Support: Strong as an illustrative worked example of the canvas methodology; explicitly hypothetical/illustrative rather than an empirical claim about any real MBA program's actual practice.
```

```
Claim: Many organizations' mission statements are vague and multifaceted in ways that serve marketing purposes well but fail to specify a usable prediction objective for an AI tool, and business schools in particular have many strategies that implicitly or explicitly define "best" (e.g., maximizing GMAT scores, boosting rankings in the Financial Times or US News & World Report, recruiting a mix of quantitative/qualitative skill sets, prioritizing international students, prioritizing diversity) — no school can pursue all of these simultaneously without compromising on all dimensions and excelling at none.
Type: Interpretive
Evidence Provided: A list of concrete alternative strategic definitions of "best" a business school might implicitly or explicitly adopt, presented as illustrative of the underlying ambiguity problem rather than as an empirically surveyed set of actual school strategies.
Strength of Support: Moderate — a plausible, well-illustrated interpretive argument grounded in the authors' own professional familiarity with business-school strategy (established in Ch.14's MBA example), rather than a claim citing external survey data on school mission statements.
```

```
Claim: Estimating the ROI of inserting a prediction machine into a task specifically means estimating the benefit of the enhanced prediction minus the cost of generating that prediction — once reasonable estimates exist, AI tools should be rank-ordered from highest to lowest ROI and implemented top-down as long as the expected ROI makes sense.
Type: Interpretive (methodological)
Evidence Provided: Stated directly in the chapter's Key Points (book p.164), echoing and sharpening the ROI-ranking implementation methodology introduced in Chapter 14's own Key Points.
Strength of Support: Strong as the chapter's own explicit operational definition of ROI in this context, though it does not specify how to estimate either the benefit or the cost in practice.
```

```
Claim: Identifying the core prediction at the heart of a task — the item at the center of the AI canvas — can itself require "AI insight," not merely careful specification once the prediction target is already known.
Type: Interpretive
Evidence Provided: Stated directly in the chapter's Key Points (book p.164): "At the center of the AI canvas is prediction. You need to identify the core prediction at the heart of the task, and this can require AI insight."
Strength of Support: Strong as the chapter's own explicit claim, and it directly ties the AI canvas's central element back to the "AI Insight" concept defined in Chapter 2 (recognizing an unfamiliar problem as one an AI could solve).
```

## 4. Frameworks, Models, and Mental Models

```
Name: The AI Canvas (Figures 15-1, 15-2, 15-3)
Description: A seven-box decomposition template for specifying everything needed to build, evaluate, or advise on an AI tool for a specific task-level decision, directly derived from the anatomy-of-a-decision elements introduced in Chapter 8 (Figure 8-1: prediction, input, judgment, training, action, outcome, feedback).
Components: Top row — Prediction (what you need to know to make the decision), Judgment (how you value different outcomes and errors), Action (what you are trying to do), Outcome (your metric for task success). Bottom row — Input (what data you need to run the predictive algorithm), Training (what data you need to train the predictive algorithm), Feedback (how you use outcomes to improve the algorithm over time).
How It Works: A team fills in each of the seven boxes for a specific task, in the process being forced to answer seven concrete questions rather than leaving any of prediction, judgment, action, outcome, input, training, or feedback vaguely implied. The exercise typically surfaces where the true difficulty lies — most often in specifying Prediction and Judgment precisely, since these require the organization to have (or develop) a genuinely specific objective.
When It Is Useful: Whenever an organization has identified a candidate task (via the Ch.14 workflow decomposition) and needs to move from "AI might help here" to an actionable specification of what data, judgment criteria, and success metrics the AI tool requires — used by the authors both as an advising tool for CDL startups and, in the chapter, as a business-side planning tool (MBA recruiting example).
Limitations: The canvas structures the questions but does not answer them — as the chapter's own examples show, filling it out honestly can reveal that an organization lacks a sufficiently specific objective, which the canvas cannot resolve on its own (it surfaces the problem rather than solving it).
```

## 5. Research and Evidence

None identified as formally cited academic studies within this chapter — the chapter's evidence consists of a named company case study (Atomwise, with a named-CEO quote and a specific, dated data-scale figure) and a fully worked hypothetical example (MBA recruiting), rather than cited external research.

## 6. Experiments

None identified.

## 7. Cases and Stories

```
Case Title: Atomwise's AI-powered drug-candidate binding-affinity prediction
People / Organization: Atomwise (biotech company); CEO Abraham Heifets
Context: The chapter's primary worked example demonstrating the AI canvas applied to a real company, illustrating how the seven-element decomposition clarifies exactly what an AI tool does and does not do within a larger workflow.
What Happened: Atomwise built a prediction tool to shorten the time involved in discovering promising pharmaceutical drug candidates. Since millions of possible drug molecules could theoretically become drugs, but purchasing and testing each one is time-consuming and costly, drug companies traditionally made educated guesses (predictions) based on research about which molecules were most likely to bind effectively to a disease target while failing to bind to unrelated proteins (liver, kidneys, heart, brain) that would cause toxic side effects. Atomwise's AI tool predicts the binding affinity of molecules to a target protein, allowing it to recommend to drug companies a ranked list of the molecules most likely to work — e.g., providing the top twenty molecules with the highest binding affinity for a protein such as the Ebola virus target — handling millions of possibilities rather than testing molecules one at a time. As of July 2017, the underlying prediction machine had learned from 38 million public data points on binding affinity, plus additional data either purchased or generated by Atomwise itself, with each data point consisting of molecule and protein characteristics plus a measure of binding between them.
Outcome: The drug company still needs to test and verify candidates through a combination of human and machine judgments and actions, but the Atomwise AI tool dramatically lowers the cost and accelerates the speed of the first task (finding promising candidates) within the larger drug-discovery workflow. The chapter's Figure 15-2 fills out the full AI canvas for Atomwise: Prediction = binding affinity; Judgment = balancing binding affinity to the disease protein against potential side effects; Action = conduct the test to help cure or prevent disease (expensive); Outcome = test results (successful tests leading to a new drug treatment); Input = protein characteristics; Training = binding affinity of molecules and proteins from past studies, plus molecule/protein characteristics; Feedback = new data on binding affinity from Atomwise's own recommendations, using test outcomes regardless of their success to improve future predictions.
Concept Illustrated: The AI Canvas methodology applied end to end to a real company, and the broader principle that an AI tool's value proposition lies in removing one specific prediction task from human hands (here, initial candidate screening) while leaving surrounding judgment- and action-heavy tasks (testing, verification) to a human-machine combination.
Why This Case Is Useful: A concrete, quantified (38 million data points, top-20 ranked output), named-executive-quoted case that makes the otherwise abstract seven-box canvas exercise tangible, and that vividly illustrates context-dependent judgment via the chemotherapy-vs-acne-cream side-effect-tolerance example.
Potential for Reuse: High
```

```
Case Title: The hypothetical AI canvas for MBA recruiting admissions decisions
People / Organization: Not specified (a hypothetical business school, building on the same MBA-recruiting context introduced in Ch.14)
Context: The chapter's second worked example, applying the AI canvas to a large-organization, non-drug-discovery context, and using it to surface the deeper problem of underspecified organizational objectives.
What Happened: The authors imagine a school whose strategy is to have the greatest impact on business globally (a subjective but global-rather-than-local, impact-rather-than-income-or-wealth-focused notion). To make this predictable, they (acting as reward-function engineers) propose a training-data proxy: identifying the fifty most impactful alumni from each graduating class — a subjective but not impossible judgment call. The resulting Figure 15-3 canvas: Prediction = predict whether an applicant would be among the 50 most influential alumni 10 years after graduation; Judgment = determine the relative value of accepting a top-50-caliber candidate versus the cost of a false positive (accepting a candidate who is not top-50) versus the cost of a false negative (missing/not targeting a candidate who would have been top-50); Action = accept applicants into the program; Outcome = higher-quality alumni, as measured by global influence 10 years after graduation; Input = application forms, résumés, GMAT scores, social media; Training = application forms, résumés, GMAT scores, social media, plus the outcome/impact measure; Feedback = update with applicant and career outcomes annually.
Outcome: The chapter uses the exercise to show that once the prediction objective is specified, identifying the needed input data is straightforward (application information, possibly social media, with career-outcome feedback observed over time) — but that specifying the objective in the first place (what "best" means, operationalized as a measurable target) is the genuinely hard step, one that is subjective but must be made concrete enough to train a predictive algorithm.
Concept Illustrated: The AI Canvas applied to a non-drug-discovery, judgment-heavy organizational decision, and the "prior problem of specifying the objective" concept — the canvas methodology forces an organization to convert a vague strategic aspiration ("greatest global impact") into an operational, measurable prediction target.
Why This Case Is Useful: Directly continues and deepens the Ch.14 MBA hypothetical with a fully specified, element-by-element canvas, giving readers a transferable template they can adapt to their own organization's admissions-like or selection-like decisions.
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: The AI Canvas as a decomposition discipline
Example: The Atomwise case, fully filled out across all seven canvas boxes (Figure 15-2) with concrete, specific answers for each element.
Why It Works: Moves the canvas from an abstract seven-box diagram to a fully worked, verifiable example grounded in a real company, a named-executive quote, and a specific data-scale figure — showing exactly what a "good" completed canvas looks like.
Possible Alternative Domain: Business, AI, Healthcare/Biotech
```

```
Concept: The prior problem of specifying a vague objective
Example: The business-school "best students" problem — a mission statement that sounds clear in a marketing brochure (recruit the "best" students) turns out to require resolving genuine ambiguity (best by salary? by CEO likelihood? by diversity? by donations?) before any AI tool can be built.
Why It Works: A relatable, intuitively graspable example (everyone has encountered a vague institutional mission statement) that makes an abstract point — organizational objectives are often underspecified — concrete and immediately actionable as a diagnostic question to ask before any AI project begins.
Possible Alternative Domain: Business, Education, Everyday Life
```

## 9. Counterintuitive Insights

```
Insight: The hardest part of building an AI tool is often not a technical or data problem at all, but an organizational one — forcing leadership to answer a question ("what is our real objective, anyway?") that the organization had previously never needed to answer with precision.
Common Belief: Building an AI tool is primarily a technical challenge — getting enough data, choosing the right algorithm, achieving sufficient accuracy.
Author's Argument: Attempting to fill in the Prediction and Judgment boxes of the AI canvas routinely reveals that an organization's stated goals are too vague or multifaceted to specify what should actually be predicted, turning what looked like a data-science project into an "existential discussion" about organizational objectives.
Evidence: The business-school "best students" example (highest salary offer upon graduation? most likely to assume a CEO role within five years? most diverse? most likely to donate to the school after graduation?) and the generalized point (in Key Points) that even seemingly straightforward objectives like profit maximization are ambiguous once you ask over what time horizon (week, quarter, year, decade) profit should be maximized.
Why It Is Surprising: It inverts the expected difficulty ordering for AI projects — the prediction technology itself (the part that sounds hard) is often more tractable than the judgment/objective-setting step (the part that sounds like it should already be settled).
```

## 10. Unique or Unusual Ideas

```
Idea: Positioning the AI canvas explicitly as a direct structural derivative of an earlier analytical framework (the anatomy of a decision, Figure 8-1) rather than as a freestanding new tool — making the canvas a practical, fillable instrument built for consistency with the book's own theoretical apparatus.
Why It Seems Unique: Rather than introducing a new ad hoc business-planning template disconnected from the book's argument, the authors explicitly trace the canvas's seven boxes back to the decision-anatomy vocabulary established six chapters earlier, reinforcing the book's overall internal consistency and giving the canvas theoretical grounding rather than presenting it as a generic consulting tool.
Potential Connection to Other Topics: Business Model Canvas and Lean Canvas methodologies in entrepreneurship, which the AI Canvas is structurally reminiscent of (a fillable, box-based strategic template), though the chapter does not itself draw this comparison.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: The chapter presents the AI canvas as a tool that "forces clarity" and "introduces discipline," implying that going through the exercise reliably produces a usable, specific objective — but its own examples (business-school "best," profit-maximization time horizon) suggest that the exercise may just as often surface irreducible organizational disagreement or genuine strategic trade-offs that cannot be neatly resolved by filling in a box.
Author's Position: The chapter treats "sharpening the mission statement" as an achievable, even routine, first step in AI strategy work, without extensively addressing what happens when leadership cannot agree on the answer.
Possible Counterargument: In some organizations, the vagueness of a mission statement may not be a solvable specification problem but a deliberately preserved ambiguity (e.g., balancing multiple stakeholder interests, avoiding alienating some constituency) — in which case the AI canvas exercise would surface not a fixable gap but a genuine, ongoing organizational tension that a single planning session cannot resolve.
What Evidence Would Help Resolve It: Case evidence on organizations that attempted the AI-canvas exercise and failed to reach agreement on the objective — this chapter's own examples are all successfully resolved hypotheticals, not documented cases of the exercise stalling.
```

## 12. Quotable Ideas

```
Paraphrase (short): One of the things that really separates us from the high primates is that we're tool builders... What a computer is to me is it's the most remarkable tool that we've ever come up with, and it's the equivalent of a bicycle for our minds (Steve Jobs).
Why the Idea Matters: Frames the entire chapter's stance on current AI — as an empowering tool that amplifies human decision-making, not a replacement intelligence — right at the outset, before any technical or business content is introduced.
Source Location: Book p.157, quoting Steve Jobs
```

```
Paraphrase (short): For a drug to work, it has to bind the disease target and fail to bind proteins in your liver, kidneys, heart, brain, and other things that would cause toxic side effects — it comes down to "stick to the things you want to stick to, fail to stick to the things you don't" (Atomwise CEO Abraham Heifets).
Why the Idea Matters: A vivid, memorable, plain-language summary of binding-affinity prediction that makes an otherwise technical biotech concept immediately graspable.
Source Location: Book p.159, quoting Abraham Heifets
```

```
Paraphrase (short): You are more tolerant of side effects for chemotherapy than for an acne cream (Abraham Heifets).
Why the Idea Matters: A sharp, concrete illustration of why "judgment" (the relative cost of errors) is context-dependent and cannot be derived from the prediction itself — it must be set explicitly by humans.
Source Location: Book p.160, quoting Abraham Heifets
```

```
Paraphrase (short): What is our real objective, anyway?
Why the Idea Matters: The chapter's own distillation of the "existential discussion" that the AI canvas exercise often triggers — a one-line summary of the chapter's most counterintuitive finding (Section 9).
Source Location: Book p.164 (Key Points)
```

## 13. Psychology Connections

None identified — the chapter is primarily organizational/methodological in content rather than psychological.

## 14. Mathematics and Decision Science Connections

```
Connection: The MBA canvas's judgment element (weighing the cost of a false positive — accepting a non-top-50 candidate — against the cost of a false negative — missing a top-50 candidate) is a direct application of the false-positive/false-negative error-cost framework introduced in Chapter 13, now embedded as one specific box within the broader AI canvas.
Connection: The Atomwise ranked-list approach (top-20 molecules by binding affinity, handling millions of possibilities at once) reflects a standard machine-learning ranking/scoring paradigm, applied here to a molecular screening problem rather than a typical recommendation or search context.
```

## 15. Sports Connections

None identified in the chapter's direct examples; no forced inference added.

## 16. AI and Machine Learning Connections

```
Direct examples from the book: Amazon Echo (speech-intention prediction); Apple Siri (command-context prediction); Amazon recommendations (purchase-intent prediction); Google search (relevant-link prediction); Tesla Autopilot (braking-timing prediction); Facebook newsfeed (news-relevance prediction); Atomwise's binding-affinity prediction model trained on 38 million+ public data points (molecule/protein characteristics plus a binding measure); the hypothetical MBA-recruiting predictive-ranking model trained on application data, résumés, GMAT scores, and social media, with annual feedback from career outcomes.
Inferred connection (my own): The Atomwise model is describable in modern ML terms as a ranking/regression model over a molecule-protein interaction feature space, and the MBA canvas describes a standard supervised binary/ranking classification setup (predict top-50-alumnus likelihood) with an explicit human-defined cost-asymmetric loss function (false positive vs. false negative costs) — though the chapter itself does not use this specific technical vocabulary.
```

## 17. Content Creation Opportunities

```
Idea Title: "The 7-Box Canvas That Decides Whether Your AI Idea Actually Works"
Format: YouTube Long-form | Community Post
Application Domain: AI | Business
Hidden Principle: Optimization
Story Hook (Layer 1): A biotech startup uses one simple 7-box worksheet to decide which of millions of drug molecules are worth testing — and the same worksheet works for deciding who gets into your MBA program.
Principle Framework (Layer 2): Before building any AI tool, force yourself to answer seven specific questions — what to predict, how to judge errors, what data trains it, what data runs it, what action follows, how you measure success, and how outcomes feed back — because skipping any one of them means building blind.
Best Supporting Case: The Atomwise AI canvas (Figure 15-2, Section 7).
Character Application: Sigma: Architect
Psychology Angle: None identified.
Math Angle: Direct — false positive/false negative cost trade-offs as one canvas element.
Sports Angle: None identified.
Business Angle: Direct — a reusable planning template for any AI initiative.
Investing Angle: Inferred — evaluating an AI startup's pitch by checking whether they can clearly fill out all seven canvas boxes.
History Angle: None identified.
AI Angle: Direct — a practical AI-tool specification methodology.
```

```
Idea Title: "Your Company's Mission Statement Isn't Specific Enough to Build an AI For"
Format: YouTube Short | Visual Explainer
Application Domain: Business | AI
Hidden Principle: Signal vs. Noise
Story Hook (Layer 1): Ask any company what "best" means and you'll get a marketing slogan. Ask an AI to predict "best" and the slogan falls apart.
Principle Framework (Layer 2): Vague strategic language works fine for humans making judgment calls case by case, but a prediction machine needs a single, specific, measurable target — which means building an AI tool often starts with an uncomfortable argument about what your organization actually wants.
Best Supporting Case: The business-school "best students" example and the profit-maximization time-horizon problem (Section 9, Key Points).
Character Application: Insight: Interpreter
Psychology Angle: None identified.
Math Angle: None identified.
Sports Angle: None identified.
Business Angle: Direct — mission-statement specificity as a prerequisite for AI strategy.
Investing Angle: None identified.
History Angle: None identified.
AI Angle: Direct — the objective-specification bottleneck in AI project planning.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B04-C15-01
Title: AI tools as predictive components, not full workflows
Type: Concept
Summary: Six major real-world AI tools (Echo, Siri, Amazon recommendations, Google search, Tesla Autopilot, Facebook newsfeed) each deliver only a single predictive component that empowers a human decision, rather than performing an entire workflow — "AI empowers."
Source: Book p.157
Tags: AI tools, prediction, decision support
Related Concepts: Workflow-task-decision hierarchy (Ch.14)
```

```
CARD ID: B04-C15-02
Title: The AI Canvas
Type: Model
Summary: A seven-box template (Prediction, Judgment, Action, Outcome, Input, Training, Feedback), derived from the anatomy of a decision (Ch.8), used to decompose a task's decision into everything needed to build, evaluate, or advise on an AI tool for it.
Source: Book p.158–159, Figure 15-1
Tags: framework, AI canvas, decision decomposition
Related Concepts: Anatomy of a decision (Ch.8)
```

```
CARD ID: B04-C15-03
Title: Atomwise's binding-affinity prediction canvas
Type: Case
Summary: Atomwise predicts molecule-protein binding affinity to rank drug candidates (e.g., top 20 for a target like Ebola), trained on 38M+ data points as of July 2017; the full AI canvas specifies judgment as balancing disease-targeting payoff against side-effect cost.
Source: Book p.158–161, Figure 15-2
Tags: case, Atomwise, drug discovery, AI canvas
Related Concepts: The AI Canvas
```

```
CARD ID: B04-C15-04
Title: The MBA recruiting AI canvas and the objective-specification problem
Type: Case
Summary: A hypothetical AI canvas for MBA admissions predicts whether an applicant will be among the top-50 most influential alumni 10 years out; building it requires first resolving what "best" means, exposing that vague mission statements aren't specific enough to train a prediction machine.
Source: Book p.162–164, Figure 15-3
Tags: case, MBA recruiting, AI canvas, objective specification
Related Concepts: Reward function engineering (Ch.9)
```

```
CARD ID: B04-C15-05
Title: "What is our real objective, anyway?"
Type: Insight
Summary: The AI canvas exercise often surfaces that an organization's real difficulty in deploying AI is not technical but the prior, harder problem of specifying a genuinely precise objective — even seemingly clear goals like profit maximization are ambiguous once a time horizon is required.
Source: Book p.164 (Key Points)
Tags: objective specification, organizational strategy, AI adoption
Related Concepts: The AI Canvas, reward function engineering (Ch.9)
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: Current AI tools deliver only a single predictive component within a decision, not an entire workflow, so evaluating or building an AI tool requires decomposing the target decision into its full set of constituent elements; the authors formalize this as the "AI canvas" (seven boxes derived from the Ch.8 anatomy of a decision) and show, via the Atomwise and MBA-recruiting worked examples, that the exercise often reveals the real bottleneck is not data or algorithms but the organization's failure to have specified a sufficiently precise objective.
Top 5 Concepts: (1) AI tools as predictive components rather than full workflows. (2) The AI Canvas (Prediction, Judgment, Action, Outcome, Input, Training, Feedback). (3) The prior problem of specifying the objective ("what is our real objective, anyway?"). (4) Judgment as context-dependent error-cost weighting (chemotherapy vs. acne cream). (5) Vague mission statements as a structural obstacle to AI deployment.
Top 3 Claims: (1) None of the chapter's six named AI products perform a full workflow — each is a single predictive component. (2) Atomwise's tool dramatically lowers cost/accelerates the molecule-screening task but leaves testing/verification to human-machine collaboration. (3) Many organizations' mission statements are too vague or multifaceted to specify a usable AI prediction target without first resolving genuine strategic trade-offs.
Top 3 Cases: (1) Atomwise's binding-affinity prediction tool and its fully filled-out AI canvas. (2) The hypothetical MBA-recruiting AI canvas (top-50-alumni prediction). (3) The business-school "best students" mission-statement ambiguity example.
Top 3 Studies: None formally cited as independent academic studies in this chapter — evidence is drawn from a named-company case study (Atomwise, with a named-CEO quote and dated data figure) and a fully worked hypothetical (MBA recruiting) rather than cited research.
Most Unique Idea: Explicitly deriving the AI canvas's seven boxes from the book's own earlier anatomy-of-a-decision framework (Ch.8), giving a practical planning tool theoretical grounding within the book's own argument rather than presenting it as a freestanding consulting template.
Most Counterintuitive Idea: The hardest part of building an AI tool is often not technical at all — it's the organizational work of answering "what is our real objective, anyway?", a question the organization may never have needed to answer with precision before.
Biggest Weakness or Open Question: The chapter treats sharpening a vague mission statement as an achievable first step in AI strategy without addressing what happens when an organization's ambiguity is a deliberately preserved balance of competing stakeholder interests rather than a solvable specification gap.
Best Content Opportunity: "The 7-Box Canvas That Decides Whether Your AI Idea Actually Works" (Section 17) — a concrete, reusable planning template demonstrated on a vivid biotech case, directly actionable for any viewer evaluating their own AI project idea.
```
