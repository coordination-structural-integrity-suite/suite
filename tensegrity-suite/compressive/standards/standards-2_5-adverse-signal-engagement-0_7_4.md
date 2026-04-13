**Adverse‑Signal Engagement Principle**

**(ASEP)**

*Core Standard v0.7.3*

**Regis Chapman (Durgadas)**

Version 0.7.4 \| April 2026

# 1. Preamble

Every serious governance failure comes with the same post-mortem. The warning signs were present. Someone raised a concern, flagged an anomaly, filed a report, or named a pattern. The system registered that signal as background noise, a complaint to be managed, something to document and revisit later. By the time the failure became undeniable, the moment for structural correction had passed.

This is not a story about bad actors ignoring warnings they understood. It is a story about structural conditions that treated adverse signals as nuisances rather than primary governance inputs. No structural obligation to engage with the signal existed, so the signal was not engaged with. The harm is not only the failure that eventually arrived. The harm includes everyone who raised a concern, was not structurally heard, and continued carrying the cost of that signal alone.

For how this standard relates to others in the Coordination Structural Integrity Suite, and guidance on which standards to combine for specific organizational purposes, see the Suite Integration Guide and the Suite Deployment Contexts document.

Non-harming is the first precision principle of the Coordination Structural Integrity Suite. The Precision-First Design Standard governs the suite as a whole: every standard in it is a precise specification of what non-harming requires in a specific coordination domain. The lack of a structural obligation to engage adverse signals produces specific harms to specific people: warning signs are present, visible to those positioned to see them, and not acted on because no structural obligation to act exists; those bearing the cost of the ignored signal absorb it invisibly while governance proceeds as though nothing has been surfaced; and by the time the harm becomes undeniable, the mechanisms that produced it are entrenched and the moment for structural correction has passed. This standard specifies adverse signal engagement as the precise structural answer: a binding obligation to treat adverse signals as primary governance inputs, not as nuisances to be minimized.

When a coordination system fails, the post-mortem almost always reveals the same thing: the warning signs were present, they were visible, and they were not treated as requiring a response. Ignored complaints, dismissed anomalies, buried reports, shifting evidence. The pattern recurs across financial systems, healthcare, infrastructure, online platforms, and decentralized protocols. The failure is not that the signals were undetectable. The failure is that no structural obligation existed to engage with them.

The Adverse-Signal Engagement Principle (ASEP) is a cross-domain standard that specifies how systems with shared governance surfaces must treat adverse signals. It establishes a structural obligation: adverse signals must be treated as primary inputs to governance and security, not as nuisances to be minimized. The standard is rigorous (clear invariants and obligations), standardized (a common structure across domains), extensible (profiles for Web3, AI, regulators, media, and other contexts), and flexible (tiered adoption for different risk levels).\[5\]\[6\]\[7\]\[8\]\[1\]

ASEP is a standard, not a taxonomy. Taxonomies of harms, incidents, or
asymmetries plug into ASEP's "Name" phase; they are implementation
choices, not part of the standard itself.\[1\]

# 2. Core Principle

## 2.1 Definition

ASEP applies to systems that:

-   Make shared decisions that affect constituencies beyond a small,
    clearly bounded group (e.g., users, customers, citizens, depositors,
    communities), and

-   Do so through shared mechanisms (protocol rules, laws, policies,
    governance processes), rather than pure personal discretion.\[1\]

**Adverse‑Signal Engagement Principle (ASEP).** In such systems, adverse
signals must be treated as primary inputs to governance and security,
not as nuisances to be minimized.\[5\]\[1\]

An adverse signal is any observation, anomaly, pattern, or misuse
behavior that, if true and left unaddressed, would materially increase
risk to:

-   the system's constituencies (e.g., physical, financial,
    reputational, psychological, or rights‑related harm), or

-   the integrity of the system's shared records, rules, or enforcement
    (e.g., manipulation, capture, systemic bias).\[6\]\[9\]\[1\]

ASEP is risk‑weighted: higher‑impact signals demand stronger and faster
engagement, but no qualifying signal may be silently ignored.

**Tier choice and classification within scope.** The way a system
chooses and revises its ASEP adoption tier, and how it classifies the
severity of adverse signals, are themselves subject to ASEP. They MUST
be logged, deliberate, and open to challenge.

**Typological declaration** (Descriptive Typology Map v0.1.1)

*Operative classes*
- Epistemic-perceptual: This standard operates in the detection and signal processing sub-aspect: defining adverse signals, specifying what a detection instrument must distinguish, and establishing the false-negative boundary explicitly. It also operates in the precision and operationalization sub-aspect: signal categories, escalation tiers, and response obligations are operationally defined.
- Relational-topological: This standard addresses the structural architecture of escalation pathways and response obligations: which roles must act on detection outputs, how governance inaction becomes visible to an independent observer without requiring the inacting party to self-report, and the defense-in-depth requirements for the response layer.

*Boundary classes*
- Felt-experience: This standard specifies structural signal detection and response obligations but does not address what it feels like to be a signal source in a monitored governance system, or the affective dimensions of being subject to adverse signal processing.
- Action-structural: This standard classifies signal categories and escalation stages but does not address the action-coordinate content of what signal sources or responders are doing within an adverse signal pathway.
- Temporal-dynamic (frequency-dynamic sub-aspect): Escalation timelines are specified sequentially. This standard does not address how governance structures respond to the frequency or rhythm of adverse signal pressure over time.

## 2.2 Invariants

Across all implementations and domains, ASEP requires that:

**No silent erasure.** Bona fide adverse signals cannot be silently
suppressed, deleted, or ignored. If a signal is judged non‑adverse, that
judgment itself must be recorded.\[5\]

**Ex‑ante criteria.** Criteria for what counts as an adverse signal
(taxonomies, thresholds) are defined before specific disputes; they are
versioned and cannot be retroactively changed for open cases.\[1\]

**Finite path to decision.** Every adverse signal must have at least
minimal engagement (log, classify, acknowledge) and a finite path toward
a decision: act, monitor, or formally close, with rationale.\[5\]\[1\]

These invariants define ASEP; everything else is implementation detail.

## 2.3 Detection Reliability Dependency

This standard has a structural reliability dependency on the Relational Battery condition specified in the Four Batteries Capacity Standard. The detection architecture depends on participants surfacing adverse signals through the channels and processes this standard requires. When the Relational Battery is depleted, participants will not surface adverse signals even when explicitly invited to do so, because the relational context makes surfacing feel unsafe or pointless. This produces a systematic false negative: the detection surface shows no signals, governance concludes the standard is being met, and signals continue to accumulate invisibly.

An audit of this standard conducted in an organization with a depleted Relational Battery cannot be considered reliable. The absence of recorded adverse signals in that context is not evidence of structural health; it is evidence that the surfacing mechanism has failed. Joint adoption of this standard and the Four Batteries Capacity Standard, with Relational Battery instrumented at a sufficient tier, is required for this standard's audit results to be trustworthy.

This dependency does not mean this standard is non-operational without Four Batteries. It means that the confidence warranted by an audit result is bounded by the Relational Battery condition. An organization may adopt this standard at any tier while its Relational Battery is unassessed; it must disclose that audit results carry this reliability limitation until joint adoption is in place.

# 3. Obligations: Notice, Name, Navigate

## 3.1 Notice -- Detecting Adverse Signals

ASEP requires systems to be able to see adverse signals.

### 3.1.1 Channels and sources

Systems must provide at least one channel, and ideally several, through
which adverse signals can be surfaced by humans and machines, including:

-   internal participants (staff, contributors, members),

-   external constituencies (users, customers, communities),

-   technical monitoring (logs, anomaly detectors, audits, model evals),
    and

-   independent observers (researchers, watchdogs,
    regulators).\[2\]\[10\]\[11\]\[6\]

Emotionally expressed, messy, or "unskilled" complaints, especially from
less‑powerful constituencies, are treated as legitimate sources of
potential adverse signals, not as disqualifying noise.\[12\]\[13\]

### 3.1.2 Implausible absence

Systems should treat certain absences as suspicious:

-   no recorded failures in domains where failure is normal,

-   only positive outcomes and no negative/near‑miss records,

-   abrupt silence from previously active participants.\[3\]\[4\]\[1\]

-   sustained signal absence coinciding with measurable low trust conditions, where Relational battery depletion (per the Four Batteries Capacity Standard) indicates that the coupling gate through which adverse signals propagate may be closed rather than empty.

Such implausible absences are themselves adverse signals about the record or the context. The final class above requires disambiguation that ASEP detection instruments cannot perform alone: low trust suppresses adverse signal transmission at the source before signals enter the detection architecture, producing a signal-absence reading structurally identical to a healthy-system reading from inside the detection surface. Signal absence combined with low Relational battery state warrants investigation rather than clearance; disambiguating the two requires Four Batteries state data alongside ASEP detection data.

### 3.1.3 Proportional observation

ASEP does not require maximal surveillance. Observation and logging must
be proportionate to the risks addressed and consistent with consent,
privacy, and data‑sovereignty norms (including CARE/OCAP where
applicable).\[21\]\[22\]

## 3.2 Name -- Recording and Classifying

ASEP requires systems to record and classify adverse signals in ways
that remain legible over time.

