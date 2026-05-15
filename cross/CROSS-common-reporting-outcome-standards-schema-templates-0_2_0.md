---
title: CROSS - Common Reporting Outcome Standards Schema - Templates
version: 0.2.0
date: 2026-05-14
license: CC0
status: Working draft. Companion templates document to CROSS-common-reporting-outcome-standards-schema-0_2_0.md. Supersedes version 0.1.0.
---

# CROSS: Common Reporting Outcome Standards Schema - Templates

Version 0.2.0 | 2026-05-14 | CC0

---

## How to Use This Document

This document contains the fillable forms that applicants, reviewers, and grantees use to implement CROSS version 0.2.0. Each template is self-contained. Brief inline instructions explain what each field requires. Completion checklists appear at the end of each template.

**Which entry specification template to use.** The obligation mode for a round is declared by the funder in the published round specification before the round opens. Applicants do not choose the mode.

- Build obligation round: use Template 1A (Deliverable Specification Form)
- Change obligation round, Small Team scale: use Template 1C (FROM/TO Specification, Small Team)
- Change obligation round, Standard scale: use Template 2 (FROM/TO Specification with Theory of Change)
- Retroactive obligation round: use Template 1B (Retroactive Contribution Form)

All applications also require: Template 3 (Indicator Registration Form, one per indicator), Template 4 (Concurrent Funding Disclosure), and Template 5 (Adverse Signal Disclosure). Reviewers complete Templates 6, 7, and 8 (conflict of interest forms). Template 9 is for privacy-sensitive accommodation requests. Template 10 (Gate Evidence Submission) is used at progress verification and completion verification gates, not at application.

The distinction between Standard and Small Team scale in change-obligation rounds is determined by the granting committee's configuration based on funding amount and the scope of the public impact claim. When in doubt, use the Standard version.

---

## Template 1A: Build Accountability - Deliverable Specification Form

*Use this form when the round operates in build obligation mode. The entry specification asks what the applicant will produce and how a reviewer could verify it is complete. Attach this form to the main application.*

---

### Project Name

> [Enter project name]

---

### Deliverable Name

*A short label for what will be produced. This is not the completion criteria; it is a recognizable name.*

> [Enter deliverable name]

---

### Deliverable Type

*What form will the deliverable take? Select the closest category or name another if none fit.*

- [ ] Working software (library, protocol, tool, module)
- [ ] Deployed smart contract or on-chain protocol
- [ ] Research or design document
- [ ] Dataset or data infrastructure
- [ ] Specification or standard
- [ ] Other: [specify]

**Format for delivery**

*How will the deliverable be made publicly available? Name the repository, registry, publication venue, or other delivery mechanism.*

> [Enter format and delivery location]

---

### Completion Criteria

*What must be true for this deliverable to be considered complete? State the criteria with enough specificity that a reviewer who did not commission the work could verify each one independently. Criteria that a reviewer cannot verify without contacting you do not satisfy this field.*

**Criterion 1**

> [Enter criterion]

**Criterion 2**

> [Enter criterion, add as many criteria as needed]

**Criterion 3**

> [Enter criterion or write "not applicable"]

**Independent verifiability statement**

*In one or two sentences: how would an independent reviewer confirm that each criterion above was met? Name any external source, registry, repository, or named party they would consult.*

> [Enter independent verifiability statement]

---

### Named Beneficiary or User

*Who will use this deliverable? Name at least one specific party (a named organization, developer community, protocol, or user type) outside your own team who has expressed a need for it. This field satisfies the beneficiary validation requirement where the coordinating party engagement dimension is activated.*

> [Enter named beneficiary or user, and briefly describe how the need was expressed]

---

### Coordinating Party Engagement Dimension (if activated by the funder)

*Complete this section only if the funder has activated the coordinating party engagement dimension for this round. Describe the current absence or inadequacy of the deliverable, with named evidence of the gap it addresses.*

**Evidence of the gap the deliverable addresses**

