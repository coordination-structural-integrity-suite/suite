---
title: CROSS Runbooks
version: 0.1.0
date: 2026-05-14
license: CC0
status: First edition. Companion document to CROSS Common Reporting Outcome Standards Schema version 0.2.0.
related_documents:
  - standards/CROSS-common-reporting-outcome-standards-schema-0_2_0.md
  - standards/CROSS-grant-configurator-0_1_0.md
---

# CROSS Runbooks

Version 0.1.0 | 2026-05-14 | CC0

---

## About Runbooks

A runbook is a pre-built, documented configuration package for a common program type. Each runbook specifies a complete gate configuration: the obligation mode, which gates are active, the evidence scope and evidence strength at each gate, and the infrastructure declaration requirements for any gate that requires independent review or higher. Runbooks also specify a recommended evolution path describing the configuration changes that would constitute a maturation of the program's obligation posture if the program continues into subsequent stages or rounds.

A funder adopting a runbook takes it as a starting configuration. Fields that are labeled "configurable" in the runbook may be adjusted by the funder through the Grant Configurator. Fields that are labeled "minimum" may not be loosened; they may only be tightened. Fields that are labeled "fixed" may not be changed without departing from the runbook.

Selecting a runbook does not waive any requirement of the CROSS Common Reporting Outcome Standards Schema. Runbooks are configurations within the schema; they do not override it. If a requirement of the standard conflicts with a runbook field, the standard governs.

Conflict of interest requirements from Part VII of the standard apply to all runbooks. Runbooks do not reduce conflict of interest obligations. A runbook may specify how conflict of interest declarations are operationally implemented for the program type; it may not lower the standard.

Concurrent funding disclosure from Part VI applies to all runbooks without exception.

---

## Runbook 1: Discovery Sprint

**Program type this runbook serves.** Short-duration grants producing research, design artifacts, protocol specifications, or feasibility assessments. The funder's goal is an artifact that advances understanding of a problem or a design space, not a measurable change in a population's condition. Discovery sprint grants are typically small and run for four to sixteen weeks.

**Obligation mode: Build obligation.**

The deliverable is a document, specification, dataset, assessment, or design artifact. The entry specification asks what the artifact will be and how a reviewer could verify it is complete.

**Gate configuration.**

| Gate | Active | Evidence scope | Evidence strength | Infrastructure requirement |
|---|---|---|---|---|
| Entry specification | Yes | Output | Self-report with documentation | Staff review of deliverable specification against the published completion criteria format |
| Progress verification | No | -- | -- | -- |
| Completion verification | Yes | Output | Self-report with documentation for grants below the funder's small grant threshold; third-party verifiable for grants at or above threshold | Named staff member reviews the submitted artifact against published completion criteria before final payment |
| Continuation specification | No | -- | -- | -- |

**Entry specification requirements for this runbook.** The applicant must name: (1) the artifact to be produced, in plain language; (2) the format in which it will be delivered (document, data file, code repository, presentation, or named equivalent); (3) the completion criteria in enough specificity that a reviewer who did not commission the work could determine whether they are met; and (4) the audience who would use or benefit from the artifact, with at least one named party outside the applicant's organization who has expressed interest.

**Conflict of interest.** Standard three-tier declaration applies. Because discovery sprint grants are small and the time commitment for reviewers is brief, the conflict of interest declaration may be administered through a concise form covering all three tiers. No waiver process is available for Tier 1 conflicts regardless of grant size.

**Infrastructure declaration requirements.** No gate in this runbook requires independent review. The infrastructure declaration for the completion verification gate specifies the named staff member and the timeline for artifact review after submission. This must be published before the round opens.

**Optional dimension activation.** For discovery sprint grants, the environmental and social impact, gender equity, and procurement integrity dimensions are typically not activated. The funder may activate them if the program area warrants.