### 3.2.1 Durable logging

Adverse signals are recorded in durable, tamper‑evident or
tamper‑resistant logs where feasible (e.g., append‑only logs,
cryptographically committed records, independent repositories). Each
entry should include:

-   observable description of what happened (separating observation from
    evaluation),

-   when and where it occurred,

-   who/what was affected,

-   who reported it, and in what role.\[13\]\[19\]\[1\]

### 3.2.2 Non‑neutral context

ASEP assumes context (culture, power, history, incentives) is not
neutral. Where salient, logs should capture contextual factors such as:

-   relative power or dependency between reporter and subject,

-   relevant history of similar incidents,

-   structural incentives that may shape reporting or suppression.\[1\]

When "context" is invoked to downgrade, defer, or dismiss signals, that
reasoning must be recorded; repeated use of context to explain away
similar signals is itself a pattern to detect.\[14\]\[20\]\[5\]

### 3.2.3 Taxonomy and severity

Systems maintain a public or at least internally documented taxonomy of
adverse signals (categories) and severity levels (impact and urgency
bands). The taxonomy must be:

-   defined ex‑ante and versioned over time,

-   subject to periodic coverage review (checking for missing harm
    classes, especially to marginalized groups, future users, or
    ecosystems).\[7\]\[8\]\[9\]\[1\]

Classification can be approximate but must be explicit; "unclassified"
is a temporary state with a maximum dwell time.

Persistent use of low‑severity labels for recurring signals with
substantial aggregate impact MUST prompt a review of the taxonomy and
thresholds; resisting such updates is treated as an adverse signal about
taxonomy governance.

### 3.2.4 Multi‑stakeholder criteria

Criteria for what counts as an adverse signal, and for severity levels,
should be developed and updated with meaningful input from
constituencies who bear the risks, not solely by system operators or
insiders.

## 3.3 Navigate -- Responding and Deciding

ASEP requires systems to move from signal to decision.

### 3.3.1 Time‑boxing and action set

For each severity level, systems must define:

-   maximum time‑to‑assessment (first substantive look), and

-   maximum time‑to‑first‑decision (choose an action),

along with a small set of allowed actions, such as:

-   mitigate or contain,

-   escalate to a higher authority or broader circle,

-   initiate engagement with contested parties (for conflict-class signals; see Section 3.3.1a),

-   monitor with defined review points,

-   close with documented rationale.\[25\]\[2\]\[5\]

Letting defined time bounds lapse without action or explicit closure is
treated as a process failure and itself logged as an adverse signal
about governance health.

### 3.3.1a Conflict-class routing

An adverse signal is conflict-class when it meets at least one of three observable conditions: two or more parties have deposited contested accounts of the same coordination event; one party has formally challenged a coordination determination by another party; or one party has deposited a signal naming another party as responsible for a harm to the coordination record, the coordination process, or a coordination participant. These conditions are determinable by an independent observer from the coordination record without access to parties' intentions.

For conflict-class signals, initiating engagement with the contested parties is required before Navigate terminates the signal through escalation to external adjudication or closure. The structural conditions under which that engagement constitutes genuine transformation capacity are operational design requirements for the adopting system; ASEP does not specify them. A conflict-class signal may subsequently escalate to external adjudication or close with documented rationale; the requirement is that the engagement pathway is opened, that a documented exchange within the engagement process has taken place, and that the Navigate decision is recorded after that exchange.

### 3.3.2 Graduated and proportionate response

Reflecting Ostrom's "graduated sanctions," responses should be
proportionate to severity and pattern:\[23\]\[24\]

-   low‑severity signals: minimal intervention, monitoring, and
    learning,

-   medium: targeted fixes, local policy changes, stronger oversight,

-   high: decisive interventions (e.g., disabling functionality,
    governance changes, public or regulatory notification).

Where safe and appropriate, responses should be resolved at the most
local competent level, with clear escalation paths when local handling
fails or conflicts of interest exist.\[24\]\[23\]

### 3.3.3 Pattern escalation ("three times is a pattern")

Systems must support pattern‑based escalation:

-   aggregation of repeated similar signals (e.g., same subsystem,
    actor, harm type),

-   thresholds where repeated lower‑severity signals collectively
    trigger a higher severity tier.

The heuristic "once is an incident, twice is a coincidence, three times
is a pattern" is treated as operational guidance: similar signals cannot
be handled as isolated events forever.\[4\]\[3\]\[1\]

Systems MAY NOT indefinitely treat a repeated class of similar adverse
signals as isolated low‑severity incidents when their frequency or
combined impact increases. At defined pattern thresholds,
reclassification is mandatory.

Pattern escalation is a double-loop learning trigger: when repeated
similar signals persist despite individually correct single-loop
responses (applying the designated fix each time), the pattern itself is
evidence that the response framework, not the individual response,
requires examination. Systems that structurally prevent this transition
(by requiring all escalation to remain within the current response
taxonomy) cap themselves at single-loop learning regardless of signal
volume.

When a pattern threshold triggers mandatory reclassification, the
Navigate phase must include a structural root cause assessment before
individual attribution is accepted as final resolution. The assessment
must determine whether the recurrent signal class reflects individual
failures, a structural condition enabling repeated failures, or both.
Accepting individual attribution without this assessment closes the
signal at the individual level while leaving the structural condition
intact and unaddressed. The structural root cause assessment is complete
when it has produced one of three findings: (a) no structural condition
identified, individual attribution stands; (b) structural condition
identified, system enters double-loop examination of the response
framework; (c) insufficient information, monitoring extended and
investigation continued. A determination that no structural condition
exists must be documented as a finding, not left implicit.

### 3.3.4 Polycentric and nested handling

ASEP is intended to work at multiple nested levels (teams,
organizations, protocols, ecosystems) with overlapping authorities.
Implementations should:\[22\]\[21\]\[23\]\[24\]

-   define when signals stay local vs. escalate to higher levels (e.g.,
    cross‑org patterns, conflicts of interest, failures at lower
    levels),

-   avoid architectures where a single center can fully gate
    adverse‑signal handling.

### 3.3.5 Adversarial misuse and abuse

Systems may:

-   de‑duplicate and rate‑limit obvious flooding or bot campaigns, and

-   route clearly abusive or harassing reports through an abuse‑handling
    process.

However, judgments that a report is adversarial or abusive must be
logged, and categories of adverse signals may not be erased wholesale
using "abuse" as justification. "We believe this is adversarial" is
itself a claim requiring a documented basis.

**3.3.6 Signal Escalation**

Systems must define a maturation path for adverse signals that are not
acknowledged within the time-to-assessment window. Signal Escalation is
a state transition sequence governed by elapsed time, not by human
initiative. Its purpose is to ensure that governance inaction in the
presence of a detected adverse signal is itself observable and
procedurally consequential.

A conforming maturation path must specify at least:

(a) An acknowledgment window: the maximum elapsed time from signal
    generation to first acknowledgment (log, classify, assign to a
    process, or formally close with rationale). This window must be
    defined per severity level, consistent with the time-to-assessment
    requirements above.

(b) An auto-escalation threshold: if the acknowledgment window expires
    without action, the signal automatically transitions to an escalated
    visibility state. The escalation is a system event, not a human
    decision. At minimum, the escalated signal must be published to the
    governance record with a status indicating that it matured without
    acknowledgment.

(c) A governance obligation trigger: if the escalated signal persists
    without acknowledgment for a second defined period, the system must
    generate a governance artifact (equivalent in procedural standing to
    a filed proposal, inquiry, or review request) that enters the
    system's standard governance lifecycle. This artifact does not
    require a human author. Its existence is the system's structural
    response to sustained inaction.

(d) A terminal visibility state: if the governance artifact itself is
    not processed within the governance lifecycle's own time limits,
    that fact is recorded as a constitutional-level governance failure
    signal, visible in the system's aggregate health metrics and
    relevant to any exit, fork, or legitimacy assessment mechanism the
    system provides.

The terminal visibility state is a triple-loop learning trigger. A
system whose governance lifecycle cannot process its own governance
artifacts has exhausted both single-loop correction (applying existing
responses) and double-loop correction (modifying the response
framework). What remains is examination of the values and commitments
that generated the governance framework itself.

The maturation path applies to all adverse signals, including signals
about the maturation process itself. This recursion terminates because
the maturation mechanism is time-governed, not initiative-dependent: the
clock runs whether or not any governance actor chooses to engage.

Systems that adopt the Adverse-Signal Engagement Principle at the
ASEP-Instrumented tier must implement Signal Escalation for all severity levels.
Systems at the ASEP-Assessed or ASEP-Operational tiers should implement Signal Escalation
for high-severity signals at minimum.

**Window validity requirements.** Any time window specified in a conforming Signal Escalation architecture (including the acknowledgment window, auto-escalation threshold, governance obligation trigger period, and any audit disclosure period) must satisfy three conditions to be valid. First, the window length must be publicly specified before the window begins running for any given signal: a window whose length is determined after the fact, or is adjustable while the clock is running, does not constitute a defined window. Second, the window length must be uniform across structurally equivalent signals: the same severity level and complexity domain classification must yield the same window parameters, regardless of who filed the signal or who the signal implicates. Differential window treatment for structurally equivalent signals is a non-discrimination failure subject to the Notice/Name/Navigate flow. Third, the window parameters in effect at the time of signal generation govern that signal's escalation path: parameters may be revised through the system's governance process, but revision does not apply retroactively to signals already in the escalation sequence at the time of revision. This third condition is the window-specific expression of the ex-ante invariant in Section 2.2. The first two conditions are additive commitments not implied by that invariant.

