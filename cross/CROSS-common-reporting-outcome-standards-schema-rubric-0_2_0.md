---
title: CROSS - Common Reporting Outcome Standards Schema - Assessment Rubric
version: 0.2.0
date: 2026-05-14
license: CC0
status: Working draft. Companion rubric to CROSS-common-reporting-outcome-standards-schema-0_2_0.md. Supersedes version 0.1.0.
---

# CROSS: Common Reporting Outcome Standards Schema - Assessment Rubric

Version 0.2.0 | 2026-05-14 | CC0

---

## How to Use This Document

This rubric is the reviewer-facing evaluation tool for applications assessed against the Common Reporting Outcome Standards Schema (CROSS) version 0.2.0. It is designed to be used during an active review without cross-referencing the full standard. Reviewers who have not read the standard should still be able to complete a well-grounded evaluation using this document alone.

This version covers three obligation modes: build obligation, change obligation, and retroactive obligation. Before applying any scored criteria, a reviewer must determine which mode the round operates in and navigate to the correct entry specification gate in Section 2. The mode is declared in the published round specification; it is not determined by the reviewer and is not open to interpretation during review.

The rubric is organized into six sections. Section 1 is a pre-assessment configuration step: the reviewer confirms the mode and active gates. Section 2 contains the mode-specific entry specification gate, which is binary. Sections 3 and 4 contain the scored rubric criteria: indicator specification (11 fields) and data quality standards (5 standards). Section 5 covers three binary conformance checks that run parallel to scoring. Section 6 specifies the recommendation vocabulary.

All three recommendation categories (Fund, Fund with conditions, Do not fund) depend on the complete evaluation record. A strong indicator score does not override a conformance check failure. A gate failure in Section 2 terminates evaluation before scoring begins.

---

## Section 1: Round Configuration

Before beginning evaluation, confirm the following from the published round specification. Record the findings; they shape which sections of this rubric apply.

**1. Obligation mode.** Which mode does this round operate in?

- [ ] Build obligation: the funded work must produce a specified deliverable
- [ ] Change obligation: the funded work must produce a measurable change in a defined population
- [ ] Retroactive obligation: the application presents evidence of prior demonstrated contribution

**2. Active gates.** Which gates are active in this round's published configuration?

- [ ] Entry specification gate (always active)
- [ ] Progress verification gate(s): how many? ___
- [ ] Completion verification gate
- [ ] Continuation specification gate

**3. Evidence scope and strength at the completion verification gate.** Record the published configuration. This determines the minimum threshold for a Fund recommendation.

Evidence scope: _______________ (output / usage / outcome / impact)

Evidence strength: _______________ (self-report with documentation / third-party verifiable / independent review / independent evaluation)

**4. Infrastructure declaration.** If any gate is configured at independent review level or above, confirm that the infrastructure declaration is present in the round specification before proceeding. A gate at independent review level without a named reviewer, stated qualifications, and published process does not satisfy the conformance requirement. Record any gap here.

> [Note any missing infrastructure declarations, or write "Not applicable" if no gates require independent review]

---

## Section 2: Entry Specification Gate

Navigate to the sub-section that matches the obligation mode confirmed in Section 1. Complete the gate assessment before opening any scored rubric sections. A gate failure terminates evaluation; do not apply the indicator rubric to a gate failure.

---

### Section 2A: Entry Specification Gate - Build Obligation

**What the gate is asking.** Can the applicant name a falsifiable deliverable with independently verifiable completion criteria?

A falsifiable deliverable is an artifact, product, or documented output whose existence and quality can be confirmed by a reviewer who did not commission the work. Completion criteria are independently verifiable when a reviewer with access to the submitted artifact, and no additional information from the applicant, could determine whether those criteria are met.

This gate does not ask whether the applicant has already started building, whether the deliverable will be widely adopted, or whether the applicant's approach is the best available. It asks only whether the commitment is specific enough to evaluate at the end of the grant period.

