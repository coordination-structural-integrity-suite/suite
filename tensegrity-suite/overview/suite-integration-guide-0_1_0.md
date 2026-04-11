---
title: Suite Integration Guide
version: 0.1.0
date: 2026-04-06
status: Draft
---

# Suite Integration Guide

**Version:** 0.1.0 | April 2026

*Coordination Structural Integrity Suite*

---

## What This Document Is For

The nine standards in the Coordination Structural Integrity Suite are each independently adoptable. The README and each standard's own documentation explain what each one does. What they do not explain in full is what happens structurally when you deploy them together: which combinations are load-bearing for which failure modes, where detection reliability breaks down when certain standards are absent, and how to sequence adoption when you cannot adopt all nine at once.

This guide addresses those questions. It does not replace the standards. It does not specify implementation paths; those are protocol-bound and context-specific. It specifies the structural logic of deploying the suite as a whole, so that practitioners can make informed adoption decisions and understand what partial adoption actually covers and leaves exposed.

Two things this guide is not:

It is not a configuration library. The Suite Deployment Contexts document (forthcoming) will catalog the structural arrangement of standards appropriate to named organizational contexts: nascent Decentralized Autonomous Organizations (DAOs), scaling protocols, post-crisis organizations. This guide addresses integration logic that applies across configurations.

It is not a checklist. A practitioner who reads this guide and uses it as a checklist to confirm that their suite adoption is complete has missed the point. The guide is a diagnostic instrument. Its job is to surface the structural question each adoption decision creates.

---

## The Two-Layer Architecture

The suite has two structural layers with different logics. Getting this distinction right is prior to every other integration question.

The six Tensegrity Compressive Standards are floors. They specify what must not be violated. Violating a compressive standard means a structural exploitation vector is open. The violation is detectable, at least in principle, because these standards specify observable structural conditions and prohibit specific structural absences.

The three Tensegrity Generative Standards specify what must be structurally present for coordination capacity to develop. A system can meet all six compressive standards and still fail to develop genuine coordination capacity. That is not a failure of the compressive layer. It is a structural condition the generative layer addresses.

The failure modes are different in kind. Compressive failures are exploitation vectors: they enable bad actors, or enable well-intentioned actors operating in the wrong structural conditions, to concentrate power, suppress signals, and extract without accountability. Generative failures are attritional: they drain the structural resources that coordination depends on, invisibly, until the system cannot self-correct under novel stress.

A system fully protected on the compressive layer but lacking generative infrastructure is protected but brittle. It cannot develop the coordination capacity that would let it evolve, adapt, and recover from challenges it did not anticipate. A system with rich generative capacity but absent compressive floors is vibrant but exploitable; the generative capacity will be captured or drained by the structural dynamics the compressive floors are designed to prevent.

Neither layer is sufficient. The layers address different failure modes with different structural logics. Treating either layer as the complete suite is the most consequential integration error the guide exists to prevent.

---

## Detection Reliability Dependencies

This is the structural fact that has the most direct implications for audit practice and adoption sequencing: some compressive standards produce unreliable detection results when certain generative conditions are absent. This is not a flaw in the compressive standards. It is a structural property of how detection works. When a compressive standard's detection architecture depends on participants surfacing signals, depleted relational conditions or broken sensemaking infrastructure will produce false negatives: the surface shows compliance while the structural failure accumulates invisibly.

Four dependencies are currently specified.

**Adverse Signal Engagement Principle Core Standard depends on the Relational Battery condition of the Four Batteries Capacity Standard.** The Adverse Signal Engagement Principle Core Standard requires that participants surface signals contradicting current models through designated channels. When the Relational Battery is depleted, participants will not surface adverse signals even when explicitly invited to do so, because the relational context makes surfacing feel unsafe or pointless. An audit of the Adverse Signal Engagement Principle Core Standard conducted in an organization with a depleted Relational Battery will show no recorded adverse signals. Governance will conclude the standard is being met. The signals are not absent; the surfacing mechanism has failed. Joint adoption of the Adverse Signal Engagement Principle Core Standard and the Four Batteries Capacity Standard, with Relational Battery instrumented at a sufficient tier, is required for audit results to be trustworthy. The Adverse Signal Engagement Principle Core Standard carries this dependency in its normative text (Section 2.3).

**Structural Consent Legibility Standard depends on the Relational Battery condition of the Four Batteries Capacity Standard.** Consent that is structurally present, where negotiated limits, bidirectional awareness, and revocability are all formally in place, can be structurally hollow when the Relational Battery is depleted. Participants agree because the relational context makes refusal feel unsafe, not because they freely consent. The audit surface shows the three consent features present; the underlying condition means consent is structural theater rather than genuine authorization. Joint adoption of the Structural Consent Legibility Standard and the Four Batteries Capacity Standard, with Relational Battery instrumented, is required for consent audit results to reflect actual consent conditions.

