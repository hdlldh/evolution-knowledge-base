# Prediction Machines — Chapter 10: Predicting Judgment
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Extraction
**Source:** Book pages 107–114 (PDF pages 120–127)
**Date:** 2026-08-04
**Revised:** Per Chapter_10_Audit.md — added the concrete list of strategic "never done it before" business decisions and sharpened the "behavior changes because of the decision" mechanism.

BOOK:
Prediction Machines: The Simple Economics of Artificial Intelligence

AUTHOR:
Ajay Agrawal, Joshua Gans, Avi Goldfarb

CHAPTER:
10 — Predicting Judgment

---

## 1. Chapter Thesis

The line between "prediction" and "judgment" is not as fixed as earlier chapters might suggest: because judgment itself is expressed through repeated human decisions, and because AI is fundamentally good at learning patterns from repeated examples, machines can often learn to *predict human judgment* by training on data about the inputs humans received and the decisions they made in response — the underlying prediction problem becomes "given this input, what would a human do?" This doesn't eliminate the human role, but it does mean prediction can encroach into territory previously assumed to require ongoing human involvement. Still, humans retain durable advantages in three specific circumstances: where machines lack the sensory, preference-revealing, or privacy-restricted data needed to learn judgment at all; where the relevant events are too rare for a machine to have learned from enough examples (rare events, "unknown unknowns"); and where humans can substitute a *model* of the underlying process (rather than raw historical data) to make good decisions even absent sufficient data — a distinctly human capability illustrated by Abraham Wald's WWII bomber-armor analysis.

## 2. Key Concepts

```
Concept Name: Predicting human judgment ("What would a human do?")
Definition: The idea that judgment itself can become a target for prediction — instead of (or alongside) predicting an external world state, a machine can be trained on paired data (inputs a human received, and the decision the human made in response) to predict what a human would decide given a new input, effectively learning to imitate/automate the judgment step, not just the prediction step, of a decision.
Why It Matters: This reframes the human/machine boundary established in Ch.8–9: judgment was previously treated as an irreducibly human capability that machines merely receive predictions to serve, but this chapter shows judgment itself can be learned by a machine wherever there is enough repeated example data — raising the question (posed directly) of whether AI could eventually predict human judgment well enough to circumvent the need for humans altogether.
How the Author Uses It: Introduced via Waymo's self-driving cars (which must learn not just how to reach a destination, but how to brake/drive in ways comfortable for passengers — an aspect of human judgment about ride comfort that is impractical to hand-code for every situation, so instead the system is trained to predict "what would a human do in this situation?"), then generalized: "In any environment where humans make decisions over and over again and we are able to collect data about the data they receive and the decisions they make in response, we will likely be able to automate those decisions by rewarding the prediction machine for predicting: What would a human do?"
Related Concepts: Hard-coding judgment (Ch.9), reward function engineering, Grammarly and Lola cases
```

```
Concept Name: Machine limits in predicting judgment — describable vs. subtle preferences
Definition: A distinction between judgment criteria that are explicit/describable (and therefore learnable by a machine relatively easily) and subtler human preferences that are harder to articulate or anticipate, which a machine can still learn — but only from enough observed examples, and sometimes only by uncovering criteria the human experts themselves couldn't describe in advance.
Why It Matters: Refines the "machines can predict judgment" claim with an important nuance: ease of learning depends on whether the judgment criteria are the kind that can be made explicit, and machines may in some cases uncover implicit human decision criteria (tacit knowledge, per Ch.9's McAfee/Brynjolfsson quote) that the human experts themselves never articulated.
How the Author Uses It: Illustrated by Lola, a travel-booking AI startup, whose AI found it easy to apply judgment on describable criteria (hotel availability, price) but initially couldn't match a human travel agent's tacit expertise (e.g., knowing to book a breakfast reservation inside Disney World before gates open, to secure an unobstructed photo op at Cinderella Castle) — yet the chapter notes Lola's AI *did* eventually uncover decision patterns human agents made but couldn't describe in advance, such as preferences for modern hotels or corner-location hotels.
Related Concepts: Predicting human judgment, tacit knowledge (Ch.9), human trainers
```

```
Concept Name: Human trainers (supervising AI toward eventual unnecessary correction)
Definition: The practice of having a human supervise an AI's judgment-prediction performance during a transitional period, correcting its mistakes, so the AI can learn from those corrections until it becomes good enough that human correction is no longer needed — particularly important when automating a process with very little tolerance for error.
Why It Matters: Describes the realistic operational pathway by which "machines learn to predict judgment" actually happens in practice — not a single training event, but an ongoing human-in-the-loop correction process with a defined (if implicit) endpoint where humans become unnecessary for that specific aspect of the task.
How the Author Uses It: Presented as a general principle following the Lola/Grammarly discussion, without a single fully worked example, but implicitly connecting to both cases' descriptions of learning from corpora of human-corrected work (Grammarly) and accepted/rejected suggestions (Grammarly) or observed agent bookings (Lola).
Related Concepts: Predicting human judgment, prediction by exception (Ch.7)
```