**Direction specification without deliverable.** The primary failure mode in build-obligation rounds is offering a direction or vision in place of a deliverable specification. "Making DeFi more transparent" is a direction. "A reporting module that produces a human-readable summary of fees collected by any ERC-4626 vault, published as an open-source library under the MIT license, with at least one deployed instance on Ethereum mainnet, documented with a usage example and test suite" is a deliverable. The difference is testability: a reviewer at grant end can confirm whether the second was delivered; the first cannot be verified or falsified.

**Underspecified completion criteria.** A deliverable is named but the completion criteria are too vague for independent verification. "A working prototype" specifies a form but not a standard. "A prototype that successfully executes the three functions listed in the specification document, as demonstrated in a public recording or live session, with accompanying test results from the specified test suite" specifies a verifiable standard. The rubric can be applied to an application that passes the gate but has underspecified criteria; it will score 2 or lower on Fields 10 and 11.

**Gate finding options.**

Gate passes: document "Gate passes: applicant names [deliverable, paraphrased] with completion criteria sufficient for independent verification: [describe what verification would look like]." Proceed to Section 3.

Gate fails: document "Gate fails: [describe what was offered instead of a falsifiable deliverable or verifiable completion criteria]." Close the evaluation record. Distinguish which failure type applied so the applicant receives the correct corrective signal.

---

### Section 2B: Entry Specification Gate - Change Obligation

**What the gate is asking.** Can the applicant name the FROM state as a specific measurable condition in a defined population?

A FROM state is specific when it names a condition. A condition describes an observable state that exists in the world and can be measured. A category describes a type of problem without grounding it in an observable measurement.

A FROM state that passes the gate: "96 to 99 percent network reachability drops for users in Iran during government-imposed shutdowns, as measured by Open Observatory of Network Interference probe data from 2023 to 2025." This names a measurable quantity, a defined population, a triggering condition, a data source, and a time period. A reviewer can verify that this condition exists.

A FROM state that fails the gate: "There is a lack of privacy tools for people in repressive contexts." This names a category and a vague population. Neither is measurable. A reviewer cannot verify whether this condition exists or how severe it is.

**Two gate failure types in change-obligation rounds.** These are the Frame Language diagnostic categories D2 and D1. They look superficially similar during review but have different implications for the applicant.

Class D2 (values aspiration without conditions): the application offers values language, community commitments, or a mission statement in place of a diagnosis. When asked for a specific FROM state, a D2 application produces more values language because no diagnostic work preceded the application. D2 applications cannot produce a plausible FROM state on request. Gate failure is immediate. The applicant has not performed a problem diagnosis; the path to resubmission is to do the diagnostic work before applying again.

Class D1 (canonical vocabulary without structural grounding): the application uses technically correct vocabulary and names something that resembles a problem diagnosis. A specific FROM state can be articulated. The gate passes. The failure appears at the rigor tier: the indicators claimed are not supported by a sourced data methodology, the baseline is undocumented, or the construction methodology cannot be replicated. A D1 application may score 2s and 1s across the indicator rubric after passing the gate. Treating a D1 failure as a gate failure produces false negatives; the applicant has done diagnostic work and deserves a specific rigor-tier finding about what specification is missing.

**Application timing is not the diagnostic.** A team that built something before the grant round opened is not automatically exhibiting a gate failure. They can name the FROM state precisely because they built the solution to address it. Application timing tells the reviewer when the applicant sought funding; it does not reveal whether a diagnosis was performed.

**Build nested inside change is valid.** An application that describes what it will build while also naming a qualifying FROM state has not failed the change-obligation gate. The build is the mechanism; the change specification is intact. The gate question is whether a FROM state can be named, not whether the applicant also commits to producing an artifact. Build becomes the failure mode when it has replaced the change specification: the applicant names a deliverable but cannot produce a FROM state because the problem was never diagnosed.

**Gate finding options.**

Gate passes: document "Gate passes: applicant names [specific condition, verbatim or paraphrased] in [specific population] with [named source or evidence]." Proceed to Section 3.