**Structural Power Obligation Standard (coordination dimension) depends on the Sensemaking Standard.** Interpretive power concentration is the primary accumulation vector in the coordination dimension. It operates by controlling what is thinkable within the system's meaning-making processes: who defines what signals mean, who determines what a disruption requires, whose interpretive frame resolves ambiguous situations. This form of concentration is only detectable when meaning-making processes are observable and the authority over those processes is legible. If sensemaking infrastructure is absent or non-functional, the coordination dimension of Structural Power Distribution detection is blind to the most consequential form of power accumulation. A power distribution audit that does not include a sensemaking assessment cannot claim completeness on the coordination dimension.

**Information Asymmetry Classification Standard (omission class) depends on the Sensemaking Standard and the Contribution Battery of the Four Batteries Capacity Standard.** Omission asymmetry, the class covering what is deliberately never said, is only detectable when sensemaking processes surface what participants are not naming: the questions no one asks, the topics that are never opened, the disruptions that fail to occasion sensemaking. If sensemaking infrastructure is absent, omission asymmetry detection has no surfacing mechanism. Contribution Battery depletion drives activity outside the visible governance record, which constitutes omission asymmetry that standard detection will not find because the activity generating it is invisible to governance. An omission asymmetry assessment conducted without sensemaking infrastructure and without Contribution Battery instrumentation will systematically underreport the omission class.

### What Detection Reliability Dependencies Mean for Practice

An audit result is not an audit result if its detection surface is compromised. The four dependencies above are not theoretical concerns. They are the specific structural conditions under which a governance system can confidently confirm that it is healthy because the detection mechanism for its structural failures is itself broken.

The practical implication is that audit confidence is bounded by generative standard conditions. Before drawing conclusions from a compressive standard audit, a practitioner should ask: are the generative conditions this standard's detection architecture depends on present and instrumented? If the answer is no or unknown, the audit result must carry a stated reliability limitation.

An organization at Tier 3 on the Adverse Signal Engagement Principle Core Standard with no Four Batteries Capacity Standard adoption has auditable processes for engaging adverse signals and no basis for confidence that those processes are producing signals. That is not Tier 3 reliability. It is Tier 3 process with Tier 0 signal integrity. The adoption tier architecture does not specify this bound; this guide does.

---

## Start Where It Hurts: Five Adoption Entry Points

If you are deciding where to begin, the most reliable guide is not a general recommendation. It is a map from your current pain presentation to the standards most likely to address it.

**Signals are being suppressed or dismissed.** Start with the Adverse Signal Engagement Principle Core Standard and the Four Batteries Capacity Standard together. Suppressed signals are both a structural engagement failure and a Relational Battery failure. Adopting only the Adverse Signal Engagement Principle Core Standard will instrument processes for engaging signals that participants are not surfacing; the instrumentation will show false compliance. Adopting only the Four Batteries Capacity Standard will surface the depletion state without providing the structural obligation to engage despite it. The two together close the loop: the obligation to engage (compressive) operating in conditions where engagement is possible (generative). Neither is sufficient without the other when the presenting problem is signal suppression.

**Governance capture or authority concentration.** Start with the Structural Power Obligation Standard and the Structural Consent Legibility Standard together. Capture typically operates through two mechanisms simultaneously: authority accumulation across the three power dimensions (authority, coordination, specialization), and consent that is formally present but structurally hollow. The Structural Power Obligation Standard makes accumulation legible and contestable. The Structural Consent Legibility Standard ensures that agreement to participate is distinguishable from agreement to the specific authority distribution that capture has produced. Adopting only one leaves the other mechanism intact. Note also the detection dependency: if capture is already advanced, Relational Battery instrumentation (Four Batteries Capacity Standard) is needed to confirm that power distribution assessments are not producing false negatives through participant unwillingness to surface what they see.

**Invisible work and contributor burnout.** Start with the Four Batteries Capacity Standard and the Regenerative Obligation Standard together. The Hidden Factory dynamic, where the organization's actual work migrates to channels governance cannot see, is the Four Batteries presentation of invisible work. The Regenerative Obligation Standard specifies the floor: extraction of that invisible labor is a structural violation when not matched by regenerative return satisfying non-fungibility, proximity, and embeddedness simultaneously. The Four Batteries Capacity Standard makes the invisible work legible; the Regenerative Obligation Standard specifies what the organization's obligation to that work is once it is legible. Adopting only the Four Batteries Capacity Standard surfaces what is invisible without specifying the accountability obligation. Adopting only the Regenerative Obligation Standard specifies an obligation to return that the organization cannot verify it is meeting because the extraction is unmeasured.

