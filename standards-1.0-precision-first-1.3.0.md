**Precision-First Design Standard**

*A Transferable Standard for Specification Domains*

Regis Lloyd Chapman (Durgadas)

Version 1.3.0 | February 2026

# Abstract

Most accountability failures are not caused by bad actors or political breakdown. They are caused by instrument deficiency: rules that cannot be violated in a falsifiable way, detection systems that were never specified before deployment, and definitional gaps that generate compensatory institutions rather than corrections. These gaps persist because the institutions built to absorb their costs become more legible and better funded than the instruments that would make them unnecessary.

This standard names that pattern as a precision deficit and proposes a corrective: precision-first design. The corrective is not optional in systems that lack trusted interpretive intermediaries. Where such intermediaries exist (courts, regulators, credentialed professionals with recognized authority), vague standards can function because an authority supplies precision at dispute time. Systems that remove that backstop by design, whether through decentralization, scale, cross-jurisdictional operation, or structural independence from interpretive authority, face a different condition. In their absence, a vague standard is not imprecise; it is a permanently open gap. The precision-first invariant follows directly from this structural condition, not from a design philosophy.

This document defines the invariant, establishes six corollaries, provides worked examples across five frameworks, and describes three adoption levels for teams, governance bodies, legal drafters, and standards bodies. Its larger ambition is metrological: to begin the discipline of precise measurement in domains where accountability has historically depended on interpretive authority rather than structural specification.

# 1. The Problem: Reactive Design and the Precision Deficit

Every system that governs behavior encodes assumptions about what its participants will do, what violations look like, and how disputes will be resolved. When those assumptions are left implicit, three failure modes become nearly inevitable.

## 1.1 You cannot detect what you have not defined

A governance rule against "unfair outcomes" cannot be enforced because no party can agree, after the fact, on what "unfair" meant before the outcome occurred. The same applies to "transparency," "decentralization," "good faith," "reasonable," and the rest of the vocabulary common to governance documents, software terms of service, professional codes of conduct, and regulatory frameworks. Each of these terms is a precision deficit: a normative claim without an operational specification.

Precision deficits are not merely vague. They are structurally exploitable. A participant who benefits from a practice that the governing system was intended to prohibit can invoke the ambiguity to defeat enforcement. The precision deficit is the mechanism by which extraction persists inside ostensibly governed systems.

## 1.2 Reactive specification defers accountability

The standard response to a governance failure is to add a rule after the fact. This is reactive specification: sharpening definitions in response to harm rather than in anticipation of it. Reactive specification has two structural problems.

First, it cannot undo the harm that motivated it. Second, and more importantly, it signals to participants that ambiguity will be tolerated until someone complains loudly enough, which selects for participants willing to operate in grey zones and against participants who assume the system means what it says.

A system designed reactively tends to accumulate layers of retrospective rules over a shrinking normative core. Over time, the system becomes harder to understand, harder to audit, and harder to extend, while the core problem, definitional ambiguity, remains unaddressed.

There is a structural asymmetry in low-precision environments that is easy to miss. Actors who seek to exploit a system do not need precision standards to find gaps; they only need the gaps to exist. Actors who seek to build reliable, accountable systems do need precision standards: to know what "well-specified" means, to justify the upfront investment in definition, and to detect when something has gone wrong. The absence of shared precision standards therefore tilts the playing field toward opportunists and against builders. Precision-first design is, among other things, a structural response to this asymmetry: it closes gaps before they are exploited rather than after.

A precision deficit does not remain unfilled. It creates pressure, and that pressure generates responses: institutions, tooling, professional roles, informal norms, and workaround processes that absorb the demand the missing instrument would have handled. Many of these responses are well-intentioned and practically useful. None of that changes their structural status. They exist because the deficit exists. Once established, a compensatory response becomes difficult to distinguish from a solution: the deficit that made it necessary stops being experienced as a problem, and the institution is experienced as the answer. This is how precision deficits persist in systems full of people who believe they are solving them. It is also how the deficit becomes a stable resource. As workarounds accumulate and the gap becomes more legible, exploitation costs fall: noticing a navigable gap and extracting value from it requires only awareness, while closing it requires collective action, redesign, and absorption of costs by parties who built on top of the deficit. The well-intentioned compensatory response and its exploitative twin are responses to the same stimulus and, without a defined standard underneath, are structurally indistinguishable. Precision-first design does not aim to eliminate legitimate compensatory responses, many of which are valuable and some load-bearing. It aims to close the deficit that makes them indistinguishable from exploitation, and to shift the cost structure so that the gap becomes falsifiably detectable rather than indefinitely navigable.

