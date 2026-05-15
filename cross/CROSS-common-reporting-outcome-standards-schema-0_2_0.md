---
title: CROSS - Common Reporting Outcome Standards Schema
version: 0.2.0
date: 2026-05-14
license: CC0
status: Working draft. Supersedes version 0.1.0. Incorporates comparative research across thirteen grant programs spanning web3, open source, and institutional funding contexts.
related_documents:
  - standards/standards-3_0-adverse-signal-engagement-0_7_11.md
  - standards/standards-3_0-information-asymmetry-0_1_25.md
  - standards/standards-3_0-precision-first-2_1_7.md
  - standards/standards-3_0-regenerative-obligation-0_1_7.md
  - standards/standards-3_0-coordination-scaling-0_1_0.md
companion_documents:
  - standards/CROSS-runbooks-0_1_0.md
  - standards/CROSS-common-reporting-outcome-standards-schema-guidance-0_2_0.md
  - standards/CROSS-common-reporting-outcome-standards-schema-templates-0_2_0.md
  - standards/CROSS-common-reporting-outcome-standards-schema-rubric-0_2_0.md
  - standards/CROSS-common-reporting-outcome-standards-schema-worked-examples-0_2_0.md
implementation_documents:
  - standards/CROSS-grant-configurator-0_2_0.md
  - standards/CROSS-grantee-dashboard-0_2_0.md
  - standards/CROSS-reviewers-dashboard-0_1_0.md
  - standards/claude-skills/claude-skill-CROSS-0_2_0.md
---

# CROSS: Common Reporting Outcome Standards Schema

Version 0.2.0 | 2026-05-14 | CC0

---

## Purpose

CROSS specifies what funded interventions are obligated to demonstrate. It provides grants ecosystems with a portable obligation schema that accommodates multiple obligation modes, calibrates evidentiary pressure to program context, and generates structured reporting data that is comparable across funders, rounds, and grantees.

Version 0.2.0 extends version 0.1.0 in three structural ways. First, CROSS now recognizes three distinct obligation modes: build obligation, change obligation, and retroactive obligation. The Theory of Build is a failure mode only within a change-obligation round; it is a correct and complete specification within a build-obligation round. Second, CROSS introduces a gate architecture with four named gate types whose evidence requirements are configured by the funder and published before any round opens. Third, CROSS introduces a program-level continuation gate that governs progression across rounds and stages, enabling staged program designs of the kind used by major public goods funders.

CROSS is not a process standard. It does not specify how rounds are structured, how funds are distributed, or how funding decisions are made. CROSS specifies the content of obligation: what applicants must demonstrate, what funders must evaluate, what grantees must report, and how evidentiary pressure is structured across the funding lifecycle.

Funder obligation maturation is trackable through CROSS. A funder operating within a conformant program records their gate configuration for each round. Funders who maintain a versioned round record can track gate configurations across rounds, making funder maturation visible to the field over time.

---

## Scope

CROSS applies to any grants program that makes funding decisions based on expected or demonstrated contribution. It is designed for adoption by public goods funders in the web3 ecosystem (Octant, Gitcoin, Stellar Development Foundation, and similar programs) and is portable to grant-making contexts outside web3. Any organization that funds interventions and expects grantees to be obligated to demonstrate results can adopt CROSS independently of any other standard or protocol.

Runbooks providing pre-built configurations for common program types are companion documents to this standard. A funder adopting CROSS may select a runbook as a starting configuration or build a custom configuration from the gate architecture specification in Part IV.

---

## Part I: Independence and Suite References

CROSS is an independent standard. It is not a document of any specific grants program or protocol. Any grants ecosystem may adopt CROSS in whole or in part without adopting any other standard it references.

CROSS incorporates requirements from the following Coordination Structural Integrity Suite standards by reference. Adopters of CROSS inherit the requirements of these standards in the contexts specified below. They do not need to implement the full Suite to use CROSS.

The Adverse-Signal Engagement Principle Core Standard applies to adverse signal disclosure. Applicants must surface signals that contradict their self-presentation: prior grant rejections from similar programs, contradictory technical findings, negative due diligence results from other funders. Reviewers must not suppress adverse signals surfaced during evaluation.

The Information Asymmetry Classification Standard applies to concurrent funding disclosure. Undisclosed concurrent funding is an omission asymmetry under the Information Asymmetry Classification Standard. The disclosure requirement in Part VI of this standard instantiates the omission class in the grant application context.

