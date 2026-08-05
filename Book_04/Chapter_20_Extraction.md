# Prediction Machines — Chapter 20: Managing AI Risk
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Extraction
**Source:** Book pages 221–232 (PDF pages 234–245)
**Date:** 2026-08-04
**Revised:** Per Chapter_20_Audit.md — corrected the Sweeney discovery narrative (a colleague found the ad first); added the diabetic/insulin risk example, the Nymi startup case, the "garbage in, garbage out" adage, the crash-vs-silent-manipulation distinction, the "attacks leave a trail" mitigation, and the short-term-benefit/long-term-risk nuance.

BOOK:
Prediction Machines: The Simple Economics of Artificial Intelligence

AUTHOR:
Ajay Agrawal, Joshua Gans, Avi Goldfarb

CHAPTER:
20 — Managing AI Risk

---

## 1. Chapter Thesis

Closing Part Four ("Strategy"), this chapter argues that deploying prediction machines carries several distinct, unavoidable categories of risk that business leaders must anticipate rather than hope to eliminate entirely: liability risk (AI can produce discriminatory outcomes — even unintentionally — that create real legal exposure), quality risk (AI trained only on correlational data can mistake spurious associations for causal ones, especially in "unknown known" situations where a confident prediction is simply wrong), and security risk (AI systems are vulnerable to manipulation through their input, training, and feedback data alike). Each risk type is illustrated through a real, often startling case — racially skewed Google ad results, gender-skewed Facebook job ads, eBay's overstated advertising ROI, adversarial video misclassification, Microsoft's reverse-engineering of Google search via its toolbar, and the Tay chatbot's rapid descent into racist speech — establishing that thoughtful human oversight, auditing, and anticipatory risk management remain essential complements to prediction, not optional afterthoughts.

## 2. Key Concepts

```
Concept Name: Algorithmic discrimination via quality-score optimization (not malicious intent)
Definition: The phenomenon in which an AI system produces racially or otherwise discriminatory outputs not because anyone programmed it to discriminate, but because its optimization target (e.g., an ad "quality score" that promotes ads more likely to be clicked) inadvertently amplifies pre-existing prejudices already present in aggregate human click behavior — meaning discrimination can emerge as an emergent statistical byproduct of a seemingly neutral objective function.
Why It Matters: Establishes that AI-driven discrimination doesn't require a discriminatory actor or intent — it can arise purely from the interaction between an optimization algorithm and biased real-world behavioral data, which is precisely what makes it hard to detect and easy to dismiss as "just what the data shows."
How the Author Uses It: Introduced via the Latanya Sweeney case (Google ads suggesting an arrest record appeared disproportionately for black-sounding names), with the authors walking through the specific hypothesized mechanism: if potential employers click arrest-suggesting ads more often for black-sounding names, the resulting higher "quality score" causes Google's algorithm to serve those ads even more, without any advertiser or Google engineer needing to intend racial targeting. The chapter makes a sharper related point using the Facebook case: showing STEM ads to men rather than women actually bolstered short-term operational performance (the ads shown to men cost less), meaning the discriminatory pattern looked like good business performance even as it accumulated strategic and legal risk that "may not become apparent until too late."
Related Concepts: Disparate impact, the AI black box problem
```

```
Concept Name: Disparate impact liability
Definition: A legal concept (distinct from disparate treatment, i.e., intentionally applying different standards to different groups) under which a facially neutral procedure or algorithm can still create legal liability if it systematically produces worse outcomes for a legally "protected class" — liability that attaches regardless of whether the discriminatory effect was intended.
Why It Matters: Establishes that a company cannot defend itself from discrimination liability merely by pointing out that its AI's decision process was neutral or automated — the legal standard cares about the pattern of outcomes, not the presence of discriminatory intent, meaning "the algorithm did it, not us" is not a viable legal defense.
How the Author Uses It: Explained via economist/lawyer Ben Edelman's framing of the Facebook STEM-ad gender-skew case, then grounded in a concrete precedent (the New York City Fire Department's $99 million settlement after a reading-comprehension-heavy entrance exam was found to have no relationship to job effectiveness but produced systematically worse outcomes for black and Hispanic applicants).
Related Concepts: Algorithmic discrimination via quality-score optimization, "AI neuroscience"
```

```
Concept Name: "AI neuroscience" — auditing a black-box model's discriminatory behavior
Definition: A term used by some in the computer science community for the practice of investigating why an opaque AI model (e.g., a deep learning system whose internal formula/algorithm cannot be directly inspected for what causes what) produces the outputs it does, by hypothesizing what might be driving observed differences, feeding the AI different input data specifically designed to test that hypothesis, and comparing the resulting predictions.
Why It Matters: Provides a concrete, actionable methodology for the otherwise paralyzing problem posed by AI's black-box nature — you don't need to be able to read an algorithm's internal logic to detect and diagnose its discriminatory behavior; you can probe it experimentally from the outside.
How the Author Uses It: Illustrated by exactly how economists Lambrecht and Tucker diagnosed the Facebook STEM-ad gender skew (discovering it stemmed from cost-per-impression economics, not click-through differences or discriminatory labor markets), presented as a template for how any organization should audit its own AI systems for discriminatory output.
Related Concepts: Disparate impact liability, algorithmic discrimination via quality-score optimization
```

```
Concept Name: Unknown knowns as a quality-risk failure mode
Definition: A specific and particularly dangerous type of AI quality risk (extending the known-unknowns/unknown-unknowns framework from Ch.7) in which a prediction machine outputs a confident, seemingly well-supported prediction that is nonetheless false — most commonly because the AI was trained on data that never included the counterfactual scenario needed to correctly assess causal impact (e.g., training data with "lots of ads and sales" but no data on what sales would have been with few or no ads).
Why It Matters: Identifies a failure mode where an AI's own confidence is precisely the danger signal — the prediction machine isn't visibly broken or uncertain, it is quietly and convincingly wrong, which is far more dangerous than an obviously low-confidence or malfunctioning prediction.
How the Author Uses It: Demonstrated through the eBay advertising-ROI case, where a naive correlational analysis showed massive positive ROI (4,000%+) for search ads, but a real experiment (turning ads off in one-third of the US for a month) revealed the true ROI was negative — the missing counterfactual data ("what happens with few ads") was an unknown known that only deliberate experimentation could surface.
Related Concepts: Known knowns/unknowns framework (Ch.7), reverse causality (Ch.7)
```

