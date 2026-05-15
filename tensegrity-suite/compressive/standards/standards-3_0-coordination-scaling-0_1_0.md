---
title: Coordination Scaling Standard
document_id: standards-2_6-coordination-scaling-0_1_0.md
ring: Standards (2.6)
version: v0.1.1
date: 2026-04-17
status: Normative. Seventh Tensegrity Compressive Standard in the Coordination Structural Integrity Suite. Radius 5 through Radius 150 specifications are normative. Radius 500 and Radius 1500 specifications are provisional pending validation through cohort experience at those thresholds.
abbreviation: CSS
---

# Coordination Scaling Standard

## Preamble

Every coordination system operates at a scale. Scale is not incidental to coordination: it determines which coordination functions are structurally possible, which informal mechanisms hold, which formal structures become necessary, and which exploitation vectors open. A coordination system that works at fifteen people will not work the same way at fifty. A system that works at fifty will face structural breaks at one hundred fifty that it is not designed to survive.

Most coordination failures are diagnosed by their symptoms: conflict escalation, norm violations, power concentration, sensemaking breakdown. These are real failures. But the structural cause is often prior and simpler: the coordination system crossed a scale threshold without installing the structural conditions that threshold requires. The failure was predictable. It was not predicted because no one named the threshold or specified what crossing it without preparation produces.

This standard closes that gap. It specifies, for each Dunbar-scale threshold, the minimum conditions that must be in place before crossing, the maximum conditions whose absence enables capture, the exploitation vectors that open at the threshold (the attack surface), and the interface conditions a conformant unit presents at its boundary.

A coordination system conformant with this standard does not guarantee coordination health. It guarantees that the structural conditions required for coordination to be possible at its current scale are present; the conditions enabling scale-specific capture are absent. The other standards in the Coordination Structural Integrity Suite specify the structural conditions required within those conditions.

Scale-blindness is a precision deficit. A specification of structural conditions that does not account for scale is imprecise: it implies conditions hold across all scales when they do not. This standard is the instrument that makes scale-precision a conformance obligation.

**Typological declaration** (Descriptive Typology Map v0.1.1)

*Operative classes*
- Structural-mechanical: this standard specifies structural conditions (minimum conditions, maximum conditions, threshold crossing requirements, sequential build requirement, founding window architecture) and assesses whether those conditions are embedded in a coordination unit's architecture. Primary vocabulary is structural specification and structural presence or absence.
- Relational-topological: this standard addresses the relational substrate of coordination (Dunbar-scale thresholds, sympathy networks, role and capacity dependencies, reputation network reach) and assesses coordination capacity as a function of relational network structure.
- Temporal-dynamic: this standard addresses threshold crossings as developmental events (founding window, sequential build requirement, born-below condition, trigger conditions for approach detection) and requires structural anticipation across a coordination unit's developmental arc.

*Boundary classes*
- Felt-experience: this standard assesses whether structural conditions are present at each scale threshold, not whether coordination feels appropriate, fair, or satisfying to participants. Structural accessibility of minimum conditions is within scope; subjective experience of operating under them is not.
- Epistemic-perceptual: this standard specifies what structural conditions must exist at each Radius, not how participants perceive or make meaning from their coordination context. Sensemaking capacity and shared understanding as experiential states are outside this standard's vocabulary; the structural conditions that make them possible at each Radius (such as shared language architecturally transmitted at Radius 150) are within scope only as minimum conditions.

---

## Changelog