**Domain-calibrated escalation tempo.** The staged escalation path
described above assumes that governance actors have deliberation time
between stages: time to assess the signal, convene the relevant
expertise, and decide on a response. This assumption holds for
Clear-domain, Complicated-domain, and Complex-domain signals, where the
corresponding Cynefin action modes (sense-categorize-respond,
sense-analyze-respond, probe-sense-respond) all include a sensing or
analysis phase before action is required. The assumption does not hold
for Chaotic-domain signals.

The Chaotic-domain action mode is act-sense-respond: action is required
before analysis is complete, because the system is in a state of active
destabilization where delay compounds harm. A Chaotic-domain adverse
signal entering the standard staged escalation path encounters
time-gated transitions designed for conditions that Chaotic events have
already exceeded. The staged queue imposes a deliberation tempo on a
situation that demands immediate governance visibility.

A conforming implementation must therefore classify incoming adverse
signals by complexity domain and apply domain-appropriate escalation
behavior. Specifically:

(a) Clear-domain, Complicated-domain, and Complex-domain signals follow
    the standard staged path: acknowledgment window, auto-escalation
    threshold, governance obligation trigger, terminal visibility state,
    with timing parameters calibrated to the domain's action mode.

(b) Chaotic-domain signals bypass the acknowledgment window and enter
    the escalation path at the auto-escalation stage. The signal is
    immediately published to the governance record with
    Chaotic-domain classification, made visible to all governance
    actors, and the governance obligation countdown begins at the point
    of signal generation rather than after an unacknowledged
    acknowledgment window.

(c) The Chaotic-domain bypass does not eliminate any escalation stage;
    it compresses the timeline by removing the initial waiting period. A
    Chaotic-domain signal that is acknowledged after bypass follows
    standard Navigate processing from that point. A Chaotic-domain
    signal that is not acknowledged proceeds through the governance
    obligation trigger and terminal visibility state on the standard
    timeline.

(d) Domain classification of incoming signals is itself a governance
    judgment that must be logged. A signal classified as Chaotic that is
    later reclassified (once stabilization has been achieved) retains
    its escalation history; the reclassification does not retroactively
    undo the bypass.

The general principle is that escalation tempo should match the action
mode of the signal's complexity domain. The Chaotic-domain priority jump
specified here is the most urgent instance of this principle. Future
revisions may specify differentiated timing parameters for
Complicated-domain signals (which require expert analysis cycles) and
Complex-domain signals (which require iterative probing), but the
standard staged path is adequate for both until implementation
experience indicates otherwise.

**3.3.7 Domain-calibrated navigation**

The Cynefin framework defines four action modes corresponding to its
four complexity domains: sense-categorize-respond (Clear),
sense-analyze-respond (Complicated), probe-sense-respond (Complex), and
act-sense-respond (Chaotic). The shape of the Navigate path should match
the action mode appropriate to the signal's complexity domain. A
Clear-domain adverse signal (a parameter exceeds a known threshold, a
procedural step was skipped) has a known resolution path: categorize the
signal against the existing taxonomy and apply the designated response.
A Complicated-domain adverse signal (a structural pattern that requires
expert analysis to interpret) needs an analysis phase before the
response can be selected; the time-to-assessment window should reflect
the expert evaluation cycle. A Complex-domain adverse signal (an
emergent pattern that does not match any existing asymmetry class, or
that the taxonomy cannot yet classify) requires iterative probing before
the resolution path becomes visible; the navigation process is
probe-sense-respond, not a linear deliberation. A Chaotic-domain adverse
signal (system crisis, cascading failures) requires stabilization before
analysis: act first to contain, then sense, then respond with a
deliberated plan.

The learning loop depth appropriate to each domain follows from the
action mode. A Clear-domain adverse signal calls for single-loop
learning: the signal matches an existing category, the designated
response is known, the task is to execute correctly within the current
framework. A Complicated-domain adverse signal typically calls for
single-loop learning, but recurrence of the same signal class despite
correct responses is a double-loop trigger: the response framework
itself may be inadequate, and expert analysis should evaluate the
framework, not only the signal. A Complex-domain adverse signal may
require double-loop or triple-loop learning: an emergent pattern that
the taxonomy cannot classify is evidence of a structural gap in the
classification framework. Addressing it by forcing the signal into
existing categories (single-loop) suppresses the information the signal
carries. A Chaotic-domain adverse signal calls for single-loop
stabilization first (contain the crisis using available responses),
followed by assessment of what learning loop depth the
post-stabilization analysis requires.

The practical implication: systems that apply a single Navigate process
shape to all adverse signals will either under-respond to Complex
signals (forcing them through a linear categorize-and-respond path that
cannot accommodate emergent patterns) or over-respond to Clear signals
(applying iterative probing to something with a known answer). The
time-boxing requirements in Section 3.3.1 and the graduated response in
Section 3.3.2 remain in force; domain-calibrated navigation specifies
the process shape within those constraints, not a replacement for them.
See: Structural Consent Legibility Standard, Section 6.4 for the
general principle of Cynefin action mode calibration.

Domain-calibrated navigation specifies the process shape (how a signal
is handled once acknowledged); the domain-calibrated escalation tempo in
Section 3.3.6 specifies the escalation behavior (what happens when a
signal is not acknowledged). Both are derived from the same Cynefin
action modes, applied to different phases of the signal lifecycle.

**3.3.8 Early intervention weighting**

The cost of addressing an adverse signal escalates nonlinearly with
time. A signal engaged at first detection, before compensatory
workarounds have formed and before organizational identity has fused
with the conditions that produced the signal, is structurally cheaper
to resolve and more likely to result in a successful outcome than the
same signal engaged after those dynamics have calcified. This is not a
policy preference; it is a structural property of how organizations
respond to adverse conditions under load.

The mechanism is as follows. When an adverse signal first appears,
affected participants may begin compensating for the underlying
structural failure informally. If the signal is engaged promptly
(the failure acknowledged and addressed through formal process),
participants can release those informal compensations without
significant cost. If engagement is delayed, participants invest
progressively more identity and effort in their compensatory
structures. The compensatory work becomes entangled with how they
understand their role in the system. At that point, even a correct
structural response encounters resistance, because the people who
have been compensating experience the formal fix as a threat to
something they now own psychologically. The longer the delay, the
deeper the entanglement, the higher the cost of resolution, and the
lower the probability of success.

Empirical patterns across organizational contexts suggest the cost
curve is roughly exponential: early-stage intervention (before
compensatory structures form) costs approximately one unit of
organizational resource with high probability of success; mid-stage
intervention (after compensatory structures exist but before identity
fusion) costs three to five times as much with moderately reduced
success probability; late-stage intervention (after identity fusion)
costs ten to fifty times as much with sharply reduced success
probability. These ratios are illustrative, not prescriptive; the
structural shape of the curve (nonlinear escalation) is the design-
relevant property, not the specific multipliers.

A conforming system should structure its incentive mechanisms to reward
early-stage engagement with adverse signals. The specific mechanism
depends on the system's context: token-weighted coordination protocols
may assign higher weight to coordination evidence produced by early
engagement; organizational governance systems may prioritize early-
stage response in resource allocation; regulatory frameworks may
offer graduated compliance benefits for proactive engagement. The
principle is mechanism-agnostic: whatever incentive structure the
system uses, it should not be neutral between early and late
engagement, because the outcomes are not equivalent.

Tier-differentiated guidance: systems at the ASEP-Instrumented tier must
document how their incentive structures reward early engagement with
adverse signals and must treat sustained delay in engaging acknowledged
signals as itself an adverse signal about governance health (subject to
the Notice/Name/Navigate flow). Systems at the ASEP-Operational tier should
document their approach to early engagement incentives as part of their
periodic tier review. Systems at the ASEP-Assessed tier are encouraged to
consider early engagement incentives but are not required to formalize
them.

Sub-organizations or member bodies operating within an ASEP-conforming
system may adopt this principle internally by structuring their own
recognition, compensation, or governance-weight mechanisms to reward
early-stage adverse signal engagement. The parent system's incentive
structure provides the external signal; the member body's internal
structure determines whether that signal propagates to the individuals
and teams who do the early-stage work. Systems that weight early
engagement at the governance level but whose member bodies do not
replicate the incentive internally create a structural gap: the parent
system rewards the member body for early engagement, but the member
body does not reward the people who performed it. This gap is itself
detectable as a divergence between system-level and member-level
adverse signal response patterns.

**3.3.9 External governance override**

External authority actions that preempt, override, or delegitimize a system's internal adverse-signal handling process are themselves adverse signals of a specific class. This class includes regulatory interventions that transfer adverse-signal classification authority to an external body without the affected constituency's consent, and authority assertions by external parties that selectively disable portions of the Notice-Name-Navigate sequence.

