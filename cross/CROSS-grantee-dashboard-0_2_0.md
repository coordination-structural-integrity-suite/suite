---
title: CROSS Grantee Dashboard
version: 0.2.0
date: 2026-05-14
license: CC0
status: Working draft. Implementation specification inheriting from CROSS-common-reporting-outcome-standards-schema-0_2_0.md. Supersedes version 0.1.0.
related_documents:
  - standards/CROSS-common-reporting-outcome-standards-schema-0_2_0.md
  - standards/CROSS-grant-configurator-0_2_0.md
---

# CROSS Grantee Dashboard

Version 0.2.0 | 2026-05-14 | CC0

---

## Section 1: Purpose and Scope

The CROSS (Common Reporting Outcome Standards Schema) Grantee Dashboard is a post-award obligation tool. It takes the structured commitments from an approved grant application and converts them into a persistent, live record that accumulates over the full duration of the grant. The Dashboard is the operational home for everything a grantee committed to at award time: the indicator targets, the gate configuration, the reporting schedule, the disbursement conditions, and the methodology declarations that make those commitments verifiable.

The Dashboard is not a reporting form. A reporting form is filled out at each reporting milestone and submitted for review. The Dashboard is the record in which each submission lands and accumulates. It persists between reporting periods, displays running progress, enforces schema conformance at submission time, tracks gate evidence packages, and produces the signed attestations that constitute the onchain obligation record.

The Dashboard is schema-driven rather than freeform. Because field definitions, measurement form declarations, operational definitions, construction methodologies, disaggregation categories, and gate configurations were specified before the award in the round specification produced by the CROSS Grant Configurator, subsequent reporting is structured input against a declared schema. Grantees do not choose what to report at each period; they submit values against the commitments they already made and evidence against the gate requirements that were published before the round opened.

This version (0.2.0) extends version 0.1.0 in three structural ways. First, the Dashboard is now mode-aware: the obligation registry records the obligation mode (build, change, or retroactive), and indicator progress tracking, attestation format, and completion verification behavior differ by mode. Second, gate evidence submission tracking is introduced as a discrete function: progress verification gates and the completion verification gate each have their own evidence submission and verification workflow, separate from the periodic indicator reporting workflow. Third, the data model updates the `data_type` field to `measurement_form` with three classification axes, reflecting the v0.2.0 change to the indicator specification in the CROSS standard.

The Dashboard serves two principal user groups. Grantees use it to submit periodic reports, submit gate evidence packages, track progress against their targets, monitor the status of disbursement conditions, and sign attestations. Funders use it to review grantee progress, verify gate submissions and conditions, approve methodology changes, and view cross-grantee comparisons for round-level common indicators.

---

## Section 2: Obligation Registry

When a grant is awarded, the Dashboard generates one obligation registry entry for the funded application. The obligation registry is the authoritative record of what the grantee committed to at award time and the terms under which disbursement occurs. Every subsequent report, gate submission, condition verification, and attestation is filed against this registry entry.

### Registry contents

Each obligation registry entry contains the following elements.

**Round specification reference.** The round identifier and a reference to the round schema published by the funder at round open. The round schema is not embedded in the registry; it is referenced by identifier. Both documents are immutable once published.

**Obligation mode.** The declared obligation mode for this round: build, change, or retroactive. The mode determines which indicator tracking behavior applies (Section 3), which gate evidence requirements are active (Section 6), and which progress display logic is used.

**Gate configuration reference.** The evidence scope, evidence strength, and infrastructure declaration for each active gate in this round, as specified in the round specification. The Grantee Dashboard uses this configuration to structure gate submission forms, display gate status, and enforce the disbursement logic that connects gate verification to payment.

**Indicator commitments.** For every outcome indicator the grantee committed to in their approved application, the registry records all fields from Part V of the CROSS standard: indicator name, rationale, measurement form description with three-axis classification (source type, measurement form, aggregation type), operational definition, construction and aggregation methodology, cumulative or non-cumulative designation, disaggregation categories, data source and collection method, data cost attestation, baseline, and target. These fields are recorded exactly as submitted and approved. They are not paraphrased or reformatted.