| Version | Date | Notes |
|---------|------|-------|
| v0.1.3 | 2026-04-17 | Primary detection signals added to maximum conditions at Radius 5, 15, 50, and 150 (IACS pattern). Threshold approach signal note added to Section 10 (gradient vs. binary threshold). De-crossing and conflicting indicator resolution rules added to Section 3. Contextual baseline statement added to Section 10 (PFDS Corollary 9 requirement; Dunbar thresholds are research-derived approximations; functional questions are primary instrument). |
| v0.1.2 | 2026-04-17 | Developmental alignment distribution removed from Effective Radius factor list (proto-Frame Language sensemaking; belongs in Frame Language, not as a structural Radius input). Nominal and robust Effective Radius defined as distinct constructs. CSS-Instrumented monitoring requirement replaced with named trigger conditions approach; founding window activation criterion added (opens when first trigger fires). Contribution topology noted as PoC implementation path for robust Effective Radius and maximum conditions assessment. Typological declaration added in correct PFDS form (Descriptive Typology Map v0.1.1). Section 10 factor list explicitly linked to functional questions as their operative instrument. Section 12 stale Board conditions reference corrected. |
| v0.1.1 | 2026-04-17 | Board and Dome replaced throughout with Minimum Conditions and Maximum Conditions. Board/Dome are LayerCake visualization vocabulary and do not belong in normative standards text. Four Batteries language removed from Radius 150 minimum conditions. |
| v0.1.0 | 2026-04-17 | Initial normative standard. Promoted from bucket/bucket-dunbar-layer-architecture-0_1_0.md (v0.1.2). Radius 5 through 150 normative; Radius 500 and 1500 provisional. Adoption architecture added. |

---

## Section 1: Purpose and Scope

This standard applies to any coordination unit (a project, organization, DAO, working group, protocol, or any other structured group of people coordinating toward a shared purpose). It applies regardless of domain, legal structure, or technological substrate.

The standard specifies the structural conditions required for coordination to function at each Dunbar-scale threshold. It does not specify how to organize. It specifies what must be structurally present and what must be structurally prevented at each scale, so that coordination at that scale is possible.

The standard is organized around six Radii: Radius 5, Radius 15, Radius 50, Radius 150, Radius 500, and Radius 1500. Each Radius names a coordination segment defined by the relational threshold at which specific coordination functions change. The Radii are nested: a unit operating at Radius 150 is also operating at Radius 50, 15, and 5. All minimum conditions for all crossed thresholds apply simultaneously.

Radius 5 through Radius 150 specifications are normative. Radius 500 and Radius 1500 specifications are provisional and are included as theoretical reference. The provisional specifications represent the best current architectural understanding and require validation through cohort experience at those thresholds before normative status is appropriate.

---

## Section 2: Foundational Constructs

**Radius.** A Dunbar-scale coordination segment defined by the relational threshold at which specific coordination conditions change. A Radius names a nested coordination unit characterized by what coordination is structurally possible within it, what interface conditions exist at its boundary, what minimum conditions are required, and what maximum conditions must not be absent. Six Radii are defined: Radius 5, Radius 15, Radius 50, Radius 150, Radius 500, Radius 1500, numbered by approximate relational threshold. Radii are nested; smaller Radii are contained within larger ones.

**Effective Radius.** The Radius at which a coordination unit is actually operating, determined by an aggregate of at minimum: the number of members, the frequency and quality of their interaction, the depth of shared context, and the communication medium mix. Effective Radius is not headcount alone. A group of 150 members with strong shared context and high-frequency interaction may sustain Radius 150 coordination functions. A group of 80 members with thin shared context and low interaction quality may not. The minimum conditions in this standard apply to the effective Radius, not the nominal headcount.

**Nominal Effective Radius.** The Effective Radius a coordination unit presents with its full membership present. This is the standard output of a Section 10 assessment under normal operating conditions.

**Robust Effective Radius.** The threshold a coordination unit can sustain under worst-case single departure: the highest Radius at which minimum conditions would still hold if the highest-coordination-weight individual left. If any minimum condition for a crossed threshold would fail on a single departure, the robust Effective Radius is below the nominal Effective Radius. The gap between nominal and robust Effective Radius measures structural fragility due to coordination weight concentration. For organizations using PoC infrastructure, contribution topology assessment provides the instrument for this determination.

**Minimum Conditions.** The structural conditions that must be in place at a given Radius for coordination at that Radius to be possible. A minimum condition is a required structural specification: without it, specific coordination functions cannot be maintained and the attack surface at that threshold opens. A unit that has crossed a threshold without its minimum conditions installed is operating in the broken state that they prevent. Minimum conditions are Radius-specific: the minimum conditions that close the attack surface at Radius 50 are not the minimum conditions that close it at Radius 150. All minimum conditions for all crossed thresholds must be present simultaneously.