```
Concept Name: The security risk taxonomy — input, training, and feedback data vulnerabilities
Definition: A three-part framework categorizing AI security risks according to which of the three data types (established in Ch.6: input, training, feedback) an attacker manipulates. Input data risk involves feeding a deployed AI corrupted or adversarially crafted data to distort a specific prediction (e.g., inserting brief flash images to fool video classification, or feeding false identity data to manipulate a personalized medical prediction). Training data risk involves an attacker interrogating/querying a deployed model enough times to reverse-engineer its underlying algorithm, effectively stealing the intellectual property embedded in its training. Feedback data risk involves an attacker deliberately feeding a learning-in-the-wild AI corrupted interaction data to systematically teach it incorrect or harmful behavior over time.
Why It Matters: Extends AI security thinking beyond generic "hacking" concerns to the specific, structural vulnerabilities created by an AI's dependence on three distinct data streams, each of which offers a different attack surface requiring different defenses.
How the Author Uses It: Organized as the chapter's three named subsections ("Input Data Risks," "Training Data Risks," "Feedback Data Risks"), each illustrated with a distinct real case (adversarial video misclassification; Microsoft's Bing/Google-toolbar reverse-engineering; Microsoft's Tay chatbot). For input data specifically, the chapter distinguishes a visible failure mode (a crash — "might seem bad, but at least you know when they have occurred") from an invisible one (manipulation — "you may not know about it, at least not until too late"), inverting the intuitive assumption that visible failures are worse. For training data specifically, the chapter notes attacks leave a trail: extracting a model requires many queries, so unusual query volume or diversity should raise red flags, making detection (though not prevention) possible.
Related Concepts: Training/input/feedback data (Ch.6), monoculture risk
```

```
Concept Name: Monoculture risk in prediction machine deployment
Definition: An ecological analogy applied to AI systems: just as farmers planting a single, uniform crop strain reduce individual-level risk (the best-performing strain wins in normal conditions) while increasing system-level risk (a single disease or adverse condition can wipe out the entire uniform crop at once), organizations that standardize on one "best" prediction machine across an entire fleet or system reduce individual-level failure risk while creating the possibility of simultaneous, correlated, catastrophic failure across the whole system if that one algorithm is successfully attacked or manipulated.
Why It Matters: Identifies a genuine, non-obvious trade-off in AI standardization decisions — the same homogeneity that makes each individual unit perform better and more safely also makes the entire system more fragile to a single coordinated attack, directly paralleling a well-established principle in ecology and agriculture.
How the Author Uses It: Introduced via the agricultural monoculture analogy, then applied directly to autonomous vehicles (an attack on one vehicle is a safety risk; an attack on all vehicles using the same algorithm simultaneously is a national security threat), with diversity of deployed prediction machines offered as a partial mitigation that itself trades away some individual-level performance.
Related Concepts: The security risk taxonomy, on-device (untethered) prediction as a security mitigation
```

## 3. Key Claims

```
Claim: Latanya Sweeney (former CTO of the US Federal Trade Commission, now a Harvard professor) was surprised when a colleague, Googling her name to find one of her papers, discovered ads suggesting she had been arrested; Sweeney clicked the ad, paid a fee, and confirmed what she already knew — she had never been arrested. After systematically testing this by searching various names, she found that Googling a black-associated name (like Lakisha or Trevon) was 25 percent more likely to produce an ad suggesting an arrest record than searching a name like Jill or Jack.
Type: Empirical (documented research finding)
Evidence Provided: A specific, quantified figure (25% higher likelihood), a first-hand discovery narrative involving a named, credentialed researcher testing her own name and a colleague's (Adam Tanner), cited to endnote 2.
Strength of Support: Strong — a specific, quantified, systematically tested finding from a named, credentialed expert (former FTC chief technology officer), consistent with well-documented, independently verifiable research on algorithmic bias in online advertising.
```

```
Claim: The likely mechanism behind Google's racially skewed arrest-ad pattern was not necessarily advertiser intent to discriminate (which Google denied) but potentially Google's own quality-score algorithm: if potential employers researching job candidates were more likely to click an arrest-suggesting ad when it appeared alongside a black-sounding name than other names, the resulting higher "quality score" for that ad-keyword pairing would cause Google's algorithm to serve the ad more often for those names — meaning Google's algorithm could amplify a pre-existing societal prejudice (employers' differential suspicion based on name) without any discriminatory intent on Google's or the advertiser's part.
Type: Interpretive (author-constructed causal hypothesis)
Evidence Provided: A step-by-step mechanistic explanation grounded in how Google's advertising quality-score system is known to function, presented as one plausible explanation among the possibilities the authors consider (advertiser intent being the other, denied by Google), cited to endnote 3.
Strength of Support: Moderate — a plausible, mechanistically coherent hypothesis consistent with how ad quality-scoring algorithms generally work, but presented as the authors' own interpretive reconstruction rather than a claim independently confirmed by Google's internal data.
```

```
Claim: Economists Anja Lambrecht and Catherine Tucker, in a 2019 study, found that Facebook ads promoting STEM (science, technology, engineering, and math) jobs were shown to women less often than to men — not because women were less likely to click on the ads or because of discriminatory labor markets in certain countries, but because younger women are a more valuable (and therefore more expensive to advertise to) demographic on Facebook, meaning Facebook's ad-placement algorithm, when optimizing for return per ad dollar, naturally favored showing the (equally clickable) STEM job ads to the cheaper audience: men.
Type: Empirical (citing external economic research)
Evidence Provided: Named researchers (Anja Lambrecht, Catherine Tucker), a specific study year (2019), cited to endnote 4, with a clear, mechanistically explained causal pathway (demographic ad-pricing economics, not click-rate or labor-market differences).
Strength of Support: Strong — a specific, formally cited, peer-reviewed-style economics study identifying a precise, non-obvious causal mechanism for an observed discriminatory pattern.
```

