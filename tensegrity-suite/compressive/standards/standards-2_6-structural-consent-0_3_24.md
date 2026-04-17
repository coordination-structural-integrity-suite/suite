Structural Consent Legibility Standard

**Version:** v0.3.24

**Date:** 2026-04-17

**Author:** Regis Chapman (Durgadas)

**Status:** Working draft. Invariants, domain architecture, bandwidth
framework, detection architecture, and standing evaluation are
specified. OCAP/CARE integration layer is specified. Empirical
calibration of detection thresholds and complexity-domain time windows
requires pilot data.

**Companion Standards:** This standard is designed for use alongside the
Precision-First Design Standard and the Adverse-Signal Engagement
Principle Core Standard. See Section 7.5 for the Tensegrity Compressive Standards within the Coordination Structural Integrity Suite
architecture. Each companion standard is independently adoptable; joint
adoption at the highest tier of each constitutes the Tensegrity Compressive Standards within the Coordination Structural Integrity Suite.

1\. Purpose

Every governance system claims to act with the consent of its participants. Very few can demonstrate it. The gap between claimed consent and verifiable consent is not a philosophical distinction. It is the structural condition through which extraction operates inside systems designed to prevent it.

Consent in most governance systems gets reduced to a voting threshold: enough participants voted yes, so the change is authorized. But the question this standard addresses is different. Who was acting? Who benefited from the action? When these questions are unanswerable from the governance record, participants have no structural basis to verify whether the consent claimed on their behalf was genuine. Without that basis, the system can authorize decisions that benefit decision-makers at the expense of governed parties, and the governed parties have no structural vocabulary to name what happened.

For how this standard relates to others in the Coordination Structural Integrity Suite, and guidance on which standards to combine for specific organizational purposes, see the Suite Integration Guide and the Suite Deployment Contexts document.

Non-harming is the first precision principle of the Coordination Structural Integrity Suite. The Precision-First Design Standard is the meta-standard for the suite: every standard in it is a precise specification of what non-harming requires in a specific coordination domain. The lack of structural consent legibility produces specific harms to specific people: extraction operates inside systems that claim consent-based coordination, without participants having any structural basis to verify that the consent claimed on their behalf is genuine; coordination decisions that benefit decision-makers at the expense of the affected participant population proceed because the distinction between who is acting and who benefits from the action is invisible in the coordination record; and participants bear the costs of systems they cannot exit, cannot effectively challenge, and cannot verify are operating in their interests. This standard specifies two-axis consent legibility as the precise structural answer: an architecture that makes the 'who is acting' and 'who benefits from the action' questions independently answerable from the record.

Every coordination system claims to act with the consent of its participants. Almost none can prove it. The gap between claimed consent and structural consent is not a philosophical distinction. It is the mechanism through which extraction operates inside systems that were designed to prevent it.

Consent in most coordination systems is reduced to voting: a numerical
threshold is met, and the change is deemed authorized. This standard
establishes a higher bar. Drawing on Betty Martin's Wheel of Consent
framework, it requires that every consent-bearing interaction be
structurally legible along two axes: who is acting, and who benefits
from the action. When these two questions are not answered, or when the
answers are obscured, the interaction operates in a shadow dynamic that
may be invisible to the system's participants but is structurally
detectable.

No widely deployed coordination mechanism fully satisfies this standard's
requirements. Token-weighted voting, delegated authorization, optimistic
approval, and on-chain permission systems all fail to answer the "who is
it for" axis and cannot structurally distinguish proposals that benefit
the voting body from proposals that benefit the governed constituency.
Regulatory consent frameworks address revocability but produce enduring
at scale through consent fatigue. This standard addresses that gap
across all of these contexts.

The standard is transferable. It is designed for adoption by any
coordination system or organization that needs to verify that consent is
structurally present, not merely claimed. Adoption
tiers (Section 5) allow organizations to adopt the standard at the level
appropriate to their operational context.

**Typological declaration** (Descriptive Typology Map v0.1.1)

*Operative classes*
- Relational-topological: This standard operates primarily in this class. Consent is a structural property of the relationship between parties: who is acting and who benefits from the action. The two-axis framework decomposes every consent-bearing interaction into independently assessable relational properties, making the structural topology of consent visible to an independent observer.
- Epistemic-perceptual: This standard operates in the precision and operationalization sub-aspect: making consent independently verifiable by decomposing it into observable structural axes. It also addresses detection: specifying how shadow dynamics become structurally visible.

*Boundary classes*
- Felt-experience: This standard assesses structural consent legibility, not experienced consent. Structural legibility is necessary but not sufficient for consent that is genuinely experienced as free, fair, and accessible. What a participant experiences inside a structurally legible consent transaction is outside this standard's vocabulary; it is the class where structural legibility ends and lived experience begins.
- Structural-mechanical: This standard does not address how consent misalignment generates structural loads in the tensegrity configuration, modifies pre-stress distribution, or creates exploitation vectors at the configuration level.
- Temporal-dynamic (frequency-dynamic sub-aspect): This standard addresses structural conditions for consent legibility but not how consent architecture responds to the frequency or rhythm of coordination pressure over time.

2\. Foundational Framework: The Wheel of Consent

This standard adopts Betty Martin's Wheel of Consent as its foundational
consent framework. The four-quadrant model and shadow dynamics are
Martin's original contribution, cited here with attribution. The
application of this framework to coordination systems and protocols, and data sovereignty, including the five consent domains and
the structural verification architecture defined in this standard, is
original to this standard.

2.1 The Two Axes

Every consent-bearing interaction involves two questions asked
simultaneously:

**Who is doing?** (The action axis.) One party acts; the other is acted
upon.

**Who is it for?** (The benefit axis.) The action benefits one party;
the other party provides the gift that makes the action possible.

These two axes are independent. The party acting is not necessarily the
party benefiting. Conflating them (assuming that the actor is always the
beneficiary, or that the acted-upon party is always the beneficiary) is
the structural root of most consent failures.

**Cost-bearing party identification.** The two-axis framework identifies who acts and who benefits. A structural supplement is required to identify who bears the cost. In any consent-bearing interaction, costs — risk, expenditure, constraint, or negative consequence — are distributed among parties. The cost-bearing party may be the acting party, the benefiting party, or a third party who is structurally outside the two-axis interaction but materially affected by it. When the cost-bearing party is distinct from both the acting party and the benefiting party, the consent architecture must identify the cost-bearing party explicitly and obtain their consent to the cost distribution before the action proceeds. Failure to identify the cost-bearing party is a consent failure even when both axes of the Wheel of Consent are fully satisfied: an action that is structurally legible on the who-acts and who-benefits questions but obscures who bears the cost operates in a shadow dynamic for the cost-bearing party, regardless of how clearly the action and benefit axes are answered.

2.2 The Four Quadrants

The intersection of the two axes produces four consent dynamics:

**Serving.** You are acting, and the action is for the other party's
benefit. Your gift is your action. The other party's role is to accept
what they asked for. The virtue of this quadrant is generosity: acting
within your limits for another's benefit. The key constraint is that you
must know your own limits; serving beyond your capacity produces the
shadow dynamic.

**Taking.** You are acting, and the action is for your own benefit. The
other party's gift is access. Their role is to allow what you asked for.
The virtue of this quadrant is integrity: knowing what you want and
asking for it clearly. The key constraint is that you must respect the
other party's limits; taking beyond what was allowed produces the shadow
dynamic.

**Accepting.** The other party is acting, and the action is for your
benefit. Their gift is their action. Your role is to receive what you
asked for. The virtue of this quadrant is surrender: trusting another to
act on your behalf. The key constraint is that you must actually ask for
what you want, not just what you think you should want.

**Allowing.** The other party is acting, and the action is for their
benefit. Your gift is access to you. Your role is to permit what they
asked for, within your limits. The virtue of this quadrant is trust:
permitting another to act for their own benefit in a way that affects
you. The key constraint is that you must set limits; allowing without
limits produces the shadow dynamic.

2.3 Shadow Dynamics

Each quadrant has a corresponding shadow: the same action performed
without consent, or with consent that was not structurally valid.

**Serving without agreement: martyrdom.** Acting for another's benefit
beyond your own limits, producing resentment. The action looks generous
but is structurally unsustainable.

**Taking without agreement: stealing.** Acting for your own benefit
without the other party's authorization, or beyond the authorization
given.

**Accepting without agreement: entitlement.** Receiving another's action
as though it were owed, without negotiation or acknowledgment.

**Allowing without agreement: enduring.** Permitting another's action
beyond your limits because you do not feel able to refuse, producing
silent suffering.

Martin's critical insight: the shadows are not aberrations. They are
adaptive survival mechanisms, learned in childhood and reinforced by
systems that reward compliance over self-knowledge. Individuals and
organizations default to shadow dynamics when they lack the capacity (or
the structural support) to perceive and act on the distinction between
what they want and what they are willing to do.

2.3.1 Structural Test for Consent Validity

Three cross-cutting structural features distinguish consent from shadow
dynamics across all four quadrant types. These features constitute the
standard's structural test for whether an interaction operates inside
the circle of consent or in a shadow dynamic.

**Negotiated limits.** Non-shadow dynamics have explicit boundaries that
the consenting party sets and maintains. Shadow dynamics operate without
negotiated limits or beyond the limits that were set. Serving without
agreed limits becomes martyrdom. Allowing without set limits becomes
enduring. The presence of explicit, negotiated boundaries is the first
structural indicator of valid consent.

**Bidirectional awareness.** Non-shadow dynamics require both parties to
know who is doing and who it is for. Shadow dynamics obscure one or both
axes. When the beneficiary of a coordination action is hidden (stealing)
or when the person acted upon does not know the action is for the other
party's benefit (enduring), the bidirectional awareness test fails. The
system must be able to verify that both axes were legible to both
parties at the time of the interaction.