**Recommended rubric emphasis.** For discovery sprint rounds, the rubric should weight Field 11 (completion criteria specificity) and Field 5 (construction and aggregation methodology) most heavily. The central reviewer question is: can someone who did not commission this work confirm from publicly accessible evidence alone that the deliverable was completed and meets the stated criteria? The Integrity standard is the second priority: is the verifying party independent of the applicant? The causal chain validity assessment, cumulative/non-cumulative distinction, and disaggregation ratchet are less applicable at this program type and may be marked not applicable in the confirmed rubric. Funder guidance additions should focus on what constitutes a credible public delivery location for this round's expected artifact types.

**Recommended evolution path.** A team that completes a discovery sprint with a well-specified artifact is a natural candidate for Staged Development (Runbook 2) if the artifact points toward a buildable deliverable, or Retroactive Impact (Runbook 4) in a subsequent cycle if the discovery sprint output has since been adopted by others. Discovery sprint completion does not automatically qualify a team for a subsequent round; the continuation specification gate in the next program must be passed on its own terms.

**Example programs.** Gitcoin research and open data rounds, Ethereum Foundation ecosystem support program small grants for protocol design work, Octant exploratory rounds where the deliverable is a specification or design document rather than working software.

---

## Runbook 2: Staged Development

**Program type this runbook serves.** Multi-stage programs in which teams progress through defined development phases. Stage 1 produces an initial deliverable. Stage 2 requires evidence that the Stage 1 deliverable is in use and a specification for the next phase. Later stages may escalate to change obligation if a measurable population condition is the program's ultimate goal. This runbook covers a two-stage program; programs with three or more stages should use Runbook 5 (Graduated Evidence).

**Obligation mode: Build obligation at Stage 1. Build obligation or change obligation at Stage 2, configurable by the funder.**

**Stage 1 gate configuration.**

| Gate | Active | Evidence scope | Evidence strength | Infrastructure requirement |
|---|---|---|---|---|
| Entry specification | Yes | Output | Self-report with documentation | Staff review of deliverable specification |
| Progress verification | Configurable | Output | Self-report with documentation | Staff check-in at mid-point if activated |
| Completion verification | Yes | Output | Third-party verifiable | Named staff or named independent reviewer confirms the deliverable is publicly accessible and meets the published completion criteria |
| Continuation gate (Stage 1 to Stage 2) | Yes | Usage | Third-party verifiable | Named staff verifies publicly accessible evidence of use by parties outside the applicant's control before Stage 2 funding is released |

**Stage 2 gate configuration (build obligation variant).**

| Gate | Active | Evidence scope | Evidence strength | Infrastructure requirement |
|---|---|---|---|---|
| Entry specification | Yes | Output and Usage | Third-party verifiable | Review of Stage 1 completion verification record plus evidence of external use |
| Progress verification | Configurable | Output | Self-report with documentation | Staff check-in if activated |
| Completion verification | Yes | Output and Usage | Third-party verifiable | Named reviewer confirms the Stage 2 deliverable meets the published criteria and has demonstrable uptake |
| Continuation gate (Stage 2 onward) | Configurable | Usage | Independent review | If further stages are planned, a named independent reviewer verifies sustained usage before Stage 3 funding is committed |

**Stage 2 gate configuration (change obligation variant).** If the funder activates change obligation for Stage 2, the entry specification gate additionally requires: a FROM state specification with a named data source, a baseline documented against the Stage 1 period, and a target for the Stage 2 period. All change obligation requirements from Part III and the indicator specification requirements from Part V of the standard apply in full.

**Continuation gate requirements.** The continuation gate from Stage 1 to Stage 2 is the instrument that enforces the usage requirement. A team that delivered a Stage 1 artifact but cannot demonstrate that anyone outside the team is using it does not pass the continuation gate. Usage in this context means documented use by parties outside the applicant's control, at a scale and in a manner that an independent reviewer can verify from public sources. Applicant-asserted usage without accessible public evidence does not satisfy third-party verifiable evidence strength.

**Conflict of interest.** Standard three-tier declaration applies at each stage. Reviewers involved in Stage 1 evaluation who have since developed a new relationship with the applicant team must complete a fresh declaration before Stage 2 review begins.