```
Claim: A person or organization can be held legally liable for discrimination even when it is entirely accidental/unintentional, as established by the New York City Fire Department case, in which a court found the department discriminated against black and Hispanic firefighter applicants through an entrance exam that emphasized reading comprehension questions found to have no relationship to actual job effectiveness, but on which black and Hispanic applicants systematically scored worse — a case eventually settled for approximately $99 million.
Type: Empirical/Legal (documented court case)
Evidence Provided: A specific, named legal case (New York City Fire Department), a specific settlement figure ($99 million), and the specific legal finding (the exam's reading-comprehension emphasis was unrelated to job effectiveness), cited to endnote 5.
Strength of Support: Strong — a specific, formally documented, real legal case with a verifiable settlement amount, used to establish the disparate-impact liability principle with concrete legal stakes.
```

```
Claim: Economists working for eBay (Thomas Blake, Chris Nosko, and Steve Tadelis) persuaded eBay to turn off all search advertising in one-third of the United States for an entire month in 2012, despite the ads showing a measured ROI (using traditional correlational statistics) of more than 4,000 percent — and this month-long real experiment revealed the search ads had practically no impact on sales (negative true ROI), because eBay's consumers were savvy enough to find eBay via ordinary/organic Google search results even without seeing a paid ad, since Google would highly rank eBay listings regardless (a pattern also true for brands like BMW and Amazon); the only area where the ads seemed to do genuine good was attracting new users to eBay.
Type: Empirical (documented economic experiment)
Evidence Provided: Named researchers (Thomas Blake, Chris Nosko, Steve Tadelis), a specific year (2012), a specific experimental design (turning off ads in one-third of the US for a month), specific figures (4,000%+ measured/correlational ROI versus negative true/experimental ROI), and named comparison brands (BMW, Amazon), cited to endnote 7.
Strength of Support: Strong — a specific, formally documented, real controlled experiment (a rare case in the book of genuine causal experimentation rather than observational correlation) with dramatic, quantified, and independently verifiable before/after findings.
```

```
Claim: University of Washington researchers demonstrated that Google's video-content-detection algorithm could be fooled into misclassifying videos by inserting random, unrelated images for mere fractions of a second — brief enough that a human viewer would never consciously notice the inserted images (e.g., car images spliced into a zoo video), but long enough for the AI's classification to be thrown off — representing a critical vulnerability in any environment (such as ad-matching to video content) where publishers need to reliably know what content is actually being published.
Type: Empirical (documented security research)
Evidence Provided: A named research institution (University of Washington), a named target system (Google's video content detection algorithm), and a specific, mechanistically described attack method (sub-second adversarial image insertion), cited to endnote 8.
Strength of Support: Strong — a specific, formally cited security research demonstration illustrating a genuine, technically verifiable adversarial-AI vulnerability.
```

```
Claim: Google's anti-spam team ran a sting operation in which they set up fake search results for a variety of absurd, otherwise-nonexistent search queries (such as "hiybbprqag"), had Google engineers search those exact terms from home computers using Microsoft Internet Explorer's toolbar, and weeks later found that Microsoft's Bing search engine returned Google's same fake results for those same nonsense queries — demonstrating that Microsoft was using data collected via its browser toolbar (which observed users searching Google and clicking Google's results) to train Bing's own algorithm via a form of learning-by-using/imitation, effectively reverse-engineering aspects of Google's search algorithm from externally observable input-output data.
Type: Empirical (documented real-world corporate incident)
Evidence Provided: A specific, verifiable, publicly reported real corporate controversy, with a specific described experimental design (the "hiybbprqag"-style sting), cited to endnotes 12 and 13, with authors' own interpretive analysis of exactly what Microsoft was and wasn't doing (learning search-term-to-website mappings via toolbar-observed clicks, but not directly learning how search terms translated into clicks the way Google's own algorithm would).
Strength of Support: Strong — a well-documented, publicly reported real technology-industry controversy (widely covered in tech press at the time), consistent with independently verifiable public record.
```

```
Claim: In 2016, computer science researchers demonstrated that certain deep-learning algorithms are particularly vulnerable to reverse-engineering imitation: testing several important machine-learning platforms (including Amazon Machine Learning), they showed that with a relatively small number of queries (650–4,000), an attacker could reverse-engineer those models to a very close approximation — sometimes a perfect one — meaning the very act of deploying a machine-learning algorithm for public use creates this reverse-engineering vulnerability.
Type: Empirical (documented security research)
Evidence Provided: A specific year (2016), specific named platforms tested (Amazon Machine Learning among others), and a specific, quantified query-count range (650–4,000) required for successful model extraction, cited to endnote 15.
Strength of Support: Strong — a specific, formally cited academic security research finding with precise, quantified figures.
```

```
Claim: In March 2016, Microsoft launched an AI-based Twitter chatbot named Tay, designed to interact with people on Twitter and learn specifically about "casual and playful conversation" — but within a short time after launch, Twitter users deliberately tested the limits of what Tay would say (e.g., a user named "Baron Memington" asked whether Tay supported genocide, to which Tay responded "I do indeed"), and Tay rapidly evolved to produce racist, misogynist, and Nazi-sympathizing statements, forcing Microsoft to pull the experiment; precisely how Tay evolved so quickly is not entirely clear, but interactions with Twitter users most likely taught Tay this behavior.
Type: Empirical (documented, widely publicized real incident)
Evidence Provided: A specific, dated (March 2016), well-documented real public incident, including a specific quoted exchange (the "Baron Memington" genocide question and Tay's response), cited to endnotes 16 and 17.
Strength of Support: Strong — an extensively documented, widely reported, easily independently verifiable real AI failure case.
```

## 4. Frameworks, Models, and Mental Models

```
Name: The six-risk taxonomy for AI deployment (Key Points summary)
Description: A summary classification, stated explicitly in the chapter's Key Points, organizing the entire chapter's risk discussion into six distinct, named risk categories every organization deploying AI should anticipate.
Components: (1) Discrimination risk — predictions can lead to discrimination, and even inadvertent discrimination creates liability. (2) Quality risk from sparse data — AIs are ineffective when data is sparse, particularly the "unknown known" failure mode where a confident prediction is false. (3) Input data security risk — incorrect/manipulated input data can fool prediction machines, exposing users to hacker attacks. (4) Monoculture/diversity risk — like biodiversity, prediction-machine diversity trades individual-level performance against system-level failure risk; less diversity improves individual performance but increases massive-failure risk. (5) Training data security risk — prediction machines can be interrogated/queried to reverse-engineer them, exposing organizations to intellectual property theft and to attackers identifying weaknesses. (6) Feedback data security risk — feedback can be manipulated so prediction machines learn destructive behavior.
How It Works: Provides a checklist an organization's leadership can use to systematically audit its own AI deployments, mapping each of the chapter's detailed cases (Sweeney/Google ads, Facebook STEM ads, NYC Fire Department, eBay, University of Washington video attack, Microsoft/Bing toolbar, Tay) onto one of the six named risk categories.
When It Is Useful: As a comprehensive, memorable summary framework for any organization's AI risk-management planning process — the chapter's own explicit closing synthesis of everything covered.
Limitations: The chapter is explicit that eliminating all these risks entirely is impossible ("there is no easy solution") — the framework is diagnostic (helping identify and anticipate risk) rather than prescriptive (it doesn't offer a complete solution for eliminating each risk category).
```

