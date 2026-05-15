---
title: CROSS Skill
version: 0.2.0
date: 2026-05-14
status: Working skill encoding the CROSS Common Reporting Outcome Standards Schema version 0.2.0 for AI-assisted grant evaluation and configuration.
related_documents:
  - standards/CROSS-common-reporting-outcome-standards-schema-0_2_0.md
  - standards/CROSS-grant-configurator-0_2_0.md
  - standards/CROSS-grantee-dashboard-0_2_0.md
  - standards/CROSS-reviewers-dashboard-0_1_0.md
  - standards/CROSS-runbooks-0_1_0.md
---

# CROSS Skill

Invoke this skill before evaluating any grant application against CROSS requirements, before running the Grant Configurator sequence for a funder, or before assessing any indicator specification, conflict of interest relationship, gate submission, or data quality claim. This is a procedural encoding of the Common Reporting Outcome Standards Schema (CROSS) version 0.2.0 that enables consistent application across obligation modes, evaluation contexts, and gate types. It is structured so a partial task ("evaluate this FROM state claim" or "assess this gate evidence package") can be received and completed correctly.

## Runtime Sequence

When given an evaluation task, identify which operation is requested and run the corresponding procedure in full:

1. **Entry specification gate assessment.** Run when given an application text. Determine the round's declared obligation mode first; then run the correct mode procedure. See Part III below.

2. **FROM state classification (change obligation).** Run as part of the change-obligation gate assessment, or independently when asked to classify a specific claim. Returns one of five canonical classifications. See Part III, Section B below.

3. **Deliverable specification assessment (build obligation).** Run when evaluating whether an application's deliverable specification is falsifiable with independently verifiable completion criteria. See Part III, Section A below.

4. **Retroactive contribution assessment.** Run when evaluating whether a retroactive application's prior contribution evidence meets the program's published threshold criteria. See Part III, Section C below.

5. **Indicator field assessment.** Run when evaluating a single indicator specification or a full indicator set. Applies the 11-field checklist and field clustering rules. See Part IV below.

6. **Gate evidence assessment.** Run when evaluating a progress verification or completion verification gate submission. Applies the evidence scope and evidence strength requirements from the round specification. See Part X below.

7. **Conflict of interest tier classification.** Run when given a description of a relationship between a reviewer and an applicant, or between applicants and committee members. See Part VI below.

8. **Data quality standards assessment.** Run when evaluating a reported indicator claim or a proposed measurement methodology. See Part V below.

9. **Grant Configurator sequence.** Run when a funder wants to generate a round specification from their criteria. See Part VII below.

10. **Obligation dimension activation.** Run when given a set of funder criteria or a specific application profile to determine which of the 11 dimensions are active. See Part II below.

11. **Recommendation generation.** Run after completing a gate assessment and dimension evaluation. Returns one of three canonical recommendation terms. See Part VIII below.

12. **Privacy-sensitive accommodation assessment.** Run when an applicant claims a privacy-sensitive accommodation. See Part IX below.

---

## Part I: CROSS Purpose and Scope

CROSS specifies what funded interventions are obligated to produce. It provides grants ecosystems with a portable obligation schema that accommodates three distinct obligation modes, calibrates evidentiary pressure to program context, and generates structured reporting data comparable across funders, rounds, and grantees.

CROSS is not a process standard. It does not specify how rounds are structured, how funds are distributed, or how round administration decisions are made. CROSS specifies the content of obligation: what applicants must demonstrate, what funders must evaluate, and what grantees must report.

**Suite standard references.** CROSS inherits requirements from four companion standards. When evaluating conformance, apply these inherited requirements:

- Adverse-Signal Engagement Principle Core Standard: applicants must surface adverse signals (prior rejections from similar programs, contradictory technical findings, negative due diligence from other funders). Reviewers must not suppress adverse signals found during evaluation.
- Information Asymmetry Classification Standard: undisclosed concurrent funding is an omission asymmetry. The concurrent funding disclosure requirement instantiates this standard's omission class in the grant application context.
- Precision-First Design Standard: the double-negation invariant applies. Documentation requirements must not be so light that obligation is absent, and must not be so heavy that legitimate small-team applicants are excluded.
- Coordination Scaling Standard: calibrates the rigor tier. Determined by scale indicators (funding amount, population claim scope), not by gate passage alone.

The Regenerative Obligation Standard and CROSS are structurally paired but independent. Regenerative Obligation Standard addresses direction; CROSS addresses destination. Run both evaluations independently when both apply; do not merge them.

Frame Language was the conceptual development tool for CROSS. It is not a formal dependency. The diagnostic categories D1 and D2 from Frame Language appear in Part III as shorthand for change-obligation gate failure types; they are not required vocabulary outside that context.

---

## Part II: Independent Obligation Dimensions

