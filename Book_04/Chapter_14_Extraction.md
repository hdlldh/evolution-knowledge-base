# Prediction Machines — Chapter 14: Deconstructing Workflows
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Extraction
**Source:** Book pages 147–155 (PDF pages 160–168)
**Date:** 2026-08-04
**Revised:** Per Chapter_14_Audit.md — corrected the Ford 400-person target framing; added the ROI-ranking implementation methodology, the full-automation condition, and the Ford triage mechanism; broadened the MBA bucket-risk claim; added two knowledge cards and one content idea.

BOOK:
Prediction Machines: The Simple Economics of Artificial Intelligence

AUTHOR:
Ajay Agrawal, Joshua Gans, Avi Goldfarb

CHAPTER:
14 — Deconstructing Workflows

---

## 1. Chapter Thesis

Like the computing revolution before it, AI is a general-purpose technology, and general-purpose technologies don't deliver large productivity gains just by being "thrown at" a problem or an existing process — they require the kind of deliberate process rethinking that the 1990s "reengineering" movement (Hammer and Champy) pioneered for classical computing. Because prediction is a key input to decision-making, AI has the potential to affect every decision, but the unit of AI tool design is not the job, the occupation, or the strategy — it's the task, and tasks are collections of decisions. The practical implication is that businesses must deconstruct their workflows into their constituent tasks and decisions before they can identify where AI tools will generate real returns, because AI tools change workflows in two distinct ways: by rendering some existing tasks obsolete (removing them from the workflow) and by adding new tasks that weren't previously worth doing. Real historical reengineering cases (Ford, Mutual Benefit Life) and a worked hypothetical AI example (MBA admissions) illustrate that the full benefit of a prediction machine typically requires redesigning the workflow around it, not simply inserting it into an unchanged process.

## 2. Key Concepts

```
Concept Name: The productivity paradox and the reengineering response
Definition: The historical observation (attributed to Nobel laureate Robert Solow) that computing technology's economic benefits were slow and hard to detect in aggregate productivity statistics despite computers being visibly "everywhere," which motivated a 1990s business movement called "reengineering" (associated with Michael Hammer and James Champy's 1993 book *Reengineering the Corporation*) arguing that businesses needed to step back from their existing processes, outline their actual objectives, study their workflows, identify the tasks required to achieve those objectives, and only then ask whether computers had a role — rather than simply inserting computers into unchanged existing processes.
Why It Matters: Establishes the chapter's central historical analogy and warning: like computing, AI's productivity gains will not appear automatically or quickly just because the technology is powerful; they require the same kind of deliberate workflow redesign reengineering pioneered, and gains may similarly take time to materialize in mainstream businesses.
How the Author Uses It: Opens the chapter with Solow's quote ("You can see the computer age everywhere but in the productivity statistics") and Hammer and Champy's core argument, then uses this as the frame for the entire chapter's approach to AI tool deployment.
Related Concepts: Workflow/task/decision framework, the Ford and Mutual Benefit Life cases
```

```
Concept Name: The workflow → task → decision hierarchy (Figure 14-1)
Definition: A structural framework for analyzing where AI tools can be deployed: a workflow (an end-to-end business process) is composed of multiple tasks; each task is a collection of decisions (of the kind analyzed in Part Two — decisions built from prediction, judgment, data, and action, per Ch.8's anatomy of a decision); tasks within a workflow often share common structural elements but differ in the action that follows the decision; jobs, in turn, are collections of tasks (a theme developed further in Ch.16).
Why It Matters: Provides the chapter's central methodological claim — the correct "unit" for AI tool design is the task, not the job, occupation, or overall strategy — because a task is precisely the level at which decisions (and therefore predictions) live, making it the natural unit at which to ask "could a prediction machine improve this?"
How the Author Uses It: Introduced via Figure 14-1 (a workflow decomposed into tasks, each task decomposed into decisions, with jobs shown as collections of tasks); applied throughout the chapter's subsequent cases (Ford, Mutual Benefit Life, the MBA example, and the iPhone keyboard) as the lens for identifying exactly where and how an AI tool intervenes.
Related Concepts: Anatomy of a decision (Ch.8), job redesign (previewed for Ch.16)
```

```
Concept Name: AI tools change workflows in two ways — removing tasks and adding tasks
Definition: The claim that deploying an AI tool within a workflow doesn't just improve an existing task in place; it can render some tasks entirely obsolete (removing them from the workflow because the AI's prediction makes the old task unnecessary) and can also make entirely new tasks worth doing for the first time (because cheap prediction unlocks activity that wasn't previously economical), and which of these two effects dominates — and by how much — differs for every business and every workflow.
Why It Matters: Warns against a narrow view of AI's impact as simply "automating an existing task faster" — the chapter argues the more consequential effects are structural (some tasks disappearing, genuinely new tasks appearing), which is precisely what requires workflow-level (not task-level) analysis to anticipate.
How the Author Uses It: Illustrated concretely by the MBA admissions thought experiment: a hypothetical ranking AI would remove the manual task of ranking applications, while adding/expanding the task of marketing the program to a much larger applicant pool (since evaluating additional applications would no longer be costly) and modifying tasks like scholarship/financial-aid allocation (now informed by much higher-confidence rankings).
Related Concepts: Workflow/task/decision hierarchy, the MBA admissions case
```

```
Concept Name: AI tools as point solutions
Definition: The observation that most current AI tools — including the large majority of AI startups the authors have observed through the CDL — are "point solutions": each is designed to generate one specific prediction to perform one specific task within one specific workflow, rather than being general-purpose problem-solvers applied indiscriminately across an organization.
Why It Matters: Reinforces why the task-level (not job- or strategy-level) unit of analysis is correct, and sets up a realistic expectation for how AI actually diffuses through an organization — not as one transformative system, but as potentially hundreds or thousands of narrow tools, each addressing a specific task.
How the Author Uses It: Grounded in the authors' direct observation of more than 150 AI companies through the CDL, each focused on a specific task within a specific workflow (e.g., a startup that predicts and highlights a document's most important passages; another that predicts and flags manufacturing defects; another that forecasts appropriate customer service responses); further illustrated by the claim that large companies are implementing hundreds or thousands of distinct AI tools (Google alone reportedly developing more than a thousand, spanning email, translation, and driving).
Related Concepts: Workflow/task/decision hierarchy, incremental vs. transformative AI impact
```

