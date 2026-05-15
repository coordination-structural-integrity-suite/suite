---
title: CROSS Reviewers Dashboard
version: 0.1.0
date: 2026-05-14
license: CC0
status: First draft. Implementation specification inheriting from CROSS-common-reporting-outcome-standards-schema-0_2_0.md.
related_documents:
  - standards/CROSS-common-reporting-outcome-standards-schema-0_2_0.md
  - standards/CROSS-grant-configurator-0_2_0.md
  - standards/CROSS-grantee-dashboard-0_2_0.md
  - standards/CROSS-common-reporting-outcome-standards-schema-rubric-0_2_0.md
---

# CROSS Reviewers Dashboard

Version 0.1.0 | 2026-05-14 | CC0

---

## Section 1: Purpose and Scope

The CROSS Reviewers Dashboard is the stage-gated interface through which grant evaluators assess applications against the round's published obligation standard. It is the fourth operational tool in the CROSS implementation architecture, alongside the Grant Configurator, the Grantee Dashboard, and the CROSS skill.

The Reviewers Dashboard serves a distinct set of functions that neither the Grant Configurator nor the Grantee Dashboard can perform. The Configurator defines the round's obligation schema. The Grantee Dashboard tracks post-award performance. The Reviewers Dashboard governs the evaluation stage: the period between applications closing and funding decisions being made. During this stage, the Reviewers Dashboard enforces conflict of interest declarations as access controls, maintains assessment isolation between reviewers, loads the correct rubric for the round's configured obligation mode, and provides AI-assisted evaluation support.

The Reviewers Dashboard is active only during the evaluation stage. Before applications close, it has no function. After funding decisions are made and communicated, it closes again. This boundary is enforced structurally, not by convention: the Dashboard's application content access is gated to the evaluation window as configured in the Grant Configurator, and no reviewer including program administrators can access application content outside that window through the Dashboard interface.

The primary output of the Reviewers Dashboard is the evaluation record: a structured set of per-application assessments that the funder uses to make funding decisions. Each evaluation record contains the reviewer's scored rubric assessment, conformance check findings, and recommendation, alongside the AI assistance outputs that informed it. The evaluation record is the obligation instrument for the review process itself.

---

## Section 2: Evaluation Stage Gating

The evaluation stage opens when the program administrator sets the stage to active in the Grant Configurator or in the Reviewers Dashboard administrative interface. It closes when the program administrator marks it closed, or when the configured evaluation window duration elapses.

While the evaluation stage is open, reviewers with assigned roles can access applications assigned to them, subject to the conflict of interest handling described in Section 3. While the evaluation stage is closed, no reviewer can access application content regardless of their role. This includes lead reviewers and funder administrators: the stage gate is not a role permission; it is a temporal gate that applies universally.