**Revocability.** Non-shadow dynamics can be withdrawn: the serving
party can stop serving, the allowing party can revoke access. Shadow
dynamics persist because the cost of withdrawal is structurally
prohibitive. When a participant cannot revoke consent without incurring
costs that exceed the benefit of participation, the interaction has
moved from the consent quadrant to its corresponding shadow. The system
must verify that withdrawal is structurally feasible, not merely
formally permitted.

A detection architecture implementing this standard instruments all
three features. The absence of negotiated limits in high-service
contexts, the absence of bidirectional awareness in self-benefiting
coordination actions, and the structural infeasibility of withdrawal in
nominally consensual participation are the shadows' structural
fingerprints.

2.3.2 External Legal Override as Structural Threat

A distinct class of consent failure is produced not by parties' failure of capacity or consent architecture, but by the imposition of external legal requirements that override the explicit consent arrangements within the coordination system. Securities law may classify participation tokens in ways that impose obligations participants did not consent to. Employment and labor law may impose obligations on contributors who participated under different terms. Territorial data requirements may override data sovereignty arrangements that were explicitly consented to. Anti-money-laundering and know-your-customer requirements may impose surveillance obligations that participants did not agree to when they joined the system.

This shadow dynamic differs from the four quadrant-generated shadows: it is externally imposed rather than generated by the parties' relationship. Neither party's failure of consent practice produces it. The structural threat is that participants believe they have consented only to what is in the coordination documents, while external legal frameworks impose material obligations that were not in those documents and that participants did not structurally choose.

The consent architecture must name this threat explicitly for the adopting context, identify which external legal jurisdictions apply, and specify how the organization addresses the gap between its explicit consent architecture and externally imposed obligations. Absence of this disclosure is a consent legibility failure: participants cannot evaluate what they are consenting to if the consent architecture does not acknowledge the legal constraints that can override parts of it.

2.4 The Circle of Consent

The Wheel's circle represents the consent agreement. Inside the circle,
gifts are given and received within negotiated limits. Outside the
circle, the same actions become their shadows. The structural difference
is the presence or absence of a clear, mutual agreement about who is
doing and who it is for.

This standard operationalizes the circle: a system satisfying this
standard makes the consent boundary structurally legible and detectable,
so that shadow dynamics can be identified rather than hidden.

3\. Invariants

Across all implementations and domains, this standard requires:

3.1 Identify

**Prior condition: action specification.** The Identify invariant presupposes that the action being consented to has been specified with sufficient precision for affected parties to evaluate whether they are materially affected. A standing claim cannot be properly made or evaluated against an underspecified action. "Approving the coordination proposal" is not a sufficient action specification for standing evaluation; "approving the coordination proposal that alters fee distribution in the following way" is. When an action is specified only at a category level — "the committee is authorized to make fee decisions" — the affected constituency cannot be identified in advance, and the Identify invariant cannot be satisfied before the action proceeds. Systems that use category-level authorization as a substitute for per-action consent must specify the conditions under which a specific action within the authorized class triggers a standing evaluation, and must perform that evaluation before the specific action proceeds.

For any consent-bearing action, the affected constituency must be
identified before the action proceeds. "Affected constituency" means the
set of participants whose coordination standing, coordination records,
data sovereignty, participation terms, or observation exposure would be
materially altered by the action.

Identification must be evidence-based where system evidence exists.
Self-identification of standing is permitted; standing claims are
subject to structured evaluation and challenge.

The absence of standing claims from parties who should be affected
(based on available system evidence) is itself an adverse signal,
subject to Adverse-Signal Engagement Principle processing.

3.1.1 Standing Evaluation Mechanism

The standing evaluation mechanism combines four elements:
self-identification (low barrier to entry), evidence-backed evaluation
(claims assessed against system data), implausible absence detection
(monitoring for expected claims that do not appear), and distributed
evaluation (the evaluation function is not concentrated in a single
actor).

Self-identification ensures that unexpected affected parties can
surface. Any party may claim standing for any consent-bearing action.
The system does not pre-screen who is "really" affected; it evaluates
claims after they are made.

Evidence-backed evaluation applies three criteria to each standing
claim. First: is there system evidence that this party's coordination
standing, coordination records, data sovereignty, participation terms,
or observation exposure would be materially altered by the action?
Second: if the claimant self-identifies without system evidence, is the
claim plausible given the action's scope? Third: if a party who should
be affected has not claimed standing, what structural factors might
explain the absence (information asymmetry, bandwidth constraints, exit
costs)?

Implausible absence detection addresses a failure mode that no analogous
system handles well. The detection layer monitors for parties who should
be affected based on available system evidence but have not claimed
standing. The absence is processed as an adverse signal through Signal
Escalation: it may indicate information asymmetry (the party does not
know about the action), bandwidth constraint (the party cannot evaluate
whether they are affected), or structural coercion (the party knows they
are affected but the cost of claiming standing is prohibitive).

Distributed evaluation ensures that the standing assessment function is
not concentrated in a single evaluator. Multiple evaluators assess
standing claims, with the detection layer serving as the integrity check
on the evaluation process itself. This design draws on the Internet
Engineering Task Force's rough consensus model, where the working group
chair evaluates objection quality rather than counting votes, but
distributes the evaluation function to avoid the single-point-of-failure
that the Internet Engineering Task Force model creates when chairs have
unchecked discretion.

3.1.2 Constituency Definition as Structural Precondition

The per-action identification requirement in Section 3.1 presupposes
that the governing system maintains a durable, accessible definition of
who holds participation rights and on what basis. Without this
definition, the identification requirement cannot be fully satisfied: an
affected constituency cannot be identified against a reference that does
not exist. A system that performs per-action identification without a
persistent constituency definition is identifying parties against an
implicit, unspecified reference, which is not structurally legible.

The durable constituency definition must satisfy three conditions.
First, it must be accessible to any party asserting standing, without
requiring access from parties holding more authority. Second, it must be
durable: the definition cannot be modified unilaterally by parties
holding concentrated authority; any modification that alters who holds
participation rights is a coordination consent action requiring the
Authorize invariant as applied to the affected constituency whose
standing is altered. Third, it must be specific enough that an
independent observer can determine whether any given party holds
participation rights, without access to the author's intent or
unpublished context.

The absence of a durable constituency definition is itself a consent
architecture failure: it prevents the Identify invariant from being
satisfied structurally rather than merely procedurally. Ostrom's first
design principle (clearly defined boundaries for the governed
constituency) identifies this as a precondition for sustainable commons
governance; this section makes it a structural consent requirement.

3.2 Authorize

The affected constituency must have a meaningful opportunity to
authorize or refuse the action. "Meaningful" requires that the four
system obligations specified in Section 6 are satisfied: legibility,
time, support, and exit/objection cost. In addition:

The authorization mechanism answers both Wheel of Consent questions: who
is acting, and who benefits.

Authorization that excludes affected parties, or that includes
unaffected parties whose participation dilutes the affected
constituency's voice, is a consent failure.

Silence, inaction, and the absence of objection are not consent. Systems
must structurally distinguish between "authorized," "not yet responded,"
and "unable to respond."

3.3 Verify

Consent is not a one-time event. Systems must be able to verify, after
the fact, that consent was structurally valid at the time it was given.
Verification requires that:

The consent record identifies who acted, who benefited, who was
affected, and what the agreed limits were.

