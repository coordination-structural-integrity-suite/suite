Structural Power Obligation Standard: A Framework for Assessing Centralization, Decentralization, and the Dimensions They Conflate

**Version:** v0.1.18

**Date:** 2026-04-11

**Author:** Regis Lloyd Chapman (Durgadas)

**Status:** Working draft. Foundational framework, three dimensions, invariants, change classification architecture, detection architecture, and tiered adoption are specified. Concentration threshold calibration and coopetition-specific detection signatures require pilot data. Cross-organizational power distribution: structural requirements for multi-level contexts established in Sections 3.1 and 4.4; detection architecture for spanning system boundaries remains an open design question (Section 11.3).

**Companion Standards:** This standard is designed for use alongside a precision-in-specification standard, an adverse signal engagement standard, a structural consent standard, and an information asymmetry classification standard. See Section 9 for the structural integrity architecture. Each companion standard is independently adoptable; joint adoption at the highest tier of each constitutes the Tensegrity Compressive Standards within the Coordination Structural Integrity Suite.

---

1\. Purpose

The word decentralization appears constantly in governance documents for organizations that feel thoroughly centralized to most of their participants. The opposite is also common: systems with visible coordination density are called centralized by critics who have not examined where formal authority actually sits. Neither word means much without a framework that specifies which dimensions of power are being measured.

Power in coordination systems accumulates across at least three independent dimensions: where formal authority sits, who has the practical capacity to coordinate and integrate decisions, and how interpretive work is distributed across the system. A system can distribute formal authority perfectly while concentrating interpretive capacity in a small group, and call itself decentralized without being dishonest about the formal structure. The participants who experience that concentration have no structural vocabulary to name it, and the system has no structural mechanism to detect or correct what it cannot see.

For how this standard relates to others in the Coordination Structural Integrity Suite, and guidance on which standards to combine for specific organizational purposes, see the Suite Integration Guide and the Suite Deployment Contexts document.

Non-harming is the first precision principle of the Coordination Structural Integrity Suite. The Precision-First Design Standard governs the suite as a whole: every standard in it is a precise specification of what non-harming requires in a specific coordination domain. The lack of a multi-dimensional framework for power distribution produces specific harms to specific people: power accumulates in the interpretive and coordination dimensions while the authority dimension appears distributed, and a system that cannot see this conflation cannot correct for it; governance that cannot verify its own distribution claims allows concentration to compound over time, hidden behind the language of decentralization; and the participants who bear the costs of that hidden concentration have no structural basis on which to name it. This standard specifies three-dimensional power distribution assessment as the precise structural answer: a framework that distinguishes the three independently variable dimensions of power accumulation so that concentration becomes structurally detectable rather than indefinitely arguable.

"Decentralization" is one of the most frequently invoked values in Web3 governance and one of the least precisely defined. "Centralization" is its counterpart: named as a failure mode, rarely specified as a structural phenomenon. The gap between the frequency of these terms and the precision with which they are used is not a communication problem. It is a structural condition that enables power to accumulate inside systems whose participants believe they have prevented it.

This standard establishes a framework for assessing power distribution that takes centralization and decentralization seriously enough to decompose them. Drawing on Lawrence and Lorsch's foundational research in organizational differentiation and integration, the standard treats "centralization" and "decentralization" not as poles of a single spectrum but as bundles of structurally independent dimensions that vary independently and require independent assessment. A system that distributes formal authority while concentrating interpretive capacity has not achieved decentralization in any meaningful sense. A system with high coordination density and distributed authority has not centralized even if it appears tightly organized.

The standard addresses a specific failure mode: structural power accumulating across one or more dimensions in ways that exceed authorized concentration levels, regardless of whether that accumulation is intentional. Structural power can accumulate through drift, through deliberate strategic action, through network effects, or through the gradual erosion of the conditions that made distribution possible at founding. The mechanism differs. The structural outcome is the same: governance that cannot verify its own distribution claims cannot correct for concentration it cannot see.

The standard is transferable. It is designed for adoption by any coordination system, governance protocol, or organization that needs to assess whether its power distribution is structurally present rather than merely claimed. Adoption tiers (Section 7) allow organizations to adopt the standard at the level appropriate to their operational context.

**Typological declaration** (Descriptive Typology Map v0.1.1)

*Operative classes*
- Relational-topological: This standard operates primarily in this class. Power distribution is a property of the structural topology of authority relationships: where decision-making formally resides (Locus of Authority), how coordination and integration are structured (Degree of Coordination and Integration), and how specialization and differentiation are distributed (Degree of Specialization and Differentiation). All three dimensions are relational-topological properties.
- Epistemic-perceptual: This standard operates in the precision and operationalization sub-aspect: decomposing "centralization" and "decentralization" into independently checkable structural conditions. It also addresses detection: specifying the observable criteria by which power concentration becomes visible to an independent observer.

*Boundary classes*
- Felt-experience: This standard assesses structural power distribution but does not address what it feels like to be a participant in a power-concentrated or power-distributed system. Whether distribution is experienced as equitable or empowering is outside this standard's vocabulary.
- Structural-mechanical: This standard does not address how power concentration modifies pre-stress distribution, creates load-bearing asymmetries in the tensegrity configuration, or affects the configuration's anisotropy profile.
- Temporal-dynamic (frequency-dynamic sub-aspect): This standard addresses structural conditions for power distribution but not how governance structures respond to the frequency or rhythm of concentration pressure over time.

---

2\. Foundational Framework: The Three Dimensions

This standard adopts Lawrence and Lorsch's differentiation-integration model as its foundational organizational framework, extended here to governance and coordination system contexts. The three-dimensional decomposition and its application to power distribution assessment are original to this standard.

**Citation:** Lawrence, Paul R., and Jay W. Lorsch. "Differentiation and Integration in Complex Organizations." *Administrative Science Quarterly* 12, no. 1 (1967): 1-47.

2.1 The Single-Slider Failure

Most organizational and governance discourse treats centralization and decentralization as a single spectrum: more centralized at one end, more decentralized at the other. This framing bundles three structurally independent dimensions into one, producing systematic design and diagnostic failures.

When discourse treats centralization as a single slider, it typically assumes: concentrated authority implies high coordination and low specialization; distributed authority implies low coordination and high specialization. This assumption makes entire design regions invisible. A federated governance structure with distributed formal authority, high coordination density, and deep domain specialization disappears from the possibility space. More importantly for this standard, it makes certain power accumulation patterns undetectable: a system can score as highly decentralized on the authority dimension while operating in a condition of extreme concentration on the interpretive or network dimensions.

