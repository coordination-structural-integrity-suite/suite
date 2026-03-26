# standards

This repository contains seven coordination standards developed in the course of building the Proof of Coordination protocol. They address structural failure modes that recur across coordination systems regardless of domain.

## What these standards are

Coordination systems fail in predictable ways: not because participants are malicious or incompetent, but because the systems lack structural floors and generative capacity. A structural floor is a minimum condition that, when absent, makes exploitation and degradation predictable rather than merely possible. Generative capacity is the substrate that makes those floors meaningful rather than merely procedural.

These standards specify both. They are organized into two sub-layers within the Structural Integrity Layer: the Commitment Standards (compressive) close exploitation vectors, and the Cohesion Standards (tensile) specify the capacity conditions that make the compressive standards function as coordination instruments rather than compliance checklists.

Each standard is an instrument: a standalone specification of a structural requirement with verifiable compliance conditions. They are not prescriptive workflows, style guides, or evaluation rubrics. They specify structural conditions; they do not specify how to organize.

## What these standards are not

These standards are not complete coordination infrastructure. Partial adoption is legitimate. Partial adoption claimed as full conformance is not. Organizations adopting one or more of these standards without the full set should disclose which standards they have adopted rather than claiming general conformance.

These standards do not specify governance outcomes. They specify structural conditions. What organizations do within those conditions is outside their scope.

## The Commitment Standards (compressive sub-layer)

Five standards that specify structural floors. Each names a class of structural failure and specifies the condition that prevents it.

**Precision-First Design Standard:** Requires that every element of a governed system increase the precision with which the system's dynamics can be observed, classified, and acted upon. Closes the gap between what a coordination system says it does and what it structurally does. Seven corollaries including residue-based verification.

**Adverse-Signal Engagement Principle Core Standard:** Requires engagement with signals that contradict current models rather than suppression or reframing. Closes the gap between appearing to address problems and actually addressing them.

**Structural Consent Legibility Standard:** Requires that consent to participation be structurally distinguishable from consent to specific terms, outcomes, and power arrangements. Three consent features: negotiated limits, bidirectional awareness, revocability.

**Information Asymmetry Classification Standard:** Requires classification and disclosure of the structural types of information asymmetry present in a coordination system. Six classes: positional, temporal, interpretive, relational, omission, complexity.

**Structural Power Distribution Standard:** Requires that structural power arrangements be legible and contestable by participants who hold less of it. Three dimensions: coordination, authority, specialization.

## The Cohesion Standards (tensile sub-layer)

Two standards that specify the capacity conditions required for the Commitment Standards to function as coordination instruments.

**Sensemaking Standard:** Specifies what sensemaking must structurally provide without prescribing method. Five structural invariants derived from cross-traditional analysis, three sensemaking scales, three action invariants. The standard that governs the generative process producing both sub-layers.

**Four Batteries Generative Capacity Standard:** Specifies four resource conditions for generative capacity (personal, relational, contribution, mission) across two dimensions (charge and developmental state). Six structurally coupled connections between individual batteries and individual Commitment Standards specify the operational interface between the two sub-layers.

## Relationship between sub-layers

The relationship is tensegrity, not hierarchy. The compressive standards provide the structural floor without which coordination degrades into exploitation. The cohesion standards provide the sensemaking capacity without which coordination degrades into compliance. Both types of degradation produce organizations that appear to be coordinating while failing to coordinate. Neither sub-layer alone is sufficient; each requires the other.

## Relationship to the Proof of Coordination protocol

These standards are the normative foundation for the Proof of Coordination protocol, which builds measurement infrastructure for coordination capacity. The standards can be adopted independently of the full protocol. The protocol depends on them structurally.

Full protocol documentation will be linked here as it is released.

## Licensing

- **Specifications** (`standards-*.md` and other standards documents): Licensed under Creative Commons Attribution 4.0 International (CC BY 4.0). See `LICENSE-SPEC`.
- **Code and software artifacts** (now or future: examples, scripts, tests, reference implementations): Licensed under Apache License 2.0. See `LICENSE`.