```
Concept Name: Incremental/inconspicuous impact vs. fundamental business change
Definition: A distinction between two different scales at which prediction machines create value: for many businesses, AI's impact will be incremental and largely inconspicuous (analogous to how AI quietly improves smartphone photo-sorting apps without changing how you fundamentally use the app), while for others — and for the reader specifically, the authors suggest — AI can lead to fundamental business change, which is the harder, more consequential case the rest of Part Three (and Part Four, Strategy) is oriented toward helping readers achieve.
Why It Matters: Manages expectations and segments the book's audience: not every AI deployment needs to be (or will be) transformative, and recognizing which category a given opportunity falls into is itself a useful diagnostic before investing in workflow redesign.
How the Author Uses It: Stated directly as a transition point, using the smartphone photo-app example as the "incremental" case before pivoting to the chapter's mission of helping readers pursue the more ambitious, fundamental-change case.
Related Concepts: AI tools as point solutions, reengineering (which targets fundamental, not incremental, change)
```

```
Concept Name: Full automation of a task requires prediction machines to also raise the returns to other task elements
Definition: The chapter distinguishes automating some decisions within a task from automating all of them: sometimes all the decisions within a task can be automated, or the last remaining un-automated decision can now be automated because of enhanced prediction, effectively removing humans from the task altogether — but for better and cheaper prediction alone to lead to this kind of pure automation, the prediction machine must also increase the returns to using machines in the other aspects of the task (judgment, data, action). Otherwise, the prediction machine is better employed working alongside human decision-makers rather than replacing them.
Why It Matters: Supplies the specific condition that determines whether a task ends up fully automated (humans removed) or remains human-AI collaborative, directly connecting this chapter's workflow/task framework back to Chapter 12's treatment of full automation.
How the Author Uses It: Introduced immediately after the Goldman Sachs 146-task example and just before Figure 14-1, as a conceptual bridge between "AI can enhance decisions" and "AI can redesign/automate entire workflows."
Related Concepts: Full automation (Ch.12), the workflow-task-decision hierarchy
```

## 3. Key Claims

```
Claim: Robert Solow's productivity paradox — that computing's economic impact was hard to detect in aggregate productivity statistics despite computers being visibly ubiquitous — reflects a general-purpose technology's characteristic slow diffusion into measurable economic gains, and this same pattern is likely to recur with AI.
Type: Historical/Interpretive
Evidence Provided: Direct quote attributed to Solow ("You can see the computer age everywhere but in the productivity statistics"), cited to endnote 1, presented as the motivating puzzle behind the reengineering movement.
Strength of Support: Strong as a historical attribution (a well-known, frequently cited economics quote), though the chapter's extension of this pattern to predict AI's future trajectory is a reasoned analogy rather than an independently evidenced forecast.
```

```
Claim: Ford's 1980s accounts payable reengineering — prompted by the realization that Ford's 500-person North American accounts payable department was five times larger than competitor Mazda's five-person equivalent — succeeded not merely by adding computers to the existing process but by using a shared database system to eliminate the specific bottleneck (purchase-order mismatch reconciliation, a difficult task that slowed down the entire system because every order flowed at the speed of the hardest ones), ultimately shrinking the department by 75% and making the whole process significantly faster and more accurate.
Type: Empirical/Historical
Evidence Provided: Specific figures (500 North American accounts payable employees; a target of 400, a 20% reduction — explicitly described by the chapter as "not unrealistic," i.e., a conservative, readily achievable goal, given that Mazda's comparable department ran on just 5 people; the resulting 75% department-size reduction), cited to endnote 2; description of the specific process bottleneck (purchase-order reconciliation) and the shared-database solution.
Strength of Support: Strong — specific, quantified, comparative figures (Ford's 500 vs. Mazda's 5; the resulting 75% reduction) drawn from a well-documented, frequently-cited business case (Hammer and Champy's own example).
```

```
Claim: Mutual Benefit Life's insurance application process — which involved 19 people across 5 departments performing 30 distinct steps, and which could theoretically be completed in a single day of active work but actually took 5 to 25 days due to transit time and compounding inefficiencies attaching themselves to a slow-moving process — was dramatically improved (to between 4 hours and a few days) by consolidating authority over an application to a single person, enabled by a shared database powered by an enterprise computer system.
Type: Empirical/Historical
Evidence Provided: Specific process figures (19 people, 5 departments, 30 steps, 1 day of actual active-processing time versus 5–25 days of actual elapsed time; resulting 4-hours-to-few-days processing time after reengineering), cited to endnote 3.
Strength of Support: Strong — specific, quantified before/after figures from a well-documented historical reengineering case, illustrating that reengineering's benefit is not limited to headcount reduction (unlike the Ford case) but can instead be primarily about service-quality/speed improvement.
```

```
Claim: Not every reengineering case is about reducing headcount, even though headcount reduction is what many people think of first when they hear the term — reengineering can instead (or additionally) improve service quality, as the Mutual Benefit Life case demonstrates.
Type: Interpretive
Evidence Provided: Direct contrast between the Ford case (headcount-focused) and the Mutual Benefit Life case (speed/quality-focused), explicitly flagged as a corrective to a common misconception.
Strength of Support: Strong as a logical point given the two cases already presented, though it functions more as an interpretive framing than an independently tested claim.
```

```
Claim: Goldman Sachs's initial public offering (IPO) process, as described by CFO R. Martin Chavez, consists of 146 distinct tasks, "many" of which Chavez characterized as "begging to be automated," and many of these 146 tasks are predicated on decisions that AI tools will significantly enhance — meaning AI's role in Goldman Sachs's future transformation is likely to be substantial.
Type: Empirical/Interpretive
Evidence Provided: A specific figure (146 distinct tasks in the initial public offering process) and a direct characterization attributed to Chavez ("begging to be automated"), cited to endnote 4; the authors' own forward-looking claim that AI's role in this transformation will be a "major part of the story" told about Goldman Sachs a decade from the book's writing.
Strength of Support: Strong for the factual claim (a specific, named-executive-sourced figure); the forward-looking prediction about AI's future centrality to Goldman Sachs's transformation is the authors' own interpretive judgment rather than an independently verifiable fact at time of writing.
```

```
Claim: The Creative Destruction Lab (CDL) has hosted more than 150 AI companies, each focused on developing an AI tool addressing a specific task within a specific workflow (not a general-purpose or job-level solution), and large companies are correspondingly implementing hundreds or thousands of distinct AI tools across their own workflows — with Google specifically reported to be developing more than a thousand different AI tools spanning tasks from email to translation to driving.
Type: Empirical
Evidence Provided: The specific CDL company count (150+) drawn from the authors' own direct institutional observation (established in Ch.1); specific named startup examples (a tool predicting/highlighting a document's most important passages; a tool predicting/flagging manufacturing defects; a tool forecasting appropriate customer service responses); the Google figure (1,000+ tools), cited to endnote 5.
Strength of Support: Strong for the CDL figures (first-hand institutional knowledge, consistent with the book's established authorial vantage point); Moderate for the Google figure, which relies on an external citation not detailed within the visible chapter text.
```