Three misuse patterns recur with sufficient frequency to merit specific identification. The first is centralization-as-coordination: advocating for authority concentration primarily to solve a coordination problem, when the coordination goal would be achievable through integration mechanisms that do not require authority concentration. The second is decentralization-as-specialization: justifying distributed authority primarily through appeals to local expertise and context, when the actual design target is specialization rather than authority distribution. The third is axis conflation: treating the three dimensions as necessarily coupled, so that high coordination implies centralized authority or distributed authority implies low coordination.

Each misuse pattern is itself a detection signal within this standard: when governance discourse consistently conflates these dimensions, it is a structural indicator that power accumulation in the conflated dimensions is less visible to the organization's participants.

2.2 The Three Dimensions

Every governance system and coordination protocol can be characterized along three independent dimensions. Assessment requires examining each dimension independently before examining their interactions.

**Dimension A: Locus of Authority.** Where decision-making power formally resides. Who can make binding decisions for the system as a whole, for subsystems, and for individual participants. Authority distribution is the dimension most commonly assessed in decentralization claims, and it is the dimension the Nakamoto Coefficient (discussed in Section 3.1) measures. It is one of three.

**Dimension C: Degree of Coordination and Integration.** The strength and density of mechanisms that create alignment, consistency, and cross-unit synchronization. Coordination can be high in systems with distributed authority (federated governance) and low in systems with concentrated authority (fragmented hierarchies). Interpretive power, the capacity to define what the coordination mechanisms mean and how they are applied, is the primary power accumulation vector in this dimension.

**Dimension S: Degree of Specialization and Differentiation.** The extent to which units, participants, and subsystems face distinct environments, develop unique practices, and tailor approaches to local contexts. Specialization distribution is the power dimension most directly affected by network effects: as a coordination system scales, the structural capacity to participate meaningfully in specialized governance domains concentrates among participants with the accumulated interpretive bandwidth to navigate those domains.

2.3 Independence and Interaction

The three dimensions are independent by design. High coordination does not require centralized authority. Distributed authority does not require low coordination. Deep specialization does not require either. Systems can occupy any position in the three-dimensional space, and the design choice of where to position in each dimension is a governance decision that requires the consent of the affected constituency (as specified in the Structural Consent Legibility Standard).

The dimensions interact in ways that matter for power distribution monitoring. High coordination density combined with authority concentration produces the most durable form of power accumulation: the coordination infrastructure reinforces the authority structure, making alternatives structurally unavailable rather than merely unattractive. High specialization combined with interpretive concentration produces a second durable form: deep expertise concentrates in the participants who already have interpretive authority, creating a self-reinforcing loop that is difficult to interrupt without disrupting the specialization that produces system value. These interaction patterns are addressed in Section 6.

---

3\. Power Distribution Across Dimensions

Each dimension has a corresponding structural power concern, a primary detection instrument, and a set of observable signals. This section maps each dimension to its power concern and introduces the detection frameworks that operationalize it.

3.1 Authority Dimension: Formal Decision-Making Concentration

The authority dimension's structural power concern is the concentration of binding decision-making capacity in a small set of actors, whether through formal governance design, through gradual accumulation of role authority, or through the erosion of checks on unilateral action.

The Nakamoto Coefficient, proposed by Srinivasan and Lee, is the most widely used existing measure for authority dimension concentration. It defines the minimum number of entities required to compromise a given subsystem: a higher coefficient indicates greater resistance to collusion and capture. The coefficient is a valid and operationally useful detection instrument for one slice of the authority dimension: the minimum compromise number at a point in time.

The standard extends beyond the Nakamoto Coefficient in three ways. First, the coefficient measures a single threshold; this standard monitors trend direction over time. A coefficient of twelve that has declined from twenty over six epochs is a different structural condition than a coefficient of twelve that has been stable. Second, the coefficient addresses formal voting or validation capacity; it does not address the informal authority that accumulates through relational position, information access, or interpretive control, which are addressed in the coordination and specialization dimensions respectively. Third, the coefficient is calculated per subsystem; this standard requires cross-subsystem analysis to detect whether authority that appears distributed across subsystems is actually held by an overlapping actor cluster.

Ostrom's third design principle for governing commons provides the structural requirement for the authority dimension: those affected by governance rules must have meaningful participation in modifying them. This is the normative benchmark against which authority distribution is assessed. Authority concentration that excludes affected constituencies from rule modification is a structural failure regardless of the Nakamoto Coefficient's numerical value.

In nested and polycentric governance contexts, the authority dimension extends across levels of the governance structure. Subsidiarity is the normative benchmark for cross-level authority distribution: authority must be held at the lowest level capable of exercising it effectively and accountably. Concentration of authority at levels higher than subsidiarity requires is a structural failure of the same category as intra-level concentration, and triggers the Authorize invariant at each level where it occurs.

3.2 Coordination Dimension: Interpretive Capacity Concentration

The coordination dimension's structural power concern is the concentration of interpretive capacity: the ability to define what coordination mechanisms mean, how they apply, and what falls within or outside their scope. Control of the interpretive layer is structural power that does not require formal authority and does not register in authority-dimension measurements.

Interpretive capacity concentration is addressed by the Information Asymmetry Classification Standard's Class 3 (interpretive asymmetry), which specifies detection signals for this failure mode and should be consulted alongside this standard for full coverage of the coordination dimension. This standard addresses the power distribution question: whether interpretive capacity is distributed across the participant population or concentrated in a subset, and whether that concentration was authorized or represents drift.

Lukes' three dimensions of power provide the primary detection framework for the coordination dimension. Dimension one covers visible decision-making: who participates in coordination mechanism design, whether that participation is proportional to the affected constituency, and whether dissenting interpretations are documented or suppressed. Dimension two covers agenda-setting: what coordination problems are considered eligible for governance attention, who controls that eligibility determination, and what systematically fails to reach the coordination agenda. Dimension three covers preference-shaping: how the coordination framework's own language and structure causes participants to perceive certain arrangements as natural or inevitable rather than as design choices open to modification.