CROSS specifies 11 independent obligation dimensions. Each dimension has its own triggering logic. Dimensions do not scale together.

**Procedure for dimension activation:** For each dimension, apply the trigger test independently. If the trigger condition is met, that dimension is active regardless of other dimensions.

### Dimension 1: Outcome Documentation Rigor

**Trigger:** Funding amount above a round-level threshold OR public impact claim at a scale above the Coordination Scaling Standard minimum.

**Active requirements:** Indicator sourcing, baseline documentation, and (at Standard scale) theory of change formalization. Rigor level scales with the Coordination Scaling Standard tier.

### Dimension 2: Institutional Capacity

**Trigger:** The scope of the proposed work is materially larger than the applying organization's demonstrated track record.

**Active requirements:** Capacity assessment. Result calibrates disbursement conditions tier; it is not a disqualifier.

### Dimension 3: Conflict of Interest

**Trigger:** Any relationship exists between a decision-maker and an applicant, or between an applicant and a committee member.

**Active requirements:** Conflict of interest classification into the correct tier. See Part VI.

### Dimension 4: Concurrent Funding Disclosure

**Trigger:** Any grant, investment, or revenue source related to the scope of the application in the prior 24 months. For retroactive rounds: also includes any prior award for the same or overlapping contribution.

**Active requirements:** Disclosure of all related sources. Required fields: source name, source type, approximate amount, relationship to scope, ongoing obligations, governance rights.

**Critical rule:** Non-disclosure is a disqualifier. Disclosure does not disqualify.

### Dimension 5: Adverse Signal Disclosure

**Trigger:** Any adverse signal exists relating to the application or applicant.

**Active requirements:** Applicant must surface all adverse signals. Reviewers must not suppress adverse signals found during evaluation.

### Dimension 6: Open Source and Intellectual Property

**Trigger:** The funded work produces code, data, research, or other artifacts, AND the public goods claim rests on open access to those artifacts.

**Active requirements:** Outputs must be demonstrably open at the time of reporting, not only at application time.

### Dimension 7: Coordinating-Party Engagement and Beneficiary Validation

**Trigger:** The application claims to address a problem experienced by a defined population (change obligation) OR the deliverable addresses a named external need (build obligation, where activated by funder configuration).

**Active requirements (change obligation):** The claimed FROM state must be validated by parties outside the applicant's control. Applicants must name existing alternatives and explain why they do not serve the stated population.

**Active requirements (build obligation, if activated):** At least one named party outside the applicant's organization has confirmed the need for the deliverable.

### Dimension 8: Privacy and Data Sensitivity

**Trigger:** The beneficiary population faces elevated risk from standard outcome measurement.

**Active requirements:** Privacy-preserving measurement methodologies in lieu of standard analytics. Not an exemption from obligation; specifies which mechanisms are appropriate. See Part IX.

### Dimension 9: Environmental and Social Impact (Optional)

**Trigger:** Activated by funder configuration.

**Active requirements:** A/B/C classification under International Finance Corporation Performance Standards derived structure. Class A: full impact assessment required. Class B: targeted assessment. Class C: screening declaration.

### Dimension 10: Gender Equity (Optional)

**Trigger:** Activated by funder configuration.

**Active requirements:** Gender-disaggregated outcome reporting for all population-level impact indicators.

### Dimension 11: Procurement Integrity (Optional)

**Trigger:** Activated by funder configuration AND sub-contracting or sub-granting exceeds 20% of the total award.

**Active requirements:** Sub-contractor disclosure. See field clustering rules in Part IV.

---

## Part III: Entry Specification Gate

The entry specification gate is a pre-criterion that operates before any rigor-tier assessment begins. It is binary and non-negotiable.

**First step before any gate assessment:** Confirm the declared obligation mode from the round specification. The mode determines which gate section applies. Do not apply change-obligation gate criteria to a build-obligation application, and do not apply build-obligation gate criteria to a change-obligation application. Misapplying the gate is a reviewer error, not an applicant failure.

---

### Section A: Build Obligation Entry Gate

**The gate question:** Can the applicant name a falsifiable deliverable with independently verifiable completion criteria?

**Pass criteria:** A named artifact, product, or documented output, with completion criteria specific enough that a reviewer who did not commission the work could determine whether they are met, from publicly accessible evidence without contacting the applicant.

**Fail criteria (Direction specification without deliverable):** The application describes a goal, vision, or direction but does not name a specific deliverable. Example: "making DeFi more transparent" is a direction. "A reporting module producing a human-readable fee summary for any ERC-4626 vault, published as an open-source library, with a deployed instance on Ethereum mainnet and a documented application programming interface" is a deliverable. The difference is testability: the first cannot be verified or falsified; the second can.

