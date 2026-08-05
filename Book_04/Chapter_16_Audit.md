# Prediction Machines — Chapter 16: Job Redesign
**Author:** Ajay Agrawal, Joshua Gans, Avi Goldfarb
**Type:** Audit
**Source:** Book pages 165–175 (PDF pages 178–188)
**Date:** 2026-08-04

## Missing Items

1. **The specific breakdown of fulfillment as a multi-step workflow (book p.167)**: The extraction's Section 7 (Kiva case) describes fulfillment generically. The chapter gives a specific, task-by-task breakdown directly relevant to the book's own Ch.14 workflow/task vocabulary: "fulfillment includes a number of steps such as locating items in a large warehouse-type facility, picking the items off shelves, scanning them for inventory management, placing them in a tote, packing them in a box, labeling the box, and shipping it for delivery." The extraction should enumerate this list, since it is precisely the kind of task decomposition the book has advocated since Chapter 14, applied here to a concrete industry.
2. **Inventory-management prediction predates AI and online shopping by decades (book p.167)**: The chapter notes: "These well-established prediction tasks had been a key part of off-line retail and warehouse management for decades. Machine-learning technologies made these predictions even better." The extraction's Section 7 mentions inventory-management prediction but omits this explicit continuity claim — that predicting stock-outs/reorder needs is not a new, AI-native task but a decades-old retail practice that ML merely improved, which is a nuance worth preserving (AI as enhancement of an existing prediction task, not creation of a new one).
3. **The "cheap prediction increases imaging volume" economic argument (book p.170, Role 1)**: The chapter's first radiologist role includes a specific, somewhat counterintuitive economic point the extraction's Section 4 framework omitted: "As the cost of imaging falls, the amount of imaging will increase, so it is possible that in the short and possibly medium terms, this increase will offset the decline in the human time spent with each image." This is a direct application of the "cheap changes everything"/more-usage logic established in Chapter 2, now applied specifically to predict that radiologists' total image-selection workload may not shrink even as AI handles more per-image interpretation — a genuinely counterintuitive point given the chapter's overall "radiologists will spend less time reading images" framing.
4. **Interventional radiology may get easier, not just "unaffected" (book p.170, Role 2)**: The chapter states interventional radiology "involves human judgment and dexterous human action that is unaffected by advances in AI, except perhaps in making the interventional radiologist's job somewhat easier by providing better-identified images." The extraction's Section 4 (five-role framework) describes this role as simply "unaffected" by AI, dropping the explicit exception that AI may still assist this role indirectly via improved image identification.
5. **The "doctor's doctor" self-conception and the "assessment in the negative" framing (book p.170–171, Role 3)**: Two related points from Role 3 are missing: (a) the chapter's own quotable phrase that "many radiologists see themselves as the 'doctor's doctor'"; and (b) the specific, somewhat counterintuitive point that a radiologist's assessment is often stated "in the negative" (e.g., "pneumonia not excluded") rather than as a positive diagnosis (e.g., "the patient almost surely has pneumonia") — a nuance about how diagnostic uncertainty is communicated that the extraction's case narrative did not capture.
6. **Biopsies framed as "the less risky decision," and the prediction machine's specific role as increasing confidence in NOT operating (book p.172)**: Two connected claims from the chapter's Mr. Patel discussion are missing from the extraction: (a) "Ordering the biopsy is the less risky decision; yes, it is costly, but it can yield a more certain diagnosis" — an explicitly counterintuitive framing (the invasive, costly option is the lower-risk one in decision-theoretic terms); and (b) "the role of the prediction machine is to increase a doctor's confidence in not conducting a biopsy... If the machine improves prediction, it will lead to fewer invasive examinations" — a specific, falsifiable claim about the direction of AI's effect (fewer invasive procedures over time) that connects directly back to Ch.13's stakes/false-positive framework.
7. **The rhetorical "saved salaries" setup in the school bus driver case (book p.173)**: The chapter poses a rhetorical question the extraction's case narrative omitted: "When someone called a 'school bus driver' no longer drives buses, should local governments start spending these saved salaries?" This framing explicitly sets up the naive assumption (full driving automation = full cost savings) that the rest of the section then rebuts by identifying the supervisory/disciplinary tasks that persist — losing this rhetorical setup weakens the case's argumentative structure.
8. **The specific "calculator skill" detail in the Key Points' final bullet (book p.175)**: The chapter's closing point is more specific than the extraction's Section 4/18 renderings: "the arrival of the spreadsheet diminished the returns to being able to perform many calculations quickly on a calculator." The extraction generalizes this to "shift the relative returns to different skills" without naming the specific devalued skill (fast manual calculation on a calculator), which sharpens the bookkeeper case's before/after contrast.

## Corrections Needed

None identified — spot-checked figures (40,000 full-time Amazon pickers, ~120 picks/hour, Kiva's $775 million 2012 acquisition, Frey and Osborne's 89% school-bus-driver automation figure, the Mr. Patel 66.6%/33.3%/0.1% figures, Hinton's October 2016 CDL quote to 600 people) all match the chapter text.

## Overgeneralizations

None identified.

## Important Nuance Lost

- As detailed in Missing Item #3, the extraction's framing that "radiologists will spend less time reading images" is not fully qualified by the chapter's own caveat that falling imaging costs could increase imaging volume enough to offset that decline — presenting the "less time reading images" conclusion as more settled than the chapter itself treats it.
- As detailed in Missing Item #6, the extraction's Mr. Patel case (Section 7, Section 12) captures the illustrative probability figures but not the chapter's more pointed argument about what those figures are *for* — specifically, that better prediction is expected to reduce the rate of invasive examinations over time, which is the chapter's actual causal claim about AI's clinical impact, not merely an illustration of residual uncertainty.

## Additional Cases and Examples

None identified beyond what's already captured in Section 7.

## Additional Research Evidence

None identified beyond what's already captured in Section 5 and this audit.

## Potential Disagreements to Track Later

None newly identified beyond what's already flagged in the extraction's Section 11.

## Additional Content Opportunities

None identified beyond what's already captured in Section 17 — the missing items above refine existing captured content rather than introduce net-new teachable material.

## Recommended Changes to the Original Extraction

1. **Section 7, Kiva/fulfillment case** — add the specific seven-step fulfillment workflow breakdown (locating, picking, scanning, toting, packing, labeling, shipping), and note that inventory-management prediction predates AI/online retail by decades.
2. **Section 4, five-role radiologist framework** — add the "cheap imaging increases volume" economic nuance to Role 1, and the "somewhat easier via better-identified images" exception to Role 2.
3. **Section 7, Hinton/radiologist case** — add the "doctor's doctor" quote and the "assessment in the negative" (e.g., "pneumonia not excluded") framing to Role 3.
4. **Section 3 (Key Claims) or Section 7** — add the "biopsy as the less risky decision" claim and the specific claim that the prediction machine's role is to increase confidence in not operating, leading to fewer invasive examinations over time.
5. **Section 7, school bus driver case** — restore the rhetorical "should local governments start spending these saved salaries?" framing as the setup the case is rebutting.
6. **Section 18 (Card B04-C16-07) and Section 4** — sharpen the final Key Points bullet to name the specific devalued skill (fast manual calculation on a calculator), not just "different skills" generically.
7. **Section 12 (Quotable Ideas)** — add "many radiologists see themselves as the 'doctor's doctor'" and "prediction machines will reduce uncertainty, but they won't always eliminate it" as additional quotable lines.

All other sections are accurate as extracted; no further changes needed.