Third-dimension drift is the hardest to detect because it operates through the absence of challenge rather than through observable conflict. Legitimacy theory provides the operationalization instrument: the transition from normative legitimacy (participants engage because the coordination framework is right and requires ongoing justification) to cognitive legitimacy (participants engage because the coordination framework is simply how things are done, requiring no justification) is detectable by the absence of justification patterns in governance records. When an organization stops justifying foundational coordination choices and those choices go unquestioned, the transition has likely occurred. This is a temporal pattern requiring longitudinal governance record analysis rather than point-in-time assessment.

3.3 Specialization Dimension: Network Power and Participation Stratification

The specialization dimension's structural power concern is the concentration of meaningful participation capacity among participants with accumulated interpretive bandwidth, combined with the structural barriers that prevent new participants from developing equivalent capacity. This concern intensifies as systems scale, because scaling produces network effects that make the system more valuable to join while simultaneously raising the interpretive threshold required to participate in specialized governance domains.

Grewal's network power framework is the primary detection instrument for this dimension in protocol and network contexts. Grewal identifies two mechanisms through which network effects produce structural power: the attractiveness of joining a network (positive for participants) and the convergence dynamic through which alternatives become structurally unavailable even when formally permitted (negative for the system's overall power distribution). When a coordination system's adoption is sufficient to make alternatives structurally impractical, participation in that system's specialized governance domains concentrates among those who were present early enough to develop the required interpretive capacity. This is not a failure of intent; it is the structural equilibrium that network effects produce.

Hirschman's exit, voice, and loyalty framework provides the participation health measurement instrument. The ratio of exit availability to voice effectiveness is a continuous measure of whether participation in specialized governance domains is genuinely voluntary. When exit costs are high and voice mechanisms are insufficient, participation in governance becomes structurally compelled rather than chosen: the loyalty dynamic is operating through structural constraint rather than genuine commitment. This connects directly to the Structural Consent Legibility Standard's enduring shadow dynamic, which specifies the consent failure that occurs when participants remain beyond their limits because withdrawal is structurally prohibitive.

---

4\. Invariants

Across all implementations and domains, this standard requires three invariants. The invariants apply to each of the three dimensions independently; satisfying one does not satisfy the others.

4.1 Distribute

Power distribution across all three dimensions must be assessed and documented. Assessment of the authority dimension alone does not satisfy this invariant. The assessment must: identify the current distribution profile across all three dimensions, identify the authorized distribution profile as established through legitimate governance, and identify the gap between the two in each dimension.

The absence of an authorized distribution profile is itself a finding: systems that have not specified what power distribution they intend to maintain cannot detect unauthorized concentration. Establishing an authorized distribution profile is a prerequisite for the Distribute invariant. Note: Section 7.1 (SPDS-Assessed) specifies that at the lowest adoption tier, an absent authorized distribution profile may be satisfied by identifying it as an open governance task rather than requiring it to be complete; the finding is acknowledged and scheduled rather than resolved. This provision applies only at SPDS-Assessed; at SPDS-Operational and above, the profile must be established and accessible.

The authorized distribution profile presupposes a defined constituency: the set of participants whose standing within the governance system is subject to this standard's assessment. The constituency definition itself — who holds participation rights and on what basis — is a structural condition subject to power distribution analysis, not merely an administrative precondition. An undefined or implicitly defined constituency is itself a finding under this invariant, for the same reason an absent authorized distribution profile is: without a defined constituency, concentration cannot be assessed against a reference that does not exist.

Modification of the constituency definition by parties holding concentrated authority is an authority-dimension concentration event. Expanding or contracting membership, altering the basis on which participation rights are held, or reclassifying participants in ways that alter their governance standing each shift the distribution of authority-dimension power. Each such action triggers the Authorize invariant: the affected constituency must be identified before modification proceeds and must have a documented opportunity to authorize or refuse. This requirement holds regardless of whether the modification is deliberate or occurs through drift. Ostrom's first design principle (clearly defined boundaries for the governed constituency) identifies constituency definition as a precondition for sustainable commons governance; this section makes it an explicit precondition for this standard's assessment architecture.

4.2 Authorize

Concentration that exceeds authorized thresholds in any dimension requires legitimate authorization from the affected constituency before it is ratified as an intended structural condition rather than a deviation requiring correction. "Legitimate authorization" requires that: the affected constituency is identified before the ratification event, each identified member of the affected constituency has a documented opportunity to record their authorization or refusal before ratification occurs, and the authorization record is durable and accessible to the affected constituency.

Concentration that occurred through drift rather than deliberate action is not exempt from this invariant. The authorization requirement applies to the structural condition, not to the mechanism through which it arose. A system that detects unauthorized concentration and ratifies it without affected constituency consent has performed authorization theater rather than legitimate authorization.

4.3 Monitor

Ongoing detection architecture must instrument all three dimensions continuously. Monitoring establishes trend direction in addition to point-in-time concentration values. The detection architecture must be capable of producing a change classification (Section 5) for any detected concentration shift in any dimension. Monitoring results must be durable, tamper-evident, and accessible to the affected constituency as a condition of the monitoring function's legitimacy.

4.4 Multi-level extension

The Distribute, Authorize, and Monitor invariants apply at each level of any nested or polycentric governance structure in which the adopting system participates. A system embedded within a larger governance structure, or one containing nested subsystems, must assess and document power distribution at each level, not only within its own boundary.

At SPDS-Assessed and below, where cross-boundary detection architecture is not yet specified (see Section 11.3), this invariant is partially satisfied by documented disclosure: the system must identify the cross-boundary exposure, describe what is not yet monitorable, and treat that gap as a structural finding subject to periodic review at each tier review cycle. A current assessment of whether the detection gap has been addressed is required at each review. This provision applies only where the standard itself names an open design question (Section 11.3); it may not be invoked to self-declare compliance gaps for other coverage limitations.

At SPDS-Instrumented, partial compliance by disclosure is not sufficient. A system at this tier must either implement cross-boundary detection architecture or explicitly decline to adopt the multi-level extension. Declining adoption at SPDS-Instrumented is not a compliance gap; it is a scoped adoption decision that requires a structural exposure disclosure specifying what cross-level power distribution the system does not assess and what additional risk that creates.

---

5\. Change Classification Architecture

Every detected concentration shift in any dimension requires classification before any response is prescribed. The classification architecture distinguishes four categories of change. The classification determines the response obligation; it does not prescribe response content, which remains with the adopting system's governance.

5.1 The Four Classifications

