---
title: CROSS - Common Reporting Outcome Standards Schema - Guidance
version: 0.2.0
date: 2026-05-14
license: CC0
status: Working draft. Companion guidance document to CROSS-common-reporting-outcome-standards-schema-0_2_0.md. Supersedes version 0.1.0.
---

# CROSS: Common Reporting Outcome Standards Schema - Guidance

Version 0.2.0 | 2026-05-14 | CC0

---

This document is the practitioner companion to CROSS (Common Reporting Outcome Standards Schema) version 0.2.0. It does not restate the standard. It explains how to apply the standard's criteria, what qualifies and what does not at each decision point, and what the most common failure modes look like. It is written for two audiences: applicants completing a CROSS-conformant grant application, and reviewers evaluating one.

This version of the guidance covers three obligation modes: build obligation, change obligation, and retroactive obligation. Part 1 covers the entry specification for each mode. Part 2 covers the gate architecture. Parts 3 through 9 cover indicator specification and conformance requirements that apply across modes, with mode-specific notes where the application differs.

---

## Part 1: How to Answer the Entry Specification

### 1A: Build Obligation

**What the entry gate is asking.** Can the applicant name a falsifiable deliverable with independently verifiable completion criteria?

A falsifiable deliverable is an artifact, product, or documented output whose existence and quality can be confirmed by a reviewer who did not commission the work. The test is not whether the deliverable will be valuable or widely adopted. The test is whether a reviewer at the end of the grant period, looking at what was submitted, could determine whether it was done.

**What makes a deliverable specification falsifiable.** A deliverable specification is falsifiable when the completion criteria are specific enough that failure is a recognizable outcome. "Build a reporting tool" is not falsifiable because any tool, however incomplete, could be claimed to satisfy it. "A reporting module that produces a human-readable fee summary for any ERC-4626 vault, published as an open-source library under MIT license, with at least one deployed instance on Ethereum mainnet, a documented application programming interface, and a test suite covering the three functions specified in the design document" is falsifiable because a reviewer can check each element.

The completion criteria do not need to be technical. "A research report of at least 15,000 words, published under a Creative Commons open license, covering the three questions named in the application's research plan, with a literature review, at least five primary source interviews, and a named target audience who received the draft before publication" is falsifiable. The reviewer can count words, check the license, verify the scope, and confirm whether the interviews and review were conducted.

**What disqualifies a build-obligation entry specification.** The primary failure mode is offering a direction or vision in place of a deliverable. "Making DeFi more transparent" is a direction. "Building better tooling for privacy" is a direction. A direction cannot be verified at grant end because it does not specify what done looks like. An application that describes what it is trying to achieve, not what it will produce, fails the entry gate.

A second failure mode is naming a deliverable without specifying completion criteria. "A working prototype" names a form (a prototype) but not a standard (what working means). A reviewer cannot verify whether a prototype is working without criteria. The entry gate requires both: a named artifact and verifiable criteria for what counts as complete.

**Build obligation is not the same as "has begun building."** Some programs incorrectly apply change-obligation gate logic to build-obligation applications, treating an applicant who has already started building as though that is a suspicious circumstance. It is not. A team that has already built part of what they are proposing is in a stronger position to specify the deliverable and the completion criteria precisely, because they have working knowledge of the problem. The entry gate asks whether the commitment is falsifiable; it does not ask when the work began.

**The deliverable specification at different scales.** A small-team discovery sprint and a large multi-stage development program both use build obligation, but the depth of specification is calibrated to scale. A small team committing to a design document needs: the document type, the scope (what questions it addresses or what design decisions it makes), the format for delivery (public publication, named repository, or named partner), and what constitutes a complete document. A large development program additionally needs: milestone-level completion criteria for each grant period, a named verification mechanism at the completion gate, and evidence that the deliverable will be publicly accessible.

---

### 1B: Change Obligation

**What the entry gate is asking.** Can the applicant name the FROM state as a specific measurable condition in a defined population?

This is the gate that appeared in version 0.1.0 as the sole entry gate. In version 0.2.0, it is correctly scoped to change-obligation rounds. The Theory of Build gate now refers to a named failure mode within this mode (offering a deliverable commitment where a problem diagnosis is required), not to the gate itself.