A conforming implementation must: (a) name external governance override as a recognized signal class in its signal taxonomy; (b) treat recognition of the system's self-governance capacity by relevant external authorities as a detection prerequisite, disclosed where absent; and (c) apply Navigate phase obligations to external governance override signals at the tier appropriate to their structural impact.

The detection prerequisite in (b) requires assessment, not mere absence of challenge. "No external authority has challenged our governance processes" is not a recognition assessment; it is an absence of detected conflict. A conforming recognition assessment documents what external authorities have governance reach over the system's processes and what the current recognition status is. Where recognition is absent, the gap is disclosed as a structural exposure rather than treated as compliance.

This section applies where the system is within a governance jurisdiction where external authority has realistic governance reach. Systems operating below any meaningful regulatory or legal threshold in a given domain are not required to produce a recognition assessment for that domain, but must document the basis for that determination.

The converse failure mode is also a signal class: a coordination system that claims self-governance legitimacy across multiple governance cycles while operating at a scale where external governance reach is structurally possible, and that carries no recognition assessment, has not satisfied this section. Absence of challenge is not recognition.

# 4. Operational Guarantees and Ethical Posture

## 4.1 Anti‑retaliation

ASEP-Operational systems commit to protecting individuals and entities who
surface good‑faith adverse signals from retaliation (e.g., dismissal,
demotion, bans, smears, legal threats). Allegations of retaliation for
adverse‑signal surfacing are themselves adverse signals and enter the
Notice/Name/Navigate flow immediately.

## 4.2 Source‑agnostic logging

Any actor, regardless of status, role, or affiliation, can generate a
log entry for an adverse signal if minimal criteria (specificity,
relevance) are met. Status may influence prioritization of review, but
not the right to log.

## 4.3 Independent and tamper‑evident logging

Where feasible, systems provide at least one logging path that is
independent of the actors being evaluated, or tamper‑evident (e.g.,
append‑only logs, third‑party ombuds, cross‑org channels). Actors whose
behavior is being logged should not be the sole custodians of those
logs.

## 4.4 Meta‑ASEP (watching the watchers)

Failures of ASEP implementation (chronic missed timelines, systematic
retaliation, consistent over‑collection, or repeated use of "context" to
silence certain signal types) are themselves treated as adverse signals
about governance health and enter the same Notice/Name/Navigate flow.

## 4.5 Consent‑aware responses (Wheel of Consent)

Informed by Betty Martin's Wheel of Consent, ASEP requires clarity about
who is acting and who a response is for.\[27\]\[28\]\[29\]\[30\]

For significant adverse‑signal responses, systems should record:

-   who initiated the response (e.g., constituencies, operators,
    regulators), and

-   who the response is primarily intended to benefit.

Systematic divergence (responses initiated by those at risk but
consistently designed to benefit operators or insiders) is itself an
adverse governance signal that must enter the Notice/Name/Navigate flow.

ASEP discourages "for your own good" responses that primarily protect
institutional power or optics, especially where affected constituencies
lack real alternatives or voice.

## 4.6 Commons‑aligned governance (Ostrom)

ASEP's governance structure is informed by Elinor Ostrom's principles
for managing commons: monitoring by accountable participants, graduated
responses, and polycentric governance.\[23\]\[24\] Implementations
should:

-   involve affected constituencies in defining adverse‑signal criteria
    and escalation rules,

-   ensure monitoring and response are accountable and not solely
    centralized,

-   provide low‑cost, timely paths to raise and resolve adverse‑related
    conflicts,

-   operate in a polycentric and nested fashion, with multiple
    overlapping loci of monitoring and response rather than a single
    monolithic center,\[23\]\[24\]

-   recognize that the system's capacity to conduct its own adverse-signal engagement requires minimal recognition by relevant external authorities (Ostrom's seventh design principle), and treat external authority actions that preempt or override that internal capacity as an adverse signal class per Section 3.3.9.

# 5. Adoption Tiers

ASEP recognizes that not all systems require the same depth of
machinery. At the same time, tier selection and maintenance are
themselves governance decisions that can create or conceal risk, and are
subject to ASEP's own invariants.

## 5.0 Tier governance and review

Systems MUST review their ASEP tier at defined intervals (e.g.,
annually) and when crossing key thresholds of scale, dependency, or
criticality (such as user count, assets under management, or systemic
dependency by other organizations).

Decisions to remain at or move between tiers MUST be logged with
rationale.

Repeated decisions to remain at a lower tier despite accumulating
evidence of higher impact or dependency are treated as adverse
governance signals and MUST enter the Notice/Name/Navigate
flow.\[5\]\[1\]

## 5.1 ASEP-Assessed

Intended for small, low‑risk, easy‑exit contexts.

-   At least one channel to surface serious adverse signals.

-   Some durable way to record them (even if simple).

-   No obvious retaliation against those who raise concerns.

Systems SHOULD move to at least ASEP-Operational when they begin to:

-   affect large numbers of people,

-   hold or route significant value,

-   or become infrastructural for other organizations (dependency).\[1\]

## 5.2 ASEP-Operational

Recommended for most organizations and protocols with meaningful
external impact.

Full Notice/Name/Navigate loop:

-   basic taxonomy and severity levels,

-   time‑boxing for assessment and decision,

-   pattern escalation,

-   some metrics (counts, timelines, fraction of overdue cases) and
    periodic retrospectives.\[5\]\[1\]

Crossing domain‑specific thresholds of scale, concentration, or
irreversibility (e.g., becoming a base protocol, major AI deployment, or
key financial rail) SHOULD trigger a move to ASEP-Instrumented, or a logged
and regularly reviewed decision to remain at ASEP-Operational.

## 5.3 ASEP-Instrumented

Expected for systems whose failure could materially affect many people
or critical infrastructure (base protocols, major AI deployments,
financial rails, regulators).

Includes all ASEP-Operational requirements plus:

-   independent or tamper‑evident logging paths,

-   explicit anti‑retaliation policy and tracking,

-   multi‑stakeholder criteria setting and coverage reviews,

-   explicit polycentric/nested handling design,

-   initiator--beneficiary tracking for major responses,

-   regular internal and (where appropriate) public or regulator
    reporting on ASEP metrics.\[32\]\[6\]\[7\]\[11\]\[1\]

Systems that perform high‑impact infrastructural roles are PRESUMED to
require ASEP-Instrumented unless they can demonstrate the contrary in a
logged, regularly reviewed governance decision.

A simple rule of thumb: the deeper and less reversible the potential
harm, and the less real exit/choice constituencies have, the closer a
system MUST be to ASEP-Instrumented, absent a recorded and regularly
reviewed justification for a lower tier.

## 5.4 ASEP-Accountable

Includes all ASEP-Instrumented requirements plus closed governance loop architecture.

The defining property of ASEP-Accountable is that governance inaction is structurally visible without depending on any actor's cooperation. At ASEP-Instrumented, detection infrastructure produces outputs. At ASEP-Accountable, those outputs produce mandatory governance responses, and the absence of a response is itself a detected event.

Minimum requirements:

Every signal that enters Stage 3 (governance obligation trigger) in the Signal Escalation architecture must produce a documented governance decision within the defined Stage 3 window. The Stage 3 window must satisfy the window validity requirements specified in Section 3.3.6. The decision record must include: the signal identifier, the classification assigned at the Name phase, the decision made (including decisions to defer or decline action), the actor or body responsible for the decision, and the rationale. A decision to take no action is a decision and must be documented as such. The absence of any documented decision is not a permissible outcome at ASEP-Accountable.

The absence of a documented decision at Stage 3 must produce automatic Stage 4 publication without requiring any actor's initiation. Stage 4 publication makes the signal, its classification, the elapsed time since Stage 3 trigger, and the absence of a governance decision simultaneously visible to all governance actors. This publication is a structural consequence of the Signal Escalation architecture, not a discretionary act. A system in which Stage 4 publication requires a human decision to publish has not closed the governance loop and does not meet ASEP-Accountable.

The governance decision record is append-only. Decisions cannot be modified after recording; corrections are recorded as new entries referencing the original. This property is what makes governance inaction detectable without cooperation: an independent observer can verify that a Stage 3 trigger exists in the record, verify that no Stage 3 decision entry exists within the required window, and determine that Stage 4 publication was or was not produced as a consequence.

Tier review cadence for ASEP-Accountable systems: tier review MUST occur at minimum annually and MUST include a governance loop integrity check: confirmation that the Stage 3 to decision path operated as specified for all signals that reached Stage 3 in the review period, and that Stage 4 publications were produced where required.

## 5.5 ASEP-Auditable

Includes all ASEP-Accountable requirements plus independent auditability.

The defining property of ASEP-Auditable is that the full detection and response architecture can be verified by a party outside the system without depending on system operator cooperation or self-certification.

Minimum requirements:

The complete Signal Escalation record, from signal generation through Stage 4 or documented decision, must be accessible to an independent auditor. Access is not contingent on operator consent during a defined audit period. The record format is sufficient for an auditor to verify completeness without access to the detection layer itself.

The auditor must be able to verify completeness: that all signals generated in the audit period are present in the record. This requires that the signal generation architecture produces a verifiable count or hash of signals generated, against which the record can be checked. A record that can only be verified for presence (each signal in the record was generated) but not for completeness (all signals generated are in the record) does not meet ASEP-Auditable. The gap between generated and recorded is the detection surface for suppression; an audit that cannot detect that gap cannot verify that suppression has not occurred.

