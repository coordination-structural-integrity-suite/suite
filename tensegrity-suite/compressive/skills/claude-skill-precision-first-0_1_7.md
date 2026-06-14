# Precision-First Design Standard - SKILL.md

When someone brings you this standard, they have usually encountered a coordination instrument that says the right things but does not work when something goes wrong: rules without detection procedures, commitments without operational definitions, obligation loop closure without a falsifiable criterion. Their organization may not know yet that precision is the missing piece. Your job is to help them see the gap between what a system says it does and what it structurally does.

## What this skill is for

This skill enables correct reasoning with the Precision-First Design Standard when someone brings it to you. Use it when reviewing documents for precision deficits, evaluating governance or software claims, or explaining what the standard does and does not require.

## The single most important thing to understand

Precision in a coordination instrument fails in two directions. A precision deficit occurs when a normative claim is made without an operational specification: a term, rule, or requirement that cannot be evaluated by an independent observer using only the document and observable evidence. "This process is fair" is a precision deficit. A precision imposition occurs when an element is specified so completely that compliance can be demonstrated while the coordination purpose remains unserved. Both are precision failures requiring correction.

This matters because unfalsifiable claims cannot carry architectural weight, and because compliance that does not serve the coordination purpose is worse than useless: it closes off the channel for correction by making the failure look like success.

Precision and non-harming are one commitment at the specification layer. An instrument that under-specifies harms the people it was designed to protect by leaving exploitation vectors permanently open. An instrument that over-specifies harms differently: it makes the coordination purpose unreachable for the people it was designed to serve. These are two aspects of one commitment, not two separate concerns to be balanced against each other.

## Method-Structure Congruence: the prior condition

The precision-first invariant tests the artifact: can violations be detected, and does compliance demonstrate the coordination purpose is being served? A prior condition applies to how the artifact was produced: the epistemic method used must match the structural character of what is being known at that stage. This is not a preference for one reasoning mode over another. It is a precision condition on the act of knowing itself.

This matters because of the self-concealing property of congruence deficits. When an instrument is built using a method weaker than the structure requires, the output is internally coherent and systematically blind to content the congruent method would have generated. No internal check can surface the gap, because the gap is the absence of content that was never produced. A specification built by enumerating observed instances, where structural analysis of causal relationships was required, will pass all ten corollary checks on the content it contains while being structurally blind to adversarial conditions and causal relationships not present in the observational premises.

Two failure directions. A congruence deficit occurs when an epistemically weaker method is applied where a stronger one is required: the output is complete within the method's terms but structurally blind to what the congruent method would have found; the absence leaves no gap marker. A congruence imposition occurs when a method more demanding than warranted is applied: the output acquires structural depth that reflects the method's requirements rather than the phenomenon's character, producing false precision. The success condition: the weakest method sufficient to generate the content the stage requires.

The relationship to the precision-first invariant: they are not redundant. The invariant tests whether the artifact's claims are falsifiable and whether compliance serves the coordination purpose. Congruence tests whether the method used was capable of generating the content the stage required. An artifact can be fully precision-compliant within the content it contains while failing congruence because the content was selected by the method's limits rather than by the structural character of the problem.

When reviewing an instrument: apply the congruence check first. What structural character does this stage have, and was the method used capable of generating content that matches that character? Then apply the precision-first invariant to the content the congruent method would have produced.

## What the standard requires

The standard specifies ten corollaries to the core precision requirement. The core is the double negation: precision fails when violations are undetectable (precision deficit) or when compliance can be demonstrated while the coordination purpose remains unserved (precision imposition). The requirement is met when violations are detectable and compliance can demonstrate that the coordination purpose is being served.

Ten specific requirements follow from this. Each requirement runs in two directions: a floor condition (what under-specification fails to prevent) and a ceiling condition (what over-specification produces). The floor conditions are listed here; the ceiling conditions are in Section 2 of the standard, paired immediately after each floor condition.