For build-obligation applications: the registry records the deliverable specification and completion criteria from Template 1A in place of the change-obligation FROM/TO indicator fields. The completion criteria are what the completion verification gate assesses.

For retroactive applications with a configured forward commitment: the forward commitment is recorded as a build-obligation indicator commitment alongside the prior contribution evidence summary.

**Concurrent funding disclosure snapshot.** The full concurrent funding disclosure as submitted at the time of application. This snapshot is taken at award and does not update automatically. Subsequent changes to the grantee's funding relationships that are material to the scope of the award must be disclosed through the amendment process.

**Hard-gate conditions and their verification status.** Where the funding committee's recommendation specified conditions that must be satisfied before disbursement occurs, the registry lists each condition, its verification method, the named verification contact, and its current status (pending, verified, or failed).

**Reporting schedule.** The reporting frequency was set in the round specification. The registry records the full schedule: each reporting period's start and end dates, the submission deadline, and the disbursement decision (if any) that depends on each report.

**Disbursement structure.** Each tranche, the amount, the milestone or reporting submission it depends on, and any gate verification requirements that gate that tranche.

### Mutability structural conditions

The obligation registry is immutable once set at award. When a change is necessary, it must go through the amendment process. An amendment requires committee approval and records the prior value, the new value, the reason, and the approval timestamp. The original commitment remains visible in the registry alongside the amendment. The registry does not hide or overwrite what was originally committed; it appends the approved change as a documented amendment.

---

## Section 3: Indicator Progress Tracking

The Dashboard tracks and displays progress for each indicator in the obligation registry. Progress display logic depends on the obligation mode and, for change-obligation and some build-obligation indicators, whether the indicator is cumulative or non-cumulative.

### Build-obligation progress tracking

For build-obligation applications, progress is tracked as completion status against the published criteria, not as incremental values against a numeric target. The Dashboard displays: each completion criterion from the registry, the current confirmation status of each criterion (not yet confirmed, in progress, or confirmed), the named verifying party for each criterion (where specified), and the overall completion status of the deliverable (all criteria confirmed, partial, or no criteria confirmed).

For build-obligation grants with milestone-based disbursements, each milestone has its own set of criteria and its own confirmation status. Progress across milestones is displayed in timeline form, with each milestone's status visible in relation to the overall grant timeline.

The Dashboard must not display a "percentage complete" or numeric progress figure for a build-obligation indicator unless the indicator is explicitly a quantitative count (for example, a deliverable milestone that requires a specific number of test cases to pass). Binary or qualitative completion criteria are not amenable to percentage representations and must not be forced into one.

### Change-obligation progress tracking: cumulative indicators

For indicators designated as cumulative, the Dashboard displays: the running total accumulated from all reporting periods to date, the period-by-period increments submitted in each report, the life-of-grant target, and the percentage of the life-of-grant target achieved to date.

### Change-obligation progress tracking: non-cumulative indicators

For indicators designated as non-cumulative, the Dashboard displays the most recent period's status value, the life-of-grant target status (the target status to be achieved by grant end, not a sum of period targets), and the trend across periods (a time-series display of reported values by period).

The Dashboard must not sum non-cumulative indicator values across periods and must not display a "total" for a non-cumulative indicator. A non-cumulative indicator measures a status at a point in time; summing status measurements is a data construction error. This prohibition is enforced by design: the Dashboard's aggregation logic must distinguish the two types and apply the correct display accordingly.

### Retroactive obligation progress tracking

For retroactive applications without a forward commitment, there is no post-award progress to track. The obligation registry records the prior contribution evidence, and the funder's rubric assessment is the sole obligation record for that grant. The Dashboard records the assessment and the award; no periodic reporting is required.

For retroactive applications with a configured forward commitment, the forward commitment is tracked as a build-obligation indicator. Progress display follows the build-obligation tracking logic above.

### Methodology consistency check at submission