**Decisions made without adequate information.** Start with the Information Asymmetry Classification Standard and the Sensemaking Standard together. The Information Asymmetry Classification Standard provides the taxonomy of structural gaps: six primary classes (positional, temporal, interpretive, relational, omission, complexity) that create the structural conditions under which poor decisions are made not from bad intent but from what is structurally unknowable from certain positions. The Sensemaking Standard specifies the conditions under which those gaps can be surfaced and processed by the people who bear them. Taxonomy without surfacing infrastructure names the gaps and leaves them in place. Surfacing infrastructure without taxonomy generates sensemaking occasions without a framework for classifying what they surface. The combination makes information gaps both nameable and processable.

**Conflict destroying organizational capacity.** Start with the Conflict Transformation Standard and the Adverse Signal Engagement Principle Core Standard together. The Conflict Transformation Standard provides the structural container: a transformation spine from early informal engagement through facilitated transformation through adjudication, with adjudication last, and recognition that conflict engagement is coordination work rather than governance overhead. The Adverse Signal Engagement Principle Core Standard ensures that what emerges from conflict processing, the signals conflict surfaces about structural conditions, is engaged rather than suppressed or routed directly to adversarial resolution. Conflict transformation without adverse signal engagement can successfully transform individual conflicts while leaving the structural conditions that generate them intact. Adverse signal engagement without conflict transformation routes every structural signal to a governance system with no graduated engagement architecture, which typically means the signal reaches adjudication before it can be processed as developmental information.

### Combining Multiple Entry Points

These five entry points are not exhaustive, and the pain presentations they describe are not mutually exclusive. An organization facing governance capture will often also have signal suppression and invisible work dynamics, because these structural conditions co-occur and reinforce each other. When multiple entry points apply, the joint starting set should cover all of them, with the understanding that the detection reliability dependencies above apply to the full joint set.

The full suite offers full structural coverage. The entry points are starting positions for organizations that cannot adopt all nine standards simultaneously. They are not resting positions.

---

## What Each Standard Adds to the Set

This section describes what becomes structurally detectable, and what remains structurally blind, as each standard is added to an adoption set. Read it as a dependency map: what does each standard assume is already present to function at full reliability?

**Adding the Precision-First Design Standard** closes the gap between what a system claims to do and what it structurally does. Every other standard in the suite depends on this one implicitly: a system that cannot specify the structural mechanisms behind its claims cannot reliably identify deficits under any other standard either. The Precision-First Design Standard is the meta-standard; its absence means every other audit result is potentially artifact rather than finding.

**Adding the Adverse Signal Engagement Principle Core Standard** installs the mandatory processing obligation. Without it, a system can receive signals that contradict its models, acknowledge them, discuss them, and dismiss them without that dismissal being structurally visible. With it, every signal that enters the system must be registered, engaged, and closed with a traceable conclusion; dismissal without documented engagement is a structural violation. At full reliability, requires Relational Battery instrumentation.

**Adding the Structural Consent Legibility Standard** makes consent structure observable rather than assumed. Without it, a system may have participation but no structural mechanism to distinguish consent to participation from consent to specific power arrangements, terms, or outcomes. With it, the three consent features, negotiated limits, bidirectional awareness, and revocability, are observable and can be evaluated against the actual consent conditions in the system. At full reliability, requires Relational Battery instrumentation.