The pattern is not specific to any single domain. A conflict resolution protocol that defines dispute criteria and resolution procedures operationally is a precision instrument. A court system that resolves disputes after they occur by supplying interpretive authority at adjudication time is a compensatory response to the absence of that instrument. Both address the felt need; only one addresses the cause. The compensatory response consistently attracts more funding and adoption because disputes are legible events with willing payers at the moment of crisis, while the precision instrument requires investment before the crisis, distributed across parties who have not yet experienced the harm it would prevent. The same pattern appears in food safety: HACCP defines critical control points and operational thresholds before contamination occurs; product recalls and litigation respond after. In construction: precise load specifications and material standards are precision instruments; structural failure litigation is the compensatory response. In surgery: an operational checklist defining what "prepared for surgery" means is a precision instrument; malpractice suits are the compensatory response. In each domain the precision instrument is chronically underfunded relative to the remediation system it would render less necessary.

When a precision deficit is sufficiently entrenched, compensatory responses generate their own compensatory responses. Builders who meet code requirements without meeting quality standards exploit the gap between "code compliant" and "built well," because code compliance is falsifiable and quality is not. Home inspectors emerge as a compensatory response to that gap. Builders suppress inspectors through litigation. Inspectors develop workarounds to document failures without naming the responsible party. Each layer addresses the pressure generated by the previous layer without touching the original deficit. The distance between the gap and its visible symptoms grows until the causal connection becomes invisible and the symptoms are treated as independent problems requiring independent solutions. This is how precision deficits become permanent features of a landscape rather than correctable design errors: not because they cannot be fixed, but because the compensatory infrastructure built on top of them becomes more legible, better funded, and more politically defensible than the instrument that would make it unnecessary.

## 1.3 The precision-first alternative

The recursive layering described above is not a pathological edge case; it is the default trajectory of any precision deficit left unnamed. Each compensatory layer adds distance between the gap and its visible symptoms, until the causal connection disappears and the symptoms are treated as independent problems. Precision-first design interrupts this trajectory at the source. It treats definitional precision as a prerequisite for deployment rather than a remedy for failure. Before a rule can govern behavior, the terms of that rule must be operationally defined. Before a detection instrument can be deployed, it must specify what signal it is measuring and how that signal distinguishes the target state from adjacent states.

This is not a counsel of perfection. No specification is complete at first draft. The precision-first standard requires that the design process actively seeks and reduces precision deficits, that vague normative language triggers a correction process rather than acceptance, and that the system's measurement instruments are treated as primary artifacts, not secondary documentation.

# 2. The Precision-First Invariant

> ***Every element of a governed system must increase the precision with which the system's relevant dynamics can be observed, classified, and acted upon. A change that replaces a typed construct with a vague term, reduces the resolution of a detection instrument, obscures the boundary between distinguishable states, or substitutes normative language for operational definitions is a precision failure. Precision failures are design errors requiring correction, regardless of intent or ratification outcome.***

This invariant has six corollaries.

-   A term is operationally defined if and only if its presence or absence can be determined by an independent observer using only the definition and observable evidence. Terms that require interpretation by a privileged party are not operationally defined. The Wheel of Consent illustrates the corrective: by decomposing "consent" into a two-axis structure, it makes presence or absence determinable by an independent observer without access to the parties' intentions. OCAP and CARE apply the same move to "data sovereignty" and "ethical use" respectively.

-   A taxonomy is complete if and only if it specifies what falls outside all of its categories. A taxonomy that classifies everything within its stated scope but provides no mechanism for handling edge cases has hidden a precision deficit. Ostrom's eight design principles illustrate the corrective: they replace the holistic judgment "this is well-governed" with a partial order of independently checkable structural conditions, each of which specifies what satisfying and failing to satisfy it looks like.

-   A detection instrument is precise if and only if it can distinguish its target state from the most likely false-positive states. An instrument that cannot explain what it would not detect is not precise. The Adverse-Signal Engagement Principle (ASEP) Core Standard illustrates the corrective: by defining what counts as an adverse signal and what does not, it establishes the false-negative boundary explicitly, making it possible to determine not only what the instrument detects but what it would fail to detect and why.

-   A governance process is precise if and only if the conditions for initiating, continuing, and concluding the process are operationally defined. A process that depends on the good judgment of participants at critical junctures has substituted human discretion for structural precision. Ostrom's principles of monitored enforcement and graduated sanctions illustrate the corrective: each specifies the conditions for initiating a response, the criteria for its continuation, and the proportionality relationship between violation severity and sanction, removing discretion from the critical junctures where it is most exploitable.

-   A detection system is complete if and only if the failure to respond to a detection output is itself detectable without requiring the cooperation of the party that failed to respond. A system that can observe a failure but cannot observe its own governance inaction in the presence of that observation has an undocumented false-negative class at the interface between detection and response. Signal Escalation illustrates the corrective: by defining a time-governed state transition sequence through which unacknowledged detection outputs become progressively more visible and procedurally consequential, it makes governance inaction observable to an independent observer without requiring the inacting party to self-report. The escalation path converts elapsed time into escalating visibility, providing the base case that prevents infinite regress in recursive governance monitoring.