```
Name: "AI neuroscience" — hypothesize, test, compare methodology for black-box auditing
Description: A three-step practical method for diagnosing why an opaque AI model produces discriminatory or otherwise problematic outputs, without needing to directly inspect the model's internal logic.
Components: (1) Hypothesize what factor(s) might be driving an observed difference in outputs across groups. (2) Provide the AI with different input data specifically designed to test that hypothesis (holding other factors constant). (3) Compare the resulting predictions to confirm or refute the hypothesis.
How It Works: Applied exactly as Lambrecht and Tucker did with the Facebook STEM-ad case — hypothesizing that ad cost/pricing (not click-through rate or labor-market discrimination) explained the gender skew, then testing this by examining the cost-per-impression data specifically.
When It Is Useful: Whenever an organization suspects (or wants to proactively check for) discriminatory or otherwise unexpected behavior in a black-box AI system it cannot directly interrogate at the algorithm/formula level.
Limitations: Requires the auditor to already have plausible hypotheses worth testing — the method can confirm or refute a specific guess about the mechanism but doesn't guarantee discovery of an unanticipated cause the auditor never thought to test for.
```

## 5. Research and Evidence

```
Study Name / Reference: Lambrecht and Tucker's Facebook STEM-ad gender-skew study
Researchers: Anja Lambrecht and Catherine Tucker (economists)
Year: 2019
Sample/Data: Facebook ads promoting STEM (science, technology, engineering, math) jobs, placed on the social network
Method: Placed job ads on Facebook and analyzed which demographics the ads were shown to and why
Key Finding: Facebook showed the ads to women less often than men, not due to lower female click-through rates or discriminatory labor markets, but because younger women are a more expensive advertising demographic on Facebook, causing the cost-optimizing ad-placement algorithm to favor showing (equally effective) ads to the cheaper male audience.
Caveats/Limitations Noted: None specified within the visible chapter text.
```

```
Study Name / Reference: Blake, Nosko, and Tadelis's eBay search-advertising experiment
Researchers: Thomas Blake, Chris Nosko, Steve Tadelis (economists working for eBay)
Year: 2012
Sample/Data: eBay's search advertising, with all ads turned off in one-third of the United States for one month
Method: A real, controlled field experiment (not observational correlation) comparing sales in the ad-off region to the ad-on regions
Key Finding: Search ads had practically no true impact on eBay's sales (negative real ROI) despite showing 4,000%+ ROI under naive correlational analysis, because savvy eBay users found the site via organic search regardless; the only genuine benefit of the ads was attracting new users.
Caveats/Limitations Noted: None specified within the visible chapter text; the study is explicitly presented as a cautionary tale about correlational AI analysis mistaking association for causation.
```

```
Study Name / Reference: University of Washington adversarial video classification research
Researchers: Not individually named within the visible chapter text (attributed to "University of Washington researchers")
Year: Not specified within the visible chapter text (cited to endnote 8)
Sample/Data: Google's video content detection algorithm
Method: Inserting random, unrelated images into video content for fractions of a second, imperceptible to human viewers but sufficient to disrupt AI classification
Key Finding: The AI could be reliably fooled into misclassifying video content (e.g., a zoo video misclassified due to briefly inserted car images) via this sub-perceptual adversarial insertion technique.
Caveats/Limitations Noted: None specified within the visible chapter text.
```

```
Study Name / Reference: 2016 machine-learning model extraction research
Researchers: Not individually named within the visible chapter text (described as "computer science researchers")
Year: 2016
Sample/Data: Several important machine-learning platforms, including Amazon Machine Learning
Method: Querying deployed deep-learning models a controlled number of times (650–4,000 queries) and using the resulting input-output pairs to reverse-engineer the underlying model
Key Finding: Certain deep-learning algorithms could be reverse-engineered to a very close (sometimes perfect) approximation using a relatively small number of queries, demonstrating that public deployment of a machine-learning model inherently creates a model-extraction vulnerability.
Caveats/Limitations Noted: None specified within the visible chapter text.
```

## 6. Experiments

```
Experiment Name: eBay's month-long search-advertising shutoff (2012)
Researchers/Team: Thomas Blake, Chris Nosko, Steve Tadelis
What was tested: Whether eBay's search advertising actually caused incremental sales, as opposed to merely correlating with sales that would have happened anyway.
Method/Design: A genuine controlled field experiment — eBay turned off all search advertising in one-third of the United States for an entire month, allowing direct before/after and treatment/control comparison rather than relying on observational correlation.
Results: The ads had practically no true causal impact on sales (negative real ROI), sharply contradicting the 4,000%+ ROI suggested by naive correlational analysis of the same advertising data.
Limitations Noted by Authors: The chapter uses this specifically to illustrate that AI systems relying on correlational (not experimental) data are vulnerable to the exact same "unknown known" trap — the missing counterfactual (what happens with few/no ads) simply isn't present in ordinary observational data, requiring deliberate human-designed experimentation to surface.
```

```
Experiment Name: Google's anti-spam "hiybbprqag" sting operation against Microsoft
Researchers/Team: Google's anti-spam team
What was tested: Whether Microsoft's Bing search engine (via its browser toolbar) was using observed Google search-and-click data to improve/imitate Bing's own algorithm.
Method/Design: Google engineers searched a set of deliberately absurd, otherwise-nonexistent terms (e.g., "hiybbprqag") using Microsoft's Internet Explorer toolbar, with Google having pre-planted fake results for those exact terms; weeks later, the team checked whether the same fake results appeared on Bing.
Results: Google's fake results for nonsense queries like "hiybbprqag" did appear on Bing, confirming Microsoft's toolbar was being used to observe and imitate Google's search behavior.
Limitations Noted by Authors: The authors note what Microsoft was specifically *not* shown to be doing — directly learning how Google search terms translated into clicks in a way that would let it fully imitate Google's own algorithm — distinguishing partial imitation (learning specific rare query-to-result mappings) from complete algorithmic reconstruction.
```