**Maximum Conditions.** The structural specification whose absence is the precondition for capture at a given Radius. Absent maximum conditions mean the coordination unit can expand into territory without structural limit, concentrate gravitas without structural check, or allow any single actor's influence to grow without structural constraint. Maximum conditions do not prevent growth or gravitas; they prevent growth and gravitas from becoming structurally unchecked. Absent maximum conditions at any crossed threshold is a conformance failure.

**Threshold crossing.** The transition across a Radius boundary. A crossing occurs when a unit's effective Radius moves from below a threshold to above it. A crossing without the appropriate minimum conditions installed opens the attack surface at that threshold immediately. Thresholds are crossed as aggregate conditions, not as headcount events: interaction quality, shared context depth, and communication medium mix change alongside headcount.

**Founding window.** The period before a threshold crossing during which the minimum conditions for the next Radius can be installed most effectively. The founding window closes at the crossing. Installing minimum conditions after the crossing is structurally possible but is opposed by the coordination conditions their absence produces. Installing minimum conditions during the crisis that their absence creates produces poorly designed specifications. The standard requires that minimum conditions for each threshold be installed before the crossing.

**Born-below condition.** A coordination unit can begin its existence below the effective Radius its coordination purpose requires, not through insufficient headcount but through insufficient shared context depth or interaction quality. A unit born below a threshold it is already operating above has never had the minimum conditions for that threshold. It does not experience the absence as loss; it experiences it as the normal condition of its existence. This is the most structurally dangerous configuration because there is no prior state to restore. Minimum conditions must be built from inside the broken state.

---

## Section 3: Design Constraints

**Effective Radius is an aggregate condition, not a headcount event.** The conditions specified in this standard apply to a unit's effective Radius. Headcount is one input to effective Radius determination but is not the sole determinant. A unit must assess its effective Radius before determining which minimum conditions apply.

**Minimum conditions are Radius-specific.** Each threshold breaks a different coordination function and requires different minimum conditions. The minimum conditions for Radius 50 do not substitute for those at Radius 150. Adding members into thin shared context or low-interaction conditions can reduce the effective Radius even as headcount rises. Deepening shared context and interaction quality can raise the effective Radius without adding members. Both directions of change affect which minimum conditions are required.

**All minimum conditions for all crossed thresholds apply simultaneously.** A unit that has crossed Radius 150 is simultaneously subject to the minimum conditions for Radius 5, 15, 50, and 150. Conformance requires all minimum conditions for all crossed thresholds to be present. Conformance with Radius 150 minimum conditions alone, without Radius 5 through 50 conditions, is not conformance.

**The sequential build requirement.** Each threshold crossing is a founding window moment. The minimum conditions for the next Radius must be installed before crossing. This is a sequential constraint: a unit cannot install Radius 150 minimum conditions before Radius 50 minimum conditions, because Radius 50 minimum conditions are a structural precondition for Radius 150 minimum conditions to function. Sequence violations produce compound structural debt.

**Each threshold's minimum conditions simultaneously close an attack surface.** The structural conditions required for coordination at each Radius are identical to the structural conditions required to close the adversarial opening that the threshold creates. Specifying minimum conditions for coordination purposes and specifying the defense against the threshold attack surface are the same act.

**The boundary model is correct.** The Radius thresholds represent qualitatively different relationship types with different cognitive and social demands, not points on a single continuum. A 2022 mathematical treatment (Tamarit, Sánchez, and Cuesta, *Scientific Reports*) showed that discrete thresholds emerge naturally from continuous resource-constraint optimization across three large empirical datasets. The layer breaks are real structural features, not arbitrary divisions. This standard's design logic rests on the boundary model.

**Effective Radius can decrease.** Adding members into thin shared context or low-interaction conditions reduces Effective Radius. Losing high-coordination-weight individuals can drop the robust Effective Radius below a previously crossed threshold. When reassessment indicates that a previously crossed threshold is no longer crossed by current aggregate conditions, this is a de-crossing event. Minimum conditions for the de-crossed threshold remain structurally valuable and should be maintained; the unit is no longer in conformance failure at that threshold but has gained a structural reserve that protects against future re-crossing.

