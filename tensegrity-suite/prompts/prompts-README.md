# Prompts

Paste-and-go prompts for using the Coordination Structural Integrity Suite with any AI assistant.

Copy the full contents of any prompt file, paste it into any AI chat (Claude, ChatGPT, Gemini, or similar), and describe your situation or attach the document you want assessed. No prior knowledge of the suite is required. The prompts carry everything the AI needs.

**If you are new to the suite and do not know where to start, use the [Where Do I Start? triage prompt](suite/suite-triage-where-do-i-start-0_1_0.md) first.** It assesses your situation and routes you to the right instrument, with an explanation of why.

**Two entry paths.** This prompt system has two tracks. Start with the Explore prompt if you are new to the suite, want to understand whether it applies, or want to orient yourself before committing to a formal process. Start with the Coordination Structural Integrity Suite Assessment if you want to formally assess your organization's structural health across all nine standards and produce a concrete gap map and advancement roadmap. The assessment process works best after the exploration — it builds on the vocabulary and structural self-knowledge the exploration develops.

Five prompt formats are used across this repository:

**Exploration format**: orients you to the suite and your structural situation, routes you to the right instrument, and produces a findings document you can save and carry forward. Used for the Explore prompt.

**Assessment format**: guides you through a structured five-stage process — foundation check, self-assessment across all nine standards, gap mapping, and advancement planning. Multi-session. Produces a downloadable output at each stage. Used for the Coordination Structural Integrity Suite Assessment.

**Audit format** (compressive standards): identifies where a document or system fails to meet a structural requirement. Output is a failure map organized by criterion, most consequential deficits first. Used for the six Tensegrity Compressive Standards.

**Capacity development format** (generative standards): identifies whether the structural conditions enabling a capacity are present and what the growth edges are. Output is a presence map with cultivation guidance. Used for the three Tensegrity Generative Standards.

**Application guide format** (framework-application documents and suite documents): walks through a framework or document's logic against a specific situation the user brings. No conformance score. Output is a structural reading of your case or a routing recommendation. Used for framework-application documents (Six-V Trust Framework), suite documents (Tensegrity Architecture, Structural Patterns Primer, Suite Integration Guide, Suite Deployment Contexts), and pre-deployment assessments (Conflict Transformation Preconditions Specification).

---

## Where Do I Start?

Two entry points. Choose based on where you are.

| Prompt | Use it when |
|---|---|
| [Explore the Coordination Structural Integrity Suite](suite/suite-explore-coordination-structural-integrity-suite-0_1_0.md) | You are new to the suite, unsure whether it applies, or want to understand your structural situation before committing to a formal process. Produces an exploration findings document you can carry into the assessment process. |
| [Coordination Structural Integrity Suite Assessment — Stage 1](suite/suite-assessment-stage-1-orientation-0_1_0.md) | You want to formally assess your organization's structural health across all nine standards. Five-stage process. Best after completing the Explore prompt. |

The legacy triage prompt ([Where Do I Start?](suite/suite-triage-where-do-i-start-0_1_1.md)) is still available for direct routing to individual instruments when you already know which standard or prompt you need.

---

## Coordination Structural Integrity Suite Assessment

A five-stage structured process for assessing your organization's structural health across all nine standards. Each stage produces a downloadable output. Stages can be completed in separate sessions — bring your prior stage output to each new session.

| Stage | Prompt | What it does |
|---|---|---|
| Stage 1 | [Process Orientation](suite/suite-assessment-stage-1-orientation-0_1_0.md) | Orients you to the full process, establishes what you are hoping to understand, presents the data consent statement. Output: process summary. |
| Stage 2 | [Structural Foundation Check](suite/suite-assessment-stage-2-foundation-check-0_1_0.md) | Assesses which of the six coordination commons components are present, partial, or absent in your actual practice. Output: commons components inventory. |
| Stage 3 | [Standards Self-Assessment](suite/suite-assessment-stage-3-self-assessment-0_1_0.md) | For each of the nine standards, assesses where your organization currently stands against what the standard requires. Multi-session. Output: standards self-assessment with structured finding per standard. |
| Stage 4 | [Gap Map and Priorities](suite/suite-assessment-stage-4-gap-map-0_1_0.md) | Synthesizes your Stage 2 and Stage 3 findings into your three most structurally significant gaps, with gap type and what addressing each would look like. Output: gap map. |
| Stage 5 | [Advancement and Future Framing](suite/suite-assessment-stage-5-advancement-0_1_0.md) | Consolidates findings, establishes concrete next steps for each priority gap, frames a six-month re-assessment. Output: advancement summary. |

---

## Suite-Level Prompts

For auditing or assessing against multiple standards at once, or for orientation to the suite as a whole.

| Prompt | Use it on |
|---|---|
| [Compressive Audit](suite/suite-compressive-audit-0_1_1.md) | Any coordination system — runs all six Tensegrity Compressive Standards |
| [Generative Assessment](suite/suite-generative-assessment-0_1_1.md) | Any coordination system — runs all three Tensegrity Generative Standards |
| [Full Suite Audit](suite/suite-full-audit-0_1_1.md) | Any coordination system — runs all nine standards with cross-layer interaction analysis |

---

## Tensegrity Compressive Standards

### Precision-First Design Standard

| Prompt | Use it on |
|---|---|
| [General Audit](precision-first/precision-first-audit-general-0_1_2.md) | Any document, specification, or standard |
| [Governance Audit](precision-first/precision-first-audit-governance-0_1_2.md) | Decentralized autonomous organization proposals, bylaws, charters, policies, constitutions |
| [Software Audit](precision-first/precision-first-audit-software-0_1_2.md) | Application programming interface contracts, requirements docs, schemas, technical designs |