Gate fails: document "Gate fails: [describe what was offered instead of a FROM state specification, and note whether the failure type is D2 or D1-equivalent]." Close the evaluation record. Do not apply the indicator rubric.

---

### Section 2C: Entry Specification Gate - Retroactive Obligation

**What the gate is asking.** Does the applicant present evidence of prior contribution meeting the program's published threshold criteria?

In retroactive rounds, the gate question is not about diagnosis or deliverable specification. It is about whether the evidence presented clears the program's published minimum threshold for what constitutes a qualifying prior contribution. The published rubric from the round specification is the instrument; the gate confirms whether the application contains the required evidence in the required form.

**What the reviewer is assessing.** The application must contain: a description of what contribution was produced, the period during which it was produced, evidence of who is using or has benefited from it that is accessible from sources outside the applicant's control, and a concurrent funding disclosure covering any prior awards for the same or overlapping work. If any of these is absent, the entry specification gate fails.

**The rubric dependency.** Unlike build and change obligation, retroactive applications are assessed primarily against the program's published rubric rather than the CROSS indicator specification rubric in Section 3. The Section 3 rubric applies if the program has configured additional indicator-based reporting for retroactive applications (for example, a forward commitment combined with an indicator specification). If no indicator specification is required, proceed from this gate to Section 5 (conformance checks) and Section 6 (recommendation framework), using the program's published rubric for the substantive scoring.

**Gate finding options.**

Gate passes: document "Gate passes: applicant presents evidence of prior contribution in [described form] covering [described period], with evidence of external use [describe source]." Proceed to applicable scoring (program rubric, Section 5, Section 6).

Gate fails: document "Gate fails: [describe what is absent from the application: no contribution description, no period, no independently accessible evidence of use, or no concurrent funding disclosure]." Close the evaluation record.

---

## Section 3: Indicator Specification Rubric

### Overview

CROSS requires applicants to self-specify their outcome indicators. The rubric in this section assesses the quality of the applicant's self-specified indicators across 11 required fields. Each field is scored on a 1-4 scale using the definitions below.

**Score 4 (Meets standard):** The field is complete, specific, and independently verifiable. An independent reviewer with access to the stated sources could confirm the field content without contacting the applicant.

**Score 3 (Minor gap):** The field is substantially complete. One specific, addressable gap is present. The gap is resolvable without structural redesign of the indicator. A score of 3 does not trigger a condition; reviewers note it in the evaluation record.

**Score 2 (Conditional):** The field has a significant gap that must be resolved before disbursement. A score of 2 generates a condition. The condition must be specific, verifiable, and time-bounded. An application with one or more 2s cannot receive a Fund recommendation; it receives Fund with conditions if all other criteria are met.

**Score 1 (Fails standard):** The field is absent, generic, or unverifiable. An application with any indicator field scored 1 is ineligible for funding without resubmission. A score of 1 on the primary indicator produces a Do not fund recommendation.

Where multiple indicators are specified, each indicator is scored independently. The recommendation reflects the weakest primary indicator.

In retroactive obligation rounds where no indicator specification is required by the program configuration, Sections 3 and 4 do not apply. See Section 2C.

---

### Field 1: Indicator Name

**Reviewer question:** Is a short, descriptive label present? Is it distinguishable from generic category labels?

| Score | Criterion |
|---|---|
| 4 | Name is present and distinguishable from generic category labels. It would be recognizable as referring to this specific indicator in a cross-funder comparison. |
| 3 | Name is present but is a category label that could apply to materially different operational definitions. The operational definition field compensates. |
| 2 | Name is absent or is a copy of the program area eligibility criterion rather than an indicator label. |
| 1 | No indicator name is present. |

---

### Field 2: Rationale for Indicator

**Reviewer question:** Does the applicant explain why this indicator was chosen over available alternatives? Is the diagnostic reasoning that preceded tool selection visible?

Rationale is mandatory. An applicant who cannot articulate why they selected a particular indicator over obvious alternatives has not engaged seriously with whether the measurement instrument is valid.

