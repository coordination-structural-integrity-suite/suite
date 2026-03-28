# Prompts

Paste-and-go prompts for using standards in this repository with any AI assistant.

Copy the full contents of any prompt file, paste it into any AI chat (Claude, ChatGPT, Gemini, or similar), and attach or describe the document or system you want audited or assessed. No prior knowledge of the standard is required. The prompts carry everything the AI needs.

Two prompt formats are used across this repository:

**Audit format** (compressive standards): identifies where a document or system fails to meet a structural requirement. Output is a failure map organized by criterion, most consequential deficits first. Used for the five Tensegrity Compressive Standards.

**Presence-assessment format** (generative standards): identifies whether the structural conditions enabling a capacity are present, partially present, or absent. Output is a presence map organized by invariant, distinguishing evidence of structural presence from gaps. Used for the three Tensegrity Generative Standards.

---

## Suite-Level Prompts

For auditing or assessing against multiple standards at once.

| Prompt | Use it on |
|---|---|
| [Compressive Audit](suite-compressive-audit-0_1_0.md) | Any coordination system — runs all five Tensegrity Compressive Standards |
| [Generative Assessment](suite-generative-assessment-0_1_0.md) | Any coordination system — runs all three Tensegrity Generative Standards |
| [Full Suite Audit](suite-full-audit-0_1_0.md) | Any coordination system — runs all eight standards with cross-layer interaction analysis |

---

## Tensegrity Compressive Standards

### Precision-First Design Standard

| Prompt | Use it on |
|---|---|
| [General Audit](../compressive/prompts/precision-first/precision-first-audit-general-0_1_1.md) | Any document, specification, or standard |
| [Governance Audit](../compressive/prompts/precision-first/precision-first-audit-governance-0_1_1.md) | Decentralized autonomous organization proposals, bylaws, charters, policies, constitutions |
| [Software Audit](../compressive/prompts/precision-first/precision-first-audit-software-0_1_1.md) | Application programming interface contracts, requirements docs, schemas, technical designs |

### Adverse Signal Engagement Principle Core Standard

| Prompt | Use it on |
|---|---|
| [Organizational Audit](../compressive/prompts/adverse-signal/organizational-adverse-signal-audit-0_1_0.md) | Governance documents, policies, process descriptions |
| [Regulatory Compliance Audit](../compressive/prompts/adverse-signal/regulatory-compliance-adverse-signal-audit-0_1_0.md) | Compliance frameworks, regulatory submissions |
| [AI Systems Audit](../compressive/prompts/adverse-signal/ai-adverse-signal-audit-0_1_0.md) | AI system designs, model documentation, feedback architectures |

### Structural Consent Legibility Standard

| Prompt | Use it on |
|---|---|
| [Consent Legibility Audit](../compressive/prompts/structural-consent/structural-consent-audit-0_1_0.md) | Governance documents, participation terms, consent architecture |

### Information Asymmetry Classification Standard

| Prompt | Use it on |
|---|---|
| [Asymmetry Classification Audit](../compressive/prompts/information-asymmetry/information-asymmetry-audit-0_1_0.md) | Coordination system descriptions, governance documents, platform architecture |

### Structural Power Distribution Standard

| Prompt | Use it on |
|---|---|
| [Power Distribution Audit](../compressive/prompts/structural-power-distribution/structural-power-distribution-audit-0_1_0.md) | Governance documents, organizational descriptions, protocol architecture |

---

## Tensegrity Generative Standards

### Sensemaking Standard

| Prompt | Use it on |
|---|---|
| [Sensemaking Presence Assessment](../generative/prompts/sensemaking/sensemaking-presence-assessment-0_1_0.md) | Coordination systems, organizations, or processes — assesses structural presence of sensemaking capacity |

### Four Batteries Capacity Standard

| Prompt | Use it on |
|---|---|
| [Four Batteries Presence Assessment](../generative/prompts/four-batteries/four-batteries-presence-assessment-0_1_0.md) | Coordination systems or organizations — assesses structural presence of generative capacity conditions |

### Conflict Transformation Standard

| Prompt | Use it on |
|---|---|
| [Conflict Transformation Presence Assessment](../generative/prompts/conflict-transformation/conflict-transformation-presence-assessment-0_1_0.md) | Coordination systems or organizations — assesses structural presence of conflict transformation capacity |

---

## Claude Skills

For more complex evaluation work requiring extended reasoning with the standards, use the Claude skills in `../skills/`. Skills encode the frame needed for correct reasoning with each standard and with the suite as a whole.

- `claude-skill-suite-0_1_0.md` — Full suite skill covering all eight standards, the compressive/generative distinction, and cross-layer interactions
- Individual skills for each standard: `claude-skill-[standard-name]-0_1_0.md`