*Name an independent source (a named party who has confirmed the need, an existing tool's documented limitation, or a named data source confirming the gap). Your own assessment of the gap does not satisfy this field.*

> [Enter evidence of the gap, or write "Not activated" if this dimension is not enabled for this round]

---

### Completion Checklist - Template 1A

- [ ] Deliverable name is present and descriptive
- [ ] Deliverable type is selected or named
- [ ] Format and delivery location are specified
- [ ] Completion criteria are stated with enough specificity for independent verification
- [ ] Independent verifiability statement names the source or party a reviewer would consult
- [ ] Named beneficiary or user is provided with a brief description of the expressed need
- [ ] Coordinating party engagement section is completed or marked "Not activated"
- [ ] No fields left blank

---

## Template 1B: Retroactive Accountability - Prior Contribution Form

*Use this form when the round operates in retroactive obligation mode. The entry specification asks what prior contribution was produced, when, and with what evidence of use. Attach this form to the main application.*

---

### Project Name

> [Enter project name]

---

### Contribution Summary

*In two to four sentences: what was produced, when, and what public good does it serve? This is the plain-language description of the prior contribution.*

> [Enter contribution summary]

---

### Contribution Period

*The dates during which the contribution was produced or sustained.*

**Start date:** ___________________________

**End date (or "ongoing"):** ___________________________

---

### Evidence of Contribution

*Name the publicly accessible sources that confirm the contribution exists. Each source must be accessible to an independent reviewer without contacting you. Provide at least two sources.*

| Source | What it confirms | URL or access method |
|---|---|---|
| [Source name] | [What this source confirms about the contribution] | [URL or how to access] |
| [Source name] | [What this source confirms] | [URL or how to access] |
| [Add rows as needed] | | |

---

### Evidence of Use

*Name the publicly accessible evidence that the contribution is being used by parties outside your team. Adoption metrics, named organizations using the contribution, public citations, download counts, or on-chain usage data from named sources all qualify. Self-reported usage without independent corroboration does not satisfy this field on its own.*

| Evidence of use | Source | Scale or scope |
|---|---|---|
| [Describe the usage evidence] | [Named independent source] | [Brief note on scale: e.g., number of users, organizations, or transactions] |
| [Add rows as needed] | | |

---

### Prior Award Disclosure

*List any prior awards received for the same or substantially overlapping contribution, from this or any other program. Non-disclosure is a disqualifier. Disclosure is not.*

- [ ] No prior awards exist for this contribution or substantially overlapping work.

- [ ] Prior awards exist. Complete the table below.

| Program or funder | Award period | Overlap with this contribution |
|---|---|---|
| [Funder name] | [Period] | [Describe the overlap] |
| [Add rows as needed] | | |

---

### Forward Commitment (if configured by the funder)

*Complete this section only if the funder has activated a forward commitment requirement for this round. State the specific action you commit to completing as a condition of receiving the award.*

**Commitment description**

*Name the deliverable or action you commit to.*

> [Enter commitment description, or write "Not configured" if this section does not apply]

**Completion criteria**

*How will a reviewer confirm the commitment was fulfilled? State verifiable criteria.*

> [Enter completion criteria]

**Timeline**

*By when do you commit to completing this?*

> [Enter timeline]

---

### Completion Checklist - Template 1B

- [ ] Contribution summary is present and specific
- [ ] Contribution period is stated
- [ ] At least two sources of independently accessible contribution evidence are named
- [ ] Evidence of use from independent sources is provided
- [ ] Prior award disclosure is complete (either "none" attestation or table)
- [ ] Forward commitment section is completed or marked "Not configured"
- [ ] No fields left blank

---

## Template 1C: Change Accountability - FROM/TO Specification (Small Team Version)

*Use this form when the round operates in change obligation mode and the committee has determined that Small Team scale applies. It captures the essential FROM state and TO state. Attach this form to the main application.*

**Fields omitted from the Standard version and why:** Theory of change formalization (activities, outputs, outcomes, named assumptions), adaptive management mechanism. The Coordination Scaling Standard makes these optional for small-team applications with specific diagnoses and modest claims. All other FROM/TO fields remain required.

---

### Project Name

> [Enter project name]

---

### FROM State: The Condition Before the Intervention

*Describe the specific, measurable problem your project addresses. The FROM state is not a category of concern; it is a documented condition in a defined population. A qualifying FROM state names a condition, a population, a source of evidence, and when that evidence was collected.*

**Condition**

*In one or two sentences: what is the specific problem, expressed as a measurable state? Use numbers, rates, or observable binary conditions where possible.*

> [Enter the specific condition]

**Population**

*Who or what is affected? Name the population precisely: geography, user type, protocol, sector, or other defining characteristic.*

> [Enter the defined population]

**Source of evidence for the FROM state**

*Name the source. It must be accessible to an independent reviewer. Applicant-controlled sources without independent corroboration do not satisfy the integrity standard.*

> [Enter the named source]

**Date or period of measurement**

> [Enter date or period]

---

### TO State: The Expected Condition After the Intervention

**Target condition**

*What specific, measurable state will the indicator be in at grant end? Use the same units as the FROM state.*

> [Enter the target condition]

**Unit of measurement**

*Confirm that this is the same unit used in the FROM state above.*

> [Enter unit of measurement]

**Measurement method at grant end**

*How will you measure the TO state? Name the source and collection approach.*

> [Enter measurement method]

**Timeline**

> [Enter timeline]

---

### Connecting FROM to TO

*One paragraph explaining how your project's activities connect the FROM state to the TO state. Identify one key assumption your explanation rests on.*

> [Enter connecting paragraph]

---

### Completion Checklist - Template 1C

- [ ] FROM state names a specific condition (not a category of concern)
- [ ] FROM state identifies a defined population with sufficient precision
- [ ] FROM state includes a named, independently accessible source
- [ ] FROM state includes a date or measurement period
- [ ] TO state uses the same units as the FROM state
- [ ] TO state is expressed as a target status (non-cumulative) or cumulative total (cumulative)
- [ ] TO state names the measurement method to be used at grant end
- [ ] TO state includes a timeline
- [ ] Connecting paragraph identifies at least one key assumption
- [ ] No fields left blank

---

## Template 2: Change Accountability - FROM/TO Specification with Theory of Change (Standard Version)

*Use this form for Standard scale change-obligation applications. It captures the full FROM state, a formalized theory of change with named assumptions at each step, the TO state, and an adaptive management mechanism. Attach this form to the main application.*

---

### Project Name

> [Enter project name]

---

### FROM State: The Condition Before the Intervention

**Condition**

> [Enter the specific condition]

**Population**

> [Enter the defined population]

**Source of evidence for the FROM state**

> [Enter the named source]

**Date or period of measurement**

> [Enter date or period]

---

### Theory of Change

*A theory of change documents the logical pathway from your project's activities to the outcome you are claiming. Each step requires named assumptions: the conditions that must hold for that step to produce the next.*

**Activities**

| Activity | Description |
|---|---|
| Activity 1 | [Enter activity description] |
| Activity 2 | [Enter activity description] |
| Activity 3 | [Enter activity description, add rows as needed] |

**Assumptions at the activity level**

*What must be true for these activities to be executable as planned?*

> [Enter activity-level assumptions]

**Outputs**

| Output | How you will verify it was produced |
|---|---|
| Output 1 | [Enter verification method] |
| Output 2 | [Enter verification method] |
| Output 3 | [Enter verification method, add rows as needed] |

**Assumptions at the output level**

> [Enter output-level assumptions]

**Outcomes**

| Outcome | Relationship to your primary indicator |
|---|---|
| Outcome 1 | [Enter relationship to indicator] |
| Outcome 2 | [Enter relationship to indicator] |
| Outcome 3 | [Enter relationship to indicator, add rows as needed] |

**Assumptions at the outcome level**

*What must be true for your outputs to produce these outcomes?*

> [Enter outcome-level assumptions]

---

### TO State: The Expected Condition After the Intervention

**Target condition**

*Must use the same units as the FROM state.*

> [Enter the target condition]

**Unit of measurement**

> [Enter unit of measurement]

**Measurement method at grant end**

> [Enter measurement method]

**Timeline**

> [Enter timeline]

---

### Adaptive Management Mechanism

**Monitoring approach**

*How and how often will you check whether your key assumptions are holding?*

> [Enter monitoring approach]

**Decision triggers**

*What evidence of assumption failure or unexpected conditions will prompt a change in activities or outputs?*

> [Enter decision triggers]

**Adjustment authority**

*Who has authority to make significant changes to approach, and how will those changes be reported to the funder?*

> [Enter adjustment authority]

---

### Completion Checklist - Template 2

- [ ] FROM state names a specific condition (not a category of concern)
- [ ] FROM state identifies a defined population
- [ ] FROM state includes a named, independently accessible source
- [ ] FROM state includes a date or measurement period
- [ ] Theory of change lists specific activities, outputs, and outcomes (not categories)
- [ ] Named assumptions appear at each step: activity level, output level, outcome level
- [ ] TO state uses the same units as the FROM state
- [ ] TO state is expressed as a target status (non-cumulative) or cumulative total (cumulative)
- [ ] TO state names the measurement method
- [ ] TO state includes a timeline
- [ ] Adaptive management mechanism names a monitoring approach, decision triggers, and adjustment authority
- [ ] No fields left blank

---

## Template 3: Indicator Registration Form

*Complete one form for each claimed outcome indicator. Submit one form per indicator. Attach all indicator registration forms to the main application.*

*Note: this form applies in build-obligation and change-obligation rounds. In retroactive obligation rounds, complete this form only if the program has configured indicator-based forward reporting.*

*Small Team version note: the Data Cost Estimation field has a simplified version for Small Team applications, noted within that field below. All other fields are identical across both scales.*

---

### Project Name

> [Enter project name]

### Indicator Number

> Indicator number: [e.g., 1 of 3] | [ ] Primary indicator

---

### Field 1: Indicator Name

*A short descriptive label. This is not the operational definition.*

> [Enter indicator name]

---

### Field 2: Rationale for Indicator

*Explain why you selected this indicator over available alternatives. What other indicators did you consider? Why does this one best capture the outcome or deliverable you are claiming? Name at least one alternative considered. This field is mandatory, not optional.*

> [Enter rationale, including alternatives considered and why this indicator was chosen]

---

### Field 3: Measurement Form and Evidence Classification

*Describe what a result looks like and in what form it will be reported. Be specific: name where the evidence comes from, how the result is expressed, and whether values sum across periods or describe a status at a point in time.*

*Useful description (build obligation example): "A binary indicator: either the library is published to the named package registry at the specified version, confirmed by a public repository check, or it is not. Non-cumulative."*

*Useful description (change obligation example): "A count of unique wallet addresses per 30-day window that completed at least one qualifying transaction on the named contract, sourced from on-chain public data via the named block explorer application programming interface. Non-cumulative: each month's count describes the status for that month."*

**Measurement form description**

> [Enter plain-language description of measurement form and evidence]

**Classification (complete or leave for reviewer classification)**

| Axis | Options | Your classification |
|---|---|---|
| Source type | On-chain verifiable / Off-chain verifiable / Qualitative or narrative | [Enter or leave blank] |
| Measurement form | Quantitative / Ordinal / Binary / Qualitative | [Enter or leave blank] |
| Aggregation type | Cumulative (values sum across periods) / Non-cumulative (describes a status at a point in time) | [Enter or leave blank] |

---

### Field 4: Operational Definition

*Specifies what counts and what does not count as one unit of the claimed result. Complete all four sub-fields.*

**4a. Inclusion criteria**

*What qualifies as one instance of this indicator?*

> [Enter inclusion criteria]

**4b. Exclusion criteria**

*What does this indicator explicitly not count?*

> [Enter exclusion criteria]

**4c. Unit of analysis**

*What is the entity being counted or measured? (person, wallet address, transaction, site, organization, other named unit)*

> [Enter unit of analysis]

**4d. Edge case determination**

*At least one example of an ambiguous case and how your operational definition handles it.*

> [Enter at least one edge case example and resolution]

---

### Field 5: Construction and Aggregation Methodology

*The calculation rule in sufficient detail that an independent reviewer with access to your stated data source could replicate your result.*

**Formula or counting rule** *(for build-obligation indicators: the completion determination process)*

> [Enter formula, counting rule, or completion determination process]

**Partial or missing data handling**

> [Enter partial data handling approach]

**Aggregation from sub-units**

> [Enter aggregation approach, or write "Not applicable"]

---

### Field 6: Cumulative or Non-Cumulative

- [ ] **Cumulative.** This indicator sums across reporting periods. The life-of-grant target is a total reached by addition across all periods.

- [ ] **Non-cumulative.** This indicator measures a status at a point in time. The life-of-grant target is the target status at grant end. Summing a non-cumulative indicator across periods is a data construction error.

- [ ] **Not applicable.** Binary completion criteria for a build-obligation deliverable; not subject to period-by-period accumulation.

**Implication for your target**

*In one sentence, confirm what this designation means for how your life-of-grant target is expressed.*

> [Enter confirmation]

---

### Field 7: Disaggregation Categories

**Ratchet notice:** Disaggregation categories committed to in this form may be supplemented in subsequent reporting periods (you may add categories), but may not be removed without committee approval and documented rationale.

| Disaggregation category | How values will be reported separately |
|---|---|
| [Category 1] | [Description] |
| [Category 2] | [Description] |
| [Add rows as needed] | |

*If you do not plan to disaggregate this indicator, write "None committed" and explain why disaggregation is not applicable.*

> [Enter "None committed" with explanation, or leave the table above completed]

---

### Field 8: Data Source and Collection Method

**Named data source**

*For change-obligation indicators: the specific source (contract address, named public application programming interface endpoint, named third-party platform, institutional partner, or named survey instrument). For build-obligation indicators: the named artifact location and the named party who will confirm it meets the completion criteria.*

> [Enter named data source]

**Collection method**

> [Enter collection method]

**Independent corroboration**

*How can an independent reviewer access or verify this data without relying solely on your reporting?*

> [Enter independent corroboration mechanism]

---

### Field 9: Data Cost Estimation

**Standard version:** Provide an estimate of the cost of data collection for this indicator across the full grant period.

**Small Team version (simplified):** Attest that data collection for this indicator is feasible within your project budget using free or low-cost methods.

Select the version that applies:

- [ ] Standard version

> **Approximate cost:** \$[amount]
>
> **Funding source for data collection:** [Grant budget / other named source]
>
> **Budget line item or category:** [Enter line item]

- [ ] Small Team version (simplified)

> **Attestation:** Data collection for this indicator is feasible within our project budget. The data source ([enter source name]) is available at no cost or negligible cost. We have confirmed access to this source.

---

### Field 10: Baseline (FROM State)

*Complete the section that matches the obligation mode.*

**Change-obligation:** The documented state of the condition before the intervention begins.

**Baseline value**

> [Enter baseline value]

**Date or period of baseline measurement**

> [Enter date or period]

**Source of baseline data**

> [Enter baseline source]

**Pre-intervention confirmation**

*Confirm that this baseline was established before your intervention began, or explain why a pre-intervention baseline is not available and what you are using instead.*

> [Enter pre-intervention confirmation or explanation of alternative]

---

**Build-obligation (coordinating party engagement dimension activated):** The documented current absence or inadequacy of the deliverable, with named evidence of the gap.

**Evidence of the gap**

> [Enter named independent evidence of the gap this deliverable addresses, or write "Not applicable" if the coordinating party engagement dimension is not activated for this round]

---

**Retroactive obligation:** The documented state of the prior contribution at the time the award period begins.

**Description of prior contribution state**

> [Enter description of what existed and in what condition at the start of the award period, or write "Not applicable"]

---

### Field 11: Target (TO State)

*Complete the section that matches the obligation mode.*

**Change-obligation:** The expected state of the indicator at grant end.

**Target value**

> [Enter target value]

**Target type (confirm)**

- [ ] Target status (for non-cumulative indicators): the expected state at grant end
- [ ] Cumulative total (for cumulative indicators): the total to be reached by summing across all reporting periods

**Timeline for reaching target**

> [Enter timeline]

---

**Build-obligation:** The completion criteria the deliverable must meet.

**Completion criteria**

*State the criteria with enough specificity that an independent reviewer could determine whether they are met.*

> [Enter completion criteria, or write "Covered in Template 1A" if already specified there]

**How a reviewer would verify completion**

> [Enter verification approach]

---

**Retroactive with forward commitment:** The named action the awardee commits to completing.

**Forward commitment target**

> [Enter forward commitment target with completion criteria, or write "Not configured"]

---

### Completion Checklist - Template 3

- [ ] Indicator name is filled in
- [ ] Rationale explains why this indicator was chosen over alternatives
- [ ] Measurement form is described in plain language with enough specificity to classify
- [ ] Classification table is completed or acknowledged as left for reviewer classification
- [ ] Operational definition includes all four sub-fields
- [ ] Construction methodology is specific enough for an independent reviewer to replicate
- [ ] Partial data handling is addressed
- [ ] Cumulative, non-cumulative, or not applicable is designated with implication confirmed
- [ ] Disaggregation categories are listed or "None committed" is stated with explanation
- [ ] Disaggregation ratchet notice has been read and acknowledged
- [ ] Named data source is specific (not a category)
- [ ] Independent corroboration mechanism is named
- [ ] Data cost estimation is complete (Standard or Small Team version)
- [ ] Baseline section appropriate to the mode is complete
- [ ] Target section appropriate to the mode is complete
- [ ] No fields left blank

---

## Template 4: Concurrent Funding Disclosure Form

*All active grants, investments, or revenue sources from the prior 24 months that are related to the scope of this application must be disclosed. Non-disclosure of concurrent funding is a disqualifier. Disclosure is not.*

*For retroactive obligation applications: also disclose any prior awards received for the same or substantially overlapping contribution from this or any other program.*

*Submit one row per disclosed source. If you have no sources to disclose, complete the attestation at the bottom and state "None."*

---

### Project Name

> [Enter project name]

### Applicant Name or Organization

> [Enter applicant name or organization]

---

### Disclosed Funding Sources

| Field | Entry |
|---|---|
| **Source name** | [Name of investor, foundation, decentralized autonomous organization, protocol, or other funder] |
| **Source type** | [ ] Grant / [ ] Investment / [ ] Revenue / [ ] Prior retroactive award / [ ] Other: [specify] |
| **Approximate amount** | \$[amount] or [describe if non-monetary] |
| **Grant period or investment date** | [Start date to end date, or date] |
| **Relationship to this application's scope** | [Describe how this funding source relates to the work described in this application. If the scopes are non-overlapping, explain why. If they overlap, describe the boundary.] |
| **Ongoing milestone or reporting obligations to this source** | [ ] Yes / [ ] No. If yes: [describe obligations] |
| **Decision-making rights held by this source over the funded work** | [ ] Yes / [ ] No. If yes: [describe rights held] |

*Copy this table for each additional source.*

---

### Attestation

I confirm that the above is a complete and accurate disclosure of all active funding sources related to the scope of this application from the prior 24 months, and (for retroactive applications) all prior awards for the same or overlapping contribution. I understand that non-disclosure of concurrent funding is a disqualifier under CROSS, and that disclosure itself is not a disqualifier.

**Applicant signature (or equivalent attestation):** ___________________________

**Date:** ___________________________

---

### Completion Checklist - Template 4

- [ ] One table per disclosed source
- [ ] Source type is specified for each entry
- [ ] Approximate amount is provided for each entry
- [ ] Grant period or investment date is provided for each entry
- [ ] Relationship to application scope is explained in free text for each entry
- [ ] Ongoing obligations are noted (yes/no with detail) for each entry
- [ ] Decision-making rights are noted (yes/no with detail) for each entry
- [ ] If no sources: "None" is stated explicitly and attestation is signed
- [ ] Attestation is signed and dated

---

## Template 5: Adverse Signal Disclosure Form

*Applicants must surface signals that contradict their self-presentation: prior grant rejections from similar programs, contradictory technical findings, and negative due diligence results from other funders. Reviewers also have an obligation: adverse signals found during evaluation must not be suppressed.*

---

### Project Name

> [Enter project name]

### Applicant Name or Organization

> [Enter applicant name or organization]

---

### Initial Determination

**Do any adverse signals exist relating to this application?**

- [ ] No. I confirm that no prior rejections, contradictory technical findings, or negative due diligence results from other funders exist that are relevant to this application. Proceed to the attestation.

- [ ] Yes. Complete the signal disclosure table(s) below for each adverse signal.

---

### Signal Disclosure (one table per adverse signal)

| Field | Entry |
|---|---|
| **Signal type** | [ ] Prior rejection from a similar program / [ ] Contradictory technical finding / [ ] Negative due diligence from another funder / [ ] Other: [specify] |
| **Source** | [Name the program, funder, publication, or entity] |
| **Date** | [Date of the rejection, finding, or due diligence result] |
| **Brief description** | [Describe the adverse signal in plain terms] |
| **Applicant's explanation** | [Explain how this signal has been addressed, or why it does not affect this application's validity] |