**Drift.** Unintentional accumulation of concentration, typically invisible to the organization experiencing it, characterized by the absence of a coherent authorization event and the absence of an articulable connection to changed conditions. Drift does not require bad actors; it is the structural equilibrium that systems produce when extraction-resistance mechanisms are absent or have been eroded. Detection signature: concentration increasing over time without corresponding governance authorization, without articulable diagnosis, and without coherent guiding policy that explains the accumulation as an intended structural outcome.

**Coherent evolution.** Gradual strategy refinement that remains continuous with prior direction but develops it in response to changed conditions. Concentration that results from coherent evolution is distinguishable from drift by the presence of an articulable diagnosis explaining why current conditions require it and a guiding policy that makes the concentration instrumentally coherent with stated organizational purpose. Coherent evolution does not require a formal authorization event if the concentration remains within the authorized distribution profile established at the previous authorization point. Detection signature: concentration increasing within authorized thresholds with a documentable kernel (diagnosis, guiding policy, coherent actions) that explains the concentration as strategically coherent.

**Strategic pivot.** Intentional departure from prior distribution profile, authorized through legitimate governance, responsive to identifiable external conditions, with affected constituency involvement satisfying the Authorize invariant. A strategic pivot is distinguished from coherent evolution by the explicit departure from prior direction and from drift by the presence of legitimate authorization. Detection signature: concentration shift exceeding prior authorized thresholds accompanied by a documented governance authorization event with affected constituency participation.

**Capture.** Intentional concentration by a subset of actors at the expense of the affected constituency, disguised as drift, evolution, or strategic pivot. Capture is the hardest classification to establish because it requires distinguishing strategic intent from structural outcome. The detection approach is to apply Lukes' third dimension: preference-shaping that makes the concentration feel natural or inevitable is the structural fingerprint of capture rather than drift. Detection signature: concentration benefiting a consistent subset of actors across multiple governance cycles, combined with suppression of dissenting interpretations, legitimacy transition from normative to cognitive, and resistance to the transparency requirements of the Authorize invariant.

5.2 Classification Procedure

Classification proceeds in three steps. First, establish whether a coherent authorization event exists for the concentration shift. If yes, and if the event satisfied the Authorize invariant, the classification is strategic pivot. If yes, but the event did not satisfy the Authorize invariant, the classification is capture pending further analysis.

Second, if no authorization event exists, apply the Rumelt kernel test: can the organization articulate a current diagnosis of its conditions, a guiding policy that responds to that diagnosis, and a set of coherent actions that implement the guiding policy, where the concentration is explicable as an outcome of that coherent policy? If yes, and if the concentration remains within the authorized distribution profile, the classification is coherent evolution. If yes, but the concentration exceeds the authorized profile, the organization must initiate the Authorize invariant process before the evolution classification is confirmed.

Third, if neither an authorization event nor an articulable kernel exists, the classification is drift. If the kernel exists but consistently describes policies that benefit a concentrated subset at the expense of the broader constituency, the classification is capture.

5.3 Response Obligations by Classification

Drift triggers a mandatory response obligation: the adopting system must initiate a documented review process, produce a concentration report accessible to the affected constituency, and generate a governance outcome within a defined timeframe. The standard specifies the obligation and minimum process shape; response content remains with the adopting system's governance.

Capture triggers the same mandatory response obligation as drift, with the addition that the review process must include independent evaluation not conducted by the actors whose concentration constitutes the potential capture.

Coherent evolution within authorized thresholds triggers documentation requirements: the organization must maintain an accessible record of the kernel that explains the concentration as strategically coherent.

Strategic pivot triggers the Authorize invariant process if not already completed, plus documentation of the authorized distribution profile change.

---

6\. Detection Architecture

The tier names in this standard use the prefix SPDS (Structural Power Obligation Standard).

Systems adopting this standard at the SPDS-Instrumented tier must implement a detection architecture that instruments all three dimensions. Detection is probabilistic: the detection layer flags signals for review and classification, not adjudication. Each dimension has a composite signal model.

6.1 Authority Dimension Detection

Primary signal: Nakamoto Coefficient trend. The coefficient calculated per subsystem at defined intervals, with trend direction tracked over time. Declining trends trigger monitoring; sustained declining trends across multiple subsystems trigger classification review.

Secondary signal: authorization event frequency. The ratio of concentration shifts to documented authorization events. A high ratio indicates that authority is accumulating without corresponding governance authorization.

Tertiary signal: affected constituency participation in rule modification. The proportion of authority-affecting governance decisions in which the materially affected constituency participated at a level proportional to their stake. Systematic underrepresentation triggers classification review.

6.2 Coordination Dimension Detection

Primary signal: framework concentration. The pattern of who participates in coordination mechanism design and classification decisions, whether that participation is proportional to the affected constituency, and whether dissenting interpretations are documented or suppressed.

Secondary signal: agenda exclusion pattern. The pattern of coordination problems that consistently fail to reach governance attention, examined against the question of whose interests are served by the absence of those problems from the agenda. Requires longitudinal governance record analysis.

Tertiary signal: legitimacy transition indicator. The pattern of justification in governance records: the frequency with which foundational coordination choices are actively justified versus assumed as given. Declining justification frequency over time is a third-dimension drift signal.

6.3 Specialization Dimension Detection

Primary signal: participation stratification index. The distribution of meaningful participation in specialized governance domains across the participant population, measured as the proportion of participants who have demonstrably influenced specialized governance outcomes over a defined period. Concentration above a calibrated threshold triggers monitoring.

Secondary signal: exit and voice ratio. The structural availability of exit (switching cost transparency, alternative viability) relative to the effectiveness of voice mechanisms (whether objections to governance outcomes by non-concentrated actors produce documented deliberation and response). A deteriorating ratio triggers monitoring.

Tertiary signal: network convergence pressure. For protocol and network contexts: evidence that the system's adoption level has produced convergence dynamics making alternatives structurally unavailable, combined with barriers to new participant development of specialized governance capacity. Grewal's convergence dynamic is the detection target, not adoption growth itself.

6.4 Composite Classification Trigger

Individual signals trigger monitoring. Persistent patterns combining primary, secondary, and tertiary signals across multiple governance cycles trigger classification review under Section 5. The classification architecture requires composite signal evidence; no single signal is treated as conclusive.

The detection architecture must be transparent to participants. Organizations operating at the SPDS-Instrumented tier must document what patterns are being monitored, because the monitoring scope is itself a governance decision subject to the Authorize invariant in the coordination dimension. An undisclosed detection surface is a structural consent failure.