The consent record is durable and tamper-evident (consistent with the
Adverse-Signal Engagement Principle's durable logging requirement).

Shadow dynamics are detectable: the system can identify when an action
that was nominally consented to actually operated in a shadow quadrant
(e.g., a ratification that met quorum but benefited the voting body at
the expense of the governed constituency).

3.4 Consent Failures as Adverse Signals

A consent process that produces any of the following is an adverse
signal subject to the Adverse-Signal Engagement Principle:

Unanimous agreement in a domain where disagreement is normal
(implausible absence of dissent).

Authorization by a body that benefits from the action at the expense of
the affected constituency (Wheel of Consent violation: the action is
"for" the acting body, not the affected constituency, but is framed as
service).

Affected parties who were not notified, could not participate, or lacked
the bandwidth to evaluate what they were consenting to.

Silence treated as consent without explicit, prior opt-in to that
interpretation.

A standing claim that is implausible given available system evidence.

The implausible absence of a standing claim from a party who should be
affected.

4\. Consent Domains

This standard recognizes five domains in which consent operates. Systems
adopting this standard must identify which domains are relevant to their
operations and satisfy the invariants (Section 3) in each relevant
domain.

4.1 Coordination Consent

Changes to rules, parameters, structures, and decision-making processes.
The Wheel of Consent test: who is proposing the change, and who benefits
from ratification?

Shadow dynamics in this domain: a coordination body that ratifies changes
benefiting itself at the constituency's expense (entitlement/stealing);
participants who endure coordination outcomes they did not meaningfully
consent to because the cost of exit or objection is too high (enduring);
coordination service that exceeds the server's capacity, producing
resentment-driven gatekeeping or burnout (martyrdom).

Relationship to OCAP: Authority to Control. Relationship to CARE:
Authority to Control, Responsibility.

4.2 Data Consent

What data is collected, who sees it, how it is used, and how long it is
retained. The Wheel of Consent test: who is collecting the data, and who
benefits from the collection?

Shadow dynamics in this domain: data collection framed as service to the
data subject but primarily benefiting the collector or third parties
(stealing disguised as serving); data subjects who permit collection
beyond their comfort because they see no alternative (enduring); systems
that treat data access as an entitlement rather than a negotiated gift
(entitlement).

Three patterns characterize the current landscape across coordination
contexts. Systems that grant access to individual interactions without
bounding the scope of profile construction that aggregated access
enables fail the Data consent test: users consent to individual
visibility but not to what that visibility makes possible in aggregate.
Zero-knowledge and selective-disclosure architectures represent the
strongest current approach to Data consent, because the disclosing party
controls what is revealed, but they commonly leave metadata leakage
unaddressed in the Observation consent domain. Regulatory frameworks
(such as GDPR and CCPA) are strong on consent revocability but produce
enduring at scale through consent fatigue: mandatory consent interfaces
function as structural coercion when the practical cost of refusal is
exclusion from necessary services. No existing approach adequately
addresses cross-domain consent interactions.

Relationship to OCAP: Ownership, Control, Access, Possession (all four
elements). Relationship to CARE: Collective Benefit, Ethics.

4.3 Participation Consent

Entry into, ongoing terms of, and exit from a system or organization.
The Wheel of Consent test: who set the participation terms, and who
benefits from the participant's presence?

Shadow dynamics in this domain: participants who remain in a system
beyond their limits because switching costs make exit structurally
impractical (enduring); systems that extract value from participants
while framing participation as a benefit to the participant (stealing
disguised as serving); participants who serve the system beyond their
capacity because the culture rewards overcommitment (martyrdom).

4.3.1 Delegation Scope

When an individual enters a system, the entry terms must specify what
consent authority is delegated to the organizational layer, in which
domains, and for what purposes. Delegation without specification is a
consent failure.

A delegation scope statement must identify: which consent domains the
organizational layer may act in on the participant's behalf, what types
of actions are within scope (e.g., parameter changes within the current
framework vs. structural changes to the framework itself), and what
actions are reserved for individual consent regardless of organizational
coordination outcomes.

Scope expansion requires re-consent. If the organization seeks to use
participant data, modify participation terms, or extend observation
scope beyond what was specified at entry, it must obtain individual
consent for the expanded scope. This is not a coordination vote; it is a
per-individual consent process in the relevant domain, because the
affected constituency is individual, not organizational.

Relationship to OCAP: Control, Possession. Relationship to CARE:
Collective Benefit, Responsibility.

4.4 Output Consent

How system outputs (reputation signals, scores, assessments,
recommendations) are used beyond their originating context. The Wheel of
Consent test: who produced the output, and who benefits from its use?

Shadow dynamics in this domain: outputs used for purposes the
originating constituency did not consent to (stealing); originating
constituencies that permit output use beyond their comfort because the
system makes refusal structurally difficult (enduring); downstream
consumers who treat outputs as entitlements rather than gifts from the
originating constituency (entitlement).

Relationship to OCAP: Ownership, Control. Relationship to CARE:
Collective Benefit, Authority to Control, Ethics.

4.5 Observation Consent

What a system monitors, how monitoring is conducted, and who sees
monitoring outputs. The Wheel of Consent test: who is conducting the
observation, and who benefits from it?

Shadow dynamics in this domain: observation framed as service to the
observed but primarily benefiting the observer or the system (stealing
disguised as serving); observed parties who permit monitoring beyond
their comfort because the alternative is exclusion from the system
(enduring); observers who treat access to observation data as an
entitlement rather than a gift from the observed (entitlement).

4.5.1 Observation Consent Specification

Consent to observation must be obtained at each coordination layer at
which participants can make an independent decision about what they
permit to be monitored. In a protocol with layered adoption architecture,
this requires at minimum: network-level consent (at protocol adoption),
organization-level consent (at onboarding), and scope-change consent
(when the detection surface expands). Each layer requires specified
scope and recourse. Adopting systems with different coordination
architectures must identify the analogous layers for their design.

**Level 1: Network-level consent (at protocol adoption).** When an
organization joins a network or protocol adopting this standard, it
consents to the observation scope specified in that network or protocol
at the time of adoption. This consent is structurally valid when: the
organization chose to join (not compelled), the observation scope is
specified and bounded (not open-ended), and the purpose is stated (e.g.,
asymmetry detection, not general surveillance).

**Level 2: Organization-level consent (at onboarding).** The
onboarding process must include an explicit observation consent step.
The organization acknowledges: what is observed, how observations are
processed, who sees the outputs, and what recourse exists if the
observation scope is exceeded. This is the Wheel of Consent's "allowing"
quadrant implemented correctly: the organization grants access to the
observer for a specified purpose, within negotiated limits.

**Level 3: Scope-change consent (when detection surface expands).** If
the observation scope is expanded through coordination action, existing
participating organizations must be notified and given the opportunity
to consent to the expanded scope. Scope expansion without re-consent is
a consent failure in the Observation consent domain. This does not grant
participating organizations a veto over observation improvements; it
requires notification, evaluation support (per the system obligations in
Section 6), and a meaningful option to adjust participation terms if the
expanded scope exceeds the organization's comfort.

Recourse for observation scope disputes follows a three-step path:
formal challenge through the system's coordination process, self-audit by
the observation layer to verify whether the observation was within
scope, and scope clarification through Signal Escalation if the boundary
is substantively ambiguous.

4.5.2 Voice and Audio Recording as Observation Domain

Audio recording of coordination sessions is a specific instance of observation consent that requires named treatment within the Level 2 consent architecture. When the adopting system or protocol designates spoken coordination sessions as sensemaking record sources (per the Sensemaking Standard, Section 9.2), the observation consent scope specified at onboarding must explicitly cover that recording practice: what sessions may be recorded, how recordings are processed and stored, who has access to recordings and transcripts, and the retention and deletion terms. Observation consent that does not name audio recording as an in-scope modality does not cover it; recording without explicit scope coverage is a consent failure in this domain.

Within a session covered by organizational-level recording consent, individual participants retain identity-linked consent rights that the organizational layer may not override. Voice anonymization is the privacy-preserving default under Section 4.6.2: a participant who requests that their voice not be individually identifiable in a transcript or recording is exercising an identity-linked consent right that must be honored without requiring justification and without adverse coordination consequences. This is a boundary within the session, not a withdrawal from it, and the consent architecture must structurally support it.

The content-driven recording pause is structurally distinct from the identity-linked request. When a participant requests that recording be paused in order to address a coordination matter rather than for identity reasons, that request implicates the sensemaking record architecture rather than individual identity consent. Conflating the two produces either honor-everything (suppressing coordination signals) or escalate-everything (violating individual consent rights). The Sensemaking Standard, Section 9.2, specifies how the content-driven pattern is classified and processed. The Adverse Signal Engagement Principle, Sections 3.1.2 and 4.1, governs the escalation path and anti-retaliation obligations.

Relationship to Sensemaking Standard: Section 9.2 (spoken coordination channels, consent architecture for recording). Relationship to OCAP: Access, Control. Relationship to CARE: Responsibility, Ethics.

4.5.3 Measurement Framework Consent

Consent to a measurement framework is a distinct consent layer from consent to data collection and from consent to coordination participation. A party being measured by a framework that cannot fully perceive their coordination dynamics has not fully consented unless that limitation has been made explicitly legible to them. This includes: what categories of coordination activity the framework can detect, what categories it cannot, and whether the framework's own vocabulary gaps are acknowledged and documented. When the measurement architecture's perceptual limits systematically exclude a party's coordination activities from the record, the party is consenting under a material omission. That omission must be disclosed at the Level 2 consent stage (Section 4.5.1) and must be updated through the Level 3 scope-change process whenever the detection architecture is revised in ways that expand or contract the perceptual boundary. Relationship to Information Asymmetry Classification Standard: Descriptive Capacity Asymmetry (Extension Class C, Section 5), which specifies the mechanism by which measurement vocabulary limitations produce structural invisibility.

4.6 Domain Interaction

The five domains are not independent. A single system action may
implicate multiple domains simultaneously. For example: a coordination
change (4.1) that modifies data collection practices (4.2) affecting
participants who did not consent to the new collection scope (4.3) and
whose outputs will be used in new contexts (4.4) under new observation
rules (4.5).

Systems adopting this standard at the structured or critical level must
identify cross-domain consent implications for actions that span
multiple domains. A consent process that is valid in one domain but
creates a shadow dynamic in another is a consent failure.

4.6.1 Individual and Organizational Consent

When individual consent and organizational consent conflict, neither
layer takes blanket precedence. This standard establishes a principle of
layered specificity: the layer closest to the affected party governs,
unless the affected party has explicitly delegated consent authority to
the organizational layer for a specified scope (see Section 4.3.1).

Organization-first consent (where organizational coordination decisions
automatically bind participants) produces enduring by default.
Participants who disagree with a data use decision must either exit at
structural cost or endure. Individual-first consent (where every
organizational decision affecting individual data requires
per-individual authorization) is operationally impractical for
coordination systems. Layered specificity resolves this: the delegation
scope established at participation entry (Section 4.3.1) defines what
the organizational layer may decide on the individual's behalf.

When individual and organizational consent conflict on a matter within
the delegation scope, the escalation path is: mediation, review of
whether the delegation scope actually covers the disputed action, and
Signal Escalation processing of the conflict as a coordination consent
domain signal. The system does not default to organizational override.

4.6.2 Privacy Directionality as a Cross-Domain Constraint

Across all five consent domains, where a design choice exists between a more and a less privacy-preserving option, the more privacy-preserving option is the structural default. This default may be departed from only when a specific, documented reason requires the less privacy-preserving option and that reason is legible to the affected constituency. A departure without a documented reason is a precision deficit under the Precision-First Design Standard and a consent failure in the relevant domain.

This is a cross-domain constraint, not a property of any single domain. It applies to coordination consent (what coordination records are public), data consent (what participant data is collected and retained), participation consent (what information entry or continued membership requires), output consent (how outputs travel beyond their originating context), and observation consent (what is monitored and at what resolution).

**System-initiated and participant-initiated exposure are distinct categories.** The privacy-as-default principle applies to system-initiated exposure: any disclosure of participant information that occurs without a specific, prior consent action by the affected participant. System-initiated exposure that is not required for the system's minimum viable function is a consent failure in the relevant domain unless the affected participant has explicitly authorized it.

Participant-initiated disclosure is categorically different. It is triggered by an explicit consent action: entering a coordination process, submitting a record, naming a counterparty, or configuring a disclosure preference. The minimum disclosure that follows from such an action as a structural consequence of that action is not system-initiated exposure. It is the functional scope of the consent already given.

This distinction is particularly relevant in confirmation architectures, where a participant who names a counterparty has entered the Wheel of Consent's allowing quadrant with respect to that counterparty for that event. The counterparty's ability to perceive enough of the event to confirm it is a consequence of being named, not a system-imposed disclosure. The privacy-default principle does not constrain this case; the three invariants (Identify, Authorize, Verify) govern it instead.

A detection instrument implementing this standard can distinguish the two categories by asking: did a specific, documented consent action by the affected participant precede this disclosure? If yes, the disclosure is participant-initiated and evaluated under the three invariants. If no, it is system-initiated and evaluated against the privacy-as-default principle.

Relationship to OCAP: Ownership, Control, Possession. Relationship to CARE: Authority to Control, Responsibility.

5\. Tiered Adoption

The tier names in this standard use the prefix SCLS (Structural Consent Legibility Standard).

5.1 SCLS-Assessed

The system acknowledges that consent is structurally relevant to its
operations. Consent decisions are logged. The five consent domains are
identified as applicable or not applicable to the system's operations.

Minimum requirement: a consent inventory that maps the system's
operations to the five domains and identifies where consent is currently
obtained, where it is assumed, and where it is absent.

5.2 SCLS-Operational

The system has defined processes for identifying affected constituencies
and obtaining authorization in each relevant consent domain. Consent
failures are logged and reviewable. The Wheel of Consent test (who is
acting, who benefits) is applied to consent-bearing interactions.

Minimum requirement: for each relevant consent domain, a documented
consent process that satisfies the Identify and Authorize invariants
(Sections 3.1 and 3.2). Shadow dynamics are named as known risks.

5.3 SCLS-Instrumented

The system treats consent failures as protocol-level violations subject
to detection and escalation. Shadow dynamics are structurally
detectable, not just named as risks. The Verify invariant (Section 3.3)
is fully satisfied: consent records are durable, tamper-evident, and
auditable. Consent failures are adverse signals processed through the
system's adverse signal processing.

Minimum requirement: a detection architecture capable of identifying
shadow dynamics in each relevant consent domain, integrated with the
system's adverse signal processing. Standing evaluation mechanism for
affected constituency claims (Section 3.1.1). Signal escalation for
implausible absence of standing claims.

5.3.1 Shadow Dynamics Detection Architecture

Systems adopting this standard at the SCLS-Instrumented level must implement
detection signatures for each shadow dynamic. Detection is
probabilistic: the detection layer flags signals for Signal Escalation
processing, not adjudication. Detection for each shadow type must be
graduated: at minimum a monitoring threshold (a signal that initiates
monitoring) and an escalation threshold (a signal or signal combination
that triggers Signal Escalation processing). The following specifies a
conformant graduated detection architecture for each shadow type.

**Entitlement/Stealing: ratification benefits the voting body at the
constituency's expense.**

Primary signal: benefit-vote correlation. The overlap ratio between
parties who voted to ratify and parties who measurably benefit from the
ratified action, computed across multiple coordination actions. A ratio
consistently above a calibrated threshold is a monitoring trigger.

Secondary signal: affected-constituency participation gap. Low
participation by the materially affected constituency combined with high
participation by the benefiting body in the same deliberation and
ratification process.

Tertiary signal: conflict-of-interest disclosure absence. Coordination
actions with high benefit-vote correlation where the proposer's
conflict-of-interest disclosures are absent, vague, or pro forma.

**Enduring: participation structurally compelled rather than chosen.**

Primary signal: compliance-deliberation divergence. High ratification
rates combined with low deliberation participation across coordination
actions. Participants who consistently vote without participating in the
deliberation that precedes the vote are exhibiting a compliance pattern
that may indicate structural compulsion rather than genuine consent.

Secondary signal: exit cost correlation. Participants with the highest
structural exit costs (largest locked stakes, longest tenure, most
dependencies) who show the highest compliance rates and lowest
deliberation participation.

Tertiary signal: battery vector stress signatures. Elevated stress
indicators concurrent with coordination compliance, where available in the
system's measurement architecture.

**Martyrdom: coordination service exceeding the server's limits.**

Primary signal: service concentration with declining quality. A small
number of participants handling a disproportionate share of coordination
labor with declining quality metrics over time (longer response
latencies, shorter review outputs, higher revision rates).

Secondary signal: delegation absence. Concentrated coordination labor
without corresponding delegation or succession activity despite
available capacity in the coordination body.

Tertiary signal: resistance to relief. When coordination labor rebalancing
is proposed, the concentrated participant resists or does not
participate in deliberation about rebalancing.

Detection signals are composite. A single instance of any monitoring-threshold
signal triggers monitoring. Persistent patterns across multiple coordination
actions, combined with higher-confidence signals, trigger escalation
through the system's Signal Escalation process. Individual signals are
never treated as conclusive. The detection architecture must
be transparent to participants: organizations operating at the
SCLS-Instrumented level must know what patterns are being monitored (this is
itself a consent requirement in the Observation consent domain; see
Section 4.5.1).

5.4 SCLS-Loop-Closed

Includes all SCLS-Instrumented requirements plus closed coordination loop architecture.

The defining property of SCLS-Loop-Closed is that inaction by coordination actors in the presence of a detected consent failure is structurally visible without depending on any actor's cooperation. At SCLS-Instrumented, the detection architecture produces consent failure outputs. At SCLS-Loop-Closed, those outputs produce mandatory documented responses, and the absence of a response is itself a detected event.

Minimum requirements:

Every consent failure detection output (shadow dynamic detection, implausible absence of a standing claim, or consent invariant violation per Section 3.4) must produce a documented coordination review within a defined window. A window is valid under SCLS-Loop-Closed if it satisfies three conditions: it is specified before any adoption claim is made; it is publicly documented so that any coordination actor can verify whether the system is meeting its own stated commitment; and it is short enough that inaction within it is detectable before the next coordination cycle in which the underlying consent failure could compound. The adopting system must define its coordination cycle length in the same public documentation that specifies the window, as the two specifications are co-dependent. The review record must include: the consent failure identifier, the shadow dynamic classification or invariant violation type, the review outcome (including outcomes of no action, deferral, or declined action), the actor or body responsible for the review, and the rationale. A decision to take no action is a decision and must be documented as such. The absence of any documented review is not a permissible outcome at SCLS-Loop-Closed.

The absence of a documented review within the defined window must produce automatic disclosure to all coordination actors without requiring any actor's initiation. This disclosure makes the consent failure detection output, its classification, the elapsed time since detection, and the absence of a coordination review simultaneously visible to all coordination actors. This disclosure is a structural consequence of the consent failure detection architecture, not a discretionary act. A system in which this disclosure requires a human decision to publish has not closed the coordination loop and does not meet SCLS-Loop-Closed.

The coordination review record is append-only. Reviews cannot be modified after recording; corrections are recorded as new entries referencing the original. This property is what makes inaction detectable without cooperation: an independent observer can verify that a consent failure detection output exists in the record, verify that no review entry exists within the required window, and determine that automatic disclosure was or was not produced as a consequence.

Tier review cadence for SCLS-Loop-Closed systems: tier review MUST occur at minimum annually and MUST include a coordination loop integrity check: confirmation that the detection-to-review path operated as specified for all consent failure detection outputs in the review period, and that automatic disclosures were produced where required.

5.5 SCLS-Auditable

Includes all SCLS-Loop-Closed requirements plus independent auditability.

The defining property of SCLS-Auditable is that the full detection and response architecture can be verified by a party outside the system without depending on system operator cooperation or self-certification.

Minimum requirements:

The complete consent failure record, from detection output through documented review or automatic disclosure, must be accessible to an independent auditor. Access is not contingent on operator consent during a defined audit period. The record format is sufficient for an auditor to verify completeness without access to the detection layer itself.

The auditor must be able to verify completeness: that all consent failure detection outputs generated in the audit period are present in the record. This requires that the detection architecture produces a verifiable count or hash of outputs generated, against which the record can be checked. A record that can only be verified for presence (each failure in the record was detected) but not for completeness (all detections are in the record) does not meet SCLS-Auditable. The gap between generated and recorded detection outputs is the detection surface for suppression; an audit that cannot detect that gap cannot verify that suppression has not occurred.

The auditor must be able to verify classification integrity: that each recorded consent failure was classified using the shadow dynamic taxonomy and consent invariant tests in this standard, and that the classification applied is consistent with the detection evidence recorded.

The auditor must be able to verify response completeness: that every consent failure detection output in the record produced either a documented review within the specified window or an automatic disclosure. Gaps in this chain are reportable findings.

The audit itself must be documented: scope, period, auditor identity or body, findings, and system response to findings. Audit reports are retained in the coordination record under the same append-only constraints as documented reviews.

SCLS-Auditable systems must make audit reports available to their participant population within a defined period after audit completion. The disclosure period is specified by the system and subject to the same precision and legibility obligations specified in Section 6.1.

6\. Bandwidth and Consent

A consent mechanism that satisfies the structural requirements of this
standard may still fail if the affected constituency lacks the bandwidth
to exercise it. This section specifies the relationship between consent
and the capacity to exercise consent, establishing bandwidth as a system
obligation rather than a participant qualification.

6.1 System Obligations for Consent Validity

Consent is structurally valid when the system satisfies four
obligations. The obligations are on the system, not the participant.
This avoids the paternalism trap of requiring participants to
demonstrate understanding before being allowed to consent, while
ensuring that consent opportunities are substantively meaningful.

**Legibility obligation.** The action being consented to must be
described in terms the affected constituency can evaluate. "We're
changing the fee structure" fails the legibility obligation. "We're
increasing the confirmation fee from 0.10 to 0.30 units per
cross-organizational confirmation, effective next period, affecting
organizations that currently use more than five cross-organizational
confirmations per period" satisfies it. Vague consent is not consent:
the precision requirement applies to the description of what is being
authorized, not only to the authorization mechanism itself.

**Time obligation.** The consent window must be proportional to the
complexity of what is being consented to, calibrated by Cynefin domain.
The Cynefin calibration governs both the duration and the shape of the
consent process (see Section 6.4).

**Support obligation.** The system must provide the analytical
infrastructure for the affected constituency to evaluate implications.
This may include impact assessments, modeling tools, deliberation
forums, or expert consultation. The system provides the support; it does
not require the participant to independently acquire the expertise.

**Exit/objection cost obligation.** The structural cost of dissent
(including exit, objection, and abstention) must not be punitive.
Systems where objecting to a coordination outcome carries a cost
(reputation penalty, social sanction, loss of access) that exceeds the
benefit of participation operate in the enduring shadow by default. This
obligation is the strongest test of consent validity: would a
participant who disagreed with the outcome feel that they had a
meaningful opportunity to object and be heard?

If all four obligations are met, consent is valid even if individual
participants chose not to use the support provided. The structural
question is whether the opportunity was meaningful, not whether every
individual exercised it.

6.2 Bandwidth Types

The capacity to exercise consent decomposes into four bandwidth types.
Each type is independently necessary; a deficit in any single type can
render consent substantively empty even when the other three are
sufficient.

**Ontological bandwidth:** the capacity to perceive that a consent
distinction exists. A participant with insufficient ontological
bandwidth cannot see that "who is doing" and "who is it for" are
separate questions. Systems that suppress ontological bandwidth (by
conflating service with obligation, or by not making the distinction
between action and benefit visible) make consent failures invisible to
the participants experiencing them.

**Epistemic bandwidth:** the capacity to evaluate whether a given
interaction falls on one side of a consent distinction or the other. A
participant with ontological bandwidth but insufficient epistemic
bandwidth can see the distinction but cannot assess whether a specific
coordination proposal is genuine serving or martyrdom-driven gatekeeping.

**Pedagogical bandwidth:** the capacity to teach and transmit consent
distinctions so they become operational within the system. Organizations
with pedagogical bandwidth can onboard new members into the consent
framework. Organizations without it rely on implicit learning, which
means new members inherit whatever shadow dynamics are dominant in the
existing culture.

**Operational bandwidth:** the capacity to act on what you perceive,
evaluate, and know how to teach. Without operational bandwidth, a system
can score perfectly on the first three types while producing enduring
dynamics at scale, because participants know what is happening but
cannot change it. When a participant perceives a consent violation,
evaluates it correctly, and could explain it to others, but the
structural cost of acting (exit cost, social cost, career cost) exceeds
their tolerance, operational bandwidth is the binding constraint.

6.3 Bandwidth as Cross-Cutting Design Constraint

Every requirement in this standard that depends on a participant's
capacity to perceive, evaluate, teach, or act on a distinction assumes
that the participant has sufficient bandwidth in the relevant dimension.
Systems that create requirements without supporting the bandwidth those
requirements draw on produce structurally valid-looking consent that is
substantively empty. Bandwidth is not a participant qualification; it is
a system obligation.

Six information asymmetry classes each target specific bandwidth types:
positional, temporal, interpretive, relational, complexity, and omission
asymmetry. Positional and interpretive asymmetry primarily suppress
ontological bandwidth (the capacity to perceive that the asymmetry
exists). Temporal, relational, and complexity asymmetry primarily
suppress epistemic bandwidth (the capacity to evaluate whether a
specific interaction exploits the asymmetry). Omission asymmetry
suppresses ontological bandwidth (what is not said is invisible by
definition). This mapping means that a system which does not measure and
support bandwidth cannot verify consent or detect asymmetry.

Inequality and corruption operate by systematically suppressing the
bandwidth types that would make them visible. This is a structural
claim, not a metaphor. The party benefiting from asymmetry has
structural incentives to suppress the bandwidth types that would make
the asymmetry detectable. Systems adopting this standard should evaluate
their consent processes against this principle: does the system invest
in the bandwidth types that its consent requirements draw on, or does it
create requirements that assume bandwidth the system does not support?

The bandwidth types also constrain what depth of learning an
organization can sustain. Single-loop learning (correcting actions
within the current framework) requires epistemic bandwidth: the capacity
to evaluate whether a specific action was correct. Double-loop learning
(questioning the framework itself) requires ontological bandwidth: the
capacity to perceive that the framework is a variable, not a given.
Triple-loop learning (questioning the values that generated the
framework) requires ontological bandwidth at a deeper level: the
capacity to perceive that the values motivating the framework are
themselves open to examination. A system that does not invest in
ontological bandwidth structurally caps itself at single-loop learning,
regardless of what its coordination process formally permits. This has a
direct design implication: coordination processes that require structural
change (changes to the framework itself, rather than changes within it)
must invest in ontological bandwidth, not only epistemic bandwidth, or
the coordination process will default to single-loop responses at every
level. Consent processes must be designed with the learning loop depth
they require in mind.

6.4 Domain Complexity and Consent Process Shape

Consent processes must be calibrated to the epistemic structure of the
decision domain: the type of understanding available to the affected
constituency differs structurally across complexity levels, and the
consent process must match those differences. The following specifies
the consent process requirements for four complexity levels, using the
Cynefin framework's four domains and corresponding action modes as a
conformant calibration tool. Systems that calibrate consent process
shape using a different complexity classification framework must satisfy
the same structural requirements.

**Clear domain: sense-categorize-respond.** The causal relationships are
known and the implications of the proposed action are evaluable from the
specification alone. The consent process is linear: the affected
constituency receives a legible description, evaluates it against known
criteria, and authorizes or refuses. Fixed time windows are appropriate
because the evaluation task is bounded. The system obligation is to
provide the specification at sufficient precision (legibility
obligation) and sufficient time to read it (time obligation).

**Complicated domain: sense-analyze-respond.** The causal relationships
exist but require expert analysis to trace. The implications of the
proposed action are evaluable, but not by the affected constituency
alone. The consent process requires an analysis phase: the system
provides expert evaluation infrastructure (support obligation), the
affected constituency reviews both the proposal and the expert analysis,
and authorizes or refuses on the basis of both. Longer time windows are
appropriate, scaled to the expert evaluation cycle. The system
obligation is to provide the analytical support, not to require the
affected constituency to independently acquire the expertise.

**Complex domain: probe-sense-respond.** The causal relationships are
emergent and the implications of the proposed action cannot be fully
pre-specified. The consent process cannot be linear, because there is no
complete specification to evaluate before the action is taken. The
consent process is iterative: the system proposes a bounded probe (a
limited-scope implementation), the affected constituency consents to the
probe, the probe's effects are observed, and the constituency reconsents
(or refuses) based on observed effects before the change is extended.
Fixed time windows are inappropriate because the evaluation depends on
observation of emergent effects. The system obligation is to bound the
probe's scope, provide observation infrastructure, and ensure that
consent to the probe does not constitute consent to full deployment.

**Chaotic domain: act-sense-respond.** The system is in crisis and
action must precede analysis. The consent process is inverted: the
system acts first (under whatever emergency authority its coordination
system specifies), then provides the affected constituency with an account of
what was done and why, and obtains post-hoc ratification once the system
returns to a non-chaotic state. The system obligation is to constrain
emergency authority to the minimum action required, to document the
action for subsequent review, and to ensure that post-hoc ratification
is substantive (the affected constituency can reverse or modify the
emergency action if the ratification process determines the action was
disproportionate or misdirected).

This principle extends beyond consent. Any process in a system adopting
this standard that classifies actions by complexity domain and prescribes
a response should verify that the response matches the action mode for
that domain.
A coordination process that applies a linear deliberation-then-vote model
to a Complex-domain change is using a Clear-domain action mode in a
Complex-domain context; the mismatch will produce either false certainty
(the constituency votes on implications that cannot yet be known) or
structural enduring (the constituency votes because the process requires
it, not because the evaluation is complete). Similarly, a detection
process that applies sense-analyze-respond to a Complex-domain asymmetry
will fail to detect emergent patterns that only become visible through
iterative probing. The Cynefin action mode is not a label; it is an
operational constraint on what kind of process is valid in each domain.

7\. Relationship to Other Standards

7.1 Precision in Specification

Consent claims must be precise. "We consulted stakeholders" fails the
precision test the same way "we checked for problems" fails any adverse
signal process. The principle of precision-first specification applies
to consent processes: vague consent is not consent. A consent process
that does not specify who acted, who benefits, who was affected, and
what the agreed limits were is not a consent record. Systems adopting
this standard at the SCLS-Instrumented level are strongly recommended to
pair it with a precision-in-specification standard that applies
precision requirements to coordination proposals, consent records, and
detection outputs.

7.2 Adverse Signal Processing

Consent failures are adverse signals. Any adverse signal processing
system paired with this standard should apply three properties to
consent failures: they must be detectable (consent failures are
observable events, not inferences), classifiable by domain and shadow
type (naming what kind of failure occurred is a precondition for
resolution), and navigable (there must be a finite path to resolution
for every class of consent failure).

The absence of dissent in a domain where dissent is normal is a consent
signal, not a consent confirmation. Any adverse signal processing system
must be capable of detecting implausible absence, not only explicit
signals, or it will fail to catch the most structurally embedded consent
failures.

An adverse signal that the affected constituency lacks the epistemic
bandwidth to evaluate is a failure of the notice function in practice,
even if the signal is formally detectable. This is a recursive design
point: the failure of the notice mechanism is itself a consent failure,
and must be detectable by the same system.

7.3 Wheel of Consent

Betty Martin's Wheel of Consent is the foundational consent framework
for this standard. The two-axis model (who is doing / who is it for),
the four quadrants (Serving, Taking, Accepting, Allowing), and the four
shadow dynamics (martyrdom, stealing, entitlement, enduring) are
Martin's original contribution. This standard applies the framework to
coordination systems and protocols, and data sovereignty. The
coordination domain mapping, shadow-to-failure-mode translation, five
consent domains, and structural verification architecture are original
to this standard.

Citation: Martin, Betty. *The Art of Receiving and Giving: The Wheel of
Consent.* 2021.

7.4 OCAP and CARE

This standard keeps OCAP (Ownership, Control, Access, Possession) and
CARE (Collective Benefit, Authority to Control, Responsibility, Ethics)
as independent cited frameworks with an integration layer. The standard
does not absorb, subsume, or interpret OCAP or CARE. These frameworks
were developed by and for indigenous communities (OCAP by the First
Nations Information Governance Centre; CARE by the Global Indigenous
Data Alliance), and their political and ethical authority remains with
the originating communities.

**Mapping.** The following table maps OCAP elements and CARE principles
to this standard's five consent domains.

  ---------------- ---------------- ---------- ------------------- ------------ -----------------
  **Framework      **Governance**   **Data**   **Participation**   **Output**   **Observation**
  Element**                                                                     

  OCAP: Ownership                   ✓                              ✓            

  OCAP: Control    ✓                ✓          ✓                   ✓            ✓

  OCAP: Access                      ✓                                           ✓

  OCAP: Possession                  ✓          ✓                                

  CARE: Collective                  ✓          ✓                   ✓            
  Benefit                                                                       

  CARE: Authority  ✓                                               ✓            
  to Control                                                                    

  CARE:            ✓                           ✓                                ✓
  Responsibility                                                                

  CARE: Ethics                      ✓                              ✓            ✓
  ---------------- ---------------- ---------- ------------------- ------------ -----------------

**Compliance bridge.** Satisfying this standard is a structural
prerequisite for OCAP and CARE compliance but does not constitute OCAP
or CARE compliance. OCAP and CARE have normative requirements
(particularly around indigenous governance authority and collective
benefit) that are outside this standard's scope. A system that satisfies
this standard in all five consent domains has satisfied the structural
mechanisms that OCAP and CARE require, but the normative evaluation of
whether those mechanisms serve the originating community's interests
remains with the originating community.

**Non-absorption clause.** This standard does not replace, subsume, or
interpret OCAP or CARE. It provides structural mechanisms that
OCAP/CARE-adopting systems can use, but the normative authority for what
constitutes compliance with OCAP or CARE remains with the First Nations
Information Governance Centre and the Global Indigenous Data Alliance
respectively.

Citations: First Nations Information Governance Centre. The First
Nations Principles of OCAP. https://fnigc.ca/ocap-training/. Global
Indigenous Data Alliance. CARE Principles for Indigenous Data
Governance. https://www.gida-global.org/care.

7.5 Tensegrity Compressive Standards within the Coordination Structural Integrity Suite

This standard is one of the seven Tensegrity Compressive Standards within the Coordination Structural Integrity Suite: the Precision-First Design Standard, the Adverse-Signal Engagement Principle Core Standard, the Structural Consent Legibility Standard, the Information Asymmetry Classification Standard, the Structural Power Obligation Standard, the Regenerative Obligation Standard, and the Coordination Scaling Standard. Each standard addresses a distinct failure mode. Each is independently valid: no standard requires the others for its own validity. Together, they form a reinforcing set.

Systems adopting any one of the seven Tensegrity Compressive Standards are strongly recommended to adopt all seven. The full Tensegrity Compressive Standards designation applies to systems that adopt all seven at Tier 4 (Loop-Closed) or above. The designation is descriptive: a system either satisfies all seven standards at Tier 4 or above, or it does not. Partial adoption at any tier is a legitimate developmental stage; claiming full Tensegrity Compressive Standards conformance on the basis of partial adoption is structural exposure theater. Partial adopters should produce a structural exposure disclosure naming which standards are not adopted and which failure modes remain unaddressed.

A structural exposure disclosure must contain four elements to be substantive. First, the disclosure must name each standard not adopted or not yet at Tier 4, using its full canonical name. Second, for each absent standard, the disclosure must describe in plain language the specific failure mode class that standard addresses and what becomes structurally undetectable in its absence. Third, for each absent standard, the disclosure must state a self-assessed exposure level (low, medium, or high) with a rationale sufficient for an independent reader to evaluate the assessment. Fourth, for each absent standard where compensating controls exist, the disclosure must name those controls, describe their mechanism, and explain why they are considered adequate for the assessed exposure level. Where no compensating controls exist, the disclosure must say so explicitly. A disclosure that satisfies the form without the substance is itself a precision deficit under the Precision-First Design Standard. The full conformance theater prevention architecture is specified in the Proof of Coordination Architecture document.

The Sensemaking Standard covers an organization's capacity to perceive and apply all seven standards with understanding. It is architecturally distinct from the Tensegrity Compressive Standards within the Coordination Structural Integrity Suite.

8\. Inheritance Clause

Systems adopting this standard should include the following statement in
their coordination documentation:

*Structural Consent Legibility Inheritance: This
\[document/system/protocol\] adopts the Structural Consent Legibility
Standard (v\[X\], \[date\]) at the \[SCLS-Assessed /
SCLS-Operational / SCLS-Instrumented / SCLS-Loop-Closed / SCLS-Auditable\] level. The consent domains identified
as relevant to this system's operations are: \[list relevant domains
from the five\]. Consent domains identified as not applicable: \[list,
with rationale\].*