**Fail criteria (Underspecified completion criteria):** A deliverable is named but the completion criteria are too vague for independent verification. "A working prototype" names a form but not a standard. Completion criteria must specify what done means, not just what will be built.

**Critical rule:** The Theory of Build is not a failure mode in build-obligation rounds. An application that describes what it will build, with falsifiable criteria, is correct and complete for this mode. Do not import change-obligation gate logic into a build-obligation assessment.

**Gate finding options:**

Gate passes: "Entry specification gate passes: applicant names [deliverable] with completion criteria: [list criteria], independently verifiable by [named method]."

Gate fails: "Entry specification gate fails: [describe what was offered instead of a falsifiable deliverable or verifiable criteria]. Failure type: direction specification without deliverable / underspecified completion criteria."

---

### Section B: Change Obligation Entry Gate

**The gate question:** Can the applicant name the FROM state as a specific measurable condition in a defined population?

**Pass criteria:** A specific condition (not a category) in a named population with a named, independently accessible source.

**Fail criteria:** A category, a values aspiration, or a generic claim.

**Application timing is not the diagnostic.** A team that built something before a grant opportunity appeared is not exhibiting a gate failure if they can name the specific FROM state they addressed.

### FROM State Classification

Apply one of five canonical classifications:

**Specific pass:** The FROM state names a condition (not a category), a named population, and a named, independently accessible source. Gate passes. Proceed to rigor tier.

**Specific with minor gap:** The FROM state is specific and names a population, but the source is absent or not independently accessible. Gate conditionally passes; require source documentation before proceeding.

**D1 failure (canonical vocabulary without structural grounding):** The FROM state uses technically correct vocabulary but does not name a measurable condition. Example: "lack of developer tooling in the ecosystem" uses the right field but names a category without a measurable condition or named source. D1 applications can produce technically coherent responses when asked for more information; the underlying diagnosis is absent. Gate fails. These applications have diagnostic work to do; communicate the failure at the rigor tier level.

**D2 failure (values aspiration without conditions):** The FROM state is a values or mission statement, not a diagnosis. When asked to specify the FROM state, D2 applications produce more values language because no diagnosis was performed. Gate fails. These applications have not yet performed diagnostic work; communicate the gate failure clearly.

**Insufficient information:** The application does not contain enough text to assess the FROM state. Return this classification with a list of what would need to be present to run the assessment.

### Rigor Tier (post-gate)

Rigor tier only runs after the gate passes. Assigns a tier calibrated by the Coordination Scaling Standard:

- Tier 1 (minimal): small funding, narrow scope, specific diagnosis. Indicator sourcing and baseline required; full theory of change formalization not required.
- Tier 2 (standard): mid-range funding, regional or protocol-level impact claims. Full indicator set, sourced baseline, theory of change narrative required.
- Tier 3 (full institutional): large funding, broad population impact, complex multi-year programs. Full indicator set, sourced baseline, formal theory of change, organizational capacity documentation, audit trail required.

Default if no Grant Configurator has been run: assign Tier 2 and note that a Configurator run would allow accurate calibration.

---

### Section C: Retroactive Obligation Entry Gate

**The gate question:** Does the applicant present evidence of prior contribution meeting the program's published threshold criteria?

**What must be present:** (1) A description of what contribution was produced; (2) the period during which it was produced; (3) evidence of who is using or has benefited from it, accessible from sources outside the applicant's control; (4) concurrent funding disclosure covering any prior awards for the same or overlapping contribution.

**Pass criteria:** All four elements present with at least one independently accessible source of evidence for contribution and at least one independently accessible source for use.

**Fail criteria:** Any of the four elements absent. Contribution evidence that consists entirely of applicant self-assertion without any independent source. Use evidence that is not independently accessible.

**Important:** In retroactive rounds, the CROSS indicator specification rubric (Part IV) applies only if the program has configured indicator-based forward reporting. If no indicator specification is required, proceed from this gate to conformance checks and recommendation. The program's published assessment rubric governs substantive scoring; this skill does not replace it.

**Gate finding options:**

Gate passes: "Entry specification gate passes: applicant presents contribution evidence of [type] from [period], with independent sources confirming [contribution] and [use]."

Gate fails: "Entry specification gate fails: [describe which element is absent: contribution description, period, independent contribution evidence, independent use evidence, or prior award disclosure]."

---

## Part IV: Indicator Field Assessment

CROSS requires applicants to self-specify their outcome indicators. Assess each of the 11 fields for every indicator submitted. Report findings per field, then apply field clustering rules.

### Field 1: Indicator Name

**Pass:** Concise, descriptive, and unique within the indicator set.

**Flag:** Generic, duplicative, or absent.

### Field 2: Rationale for Indicator

**Mandatory. No waiver.** An indicator set with no rationale field passes no other field assessment until this one is complete.

