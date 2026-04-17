---
title: Coordination Scaling Standard
document_id: standards-2_6-coordination-scaling-0_1_0.md
ring: Standards (2.6)
version: v0.1.0
date: 2026-04-17
status: Normative. Seventh Tensegrity Compressive Standard in the Coordination Structural Integrity Suite. Radius 5 through Radius 150 specifications are normative. Radius 500 and Radius 1500 specifications are provisional pending validation through cohort experience at those thresholds.
abbreviation: CSS
---

# Coordination Scaling Standard

## Preamble

Every coordination system operates at a scale. Scale is not incidental to coordination: it determines which coordination functions are structurally possible, which informal mechanisms hold, which formal structures become necessary, and which exploitation vectors open. A coordination system that works at fifteen people will not work the same way at fifty. A system that works at fifty will face structural breaks at one hundred fifty that it is not designed to survive.

Most coordination failures are diagnosed by their symptoms: conflict escalation, norm violations, power concentration, sensemaking breakdown. These are real failures. But the structural cause is often prior and simpler: the coordination system crossed a scale threshold without installing the structural conditions that threshold requires. The failure was predictable. It was not predicted because no one named the threshold or specified what crossing it without preparation produces.

This standard closes that gap. It specifies, for each Dunbar-scale threshold, the structural conditions that must be in place before crossing (the Board), the structural conditions whose absence enables capture (the Dome), the exploitation vectors that open at the threshold (the attack surface), and the interface conditions a conformant unit presents at its boundary.

A coordination system conformant with this standard does not guarantee coordination health. It guarantees that the structural conditions required for coordination to be possible at its current scale are present; the conditions enabling scale-specific capture are absent. The other standards in the Coordination Structural Integrity Suite specify the structural conditions required within those conditions.

Scale-blindness is a precision deficit. A specification of structural conditions that does not account for scale is imprecise: it implies conditions hold across all scales when they do not. This standard is the instrument that makes scale-precision a conformance obligation.

---

## Changelog

| Version | Date | Notes |
|---------|------|-------|
| v0.1.0 | 2026-04-17 | Initial normative standard. Promoted from bucket/bucket-dunbar-layer-architecture-0_1_0.md (v0.1.2). Radius 5 through 150 normative; Radius 500 and 1500 provisional. Board/Dome vocabulary applied throughout. Adoption architecture added. |

---

## Section 1: Purpose and Scope

This standard applies to any coordination unit (a project, organization, DAO, working group, protocol, or any other structured group of people coordinating toward a shared purpose). It applies regardless of domain, legal structure, or technological substrate.

The standard specifies the structural conditions required for coordination to function at each Dunbar-scale threshold. It does not specify how to organize. It specifies what must be structurally present and what must be structurally prevented at each scale, so that coordination at that scale is possible.

The standard is organized around six Radii: Radius 5, Radius 15, Radius 50, Radius 150, Radius 500, and Radius 1500. Each Radius names a coordination segment defined by the relational threshold at which specific coordination functions change. The Radii are nested: a unit operating at Radius 150 is also operating at Radius 50, 15, and 5. All Board conditions for all crossed thresholds apply simultaneously.

Radius 5 through Radius 150 specifications are normative. Radius 500 and Radius 1500 specifications are provisional and are included as theoretical reference. The provisional specifications represent the best current architectural understanding and require validation through cohort experience at those thresholds before normative status is appropriate.

---

## Section 2: Foundational Constructs

**Radius.** A Dunbar-scale coordination segment defined by the relational threshold at which specific coordination conditions change. A Radius names a nested coordination unit characterized by what coordination is structurally possible within it, what interface conditions exist at its boundary, what Board conditions are required, and what Dome conditions must not be absent. Six Radii are defined: Radius 5, Radius 15, Radius 50, Radius 150, Radius 500, Radius 1500, numbered by approximate relational threshold. Radii are nested; smaller Radii are contained within larger ones.

**Effective Radius.** The Radius at which a coordination unit is actually operating, determined by an aggregate of at minimum: the number of members, the developmental alignment distribution of those members, the frequency and quality of their interaction, the depth of shared context, and the communication medium mix. Effective Radius is not headcount alone. A group of 150 members with high developmental alignment and strong shared context may sustain Radius 150 coordination functions. A group of 80 members with wide developmental variance and shallow shared context may not. The Board conditions in this standard apply to the effective Radius, not the nominal headcount.