**Infrastructure declaration requirements.** The continuation gate is configured at third-party verifiable level; no independent reviewer is required for the standard configuration. If Stage 2 uses independent review at the completion verification gate, the infrastructure declaration must name the reviewer and the timeline before the Stage 2 round opens. The funder must not specify independent review in the published round configuration and then retrospectively reduce it to self-report.

**Recommended rubric emphasis.** Stage 1 rubric emphasis mirrors the Discovery Sprint: Field 11 (completion criteria), Field 5 (methodology), Integrity standard. Stage 2 rubric emphasis shifts to the beneficiary engagement dimension (is the usage claim independently validated?), Field 10 (is the usage baseline credible and independently sourced?), and the Validity standard (does the usage evidence connect causally to the Stage 1 deliverable rather than to background adoption trends?). The continuation gate rubric should give the Integrity standard the highest weight: usage claimed without any independently accessible public source does not satisfy third-party verifiable evidence strength. Funder guidance additions should clarify what constitutes acceptable evidence of external adoption for this program's domain.

**Recommended evolution path.** A program operating this runbook for three or more cycles should consider whether the continuation gate should escalate to outcome evidence, and whether Stage 2 or Stage 3 should require change obligation. That escalation is the Graduated Evidence configuration (Runbook 5).

**Example programs.** Octant multi-epoch programs where teams must demonstrate use before receiving a second epoch, Stellar Development Foundation Community Fund projects with a first-round deliverable requirement and a second-round continuation requirement, staged development programs where continuation is conditioned on demonstrated uptake.

---

## Runbook 3: Community Allocation with Build Obligation

**Program type this runbook serves.** Community-allocated rounds in which funding amounts are determined by a community mechanism (quadratic funding, direct voting, token-weighted allocation, or similar) rather than a committee deliberation. The grant program's obligation structure is separate from the allocation mechanism; this runbook specifies the obligation structure. The allocation mechanism itself is not governed by CROSS.

This runbook assumes that many applicants will be small teams with limited reporting capacity. Evidence requirements are calibrated accordingly. The Precision-First Design Standard's double-negation invariant applies: requirements must not be so heavy that legitimate small-team applicants are excluded.

**Obligation mode: Build obligation.**

**Gate configuration.**

| Gate | Active | Evidence scope | Evidence strength | Infrastructure requirement |
|---|---|---|---|---|
| Entry specification | Yes | Output | Self-report with documentation | Automated check against published field requirements; staff spot-review of a sample of submissions |
| Progress verification | No (configurable for grants above threshold) | -- | -- | -- |
| Completion verification | Yes | Output | Self-report with documentation for grants below the small grant threshold; third-party verifiable for grants at or above threshold | Named staff confirms the publicly accessible deliverable meets the stated completion criteria |
| Continuation specification | Configurable | Usage | Third-party verifiable | Activated for teams applying for a second round from the same funder; staff verifies public evidence of use |

**Entry specification requirements for this runbook.** The applicant states: (1) what they are building; (2) what done looks like (completion criteria); and (3) who will use it. The beneficiary field does not require a named individual; a specific user type or developer profile is sufficient at this evidence strength level. The application does not require a FROM state, outcome indicator, or theory of change. Those apply in change-obligation rounds; this is a build-obligation round. Reviewers must not apply change-obligation gate criteria to build-obligation applications.

**Key configuration note: continuation gate for returning teams.** When a team applies for a second consecutive round from the same funder, the continuation specification gate activates. The team must present evidence that the prior round's deliverable is publicly accessible and in use. This gate distinguishes a team with a track record of delivery from a team proposing a perpetual first stage. It is not a requirement for first-round applicants; applying for the first time does not require a usage demonstration.

**Conflict of interest in community-allocated rounds.** Community-allocated rounds frequently involve governance token holders or community members as decision-makers. Governance token voting on proposals affecting an applicant project is a Tier 2 conflict of interest under Part VII of the standard. Allocation mechanisms that use token voting must maintain a conflict of interest disclosure process for this category. Anonymous allocation mechanisms where voters cannot be individually identified must document their approach to Tier 1 conflict of interest prevention in the infrastructure declaration.