### Adverse Signal Engagement Principle Core Standard

| Prompt | Use it on |
|---|---|
| [Organizational Audit](adverse-signal/organizational-adverse-signal-audit-0_1_1.md) | Governance documents, policies, process descriptions |
| [Regulatory Compliance Audit](adverse-signal/regulatory-compliance-adverse-signal-audit-0_1_1.md) | Compliance frameworks, regulatory submissions |
| [AI Systems Audit](adverse-signal/ai-adverse-signal-audit-0_1_1.md) | AI system designs, model documentation, feedback architectures |

### Structural Consent Legibility Standard

| Prompt | Use it on |
|---|---|
| [Consent Legibility Audit](structural-consent/structural-consent-audit-0_1_1.md) | Governance documents, participation terms, consent architecture |

### Information Asymmetry Classification Standard

| Prompt | Use it on |
|---|---|
| [Asymmetry Classification Audit](information-asymmetry/information-asymmetry-audit-0_1_1.md) | Coordination system descriptions, governance documents, platform architecture |

### Structural Power Distribution Standard

| Prompt | Use it on |
|---|---|
| [Power Distribution Audit](structural-power-distribution/structural-power-distribution-audit-0_1_1.md) | Governance documents, organizational descriptions, protocol architecture |

### Regenerative Accountability Standard

| Prompt | Use it on |
|---|---|
| [Regenerative Accountability Audit](regenerative-accountability/regenerative-accountability-audit-0_1_1.md) | Organizations or protocols — assesses whether return to harm-bearing parties meets three simultaneous validity conditions |

---

## Tensegrity Generative Standards

### Sensemaking Standard

| Prompt | Use it on |
|---|---|
| [Sensemaking Presence Assessment](sensemaking/sensemaking-presence-assessment-0_1_2.md) | Coordination systems, organizations, or processes — assesses structural presence of sensemaking capacity |

### Four Batteries Capacity Standard

| Prompt | Use it on |
|---|---|
| [Four Batteries Presence Assessment](four-batteries/four-batteries-presence-assessment-0_1_2.md) | Coordination systems or organizations — assesses structural presence of generative capacity conditions |

### Conflict Transformation Standard

| Prompt | Use it on |
|---|---|
| [Conflict Transformation Presence Assessment](conflict-transformation/conflict-transformation-presence-assessment-0_1_2.md) | Coordination systems or organizations — assesses structural presence of conflict transformation capacity |

---

## Suite Document Prompts

Suite documents are orientation, diagnostic, and configuration tools for the suite as a whole. Their prompts use application guide format: they work with the situation you describe rather than auditing a document for compliance.

### Tensegrity Architecture

| Prompt | Use it when |
|---|---|
| [Architecture Orientation](tensegrity-architecture/tensegrity-architecture-orientation-0_1_0.md) | You are encountering the suite for the first time, want to understand why it has the shape it does, or want to identify your entry point |

### Suite Structural Patterns Primer

| Prompt | Use it when |
|---|---|
| [Pattern Recognition](structural-patterns-primer/structural-patterns-primer-recognition-0_1_0.md) | You can describe a recurring dynamic and want to know what structural pattern it represents and which standards address it |

### Suite Integration Guide

| Prompt | Use it when |
|---|---|
| [Adoption Sequencing](integration-guide/integration-guide-adoption-sequencing-0_1_0.md) | You are already adopting standards and want to know what to prioritize next, or you want to check whether your current audit results are reliable |

### Suite Deployment Contexts

| Prompt | Use it when |
|---|---|
| [Combination Selection](deployment-contexts/deployment-contexts-combination-selection-0_1_0.md) | You have a specific presenting situation and want to know which standards combination to deploy, with contextual adjustments |

### Conflict Transformation Preconditions Specification

| Prompt | Use it when |
|---|---|
| [Readiness Assessment](conflict-transformation-preconditions/conflict-transformation-preconditions-readiness-0_1_0.md) | You are planning to run a conflict transformation process and want to verify structural preconditions are in place |

---

## Framework-Application Document Prompts

Framework-application documents are operational tools that apply the foundational frameworks to specific decision domains. Their prompts walk through a sequence against a specific case rather than checking conformance.

### Six-V Trust Framework

| Prompt | Use it on |
|---|---|
| [Application Guide](six-v/six-v-application-guide-0_1_0.md) | A specific relationship advancing in access or trust, a credentialing process you are designing, or a past trust-extension failure you are analyzing |

---

## Claude Skills

For more complex evaluation work requiring extended reasoning with the suite, use the Claude skills in `../claude-skills/`. Skills encode the frame needed for correct reasoning with each document and with the suite as a whole.

- `claude-skill-coordination-suite-triage-0_1_0.md` — Triage skill: routes by situation to the right instrument across the full prompt system
- `claude-skill-suite-0_1_1.md` — Full suite skill covering all nine standards, the compressive/generative distinction, and cross-layer interactions
- `claude-skill-tensegrity-architecture-0_1_0.md` — Tensegrity Architecture skill: orientation and entry point identification
- `claude-skill-structural-patterns-primer-0_1_0.md` — Structural Patterns Primer skill: pattern recognition across ten named structural patterns
- `claude-skill-integration-guide-0_1_0.md` — Suite Integration Guide skill: adoption sequencing and detection reliability dependencies
- `claude-skill-deployment-contexts-0_1_0.md` — Suite Deployment Contexts skill: combination selection and contextual calibration
- `claude-skill-conflict-transformation-preconditions-0_1_0.md` — Conflict Transformation Preconditions Specification skill: pre-deployment readiness assessment
- Individual standard skills: `claude-skill-[standard-name]-0_1_1.md`
- `claude-skill-six-v-0_1_0.md` — Six-V Trust Framework skill (framework-application document class)
