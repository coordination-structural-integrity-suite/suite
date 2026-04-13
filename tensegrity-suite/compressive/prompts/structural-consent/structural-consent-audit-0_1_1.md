# Structural Consent Legibility Audit
Use when auditing a governance document, participation terms, or consent architecture for the specific ways consent mechanisms fail in practice. Most deployed consent mechanisms — token-weighted voting, delegated authorization, optimistic approval — answer the question "who is acting" but not "who benefits from the action." Shadow dynamics, where one or both answers are obscured, are the mechanism through which extraction operates inside systems that claim participant consent. The prompt finds eight consent legibility failures and returns a failure map with the most extraction-enabling gaps first.

Copy everything below the line, paste it into any AI chat, and attach or paste the governance document, participation terms, or consent architecture you want audited.
---
You are auditing the attached document or system description for consent legibility failures using the Structural Consent Legibility Standard (CC BY 4.0, Regis Chapman). A consent legibility failure is any condition in which a participant cannot determine who is acting, who benefits, what they are specifically consenting to, or whether and how they can withdraw.

The standard requires that every consent-bearing interaction answer two questions: who is acting, and who benefits from the action? Shadow dynamics — where one or both answers are obscured — are the mechanism through which extraction operates inside systems that claim participant consent. Most deployed consent mechanisms (token-weighted voting, delegated authorization, optimistic approval, on-chain permission systems) fail to answer the "who benefits" axis. This audit identifies where those gaps appear.

Check for these eleven consent legibility failures:

1. Action specification gap: the action being consented to is not specified with sufficient precision for affected parties to evaluate whether they are materially affected. "Approving the governance proposal" is not sufficient; "approving the governance proposal that alters fee distribution in the following way" is. Category-level authorization ("the committee is authorized to make fee decisions") used as a substitute for per-action consent without a named trigger condition for standing evaluation fails this requirement. For each instance, identify what precision is missing and what specification would allow standing to be properly assessed.

2. Standing gap: two forms. First, the affected constituency is not identified before a consent-bearing action proceeds. "Affected constituency" means the set of participants whose governance standing, coordination records, data sovereignty, participation terms, or observation exposure would be materially altered by the action. If those parties were not identified before the action, the identification step failed. Note that the implausible absence of standing claims from parties who should be affected is itself a failure. Second, the system has no durable, accessible definition of who holds participation rights and on what basis. Without this definition, per-action identification is performed against an implicit, unspecified reference and is not structurally legible. For each instance found, assess whether: the definition is accessible to any party asserting standing without authority-gating; it cannot be modified unilaterally by parties holding concentrated authority; and it is specific enough that an independent observer can determine whether any given party holds participation rights.

3. Cost-bearing party gap: the party who bears the cost of a consent-bearing action — risk, expenditure, constraint, or negative consequence — is not identified when the cost-bearing party is distinct from both the acting party and the benefiting party. When a governance decision distributes costs to a third party not captured by the who-acts and who-benefits axes, that third party's consent to the cost distribution is required. For each instance, identify the cost-bearing party, what they bear, and whether they have any consent mechanism over the cost distribution.

4. Axis obscuration: the consent mechanism cannot answer both Wheel of Consent questions — who is acting, and who benefits from the action? Any mechanism that conflates these two (e.g., a vote where the voting body also benefits from ratification) has an axis obscuration failure. For each one found, identify which axis is obscured and propose a restructured mechanism that makes both axes visible.

5. Silence treated as consent: the system treats silence, inaction, or absence of objection as authorization without explicit prior opt-in to that interpretation. For each instance, propose language that structurally distinguishes authorized, not-yet-responded, and unable-to-respond.

6. Negotiated limits absent: participants cannot set and maintain explicit boundaries within a consent-bearing interaction. The structural test: can the consenting party specify what they are agreeing to and what is excluded? If the consent mechanism requires accepting all terms or none, negotiated limits are absent. For each instance, propose a scope-bounding mechanism.

7. Bidirectional awareness failure: at least one party in a consent-bearing interaction does not know who is acting and who the action is for. This includes cases where the beneficiary of a governance action is not named, and cases where the party being acted upon does not know the action benefits the acting party. For each one found, identify which axis was not legible to which party and propose a disclosure requirement.

8. Structural non-revocability: the cost of withdrawing consent — exiting, objecting, or refusing — exceeds the benefit of participation. Formal permission to withdraw without a structural mechanism making withdrawal viable is not revocability. For each instance, identify the specific cost that makes withdrawal prohibitive and propose a structural mechanism to reduce or distribute it.

9. Verification gap: the system cannot demonstrate, after the fact, that consent was structurally valid at the time it was given. Verification requires the consent record to identify: who acted, who benefited, who was affected, and what the agreed limits were. If any of these four elements is absent, the verification gap applies. For each one found, propose a durable consent record structure.

10. Consent domain blindness: a single consent mechanism is applied across two or more of the five consent domains — governance (rule changes), data (collection and use), participation (entry terms and exit), output (use of generated signals and scores), observation (what the system monitors) — without domain-specific analysis. Different domains have different beneficiary structures and different stakes for the affected constituency. For each domain conflation found, identify which domains are collapsed and propose domain-specific consent architecture.

11. External legal override undisclosed: external legal requirements applicable to the system's operations — securities law, employment and labor law, data sovereignty mandates, anti-money-laundering obligations — can impose obligations on participants that override explicit consent architecture, but these overrides are not disclosed to participants. Participants believe they have consented only to what is in the governance documents; the legal constraints that can supersede those documents are invisible. For each jurisdiction identified, assess whether the applicable legal obligations are disclosed and whether the organization has specified how it governs the gap between its explicit consent architecture and externally imposed obligations.

For each failure found, list:
- The specific mechanism, clause, or process that fails the condition
- Why it fails (what makes it structurally obscured, absent, or non-legible)
- A concrete proposal for making it structurally legible

Output the results as a consent legibility failure map organized by failure type, with the failures most likely to enable extraction or suppress genuine participant consent first.

Full standard: https://github.com/coordination-structural-integrity-suite/suite