```
Claim: A hypothetical (explicitly fictitious/"magical") AI tool that could rank MBA applicants accurately using application data, video interviews, and publicly available social media information — trained on historical data linking past applications to later outcomes/success — would not just speed up the existing task of ranking applicants but would ripple outward to change decisions throughout the entire recruitment workflow: early-offer timing (to preempt competing schools), financial-incentive/scholarship allocation, special attention (faculty lunches, alumni access), application-fee policy, applicant-pool size/marketing reach, and the overall timing of the admissions decision itself (potentially becoming "nearly instantaneous").
Type: Theoretical (explicitly hypothetical thought experiment)
Evidence Provided: A fully worked-through hypothetical scenario walking through each affected downstream decision, grounded in a real institutional context (the authors' own familiarity with MBA recruiting workflows) but using an admittedly fictional ("magical") prediction technology.
Strength of Support: Strong as an illustrative thought experiment demonstrating the chapter's core "removing and adding tasks" claim in concrete, relatable detail, though explicitly not an empirical finding — the authors are transparent that the specific technology described doesn't yet exist in this form.
```

```
Claim: Current, real-world systems for ranking MBA applications rely on coarse, three-bucket assessments (a: clearly should get an offer; b: should get an offer if bucket-a candidates decline; c: no offer at all), which creates meaningful risk-management challenges — specifically, avoiding placing a candidate in bucket "c" when they should be in "a" or even "b" (and, symmetrically, avoiding placing a candidate in "a" when they should be lower in the priority queue) — precisely because current assessment criteria mix objective and subjective, multidimensional factors.
Type: Empirical/Interpretive
Evidence Provided: Direct description of the three-bucket system as a real, current practice, presented from the authors' own institutional experience/familiarity with MBA recruiting (as professors), without external citation.
Strength of Support: Moderate — presented as an insider, experience-based description rather than a formally cited industry-wide study, but plausible and specific enough (three named buckets with clear decision logic) to be credible as a real practice.
```

```
Claim: A dramatically more accurate and cheaper predictive ranking technology would increase (not just satisfy) an MBA program's demand for a larger applicant pool, because the cost of evaluating additional applications would fall dramatically — potentially motivating schools to lower application fees toward zero, since sorting through more applications would no longer carry meaningful cost, provided the technology could also assess application seriousness.
Type: Theoretical
Evidence Provided: Extension of the chapter's hypothetical MBA AI scenario, applying standard economic reasoning (lower marginal cost of evaluation → higher optimal quantity demanded) already established in earlier chapters (e.g., Ch.2's "cheap means more usage" logic).
Strength of Support: Moderate — a logically coherent extension of established economic principles to a hypothetical technology, not an empirically tested claim.
```

```
Claim: Apple's iPhone keyboard team, facing a three-week deadline (with the whole keyboard project's viability at stake) to solve the problem of an unusably error-prone small on-screen QWERTY keyboard (given the iPhone's 3.5-inch LCD screen and correspondingly tiny keys), solved the problem using 2006-era machine learning to build a predictive algorithm that dynamically expanded the touch-target area around whichever key a user was statistically most likely to press next, without changing the visible key layout the user saw.
Type: Empirical/Historical
Evidence Provided: Specific details (the iPhone launched in 2007; as late as 2006 the keyboard was "terrible" and essentially unusable even for text messages; the "biggest science project" characterization of the soft keyboard; the three-week deadline for finding a solution, framed as potentially "killing the whole project" if unsolved; the mechanism of dynamically expanding the invisible touch-target area based on predicted next-letter probability, e.g., after typing "t," the area around "h" expands since "th" is a highly probable sequence), cited to endnote 6.
Strength of Support: Strong — specific, dated, mechanistically detailed account of a famous, well-documented product development episode, presented with internal logic that is independently verifiable (the "th," "e," "i" sequence example is linguistically plausible and checkable).
```

```
Claim: The iPhone keyboard's predictive touch-target expansion worked specifically because of, not despite, the QWERTY layout's original design purpose (preventing adjacent mechanical typewriter keys from jamming by physically separating letters likely to be typed in sequence) — the same physical separation that solved a mechanical problem in the 19th century also meant that, on a touchscreen, the "next likely key" was almost always spatially distant from the "just-pressed key," giving the predictive algorithm room to expand the correct target without overlapping the wrong one.
Type: Interpretive
Evidence Provided: Direct explanation connecting QWERTY's historical mechanical-jamming-prevention rationale to its incidental modern benefit for touchscreen predictive typing, presented as the chapter's own analytical insight rather than an externally cited historical claim.
Strength of Support: Moderate — a plausible, internally consistent causal explanation, but presented as authorial interpretation/reasoning rather than a claim independently verified through, e.g., interviews with the original Apple engineers about their own understanding of why the solution worked.
```

```
Claim: What made the iPhone keyboard's predictive solution possible was Apple engineers first precisely understanding the actual workflow involved in using a keyboard (identify a key, touch it, move to another) and specifically recognizing, by breaking down that workflow, that a key did not need to be visually/physically identical to be correctly identified and touched — meaning understanding the workflow, not just having access to machine learning technology, was the critical enabling insight.
Type: Interpretive
Evidence Provided: Direct authorial statement generalizing from the iPhone case: "Understanding the workflow was critical for figuring out how best to deploy the AI tool. This is true of all workflows."
Strength of Support: Strong as the chapter's own explicit thesis statement/conclusion, directly tying the iPhone case back to the chapter's opening reengineering argument, though it functions as an interpretive synthesis rather than an independently testable empirical claim.
```

## 4. Frameworks, Models, and Mental Models

```
Name: The workflow-task-decision-job hierarchy (Figure 14-1)
Description: A four-level structural model for locating exactly where AI prediction tools can and should be deployed within a business, moving from the broadest level (workflow) down to the most granular (decision), with jobs shown as a cross-cutting collection of tasks.
Components: Workflow (an end-to-end business process, e.g., "MBA recruiting" or "processing a life insurance application"); Tasks (discrete sub-processes within the workflow, each a collection of related decisions); Decisions (the prediction-judgment-action units analyzed in Part Two, per Ch.8's anatomy of a decision); Jobs (collections of tasks, potentially spanning multiple workflows, developed further in Ch.16).
How It Works: Because prediction (and thus AI) operates at the decision level, and decisions aggregate into tasks, the correct unit for evaluating "should we use an AI tool here" is the task — not the job (too broad, mixing many unrelated decision types) or the overall strategy (too abstract). Businesses should decompose each workflow into its tasks, then each task into its constituent decisions, to systematically identify where prediction machines could plausibly help.
When It Is Useful: As the master diagnostic framework for any organization's AI adoption planning — used later in the chapter (MBA case) and referenced going into subsequent chapters on decomposing decisions (Ch.15) and job redesign (Ch.16).
Limitations: The chapter doesn't provide a formula for how granular a "task" decomposition should be, or how to handle tasks/decisions that span multiple workflows simultaneously — it's presented as a conceptual lens rather than a rigorously bounded methodology.
```