The inheritance clause commits the adopting system to: (a) identifying
which of the five consent domains are relevant to its operations, (b)
satisfying the three invariants (Identify, Authorize, Verify) in each
relevant domain at the adopted tier, (c) treating consent failures as
adverse signals subject to its adverse signal processing, and (d)
specifying which consent domains are applicable and which are not, with
rationale, so that the adoption scope is explicit and auditable.

Adoption of this standard at any tier below the full Tensegrity Compressive Standards threshold (Tier 4 across all seven Tensegrity Compressive Standards) does not constitute full Tensegrity Compressive Standards conformance and does not reduce structural exposure from uncovered standards. Systems in partial adoption are required to produce a structural exposure disclosure in place of a conformance claim, per the specification in the Proof of Coordination Architecture document.

8.1 Precision-First Inheritance

*Precision-First Inheritance: This document adopts the Precision-First Design Standard at the PFDS-Operational tier. Every element of this document is subject to that standard at the declared tier. Any revision that reduces definitional precision, replaces typed constructs with vague terms, collapses previously distinguishable states, or makes a falsifiable claim unfalsifiable is a design error requiring correction, not a legitimate exercise of coordination or editorial discretion.*

9. Open Design Questions

The following questions are structurally required by this standard but
not yet fully resolved. They are listed here to make the design space
explicit. Questions resolved during the February 2026 research session
are marked as resolved with references to the sections where the
resolution appears.