The evaluation window duration and the process for opening and closing the stage are configured in the Grant Configurator (Q1 of the Configurator's question sequence includes the named conflict of interest receiving authority; the Reviewers Dashboard uses the same named authority as the gatekeeper for stage transitions). Funders may configure automated stage opening tied to the round's published close date, or manual stage opening requiring a named administrator action.

The Reviewers Dashboard records the exact timestamp at which the evaluation stage opened and at which it closes. These timestamps become part of the institutional record for the round.

---

## Section 3: Conflict of Interest Handling

Conflict of interest declaration is not a pre-condition the Reviewers Dashboard asks reviewers to confirm at login. It is a gate enforced at the application level: a reviewer who has not submitted a valid conflict of interest declaration for a specific application cannot open that application. The gate operates independently for each reviewer-application pair.

### Declaration gate behavior

When a reviewer attempts to open an application for which they have not submitted a conflict of interest declaration, the Dashboard presents the declaration form (Template 6 from the CROSS templates document) before allowing access to application content. The reviewer must complete the declaration and submit it to the named receiving function before the application opens.

The declaration is application-specific, not round-level. A reviewer who declares no conflicts for Application A and a Tier 2 conflict for Application B cannot open Application B until the Tier 2 conflict has been resolved through the waiver process. The reviewer may continue reviewing Application A while the waiver for Application B is pending.

### Tier 1 named response

If a reviewer's declaration for a specific application indicates a Tier 1 relationship, the Dashboard blocks access to that application for that reviewer permanently for this round. The block is not reversible by the reviewer; only a program administrator can remove a Tier 1 block, and only for the purpose of reassigning the application to a non-conflicted reviewer. The Tier 1 block and the relationship it identified are recorded in the evaluation record for that application.

### Tier 2 named response

If a reviewer's declaration indicates a Tier 2 relationship, the Dashboard blocks access to that application until either: a waiver is approved by the named receiving function and recorded in the Dashboard, or the reviewer elects recusal. The waiver approval is recorded with the approver's identity, the justification submitted, and the timestamp. The waiver approval is accessible to the program administrator and is included in the institutional record for the round.

### Post-participation certification

When a reviewer submits their final assessment for an application, the Dashboard presents the post-participation certification form (Template 8) before the submission is accepted. The reviewer confirms that no new conflicts arose during review and that their pre-review declaration remained accurate. The certification is recorded alongside the assessment.

### Conflict of interest record in the evaluation output

The evaluation record for each application includes a conflict of interest summary: which reviewers declared which relationships, which Tier 1 blocks applied, which Tier 2 waivers were granted, and which post-participation certifications were completed. This summary is part of the institutional record archived at round close (see Section 9).

---

## Section 4: Assessment Isolation

Reviewers cannot see other reviewers' assessments for an application until they have submitted their own assessment for that application. This isolation prevents anchoring effects, where an early reviewer's score or finding influences subsequent reviewers toward conformity rather than independent judgment.

Assessment isolation is enforced at the data access level, not by convention. A reviewer who has submitted their assessment for an application may see other submitted assessments for that application, subject to the role permissions in Section 5. A reviewer who has not yet submitted cannot see any other assessment for that application regardless of role.

The isolation boundary is the submission act. Saving a draft does not count as submission. The reviewer must explicitly submit their assessment before the isolation lifts.

### Lead reviewer aggregation view

Lead reviewers have access to an aggregate view that shows, for each application, which reviewers have submitted and which have not, without revealing the content of submitted assessments to reviewers who have not yet submitted their own. The aggregate view is available to lead reviewers to manage the review process timeline; it does not enable the lead reviewer to see assessment content before submitting their own.

Once a lead reviewer has submitted their own assessment for an application, they gain access to all submitted assessments for that application. This enables the lead reviewer to identify divergences among guest reviewer assessments and initiate the reconciliation process described in Section 6.

### Isolation configuration

Funders may configure perpetual isolation: submitted assessments remain invisible to all reviewers until the program administrator closes the evaluation stage. This configuration is appropriate for programs where full independence is paramount and there is no deliberative process between individual reviewer submission and the final funding decision. Under perpetual isolation, lead reviewers cannot see individual assessment content until the stage closes.

---

## Section 5: Role Differentiation

The Reviewers Dashboard distinguishes three access roles. Roles are assigned by the program administrator in the Grant Configurator or in the administrative interface of the Dashboard before the evaluation stage opens.

**Guest reviewer.** A guest reviewer sees only the applications assigned to them by the program administrator or lead reviewer. They do not see the full applicant list, other reviewers' identities or assignments, or assessment content from other reviewers (subject to the isolation rules in Section 4). Guest reviewers submit conflict of interest declarations, complete AI-assisted evaluation, and submit their assessments. They do not have administrative access to any round-level configuration.

This role is the appropriate configuration for invited external reviewers, community evaluators, or domain experts who are brought in for a specific round with a specific assignment set. The role isolation ensures that their participation does not expose them to the full applicant pool or to deliberative information that would not be appropriate for an outside evaluator.

**Lead reviewer.** A lead reviewer sees all applications in the round and all submitted assessments (subject to isolation rules until they have submitted their own assessment for each application). They may assign applications to guest reviewers, view the conflict of interest summary for any application, and initiate assessment reconciliation when guest reviewer assessments diverge substantially. Lead reviewers have the same access to AI assistance as guest reviewers. They have no administrative access to round configuration.

**Funder administrator.** A funder administrator holds all lead reviewer permissions plus the ability to: open and close the evaluation stage, approve Tier 2 conflict of interest waivers (as the named receiving function), configure guest reviewer and lead reviewer assignments, access the full conflict of interest record for the round, and export the complete evaluation record for institutional archival. Funder administrators may not modify submitted assessments. They may flag an assessment for re-review with a documented reason, which reopens the assessment for the reviewer who submitted it.

---

## Section 6: Rubric Loading and Scoring

When a reviewer opens an application, the Dashboard loads the confirmed rubric block from the published round specification. The rubric was generated, reviewed, and explicitly confirmed by the funder in Q12 of the Grant Configurator before the round opened. It is not re-derived at runtime from the CROSS assessment rubric companion document; the confirmed text in the round specification is the authoritative instrument. The Dashboard presents this confirmed rubric as the structured scoring interface. Any funder additions or round-specific guidance from Q12.2 appear alongside the standard CROSS criteria. Common indicator rubric criteria from Q12.3 appear as additional scored sections following the indicator specification rubric.

### Rubric structure in the Dashboard

The scoring interface presents the rubric in the sequence specified in the assessment rubric document. For each section, the Dashboard provides: the reviewer question from the rubric, the scoring criteria (the 1-4 table), a text field for the reviewer's finding, and the score selector.

For the entry specification gate (Section 2 of the rubric), the Dashboard requires the reviewer to record a gate finding before the scoring fields become active. A gate failure finding closes the scoring fields and routes the review directly to the recommendation section with a Do not fund pre-selection that the reviewer may not override.

For the conformance checks (Section 5 of the rubric), the Dashboard presents each check as a binary pass/fail with a required text field for findings. A conformance check failure produces a Do not fund pre-selection.

### Score entry and validation

The Dashboard validates that all required rubric fields are completed before the submission workflow begins. An incomplete rubric cannot be submitted. Required fields are: gate finding, all scored indicator fields for the primary indicator, all five data quality standard findings, and all three conformance check findings.

Recommendations are drawn only from the three CROSS recommendation categories: Fund, Fund with conditions, or Do not fund. The Dashboard does not permit any other recommendation vocabulary.

For Fund with conditions recommendations: the Dashboard requires at least one condition to be specified before submission is accepted. Each condition must have: a specific description of what must be resolved, a named verification method, and a stated deadline. The Dashboard validates that all three components are present for each condition.

### Assessment reconciliation

When guest reviewer assessments for the same application diverge substantially (defined as a difference of 2 or more points on any scored indicator field, or divergent gate findings, or divergent conformance check findings), the lead reviewer is notified. The lead reviewer may: add their own assessment to the record, initiate a discussion note visible to all reviewers who assessed the application, or escalate to the program administrator.

Reconciliation does not require reviewers to change their submitted assessments. The institutional record retains all submitted assessments. The lead reviewer's role is to document the divergence and ensure the final funding decision record acknowledges it, not to enforce consensus.

---

## Section 7: AI Assistance

The Reviewers Dashboard provides AI-assisted evaluation through three layers. The layers are cumulative: Layer 2 builds on Layer 1, and Layer 3 synthesizes both. Each layer produces a discrete output stored alongside the reviewer's assessment in the evaluation record. Layers are invoked sequentially; the reviewer may view each layer's output, supplement or override it, and invoke the next layer.

The AI assistance is a tool for the reviewer, not a substitute for the reviewer. The reviewer's final assessment is the obligation instrument. AI outputs inform it. The reviewer edits, overrides, and supplements AI-generated content before submission. A reviewer who accepts AI outputs without review has not fulfilled their review obligation.

All AI assistance is invoked using the CROSS skill (claude-skills/claude-skill-CROSS-0_2_0.md) as the machine-readable encoding of the standard, combined with the round specification for rubric calibration.

### Layer 1: Submitted evidence verification

Layer 1 checks whether the evidence the applicant submitted with their application matches the claims made in the entry specification. The check covers: does the named data source exist and is it publicly accessible? does the reported baseline value correspond to what the named source shows? for build-obligation applications, is the named deliverable location accessible? for retroactive obligation applications, does the evidence of use cited match independently verifiable records?

This layer is implemented via the evidence verification endpoint (currently at `/api/evidence/verify` in the Octant grant operations dashboard). It returns a structured verification report for each submitted evidence item: verified, verified in substance (with a note on what could not be confirmed), or cannot be verified from any public source (with the reason and what was tried).

The "cannot be verified" output from Layer 1 triggers the extended verification procedure from the document editing guidebook before the finding is recorded as unverifiable: Playwright rendering for JavaScript-dependent pages, direct API query of the data source, on-chain query via named public indexers, and aggregator checks via named third-party data providers.

### Layer 2: Independent investigation

Layer 2 conducts an independent investigation of the applicant's claims against third-party sources, without relying on the materials the applicant submitted. It is the equivalent of the manual evaluation sessions conducted for Epoch 12 evaluations, whose format and depth serve as the calibration baseline for this layer.

Layer 2 investigates the following categories for each applicant:

**Repository activity.** For applicants claiming software or protocol development: GitHub repository commit history, contributor count, open issues count and trend, recent pull request activity, code quality signals, and release history. The investigation notes the date of the last commit relative to the application submission date.

**Package and deployment records.** For applicants with published libraries or deployed contracts: npm download counts and trend (for JavaScript libraries), deployment verification on named chains via public block explorers, contract interaction counts, and unique address counts from named indexers.

**On-chain usage data.** For applicants making on-chain usage claims: independent query of the claimed contract addresses or protocol addresses from named public blockchain data sources. Comparison against the applicant's stated baseline and target.

**Prior grants and funding history.** Search across known grant history databases (Gitcoin grants data, KarmaGAP, on-chain treasury records where accessible) for prior grants to this applicant or this project. Cross-reference against the applicant's concurrent funding disclosure to identify any discrepancy. Prior funding history with this program is checked against available evaluation records.

**Adverse signal investigation.** Independent search for adverse signals: prior rejections from comparable programs, published technical criticisms, community dispute records, documented coordinating conflicts, or negative due diligence findings that appear in public sources.

**Claim verification.** For specific quantitative claims made in the application that can be independently verified (user counts, transaction counts, download figures, protocol metrics), Layer 2 queries the named or inferable sources and reports whether the claim is confirmed, confirmed in substance, or cannot be verified from public sources.

The Layer 2 output is a structured investigation report organized by category, using the evaluation format from the Epoch 12 evaluation files as the structural template. Each finding uses the three-value taxonomy: Confirmed, Confirmed in substance (with an explicit statement of what could not be verified), or Cannot be verified from any public source (with reason and what was tried). The taxonomy "Plausible but unverified" is not used; it is a placeholder that must be resolved.

### Layer 3: Draft evaluation

Layer 3 applies the CROSS assessment rubric to the combined findings from Layers 1 and 2 and produces a draft evaluation: per-criterion scores with supporting notes, conformance check findings, and a preliminary recommendation. The draft is pre-populated in the scoring interface described in Section 6.

Layer 3 uses the round specification's obligation mode to select the correct rubric variant. For build-obligation rounds it applies the build-obligation gate and completion criteria assessment. For change-obligation rounds it applies the FROM state gate and the eleven-field indicator specification rubric. For retroactive obligation rounds it applies the program's published contribution assessment rubric.

The draft evaluation is clearly labeled as AI-generated in the scoring interface. The reviewer sees each draft score and note with an indication that it was generated by Layer 3. The reviewer edits, overrides, and supplements the draft before submitting. No draft score or note is submitted as the reviewer's assessment without the reviewer having actively confirmed or modified it.

Layer 3 pre-populates the conflict of interest conformance check as "pending" and requires the reviewer to complete it directly. The AI layer does not assess the reviewer's own conflict of interest status; that is the reviewer's declaration, not a matter for AI inference.

---

## Section 8: Reviewer Assessment Submission

When a reviewer has completed their scoring interface (with or without AI assistance) and is ready to submit, the Dashboard presents the submission workflow.

The submission workflow requires in sequence: confirmation that the conflict of interest declaration was submitted to the named receiving function before review began, scoring completion validation (all required rubric fields completed), post-participation certification (Template 8), and final submission.

Once submitted, the assessment is locked for that reviewer. The reviewer cannot edit a submitted assessment. If the program administrator flags an assessment for re-review, the assessment is unlocked for the reviewer who submitted it and they may revise it, with the revision recorded as an amendment to the assessment record.

The submitted assessment record contains: the reviewer's identity (role, not necessarily name, depending on the program's configured anonymization setting), the submission timestamp, the full scored rubric with all findings and notes, the recommendation (Fund, Fund with conditions, or Do not fund), the conditions list if applicable, the conformance check findings, the conflict of interest summary for this reviewer-application pair, the Layer 1, 2, and 3 AI outputs as they existed at submission time, and the post-participation certification.