*Copy this table for each additional adverse signal.*

---

### Attestation

I confirm that the above disclosure is complete and accurate to the best of my knowledge. I understand that non-disclosure of adverse signals is a process violation under the Adverse-Signal Engagement Principle Core Standard, whose requirements CROSS incorporates by reference. Disclosure does not disqualify this application; it initiates a structured engagement process.

**Applicant signature (or equivalent attestation):** ___________________________

**Date:** ___________________________

---

### Completion Checklist - Template 5

- [ ] Initial determination is made (yes or no)
- [ ] If no: attestation is signed and dated
- [ ] If yes: one table per adverse signal, all fields complete
- [ ] Signal type is specified for each entry
- [ ] Source is named for each entry
- [ ] Date is provided for each entry
- [ ] Brief description is clear and accurate
- [ ] Applicant's explanation addresses the signal directly
- [ ] Attestation is signed and dated

---

## Template 6: Conflict of Interest Declaration Form - Reviewer Version

*Complete this form before beginning your review of any application. Submit to the designated receiving function (named by the committee; not the person making the funding decision). Do not begin review until you have submitted this declaration.*

---

### Reviewer Name

> [Enter reviewer name]

### Application(s) Being Reviewed

> [Enter application names or identifiers]

### Date of Declaration

> [Enter date]