**Concurrent funding disclosure.** Required for all applicants regardless of allocation size. Non-disclosure is a disqualifier. The field may be completed with "none" if no concurrent funding exists, but the field must be answered; it is not optional.

**Infrastructure declaration requirements.** No independent review is required at any gate in the standard configuration. The infrastructure declaration specifies who reviews submitted artifacts against completion criteria, what the review process is, and what the timeline is before final payment.

**Recommended rubric emphasis.** For community-allocated build-obligation rounds, Field 11 (completion criteria) and the beneficiary validation dimension are the most load-bearing rubric sections. The beneficiary validation question is: does a real external party need this, and has that need been confirmed by someone outside the applicant's organization? The concurrent funding disclosure conformance check should be weighted heavily given the community allocation context; governance token voting relationships are especially common and must be assessed under the conflict of interest framework. The Precision standard and formal causal chain validity assessment are less applicable and may be simplified or marked advisory. Funder guidance additions should clarify what counts as an adequate completion demonstration for the types of deliverables this round expects, so reviewers apply a consistent standard across many small applications.

**Recommended evolution path.** A funder running community allocation for multiple cycles should consider activating the continuation specification gate for returning teams after the second round, and requiring third-party verifiable evidence at completion regardless of grant size from the third cycle onward. This represents a natural maturation of obligation posture without changing the core build-obligation mode.

**Example programs.** Octant standard rounds, Gitcoin quadratic funding rounds, Arbitrum community allocation programs, any program where community signaling or voting determines allocation and the deliverable is a public good artifact.

---

## Runbook 4: Retroactive Impact

**Program type this runbook serves.** Programs that fund past contribution: work that has already been produced and is already in use. No prospective commitment to future deliverables or outcomes is required at entry. The obligation object is the demonstrated prior contribution, assessed against the program's published criteria.

Retroactive obligation is not the absence of obligation; it is obligation for what has already happened. The entry specification asks what the applicant has contributed, to whom, and with what evidence. The assessment rubric evaluates the quality, scale, and alignment of that contribution against the funder's published criteria.

**Obligation mode: Retroactive obligation.**

**Gate configuration.**

| Gate | Active | Evidence scope | Evidence strength | Infrastructure requirement |
|---|---|---|---|---|
| Entry specification | Yes | Output and/or Usage | Third-party verifiable | Named review panel with published rubric assesses submissions against defined contribution criteria before allocation |
| Progress verification | Not applicable | -- | -- | -- |
| Completion verification | Not applicable | -- | -- | -- |
| Continuation specification | Configurable | Usage or Outcome | Third-party verifiable or Independent review | Activated where the funder specifies that a subsequent round requires evidence of continued public uptake of prior-funded contributions |
| Forward commitment (optional) | Configurable | Output | Self-report with documentation | If activated, the awardee commits to a named forward action as a condition of receiving the award; completion is verified by named staff at the close of the commitment period |

**Entry specification requirements for this runbook.** The applicant presents: (1) what contribution has been produced; (2) the period during which it was produced; (3) evidence of who is using it or who has benefited, accessible from sources outside the applicant's control; (4) the relationship between the contribution and the funder's published eligibility criteria; and (5) any prior awards received for the same or substantially overlapping work from this or any other funder, which is the concurrent funding disclosure requirement applied to the retroactive context.

**Assessment rubric requirement.** The funder must publish an assessment rubric before the round opens. The rubric must specify: what kinds of contribution qualify, how contribution is weighted against scale of use, how the review panel resolves disagreements, and what the minimum threshold for an award is. A retroactive round without a published rubric does not satisfy the infrastructure declaration requirement. The rubric is not advisory; it is the instrument against which submissions are assessed.

