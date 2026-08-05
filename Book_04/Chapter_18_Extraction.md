# Prediction Machines — Chapter 18: When AI Transforms Your Business
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Extraction
**Source:** Book pages 191–202 (PDF pages 204–215)
**Date:** 2026-08-04
**Revised:** Per Chapter_18_Audit.md — added the five-scenario "where does the data reside" framework, the forecast-vs-optimal-response distinction, the threefold reason judgment resists programming, the explicit Ch.19 forward reference, and the two distinct advertiser-data-buying motivations.

BOOK:
Prediction Machines: The Simple Economics of Artificial Intelligence

AUTHOR:
Ajay Agrawal, Joshua Gans, Avi Goldfarb

CHAPTER:
18 — When AI Transforms Your Business

---

## 1. Chapter Thesis

Extending Chapter 17's three-ingredient framework for strategic AI change, this chapter argues that AI's central strategic effect is to redraw the boundary of the firm — the long-term, top-level decision about where your business ends and someone else's begins — across three distinct resources: capital equipment, labor, and data. In each domain, prediction machines reduce uncertainty, which increases a company's ability to write specific contracts ("ifs" that can be matched to "thens"), which in turn increases the incentive to contract out capital and prediction/data/action-focused labor to outside parties. But the effect on judgment-focused labor runs in the opposite direction: because judgment quality is inherently difficult to specify or monitor in a contract, and because prediction and judgment are complements, rising prediction value increases the strategic importance of keeping judgment-focused workers in-house. The chapter closes by showing that the same logic — a boundary drawn at exactly the point where AI stops being strategic and becomes a mere input — explains the opening case of a startup that chose to sell predictions instead of diagnoses.

## 2. Key Concepts

```
Concept Name: The boundary of the firm as AI's central strategic battleground
Definition: The classic economic question of where a business's activities end and another business's (or a market transaction's) begin — what a company chooses to own, produce, or control in-house versus contract out or purchase externally. The chapter argues that prediction machines, by reducing uncertainty, systematically shift this boundary because uncertainty is a key reason firms choose to own activities internally rather than rely on external contracts.
Why It Matters: Reframes "AI strategy" away from a narrow question of which AI tools to buy or build, toward the much broader, more consequential question of how AI reshapes what your organization owns and controls at all — its capital equipment, its workforce composition, and its data assets.
How the Author Uses It: Introduced via the opening physician-diagnosis startup case, then developed systematically across three sections — "Impact of AI: Capital," "Impact of AI: Labor," and "Impact of AI: Data" — each applying the same core logic (uncertainty reduction → more specifiable contracts → altered make-or-buy decisions) to a different resource.
Related Concepts: The three-ingredient test for AI strategic significance (Ch.17), "ifs" and "thens" in contracting
```

```
Concept Name: "Ifs" and "thens" — prediction's effect on contract specificity
Definition: A framework for understanding why reduced uncertainty increases outsourcing: a contract can only specify what a party should do ("then") in response to a defined set of contingencies ("if"); because prediction machines expand the number of contingencies that can be reliably forecast (reliable "ifs"), they expand what can be written into an explicit contract, making it safer and cheaper to rely on outside parties rather than own an activity internally to retain control over unpredictable situations.
Why It Matters: Provides the precise causal mechanism connecting "AI reduces uncertainty" (established since early chapters) to "AI changes firm boundaries" (this chapter's specific claim) — uncertainty reduction doesn't just help a single decision, it changes what can be credibly promised in a contract, which is the basic building block of outsourcing decisions.
How the Author Uses It: Applied to the airline case (predicting weather-related contingencies lets majors write more specific contracts with regional partners) and the automaker case (predicting consumer satisfaction lets automakers write specific up-front contracts with parts suppliers instead of manufacturing in-house).
Related Concepts: The boundary of the firm, judgment's contract-resistance (see below)
```

```
Concept Name: Judgment's resistance to contracting — why AI increases in-house employment for judgment roles
Definition: The claim that judgment-focused labor moves in the opposite direction from capital and prediction/data/action-focused labor as AI diffuses: because judgment quality is inherently difficult to specify in a contract and difficult for an outside party to monitor, and because if judgment could be well-specified it could simply be programmed into a machine (eliminating the need for a human at all), the very fact that judgment remains a human role implies it resists contractual specification — meaning rising AI adoption should increase in-house employment of judgment-focused workers even as it increases outsourcing of other labor and capital. The chapter gives a specific threefold reason judgment resists being programmed: valuable human judgment is used precisely because its rewards "are either unstable or unknown, or require human experience to implement."
Why It Matters: A genuinely counterintuitive extension of the prediction/judgment complementarity principle (Ch.9) to firm-boundary economics — it's not just that judgment becomes more valuable as prediction improves (already established), but that this rising value specifically manifests as insourcing (bringing judgment roles in-house) rather than merely higher pay or status for judgment-holders wherever they sit.
How the Author Uses It: Derived through a chain of reasoning connecting reward-function engineering (Ch.9), the ATM/bank teller case's shift toward relational HR management, and firm-boundary economics, then stated as a direct Key Points takeaway.
Related Concepts: Reward function engineering (Ch.9), job reconstitution (Ch.16), the boundary of the firm
```

```
Concept Name: Data ownership as a distinct strategic axis, separate from prediction technology itself
Definition: The claim that because data and prediction machines are economic complements, procuring or developing AI technology is of limited strategic value unless a company also has (or can obtain) the data needed to feed it — meaning the make-or-buy decision for AI actually decomposes into two separate decisions: whether to own the prediction machine, and whether to own the underlying data, which can be combined in different ways depending on who holds unique, valuable data.
Why It Matters: Corrects a common oversimplification that treats "adopting AI" as a single decision, showing instead that a company can strategically own predictions without owning data (buying predictions as a bundled service, as with Google's advertising network), own data without prioritizing in-house prediction, or need to own both if AI is core to its strategy.
How the Author Uses It: Illustrated via the Ada Support case (an AI startup insisting on owning interaction data before integrating with a larger partner), the online advertising data market (cookies, data brokers, and the distinction between selling raw data versus selling bundled predictions), and Google/Meta/Microsoft's strategic choice to build proprietary advertising networks specifically to own consumer-preference data.
Related Concepts: Data grades (Ch.17), the boundary of the firm
```