**Board.** The structural conditions that must be in place at a given Radius for coordination at that Radius to be possible. A Board condition is a minimum structural requirement: without it, specific coordination functions cannot be maintained and the attack surface at that threshold opens. A unit that has crossed a threshold without its Board installed is operating in the broken state that the Board prevents. Boards are Radius-specific: the Board that closes the attack surface at Radius 50 is not the Board that closes it at Radius 150. All Boards for all crossed thresholds must be present simultaneously.

**Dome.** The structural condition whose absence is the precondition for capture at a given Radius. An absent Dome means the coordination unit can expand into territory without structural limit, concentrate authority without structural check, or allow any single actor's influence to grow without structural constraint. The Dome does not prevent growth or authority; it prevents growth and authority from becoming structurally unchecked. Absent Dome at any crossed threshold is a conformance failure.

**Threshold crossing.** The transition across a Radius boundary. A crossing occurs when a unit's effective Radius moves from below a threshold to above it. A crossing without the appropriate Board installed opens the attack surface at that threshold immediately. Thresholds are crossed as aggregate conditions, not as headcount events: effective developmental alignment, interaction quality, and shared context depth change alongside headcount.

**Founding window.** The period before a threshold crossing during which the Board for the next Radius can be installed most effectively. The founding window closes at the crossing. Installing a Board after the crossing is structurally possible but is opposed by the coordination conditions the absent Board produces. Installing a Board during the crisis that the absent Board creates produces poor Board architecture. The standard requires that each Board be installed before the threshold is crossed.

**Born-below condition.** A coordination unit can begin its existence below the effective Radius its coordination purpose requires, not through insufficient headcount but through insufficient developmental alignment, shared context depth, or interaction quality. A unit born below a threshold it is already operating above has never had the Board for that threshold. It does not experience the absence as loss; it experiences it as the normal condition of its existence. This is the most structurally dangerous configuration because there is no prior state to restore. The Board must be built from inside the broken state.

---

## Section 3: Design Constraints

**Effective Radius is an aggregate condition, not a headcount event.** The conditions specified in this standard apply to a unit's effective Radius. Headcount is one input to effective Radius determination but is not the sole determinant. A unit must assess its effective Radius before determining which Board conditions apply.

**Boards are Radius-specific.** Each threshold breaks a different coordination function and requires a different Board. The Board for Radius 50 does not substitute for the Board for Radius 150. Adding members of lower developmental alignment can reduce the effective Radius even as headcount rises. Raising developmental alignment can raise the effective Radius without adding members. Both directions of change affect which Boards are required.

**All Boards for all crossed thresholds apply simultaneously.** A unit that has crossed Radius 150 is simultaneously subject to the Board conditions for Radius 5, 15, 50, and 150. Conformance requires all Board conditions for all crossed thresholds to be present. Conformance with Radius 150 Board conditions alone, without Radius 5 through 50 conditions, is not conformance.

**The sequential build requirement.** Each threshold crossing is a founding window moment. The Board for the next Radius must be installed before crossing. This is a sequential constraint: a unit cannot install the Radius 150 Board before the Radius 50 Board, because the Radius 50 Board is a structural precondition for the Radius 150 Board to function. Sequence violations produce compound structural debt.

**Each Board simultaneously closes an attack surface.** The structural conditions required for coordination at each Radius are identical to the structural conditions required to close the adversarial opening that the threshold creates. Specifying the Board for coordination purposes and specifying the defense against the threshold attack surface are the same act.

**The boundary model is correct.** The Radius thresholds represent qualitatively different relationship types with different cognitive and social demands, not points on a single continuum. A 2022 mathematical treatment (Tamarit, Sánchez, and Cuesta, *Scientific Reports*) showed that discrete thresholds emerge naturally from continuous resource-constraint optimization across three large empirical datasets. The layer breaks are real structural features, not arbitrary divisions. This standard's design logic rests on the boundary model.

**Radius 500 and 1500 are provisional.** The specifications for Radius 500 and Radius 1500 represent the best current theoretical understanding. They require validation through cohort experience at those thresholds. Designing for current AI or current institutional forms at upper Radii would embed constraints that do not survive the conditions those Radii produce. The provisional specifications name functional requirements; they do not specify implementation.