-   A specification is precise about its failure modes if and only if no critical property depends on a single defensive mechanism whose failure would leave that property entirely undefended. A critical property protected by only one mechanism has an undocumented failure mode: the failure of the mechanism itself. Defense-in-depth requires that critical properties be protected by independent, structurally distinct mechanisms such that the failure of any single mechanism is detectable by the others and does not collapse the property it was designed to protect. The Proof of Coordination protocol's Witness Layer illustrates the corrective: its three-tier architecture (event witnessing, pattern witnessing, governance witnessing) provides three structurally independent detection functions with different trust assumptions and different attack surfaces, so that capturing any single function is detected by the function above it. A specification that names a critical property and assigns it a single guardian has made a precision claim about the guardian's reliability without specifying the conditions under which that claim fails.

These corollaries apply to software specifications, contracts, governance protocols, standards documents, medical protocols, regulatory frameworks, and any other artifact that purports to coordinate or govern behavior.

The invariant is stated as an invariant rather than a preference because it derives from a structural condition, not a design philosophy. In systems that have trusted interpretive intermediaries (courts, regulators, arbitrators, credentialed experts with recognized authority), vague standards can function: the intermediary supplies precision at dispute time. Systems that lack this backstop, whether by design or by circumstance, face a different structural condition. In the absence of a trusted interpreter, ambiguity cannot be resolved after the fact. It can only be eliminated in advance. A vague standard in such a system is not merely imprecise; it is a permanently open gap. The precision-first invariant follows directly: in systems without trusted interpretive authorities, precision is non-optional.

# 3. Why Precision is Foundational, Not Supplementary

## 3.1 The gauge block analogy

In precision machining, a Johansson gauge block (also called a Jo block or slip gauge) is a ground steel block whose faces are manufactured flat and parallel to a tolerance measured in millionths of an inch. These blocks are not useful in isolation. Their value comes from a property called wringing: when two blocks are slid together with a slight twist, molecular adhesion causes them to stick, and a set of gauge blocks can be combined to produce any measurement to high precision. The set is self-verifying: each block can be calibrated against the others without an external authority.

A precision-first system works on the same principle. Each precisely defined framework is a ground surface. Frameworks interlock: a consent violation in one framework's terms produces a detectable signal in another framework's classification system. The system is self-calibrating because the standards are precise enough to verify each other. A system built from vague normative language has no equivalent interlocking property. Each standard floats independently, and failures fall between them.

There is a specific mistake this analogy helps name. A builder who achieves precision at one layer sometimes assumes that precision transfers upward without additional work, as if a precisely ground gauge block guarantees that the assembly built from it will be equally precise. It does not. Each new layer must specify its own tolerances, must verify that the joints between layers meet those tolerances, and must be calibrated against the layer below. Precision at layer N is a necessary but not sufficient condition for precision at layer N+1. The failure to treat each layer as requiring its own specification is a distinct class of precision error: not a deficit at the foundational layer, but an inheritance assumption that carries the deficit forward invisibly. Governance stacks, software architectures, and protocol specifications all exhibit this failure mode: a precise lower-layer standard is cited, the upper layer is treated as inheriting its precision by association, and the gap between them becomes the exploitable zone.

## 3.2 Precision enables detection; detection enables accountability

The causal chain from precision to accountability is direct. A precisely defined standard can be violated in a falsifiable way. A falsifiable violation can be detected. A detected violation can trigger a response. A response can be evaluated for proportionality against the violation. Accountability is the name for this whole chain operating correctly.

Remove precision from the first link and the chain does not merely weaken; it breaks. Vague standards can be violated without detection because no one can agree on what a violation looks like. Without detection, there is no accountability. The appearance of governance persists while its function disappears.

This is not an abstract concern. The accountability failures that motivated this standard, documented across governance systems, platform moderation, standards bodies, regulatory frameworks, and coordination protocols, were made possible by precision deficits in the systems that were supposed to prevent them. The precision deficit is not a symptom of governance failure; it is the mechanism.

## 3.3 Precision as a proactive strategy, not a bureaucratic overhead

A common objection to precision-first design is that it slows down development. This objection confuses upfront specification with bureaucratic overhead. The comparison class is not "no specification" but "specification now versus specification after the first governance failure." Post-failure specification includes the costs of the failure itself, the adversarial negotiation of the remedial definition, and the reputational damage to the system's credibility.

Precision-first design is, in expected-value terms, the cheaper path. It shifts specification effort from crisis response to design time, where it is less adversarial, less costly, and more likely to produce durable results. The objection that precision takes too long is, in most cases, a preference for deferring the cost rather than a genuine analysis of total cost.