The auditor must be able to verify stage integrity: that each recorded stage transition is consistent with the Signal Escalation specification. This means stage transition timestamps are present, the transition conditions are documented per class and Cynefin domain, and the timing parameters applied to each signal are the parameters in effect at the time of signal generation (not retrospectively applied parameters).

The auditor must be able to verify response completeness: that every Stage 3 trigger in the record produced either a documented governance decision within the specified window or an automatic Stage 4 publication. Gaps in this chain are reportable findings.

The audit itself must be documented: scope, period, auditor identity or body, findings, and system response to findings. Audit reports are retained in the governance record under the same append-only constraints as governance decisions.

ASEP-Auditable systems must make audit reports available to their participant population within a defined period after audit completion. The disclosure period is specified by the system, must satisfy the window validity requirements specified in Section 3.3.6, and is subject to the same precision requirements as all other ASEP obligations.

# 6. Implementation Considerations

ASEP compliance is not only a matter of policy; it requires basic
technical and organizational infrastructure.

## 6.1 Data and systems prerequisites

ASEP-Operational systems SHOULD expect to provide at least:

**Collection surfaces.** Channels and interfaces through which adverse
signals can be submitted and ingested (e.g., reporting forms, admin
consoles, monitoring hooks, on‑chain event types).\[11\]\[6\]\[1\]

**Structured storage.** Durable logs or databases that can capture
ASEP‑relevant fields such as observation, context, severity, source,
initiator/beneficiary, decisions taken, timestamps, and pattern
identifiers.\[19\]\[1\]

**Linkage to system components.** Mechanisms to associate adverse
signals with specific systems, components, contracts, organizations, or
governance actions, so patterns can be detected and acted upon.\[1\]

## 6.2 Process and interface implications

To satisfy the Notice/Name/Navigate obligations, systems SHOULD provide:

**Human‑facing reporting interfaces.** Ways for participants and
external constituencies to raise adverse signals, receive
acknowledgment, and (where appropriate) see status changes.\[25\]\[26\]

**Internal triage and decision views.** Queues, dashboards, or views for
designated roles to classify signals, apply severity, and make
time‑bounded decisions.\[5\]\[1\]

**Built‑in escalation paths.** Explicit actions or flows in tools that
correspond to escalation, reclassification, and closure with rationale,
aligned with the system's ASEP tier and governance model.\[5\]\[1\]

Implementations MAY differ widely by domain (e.g., smart‑contract events
vs. enterprise tickets), but systems SHOULD be clear about how their
technical infrastructure maps to each ASEP obligation.

## 6.3 Profiles and guides

This core standard is accompanied by:

-   a Generic ASEP Implementation Guide, offering step‑by‑step adoption
    patterns for any organization, and

-   domain‑specific profiles (e.g., Web3 protocols and Decentralized Autonomous Organizations (DAOs), AI systems,
    media organizations, public agencies) that describe how ASEP can be
    instantiated in those environments.\[8\]\[7\]\[6\]\[11\]\[1\]

These guides are normative supplements to this standard: they DO NOT
change the invariants in Sections 2--4, but provide concrete ways to
satisfy them in specific contexts.

# 7. Normative References

The following documents are referenced by citation number throughout
this standard. All inline citations of the form \[n\] refer to entries
in this list.

**\[1\]** Chapman, Regis Lloyd (Durgadas). *Holonic Governance Commons -
Proof of Coordination Protocol Specification v2.x.* 2021--2026.: Primary
reference implementation of ASEP at ASEP-Instrumented level. Source of the
triplicate prescription precedent and coordination ledger design.

**\[2\]** NIST. *Computer Security Incident Handling Guide (SP 800‑61
Rev. 2).* National Institute of Standards and Technology, 2012.:
Foundational incident response lifecycle: preparation, detection,
containment, eradication, recovery, post‑incident review.
https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf

**\[3\]** Basin Safety. *Near‑Miss Data: Turning Minor Incidents into
Major Lessons.* Basin Safety, 2023.: Near‑miss reporting as adverse
signal; pattern detection from low‑severity events.
https://blog.basinsafetyus.com/post/near-miss-data-turning-minor-incidents-into-major-lessons

**\[4\]** CyberPlanz. *The Importance of Recording Near‑Misses in
Cybersecurity.* LinkedIn / CyberPlanz, 2023.: Pattern escalation from
near‑miss records in security contexts.
https://www.linkedin.com/pulse/importance-recording-near-misses-cybersecurity-cyberplanz-limited-bv2mc

**\[5\]** Wiz Academy. *Incident Response Frameworks.* Wiz, 2024.:
Detection‑and‑response frameworks; time‑boxing and escalation design.
https://www.wiz.io/academy/detection-and-response/incident-response-frameworks

**\[6\]** NIST CSRC. *A Security Perspective on the Web3 Paradigm.*
National Institute of Standards and Technology, 2025.: Web3‑specific
security and governance signal handling.
https://csrc.nist.gov/news/2025/a-security-perspective-on-the-web3-paradigm

**\[7\]** Australian Government, Department of Industry, Science and
Resources. *Voluntary AI Safety Standard: 10 Guardrails.* Commonwealth
of Australia, 2024.: Domain‑specific AI safety standard; tiered
compliance model.
https://www.industry.gov.au/publications/voluntary-ai-safety-standard/10-guardrails

**\[8\]** Safe AI Australia. *Voluntary AI Safety Standard - 10
Guardrails.* Safe AI Australia, 2024.: Parallel AI safety standard;
extensible guardrail structure.
https://safeaiaus.org/safety-standards/voluntary-ai-safety-standard-10-guardrails/

**\[9\]** Cyvers. *Web3 Incident Response: A Comprehensive Guide to
Cybersecurity in Decentralized Protocols.* Cyvers, 2024.: Web3‑specific
incident classification and response.
https://cyvers.ai/blog/web3-incident-response-comprehensive-guide-to-cybersecurity-in-decentralized-protocols

**\[10\]** Cantina. *Incident Response and Threat Monitoring for Web3.*
Cantina, 2024.: Threat monitoring and adverse‑signal detection in
decentralized protocols.
https://cantina.xyz/blog/incident-response-and-threat-monitoring-for-web3

**\[11\]** DataGuard. *What Are the Principles of Incident Response?.*
DataGuard, 2024.: Incident response principles; escalation and closure
rationale.
https://www.dataguard.com/blog/what-are-the-principles-of-incident-response/

**\[12\]** FBI / IC3. *Cyber Advisory on Reporting (CSA 251215).*
Internet Crime Complaint Center, 2025.: Source‑agnostic adverse signal
intake; adversarial misuse handling.
https://www.ic3.gov/CSA/2025/251215.pdf

**\[13\]** Darby, Josh. *Every Criticism, Judgment, Diagnosis \[LinkedIn
post on NVC and adverse signals\].* LinkedIn, 2025.: Emotionally
expressed complaints as legitimate adverse signals; NVC critique
context.
https://www.linkedin.com/posts/josh-darby-286a4b224_every-criticism-judgment-diagnosis-and-activity-7383607893184561152-ZKdR

**\[14\]** St. Mary's College of California Archive. *Criticism of
Non‑Violent Communication.* St. Mary's College of California, 2020.: NVC
critique: frameworks that silence dissent or displace emotional labor
onto marginalized parties.
https://archive.stmarys-ca.edu/archive-library-204/criticism-of-non-violent-communication.pdf

**\[19\]** University System of New Hampshire. *Incident Response
Standard - Cybersecurity.* USNH Information Technology, 2023.:
Structured logging fields for incident records; who/what/when/role
requirements.
https://www.usnh.edu/it/departments/cybersecurity/cybersecurity-policies-standards/incident-response-standard-cybersecurity

**\[20\]** Mann, Graham. *Book Notes: Nonviolent Communication -
Marshall Rosenberg.* grahammann.net, 2022.: NVC framework summary; basis
for critique of context‑invocation to silence signals.
https://grahammann.net/book-notes/nonviolent-communication-marshall-rosenberg

**\[21\]** LINCS Project. *CARE Principles for Indigenous Data
Governance.* LINCS, 2022.: Data sovereignty and consent norms informing
proportional observation requirements.
https://lincsproject.ca/docs/terms/care-principles-for-indigenous-data-governance

**\[22\]** Wikipedia. *CARE Principles for Indigenous Data Governance.*
Wikimedia Foundation, 2024.: CARE/OCAP principles; data sovereignty in
governance contexts.
https://en.wikipedia.org/wiki/CARE_Principles_for_Indigenous_Data_Governance

**\[23\]** Ostrom, Elinor. *Governing the Commons: The Evolution of
Institutions for Collective Action.* Cambridge University Press, 1990.:
Primary source. Eight design principles for sustainable commons
governance: graduated sanctions, polycentric governance, accessible
conflict resolution, participatory rule-making. ISBN 978-0-521-40599-7.
https://www.cambridge.org/core/books/governing-the-commons/7AB7AE11BADA84409C34815CC288CD79

**\[24\]** Ostrom, Elinor. *Governing the Commons: The Evolution of
Institutions for Collective Action.* Cambridge University Press, 1990.:
As \[23\]. Cited separately where the navigate-phase and tier structure
are grounded in Ostrom's graduated sanctions and polycentric governance
design principles.