## 3. Key Claims

```
Claim: An early-stage machine learning company that was building an AI tool to provide doctors with binary diagnoses ("does the patient have this condition, yes or no") had to obtain costly regulatory approval and consider partnering with an established pharmaceutical or medical device company — but when co-author Joshua asked "why are you providing doctors with diagnoses?" and suggested the company instead sell only the underlying prediction (e.g., "there is an 80 percent chance the patient has the condition"), this reframing eliminated the need for regulatory approval (since physicians already have many tools for reaching a diagnostic conclusion from such information), removed the need to partner early with established companies, and replaced the hard problem of "how do we translate a prediction into a diagnosis" with the much simpler problem of "what threshold accuracy (70%? 80%? 99%?) is needed to deliver a valuable prediction."
Type: Empirical/Strategic advisory (real consulting anecdote)
Evidence Provided: A first-hand account from co-author Joshua of an actual strategic consulting interaction with a named-anonymous ("an early-stage machine learning company") venture, presented as the chapter's opening motivating case and revisited at the chapter's close once the full framework has been developed.
Strength of Support: Strong as a first-hand, specific account of a real strategic decision the authors were directly involved in, though the company itself is not named and no quantified business outcome (e.g., whether this advice was followed or what resulted) is reported within the visible text.
```

```
Claim: Economists Silke Forbes and Mara Lederman found that major US airlines (e.g., United, American) retain direct control over routes prone to unpredictable weather-related disruptions, while contracting routine, more predictable routes out to lower-cost regional partners (e.g., American Eagle, SkyWest) — even though regional partners typically operate at meaningfully lower cost (some studies showing senior major-airline pilots earning 80% more than regional-partner counterparts) — because weather uncertainty, in a tightly networked and capacity-managed industry, creates ripple effects that majors don't want to be "hamstrung" by contract negotiations with independent partners when fast, uncertain-cost changes are needed.
Type: Empirical (citing external economic research)
Evidence Provided: Named researchers (Silke Forbes, Mara Lederman), a study of the US airline industry's organization "around the turn of the millennium," cited to endnote 2, plus a specific supporting figure (80% higher senior-pilot pay at majors versus regional partners).
Strength of Support: Strong — a specific, formally cited academic economics study identifying a clear causal mechanism (weather uncertainty, not just cost) for an otherwise puzzling industry structure.
```

```
Claim: Economists Sharon Novak and Scott Stern found that luxury automakers who manufactured their own parts improved faster from one model year to the next (measured via Consumer Reports customer ratings) than automakers who outsourced parts production, because owning production gave them the control needed to adapt readily to customer feedback — but outsourcing automakers received a different benefit: because parts suppliers made better parts than automakers' own initial in-house efforts, outsourcers' *first* models were of higher quality than the first models of automakers making their own parts.
Type: Empirical (citing external economic research)
Evidence Provided: Named researchers (Sharon Novak, Scott Stern), a named data source (Consumer Reports ratings), cited to endnote 3, describing a clear trade-off (faster improvement over time via in-house control vs. higher initial quality via outsourced expertise).
Strength of Support: Strong — a specific, formally cited academic study with a named data source and a clearly stated, non-obvious trade-off (initial quality vs. rate of improvement) rather than a simple "outsourcing is better/worse" finding.
```

```
Claim: If AI became cheap and accurate enough to substantially reduce weather-related uncertainty for airlines and consumer-preference uncertainty for automakers, it would reduce both industries' need to own capital equipment (airplanes, parts-manufacturing factories) for two related reasons: first, more reliably predictable contingencies ("ifs") allow companies to write more specific contracts covering those contingencies, making outsourcing to lower-cost partners/suppliers safer; second, better up-front prediction (e.g., of consumer satisfaction) reduces the need for costly mid-cycle adjustments or contract renegotiations, letting companies confidently commit to outsourced arrangements from the start. Notably, the airline scenario requires two distinct predictive capabilities, not one: AI would need to forecast weather events themselves *and separately* generate predictions for how best to deal with weather-related interruptions once they occur — predicting the event alone isn't sufficient to justify the contracting-out shift.
Type: Theoretical (thought experiment applying the "ifs and thens" framework)
Evidence Provided: A structured extension of the airline and automaker cases into a hypothetical "what if AI reduced this specific uncertainty" scenario, explicitly built on the three-ingredient framework from Ch.17.
Strength of Support: Strong as an internally consistent application of the chapter's own framework; explicitly hypothetical/forward-looking rather than a claim about an implemented outcome, and the chapter itself flags an important caveat (see Section 11) about complexity potentially offsetting this outsourcing effect.
```

```
Claim: According to Bureau of Labor Statistics data (Figure 18-1), bank tellers were not automated out of a job by the introduction of ATMs (developed in the 1970s, deployed extensively through the 1980s) — despite ATMs being explicitly designed to automate the teller role — but tellers were automated out of the specific bank-telling task; freed from the security burden and transactional cost of handling cash, bank branches proliferated (43% more branches in urban areas), in more shapes and sizes, staffed by people still anachronistically called "tellers" but now functioning as marketing and customer-service agents for bank products.
Type: Empirical
Evidence Provided: A specific figure (Figure 18-1, sourced to James E. Bessen, "How Computer Automation Affects Occupations: Technology, Jobs, and Skills," Boston University School of Law, Law and Economics Research Paper No. 15-49, October 2016), plus a specific quantified outcome (43% more urban bank branches).
Strength of Support: Strong — a specific, formally cited economics research paper with a supporting empirical figure, extending the book's established "task automation ≠ job elimination" argument (Ch.16) with a concrete, well-documented historical case.
```