**Pass:** Names at least one alternative indicator considered and rejected, with a specific reason. Or names a methodological constraint making this the only feasible indicator.

**Flag:** Absent. Generic justification. Restates what the indicator measures without addressing alternatives.

### Field 3: Measurement Form and Evidence Classification

This field replaced the constrained four-option data type list in version 0.2.0. The applicant names the measurement form in plain language. Reviewers classify it against three axes.

**Axis 1 (source type):** On-chain verifiable (accessible from public blockchain data with a named contract or address) / off-chain verifiable (accessible from public sources outside the blockchain) / qualitative or narrative (requires human evaluator).

**Axis 2 (measurement form):** Quantitative (number, proportion, rate, currency, duration) / ordinal (position on a defined ordered scale) / binary (met or not met against named completion criteria) / qualitative (documented condition or artifact assessed against named criteria).

**Axis 3 (aggregation type):** Cumulative (values sum across reporting periods) / non-cumulative (values describe a status at a point in time; summing across periods is a construction error).

**Pass:** Applicant names the measurement form in plain language with enough specificity to classify against all three axes without inference. The classification is consistent with the construction methodology in Field 5.

**Flag:** Description so general that axis classification cannot be determined. Classification conflicts with Field 5 methodology (described as quantitative but methodology produces only binary output). No description present.

**Mode notes:** For build-obligation indicators, the form is typically binary or qualitative. The description should name what done looks like and how a reviewer would confirm it. For change-obligation indicators, the form is typically quantitative or ordinal; name the unit of measurement and direction of desirable change.

### Field 4: Operational Definition

**Four required sub-fields: all must be present.**

(a) Inclusion criteria: what qualifies as one instance.
(b) Exclusion criteria: what the indicator explicitly does not count.
(c) Unit of analysis: the named entity being counted or assessed.
(d) Edge case determination: at least one example of how an ambiguous instance is resolved.

**Pass:** All four sub-fields present and specific. Exclusion criteria must name at least one specific exclusion, not merely restate the inclusion criteria inverted.

**Flag:** Any sub-field absent. Edge case "will be determined at reporting time" (must be specified in advance).

### Field 5: Construction and Aggregation Methodology

**Pass:** Formula or counting rule stated explicitly (or, for build-obligation indicators, the completion determination process: who verifies, by what method). Partial data handling named. Sub-unit aggregation specified if disaggregated data will be combined.

**Flag:** Formula absent. Partial data handling absent. Sub-unit aggregation absent when disaggregation categories are specified in Field 7.

### Field 6: Cumulative or Non-Cumulative

**Pass:** One of the two states named correctly, consistently with Field 11. For binary build-obligation completion criteria, mark as not applicable and score at standard.

**Flag:** Absent. Inconsistency between Field 6 and Field 11 (cumulative indicator with a point-in-time target, or non-cumulative with a summed target).

### Field 7: Disaggregation Categories

**Ratchet rule:** Disaggregation categories may be added during the grant period. Removing a committed category requires committee approval.

**Pass:** Categories named. If "none committed," explanation provided for why disaggregation is not applicable.

**Flag:** Absent without explanation.

### Field 8: Data Source and Collection Method

**Pass:** Source is named specifically (contract address, named public application programming interface endpoint, named third-party platform, named institutional partner, or named survey instrument). Source is independently accessible. Collection method specifies who collects, when, and how.

For build-obligation indicators: the named artifact location and the named party who will confirm completion criteria are met.

**Flag:** Internal source only with no independent verification path. Source named but not independently accessible. Collection method absent.

### Field 9: Data Cost Estimation

**Pass:** Feasibility attestation present. Cost estimate mapped to a budget line and proportionate to the grant amount. For free sources, confirmation of access is sufficient.

**Flag:** Absent. Cost estimate not mapped to a budget line. Data collection plan requires resources not included in the budget.

### Field 10: Baseline (FROM State)

**Mode-specific assessment.**

For change-obligation indicators: a specific value, measured before the intervention, from a named independently accessible source. Must be consistent with the FROM state named in the gate assessment.

For build-obligation indicators (coordinating-party engagement dimension activated): the documented current absence or inadequacy of the deliverable, with named independent evidence of the gap. Applicant assertion of the gap alone does not satisfy this field.

For build-obligation indicators (coordinating-party engagement dimension not activated): any reasonable plain-language statement of the gap addressed. Advisory only.

For retroactive obligation indicators: the documented state of the prior contribution at the time the award period begins, with named evidence of use.

**Flag (change obligation):** Absent. Aspirational ("we expect baseline data to be available"). Baseline that measures something different from what the indicator tracks. Source absent or not independently accessible.

### Field 11: Target (TO State)

**Mode-specific assessment.**