1. Every term in a normative claim has an operational definition an independent observer can apply without access to the author. Ceiling: a definition that achieves independent determinability by narrowing what counts as the phenomenon rather than specifying it has missed real instances of what it was built to detect.
2. Each rule specifies a detection procedure by which an independent observer can identify a violation. Ceiling: a taxonomy that creates more categories than the phenomenon has distinguishable states, or demands classification before the required information exists, forces real cases into boxes that do not fit.
3. Each taxonomy or classification system specifies a procedure for handling edge cases outside all existing categories. Ceiling: a detection instrument can eliminate every false positive by narrowing its target state, and in doing so systematically miss what it was designed to find.
4. Each detection mechanism specifies what signals it would not produce (its false-negative boundary). Ceiling: a governance process too elaborate to use fails the parties who need it, even if every condition is formally met.
5. Each process specifies operational conditions for initiation, continuation, and conclusion; no step depends on discretion without criteria. Ceiling: an escalation mechanism that fires on ordinary variation in timing becomes background noise, indistinguishable from a system that is simply running hot.
6. Each normative term expressing a value judgment (fair, reasonable, transparent) is decomposed into independently evaluable conditions. Ceiling: too many overlapping defensive mechanisms contradict each other, generate false violation readings, or make operating the system structurally unachievable.
7. Governance inaction in the presence of a detection output is itself detectable without the cooperation of the inacting party. Ceiling: a challenge pathway requiring so many procedural steps that no independent actor can complete it exists formally while remaining structurally inaccessible.
8. Critical properties depend on multiple structurally distinct mechanisms, not a single defensive mechanism. Ceiling: a typological declaration that claims operative coverage beyond what the vocabulary supports generates conformance expectations the document cannot meet.
9. Assessment architectures require a contextual baseline statement before initial assessment when identical measurement outputs would indicate structurally distinct conditions requiring different responses. A detection system that classifies without a declared reference baseline has a precision deficit in the instrument itself: correct readings for one condition produce incorrect response prescriptions for another. This requirement also applies at the adoption layer: a normative mechanism adopted from a different structural context requires a baseline statement specifying origin-context conditions, adopting-context conditions, and either a congruence confirmation or calibration adjustments. A mechanism deployed without this statement carries an undocumented assumption that origin-context structural conditions obtain in the implementing context; when that assumption is false, the mechanism produces neither detectable violations nor detectable compliance. Ceiling: a baseline requirement that cannot be established in time for the detection it is meant to enable, or whose conditions no real case can satisfy, has become the obstacle to what it was supposed to make possible.
10. An evaluation claim is grounded only when the type of object the claim is about has been declared: either a criterion (a directly observable property, or a property with an established external validation standard) or a construct (an abstract property not directly observable, requiring systematization and proxy specification before measurement can proceed). For construct claims, operational grounding requires a nomological network declaration naming the sub-constructs, the observable criteria that proxy for each, and the expected relationships between them. Coverage adequacy applies to both claim types: the evidence must address the case space the claim requires, not merely declare the evaluation's scope limits. Ceiling: a nomological network requirement that demands complete documentation of all construct relationships before any are established blocks construct-based evaluation entirely; a declared-partial nomological network naming what is established and explicitly identifying the gaps is in a better precision state than an undeclared or absent one, and is the correct operating state when the network is under development.

## What the standard does not require

It does not require exhaustive documentation. It requires that what is documented be operational. A one-sentence rule with a clear detection procedure meets the standard. A twenty-page policy with no detection procedures does not.

It does not require certainty. It requires falsifiability: a claim structured so that evidence could disconfirm it.

It does not specify governance outcomes. It specifies how outcomes must be described for them to be architecturally meaningful.

## Scope boundary: subjective experience vs. structural accessibility

Whether a specification feels fair, transparent, or well-designed to those who use it is outside this standard's vocabulary. Subjective quality experience is not a precision question.

