# Prediction Machines — Chapter 14: Deconstructing Workflows
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Audit
**Source:** Book pages 147–155 (PDF pages 160–169)
**Date:** 2026-08-04

## Missing Items

1. **The ROI-ranking implementation methodology (book p.155, Key Points)**: The chapter's own Key Points section gives a concrete, actionable business process for AI implementation that the extraction did not capture as a distinct framework: "In deciding how to implement AI, companies will break their workflows down into tasks, estimate the ROI for building or buying an AI to perform each task, rank-order the AIs in terms of ROI, and then start from the top of the list and begin working downward. Sometimes a company can simply drop an AI tool into its workflow and realize an immediate benefit due to increasing the productivity of that task. Often, however, it's not that easy. Deriving a real benefit from implementing an AI tool requires rethinking, or 'reengineering' the entire workflow." This is the chapter's most concrete operational takeaway — a step-by-step method (decompose → estimate ROI per task → rank → implement top-down) — and it also introduces an important nuance the extraction's Section 4 frameworks missed entirely: sometimes a drop-in AI tool works immediately without any workflow redesign at all, and reengineering is only needed when it doesn't.
2. **"Automate all decisions" vs. partial automation, and the condition for full automation (book p.149)**: Immediately after the Goldman Sachs paragraph and just before Figure 14-1, the chapter makes a distinct conceptual point the extraction omitted: "Sometimes we can automate all the decisions within a task. Or we can now automate the last remaining decision that has not yet been automated because of enhanced prediction. The rise of prediction machines motivates thinking about how to redesign and automate entire processes... effectively removing humans from such tasks altogether. But for better and cheaper prediction alone to lead to pure automation, employing prediction machines must also increase the returns to using machines in other aspects of a task. Otherwise, you will want to employ a prediction machine to work with human decision-makers." This directly connects back to Chapter 12's full-automation discussion and adds a specific condition (AI must also raise the returns to machine-performed judgment/data/action, not just prediction) that determines whether a task becomes fully automated or remains human-AI collaborative — a distinct, citable claim the extraction's frameworks section did not include.

## Corrections Needed

1. **Ford's 400-person target was described backward (book p.148)**: The extraction's Key Claims section (Ford case) states the 400-person target, a 20% reduction, was "initially considered ambitious." The chapter says the opposite: "Ford hoped that by spending big on computers, it could reduce that number by 20 percent. The goal of having four hundred people in the department was **not unrealistic**; after all, its competitor Mazda had just five people in accounts payable." The book frames 400 as a modest, readily achievable goal — practically unambitious — precisely because Mazda proved a department could run on far fewer people (5) than even Ford's reduced target (400). The extraction's "initially considered ambitious" reverses this framing and should be corrected to reflect that the target was seen as conservative/easily achievable, not ambitious.

## Overgeneralizations

None identified.

## Important Nuance Lost

- **The computer's specific triage mechanism in the Ford case (book p.148)** was flattened into a generic "eliminated the bottleneck" description. The chapter is more specific: "Not only could a computer reduce mismatches that held up the system, but it could sort the difficult from the easier cases and ensure the easier ones went through at a reasonable speed." The mechanism wasn't just fixing the bottleneck directly — it was triage: separating easy orders (which could then move fast) from hard ones (which still needed dedicated handling), rather than making every order equally fast.
- **The MBA bucket-misclassification risk was narrower in the extraction than in the chapter (book p.151–152)**: The extraction's claim/case describes the risk as avoiding misclassifying a true "a" candidate into bucket "c." The chapter's actual statement is broader: "you do not want to place someone in bucket (c) when they should be in (a) **or even (b)**" — i.e., the costly error includes wrongly bucketing a "b"-worthy candidate into "c," not only an "a"-worthy one. The extraction's narrower framing understates the range of misclassification risk the chapter describes.

## Overgeneralizations

None identified.

## Additional Cases and Examples