**Prior award disclosure.** An applicant receiving a retroactive award for work that was prospectively funded by another source during the same period must disclose the prior funding in the concurrent funding disclosure field. An applicant who has already received a retroactive award from another program for the same contribution must also disclose. Receiving multiple retroactive awards for the same work is not automatically disqualifying, but it must be disclosed and may be considered in the rubric assessment.

**Conflict of interest.** Panel members for retroactive rounds must declare conflicts under the full three-tier framework. Because retroactive rounds assess contributors who are likely to be known within the community, Tier 2 disclosures covering co-authorship, project collaboration, and mentorship relationships are especially common. Panel composition must account for this, and the waiver process must be active before any panel review begins.

**Infrastructure declaration requirements.** Retroactive rounds require at minimum third-party verifiable evidence strength at the entry specification gate, and the review panel constitutes the independent review mechanism at that gate. The infrastructure declaration must name the panel members, state their qualifications relevant to the contribution area, and specify the process for handling panel conflicts of interest. This is a gate at independent review level; all infrastructure declaration requirements from Part IV of the standard apply.

**Recommended rubric emphasis.** The retroactive obligation rubric is entirely funder-authored (Q12.4 of the Configurator). The following structure is recommended as a starting template. Contribution scope and originality: what was produced and what makes it non-duplicative of existing work? Evidence of adoption: what independently accessible sources confirm the contribution is being used, by whom, and at what scale? Sustainability and trajectory: is the contribution maintained and growing, or was it a single output with declining use? Relevance to program criteria: how directly does the contribution address the program's published eligibility domain? The Integrity standard is the highest-priority data quality criterion for retroactive rounds: all contribution and adoption evidence must originate from sources outside the applicant's control. Applicant self-assertion of impact without any independent source fails the Integrity standard regardless of how detailed the self-report is.

**Recommended evolution path.** A funder running retroactive rounds who finds that the same contributors apply repeatedly with overlapping work should consider adding a continuation specification requiring evidence of new contribution since the prior award period. A funder who wants to move from pure retroactive assessment toward a combination of retroactive reward and prospective obligation should configure the forward commitment field and, in subsequent rounds, treat it as a progress verification gate.

**Example programs.** Optimism Retroactive Public Goods Funding, Protocol Guild distributions for Ethereum core protocol contributors, any program where funding is allocated based on demonstrated past public goods contribution rather than a prospective proposal.

---

## Runbook 5: Graduated Evidence

**Program type this runbook serves.** Multi-stage programs in which evidence requirements escalate at each continuation gate. The program is designed so that small, exploratory grants carry light obligation; medium, validated grants carry moderate obligation; and large, scaling grants carry rigorous obligation including independent evaluation. This structure is adapted from the staged-funding model used by the United States Agency for International Development's Development Innovation Ventures program for application in public goods grant contexts.

This runbook covers a three-stage program. Programs with two stages should use Runbook 2 (Staged Development). Programs with four or more stages should extend this runbook's pattern.

**Obligation mode: Build obligation at Stage 1. Build obligation or change obligation at Stage 2, configurable by the funder. Change obligation at Stage 3, with independent evaluation at the completion gate.**

**Stage 1 gate configuration.**

| Gate | Active | Evidence scope | Evidence strength | Infrastructure requirement |
|---|---|---|---|---|
| Entry specification | Yes | Output | Self-report with documentation | Staff review of deliverable specification |
| Progress verification | Configurable | Output | Self-report with documentation | Staff check-in if activated |
| Completion verification | Yes | Output | Third-party verifiable | Named staff confirms publicly accessible deliverable |
| Continuation gate (Stage 1 to Stage 2) | Yes | Output and Usage | Third-party verifiable | Staff verifies publicly accessible evidence of use by external parties before Stage 2 funding is committed |

**Stage 2 gate configuration.**