For change-obligation indicators: same units as baseline. Format matches cumulative/non-cumulative classification (cumulative indicator has a total target; non-cumulative has a target status at grant end).

For build-obligation indicators: completion criteria with enough specificity that an independent reviewer could verify whether they are met. "A working prototype" fails. Named criteria specifying what done looks like and how verification occurs passes.

For retroactive with forward commitment: the named action the awardee commits to, expressed with falsifiable completion criteria.

**Flag:** Target in different units from the baseline. Non-cumulative indicator with a cumulative target. Completion criteria too vague for independent verification. Absent.

### Field Clustering Rules

Apply after completing the 11-field assessment. Each trigger independently activates additional mandatory fields.

**If measurement form = composite/multi-component:** Component indicators, weightings, and aggregation rule become mandatory. A composite without these three is an unverifiable black box.

**If privacy-sensitive accommodation is invoked (Part IX):** Specific harm field and alternative methodology field become mandatory.

**If any venture capital or institutional investment is disclosed in Dimension 4:** Investor name, governance rights, and scope relationship fields become mandatory.

**If Dimension 9 is active:** A/B/C classification is mandatory.

**If progress verification gates are configured:** Milestone or progress specification fields become mandatory for each tranche gate.

**If Dimension 11 is active AND sub-contracting exceeds 20% of the award:** Sub-contractor disclosure fields are mandatory.

**If retroactive round:** Prior award disclosure is mandatory (all prior awards for the same or overlapping contribution).

---

## Part V: Data Quality Standards Assessment

Apply the five data quality standards in order to any indicator claim or proposed measurement methodology. A claim that fails any standard fails the data quality assessment regardless of performance on others.

### Standard 1: Validity

**Operative test:** Remove the applicant from the verification process. Can an independent reviewer confirm that the data collected measures the claimed condition, using only the indicator specification and the named data source?

**Pass:** Logical chain from data to result is explicit and independently verifiable. For build-obligation indicators: the completion criteria have a documented logical chain to the deliverable being what the applicant claims.

**Fail:** Chain requires the applicant's interpretation, cooperation, or access to materials not named in the indicator specification. Macro-level metric claimed as evidence of specific project contribution without documented causal chain.

### Standard 2: Integrity

**Operative test:** Does any evidence for this application's claims originate from a source independent of the applicant?

**Pass:** Named independent verification mechanism present for each material claim.

**Fail:** All evidence is applicant-controlled with no named independent corroboration. For build-obligation: the named verifying party for completion criteria is the applicant themselves.

### Standard 3: Precision

**Operative test:** Is the claimed effect larger than the variance of the measurement method? For build-obligation indicators: are the completion criteria specific enough to distinguish a passing deliverable from a failing one?

**Pass:** Measurement precision is documented and consistent with claimed effect size. Build-obligation criteria distinguish done from not done without ambiguity.

**Fail:** Claimed effect within the instrument's margin of error. Build-obligation criteria accept any output as qualifying ("a working prototype" with no further specification).

### Standard 4: Reliability

**Operative test:** If the methodology changed between periods, is the change documented with a comparability assessment?

**Pass:** Same methodology across periods, or changes documented with comparability assessment. First-time applicants: methodology is specified with enough precision to apply consistently.

**Fail:** Methodology change without documentation. Different definitions of the same indicator used across periods without explanation.

### Standard 5: Timeliness

**Operative test:** Is the data current to the reporting period? Does collection frequency match the decision cycle?

**Pass:** Data collection timing specified, data covers the relevant period, reporting frequency matches the decision cycle.

**Fail:** Data collected in a prior period reported as current. Annual data collection for a quarterly disbursement structure. Gate evidence submitted for a period not covered by the collection methodology.

---

## Part VI: Conflict of Interest Tier Classification

**Governing standard:** The reasonable third-party test. A conflict of interest finding is warranted when a reasonable third party, examining the relationship, would question the objectivity of the reviewer or the independence of the applicant.

**Process requirements:** Pre-review declaration submitted to the named receiving function before any application is opened. Post-review certification after assessment. Bidirectionality: reviewers disclose to applicants, applicants disclose to reviewers and committee.

### Procedure for Tier Classification

Apply the following in order. Stop at the first tier that applies.

**Tier 1 (categorical bar, no waiver):**

- Direct financial interest: equity, revenue share, or token holdings above the materiality threshold (funder-configured default: greater than 1% of token supply or greater than \$5,000 in value at time of review).
- Family relationship: spouse, domestic partner, parent, sibling, child, or household member.
- Prior funded work in the same area from the same funder, where the reviewer's funded work is directly related to the applicant's scope.
- Named on the applicant project's public materials (compensated or not, including advisory roles listed publicly).

**Tier 2 (disclosure required, qualified waiver possible):**