| Score | Criterion |
|---|---|
| 4 | Rationale names at least one alternative indicator considered and explains why the chosen indicator better matches the intervention's claim. The reasoning demonstrates that selection was a deliberate decision. |
| 3 | Rationale explains why the chosen indicator is appropriate but does not name alternatives considered. The reasoning is plausible and specific, not generic. |
| 2 | Rationale is present but circular (e.g., "we chose transaction volume because we measure transactions"). No diagnostic reasoning is visible. |
| 1 | Rationale is absent. |

---

### Field 3: Measurement Form and Evidence Classification

**Reviewer question:** Has the applicant named the measurement form in plain language, with enough specificity to classify it against the three evidence classification axes? Is the stated measurement form consistent with the construction methodology in Field 5?

This field replaces the constrained four-option data type list from version 0.1.0. The applicant now names the measurement form in plain language rather than selecting from a list. Reviewers classify the stated form against three axes for data quality assessment purposes. The applicant is not required to use the axis vocabulary; the reviewer applies the classification.

**Axis 1: Source type.** Where does the evidence originate?
- On-chain verifiable: accessible from public blockchain data with a named contract or address
- Off-chain verifiable: accessible from public sources outside the blockchain (public code repository, published report, named application programming interface)
- Qualitative/narrative: documented through structured narrative, interview data, or artifact review requiring a human evaluator

**Axis 2: Measurement form.** How is the result expressed?
- Quantitative: expressed as a number, proportion, rate, currency amount, or duration
- Ordinal: expressed as a position on a defined ordered scale
- Binary: expressed as met or not met against named completion criteria
- Qualitative: expressed as a documented condition, verified artifact, or narrative record assessed against named criteria

**Axis 3: Aggregation type.** How do period values relate to each other?
- Cumulative: values sum correctly across reporting periods; see Field 6 for the applicant's explicit designation
- Non-cumulative: values describe a state at a point in time; summing across periods is a construction error

**For build-obligation indicators:** the measurement form is typically binary or qualitative. The measurement form declaration specifies what done looks like with enough precision that a reviewer who did not commission the work could verify it independently.

**For change-obligation indicators:** the measurement form is typically quantitative or ordinal. The declaration must include the unit of measurement and the direction of desirable change.

| Score | Criterion |
|---|---|
| 4 | The applicant names the measurement form in plain language with enough specificity to classify against all three axes without inference. The classification is internally consistent with the construction methodology in Field 5. |
| 3 | The measurement form is named but requires modest inference to classify. The classification is possible; the applicant has not made one or two axes explicit. Internally consistent with Field 5. |
| 2 | The measurement form is named but the classification along at least one axis conflicts with the construction methodology (e.g., described as quantitative but the methodology produces only binary results), OR the description is so general that axis classification cannot be determined. |
| 1 | No measurement form description is present. |

---

### Field 4: Operational Definition

**Reviewer question:** Are all four required sub-components present: inclusion criteria, exclusion criteria, unit of analysis, and at least one edge case determination?

| Score | Criterion |
|---|---|
| 4 | All four sub-components are present and specific: inclusion criteria state what qualifies as one instance; exclusion criteria state what the indicator explicitly does not count; unit of analysis names the entity being counted or assessed; at least one edge case shows how an ambiguous instance is resolved. |
| 3 | Three of four sub-components are present. The missing sub-component is restorable without redesigning the indicator. Edge case determination is most commonly absent. |
| 2 | Two of four sub-components are present. The indicator can be understood in principle but cannot be replicated without applicant clarification. |
| 1 | Operational definition is absent or consists entirely of the indicator name restated. No sub-components are identifiable. |

---

### Field 5: Construction and Aggregation Methodology

**Reviewer question:** Is the construction methodology detailed enough that an independent reviewer with access to the stated data source could replicate the result, without contacting the applicant?

For build-obligation indicators: the construction methodology specifies how completion is determined, who performs the verification, and by what process.