When a grantee submits a change-obligation indicator value that differs substantially from the prior period's value, the Dashboard requires a methodology note before accepting the submission. The threshold for "differs substantially" is a change exceeding 20% of the prior period's value, or a direction reversal, unless the indicator is explicitly designed to fluctuate. The threshold may be configured by the funder at the round level.

This mechanism enforces the reliability standard from Part VIII of the CROSS standard. It does not reject the submission; it holds it pending the note. Once a methodology note is attached, the submission proceeds.

---

## Section 4: Disaggregation Ratchet Handling

The disaggregation ratchet is established in Part V of the CROSS standard. Disaggregation categories committed to in the application may be supplemented in subsequent reporting periods but may not be removed without committee approval and documented rationale.

The Dashboard enforces the disaggregation ratchet through two mechanisms.

First, committed disaggregation categories appear as required fields in every subsequent report. The Dashboard's report submission interface generates required fields from the obligation registry at the start of each reporting period.

Second, attempting to submit a report without a committed disaggregation category produces a validation error. The Dashboard rejects the submission and identifies the missing required field by name.

Adding a new disaggregation category is permitted and does not require committee approval. Once a disaggregation category has been reported, it enters the ratchet and cannot be silently dropped.

---

## Section 5: Reporting Schedule and Timeline

The reporting frequency was established in the round specification and carried into the obligation registry. The Dashboard derives the full reporting schedule from the frequency and the grant start date, producing a complete list of reporting periods with deadlines before the grant begins.

At any point in the grant, the Dashboard displays: the next reporting deadline, the period covered by the upcoming report, the list of fields that must be completed for a valid submission, and where applicable, the disbursement tranche that depends on the submission.

### Overdue mechanism

A report not submitted by its deadline triggers a notification to both the grantee and the funder. After a grace period of 14 days past the deadline (configurable by the funder at the round level), an overdue report triggers a flag on the disbursement decision associated with that reporting period. The flag does not automatically block disbursement; it requires the funder's active review before disbursement proceeds.

---

## Section 6: Gate Evidence Submission Tracking

The gate architecture from Part IV of the CROSS standard introduces four gate types whose evidence requirements are configured in the round specification. The Dashboard tracks each active gate as a discrete obligation event, separate from periodic indicator reporting.

### Gate types and Dashboard behavior

**Entry specification gate.** The entry specification gate is assessed at the application stage; it is not a post-award Dashboard function. The Dashboard records whether the entry specification gate passed (a required field on all registry entries) and retains the gate finding as part of the obligation registry.

**Progress verification gates.** Each configured progress verification gate corresponds to a milestone disbursement tranche. The Dashboard surfaces a gate submission form when the grantee's grant reaches the relevant point in the timeline. The grantee submits an evidence package using Template 10 (Gate Evidence Submission Form). The submission records: the gate being submitted for, the evidence type and scope, publicly accessible evidence links or artifact descriptions, and any mode-specific completion criteria status.

For build-obligation progress gates: the submission must include a publicly accessible link to the artifact demonstrating progress, and confirmation of which completion criteria from the milestone are met.

For change-obligation progress gates: the submission must include the indicator value for the period, the data source reference, and evidence at the strength level configured for this gate.

**Completion verification gate.** This gate determines whether final payment is released. The Dashboard makes the completion verification gate submission form available after the final reporting period has closed. The grantee submits their completion evidence package using Template 10. The completion gate cannot be bypassed or self-attested; grantee self-report alone does not satisfy the completion verification gate at any evidence strength level.

For build-obligation rounds: the completion gate submission must include a publicly accessible link demonstrating that the specified deliverable is publicly available, plus confirmation that each completion criterion is met. The Dashboard enforces the public accessibility requirement: the submission cannot be marked complete unless a publicly accessible URL is provided. Final payment is blocked until this field is confirmed.

For change-obligation rounds: the completion gate submission must include outcome data against the baseline established at entry, at the evidence scope and strength configured for the round.