**The FROM state.** A FROM state is specific when it names a condition. A condition describes an observable state that exists in the world and can be measured. A category describes a type of problem without grounding it in an observable measurement. The difference matters because conditions can be verified; categories cannot.

A FROM state that passes: "96 to 99 percent network reachability drops for users in Iran during government-imposed shutdowns, as measured by Open Observatory of Network Interference probe data from 2023 to 2025." This names a measurable quantity (reachability rate), a defined population (users in Iran), a triggering condition (government-imposed shutdowns), a data source (Open Observatory of Network Interference probe data), and a time period (2023 to 2025). A reviewer can verify that this condition exists.

A FROM state that fails: "There is a lack of privacy tools for people in repressive contexts." This names a category (lack of privacy tools) and a vague population (people in repressive contexts). Neither is measurable. A reviewer cannot verify whether this condition exists or how severe it is.

**Class D2 failure (values aspiration without conditions).** Some applications offer values language, community commitments, or a mission statement in place of a diagnosis. When asked for a specific FROM state, these applications produce more values language because no diagnostic work preceded the application. They articulate what they are trying to achieve: more privacy, better coordination, greater equity. These are directions, not conditions. Applications of this type cannot produce a plausible FROM state on request because the diagnostic work was not done before the application was written.

This is a structural failure, not a communication failure. Applicants in this situation cannot name the FROM state because they do not know what it is. They began with a desired outcome and worked backward to a scope of work, rather than beginning with a documented problem and working forward to an intervention designed to address it.

**Class D1 failure (canonical vocabulary without structural grounding).** A second type of application passes the gate because it uses technically correct vocabulary and names something resembling a problem diagnosis. The failure appears at the rigor tier: the specific measurable indicators are unsupported, the baseline is undocumented, or the construction methodology cannot be replicated. An application of this type may score 2s and 1s across the indicator rubric after passing the gate.

These two failure types require different responses from a review committee. A D2 failure is a gate failure: the path to resubmission is to do the diagnostic work first. A D1 failure is a rigor-tier failure: the path to resubmission is specific field completion. Treating a D1 failure as a D2 failure misdirects the applicant.

**Application timing is not the diagnostic.** A team that built something before the grant application opened is not automatically exhibiting a gate failure. They can name the FROM state precisely because they built the solution to address it. Application-window activity is a weak corroborating signal about whether work was shaped around funder expectations; it is not a gate criterion.

**Build nested inside change is valid.** Describing what will be built is not a failure in a change-obligation round. What matters is whether the build commitment replaces or sits inside the change specification. Build is validly nested when the applicant can name a FROM state that satisfies the entry gate, and the built thing is the mechanism for addressing that condition. The change specification is intact; the build is the delivery vehicle for the change. Build becomes the failure mode when it has replaced the change specification entirely: the applicant names a deliverable where a problem diagnosis was required, and cannot produce a FROM state because the problem was never diagnosed before the solution was designed. An applicant who began with the problem produces the FROM state naturally, because naming a specific measurable condition in a defined population is the output of having diagnosed it. An applicant who began with the solution cannot, because no problem was named before the solution was conceived.

**Change obligation at different scales.** A small team with a clear diagnosis and a modest claim needs less formal documentation of the FROM state than a large institutional applicant making a broad population-level claim. The Coordination Scaling Standard calibrates this. Both must name a specific measurable condition; the depth of corroboration and the formality of the indicator specification scale upward with the scope of the claim.

---

### 1C: Retroactive Obligation

**What the entry gate is asking.** Does the applicant present evidence of prior contribution meeting the program's published threshold criteria?

Retroactive obligation is not the absence of obligation; it is obligation for what has already happened. The applicant must demonstrate, not assert, that prior contribution occurred. The difference is evidence that an independent reviewer can access and assess without relying on the applicant's self-report.

**What qualifies as evidence of prior contribution.** Evidence that meets the standard is publicly accessible from sources the applicant does not control. On-chain usage data with a named contract address or deployment record. A public code repository with a documented commit history, stars, forks, or downloads. Published documentation that other projects cite. Named organizations or individuals who use the contribution and can confirm that use. Ecosystem metrics from named third-party data providers.