There is a second, less obvious function of a named precision standard: it provides builders with structural permission to do upfront what they would otherwise only do reactively. In the absence of a shared standard, the designer who insists on operational definitions before deployment appears to be imposing overhead. The standard changes this. It gives the designer a reference: this is not personal preference; it is a named condition that any serious governed system must satisfy. Theodore Porter's historical analysis of quantification in public life makes this dynamic explicit. Precise, publicly legible standards substitute for personal trust; they allow accountability to function across actors who do not know each other and cannot rely on interpretive goodwill. This is the condition that many modern systems have created at scale, and that precision-first design addresses at the specification layer.

# 4. Five Frameworks That Instantiate Precision-First Design

The following frameworks are cited as exemplars of precision-first design because each replaces a vague normative concept with a typed, operationally defined construct. They are not the only such frameworks; they are examples of what precision-first specification looks like in practice. Each is briefly described with its precision contribution made explicit.

## 4.1 Ostrom's Design Principles for Commons Governance

**Source:** Ostrom, Elinor. *Governing the Commons.* Cambridge University Press, 1990.

Precision contribution: Replaces "good governance" with eight structural conditions, each independently checkable. A governance system either satisfies each condition or it does not; the determination is falsifiable.

The eight principles are: (1) clearly defined boundaries for the governed constituency; (2) congruence between rules and local conditions; (3) meaningful participation by those governed in rule modification; (4) monitoring by accountable parties using defined instruments; (5) graduated sanctions proportionate to violation severity; (6) structured conflict resolution mechanisms; (7) recognition of the constituency's right to self-govern; and (8) nested governance layers with foundational rules having the most robust constituency participation.

The precision contribution of Ostrom's framework is that each principle is a checkable structural condition, not a normative aspiration. A governance system can be evaluated against each of the eight conditions independently, and the result is a partial order of structural adequacy rather than a holistic judgment.

## 4.2 Wheel of Consent

**Source:** Martin, Betty. *The Art of Receiving and Giving: The Wheel of Consent.* Luminare Press, 2021.

Precision contribution: Replaces the single concept of "consent" with a two-axis measurement instrument that produces eight distinguishable interaction states, four consensual and four non-consensual.

The two axes are who is doing the action and who the action is for. Their intersection produces four quadrants: Serve (doing for another), Accept (receiving what another does for you), Take (doing for yourself), and Allow (permitting another to act for their own benefit). Each quadrant has a non-consensual shadow state that occurs when the action proceeds without explicit agreement.

The precision contribution is that "consent" is decomposed into a typed structure where each state is distinguishable from adjacent states. An interaction can be classified without reference to how it felt or what the parties intended; the classification depends only on the observable structure of who was doing and who it was for, and whether that structure was explicitly agreed. This makes consent analysis falsifiable in contexts where it previously depended on post-hoc interpretation.

## 4.3 OCAP

**Source:** First Nations Information Governance Centre. *OCAP Principles.* fnigc.ca.

Precision contribution: Replaces "data sovereignty" and "transparency" with four independently measurable axes: Ownership (who the data belongs to), Control (who decides how it is used), Access (who can see or retrieve it), and Possession (who physically or custodially holds it).

The precision contribution is that each axis can be satisfied or violated independently. A system can be fully transparent (Access is unrestricted) while still violating data sovereignty (Ownership and Control belong to parties other than the originating community). A system can satisfy Possession (the community holds its own data) while violating Control (an external party determines how it is used). The decomposition exposes combinations that a single-axis concept of "data sovereignty" would obscure.

OCAP applies wherever data moves between parties with different interests: software platforms handling user data, research institutions working with community-generated datasets, governance systems collecting participation records, and any system that produces outputs that travel beyond the originating constituency.

## 4.4 CARE Principles for Indigenous Data Governance

**Source:** Carroll, S.R. et al. "The CARE Principles for Indigenous Data Governance." *Data Science Journal,* 2020.

Precision contribution: Replaces "ethical use" with four typed obligations: Collective Benefit (outputs must benefit the originating community), Authority to Control (the community retains governance rights over its data), Responsibility (those using the data bear obligations to the community), and Ethics (use must align with community values and rights).

The precision contribution is that "ethical use" is decomposed into four independently evaluable conditions. A use of data can satisfy Collective Benefit while violating Authority to Control. A use can satisfy Ethics in the abstract while violating Responsibility by failing to discharge specific obligations to the originating community. The decomposition enables structured evaluation rather than holistic moral judgment.

CARE is particularly relevant for any system that aggregates individual participation records into collective outputs: reputation systems, coordination metrics, behavioral analytics, and governance participation records. In each case, the question is not merely whether the use is ethical in the abstract but whether each of the four conditions is met for the specific originating constituency.

## 4.5 The Adverse-Signal Engagement Principle: A Worked Example of the Conversion Process

Source: Chapman, Regis Lloyd (Durgadas). Adverse-Signal Engagement Principle (ASEP) Core Standard. v0.4.8, February 2026.

Precision contribution: Converts the vague principle "do not ignore warning signs" into a fully operational standard with typed inputs, three non-negotiable invariants, a three-phase processing loop with sub-obligations, and tiered adoption requirements.