```
Claim: The introduction of ATMs produced a significant organizational transformation because the new teller role required substantially more subjective judgment — the original teller tasks (cash handling) were, by definition, routine and easily mechanized, but the new tasks (discussing banking needs, advising on loans, working out credit card options) were more complicated, making it harder to evaluate whether a new teller was doing a good job, and shifting bank HR management from objective performance measures (e.g., queue length) toward subjective ones (e.g., performance reviews weighing task complexity and individual strengths/weaknesses) — a shift the chapter argues is generally difficult to implement because it requires substantial trust, since subjective reviews make it easier for a company to unfairly deny a bonus or promotion than objective measures would.
Type: Empirical/Interpretive
Evidence Provided: Direct extension of the ATM/teller case, combined with general HR-economics reasoning about the objective/subjective performance-measurement trade-off, and a named cautionary counter-case (Wells Fargo's account-manager fraud scandal, cited to endnote 5, as an example of what can go wrong when objective performance measures are used in a complex environment).
Strength of Support: Strong for the Wells Fargo reference (a well-documented, widely reported real scandal); the broader HR-economics reasoning is presented as standard economic logic rather than independently tested within this chapter.
```

```
Claim: Counterintuitively, better prediction increases (not decreases) the uncertainty a company has over the quality of human judgment-based work performed, because as machine predictions proliferate and judgment becomes the primary remaining human role, judgment quality is inherently hard to specify or monitor in a contract — meaning companies need to keep reward-function engineers and other judgment-focused workers in-house rather than contracting them out, even as AI simultaneously makes it easier to contract out prediction/data/action-focused labor and capital equipment.
Type: Interpretive (explicit "counterintuitively" framing by the authors)
Evidence Provided: A logical derivation from the chapter's own established premises (prediction/judgment complementarity, contract-specifiability logic), explicitly labeled by the authors as a counterintuitive implication rather than an independently tested empirical claim.
Strength of Support: Strong as a logically coherent extension of the book's core economic framework; the authors themselves flag it as the chapter's sharpest, most surprising point rather than presenting it as self-evident.
```

```
Claim: The AI startup Ada Support, which helps other companies interact with their customers via chat, had the opportunity to integrate its product into a large established chat provider's system (a tempting path to faster traction and a larger user base), but recognized that doing so would mean the established company would own the resulting feedback data on customer interactions — without which Ada would be unable to improve its product based on real-world usage — so Ada reconsidered and did not integrate until it could ensure it would own the resulting data, securing a pipeline of data for continual learning both immediately and into the future.
Type: Empirical (named startup case)
Evidence Provided: A specific, named company (Ada Support) and a described strategic decision process (considering, then declining, an integration opportunity specifically to preserve data ownership).
Strength of Support: Strong as a specific, named business case, though presented without a citation to an external source (e.g., an interview or press account), suggesting it may derive from the authors' direct knowledge (consistent with their CDL-adjacent vantage point).
```

```
Claim: Advertising has a fundamental targeting problem — captured in John Wanamaker's famous line, "Half the money I spend on advertising is wasted; the trouble is, I don't know which half" — because when an ad is shown to everyone visiting a website and the advertiser pays per impression, only a fraction of viewers are potential customers, depressing the advertiser's willingness to pay per impression; this was historically solved by building media outlets around specific audience interests (sports, finance, etc.), and more recently solved via browser cookies that let advertisers track users across websites and target ads based on browsing behavior (e.g., seeing pants ads on unrelated sites after visiting a pants-shopping site).
Type: Historical/Interpretive
Evidence Provided: A named historical quote (attributed to John Wanamaker, credited among others with creating the modern structure of media advertising), combined with a general economic description of the advertising-targeting problem and the cookie-based solution, cited to endnote 6.
Strength of Support: Strong for the Wanamaker quote as a well-known, frequently cited historical attribution; the broader economic argument about targeting and cookies is standard, well-established advertising-economics reasoning presented without additional formal citation.
```

```
Claim: Google, Meta, and Microsoft do not sell their rich data on user needs/preferences directly; instead, they effectively sell the *predictions* that data generates, bundled as part of an advertising service — when an advertiser buys ads through Google's network, the ad is shown specifically to users the network predicts are most likely to be influenced by it, and advertising through Meta or Microsoft yields similar results — meaning the advertiser buys the prediction without ever gaining direct access to the underlying data.
Type: Empirical/Interpretive
Evidence Provided: Named companies (Google, Meta, Microsoft) and a description of how their advertising networks function, cited to endnote 7, presented as the chapter's paradigm case of "selling predictions" as a distinct business model from "selling data."
Strength of Support: Strong — a specific, verifiable description of a well-known, real business model (targeted advertising via major ad networks), consistent with the book's established sourcing pattern.
```

```
Claim: Data's strategic value specifically depends on its uniqueness — if a company's data is not unique, it is hard to build a strategic business around a prediction machine using it, because there is no real, defensible pathway to learning that competitors couldn't also access; however, even non-unique data/predictions can still be operationally useful (e.g., helping an advertiser target the highest-value customer), meaning better prediction can help an organization without being a source of durable *strategic* advantage.
Type: Interpretive
Evidence Provided: Presented as a direct logical implication of the data-uniqueness argument, illustrated by the advertising-network example already established, without additional external citation.
Strength of Support: Strong as a logically coherent extension of standard competitive-strategy reasoning (the need for a defensible, non-replicable resource) to the specific context of data and prediction machines.
```

```
Claim: The strategic decision of whether to own data and predictions in-house versus purchase them from others depends on how central prediction machines are to a company's core strategy: if AI is merely an off-the-shelf input, a company can treat it like most companies treat energy (purchased from the market, without needing to own the underlying generation capacity), but if prediction machines are meant to be the center of a company's strategy, the company needs to control the data to keep improving the machine, meaning both data and the prediction machine must be kept in-house.
Type: Interpretive (strategic framework, revisiting the chapter's opening case)
Evidence Provided: Direct logical resolution of the chapter's opening physician-diagnosis case: because diagnosis (not prediction) is the doctor's core strategic decision, doctors can safely buy a prediction as an added input without needing to own the underlying data or prediction machine, whereas for the AI startup, prediction *is* the core of the business, so it must own both.
Strength of Support: Strong as the chapter's own explicit resolution of its opening motivating case, providing a clean, generalizable decision rule (is AI core to your strategy, yes/no) for the make-or-buy question central to the whole chapter.
```