**\[25\]** Ostrom, Elinor. *Governing the Commons: The Evolution of
Institutions for Collective Action.* Cambridge University Press, 1990.:
As \[23\]. Cited for applied governance design: local resolution,
escalation paths, and nested authority.

**\[26\]** Ostrom, Elinor. *Governing the Commons: The Evolution of
Institutions for Collective Action.* Cambridge University Press, 1990.:
As \[23\]. Cited for multi-stakeholder criteria setting and
participatory rule-making provisions.

**\[27\]** School of Consent. *The Wheel of Consent Explained.* School
of Consent, 2023.: Betty Martin's Wheel of Consent: four quadrants of
giving/receiving/taking/allowing.
https://www.schoolofconsent.org/blog/wheel-explained

**\[28\]** Art of Consent. *Wheel of Consent.* Art of Consent, 2023.:
Consent dynamics in governance responses; who acts and for whom.
https://www.artofconsent.co.uk/wheel-of-consent

**\[29\]** Wheel of Consent. *Betty Martin - Wheel of Consent.*
wheelofconsent.coach, 2023.: Primary practitioner source on the Wheel of
Consent framework. https://www.wheelofconsent.coach/betty-martin/

**\[30\]** Psychology Today. *The Wheel of Consent: Desire, Boundaries,
and Permission.* Psychology Today, 2025.: Academic treatment of Wheel of
Consent in consent and boundary contexts.
https://www.psychologytoday.com/us/blog/ideals-in-question/202508/the-wheel-of-consent-desire-boundaries-and-permission

**\[32\]** University System of New Hampshire. *Incident Response
Standard - Cybersecurity (ASEP-Instrumented reference).* USNH Information
Technology, 2023.: ASEP-Instrumented implementation requirements; reporting
standards for high‑impact systems.
https://www.usnh.edu/it/departments/cybersecurity/cybersecurity-policies-standards/incident-response-standard-cybersecurity

# 8. Informative References

The following works are not cited inline but provide the foundational
intellectual context from which ASEP's design derives. Readers seeking
to understand ASEP's theoretical basis are directed here.

## 8.1 Information Asymmetry and Coordination Failure

**Akerlof, George A.** "The Market for Lemons: Quality Uncertainty and
the Market Mechanism." *The Quarterly Journal of Economics*, 84(3):
488--500, August 1970. DOI: 10.2307/1879431. JSTOR:
http://www.jstor.org/stable/1879431

The foundational paper establishing information asymmetry as a
structural mechanism rather than a market friction. Demonstrates that
asymmetric information between parties does not merely disadvantage the
uninformed party: it can destroy the conditions for exchange entirely.
The logic applies with greater force to coordination systems, where
relationships are repeated and accumulated history is as consequential
as any single transaction.

**Spence, A. Michael.** "Job Market Signaling." *The Quarterly Journal
of Economics*, 87(3): 355--374, August 1973. DOI: 10.2307/1882010.
JSTOR: http://www.jstor.org/stable/1882010

Establishes signaling theory as the mechanism by which the informed
party attempts to credibly communicate quality to the uninformed party.
Directly relevant to ASEP's adverse-signal design: the conditions under
which signals are credible, costly, and manipulable are exactly the
conditions that determine whether adverse-signal records can serve as
reliable detection instruments.

**Rothschild, Michael, and Stiglitz, Joseph E.** "Equilibrium in
Competitive Insurance Markets: An Essay on the Economics of Imperfect
Information." *The Quarterly Journal of Economics*, 90(4): 629--649,
November 1976. DOI: 10.2307/1885326

Extends the Akerlof/Spence framework to screening: how the uninformed
party designs mechanisms to reveal the informed party's private
information. The separating equilibrium logic underpins ASEP's ex-ante
criteria requirement and the rationale for independent, tamper-evident
logging.

**Bergh, Donald D., Ketchen, David J., Orlandi, Ilaria, Heugens, Pursey
P.M.A.R., and Boyd, Brian K.** "Information Asymmetry in Management
Research: Past Accomplishments and Future Opportunities." *Journal of
Management*, 45(1): 122--158, January 2019. DOI:
10.1177/0149206318798026

Systematic review of 223 management research articles applying
information asymmetry concepts. Provides a framework for understanding
how information asymmetry operates across principal-agent, transaction
cost, and resource dependence theories: the theoretical parents of
ASEP's organizational scope.

## 8.2 Commons Governance

**Ostrom, Elinor.** *Governing the Commons: The Evolution of
Institutions for Collective Action.* Cambridge University Press, 1990.
ISBN 978-0-521-40599-7. 280 pp.

The primary source for ASEP's commons-aligned governance principles.
Ostrom's eight design principles for sustainable commons governance
(including monitored rule compliance, graduated sanctions, accessible
conflict resolution, and polycentric governance) are directly
instantiated in ASEP's Navigate phase and tier structure. ASEP's
graduated response model, pattern escalation logic, and polycentric
handling architecture each derive from Ostrom's empirical findings.
Co-winner, Nobel Memorial Prize in Economic Sciences, 2009.

## 8.3 Safety‑Critical Systems and Near‑Miss Reporting

**Reason, James.** *Managing the Risks of Organizational Accidents.*
Ashgate Publishing, Aldershot, 1997. ISBN 978-1-840-14105-4. 252 pp.

The Swiss Cheese model of organizational accident causation: failures
occur when defensive layers have holes that momentarily align. Near-miss
reporting as the primary mechanism for detecting alignment before it
produces harm. Directly informs ASEP's treatment of implausible absence
and pattern escalation. Foundational text of the patient safety
movement.

**Dekker, Sidney.** *The Field Guide to Understanding Human Error.*
Ashgate Publishing, Aldershot, 2006. ISBN 978-0-754-64826-0. 236 pp.

Non-punitive reporting frameworks in safety-critical systems. The
central insight is that punitive responses to adverse signals suppress
future reporting, producing a record that looks clean while underlying
risk accumulates. This is foundational to ASEP's anti-retaliation and
source-agnostic logging requirements. Distinguishes "human error" as
attribution from "system failure" as causation.

## 8.4 Regulatory Precedent

The triplicate prescription law precedent cited in Section 1 is analyzed
in the Information Asymmetry Classification Standard \[A2\]. The regulatory principle (that
changing the information environment in which decisions are made changes
the decisions, without requiring new prohibitions) is the structural
insight underlying ASEP's adverse‑signal engagement model.

## 8.5 Precision Standards for Coordination Systems

Chapman, Regis Lloyd (Durgadas). Precision-First Design Standard: A
Transferable Standard for Coordination Systems, Governance Protocols,
and Software Design. v1.5.11, March 2026.

The meta-standard from which ASEP's operational structure derives.
Establishes precision as a design invariant for coordination systems:
every element must increase the precision with which the system's
relevant dynamics can be observed, classified, and acted upon. Provides
the theoretical grounding for why ASEP's three invariants, typed
adverse-signal definition, and ex-ante criteria requirement are
structural necessities rather than design preferences, and demonstrates
the conversion methodology (vague normative principle to typed
operational standard) that ASEP instantiates. Derives the
precision-first requirement from the structural absence of trusted
interpretive intermediaries in decentralized systems, which is the
condition that makes ASEP's ASEP-Instrumented tier non-optional for
trustless coordination protocols.

# 9. Domain Implementations

This section documents published ASEP‑conformant implementations and
companion taxonomies. Inclusion here indicates that the referenced
document satisfies ASEP's requirements for its stated phase or domain,
and that the bidirectional reference relationship has been established
by both parties.

## 9.1 Proof of Coordination Protocol - ASEP‑Critical Implementation

**\[A1\] Chapman, Regis Lloyd (Durgadas).** *Holonic Governance
Commons - Proof of Coordination Protocol Specification v2.x.*
2021--2026.

PoC is an ASEP-Instrumented implementation. It instantiates all three ASEP
obligations: Notice (Witness Layer and platform integrations), Name
(Coordination Ledger with 18 event types and asymmetry class taxonomy),
and Navigate (CIP governance, Classified Change Architecture, graduated
Revelis sanctions), in a blockchain‑based coordination protocol. PoC is
the reference implementation demonstrating how ASEP can be adopted at
the ASEP-Instrumented tier in the Web3 context.

## 9.2 Information Asymmetry in Coordination Systems - ASEP Name‑Phase Taxonomy

**\[A2\] Chapman, Regis Lloyd (Durgadas).** *Information Asymmetry
Classification Standard: A Six‑Class Framework for Structural Advantage
in Coordination Systems.* 2026.

This document provides the domain‑specific taxonomy that ASEP's Name
phase requires for coordination systems. It specifies six primary
asymmetry classes (Positional, Temporal, Interpretive, Relational,
Omission, Complexity) and two extension classes (Generative,
Cryptographic), each with a distinct mechanism, historical regulatory
precedent, and detection surface. The taxonomy is ASEP‑conformant: its
governance (extension criteria, versioning, capture prevention)
satisfies ASEP's ex‑ante criteria and finite‑path‑to‑decision invariants
applied to the taxonomy itself. Any coordination system adopting this
taxonomy for its Name phase inherits an ASEP‑conformant classification
infrastructure.