The Adverse-Signal Engagement Principle is included here not as a fifth framework alongside Ostrom, Wheel of Consent, OCAP, and CARE, but as a demonstration of the conversion process that precision-first design requires. It shows the methodology in full: a vague normative principle enters, an operational standard exits. The vague input ("pay attention to warning signs") cannot be violated in a falsifiable way. The operational output (an adverse signal is a typed artifact with a defined scope, subject to three invariants and a three-phase lifecycle) can. This is the move that precision-first design makes repeatable: any vague normative principle that governs behavior in any system is a candidate for the same conversion.

The Adverse-Signal Engagement Principle also applies the precision-first standard recursively: failures of its own process are adverse signals under the same standard. A standard that is precise enough to detect its own violations is self-calibrating in the same way that a set of gauge blocks is self-calibrating. This property is a design goal, not an accident.

# 5. Applying Precision-First Design

## 5.1 Adoption levels

Precision-first design can be adopted at three levels of depth.

Level 1, auditing, involves reviewing an existing document, system, or process for precision deficits: terms that are normative but not operationally defined, detection instruments that cannot specify what they would not detect, and governance processes with unspecified discretion points. The output is a precision deficit map: a structured list of the places where accountability is structurally unenforceable in the current specification.

Level 2, remediation, involves resolving identified precision deficits by replacing vague terms with operational definitions, adding typed taxonomies to replace holistic judgments, and specifying the conditions for each discretionary decision point. The five frameworks in Section 4 are tools for remediation: each one provides a typed structure that can replace a class of vague normative language.

Level 3, design-time adoption, involves treating precision as a prerequisite for publication rather than a post-publication refinement. At this level, no element of a specification is considered complete until it is operationally defined. The test is: can an independent observer, using only this document and observable evidence, determine whether this condition is satisfied or violated?

## 5.2 The precision review checklist

Before publishing or deploying a governance rule, software specification, or standards document, the following questions should each have a yes answer.

-   Is every key term defined operationally, without reference to a privileged interpreter?

-   For each rule, is there a specified procedure by which a violation can be detected by an independent observer?

-   For each taxonomy or classification system, is there a specified procedure for handling edge cases that fall outside all existing categories?

-   For each detection instrument, is there an explicit specification of what signals it would not produce, to establish its false-negative boundary?

-   For each process, are the conditions for initiation, continuation, and conclusion operationally defined, or does the process depend on discretion at any step?

-   For each normative term (fair, reasonable, transparent, ethical, and similar), is there a typed decomposition that replaces the term with independently evaluable conditions?

A "no" answer to any of these questions identifies a precision deficit. The deficit should be resolved before publication, or flagged explicitly as a known gap with a specified timeline for resolution.

## 5.3 Precision-first in governance change processes

Governance change processes (amendment procedures, proposal systems, parameter updates, and analogues) are particularly susceptible to precision degradation over time. Each change introduces an opportunity to add vague language, collapse previously distinct categories, or substitute normative assertions for operational definitions.

A precision-first governance change process requires that each proposed change be evaluated against the following criterion: does this change increase or decrease the precision with which the relevant dynamics can be observed, classified, and acted upon? A change that increases precision is a structural improvement regardless of its surface subject. A change that decreases precision is a structural regression regardless of its stated purpose.

This criterion is not an obstacle to legitimate governance change. It is a filter that distinguishes changes that improve the system's measurement instrument from changes that degrade it. Governance bodies that internalize this filter tend to produce specifications that grow more precise over time rather than accumulating normative drift.

Precision failures have different complexity profiles, and the appropriate precision standard depends on where a process sits in its maturation trajectory. A precision failure in a well-understood process (ambiguous parameter specification where operational definition is achievable) is a straightforward deficit: the specification should be more precise and can be. A precision failure in an emergent process (premature specification that forecloses emergent understanding) is a different kind of error: over-precision that prevents learning. As practices mature from emergent to procedural, the expected precision level should increase correspondingly. A specification that is appropriately exploratory when a practice is new should become progressively more operationally defined as the practice matures. Governance change processes should therefore evaluate precision not only against a static standard but against the maturity of the process being specified: is this specification as precise as the current maturity level warrants, without being more precise than the maturity level can support?

## 5.4 Precision-first in software development

In software development, precision-first design maps onto familiar practices with a specific frame added. Requirements specifications should distinguish between operational definitions (what the system must be capable of detecting or producing) and normative aspirations (what the system should do in a value sense). Acceptance criteria should be stated in terms that an independent tester can evaluate without access to the original author's intent.

API contracts, data schemas, and event taxonomies are precision instruments. A schema that uses a string type where a typed enum is possible has introduced a precision deficit. A taxonomy that has an "other" or "miscellaneous" category without a specified overflow procedure has deferred a classification decision that will become a dispute.