For change-obligation indicators: the standard data construction methodology applies (formula or counting rule, partial data handling, sub-unit aggregation).

| Score | Criterion |
|---|---|
| 4 | The formula or counting rule (or, for build indicators, the completion determination process) is stated explicitly. Partial data handling is specified. Aggregation from sub-units to project level is described. An independent reviewer could execute the methodology given the stated source. |
| 3 | The formula or completion process is stated but one secondary element (partial data handling or aggregation) is absent. Replication is possible with minor inference. |
| 2 | The methodology names the data source and describes the result category but does not specify a counting rule or completion determination process. Replication requires significant applicant clarification. |
| 1 | No construction methodology is present. The result is asserted without any described production process. |

---

### Field 6: Cumulative or Non-Cumulative

**Reviewer question:** Has the applicant designated the indicator as cumulative or non-cumulative? Does the target calculation match the designation?

Note: this field is primarily relevant for change-obligation and build-obligation indicators that involve counting over time. Binary completion criteria (did or did not ship the deliverable) are not subject to the cumulative/non-cumulative distinction; mark as not applicable and score 4 for build-obligation binary indicators.

| Score | Criterion |
|---|---|
| 4 | Designation is present and correct. The target is expressed consistently: a cumulative indicator has a life-of-grant total target; a non-cumulative indicator has a target status at grant end, not a sum of period targets. |
| 3 | Designation is present and correct. The target is expressed in the right form but lacks a per-period breakdown expected given the reporting frequency. Minor gap only. |
| 2 | Designation is present but the target calculation is internally inconsistent with it (treating a non-cumulative indicator as cumulative, or vice versa). |
| 1 | Designation is absent. |

---

### Field 7: Disaggregation

**Reviewer question:** Are disaggregation categories named? Is the applicant aware that committed categories may be supplemented but not removed without committee approval?

| Score | Criterion |
|---|---|
| 4 | Disaggregation categories are named. The applicant acknowledges that committed categories may be supplemented but not removed without committee approval. |
| 3 | Disaggregation categories are named but no acknowledgment of the ratchet constraint is present. The categories are clear and applicable. |
| 2 | Disaggregation categories are stated at a level of generality that does not permit actual disaggregation (e.g., "by region" without specifying which regions). |
| 1 | No disaggregation categories are named. |

---

### Field 8: Data Source and Collection Method

**Reviewer question:** Is the named source independently accessible? Is the collection method described? Does any evidence source independent of the applicant appear?

For build-obligation indicators: the data source for completion verification is the named artifact itself plus the named party who will confirm it meets the completion criteria.

| Score | Criterion |
|---|---|
| 4 | The data source is named specifically (contract address, named public application programming interface endpoint, named third-party platform, named institutional partner, named survey instrument, or named artifact with named verifying party). The collection method is stated. The source is independently accessible. |
| 3 | The source is named but access requires a process not described (e.g., "data from our partner organization" without naming the organization or the access method). |
| 2 | The source is a category rather than a named source. |
| 1 | No data source is named. |

---

### Field 9: Data Cost Estimation

**Reviewer question:** Has the applicant attested that data collection is feasible within the project budget?

| Score | Criterion |
|---|---|
| 4 | Applicant attests to feasibility. Approximate cost is stated (or confirmed as zero with source named). The source of funding for collection within the project budget is identified. |
| 3 | Applicant attests to feasibility and confirms free access to the data source, but no budget line or cost estimate is provided. Adequate for free sources; minor gap for paid sources. |
| 2 | Applicant names a data source but makes no attestation of feasibility or cost. |
| 1 | No data cost estimation or feasibility attestation is present. |

---

### Field 10: Baseline (FROM State)

**Reviewer question and mode-specific assessment.**

**For change-obligation indicators:** Is the FROM state specific, measurable, and sourced? Does it express the same unit and type as the indicator's operational definition?