| Gate | Active | Evidence scope | Evidence strength | Infrastructure requirement |
|---|---|---|---|---|
| Entry specification | Yes | Output and Usage | Third-party verifiable | Review panel or named staff reviews the continuation gate evidence record and the Stage 2 proposal |
| Progress verification | Yes | Output or Outcome | Third-party verifiable | Named staff reviews the progress artifact at the mid-stage disbursement point |
| Completion verification | Yes | Usage or Outcome | Independent review | Named independent reviewer with relevant domain expertise confirms completion against published criteria |
| Continuation gate (Stage 2 to Stage 3) | Yes | Outcome | Independent review | Named independent reviewer confirms that measurable change evidence meets the standard before Stage 3 funding is committed |

**Stage 3 gate configuration.**

| Gate | Active | Evidence scope | Evidence strength | Infrastructure requirement |
|---|---|---|---|---|
| Entry specification | Yes | Outcome | Independent review | Review panel assesses the Stage 2 completion record and the Stage 3 proposal, including a cost-effectiveness consideration |
| Progress verification | Yes | Outcome | Third-party verifiable | Named staff reviews outcome data at the mid-stage disbursement point |
| Completion verification | Yes | Impact | Independent evaluation | A qualified evaluator with relevant domain expertise conducts a structured assessment of whether the funded work produced the claimed outcome, using methods sufficient to support causal inference |
| Continuation gate (Stage 3 onward) | Configurable | Impact | Independent evaluation | If further stages are planned, an impact evaluation finding is required before commitment |

**Cost-effectiveness at the Stage 2 to Stage 3 continuation gate.** The continuation gate from Stage 2 to Stage 3 includes a cost-effectiveness consideration as a required element, per Part IV of the standard. The review panel must assess whether the evidence from Stage 2 indicates that further investment in this intervention produces meaningful change relative to available alternatives. This is not a disqualifying criterion at Stage 1 or Stage 2 entry; it applies only at the continuation gate before Stage 3 funding is committed.

**Change obligation activation.** At Stage 2, the funder may configure either build obligation or change obligation. Build obligation at Stage 2 is appropriate where the program area is still developing the deliverable infrastructure needed before population-level outcomes can be measured. Change obligation at Stage 2 is appropriate where Stage 1 produced a deployed artifact with external users and a measurable baseline exists. The Grant Configurator supports mode assignment per stage.

**Conflict of interest.** Standard three-tier declaration applies at each stage. Independent reviewers at Stage 2 and evaluators at Stage 3 must complete conflict of interest declarations before accessing any application material. The infrastructure declaration for Stage 2 independent review and Stage 3 independent evaluation must confirm the declaration status of the named reviewer or evaluator before the relevant round opens.

**Infrastructure declaration requirements.** Stage 2 completion verification and the Stage 2 to Stage 3 continuation gate require independent review. Stage 3 completion verification requires independent evaluation. For each of these, before the relevant round opens, the funder must publish: who will conduct the review or evaluation, what qualifications they hold relative to the program area, what process they will follow, and what the timeline for completion is. A generic designation such as "expert panel" without named individuals and stated qualifications does not satisfy the infrastructure declaration requirement.

**Recommended rubric emphasis.** The rubric must be calibrated per stage. Stage 1 emphasis mirrors the Discovery Sprint: Field 11, Field 5, Integrity standard. Stage 2 emphasis adds the Validity standard (is there a documented causal chain from the Stage 1 deliverable to the observed usage or outcome?) and Field 10 (is the baseline for the Stage 2 indicator independently sourced and expressed in consistent units with the target?). The cost-effectiveness advisory criterion should appear in the Stage 2 rubric as an advisory item for reviewers to note. Stage 3 emphasis shifts to the Precision standard (is the measurement instrument precise enough to detect the claimed effect size?) and the Validity standard for causal attribution (does the evidence support a credible causal inference, not merely correlation?). The cost-effectiveness criterion becomes required at Stage 3 entry. Funder guidance additions for each stage should specify what the program considers adequate causal documentation for this domain, since causal standards vary significantly across fields.