**Continuation specification gate.** For programs with a program-level continuation gate, the Dashboard surfaces a continuation gate submission interface when the grantee is preparing to apply for the next stage. The continuation gate submission records: evidence at the required scope and strength for the configured continuation gate, and any cost-effectiveness assessment if the continuation gate requires it (applicable to Stage 2-to-Stage 3 transitions in Graduated Evidence programs). The continuation gate submission is linked to the next stage's application, not to the current award.

### Gate verification workflow

Gate submissions received from grantees are routed to the configured verification contact for the gate. The verification contact reviews the submitted evidence against the published gate criteria and marks the gate as verified or failed.

Grantees cannot mark their own gate submissions as verified. Self-attestation is not sufficient for any gate at progress verification level or above. The role restriction is enforced at the interface level: the verification status field is not editable by grantee users.

Where a gate is configured at independent review level or above, the named reviewer from the infrastructure declaration is the verification contact. The Dashboard records the reviewer's identity, the date of verification, and any notes. This record is part of the onchain obligation record for the grant.

Failed gate submissions block the associated disbursement tranche. The grantee may resubmit with corrected or supplemented evidence. The funder may document a waiver with a recorded rationale. Both paths create an amendment record.

### Gate status display

The Dashboard displays gate status for each active gate in a prominent position on the grantee's record. Status values: not yet open (the gate's submission window has not opened), open for submission, submitted (evidence received, pending review), verified, failed, and waived (with rationale on record).

The disbursement interface shows which tranches are blocked by pending gate verifications, making the connection between gate status and payment release explicit.

---

## Section 7: Disbursement Condition Tracking

Where the funding committee issued a "Fund with conditions" recommendation, the award included specific conditions that must be satisfied before disbursement occurs. The Dashboard tracks each condition as a discrete record.

Each condition record contains: the specific requirement as stated in the committee recommendation (verbatim, not paraphrased), the named verification method, the verification contact, and the status (pending, verified, or failed).

Disbursement is locked for the relevant tranche until all conditions associated with that tranche are marked verified. The verification contact named in the condition record may mark the condition verified; the grantee cannot. Where a condition fails, it blocks disbursement until remediation is complete and re-verified, or until the committee takes a formal action recorded as an amendment.

---

## Section 8: Attestation Format and Signing

Each periodic report submitted by the grantee is a signed attestation. The attestation constitutes a formal, datestamped declaration that the submitted data is accurate, sourced as specified in the obligation registry, and constructed using the committed methodology.

### Attestation structure

Each attestation contains: the period covered, the indicator values submitted with disaggregated breakdowns, the construction methodology reference (matching the committed methodology or the most recent approved amendment), any methodology note required by the reliability check, and a standard declaration generated by the Dashboard that the grantee confirms by signing.

Gate submissions produce separate gate attestations that are distinct from periodic indicator attestations. A gate attestation declares that the evidence submitted is accurate, the deliverable is publicly accessible (for build-obligation completion gates), and the data was collected and constructed using the specified methodology. Gate attestations are signed by the grantee and countersigned by the verification contact upon verification.

### Methodology change process

If the committed construction methodology must change, the grantee must submit a methodology change notice before submitting data under the new methodology. The change notice documents: the reason the methodology must change, the impact on comparability with prior periods, and the committee's approval. The committee's approval is recorded as an amendment. The Dashboard records the prior methodology text, the new text, the reason, and the approval timestamp.

A grantee cannot submit an attestation under a new methodology without a prior approved change notice. The Dashboard rejects submissions whose methodology reference does not match the committed methodology or the most recent approved amendment.

---

## Section 9: Onchain Publication Protocol

The Dashboard produces attestations suitable for publication on a blockchain. The onchain record enables any party to inspect the record, verify the signature, confirm that the methodology has not changed without notice, and assess the grantee's historical performance without relying on the funder's continued custody of the data.

### Data model for an onchain attestation

Each onchain attestation record contains the following fields.

`round_id`: the identifier of the funding round.

`grantee_id`: the identifier of the grantee entity.

`reporting_period`: the start and end dates of the period covered.