The Precision-First Design Standard applies to indicator sourcing and the double-negation invariant. Documentation requirements must not be so light that obligation is absent, and must not be so heavy that legitimate small-team applicants are excluded. The proportionality requirements in Part IV are a Precision-First Design Standard corollary.

The Coordination Scaling Standard governs which evidence tier applies based on the scale and public impact claims of the application. Small technical teams with clear diagnoses do not require the same obligation machinery as large institutional applications. The Coordination Scaling Standard provides the calibration.

The Regenerative Obligation Standard and CROSS are structurally paired. The Regenerative Obligation Standard handles direction: how internal extraction and return mechanics operate within a funding mechanism. CROSS handles destination: what funded interventions must produce. A funding mechanism can satisfy the Regenerative Obligation Standard and fail CROSS, or satisfy CROSS and fail the Regenerative Obligation Standard. These are independent evaluations.

CROSS was developed using Frame Language as a conceptual tool. Frame Language is not a formal dependency of this standard. Adopters of CROSS are not required to use, cite, or license Frame Language.

---

## Part II: Independent Obligation Dimensions

CROSS specifies multiple obligation dimensions. Each dimension has its own triggering logic and its own tier structure. Dimensions do not scale together. A small grant does not automatically receive relaxed standards on all dimensions. A large grant does not automatically receive heavier requirements on all dimensions. Each dimension is assessed independently based on its own trigger.

The following dimensions are specified in this standard. Additional dimensions may be activated by funder configuration through the Grant Configurator.

**Outcome documentation rigor.** Triggered by: funding amount and the scale of the public impact claim. The Coordination Scaling Standard provides the calibration. Small-team applications with specific diagnoses and modest claims require less formal documentation than large institutional applications with broad population impact claims.

**Institutional capacity.** Triggered by: the scope of the proposed work relative to the applying organization's demonstrated track record. A team proposing a \$150,000 multi-year infrastructure project with no prior grant history faces a higher institutional capacity bar than a team with ten years of verified outputs proposing a \$20,000 continuation. Capacity assessment is not a disqualifier; it calibrates the disbursement conditions tier.

**Conflict of interest.** Triggered by: the nature of relationships between decision-makers and applicants, and between applicants and committee members. Three tiers apply: categorical bar (no waiver), qualified waiver, and disclosure-encouraged. Specified in full in Part VII.

**Concurrent funding disclosure.** Triggered by: whether the applicant has active grants, investments, or revenue sources related to the scope of the application in the prior 24 months. Required field for all applications, across all obligation modes. Non-disclosure is a disqualifier; disclosed concurrent funding is not.

**Adverse signal disclosure.** Triggered by: whether any adverse signals exist relating to the application. Applicants must disclose prior rejections from similar programs, contradictory technical findings, and negative due diligence results from other funders. Reviewers must not suppress adverse signals found during evaluation.

**Open source and intellectual property.** Triggered by: whether the funded work produces code, data, research, or other artifacts, and what the public goods claim rests on. For work claiming a public goods benefit through open access to its outputs, those outputs must be demonstrably open at the time of reporting, not only at the time of application.

**Beneficiary engagement and beneficiary validation.** Triggered by: whether the application claims to address a problem experienced by a defined population. In change-obligation rounds, the claimed FROM state must be validated by parties outside the applicant's control. In build-obligation rounds, the claimed need for the deliverable must be validated by at least one party outside the applicant's organization who would use or benefit from it.

**Privacy and data sensitivity.** Triggered by: whether the beneficiary population faces elevated risk from standard outcome measurement. For interventions where standard measurement would compromise the safety of the beneficiary population, privacy-preserving measurement methodologies are required in lieu of standard analytics. The accommodation is not an exemption from obligation; it specifies which obligation mechanisms are appropriate to the context.

**Environmental and social impact.** Optional dimension. Activated by funder configuration when the funded work may produce significant, diverse, potentially irreversible, or unprecedented impacts on communities, ecosystems, or cultural heritage. If activated, follows the A/B/C classification structure derived from International Finance Corporation Performance Standards and Green Climate Fund Environmental and Social Policy.

**Gender equity.** Optional dimension. Activated by funder configuration when the funded work affects populations where gender-disaggregated outcomes are material to the public goods claim.