## 4. Frameworks, Models, and Mental Models

```
Name: The three-domain model of AI's boundary-of-the-firm impact (Capital, Labor, Data)
Description: A structural framework, organized as the chapter's own three named sections ("Impact of AI: Capital," "Impact of AI: Labor," "Impact of AI: Data"), applying the same uncertainty-reduction → contract-specificity → make-or-buy logic across three distinct resource categories a firm must decide whether to own or outsource.
Components: Capital (e.g., airplanes, parts-manufacturing factories — AI-driven prediction increases outsourcing/contracting by expanding specifiable "ifs"); Labor, split into two opposite sub-effects (prediction/data/action-focused labor becomes easier to contract out, following the same logic as capital, while judgment-focused labor becomes *more* valuable to keep in-house, because judgment resists contractual specification); Data (a company must decide whether to own data and predictions in-house or purchase them, depending on whether unique data/AI is core to its strategic advantage).
How It Works: For each domain, the analyst asks: does better prediction reduce a specific uncertainty in this domain enough to allow more explicit contracting? If yes for capital/prediction-labor/non-unique-data, outsourcing becomes more attractive; if the domain is judgment or strategically core unique data, the opposite occurs and in-house ownership becomes more valuable.
When It Is Useful: As a systematic checklist for C-suite strategic planning once an organization has identified that AI is strategically significant (per Ch.17's three-ingredient test) — helps translate "AI matters strategically" into concrete make-or-buy decisions across a firm's major resource categories.
Limitations: The chapter itself notes the capital analysis holds network/product complexity fixed, and acknowledges it's unclear whether AI-enabled complexity increases might offset the outsourcing-favoring effect of better prediction — the framework's predictions are directionally clear but the chapter is explicit that magnitudes and net effects are genuinely uncertain "at this stage."
```

```
Name: The "core to strategy" test for AI make-or-buy decisions
Description: A simple decision rule for whether a company should own its prediction machine and underlying data in-house, or purchase predictions/data as external inputs.
Components: A single diagnostic question — is the prediction machine merely an input you can take off the shelf (like energy), or is it meant to be the center of your company's strategy?
How It Works: If AI is a peripheral input, purchase it from the market like any commodity input, without needing to own the underlying data-generation capability. If AI is core to the company's competitive strategy, both the data and the prediction machine must be controlled in-house, because ongoing strategic advantage requires the ability to keep improving the machine via proprietary data.
When It Is Useful: As the chapter's final, distilled decision heuristic — directly resolves the opening diagnosis-vs-prediction case and generalizes to any company facing a build-vs-buy AI decision.
Limitations: The chapter doesn't provide a rigorous method for determining in advance whether AI *should* be core to a given company's strategy — that determination itself may require the kind of AI canvas/workflow-decomposition analysis introduced in Ch.14–15.
```

```
Name: The five-scenario "where does the data reside" strategic taxonomy
Description: A specific, actionable checklist for evaluating data-acquisition strategy based on who currently holds the data a company needs, with a different implied strategy for each scenario.
Components: (1) Data resides with an exclusive/monopoly provider — risk that the provider appropriates the entire value of your AI. (2) Data resides with competitors — there may be no strategy that makes procuring it worthwhile. (3) Data resides with consumers — it can be exchanged for a better product or higher-quality service. (4) Mutual-value data — a data swap may be possible if you and another party each hold data valuable to the other. (5) Data resides with multiple providers — may require a more complicated arrangement combining purchased data and purchased predictions.
How It Works: A company facing an AI make-or-buy decision should first identify which of these five scenarios describes its actual data-access situation, since the correct strategic response (build defenses against value appropriation, abandon the pursuit, offer a product/service exchange, negotiate a swap, or assemble a combined purchase arrangement) differs sharply across scenarios.
When It Is Useful: As a practical diagnostic once a company has determined (via the "core to strategy" test) that data ownership matters, for figuring out concretely how to pursue that data given real-world constraints on who already holds it.
Limitations: The chapter doesn't specify how to determine which scenario applies in ambiguous or mixed cases (e.g., data held by both a near-monopoly provider and multiple smaller providers simultaneously), nor does it rank the five scenarios by typical difficulty or cost.
```

## 5. Research and Evidence

```
Study Name / Reference: Forbes and Lederman's study of US airline industry organization
Researchers: Silke Forbes and Mara Lederman (economists)
Year: Not specified within the visible chapter text (cited to endnote 2); study examines industry organization "around the turn of the millennium"
Sample/Data: The organizational structure of US major airlines and their regional partner airlines (e.g., United/American vs. American Eagle/SkyWest)
Method: Not detailed within the visible chapter text
Key Finding: Weather-related uncertainty, not merely cost differences, drives the choice of which routes majors retain direct control over versus contract out to lower-cost regional partners; some studies cited within found senior major-airline pilots earn 80% more than regional-partner counterparts.
Caveats/Limitations Noted: None specified within the visible chapter text.
```

```
Study Name / Reference: Novak and Stern's study of luxury automaker parts-sourcing and quality improvement
Researchers: Sharon Novak and Scott Stern (economists)
Year: Not specified within the visible chapter text (cited to endnote 3)
Sample/Data: Luxury automakers, comparing those that manufacture their own parts versus those that outsource, measured via Consumer Reports customer ratings
Method: Comparing rate of model-year-over-model-year quality improvement (using Consumer Reports data) between in-house-parts and outsourced-parts automakers
Key Finding: In-house-parts automakers improved faster year over year (better control enabling adaptation to customer feedback), but outsourced-parts automakers had higher-quality *initial* models (because specialized suppliers made better parts than automakers' own first attempts) — a genuine trade-off rather than a one-directional finding.
Caveats/Limitations Noted: None specified within the visible chapter text.
```