`indicator_id`: the identifier of the indicator, matching the indicator commitment in the obligation registry.

`value`: the reported value for this indicator in this period. For build-obligation completion attestations, this is the confirmation status of each completion criterion, not a numeric value.

`measurement_form_hash`: a cryptographic hash of the measurement form description and three-axis classification as recorded in the obligation registry at commitment time (or the most recent approved amendment). This replaces the `data_type` field from version 0.1.0.

`methodology_hash`: a cryptographic hash of the methodology text as recorded in the obligation registry.

`data_source_id`: the identifier of the named data source.

`timestamp`: the date and time of attestation submission.

`grantee_signature`: the cryptographic signature over the canonical encoding of the above fields.

Gate attestations use the same structure with `value` replaced by `gate_evidence_reference` (a content-addressed reference to the submitted evidence package) and an additional `gate_type` field identifying which gate is being attested.

### Append-only record

The onchain record is append-only. Corrections are recorded as correction attestations that reference the original by identifier and state the corrected value and reason. The original attestation remains on the record alongside the correction.

### The three-component obligation ledger

A complete CROSS obligation ledger entry consists of: the round schema (published by the funder at round open, immutable), the application commitments (published onchain at award), and the periodic attestations plus gate attestations (published at each submission). Together, these allow any external party to verify what the round required, what the grantee committed to, and what the grantee actually reported, period by period and gate by gate.

---

## Section 10: Funder View (Cross-Grantee)

The funder's view aggregates across all active grantees in a round. The funder can see the full portfolio without navigating to each grantee individually.

The funder view displays for each active grantee: the grantee's name and identifier, their primary indicator and current progress (or completion status for build-obligation grantees), the next reporting or gate deadline, and any flags (overdue reports, gate submissions pending review, conditions with pending or failed verification status).

### Cross-grantee comparison for common indicators

For rounds with configured round-level common indicators, the funder view shows a cross-grantee comparison table for those indicators. Applicant-specified indicators, even when they share a name, may have different operational definitions and are not compared in the cross-grantee table. The Dashboard must not aggregate or compare applicant-specified indicators across grantees.

### Funder permissions

Funders can view all grantee data, mark conditions as verified (subject to the verification role restriction), approve methodology change notices, approve committee-level amendments, and verify gate submissions where the funder is the named verification contact.

Funders cannot modify submitted attestations. If the funder believes a submitted value is erroneous, the correction path is the correction attestation process, which the grantee submits. This division maintains the integrity of the attestation record: the grantee is the signatory, and only the grantee can sign a correction.

---

## Section 11: Data Model

The following data model specifies the core entities. Implementers may extend these entities with additional fields but must not remove or rename the fields specified here, as they establish the interoperability layer for cross-funder portability.