```
Concept Name: Three types of data humans have that machines don't (yet)
Definition: A taxonomy of three specific data advantages that currently keep humans relevant even as machines improve at predicting judgment: (1) human senses — human eyes, ears, nose, and skin still surpass machine sensory capability in many ways; (2) humans as the ultimate arbiters of their own preferences — consumer preference data is valuable precisely because only humans can reveal it, which is why businesses invest heavily (loyalty card discounts, free services in exchange for data) to extract it; (3) privacy-restricted data — as long as people keep certain categories of information (sexual activity, financial situation, mental health status, "repugnant thoughts") to themselves, machines will lack sufficient data to predict behavior in those domains, leaving room for human judgment grounded in interpersonal understanding that doesn't require the same explicit data.
Why It Matters: Provides a concrete, three-part answer to "will humans be pushed out?" — grounding the abstract claim that "humans are a resource" in specific, actionable categories of comparative advantage that hiring/organizational decisions can be built around.
How the Author Uses It: Directly answers the chapter's "Will Humans Be Pushed Out?" section heading; each of the three data types is given its own brief supporting example (loyalty cards; Google/Facebook's free-services-for-data model; the privacy-protected categories list).
Related Concepts: Prediction relies on data, privacy trade-offs (previewed for Part Four discussion)
```

```
Concept Name: Prediction with little data (rare events revisited)
Definition: A second durable limit on machines' ability to predict judgment: machines require enough observed examples to learn a pattern, so events that are inherently rare (or entirely novel) leave machines with insufficient data to predict either the event itself or the judgment a human would apply to it — directly building on Chapter 7's "known unknowns" (rare, foreseeably-hard-to-predict events like elections/earthquakes) and "unknown unknowns" (genuinely unprecedented events).
Why It Matters: Establishes that predicting judgment is subject to the same fundamental data-availability constraint as predicting any other outcome — a machine cannot predict "what a human would do" in a situation type it has never observed a human actually facing, no matter how sophisticated its pattern-matching becomes.
How the Author Uses It: Explicitly cross-references Ch.7's known unknowns/unknown unknowns framework, restates that humans remain comparatively good at prediction with little data (e.g., recognizing faces even as people age, an example reused from Ch.7), and extends the point to strategic business decisions: a company facing a genuinely new technology (the internet, bioengineering, or AI itself) cannot be well-predicted by a machine because there's no relevantly similar precedent in the data, whereas humans can reason by analogy across different contexts. The chapter grounds this further with everyday-but-unprecedented corporate decisions: should you add a new product to a product line, merge with a competitor, or acquire an innovative startup or channel partner? The sharper mechanism at work is not merely that these events are rare, but that people's behavior will change specifically *because* of the contemplated decision — so past behavior stops being a useful guide for future behavior, leaving the prediction machine without relevant data.
Related Concepts: Known knowns/unknowns taxonomy (Ch.7), unknown knowns and the book-reading counterfactual (Ch.7 callback)
```

```
Concept Name: Experiments vs. modeling as human (and sometimes machine) solutions to insufficient data
Definition: Two distinct strategies for making good decisions when you lack sufficient natural/historical data to predict an outcome or the judgment underlying it: (1) experiments — deliberately generating new data by randomly assigning different conditions (e.g., a randomized controlled trial) and observing outcomes, usable by both humans and (when the situation recurs often enough) machines; (2) modeling — building a deep, structural understanding of the process that generated observed data, allowing inference about missing or counterfactual data without needing to observe it directly, particularly valuable when experiments are impossible or too costly.
Why It Matters: Provides two complementary human (and partly machine-usable) tools for overcoming the "prediction with little data" limitation just described — showing that data scarcity doesn't always mean decision paralysis, but does typically require either investing in new data generation (experiments) or investing in structural understanding (modeling), both of which currently draw more on distinctly human skills, especially for one-off or high-stakes situations.
How the Author Uses It: The book-recommendation counterfactual example from Ch.7 is revisited to introduce the RCT/experiment concept concretely (randomly assigning some readers to a "treatment" of reading the book, others to a "control" of not reading it, then comparing how each group applies AI in their work); modeling is then introduced via the ZipRecruiter pricing case (revisited from Ch.9) and, most vividly, via Abraham Wald's WWII bomber-armor case (Section 7).
Related Concepts: Randomized controlled trial (Ch.7's Colombian bank case), the counterfactual (Ch.7), Abraham Wald's bomber case, human reward function engineers
```

## 3. Key Claims

```
Claim: In any domain where humans repeatedly make decisions and data can be collected on both the inputs they received and the decisions they made, it is likely possible to automate those decisions by training a prediction machine to predict "what would a human do?" — driving is not a unique or special case.
Type: Theoretical/Interpretive
Evidence Provided: The Waymo self-driving case (learning comfortable braking behavior by predicting human driving responses rather than hand-coding rules for every scenario), generalized to a broader principle.
Strength of Support: Moderate — the driving example is well-developed and plausible, but the generalized claim ("in any environment...") is asserted as a broad principle rather than independently tested across multiple additional domains within this chapter.
```

```
Claim: Grammarly successfully predicts what a human editor would do — going beyond mechanical grammar-rule application to assess whether deviations from "perfect" grammar are actually preferred by human readers — by learning from two data sources: a corpus of documents corrected by skilled editors, and feedback from users who accepted or rejected its suggestions.
Type: Empirical
Evidence Provided: A specific, checkable illustrative example (the chapter runs one of its own preceding sentences through Grammarly, which flags "It's" (should be "Its") and "grammer" (misspelled) and notes "main" is often overused); description of Grammarly's founding (2009, by Alex Shevchenko and Max Lytvyn) and its dual training method.
Strength of Support: Strong for the illustrative mechanism (a concrete, reader-verifiable example), though no quantified accuracy/adoption metrics are given for Grammarly's overall performance.
```