```
Study Name / Reference: Bessen's study of ATM adoption and bank teller employment
Researchers: James E. Bessen
Year: October 3, 2016 (Boston University School of Law, Law and Economics Research Paper No. 15-49)
Sample/Data: US bank teller employment and ATM installation counts, 1970–2010s (Figure 18-1), sourced to Bureau of Labor Statistics data
Method: Time-series comparison of tellers employed versus ATMs installed
Key Finding: Despite ATMs being designed to automate the teller role, tellers were not automated out of a job overall — teller employment did not follow the sharply declining pattern one might expect given rising ATM installation; instead, the *content* of the teller job shifted toward marketing/customer service, and total bank branches (and teller employment) grew as branches proliferated (43% more in urban areas).
Caveats/Limitations Noted: None specified within the visible chapter text; the source is a formally cited working paper (SSRN 2690435).
```

## 6. Experiments

None identified as formal controlled experiments — the chapter's evidence is drawn from cited academic economics research (Forbes/Lederman, Novak/Stern, Bessen), named business cases (Ada Support, Google/Meta/Microsoft advertising), and a historical quote (Wanamaker) rather than described experimental studies.

## 7. Cases and Stories

```
Case Title: The diagnosis-vs-prediction startup (chapter frame narrative)
People / Organization: Co-author Joshua Gans; an unnamed early-stage machine learning company
Context: The chapter's opening and closing case, bookending the entire chapter's framework — introduced as a puzzle at the start, resolved explicitly using the chapter's full "core to strategy" logic at the end.
What Happened: See Section 3 for full details.
Outcome: The venture was advised to sell only the underlying prediction rather than a full binary diagnosis, eliminating regulatory-approval requirements, the need for early partnership with established companies, and the technical burden of translating prediction into diagnosis — replaced instead by the much simpler question of what accuracy threshold constitutes a valuable prediction.
Concept Illustrated: The boundary of the firm as AI's central strategic battleground; the "core to strategy" test for AI make-or-buy decisions (the doctor's core strategic decision is diagnosis, not prediction, so the doctor can safely buy the prediction as an input).
Why This Case Is Useful: A concrete, real (if anonymized) consulting anecdote that gives the entire chapter's abstract firm-boundary economics a memorable, practical throughline — readers encounter the puzzle before the framework and see it resolved after, reinforcing retention.
Potential for Reuse: High
```

```
Case Title: US airlines' major-vs-regional-partner route allocation
People / Organization: United, American (major airlines); American Eagle, SkyWest (regional partners); Silke Forbes, Mara Lederman (researchers)
Context: The chapter's primary illustration of how uncertainty (not just cost) drives firm-boundary decisions, setting up the "Impact of AI: Capital" section's hypothetical extension.
What Happened: See Section 3 and Section 5 for full details.
Outcome: Majors retain direct control over weather-uncertainty-prone routes despite regional partners' lower costs, because uncertainty (not cost) is the deciding factor in this boundary choice.
Concept Illustrated: The boundary of the firm as driven by uncertainty rather than cost alone; sets up the chapter's hypothetical about how AI-driven weather prediction could shift this balance toward more contracting-out.
Why This Case Is Useful: A specific, real industry case with a clear, counterintuitive puzzle (why do majors keep the more expensive option?) resolved by a precise economic mechanism (uncertainty, not just cost) that directly generalizes to the chapter's AI argument.
Potential for Reuse: High
```

```
Case Title: Luxury automakers' parts-sourcing trade-off
People / Organization: Unnamed luxury automakers; Sharon Novak, Scott Stern (researchers); Consumer Reports (data source)
Context: The chapter's second illustration of uncertainty-driven firm-boundary decisions, paired with the airline case to establish the general pattern before the AI-specific hypothetical.
What Happened: See Section 3 and Section 5 for full details.
Outcome: In-house parts manufacturing yields faster year-over-year improvement (via customer-feedback control); outsourced parts manufacturing yields higher initial quality (via supplier specialization) — a genuine, non-obvious trade-off.
Concept Illustrated: The "ifs and thens" framework and the boundary of the firm, applied to a manufacturing (rather than services/routing) context, broadening the chapter's evidence base beyond a single industry.
Why This Case Is Useful: Complements the airline case by showing the same uncertainty-driven boundary logic applies to a physical-manufacturing context, with a distinct, memorable trade-off (initial quality vs. rate of improvement) that's easy to teach.
Potential for Reuse: High
```

```
Case Title: ATMs and the transformation (not elimination) of the bank teller job
People / Organization: Banks (unnamed generally); James E. Bessen (researcher); Wells Fargo (cautionary counter-case)
Context: The chapter's central "Impact of AI: Labor" case, illustrating both the judgment-shift argument and the objective-vs-subjective performance-measurement trade-off.
What Happened: See Section 3 and Section 5 for full details.
Outcome: Tellers were automated out of the routine cash-handling task, not out of a job; the role shifted toward marketing/customer service (requiring more subjective judgment), branches proliferated (43% more in urban areas), and HR management shifted toward relational, trust-based, subjective performance evaluation.
Concept Illustrated: Judgment's resistance to contracting; the objective-vs-subjective HR management trade-off, with Wells Fargo's account-fraud scandal as a cautionary example of what can go wrong when objective performance measures are misapplied in a complex environment.
Why This Case Is Useful: Directly extends the book's established "task automation ≠ job elimination" argument (Ch.16) with a rigorously documented, quantified historical case, while adding new content specific to this chapter (the HR-management/contract-specificity angle).
Potential for Reuse: High
```