Error handling is a precision domain. A system that logs errors as "unexpected error" without classification has reduced its own observability. A system that distinguishes error classes by their structural signature, their detectability at different layers, and their recovery procedures is operating at a higher precision level and will be easier to monitor, audit, and improve.

# 6. Precision Failures: Recognition and Response

The following patterns are recognizable precision failures. Each is described with its structural signature and the typical response it enables.

## 6.1 Normative substitution

Pattern: A typed construct is replaced with a normative term. Example: "the system must provide meaningful transparency" replaces "the system must publish X, Y, and Z in format F within T days." Structural signature: the new term cannot be violated in a falsifiable way. Response: identify what the normative term was intended to require, decompose it into independently evaluable conditions, and specify each condition operationally.

## 6.2 Category collapse

Pattern: Two previously distinct categories are merged, either explicitly or by treating them as interchangeable in practice. Structural signature: cases that were handled differently under the prior taxonomy are now handled identically, but the cases are not identical. Response: restate the distinction, specify the criterion for assignment to each category, and retroactively classify the merged cases.

## 6.3 Discretion point accumulation

Pattern: Over successive revisions, a process accumulates unspecified discretion points where the outcome depends on the judgment of a particular party. Structural signature: the process description uses language like "as appropriate," "at the committee's discretion," or "subject to review" without specifying the criteria for the discretionary determination. Response: for each discretion point, either specify the criteria operationally or explicitly acknowledge it as a zone of principled discretion and specify the accountability structure for that zone.

## 6.4 Detection instrument degradation

Pattern: A detection instrument is modified so that its sensitivity decreases or its false-negative rate increases, without acknowledging this as a change to the system's measurement capability. Structural signature: the modified instrument would not detect events that the prior instrument would have detected, but the change is framed as a refinement rather than a reduction. Response: require that any change to a detection instrument include a specification of its false-negative boundary before and after the change.

## 6.5 Inheritance without specification

Pattern: A document or system claims to inherit or comply with a standard without specifying which provisions apply, how they map to the local context, and how compliance is determined. Structural signature: the inheritance claim is not falsifiable because there is no operational specification of what compliance requires. Response: require that any inheritance claim include an explicit mapping from the inherited standard's provisions to the local system's elements, with operational compliance criteria for each.

# 7. Relationship to Existing Standards and Frameworks

Standards bodies have been producing governance and specification standards for over a century. ISO, IEEE, W3C, NIST, and their domain-specific equivalents have generated frameworks of value, many of which exhibit high precision within their defined scope. This standard does not compete with them. It provides a meta-criterion for evaluating any of them: how precisely does this standard define the dynamics it governs, and where does it leave accountability structurally unenforceable?

The need for that meta-criterion is not historical. It is structural, and it is recent. Existing standards bodies were designed for contexts in which trusted interpretive intermediaries exist: courts that can resolve ambiguous contract terms, regulators that can supply operational definitions at enforcement time, credentialed professionals whose judgment fills gaps that written standards leave open. In those contexts, a standard that is primarily normative can function because the interpretive infrastructure supplies precision where the document does not.

Many modern systems operate without that infrastructure, whether by design or by circumstance. Decentralized protocols remove it by architectural choice. Cross-jurisdictional systems outscale it. Rapidly evolving domains (AI governance, platform regulation, coordination protocol design) outpace the interpretive institutions that would normally supply precision. A standard that depends on trusted interpretation to function is not a standard in environments where that interpretation is unavailable; it is a placeholder that defers the accountability question to whoever manages to occupy the interpretive role. Theodore Porter's historical analysis of quantification makes this dynamic explicit: precise, publicly legible standards emerge as a necessity precisely where trusted interpretive communities are absent. A meta-criterion that makes precision itself a prerequisite is the appropriate response to that structural gap, not a refinement of existing compliance frameworks.

What this looks like in practice differs by domain. In decentralized governance, the deficit appears as decision rules that cannot be violated in a falsifiable way, classification gates controlled by interested parties, and normative terms that argue both sides of any dispute without resolution. In software specification, it appears as acceptance criteria that depend on the original author's intent, error taxonomies with unspecified overflow, and interface contracts that use loosely typed definitions where precise typed enums are possible. In legal drafting, it appears as obligations that require a privileged interpreter to determine whether they have been met, and dispute resolution clauses that defer to judgment at precisely the moment when judgment is most contested. In medical protocol design, it appears as clinical guidelines that specify interventions without specifying the observable criteria for initiating or discontinuing them. In each case the structural signature is the same: a precision deficit creates pressure, the pressure generates compensatory responses, and the responses become load-bearing before the deficit is named. This standard provides the instrument for naming it.

# 8. Adoption and Attribution

This standard is offered for adoption by any team, organization, legal drafter, or standards body in any domain where accountability gaps are traceable to precision deficits. Adoption does not require acknowledgment of this document, though attribution to the underlying frameworks (Ostrom, Martin, FNIGC, Carroll et al.) should follow the citation practices of the adopting domain.