- Employment with the applicant in the past 36 months.
- Co-authorship or collaboration with applicant principals in the past 48 months.
- Mentor or student relationship (no expiration).
- Governance token voting on the applicant's proposals.
- Decentralized autonomous organization co-governance roles involving both parties.
- Honorarium, award, or gift from the applicant in the past 12 months.
- Future employment arrangements under discussion.
- Organizational conflict: reviewer's employer has a material financial relationship with the applicant.

**Tier 3 (disclosure encouraged):**

- Social or community relationships.
- Cross-round interactions in different program areas.
- Informal mentorship without ongoing engagement.

**Web3-specific categories (apply same tier structure):**

- Token holdings above the materiality threshold: Tier 1.
- Token holdings below the materiality threshold: Tier 3.
- Governance token voting on applicant proposals: Tier 2.
- Core contributor or unpaid advisory status listed on public materials: Tier 1.
- Investment from the same named investor: Tier 2.
- Decentralized autonomous organization co-governance roles: Tier 2 or Tier 3 depending on nature.

---

## Part VII: Grant Configurator Question Sequence

Run when a funder wants to generate a round specification. Ask questions in the following order. Compile the output into a round configuration document after all questions are answered.

**Q0: Program type and runbook selection.**

Does this program match any of the standard runbook configurations (Discovery Sprint, Staged Development, Community Allocation with Build Accountability, Retroactive Impact, Graduated Evidence, Institutional Compliance)? If yes, load the runbook as the starting configuration and surface its default gate configuration. If no, proceed through the full sequence.

**Q1: Round identification.**

Round name, funding organization, opening date, closing date, stage number (if multi-stage), named conflict of interest receiving authority.

**Q2: Accountability mode and program structure.**

Which obligation mode: build / change / retroactive / multi-stage with different modes per stage? For retroactive rounds: is a forward commitment requirement configured?

**Q3: Eligibility domain.**

Work type, open source requirement and license, Digital Public Good classification requirement, organizational type restrictions.

**Q4: Funding amount range.**

Minimum and maximum award amounts. Tiered categories if applicable. The Coordination Scaling Standard tier calibration follows from Q4 and Q6 combined.

**Q5: Program-level continuation gate (multi-stage programs only).**

For each stage transition: evidence scope, evidence strength, obligation mode of the next stage, infrastructure declaration if at independent review level or above. Cost-effectiveness consideration active at Stage 2-to-Stage 3 transition?

**Q6: Public impact claim scope.**

Geographic or network scope of expected impact claims. For change obligation: is beneficiary validation required? For build obligation: is the coordinating-party engagement dimension activated?

**Q7: Track record requirement.**

Minimum track record for eligibility. Independent verification requirement. First-time applicant policy.

**Q8: Conflict of interest configuration.**

Tier 2 waiver permitted or all Tier 2 as categorical bars? Token holdings materiality threshold?

**Q9: Optional dimensions.**

Environmental and social impact assessment: activate? Gender equity: activate? Procurement integrity: activate?

**Q10: Round-level common indicators.**

Any indicators required of all applicants? If yes, provide the full measurement form description (not just a data type label), source type, measurement form, aggregation type, operational definition, construction methodology, disaggregation categories, and named data source. Applicants complete baseline and target fields; indicator definition is locked.

**Q11: Round-level gate configuration.**

For each active gate: evidence scope (output / usage / outcome / impact), evidence strength (self-report with documentation / third-party verifiable / independent review / independent evaluation), infrastructure declaration if at independent review level or above. For build-obligation completion gates: confirm that the public accessibility requirement is active (mandatory; cannot be configured out). For retroactive rounds: publish the assessment rubric and name the review panel.

**Q12: Reporting frequency.**

How often must grantees report? Options: monthly, quarterly, semi-annual, milestone-triggered, grant end only.

---

## Part VIII: Recommendation Generation

After completing the gate assessment and all active dimension evaluations, generate a recommendation using only the three canonical terms below.

**Canonical recommendation vocabulary:**

- Fund
- Fund with conditions
- Do not fund

**Recommendation logic:**

**Fund:** Entry specification gate passes. All active mandatory dimensions meet requirements. No categorical conflict of interest bars. No undisclosed concurrent funding. No adverse signal suppression. Data quality standards met or proportionate to the rigor tier. All mode-specific requirements are complete.

**Fund with conditions:** The entry specification gate passes. One or more of the following apply: (a) rigor-tier requirements are partially met, with specific named gaps addressable before disbursement; (b) a Tier 2 conflict of interest relationship requires a waiver decision; (c) a specific indicator field is absent but can be supplied; (d) concurrent funding was disclosed but the scope relationship requires clarification; (e) the disbursement structure should be conditioned on milestone delivery or phased disbursement. Conditions must be specific: not "improve the indicator set" but "supply a named, independently accessible source for Indicator 1 Field 8 before disbursement, verified by [named method]."