What does not qualify on its own: the applicant's description of their own work, a team bio, or a list of features the applicant says they built. These may be accurate but they are not independently verifiable. They must be accompanied by at least one external source that confirms the contribution is real and in use.

**The prior award disclosure requirement.** Retroactive applications must disclose any prior awards received for the same or substantially overlapping contribution, from this or any other program. This is the concurrent funding disclosure requirement applied to the retroactive context. Receiving multiple retroactive awards for the same contribution is not automatically disqualifying, but it must be disclosed and may be weighted in the rubric assessment. Non-disclosure is a disqualifier.

**The forward commitment option.** Programs may configure a forward commitment as a condition of the retroactive award. If activated, the awardee commits to a named forward action (a specified deliverable, a continuation commitment, a public-access maintenance obligation) as a condition of receiving the award. The forward commitment is assessed under build-obligation criteria: it must name a falsifiable deliverable with verifiable completion criteria. If a program has activated a forward commitment and the applicant's forward commitment fails the build-obligation entry specification, that is a rigor-tier finding, not a gate failure for the retroactive application itself.

**What reviewers are assessing.** The program's published rubric governs the substantive scoring of retroactive applications; it is not the same as the CROSS indicator specification rubric. The CROSS conformance checks (concurrent funding disclosure, adverse signal disclosure, conflict of interest) apply in full. The indicator specification rubric in Section 3 of the assessment rubric applies only if the program has configured indicator-based forward reporting alongside the retroactive award.

---

## Part 2: Gate Architecture

Understanding the gate architecture helps applicants prepare the right evidence at the right time, and helps reviewers know what they are authorized to require.

### The four gates

The entry specification gate determines who enters the round. Its content depends on the mode (Part 1 above). It is always present; what it asks is mode-specific.

Progress verification gates trigger mid-funding disbursements. Each tranche disbursement is contingent on verification of progress against the milestone committed at the prior stage. The minimum acceptable evidence at a progress verification gate is a publicly linkable artifact demonstrating work toward the specified deliverable or indicator. Funders may configure higher evidence requirements. Where no mid-funding disbursement is planned, progress verification gates are not required.

The completion verification gate determines who receives final payment. This gate cannot be informal. The funder must have a published mechanism for determining whether completion criteria have been met. Grantee self-report alone does not satisfy the completion verification gate at any evidence strength level.

For build-obligation rounds: the completion gate must additionally confirm that the specified deliverable is publicly accessible before final payment is released. A deliverable that was produced but is not public does not satisfy a build-obligation completion gate.

For change-obligation rounds: the completion gate requires outcome evidence against the baseline established at entry, assessed by the named mechanism in the infrastructure declaration.

The continuation specification gate governs progression across rounds or stages. It is configured at the program level, not the round level, and it must be published before any round in the program opens. It is the primary mechanism for escalating evidentiary pressure as a project matures.

### What applicants need to know about gate configuration

Before applying to any round, applicants should confirm: which gates are active, what evidence scope and strength is required at each gate, and whether the funder has published an infrastructure declaration for gates at independent review level. The infrastructure declaration names who will review the evidence, their qualifications, and the timeline. If a gate is configured at independent review level and no infrastructure declaration is present, the funder has a conformance obligation to fulfill before the round can proceed.

The gate configuration cannot be retrospectively tightened against applicants who entered the round under a published configuration. A funder may not apply a higher evidence requirement than was published at round opening. A funder may not waive a published requirement without documented rationale submitted to a named authority before the gate is reached.

### Evidence scope and strength

Evidence scope describes what kind of evidence the gate accepts: output evidence (the deliverable exists), usage evidence (the deliverable is being used by external parties), outcome evidence (a measurable change has occurred in the specified population), or impact evidence (a credible causal link is established between the funded work and the measured change).