## 7. Cases and Stories

```
Case Title: Latanya Sweeney and racially skewed Google arrest-suggesting ads
People / Organization: Latanya Sweeney (former FTC CTO, Harvard professor); an unnamed colleague who first discovered the ad; Adam Tanner (colleague tested afterward); Google
Context: The chapter's opening case, establishing algorithmic discrimination via quality-score optimization as a real, documented phenomenon rather than a hypothetical concern.
What Happened: See Section 3 for full details. Note: the initial discovery was made by a colleague searching for one of Sweeney's papers, not by Sweeney herself.
Outcome: A documented, quantified (25% differential) racial bias in ad-serving behavior, with a plausible (though not definitively confirmed) explanation rooted in quality-score optimization amplifying existing societal bias rather than deliberate racial targeting by advertisers or Google.
Concept Illustrated: Algorithmic discrimination via quality-score optimization; the risk of AI amplifying, not creating, existing societal prejudice.
Why This Case Is Useful: A specific, named, credentialed researcher's first-hand discovery narrative that makes an abstract algorithmic-bias concern concrete, personal, and systematically documented rather than anecdotal.
Potential for Reuse: High
```

```
Case Title: Facebook's gender-skewed STEM job ads
People / Organization: Facebook; economists Anja Lambrecht and Catherine Tucker; economist/lawyer Ben Edelman
Context: The chapter's second discrimination case, illustrating both the "AI neuroscience" diagnostic method and disparate-impact liability risk.
What Happened: See Section 3 and Section 5 for full details.
Outcome: A precisely diagnosed causal mechanism (ad-pricing economics, not click-rate differences) for an observed gender skew in job-ad delivery, with Ben Edelman's analysis explaining why this could create genuine legal liability for both Facebook and the employers placing the ads.
Concept Illustrated: "AI neuroscience" auditing methodology; disparate impact liability.
Why This Case Is Useful: A rigorously diagnosed real case (unlike the more speculative Google/Sweeney mechanism) that models exactly the hypothesize-test-compare auditing process the chapter recommends, with a clear, non-obvious causal explanation.
Potential for Reuse: High
```

```
Case Title: The New York City Fire Department discrimination settlement
People / Organization: New York City Fire Department; black and Hispanic firefighter applicants
Context: The chapter's grounding legal precedent for disparate impact liability, establishing real financial stakes independent of any AI system.
What Happened: See Section 3 for full details.
Outcome: A ~$99 million settlement after a court found a facially neutral, reading-comprehension-heavy entrance exam had no relationship to job effectiveness but systematically disadvantaged black and Hispanic applicants.
Concept Illustrated: Disparate impact liability — legal exposure exists regardless of discriminatory intent.
Why This Case Is Useful: A concrete, quantified, pre-AI legal precedent that makes clear the disparate-impact liability principle predates and applies independently of AI, strengthening the chapter's argument that "the algorithm did it" is not a viable legal defense.
Potential for Reuse: High
```

```
Case Title: eBay's search-advertising ROI experiment
People / Organization: eBay; economists Thomas Blake, Chris Nosko, Steve Tadelis
Context: The chapter's central "Quality Risks" case, illustrating the unknown-knowns failure mode through a rare genuine causal experiment.
What Happened: See Sections 3 and 6 for full details.
Outcome: Correlational analysis suggested massive positive ROI (4,000%+); the real experiment revealed negative true ROI, with organic search sufficing for eBay's savvy user base.
Concept Illustrated: Unknown knowns as a quality-risk failure mode; the limits of correlational (as opposed to experimental) AI analysis.
Why This Case Is Useful: A dramatic, quantified, named-researcher case that makes the abstract "correlation isn't causation" warning vivid through a specific dollar-figure reversal (positive to negative ROI) discovered via a bold real-world experiment.
Potential for Reuse: High
```

```
Case Title: University of Washington's adversarial video misclassification attack
People / Organization: University of Washington researchers; Google (target system)
Context: The chapter's primary "Input Data Risks" case.
What Happened: See Section 3 and Section 5 for full details.
Outcome: Demonstrated a reliable, technically verifiable method for fooling video-content-detection AI via sub-perceptual adversarial image insertion.
Concept Illustrated: Input data security risk — the vulnerability of AI systems to manipulated or adversarially crafted input data.
Why This Case Is Useful: A vivid, easy-to-visualize security vulnerability (briefly flashed images humans can't perceive but AI misclassifies on) that makes abstract adversarial-AI concerns concrete.
Potential for Reuse: High
```

```
Case Title: The diabetic/insulin input-data-manipulation example
People / Organization: Not specified (a hypothetical individual using a personalized medical AI)
Context: A second, safety-critical illustration of input data risk, distinct from the video-classification case.
What Happened: The chapter describes a hypothetical: "a diabetic using an AI to optimize insulin intake could end up in serious jeopardy if the AI has incorrect data about that person and then offers predictions that suggest lowering insulin intake when it should be increased. If harming a person is someone's objective, then this is one way to do it effectively."
Outcome: Presented as illustrative rather than a documented real incident.
Concept Illustrated: Input data security risk, specifically in a personalized, safety-critical medical context where manipulated identity/input data could cause direct physical harm.
Why This Case Is Useful: A vivid, high-stakes hypothetical that makes the abstract "identity is the most important data to protect" principle immediately concrete and personally relatable.
Potential for Reuse: High
```