Organizations that adopt this standard are encouraged to produce a precision deficit map of their existing specifications (see Section 5.1, Level 1 adoption) as their first action. This map creates a baseline against which future precision improvements can be measured.

Adoption of this standard in conjunction with a formal governance change process should include the precision criterion from Section 5.3 as an explicit evaluation criterion for all proposed changes. This prevents normative drift over time by building precision maintenance into the change process itself.

# 9. Inheritance Clause

Documents and systems that adopt this standard may include the following statement to make their adoption explicit:

> ***Precision-First Inheritance: This document adopts the Precision-First Design Standard (v1.3, February 2026). Every element of this document is subject to that standard. Any revision that reduces definitional precision, replaces typed constructs with vague terms, collapses previously distinguishable states, or makes a falsifiable claim unfalsifiable is a design error requiring correction, not a legitimate exercise of governance or editorial discretion.***

The inheritance clause is optional for general adoption. It is recommended for governance documents, standards specifications, and any system where the precision-first commitment needs to be enforceable against future revision.

# 10. From Precision to Metrology

This document is a precision standard. Its larger ambition is metrological.

Precision is a property of a single instrument or definition: how finely can this discriminate? Metrology is the discipline of establishing, maintaining, and relating measurement standards so that they are mutually consistent, traceable, and transferable across contexts without requiring the presence of the originating practitioner. Precision is necessary for metrology, but not sufficient. A precise instrument that no one else can replicate or calibrate against is not yet metrological infrastructure.

Historians of physical measurement have documented the same sequence at each stage of industrial and scientific development: a precision instrument appears, solves a local problem, and then becomes the foundation for a broader discipline of measurement only when it is standardized, named, and made transferable. Simon Winchester's account of precision manufacturing (The Perfectionists, 2018) argues that every major technological advance was gated by a prior advance in measurement precision: you cannot make what you cannot measure. Ken Alder's account of the creation of the metric system (The Measure of All Things, 2002) shows that standardized measurement is a social and political achievement, not merely a technical one: its defining purpose was to make a measurement taken by one person in one place mean the same thing to a different person in a different place, without requiring personal trust between them.

Modern systems have completed one half of this transition in some domains. Cryptographic protocols applied precision to transactions: zero-knowledge proofs, trustless execution, deterministic state machines. A transaction either occurred or it did not; the determination requires no trusted interpreter. The result is that anyone, anywhere, using only the public record, can verify a transaction with the same result. That is metrology: a measurement standard that transfers across actors and contexts without requiring interpretive authority.

Governance, coordination, and accountability remain in a pre-metrological state across most domains: judgment-dependent, context-local, irresolvable without trusted insiders. The gap has been invisible precisely because its costs are attributed to human nature, bad actors, and politics rather than to missing instruments. You cannot see what you cannot measure, which means you cannot see the absence of the instrument that would do the measuring.

This standard is designed to begin the transition in the domains where that gap is most consequential. The goal is not a single standard for a single system. It is a metrological discipline for accountability: a shared reference framework precise enough to allow measurements taken in one context to mean the same thing in another, to allow accountability to function across actors who do not share history or trust, and to allow the chronic failures of governed systems to be diagnosed as instrument deficiencies rather than endured as human constants.

That is the ambition this standard is built toward.

# 11. Relationship to the Structural Integrity Tetrad

This standard is one of four standalone standards that form the structural integrity tetrad: the Precision-First Design Standard, the Adverse-Signal Engagement Principle Core Standard, the Structural Consent and Legibility Standard, and the Information Asymmetry Classification Standard. Each standard addresses a distinct failure mode. Each is independently valid: no standard requires the others for its own validity. Together, they form a reinforcing set. A system that satisfies all four has addressed the structural conditions under which accountability failure becomes predictable.

Systems adopting any one of the four standards at its highest adoption level are strongly recommended to adopt all four. The designation "structural integrity tetrad" applies to systems that adopt all four standards at their highest respective tiers. The tetrad designation is descriptive, not a separate certification: a system either satisfies all four standards at their highest level or it does not. Cross-references between the standards are recommendations, not requirements.

The Proof of Coordination protocol is one system that adopts all four standards. It is not the only possible adopter; the standards are designed for independent adoption by any system in any domain.

# References

Carroll, S.R., Herczog, E., Hudson, M., Russell, K., and Stall, S. "The CARE Principles for Indigenous Data Governance." *Data Science Journal* 19(1): 43, 2020. https://doi.org/10.5334/dsj-2020-043

First Nations Information Governance Centre. *OCAP Principles.* Ottawa: FNIGC, 2014. fnigc.ca.

Martin, Betty. *The Art of Receiving and Giving: The Wheel of Consent.* Luminare Press, 2021.

Ostrom, Elinor. *Governing the Commons: The Evolution of Institutions for Collective Action.* Cambridge University Press, 1990.