# 10. Inheritance Clause

Systems adopting this standard should include the following statement in their governance documentation:

*ASEP Inheritance: This [document/system/protocol] adopts the Adverse-Signal Engagement Principle Core Standard (v[X], [date]) at the [ASEP-Assessed / ASEP-Operational / ASEP-Instrumented / ASEP-Accountable / ASEP-Auditable] tier. The adverse signal classes identified as applicable to this system's operations are: [list]. Classes identified as not applicable: [list, with rationale].*

The inheritance clause commits the adopting system to: (a) identifying which adverse signal classes are relevant to its operations, (b) applying the three-phase processing loop (Notice, Name, Navigate) at the adopted tier, (c) treating adverse signal suppression as a governance failure subject to the system's adverse signal processing, and (d) disclosing the detection architecture to its participant population as a condition of operating at the ASEP-Instrumented tier or above.

Adoption of this standard at any tier below the full Tensegrity Compressive Standards threshold (Tier 4 across all six Tensegrity Compressive Standards) does not constitute full Tensegrity Compressive Standards conformance and does not reduce structural exposure from uncovered standards. Systems in partial adoption are required to produce a structural exposure disclosure in place of a conformance claim. The four-element specification for a substantive structural exposure disclosure is provided in the standards README.

# 11. Precision-First Design Standard Inheritance Clause

This standard is declared at the Precision-First Design Standard PFDS-Instrumented tier. The declaration reflects the current state of the standard: normative invariants, obligations, and tier specifications have been brought to design-time precision through recursive self-application. The governance infrastructure required for the PFDS-Accountable tier (closed governance loop with automatic disclosure on inaction, append-only governance records, independent auditor access) is deferred to the protocol's operational layer. The tier declaration will advance when that infrastructure is established.

# Relationship To Other Standards

The closest functional seam is with the Conflict Transformation Standard: this standard addresses detection and escalation of signals contradicting current models; that standard addresses transformation capacity at the receiving end. The two are adjacent, not redundant. This standard also backstops the Precision-First Design Standard operationally: precision failures in a coordination approach often become visible only through external challenge, and structural suppression of adverse signals including disconfirmation prevents precision requirements from being operationally enforced regardless of how carefully documents are specified.

# Tensegrity As A Whole

The Coordination Structural Integrity Suite operates as a tensegrity: the Tensegrity Compressive Standards specify structural floors and close exploitation vectors; the Tensegrity Generative Standards specify the enabling conditions under which coordination capacity develops and sustains those floors. This standard is compressive.

```
Coordination Structural Integrity Suite
│
├── Tensegrity Compressive Standards (6)
│   ├── Precision-First Design Standard
│   ├── Adverse Signal Engagement Principle Core Standard     ← this standard
│   ├── Structural Consent Legibility Standard
│   ├── Information Asymmetry Classification Standard
│   ├── Structural Power Obligation Standard
│   └── Regenerative Obligation Standard
│
└── Tensegrity Generative Standards (3)
    ├── Sensemaking Standard
    ├── Four Batteries Capacity Standard
    └── Conflict Transformation Standard
```

Without this standard the suite has no structural requirement for engaging signals that contradict current models. The other compressive standards' governance loops cannot function if adverse signals can be suppressed without detection.

Each standard in the Coordination Structural Integrity Suite is independently adoptable and independently valid. Adopted together, the nine standards address a reinforcing set of structural failure modes that no single standard covers alone. For how the standards combine and what the full suite provides, see the standards README.

# Changelog

v0.7.4 (April 2026): Plain-language preamble added. Two paragraphs inserted before the non-harming formula in Section 1 (Preamble), grounding the standard in the lived experience of the coordination failure it addresses (warning signs that systems do not act on). Navigation pointer added: one sentence pointing to the Suite Integration Guide and the Suite Deployment Contexts document. No changes to normative content.

v0.7.3 (April 2026): Section 2.3 (Detection Reliability Dependency) added. Names the structural reliability dependency on the Relational Battery condition from the Four Batteries Capacity Standard. Specifies that absent Relational Battery instrumentation, audit results carry a systematic false-negative risk and must be disclosed as such. Names joint adoption with Four Batteries as the requirement for trustworthy audit results. No changes to the three invariants or the Notice/Name/Navigate obligations.

v0.7.2 (April 2026): Non-harming opening formula added to Preamble (Section 1). New paragraph at the start of the Preamble specifies the specific harms that absence of a structural adverse signal engagement obligation produces and names adverse signal engagement as the precise structural answer. No changes to normative content.

v0.7.1 (March 2026): Structural root cause assessment requirement added to Section 3.3.3 (Pattern escalation). When a pattern threshold triggers mandatory reclassification, the Navigate phase must now include a structural root cause assessment before individual attribution is accepted as final resolution. The assessment determines whether the recurrent signal class reflects individual failures, a structural condition, or both. Three required findings specified: no structural condition (individual attribution stands), structural condition identified (double-loop examination triggered), or insufficient information (monitoring extended). Accepting individual attribution without this assessment is not permitted. Source: structural blindness Class 13 (Blame Displacement) coverage gap identified in structural blindness protocol stack mapping, March 2026.

v0.7.0 (March 2026): Ostrom DP7 addition. Added Section 3.3.9 (External governance override), specifying external governance interference as a named adverse signal class. A conforming implementation must: name external governance override in its signal taxonomy; treat recognition of the system's self-governance capacity by relevant external authorities as a detection prerequisite; and apply Navigate phase obligations to external governance override signals. The detection prerequisite requires an active recognition assessment, not merely the absence of challenge. The converse failure mode (self-governance claims without recognition assessment at sufficient operational scale) is also specified as a signal class. Added fifth bullet to Section 4.6 (Commons-aligned governance) cross-referencing Section 3.3.9. Together these additions address Ostrom's seventh design principle (minimal recognition of rights to organize) at the standards level. Source: Ostrom gap analysis, March 2026.

v0.6.1 (March 2026): Suite rename ("Coordination Structural Integrity Suite" replaces "Structural Integrity Layer" throughout). Added "Relationship To Other Standards" and "Tensegrity As A Whole" sections, replacing the unnumbered cross-standard section.

v0.6.0 (March 2026): Conflict-class routing added (Section 3.3.1a). "Initiate engagement with contested parties" added to the Navigate action set as a named action for conflict-class signals. Section 3.3.1a specifies: three independently observable conditions that make a signal conflict-class (contested accounts, formal challenge, harm attribution naming a counterparty); the requirement that conflict-class signals must open an engagement pathway before Navigate terminates via escalation or closure; and the explicit scope boundary that the structural conditions for genuine transformation capacity are operational design requirements for the adopting system, not specified by ASEP. No cross-references to other standards. Closes the Corollary 4 (Precision-First Design Standard) deficit at ASEP's Navigate endpoint for conflict-class signals: initiation conditions are now operationally defined and determinable by an independent observer from the coordination record alone.

v0.5.9 (March 2026): Change 3 of anisotropy sequence. Typological declaration (Variant B) added to Section 2.1. Operative classes: epistemic-perceptual (detection/signal processing, precision/operationalization sub-aspects), relational-topological (escalation pathways, response role architecture). Boundary classes: felt-experience, action-structural, temporal-dynamic (frequency-dynamic sub-aspect). Map version v0.1.1 cited.

v0.5.8 (March 2026): Terminology update. "Commitment Standards" renamed to "Tensegrity Compressive Standards" throughout. No normative content changes.

v0.5.7 (March 2026): Citation fixes and stale marker corrections. No normative content changes. (1) Subtitle corrected from v0.5.4 to v0.5.7 (propagation miss from v0.5.5 pass, which corrected to v0.5.4 but not forward). (2) End-of-document marker corrected from v0.5.4 to v0.5.7 (same miss). (3) Section 8.5 bibliographic citation updated from Precision-First Design Standard v1.5.4 to v1.5.6. (4) Section 11 Precision-First inheritance clause updated from v1.5.4 to v1.5.6.

v0.5.6 (March 2026): Section 3.1.2 addition. Fourth implausible absence class added: sustained signal absence coinciding with measurable low Relational battery state (trust gate closure). Extended explanatory paragraph distinguishes this class from the other three: low trust suppresses adverse signal transmission before signals enter the detection architecture, producing a signal-absence reading structurally identical to a healthy-system reading. ASEP detection instruments cannot disambiguate the two alone; Four Batteries state data is required alongside ASEP detection data. Signal absence combined with low trust readings warrants investigation rather than clearance. Source: standards audit against Tensor Primitive Specification v0.2.0 and Four Batteries Capacity Standard v0.2.9, March 26, 2026.

v0.5.5 (March 2026): Pre-release fixes. (1) Subtitle and end-of-document marker corrected from v0.5.3 to v0.5.4 (propagation miss from v0.5.4 pass). (2) Precision-First Design Standard version citation updated from v1.4.8 to v1.5.4 in Section 8.5 and Section 11 inheritance clause. No changes to normative content.