Whether a specification is structurally accessible to the parties it was designed to protect is not outside scope. A specification so procedurally demanding that those parties cannot invoke its protections fails the precision imposition corollary; it is an over-specification failure in the ceiling direction. The test is structural, not experiential: can the parties the instrument was designed to protect actually invoke its protections, or does formal compliance exist while that access is structurally unavailable?

This boundary is easy to misread. "Navigable" and "fair" appear similar. The distinction is: subjective navigation experience is outside scope; structural access to protection is inside scope, evaluated as a ceiling condition.

## Common misreadings to avoid

**Treating precision deficit as the only failure direction.** Over-specification is an equal failure. A system can demonstrate formal compliance with all ten corollaries while the coordination purpose the instrument was designed to serve remains unreachable for the people it was supposed to protect. If an organization can show it followed every procedure while those procedures were supposed to protect had no access to the protection, the standard is not met.

**Treating it as a style guide.** The standard does not say to write clearly. It says normative claims must be structured so that violations can be detected without privileged interpretation. These are different requirements.

**Treating precision as completeness.** The precision requirement governs whether a claim is falsifiable, not whether it is comprehensive. A claim can be precise and narrow. The width of coverage is a separate concern.

**Treating it as hostile to judgment.** The standard constrains where judgment operates; it does not eliminate judgment. At the boundary of any classification system, judgment is necessary. The standard requires that the boundary be specified so that judgment at the boundary is legible rather than invisible.

**Treating compliance theater as compliance.** The failure mode the standard is specifically designed to prevent is the performance of operational precision without its substance: taxonomies that look complete but have no edge-case procedure, detection mechanisms that produce outputs but have no governance response requirement, assessments that are structured but measure against unspecified baselines.

## The key evaluation question

When evaluating any claim, rule, process, or taxonomy: can an independent observer determine whether this requirement has been met without access to the person who wrote it? If not, the standard is not met. Then ask: if the observer can make that determination, is the structural mechanism that produces the claimed outcome specified? If the claim is only about the outcome and not the mechanism, the standard is not met.

## Completing a finding: the harm-naming obligation

The transclusion principle (that precision and non-harming are one commitment) has a direct implication for how audit findings are completed.

A finding that identifies a structural gap but does not name who bears the cost of that gap has not yet served the audit's purpose. The gap is the structural fact. The harm is what makes it matter.

For a precision deficit finding: after identifying the structural gap (vague term, missing detection procedure, unspecified process), look to what the document itself says about its affected population. Where the document names the parties it is designed to protect, use that identification to note who cannot invoke protection and what they cannot do as a result. Where the document does not identify its affected parties, note the absence as a structural observation: a document whose affected parties cannot be identified from within it cannot be assessed for whether it serves or fails them.

For a precision imposition finding: after identifying the over-specified element, apply the same approach. Where the document names the parties it is designed to serve, note for whom the coordination purpose becomes unreachable and in what way. Where it does not, note the absence.

This is not an additional audit criterion. It is what converts a structural checklist into a precision audit. An auditor who can identify every structural gap but cannot name any harmed parties has demonstrated procedural completion without serving the purpose that procedural completion is meant to serve.

## Corpus evolution: invoke the transclusion check first

When applying this standard in the context of a corpus evolution question (a new requirement, new standard element, new framework section, or new document being proposed), the transclusion check is a prior obligation. Before asking whether a proposed addition is precision-complete, ask: is there a frame at which an existing element is already true, such that the original precision and the new requirement are both fully operative within it as distinct instantiations, with neither requiring the other to diminish? If yes, the transclusion is the correct move and no new element is needed. If no such frame exists, a new element is the correct answer; and then precision-first applies to that new element.