```
Claim: Lola's AI, automating travel-booking judgment, could easily replicate judgment on describable criteria (hotel availability, price) but could not initially match a human travel agent's deeper, tacit expertise for family vacation bookings — though the AI could, over time, uncover decision patterns human agents themselves could not articulate in advance.
Type: Empirical
Evidence Provided: A direct quote from New York Times reporting: the AI "couldn't match the expertise of, for example, a human agent with years of experience booking family vacations to Disney World. The human can be more nimble—knowing, for instance, to advise a family that hopes to score an unobstructed photo with the children in front of the Cinderella Castle that they should book a breakfast reservation inside the park, before the gates open"; the chapter's own follow-up observation that Lola's AI did uncover otherwise-inarticulable agent preferences (e.g., for modern hotels, or hotels on a street corner).
Strength of Support: Strong for the specific reported example (attributed to named founders' company and a major news outlet), though the "eventually uncovered" claim about implicit criteria is asserted with only two brief examples (modern hotels, corner-location hotels) rather than systematic evidence.
```

```
Claim: Humans retain a durable data-based advantage over machines in predicting judgment via three specific mechanisms: superior sensory capability (sight, hearing, smell, touch), being the sole direct source of true preference data, and privacy norms that withhold entire categories of behaviorally-relevant data (sexual activity, finances, mental health, unacceptable thoughts) from machines.
Type: Theoretical/Interpretive
Evidence Provided: Illustrative, unquantified examples for each category (loyalty card discounts and free Google/Facebook services as mechanisms for extracting preference data; the privacy-protected categories listed by name).
Strength of Support: Moderate — a plausible, well-organized taxonomy, but presented via illustrative reasoning rather than data/studies quantifying the actual size or durability of each advantage.
```

```
Claim: Machines will remain poor at predicting judgment for rare events and genuinely novel situations (extending Ch.7's known unknowns/unknown unknowns categories), including strategic business decisions like how to respond to a new technology, because there is no sufficiently similar historical precedent in the data for the machine to learn from, whereas humans can reason by analogy across superficially different contexts.
Type: Theoretical
Evidence Provided: Restated cross-reference to Ch.7's taxonomy; the human face-recognition-despite-aging example (reused from Ch.7); the assertion that a company facing internet, bioengineering, or AI-driven disruption cannot be well-served by machine prediction of appropriate strategic judgment.
Strength of Support: Moderate — logically consistent with the established known-unknowns/unknown-unknowns framework, but this specific chapter doesn't add new independent evidence beyond restating and extending the Ch.7 argument.
```

```
Claim: Abraham Wald's WWII analysis of returning bomber damage patterns — correctly recommending armor be added where bullet holes were *not* found on returning planes, rather than where they were found — required a structural model of the underlying data-generating process (which planes survive to be observed) that neither raw data alone nor a prediction machine (then or, per the authors, for the foreseeable future) could have produced.
Type: Historical/Empirical (a specific, well-documented historical episode)
Evidence Provided: The described reasoning: engineers wanted to add armor without compromising performance, but couldn't determine where via costly/fatal experimentation; statistician Abraham Wald was consulted; he recognized the observed bullet-hole data was systematically biased because it excluded bombers that did not return (destroyed by hits in the unobserved, presumably fatal locations); air force engineers accordingly increased armor in the locations *without* observed bullet holes, improving survival, cited to endnote 3.
Strength of Support: Strong — a specific, well-documented historical case (widely known in statistics as a canonical survivorship-bias example) with a clear causal mechanism and outcome, attributed to a named, credentialed historical figure.
```

```
Claim: Wald's insight required understanding the process that generated the (missing) data — a kind of reasoning the chapter asserts is "beyond the abilities of prediction machines" for the foreseeable future, especially when the relevant problem has no prior historical examples to draw from (as WWII bomber survivability had none).
Type: Interpretive
Evidence Provided: Direct assertion following the Wald case, framed as a durable, structural limitation rather than a temporary technological gap.
Strength of Support: Moderate — a strong claim about the foreseeable future capabilities of prediction machines, asserted with conviction but without independent technical evidence establishing why such reasoning is structurally impossible (versus merely difficult) for current or near-future AI.
```

## 4. Frameworks, Models, and Mental Models

```
Name: "What would a human do?" as a general-purpose training objective
Description: A reframing of many automation problems: instead of trying to directly hand-specify correct behavior for every situation, collect paired data on (a) the inputs a human decision-maker received and (b) the decision the human made, and train a prediction machine to predict (b) given (a) — effectively converting judgment-automation into a standard supervised-prediction problem.
Components: A repeated human decision process; collectible input data; collectible outcome data (the human's actual decision); a prediction machine trained to map input to human-decision-output.
How It Works: Applies wherever decisions are made "over and over again" with observable inputs and outputs — the machine doesn't need explicit rules, only enough paired examples to learn the input-to-judgment mapping, exactly as it would learn any other prediction task.
When It Is Useful: As a general template for identifying automation opportunities in judgment-heavy tasks, distinct from and complementary to the earlier "hard-coding judgment" (Ch.9) approach — this approach lets the machine learn judgment from examples rather than requiring a human to explicitly articulate the reward function in advance.
Limitations: Only works where (a) the decision recurs frequently enough to generate sufficient training data, (b) the relevant inputs and human decisions can actually be captured as data, and (c) the human judgment being predicted isn't dependent on data types machines structurally lack access to (sensory, preference-revealing, or privacy-protected data) — limitations developed in the chapter's subsequent sections.
```