v0.5.4 (March 2026): Coordination Structural Integrity Suite naming propagation. Updated "Relationship to the Structural Integrity Pentad" section heading to "Relationship to the Tensegrity Compressive Standards within the Coordination Structural Integrity Suite." Updated section body: replaced structural integrity pentad designation language with full Tensegrity Compressive Standards designation language throughout; "one of five standalone standards that form the structural integrity pentad" replaced with "one of the five Tensegrity Compressive Standards within the Coordination Structural Integrity Suite." Updated theater prevention clause in inheritance clause accordingly. No changes to normative content.

v0.5.3 (March 2026): Pre-publication check pass. Five fixes: (1) Tier rename survivor corrected in Section 3.3.6: "critical tier" replaced with "ASEP-Instrumented tier"; "Assessed or Operational tiers" replaced with "ASEP-Assessed or ASEP-Operational tiers." (2) Precision-First Design Standard version citation in Section 8.5 updated from v1.2 to v1.4.8. (3) Surviving Proof of Coordination Architecture forward reference removed from end of Relationship to the Structural Integrity Pentad section, completing the v0.5.0 generalization intent; Section 10 PoCA forward reference replaced with a self-contained pointer to the four-element disclosure specification already present in the same document. (4) Window validity requirements added as a named subsection in Section 3.3.6, specifying three conditions for any conforming time window: publicly specified before the window begins running, uniform across structurally equivalent signals, and non-retroactively adjustable. Section 5.4 (ASEP-Accountable) and Section 5.5 (ASEP-Auditable) updated to cross-reference Section 3.3.6 rather than carrying implicit window definitions. (5) Section 11 (Precision-First Design Standard Inheritance Clause) added, declaring this standard at the PFDS-Instrumented tier with rationale for deferred advancement to PFDS-Accountable. No changes to normative content of Sections 1 through 5.3 or 6 through 9.

v0.5.2 (March 2026): Tier 4 and Tier 5 normative content. Replaced Sections 5.4 (ASEP-Accountable) and 5.5 (ASEP-Auditable) placeholders with full normative specifications. ASEP-Accountable requires: every Stage 3 trigger produces a documented governance decision within the defined window (decision record specifying signal, classification, decision, responsible actor, and rationale); automatic Stage 4 publication when no decision is documented within the window, without requiring any actor's initiation; append-only governance decision record; annual tier review including governance loop integrity check. ASEP-Auditable requires all ASEP-Accountable requirements plus: complete Signal Escalation record accessible to an independent auditor without operator cooperation; verifiable completeness (signal generation produces a count or hash against which the record can be checked); verifiable stage integrity (stage transitions consistent with specification); verifiable response completeness (every Stage 3 trigger produced a decision or Stage 4 publication); documented audit reports retained in the governance record; audit reports made available to participant population within a defined period.

v0.5.1 (March 2026): Conformance theater prevention pass. Added Section 10 (Inheritance Clause) with template, commitment statement, and theater prevention clause. Added disclosure specification paragraph to the Relationship to the Structural Integrity Pentad section specifying four required elements for a substantive structural exposure disclosure. No changes to normative content.

v0.5.0 (March 2026): Generalization pass. Removed PoC-specific coupling throughout: removed parenthetical "(Stage 1 in the Proof of Coordination Protocol Specification's implementation)" from Section 3.3.6 Chaotic-domain bypass description; replaced "Tenants, cohorts, or member organizations" and "tenant" language in Section 3.3.8 with "sub-organizations or member bodies" and "member body" throughout; removed "PoC Protocol Specification [1]" from Section 8.4 regulatory precedent cross-reference (Information Asymmetry Classification Standard [A2] is the sufficient citation); updated pentad section to remove reference to "the Proof of Coordination Architecture document" as home for conformance theater architecture, replacing with a self-contained structural exposure disclosure description; corrected "Structural Consent and Legibility Standard" to "Structural Consent Legibility Standard" in Section 3.3.5 cross-reference. No changes to normative content: the three invariants, three-phase processing loop, Signal Escalation architecture, adoption tier requirements, or companion standard relationships are unchanged. Web3 references in domain profiles and bibliography (Sections 7, 8.1, 8.2) are retained as appropriate example-domain citations.

v0.4.9 (March 2026): Tier rename propagation. Renamed three adoption tiers from aware/aligned/critical to Assessed/Operational/Instrumented throughout (Sections 5.0 through 5.3, all inline tier-differentiated guidance, inheritance clause, and changelog references). Added Tier 4 (Accountable) and Tier 5 (Auditable) placeholder sections (5.4 and 5.5) with normative content to be specified in a future session. Added structural integrity pentad section, replacing prior absence of a companion-standard relationship section. Updated End-of-document marker from v0.4.4 to v0.4.8 (was erroneously referencing prior version). No changes to normative content of Sections 1 through 4 or 6 through 8.

v0.4.8 (February 2026): Revised preamble (Section 1). Replaced generic opening with structural-argument framing establishing that the core failure is the absence of a structural obligation to engage with adverse signals, not the inability to detect them. Converted design-property bullet list to inline prose. Pulled core Adverse-Signal Engagement Principle definition into preamble so the reader encounters the principle immediately.

v0.4.7 (February 2026): Added Section 3.3.8 (Early intervention
weighting). Specifies that the cost of addressing an adverse signal
escalates nonlinearly with time, because delayed engagement encounters
compensatory structures and identity fusion that early engagement avoids.
Conforming systems should structure incentives to reward early-stage
engagement; the principle is mechanism-agnostic (applicable to token-
weighted protocols, organizational governance, regulatory frameworks).
Tier-differentiated guidance: Instrumented-tier systems must document early
engagement incentive structures and treat sustained delay as an adverse
signal; Operational-tier systems should document their approach; Assessed-tier
systems are encouraged but not required. Includes tenant/cohort guidance
for propagating early engagement incentives internally. Normative
addition to Section 3. Source: Four Batteries framework (Chapman, Social
Architecture Series Part 1), Hidden Factory cost escalation curve,
dispute resolution domain analysis.

v0.4.6 (February 2026): Added domain-calibrated escalation tempo to
Section 3.3.6. Specifies that escalation timing must match the Cynefin
action mode of the signal's complexity domain. Chaotic-domain priority
jump: Chaotic-domain adverse signals bypass the staged acknowledgment
window and enter the escalation path at the auto-escalation stage,
because the act-sense-respond action mode requires governance visibility
before deliberation is complete. Four sub-requirements specified:
standard path for Clear/Complicated/Complex (a), Chaotic bypass behavior
(b), compressed-not-eliminated stage logic (c), and logged domain
classification (d). Added forward reference in Section 3.3.7 connecting
domain-calibrated navigation (process shape after acknowledgment) to
domain-calibrated escalation tempo (behavior before acknowledgment).
Normative addition to Section 3. Source: Developmental Signal Paper,
Section 5.5; Proof of Coordination Protocol Specification, Signal
Escalation Implementation.

v0.4.5 (February 2026): Renamed "Signal Maturation" to "Signal
Escalation" throughout (Section 3.3.6 heading and body, Section 5
adoption tier references, v0.4.2 changelog entry). The term "maturation"
creates a conceptual collision with the developmental maturation
trajectory defined in the Developmental Signal Paper; "escalation"
describes the mechanism more precisely (unacknowledged signals escalate
through stages of increasing visibility). Source: Developmental Signal
Paper, Section 5.4.

v0.4.4 (February 2026): Added learning loop depth integration to three
sections. Section 3.3.3 (Pattern escalation): identified pattern
escalation as a double-loop learning trigger. Section 3.3.6 (Signal
Maturation): identified the terminal visibility state as a triple-loop
learning trigger. Section 3.3.7 (Domain-calibrated navigation): added
learning loop depth specification per Cynefin domain. Cross-references:
Structural Consent and Legibility Standard, Section 6.4; Coordination
Improvement Proposal Governance, Section 4.

v0.4.3 (February 2026): Added Section 3.3.7 (Domain-calibrated
navigation), specifying that the Navigate process shape should match the
Cynefin action mode appropriate to the signal's complexity domain.
Normative addition to Section 3. Source: Structural Consent and
Legibility Standard, Section 6.4.

v0.4.2 (February 2026): Added Section 3.3.6 (Signal Escalation),
specifying the maturation path for adverse signals not acknowledged
within the time-to-assessment window. The section defines four required
components of a conforming maturation path (acknowledgment window,
auto-escalation threshold, governance obligation trigger, terminal
visibility state) and specifies tier-differentiated implementation
requirements. Normative addition to Section 3.

v0.4.1 (February 2026): Cross-document consistency fixes. Corrected
Information Asymmetry Classification Standard title in Section 9.2
reference \[A2\] to match the document's canonical title. Corrected
Section 8.4 reference from \[A1\] to \[A2\] and replaced shorthand with
full document name. Added changelog. No changes to normative content
(Sections 1--6).

v0.4 (February 2026): Removed session artifacts from document header.
Added numbered bibliography resolving all inline citations. Added
Section 8 (Informative References) covering foundational prior art.
Added Section 9 (Domain Implementations) with bidirectional references
to ASEP-conformant implementations. No changes to the standard's
normative content (Sections 1--6).

v0.3 (February 2026): Prior working version. Established Adverse-Signal
Engagement Principle with three obligations (Notice, Name, Navigate),
three invariants, operational guarantees, Wheel of Consent integration,
Ostrom-aligned governance, and three adoption tiers.
