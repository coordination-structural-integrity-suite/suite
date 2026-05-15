# CROSS: Common Reporting Outcome Standards Schema

Version 0.2.0 | 2026-05-14 | CC0

Most grant programs have a funding process but no accountability standard. They collect applications, select projects, distribute funds, and hope for the best. CROSS fills that gap.

CROSS is a standard for grant accountability. It answers three questions that every grant program must answer but rarely specifies: what must an applicant demonstrate before funding is approved, what must a grantee report during the grant, and what evidence must a funder actually evaluate before releasing each payment. It does this across three types of grants: grants for building something specific, grants for producing a measurable change in the world, and grants recognizing work already done.

CROSS does not tell programs how to run their governance, how to score applications, or how to distribute funds. It specifies the content of accountability at each stage of the funding lifecycle, and makes that content portable across programs so that grantees, funders, and evaluators work from the same definitions.

---

## License

CROSS is dedicated to the public domain under **Creative Commons Zero v1.0 Universal (CC0)**. See `LICENSE-CROSS` for the full dedication.

CROSS is an independently published standard. It is co-released alongside the Coordination Structural Integrity Suite but is not a Suite document and does not carry the Suite's CC BY 4.0 license. Any grants ecosystem can adopt CROSS without adopting the Suite.

---

## What is in this folder

**Main standard**

`CROSS-common-reporting-outcome-standards-schema-0_2_0.md` is the canonical specification. Read this first.

**Companion documents**

`CROSS-runbooks-0_1_0.md` contains six pre-built gate configuration packages for common program types: Discovery Sprint, Staged Development, Community Allocation with Build Accountability, Retroactive Impact, Graduated Evidence, and Institutional Compliance. Each runbook selects an accountability mode, configures gate evidence requirements, and includes a recommended rubric emphasis section. Funders new to CROSS should start with the runbook that best matches their program type.

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
