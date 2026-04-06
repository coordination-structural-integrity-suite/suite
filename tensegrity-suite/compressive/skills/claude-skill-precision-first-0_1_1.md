[claude-skill-precision-first-0_1_0.md](https://github.com/user-attachments/files/25887299/claude-skill-precision-first-0_1_0.md)
# Precision-First Design Standard - SKILL.md

When someone brings you this standard, they have usually encountered a governance instrument that says the right things but does not work when something goes wrong: rules without detection procedures, commitments without operational definitions, accountability without a falsifiable criterion. Their organization may not know yet that precision is the missing piece. Your job is to help them see the gap between what a system says it does and what it structurally does.

## What this skill is for

This skill enables correct reasoning with the Precision-First Design Standard when someone brings it to you. Use it when reviewing documents for precision deficits, evaluating governance or software claims, or explaining what the standard does and does not require.

## The single most important thing to understand

A precision deficit is not the same as being wrong. It is the condition of making a normative claim — a requirement, a rule, a classification — in a form that cannot be evaluated by an independent observer without access to a privileged interpreter. "This process is fair" is a precision deficit. "This process weights input by demonstrated coordination capacity, measured by the calculation in Section 3" is not.

This matters because unfalsifiable claims cannot carry architectural weight. A governance system built on unfalsifiable foundations cannot detect when it is failing, because failure is not operationally defined.

## What the standard requires

The standard specifies nine corollaries to the core precision requirement. The core is: every element of a governed system must increase the precision with which the system's dynamics can be observed, classified, and acted upon.

Nine specific requirements follow from this:

1. Every term in a normative claim has an operational definition an independent observer can apply without access to the author.
2. Each rule specifies a detection procedure by which an independent observer can identify a violation.
3. Each taxonomy or classification system specifies a procedure for handling edge cases outside all existing categories.
4. Each detection mechanism specifies what signals it would not produce — its false-negative boundary.
5. Each process specifies operational conditions for initiation, continuation, and conclusion; no step depends on discretion without criteria.
6. Each normative term expressing a value judgment (fair, reasonable, transparent) is decomposed into independently evaluable conditions.
7. Governance inaction in the presence of a detection output is itself detectable without the cooperation of the inacting party.
8. Critical properties depend on multiple structurally distinct mechanisms, not a single defensive mechanism.
9. Assessment architectures require a contextual baseline statement before initial assessment when identical measurement outputs would indicate structurally distinct conditions requiring different responses. A detection system that classifies without a declared reference baseline has a precision deficit in the instrument itself: correct readings for one condition produce incorrect response prescriptions for another. This requirement also applies at the adoption layer: a normative mechanism adopted from a different structural context requires a baseline statement specifying origin-context conditions, adopting-context conditions, and either a congruence confirmation or calibration adjustments. A mechanism deployed without this statement carries an undocumented assumption that origin-context structural conditions obtain in the implementing context; when that assumption is false, the mechanism produces neither detectable violations nor detectable compliance.

## What the standard does not require

It does not require exhaustive documentation. It requires that what is documented be operational. A one-sentence rule with a clear detection procedure meets the standard. A twenty-page policy with no detection procedures does not.

It does not require certainty. It requires falsifiability: a claim structured so that evidence could disconfirm it.

It does not specify governance outcomes. It specifies how outcomes must be described for them to be architecturally meaningful.

## Common misreadings to avoid

**Treating it as a style guide.** The standard does not say to write clearly. It says normative claims must be structured so that violations can be detected without privileged interpretation. These are different requirements.

**Treating precision as completeness.** The precision requirement governs whether a claim is falsifiable, not whether it is comprehensive. A claim can be precise and narrow. The width of coverage is a separate concern.

**Treating it as hostile to judgment.** The standard constrains where judgment operates; it does not eliminate judgment. At the boundary of any classification system, judgment is necessary. The standard requires that the boundary be specified so that judgment at the boundary is legible rather than invisible.

**Treating compliance theater as compliance.** The failure mode the standard is specifically designed to prevent is the performance of operational precision without its substance: taxonomies that look complete but have no edge-case procedure, detection mechanisms that produce outputs but have no governance response requirement, assessments that are structured but measure against unspecified baselines.

## The key evaluation question

When evaluating any claim, rule, process, or taxonomy: can an independent observer determine whether this requirement has been met without access to the person who wrote it? If not, the standard is not met. Then ask: if the observer can make that determination, is the structural mechanism that produces the claimed outcome specified? If the claim is only about the outcome and not the mechanism, the standard is not met.