**When assessment factors conflict, assess conservatively.** When different factors point in different directions (headcount suggests Radius 150 but interaction quality suggests Radius 50), assess at the higher threshold. The minimum conditions for the higher threshold are a structural floor that protects against the coordination break that factor inconsistency produces.

**Radius 500 and 1500 are provisional.** The specifications for Radius 500 and Radius 1500 represent the best current theoretical understanding. They require validation through cohort experience at those thresholds. Designing for current AI or current institutional forms at upper Radii would embed constraints that do not survive the conditions those Radii produce. The provisional specifications name functional requirements; they do not specify implementation.

---

## Section 4: Radius 5

### 4.1 Threshold Justification

Below five members, every relationship in the group can be held in working memory simultaneously. Each member can track the current state of every other member and every relationship between members without structural support. Above five, this is no longer possible. Full bilateral awareness that informal coordination assumes becomes cognitively unavailable. State opacity (not knowing someone's actual state) becomes structurally possible for the first time.

### 4.2 Attack Surface

An actor whose actual intentions or state are unknown to others can be introduced into the group. The attack surface is state opacity: the group cannot informally verify what it informally assumed it could verify. A manufactured identity or misrepresented state introduced into a small team whose members cannot hold all relationship states simultaneously is the entry mechanism.

### 4.3 Minimum Conditions

Full mutual state legibility must be maintained explicitly rather than assumed informally. Each member's current capacity, commitment, and significant concerns must be knowable to all other members through a minimal explicit mechanism.

Minimum conditions are absent when any member's state is structurally opaque to the group: the group's knowledge of a member's current state depends on that member choosing to disclose rather than on a structural mechanism that makes the state legible.

Minimum conditions do not require surveillance. They require structural design so that state is maintained as a shared artifact rather than as individually held private information.

### 4.4 Maximum Conditions

No single member can hold veto power over all others without the explicit, renewed consent of the group. Absent maximum conditions: dyadic dominance. One member structurally controls the group's decisions, resource access, or narrative, not through formal gravitas but through the informal power that state opacity and bilateral awareness failure enable at this scale.

Primary detection signals: one member consistently initiates and concludes decisions while others defer on contested questions; one member's absence stops coordination while others' absences do not; resource access or external contacts route exclusively through one member without the group's explicit authorization.

### 4.5 Interface Conditions

A Radius 5 unit presents at its boundary: a confirmed mutual state legibility mechanism; the absence of unilateral veto structure; and a named coordination purpose that is legible to adjacent Radii.

---

## Section 5: Radius 15

### 5.1 Threshold Justification

Below fifteen members, informal mutual support networks function through direct relationship. Sympathy group coherence (the capacity to mobilize care, attention, and resources for a member in distress) is maintained through personal knowledge and relationship. Above fifteen, this coherence fragments. Not everyone knows everyone's situation well enough to mobilize informally. The sympathy network the group assumed it had begins to fail structurally.

### 5.2 Attack Surface

Social isolation and trust exploitation become structurally possible. An actor can exploit the sympathy network's fragmentation to isolate a target: reducing their access to informal support while maintaining the appearance of group normalcy. Social engineering operates at this Radius by exploiting the gap between what the sympathy network believes about members' states and what is actually true.

### 5.3 Minimum Conditions

An explicit mutual support architecture. The sympathy network function must be structurally maintained rather than informally assumed. At minimum: a named mechanism through which members signal distress or need, and a named mechanism through which the group responds. Minimum conditions are absent when the sympathy function is assumed to work informally at a scale where it structurally cannot.

### 5.4 Maximum Conditions

No member can be structurally isolated from the support network. Isolation used as a control mechanism, reducing a member's access to sympathy network resources to increase their dependence on a single relationship, is the maximum conditions failure at this Radius. Absent maximum conditions: coercive control through isolation.

Primary detection signals: a member's participation in group communication decreases while one specific relationship intensifies; distress signals from one member go unacknowledged by the group but are received by a single other member; a member reports that only one other member understands their situation or can help them.

### 5.5 Interface Conditions

A Radius 15 unit presents at its boundary: an explicit mutual support architecture; an isolation prevention mechanism; and confirmed state legibility from Radius 5 maintained at scale.

---

## Section 6: Radius 50

### 6.1 Threshold Justification

Below fifty members, informal knowledge of who can do what (who has which skills, what domain knowledge, what current capacity, what coordination functions depend on them) is commonly held and regularly updated through direct interaction. Above fifty, this informal capacity inventory becomes unreliable. Members begin to not know what other members can do. The informal staffing mechanism that matched tasks to people through relational knowledge stops functioning. Formal role clarity becomes structurally necessary.

### 6.2 Attack Surface

Gravitas claims without verification become structurally possible. An actor can claim competence, positional gravity, or role responsibility the group cannot informally check. Single points of failure concentrate invisibly: one person holds knowledge or relationships that no one else knows are load-bearing, and when they leave, the group discovers the dependency only through the failure.

### 6.3 Minimum Conditions

Explicit role and capacity legibility. What each member can do, what they are responsible for, and what coordination functions depend on them must be explicitly recorded and maintained, not held informally. The record must be current, accessible to all members without permission, and specific about function rather than title.

Named redundancy for load-bearing functions. Every coordination function that would cause significant disruption if its primary holder became unavailable must have a named redundancy or succession plan. A load-bearing function is any function where "what happens if the primary holder leaves tomorrow?" does not have a named answer.

Minimum conditions are absent when role knowledge is assumed to be informally shared at a scale where it cannot be, or when any load-bearing function has no named redundancy.

### 6.4 Maximum Conditions

No single member or small cluster can hold multiple load-bearing roles without structural acknowledgment and explicit consent from the group. Absent maximum conditions: concentrated dependency that creates coercive leverage: the actor holding multiple load-bearing functions can extract concessions by implying or threatening withdrawal. Maximum conditions prevent invisible power concentration through role accumulation.

Primary detection signals: a member holds primary responsibility for more than two load-bearing functions and the group cannot name a redundancy for any of them; the answer to "what happens if this person is unavailable tomorrow?" is "we don't know" across multiple coordination domains simultaneously; a member's stated or implied withdrawal is sufficient to change a group decision.

### 6.5 Interface Conditions

A Radius 50 unit presents at its boundary: an explicit role and capacity record; named redundancy for all load-bearing functions; and mutual support architecture from Radius 15 maintained at scale.

---

## Section 7: Radius 150

### 7.1 Threshold Justification

Below one hundred fifty members, informal reputation-based norm response functions: when someone violates a shared norm, word travels through personal relationship networks and social consequences reach the violator. Above one hundred fifty, not everyone knows everyone. Reputation signals attenuate. Norm violations can occur without social consequences reaching the violator because the informal network that would carry those consequences has fragmented. Formal structures for norm maintenance become structurally necessary.

This is the primary Dunbar threshold and the anchor Radius for the current corpus. It is also the threshold at which the founding window condition becomes critical for shared language and foundational commitments.

### 7.2 Attack Surface

Norm violation without informal consequences becomes structurally possible. An adversarial actor can violate shared norms and the informal reputation mechanism that would sanction them has insufficient reach. Institutions designed for cooperative conflict have no purchase on actors who have decided the institution itself is the target.

Simultaneously: the founding window closing without minimum conditions installed. If a coordination system crosses Radius 150 without establishing the conditions described in Section 7.3, it has crossed into a scale where informal transmission of founding context is no longer reliable; minimum conditions cannot be installed retroactively without a crisis that makes installation desperate, which produces poorly designed specifications.

### 7.3 Minimum Conditions

Radius 150 minimum conditions require four structural conditions, each closing a distinct coordination function break at this threshold:

**Shared language and foundational commitments architecturally transmitted.** The founding window is established: shared language has been transmitted through a constitutional-layer mechanism rather than informally held by founding members, and foundational commitments are accessible to all members as a structural artifact rather than as institutional memory. The mutual support architecture from smaller Radii is maintained at this scale.

**Individual capacity structurally sustained.** Coordination functions that depend on discretionary personal effort are explicitly resourced and compensated rather than assumed to run on goodwill. Minimum conditions are absent when these functions are assumed to run on goodwill at a scale where that assumption no longer holds.

**Infrastructure integrity with named redundancy.** Minimum infrastructure integrity for the coordination functions the group depends on. No single actor holds infrastructure access, system knowledge, or external relationships without a named redundancy or succession plan. Load-bearing infrastructure functions are explicitly documented.

**Coordination operability.** Coordination decisions can be operationalized without requiring voluntary conformance from every actor in the group. No single points of failure exist in the coordination execution path. This is the structural prerequisite for formal norm response at this Radius: a coordination mechanism that depends on universal voluntary conformance cannot issue named responses to norm violations by the actors most likely to produce them.

Minimum conditions are absent when any of the four conditions is missing. Partial installation is not conformance; the four conditions are constitutively interdependent.

### 7.4 Maximum Conditions

No single actor or small faction holds veto power over coordination mechanisms. No single actor holds the founding context as exclusive knowledge; the founding context must be architecturally transmitted and accessible to all members, not held as information asymmetry by founding members. Absent maximum conditions: founder capture. The founding team retains structural control beyond the founding window through information asymmetry, relationship networks, or coordination design that preserves founding-moment power at operating scale.

Primary detection signals: founding members consistently hold information about coordination history or external relationships that current members cannot access independently; resource relationships or key external contacts route exclusively through founding members without named redundancy; founding-period decisions cannot be examined or contested by current members without founding member cooperation; the coordination mechanisms were designed in ways that systematically advantage actors present at founding.

### 7.5 Interface Conditions

A Radius 150 unit presents at its boundary: all four minimum conditions confirmed present (shared language transmitted, individual capacity structurally sustained, infrastructure integrity with redundancy, coordination operability); formal norm response mechanism operational; founding context architecturally transmitted rather than informally held; and all lower-Radius interface conditions maintained at scale.

---

## Section 8: Radius 500 (Provisional)

*The following specification is provisional. It represents the best current theoretical understanding and requires validation through cohort experience at this threshold before normative status is appropriate. The specification names functional requirements. Specific implementation is not specified and must not be assumed to be equivalent to any form available in 2026.*

### 8.1 Threshold Justification

Below five hundred members, a single shared narrative (a common understanding of what the group is, what it is doing, and why) can be maintained through cultural transmission and direct interaction. Above five hundred, factions naturally form around competing narratives. The single shared narrative fragments into distinct interpretive communities with genuinely different understandings of the group's purpose and history.

### 8.2 Attack Surface

Narrative capture and disinformation become structurally effective. A single adversarial narrative does not need to capture the whole group: it only needs to become one of several competing narratives and exploit the factional structure. The informal consensus mechanism that would identify false claims as false has already fragmented. Additionally: the ontological surface (the shared language that makes cross-unit coordination possible) degrades through informal transmission at this scale. Units using the same words begin to mean different things by them.

### 8.3 Minimum Conditions (Provisional)

Ontological surface: formal specification of the shared language that makes cross-unit coordination possible, machine-readable where feasible, precise enough that units implementing the same interface are using the same concepts rather than the same words.

Plural narrative architecture: formal acknowledgment that multiple narratives exist, named processes for surfacing and mediating narrative conflicts, and structural protection against any single narrative claiming to represent the whole group's perspective.

Detection architecture structural rather than social: monitoring of coordination signals at scale without depending on human monitoring of every signal.

### 8.4 Maximum Conditions (Provisional)

No single narrative can claim exclusive gravitas to represent the group's founding context or current purpose. No single faction can capture the ontological surface and use it to privilege their interpretive frame over others.

### 8.5 Interface Conditions (Provisional)

A Radius 500 unit presents at its boundary: an ontological surface specification confirmed and accessible to adjacent units; plural narrative architecture operational; detection architecture structural; and all Radius 150 interface conditions maintained at scale.

---

## Section 9: Radius 1500 (Provisional)

*The following specification is provisional. It represents the best current theoretical understanding and requires validation through cohort experience at this threshold before normative status is appropriate.*

### 9.1 Threshold Justification

Below fifteen hundred members, coordinated action can be maintained through relatively flat coordination structure with some formal instrumentation. Above fifteen hundred, the coordination load exceeds what any coordination structure without significant administrative apparatus can carry. Bureaucratic coordination becomes structurally required: specialized roles for coordination functions, hierarchical decision routing, formal record-keeping systems.

### 9.2 Attack Surface

Administrative capture: whoever controls the administrative apparatus controls the coordination system. The formal institutional layer built to make coordination possible becomes the primary capture vector. An actor who controls record-keeping, resource allocation routing, or decision authorization processes has structural leverage over the entire group regardless of what coordination documents say.

### 9.3 Minimum Conditions (Provisional)

Administrative apparatus designed for functional independence from external coercion: the administrative functions of the group must be capable of operating without requiring permission or cooperation from any external party whose interests may conflict with the group's foundational commitments. No single administrative actor or small cluster holds exclusive control over the coordination record, resource allocation, or decision authorization.

Amendment mechanism: a formal process by which foundational commitments can be updated as understanding deepens, without requiring commitments to be frozen at founding-moment understanding. Future participants must be able to apply foundational commitments to conditions not yet imagined without being bound to the specific mechanisms of the founding moment.

Conditions-of-possibility guardianship: a named structural mechanism for representing the interests of parties affected by the group's coordination who cannot participate through standard mechanisms, including future members whose conditions for genuine participation the current group is responsible for maintaining.

### 9.4 Maximum Conditions (Provisional)

No administrative apparatus holds exclusive jurisdiction over the coordination record. No single actor or small cluster uses administrative control to concentrate founding-context knowledge as exclusive power. The constitutional layer of foundational commitments remains accessible to all members as a resource for evaluating administrative actions, not held as specialist knowledge controlled by administrators.

### 9.5 Interface Conditions (Provisional)

A Radius 1500 unit presents at its boundary: administrative independence from external coercion confirmed; amendment mechanism operational and accessible; conditions-of-possibility guardianship named and functioning; and all Radius 500 interface conditions maintained at scale.

---

## Section 10: Effective Radius Assessment

**Contextual baseline.** The threshold numbers in this standard (5, 15, 50, 150) are derived from research conducted primarily in Western, industrialized, and digital-native organizational contexts. Units with significantly different structural contexts (very high pre-existing trust, co-located intensive interaction, non-Western cultural frameworks for group membership, or very low baseline interaction frequency) should treat the numbers as approximate anchors. The functional questions below are the primary instrument in all contexts; the threshold numbers are reference points for units without better calibration data.

A coordination unit determines its effective Radius by assessing the aggregate of: member count; interaction frequency and quality; shared context depth; and communication medium mix. The assessment questions below are the operative instrument for these factors: each question identifies the coordination function that breaks when a threshold is crossed, which is the observable equivalent of the aggregate conditions that produce the crossing.

The assessment questions below determine the nominal Effective Radius: the highest Radius at which the unit can maintain coordination functions under normal operating conditions. After completing the nominal assessment, the unit should assess its robust Effective Radius by identifying which minimum conditions for crossed thresholds would fail under worst-case single departure of a high-coordination-weight individual. A gap between nominal and robust Effective Radius is a maximum conditions concern regardless of whether the formal maximum conditions criteria are met.

For organizations without PoC infrastructure, the assessment questions below are the primary instrument. For organizations using PoC infrastructure, contribution topology output provides a direct instrument for robust Effective Radius determination and maximum conditions verification.

Assessment questions:

**Can all members hold all other members' current states in working memory without structural support?** If yes: Radius 5 or below. If no: Radius 5 has been crossed.

**Does the sympathy network (the capacity to mobilize care and resources for a member in distress) function through direct personal knowledge of all members?** If yes: below Radius 15. If no: Radius 15 has been crossed.

**Is informal knowledge of who can do what, and what coordination functions depend on whom, commonly held and regularly updated through direct interaction?** If yes: below Radius 50. If no: Radius 50 has been crossed.

**Does informal reputation-based norm response function: can norm violations reliably reach their social consequences through personal relationship networks?** If yes: below Radius 150. If no: Radius 150 has been crossed.

**Can a single shared narrative be maintained through cultural transmission and direct interaction across the full membership?** If yes: below Radius 500. If no: Radius 500 has been crossed (provisional).

Once crossed thresholds are identified, the unit assesses which minimum conditions are present for each crossed threshold and which are absent. All absent minimum conditions for all crossed thresholds are conformance gaps.

The assessment questions detect threshold crossing, not threshold approach. Coordination functions degrade before they break: the sympathy network becomes unreliable before it fails; informal role knowledge becomes patchy before it collapses. A unit that answers "yes" to a question while noticing that the function feels stressed or unreliable is detecting approach, not absence. Approach signals are not conformance findings, but they are the trigger conditions that should activate the founding window protocol for the next threshold.

---

## Section 11: Adoption Architecture

### CSS-Assessed

The coordination unit has identified its effective Radius using the assessment method in Section 10. It has named which thresholds it has crossed. It has documented which minimum conditions for crossed thresholds are present and which are absent. The gap map is complete.

CSS-Assessed does not require minimum conditions to be installed. It requires honest identification of the current state.

### CSS-Operational

The coordination unit has installed minimum conditions for its current effective Radius and all lower crossed thresholds. All minimum conditions for all crossed thresholds are structurally present. Maximum conditions for all crossed thresholds are absent (capture vectors are closed).

CSS-Operational requires that the conditions be structural (embedded in the unit's architecture) rather than aspirational or policy-stated. A condition is structural rather than policy-stated when its presence or absence is determinable by an independent observer using only the definition and observable evidence, without requiring the cooperation of the unit or any of its members.

### CSS-Instrumented

The coordination unit has a structural mechanism for detecting when it is approaching the next threshold, and a founding window protocol: a named plan for installing minimum conditions before the next threshold is crossed.

The detection mechanism does not require continuous measurement infrastructure. It requires named trigger conditions: specific observable signals that indicate a threshold may be approaching and that prompt a new Section 10 assessment. Trigger conditions vary by organization; examples include: membership has grown significantly since the last assessment; new members can no longer informally identify who is responsible for which coordination functions; informal knowledge of member states or capacities has become unreliable; a departure caused unexpected coordination failures; conflict escalation has increased without an identified cause. When any named trigger fires, the unit runs the Section 10 assessment to determine whether threshold approach has occurred.

The founding window for the next threshold opens when the first named trigger condition fires. From that point, the founding window protocol is active and minimum conditions for the next Radius must be under installation before additional triggers indicate the crossing has occurred.

CSS-Instrumented requires that trigger conditions be named in advance and that the founding window protocol name who is responsible for each minimum condition installation and what the installation timeline is.

### CSS-Loop-Closed

The coordination unit has crossed at least one threshold with minimum conditions installed in advance; it has executed a founding window protocol and validated that minimum conditions were effectively installed after the crossing. The founding window process has been tested against the lived experience of a threshold crossing and corrected from practice where the specification proved incomplete.

CSS-Loop-Closed requires evidence of at least one executed and validated threshold crossing.

### CSS-Auditable

An independent observer (someone with no prior relationship to the coordination unit) can assess the unit's effective Radius, identify all crossed thresholds, verify that minimum conditions for all crossed thresholds are structurally present, verify that maximum conditions for all crossed thresholds are absent, and produce a finding without requiring access to information the unit controls. All interface conditions for all crossed thresholds are documented and externally legible.

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

The Coordination Scaling Standard closes the scale-blindness exploitation vector: the structural break that occurs when a coordination system crosses a Dunbar-scale threshold without the structural conditions that threshold requires. It is precondition compressive: it specifies the structural substrate within which the other standards' conditions become possible at each scale. A coordination system operating below the minimum conditions for its current Radius cannot reliably meet the conditions of the other compressive standards, because the coordination functions those standards protect have already broken at the threshold.

---

*Sources: Robin Dunbar, "Neocortex size as a constraint on group size in primates," Journal of Human Evolution, 1992; Tamarit, Sánchez, and Cuesta, "Beyond Dunbar circles: a continuous description of social relationships and resource allocation," Scientific Reports, 2022; bucket/bucket-dunbar-layer-architecture-0_1_0.md v0.1.2 (primary source document for this standard's architectural content).*