---

### Tier 1: Categorical Bar - No Waiver Available

*If any Tier 1 relationship exists, you must recuse from this application immediately. There is no waiver process for Tier 1.*

**1a. Direct financial interest in the applicant entity**

*Includes equity, revenue share, or token holdings above the materiality threshold (greater than 1% of circulating supply or greater than the funder's stated materiality threshold in value at time of review).*

- [ ] This relationship exists. Applicant name: ___________________________ Nature of interest: ___________________________ Approximate value: ___________________________
- [ ] This relationship does not exist.

**1b. Family relationship with any principal, director, officer, or owner of the applicant project**

- [ ] This relationship exists. Applicant name: ___________________________ Nature of relationship: ___________________________
- [ ] This relationship does not exist.

**1c. Prior receipt of funding from this funder in the same program area, where your funded work is directly related to the applicant's scope**

- [ ] This relationship exists. Applicant name: ___________________________ Nature of relationship: ___________________________
- [ ] This relationship does not exist.

**1d. Named as a team member, advisor, or contributor on the applicant project's public materials**

- [ ] This relationship exists. Applicant name: ___________________________ Nature of listing: ___________________________
- [ ] This relationship does not exist.

---

### Tier 2: Disclosure Required - Qualified Waiver Possible

*If any Tier 2 relationship exists, do not begin review until written waiver approval is granted by the named authority. Waiver is not available where the relationship creates a financial interest.*

**2a. Employment with the applicant organization in the past 36 months**

- [ ] This relationship exists. Applicant: ___ Period: ___ Role: ___ Waiver justification: ___
- [ ] This relationship does not exist.

**2b. Co-authorship or active project collaboration with applicant principals in the past 48 months**

- [ ] This relationship exists. Applicant: ___ Nature: ___ Period: ___ Waiver justification: ___
- [ ] This relationship does not exist.

**2c. Mentor or student relationship with applicant principals (no expiration)**

- [ ] This relationship exists. Applicant: ___ Nature: ___ Waiver justification: ___
- [ ] This relationship does not exist.

**2d. Governance token voting power exercised on proposals affecting the applicant project**

- [ ] This relationship exists. Applicant: ___ Description: ___ Waiver justification: ___
- [ ] This relationship does not exist.

**2e. Decentralized autonomous organization co-membership in coordinating or committee roles within the same decentralized autonomous organization as the applicant**

- [ ] This relationship exists. Applicant: ___ Organization and role: ___ Waiver justification: ___
- [ ] This relationship does not exist.

**2f. Receipt of an honorarium, award, or gift from the applicant entity in the past 12 months**

- [ ] This relationship exists. Applicant: ___ Nature and value: ___ Waiver justification: ___
- [ ] This relationship does not exist.

**2g. Active job negotiations or arrangements for future employment with the applicant organization**

- [ ] This relationship exists. Applicant: ___ Nature: ___ Waiver justification: ___
- [ ] This relationship does not exist.

**2h. Organizational conflict: your employer has a material financial relationship with the applicant**

- [ ] This relationship exists. Applicant: ___ Nature of employer's relationship: ___ Waiver justification: ___
- [ ] This relationship does not exist.

---

### Tier 3: Disclosure Encouraged

*Disclose any social and community relationships, prior cross-round interactions, or informal mentorship that apply. If the reasonable third party standard is met (an informed observer would conclude you cannot maintain independence), treat the relationship as Tier 2 and request a waiver.*

> [Enter any Tier 3 relationships, or write "None to disclose"]

---

### Web3-Specific Categories

**Token holdings in the applicant project above the materiality threshold**

- [ ] Yes. Amount: ___________________________ (assign to Tier 1 above)
- [ ] No.

**Governance token voting on applicant project proposals**

- [ ] Yes. Description: ___________________________ (assign to Tier 2 above if not financial)
- [ ] No.

**Core contributor or unpaid advisory status on applicant project**

- [ ] Yes. Nature of role: ___________________________ (assign to Tier 1 or Tier 2 depending on nature)
- [ ] No.

**Receipt of investment from the same named investor backing the applicant**

- [ ] Yes. Investor name: ___________________________ (assess under Tier 2 or Tier 3)
- [ ] No.

**Decentralized autonomous organization co-coordinating roles shared with the applicant**

- [ ] Yes. Description: ___________________________ (assess under Tier 2 or Tier 3)
- [ ] No.

---

### Attestation

I confirm that this declaration is complete and accurate to the best of my knowledge. I understand that undisclosed Tier 1 relationships constitute a disqualifying violation and that undisclosed Tier 2 relationships constitute a process violation requiring remediation. The reasonable third party standard applies to novel relationship types not listed above.

**Reviewer signature (or equivalent attestation):** ___________________________

**Date:** ___________________________

---

### Completion Checklist - Template 6

- [ ] All Tier 1 items are checked (yes or no)
- [ ] If any Tier 1 item is checked yes: recusal has been initiated and committee notified
- [ ] All Tier 2 items are checked (yes or no)
- [ ] If any Tier 2 item is checked yes: waiver justification provided and waiver request submitted before review begins
- [ ] Tier 3 free text is completed or "None to disclose" is stated
- [ ] All web3-specific categories are checked
- [ ] Attestation is signed and dated
- [ ] Declaration submitted to the designated receiving function before review begins

---

## Template 7: Conflict of Interest Declaration Form - Applicant Version

*Applicants are required to disclose relationships to committee members and reviewers known to them. This form covers relationships you are aware of at the time of submission. Submit with your application.*

---

### Project Name

> [Enter project name]

### Applicant Name or Organization

> [Enter applicant name or organization]

### Date of Declaration

> [Enter date]

---

### Disclosure of Known Relationships to Committee Members and Reviewers

*For each committee member or reviewer whose identity is known to you, assess whether any of the relationships below exist. You are not required to research the identities of reviewers you do not already know.*

| Committee member or reviewer name | Nature of relationship | Tier assessment | Notes |
|---|---|---|---|
| [Name] | [Description] | Tier [ ] 1 / 2 / 3 | [Any additional context] |
| [Add rows as needed] | | | |

*If no known relationships exist, write "None known" in the first row.*

---

### Tier Definitions for Applicant Reference

**Tier 1 (categorical bar):** Direct financial interest in the reviewer from your project, family relationship, or having the reviewer named on your project's public materials.

**Tier 2 (disclosure required, qualified waiver possible):** Employment of the reviewer by your organization in the past 36 months, co-authorship or active collaboration in the past 48 months, mentor or student relationship, governance token voting by the reviewer on your project's proposals, or organizational financial relationship between your project and the reviewer's employer.

**Tier 3 (disclosure encouraged):** Social and community relationships, prior cross-round interactions, informal mentorship or advisory conversations.

---

### Web3-Specific Categories

**Committee member or reviewer holds tokens in your project above the materiality threshold**

- [ ] Yes. Name(s) and description: ___________________________
- [ ] No known instances.

**Committee member or reviewer has governance voting power on your project's proposals**

- [ ] Yes. Name(s) and description: ___________________________
- [ ] No known instances.

**Committee member or reviewer is a core contributor or unpaid advisor on your project**

- [ ] Yes. Name(s) and description: ___________________________
- [ ] No known instances.

**Committee member or reviewer received investment from the same named investor as your project**

- [ ] Yes. Investor name and description: ___________________________
- [ ] No known instances.

---

### Attestation

I confirm that this declaration is complete and accurate to the best of my knowledge. I understand that this form covers relationships I am aware of at the time of submission and that I will notify the committee administrator promptly if I become aware of additional relevant relationships after submission.

**Applicant signature (or equivalent attestation):** ___________________________

**Date:** ___________________________

---

### Completion Checklist - Template 7

- [ ] All known relationships are listed, or "None known" is stated
- [ ] Each disclosed relationship is assigned to a tier
- [ ] Web3-specific categories are assessed and checked
- [ ] Attestation is signed and dated
- [ ] Submitted with the application

---

## Template 8: Post-Participation Conflict of Interest Certification - Reviewer Version

*Complete this form after your review of an application is complete. Submit to the designated receiving function alongside your review output.*

---

### Reviewer Name

> [Enter reviewer name]

### Application(s) Reviewed

> [Enter application names or identifiers]

### Date of Review Completion

> [Enter date]

---

### Certification

**1. No new conflicts arose during review.**

During my review of the application(s) listed above, no new relationships, financial interests, or other conflicts arose that were not disclosed in my pre-review conflict of interest declaration. My pre-review declaration remained accurate throughout the review process.

- [ ] Confirmed.
- [ ] Not confirmed. I became aware of the following during review: ___________________________ *(Submit this form to the committee administrator immediately for remediation guidance.)*

**2. Declaration remained accurate.**

The relationships and declarations in my pre-review conflict of interest declaration accurately reflected my situation throughout the review period.

- [ ] Confirmed.
- [ ] Not confirmed (see above).

---

**Reviewer signature (or equivalent attestation):** ___________________________

**Date:** ___________________________

---

### Completion Checklist - Template 8

- [ ] Reviewer name and application(s) reviewed are listed
- [ ] Date of review completion is provided
- [ ] Certification items 1 and 2 are both checked confirmed, or discrepancy is described and reported
- [ ] Signed and dated
- [ ] Submitted to the designated receiving function

---

## Template 9: Privacy-Sensitive Context Accommodation Request

*For applications invoking the privacy-sensitive accommodation for indicator sourcing. The accommodation specifies which obligation mechanisms are appropriate to a context where standard measurement would compromise beneficiary safety; it is not an exemption from obligation. Submit with the Indicator Registration Form for the affected indicator(s).*

---

### Project Name

> [Enter project name]

### Applicant Name or Organization

> [Enter applicant name or organization]

### Indicator Number(s) Affected

*Reference the indicator number from Template 3.*

> [Enter indicator number(s)]

---

### Field 1: Standard Measurement Methodology That Would Normally Apply

*Describe the standard approach that would typically be used for this type of indicator if no privacy concern existed.*

> [Enter the standard methodology that would normally apply]

---

### Field 2: Specific Harm the Standard Methodology Would Create

*Name the specific harm, concretely: the population, the mechanism of harm (legal exposure, identification by state actors, retaliation risk), and why this harm is credible in the specific context. Generic references to "privacy" do not satisfy this field.*

> [Enter the specific harm, population, and harm mechanism]

---

### Field 3: Alternative Methodology Proposed

**Description of alternative methodology**

> [Enter description of the alternative methodology]

**How this methodology produces verifiable outcome evidence**

*Explain how an independent reviewer could confirm, without access to beneficiary-identifying information, that the claimed outcome was produced.*

> [Enter explanation of verifiability]

---

### Field 4: Institutional Partner or Established Methodology

*The alternative must draw on an institutional partner or established methodology recognized in the relevant field.*

**Named partner or methodology**

> [Name the partner or methodology]

**Explanation of appropriateness**

> [Explain why this partner or methodology is appropriate to this specific context]

---

### Field 5: Confirmation of Verifiable Outcome Evidence

- [ ] I confirm that the alternative methodology will produce verifiable outcome evidence that an independent reviewer can assess without requiring access to beneficiary-identifying information.

> [Enter confirmation, or describe which condition is not met and what alternative assurance mechanism you propose]

---

### Attestation

**Applicant signature (or equivalent attestation):** ___________________________

**Date:** ___________________________

---

### Completion Checklist - Template 9

- [ ] Standard methodology is named specifically
- [ ] Specific harm is described concretely with named population and harm mechanism
- [ ] Alternative methodology is described in sufficient detail for independent assessment
- [ ] Explanation of verifiability is provided
- [ ] Institutional partner or established methodology is named
- [ ] Confirmation of verifiable outcome evidence is checked
- [ ] Attestation is signed and dated
- [ ] Submitted with the relevant Indicator Registration Form

---

## Template 10: Gate Evidence Submission Form

*Use this form to submit evidence at a progress verification gate or a completion verification gate. Do not use this form at the entry specification stage; the entry specification is part of the application. Submit to the designated funder contact by the published gate deadline.*

---

### Project Name

> [Enter project name]

### Grant Reference

> [Enter grant identifier or round name]

### Gate Being Submitted For

- [ ] Progress verification gate (tranche disbursement)
  - Which tranche: _______________
  - Published gate deadline: _______________
- [ ] Completion verification gate (final payment)
  - Published gate deadline: _______________
- [ ] Continuation specification gate (progression to next stage)
  - Stage being applied for: _______________

### Date of Submission

> [Enter date]

---

### Round Configuration (confirm from published round specification)

**Obligation mode:** [ ] Build / [ ] Change / [ ] Retroactive

**Evidence scope required at this gate:** [ ] Output / [ ] Usage / [ ] Outcome / [ ] Impact

**Evidence strength required at this gate:** [ ] Self-report with documentation / [ ] Third-party verifiable / [ ] Independent review / [ ] Independent evaluation

---

### Evidence Package

*Complete the section that matches the obligation mode.*

---

**Build Accountability Evidence**

**Deliverable status**

*Describe what has been produced and its current state relative to the published completion criteria.*

> [Enter deliverable status]

**Evidence of public accessibility** *(required at completion verification gate)*

*Provide the public URL, repository link, registry entry, or other publicly accessible location where the deliverable can be found and verified.*

> [Enter public location]

**Completion criteria check**

*For each completion criterion stated in the entry specification (Template 1A or Template 3), confirm whether it is met and provide evidence.*

| Criterion | Status | Evidence |
|---|---|---|
| [Criterion from entry spec] | [ ] Met / [ ] In progress / [ ] Not yet met | [Named evidence source or artifact] |
| [Add rows as needed] | | |

**Named verifying party** *(required if gate is at independent review level)*

*Name the party who has confirmed the deliverable meets the completion criteria.*

> [Enter verifying party name and role, or write "Not required at this gate level"]

---

**Change Accountability Evidence**

**Indicator and reporting period**

*Name the primary indicator and the period this submission covers.*

> Indicator: _______________
> Reporting period: _______________

**Reported value**

> Value: _______________
> Source: _______________
> Collection date: _______________

**Change from baseline**

> Baseline (FROM state): _______________
> Current value: _______________
> Target (TO state): _______________
> Progress toward target: _______________

**Evidence documentation**

*Provide the publicly accessible evidence source or attach the evidence package. Name the source and the collection method used.*

> [Enter evidence source and collection method]

**Named reviewer** *(required if gate is at independent review level)*

> [Enter reviewer name and role, or write "Not required at this gate level"]

---

**Retroactive with Forward Commitment**

**Forward commitment reference**

*Reference the commitment stated in Template 1B.*

> [Enter commitment description]

**Completion status**

> [Describe what was completed and when]

**Completion evidence**

> [Named publicly accessible evidence that the commitment was fulfilled]

---

### Applicant Attestation

I confirm that the evidence submitted in this form is accurate and complete to the best of my knowledge. I understand that grantee self-report alone does not satisfy the completion verification gate and that the funder will review this submission against the published completion criteria before releasing final payment.

**Applicant signature (or equivalent attestation):** ___________________________

**Date:** ___________________________

---

### Completion Checklist - Template 10

- [ ] Project name, grant reference, and gate type are specified
- [ ] Round configuration (mode, evidence scope, evidence strength) is confirmed from the published round specification
- [ ] Evidence section appropriate to the mode is completed
- [ ] For build obligation at completion gate: public accessibility location is provided
- [ ] For gates at independent review level: named reviewer or verifying party is identified
- [ ] Applicant attestation is signed and dated
- [ ] Submitted by the published gate deadline

---

*End of CROSS Templates, version 0.2.0.*