```
Name: Experiments vs. modeling (as the two-part toolkit for insufficient-data situations)
Description: A framework distinguishing two different strategies for making good decisions or predictions when historical/observational data is insufficient, differing in whether they generate new data (experiments) or extract more from existing/limited data via structural understanding (modeling).
Components: Experiments — random assignment to treatment/control conditions, observed outcome comparison; requires a situation that recurs often enough to be worth designing and running a trial for. Modeling — a theoretically-grounded understanding of the data-generating process, allowing correct inference (e.g., about unobserved counterfactuals or systematically missing data) without directly observing every relevant case.
How It Works: Experiments are illustrated via the book-recommendation RCT concept and are explicitly noted to be usable by machines too once a situation recurs often enough (the chapter connects this to why machines already outperform humans at various video games, via self-play/experimentation). Modeling is illustrated via ZipRecruiter's need to model longer-term profit-maximization objectives beyond what its price experiment alone could reveal, and — most dramatically — via Wald's bomber-armor analysis, where the "missing" (non-returning) bombers had to be reasoned about structurally since they could never be directly observed.
When It Is Useful: Experiments are best when a decision/situation is repeatable and testable; modeling is essential specifically when experimentation is impossible (situation too rare) or too costly (as with WWII bomber survivability, where "experimentation" would mean losing pilots).
Limitations: The chapter explicitly frames modeling skill as requiring deep training (citing economics PhD programs and MBA curricula, including ones the authors developed at the University of Toronto) and flags that without such skill, decision-makers risk falling into the "unknown knowns" trap (Ch.7) — mistaking a prediction machine's pattern-matching output for genuine causal understanding when the underlying data-generating process (including selection effects like Wald's survivorship bias) isn't properly modeled.
```

## 5. Research and Evidence

None identified as formally cited academic studies within this chapter — the chapter's evidence consists of real-company cases (Waymo, Grammarly, Lola, ZipRecruiter) and a historical episode (Wald's WWII analysis) rather than academic research citations (beyond passing endnote references not detailed in the visible text).

## 6. Experiments

```
Experiment Name: The hypothetical book-recommendation randomized controlled trial (revisited from Ch.7)
Setup: A hypothetical RCT design proposed to resolve the causal question (does reading this book actually cause better AI management?) left unresolved in Chapter 7's self-referential example.
Participants: Hypothetical readers, randomly assigned to treatment or control groups.
Procedure: Assign some people to a "treatment" group (force them to read the book, possibly with a consequential exam to ensure engagement) and others to a "control" group (prevent them from reading it, or at least don't advertise it to them); wait and collect data on how each group applies AI in their work; compare the two groups.
Result: Not actually run in the chapter — presented as a hypothetical design to illustrate the experimental method, not as reported findings.
Interpretation: The difference between treatment and control group outcomes would represent the causal effect of reading the book, addressing the counterfactual problem (what would have happened without reading it) that raw observational/correlational data cannot resolve.
What It Demonstrates: How randomized experiments solve the counterfactual/causal-inference problem introduced in Ch.7, and that such experiments are "very powerful" — used to justify high-stakes decisions like new medical treatment approvals and widely relied upon by data-driven companies (Google to Capital One, named as examples).
Potential Alternative Explanation: Not applicable — this is a hypothetical illustrative design, not an actual reported experiment with results to critique.
```

## 7. Cases and Stories

```
Case Title: Waymo's self-driving cars and passenger-comfortable braking
People / Organization: Waymo (Google subsidiary)
Context: Opens the chapter as the primary illustration of "predicting judgment" via the "what would a human do?" training objective.
What Happened: Waymo successfully tested automated point-to-point transportation, but driving also requires managing effects on passengers that are much harder to observe directly than the mechanics of navigation — e.g., braking in a manner comfortable for others in the car, a skill new human drivers must also learn. Because there are thousands of related micro-decisions involved in driving, it's impractical to hand-code judgment for every possible situation; instead, Waymo trains its systems on many examples to learn to predict human judgment ("What would a human do in this situation?").
Outcome: Used to launch the chapter's general claim that any domain with repeated human decisions and observable input/outcome data can likely have those decisions automated the same way.
Concept Illustrated: Predicting judgment as an alternative to hard-coding it, specifically for judgment involving hard-to-observe effects (passenger comfort) rather than easily-specified objectives (reaching a destination).
Why This Case Is Useful: A high-profile, real, technically sophisticated example that makes an abstract "predicting judgment" concept concrete via a widely-recognized company and product category.
Potential for Reuse: High
```

```
Case Title: Grammarly and predicting editorial judgment
People / Organization: Grammarly; founders Alex Shevchenko and Max Lytvyn (founded 2009)
Context: The chapter's second major illustration of predicting judgment, in a text-editing rather than physical-driving domain.
What Happened: Grammarly pioneered using machine learning to improve formal written composition, focused mainly on grammar and spelling. It achieves this by learning from two sources: a corpus of documents corrected by skilled editors, and feedback from users who accepted or rejected its own suggestions — in both cases, predicting what a human editor would do. It goes beyond mechanical rule application to assess whether deviations from strict grammatical correctness are actually preferred by human readers (implying some "errors" may be stylistically preferable, and Grammarly learns this preference too, not just the rules).
Outcome: The chapter demonstrates this directly by running one of its own preceding sentences through Grammarly, which correctly flags a contraction error ("It's" should be "Its") and a spelling error ("grammer" should be "grammar"), and separately flags stylistic overuse of the word "main."
Concept Illustrated: Predicting judgment via dual training sources (expert-corrected corpus + user accept/reject feedback), and going beyond rule-based correctness to predict actual human/reader preference.
Why This Case Is Useful: An immediately verifiable, self-demonstrating example (readers can test Grammarly themselves) that makes the "predicting judgment beyond mechanical rules" concept concrete and checkable.
Potential for Reuse: High
```