---

7\. Tiered Adoption

7.1 SPDS-Assessed

The system acknowledges that power distribution is structurally relevant to its operations across all three dimensions. An initial distribution assessment is conducted covering all three dimensions. The authorized distribution profile is documented or identified as an open governance task.

Minimum requirement: a power distribution inventory that maps the system's current concentration profile across the three dimensions, identifies where distribution has been specified and where it is assumed, and names the three misuse patterns from Section 2.1 as known structural risks.

7.2 SPDS-Operational

The system has defined processes for assessing distribution across all three dimensions and for applying the change classification architecture to detected concentration shifts. The Rumelt kernel test is applied periodically as a coherence check.

Minimum requirement: for each dimension, a documented assessment process satisfying the Distribute and Authorize invariants, with the change classification architecture applied to detected shifts. The authorized distribution profile is established and accessible to the affected constituency.

7.3 SPDS-Instrumented

The system treats unauthorized concentration as a governance-level violation subject to detection and mandatory response. The Monitor invariant is fully satisfied: detection architecture instruments all three dimensions continuously, produces change classifications for detected shifts, and generates durable tamper-evident records. The detection architecture is disclosed to participants.

Minimum requirement: detection architecture per Section 6 covering all three dimensions, the composite classification trigger mechanism, and the mandatory response obligations per Section 5.3.

7.4 SPDS-Accountable

Includes all SPDS-Instrumented requirements plus closed governance loop architecture.

The defining property of SPDS-Accountable is that governance inaction in the presence of a detected concentration event is structurally visible without depending on any actor's cooperation. At SPDS-Instrumented, the detection architecture produces concentration classification outputs. At SPDS-Accountable, those outputs produce mandatory governance responses, and the absence of a response is itself a detected event.

Minimum requirements:

Every concentration detection output above an authorized threshold (per the composite classification trigger in Section 6.4) must produce a documented governance review within a defined window. A window is valid under SPDS-Accountable if it satisfies three conditions: it is specified before any adoption claim is made; it is publicly documented so that any governance actor can verify whether the system is meeting its own stated commitment; and it is short enough that governance inaction within it is detectable before the next governance cycle in which the underlying concentration could compound. The adopting system must define its governance cycle length in the same public documentation that specifies the window, as the two specifications are co-dependent. The review record must include: the concentration event identifier, the dimension or dimensions implicated (authority, coordination, specialization), the change classification assigned (drift, coherent evolution, strategic pivot, or capture per Section 5), the review outcome (including outcomes of authorized acceptance, remediation plan, or deferral with timeline), the actor or body responsible for the review, and the rationale. A decision to authorize or accept a detected concentration shift is a decision and must be documented with rationale. A decision to take no action is a decision and must be documented as such. The absence of any documented review is not a permissible outcome at SPDS-Accountable.

The absence of a documented review within the defined window must produce automatic disclosure to all governance actors without requiring any actor's initiation. This disclosure makes the concentration event, its classification, the elapsed time since detection, and the absence of a governance review simultaneously visible. A system in which this disclosure requires a human decision to publish has not closed the governance loop and does not meet SPDS-Accountable.

The governance review record is append-only. Reviews cannot be modified after recording; corrections are recorded as new entries referencing the original. This property is what makes governance inaction detectable without cooperation: an independent observer can verify that a concentration detection output exists in the record, verify that no review entry exists within the required window, and determine that automatic disclosure was or was not produced as a consequence.

Tier review cadence for SPDS-Accountable systems: tier review MUST occur at minimum annually and MUST include a governance loop integrity check: confirmation that the detection-to-review path operated as specified for all concentration detection outputs in the review period, and that automatic disclosures were produced where required. The annual review must also include a distribution profile reconfirmation: the authorized distribution profile across all three dimensions is reviewed and reconfirmed or updated.

7.5 SPDS-Auditable

Includes all SPDS-Accountable requirements plus independent auditability.

The defining property of SPDS-Auditable is that the full detection and response architecture can be verified by a party outside the system without depending on system operator cooperation or self-certification.

Minimum requirements:

The complete concentration event record, from detection output through documented governance review or automatic disclosure, must be accessible to an independent auditor. Access is not contingent on operator consent during a defined audit period. The record format is sufficient for an auditor to verify completeness without access to the detection layer itself.

The auditor must be able to verify completeness: that all concentration detection outputs generated in the audit period are present in the record. This requires that the detection architecture produces a verifiable count or hash of outputs generated, against which the record can be checked. A record that can only be verified for presence (each concentration event in the record was detected) but not for completeness (all detected events are in the record) does not meet SPDS-Auditable.

The auditor must be able to verify dimension integrity: that each recorded concentration event was classified against the three-dimension framework and the change classification architecture in this standard, and that the authorized distribution profile in effect at the time of detection was applied.

The auditor must be able to verify response completeness: that every concentration detection output above an authorized threshold produced either a documented governance review within the specified window or an automatic disclosure. Gaps in this chain are reportable findings.

The audit itself must be documented: scope, period, auditor identity or body, findings, and system response to findings. Audit reports are retained in the governance record under the same append-only constraints as governance reviews.

SPDS-Auditable systems must make audit reports available to their participant population within a defined period after audit completion. The disclosure period is specified by the system and subject to the same precision requirements as all other SPDS obligations.

---

8\. Relationship to Other Standards

8.1 Precision in Specification

Power distribution claims must be precise. "We are a decentralized protocol" fails the precision test unless the claim specifies which dimension is being described, at what level of distribution, and how that claim is verified. The legibility obligation from a precision-in-specification standard applies to distribution claims the same way it applies to governance proposals: vague claims are not claims.

8.2 Adverse Signal Processing

Unauthorized concentration is an adverse signal. Any adverse signal processing system paired with this standard should treat concentration shifts that fail the classification procedure as adverse signals requiring notice, classification, and a navigation path. The implausible absence of concentration monitoring results in a system that has operated continuously is itself an adverse signal: absence of detection is not evidence of absence of concentration.

8.3 Structural Consent Legibility Standard

The Authorize invariant requires affected constituency consent for concentration above authorized thresholds. The Structural Consent Legibility Standard (SCLS) specifies what structural consent means and how it is verified. The two standards are deeply interdependent: power distribution without consent verification is a structural condition that enables extraction, and consent without power distribution assessment produces consent mechanisms that may be formally satisfied while operating in the enduring shadow dynamic. Systems adopting both standards at their Instrumented tiers satisfy the Authorize invariant and the SCLS Authorize invariant through a unified consent process applicable to both.