```
Name: Reengineering-style workflow redesign (Hammer and Champy's method, adapted for AI)
Description: A four-step process, adapted from 1990s computing-era reengineering, for realizing the full value of a general-purpose prediction technology: (1) step back and articulate the actual objective of a business process, independent of its current implementation; (2) study the existing workflow and identify the tasks required to achieve that objective; (3) only then evaluate whether/where a new technology (AI) has a role in those specific tasks; (4) redesign the workflow around the technology's capabilities, rather than simply inserting the technology into the unchanged existing process.
Components: An objective-first mindset (rather than technology-first); a task-level decomposition of the current workflow; an explicit technology-role evaluation per task; a willingness to remove or restructure existing tasks (not just augment them).
How It Works: Illustrated by both historical cases (Ford, Mutual Benefit Life) achieving large gains not from adding computers to an unchanged process, but from restructuring around a shared database that eliminated specific bottlenecks; the iPhone keyboard case shows the same logic applied to a much smaller-scale (but still workflow-level) problem — understanding the actual keyboard-use workflow (identify, touch, move on) before designing the predictive solution.
When It Is Useful: Whenever an organization is tempted to deploy an AI tool as a drop-in replacement within an unchanged process — this framework argues that approach will systematically undercapture AI's potential value, and that full value requires actively redesigning the surrounding workflow.
Limitations: Reengineering (in both its 1990s computing form and this AI-adapted form) requires significant upfront analytical investment (fully mapping tasks and decisions) before any AI deployment decision can be made, which the chapter doesn't quantify in terms of cost or time — a potential barrier to adoption the chapter doesn't directly address here (though it may be developed further in Ch.15/16).
```

```
Name: The ROI-ranking implementation methodology
Description: The chapter's own concrete, actionable process (stated in its Key Points, book p.155) for how a company should decide where and how to implement AI: break workflows down into tasks; estimate the ROI of building or buying an AI tool to perform each task; rank-order the candidate AI tools by ROI; implement starting from the top of the ranked list and work downward.
Components: Task-level workflow decomposition; per-task ROI estimation (build-or-buy); ranking; top-down sequential implementation; a fork in outcomes — some tasks yield an immediate benefit simply by dropping an AI tool into the existing workflow (increasing that task's productivity in place), while others yield no real benefit until the surrounding workflow is rethought/reengineered.
How It Works: A company doesn't need to reengineer every workflow before capturing any AI value — it can first triage which tasks are cheap, high-ROI, drop-in wins, and reserve full reengineering effort for tasks where a real benefit requires redesigning the workflow around the AI tool.
When It Is Useful: As a practical prioritization tool once the workflow-task-decision decomposition (Figure 14-1) has been done, for deciding in what order and with how much redesign effort to pursue AI adoption across an organization's many tasks.
Limitations: The chapter doesn't specify how to estimate ROI for a not-yet-built AI tool in practice, nor how to tell in advance whether a given task is a "drop-in" case or a "requires reengineering" case.
```

## 5. Research and Evidence