```
Case Title: Lola and the limits of predicting travel-booking judgment
People / Organization: Lola (travel-booking automation startup); The New York Times (quoted reporting)
Context: The chapter's central cautionary/nuancing case, showing where predicting judgment currently falls short of expert human tacit knowledge — while also showing the machine can eventually surface implicit criteria.
What Happened: Lola's AI automates hotel booking by finding good options based on describable criteria (availability, price) but, per New York Times reporting, initially couldn't match a human agent's expertise — such as knowing to book a breakfast reservation inside Disney World before gates open, specifically to help a family secure an unobstructed photo with children in front of Cinderella Castle. However, Lola's AI did eventually uncover decision patterns that human agents had actually been applying but couldn't describe in advance, such as preferences for modern hotels or corner-location hotels.
Outcome: Frames the central open question for AI-judgment-prediction deployments: how many observations does a prediction machine need to learn subtler, harder-to-articulate criteria, beyond the easily describable ones it picks up quickly?
Concept Illustrated: The gradient between easily-describable judgment criteria (fast to learn) and subtle/tacit judgment criteria (slow to learn, but not necessarily unlearnable, and sometimes literally inarticulable even by the human experts being imitated).
Why This Case Is Useful: A nuanced, honest case (not simply "AI succeeds" or "AI fails") that captures the genuine complexity of predicting judgment, paired with a vivid, specific, emotionally resonant example (a family photo op at Disney World) that makes the abstract "tacit expertise" concept concrete.
Potential for Reuse: High
```

```
Case Title: Abraham Wald and WWII bomber survivorship bias
People / Organization: Abraham Wald (statistician); Allied air force engineers; WWII bombing raids over Germany
Context: The chapter's central, most vivid illustration of "modeling" as a distinctly human tool for reasoning about data that is structurally missing (not just rare).
What Happened: Allied engineers wanted to add armor to bombers without compromising performance, requiring them to determine exactly where to add weight. Direct experimentation was possible in principle but far too costly (pilots would die). Engineers observed bullet-hole damage patterns on bombers that *returned* from raids over Germany and initially assumed these hit locations were the ones needing more armor. Statistician Abraham Wald was consulted and, after careful mathematical reasoning, recommended the opposite: armor the areas *without* observed bullet holes. His insight was that the data was systematically censored — some bombers never returned at all, and Wald reasoned these missing bombers had likely been hit in the locations that (unlike the survivors' hit locations) proved fatal. Air force engineers implemented Wald's recommendation, increasing armor in the bullet-hole-free zones, improving aircraft survival.
Outcome: A now-canonical example (in statistics generally, though the chapter doesn't note its broader fame) of solving a survivorship-bias problem through structural reasoning about a data-generating and data-censoring process, rather than through observed data patterns taken at face value.
Concept Illustrated: Modeling as a way to correctly interpret (and correct for systematic bias in) available data by reasoning about the process that produced it — including reasoning about data that is structurally absent (destroyed bombers) rather than merely statistically rare.
Why This Case Is Useful: An exceptionally famous, well-documented, high-stakes historical case that makes an abstract statistical concept (selection/survivorship bias, and the value of structural modeling over naive pattern-matching) vivid, memorable, and immediately transferable to business/data contexts.
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: Machines predicting judgment via "what would a human do?"
Example: Waymo training its self-driving system to predict comfortable braking behavior by learning from human driving examples, rather than hand-coding rules for every scenario.
Why It Works: A widely-recognized, high-stakes technology (self-driving cars) that makes an abstract training-objective reframing concrete and immediately understandable.
Possible Alternative Domain: AI, Everyday Life
```

```
Concept: The gap between easily-describable and tacit judgment criteria
Example: Lola's AI easily handling hotel price/availability but initially missing a human agent's Disney World Cinderella Castle photo-op trick.
Why It Works: A specific, vivid, emotionally resonant scenario (a family photo moment) that makes an abstract "tacit expertise" concept concrete and memorable, while honestly acknowledging AI's current limitation rather than overselling its capability.
Possible Alternative Domain: Business, Everyday Life
```

```
Concept: Modeling as a way to reason about structurally missing data
Example: Abraham Wald recommending armor be added where bullet holes were absent, not present, on returning WWII bombers.
Why It Works: A dramatic, high-stakes, well-documented historical case with a genuinely counterintuitive conclusion that makes survivorship bias and structural data modeling unforgettable.
Possible Alternative Domain: Mathematics, History, Business (survivorship bias appears constantly in business analytics, e.g., studying only surviving companies/products)
```

## 9. Counterintuitive Insights

```
Insight: The right response to bullet-hole damage data on returning WWII bombers was to armor the places *without* visible damage, not the places with it — because the planes hit in those undamaged-looking areas' true danger zones never made it back to be observed at all.
Common Belief: You should reinforce the areas where damage is actually observed, since that's where the evidence shows planes get hit.
Author's Argument: The observed data was systematically biased by a selection/censoring process (only surviving bombers could be observed), so naively acting on the visible pattern would have been actively counterproductive; correct action required modeling the unobserved, "missing" data (destroyed bombers) structurally.
Evidence: Abraham Wald's WWII bomber-armor analysis and its real-world implementation and outcome.
Why It Is Surprising: It inverts the intuitive, seemingly "data-driven" conclusion (protect where damage is seen) in favor of a conclusion that requires reasoning about what's systematically *absent* from the data — a lesson the chapter explicitly says remains "beyond the abilities of prediction machines" for the foreseeable future.
```