**Procurement integrity.** Optional dimension. Activated by funder configuration when the funded work involves sub-contracting, sub-granting, or re-granting to third parties exceeding 20% of the total award.

---

## Part III: Obligation Modes

Every CROSS-conformant round operates in one of three obligation modes. The mode is declared by the funder in the Grant Configurator before the round opens and published as part of the round specification. Applicants are entitled to know which mode applies before they submit.

The mode determines what the entry specification gate asks, what the completion verification gate requires, and what failure modes are relevant at each gate. A finding that would disqualify an application in one mode may be correct and complete in another.

**Build obligation.** The funded work must produce a specified deliverable. The obligation object is the deliverable itself: does it exist, does it meet the stated completion criteria, and is it publicly accessible? The entry specification asks whether the applicant can name a falsifiable deliverable with independently verifiable completion criteria. The Theory of Build is not a failure mode in a build-obligation round; it is the correct and complete form of specification. An application that describes what it will build, with enough specificity that a reviewer who did not commission the work could verify whether it was completed, passes the entry specification.

Appropriate for: early-stage innovation grants, infrastructure development, tooling and library development, any program where the funder's primary goal is the existence of a public good artifact rather than a measured change in a population's condition.

**Change obligation.** The funded work must produce a measurable change in a defined population. The obligation object is the change itself: did the condition named in the FROM state improve toward the target named in the TO state, as measured by the specified indicator? The entry specification asks whether the applicant can name the FROM state as a specific measurable condition in a defined population. This was the sole gate in version 0.1.0 of this standard; in version 0.2.0 it is correctly scoped to change-obligation rounds.

The Theory of Build is a failure mode specifically in change-obligation rounds. An application that describes what it will build but cannot name the FROM state it addresses has not performed a problem diagnosis. It is not disqualified because it describes building; it is disqualified because it cannot answer the entry specification question for change-obligation: what specific measurable condition, in what defined population, does this intervention address?

Appropriate for: programs seeking measured population-level outcomes, continuation grants where prior epochs established a measurable baseline, programs aligned with institutional impact standards such as development agencies or foundations.

**Retroactive obligation.** The funded work has already produced value, and the funding rewards demonstrated past contribution. The obligation object is the prior contribution itself, assessed against the program's published criteria. The entry specification asks what evidence of prior contribution the applicant presents. No prospective commitment to future deliverables or outcomes is required, though the program may configure a forward commitment as a condition of the award.

Appropriate for: retroactive public goods funding programs, recognition grants for sustained infrastructure maintenance, programs where measuring prospective impact is less reliable than rewarding demonstrated past contribution.

**Application timing is not the diagnostic.** Across all three modes, when a team began their work is not a gate criterion. A team that built something before a grant opportunity appeared and presents it during an application window may be applying for build-obligation recognition of completed work, or may be presenting a baseline for a change-obligation continuation. The diagnostic is whether the entry specification question for the declared mode can be answered, not when the work began.

**Mixed and staged modes.** A multi-stage program may configure different obligation modes at different stages. An early stage may use build obligation; a later stage, after the deliverable exists and is in use, may require change obligation. The continuation gate between stages is the instrument that enforces the transition. The Grant Configurator supports mode assignment per stage.

---

## Part IV: Gate Architecture

Every CROSS-conformant round publishes a gate configuration before the round opens. The gate configuration specifies, for each active gate: the evidence scope requirement, the evidence strength requirement, and the infrastructure declaration confirming how the funder will operate the gate.

Gate configurations are not retrospective. A funder may not apply a higher evidence requirement than was published at round opening. A funder may not waive a published requirement without a documented rationale submitted to a named authority before the gate is reached.

**The four gate types.**

*Entry specification gate.* What an applicant must demonstrate to enter the round. Content depends on the declared obligation mode. In build-obligation rounds: a falsifiable deliverable specification, meaning a description of the artifact to be produced that includes completion criteria specific enough that an independent reviewer could verify whether they were met. In change-obligation rounds: a FROM state specification, meaning a specific measurable condition in a defined population with a named data source. In retroactive rounds: evidence of prior contribution meeting the program's published criteria. The entry specification gate is always present; what it asks depends on the mode.