```
Case Title: Ada Support's decision to prioritize data ownership over faster distribution
People / Organization: Ada Support (machine learning startup); an unnamed large established chat provider
Context: The chapter's primary "Impact of AI: Data" case for AI startups specifically, illustrating the strategic stakes of data ownership.
What Happened: See Section 3 for full details.
Outcome: Ada declined an integration opportunity that would have accelerated user growth but ceded data ownership, waiting until it could secure a data pipeline it would own, both immediately and going forward.
Concept Illustrated: Data ownership as a distinct strategic axis, separate from prediction technology itself — for an AI startup specifically, owning the data that enables ongoing learning can matter more than short-term distribution advantages.
Why This Case Is Useful: A specific, real (if not deeply detailed) startup decision that makes the abstract "own your data" strategic principle concrete and immediately relatable for any reader building or advising an AI-dependent business.
Potential for Reuse: High
```

```
Case Title: Online advertising's data economy — cookies, targeting, and "selling predictions"
People / Organization: John Wanamaker (historical quote); Google, Meta, Microsoft (named companies); unnamed advertising exchanges/data brokers
Context: The chapter's most extensively developed "Impact of AI: Data" case, illustrating the full spectrum of data-ownership strategies (selling data, buying data, and selling predictions instead of data).
What Happened: See Section 3 for full details.
Outcome: Distinguishes three distinct business models: (1) websites/data brokers selling raw visitor data to advertisers/exchanges; (2) companies like Google/Meta/Microsoft choosing to build proprietary ad networks specifically to own valuable consumer-preference data; (3) those same companies then selling *predictions* generated from that data (bundled with ad placement) rather than selling the raw data itself. Companies buy advertiser data for two distinct reasons that both serve the same goal of focusing ad spend on high-value customers: data that helps identify high-value customers, and separately, data that helps them avoid wasting ad spend on low-value customers.
Concept Illustrated: Data ownership as a distinct strategic axis; "selling predictions" as a business model distinct from "selling data"; data uniqueness as the determinant of strategic (versus merely operational) value.
Why This Case Is Useful: A comprehensive, real-world illustration spanning the full range of data/prediction business models discussed in the chapter, using universally recognized companies (Google, Meta, Microsoft) that make the abstract economic principles immediately concrete.
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: The boundary of the firm shifting based on uncertainty, not cost
Example: US airlines retaining control of weather-uncertain routes despite regional partners' 80%-lower pilot costs.
Why It Works: A sharp, counterintuitive puzzle (why keep the more expensive option?) with a precise, citable economic resolution (uncertainty, not cost, drives the boundary) that directly motivates the chapter's AI argument.
Possible Alternative Domain: Business, Economics
```

```
Concept: Task automation changing a job's content without eliminating the job
Example: ATMs automating cash-handling but not tellers, who shifted toward marketing/customer service and grew in number as branches proliferated.
Why It Works: A historically grounded, quantified (43% more urban branches), formally cited case that extends a principle already established in Ch.16 with fresh economic content (the HR-management/contract-specificity angle).
Possible Alternative Domain: Business, AI, Labor Economics
```

```
Concept: "Core to strategy" as the deciding factor in AI build-vs-buy decisions
Example: The opening diagnosis-vs-prediction startup case, resolved at the chapter's close.
Why It Works: A real, memorable frame narrative that gives an abstract strategic principle a concrete before/after resolution, modeling exactly the kind of reasoning a reader should apply to their own AI strategy question.
Possible Alternative Domain: Business, AI, Healthcare
```

## 9. Counterintuitive Insights

```
Insight: Better prediction increases (not decreases) the uncertainty a company has over the quality of human judgment-based work performed.
Common Belief: Better predictive technology should generally reduce uncertainty across a business, including uncertainty about how well employees are performing.
Author's Argument: As AI takes over more prediction/data/action-focused tasks, judgment becomes the primary remaining human role — but judgment quality is inherently hard to specify in a contract or monitor externally (if it could be well-specified, it could simply be programmed into a machine instead), so a company's uncertainty specifically *about the quality of its judgment-focused workers* actually rises as AI diffuses, making it strategically necessary to keep such workers in-house rather than contracting them out.
Evidence: Derived as a logical consequence of the chapter's own established premises (prediction/judgment complementarity from Ch.9, contract-specifiability logic established earlier in this chapter).
Why It Is Surprising: It inverts the expectation that "more AI/prediction = less uncertainty everywhere" — showing instead that AI's uncertainty-reducing effect is domain-specific, and can actually *increase* a specific, important kind of organizational uncertainty (about judgment quality) even while reducing others.
```

```
Insight: ATMs, a technology explicitly designed to automate bank tellers, were followed by bank branches proliferating 43% in urban areas and tellers not losing their jobs in aggregate.
Common Belief: A labor-saving automation technology explicitly designed to eliminate a specific job function should reduce employment in that role.
Author's Argument: Freed from the security burden and transactional cost of manual cash handling, banks found it profitable to open many more branches, redeploying tellers into higher-value marketing/customer-service roles rather than eliminating the position — extending the Ch.16 "task automation ≠ job elimination" pattern with a case where the *aggregate* employment number actually appears to have grown alongside the automating technology's adoption.
Evidence: Bureau of Labor Statistics data and Bessen's formally cited research (Figure 18-1), showing the ATMs-installed and tellers-employed time series alongside each other.
Why It Is Surprising: The name "automatic teller machine" itself announces an intention to replace tellers, making the actual historical outcome (branch/employment growth) a sharp reversal of the technology's own stated purpose.
```

## 10. Unique or Unusual Ideas