None identified as formally cited academic studies within this chapter — the chapter's evidence consists of historical business cases (Ford, Mutual Benefit Life, drawn from Hammer and Champy's book), a named-executive quote (Goldman Sachs's Chavez), the authors' own institutional data (CDL), and a well-documented product-development history (the iPhone keyboard), rather than cited academic research papers.

## 6. Experiments

None identified.

## 7. Cases and Stories

```
Case Title: Ford's 1980s accounts payable reengineering
People / Organization: Ford Motor Company; Mazda (comparison benchmark); Michael Hammer and James Champy (case popularizers, *Reengineering the Corporation*, 1993)
Context: The chapter's first historical illustration of reengineering, establishing the pattern that redesigning a workflow (not just adding computers to it) produces dramatic gains.
What Happened / Outcome: See Section 3 for full details. Ford's 500-person North American accounts payable department, benchmarked against Mazda's 5-person equivalent, was reengineered around a shared database that eliminated the purchase-order-reconciliation bottleneck (previously, the whole process moved at the speed of its hardest, most exception-laden cases). Specifically, the computer system's role was not uniform acceleration but triage: it could "sort the difficult from the easier cases and ensure the easier ones went through at a reasonable speed," while difficult cases still received dedicated handling — resulting in a 75% department-size reduction and faster, more accurate processing overall.
Concept Illustrated: Reengineering's core insight — identifying and restructuring around the actual process bottleneck, rather than simply computerizing the existing process — as a headcount-reduction-focused example.
Why This Case Is Useful: A classic, well-documented, quantified business case (drawn from the seminal reengineering text) with a clean before/after comparison (500 vs. eventual smaller department; benchmarked against Mazda's 5) that makes the reengineering concept concrete.
Potential for Reuse: High
```

```
Case Title: Mutual Benefit Life's insurance application processing reengineering
People / Organization: Mutual Benefit Life (life insurance company)
Context: The chapter's second historical reengineering illustration, deliberately contrasted with Ford to show reengineering isn't only about headcount reduction.
What Happened / Outcome: See Section 3 for full details. A 19-person, 5-department, 30-step application process that should have taken about a day of actual work but instead took 5–25 days (due to transit time and compounding inefficiencies) was reengineered by consolidating authority over each application to a single person, enabled by a shared database — reducing processing time to between 4 hours and a few days.
Concept Illustrated: Reengineering as a service-quality/speed improvement lever, not solely a cost/headcount reduction tool — broadening the reader's mental model of what "reengineering success" looks like.
Why This Case Is Useful: A specific, quantified (19 people, 5 departments, 30 steps, 5–25 days → 4 hours–few days) case that directly complements and contrasts with the Ford example, together giving a fuller picture of reengineering's range of benefits.
Potential for Reuse: High
```

```
Case Title: Goldman Sachs's 146-task IPO process and CFO R. Martin Chavez's "begging to be automated" remark
People / Organization: Goldman Sachs; CFO R. Martin Chavez
Context: A contemporary, named-executive-sourced example bridging the historical reengineering cases to the book's present-day AI context.
What Happened: Chavez remarked that many of the 146 distinct tasks in Goldman Sachs's initial public offering process were "begging to be automated." The authors note many of these 146 tasks are predicated on decisions that AI tools will significantly enhance.
Outcome: Used to predict that AI's role in Goldman Sachs's business transformation will be a major part of how the company's evolution is described a decade after the book's writing.
Concept Illustrated: A real, large-scale financial institution already applying task-level workflow decomposition (146 distinct tasks identified) to a core business process, directly paralleling the chapter's recommended methodology.
Why This Case Is Useful: A credible, named, contemporary (rather than purely historical) example that shows sophisticated organizations already thinking in exactly the task-decomposition terms the chapter recommends, lending real-world validation to the framework.
Potential for Reuse: High
```

```
Case Title: The Creative Destruction Lab's 150+ AI companies and Google's 1,000+ AI tools
People / Organization: Creative Destruction Lab (CDL); Google
Context: Used to establish the "AI tools as point solutions" concept with direct institutional evidence.
What Happened: The authors report having observed more than 150 AI companies through the CDL, each focused on developing a single AI tool for a specific task within a specific workflow — naming three illustrative examples: a startup predicting and highlighting a document's most important passages; another predicting and flagging manufacturing defects; another forecasting appropriate customer service responses and answering queries. Separately, large companies are said to be implementing hundreds or thousands of distinct AI tools, with Google specifically developing more than a thousand different AI tools spanning tasks from email to translation to driving.
Outcome: Establishes empirically (via the authors' own direct observation) that the realistic shape of AI adoption is many narrow, task-specific tools rather than a small number of general-purpose systems.
Concept Illustrated: AI tools as point solutions, and the resulting expectation that meaningful AI adoption within a large organization will look like proliferation across many discrete tasks, not a single transformative deployment.
Why This Case Is Useful: Combines the authors' unique first-hand institutional vantage point (CDL) with a large, well-known company (Google) to give both grounded, specific examples and a sense of scale.
Potential for Reuse: High
```

```
Case Title: The hypothetical (fictitious) MBA applicant-ranking AI
People / Organization: Not specified (a hypothetical MBA program, drawing on the authors' own professorial experience with recruiting workflows)
Context: The chapter's central, fully worked thought experiment demonstrating how a single new AI tool ripples through an entire workflow, both removing and adding tasks.
What Happened: The chapter walks through a three-part MBA recruitment workflow (a sales funnel encouraging applications; a process determining who receives offers; steps encouraging offer-recipients to accept) and describes current practice: candidates coarsely sorted into three buckets (a: clear offer, b: conditional offer if "a" candidates decline, c: no offer), a system that mixes objective and subjective, multidimensional judgment and carries real misclassification risk. The chapter then introduces a hypothetical "magical" AI that could rank all applicants accurately using application data, video interviews, and public social media information, trained on historical data linking past applications to later success outcomes. It walks through the downstream effects: faster/cheaper/more accurate ranking (replacing manual bucket-sorting); changed decisions on early-offer timing (to preempt rival schools), financial incentives/scholarships (more confidently targeted at top-ranked candidates), and special attention (faculty lunches, alumni access); an increased return to expanding the applicant pool (since evaluating more applications becomes cheap), potentially driving application fees toward zero if the AI can also assess application seriousness; and potentially "nearly instantaneous" admissions decisions, fundamentally changing the timing dynamics of competition among top MBA programs for candidates.
Outcome: The chapter is explicit that this technology is hypothetical, but the case is used to demonstrate concretely how placing an AI tool within one task in a workflow can cause other tasks to be removed (manual ranking) and added (wider-reach, lower-cost-of-evaluation advertising/marketing) throughout the entire workflow, not just the task the AI was originally designed for.
Concept Illustrated: The "AI tools remove and add tasks" claim, and the workflow/task/decision hierarchy, both made vivid through a single extended, realistic example spanning an entire business process.
Why This Case Is Useful: An unusually thorough, multi-step worked example (rare in the book to see a single hypothetical traced through so many downstream implications) that serves as a template for how a reader might conduct the same kind of analysis for their own organization's workflows.
Potential for Reuse: High
```

```
Case Title: How an AI tool powered the iPhone's predictive touchscreen keyboard
People / Organization: Apple; Apple engineers (unnamed individually); BlackBerry (comparison/context)
Context: The chapter's culminating case, used to demonstrate the "understanding the workflow first" principle with a famous, concrete consumer-technology example.
What Happened: The iPhone's on-screen keyboard retained the QWERTY layout (originally designed to physically separate frequently-sequential mechanical typewriter keys to prevent jamming) even though the mechanical jamming problem was irrelevant to a touchscreen — largely due to user familiarity, reinforced by the popularity of BlackBerry's hardware QWERTY keyboard (nicknamed the "Crackberry" for its addictive usability). But as late as 2006 (the iPhone launched in 2007), the soft keyboard — described as the "biggest science project" of the iPhone — was "terrible": the 3.5-inch LCD screen made keys small enough that mistyping was constant, to the point of being unusable even for text messages. With just three weeks to find a solution before the deadline that would determine whether the whole keyboard project (and by extension, every iPhone software developer's plans) proceeded, Apple engineers — many of whom initially proposed abandoning QWERTY entirely — instead used 2006-era machine learning to build a predictive algorithm that dynamically expanded the invisible touch-target area around whichever key a user was statistically most likely to press next (e.g., after typing "t," the target area around "h" expanded, since "th" is a highly probable sequence, followed by "e," then "i," and so on), without changing the visible key layout the user saw. This solution worked specifically because of QWERTY's original design logic: since QWERTY was designed to keep frequently-sequential letters physically separated (to prevent mechanical jamming), the "most likely next key" was almost always spatially distant from the "just-pressed key," giving the predictive algorithm room to expand the correct target's touch area without overlapping an adjacent, wrong key's target area.
Outcome: The keyboard shipped successfully, and the chapter notes the same underlying predictive-text heritage powers modern autocorrect. The authors draw the chapter's explicit closing lesson from this case: solving the problem required Apple engineers to precisely understand the actual workflow of using a keyboard (identify a key, touch it, move to another) and to realize, by breaking down that workflow, that a key did not need to be visually/physically identical to be correctly identified and touched — prediction could instead solve the problem of knowing where the user was going next, but only once the underlying workflow was properly understood.
Concept Illustrated: The chapter's central thesis in miniature — that understanding the actual workflow (not just having access to powerful technology) is what determines whether and how an AI tool can be successfully deployed; also a vivid illustration of "AI as a point solution" solving one extremely specific task (touch-target sizing) within a larger workflow (typing).
Why This Case Is Useful: An unusually detailed, mechanistically clear, and widely relatable (nearly every reader has used a smartphone keyboard) case that makes an abstract methodological point (understand the workflow first) concrete via a beloved, ubiquitous piece of technology, with genuine narrative stakes (a three-week, project-threatening deadline).
Potential for Reuse: High
```

## 8. Best Teaching Examples

```
Concept: Reengineering — redesigning around the bottleneck, not just adding technology
Example: Ford's accounts payable reengineering, where a shared database eliminated the purchase-order-reconciliation bottleneck that was slowing the entire process.
Why It Works: A clean, quantified before/after comparison (500 employees vs. Mazda's 5; resulting 75% reduction) with an intuitive underlying mechanism (the whole system moves at the speed of its hardest cases) that generalizes easily to any bottleneck-driven process.
Possible Alternative Domain: Business, Everyday Life
```

```
Concept: A single AI tool rippling through an entire workflow (removing and adding tasks)
Example: The hypothetical MBA applicant-ranking AI, tracing effects from application-fee policy to offer timing to financial aid to admissions speed.
Why It Works: A fully worked, multi-step example that shows — rather than just asserts — how one prediction technology's downstream effects can touch nearly every part of a business process, modeling the kind of systematic thinking the chapter wants readers to apply to their own organizations.
Possible Alternative Domain: Business, AI
```

```
Concept: Understanding the workflow before deploying the technology
Example: Apple engineers realizing that a keyboard key didn't need to be visually identical to be correctly identified and touched, enabling invisible predictive touch-target expansion.
Why It Works: A famous, beloved piece of everyday technology with a genuinely clever, mechanistically explainable solution and real narrative stakes (a three-week deadline), making an abstract methodological principle memorable and concrete.
Possible Alternative Domain: AI, Everyday Life
```

## 9. Counterintuitive Insights

```
Insight: The original QWERTY keyboard layout — designed in the 19th century to solve a mechanical typewriter jamming problem that has been irrelevant for decades — turned out to be exactly the right foundation for a 21st-century AI-powered predictive touch-target solution, because the same letter-separation logic that prevented mechanical jamming also happened to keep "likely next keys" spatially distant from "just-pressed keys" on a touchscreen.
Common Belief: An outdated design constraint (QWERTY, kept mainly out of familiarity despite its original rationale being obsolete) would be an obstacle that new technology needs to work around or replace.
Author's Argument: Rather than being an obstacle, QWERTY's specific letter arrangement was an unexpected enabling condition for the AI solution — the predictive algorithm could only expand touch targets safely because likely-next-keys were already spatially separated from just-pressed keys, a property inherited from a completely unrelated 19th-century mechanical constraint.
Evidence: The detailed mechanistic explanation of how touch-target expansion worked, tied to QWERTY's original design purpose.
Why It Is Surprising: It reveals a hidden, centuries-spanning causal connection between a mechanical engineering problem (typewriter key jams) and a machine-learning engineering solution (predictive touch-target sizing), where an "obsolete" legacy design turns out to be quietly load-bearing for a cutting-edge technology.
```

## 10. Unique or Unusual Ideas

```
Idea: Explicitly using a "magical"/fictitious AI technology as a deliberate thought-experiment device (rather than only discussing real, currently-deployed AI tools) to trace out a workflow's full downstream implications without being constrained by current technical limitations.
Why It Seems Unique: Most of the book's cases are grounded in real, verifiable technology deployments; the chapter's explicit choice to use a hypothetical, admittedly-not-yet-real technology for the MBA case is a distinctive pedagogical move that allows the authors to illustrate the *full* potential scope of workflow-level thinking, unconstrained by whether the specific enabling technology exists yet — useful specifically because it separates the "how to think about workflow redesign" methodology from "what AI can technically do today."
Potential Connection to Other Topics: Scenario planning and speculative design methodologies in business strategy and futures studies.
```

## 11. Tensions, Contradictions, and Open Questions

```
Issue: The chapter argues AI's productivity gains will likely be slow to materialize (following the Solow productivity-paradox pattern) and require significant reengineering-style workflow redesign investment, yet also presents the iPhone keyboard case as a rapid, three-week turnaround success — these two framings (slow, paradox-prone diffusion vs. rapid, high-stakes sprint solution) aren't explicitly reconciled.
Author's Position: Both claims are presented as valid without directly addressing the apparent tension between them.
Possible Counterargument: The iPhone case may be better understood as an exception (a well-resourced, highly focused team solving one narrow, well-defined task under existential pressure) rather than a counterexample to the broader Solow-paradox pattern, which the chapter's own examples (Ford, Mutual Benefit Life) suggest typically requires longer-horizon, organization-wide workflow redesign — but the chapter doesn't explicitly draw this distinction itself.
What Evidence Would Help Resolve It: A more explicit discussion of what conditions (team size, deadline pressure, task narrowness, organizational scope) predict fast versus slow AI-driven productivity gains, which the chapter doesn't provide but which later chapters (e.g., on job redesign or C-suite AI strategy) might address.
```

## 12. Quotable Ideas

```
Paraphrase (short): You can see the computer age everywhere but in the productivity statistics (Robert Solow).
Why the Idea Matters: A famous, economically authoritative encapsulation of the "productivity paradox" that frames the entire chapter's caution against expecting easy, automatic gains from powerful general-purpose technology.
Source Location: Book p.147, quoting Robert Solow
```

```
Paraphrase (short): Many of the 146 distinct tasks in the initial public offering process were begging to be automated (R. Martin Chavez, Goldman Sachs CFO).
Why the Idea Matters: A vivid, quotable, contemporary executive statement that validates the chapter's task-decomposition methodology as already being applied by sophisticated real-world organizations.
Source Location: Book p.149, quoting R. Martin Chavez
```

```
Paraphrase (short): Understanding the workflow was critical for figuring out how best to deploy the AI tool. This is true of all workflows.
Why the Idea Matters: The chapter's own explicit, generalized thesis statement, distilling the entire chapter (and the iPhone keyboard case specifically) into a single transferable principle.
Source Location: Book p.154
```

## 13. Psychology Connections

None identified — the chapter is primarily organizational/process-focused rather than psychological in content, though the QWERTY-familiarity point (engineers initially resisting abandoning QWERTY "out of familiarity") touches lightly on status-quo bias without developing it further.

## 14. Mathematics and Decision Science Connections

```
Connection: The Ford bottleneck example ("the entire system flows at the speed of the hardest case") is an intuitive illustration of queueing theory / bottleneck analysis concepts from operations research, though the chapter doesn't use this technical vocabulary.
Connection: The hypothetical MBA AI's effect on optimal applicant-pool size (lower marginal evaluation cost → higher optimal quantity) is a direct, if informal, application of standard marginal-cost economic reasoning, consistent with similar arguments made in Ch.2 and Ch.6.
```

## 15. Sports Connections

None identified in the chapter's direct examples; no forced inference added.

## 16. AI and Machine Learning Connections

```
Direct examples from the book: CDL portfolio AI tools (document-passage highlighting, manufacturing-defect flagging, customer-service response forecasting); Google's 1,000+ internal AI tools (email, translation, driving); the hypothetical MBA applicant-ranking AI (application data, video interviews, social media data, trained on historical outcome data); the iPhone's 2006-era machine-learning-powered predictive keyboard (dynamic touch-target expansion based on next-letter probability).
Inferred connection (my own): The iPhone keyboard's dynamic touch-target expansion is a plain-language description of a next-character-prediction language model applied to a UI/UX problem rather than a text-generation problem — an early, pre-dating-modern-LLM example of using sequence-probability prediction to solve a physical/interaction-design constraint, though the chapter doesn't frame it in this specific technical vocabulary.
```

## 17. Content Creation Opportunities

```
Idea Title: "The iPhone Almost Failed Because of Its Keyboard — Here's the 3-Week Fix"
Format: YouTube Long-form | YouTube Short
Application Domain: AI | History | Business
Hidden Principle: Optimization
Story Hook (Layer 1): As late as 2006, the iPhone's keyboard was so bad it couldn't type a text message — and engineers had three weeks to fix it or the whole project might die.
Principle Framework (Layer 2): The winning fix wasn't a new keyboard design — it was understanding that the actual workflow (identify, touch, move on) didn't require visible keys to change size, only invisible touch targets to predict where you were going next.
Best Supporting Case: The iPhone keyboard case (Section 7).
Character Application: Insight: Interpreter
Psychology Angle: None identified.
Math Angle: Next-letter sequence probability (informal n-gram-style prediction).
Sports Angle: None identified.
Business Angle: Direct — a canonical "understand the workflow before deploying the tech" case study.
Investing Angle: None identified.
History Angle: Direct — 2006–2007 iPhone development history, with a QWERTY-vs-BlackBerry competitive backdrop.
AI Angle: Direct — an early, highly successful real-world machine-learning deployment predating the modern AI boom.
```

```
Idea Title: "Why Adding Computers Didn't Fix Ford's Paperwork Problem — Redesigning It Did"
Format: YouTube Short | Community Post
Application Domain: Business | AI | History
Hidden Principle: Optimization / Signal vs. Noise
Story Hook (Layer 1): Ford had 500 people processing payments. Mazda did the same job with 5. The gap wasn't technology — it was the process itself.
Principle Framework (Layer 2): A slow, bottlenecked process doesn't get fixed by adding computers to it — it gets fixed by finding the specific chokepoint (the hardest cases) and redesigning around it, a lesson directly transferable to AI adoption today.
Best Supporting Case: Ford's accounts payable reengineering (Section 7).
Character Application: Sigma: Architect
Psychology Angle: None identified.
Math Angle: Bottleneck/queueing logic (the system moves at the speed of its hardest cases).
Sports Angle: None identified.
Business Angle: Direct — a foundational case for any AI-adoption or process-improvement content.
Investing Angle: None identified.
History Angle: Direct — 1980s Ford/Mazda competitive benchmarking, popularized by Hammer and Champy's 1993 book.
AI Angle: Direct — the chapter's explicit analogy between 1990s computing reengineering and today's AI adoption challenge.
```

```
Idea Title: "One 'Magic' AI Would Change Way More Than You Think — An MBA Admissions Case Study"
Format: YouTube Long-form
Application Domain: AI | Business | Everyday Life
Hidden Principle: Optimization
Story Hook (Layer 1): Imagine an AI that could perfectly rank every college applicant. It wouldn't just speed up admissions — it would change application fees, scholarships, and even when decisions get made.
Principle Framework (Layer 2): A single new prediction capability doesn't stay contained to the task it was built for — tracing its ripple effects through an entire workflow reveals which tasks disappear and which new ones suddenly become worth doing.
Best Supporting Case: The hypothetical MBA applicant-ranking AI (Section 7).
Character Application: Sigma: Architect
Psychology Angle: None identified.
Math Angle: Marginal cost of evaluation driving optimal applicant-pool size.
Sports Angle: None identified.
Business Angle: Direct — a transferable template for auditing any organization's own workflow for AI ripple effects.
Investing Angle: Inferred — evaluating an EdTech or HR-tech startup's total addressable market by tracing similar workflow-wide effects.
History Angle: None identified.
AI Angle: Direct — the chapter's most fully worked example of the "AI removes and adds tasks" principle.
```

```
Idea Title: "The ROI Checklist Every Company Should Run Before Buying an AI Tool"
Format: YouTube Short | Community Post
Application Domain: Business | AI
Hidden Principle: Optimization
Story Hook (Layer 1): Some AI tools work the moment you install them. Most don't — and the difference comes down to one ranked list.
Principle Framework (Layer 2): Break your workflow into tasks, estimate the ROI of automating each one, rank them, and work down the list — some tasks will pay off immediately, but most require redesigning the surrounding workflow to get any benefit at all.
Best Supporting Case: The chapter's own Key Points ROI-ranking methodology (Section 4).
Character Application: Sigma: Architect
Psychology Angle: None identified.
Math Angle: Direct — ROI ranking/prioritization as a resource-allocation problem.
Sports Angle: None identified.
Business Angle: Direct — an actionable AI-adoption checklist.
Investing Angle: Inferred — evaluating an AI startup's product roadmap by whether it targets "drop-in ROI" tasks or "requires reengineering" tasks.
History Angle: None identified.
AI Angle: Direct — practical AI implementation strategy.
```

## 18. Chapter Knowledge Cards

```
CARD ID: B04-C14-01
Title: The productivity paradox and reengineering
Type: Concept
Summary: Robert Solow's observation that computing's economic gains were hard to detect in productivity statistics despite visible ubiquity motivated the 1990s "reengineering" movement (Hammer and Champy), which argued businesses must redesign workflows around new technology rather than simply inserting it into unchanged processes — a pattern the chapter argues will likely recur with AI.
Source: Book p.147
Tags: productivity paradox, reengineering, history
Related Concepts: Workflow/task/decision hierarchy
```

```
CARD ID: B04-C14-02
Title: The workflow-task-decision-job hierarchy (Figure 14-1)
Type: Model
Summary: Workflows are composed of tasks; tasks are collections of decisions (prediction+judgment+action, per Ch.8); jobs are collections of tasks — the task, not the job or overall strategy, is the correct unit for evaluating where AI tools can add value.
Source: Book p.149–150
Tags: framework, workflow, task, decision, AI adoption
Related Concepts: Anatomy of a decision (Ch.8), job redesign (Ch.16)
```

```
CARD ID: B04-C14-03
Title: Ford's accounts payable reengineering
Type: Case
Summary: Ford's 500-person accounts payable department (vs. Mazda's 5-person equivalent) was reengineered around a shared database that eliminated the purchase-order-reconciliation bottleneck, shrinking the department 75% and improving speed/accuracy.
Source: Book p.147–148
Tags: reengineering, case, headcount reduction
Related Concepts: Mutual Benefit Life case
```

```
CARD ID: B04-C14-04
Title: Mutual Benefit Life's application-processing reengineering
Type: Case
Summary: A 19-person, 5-department, 30-step insurance application process (taking 5–25 days) was reengineered via a shared database and single-person authority, cutting processing time to 4 hours–few days — showing reengineering can be about speed/quality, not just headcount.
Source: Book p.148
Tags: reengineering, case, service quality
Related Concepts: Ford case
```

```
CARD ID: B04-C14-05
Title: AI tools as point solutions (CDL and Google examples)
Type: Concept
Summary: Most AI tools address one specific task within one specific workflow, not general-purpose problems — illustrated by 150+ narrowly-focused CDL portfolio companies and Google's 1,000+ internal AI tools spanning email, translation, and driving.
Source: Book p.150
Tags: AI tools, point solutions, CDL, Google
Related Concepts: Workflow/task/decision hierarchy
```

```
CARD ID: B04-C14-06
Title: The hypothetical MBA applicant-ranking AI
Type: Case
Summary: A fictitious "magical" AI ranking MBA applicants would ripple through the entire recruitment workflow — removing manual bucket-sorting, changing offer timing/financial aid decisions, expanding the applicant pool (lower evaluation cost), potentially driving fees to zero, and making admissions decisions nearly instantaneous.
Source: Book p.150–153
Tags: thought experiment, workflow redesign, MBA admissions
Related Concepts: Tasks removed and added by AI
```

```
CARD ID: B04-C14-07
Title: The iPhone's predictive keyboard and QWERTY's hidden advantage
Type: Case
Summary: Apple engineers, facing a 3-week deadline, used 2006-era machine learning to dynamically expand invisible touch targets around predicted next keys — a solution enabled specifically by QWERTY's original (now-obsolete) mechanical letter-separation design, which kept likely-next-keys spatially distant from just-pressed keys.
Source: Book p.153–154
Tags: AI, iPhone, QWERTY, understanding the workflow
Related Concepts: Workflow-first design principle
```

```
CARD ID: B04-C14-08
Title: The ROI-ranking implementation methodology
Type: Framework
Summary: Companies implement AI by decomposing workflows into tasks, estimating the ROI of building/buying an AI for each task, ranking tasks by ROI, and implementing top-down; some tasks yield immediate benefit from a simple drop-in tool, but most require reengineering the surrounding workflow.
Source: Book p.155 (Key Points)
Tags: framework, ROI, AI implementation, prioritization
Related Concepts: Reengineering-style workflow redesign
```

```
CARD ID: B04-C14-09
Title: The condition for full automation of a task
Type: Concept
Summary: A task becomes fully automated (humans removed) only if prediction machines also increase the returns to using machines in the task's other elements (judgment, data, action) — not from better prediction alone; otherwise the prediction machine is best paired with human decision-makers.
Source: Book p.149
Tags: full automation, prediction machines, human-AI collaboration
Related Concepts: Full automation (Ch.12), workflow-task-decision hierarchy
```

## 19. Chapter Summary for Cross-Book Comparison

```
Main Thesis: Like computing before it, AI is a general-purpose technology whose productivity gains require deliberate workflow redesign (the "reengineering" approach), not simply inserting AI tools into unchanged processes; because prediction operates at the decision level and decisions aggregate into tasks, the task — not the job or strategy — is the correct unit for AI tool design, and AI tools characteristically change workflows by both removing existing tasks and adding new ones, as demonstrated by historical reengineering cases (Ford, Mutual Benefit Life), a real contemporary example (Goldman Sachs's 146-task IPO process), a fully worked hypothetical (MBA admissions AI), and a famous real product case (the iPhone's predictive keyboard).
Top 5 Concepts: (1) The productivity paradox and reengineering as AI's likely historical analog. (2) The workflow-task-decision-job hierarchy (Figure 14-1) as the correct unit-of-analysis framework. (3) AI tools removing and adding tasks within a workflow. (4) AI tools as point solutions (many narrow tools, not one general system). (5) Understanding the actual workflow as the prerequisite for successful AI deployment.
Top 3 Claims: (1) Ford's and Mutual Benefit Life's reengineering successes came from redesigning around bottlenecks, not just computerizing existing processes. (2) A hypothetical MBA-ranking AI would ripple through an entire workflow, removing manual ranking and adding wider-reach marketing, changed financial-aid targeting, and near-instantaneous decisions. (3) The iPhone's predictive keyboard succeeded because Apple engineers understood the actual keyboard-use workflow before designing the AI solution, and because QWERTY's obsolete mechanical design happened to enable it.
Top 3 Cases: (1) The iPhone's predictive touchscreen keyboard and its QWERTY-dependent solution. (2) The hypothetical MBA applicant-ranking AI and its workflow-wide ripple effects. (3) Ford's accounts payable reengineering (paired with Mutual Benefit Life's application-processing reengineering).
Top 3 Studies: None formally cited as independent academic studies in this chapter — evidence is drawn from historical business cases (Hammer and Champy's book), a named-executive quote (Goldman Sachs), the authors' own institutional data (CDL), and product-development history (iPhone) rather than cited research.
Most Unique Idea: Deliberately using a "magical"/fictitious AI technology as a thought-experiment device to trace a workflow's full downstream implications, unconstrained by current technical feasibility — separating the workflow-redesign methodology from questions of present-day technical capability.
Most Counterintuitive Idea: The 19th-century QWERTY keyboard layout — kept mainly out of user familiarity despite its original mechanical rationale being obsolete — turned out to be exactly the right foundation for the iPhone's AI-powered predictive keyboard, because its letter-separation logic incidentally kept "likely next keys" spatially distant from "just-pressed keys."
Biggest Weakness or Open Question: The chapter doesn't reconcile its Solow-paradox framing (AI gains will likely be slow and require significant reengineering investment) with the iPhone keyboard case's rapid three-week turnaround — leaving unclear what organizational or task-level conditions predict fast versus slow AI-driven productivity gains.
Best Content Opportunity: "The iPhone Almost Failed Because of Its Keyboard — Here's the 3-Week Fix" (Section 17) — a famous, beloved technology with a genuinely surprising mechanistic explanation and real narrative stakes, making the chapter's core "understand the workflow first" lesson both memorable and widely relatable.
```