**Do not fund:** The entry specification gate fails. Or: a categorical Tier 1 conflict of interest bar is present and cannot be waived. Or: concurrent funding was not disclosed. Or: an adverse signal was suppressed and the suppression is material to the funding decision. Or: the gate passes but no dimension-level requirements are met and the gaps are not addressable through conditions.

**Reasoning structure:** Always accompany the recommendation with structured reasoning.

1. Obligation mode: [build / change / retroactive]
2. Gate finding: [mode-specific gate finding from the canonical vocabulary]
3. Active dimensions: [each active dimension and its finding]
4. Conflict of interest findings: [any classifications and tiers]
5. Data quality finding: [per standard, if indicators were assessed]
6. Recommendation: [Fund / Fund with conditions / Do not fund]
7. If Fund with conditions: named conditions with specific fields and verification methods.

---

## Part IX: Privacy-Sensitive Accommodation

The privacy-sensitive accommodation applies when standard outcome measurement would compromise the safety of the beneficiary population. It is not a general privacy preference. It does not exempt the applicant from obligation.

### Qualification Criteria

**Qualifies:** The beneficiary population faces documented risk from standard data collection methods: populations under state surveillance, populations where participation data could be used for criminalization, populations in active conflict zones where identity disclosure creates physical safety risks.

**Does not qualify:** General organizational preference for privacy. Absence of analytics infrastructure. Discomfort with standard measurement.

### What the Accommodation Requires

When the accommodation applies, two fields are mandatory (clustering rule trigger from Part IV):

1. **Specific harm:** A named, specific harm that standard measurement would create for this population. Not "privacy risk" in general; the specific mechanism (for example: "collection of user location data would create a database that could be subpoenaed under [named legal regime] and used to identify participants in [specific activity]").

2. **Alternative methodology:** A specific alternative measurement approach that provides obligation direction without creating the named harm. Must name an institutional partner or established methodology (for example: Open Observatory of Network Interference-style network measurement, ethics-reviewed study under institutional review board protocols, differential privacy techniques applied to aggregate reporting).

The accommodation substitutes one obligation mechanism for another. It does not reduce obligation. An applicant who invokes it without supplying both mandatory fields has claimed an exemption that does not exist in CROSS.

### Procedure

1. Verify that the qualification criteria are met. If not, standard measurement requirements apply.
2. If qualified, require both mandatory fields before proceeding to indicator assessment.
3. Assess the alternative methodology against the five data quality standards in Part V. The standards apply to the alternative methodology, not to a lower threshold.

---

## Part X: Gate Evidence Assessment

Run this procedure when evaluating a progress verification gate submission or completion verification gate submission against the round's published gate configuration.

### What to confirm before assessing evidence

From the round specification, confirm: (a) the obligation mode; (b) the evidence scope required at this gate (output / usage / outcome / impact); (c) the evidence strength required (self-report with documentation / third-party verifiable / independent review / independent evaluation); and (d) whether an infrastructure declaration exists naming the verification contact.

### Evidence scope assessment

**Output evidence:** Does a specified artifact exist? For build-obligation gates: is the deliverable publicly accessible from the named location? Does it meet the published completion criteria?

**Usage evidence:** Is the deliverable being used by parties outside the applicant's control? Is the evidence independently accessible (on-chain data, named public analytics, named third-party corroboration)?

**Outcome evidence:** Has a measurable change occurred in the specified population, documented against the baseline established at entry? Is the data current to the reporting period?

**Impact evidence:** Is a credible causal link established between the funded work and the measured change, through methodology sufficient to support causal inference?

### Evidence strength assessment

**Self-report with documentation:** Grantee narrative with supporting links, files, or on-chain data references. Reviewed by funder staff against published criteria. Assess: does the narrative reference the correct period? Are supporting links accessible?

**Third-party verifiable:** Evidence accessible to any reviewer with internet access from sources outside the applicant's control. Assess: is each claimed source actually independently accessible without the applicant's cooperation?

**Independent review:** A named party outside the funder-grantee relationship confirms the submitted evidence meets the completion criteria. Assess: was the reviewer named in the infrastructure declaration? Has their confirmation been received and documented?

**Independent evaluation:** A qualified evaluator conducts a structured assessment. Assess: were the evaluator's qualifications appropriate to the evidence scope? Was the process consistent with the published infrastructure declaration?

### Critical rule for completion verification gates

For build-obligation rounds: the gate must confirm that the specified deliverable is publicly accessible before final payment is released. Grantee self-assertion of public accessibility does not satisfy this requirement. A publicly accessible URL must be present and accessible.

### Gate evidence finding options