The connection is also specific to the specialization dimension: the enduring shadow dynamic in the Structural Consent Legibility Standard (participants remaining beyond their limits because exit costs are structurally prohibitive) is the consent-dimension expression of the exit and voice ratio deterioration that this standard detects in the specialization dimension. The same structural condition produces both signals; the two standards read it from different angles.

8.4 Information Asymmetry Classification Standard

The Information Asymmetry Classification Standard (IACS) addresses power that derives from information advantage. This standard addresses structural power that operates independently of information: resource concentration, authority distribution, network convergence, and legitimacy drift. The two standards are complementary and non-overlapping in scope.

The interaction between them is significant for the coordination dimension specifically: interpretive asymmetry (IACS Class 3) is the information-dimension expression of what this standard's coordination dimension measures as interpretive capacity concentration. A system applying both standards in the coordination domain will detect the same underlying structural condition from two different angles, which strengthens classification confidence. The standards should be applied jointly in the coordination dimension at the Instrumented tier.

---

9\. Structural Integrity Architecture

10\. Inheritance Clause

Systems adopting this standard should include the following statement in their governance documentation:

*Structural Power Distribution Inheritance: This [document/system/protocol] adopts the Structural Power Obligation Standard (SPDS) (v[X], [date]) at the [SPDS-Assessed / SPDS-Operational / SPDS-Instrumented / SPDS-Accountable / SPDS-Auditable] level. The authorized distribution profile across the three dimensions (Authority, Coordination, Specialization) is specified at: [reference to distribution profile document or governance record]. The concentration thresholds triggering Authorize invariant review are: [thresholds per dimension]. Dimensions identified as not applicable to this system's operations: [list, with rationale].*

The inheritance clause commits the adopting system to: (a) establishing an authorized distribution profile across all three dimensions, (b) satisfying the three invariants (Distribute, Authorize, Monitor) at the adopted tier, (c) treating unauthorized concentration as an adverse signal subject to its adverse signal processing, (d) applying the change classification architecture to detected concentration shifts, and (e) disclosing the detection architecture to its participant population as a condition of operating at the SPDS-Instrumented tier.

Adoption of this standard at any tier below the full Tensegrity Compressive Standards threshold (Tier 4 across all six Tensegrity Compressive Standards) does not constitute full Tensegrity Compressive Standards conformance and does not reduce structural exposure from uncovered standards. Systems in partial adoption are required to produce a structural exposure disclosure in place of a conformance claim, per the specification in the Proof of Coordination Architecture document.

---

10.1 Precision-First Inheritance

*Precision-First Inheritance: This document adopts the Precision-First Design Standard at the PFDS-Instrumented tier. Every element of this document is subject to that standard at the declared tier. Any revision that reduces definitional precision, replaces typed constructs with vague terms, collapses previously distinguishable states, or makes a falsifiable claim unfalsifiable is a design error requiring correction, not a legitimate exercise of governance or editorial discretion.*

---

11\. Open Design Questions

The following questions are structurally required by this standard but not yet fully resolved.

**11.1 Concentration threshold calibration.** The specific thresholds triggering Authorize invariant review in each dimension require empirical calibration against pilot data. The Nakamoto Coefficient thresholds for the authority dimension are partially addressed in existing Web3 governance research but require translation to the trend-direction monitoring architecture this standard specifies. Coordination and specialization dimension thresholds are not established in existing literature and require empirical calibration through pilot data by any system adopting this standard.

**11.2 Coopetition-specific detection signatures.** This standard's detection architecture was designed for cooperative governance contexts. In coopetition contexts, where the same actor is simultaneously a rival for governance influence and a collaborator on shared infrastructure, the concentration signals read differently: a Nakamoto Coefficient decline may represent competitive dynamics rather than capture, and authority concentration may be a coordination response to competitive pressure rather than extraction. Coopetition-specific detection signatures that distinguish these cases are an open design question requiring domain-specific pilot data.

**11.3 Cross-organizational power distribution.** In multi-protocol and Decentralized Autonomous Organization (DAO)-to-DAO contexts, power distribution cannot be assessed within a single system boundary. An actor cluster with distributed authority within each individual system may hold concentrated authority across the combined system through overlapping participation. The structural requirement for cross-level assessment is established in Section 3.1 (subsidiarity as the normative benchmark for cross-level authority distribution) and Section 4.4 (Multi-level extension, applying the three invariants at each level of nested governance structures). The detection architecture for spanning system boundaries remains an open design question: the measurement instruments and monitoring protocols for cross-boundary detection require domain-specific specification before full operationalization.

**11.4 Sensemaking standard independence criterion.** Section 9.2 establishes that the sensemaking standard requires independent observables for sensemaking capacity that are distinct from Tensegrity Compressive Standards conformance. Specifying those observables is an open design question for the sensemaking standard that must be resolved before the Tensegrity Compressive Standards-plus-sensemaking architecture can be fully operationalized.

**11.5 Constraint-type determination is outside this standard's scope.** This standard operates within an existing constraint structure. It assesses whether power distribution is structurally present, detects unauthorized concentration, and specifies response obligations when concentration is detected. It does not address who controls the upstream determination of what type of constraints apply to a given practice area or governance decision: whether a domain is governed by enabling constraints (probing, emergent practice) or governing constraints (standardized, best practice), and whether that classification is made by legitimate governance or by interest, ideology, or structural position.

Constraint-type determination is a consequential power: the choice of constraint type governs what counts as a valid response and what counts as deviation. A system where constraint-type determination is ungoverned has a structural power concentration point that this standard's three-dimension framework does not reach, because the determination operates upstream of the governance activity the standard monitors.

This is a named scope boundary, not a design oversight. The reason a new standard is not the straightforward answer is the recursive closure problem: any standard specifying who governs constraint-type determination requires a prior determination of what type of constraints govern that meta-governance function, producing infinite regress. The appropriate response to this recursion is tensegrity rather than specification: continuous monitoring of constraint-type determination by a detection layer capable of identifying when enabling-constraint domains are being treated as governing-constraint domains (and vice versa), producing signals that call for governance response rather than automated enforcement. A detection layer's tensional state monitoring function is the candidate architecture for this signal.

---

Relationship To Other Standards