---

## Section 9: Storage and Institutional Record

### Storage architecture

All evaluation records are stored in Supabase. The current architecture uses Supabase as the primary storage for evaluation data, AI assistance outputs, conflict of interest records, and assessment submissions. This architecture is noted as the current implementation; the data model in Section 10 documents the schema for future migration to alternative storage if the program requirements change.

The following data is stored per evaluation session:

- The complete evaluation record for each reviewer-application pair (rubric scores, findings, recommendation, conditions)
- The Layer 1 evidence verification output for each application
- The Layer 2 independent investigation report for each application
- The Layer 3 draft evaluation as it existed when the reviewer submitted their final assessment
- The reviewer's edits to the Layer 3 draft (stored as a diff between the draft and the submitted assessment)
- The conflict of interest declaration and post-participation certification for each reviewer-application pair
- The evaluation stage open and close timestamps for the round

### Archival to program record

Completed evaluation records are archived as part of the program's institutional record. The archival step occurs when the evaluation stage closes and the program administrator marks the round's evaluation records as ready.

The archival writes each evaluation record in a structured format organized by round, containing the investigation summary, rubric assessment, and recommendation. The archived record does not include raw AI outputs; it contains the reviewer's final assessment as submitted, with a metadata note indicating whether AI assistance was used and at which layers.

