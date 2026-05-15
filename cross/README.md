# CROSS: Common Reporting Outcome Standards Schema

Version 0.2.0 | 2026-05-14 | CC0

Most grant programs have a funding process but no accountability standard. They collect applications, select projects, distribute funds, and hope for the best. CROSS fills that gap.

CROSS is a standard for grant accountability. It answers three questions that every grant program must answer but rarely specifies: what must an applicant demonstrate before funding is approved, what must a grantee report during the grant, and what evidence must a funder actually evaluate before releasing each payment. It does this across three types of grants: grants for building something specific, grants for producing a measurable change in the world, and grants recognizing work already done.

CROSS does not tell programs how to structure their coordination, how to score applications, or how to distribute funds. It specifies the content of accountability at each stage of the funding lifecycle, and makes that content portable across programs so that grantees, funders, and evaluators work from the same definitions.

---

## Why CROSS was designed this way

Comparative examination of thirteen grant programs spanning web3, open source, and institutional funding contexts reveals a consistent pattern: the failure locates itself differently depending on the type of program.

In web3 and blockchain grant programs, the hard part is consistently upstream: at the point of claim specification. Applicants default to aspiration language: direction statements that name what they are trying to achieve rather than conditions that can be independently measured. Without a specific measurable baseline, there is no measurement instrument. There is no FROM state, so there can be no TO state, so there can be no outcome. The evaluation process ends up assessing the quality of the aspiration, not the credibility of the claim. Funding decisions are made on the basis of who sounds most plausible, not who has specified what they will actually produce.

In governmental and institutional grant programs, the hard part tends to locate itself downstream: at the point of reporting and verification. The compliance layer is thick. Applications are detailed. Reports arrive on schedule. But the reports describe activity, not outcomes. Grantees learn to write good reports rather than to produce measurable results. Funders receive documentation they cannot verify against any pre-specified baseline. The evidentiary chain between award and impact exists on paper but not in practice.

CROSS was designed to be portable across both failure modes. It does this by separating the evidentiary structure from the program design, and making both configurable.

The three obligation modes allow funders to match the accountability structure to the nature of the work. Build obligation applies where the deliverable is a specific artifact: something is either built or it is not, and the gate tests whether the delivered thing matches what was specified. Change obligation applies where the goal is a measurable shift in the world: the entry specification gate requires a specific measurable baseline and a targeted state in the same units, which prevents aspiration language from entering the record at all. Retroactive obligation applies where the work is already done: the gate tests whether the documented impact is credibly attributed to the prior work.

A structural innovation in CROSS is the distinction between build nested inside change and build as a replacement for change. Many grant programs encounter applications that profess a theory of change (a specified FROM condition, a defined population, a targeted TO state, and a mechanism connecting the intervention to the shift) but present only a theory of build: the applicant describes what they will produce without specifying what condition in the world is different because of it. Prior to CROSS, this distinction was a matter of reviewer judgment, which is inconsistently applied and difficult to defend at scale. CROSS makes it structurally testable.

Build legitimately sits inside a change-obligation claim when the applicant can name a FROM state that satisfies the entry gate: a specific measurable condition in a defined population, with a named data source, that the built thing is designed to address. In that case the build is the mechanism of change and the change specification is intact. The two are nested correctly. Build becomes the failure mode when it has replaced the change specification entirely: the applicant names a deliverable where a problem diagnosis was required, and cannot produce a FROM state because the problem was never diagnosed before the solution was designed. The entry specification gate surfaces this immediately. An applicant who began with the problem produces the FROM state, because naming a specific measurable condition in a defined population is the natural output of having diagnosed it. An applicant who began with the solution cannot, because the problem was never named before the solution was conceived.

The gate architecture allows funders to configure where the evidentiary pressure falls. A small community program running its first funding round may need only an entry specification gate: establish what is being built or changed before any funds release. A large institutional program running a multi-year initiative may need all four gates: entry specification before funding, milestone gates during delivery, a completion gate at close, and a continuation gate governing whether the grantee enters the next round. The gates that apply, and the rigor tier at which each gate is set, are published in the round specification before any application opens. The gate is one layer of detection; the assessment rubric and the reviewer assessment are structurally distinct additional layers, each operating with different evidence and different points of failure.