```
Case Title: The "sort easy from hard" triage mechanism in Ford's reengineering
People / Organization: Ford Motor Company
Context: A more precise reading of the mechanism by which Ford's shared-database computer system fixed the accounts payable bottleneck (extraction Section 7).
What Happened: Rather than uniformly speeding up all purchase-order processing, the computer system specifically separated straightforward orders from problematic ones requiring reconciliation, letting the easy majority move through quickly while difficult cases still received dedicated (slower) handling.
Outcome: The department shrank 75% and became faster and more accurate overall — achieved through triage/sorting, not uniform acceleration.
Concept Illustrated: A refinement of the general "eliminate the bottleneck" reengineering lesson — the actual mechanism was differential handling by case difficulty, a specific and reusable pattern (route easy cases fast, route hard cases to focused handling) applicable well beyond accounts payable.
Why This Case Is Useful: Sharpens the Ford case from a generic "computers fixed it" story into a specific, transferable triage design pattern relevant to any AI/automation deployment involving heterogeneous case difficulty.
Potential for Reuse: High
```

## Additional Research Evidence

None identified beyond what's already captured in Section 5 and this audit.

## Potential Disagreements to Track Later

None newly identified beyond what's already flagged in the extraction's Section 11.

## Additional Content Opportunities

```
Idea Title: "The ROI Checklist Every Company Should Run Before Buying an AI Tool"
Format: YouTube Short | Community Post
Application Domain: Business | AI
Hidden Principle: Optimization
Story Hook (Layer 1): Some AI tools work the moment you install them. Most don't — and the difference comes down to one ranked list.
Principle Framework (Layer 2): Break your workflow into tasks, estimate the ROI of automating each one, rank them, and work down the list — some tasks will pay off immediately, but most require redesigning the surrounding workflow to get any benefit at all.
Best Supporting Case: The chapter's own Key Points ROI-ranking methodology (Missing Item #1).
Character Application: Sigma: Architect
Psychology Angle: None identified.
Math Angle: Direct — ROI ranking/prioritization as a resource-allocation problem.
Sports Angle: None identified.
Business Angle: Direct — an actionable AI-adoption checklist.
Investing Angle: Inferred — evaluating an AI startup's product roadmap by whether it targets "drop-in ROI" tasks or "requires reengineering" tasks.
History Angle: None identified.
AI Angle: Direct — practical AI implementation strategy.
```

## Recommended Changes to the Original Extraction

1. **Section 4 (Frameworks)** — add a new framework entry for the ROI-ranking implementation methodology (Missing Item #1): decompose workflow into tasks, estimate ROI per task, rank-order, implement top-down; note the "sometimes a drop-in AI tool works immediately, often reengineering is required" distinction.
2. **Section 2 or 4** — add a new concept/claim for the "automate all decisions within a task" vs. partial automation condition (Missing Item #2), cross-referenced to Chapter 12's full-automation discussion.
3. **Section 3, Ford case Key Claim** — correct "initially considered ambitious" to reflect the chapter's actual framing: the 400-person target was "not unrealistic," i.e., seen as a conservative, readily achievable goal given Mazda's 5-person benchmark.
4. **Section 7, Ford case** — add the triage/sorting nuance (easy cases routed fast, hard cases routed to dedicated handling) rather than describing the fix as uniform bottleneck elimination.
5. **Section 3, MBA bucket-risk claim** — broaden "misclassifying a true 'a' candidate into bucket 'c'" to include the chapter's fuller statement: placing someone in (c) when they should be in (a) *or even (b)*.
6. **Section 18 (Knowledge Cards)** — add two new cards: one for the ROI-ranking methodology, one for the full-automation condition (prediction improving returns to other task aspects, not just prediction itself).
7. **Section 17 (Content Creation Opportunities)** — add "The ROI Checklist Every Company Should Run Before Buying an AI Tool" (see Additional Content Opportunities above).

All other sections are accurate as extracted; no further changes needed.