The closest functional adjacency is with the Adverse Signal Engagement Principle Core Standard: power concentration is a structural condition that suppresses adverse signals, and the two standards together address both the suppression mechanism and the engagement requirement. The Information Asymmetry Classification Standard addresses adjacent territory: power differentials generate positional and relational asymmetry as classified in its primary taxonomy.

Tensegrity As A Whole

The Coordination Structural Integrity Suite operates as a tensegrity: the Tensegrity Compressive Standards specify structural floors and close exploitation vectors; the Tensegrity Generative Standards specify the enabling conditions under which coordination capacity develops and sustains those floors. This standard is compressive.

```
Coordination Structural Integrity Suite
│
├── Tensegrity Compressive Standards (5)
│   ├── Precision-First Design Standard
│   ├── Adverse Signal Engagement Principle Core Standard
│   ├── Structural Consent Legibility Standard
│   ├── Information Asymmetry Classification Standard
│   └── Structural Power Obligation Standard               ← this standard
│
└── Tensegrity Generative Standards (3)
    ├── Sensemaking Standard
    ├── Four Batteries Capacity Standard
    └── Conflict Transformation Standard
```

Without this standard, advantage can accumulate across the three dimensions (authority, coordination, specialization) in ways that governance documents do not reflect and participants cannot contest. The other five compressive standards address their respective failure modes, but none addresses the structural mechanism by which advantage accumulates across multiple organizational dimensions simultaneously.

Each standard in the Coordination Structural Integrity Suite is independently adoptable and independently valid. Adopted together, the nine standards address a reinforcing set of structural failure modes that no single standard covers alone. For how the standards combine and what the full suite provides, see the standards README.

---

Changelog

**v0.1.17 (April 2026):** Plain-language preamble added. Two paragraphs inserted before the non-harming formula in Section 1 (Purpose), grounding the standard in the lived experience of the coordination failure it addresses (decentralization claimed without structural evidence of its presence). Navigation pointer added: one sentence pointing to the Suite Integration Guide and the Suite Deployment Contexts document. No changes to normative content.

**v0.1.16 (April 2026):** Non-harming opening formula added to Section 1 (Purpose). New paragraph at the start of Section 1 specifies the specific harms that absence of a multi-dimensional power distribution framework produces and names three-dimensional assessment as the precise structural answer. No changes to normative content.

**v0.1.15 (March 2026):** Cross-reference added to Section 4.1 (Distribute). The "absence of an authorized distribution profile is a finding" language now includes a pointer to Section 7.1 (SPDS-Assessed), which allows the finding to be satisfied by identifying the profile as an open governance task at the lowest adoption tier. Without this cross-reference, an auditor reading Section 4.1 before reaching Section 7 could apply the absence-as-finding language as an absolute, generating a false positive on early-stage organizations at SPDS-Assessed that have correctly documented the gap as an open task. No normative change; clarification only.

**v0.1.14 (March 2026):** Ostrom DP1 scope extension. Two paragraphs added to Section 4.1 (Distribute). First: the authorized distribution profile presupposes a defined constituency; an undefined or implicitly defined constituency is a finding of the same class as an absent authorized profile. Second: modification of the constituency definition by parties holding concentrated authority is an authority-dimension concentration event triggering the Authorize invariant, regardless of whether the modification is deliberate or occurs through drift. Source: Ostrom gap analysis, March 2026.

**v0.1.13 (March 2026):** Ostrom DP8 scope extension. Added cross-level authority distribution paragraph to Section 3.1, specifying subsidiarity as the normative benchmark for multi-level contexts: authority must be held at the lowest level capable of exercising it effectively and accountably, and concentration at higher levels triggers the Authorize invariant. Added Section 4.4 (Multi-level extension), extending the Distribute, Authorize, and Monitor invariants to nested and polycentric governance contexts. At SPDS-Assessed and below, cross-boundary exposure may be partially satisfied by documented disclosure under a standard-named provision, subject to periodic review; at SPDS-Instrumented, full implementation or explicit scoped non-adoption with structural exposure disclosure is required. Updated Section 11.3 from a fully open design question to a partially resolved entry: structural requirements are established; detection architecture for spanning system boundaries remains open. Updated Status field accordingly. Source: Ostrom gap analysis, March 2026.

**v0.1.12 (March 2026):** Suite rename ("Coordination Structural Integrity Suite" replaces "Structural Integrity Layer" throughout). Added "Relationship To Other Standards" and "Tensegrity As A Whole" sections, replacing Section 12.

**v0.1.11 (March 2026):** Precision-First compliance fix. Invariant 4.2: removed cross-reference to the Structural Consent Legibility Standard. "Legitimate authorization" is now defined self-containedly within this standard. Replaced "meaningful opportunity to authorize or refuse" (not independently verifiable) with a temporal/structural observable: affected constituency identified before ratification, each member has a documented opportunity to record authorization or refusal before ratification occurs, authorization record is durable and accessible. Standards independence preserved: this standard can now be adopted without reference to any other standard for compliance with the Authorize invariant.

**v0.1.10 (March 2026):** Change 3 of anisotropy sequence. Typological declaration (Variant B) added to Section 1 (Purpose). Operative classes: relational-topological (primary, three-dimensional power topology), epistemic-perceptual (precision/operationalization, detection sub-aspects). Boundary classes: felt-experience, structural-mechanical, temporal-dynamic (frequency-dynamic sub-aspect). Map version v0.1.1 cited.

**v0.1.9 (March 2026):** Terminology update. "Commitment Standards" renamed to "Tensegrity Compressive Standards" throughout. No normative content changes.

**v0.1.8 (March 2026):** Generalization pass completing work left unfinished in v0.1.5. Five fixes, no normative content changes. (1) Header companion standards: "constitutes the pentad" replaced with "constitutes the Tensegrity Compressive Standards within the Coordination Structural Integrity Suite." Missed in v0.1.5 naming propagation. (2) Section 11.4: "distinct from pentad compliance" replaced with "distinct from Tensegrity Compressive Standards conformance"; "pentad-plus-sensemaking architecture" replaced with "Tensegrity Compressive Standards-plus-sensemaking architecture." Two additional naming misses from v0.1.5. (3) Section 9.1: removed "(forthcoming)" from Proof of Coordination Architecture reference. v0.1.5 removed this from Section 10 but missed Section 9.1. (4) Section 10.1: Precision-First inheritance clause version citation updated from v1.5.4 to v1.5.6. (5) Section 11.5: "the Witness Layer's tensional state monitoring function" replaced with "a detection layer's tensional state monitoring function." The Witness Layer is a protocol-specific implementation; the domain-general standard names the function, not the implementation. Consistent with the generalization passes applied to the Adverse-Signal Engagement Principle and other Tensegrity Compressive Standards.