*Progress verification gates.* What a grantee must demonstrate to trigger mid-funding disbursement tranches. Each tranche disbursement is contingent on verification of progress against the milestone committed at the prior stage. The minimum acceptable evidence at a progress verification gate is a publicly linkable artifact demonstrating work toward the specified deliverable or indicator. Funders may configure higher evidence requirements; they may not configure lower ones. Where no mid-funding disbursement is planned, progress verification gates are not required, and the full obligation weight rests on the completion verification gate.

*Completion verification gate.* What a grantee must demonstrate to receive final payment. This gate cannot be informal. The funder must have a named, published mechanism for determining whether completion criteria have been met. Grantee self-report alone does not satisfy the completion verification gate at any evidence strength level. The funder must review the grantee's submission against the published completion criteria and make a documented determination. For build-obligation rounds, the completion gate must additionally confirm that the specified deliverable is publicly accessible before final payment is released. Final payment may not be released without this confirmation.

*Continuation specification gate.* What a project must demonstrate to advance from one stage to the next in a multi-stage program, or to receive funding from the same funder in a subsequent round. This gate sits above the individual round and is configured at the program level, not the round level. It is the primary mechanism for escalating evidentiary pressure as a project matures. Not all programs require a continuation gate; it is activated by funder configuration. Where configured, the continuation gate must be published before any round in the program opens, so applicants understand the progression requirements before committing to the program.

**Evidence scope.** The scope of evidence accepted at any gate falls into one of four levels, in ascending order of rigor.

Output evidence: the specified deliverable exists, or a measurable artifact demonstrates progress toward it. Applicable to build-obligation gates. A shipped feature, a deployed contract, a published dataset, a recorded demonstration meeting the specified completion criteria are all output evidence.

Usage evidence: the deliverable is being used by parties outside the applicant's control, at a scale and in a manner that an independent reviewer can verify from public sources. Not all build-obligation programs require usage evidence, but continuation gates in build-obligation programs should require it to confirm that the deliverable has public uptake.

Outcome evidence: a measurable change has occurred in the specified population, documented against the baseline established at entry. Required for completion and continuation gates in change-obligation rounds.

Impact evidence: a credible causal link is established between the funded work and the measured change, through methodology sufficient to support causal inference. Not required in most public goods grant contexts, but may be configured as a continuation gate requirement for large-scale programs with institutional funders.

**Evidence strength.** The verification mechanism at any gate falls into one of four levels, in ascending order of rigor.

Self-report with documentation: the grantee provides a narrative account with supporting links, files, or on-chain data references, reviewed by funder staff against the published criteria. Appropriate for small grants and early-stage progress verification gates.

Third-party verifiable: the evidence is independently accessible to any reviewer with internet access, from sources outside the applicant's control. On-chain data from named public contracts, public repository activity, published results with open data. Appropriate as the minimum for completion verification gates above small grant thresholds.

Independent review: a named party outside the funder-grantee relationship confirms that the submitted evidence meets the completion criteria. The reviewer may be a domain expert, a named committee member not involved in the original award decision, or another funder who has reviewed the same work. Appropriate for continuation gates and for grants above a funder-defined size threshold.

Independent evaluation: a qualified evaluator with relevant domain expertise conducts a structured assessment of whether the funded work produced the claimed output, usage, or outcome, using methods proportional to the evidence scope required. Appropriate for Stage 2 and Stage 3 grants in graduated programs, and for programs where causal attribution is material to the funding decision.

**Infrastructure declaration.** Funders configuring any gate at independent review level or above must declare, before the round opens, the specific mechanism by which that verification will be conducted: who will conduct it, what their qualification is, what process they will follow, and what the timeline for completion is. Declaring a gate at a verification level the funder cannot actually operate is a conformance violation. The infrastructure declaration is part of the published round specification and may not be changed after the round opens without documented justification and notification to applicants.

**Proportionality.** Minimum gate requirements scale with funding amount and program stage. The Coordination Scaling Standard provides the calibration logic. As a baseline: grants below a funder-defined small grant threshold may configure all gates at self-report with documentation level. Grants above the threshold must configure the completion verification gate at no lower than third-party verifiable level. Continuation gates for programs at their second stage or beyond must configure the evidence scope at usage level or higher.

**Cost-effectiveness for continuation.** Where a continuation gate is configured for a change-obligation program, the entry specification for the next stage includes a cost-effectiveness consideration: does the evidence from the prior stage indicate that further investment in this intervention produces meaningful change relative to available alternatives? This is not a disqualifying criterion at first-stage entry; it is a continuation criterion. The Grant Configurator may configure cost-effectiveness as a required or advisory element of the continuation gate.