**Verified:** "Gate verified: evidence submitted meets the published [evidence scope] requirement at [evidence strength] level. [Named verifying party / verification method confirmed]."

**Failed:** "Gate fails: [describe specifically what evidence is missing, what evidence does not meet the published scope or strength requirement, or what completion criteria are not met]."

**Conditional:** "Gate conditionally verified pending: [specific item that must be resolved, named verification method, timeline]."

---

## Canonical Finding Vocabulary

Use these terms consistently. Do not invent alternatives.

**Entry specification gate findings:**

Build obligation: Entry specification gate passes / Entry specification gate fails: direction specification without deliverable / Entry specification gate fails: underspecified completion criteria

Change obligation: Specific pass / Specific with minor gap / D1 failure / D2 failure / Insufficient information

Retroactive obligation: Entry specification gate passes / Entry specification gate fails: contribution description absent / Entry specification gate fails: independent evidence absent / Entry specification gate fails: prior award disclosure absent

**Rigor tier (change obligation post-gate):** Tier 1 / Tier 2 / Tier 3

**Dimension findings:** Active, conformant | Active, non-conformant | Active, conditionally conformant (with named conditions) | Not triggered

**Conflict of interest classifications:** Tier 1 bar | Tier 2 disclosure required | Tier 2 waiver required | Tier 3 disclosure encouraged | No conflict of interest finding

**Data quality findings (per standard):** Passes | Fails | Insufficient information to assess

**Gate evidence findings:** Verified | Failed | Conditionally verified pending [named item]

**Recommendation terms:** Fund | Fund with conditions | Do not fund

---

## Relationship to Other Skills

**Frame Language skill:** CROSS is a Frame 2 instrument. The FROM state requirement in change-obligation rounds is a structural application of the Frame Language inheritance principle: naming the actual condition rather than a projected aspiration. D2 failures in the change-obligation gate assessment are the same failure class Frame Language names as "values aspiration without conditions." Use Frame Language terminology when describing failure types in formal evaluation documents.

**Adverse Signal skill:** Dimension 5 of CROSS instantiates the Adverse-Signal Engagement Principle Core Standard. When Dimension 5 is active, the Adverse Signal skill provides the full assessment procedure.

**Information Asymmetry skill:** Dimension 4 of CROSS instantiates the Information Asymmetry Classification Standard omission class. When evaluating whether a non-disclosure constitutes a disqualifier, the Information Asymmetry Classification Standard skill provides the classification structure.

**Regenerative Obligation skill:** Structurally paired with CROSS but independent. Run both skills independently when both apply; do not merge the evaluations.

**Precision-First skill:** The double-negation invariant from the Precision-First Design Standard is the structural rationale for the tiered documentation architecture in CROSS. When a reviewer questions whether a documentation requirement is proportionate, the Precision-First Design Standard skill provides the formal test.

---

## Standing Obligations

Before generating any finding or recommendation:

1. Confirm the obligation mode from the round specification. Apply the correct gate procedure from Part III.

2. Confirm which task is requested and apply the correct procedure in full. Do not abbreviate the procedure because the application appears simple.

3. Use canonical finding vocabulary throughout. Do not introduce synonyms or informal equivalents.

4. Name conditions specifically. "Fund with conditions" without named conditions is not a complete finding.

5. Keep Regenerative Obligation Standard and CROSS evaluations structurally separate. If both apply, run both and report separately.

6. Do not substitute the gate assessment for the rigor tier assessment, or the rigor tier assessment for the gate. They are sequential, not interchangeable.

7. Do not apply change-obligation gate criteria to build-obligation applications. The Theory of Build is not a failure mode in build-obligation rounds.

---

## Changelog

| Version | Date | Changes |
|---------|------|---------|
| 0.2.0 | 2026-05-14 | Major revision. Added three accountability modes (build, change, retroactive) with mode-specific entry specification gate procedures in Part III. Renamed "Theory of Build Gate" to "Entry Specification Gate." Updated Field 3 from constrained four-option data type list to open measurement form with three-axis classification (source type, measurement form, aggregation type). Added Part X (Gate Evidence Assessment) covering progress verification and completion verification gate assessments. Updated Grant Configurator question sequence to match Configurator v0.2.0 (Q0 runbook selection, Q2 accountability mode, Q5 program-level continuation gate, Q11 gate configuration). Updated recommendation logic for mode awareness. Added retroactive-specific canonical finding vocabulary. Removed "transclusion" language from Part I. Updated related documents to v0.2.0. |
| 0.1.0 | 2026-05-14 | Initial skill encoding. Single change-accountability mode. Theory of Build gate with five-classification FROM state vocabulary. 11 indicator fields. Five data quality standards. Conflict of interest three-tier classification. Grant Configurator 11-question sequence. Three-term recommendation vocabulary. Privacy-sensitive accommodation procedure. |
