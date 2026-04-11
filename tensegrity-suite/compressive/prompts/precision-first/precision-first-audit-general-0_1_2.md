# General Precision Audit
Use when a governance document, standard, rulebook, or technical specification might be claiming more certainty or enforceability than it delivers — or when you want to know whether its normative claims can actually be applied by someone who wasn't in the room when they were written. The prompt finds terms that can't be independently verified, processes that depend on discretionary judgment at critical steps, and detection mechanisms that wouldn't catch violations. It returns a precision deficit map with the most consequential gaps first.

Copy everything below the line, paste it into any AI chat, and attach or paste the document you want audited.
---
You are auditing the attached document for precision deficits using the Precision-First Design Standard (CC BY 4.0, Regis Chapman). A precision deficit is a normative claim without an operational specification: a term, rule, or requirement that cannot be evaluated by an independent observer using only the document and observable evidence.

Audit the document against these nine criteria:

1. Is every term that appears in a normative claim, condition, or classification defined operationally, without reference to a privileged interpreter?
2. For each rule, is there a specified procedure by which a violation can be detected by an independent observer?
3. For each taxonomy or classification system, is there a specified procedure for handling edge cases that fall outside all existing categories?
4. For each detection instrument, is there an explicit specification of what signals it would not produce, to establish its false-negative boundary?
5. For each process, are the conditions for initiation, continuation, and conclusion operationally defined, or does the process depend on discretion at any step?
6. For each normative term (fair, reasonable, transparent, ethical, and any other term expressing a value judgment or quality assessment not determinable by observable evidence alone), is there a typed decomposition that replaces the term with independently evaluable conditions?
7. For each detection mechanism, is governance inaction in the presence of a detection output itself detectable without the cooperation of the inacting party?
8. For each critical property, does the specification depend on a single defensive mechanism, or are there independent, structurally distinct mechanisms such that the failure of any single one is detectable by the others?
9. For each assessment or detection output, does the assessment architecture require a contextual baseline statement before initial assessment when identical measurement outputs would indicate structurally distinct conditions requiring different responses? A detection system that records signals against an unspecified reference baseline has a precision deficit in the instrument itself: correct readings for one condition produce incorrect response prescriptions for the other. Also: for each normative mechanism adopted from a different structural context, does the document provide a baseline statement specifying the structural conditions the mechanism was designed and applied in, the structural conditions of the adopting context, and either a confirmation of congruence or a specification of calibration adjustments? A mechanism deployed without this statement carries an undocumented assumption that origin-context conditions obtain in the implementing context.

For each criterion, list:
- The specific term, rule, or process that fails the criterion
- Why it fails (what makes it vague, discretionary, or unfalsifiable)
- A concrete suggestion for making it operationally precise

Output the results as a precision deficit map: a structured list organized by criterion, with the most consequential deficits first.

Full standard: https://github.com/coordination-structural-integrity-suite/suite