---

## Part V: Indicator Specification

Applicants self-specify their outcome indicators across all obligation modes. CROSS does not pre-specify what outcomes or deliverables are valid for a given funding domain. The funder specifies eligibility criteria. The applicant specifies what their intervention produces within that domain. CROSS specifies the fields that self-specified indicators must contain and the quality standards those fields must satisfy.

Each claimed indicator requires the following fields.

**Indicator name.** A short descriptive label. The name is not the operational definition; two funders may use the same indicator name with different operational definitions.

**Rationale for indicator.** Why this indicator was selected over available alternatives. Documents the diagnostic thinking that preceded tool selection. Mandatory across all obligation modes. An applicant who cannot articulate why they chose this particular indicator, deliverable definition, or evidence form over obvious alternatives has not engaged seriously with whether their obligation instrument is valid.

**Measurement form and evidence classification.** A plain-language description of what a result looks like and in what form it will be reported. This field replaces the prior constrained list of four data types, which was calibrated only for quantitative change-obligation indicators.

The applicant names the measurement form in plain language: a count of unique addresses, a shipped library version, a published dataset with a named license, a binary yes/no against defined completion criteria, a scored assessment on a defined scale. Reviewers classify the stated form against three axes for data quality assessment purposes.

Source type: on-chain verifiable (accessible from public blockchain data with a named contract or address), off-chain verifiable (accessible from public sources outside the blockchain, such as a public code repository, a published report, or a named application programming interface), or qualitative/narrative (documented through structured narrative, interview data, or artifact review requiring a human evaluator). Each source type carries different minimum verification requirements at the data quality assessment stage.

Measurement form: quantitative (expressed as a number, proportion, rate, currency amount, or duration), ordinal (expressed as a position on a defined ordered scale), binary (expressed as met or not met against named completion criteria), or qualitative (expressed as a documented condition, verified artifact, or narrative record assessed against named criteria).

Aggregation type: cumulative (values sum correctly across reporting periods) or non-cumulative (values describe a state at a point in time; summing across periods is a construction error). Reviewers must flag a non-cumulative indicator presented with a cumulative target at the application stage, not the reporting stage.

For build-obligation indicators: the measurement form is typically binary (the deliverable either meets the completion criteria or does not) or qualitative (the deliverable is a documented artifact assessed against named criteria). The measurement form declaration specifies what done looks like with enough precision that a reviewer who did not commission the work could verify it independently.

For change-obligation indicators: the measurement form is typically quantitative or ordinal. The declaration must include the unit of measurement and the direction of desirable change.

**Operational definition.** A narrative specification of what counts and what does not count as one unit of the claimed result. Must include: inclusion criteria (what qualifies as one instance), exclusion criteria (what the indicator explicitly does not count), unit of analysis (person, wallet address, transaction, repository, site, or other named unit), and edge case determination (at least one example of how an ambiguous instance is handled). Without an operational definition, the claimed indicator is a name, not a measurement instrument.

**Construction and aggregation methodology.** The calculation rule in sufficient detail that an independent reviewer with access to the stated data source could replicate the result. Must include the formula or counting rule, how partial data is handled, and how values from sub-units are aggregated. For build-obligation indicators, the construction methodology specifies how completion is determined: what constitutes a passing demonstration, who performs the verification, and by what process. For change-obligation indicators, this is the standard data construction methodology. Self-report of a result without a stated construction methodology does not satisfy this field.

**Cumulative or non-cumulative.** Whether the indicator is cumulative (can be summed across reporting periods; life-of-grant target is achieved by addition) or non-cumulative (measures a status at a point in time; life-of-grant target is the target status at grant end, not a sum of period targets).

**Disaggregation.** The categories by which indicator values will be reported. Disaggregation categories committed to in the application may be supplemented in subsequent reporting periods but may not be removed without committee approval and documented rationale. This constraint protects longitudinal comparability.

**Data source and collection method.** The named source and the collection method. The source must be accessible to an independent reviewer. Applicant-controlled sources without named independent corroboration do not satisfy the integrity standard. For build-obligation indicators, the data source for completion verification is the named artifact itself plus the named party who will confirm it meets the completion criteria.

**Data cost estimation.** Attestation that data collection is operationally feasible within the project budget, with the approximate cost and source of funding for collection. An indicator that cannot be collected within the project budget has not been operationalized.