The sync record includes the Layer 2 investigation as a separate linked document in the vault, preserving the research depth for institutional memory purposes. Future reviewers evaluating the same project in a subsequent round can retrieve the prior investigation record from the vault as context, rather than re-investigating sources that have already been checked.

---

## Section 10: Data Model

```
Evaluation_Record {
  evaluation_id:          string (unique identifier)
  round_id:               string (foreign key to Round in Grantee Dashboard data model)
  application_id:         string (identifier of the application being evaluated)
  reviewer_id:            string
  reviewer_role:          enum (guest_reviewer | lead_reviewer | funder_administrator)
  evaluation_stage_id:    string (foreign key to the evaluation stage session)
  status:                 enum (in_progress | submitted | flagged_for_review)
  submission_timestamp:   timestamp or null

  // Conflict of interest record
  coi_declaration: {
    submitted_at:         timestamp
    submitted_to:         string (named receiving function)
    tier_1_blocks:        array of {relationship_type: string, application_id: string}
    tier_2_disclosures:   array of {relationship_type: string, waiver_granted: boolean,
                          waiver_approver: string or null, waiver_timestamp: timestamp or null}
  }
  post_participation_certification: {
    completed_at:         timestamp or null
    no_new_conflicts:     boolean or null
  }

  // AI assistance outputs (stored at submission time)
  layer_1_output: {
    generated_at:         timestamp
    evidence_items:       array of {claim: string, status: enum (confirmed | confirmed_in_substance |
                          cannot_verify), notes: text}
  } or null

  layer_2_output: {
    generated_at:         timestamp
    repository_activity:  text
    package_deployment:   text
    on_chain_usage:       text
    prior_grants:         text
    adverse_signals:      text
    claim_verification:   array of {claim: string, status: enum (confirmed | confirmed_in_substance |
                          cannot_verify), notes: text}
    full_report:          text (structured markdown in Epoch 12 evaluation format)
  } or null

  layer_3_draft: {
    generated_at:         timestamp
    draft_scores:         object (keyed by rubric field, values: {score: integer, note: text})
    draft_recommendation: enum (fund | fund_with_conditions | do_not_fund)
    draft_conditions:     array of {description: text, verification_method: text, deadline: date}
  } or null

  // Reviewer's final assessment
  rubric_assessment: {
    obligation_mode:      enum (build | change | retroactive)
    gate_finding: {
      passed:             boolean
      finding_text:       text
    }
    indicator_scores:     array of {field: string, score: integer, finding: text}
    data_quality_standards: array of {standard: string,
                          status: enum (pass | conditional | fail), finding: text}
    conformance_checks:   array of {check: string, status: enum (pass | fail | signal_documented),
                          finding: text}
    recommendation:       enum (fund | fund_with_conditions | do_not_fund)
    conditions:           array of {description: text, verification_method: text,
                          deadline: date} or null
    primary_reason:       text (single most important reason for the recommendation)
  } or null

  // Diff between Layer 3 draft and submitted assessment (null if no AI assistance used)
  layer_3_edits: {
    score_overrides:      array of {field: string, draft_score: integer, submitted_score: integer}
    note_edits:           array of {field: string, had_edit: boolean}
    recommendation_change: boolean
  } or null
}

Evaluation_Stage {
  stage_id:               string (unique identifier)
  round_id:               string
  opened_at:              timestamp
  closed_at:              timestamp or null
  opened_by:              string (administrator identity)
  closed_by:              string or null
  reviewer_assignments:   array of {reviewer_id: string, role: enum, application_ids: array of string}
}

Vault_Sync_Record {
  sync_id:                string (unique identifier)
  round_id:               string
  synced_at:              timestamp
  synced_by:              string (administrator identity)
  evaluation_ids:         array of string (evaluation records included in this sync)
  vault_paths:            array of {evaluation_id: string, vault_path: string}
  investigation_paths:    array of {application_id: string, vault_path: string}
}
```