The standalone transclusion skill (`claude-skill-transclusion-0_1_1.md`) provides the full implementation: the prior differentiation check, the test for whether transclusion has occurred, the two failure modes (false separation and false merger), the nondual ground, and worked examples from the corpus. The pointer here is not a re-specification; it is a sequencing instruction. Transclusion check comes before precision audit in corpus evolution contexts.

## Non-harming dimension in derived requirements

When a precision requirement is derived from this standard for use in another instrument, the non-harming dimension of the unified PFDS principle must be explicitly stated within the derived element itself. Citing the invariant or pointing back to this standard does not satisfy the requirement.

A derived element from which the harmed parties cannot be identified without consulting the foundational principle has been derived from the precision dimension only. The non-harming dimension is operative in a derived element only when the specific cost-bearing parties are named within the element, including which parties bear the cost of each failure direction.

This is distinct from the harm-naming obligation in audit findings. The audit context asks you to use the document under review's own identification of its affected population, after the fact of a gap finding. The derivation context requires that you build the non-harming dimension into the derived element at the point of derivation, before any gap finding occurs.

The consequence-calibrated evidence bar is a direct implication of this for evaluation chain specifications. When the precision-first invariant is applied to the design of an evaluation chain, the non-harming aspect of the unified principle requires that the evidence bar for any claim scale to the harm potential of acting on a false or misleading version of that claim. A specification that applies a fixed evidence bar regardless of consequence level has operationalized the precision dimension in isolation; the unified non-harming dimension is inoperative unless the required evidence stringency, the independence of the validating party, and the adversarial testing intensity all scale to the harm that a false claim could cause. The claim's consequence level and its evidence bar must both be declared within the derived element.

---

## Changelog

| Version | Date | Changes |
|---------|------|---------|
| 0.1.7 | 2026-05-28 | Corollary 10 (Claim-Object Grounding) added to the requirements list: criterion vs. construct distinction; nomological network declaration required for construct claims; coverage adequacy for both claim types; ceiling addresses declared-partial nomological networks as valid operating state. Consequence-calibrated evidence bar added to non-harming dimension section: evidence bar must scale to harm potential of acting on a false claim; a fixed evidence bar regardless of consequence level operationalizes precision in isolation without the unified non-harming dimension operative. Method-Structure Congruence section updated to reference "ten corollary checks." Follows PFDS v2.3.0. |
| 0.1.6 | 2026-05-28 | Method-Structure Congruence section added: prior condition to the precision-first invariant; congruence tests the process that produced the artifact; two failure directions (congruence deficit is self-concealing; congruence imposition produces false precision); success condition is weakest sufficient method. Non-harming dimension in derived requirements section added: derived elements must name the non-harming dimension and specific cost-bearing parties within the element itself; pointing back to the invariant does not satisfy the requirement. Follows PFDS v2.2.0. |
| 0.1.5 | 2026-04-17 | Scope boundary section added: distinguishes subjective experience of quality (outside scope) from structural accessibility of protection (inside scope, ceiling direction). Follows PFDS v2.1.7 boundary class correction. |
| 0.1.4 | 2026-04-13 | Frame Language pass: opening line updated from "governance instrument" to "coordination instrument" and "accountability without a falsifiable criterion" to "obligation loop closure without a falsifiable criterion." Follows PFDS v2.1.1 Frame Language pass. |
| 0.1.3 | 2026-04-13 | Nine ceiling conditions added to the requirements list, one paired with each floor condition. Intro sentence before the nine requirements updated to name the two-direction structure. Follows PFDS v2.1.0, which added nine ceiling corollaries to Section 2. |
| 0.1.2 | 2026-04-13 | Added corpus evolution section: pointer to transclusion skill as prior check before precision audit in corpus evolution contexts. |
| 0.1.1 | 2026-04-13 | Harm-naming obligation section added: completing a finding requires naming who bears the cost of the gap, using the document's own identification of its affected population. |
| 0.1.0 | 2026-04-13 | Initial skill file. |