Evidence strength describes the verification mechanism: self-report with documentation (grantee narrative reviewed by funder staff), third-party verifiable (publicly accessible from sources outside the applicant's control), independent review (a named party outside the funder-grantee relationship confirms the evidence), or independent evaluation (a qualified evaluator conducts a structured assessment).

Applicants who understand these two dimensions can calibrate their evidence preparation to the gate requirements. A progress verification gate configured at output scope and self-report strength needs a publicly linkable artifact and a brief narrative. A completion verification gate configured at outcome scope and independent review strength needs a structured outcome report with data at the operational definition level and a named reviewer who has agreed to conduct the assessment.

---

## Part 3: How to Complete Each Indicator Field

CROSS requires applicants to self-specify their outcome indicators. The funder specifies the domain; the applicant specifies what their intervention produces within it. CROSS specifies the fields each indicator must contain and the quality standards those fields must meet.

### Field 1: Indicator name

A short descriptive label. Not the operational definition. Keep names short and move the precision to Field 4. A name that tries to contain the operational definition ("number of users meaningfully engaged with privacy-preserving tools on a sustained basis") is trying to do too much; the qualifier language belongs in Field 4.

### Field 2: Rationale for indicator

Rationale is mandatory. It documents the diagnostic thinking that preceded tool selection. A weak rationale restates the claim without defending the choice ("this indicator measures our core outcome"). A strong rationale names at least one alternative indicator considered and explains why the chosen indicator better matches the intervention's causal claim. The rationale should also note what the indicator does not capture; an applicant who describes the indicator's limitations demonstrates a more mature understanding of the measurement problem than one who describes only its strengths.

### Field 3: Measurement form and evidence classification

This field replaces the constrained four-option data type list from version 0.1.0. Applicants now describe the measurement form in plain language. Reviewers classify the description against three axes for data quality assessment purposes.

**What to write in this field.** Name what a result looks like and in what form it will be reported. Be specific enough that a reviewer can answer three questions: where does the evidence come from (on-chain, off-chain verifiable source, or qualitative/narrative assessment), how is the result expressed (as a number, a position on a scale, a binary yes/no, or a documented condition), and how do period values relate (can they be summed, or does each period describe a status point in time?).

A useful description: "A count of unique wallet addresses per month that completed at least one qualifying transaction on the named contract, sourced from on-chain data via the named block explorer application programming interface. This is a non-cumulative indicator: each month's count reports the status for that month; the life-of-grant target is the count in the final month, not the sum of all months."

A description that requires the reviewer to infer too much: "User engagement metrics." This names a category, not a form.

**Mode-specific notes on measurement form.**

For build-obligation indicators: the form is typically binary (the deliverable either meets the completion criteria or does not) or qualitative (the deliverable is an artifact assessed against named criteria). The description should name what done looks like and how a reviewer would confirm it: "A binary yes/no indicator: either the library is published to the named package registry with the specified version number and passes the automated tests in the public repository, or it is not. Confirmed by the named reviewer checking the registry and the test results."

For change-obligation indicators: the form is typically quantitative or ordinal. Name the unit of measurement and the direction of desirable change: "A quantitative indicator expressed as a count of unique addresses per 30-day window, sourced from on-chain public data. An increasing count indicates progress toward the target."

For retroactive indicators where a forward commitment is configured: apply the build-obligation description guidance to the forward commitment indicator.

**The common error in this field.** Applicants who come from the v0.1.0 format sometimes try to select one of the old four options (number, percentage, yes/no, index). The field no longer works that way. Index and composite indicators require the same plain-language description as any other indicator, with the component specification in the construction methodology field (Field 5) rather than in a sub-table here.

### Field 4: Operational definition

The operational definition specifies what counts and what does not count as one unit of the claimed result. It has four required sub-components.

Inclusion criteria define what qualifies as one instance. Example: "A unique wallet address that completed at least one transaction using the protocol's privacy module during the reporting month, as recorded by the named contract address on Ethereum mainnet."

Exclusion criteria name what the indicator explicitly does not count. Example: "Test transactions from the development team's identified wallet addresses. Transactions on testnet. Transactions using the non-privacy-preserving legacy module." Exclusions matter because without them a reviewer cannot determine whether reported numbers are clean.

Unit of analysis is the named entity being counted: person, household, wallet address, transaction, site, session, message, or other. The unit must be consistent throughout the indicator's life. If the unit changes between reporting periods, the comparability of prior periods must be formally assessed and documented.

Edge case determination is at least one example of how an ambiguous instance is handled. Example: "A wallet address that transacts using both the privacy module and the legacy module in the same reporting month is counted once in the privacy module indicator and once in the legacy module indicator, not twice in either." Edge cases that are not specified in advance produce inconsistent counting criteria across periods. The operational definition is the field that makes cross-funder and cross-period comparability possible.

For build-obligation indicators, the operational definition specifies what completion means at a level of precision that resolves ambiguity: what qualifies as one passing instance of the deliverable, what does not qualify, and how an edge case (a deliverable that meets some but not all criteria) is handled.

### Field 5: Construction and aggregation methodology

The calculation rule in sufficient detail that an independent reviewer with access to the stated data source could replicate the result without contacting the applicant. Three elements are required: the formula or counting rule, how partial data is handled, and how values from sub-units are aggregated to the project level.

An unusable description: "We track user engagement through our analytics platform and report quarterly." A reviewer cannot replicate this. A replicable description: "We query unique visitor counts from Plausible Analytics at the project domain, using the application programming interface endpoint at [named location], with the date range set to the reporting quarter, counting unique visitor fingerprints as defined by Plausible's methodology, excluding traffic from the IP ranges listed in our exclusions table."

For build-obligation indicators: the methodology specifies how completion is determined, who performs the verification, and by what process. "Completion is determined by the named reviewer, who will check that the library is published to the named package registry at the specified version, that the named test suite passes without errors in the public continuous integration log, and that the application programming interface documentation is publicly accessible at the named location. The reviewer will document their finding in a brief written statement submitted to the program within two weeks of the submission deadline."

### Field 6: Cumulative or non-cumulative

A cumulative indicator can be summed across reporting periods. If a project commits to 1,200 unique users over a twelve-month grant and the indicator is cumulative, the target is reached when the running total equals 1,200. Each period adds to the previous total.

A non-cumulative indicator measures a status at a point in time. If a project commits to 500 active monthly users by grant end, the target is the status at grant end, not a sum. Summing a non-cumulative indicator across periods is a data construction error: it would be like adding January's temperature to February's temperature to get the year's total temperature.

Reviewers must flag this designation at the application stage. A project that specifies a non-cumulative indicator but sets a life-of-grant target that can only be reached by summing across periods has a structural inconsistency that, if uncorrected, will produce a reporting dispute at grant end.

### Field 7: Disaggregation

Disaggregation categories specify how the indicator will be reported broken down by subgroup: by geography, by user type, by protocol version, by language, or by other named categories.

The disaggregation ratchet is a one-way constraint: categories committed to in the application may be supplemented in subsequent reporting periods but may not be removed without committee approval and documented rationale. The purpose is to protect longitudinal comparability. Adding a new category enriches the data; removing one degrades it.

When requesting approval to remove a category, the applicant must document the reason and specify how prior-period comparability will be preserved or documented as broken.

### Field 8: Data source and collection method

The named source must be accessible to an independent reviewer. Named on-chain contract addresses, named public application programming interface endpoints, named third-party platforms with documented methodology, named institutional partners, and named survey instruments administered by third parties satisfy this requirement.

Sources that do not satisfy the integrity standard on their own: applicant-controlled dashboards with no external corroboration, internal databases accessible only to the applicant, and self-reported results without a named external verification mechanism. These may be supplementary evidence; an indicator whose sole evidence originates from applicant-controlled systems fails the integrity standard.

Naming the source is not the same as describing the collection method. "Google Analytics" is not a collection method. "Monthly unique visitor count exported from Google Analytics property [named ID] using the standard unique users metric, with bot filtering enabled, covering the date range [specified]" is a collection method.

For build-obligation indicators: the data source for completion verification is the named artifact plus the named verifying party. "The library repository at [named public URL], confirmed by [named reviewer] against the completion criteria listed in the application."

### Field 9: Data cost estimation

An attestation that data collection is operationally feasible within the project budget. Where data collection is free, name the source and confirm access. Where it has a cost, provide an approximate cost and name the budget line that funds it.

An indicator that cannot be collected within the project budget has not been operationalized. It is a commitment the project cannot keep.

### Field 10: Baseline (FROM state)

For change-obligation indicators: the documented state of the problem before the intervention begins. Specific, measurable, and sourced. Specific means a named condition, not a category. Measurable means expressed in the same units as the indicator and target. Sourced means the measurement originated from a named source independent of the applicant.

A sourced baseline: "As of December 2025, 340 unique wallet addresses per month had completed at least one transaction using the protocol's privacy module, based on on-chain data from the named contract address, queried using the specified application programming interface." This names the measurement, the unit, the source, and the time point. A reviewer can verify it independently.

For build-obligation indicators where the coordinating party engagement dimension is activated: the documented current absence or inadequacy of the deliverable, with named evidence of the gap it addresses. A named party outside the applicant's organization who has confirmed the need, or a named existing tool's documented limitation, satisfies this requirement. The applicant's assertion of the gap does not.

For retroactive obligation indicators: the documented state of the contribution at the time the award period begins, with named evidence of use. The prior contribution replaces the pre-intervention baseline; the evidence of use replaces the data source for the baseline value.

### Field 11: Target (TO state)

For change-obligation indicators: the expected state of the indicator at the end of the grant period, expressed in the same units as the baseline and operational definition. For cumulative indicators, a cumulative total. For non-cumulative indicators, a target status at grant end.

A target not grounded in the baseline creates an obligation vacuum. A project claiming a six-fold increase against baseline requires an explanation of the mechanism that produces that growth. Without it, the target is aspirational rather than evidence-grounded.

For build-obligation indicators: the completion criteria the deliverable must meet, expressed with enough specificity that an independent reviewer could determine whether they are met. "A working prototype" fails. "A prototype that executes the three functions specified in the design document, demonstrated in a public recording with no fatal errors, with test results from the specified test suite attached" passes.

For retroactive obligation with a forward commitment: the named action the awardee commits to completing as a condition of the award, expressed with falsifiable completion criteria. Apply the build-obligation guidance to the forward commitment target.

---

## Part 4: Common D1 Indicator Sourcing Failures in Change-Obligation Rounds

Class D1 (canonical vocabulary without structural grounding) passes the entry specification gate and fails at the rigor tier. Three patterns account for most D1 sourcing failures.

**The single-day peak metric.** The indicator is a metric derived from a single-day peak rather than a sustained measurement. An application reports a FROM state of "up to 50,000 users" accessing the network during the largest observed traffic event, as evidence of baseline demand. The "up to" language signals a maximum observation, not a median or average. Reviewers identify this pattern by checking whether the baseline is expressed with a central tendency measure (mean or median) and a variance measure, or only as a peak. A sourced baseline expressed only as a maximum without a distribution is not a reliable baseline for calculating change.

**The reach figure without a collection method.** A reach figure ("we have reached 10,000 people with this information") with no specified collection method. The number is present; the mechanism by which it was determined is absent. A count of newsletter subscribers is not the same as a count of people who read the newsletter. A count of social media impressions is not a count of people. Reviewers identify this pattern by checking Fields 5 and 8 against the reported number.

**The applicant-self-assertion baseline.** The coverage claim or baseline is sourced only from the applicant's own assertions, internal records, or self-reported data without named independent corroboration. A conformant application in this situation names the limitation explicitly, proposes a verification mechanism for future reporting periods, and differentiates what is known from independent sources from what is known only from internal records.

---

## Part 5: Concurrent Funding Disclosure in Practice

### What "related to the scope of this application" means

The disclosure requirement covers all active grants, investments, or revenue sources from the prior 24 months that are related to the scope of the application. "Related" is interpreted broadly: it covers funding that supports the same work, the same product, the same team's capacity to do this work, or the same beneficiary population through an overlapping mechanism.

### What must be disclosed

Venture capital investment in the same product or platform the grant work extends. A grant from another funder for the same work, running concurrently. Revenue from a commercial product that the grant work extends or subsidizes. Token issuance or protocol revenue that funds team operations, where the team's operations overlap with the scope of the grant.

For retroactive applications: all prior awards for the same or substantially overlapping contribution, from this or any other program, in any period.

### What need not be disclosed

Unrelated work by team members that does not overlap with the grant scope. Personal income from employment unrelated to the grant scope. Prior grants in different program areas with no overlap with the current application's scope or beneficiary population.

### Non-disclosure versus disclosure

Disclosure is not a disqualifier. A project with venture capital backing can receive public goods grant funding if the relationship between commercial financing and the public goods ask is clearly articulated and the grant is specifically scoped to work the commercial funding does not cover.

Non-disclosure is a disqualifier. It is not treated as an error that can be remediated. An applicant who fails to disclose a material concurrent funding relationship, where that relationship is subsequently discovered by reviewers, faces disqualification. The asymmetry is deliberate: non-disclosure is an integrity failure, not a paperwork failure.

---

## Part 6: Adverse Signal Disclosure in Practice

### What the Adverse-Signal Engagement Principle Core Standard requires in the grant context

The Adverse-Signal Engagement Principle Core Standard requires that applicants surface signals that contradict their self-presentation. In the grant application context: prior rejections from similar programs based on substantive grounds, contradictory technical assessments, and negative due diligence results from other funders, where those signals are material to the current application's claims.

### What counts as an adverse signal

A prior rejection from a program with similar eligibility criteria, where the rejection was based on substantive grounds. If a project was declined because reviewers assessed the FROM state as undiagnosed, and the same application is now being submitted to a different funder, that rejection is an adverse signal that must be disclosed.

A contradictory technical assessment: an independent audit, technical review, or peer assessment that found the project's core claims unsupported, the technology insufficiently mature, or the proposed approach unlikely to achieve the stated outcome.

Negative due diligence from other funders: a documented finding by another funder's evaluation process that surfaced a concern material to the current application.

### What adverse signal disclosure does not require

Adverse signals not material to the current application's claims. A rejection from a program with different eligibility criteria that the project did not qualify for geographically is not material to a substantive evaluation of outcomes. Informal negative opinions from ecosystem participants who have not conducted a formal evaluation are not adverse signals in the Adverse-Signal Engagement Principle Core Standard sense.

### Reviewer obligations

Reviewers who find adverse signals during evaluation must not suppress them. If a reviewer discovers that an applicant was declined by another funder on substantive grounds, that finding must enter the review record. The reverse obligation applies: reviewers must not fabricate or amplify adverse signals beyond what the evidence supports.

---

## Part 7: The Conflict of Interest Reasonable Third Party Standard in Practice

### How to apply the standard to novel relationship types

The conflict of interest framework's checklist covers common relationship types, but the governing standard is the reasonable third party test, not the checklist. Novel relationship types not on the checklist that meet the standard require the same treatment.

The test: would an informed observer with knowledge of the relevant facts conclude that this person cannot maintain independence and is therefore not capable of exercising objective and impartial judgment on this application?

Two questions apply to novel relationships. First: does this relationship create a financial interest, a loyalty interest, or a reputational interest in the outcome of the evaluation? Second: would a member of the public who understood both the relationship and the evaluation role conclude that the evaluation would be influenced by it?

A relationship that meets the standard even though it is not on the checklist: a reviewer who co-authored a position paper with the applicant's lead researcher six months ago, where that position paper directly supports the theoretical framework the application is built on. The co-authorship is recent, the intellectual alignment is direct, and an informed observer would reasonably conclude the reviewer cannot evaluate the application's theory of change impartially. Tier 2 treatment applies.

A relationship that does not meet the standard: a reviewer who attended the same conference as an applicant principal and exchanged messages in a shared community space. This is Tier 3 (disclosure encouraged) but does not meet the reasonable third party standard for a waiver or recusal requirement absent other factors.

### Tier 1 and Tier 2: the key distinction

Tier 1 relationships are categorical bars. No judgment is required and no waiver is available. If a reviewer holds equity in the applicant organization, that reviewer is out. These categories are defined to eliminate the need for judgment precisely because the relationships they describe are ones where judgment cannot be trusted.

Tier 2 relationships require judgment. Whether a relationship rises to the level of a disqualifying one depends on the nature and recency of the relationship, the degree of financial interest, and whether a reasonable third party would conclude independence is compromised. Tier 2 waivers require written justification submitted before participation, approval from a named authority other than the conflicted party, and documentation in the review record. Disclosure must come before participation, not after.

### Who is the named receiving function in a small grants program

Small grants programs often do not have dedicated conformance staff. The receiving function is whoever receives conflict of interest declarations and processes waiver requests. In a small program, this may be a program lead or a board member who does not participate in application review. The function must be a person, not a process. "Submit to the committee" is not a named receiving function.

If the program is small enough that all available staff have potential conflicts with at least some applications, an external trusted person should serve this function. It is operationally untenable for the person reviewing a conflict of interest declaration to be the same person whose independence is in question.

---

## Part 8: Privacy-Sensitive Context Accommodation

### When the accommodation applies

The privacy-sensitive accommodation applies when standard outcome measurement would compromise the safety of the beneficiary population. The harm must be specific and credible, not hypothetical. The population must face elevated risk from the act of measurement itself, not merely from the subject matter of the intervention.

The paradigm case: an application for a censorship-circumvention tool serving users in jurisdictions where use of such tools is criminalized. Standard outcome measurement (device identifiers, IP addresses, user accounts) would create a data trail that could be used to identify and prosecute users. The harm from measurement is specific: identification by state actors. The harm is credible: documented cases of user identification leading to prosecution exist in the relevant jurisdiction.

### What the accommodation requires

First, the applicant must name the specific harm that standard measurement would create. Not a general preference for privacy; a specific, named harm to a specific, named population. "Standard analytics would create identifiable records of users in Iran accessing censorship-circumvention tools, which could be used by Iranian state authorities to prosecute those users under [named legal provision]" is a specific harm statement.

Second, the applicant must name the specific alternative methodology they will use. Acceptable alternatives include Open Observatory of Network Interference-style network measurement (which assesses network conditions without identifying individual users), ethics-reviewed studies conducted by institutional partners under institutional review board protocols, differential privacy techniques applied to aggregate reporting, or other named methodologies with documented privacy properties.

The alternative methodology must be specific enough that a reviewer can evaluate whether it actually addresses the harm named. "We will use privacy-preserving methods" is not an alternative methodology.

### What does not qualify as an accommodation invocation

A general preference for privacy is not a harm statement. Absence of analytics infrastructure is not a harm statement. Discomfort with data collection is not a harm statement. The accommodation exists to protect beneficiaries, not to relieve applicants of measurement obligations they find burdensome.

---

## Part 9: Beneficiary Validation

### What "validated by parties outside the applicant's control" means

For change-obligation rounds: the FROM state must be confirmed as real by sources the applicant did not produce and does not control. This has two components. The baseline measurement must come from a named independent source. The existence of the problem must be corroborated by evidence the applicant did not generate.

"Validated by parties outside the applicant's control" means that at least one of the following is true: the baseline data comes from a named independent data source (Open Observatory of Network Interference, a government statistical agency, a peer-reviewed study, a third-party audit), or the problem is documented in a named source (journalism, non-governmental organization reports, independent technical analyses) that the applicant did not produce and does not control.

An applicant who cites only their own assessments, their own user feedback, and their own network as evidence that the problem exists has not demonstrated beneficiary validation. They have demonstrated that they believe the problem exists.

For build-obligation rounds where the coordinating party engagement dimension is activated: the claimed need for the deliverable must be validated by at least one party outside the applicant's organization who would use or benefit from it. A named person or organization who has expressed a specific need for this deliverable satisfies the requirement. A general claim that the ecosystem needs better tooling does not.

### The alternative-tool check

For change-obligation rounds: applicants who cannot name existing alternatives to their proposed solution for the stated beneficiary population have not diagnosed a problem; they have proposed a solution in search of one. The check does not ask applicants to demonstrate that no competition exists; it asks them to demonstrate awareness of the landscape and to explain why existing approaches are insufficient for the stated population.

An applicant who names existing alternatives and explains specifically why those alternatives do not serve the stated population under the stated conditions has completed the beneficiary validation exercise. An applicant who asserts that nothing comparable exists without evidence of having looked has not. When existing tools address the stated FROM state for the stated population, the applicant must explain what additional value their intervention provides.