---

## Section 11: Forward-Looking Considerations

**Integration with the Grantee Dashboard.** The evaluation record produced by the Reviewers Dashboard is the source of the obligation registry contents in the Grantee Dashboard: conditions recorded in a "Fund with conditions" recommendation become the conditions tracked in the Grantee Dashboard's disbursement condition tracking. The connection between the two dashboards is the obligation registry creation step. Conditions must be exported from the Reviewers Dashboard in the format expected by the Grantee Dashboard's obligation registry schema.

**Longitudinal investigation record.** A program that maintains an investigation archive accumulates Layer 2 records across rounds. A project evaluated in multiple rounds has a growing investigation history: prior grant usage, prior repository activity snapshots, prior adverse signal checks. Future Layer 2 investigations for the same project can retrieve this history as context, making each successive evaluation more efficient and the investigation more longitudinally coherent. This is one of the concrete expressions of the funder maturation tracking capability noted in the CROSS standard's purpose section.

**Supabase migration path.** The current Supabase storage architecture is documented as the present implementation, not the permanent one. The data model in Section 10 is designed to be portable: field names and types are specified independently of Supabase's internal representation, and the archival mechanism provides a durable copy in the program record. A migration to alternative storage requires only implementing the same data model in the target store and updating the sync logic; no structural changes to the evaluation workflow are required.

**AI assistance maturation.** The three-layer AI assistance model is specified at a level of capability available at the time of this document. Layer 2 in particular is calibrated to the current manual investigation practice for Epoch 12 evaluations. As investigation tooling improves (deeper on-chain data access, improved cross-program grant history databases, better adverse signal corpora), the Layer 2 specification should be updated to reflect the expanded investigation capability. The calibration baseline is always the most recent cycle of completed manual evaluations available in the program record.