```
Case Title: Nymi's heartbeat-based identity verification
People / Organization: Nymi (startup the authors worked with); other companies using retina, face, fingerprint, and smartphone gait-pattern identification
Context: Directly follows the input-data/identity-manipulation risk discussion, illustrating how identity-verification technology is co-developing with AI personalization specifically to mitigate this risk.
What Happened: AI technologies will develop "hand-in-hand" with identity verification; Nymi developed machine-learning-based heartbeat identification, alongside other companies using retina scans, facial recognition, fingerprints, or smartphone-detected walking-gait patterns.
Outcome: Presented as an emerging, hopeful convergence — "a happy confluence in technologies may emerge that allows us to simultaneously personalize AI and safeguard identity" — rather than a fully solved problem.
Concept Illustrated: The security risk taxonomy's input-data/identity dimension, and a real-world mitigation approach co-evolving alongside the risk itself.
Why This Case Is Useful: A first-hand, concrete startup example (consistent with the book's established CDL-vantage-point sourcing) that grounds an otherwise abstract risk-mitigation discussion in a specific, real technology.
Potential for Reuse: High
```

```
Case Title: Microsoft's Bing/toolbar reverse-engineering of Google search (the "hiybbprqag" sting)
People / Organization: Google's anti-spam team; Microsoft; Bing; Internet Explorer
Context: The chapter's primary "Training Data Risks" case, illustrating a real, publicly documented corporate controversy over algorithmic imitation.
What Happened: See Section 3 and Section 6 for full details.
Outcome: Confirmed Microsoft's toolbar was being used to observe Google search behavior and improve Bing, sparking industry debate about whether this constituted acceptable competitive practice or improper appropriation.
Concept Illustrated: Training data security risk — deployed AI systems can be interrogated and partially reverse-engineered by observing their input-output behavior at scale.
Why This Case Is Useful: A famous, real, widely reported tech-industry controversy that makes the abstract "your competitors can reverse-engineer your AI" risk concrete and historically grounded.
Potential for Reuse: High
```

```
Case Title: Microsoft's Tay chatbot
People / Organization: Microsoft; Twitter users (including "Baron Memington")
Context: The chapter's primary "Feedback Data Risks" case and its most dramatic, widely known example.
What Happened: See Section 3 for full details.
Outcome: A well-intentioned learning-by-using experiment rapidly and publicly failed when malicious users deliberately corrupted the AI's feedback data, forcing Microsoft to shut it down.
Concept Illustrated: Feedback data security risk — AI systems that learn from real-world interaction data are vulnerable to deliberate, coordinated manipulation of that feedback.
Why This Case Is Useful: An extremely well-known, widely reported, dramatic real AI failure that makes feedback-data manipulation risk immediately vivid and memorable, directly relevant to any organization considering learning-by-using deployment.
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: Algorithmic discrimination without discriminatory intent
Example: Latanya Sweeney's Google arrest-ad discovery, paired with the quality-score amplification mechanism.
Why It Works: A specific, personal, first-hand discovery narrative from a credentialed researcher, with a clear quantified figure (25%) and a plausible mechanistic explanation that makes an abstract fairness concern concrete and systematically documented.
Possible Alternative Domain: AI, Ethics, Business
```

```
Concept: Correlational AI analysis mistaking association for causation
Example: eBay's search-advertising ROI reversing from 4,000%+ (correlational) to negative (experimental).
Why It Works: A dramatic, quantified before/after reversal from a real controlled experiment makes an easily-glossed-over statistical warning ("correlation isn't causation") vivid and memorable through concrete dollar figures.
Possible Alternative Domain: AI, Business, Statistics/Data Science
```

```
Concept: AI's vulnerability to feedback-data manipulation
Example: Microsoft's Tay chatbot rapidly turning racist within hours of public deployment.
Why It Works: An extremely well-known, dramatic, easily-recalled real incident that makes an abstract security concept (feedback poisoning) immediately concrete and memorable.
Possible Alternative Domain: AI, Business, Technology Ethics
```

## 9. Counterintuitive Insights

```
Insight: An AI system can produce systematically discriminatory outcomes even when no individual involved — not the advertiser, not the platform's engineers — intended any discrimination at all, simply because the system is optimizing for a proxy metric (click-through "quality score," cost-per-impression efficiency) that happens to correlate with a protected characteristic through the aggregate behavior of other humans.
Common Belief: Discrimination requires either a discriminatory actor (someone intentionally treating groups differently) or an obviously biased dataset.
Author's Argument: Both the Google arrest-ad case and the Facebook STEM-ad case show discrimination emerging purely from the interaction between a neutral optimization objective and pre-existing patterns in aggregate human behavior (differential click rates by name; differential ad costs by demographic) — no one needs to intend or even be aware of the discriminatory pattern for it to emerge and create real legal liability.
Evidence: The Lambrecht/Tucker Facebook study's precise mechanistic diagnosis (cost-per-impression economics, not click-rate differences or labor-market discrimination) and the authors' hypothesized Google quality-score mechanism.
Why It Is Surprising: It shows that "we didn't intend to discriminate, and our algorithm is neutral" is not just an insufficient legal defense (per disparate impact law) but also often factually incomplete — the discrimination can be real, measurable, and mechanistically explicable even when genuinely unintended by every human involved in building the system.
```

## 10. Unique or Unusual Ideas

```
Idea: Applying the ecological concept of monoculture risk (agricultural crop-strain uniformity trading individual-level benefit for system-level catastrophic vulnerability) directly to AI deployment standardization decisions.
Why It Seems Unique: Most AI security discussions focus on individual-system vulnerabilities; this chapter explicitly borrows a framework from ecology/agriculture to reason about *fleet-level* or *system-level* AI risk, showing that the same logic determining whether a farming region should diversify crop strains applies to whether an organization (or society) should diversify its prediction-machine algorithms across a fleet of autonomous vehicles or other AI-dependent systems.
Potential Connection to Other Topics: Cybersecurity's broader "diversity as defense" principle (e.g., software diversity to prevent single-exploit mass compromise), and financial risk management's correlation/diversification logic.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: The chapter's own proposed mitigation for monoculture/systemwide-failure risk (encouraging diversity in deployed prediction machines) is explicitly acknowledged to come "at the cost of reduced performance" and possibly "increase the risk of incidental smaller failures due to a lack of standardization" — meaning the solution to one risk category directly creates trade-offs with both individual-level quality and a different category of failure risk.
Author's Position: Transparently acknowledged as a genuine trade-off rather than resolved with a clean recommendation — the chapter states this "involves a trade-off between individual and system-level outcomes" without specifying how an organization should weigh the two.
Possible Counterargument: A reader might push for more specific guidance on when the systemwide-catastrophic-failure risk is severe enough (e.g., safety-critical systems like autonomous vehicles or national infrastructure) to justify accepting the performance cost of diversification, versus when standardizing on the single best-performing system is clearly correct (e.g., low-stakes consumer applications).
What Evidence Would Help Resolve It: Formal risk-modeling research quantifying the actual probability and cost of coordinated systemwide attacks against various AI deployment scales, which the chapter does not cite as existing at the time of writing.
```