**Adding the Information Asymmetry Classification Standard** installs a taxonomy for what is structurally unknowable from certain positions. Without it, information failures appear as individual errors (someone did not tell someone else something) rather than structural conditions (the system's architecture creates positions from which certain information cannot be reached regardless of individual effort). With it, information gaps are classifiable and their structural sources are legible. The omission class, at full reliability, requires Sensemaking Standard infrastructure and Contribution Battery instrumentation.

**Adding the Structural Power Obligation Standard** makes power arrangements legible across all three dimensions simultaneously. A system without it may have authority-dimension documentation (who decides what) while concentration accumulates in the coordination dimension (who controls what things mean) and the specialization dimension (who can meaningfully participate in specialized governance domains). With it, all three dimensions are required to be legible and contestable. The coordination dimension, at full reliability, requires Sensemaking Standard infrastructure.

**Adding the Regenerative Obligation Standard** installs the extraction accountability floor. Without it, a system can consume coordination labor, local knowledge, legitimacy, and attention from contributors without any structural obligation to return value in a form that reaches the parties who bore the extraction. With it, each extraction event above a declaration threshold requires regenerative return satisfying non-fungibility, proximity, and embeddedness simultaneously. The stance declaration requirement makes the extraction vector legible before the accountability question arises.

**Adding the Sensemaking Standard** installs the structural conditions under which the system can produce new understanding from disruption rather than applying existing frames to novel situations. Without it, the system can learn within its existing models but cannot revise the models themselves when disruption challenges them. With it, the five structural invariants specify what genuine meaning-making requires as distinct from pattern-matching; the liminal phase requirement is the diagnostic marker. This standard also enables two compressive standards to reach full detection reliability: Structural Power Distribution (coordination dimension) and Information Asymmetry Classification (omission class).

**Adding the Four Batteries Capacity Standard** makes organizational capacity legible across two independent axes per battery. The charge axis (current depletion state) and the developmental state axis (what full charge enables at this stage of development) are structurally distinct and require separate assessment. Without this standard, a system cannot distinguish an organization that is depleted from one that is fully charged but at an early developmental state; both may look identical from outside while producing structurally different coordination outputs. With it, both axes are assessed on a regular cadence with enough specificity that a low reading would change what the organization does. This standard also enables two compressive standards to reach full detection reliability: Adverse Signal Engagement Principle Core Standard and Structural Consent Legibility Standard.

**Adding the Conflict Transformation Standard** installs the structural recognition that conflict is coordination information, not governance overhead. Without it, a system routes conflict to adjudication because it has no other structural pathway. With it, the transformation spine provides graduated engagement pathways, conflict engagement is recognized as coordination work and compensatable as such, and conflict events become depositable in the governance record as developmental rather than as failures. This addresses the structural gap that produced GravityDAO's collapse: the organization was universally recognized as necessary and failed entirely because no coordination infrastructure provided a mechanism to recognize conflict transformation as coordination work.

---

## Disclosure Requirements for Partial Adoption

Every organization that claims structural accountability without holding the full Tensegrity Compressive Standards designation, all six compressive standards at Tier 4 or above, must produce a structural exposure disclosure. The README specifies the four required elements of a substantive disclosure: naming each absent standard, describing the failure mode class it addresses, stating a self-assessed exposure level with rationale, and naming compensating controls or explicitly stating that none exist.

The suite integration logic above adds a fifth requirement to substantive disclosure: stating the detection reliability bound on any compressive standard audit results.

An organization at Tier 3 on the Adverse Signal Engagement Principle Core Standard without Four Batteries Capacity Standard adoption has a detection reliability bound on its adverse signal audits. A substantive disclosure must name this bound. An organization at Tier 3 on the Structural Power Obligation Standard without Sensemaking Standard adoption has a detection reliability bound on the coordination dimension of its power distribution audits. A substantive disclosure must name this bound.

A disclosure that meets the README's four elements but omits detection reliability bounds is form-compliant but not substantive for any compressive standard with a named detection dependency. The omission is a precision deficit under the Precision-First Design Standard and carries the same adverse signal processing obligation as any other precision failure.

---

## The Suite as a Developmental Trajectory

The adoption architecture describes five tiers and three adoption categories. Organizations do not arrive at full adoption overnight. The question this guide addresses for organizations in transit is: in what direction do you move next?

The answer is structural, not motivational. The direction that closes the most consequential open vulnerability is the next adoption priority. The detection reliability dependencies above are a direct guide to that priority: if you hold a compressive standard without the generative standard its detection depends on, your audit results are unreliable in a specific way. Closing that reliability gap is structurally more urgent than adding a new standard you do not yet hold.

The sequence implication: for most organizations, adding the Four Batteries Capacity Standard early is structurally high-priority because it enables two other compressive standards to reach reliable detection. Adding the Sensemaking Standard early is structurally high-priority because it enables two other compressive standards to reach reliable detection. These are not aspirational additions; they are the structural conditions under which the compressive standards you have already adopted can be trusted.

The suite is designed to be adopted developmentally. The standards are each independently useful from Tier 1 onward. The integration guidance here is about sequencing that developmental trajectory toward the configuration that offers the most reliable coverage of the most consequential failure modes for your organizational context.

---

## Changelog

| Version | Date | Summary |
| --- | --- | --- |
| 0.1.0 | 2026-04-06 | Initial document. Four detection reliability dependencies, five adoption entry points, per-standard addition map, disclosure requirements for partial adoption, developmental trajectory framing. |