| Score | Criterion |
|---|---|
| 4 | Baseline is specific (a named value or condition), measurable (expressed in the units of the operational definition), and sourced (the source is named and independently accessible). |
| 3 | Baseline is specific and measurable but the source is named at a category level rather than a specific source. |
| 2 | Baseline is directional rather than specific (e.g., "currently low adoption"), or the baseline and target are expressed in different units, or the baseline is asserted without any source. |
| 1 | Baseline is absent. The TO state target appears without any FROM state reference. |

**For build-obligation indicators where the coordinating party engagement dimension is activated:** Is the documented current absence or inadequacy of the deliverable present, with named evidence?

| Score | Criterion |
|---|---|
| 4 | The gap the deliverable addresses is documented with specific evidence: a named party outside the applicant's organization who has confirmed the need, a named existing tool's limitation, or a named data source confirming the gap. |
| 3 | The gap is described with reference to a named source or party but the evidence is indirect. |
| 2 | The gap is asserted by the applicant without independent evidence. |
| 1 | No evidence of the need for the deliverable is present. |

**For build-obligation indicators where the coordinating party engagement dimension is not activated:** Score 4 for any reasonable plain-language statement of what problem or gap the deliverable addresses. This dimension is advisory at this level.

**For retroactive obligation indicators:** Is the documented state of the prior contribution at the time the award period begins present, with named evidence of use?

Apply the change-obligation scoring logic to the evidence of prior contribution: is it specific, does it name a period and source, and is the source independently accessible?

---

### Field 11: Target (TO State)

**Reviewer question and mode-specific assessment.**

**For change-obligation indicators:** Is the target expressed in the same units as the baseline? Is it consistent with the cumulative/non-cumulative designation? Is it specific enough to be verifiable?

| Score | Criterion |
|---|---|
| 4 | Target is expressed in the same units as the baseline and operational definition. It is expressed correctly for the cumulative/non-cumulative designation. It is a specific value or condition, not a directional aspiration. |
| 3 | Target is specific and in the correct units but does not account for all reporting periods where sub-targets are expected. Minor gap only. |
| 2 | Target is directional rather than specific ("increase user adoption"), or units differ from the baseline, or the designation mismatch noted in Field 6 causes internal inconsistency. |
| 1 | Target is absent. |

**For build-obligation indicators:** Is the completion criteria clear enough that a reviewer who did not commission the work could verify whether it was met? Do the criteria correspond to the measurement form stated in Field 3?

| Score | Criterion |
|---|---|
| 4 | Completion criteria are stated with enough specificity that an independent reviewer could verify them. The criteria name what must be true (not just what will be built). The criteria correspond to the measurement form in Field 3 (binary criteria for binary form; artifact description for qualitative form). |
| 3 | Completion criteria are present and verifiable in principle but one element of specificity is missing (e.g., "deployed on mainnet" without naming the contract or confirming public accessibility). |
| 2 | Completion criteria are present but too vague for independent verification (e.g., "a working prototype" without specifying what working means or how it will be demonstrated). |
| 1 | No completion criteria are present. |

**For retroactive obligation with a forward commitment configured:** Is the forward commitment specific enough to verify at the close of the commitment period?

Apply the build-obligation scoring logic to the forward commitment criteria.

---

## Section 4: Data Quality Standards Assessment

The five data quality standards apply to all evidence claims in the application across all obligation modes. They are assessed as pass/conditional/fail for each standard, separately from the 1-4 indicator field scores. A conditional finding generates a condition equivalent to a score of 2 on an indicator field. A fail finding produces a Do not fund finding for that standard.

In retroactive obligation rounds where the program has not configured indicator-based reporting, assess the data quality standards against the contribution evidence presented in the entry specification. Sections 4's standards still apply to the quality of that evidence.

---

### Standard 1: Validity

**Assessment question:** Could I, with access to the stated data source and the stated construction methodology, confirm that this indicator measures what the applicant claims it measures?

For build-obligation rounds: is there a documented logical chain from the stated completion criteria to the deliverable being what the applicant says it is?