```
Round {
  round_id:            string (unique identifier)
  funder_id:           string
  round_schema:        reference (published round schema document, immutable once published)
  accountability_mode: enum (build | change | retroactive)
  gate_configuration:  object {
    entry_specification: {
      evidence_scope:    enum (output | usage | outcome | impact),
      evidence_strength: enum (self_report | third_party_verifiable | independent_review |
                         independent_evaluation),
      infrastructure_declaration: text or null
    },
    progress_verification_gates: array of {
      tranche_number:    integer,
      evidence_scope:    enum,
      evidence_strength: enum,
      infrastructure_declaration: text or null
    },
    completion_verification: {
      evidence_scope:    enum,
      evidence_strength: enum,
      infrastructure_declaration: text or null
    },
    continuation_specification: {
      configured: boolean,
      evidence_scope:    enum or null,
      evidence_strength: enum or null,
      infrastructure_declaration: text or null
    }
  }
  configuration:       object (reporting frequency, grace period, common indicators if any,
                       optional dimensions activated)
  open_date:           date
  close_date:          date
}

Obligation_Registry {
  registry_id:              string (unique identifier)
  round_id:                 string (foreign key to Round)
  grantee_id:               string
  accountability_mode:      enum (build | change | retroactive)
  indicator_commitments:    array of Indicator_Commitment
  conditions:               array of Condition
  reporting_schedule:       array of {period_start, period_end, deadline, tranche_id or null}
  disbursement_structure:   array of {tranche_id, amount, depends_on_period or null,
                            depends_on_gate: gate_submission_id or null,
                            depends_on_conditions: array of condition_id}
  concurrent_funding_snapshot: object (as submitted at award)
  created_at:               timestamp (award timestamp)
}

Indicator_Commitment {
  commitment_id:              string (unique identifier)
  registry_id:                string (foreign key to Obligation_Registry)
  indicator_name:             string
  rationale:                  text
  measurement_form: {
    description:              text (plain-language description of measurement form)
    source_type:              enum (on_chain_verifiable | off_chain_verifiable |
                              qualitative_narrative)
    form_type:                enum (quantitative | ordinal | binary | qualitative)
    aggregation_type:         enum (cumulative | non_cumulative | not_applicable)
  }
  operational_definition:     text (inclusion criteria, exclusion criteria,
                              unit of analysis, edge case determination)
  methodology:                text (construction and aggregation methodology in full)
  cumulative:                 boolean or null (null for binary completion criteria)
  disaggregation_categories:  array of string
  data_source:                text (named source and collection method)
  data_cost_attestation:      text
  baseline:                   {value, unit, source, date} or null (null for build-obligation
                              where coordinating party engagement dimension not activated)
  target: {
    build_accountability:     {completion_criteria: array of string,
                              verifying_party: string or null} or null
    change_accountability:    {value, unit, type: cumulative_total or target_status} or null
    retroactive_commitment:   {description: text, completion_criteria: array of string} or null
  }
}

Gate_Submission {
  submission_id:          string (unique identifier)
  registry_id:            string (foreign key to Obligation_Registry)
  gate_type:              enum (progress_verification | completion_verification |
                          continuation_specification)
  tranche_number:         integer or null (for progress_verification gates)
  submission_timestamp:   timestamp
  evidence_scope:         enum (output | usage | outcome | impact)
  evidence_package: {
    description:          text
    public_links:         array of string
    completion_criteria_status: array of {criterion: string, status: enum (met | pending | not_met)}
    or null (for change-obligation submissions)
    indicator_values:     array of {indicator_id: string, value, data_source_reference: text}
    or null (for build-obligation submissions)
  }
  verification_status:    enum (pending | verified | failed | waived)
  verification_contact:   string or null
  verification_timestamp: timestamp or null
  verification_notes:     text or null
  grantee_signature:      string
}

Report {
  report_id:              string (unique identifier)
  registry_id:            string (foreign key to Obligation_Registry)
  period_start:           date
  period_end:             date
  indicator_submissions:  array of Indicator_Submission
  attestation_text:       text (standard declaration text, Dashboard-generated)
  signature:              string (cryptographic signature or named signatory)
  submission_timestamp:   timestamp
  status:                 enum (submitted | overdue | flagged | accepted)
}

Indicator_Submission {
  submission_id:        string (unique identifier)
  report_id:            string (foreign key to Report)
  commitment_id:        string (foreign key to Indicator_Commitment)
  value:                number or string (typed per measurement_form in Indicator_Commitment)
  disaggregated_values: object (keys: disaggregation category names,
                        values: reported amounts or statuses)
  methodology_note:     text or null (required when reliability check triggers)
  source_reference:     text (specific reference to the data source used this period)
}

Condition {
  condition_id:            string (unique identifier)
  registry_id:             string (foreign key to Obligation_Registry)
  requirement:             text (verbatim from committee recommendation)
  verification_method:     text
  verification_contact:    string or null
  status:                  enum (pending | verified | failed)
  verification_timestamp:  timestamp or null
  verifier_id:             string or null
  notes:                   text or null
}

Amendment {
  amendment_id:                  string (unique identifier)
  registry_id:                   string (foreign key to Obligation_Registry)
  field_modified:                string (dot-path to modified field)
  prior_value:                   text or object
  new_value:                     text or object
  reason:                        text
  committee_approval_timestamp:  timestamp
  approved_by:                   string
}

Onchain_Attestation {
  attestation_id:           string (unique identifier)
  round_id:                 string
  grantee_id:               string
  reporting_period:         {start: date, end: date} or null (null for gate attestations)
  gate_type:                enum or null (null for periodic indicator attestations)
  indicator_id:             string or null
  value:                    number or string or null
  gate_evidence_reference:  string or null (content-addressed reference for gate attestations)
  measurement_form_hash:    string (cryptographic hash of measurement form description
                            and classification at commitment time)
  methodology_hash:         string
  data_source_id:           string
  timestamp:                timestamp
  grantee_signature:        string

  // Correction attestation fields (null if not a correction)
  corrects_attestation_id:  string or null
  corrected_value:          number or string or null
  correction_reason:        text or null
}
```