**9.1 Standing evaluation mechanism for affected constituency claims.**
Resolved. See Section 3.1.1. Open edge: calibration of evaluation
criteria thresholds requires pilot data.

**9.2 Detection signatures for coordination consent shadow dynamics.** Resolved.
See Section 5.3.1. Open edges: shadow detection threshold calibration
(how much benefit-vote correlation constitutes stealing vs. normal
coordination) requires pilot data. Compound shadow model (organizations
operating in multiple shadows simultaneously) requires a compositional
detection architecture; design question for the detection layer specification of any adopting system.

**9.3 Bandwidth thresholds for consent validity.** Partially resolved.
Section 6 establishes four system obligations and four bandwidth types.
The specific minimum thresholds for each bandwidth type and the
measurement instruments for each are specified in a developmental
assessment mechanism conformant with the adopting system's developmental
specification. Cynefin-calibrated time window durations for each domain
require pilot data and empirical calibration by adopting organizations.

**9.4 OCAP/CARE integration architecture.** Resolved. See Section 7.4.

**9.5 Cross-domain consent failure classification.** Open. Section 4.6
establishes that actions spanning multiple domains must have
cross-domain consent analysis. The classification system for
cross-domain consent failures and its interaction with the Information
Asymmetry Classification Standard's six asymmetry classes is not yet
specified.