**Common failure mode:** A macro-level adoption metric (ecosystem-wide transaction volume, protocol total value locked) is claimed as evidence of a specific project's contribution. The validity failure is the undocumented causal claim connecting the project's work to the metric's movement.

**Finding options:** Pass, Conditional (a specific gap in the causal documentation can be resolved before disbursement), or Fail (the indicator is structurally disconnected from the claimed result and the problem is not correctable without redesigning the indicator).

---

### Standard 2: Integrity

**Assessment question:** Does any evidence for this application's claims originate from a source independent of the applicant?

For all modes: data collection and reporting must be separated from the actor who benefits from the results. Applicant-controlled dashboards, internal databases, and self-reported results without named independent corroboration do not satisfy this standard on their own.

For build-obligation rounds: the named verifying party in Field 8 (who will confirm the deliverable meets the completion criteria) must be independent of the applicant.

**Finding options:** Pass, Conditional (a specific independent source can be added before disbursement), or Fail (all evidence is applicant-controlled and no independent source is available for the primary outcome claim).

---

### Standard 3: Precision

**Assessment question:** Is the claimed change larger than the variance of the measurement method, or are the completion criteria specific enough to distinguish done from not done?

For change-obligation rounds: the measurement instrument must be capable of detecting changes at the magnitude the project claims to produce.

For build-obligation rounds: the completion criteria must be specific enough to distinguish a passing deliverable from a failing one. Criteria that accept any output ("a working prototype," "some documentation") fail this standard.

**Finding options:** Pass, Conditional (the instrument can be refined to achieve the required precision), or Fail (the instrument is structurally incapable of detecting the claimed effect size or distinguishing completion).

---

### Standard 4: Reliability

**Assessment question:** Has the applicant used different metrics or methodologies for the same indicator in prior reporting, and if so, is the change documented with a rationale?

For first-time applicants: does the methodology specify enough precision that it could be applied consistently across reporting periods?

For continuation grants in any obligation mode: compare the indicator specification in this application against any prior reports on file. Methodology changes are not automatically disqualifying when documented; they are disqualifying when undocumented.

**Finding options:** Pass, Conditional (a specific prior discrepancy can be documented and resolved before disbursement), or Fail (multiple undocumented methodology changes make prior periods incomparable and the baseline is unreliable).

---

### Standard 5: Timeliness

**Assessment question:** Will the data be current at each disbursement decision point given the collection frequency?

For all obligation modes: data must be current to the reporting period. Annual data collection cannot support quarterly disbursement decisions. A completion claim based on work from a prior period not covered by the current gate does not satisfy timeliness.

**Finding options:** Pass, Conditional (a secondary indicator or interim collection method can bridge the frequency gap), or Fail (no feasible collection method can satisfy the timeliness requirement for the proposed disbursement structure).

---

## Section 5: Conformance Checks

The three conformance checks are binary: each either passes or fails. They are not part of the scored rubric. A conformance check failure is not a rigor-tier finding; it is a disqualifying or process-requiring finding that operates independently of indicator scores. A conformance check failure produces a Do not fund recommendation regardless of indicator scores.

---

### Check 1: Concurrent Funding Disclosure

**Test:** Is the concurrent funding disclosure complete? Are all grants, investments, or revenue sources from the prior 24 months related to the scope of this application disclosed, including approximate amounts, relationship to the application's scope, ongoing reporting obligations, and any coordinating or decision-making rights held by funders?

For retroactive obligation rounds: the disclosure must cover prior awards for the same or overlapping work, as well as active grants and investments related to the application's scope.

**Independent evidence:** If the reviewer has independent evidence of a funding relationship not disclosed in the form (public announcements, on-chain treasury flows, prior evaluations from other funders), the application fails this check. The finding must be documented with the source of the independent evidence.

**Finding options:** Pass, or Fail (form is incomplete, a required field is absent, or the reviewer has independent evidence of an undisclosed relationship). Disclosed concurrent funding is not a disqualifier; non-disclosure is.

---

### Check 2: Adverse Signal Disclosure