**Baseline (FROM state).** For change-obligation indicators: the documented state of the condition before the intervention begins, with a named data source. Required. For build-obligation indicators: the documented current absence or inadequacy of the deliverable, with named evidence of the gap it addresses. Required where the funder has activated the beneficiary engagement dimension. For retroactive indicators: the documented state of the contribution at the time the award period begins.

**Target (TO state).** The expected state of the indicator at the end of the grant period or stage. For change-obligation indicators: expressed in the same units as the baseline. For build-obligation indicators: expressed as the completion criteria the deliverable must meet. For retroactive indicators: may describe a forward commitment the awardee makes as a condition of the award, if configured by the funder.

---

## Part VI: Concurrent Funding Disclosure

All active grants, investments, or revenue sources from the prior 24 months that are related to the scope of this application must be disclosed. Required across all obligation modes. Required fields:

- Source name (investor, foundation, decentralized autonomous organization, protocol, or other)
- Approximate amount
- Relationship to this application's scope
- Whether ongoing reporting or milestone obligations to the source exist
- Whether any investor or funder has board, coordinating, or decision-making rights over the funded work

Non-disclosure of concurrent funding is a disqualifier. Disclosure is not. An applicant with venture capital backing can receive public goods grant funding if the relationship between commercial financing and the public goods ask is clear and the public goods ask is specifically scoped to work the commercial funding does not cover.

---

## Part VII: Conflict of Interest Framework

The conflict of interest framework applies independently from the outcome documentation rigor tier and independently from the obligation mode. A small-grant build-obligation round does not receive relaxed conflict of interest requirements. Relationship type, not funding amount or mode, determines conflict of interest tier assignment.

**Coverage.** Conflict of interest obligations run in both directions. Reviewers must disclose relationships to applicants. Applicants must disclose relationships to committee members and reviewers.

**Governing standard.** The reasonable third party standard applies: would an informed observer with knowledge of the relevant facts conclude that the person cannot maintain independence and is therefore not capable of exercising objective and impartial judgment? The checklist below illustrates the standard; it does not exhaust it. Novel relationship types not on the checklist that meet the reasonable third party standard require disclosure.

**Tier 1: Categorical bar. No waiver.**

- Direct financial interest in the applicant entity, including equity, revenue share, or token holdings above the materiality threshold (default: greater than 1% of circulating supply or greater than \$5,000 in value at time of review)
- Family relationship with any principal, director, officer, or owner of the applicant project
- Prior receipt of funding from this funder in the same program area where the reviewer's funded work is directly related to the applicant's scope
- Being named as a team member, advisor, or contributor on the applicant project's public materials, whether compensated or not

**Tier 2: Disclosure required. Qualified waiver possible.**

A qualified waiver requires: (a) a written justification submitted to a named authority other than the conflicted party, (b) approval granted before participation, not after, and (c) documentation in the review record. Waiver is not available where the relationship creates a financial interest.

- Employment with the applicant organization in the past 36 months
- Co-authorship or active project collaboration with applicant principals in the past 48 months
- Mentor or student relationship with applicant principals (no expiration)
- Governance token voting power exercised on proposals affecting the applicant project
- Decentralized autonomous organization co-membership in coordinating or committee roles within the same decentralized autonomous organization as the applicant
- Having received an honorarium, award, or gift from the applicant entity in the past 12 months
- Active job negotiations or arrangements for future employment with the applicant organization
- Organizational conflict: the reviewer's employer has a material financial relationship with the applicant

**Tier 3: Disclosure encouraged. Reasonable third party standard applies.**

- Social and community relationships (conference co-speakers, forum co-membership, shared group chats)
- Prior interactions across grant rounds in different program areas
- Informal mentorship or advisory conversations without ongoing engagement

**Web3-specific categories.**

The following relationship types require the same three-tier assessment but are not present in standard conflict of interest frameworks developed outside web3: token holdings (see Tier 1 materiality threshold), governance token voting on applicant proposals, core contributor or unpaid advisory status on applicant projects, having received investment from the same named investor backing the applicant, and decentralized autonomous organization co-governance roles.

**Process.**