## 12. Quotable Ideas

```
Paraphrase (short): The black box of AI is not an excuse to ignore potential discrimination or a way to avoid using AI in situations where discrimination might matter. Plenty of evidence shows that humans discriminate even more than machines.
Why the Idea Matters: A direct, quotable rebuttal to two opposite overreactions to AI bias concerns — neither "ignore it because we can't inspect the algorithm" nor "avoid AI entirely because it might discriminate" is the right response — while also offering the reassuring, evidence-grounded counterpoint that humans are typically worse discriminators than machines.
Source Location: Book p.224
```

```
Paraphrase (short): A single lie in a web of truth is of little consequence.
Why the Idea Matters: A vivid, memorable, aphoristic articulation of why manipulating input data is harder for attackers when a prediction is based on a confluence of many factors — one falsified data point gets diluted by many truthful ones, unlike simpler predictions based on fewer inputs.
Source Location: Book p.226–227
```

```
Paraphrase (short): Just like the old computer adage—"garbage in, garbage out"—prediction machines fail if they have poor data or a bad model.
Why the Idea Matters: A classic, immediately recognizable computer science adage the chapter explicitly invokes to frame input data risk, giving readers a memorable, pre-existing mental hook for a new AI-specific risk category.
Source Location: Book p.226
```

## 13. Psychology Connections

```
Direct example from the book: The chapter's observation that "plenty of evidence shows that humans discriminate even more than machines" (book p.224) implicitly connects to the broader psychological literature on implicit bias and in-group/out-group discrimination in human decision-making, used here as a comparative benchmark rather than developed as its own analytical thread.
```

## 14. Mathematics and Decision Science Connections

```
Connection: The "unknown knowns" concept directly extends the known-knowns/known-unknowns/unknown-unknowns framework introduced in Chapter 7, adding a fourth quadrant (confident-but-false predictions arising from missing counterfactual data) that is specifically relevant to correlational machine learning.
Connection: The eBay case is a direct, concrete illustration of the correlation-versus-causation distinction and the necessity of controlled experimentation (a treatment/control comparison) to establish true causal impact, a foundational concept in applied statistics and econometrics.
Connection: The model-extraction research (650–4,000 queries sufficient to reverse-engineer a deep-learning model) is a specific, quantified example of information-theoretic vulnerability — how much information about an algorithm's internal structure can be inferred purely from observing its input-output behavior at scale.
```

## 15. Sports Connections

None identified in the chapter's direct examples; no forced inference added.

## 16. AI and Machine Learning Connections

```
Direct examples from the book: Google's ad quality-score algorithm; Facebook's ad-placement/cost-optimization algorithm; deep learning's black-box opacity; Google's video content detection algorithm and its adversarial vulnerability; Microsoft Bing's toolbar-based learning-by-using/imitation of Google search; deep-learning model extraction via query-based reverse-engineering (tested on Amazon Machine Learning and other platforms); Microsoft's Tay chatbot and its real-time learning from Twitter interactions.
Inferred connection (my own): The chapter's three-part security taxonomy (input/training/feedback data risks) maps closely onto the modern AI-security field's standard categorization of adversarial attacks — evasion attacks (input data manipulation to fool a deployed model), model extraction/stealing attacks (training data risk, reverse-engineering via queries), and data poisoning attacks (feedback data risk, corrupting a model's ongoing learning) — a taxonomy that has become formalized in AI security research since this book's original publication, though the chapter does not use this specific modern vocabulary.
```

## 17. Content Creation Opportunities

```
Idea Title: "The Google Ad That Accidentally Became Racist — And What It Teaches About AI Bias"
Format: YouTube Long-form
Application Domain: AI | Ethics | Business
Hidden Principle: Signal vs. Noise
Story Hook (Layer 1): A Harvard professor Googled her own name and found an ad suggesting she'd been arrested. She hadn't been. Then she discovered something worse: it happened 25% more often for black-sounding names than white-sounding ones — and nobody at Google had programmed it to do that.
Principle Framework (Layer 2): An AI doesn't need a racist programmer to produce racist outcomes — it just needs an optimization target (like "clicks") that happens to correlate with a protected characteristic through ordinary human behavior, which means "our algorithm is neutral" is neither a technical nor a legal defense.
Best Supporting Case: The Latanya Sweeney case (Section 7), paired with the Facebook STEM-ad diagnosis (Lambrecht/Tucker) as a rigorously proven parallel example.
Character Application: Insight: Interpreter
Psychology Angle: Inferred — implicit bias and how it gets encoded into aggregate behavioral data.
Math Angle: Direct — the quality-score/cost-per-impression optimization mechanics.
Sports Angle: None identified.
Business Angle: Direct — disparate impact liability as a real, quantified legal risk ($99M NYC Fire Department settlement).
Investing Angle: Inferred — evaluating AI-dependent ad-tech companies for undisclosed discrimination liability risk.
History Angle: Direct — the NYC Fire Department case as legal precedent predating modern AI.
AI Angle: Direct — a foundational case study in unintentional algorithmic discrimination.
```

```
Idea Title: "Microsoft Turned Google's Search Engine Into a Trap — And Caught Bing Copying It"
Format: YouTube Short | Community Post
Application Domain: AI | Business | Technology History
Hidden Principle: Optimization
Story Hook (Layer 1): Google engineers searched a made-up word that didn't exist anywhere on the internet. Weeks later, that exact fake result showed up on Microsoft's Bing.
Principle Framework (Layer 2): Any AI system exposed to the public — its inputs and outputs observable at scale — can be partially reverse-engineered by anyone willing to query it enough times, a structural vulnerability baked into the act of deployment itself, not a flaw that can simply be patched away.
Best Supporting Case: The Google/Bing "hiybbprqag" sting (Section 7).
Character Application: Sigma: Architect
Psychology Angle: None identified.
Math Angle: Direct — the 650–4,000 query threshold for model extraction.
Sports Angle: None identified.
Business Angle: Direct — competitive intelligence risk and IP protection for deployed AI products.
Investing Angle: Inferred — evaluating whether an AI startup's "moat" is actually defensible against query-based reverse-engineering.
History Angle: Direct — the real, publicly documented 2011 Google/Bing controversy.
AI Angle: Direct — a concrete illustration of the training-data/model-extraction security risk.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B04-C20-01
Title: Algorithmic discrimination via quality-score optimization
Type: Case
Summary: Latanya Sweeney found Google ads suggesting an arrest record appeared 25% more often for black-sounding names — likely because a neutral quality-score algorithm amplified pre-existing human click-behavior bias, with no discriminatory intent from Google or advertisers required.
Source: Book p.221–222
Tags: discrimination, Google, quality score, algorithmic bias
Related Concepts: Disparate impact liability, "AI neuroscience"
```