```
Insight: A machine can sometimes uncover and articulate implicit human decision criteria that the human experts themselves were never able to describe in advance (e.g., Lola's AI surfacing travel agents' unstated preferences for modern or corner-location hotels).
Common Belief: If a human expert can't explain why they make a certain choice, that judgment must be too tacit/subtle for a machine to ever learn or replicate.
Author's Argument: Given enough paired input-decision data, a machine's pattern-matching can sometimes detect a real, consistent criterion in human behavior even when the humans exhibiting that behavior couldn't articulate it themselves — meaning tacit knowledge is not always a hard boundary against machine learning, only against explicit hard-coding (Ch.9's McAfee/Brynjolfsson limitation applies to codification, not necessarily to learned prediction).
Evidence: The Lola case's specific mention of uncovering agent preferences for modern hotels and corner-location hotels that agents "were unable to describe in advance."
Why It Is Surprising: It suggests machine learning can, in some cases, exceed human self-knowledge about one's own decision criteria — a machine may "know" why a human expert does something better than the expert can explain it themselves.
```

## 10. Unique or Unusual Ideas

```
Idea: Treating "judgment" itself, not just external world states, as a legitimate target of prediction — effectively collapsing part of the prediction/judgment distinction the book spent Chapters 8–9 carefully establishing, by showing judgment can itself be learned as a pattern from paired input-decision data.
Why It Seems Unique: Most of the book's framework (Ch.8–9) treats prediction and judgment as cleanly separable, complementary inputs to decision-making, with judgment durably reserved for humans; this chapter introduces a meaningful complication — judgment is durably human only where data constraints (sensory, preference, privacy, rarity) prevent a machine from learning it, not as a matter of principle.
Potential Connection to Other Topics: Imitation learning and behavioral cloning in machine learning; the philosophical question of whether learned imitation of judgment constitutes "real" judgment.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: This chapter's opening claim ("in any environment where humans make decisions over and over again... we will likely be able to automate those decisions") sits in tension with Chapters 8–9's framing of judgment as the durable, distinctly human complement to prediction — this chapter narrows that durability claim considerably, restricting genuinely durable human judgment to only three data-based circumstances (sensory/preference/privacy data) plus rare-event situations, which is a substantially more limited scope than a casual reading of Ch.8–9 alone might suggest.
Author's Position: The chapter does directly ask "Will Humans Be Pushed Out?" and answers "we don't think so," but its own supporting reasoning (three specific, potentially erodable data advantages, e.g., as sensors improve or privacy norms shift) doesn't fully guarantee permanence — the chapter's own logic suggests these advantages could, in principle, narrow over time as sensor technology and data-sharing norms change.
Possible Counterargument: A skeptical reader might note that all three of the "durable" human data advantages (sensory capability, revealed preferences, privacy-protected data) are targets of active technological and business investment (better sensors, more consumer data extraction, evolving privacy norms/regulations) — meaning today's durable advantages might not remain durable indefinitely, a possibility the chapter doesn't explicitly address or hedge against.
What Evidence Would Help Resolve It: Later chapters on AI risk (Ch.20) and societal impact (Ch.21) may address the privacy dimension specifically (already flagged as a recurring theme since Ch.1's "trade-offs" framing) — worth checking whether they revisit this chapter's assumption of durable privacy-based limits.
```

## 12. Quotable Ideas

```
Paraphrase (short): In any environment where humans make decisions over and over again, and we can collect data about the inputs they receive and the decisions they make, we will likely be able to automate those decisions by training a prediction machine to predict: What would a human do?
Why the Idea Matters: The chapter's central, most generalizable claim, reframing judgment itself as learnable rather than durably exclusive to humans.
Source Location: Book p.107
```

```
Paraphrase (short): The human can be more nimble—knowing, for instance, to advise a family that hopes to score an unobstructed photo with the children in front of the Cinderella Castle that they should book a breakfast reservation inside the park, before the gates open.
Why the Idea Matters: A vivid, specific, quotable illustration (from an outside news source) of tacit human expertise that AI initially couldn't match.
Source Location: Book p.108, quoting The New York Times on Lola
```

```
Paraphrase (short): Wald had a good model of the process that generated the data about bullet holes — he recognized that some bombers did not come back from the raids, and conjectured that these bombers got hit in places that were fatal.
Why the Idea Matters: Crystallizes the chapter's central "modeling beats naive data-reading" lesson in a single memorable historical anecdote.
Source Location: Book p.112
```

## 13. Psychology Connections