The result is a system where the hard part is placed where the structural failure mode requires it. For programs where baseline specificity is the failure mode, the entry specification gate installs it at the front. For programs where outcome verification is the failure mode, the milestone and completion gates install it at the back. The configuration is funder-facing; the field definitions are standardized across funders so that a grantee's CROSS record from one program is directly readable by a reviewer at a different program. The hard part, wherever it is placed, is done once rather than re-invented per funder.

---

## License

CROSS is dedicated to the public domain under **Creative Commons Zero v1.0 Universal (CC0)**. See `LICENSE-CROSS` for the full dedication.

CROSS is an independently published standard. It is co-released alongside the Coordination Structural Integrity Suite but is not a Suite document and does not carry the Suite's CC BY 4.0 license. Any grants ecosystem can adopt CROSS without adopting the Suite.

---

## What is in this folder

**Main standard**

`CROSS-common-reporting-outcome-standards-schema-0_2_0.md` is the canonical specification. Read this first.

**Companion documents**

`CROSS-runbooks-0_1_0.md` contains six pre-built gate configuration packages for common program types: Discovery Sprint, Staged Development, Community Allocation with Build Obligation, Retroactive Impact, Graduated Evidence, and Institutional Conformance. Each runbook selects an accountability mode, configures gate evidence requirements, and includes a recommended rubric emphasis section. Funders new to CROSS should start with the runbook that best matches their program type.

`CROSS-common-reporting-outcome-standards-schema-guidance-0_2_0.md` contains field-by-field guidance for applicants completing an entry specification under any accountability mode. It covers the three-mode entry specification architecture, the gate framework, field interpretation, and the distinction between D1 (sourcing) and D2 (specification) failures.

`CROSS-common-reporting-outcome-standards-schema-rubric-0_2_0.md` contains the funder-facing assessment rubric. It is organized by accountability mode. Funders configure the rubric for their round using the Grant Configurator; the confirmed rubric block is published before the round opens and loaded by reviewers without modification.

`CROSS-common-reporting-outcome-standards-schema-templates-0_2_0.md` contains submission templates for each accountability mode and gate type, including the gate evidence submission template.

`CROSS-common-reporting-outcome-standards-schema-worked-examples-0_2_0.md` contains six cases demonstrating how the entry specification gate and rigor tier apply across different application types, including boundary cases.

**Implementation documents**

`CROSS-grant-configurator-0_2_0.md` specifies the funder-facing instrument for configuring a CROSS-conformant round. It generates the round specification (accountability mode, gate configuration, rubric, common indicators) from a structured question sequence. It also specifies the base configuration onboarding flow for funders new to CROSS, including five funder-type profiles.

`CROSS-grantee-dashboard-0_2_0.md` specifies the post-award grantee interface: obligation registry, progress tracking by accountability mode, disaggregation ratchet, reporting schedule, gate evidence submission, disbursement conditions, and attestation format suitable for onchain publication.

`CROSS-reviewers-dashboard-0_1_0.md` specifies the evaluation-stage interface for reviewers: stage-gated access, conflict of interest enforcement as an application-level access gate, assessment isolation, three-role architecture (guest reviewer, lead reviewer, funder administrator), and three-layer AI assistance (evidence verification, independent investigation, draft evaluation).

**Skills**

`skills/claude-skill-CROSS-0_2_0.md` is the Claude skill for applying CROSS in an extended AI-assisted session. It encodes the three accountability modes, gate architecture, indicator specification fields, and the full assessment rubric in a format optimized for AI-assisted grant evaluation and program design.

---

## Relationship to the Coordination Structural Integrity Suite

CROSS inherits requirements from four Suite standards by reference:

- Adverse Signal Engagement Principle Core Standard: disclosure requirements for adverse signals
- Information Asymmetry Classification Standard: omission asymmetry requirements for concurrent funding disclosure
- Precision-First Design Standard: indicator sourcing requirements and the double-negation invariant
- Regenerative Obligation Standard: direction of accountability (what the Suite addresses) as the structural complement to CROSS's destination (what CROSS addresses)

Adoption of CROSS does not require adoption of the Suite. The inherited requirements are fully stated within CROSS.

---

## Version history

| Version | Date | Summary |
|---------|------|---------|
| 0.2.0 | 2026-05-14 | Three accountability modes, four-gate architecture, program-level continuation gate, open measurement form replacing constrained data type list, runbooks, full implementation document suite. |
| 0.1.0 | 2026-05-14 | Initial release. Change accountability mode, Level 1 and Level 2 gate structure. |