---

## Section 12: Forward-Looking Considerations

### Cross-funder portability

The Dashboard is designed for a world where grant obligation records are portable and public. A grantee who receives funding from one funder in one round and applies to another funder in a subsequent cycle can share their Dashboard record as verifiable evidence of prior grant performance. The three-component obligation ledger (round schema, application commitments, periodic and gate attestations) is readable by any party without requiring access to the original funder's internal systems. This portability requires that the data model fields in Section 11 remain stable across funders and versions.

### Privacy-sensitive accommodation

For grantees who invoked the privacy-sensitive accommodation in their applications, the onchain publication protocol supports selective disclosure. Under selective disclosure, the grantee publishes that a report or gate submission was attested without publishing the indicator values themselves. The value field is replaced with a commitment (a cryptographic hash of the value). The methodology hash and grantee signature are still published. The funder retains access to the full indicator values through the Dashboard's private funder view. Selective disclosure is available only to grantees whose obligation registries record it.

### Connection to the Reviewers Dashboard

The CROSS Reviewers Dashboard (specification forthcoming) is a stage-gated review interface that operates during the evaluation stage of a round. The Grantee Dashboard and the Reviewers Dashboard share data in one direction: completed evaluation records and rubric scores from the Reviewers Dashboard feed into the funder's decision record, which in turn informs what conditions and gate requirements appear in the obligation registry when an award is made. The connection point is the obligation registry creation step: the conditions recorded at award time come from the Reviewers Dashboard's "Fund with conditions" findings.

---

## Appendix: Relationship to CROSS Standard Parts

Section 2 (Obligation Registry) implements CROSS Part V (all indicator fields), Part VI (concurrent funding disclosure), and Part VII (conflict of interest documentation at award time).

Section 3 (Indicator Progress Tracking) implements CROSS Part III (obligation modes) and Part VIII (reliability standard for the methodology consistency check).

Section 4 (Disaggregation Ratchet Handling) implements the disaggregation ratchet in Part V.

Section 5 (Reporting Schedule and Timeline) implements the reporting frequency as set in the round specification per Part IX.

Section 6 (Gate Evidence Submission Tracking) implements CROSS Part IV (gate architecture: progress verification gates and completion verification gate). The completion gate's public accessibility requirement for build-obligation rounds is a CROSS Part IV minimum that the Dashboard enforces at the disbursement interface.

Section 7 (Disbursement Condition Tracking) implements CROSS Part II (institutional capacity dimension, disbursement conditions tier) and the "Fund with conditions" recommendation type from the assessment rubric.

Section 8 (Attestation Format and Signing) implements CROSS Part VIII (reliability, validity, integrity) and the methodology consistency requirements throughout Part V.

Section 9 (Onchain Publication Protocol) implements CROSS Part IX (the Grantee Dashboard produces structured attestations suitable for onchain publication).

Section 10 (Funder View) implements CROSS Part IX and the round-level common indicators option noted in the CROSS standard Appendix.

Section 11 (Data Model) provides the implementation encoding for all of the above.

Section 12 (Forward-Looking Considerations) implements the privacy and data sensitivity dimension from CROSS Part II and the cross-funder portability intent stated in Part IX.