**Recommended evolution path.** A program that has run three stages and produced an impact evaluation has the evidence base to publish a detailed public record of what worked, what the cost per unit of change was, and what conditions enabled or limited the outcome. The CROSS conformance record, tracked in the Grant Configurator across rounds, makes this data available. Publishing it is not a CROSS conformance requirement, but it represents the institutional learning the graduated evidence structure is designed to produce.

**Example programs.** United States Agency for International Development Development Innovation Ventures (exploratory, testable, and transition-to-scale stages), Sovereign Tech Fund infrastructure grants (exploration, development, and scaling phases), web3 programs that want to move from tool-building to measured population-level outcomes over time.

---

## Runbook 6: Institutional Conformance

**Program type this runbook serves.** Programs operating within or alongside institutional obligation frameworks: development agencies, foundations with formal reporting requirements, government grant programs, or organizations that must satisfy external conformance obligations such as environmental and social standards, procurement integrity requirements, or gender equity obligation. This runbook adapts the CROSS gate architecture to the obligation requirements common in these contexts.

This runbook is the most demanding configuration in the initial library. It is not appropriate for small community grants or early-stage innovation funding. It is appropriate for large grants to established organizations operating at scale, where the obligation requirements are proportional to the scale of the public impact claim and the institutional conformance environment.

**Obligation mode: Change obligation.**

Institutional programs at this scale should be able to specify a FROM state, a measurable indicator, and a TO state. If an applicant in this context cannot specify a FROM state, the entry specification gate fails and the application does not proceed. A large-scale institutional grant to address a problem the applicant cannot name as a specific measurable condition in a defined population does not meet the minimum standard for this funding tier.

**Dimensions activated.** In addition to the standard dimensions, this runbook activates: the environmental and social impact dimension from Part II, using the A/B/C classification structure described below; the gender equity dimension from Part II, requiring disaggregated outcome reporting; and the procurement integrity dimension from Part II, for any sub-contracting or sub-granting above 20% of the total award.

**Gate configuration.**

| Gate | Active | Evidence scope | Evidence strength | Infrastructure requirement |
|---|---|---|---|---|
| Entry specification | Yes | Outcome (FROM state required) | Third-party verifiable | Review panel assesses the FROM state specification, institutional capacity documentation, and conformance screening |
| Environmental and social screening (at entry) | Yes | Output | Independent review | Named environmental and social specialist reviews the screening documentation before any award commitment |
| Progress verification | Yes | Outcome | Third-party verifiable | Named staff reviews outcome data and conformance reports at each disbursement tranche |
| Completion verification | Yes | Outcome | Independent review | Named independent reviewer with relevant domain expertise confirms completion against the published criteria and conformance requirements |
| Continuation specification | Configurable | Outcome and Impact | Independent evaluation | Where a second phase is planned, the continuation gate requires an independent evaluation of the first phase before Phase 2 funding is committed |

**Entry specification requirements for this runbook.** The applicant must provide: (1) a FROM state specification with a named data source and a documented baseline; (2) institutional capacity documentation including organizational history, prior grants of comparable scale with verified outputs, and financial management systems; (3) environmental and social screening documentation at the level appropriate to the classified impact category; and (4) a procurement plan for any sub-contracting or sub-granting above 20% of the total award. The conflict of interest declaration covers organizational conflicts, where the reviewer's employer has a material financial relationship with the applicant, as well as individual relationships.

**Environmental and social classification.** The environmental and social impact dimension uses the following classification, derived from International Finance Corporation Performance Standards and Green Climate Fund Environmental and Social Policy.

Category A: projects with significant, diverse, potentially irreversible, or unprecedented impacts on communities, ecosystems, or cultural heritage. Requires an environmental and social impact assessment by a qualified specialist before the entry specification gate passes.

Category B: projects with limited, reversible impacts that can be mitigated with standard practices. Requires an environmental and social management plan submitted with the application.

Category C: projects with minimal environmental and social impacts. Requires a screening declaration confirming Category C classification, reviewed by named staff.

The applicant self-classifies; the independent environmental and social review at the entry specification gate may reclassify. A reclassification from Category C to Category B, or from Category B to Category A, does not automatically disqualify the application, but it extends the review timeline and changes the completion verification requirements.

