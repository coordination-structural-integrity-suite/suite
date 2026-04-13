# General Precision Audit
Use when a governance document, standard, rulebook, or technical specification might be claiming more certainty or enforceability than it delivers — or when you want to know whether its normative claims can actually be applied by someone who wasn't in the room when they were written. The prompt finds terms that can't be independently verified, processes that depend on discretionary judgment at critical steps, and detection mechanisms that wouldn't catch violations. It also finds the opposite failure: requirements specified so tightly that the coordination purpose they were designed to serve becomes unreachable. It returns a precision map with the most consequential gaps first.

Copy everything below the line, paste it into any AI chat, and attach or paste the document you want audited.
---
You are auditing the attached document using the Precision-First Design Standard (CC BY 4.0, Regis Chapman). Precision fails in two directions: a precision deficit is a normative claim without an operational specification, a term, rule, or requirement that cannot be evaluated by an independent observer using only the document and observable evidence. A precision imposition is a normative element specified so completely that compliance can be demonstrated while the coordination purpose the element was designed to serve remains unserved. Both are precision failures requiring correction.

Audit the document against these nine criteria. Each criterion runs in two directions: the floor condition asks whether the document under-specifies; the ceiling condition asks whether it over-specifies in a way that makes the criterion formally satisfied but the underlying purpose unreachable.

1. Operational definitions. Floor: Is every term that appears in a normative claim defined operationally, without reference to a privileged interpreter? Ceiling: Does any definition achieve independent determinability by narrowing what counts as the phenomenon, excluding real instances of what the definition was built to identify?

2. Violation detection. Floor: For each rule, is there a specified procedure by which a violation can be detected by an independent observer? Ceiling: Does any detection taxonomy create more categories than the phenomenon has distinguishable states, or require classification before the required information is available?

3. Edge case handling. Floor: For each taxonomy or classification system, is there a specified procedure for handling edge cases that fall outside all existing categories? Ceiling: Does any classification instrument eliminate false positives by narrowing its target state so far that it systematically misses what it was designed to find?

4. False-negative boundary. Floor: For each detection instrument, is there an explicit specification of what signals it would not produce, to establish its false-negative boundary? Ceiling: Is any process so elaborate that it cannot be completed by the parties it was designed to protect, even when every formal condition is met?

5. Process conditions. Floor: For each process, are the conditions for initiation, continuation, and conclusion operationally defined, or does the process depend on discretion at any step without criteria? Ceiling: Does any escalation mechanism fire on ordinary variation rather than on violation, producing outputs so frequently that they become indistinguishable from background noise?

6. Value judgment decomposition. Floor: For each normative term expressing a value judgment (fair, reasonable, transparent, ethical, or any quality not determinable by observable evidence alone), is there a decomposition into independently evaluable conditions? Ceiling: Do any overlapping defensive mechanisms contradict each other, generate false violation readings, or make operating the system structurally unachievable?

7. Inaction detectability. Floor: For each detection mechanism, is governance inaction in the presence of a detection output itself detectable without the cooperation of the inacting party? Ceiling: Is any challenge or correction pathway specified with so many procedural steps that no independent actor can realistically complete it, formally present but structurally inaccessible?

8. Multiple distinct mechanisms. Floor: For each critical property, does the specification depend on multiple structurally distinct mechanisms rather than a single defensive mechanism? Ceiling: Does any typological declaration claim operative coverage beyond what the vocabulary supports, generating conformance expectations the document cannot meet?

9. Contextual baseline. Floor: For each assessment or detection output, does the architecture require a contextual baseline statement before initial assessment when identical measurement outputs would indicate structurally distinct conditions requiring different responses? Also: for each normative mechanism adopted from a different structural context, does the document provide a baseline statement specifying origin-context conditions, adopting-context conditions, and either a congruence confirmation or calibration adjustments? Ceiling: Does any baseline requirement impose conditions that cannot be established in time for the detection it is meant to enable, or whose conditions no real case can satisfy, making the baseline itself the obstacle to what it was designed to make possible?

For each criterion, list:
- The specific term, rule, or process that fails the criterion
- The direction of failure (floor or ceiling) and why
- A concrete suggestion for correcting in the direction that serves the coordination purpose

Output the results as a precision map: a structured list organized by criterion, with the most consequential failures first. Label each finding as a precision deficit (under-specification) or precision imposition (over-specification) so the corrective direction is clear. For each finding, look to what the document itself says about its affected population. Where the document names the parties it is designed to protect or serve, use that identification to note who cannot invoke protection (precision deficit) or who cannot access the coordination purpose (precision imposition). Where the document does not identify its affected parties, note the absence as a structural observation rather than a gap to supply independently: a document whose affected parties cannot be identified from within it cannot be assessed for whether it serves or fails them.

Full standard: https://github.com/coordination-structural-integrity-suite/suite