```
Idea: Treating AI as an input that should be evaluated exactly like energy — purchased from the market without owning underlying generation/production capability — whenever it is not core to a company's strategy, explicitly de-glamorizing AI adoption for the majority of companies for whom it is not a strategic centerpiece.
Why It Seems Unique: Pushes back against a pervasive business narrative that every company must deeply invest in owning AI capability, offering instead a calibrated, resource-conserving default (treat it like a commodity input) unless a specific strategic test is met.
Potential Connection to Other Topics: Broader make-or-buy/vertical-integration theory in industrial organization economics, and cloud computing's own "compute as a utility" analogy.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: The chapter's capital-impact analysis (better prediction → more outsourcing) explicitly holds network/product complexity fixed, but the chapter itself acknowledges this may not hold: up-front prediction confidence might instead enable airlines/automakers to pursue *more* complex arrangements or products, and "better prediction drives more outsourcing, while more complexity tends to reduce it" — creating two opposing forces whose net effect the authors admit is genuinely unclear "at this stage."
Author's Position: Stated explicitly and honestly as an open empirical question rather than resolved one way — the authors offer a hedged prediction ("newly feasible complex processes might be done in-house, [while] many of the simpler processes previously completed in-house will be outsourced") rather than a clean directional claim.
Possible Counterargument: A reader might push the authors to specify under what conditions the complexity-increase effect dominates versus the outsourcing-favoring effect, since without such a rule the chapter's core capital-impact claim is more a plausible hypothesis than a confident prediction.
What Evidence Would Help Resolve It: Empirical tracking of actual outsourcing ratios in industries recently gaining access to significantly improved AI-driven prediction, to see which force empirically dominates — not available at the time of the book's writing.
```

## 12. Quotable Ideas

```
Paraphrase (short): Half the money I spend on advertising is wasted; the trouble is, I don't know which half.
Why the Idea Matters: A famous, historically resonant articulation of the fundamental advertising-targeting problem that the chapter's entire data-economics discussion (cookies, targeting, selling predictions) is ultimately a technological response to.
Source Location: Book p.199, attributed to John Wanamaker
```

```
Paraphrase (short): Counterintuitively, better prediction increases the uncertainty you have over the quality of human work performed: you need to keep your reward function engineers and other judgment-focused workers in-house.
Why the Idea Matters: The chapter's own explicit statement of its sharpest, most counterintuitive finding, directly usable as a standalone strategic principle.
Source Location: Book p.198
```

## 13. Psychology Connections

None identified — the chapter is primarily economic/organizational in content, with HR management discussed through an economic lens (contract theory, trust, incentive design) rather than a psychological one.

## 14. Mathematics and Decision Science Connections

```
Connection: The "ifs and thens" contracting framework is a direct, informal application of contract theory and incomplete-contracts economics — the idea that a contract can only govern contingencies that can be explicitly specified in advance, and that reducing uncertainty (via prediction) expands the space of contractible contingencies.
Connection: The Novak/Stern automaker trade-off (faster improvement vs. higher initial quality) is a concrete example of a two-dimensional optimization trade-off, where no single strategy (in-house vs. outsourced) dominates on both dimensions simultaneously.
```

## 15. Sports Connections

None identified in the chapter's direct examples; no forced inference added.

## 16. AI and Machine Learning Connections

```
Direct examples from the book: The hypothetical medical-diagnosis-prediction startup; the hypothetical AI-driven weather-contingency prediction for airlines; the hypothetical AI-driven consumer-satisfaction prediction for automakers; Ada Support's customer-interaction AI and its data-pipeline strategy; Google/Meta/Microsoft's advertising-targeting prediction systems.
Inferred connection (my own): The chapter's "data and prediction machines are complements" argument, and its resulting build-vs-buy decision rule, maps closely onto contemporary discussions of "data moats" and defensibility in AI startup strategy — the question of whether a company's proprietary data pipeline (not just its model architecture) constitutes a durable competitive advantage, a live and unresolved debate in AI industry strategy discourse that this 2018 chapter anticipates in general economic terms.
```

## 17. Content Creation Opportunities

```
Idea Title: "Why the 'Automatic Teller Machine' Didn't Kill a Single Teller Job"
Format: YouTube Short | Community Post
Application Domain: AI | Business | Labor Economics
Hidden Principle: Optimization
Story Hook (Layer 1): A machine literally named to replace bank tellers rolled out across the 1980s. Decades later, more tellers exist than before — and bank branches grew 43%.
Principle Framework (Layer 2): Automating the transactional part of a job doesn't eliminate the job — it frees up capacity for the job to grow around its more valuable, judgment-heavy tasks, which is exactly why the same logic applies to today's AI-driven automation debates.
Best Supporting Case: The ATM/bank teller case (Section 7).
Character Application: Insight: Interpreter
Psychology Angle: None identified.
Math Angle: Direct — the ATM/teller employment time series (Figure 18-1).
Sports Angle: None identified.
Business Angle: Direct — a concrete rebuttal to "automation kills jobs" narratives, grounded in formal research.
Investing Angle: Inferred — evaluating labor-market impact predictions for AI-exposed industries using this historical precedent.
History Angle: Direct — 1970s–1980s ATM rollout history.
AI Angle: Direct — directly informs expectations about AI-driven job transformation today.
```

```
Idea Title: "Should Your Doctor Buy a Diagnosis or Just a Prediction?"
Format: YouTube Long-form
Application Domain: AI | Business | Healthcare
Hidden Principle: Optimization
Story Hook (Layer 1): A health-tech startup wanted to sell doctors a diagnosis. One question — "why are you providing doctors with diagnoses?" — changed everything about their business, their regulatory path, and their odds of success.
Principle Framework (Layer 2): The right boundary for your AI product isn't "do as much as possible" — it's the exact point where your prediction stops being your core strategic asset and starts being someone else's input, and getting that boundary right can eliminate entire categories of cost and risk.
Best Supporting Case: The diagnosis-vs-prediction startup case (Section 7).
Character Application: Sigma: Architect
Psychology Angle: None identified.
Math Angle: None identified.
Sports Angle: None identified.
Business Angle: Direct — a transferable framework for scoping any AI product's boundary.
Investing Angle: Direct — a due-diligence lens for evaluating whether an AI startup has correctly scoped its product boundary (over-scoping = unnecessary regulatory/partnership burden).
History Angle: None identified.
AI Angle: Direct — a real, first-hand strategic consulting case about AI product boundary-setting.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B04-C18-01
Title: The boundary of the firm as AI's central strategic battleground
Type: Concept
Summary: Prediction machines systematically shift what a company owns/controls in-house versus contracts out, because uncertainty (which AI reduces) is a key reason firms choose to own activities internally.
Source: Book p.191–192
Tags: firm boundary, strategy, uncertainty, outsourcing
Related Concepts: Three-ingredient test for AI strategic significance (Ch.17)
```