**v0.1.18 (2026-04-11):** Renamed from Structural Power Distribution Standard to Structural Power Obligation Standard. No changes to normative content. "Obligation" replaces "Distribution" throughout to name the structural requirement from inside the standard's own logic: power is legitimate only when matched by obligation toward all cost-bearing parties across all three dimensions (authority, coordination, specialization). "Distribution" names a condition to be measured; "Obligation" names the mechanism that makes any distribution profile legitimate. Directly invokes the Multiplex Obligation Directions architecture in the foundational frameworks. See Naming Decision 2.19 in reference-terminology-conventions-0_1_2.md.

**v0.1.7 (March 2026):** Pre-release fixes. (1) Section 7.4 SPDS-Accountable: governance review record requirement corrected from "(drift, accumulation, or capture per Section 5)" to "(drift, coherent evolution, strategic pivot, or capture per Section 5)." "Accumulation" is not a defined term in Section 5; the four defined classifications are drift, coherent evolution, strategic pivot, and capture. Normative fix: the record requirement now references the standard's actual classification vocabulary. (2) Section 10.1 Precision-First inheritance clause: version citation updated from v1.4.8 to v1.5.4. No other changes to normative content.

**v0.1.6 (March 2026):** Added Section 11.5 (Constraint-type determination is outside this standard's scope). Names the upstream power concentration point this standard does not reach: who controls whether a domain is governed by enabling or governing constraints. States the recursive closure problem as the reason a new standard is not the answer. Identifies tensegrity and Witness Layer tensional state monitoring as the candidate architecture for this signal. No changes to normative content.

**v0.1.5 (March 2026):** Coordination Structural Integrity Suite naming propagation. Updated Section 9.1 heading from "The Pentad" to "The Tensegrity Compressive Standards within the Coordination Structural Integrity Suite." Updated Section 9.1 body: replaced structural integrity pentad designation language with full Tensegrity Compressive Standards designation language throughout; "fifth of five mutually reinforcing standards" replaced with "fifth of the five Tensegrity Compressive Standards within the Coordination Structural Integrity Suite." Updated Section 9.2 sensemaking layer paragraph to reference Tensegrity Compressive Standards rather than pentad throughout. Updated theater prevention clause in Section 10 and removed "(forthcoming)" from Architecture document reference. No changes to normative content.

**v0.1.4 (March 2026):** Pre-publication check pass. Five fixes. (1) Section 7.4 SPDS-Accountable: "defined window" given three validity conditions (specified before adoption, publicly documented, short enough that inaction is detectable before the next governance cycle in which the underlying concentration could compound); governance cycle length required as a co-specified public document alongside the window. (2) Section 9.1 and Section 10: Added "(forthcoming)" notation to both Proof of Coordination Architecture references for consistency with other standards in the stack. (3) Section 11.1: "genesis cohort deliberation" replaced with "empirical calibration through pilot data by any system adopting this standard." (4) Section 10.1 added: Precision-First inheritance clause at PFDS-Instrumented tier. (5) Changelog formatting fix: unclosed bold marker in v0.1.2 entry corrected.

**v0.1.3 (March 2026):** Tier 4 and Tier 5 normative content. Replaced Sections 7.4 (SPDS-Accountable) and 7.5 (SPDS-Auditable) placeholders with full normative specifications. SPDS-Accountable requires: every concentration detection output above an authorized threshold (per Section 6.4 composite classification trigger) produces a documented governance review within a defined window (record includes event identifier, implicated dimensions, change classification, outcome, responsible actor, and rationale); automatic disclosure to all governance actors when no review is documented within the window, without requiring any actor's initiation; append-only governance review record; annual tier review including governance loop integrity check and distribution profile reconfirmation across all three dimensions. SPDS-Auditable requires all SPDS-Accountable requirements plus: complete concentration event record accessible to an independent auditor without operator cooperation; verifiable completeness (detection architecture produces a count or hash of outputs against which the record can be checked); verifiable dimension integrity (three-dimension framework and change classification architecture applied consistently, authorized distribution profile at time of detection applied); verifiable response completeness (every detection output above authorized threshold produced a review or automatic disclosure); documented audit reports retained in governance record under append-only constraints; audit reports made available to participant population within a defined period.

**v0.1.2 (March 2026):** Conformance theater prevention pass. Added disclosure specification paragraph to the Relationship to the Structural Integrity Pentad section specifying four required elements for a substantive structural exposure disclosure. Added theater prevention clause to inheritance clause specifying that partial adoption does not constitute pentad conformance and requires a structural exposure disclosure per the Proof of Coordination Architecture document. No changes to normative content.

v0.1.1 (March 2026):** Tier rename propagation. Renamed three adoption tiers from aware/structured/critical to Assessed/Operational/Instrumented throughout (Section 7.1 through 7.3, Section 8.3, Section 8.4, and inheritance clause). Added Tier 4 (Accountable) and Tier 5 (Auditable) placeholder sections (7.4 and 7.5) with normative content to be specified in a future session. Updated Section 9.1 pentad conformance threshold from "highest respective tiers" to Tier 4 (Accountable) and added structural exposure disclosure requirement for partial adopters. Updated inheritance clause to list all five tier options. No changes to normative content of Sections 1 through 6 or Sections 8 through 10.

**v0.1.0 (March 2026):** Initial specification. Established: foundational framework (Lawrence and Lorsch's three dimensions with governance application), three invariants (Distribute, Authorize, Monitor), change classification architecture (drift, coherent evolution, strategic pivot, capture) with Rumelt kernel as coherence test instrument, detection architecture across all three dimensions with Nakamoto Coefficient as authority dimension partial measure, Lukes' three dimensions and legitimacy theory for coordination dimension, Hirschman's exit and voice ratio and Grewal's network power for specialization dimension, tiered adoption, relationship to companion standards, structural integrity pentad designation, sensemaking layer relationship, and inheritance clause. Single-slider failure and three misuse patterns from coordination specialization coding work included as conceptual foundation. Ostrom's collective choice principle as authority dimension structural requirement. Open design questions on threshold calibration, coopetition detection signatures, cross-organizational assessment, and sensemaking independence criterion.