**9.6 Meta-consent for observation layers.** Open. An observation layer
that audits its own observation scope is a self-referential problem. The
observation layer's monitoring of its own behavior is a coordination consent
domain question (who authorized the layer to audit itself?) that
requires external validation from the tenant body, not
self-certification. Named as an ongoing coordination challenge that
requires continuous attention rather than a one-time design decision.

Relationship To Other Standards

The closest functional adjacency is with the Information Asymmetry Classification Standard: information asymmetry directly affects consent legibility, and the six asymmetry classes provide the vocabulary for specifying what a participant has access to when consenting. The Structural Power Obligation Standard addresses adjacent territory: power differentials affect consent voluntariness in ways this standard's three consent features address structurally.

Tensegrity As A Whole

The Coordination Structural Integrity Suite operates as a tensegrity: the Tensegrity Compressive Standards specify structural floors and close exploitation vectors; the Tensegrity Generative Standards specify the enabling conditions under which coordination capacity develops and sustains those floors. This standard is compressive.

```
Coordination Structural Integrity Suite
│
├── Tensegrity Compressive Standards (7)
│   ├── Precision-First Design Standard
│   ├── Adverse Signal Engagement Principle Core Standard
│   ├── Structural Consent Legibility Standard               ← this standard
│   ├── Information Asymmetry Classification Standard
│   ├── Structural Power Obligation Standard
│   ├── Regenerative Obligation Standard
│   └── Coordination Scaling Standard
│
└── Tensegrity Generative Standards (3)
    ├── Sensemaking Standard
    ├── Four Batteries Capacity Standard
    └── Conflict Transformation Standard
```

Without this standard participation can appear consensual while being extractive. The three consent features this standard requires (negotiated limits, bidirectional awareness, revocability) are the structural conditions under which consent claims are verifiable rather than asserted.

Each standard in the Coordination Structural Integrity Suite is independently adoptable and independently valid. Adopted together, the ten standards address a reinforcing set of structural failure modes that no single standard covers alone. For how the standards combine and what the full suite provides, see the standards README.

Changelog

**v0.3.24 (2026-04-17):** Suite count correction. Coordination Scaling Standard added as seventh Tensegrity Compressive Standard throughout Section 7.5: standard count updated from six to seven in all instances; CSS added to canonical standard list; conformance threshold corrected from "all five" to "all seven." No normative content changes.

**v0.3.23 (2026-04-15):** Frame Language pass (Row 7 v0.1.6). One residual non-admissible hit: "The Sensemaking Standard governs an organization's capacity" → "covers." Admissible: all other remaining "govern" instances are Case 1 (Section 1 opening), Case 2 (Ostrom, CARE/OCAP, indigenous governance authority), Case 3 (external regulatory doctrine), or plain English verb. No normative content changes.