---

## Section 4: Radius 5

### 4.1 Threshold Justification

Below five members, every relationship in the group can be held in working memory simultaneously. Each member can track the current state of every other member and every relationship between members without structural support. Above five, this is no longer possible. Full bilateral awareness that informal coordination assumes becomes cognitively unavailable. State opacity (not knowing someone's actual state) becomes structurally possible for the first time.

### 4.2 Attack Surface

An actor whose actual intentions or state are unknown to others can be introduced into the group. The attack surface is state opacity: the group cannot informally verify what it informally assumed it could verify. A manufactured identity or misrepresented state introduced into a small team whose members cannot hold all relationship states simultaneously is the entry mechanism.

### 4.3 Board

Full mutual state legibility must be maintained explicitly rather than assumed informally. Each member's current capacity, commitment, and significant concerns must be knowable to all other members through a minimal explicit mechanism.

The Board condition is absent when any member's state is structurally opaque to the group: the group's knowledge of a member's current state depends on that member choosing to disclose rather than on a structural mechanism that makes the state legible.

The Board does not require surveillance. It requires structural design so that state is maintained as a shared artifact rather than as individually held private information.

### 4.4 Dome

No single member can hold veto power over all others without the explicit, renewed consent of the group. Absent Dome: dyadic dominance. One member structurally controls the group's decisions, resource access, or narrative, not through formal authority but through the informal power that state opacity and bilateral awareness failure enable at this scale.

### 4.5 Interface Conditions

A Radius 5 unit presents at its boundary: a confirmed mutual state legibility mechanism; the absence of unilateral veto structure; and a named coordination purpose that is legible to adjacent Radii.

---

## Section 5: Radius 15

### 5.1 Threshold Justification

Below fifteen members, informal mutual support networks function through direct relationship. Sympathy group coherence (the capacity to mobilize care, attention, and resources for a member in distress) is maintained through personal knowledge and relationship. Above fifteen, this coherence fragments. Not everyone knows everyone's situation well enough to mobilize informally. The sympathy network the group assumed it had begins to fail structurally.

### 5.2 Attack Surface

Social isolation and trust exploitation become structurally possible. An actor can exploit the sympathy network's fragmentation to isolate a target: reducing their access to informal support while maintaining the appearance of group normalcy. Social engineering operates at this Radius by exploiting the gap between what the sympathy network believes about members' states and what is actually true.

### 5.3 Board

An explicit mutual support architecture. The sympathy network function must be structurally maintained rather than informally assumed. At minimum: a named mechanism through which members signal distress or need, and a named mechanism through which the group responds. The Board is absent when the sympathy function is assumed to work informally at a scale where it structurally cannot.

### 5.4 Dome

No member can be structurally isolated from the support network. Isolation used as a control mechanism, reducing a member's access to sympathy network resources to increase their dependence on a single relationship, is the Dome failure condition at this Radius. Absent Dome: coercive control through isolation.

### 5.5 Interface Conditions

A Radius 15 unit presents at its boundary: an explicit mutual support architecture; an isolation prevention mechanism; and confirmed state legibility from Radius 5 maintained at scale.

---

## Section 6: Radius 50

### 6.1 Threshold Justification

Below fifty members, informal knowledge of who can do what (who has which skills, what domain knowledge, what current capacity, what coordination functions depend on them) is commonly held and regularly updated through direct interaction. Above fifty, this informal capacity inventory becomes unreliable. Members begin to not know what other members can do. The informal staffing mechanism that matched tasks to people through relational knowledge stops functioning. Formal role clarity becomes structurally necessary.

### 6.2 Attack Surface

Authority claims without verification become structurally possible. An actor can claim competence, authority, or role responsibility the group cannot informally check. Single points of failure concentrate invisibly: one person holds knowledge or relationships that no one else knows are load-bearing, and when they leave, the group discovers the dependency only through the failure.

### 6.3 Board

Explicit role and capacity legibility. What each member can do, what they are responsible for, and what coordination functions depend on them must be explicitly recorded and maintained, not held informally. The record must be current, accessible to all members without permission, and specific about function rather than title.

Named redundancy for load-bearing functions. Every coordination function that would cause significant disruption if its primary holder became unavailable must have a named redundancy or succession plan. A load-bearing function is any function where "what happens if the primary holder leaves tomorrow?" does not have a named answer.

The Board is absent when role knowledge is assumed to be informally shared at a scale where it cannot be, or when any load-bearing function has no named redundancy.

### 6.4 Dome

No single member or small cluster can hold multiple load-bearing roles without structural acknowledgment and explicit consent from the group. Absent Dome: concentrated dependency that creates coercive leverage: the actor holding multiple load-bearing functions can extract concessions by implying or threatening withdrawal. The Dome prevents invisible power concentration through role accumulation.

### 6.5 Interface Conditions

A Radius 50 unit presents at its boundary: an explicit role and capacity record; named redundancy for all load-bearing functions; and mutual support architecture from Radius 15 maintained at scale.

---

## Section 7: Radius 150

### 7.1 Threshold Justification

Below one hundred fifty members, informal reputation-based norm enforcement functions: when someone violates a shared norm, word travels through personal relationship networks and social consequences reach the violator. Above one hundred fifty, not everyone knows everyone. Reputation signals attenuate. Norm violations can occur without social consequences reaching the violator because the informal network that would carry those consequences has fragmented. Formal structures for norm maintenance become structurally necessary.

This is the primary Dunbar threshold and the anchor Radius for the current corpus. It is also the threshold at which the founding window condition becomes critical for shared language and foundational commitments.

### 7.2 Attack Surface

Norm violation without informal consequences becomes structurally possible. An adversarial actor can violate shared norms and the informal reputation mechanism that would sanction them has insufficient reach. Institutions designed for cooperative conflict have no purchase on actors who have decided the institution itself is the target.

Simultaneously: the founding window closing without Board installation. If a coordination system crosses Radius 150 without establishing the conditions described in Section 7.3, it has crossed into a scale where informal transmission of founding context is no longer reliable; the Board cannot be installed retroactively without a crisis that makes installation desperate, which produces poor Board architecture.

### 7.3 Board

The Radius 150 Board requires four structural conditions, each closing a distinct coordination function break at this threshold:

**Shared language and foundational commitments architecturally transmitted.** The founding window is established: shared language has been transmitted through a constitutional-layer mechanism rather than informally held by founding members, and foundational commitments are accessible to all members as a structural artifact rather than as institutional memory. The mutual support architecture from smaller Radii is maintained at this scale.

**Individual capacity structurally sustained.** The generative architecture that sustains individual capacity across the membership is economically structured rather than voluntarist. Coordination functions that depend on discretionary personal effort (conflict transformation, sensemaking, recognition labor) are explicitly resourced and compensated. The Board is absent when these functions are assumed to run on goodwill at a scale where that assumption no longer holds.

**Infrastructure integrity with named redundancy.** Minimum infrastructure integrity for the coordination functions the group depends on. No single actor holds infrastructure access, system knowledge, or external relationships without a named redundancy or succession plan. Load-bearing infrastructure functions are explicitly documented.

**Coordination operability.** Coordination decisions can be operationalized without requiring voluntary compliance from every actor in the group. No single points of failure exist in the coordination execution path. This is the structural prerequisite for formal norm enforcement at this Radius: a coordination mechanism that depends on universal voluntary compliance cannot enforce norms against the actors most likely to violate them.

The Board is absent when any of the four conditions is missing. Partial Board installation is not conformance; the four conditions are constitutively interdependent.

### 7.4 Dome

No single actor or small faction holds veto power over coordination mechanisms. No single actor holds the founding context as exclusive knowledge; the founding context must be architecturally transmitted and accessible to all members, not held as information asymmetry by founding members. Absent Dome: founder capture. The founding team retains structural control beyond the founding window through information asymmetry, relationship networks, or coordination design that preserves founding-moment power at operating scale.

### 7.5 Interface Conditions

A Radius 150 unit presents at its boundary: all four Board conditions confirmed present (shared language transmitted, individual capacity structurally sustained, infrastructure integrity with redundancy, coordination operability); generative architecture economically structured; formal norm enforcement mechanism operational; founding context architecturally transmitted rather than informally held; and all lower-Radius interface conditions maintained at scale.

---

## Section 8: Radius 500 (Provisional)

*The following specification is provisional. It represents the best current theoretical understanding and requires validation through cohort experience at this threshold before normative status is appropriate. The specification names functional requirements. Specific implementation is not specified and must not be assumed to be equivalent to any form available in 2026.*

### 8.1 Threshold Justification

Below five hundred members, a single shared narrative (a common understanding of what the group is, what it is doing, and why) can be maintained through cultural transmission and direct interaction. Above five hundred, factions naturally form around competing narratives. The single shared narrative fragments into distinct interpretive communities with genuinely different understandings of the group's purpose and history.

### 8.2 Attack Surface

Narrative capture and disinformation become structurally effective. A single adversarial narrative does not need to capture the whole group: it only needs to become one of several competing narratives and exploit the factional structure. The informal consensus mechanism that would identify false claims as false has already fragmented. Additionally: the ontological surface (the shared language that makes cross-unit coordination possible) degrades through informal transmission at this scale. Units using the same words begin to mean different things by them.

### 8.3 Board (Provisional)

Ontological surface: formal specification of the shared language that makes cross-unit coordination possible, machine-readable where feasible, precise enough that units implementing the same interface are using the same concepts rather than the same words.

Plural narrative architecture: formal acknowledgment that multiple narratives exist, named processes for surfacing and mediating narrative conflicts, and structural protection against any single narrative claiming to represent the whole group's perspective.

Detection architecture structural rather than social: monitoring of coordination signals at scale without depending on human monitoring of every signal.

### 8.4 Dome (Provisional)

No single narrative can claim exclusive authority to represent the group's founding context or current purpose. No single faction can capture the ontological surface and use it to privilege their interpretive frame over others.

### 8.5 Interface Conditions (Provisional)

A Radius 500 unit presents at its boundary: an ontological surface specification confirmed and accessible to adjacent units; plural narrative architecture operational; detection architecture structural; and all Radius 150 interface conditions maintained at scale.

---

## Section 9: Radius 1500 (Provisional)

*The following specification is provisional. It represents the best current theoretical understanding and requires validation through cohort experience at this threshold before normative status is appropriate.*

### 9.1 Threshold Justification

Below fifteen hundred members, coordinated action can be maintained through relatively flat coordination structure with some formal instrumentation. Above fifteen hundred, the coordination load exceeds what any coordination structure without significant administrative apparatus can carry. Bureaucratic coordination becomes structurally required: specialized roles for coordination functions, hierarchical decision routing, formal record-keeping systems.

### 9.2 Attack Surface

Administrative capture: whoever controls the administrative apparatus controls the coordination system. The formal institutional layer built to make coordination possible becomes the primary capture vector. An actor who controls record-keeping, resource allocation routing, or decision authorization processes has structural leverage over the entire group regardless of what coordination documents say.

### 9.3 Board (Provisional)

Administrative apparatus designed for functional independence from external coercion: the administrative functions of the group must be capable of operating without requiring permission or cooperation from any external party whose interests may conflict with the group's foundational commitments. No single administrative actor or small cluster holds exclusive control over the coordination record, resource allocation, or decision authorization.

Amendment mechanism: a formal process by which foundational commitments can be updated as understanding deepens, without requiring commitments to be frozen at founding-moment understanding. Future participants must be able to apply foundational commitments to conditions not yet imagined without being bound to the specific mechanisms of the founding moment.

Conditions-of-possibility guardianship: a named structural mechanism for representing the interests of parties affected by the group's coordination who cannot participate through standard mechanisms, including future members whose conditions for genuine participation the current group is responsible for maintaining.

### 9.4 Dome (Provisional)

No administrative apparatus holds exclusive jurisdiction over the coordination record. No single actor or small cluster uses administrative control to concentrate founding-context knowledge as exclusive power. The constitutional layer of foundational commitments remains accessible to all members as a resource for evaluating administrative actions, not held as specialist knowledge controlled by administrators.

### 9.5 Interface Conditions (Provisional)

A Radius 1500 unit presents at its boundary: administrative independence from external coercion confirmed; amendment mechanism operational and accessible; conditions-of-possibility guardianship named and functioning; and all Radius 500 interface conditions maintained at scale.

---

## Section 10: Effective Radius Assessment

A coordination unit determines its effective Radius by assessing the aggregate of: member count; developmental alignment distribution; interaction frequency and quality; shared context depth; and communication medium mix.

The effective Radius is the highest Radius at which the unit can maintain the coordination functions that Radius requires. Assessment questions:

**Can all members hold all other members' current states in working memory without structural support?** If yes: Radius 5 or below. If no: Radius 5 has been crossed.

**Does the sympathy network (the capacity to mobilize care and resources for a member in distress) function through direct personal knowledge of all members?** If yes: below Radius 15. If no: Radius 15 has been crossed.

**Is informal knowledge of who can do what, and what coordination functions depend on whom, commonly held and regularly updated through direct interaction?** If yes: below Radius 50. If no: Radius 50 has been crossed.

**Does informal reputation-based norm enforcement function: can norm violations reliably reach their social consequences through personal relationship networks?** If yes: below Radius 150. If no: Radius 150 has been crossed.

**Can a single shared narrative be maintained through cultural transmission and direct interaction across the full membership?** If yes: below Radius 500. If no: Radius 500 has been crossed (provisional).

Once crossed thresholds are identified, the unit assesses which Board conditions are present for each crossed threshold and which are absent. All absent Board conditions for all crossed thresholds are conformance gaps.

---

## Section 11: Adoption Architecture

### CSS-Assessed

The coordination unit has identified its effective Radius using the assessment method in Section 10. It has named which thresholds it has crossed. It has documented which Board conditions for crossed thresholds are present and which are absent. The gap map is complete.

CSS-Assessed does not require Board conditions to be installed. It requires honest identification of the current state.

### CSS-Operational

The coordination unit has installed Board conditions for its current effective Radius and all lower crossed thresholds. All Board conditions for all crossed thresholds are structurally present. Dome conditions for all crossed thresholds are absent (capture vectors are closed).

CSS-Operational requires that the conditions be structural (embedded in the unit's architecture) rather than aspirational or policy-stated.

### CSS-Instrumented

The coordination unit has a structural mechanism for detecting when it is approaching the next threshold. It is monitoring the aggregate conditions (member count, developmental alignment, interaction quality, shared context depth) that determine effective Radius. It has a founding window protocol: a named plan for installing the next Board before the next threshold is crossed.

CSS-Instrumented requires active detection, not reactive assessment.

### CSS-Loop-Closed

The coordination unit has crossed at least one threshold with its Board installed in advance; it has executed a founding window protocol and validated that the Board installation was effective after the crossing. The founding window process has been tested against the lived experience of a threshold crossing and corrected from practice where the specification proved incomplete.

CSS-Loop-Closed requires evidence of at least one executed and validated threshold crossing.

### CSS-Auditable

An independent observer (someone with no prior relationship to the coordination unit) can assess the unit's effective Radius, identify all crossed thresholds, verify that Board conditions for all crossed thresholds are structurally present, verify that Dome conditions for all crossed thresholds are absent, and produce a finding without requiring access to information the unit controls. All interface conditions for all crossed thresholds are documented and externally legible.

---

## Section 12: Tensegrity As A Whole

```
Coordination Structural Integrity Suite
├── Tensegrity Compressive Standards (closes exploitation vectors)
│   ├── Precision-First Design Standard [meta-standard]
│   ├── Adverse Signal Engagement Principle Core Standard
│   ├── Structural Consent Legibility Standard
│   ├── Information Asymmetry Classification Standard
│   ├── Structural Power Obligation Standard
│   ├── Regenerative Obligation Standard
│   └── Coordination Scaling Standard [precondition compressive]
└── Tensegrity Generative Standards (structural conditions for capacity)
    ├── Sensemaking Standard
    ├── Four Batteries Capacity Standard
    └── Conflict Transformation Standard
```

The Coordination Scaling Standard closes the scale-blindness exploitation vector: the structural break that occurs when a coordination system crosses a Dunbar-scale threshold without the structural conditions that threshold requires. It is precondition compressive: it specifies the structural substrate within which the other standards' conditions become possible at each scale. A coordination system operating below the Board conditions for its current Radius cannot reliably meet the conditions of the other compressive standards, because the coordination functions those standards protect have already broken at the threshold.

---

*Sources: Robin Dunbar, "Neocortex size as a constraint on group size in primates," Journal of Human Evolution, 1992; Tamarit, Sánchez, and Cuesta, "Beyond Dunbar circles: a continuous description of social relationships and resource allocation," Scientific Reports, 2022; bucket/bucket-dunbar-layer-architecture-0_1_0.md v0.1.2 (primary source document for this standard's architectural content).*