**Test:** Has the applicant disclosed adverse signals relating to this application: prior rejections from similar programs, contradictory technical findings, or negative due diligence results from other funders?

**Standard:** The Adverse-Signal Engagement Principle Core Standard, incorporated by reference in CROSS, requires applicants to surface signals that contradict their self-presentation. Reviewers must not suppress adverse signals discovered during evaluation.

**Finding options:** Pass (disclosure field is present; signals are disclosed or attested absent; no undisclosed signals discovered by reviewer), or Adverse signal documented (reviewer adds a specific signal to the evaluation record; committee notes it in deliberations). Non-disclosure of a signal the reviewer independently discovers is a process finding the committee weighs in deliberation; it does not automatically disqualify unless the signal also triggers Check 1.

---

### Check 3: Conflict of Interest

**Test:** Has each reviewer completed a conflict of interest declaration before review began? Was the declaration submitted to the named receiving function? Has a post-participation certification been completed?

**Tier 1 violations (categorical bar, no waiver):** Any Tier 1 conflict discovered after a review has been completed disqualifies the entire evaluation. The review must be restarted with a non-conflicted panel.

**Tier 2 violations (disclosure required, qualified waiver possible):** Tier 2 violations discovered during or after review require remediation: retroactive recusal, review restart, or award cancellation, depending on the degree of influence the conflicted party had.

**Finding options:** Pass (all declarations on file, submitted before review began, post-participation certifications complete, no Tier 1 or undisclosed Tier 2 conflicts identified), or Violation (document the tier, the relationship, and the remediation determination).

---

## Section 6: Recommendation Framework

CROSS recognizes three recommendation categories. No other categories exist.

---

### Fund

Available when all of the following conditions are met:

The entry specification gate passes (Section 2 finding is "Gate passes"). All indicator fields score 3 or 4 on the indicator specification rubric (no field scores 1 or 2). All five data quality standards pass. All three conformance checks pass. No unresolved conditions of any type are present.

A score of 3 on one or more indicator fields is compatible with a Fund recommendation. It indicates a minor gap and does not generate a condition. Reviewers note 3-score findings in the evaluation record for the grantee's awareness during reporting.

For retroactive obligation rounds where the indicator rubric does not apply: Fund is available when the entry specification gate passes, the program's published rubric assessment meets the award threshold, and all conformance checks pass.

---

### Fund with Conditions

Available when the gate passes and at least one indicator field scores 2, or at least one data quality standard produces a conditional finding, but no indicator field scores 1, no conformance check fails, and no gate failure has been documented.

Conditions must meet all three of the following requirements. Each condition must specify exactly what must be resolved. Each condition must be verifiable by a named method ("committee review" is not a verification method). Each condition must be time-bounded, with a stated deadline before disbursement occurs.

Conditions attach to disbursement, not to the grant period. Resolution is confirmed before funds are released. The evaluation record must list each condition, the verification method, and the deadline.

---

### Do Not Fund

Required when any of the following apply:

The entry specification gate fails. Any primary indicator field scores 1. Any conformance check fails.

The evaluation record must distinguish which type of failure produced the finding. A gate failure and a rigor-tier failure are both Do not fund findings but carry different messages. A gate failure means the applicant has not performed the required diagnostic work for the declared mode; the path to resubmission is to do that work first. A rigor-tier failure means the diagnostic work exists but the indicator specification is incomplete; the path to resubmission is to complete the specified fields.

For build-obligation gate failures: the applicant has not named a falsifiable deliverable or verifiable completion criteria; the corrective signal is to specify the deliverable and the done criteria.

For change-obligation gate failures: distinguish D2 (applicant has not diagnosed a problem; needs to do diagnostic work before applying) from D1-equivalent rigor failures (applicant has a diagnosis but the specification is incomplete; needs specific field completion).

For retroactive obligation gate failures: the applicant has not provided the required categories of contribution evidence; the corrective signal names which categories were absent.

---

*End of CROSS Assessment Rubric v0.2.0*