**v0.3.22 (2026-04-15):** Frame Language bridge vocabulary tightening. Residual Frame 1 vocabulary corrected under the revised Row 7 three-case rule. "consent-based governance" → "consent-based coordination"; "governance actions" → "coordination decisions"; "governance record" in Section 1 harms paragraph → "coordination record"; "Every governance system" (paragraph 5 of Section 1) → "Every coordination system"; "most governance systems" → "most coordination systems"; "governance mechanism" → "coordination mechanism"; "governance protocol" removed from Section 1 transferability clause (redundant with "coordination system"); "governance pressure" → "coordination pressure"; "governance systems, coordination protocols" in Section 2 attribution note → "coordination systems and protocols"; "governance domain mapping" in Section 7.3 → "coordination domain mapping"; "governance documents" in Section 2.3.2 → "coordination documents"; "governs the gap" → "addresses the gap"; "governance contexts" in Section 4.2 → "coordination contexts"; "adverse governance consequences" in Section 4.5.2 → "adverse coordination consequences"; "suppressing governance signals" in Section 4.5.2 → "suppressing coordination signals"; "governance participation" in Section 4.5.3 → "coordination participation"; "exercise of governance or editorial discretion" in Section 8.1 → "exercise of coordination or editorial discretion." Admissible exceptions retained: opening two paragraphs of Section 1 (Case 1), Ostrom commons governance reference in Section 3.1 (Case 2), indigenous governance authority in OCAP/CARE compliance bridge (Case 3). No normative content added or removed.

**v0.3.21 (2026-04-15):** Frame Language pass. Frame 1 vocabulary replaced with Frame 2 equivalents throughout normative content. "governance actions/process/vote/proposal/body/decisions/outcomes/standing/layer/architecture" replaced with "coordination" equivalents across Sections 2.3.1, 3.1, 3.1.1, 3.1.2, 4.1 (heading and body), 4.3.1, 4.5.1, 4.6, 4.6.1, 4.6.2, 5.3.1, 6.2, 6.3, 6.4, 7.1, 9.2, and 9.6. Section 4.1 renamed from "Governance Consent" to "Coordination Consent." Tier 4 renamed from "SCLS-Accountable" to "SCLS-Loop-Closed" throughout normative text (Sections 5.4 heading, 5.4 body, 5.5 opening, 7.5 conformance threshold, Section 8 inheritance clause tier list). Section 5.4 heading updated accordingly; closed-loop requirement language updated to use "coordination" equivalents throughout. "governs the suite as a whole" in Section 1 replaced with "is the meta-standard for the suite" (PFDS boilerplate correction). "their governance documentation" in Section 8 replaced with "their coordination documentation." No normative content added or removed.

**v0.3.20 (2026-04-11):** Three normative additions addressing structural consent failures surfaced by DAO failure case analysis. (1) Cost-bearing party identification added to Section 2.1: the two-axis framework is supplemented with an explicit requirement to identify who bears the cost when the cost-bearing party is distinct from both the acting and benefiting parties; failure to identify the cost-bearing party is a consent failure independent of two-axis legibility. (2) External legal override named as a structural threat in new Section 2.3.2: external legal requirements (securities classification, employment law, data sovereignty mandates, anti-money-laundering obligations) can override explicit consent architecture; the consent architecture must name applicable jurisdictions and govern the gap between explicit consent and externally imposed obligations. (3) Action specification prior condition added to Section 3.1: the Identify invariant presupposes that the action being consented to is specified with sufficient precision for affected parties to evaluate standing; category-level authorization cannot substitute for per-action consent without a named trigger condition for standing evaluation.

**v0.3.19 (2026-04-10):** Section 4.5.1 heading renamed from "Observation Consent Architecture" to "Observation Consent Specification." No normative content changes. Rename frees "Consent Architecture" as a reserved compound for use as the Multiplex Consent Architecture sub-class name in the Uniplex/Multiplex architectural frame vocabulary (see reference-terminology-conventions-0_1_2.md).

**v0.3.18 (April 2026):** Plain-language preamble added. Two paragraphs inserted before the non-harming formula in Section 1 (Purpose), grounding the standard in the lived experience of the coordination failure it addresses (consent claimed without structural verifiability). Navigation pointer added: one sentence pointing to the Suite Integration Guide and the Suite Deployment Contexts document. No changes to normative content.

**v0.3.17 (April 2026):** Non-harming opening formula added to Section 1 (Purpose). New paragraph at the start of Section 1 specifies the specific harms that absence of structural consent legibility produces and names two-axis consent legibility as the precise structural answer. No changes to normative content.

**v0.3.16 (March 2026):** Section 3.1.2 (Constituency Definition as Structural Precondition) added after Section 3.1.1. The per-action constituency identification requirement in Section 3.1 presupposes a durable, accessible definition of who holds participation rights. Three conditions specified: accessible without authority-gating, durable against unilateral modification (modification triggers the Authorize invariant), and specific enough for independent observer determination. Absence of the definition is a consent architecture failure preventing structural (not merely procedural) satisfaction of the Identify invariant. Addresses Ostrom's first design principle at the standards level.

**v0.3.15 (March 2026):** Canonical name correction. Companion standards on lines 15-17 referenced by descriptive shorthand ("precision-in-specification standard," "adverse signal engagement standard"); replaced with full canonical names (Precision-First Design Standard, Adverse-Signal Engagement Principle Core Standard).

**v0.3.14 (March 2026):** Suite rename ("Coordination Structural Integrity Suite" replaces "Structural Integrity Layer" throughout). Added "Relationship To Other Standards" and "Tensegrity As A Whole" sections, replacing Section 12.

**v0.3.13 (March 2026):** "What not how" precision pass. Three bounded edits applying the Precision-First Design Standard's structural condition requirement. (1) Status note: "Cynefin time windows" generalized to "complexity-domain time windows." (2) Section 4.5.1 opening reframed: "obtained at three levels" replaced with structural condition (consent at each governance layer where participants can make independent decisions about what they permit to be monitored); three-layer architecture (network, organization, scope-change) named as a conformant minimum for protocol-based systems; adopting systems with different governance architectures instructed to identify analogous layers. Scope and recourse requirement per layer retained. (3) Section 5.3.1 opening reframed: "three-signal detection model" replaced with graduated detection requirement (monitoring threshold and escalation threshold as minimum); specific signals for each shadow type retained as conformant graduated architecture; closing paragraph updated (monitoring-threshold signal terminology; Signal Escalation casing corrected throughout). (4) Section 6.4 retitled "Domain Complexity and Consent Process Shape"; opening paragraph restated as structural condition (consent processes calibrated to epistemic structure of decision domain); Cynefin named as conformant calibration tool rather than required framework; closing paragraph generalized from "Cynefin domain" to "complexity domain." Normative requirements at each complexity level unchanged.

**v0.3.12 (March 2026):** Change 3 of anisotropy sequence. Typological declaration (Variant B) added to Section 1 (Purpose). Operative classes: relational-topological (primary, two-axis consent topology), epistemic-perceptual (precision/operationalization, detection sub-aspects). Boundary classes: felt-experience (structural legibility vs. experienced consent named explicitly), structural-mechanical, temporal-dynamic (frequency-dynamic sub-aspect). Map version v0.1.1 cited.

**v0.3.11 (March 2026):** Terminology update. "Commitment Standards" renamed to "Tensegrity Compressive Standards" throughout. No normative content changes.

**v0.3.10 (March 2026):** Citation fix. Section 8.1 Precision-First inheritance clause updated from v1.5.4 to v1.5.6. No normative content changes.

**v0.3.9 (March 2026):** Added Section 4.5.3 (Measurement Framework Consent). Establishes consent to a measurement framework as a distinct consent layer from consent to data collection and consent to governance participation. A party measured by a framework that cannot fully perceive their coordination dynamics has not fully consented unless the framework's perceptual limits have been made explicitly legible to them: what categories are detectable, what are not, and whether vocabulary gaps are acknowledged. When measurement architecture limits systematically exclude a party's coordination activities from the record, this is a material omission that must be disclosed at Level 2 and updated via Level 3 scope-change process when the detection architecture changes. Cross-reference to Information Asymmetry Classification Standard, Extension Class C (Descriptive Capacity Asymmetry, Section 5), which specifies the mechanism. Source: standards audit session, March 26, 2026.

**v0.3.8 (March 2026):** Section 4.5.2 added: Voice and Audio Recording as Observation Domain. Names audio recording of coordination sessions as a specific observation consent instance requiring explicit coverage in the Level 2 consent architecture: recording without named scope coverage is a consent failure. Individual voice anonymization established as the privacy-preserving default per Section 4.6.2: an identity-linked request to anonymize voice must be honored without justification and without adverse governance consequences. Content-driven recording pause distinguished from identity-linked request: the former implicates the sensemaking record architecture, the latter is an individual consent right; conflating them produces either signal suppression or consent violation. Cross-references to Sensemaking Standard Section 9.2 and Adverse Signal Engagement Principle Sections 3.1.2 and 4.1 added. Source: standards audit session and Sensemaking Standard v1.1.3 alignment, March 26, 2026.

**v0.3.7 (March 2026):** Added Section 4.6.2 (Privacy Directionality as a Cross-Domain Constraint). New normative content establishing two principles across all five consent domains. First: where a design choice exists between a more and a less privacy-preserving option, the more privacy-preserving option is the structural default; departure requires a specific, documented reason legible to the affected constituency. Second: system-initiated exposure (disclosure without a prior participant consent action) and participant-initiated disclosure (disclosure triggered by an explicit consent action such as naming a counterparty or configuring a disclosure preference) are categorically distinct; the privacy-as-default principle governs the former; the three invariants govern the latter. Added OCAP and CARE relationship notes for the new section. Source: session sensemaking on CROPS alignment and EF Mandate privacy architecture principles, March 14, 2026.