**Conflict of interest in institutional contexts.** In programs involving institutional funders and established organizations, organizational conflicts are especially common: the reviewing organization and the applying organization may have partnerships, co-funding arrangements, or prior sub-contracting relationships. The organizational conflict category from Part VII of the standard applies: a reviewer whose employer has a material financial relationship with the applicant is a Tier 2 conflict requiring disclosure and a qualified waiver. In large institutional programs, this should be treated as a structural issue to be addressed in panel composition, not only through individual disclosures.

**Infrastructure declaration requirements.** The environmental and social screening at entry requires a named environmental and social specialist, their qualifications, and the review timeline. The completion verification at independent review level requires a named independent reviewer, their domain expertise, and the timeline. If a continuation specification gate is configured, the independent evaluation requires the same declarations. All must be published before the round opens.

**Procurement integrity requirements.** Where sub-contracting or sub-granting exceeds 20% of the total award, the applicant must submit a procurement plan documenting: the selection criteria for sub-contractors, the competitive process used, any relationships between the applicant and the selected sub-contractor that would constitute a conflict of interest under Part VII, and the reporting requirements placed on the sub-contractor. The funder reviews the procurement plan at the progress verification gate to confirm that awarded sub-contracts match the submitted plan.

**Recommended rubric emphasis.** For institutional conformance rounds, the FROM state quality (Field 10) is the most load-bearing rubric criterion. A weak FROM state specification is a harder failure in this program type than in community rounds: institutional funders expect documented, independently sourced baselines as a prerequisite for any outcome claim. The Validity standard (is the causal chain from intervention to claimed outcome documented at institutional standards?) and the Integrity standard (are named independent sources present for every material claim?) are the two highest-priority data quality criteria. If the environmental and social impact dimension is activated, the classification quality rubric section should specify the evidence required to substantiate each category level. Funder guidance additions should state explicitly what institutional documentation standard this program applies (International Finance Corporation Performance Standards, Green Climate Fund Environmental and Social Policy, or another named standard) so reviewers assess FROM state quality against a named benchmark rather than their own judgment.

**Recommended evolution path.** A funder operating this runbook for two or more cycles with the same class of applicants should consider publishing a program-level public record of environmental and social findings, gender-disaggregated outcome data, and completion evidence. The CROSS conformance record, tracked in the Grant Configurator, makes this data available across rounds. Publishing it represents the obligation maturation the institutional conformance configuration is designed to enable.

**Example programs.** Green Climate Fund project financing, World Bank small grants programs, Innovate UK innovation grants with procurement and reporting requirements, foundation programs requiring gender-disaggregated outcome reporting, and web3 grant programs that have chosen to align with institutional environmental and social standards for reasons of donor obligation direction or global recognition.

---

## Customizing a Runbook

A runbook is a starting point. Funders should review three areas when adapting a runbook to their program context.

The first is evidence strength. Any gate may be configured at a higher evidence strength than the runbook specifies; none may be configured lower. If a funder finds the specified strength operationally infeasible, that indicates either that the program needs additional review infrastructure, or that a different runbook is more appropriate.

The second is dimension activation. Optional dimensions (environmental and social impact, gender equity, procurement integrity) may be activated for any runbook. The runbook notes whether they are typically activated for the program type; funder configuration determines whether they apply in a specific round.

The third is stage configuration. Runbooks 2 and 5 cover staged programs. If a program has a different number of stages than the runbook specifies, extend or truncate the stage configuration. The gate architecture applies to each stage independently. Do not configure a stage without publishing its gate requirements before the stage opens.

No customization may reduce the minimum evidence requirements from Part IV of the standard, waive the conflict of interest framework from Part VII, or remove the concurrent funding disclosure requirement from Part VI.

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-14 | Initial draft. Six runbooks: Discovery Sprint, Staged Development, Community Allocation with Build Accountability, Retroactive Impact, Graduated Evidence, and Institutional Compliance. |