Alder, Ken. *The Measure of All Things: The Seven-Year Odyssey and Hidden Error That Transformed the World.* Free Press, 2002. : Documents the creation of the metric system as a social and political project to make measurement transferable across actors without requiring personal trust.

Porter, Theodore M. *Trust in Numbers: The Pursuit of Objectivity in Science and Public Life.* Princeton University Press, 1995. : Argues that precise quantitative standards substitute for personal trust in contexts where trusted interpretive communities are absent or distrusted. Provides direct theoretical grounding for the necessity of precision standards in systems without interpretive authority.

Winchester, Simon. *The Perfectionists: How Precision Engineers Created the Modern World.* HarperCollins, 2018. : Traces the role of measurement precision as the enabling condition for each successive wave of technological development, from the Industrial Revolution to microelectronics.

# Changelog

v1.3.0 (February 2026): Domain-general reframe. Repositioned the standard as applicable to any specification domain, not primarily coordination systems. Updated subtitle from "A Transferable Standard for Coordination Systems, Governance Protocols, and Software Design" to "A Transferable Standard for Specification Domains." Broadened abstract and Section 1 framing so that coordination systems are one example domain among several (medical protocols, legal drafting, software specification, regulatory frameworks). Replaced "coordination or governance system" with "governed system" in the invariant statement (Section 2). Added medical protocol design as an example domain in Section 7. Updated Section 4 heading from "Four Frameworks" to "Five Frameworks" to reflect the existing five subsections. Updated adoption level cross-reference in Section 5.1 from "four frameworks" to "five frameworks." Added Section 11 (Relationship to the Structural Integrity Tetrad), replacing the prior triad reference with the tetrad designation that includes the Information Asymmetry Classification Standard. Removed self-reference to "Internal PoC Protocol Stack Edition" from bibliography. Replaced "genuinely useful" with "practically useful" in Section 1.2 (document rule compliance). Replaced Cynefin-specific language in Section 5.3 with domain-general maturity language; the Cynefin-specific application is documented in the Sensemaking Layer Standard. Updated Adverse-Signal Engagement Principle Core Standard version reference in Section 4.5 from v0.4 to v0.5. No changes to normative content: the invariant, six corollaries, five precision failure patterns, three adoption levels, precision review checklist, and inheritance clause are unchanged.

v1.2.4 (February 2026): Added sixth corollary (defense-in-depth) to Section 2, establishing that a specification is precise about its failure modes only if no critical property depends on a single defensive mechanism whose failure would leave that property undefended. Critical properties require independent, structurally distinct mechanisms such that the failure of any single mechanism is detectable by the others. Witness Layer three-tier architecture cited as illustrative corrective. Updated corollary count from five to six in abstract, Section 2, and v1.0 changelog entry. Renamed "Signal Maturation" to "Signal Escalation" throughout (fifth corollary text, v1.2.2 changelog entry) per cross-document rename propagation. Source: Developmental Signal Paper drafting session, architectural observation; Witness Layer Technical Paper, Section 2.

v1.2.3 (February 2026): Added Cynefin domain circuit note to Section 5.3 (Precision-first in governance change processes). Precision failures have different profiles by Cynefin domain, and the expected precision level should track domain maturation: appropriately exploratory in Complex domain, progressively more operationally defined as the practice matures through Complicated to Clear. Cross-references: Witness Layer Technical Paper, Section 5.1; Structural Consent and Legibility Standard, Section 6.4.

v1.2.2 (February 2026): Added fifth corollary (Signal Escalation) to Section 2, establishing that a detection system is complete only if governance inaction in the presence of a detection output is itself detectable without the cooperation of the inacting party. Updated corollary count from four to five in abstract, Section 2, and v1.0 changelog entry.

v1.2.1 (February 2026): Cross-document consistency fixes. Corrected ASEP document name in Section 4.5 source line (was "Adverse Signal and Escalation Protocol"; corrected to canonical name). Updated inheritance clause template version from v1.0 to v1.2. No changes to normative content.

v1.2 (February 2026): Rewrote abstract to foreground compensatory response argument, trustless derivation, and metrological ambition. Added bridging sentences to Section 1.3 connecting recursive layering argument (1.2) to precision-first alternative. Added transfer error paragraph to Section 3.1 naming the layer-N-to-N+1 inheritance assumption as a distinct precision failure class.

v1.1 (February 2026): Added structural asymmetry argument (Section 1.2); derivation of invariant from the absence of trusted interpretive intermediaries (Section 2); Porter grounding and permission argument (Section 3.3); ASEP as worked example of the conversion process (Section 4.5); new closing section on precision and metrology (Section 10); expanded bibliography (Alder, Porter, Winchester).

v1.0 (February 2026): Initial release. Establishes the precision-first invariant, six corollaries, three adoption levels, precision review checklist, five precision failure patterns, and the inheritance clause.