**v0.3.6 (March 2026):** Pre-release fixes. (1) Section 7.5 final sentence: "architecturally distinct from the pentad" replaced with "architecturally distinct from the Tensegrity Compressive Standards within the Coordination Structural Integrity Suite" (propagation miss from v0.3.5 pass). (2) Companion standards preamble: "constitutes the pentad" replaced with "constitutes the Tensegrity Compressive Standards within the Coordination Structural Integrity Suite" (second propagation miss from v0.3.5 pass). (3) Section 7.5: removed "(forthcoming)" from Proof of Coordination Architecture reference, consistent with other standards in the stack. (4) Section 8.1 Precision-First inheritance clause: version citation updated from v1.4.8 to v1.5.4. No changes to normative content.

**v0.3.5 (March 2026):** Coordination Structural Integrity Suite naming propagation. Updated Section 7.5 heading from "Structural Integrity Pentad" to "Tensegrity Compressive Standards within the Coordination Structural Integrity Suite." Updated Section 7.5 body: replaced structural integrity pentad designation language with full Tensegrity Compressive Standards designation language throughout; "one of five standalone standards that form the structural integrity pentad" replaced with "one of the five Tensegrity Compressive Standards within the Coordination Structural Integrity Suite." Updated preamble reference and theater prevention clause in inheritance clause accordingly. No changes to normative content.

**v0.3.4 (March 2026):** Pre-publication check pass. Six fixes. (1) Section 3.1.1: "Witness Layer" replaced with "detection layer," completing the generalization pass from v0.3.0. (2) Section 5.4 SCLS-Accountable: "defined window" given three validity conditions (specified before adoption, publicly documented, short enough that inaction is detectable before the next governance cycle in which the deficit could compound); governance cycle length required as a co-specified public document alongside the window. (3) Section 7.5: Added "(forthcoming)" notation to Proof of Coordination Architecture reference for consistency with other standards in the stack. (4) Section 9.2: "design question for the Witness Layer Technical Paper" replaced with "design question for the detection layer specification of any adopting system." (5) Section 9.3: "Coordination Improvement Proposal zones" and "genesis cohort deliberation" replaced with domain-general equivalents. (6) Section 8.1 added: Precision-First inheritance clause at PFDS-Operational tier. Changelog formatting fix: unclosed bold marker in v0.3.2 entry corrected.

**v0.3.3 (March 2026):** Tier 4 and Tier 5 normative content. Replaced Sections 5.4 (SCLS-Accountable) and 5.5 (SCLS-Auditable) placeholders with full normative specifications. SCLS-Accountable requires: every consent failure detection output (shadow dynamic detection, implausible standing claim absence, or invariant violation per Section 3.4) produces a documented governance review within a defined window (record includes consent failure identifier, classification, outcome, responsible actor, and rationale); automatic disclosure to all governance actors when no review is documented within the window, without requiring any actor's initiation; append-only governance review record; annual tier review including governance loop integrity check. SCLS-Auditable requires all SCLS-Accountable requirements plus: complete consent failure record accessible to an independent auditor without operator cooperation; verifiable completeness (detection architecture produces a count or hash of outputs against which the record can be checked); verifiable classification integrity (shadow dynamic taxonomy and invariant tests applied consistently); verifiable response completeness (every detection output produced a review or automatic disclosure); documented audit reports retained in governance record under append-only constraints; audit reports made available to participant population within a defined period.

**v0.3.2 (March 2026): Conformance theater prevention pass. Added disclosure specification paragraph to the Relationship to the Structural Integrity Pentad section specifying four required elements for a substantive structural exposure disclosure. Added theater prevention clause to inheritance clause specifying that partial adoption does not constitute pentad conformance and requires a structural exposure disclosure per the Proof of Coordination Architecture document. No changes to normative content.

v0.3.1 (March 2026):** Tier rename propagation. Renamed three adoption tiers from aware/structured/critical to Assessed/Operational/Instrumented throughout (Sections 5.1 through 5.3, inline tier-differentiated guidance, and inheritance clause). Added Tier 4 (Accountable) and Tier 5 (Auditable) placeholder sections (5.4 and 5.5) with normative content to be specified in a future session. Updated Section 7.5 from Structural Integrity Triad to Structural Integrity Pentad: rewrote body to name all five standards, updated conformance threshold from "highest tier" to Tier 4 (Accountable), and added structural exposure disclosure requirement for partial adopters. Added Sensemaking Layer Standard relationship note to Section 7.5. Updated header and companion standard preamble from triad to pentad. Updated inheritance clause to list all five tier options. No changes to normative content of Sections 1 through 4, 6, or Sections 8 through 9.

**v0.3.0 (March 2026):** Generalization pass. Standard renamed from
Structural Consent and Legibility Standard to Structural Consent
Legibility Standard; "legibility" reframed as a property of consent
rather than a parallel concern. PoC-specific coupling removed throughout:
inheritance declarations in header replaced with companion standards
note; Section 1 Purpose generalized (web3 governance mechanisms become
examples of the general problem, not the frame); Section 4.2 Data
Consent web3 landscape survey replaced with cross-domain general
framing; Section 4.5.1 tenant language replaced with participating
organization; Section 5.3 and 5.3.1 Adverse-Signal Engagement Principle
references replaced with generic adverse signal processing language;
Witness Layer references replaced with detection layer; Quadratis
example in Section 6.1 replaced with generic example; Section 6.3
document stack and PoC cross-references (Coordination Improvement
Proposal Governance, Adverse-Signal Engagement Principle Core Standard,
Information Asymmetry Classification Standard) replaced with
self-contained descriptions; Section 6.4 protocol stack reference
generalized; Section 7.1 and 7.2 rewritten as generic companion
standard relationship descriptions rather than named PoC standard
conformance; Section 7.2.1 Adverse-Signal Engagement Principle
Conformance Points removed in full; Section 7.5 Structural Integrity
Triad reframed to describe the triad architecture without naming
specific standards; Section 8 Inheritance Clause rewritten for any
adopting system and updated to reflect new standard name. Corrected
Signal Maturation to Signal Escalation in Section 3.1.1 (existing
inconsistency from pre-v0.2.2 text). The PoC-specific conformance layer
previously embedded in this standard migrates to the Proof of
Coordination Protocol Specification v2.6.5 or a dedicated conformance
addendum.

**v0.2.4 (February 2026):** Revised opening of Section 1 (Purpose). Replaced scope sentence with structural-argument framing establishing that the gap between claimed and structural consent is the mechanism through which extraction operates inside governed systems. All content from second paragraph onward unchanged.

**v0.2.3 (February 2026):** Added Section 7.2.1 (Adverse-Signal
Engagement Principle Conformance Points). Consolidates six explicit
compliance points following the pattern established in Witness Layer
Technical Paper Section 7.4: consent failures as adverse signals
(Section 3.4), shadow dynamics detection architecture (Section 5.3.1),
Signal Escalation for consent disputes (Section 6.3), standing
evaluation as adverse signal source (Section 3.1.1), bandwidth
dependency on Notice (Section 7.2), and domain-calibrated consent
process shape (Section 6.4). Each compliance point names the
Adverse-Signal Engagement Principle obligation it satisfies (Notice,
Name, or Navigate). Source: cross-document Adverse-Signal Engagement
Principle compliance pass.

**v0.2.2 (February 2026):** Renamed "Signal Maturation" to "Signal
Escalation" throughout (Sections 5.3.1, 6.3, 6.4). The term "maturation"
creates a conceptual collision with the developmental maturation
trajectory defined in the Developmental Signal Paper; "escalation"
describes the mechanism more precisely. Source: Developmental Signal
Paper, Section 5.4.

**v0.2.1 (February 2026):** Added learning loop bandwidth prerequisite
paragraph to Section 6.3. Maps bandwidth types to learning loop depths:
epistemic bandwidth is the prerequisite for single-loop learning,
ontological bandwidth for double-loop and triple-loop learning. A system
that does not invest in ontological bandwidth structurally caps itself
at single-loop learning regardless of formal governance provisions.
Cross-references: Coordination Improvement Proposal Governance, Section
4; Adverse-Signal Engagement Principle Core Standard, Section 3.3.7.

**v0.1-skeleton (February 2026):** Initial structural skeleton.
Established: foundational framework (Wheel of Consent with attribution),
three invariants (Identify, Authorize, Verify), consent failures as
adverse signals, five consent domains with shadow dynamic mapping and
OCAP/CARE cross-references, three adoption tiers, inheritance clause,
and relationship to Precision-First and Adverse-Signal Engagement
Principle standards. Bandwidth section and OCAP/CARE integration are
placeholders pending research. Detection architecture for shadow
dynamics is an open design question.

**v0.2 (February 2026):** Populated from Research Questions Register
session. Added: structural test for consent validity (Section 2.3.1:
negotiated limits, bidirectional awareness, revocability). Standing
evaluation mechanism (Section 3.1.1: self-identification,
evidence-backed evaluation, implausible absence detection, distributed
evaluation). Delegation scope for participation consent (Section 4.3.1).
Three-level observation consent architecture (Section 4.5.1).
Individual-vs-organizational consent resolution (Section 4.6.1). Shadow
dynamics detection architecture with three-signal model (Section 5.3.1).
Bandwidth and consent framework with four system obligations and four
bandwidth types (Section 6). Bandwidth as cross-cutting design
constraint (Section 6.3). Cynefin action modes and consent process shape
as cross-cutting principle (Section 6.4). OCAP/CARE integration layer
with mapping table, compliance bridge, and non-absorption clause
(Section 7.4). Structural integrity pentad designation (Section 7.5).
Updated inheritance clause to include domain identification (Section 8).
Resolved open design questions 9.1, 9.2, and 9.4; partially resolved
9.3; added 9.6 (meta-consent). Grounded Data consent domain in current
landscape survey (Section 4.2). Added Adverse-Signal Engagement
Principle bandwidth dependency note (Section 7.2). Source: Research
Questions Register Session Handoff, February 24, 2026.