None identified directly — the chapter's content is primarily technical/economic (data availability, modeling) rather than psychological, though the Lola case's discussion of "tacit expertise" connects loosely to the psychology of expert intuition discussed more directly elsewhere in the book (Ch.7's Kahneman/Tversky material).

## 14. Mathematics and Decision Science Connections

```
Connection: Abraham Wald's survivorship-bias analysis is a foundational, widely-cited example in statistics and probability of selection bias / censored data, directly relevant to any decision science course covering sampling bias.
Connection: The experiments-vs-modeling framework directly parallels the classic methodological distinction in econometrics and causal inference between experimental identification (RCTs) and structural/theoretical modeling (used when RCTs are infeasible), a core theme in applied microeconomics.
Connection: The randomized controlled trial design revisited from Ch.7 (treatment/control groups, counterfactual reasoning) is reinforced here as a general-purpose tool, explicitly extended to note that machines too can run/benefit from experiments once a situation recurs often enough (connected to why AI outperforms humans in various video games via self-play).
```

## 15. Sports Connections

None identified in the chapter's direct examples; no forced inference added. (The chapter references "various video games" in the context of machine experimentation/self-play, but this is treated as an AI/computing example, not a sports connection.)

## 16. AI and Machine Learning Connections

```
Direct examples from the book: Waymo's self-driving cars (predicting comfortable driving/braking judgment); Grammarly (predicting editorial judgment via expert-corpus training and user feedback); Lola (predicting travel-booking judgment, with partial success and partial limitation); machines outperforming humans in video games via self-play/experimentation (mentioned briefly as evidence machines can run experiments too).
Inferred connection (my own): The "what would a human do?" training objective described in this chapter is a plain-language description of imitation learning / behavioral cloning in machine learning (training a model to replicate demonstrated human behavior from paired state-action data) — the same underlying technique previewed in Chapter 2's autonomous-vehicle discussion, now explicitly generalized as a strategy for automating judgment specifically, not just perception/navigation prediction.
```

## 17. Content Creation Opportunities

```
Idea Title: "The AI That Learned What Your Editor Would Say"
Format: YouTube Short | Visual Explainer
Application Domain: AI | Everyday Life
Hidden Principle: Optimization
Story Hook (Layer 1): Run this sentence through Grammarly and watch it catch a typo, a grammar mistake, and even a style problem — without anyone programming grammar rules for "overused words."
Principle Framework (Layer 2): Machines can learn to predict human judgment (not just facts) by training on two things: expert-corrected examples and real user accept/reject feedback — a transferable pattern for any "quality" prediction problem.
Best Supporting Case: Grammarly (Section 7).
Character Application: Insight: Interpreter
Psychology Angle: None identified.
Math Angle: None identified.
Sports Angle: None identified.
Business Angle: A template for how SaaS products can automate quality judgments at scale.
Investing Angle: None identified.
History Angle: None identified.
AI Angle: Direct — dual-source training (corpus + feedback loop) for predicting judgment.
```

```
Idea Title: "Why the Statistician Told the Air Force to Armor the Spots With NO Bullet Holes"
Format: YouTube Long-form | YouTube Short
Application Domain: History | Mathematics | Business
Hidden Principle: Signal vs. Noise / Bayesian Thinking
Story Hook (Layer 1): WWII engineers looked at bullet holes on returning bombers and wanted to armor the damaged spots — a statistician told them they had it backwards.
Principle Framework (Layer 2): The data you can see is often systematically filtered by what survived to be observed — and the most important insight can be about what's structurally missing, not what's visibly present. A transferable lens for business "survivorship bias" (e.g., studying only successful companies/products).
Best Supporting Case: Abraham Wald's bomber case (Section 7).
Character Application: Sigma: Architect
Psychology Angle: None identified.
Math Angle: Direct — selection bias, censored data, structural modeling.
Sports Angle: None identified.
Business Angle: Direct — survivorship bias in studying "what successful companies do."
Investing Angle: Direct — survivorship bias in backtested trading strategies and fund performance data.
History Angle: Direct — WWII, a specific, dateable, well-documented episode.
AI Angle: Direct — the chapter's explicit claim that this kind of reasoning remains beyond current/near-future prediction machines.
```

```
Idea Title: "The Travel AI That Couldn't Get You a Cinderella Castle Photo (Yet)"
Format: YouTube Short | Community Post
Application Domain: AI | Business | Everyday Life
Hidden Principle: Optimization
Story Hook (Layer 1): An AI travel agent could find you the best hotel price in seconds — but it took a human to know you should book breakfast inside Disney World before the gates open.
Principle Framework (Layer 2): AI learns "describable" judgment fast (price, availability) but takes much longer to learn tacit expertise — and sometimes it can even surface expert knowledge the experts themselves never articulated.
Best Supporting Case: Lola (Section 7).
Character Application: Insight: Interpreter
Psychology Angle: Tacit knowledge and the limits of expert self-explanation.
Math Angle: None identified.
Sports Angle: None identified.
Business Angle: Direct — where to expect AI to succeed quickly vs. slowly in service automation.
Investing Angle: None identified.
History Angle: None identified.
AI Angle: Direct — the gradient between explicit and tacit judgment criteria in AI training.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B04-C10-01
Title: Predicting judgment via "what would a human do?"
Type: Concept
Summary: Wherever humans make repeated decisions and both their inputs and decisions can be captured as data, a prediction machine can often be trained to predict the human's judgment directly, automating decisions without needing explicit hard-coded rules — illustrated by Waymo learning comfortable braking behavior.
Source: Book p.107
Tags: judgment, prediction, automation, framework
Related Concepts: Hard-coding judgment (Ch.9), Grammarly, Lola
```

```
CARD ID: B04-C10-02
Title: Grammarly predicts editorial judgment
Type: Case
Summary: Grammarly learns to predict what a human editor would do — beyond mechanical grammar rules, including whether readers actually prefer certain "non-standard" phrasing — by training on an expert-corrected document corpus plus user accept/reject feedback on its own suggestions.
Source: Book p.108
Tags: AI, writing, predicting judgment, case
Related Concepts: Predicting judgment via paired input-decision data
```

```
CARD ID: B04-C10-03
Title: Lola — the gap between describable and tacit judgment
Type: Case
Summary: Lola's travel-booking AI easily matched human judgment on describable criteria (price, availability) but initially missed a human agent's tacit Disney World Cinderella Castle photo-op trick — though it eventually uncovered other agent preferences (modern/corner hotels) the agents themselves couldn't articulate in advance.
Source: Book p.108–109
Tags: AI, travel, tacit knowledge, case
Related Concepts: McAfee/Brynjolfsson tacit knowledge (Ch.9), human trainers
```

```
CARD ID: B04-C10-04
Title: Three types of data humans have that machines don't
Type: Model
Summary: Humans retain a data-based advantage over machines in predicting judgment via (1) superior sensory capability, (2) being the sole source of true revealed preferences, and (3) privacy norms withholding entire categories of behavior (sexual activity, finances, mental health) from machines.
Source: Book p.109–110
Tags: framework, human advantage, privacy, data
Related Concepts: Prediction relies on data (Ch.6)
```

```
CARD ID: B04-C10-05
Title: Prediction with little data — rare events and unknown unknowns revisited
Type: Concept
Summary: Machines remain poor at predicting judgment for rare or genuinely novel situations (extending Ch.7's known unknowns/unknown unknowns), including strategic decisions about new technologies, because there's no sufficiently similar historical data to learn from — while humans can reason by analogy.
Source: Book p.110
Tags: rare events, known unknowns, strategy, limits of AI
Related Concepts: Known knowns/unknowns taxonomy (Ch.7)
```

```
CARD ID: B04-C10-06
Title: Experiments vs. modeling for insufficient-data decisions
Type: Model
Summary: Two human (and partly machine-usable) strategies for deciding well without enough natural data: experiments (randomized trials generating new data, illustrated by a hypothetical book-reading RCT) and modeling (structural understanding of the data-generating process, illustrated by ZipRecruiter's pricing decision and Abraham Wald's bomber analysis).
Source: Book p.110–113
Tags: framework, experiments, modeling, RCT
Related Concepts: Randomized controlled trial (Ch.7), counterfactual (Ch.7)
```

```
CARD ID: B04-C10-07
Title: Abraham Wald and WWII bomber survivorship bias
Type: Case
Summary: Wald recommended armoring WWII bombers where bullet holes were absent (not present) on returning planes, reasoning that bombers hit in the unobserved fatal locations never returned to be counted — a canonical example of modeling a data-generating process to correct for systematic selection bias, a skill the chapter says remains beyond prediction machines.
Source: Book p.111–113
Tags: statistics, survivorship bias, history, WWII, modeling
Related Concepts: Experiments vs. modeling, unknown knowns (Ch.7)
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: The prediction/judgment boundary established in earlier chapters is not fixed — machines can often learn to predict human judgment itself by training on paired input-decision data ("what would a human do?"), as shown by Waymo, Grammarly, and (with important limits) Lola — but humans retain durable advantages in three specific data-constrained circumstances (sensory data, revealed preferences, privacy-protected data) and in rare/novel situations where machines lack sufficient examples, where distinctly human tools — experiments and especially structural modeling (as in Abraham Wald's WWII bomber analysis) — remain necessary.
Top 5 Concepts: (1) Predicting human judgment via "what would a human do?" (2) The gradient between easily-describable and tacit judgment criteria (Lola). (3) Three types of data humans have that machines don't (sensory, preference, privacy). (4) Prediction with little data — rare events and unknown unknowns revisited from Ch.7. (5) Experiments vs. modeling as the human toolkit for insufficient-data decisions.
Top 3 Claims: (1) Any repeated human decision with capturable input/outcome data can likely be automated by training a machine to predict human judgment. (2) Machines can sometimes uncover tacit human decision criteria the humans themselves couldn't articulate (Lola's hotel preferences). (3) Structural modeling (not raw data-reading) is required to correctly interpret systematically censored/missing data, as in Wald's bomber case — a capability the authors argue remains beyond prediction machines for the foreseeable future.
Top 3 Cases: (1) Abraham Wald's WWII bomber survivorship-bias analysis. (2) Lola's travel-booking AI and the Cinderella Castle photo-op example. (3) Waymo's self-driving cars learning comfortable braking via "what would a human do?"
Top 3 Studies: None formally cited as independent academic studies in this chapter — evidence is drawn from real-company cases and one historical episode (Wald) rather than cited research papers.
Most Unique Idea: Reframing judgment itself (not just external world states) as a legitimate, learnable target of machine prediction, meaningfully narrowing the "judgment is durably human" framing established in Ch.8–9.
Most Counterintuitive Idea: The correct response to WWII bomber damage data was to armor the areas with no observed bullet holes, not the areas that were hit — because the truly dangerous hit locations destroyed their bombers before they could be observed.
Biggest Weakness or Open Question: The chapter's three "durable" human data advantages (sensory, preference, privacy) are all potential targets of ongoing technological and business erosion (better sensors, more aggressive data extraction, shifting privacy norms), and the chapter doesn't address whether or how long these advantages might actually persist.
Best Content Opportunity: "Why the Statistician Told the Air Force to Armor the Spots With NO Bullet Holes" (Section 17) — an exceptionally vivid, high-stakes historical case that transfers cleanly to business analytics, investing, and general critical-thinking content about survivorship bias.
```