Before review: each reviewer and each applicant completes a conflict of interest declaration covering all three tiers. The declaration is submitted to a named receiving function that is separate from the person making the funding decision. In programs using the CROSS Reviewers Dashboard, the conflict of interest declaration is enforced as a gate: a reviewer who has not completed their declaration for a specific application cannot open that application.

After review: each reviewer completes a post-participation certification confirming that no new conflicts arose during the review process and that the declaration remained accurate.

Non-disclosure of a Tier 1 conflict is a disqualifying violation. Non-disclosure of a Tier 2 conflict is a process violation requiring remediation. Remediation options are: retroactive recusal, review restart with a non-conflicted panel, or award cancellation, depending on the degree of influence the conflicted party had.

---

## Part VIII: Data Quality Standards

The following five standards apply to the indicator specification across all obligation modes. Reviewers apply them during gate assessment. Each standard has its own assessment question and failure mode.

**Validity.** The measurement instrument must have a documented logical chain from the evidence collected to the result level claimed. Assessment question: could an independent reviewer, given the stated source and construction methodology, confirm that the indicator measures what it claims to measure? Validity failure: the reported metric is downstream of unmeasured confounders, or the completion criteria named for a deliverable are insufficient to determine whether the work was done.

**Integrity.** Evidence collection and reporting must be separated from the actor who benefits from the results. A named independent verification mechanism is required. Assessment question: does any evidence for this claim originate from a source independent of the applicant? Integrity failure: all evidence originates from applicant-controlled systems with no independent corroboration.

**Precision.** The measurement method must be capable of detecting changes at the magnitude the project claims to produce, or confirming completion at the specificity the criteria require. Assessment question: is the measurement or verification instrument precise enough to support the claimed result? Precision failure: completion criteria so vague that any output satisfies them; or a change claim smaller than the variance of the measurement instrument.

**Reliability.** The measurement instrument and collection methodology must be consistent across reporting periods. Assessment question: if this project submitted a prior report using a different metric, methodology, or completion criteria for the same indicator, is the change documented and the comparability of prior periods determined? Reliability failure: different criteria or metrics reported in different periods without explanation.

**Timeliness.** Evidence must be current to the reporting period. Assessment question: does the collection frequency match the funder's decision cycle? Timeliness failure: annual data collection where quarterly disbursement decisions depend on current data; or a completion claim based on work from a prior period not covered by the current gate.

---

## Part IX: Implementation Architecture

CROSS is implemented through four operational tools. The standard specifies what is required. The tools make the standard usable without requiring funders, grantees, or reviewers to interpret the full specification directly.

**CROSS Grant Configurator** (CROSS-grant-configurator-0_2_0.md): the funder onboarding instrument. Generates a round-specific obligation specification from the funder's declared obligation mode, gate configuration, evidence requirements, and infrastructure declarations. Inherits all field definitions, tier logic, and conflict of interest requirements from this standard. The configurator also supports program-level configuration: the continuation gate structure and stage progression requirements are specified here, separately from individual round configuration. Runbook configurations may be selected as a starting point and customized.

**CROSS Grantee Dashboard** (CROSS-grantee-dashboard-0_2_0.md): the post-award obligation interface. Converts the round specification produced by the Grant Configurator into a live record for each funded project. Inherits the indicator schema, evidence requirements, gate configuration, disaggregation ratchet, cumulative/non-cumulative designation, and disbursement condition structure from the configurator. Tracks gate evidence submissions and produces structured attestations suitable for on-chain publication.

**CROSS Reviewers Dashboard** (CROSS-reviewers-dashboard-0_1_0.md): the stage-gated review interface. Active only during the evaluation stage of a round, as configured in the Grant Configurator. Enforces conflict of interest declarations as access gates before any application is opened. Maintains assessment isolation between reviewers until submission. Provides role-differentiated access: guest reviewers see their assigned applications; lead reviewers see all applications and submitted assessments; funder administrators see the aggregate output. Loads the appropriate rubric based on the obligation mode configured for the round. Provides AI-assisted evaluation in three layers: submitted evidence verification against the applicant's claims, independent investigation of applicant claims against third-party sources, and a draft evaluation applying the rubric to the combined findings. Human reviewer assessment is the final artifact; the AI draft and investigation findings are stored alongside it in the review record.

**CROSS skill** (claude-skills/claude-skill-CROSS-0_2_0.md): machine-readable encoding of the standard for AI-assisted implementation across all three tools. Covers three obligation modes, the four-gate architecture, open measurement form with three-axis classification, and gate evidence assessment procedures.