```
CARD ID: B04-C18-02
Title: "Ifs" and "thens" — prediction's effect on contract specificity
Type: Framework
Summary: Reduced uncertainty expands the number of contingencies ("ifs") that can be reliably forecast and written into explicit contracts ("thens"), making outsourcing safer and cheaper — illustrated by airlines (weather) and automakers (consumer satisfaction).
Source: Book p.193–195
Tags: framework, contracting, outsourcing, uncertainty
Related Concepts: The boundary of the firm
```

```
CARD ID: B04-C18-03
Title: Judgment's resistance to contracting
Type: Concept
Summary: Unlike capital and prediction/data/action-focused labor, judgment-focused labor becomes more valuable to keep in-house as AI diffuses, because judgment quality is inherently hard to specify or monitor in a contract — counterintuitively, better prediction increases uncertainty about judgment-work quality.
Source: Book p.197–198
Tags: judgment, contracting, in-house employment, counterintuitive
Related Concepts: Reward function engineering (Ch.9), job reconstitution (Ch.16)
```

```
CARD ID: B04-C18-04
Title: ATMs and the transformation of the bank teller job
Type: Case
Summary: ATMs automated the cash-handling task but not the teller job itself; tellers shifted to marketing/customer service (more subjective judgment), and bank branches grew 43% in urban areas — extending the "task automation ≠ job elimination" pattern with a new HR-management angle.
Source: Book p.195–198, Figure 18-1
Tags: case, ATM, bank tellers, HR management
Related Concepts: Judgment's resistance to contracting
```

```
CARD ID: B04-C18-05
Title: Data ownership as a distinct strategic axis
Type: Concept
Summary: Because data and prediction machines are complements, AI is of limited strategic value without data to feed it — a company can own data without prediction, own prediction without data (buying it as a bundled service), or need both if AI is core to its strategy.
Source: Book p.198–201
Tags: data ownership, strategy, complements
Related Concepts: Data grades (Ch.17), "core to strategy" test
```

```
CARD ID: B04-C18-06
Title: "Selling predictions" as a business model distinct from "selling data"
Type: Case
Summary: Google, Meta, and Microsoft don't sell their user data directly — they sell the predictions that data generates (bundled with ad placement), letting advertisers target likely-influenced users without ever accessing the underlying data.
Source: Book p.200
Tags: case, Google, advertising, data monetization
Related Concepts: Data ownership as a distinct strategic axis
```

```
CARD ID: B04-C18-07
Title: The "core to strategy" test for AI make-or-buy decisions
Type: Framework
Summary: If AI is a peripheral input, treat it like energy and buy it from the market; if AI is meant to be the center of your strategy, both data and the prediction machine must be owned in-house — resolves the chapter's opening diagnosis-vs-prediction case.
Source: Book p.201
Tags: framework, make-or-buy, AI strategy
Related Concepts: Data ownership as a distinct strategic axis, boundary of the firm
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: AI's central strategic effect is to redraw the boundary of the firm across capital, labor, and data: prediction machines reduce uncertainty, which increases contract-specificity and therefore outsourcing incentives for capital and prediction/data/action-focused labor, but the opposite holds for judgment-focused labor (which resists contractual specification and therefore should be kept in-house) and for data that is strategically core (which must be owned to sustain a durable AI-based advantage).
Top 5 Concepts: (1) The boundary of the firm as AI's central strategic battleground. (2) "Ifs" and "thens" — prediction's effect on contract specificity. (3) Judgment's resistance to contracting (counterintuitively increasing in-house employment). (4) Data ownership as a distinct strategic axis, separate from prediction technology. (5) The "core to strategy" test for AI make-or-buy decisions.
Top 3 Claims: (1) Airlines retain control of weather-uncertain routes despite regional partners' lower costs, because uncertainty (not cost) drives the boundary choice (Forbes/Lederman). (2) ATMs didn't eliminate the teller job but transformed its content toward judgment-heavy marketing/customer-service work, with branches growing 43% (Bessen). (3) Better prediction counterintuitively increases uncertainty about judgment-work quality, making in-house employment of judgment-focused workers more strategically necessary, not less.
Top 3 Cases: (1) The opening/closing diagnosis-vs-prediction startup frame narrative. (2) ATMs and the transformation of the bank teller job. (3) Online advertising's data economy (cookies, Google/Meta/Microsoft "selling predictions").
Top 3 Studies: (1) Forbes and Lederman's airline industry organization study. (2) Novak and Stern's luxury automaker parts-sourcing study. (3) Bessen's ATM/bank teller employment study — all three are formally cited peer-reviewed or working-paper-level academic economics research, an unusually research-dense chapter for the book.
Note on Forward Reference: The chapter explicitly states, at the opening of "Impact of AI: Data" (p.198), "In the next chapter, we explore issues concerning the strategic importance of investing in data collection" — confirming Chapter 19's focus before it begins.
Most Unique Idea: Treating AI as a commodity input (like energy) to be purchased from the market whenever it is not core to a company's strategy — explicitly de-glamorizing AI ownership for the majority of businesses.
Most Counterintuitive Idea: Better prediction increases (not decreases) a company's uncertainty about the quality of judgment-based human work, because judgment's resistance to contractual specification means its value — and the strategic necessity of keeping it in-house — rises precisely as AI diffuses elsewhere in the organization.
Biggest Weakness or Open Question: The chapter's capital-impact analysis explicitly acknowledges an unresolved tension between AI-driven outsourcing incentives and AI-enabled complexity increases (which favor in-house control), admitting the net effect is genuinely unclear "at this stage" rather than offering a confident directional prediction.
Best Content Opportunity: "Why the 'Automatic Teller Machine' Didn't Kill a Single Teller Job" (Section 17) — a historically grounded, quantified, immediately relevant rebuttal to contemporary "AI will destroy jobs" narratives, using a technology whose very name promised the opposite outcome from what actually occurred.
```