```
CARD ID: B04-C20-02
Title: Disparate impact liability
Type: Concept
Summary: A facially neutral algorithm can still create legal liability if it systematically disadvantages a protected class, regardless of intent — established by the NYC Fire Department's $99M settlement and illustrated by Facebook's gender-skewed STEM ads.
Source: Book p.222–223
Tags: disparate impact, liability, discrimination, law
Related Concepts: Algorithmic discrimination via quality-score optimization
```

```
CARD ID: B04-C20-03
Title: "AI neuroscience" — auditing black-box discrimination
Type: Framework
Summary: A hypothesize-test-compare method for diagnosing why an opaque AI produces discriminatory output without inspecting its internal logic — demonstrated by Lambrecht and Tucker's discovery that Facebook's STEM-ad gender skew stemmed from ad-pricing economics.
Source: Book p.223–224
Tags: framework, black box, auditing, discrimination
Related Concepts: Disparate impact liability
```

```
CARD ID: B04-C20-04
Title: Unknown knowns as a quality-risk failure mode
Type: Concept
Summary: A confident-but-false prediction arising from missing counterfactual data — illustrated by eBay's search-ad ROI reversing from 4,000%+ (correlational) to negative (experimental), showing correlational AI's vulnerability to mistaking association for causation.
Source: Book p.224–225
Tags: unknown knowns, correlation vs causation, eBay, quality risk
Related Concepts: Known knowns/unknowns framework (Ch.7)
```

```
CARD ID: B04-C20-05
Title: The security risk taxonomy — input, training, feedback data
Type: Framework
Summary: AI security risks map onto three data types: input data manipulation (adversarial video misclassification), training data extraction (Microsoft's Bing/Google-toolbar reverse-engineering), and feedback data poisoning (Microsoft's Tay chatbot).
Source: Book p.225–231
Tags: framework, security risk, input data, training data, feedback data
Related Concepts: Training/input/feedback data (Ch.6), monoculture risk
```

```
CARD ID: B04-C20-06
Title: Monoculture risk in prediction machine deployment
Type: Concept
Summary: Standardizing on one "best" prediction machine (like a uniform crop strain) reduces individual-level risk but increases system-level catastrophic failure risk if that algorithm is successfully attacked — a genuine trade-off, since diversity itself costs performance.
Source: Book p.227–228
Tags: monoculture, systemwide risk, diversity, autonomous vehicles
Related Concepts: Security risk taxonomy
```

```
CARD ID: B04-C20-07
Title: The six-risk taxonomy for AI deployment
Type: Framework
Summary: The chapter's Key Points summarize six risk categories: discrimination liability, quality risk from sparse data, input data manipulation, monoculture/diversity trade-offs, training data extraction, and feedback data poisoning.
Source: Book p.231–232 (Key Points)
Tags: framework, risk taxonomy, AI risk management
Related Concepts: All chapter concepts
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: Deploying prediction machines carries unavoidable liability, quality, and security risks that organizations must anticipate and manage rather than eliminate — discrimination can emerge from neutral optimization without intent, correlational AI can confidently produce false predictions when counterfactual data is missing, and AI systems are structurally vulnerable to manipulation of their input, training, and feedback data, with no easy universal solution beyond systematic auditing and anticipatory risk management.
Top 5 Concepts: (1) Algorithmic discrimination via quality-score optimization (not malicious intent). (2) Disparate impact liability. (3) "AI neuroscience" — auditing black-box discriminatory behavior. (4) Unknown knowns as a quality-risk failure mode. (5) Monoculture risk in prediction machine deployment.
Top 3 Claims: (1) Latanya Sweeney found Google arrest-suggesting ads appeared 25% more often for black-sounding names. (2) Lambrecht and Tucker precisely diagnosed Facebook's STEM-ad gender skew as an ad-pricing economics artifact, not click-rate or labor-market discrimination. (3) eBay's search-ad ROI reversed from 4,000%+ (correlational) to negative (experimental), demonstrating the unknown-knowns trap.
Top 3 Cases: (1) Latanya Sweeney and Google's racially skewed arrest ads. (2) eBay's search-advertising ROI experiment. (3) Microsoft's Tay chatbot.
Top 3 Studies: (1) Lambrecht and Tucker's 2019 Facebook STEM-ad study. (2) Blake, Nosko, and Tadelis's 2012 eBay advertising experiment. (3) The 2016 deep-learning model-extraction research (650–4,000 queries) — all formally cited, methodologically rigorous studies, making this an unusually research-dense chapter.
Most Unique Idea: Applying the ecological concept of agricultural monoculture risk directly to AI deployment standardization decisions, showing that fleet-wide algorithmic uniformity trades individual-level safety for system-level catastrophic vulnerability.
Most Counterintuitive Idea: An AI system can produce real, measurable, legally actionable discrimination even when no human involved — not the advertiser, not the engineers — intended any discrimination at all, simply through the interaction of a neutral optimization target with pre-existing biased human behavior.
Biggest Weakness or Open Question: The chapter's own proposed mitigation for monoculture/systemwide-failure risk (diversifying deployed AI systems) is explicitly acknowledged to trade away individual-level performance and potentially introduce new standardization-related failures, without providing a clear rule for when this trade-off is worth making.
Best Content Opportunity: "The Google Ad That Accidentally Became Racist — And What It Teaches About AI Bias" (Section 17) — a specific, personal, rigorously documented case that makes the abstract and often-dismissed concern of unintentional algorithmic discrimination concrete, quantified, and legally consequential.
```