**Runbooks.** Pre-built, documented configuration packages for common program types. Each runbook specifies a complete gate configuration, obligation mode assignment, evidence scope and strength at each gate, infrastructure declaration requirements, and a recommended evolution path to a more mature configuration. The initial runbook library covers: discovery sprint, staged development, community allocation with build obligation, retroactive impact, graduated evidence, and institutional conformance configurations. Runbooks are companion documents to this standard.

---

## Part X: Companion Documents

The standard states criteria tersely. The companion documents operationalize them for practitioners.

**Guidance** (CROSS-common-reporting-outcome-standards-schema-guidance-0_2_0.md): what qualifies and what does not at each decision point; how to answer the entry specification for each obligation mode; common failures at the gate and at the rigor tier; how to complete each indicator field; how to apply the conflict of interest standard to novel relationship types.

**Templates** (CROSS-common-reporting-outcome-standards-schema-templates-0_2_0.md): the entry specification forms (mode-specific variants for build, change, and retroactive obligation), the indicator registration form, the conflict of interest declaration forms, the gate evidence submission form, and the privacy-sensitive accommodation request. Template complexity is tiered to the scale of the application.

**Assessment Rubric** (CROSS-common-reporting-outcome-standards-schema-rubric-0_2_0.md): how reviewers assess against the gate criteria for each obligation mode. Includes the data quality standard assessment questions and failure mode descriptions from Part VIII. The rubric is mode-specific: build-obligation, change-obligation, and retroactive obligation gates produce different assessment questions.

**Worked Examples** (CROSS-common-reporting-outcome-standards-schema-worked-examples-0_2_0.md): existing evaluations illustrating gate passage and gate failure across all three obligation modes, from the Epoch 12 public goods evaluation cycle and comparable programs. Includes canonical cases demonstrating deliverable specification failures, FROM state failures, retroactive evidence failures, concurrent funding non-disclosure, conflict of interest remediation, and well-specified versus underspecified indicators.

---

## Appendix: Open Design Questions (v0.2.0)

**Single-outcome constraint.** Whether CROSS should require one primary indicator per application or permit multiple. Current position: permit multiple, require one designated primary indicator. The primary indicator is the one against which the entry specification, progress verification, and completion verification gates are primarily assessed.

**Reporting frequency.** Whether reporting frequency requirements belong in the standard or the guidance. Current position: guidance, calibrated by the Coordination Scaling Standard.

**Cost-effectiveness as a required field.** Whether cost-effectiveness assessment should be a required field at the continuation gate for all change-obligation programs or remain advisory. Current position: required for continuation in programs whose Grant Configurator specifies Stage 2 or above; advisory elsewhere.

**Round-level common indicators.** Whether funders may designate indicators common to all applications in a round, in addition to applicant-specified indicators. Current position: yes, a valid configurator option. Common indicators do not change the applicant-specification principle for all other indicators.

**Failure record obligation.** Whether CROSS-conformant funders are required to maintain a public record of terminated grants, missed milestones, and declined continuation applications. Current position: strongly indicated by the research but not yet specified as a conformance requirement. To be addressed in v0.3.0.

**Decentralized Autonomous Organization Improvement Proposal 5 relationship.** CROSS should reference Decentralized Autonomous Organization Improvement Proposal 5 as a companion coordinating instrument governing round process structure. Decentralized Autonomous Organization Improvement Proposal 5 handles how rounds are structured and funds distributed. CROSS handles what funded interventions must demonstrate. The formal relationship is to be specified in a subsequent draft.

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.2.0 | 2026-05-14 | Major structural revision. Introduced three accountability modes (build, change, retroactive). Theory of Build correctly scoped as a failure mode in change-accountability rounds only. Replaced Level 1 / Level 2 binary with four-gate architecture (entry specification, progress verification, completion verification, continuation specification). Added evidence scope and evidence strength taxonomies. Added program-level continuation gate. Replaced constrained data type list with open measurement form and evidence classification. Added Reviewers Dashboard to implementation architecture. Added runbook library concept. Added funder maturation tracking note. Resolved several v0.1.0 open questions. |
| 0.1.0 | 2026-05-14 | Initial draft. Single accountability mode (change). Binary Theory of Build gate (Level 1) and scored rigor tier (Level 2). PIRS-derived indicator schema with four-option data type field. |
